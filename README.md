# Alternative Dropbox Account

Repo to use to set up another Dropbox account on your MacOS based system.

## App Directory

Create App Directory:

```
mkdir -p ~/DropboxAltStarter.app/Contents/MacOS/
```

## System File

Use the example in repo or add file  `Info.plist` inside `DropboxAltStarter.app/Contents` with content:

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
    <key>CFBundlePackageType</key>
    <string>APPL</string>
    <key>CFBundleExecutable</key>
    <string>DropboxAltStarter</string>
    <key>LSUIElement</key>
    <string>1</string>
</dict>
</plist>
```

## Starter Script


Add file `DropboxAltStarter` (without any extension) in the folder `DropboxAltStarter.app/Contents/MacOS` with this content or use repo example:

```
#!/bin/bash
 HOME=/Users/$USER/.dropbox-alt /Applications/Dropbox.app/Contents/MacOS/Dropbox
 ```

## Permissions

To
Set rights for application to run properly

```
chmod 755 ~/DropboxAltStarter.app/Contents/MacOS/DropboxAltStarter
```

## Source

This repo is based on tutorial by Damien's blog [maketecheasier](https://www.maketecheasier.com/run-multiple-dropbox-accounts-in-mac-and-linux/)
