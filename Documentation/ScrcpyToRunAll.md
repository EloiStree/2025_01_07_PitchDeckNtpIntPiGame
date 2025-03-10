

1. **Download Scrcpy for Windows**:
   - Go to [Scrcpy GitHub Repository](https://github.com/Genymobile/scrcpy) and download the latest version of Scrcpy for Windows.

2. **Clone the required repositories**:
   - Open your terminal or command prompt and run the following commands to clone the necessary repositories into specific directories:
     ```sh
     git clone https://github.com/EloiStree/2024_05_23_SCRCPYBatFiles.git BatFiles
     git clone https://github.com/EloiStree/2025_01_12_BuildAndRunApkBroadcast.git BuildAndRunAll
     ```

3. **Create the APK**:
   - Build your game APK and place it in the `BuildAndRunAll/Build` directory. Name the file `YourGame.apk`.

4. **Run the Python script**:
   - Navigate to the `BuildAndRunAll` directory and execute the script `BuildAndRunApkToAllUSB.py` to build and run the APK on all connected USB devices:
     ```sh
     python BuildAndRunApkToAllUSB.py
     ```
