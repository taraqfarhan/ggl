# ggl : Search google from the terminal (and many more)

This is an another life-changing python script to automate a process which will prolly save your 5-10 seconds of your time.
Of course, you as a programmer need this kinda productivity. You don't need to thank me. If you really insist, I won't mind tho.

You can search:

- google even with a specific Google Chrome profile (if you're using Google Chrome)
- google images and videos
- youtube
- github, stack overflow
- wikipedia
- duckduckgo
- gmail

And you can also :
- prompt chatgpt
- email (texts only) to someone from the terminal (using gmail) (coming soon)
- open browser in incognito mode (if you're using chrome)

# Usage

```
For every web-browsers
ggl <search query>
ggl [-im|--img|--image] <search query>
ggl [-v|--vid|--video] <search query>
ggl [-y|-yt|--youtube] <search query>
ggl [-cg|--gpt|--chatgpt] <your prompt>
ggl [-w|--wiki|--wikipedia] <search query>
ggl [-g|-gh|--git|--github] <search query>
ggl [-s|-st|--stack|--stackoverflow] <search query>
ggl [-d|--ddg|--duckduckgo] <search query>
ggl [-gm|--gmail] [search query] 
ggl [-h|--help]
ggl [--mail|--send-mail] <receiver's address> [your text]

The following command are only for Google Chrome
ggl [-i|--incog|--incongnito] [search query]
ggl [-p|--profile <profile name>] [search query]
ggl [-l|--list]


For every web-browsers
-im --img --image                   show the image section for the search
-v --vid --video                    show the video section from the search
-y -yt --youtube                    search the youtube
-cg --gpt --chatgpt                 prompt chatgpt
-w --wiki --wikipedia               search the wiki
-g -gh --git --github               search the github
-s -st --stack --stackoverflow      search stack-overflow
-d --ddg --duckduckgo               search duckduckgo search engine instead of google
-h --help                           display this help page
-gm --gmail                         search your mail with that search-query
--mail --send-mail                  send mail to someone with their mail address
                                    

Only for Google Chrome
-i --incog --incognito              open Google Chrome in incognito mode
-p --profile                        set a specific chrome profile for searching
-l --list                           list all the chrome profiles


EXAMPLES:
ggl why programmers hate everyone
ggl "What's the capital of Russia"
ggl 'What does the word "retarded" mean'
ggl --img a flycatcher
ggl --video how to learn to code
ggl -yt stuxnet documentary
ggl -w computer science terminologies
ggl --git taraqfarhan/ggl
ggl -s "what language is used to write unix commands"
ggl --ddg why duckduckgo is better than google
ggl --gmail contract proposal
ggl --chatgpt why we should even bother about the command line interface
ggl --send-mail taraqfarhan@gmail.com send me the docs asap

Specific to Google Chrome only
ggl -p 3 online train ticket
ggl --profile business How does money work?
ggl -p guest how to use the dark web
ggl -i -p "Profile 3" "build linux kernel from the scratch"
ggl -i why bitcoin is illegal in some countries
```

# How to use script this on your own machine
Just clone this repo and run the python script. Ofc you'll need python3 installed on your machine first to run a python script duh!
This software isn't completed fully yet. After finishing, I will add this to Homebrew so that mac and linux users can install this software just using 
```sh
brew install ggl
```

# Configuration (for a specific Google Chrome profile)

> IF AND ONLY IF YOU WANT TO USE THE -p --profile FLAG (which is specific to Google Chrome only), YOU NEED TO CONFIGURE THE config.json FILE, OTHERWISE YOU'RE GOOD TO GO. YOU DON'T NEED ANY CONFIGURATIONS (YOU CAN SKIP THIS SECTION COMPLETELY)
> THIS SCRIPT WAS INITIALLY WRITTEN FOR MACOS. YOU SHOULD CONFIGURE THE 'config.json' FILE PROPERY TO USE THIS SCRIPT IN ANY OPERATING SYSTEM. OTHERWISE YOU MIGHT GET UNEXPECTED ERROR MESSAGES.

A config.json file will be created if you run this scipt for the first time. You will find that configuration file in:

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
