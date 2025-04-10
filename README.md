## Macos CLI Application Launcher
Simple shell script launcher for macOS using fzf with mdfind (Spotlight).

<img width="476" alt="Screenshot 2025-04-08 at 11 27 00" src="https://github.com/user-attachments/assets/350892d7-e8aa-4857-9318-0218e8245401" />

## installation
```
chmod +x fzf-launcher && sudo cp fzf-launcher /usr/local/bin/fzf-launcher
```
For realtime update you need to add a system watcher which will watch for new clip system message and execute this command. `Curl` is from hombrew on my setup, it may mater.
```
curl -XPOST "localhost:6265" -d 'reload(sqlite-utils "$HOME/Library/Application Support/BetterTouchTool/BTTClipboardManager_20241210.sqlite" "select Z_PK, ZPREVIEWTEXT from ZBTTCLIP" | jq -r --raw-output0 ".[].ZPREVIEWTEXT")'
```
## Dependencies
[file-icon-cli](https://github.com/sindresorhus/file-icon-cli) for icon conversion and imgcat for actual previews

