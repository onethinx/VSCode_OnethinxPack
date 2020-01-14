# Onethinx Core MAC OS-X dependencies pack

## How to setup Visual Studio Code with the Onethinx Core dependencies pack

## 1. Download prerequisites
- **VS Code**
    - [Download Visual Studio Code](https://code.visualstudio.com/download)
- **Onethinx Dependencies Pack**
    - [Download the Onethinx dependencies pack for Mac OS](https://github.com/onethinx/VSCode_OnethinxPack_macOS)
- **CMake**
    - [Download CMake](https://cmake.org/download/)
- **Make**
    - Install homebrew GNU by: `make brew install homebrew/core/make` as [explained here](https://apple.stackexchange.com/questions/261918/how-to-upgrade-gnu-make-in-os-x-el-capitan).
## 2. Install CMake, VS Code & extensions
  - Install CMake.
  - Install VS Code.
  - Install extensions:
    - ARM Support For Visual Studio Code (dan-c-underwood)
    - C/C++ IntelliSense, debugging (microsoft)
    - CMake language support (twxs)
    - CMake Tools (microsoft)
    - Cortex-Debug GDB support (marus25)
    - LinkerScript support for GNU (Zixuan Wang)
    - Open in Application (Fabio Spampinato)
    - Output Colorizer (IBM)
    - Tasks (actboy168)
  - Apply the CMake path to VS Settings: `"cmake.cmakePath": "/Applications/CMake.app/Contents/bin/cmake",`
## 3. Install the Onethinx Dependencies Pack
  - Put this pack on your local harddisk (eg: /Applications/VSCode_OnethinxPack_Windows).
  - If the file ~.bash_profile doesn't exist, create it: Terminal >> `cd ~ && touch .bash_profile`
  - Open ~.bash_profile: Terminal >> `cd ~ && open -e .bash_profile` 
  - Add this to the end of the file (make sure you enter the correct path) and save:
    ```
    # Loading environment variables for the Onethinx Pack
    source /locationOfYour/VSCode_OnethinxPack_macOS/variables.env
    ```
  - Set the correct path in this pack's `variables.env` file.
  - Restart your machine (or log-out and log-in) to reload the environment variables.
## 4. Check
  - If Make and the compiler is correctly installed by typing the following into your terminal or terminal window of VS Code.
    - `make -v`
    - `arm-none-eabi-gcc -v`
## 5. Remind
  - After changing the device configuration (or project file structure) to use
    - Clean Reconfigure
    - Clean Rebuild
       in order to build the image properly  
  - To delete the contents of the build folder
    - if you copied the project including build folder from another location / machine
    - when build fails.
