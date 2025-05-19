# ggl : common google searches from the command line

This is another life-changing tool to automate a process which will prolly save your 5-10 seconds of your time. Of course, you as a programmer need this kinda productivity. You don't need to thank me.

- google stuffs (even with a specific profile if you're using Google Chrome, Chromium or Brave Browser)
- search in incognito mode
- google images and videos
- search youtube videos
- prompt chatgpt, gemini
- github repos, stack overflow
- wikipedia pages
- search with duckduckgo
- search your gmail inbox
- prompt to send emails (texts only) to someone from the terminal (using gmail)

# Usage

```
ggl [-p profile] [-i | --incog] [options] <query|prompt>
ggl [--mail address [--sub subject]] <text>
ggl [-h | --config]

Options:
   -im --img             show the image section for the search
   -v --vid              show the video section from the search
   -y -yt                search the youtube
   -c --gpt              prompt chatgpt
   -g --gem              prompt gemini
   -w --wiki             search the wiki
   -gh --git             search the github
   -s -st --stack        search stack-overflow
   -d --ddg              search with duckduckgo instead of google

For emails (gmail)
   -gm --gmail           search your mail with that search-query
   --mail                prompt to send mail to someone with their mail address
   --sub                 option for --mail flag to add a subject (optional)

Only for Chrome/Chromium/Brave Browser
   -p                    set a specific chrome profile for searching
   -l --list             list all the chrome profiles
   -i --incog            open Google Chrome in incognito mode

helper options:
   -h --help             display the help page
   --config              open the config file

EXAMPLES:

ggl why programmers hate everyone
ggl "What's the capital of Russia"
ggl 'What does the word "retarded" mean'
ggl -yt stuxnet documentary
ggl --img a flycatcher
ggl --vid how to learn to code
ggl -w computer science terminologies
ggl --git taraqfarhan/ggl
ggl --stack "what language was used to write unix commands"
ggl --ddg why duckduckgo is better than google
ggl --gpt why we should even bother about the command line interface

Mail (gmail)
ggl --gmail contract proposal
ggl --send-mail taraqfarhan@gmail.com send me the docs asap
ggl --mail taraqfarhan@gmail.com --sub "Assignment Submission" submit your assignment by tomorrow

Specific to Chromimum Based Browsers (Google Chrome, Chromium, Brave) only
ggl -p 3 --img chess board
ggl -p business -yt "How does money work?"
ggl -p guest how to use the dark web
ggl -i -p "Profile 3" "build linux kernel from the scratch"
ggl -i why bitcoin is illegal in some countries
```

# How to use this script on your own machine

I will recommend you to use `Google Chrome` (Chromium or Brave) on your machine as your default browser to get the most out of this tool. If Google Chrome (Chromium, Brave) is installed on your machine, `ggl` will use Google Chrome (Chromium, Brave) for browsing, otherwise `ggl` will use your Default Browser.

Anyway, to use this script just clone this repo using

```bash
git clone https://www.github.com/taraqfarhan/ggl
```

Then run this python script. Ofc you'll need `python3` installed on your machine first to run a python script duh!

```bash
python3 /path/to/ggl  # mac/linux (like: python3 ggl -h)
py /path/to/ggl  # windows (like: py ggl -h)
```


<details markdown='1'><summary>To run `ggl` globally without specifying `python3 /path/to/ggl or py path/to/ggl` each time (like the EXAMPLES) refer to this section</summary>


##### THIS SECTION IS FOR THOSE WHO WANT TO RUN IT GLOBALLY, ANYWHERE FROM THE TERMINAL. OTHERWISE, YOU'LL HAVE TO EXPLICITLY SPECIFY THE PATH OF THE SCRIPT EACH TIME

```bash
python3 path/to/the/ggl/script  # mac/linux
py path/to/the/ggl/script  # windows
```

### Follow any of the following processes

## Process 1 (mac/linux)

Creating alias
```bash
echo "alias ggl='python3 $(pwd)/ggl'" >> ~/.zshrc && source ~/.zshrc  # from the ggl folder
```

## Process 2 (mac/linux)

Creating a symbolic link
```bash
sudo ln -s $(pwd)/ggl /usr/bin/ggl  # from the ggl folder

# you can choose any directory which is in the PATH instead of /usr/bin/
# use the follwoing command to get all the environment variable paths 
echo $PATH | tr ':' '\n'
```

## Process 3 (mac/linux/windows)

Environment Variables

#### mac/linux
```bash
echo "export PATH='$PATH:$(pwd)'" >> ~/.zshrc && source ~/.zshrc  # from the ggl folder
```

#### Windows

1. Open **Environment Variables**:

   - Press `Win + S`, search for **Environment Variables**, and click **Edit the system environment variables**.
   - In the **System Properties** window, click **Environment Variables**.

2. Add the Directory to PATH:

   - Under **System Variables** or **User Variables**, find `Path` and click **Edit**.
   - Add your directory where you have `ggl` file


</details>

# Configuration (for searching with specific profiles)

> IF AND ONLY IF YOU WANT TO USE (flags that are specific to Google Chrome, Chromium & Brave only), YOU NEED TO CONFIGURE THE config.json FILE, OTHERWISE YOU'RE GOOD TO GO. YOU DON'T NEED ANY CONFIGURATIONS (YOU CAN SKIP THIS SECTION COMPLETELY)
> YOU SHOULD CONFIGURE THE 'config.json' FILE PROPERY TO USE THIS SCRIPT IN ANY OPERATING SYSTEM. OTHERWISE YOU MIGHT GET UNEXPECTED ERROR MESSAGES.

A **config.json** file will be created automatically if you run this scipt for the first time. You need to configure that **config.json** file. Read the **COMMENTS** from the config file to follow along

1. Set the values (your own customized value) of the keys (Profiles) according to your own needs.
2. Then set the Google Chrome or Chromium or Brave Browser's path. Check the path on your computer and set the path to the **config.json** file if needed. These browsers are usually in:

```
1. mac: inside /Application/ or ~/Application/
      /Applications/Google Chrome.app (for Google Chrome)
      /Application/Chromium.app (for Chromium)
      /Application/Brave Browser.app (for Brave)
2. linux: inside /usr/bin/ (usually in this /usr/bin/ directory, check other bin directories if not found)
      /usr/bin/chrome (for google chrome)
      /usr/bin/chromium (for chromium)
      /usr/bin/brave (or /usr/bin/brave-browser for brave)
3. windows: usually in one of these directories:
      %ProgramFiles%\Google\Chrome\Application\chrome.exe
      %ProgramFiles(x86)%\Google\Chrome\Application\chrome.exe
      %LocalAppData%\Google\Chrome\Application\chrome.exe
```

### How to Find Your Browser's Profile Names

```
1. mac: inside ~/Library/Application Support/
   ~/Library/Application Support/Google/Chrome/ (for Chrome)
   ~/Library/Application Support/Chromium/ (for Chromium)
   ~/Library/Application Support/BraveSoftware/Brave-Browser (for Brave)
2. linux: inside ~/.config/
   ~/.config/google-chrome/ (for google chrome)
   ~/.config/chromium (for chromium)
   ~/.config/BraveSoftware/ (for Brave)
3. windows: C:\Users\YourUserName\AppData\Local\Google\Chrome\User Data\
```

Inspect the Directory. Match the folder name with the corresponding Chrome profile.

```
1. Default: The main profile.
2. Profile 1, Profile 2, ... Profile <some number> : Additional profiles.
```

# Caveats (Only for Windows)

- In **Windows** you can use `ggl` for Google Chrome Profiles only (not for Chromium and Brave)
- In **Windows** while prompting to send email if you use quotes in subject (after --sub) or text (at the end) you might face problems
- These issues will be fixed soon