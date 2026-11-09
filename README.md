# Axon

Downloads for the Axon browser. Get the latest version from **[Releases](https://github.com/kevingiscold/axon-releases/releases/latest)**.

- **Windows:** `Axon-Setup-<version>.exe`. If SmartScreen appears, click *More info → Run anyway*.
- **Mac:** paste this into Terminal. It picks Apple Silicon or Intel, replaces any older Axon, and clears the "app is damaged" block that macOS shows for apps not signed by Apple:

```bash
A=$(uname -m | sed 's/x86_64/x64/'); curl -fL -o /tmp/Axon.dmg "https://github.com/kevingiscold/axon-releases/releases/latest/download/Axon-mac-$A.dmg" && osascript -e 'quit app "Axon"' 2>/dev/null; hdiutil attach -nobrowse -quiet /tmp/Axon.dmg -mountpoint /Volumes/AxonInstall && rm -rf /Applications/Axon.app && cp -R /Volumes/AxonInstall/Axon.app /Applications/ && hdiutil detach -quiet /Volumes/AxonInstall && xattr -cr /Applications/Axon.app && open /Applications/Axon.app
```

- **Linux:** `Axon-linux-x64.AppImage`. Make it executable (`chmod +x`) and run it.
