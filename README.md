# Dependencies

- Python
- grim - for taking screenshots
- slurp - for selecting screen areas
- requests - for making HTTP requests

# Install requests with pip 
```bash
pip install requests
```

## For other dependencies:

**On Arch** 
```bash
sudo pacman -S grim jq slurp
```

**On Debian/Ubuntu based systems** 
```bash
sudo apt update \
sudo apt install grim jq slurp
```
```bash
sudo apt install grim jq slurp
```

**On Fedora based systems** 
```bash
sudo dnf install grim jq slurp
```

**On Gentoo systems**
```bash
sudo emerge -av gui-apps/grim gui-apps/slurp app-misc/jq
```

# Usage

In order to use this script, enter the following commands into the terminal:

```bash
git clone https://github.com/RobinTT69/e-z-screenshot-linux
```

```bash
cd e-z-screenshot-grim-linux
```

**Choose the file that correlates to your use case. If you are using x11 use the one called e-z-flameshot-xll.py, if you are using wayland, and want to use flameshot, use the one thats called e-z-flameshot.py, and if you do not want to use flameshot and are on wayland, use the e-z-grim.py file! It comes with great support across desktop environments and window managers like Hyprland.**

**OPTIONS:**
- -a, --api-key: Enter API key | Only required once unless you wish to update it
- -d, --domain: Enter the domain to be used (check below for setup, if this does not apply to you dont incude this)
- -s, --save-dir: Directory to save the screenshot
- -f, --full-screen: Capture full screen instead of a selected area (does not work in x11 script, workaround is to simply select the entire area in flameshot gui)
- -v, --verbose: Enable verbose logging for debugging (does not work in x11 script)

# Locating your API key

- Go to Account Settings

![image](https://i.e-z.host/pics/m9j6jk3a.png)

- Click 'Copy API Key'

![image](https://i.e-z.host/pics/inmghmtw.png)

# Using your own custom domain

If you are interested in using a custom domain, but are not interested in changing nameservers to the E-Z ones, do the following: 

## Domain Setup On Cloudflare 
![image](https://r2.e-z.host/ca19848c-de8c-4cae-9a10-858d6fd864b7/joyc6m3h.jpeg)

You have to also make a dns record

![image](https://r2.e-z.host/8a13052f-8c12-4034-b99f-0155cc616583/f5jrvtyn.png)

Make sure its the subdomain you want, as well as making it point to any valid local IPv4 address (for example purposes, we used 192.0.0.2). 

It also **HAS** to be proxied.

- Now go back to the directory where your script is and do ./SCRIPT-NAME.py -d https://sub.domain.tld/

# Troubleshooting
- **The python script doesnt work! It doesnt embed the images!** 
To fix this go back to the cloudflare rule you made. Tick the box that says "Preserve query string". Also, purge all cache if you have any. Now try the embed.

- **I need to change my domain! I need to change my api key!**
Run the script and this time add the -a and -d arguements, just like you did the first time you used the script.

# Credits
Credits and huge thanks to https://github.com/KeiranScript for being a contributor who helps me maintain this project as well as adding the  custom domain functionality in the scripts.
