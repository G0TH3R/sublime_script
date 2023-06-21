# Title: sublime_script
Author: G0TH3R
 
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


Copyright 2021 G0TH3R

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program. If not, see http://www.gnu.org/licenses/.
