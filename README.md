# ggl : Search google with a specific Google Chrome profile right from the terminal

Another life-changing script to automate a process which will save you prolly 3 to 5 seconds of your time. Of course, you as a programmer need this kinda productivity. You don't need to thank me. If you really insist you can always email me at taraqfarhan@gmail.com

## Configuration

Place the config.json File in the Correct Location (specified below). Manually place the config.json file if needed. You have to place your config.json file in:

1. **macOS/linux**: ~/.config/ggl/config.json
2. **Windows**: %APPDATA%\ggl\config.json

After setting the **config.json** file in correct location specified above, you need to configure the **config.json** file.

1. Set the values (your own customized value) of the keys (Chrome Profiles) according to your own needs.
2. Then set the Google Chrome's path. Check the path for Google Chrome on your computer and set the path to the **config.json** file if needed.

## How to Find Your Google Chrome Profile Names

Locate Chrome’s User Data Directory:
1. **macOS**: ~/Library/Application Support/Google/Chrome/
2. **Linux**: ~/.config/google-chrome/
3. **Windows**: C:\Users\YourUserName\AppData\Local\Google\Chrome\User Data\

Inspect the Directory. Match the folder name with the corresponding Chrome profile.
1. **Default**: The main profile.
2. **Profile 1, Profile 2, etc.**: Additional profiles.
