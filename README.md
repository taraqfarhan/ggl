# ggl : Search google with a specific Google Chrome profile right from the terminal

Another life-changing script to automate a process which will save you prolly 3 to 5 seconds of your time. Of course, you as a programmer need this kinda productivity. You don't need to thank me. If you really insist you can always email me at taraqfarhan@gmail.com

# Usage
```sh
ggl [-p|--profile <profile name>] <search query>
ggl [-l|--list]
ggl [-h|--help]
        

-p --profile        set a specific chrome profile for searching 
-l --list           list all the chrome profiles
-h --help           display this help page

EXAMPLES:
ggl why programmers are so unhappy
ggl "What's the capital of Russia"
ggl 'What does the word "retarded" mean'
ggl -p 3 python programming for beginners
ggl --profile business How does money work?
ggl -p guest how to use the dark web
```
## Configuration

Place the config.json File in the Correct Location (specified below). Manually place the config.json file if needed. You have to place your config.json file in:
```sh
1. **macOS/linux**: ~/.config/ggl/config.json
2. **Windows**: %APPDATA%\ggl\config.json
```

After setting the **config.json** file in correct location specified above, you need to configure the **config.json** file.

1. Set the values (your own customized value) of the keys (Chrome Profiles) according to your own needs.
2. Then set the Google Chrome's path. Check the path for Google Chrome on your computer and set the path to the **config.json** file if needed.

> THIS SCRIPT IS INITIALLY WRITTEN FOR MACOS, YOU SHOULD CONFIGURE THE 'config.json' FILE PROPERY, OTHERWISE YOU MIGHT GET UNEXPECTED ERROR MESSAGES

## How to Find Your Google Chrome Profile Names

Locate Chrome’s User Data Directory:
```
1. **macOS**: ~/Library/Application Support/Google/Chrome/
2. **Linux**: ~/.config/google-chrome/
3. **Windows**: C:\Users\YourUserName\AppData\Local\Google\Chrome\User Data\
```

Inspect the Directory. Match the folder name with the corresponding Chrome profile.
```
1. **Default**: The main profile.
2. **Profile 1, Profile 2, etc.**: Additional profiles.
```
