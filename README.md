# sublime_script
 
>[!info] Simple script to download and install sublime
> Works with a Debian based installation and apt as your package manager.


### Step 1: Copy the script to the target system

```bash
#!/bin/bash

sudo apt update && sudo apt upgrade
wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/sublimehq-archive.gpg > /dev/null

echo "deb https://download.sublimetext.com/ apt/stable/" | sudo tee /etc/apt/sources.list.d/sublime-text.list
deb https://download.sublimetext.com/ apt/stable/

sudo apt update
sudo apt-get install sublime-text

subl --version
```

### Step 2: Make the script executable

```bash
chmod +x sublime_script
```

### Step 3: Execute the script
```bash
sudo ./sublime_script
