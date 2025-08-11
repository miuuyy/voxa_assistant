CONTRIBUTING TO VOXA

Voxa is a Tauri application designed for Windows, utilizing a sidecar process for its backend. This guide will help you set up the project locally, test existing features, and build your own executable changes.

PROJECT STRUCTURE:
- `src-tauri`: Contains the Tauri application files (Rust backend for the UI).
- `voxa-backend`: Contains the Python-based sidecar process files.
- `src`: Contains the Tauri frontend (HTML, CSS, JavaScript).
  - `src/index.html`: The main HTML file for the Tauri frontend.
  - `src/assets`: Contains logos and other assets.

GETTING STARTED (Local Testing):

To test the existing application locally:

1. Navigate to the `src-tauri` directory in your terminal:
   `cd src-tauri`

2. Clean the Cargo build artifacts (recommended for a fresh build):
   `cargo clean`

3. Run the Tauri application in development mode:
   `npm run tauri dev`
   OR
   Build the Tauri application (this will create the installer later):
   `npm run tauri build`

BUILDING YOUR OWN EXECUTABLE (Modifying the Python Backend):

If you've made changes to the Python backend scripts and want to build a new executable:

1. Navigate to the `voxa-backend` directory in your terminal:
   `cd voxa-backend`

2. Ensure you have the necessary Python dependencies installed. You can install them using the `requirements.txt` file:
   `pip install -r requirements.txt`

3. After making your script changes, build the new executable using PyInstaller:
   `pyinstaller --clean voxa-backend.spec`
   The `voxa-backend.spec` file in this directory is the PyInstaller configuration file.

4. Once the build is complete, locate the new executable in the `voxa-backend/dist` folder.

5. **Crucially**, move this newly built executable from `voxa-backend/dist` to the `src-tauri` directory, replacing the existing sidecar executable there.

6. After replacing the executable, you can test it locally as described in the "GETTING STARTED" section (i.e., `npm run tauri dev` or `npm run tauri build` from `src-tauri`).

INSTALLER GENERATION:

Upon a successful `npm run tauri build` from the `src-tauri` directory, the installer for the application will be generated and can be found in:
`src-tauri/target/release/bundle`

---
