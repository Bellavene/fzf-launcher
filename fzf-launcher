#!/usr/bin/env python3
import sys
import os
from pyfzf import FzfPrompt

OS = sys.platform
if OS == 'darwin':
    APP_DIR = '/Applications'
    APP_DIR_SYSTEM = '/System/Applications'
    APP_DIR_USER = '/Users/Klutchevski/Applications'
    subfolders = [f.path for f in os.scandir(APP_DIR) if f.is_dir()]
    subfolders_system = [f.path for f in os.scandir(APP_DIR_SYSTEM) if f.is_dir()]
    subfolders_user = [f.path for f in os.scandir(APP_DIR_USER) if f.is_dir()]
    all_apps = subfolders + subfolders_system + subfolders_user

    fzf = FzfPrompt()
    item = fzf.prompt(all_apps)
    APP_PATH = ''.join(item)
    APP_PATH_SPACE = ""

    if ' ' in APP_PATH:
        for ch in APP_PATH:
            if ch == ' ':
                APP_PATH_SPACE += ("\\" + ch)
            else:
                APP_PATH_SPACE += ch
        if item:
            print(f"Opening {item}")
            os.system(f"/usr/bin/open {APP_PATH_SPACE}")
    else:
        if item:
            print(f"Opening {item}")
            os.system(f"/usr/bin/open {APP_PATH}")
else:
    print("Invalid OS")
    exit(1)
