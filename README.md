# Cli-app-launcher
Simple python cli app launcher for macOS using fzf.
# Install requirements
```
brew install fzf
pip install -r requirements.txt
```
# Run the app
```
python main.py
```

# Running as script
```
1. Script uses: /opt/homebrew/bin/python3 as interpreter
    if you use default python, change the path to: 
    /opt/homebrew/bin/python3 -> /usr/bin/python3
2. Give execute persmission to file:
    chmod +x main.py
3. Move it local bin directory, in order to execute it system-wide make sure this directory is in $PATH

```
```
sudo cp main.py /usr/local/bin/name-you-want
For example:
sudo cp main.py /usr/local/bin/sf
shell> sf
```

