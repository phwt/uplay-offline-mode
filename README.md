# Uplay Invisible Mode

Add Invisible mode for your Uplay client.

## Features

- **Invisibility** Appear as offline to your friends but still be able to access in-game online services.

Disabled Features
- Friend List (including invitation to game)
- News Section, Store

## How it works?

The application will block the connection of `upc.exe` which transmit your online status to your friends. Your game connection will not be affected as this only blocks Uplay Client connection.

## Set-up

#### [Download the latest release here](https://github.com/phwt/uplay-invisible-mode/releases)

### 1. Extract ALL files from .zip file

You will extract some files and folders including `upcinvisible.exe` file.

### 2. Run `upcinvisible.exe` with admin rights

The application will prompt you to select `upc.exe` from your Uplay installation folder (Default path: `C:\Program Files (x86)\Ubisoft\Ubisoft Game Launcher\upc.exe`) and Windows Firewall Outbound rule "Uplay Invisible Mode" will be created.

### 3. Finish!

The application will close and you are now ready to use.

## How to use

### 1. Run `upcinvisible.exe` with admin rights and launch Uplay client

You will see like this in the application do not enable it yet.

    Status: Disabled
    [Enable]
    
**In this phase you will still appear online to your friends**

### 2. Start the game and click `Enable` to enable invisible mode

Simply just click **Play** button at your game. **Do not enable until the `Synchronization with the cloud` dialog disappear** after that you can click on `Enable`.

**This will not instantly offline your Uplay status. It may took about minute or half for you to completely appear offline to your friends.**

### 3. Enjoy!

You can check if it working or not by noticing Error appear at bottom, Friend list appear as `Connecting...` and Store inaccessible.

![Example](https://raw.githubusercontent.com/phwt/uplay-offline-mode/master/offline_example.jpg)

If all this applies you are now completely invisible. Enjoy!

### 4. Disabling

When you have finished your game. Quit the game and click on `Disable` button (Like when enabling you will not immidiately online). After your Uplay client has established connection with the server. You can now sync your progress with the cloud.

## Built-With

- Python `3.7`
  - tkinter `8.6`
  - pyinstaller `3.4`

## Development setup

Install required library

    pip install PyInstaller

### Directory Structure
- `upcinvisible.py` - Application's main file
- `uplay_icon.ico` - Application's icon file

### Build
Build the application using `pyinstaller`

    pyinstaller --noconsole --icon=uplay_icon.ico upcinvisible.py

You will find your files at `/dist/upcinvisible`
