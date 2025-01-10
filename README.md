# ggl : Search the web from the terminal (and much more)

This is another life-changing python script to automate a process which will prolly save your 5-10 seconds of your time. Of course, you as a programmer need this kinda productivity. You don't need to thank me. If you really insist, I won't mind tho.

You can search :

- google stuffs (even with a specific Google Chrome profile: if you're using Google Chrome)
- google images and videos
- browse chrome in incognito mode (if you're using chrome)
- youtube
- github, stack overflow
- wikipedia
- duckduckgo
- gmail

And you can also :

- prompt chatgpt, gemini
- prompt to send emails (texts only) to someone from the terminal (using gmail)

# Usage

```
For every web-browsers
ggl <search query>
ggl [-im|--img|--image] <search query>
ggl [-v|--vid|--video] <search query>
ggl [-y|-yt|--youtube] <search query>
ggl [-cg|--gpt|--chatgpt] <your prompt>
ggl [--gem|--gemini] <your prompt>
ggl [-w|--wiki|--wikipedia] <search query>
ggl [-g|-gh|--git|--github] <search query>
ggl [-s|-st|--stack|--stackoverflow] <search query>
ggl [-d|--ddg|--duckduckgo] <search query>
ggl [-gm|--gmail] [search query]
ggl [--mail|--send-mail] <receiver's address> [--sub|--subject] [your text]
ggl [-h|--help]

The following command are only for Google Chrome
ggl [-i|--incog|--incongnito] [search query]
ggl [-p|--profile <profile name>] [search query]
ggl [-l|--list]


For every web-browsers
-h --help                         display this help page

-im --img --image                 show the image section for the search
-v --vid --video                  show the video section from the search
-y -yt --youtube                  search the youtube
-cg --gpt --chatgpt               prompt chatgpt
--gem --gemini                    prompt gemini
-w --wiki --wikipedia             search the wiki
-g -gh --git --github             search the github
-s -st --stack --stackoverflow    search stack-overflow
-d --ddg --duckduckgo             search duckduckgo search engine instead of google

For emails (gmail)
-gm --gmail                       search your mail with that search-query
--mail --send-mail                prompt to send mail to someone with their mail address
--sub --subject                   option for --mail --send-mail flag to add a subject (optional)

Only for Google Chrome
-i --incog --incognito            open Google Chrome in incognito mode
-p --profile                      set a specific chrome profile for searching
-l --list                         list all the chrome profiles


EXAMPLES:

For any web-browser 
ggl why programmers hate everyone
ggl "What's the capital of Russia"
ggl 'What does the word "retarded" mean'
ggl -yt stuxnet documentary
ggl --img a flycatcher
ggl --video how to learn to code
ggl -w computer science terminologies
ggl --git taraqfarhan/ggl
ggl --stack "what language is used to write unix commands"
ggl --ddg why duckduckgo is better than google
ggl --chatgpt why we should even bother about the command line interface

Mail (gmail)
ggl --gmail contract proposal
ggl --send-mail taraqfarhan@gmail.com send me the docs asap
ggl --mail taraqfarhan@gmail.com --sub "Assignment Submission" submit your assignment by tomorrow

Specific to Google Chrome only
ggl -p 3 online train ticket
ggl --profile business How does money work?
ggl -p guest how to use the dark web
ggl -i -p "Profile 3" "build linux kernel from the scratch"
ggl -i why bitcoin is illegal in some countries
```

# How to use this script on your own machine

I will recommend you to use ```Google Chrome``` on your machine as your default browser to get the most out of this tool. If Google Chrome is installed on your machine, ```ggl``` will use Google Chrome for browsing, otherwise ```ggl``` will use your Default Browser.

Anyway, to use this script Just clone this repo using 
```bash
git clone https://www.github.com/taraqfarhan/ggl
``` 
Then run this python script. Ofc you'll need ```python3``` installed on your machine first to run a python script duh! 

# Homebrew installation (for macOS/linux) (coming soon)

```ggl``` will be added to ```Homebrew``` soon. Then, for ```macOS``` and ```linux``` you can install ```ggl``` using

```bash
brew install ggl
```

# To use a python script globally (RECOMMENDED)
> THIS SECTION IS FOR THOSE WHO WANT TO RUN IT GLOBALLY FROM THE TERMINAL. OTHERWISE, YOU'LL HAVE TO EXPLICITLY SPECIFY THE PATH OF THE SCRIPT EACH TIME
```bash
python3 path/to/the/ggl/script (for macOS/linux)
python path/to/the/ggl/script (windows)
```

To use a Python script globally (i.e., you can execute it from anywhere in the terminal) on ```Windows```, ```macOS```, and ```Linux```, you need to ensure the script is accessible from your system's PATH and possibly make it executable.

### **Step 1: Place Your Script in a Directory**
Move the script (`ggl`) to a directory accessible to the PATH. Common locations:
- **macOS/Linux**: Use `/usr/local/bin`, `~/bin`, or another directory in your PATH.
- **Windows**: A folder like `C:\Scripts` or a directory already in the PATH (e.g., `C:\Python\Scripts`).

To create a new directory for scripts:
For macOS/linux:
```bash
mkdir -p ~/bin
```

For Windows, manually create a folder, e.g., `C:\Scripts`.


### **Step 2: Add the Script Directory to PATH**
If the directory containing your script is not already in the PATH, you need to add it.

#### **macOS/Linux**
1. Edit your shell configuration file:
   - For **bash**: `~/.bashrc`
   - For **zsh**: `~/.zshrc`
   - For **fish**: `~/.config/fish/config.fish`

2. Add the following line:
   ```bash
   export PATH="$PATH:~/bin"
   ```

3. Save the file and reload it:
   ```bash
   source ~/.bashrc (for bash)
   source ~/.zshrc (for zsh)
   source ~/.config/fish/config.fish (for fish)
   ```

#### **Windows**
1. Open **Environment Variables**:
   - Press `Win + S`, search for **Environment Variables**, and click **Edit the system environment variables**.
   - In the **System Properties** window, click **Environment Variables**.

2. Add the Directory to PATH:
   - Under **System Variables** or **User Variables**, find `Path` and click **Edit**.
   - Add your directory (e.g., `C:\Scripts`).

3. Save and restart your terminal.


### **Step 3: Make the Script Executable** (if needed)
#### **Linux/macOS**
Make the script executable:
   ```bash
   sudo chmod +x ~/bin/ggl
   ```

#### **Windows**
No need to make the script executable explicitly. 
But You might need to rename the script from ggl to ggl.py (if needed). Check the following steps to learn more.

### **Step 4: Testing**
Run the script in a terminal to verify it works globally.

**macOS/Linux**:
Open a new terminal and type:
   ```bash
   ggl 
   ```
**windows**:
Open Command Prompt or Windows Powershell and try 
   ```cmd
   ggl
   ggl.py
   python ggl
   python ggl.py
   python replace/this/with/your/path/to/ggl
   ```
  

# Configuration (for a specific Google Chrome profile)

> IF AND ONLY IF YOU WANT TO USE (flags that are specific to Google Chrome only), YOU NEED TO CONFIGURE THE config.json FILE, OTHERWISE YOU'RE GOOD TO GO. YOU DON'T NEED ANY CONFIGURATIONS (YOU CAN SKIP THIS SECTION COMPLETELY)
> YOU SHOULD CONFIGURE THE 'config.json' FILE PROPERY TO USE THIS SCRIPT IN ANY OPERATING SYSTEM. OTHERWISE YOU MIGHT GET UNEXPECTED ERROR MESSAGES.

A **config.json** file will be created automatically if you run this scipt for the first time. You will find that configuration file in:

```
1. macOS/linux: ~/.config/ggl/config.json
2. Windows: %APPDATA%\ggl\config.json
```

Now, you need to configure this **config.json** file.

1. Set the values (your own customized value) of the keys (Chrome Profiles) according to your own needs.
2. (if needed) Then set the Google Chrome's path. Check the path for Google Chrome on your computer and set the path to the **config.json** file if needed.

### How to Find Your Google Chrome Profile Names

Locate Chrome’s User Data Directory:

```
1. macOS: ~/Library/Application Support/Google/Chrome/
2. Linux: ~/.config/google-chrome/
3. Windows: C:\Users\YourUserName\AppData\Local\Google\Chrome\User Data\
```

Inspect the Directory. Match the folder name with the corresponding Chrome profile.

```
1. Default: The main profile.
2. Profile 1, Profile 2, etc.: Additional profiles.
```
