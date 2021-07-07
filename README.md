# alternative-dropbox-account

Create App Directory:

```
mkdir -p ~/DropboxAltStarter.app/Contents/MacOS/
```

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

Add file `DropboxAltStarter` (without any extension) in the folder `DropboxAltStarter.app/Contents/MacOS` with this content or use repo example:

```
#!/bin/bash
 HOME=/Users/$USER/.dropbox-alt /Applications/Dropbox.app/Contents/MacOS/Dropbox
 ```

To
Set rights for application to run properly

```
chmod 755 ~/DropboxAltStarter.app/Contents/MacOS/DropboxAltStarter
```


This repo is based on [tutorial by Damine](https://www.maketecheasier.com/run-multiple-dropbox-accounts-in-mac-and-linux/)
