------------------------------------------------------------------------------------------------------------------------------------------------------------------

# This guide contains info on how to setup your web development enviroment. 

## In this guide I cover:

-How to install Homebrew

-How to install necessary Packages & useful Applications

-How to install Oh-My-Zsh

-How to install Spaceship Prompt Theme for your Terminal

-How to add aliases & nvm to .zshrc

-How to change Visual Studio Font & Settings

-How to set up Node with nvm

-How to set up Eslint + Prettier with Airbnb Style Guide

-How to generate SSH key and add it to your github account

-And I added some useful Visual Studio Code extensions


# Disclaimer:

# All information provided in this guide is for general informational purposes only. You agree that you use such information entirely at your own risk. Under no circumstances will I be held responsible or liable in any way for any claims, damages, losses, expenses, costs or liabilities whatsoever (including, without limitation, any direct or indirect damages for loss of profits, business interruption or loss of information) resulting or arising directly or indirectly from your use of or inability to use this manual. 

# This guide is dumbed done to my granny's level. So if you mess your machine up, you must be a talented genius 😂

------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 1. Downlod dev-setup-scripts.zip

### click on link to download dev-setup-scripts.zip,download should begin automatically

https://github.com/eliasbnk/dev-setup/blob/main/dev-setup-scripts.zip?raw=true

------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 2. Setting Up Download Scripts

type the following into Terminal: 
 
 ```
cd /Users/`whoami`/Downloads/dev-setup-scripts
 ```
 
### [press Enter]


------------------------------------------------------------------------------------------------------------------------------------------------------------------
type the following into Terminal: 

```
ls
```

### [press Enter]

## click on ok/allow

------------------------------------------------------------------------------------------------------------------------------------------------------------------
## Terminal should return something similiar
------------------------------------------------------------------------------------------------------------------------------------------------------------------

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/ls.png)


## Compare this list to what Terminal returned (if you are in dev-setup-scripts folder you should have all of these files)

- brew-install-cask.txt

- brew-install.txt

- extensions.txt

- vscode-extension-install.sh

- vscode-settings.txt

- zshrc.txt
------------------------------------------------------------------------------------------------------------------------------------------------------------------
# If you indeed have all those files skip over to step 3. Installing Homebrew
------------------------------------------------------------------------------------------------------------------------------------------------------------------
# if your Terminal didn't return that or you dont have those files do the following
------------------------------------------------------------------------------------------------------------------------------------------------------------------

### [press command + SPACE]

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/spotlight.png)

in Spotlight type:

```
dev-setup-scripts
```
### [press Enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------
## Finder should open where dev-setup-scripts folder has been downloded
------------------------------------------------------------------------------------------------------------------------------------------------------------------

## click on dev-setup-scripts folder

### &

### [press command + C]

------------------------------------------------------------------------------------------------------------------------------------------------------------------
# go back into Terminal
------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into Terminal: 

```
cd
```

### [press Space]

### &

### [press command + V]

## it should like somthing like this

cd /Users/{YOUR_USERNAME}/{FOLDER_NAME_THE_FILE_IS_IN}/dev-setup-scripts

## if it does great, if not redownload the dev-setup-scripts.zip file into Downloads folder and repeat step 2 from beginning.

### [press Enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------
## you should now be in dev-setup-scripts folder
------------------------------------------------------------------------------------------------------------------------------------------------------------------
type the following into Terminal: 

```
ls
```
------------------------------------------------------------------------------------------------------------------------------------------------------------------
## Terminal should Return something similiar
------------------------------------------------------------------------------------------------------------------------------------------------------------------

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/ls.png)

------------------------------------------------------------------------------------------------------------------------------------------------------------------
# If Terminal still doesnt return this repeat step 2 from beginning again.
------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 3. Installing Homebrew

to download Homebrew you need paste the following link into Terminal:

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### [press Enter]

### &

## if prompted to enter your Password, enter your Password, after entering your Password [press Enter]   

# after a little while Terminal will prompt you "to continue with downloading Homebrew press return" = [press Enter] 

------------------------------------------------------------------------------------------------------------------------------------------------------------------

Wait patiently as this may takes a while (install can take around 4-5 minutes).🧐

After a little awhile Homebrew should be installed. 😊

------------------------------------------------------------------------------------------------------------------------------------------------------------------
# only continue to step 4 after Homebrew is installed 
------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 4.Installing Packages & Applications

type the following into Terminal: 

```
brew tap homebrew/cask-fonts
brew install $(<brew-install-cask.txt)
brew install $(<brew-install.txt)
```

### [press Enter]

### if prompted to input your Password, after inputing your Password [press Enter]  

------------------------------------------------------------------------------------------------------------------------------------------------------------------

Wait patiently as this may takes a while.🧐

After a little awhile all Packages & Applications should be installed. 😊

------------------------------------------------------------------------------------------------------------------------------------------------------------------
# only continue to step 5, after all Packages & Applications are installed 
------------------------------------------------------------------------------------------------------------------------------------------------------------------
## 5. Downloading Visual Studio Code Extensions

type the following into Terminal: 

```
sudo chmod u+x vscode-extension-install.sh
./vscode-extension-install.sh
```
### enter your Password, after inputing your Password [press Enter]  

------------------------------------------------------------------------------------------------------------------------------------------------------------------
## Visual Studio Code Extesion should begin downloading
------------------------------------------------------------------------------------------------------------------------------------------------------------------

Wait patiently as this may takes a while.🧐

After a little awhile all Extensions should be installed. 😊

------------------------------------------------------------------------------------------------------------------------------------------------------------------
# only continue to step 6, after all Extensions are installed 
------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 6. Installing Oh-My-Zsh

to install oh-my-zsh type the following link into Terminal: 

```
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

### [press Enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 7. Installing Spaceship Prompt Theme for Terminal

to install Spaceship Prompt Theme type the following link into Terminal:

```
git clone https://github.com/denysdovhan/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt" --depth=1
```

### [press Enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following link into Terminal: 

```
ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme" 
```

### [press Enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------
## 8. Editing .zshrc file to have nvm, aliases, and Spaceship Prompt theme.

type the following into Terminal: 

```
code ~/.zshrc
```
### [press Enter]

### click on open/ok/allow

------------------------------------------------------------------------------------------------------------------------------------------------------------------
# .zshrc should open in Visual Studio Code
------------------------------------------------------------------------------------------------------------------------------------------------------------------
# go back into Terminal
------------------------------------------------------------------------------------------------------------------------------------------------------------------
type the following into Terminal:

```
open zshrc.txt
```

### [press Enter]


------------------------------------------------------------------------------------------------------------------------------------------------------------------
# zshrc.txt should open in TextEdit
------------------------------------------------------------------------------------------------------------------------------------------------------------------

### click inside of zshrc.txt

### &

### [press command + A]

## everything in zshrc.txt should be highlighted

### [press command + C]

------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Close zshrc.txt by clicking red ❌ or by:

## click inside of zshrc.txt

### &

### [press command + Q]

------------------------------------------------------------------------------------------------------------------------------------------------------------------
## go back inside of Visual Studio Code
------------------------------------------------------------------------------------------------------------------------------------------------------------------
## you should see infront of yourself .zshrc file
------------------------------------------------------------------------------------------------------------------------------------------------------------------

## we will remove everything that is inside .zshrc file and replace it with the settings we copied from zshrc.txt to do that:

### [press command + A]

## everything in .zshrc file should be highlighted

### [press delete/backspace]

## .zshrc file should now be empty

### [press command + V]

if everything was done correctly this should replace the default settings to include nvm, aliases, and spaceship prompt theme.

### [press command + S]

------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 9. Changing Visual Studio Code's Font, Theme, and Layout.

------------------------------------------------------------------------------------------------------------------------------------------------------------------
## inside of Visual Studio Code
------------------------------------------------------------------------------------------------------------------------------------------------------------------

### [press Command + ,]

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/settings7.png)

in Search bar type:

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/settings5.png)

```
settings.json
```

### click on Edit in setiings.json 

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/setting3.png)

### &

### remove everything that is inside of settings.json to do that:

### [press Command + A]

### everything in settings.json should be highlighted

### [press delete/backspace]
 
## settings.json should now be empty.
------------------------------------------------------------------------------------------------------------------------------------------------------------------
# go back into Terminal
------------------------------------------------------------------------------------------------------------------------------------------------------------------
type the following into Terminal:

```
open vscode-settings.txt
```

### [press Enter]


------------------------------------------------------------------------------------------------------------------------------------------------------------------
# vscode-settings.txt should open in TextEdit
------------------------------------------------------------------------------------------------------------------------------------------------------------------

### click inside of vscode-settings.txt

### &

### [press command + A]

## everything in vscode-settings.txt should be highlighted

### [press command + C]

------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Close vscode-settings.txt by clicking red ❌ or by:

## click inside of vscode-settings.txt

### &

### [press command + Q]

-------------------------------------------------------------------------
## go back inside of Visual Studio Code
------------------------------------------------------------------------------------------------------------------------------------------------------------------

### click inside of settings.json

### &

### [press command + V]

if everything was done correctly this should replace the default settings to auto format on save and paste, change file theme to Material Icon Theme, change font to Fira Code, and change editors theme to Monokai.

### [press command + S]

## Close Visual Studio Code by clicking red ❌ or by:

## click inside of Visual Studio Code

### &

### [press command + Q]
------------------------------------------------------------------------------------------------------------------------------------------------------------------
# go back into Terminal 
------------------------------------------------------------------------------------------------------------------------------------------------------------------

type all of the following into Terminal at once : 

```

chmod 755 /usr/local/share/zsh
chmod 755 /usr/local/share/zsh/site-functions
source ~/.zshrc

```

### [press Enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 10. Removing dev-setup-scripts file and dev-setup-scripts.zip from your computer.


type the following into Terminal:

```
cd ..
```

that should go make Terminal go into Downlods or the Folder dev-setup-scripts file and dev-setup-scripts.zip are on your computer.

type the following into Terminal:

```
rm -rf dev-setup-scripts
rm -rf dev-setup-scripts.zip
```

### [press Enter]

both file should now be deleted and move into your Trash.

------------------------------------------------------------------------------------------------------------------------------------------------------------------
# This is optional. 
## If your dock is set to auto-hide I really reccommend running these 2 commands it will make your dock appear and disappear much faster.
------------------------------------------------------------------------------------------------------------------------------------------------------------------
type the following into Terminal: 

```
cd
```

### [press enter]

type the following into Terminal: 

```
defaults write com.apple.dock autohide-time-modifier -float 0 && Killall Dock
defaults write com.apple.Dock autohide-delay -float 0 && Killall Dock
```

### [press enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------


## 11. Setting up Node with nvm.


next we will setup node with nvm 


## (note: I use node version 12.16.2 if you want to use the latest version, or any other version of node you're welcome to do so.)

------------------------------------------------------------------------------------------------------------------------------------------------------------------
## example 1: for node version 12.16.2 preform 2 following commands 
#  if you're going to set your node to verion 12.16.2 skip example 2 & 3
------------------------------------------------------------------------------------------------------------------------------------------------------------------
type the following into Terminal:
```
cd
nvm install "v12.16.2"
```

### press Enter
------------------------------------------------------------------------------------------------------------------------------------------------------------------
type the following into Terminal:

```
nvm use "v12.16.2"
```

### [press Enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------
## example 2: for your desired version of node preform 2 following commands 
# if you're going to set your node version to your desired version skip example 1 & 3
------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into Terminal:

```
nvm install "{YOUR_DESIRED_NODE_VERSION_NUMBER}"
```

### [press Enter]
------------------------------------------------------------------------------------------------------------------------------------------------------------------
type the following into Terminal:

```
nvm use "{YOUR_DESIRED_NODE_VERSION_NUMBER}"
```

### [press Enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------
## example 3: for the latest available version of node preform 2 following commands 
# if you're going to set your node to the latest available version skip example 1 & 2
------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into Terminal:

```
 nvm install node
 ```
### [press Enter]
------------------------------------------------------------------------------------------------------------------------------------------------------------------
type the following into Terminal:
 
 ```
  nvm use node
  
 ```
### [press Enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------
# to check node version
------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into Terminal :

```
node --version
```

### [press Enter]
------------------------------------------------------------------------------------------------------------------------------------------------------------------
# iTerm2 Should return:
------------------------------------------------------------------------------------------------------------------------------------------------------------------

## v12.16.2 

or 

## v"YOUR_DESIRED_NODE_VERSION_NUMBER" 

or 

## v"LATEST_NODE_VERSION"


------------------------------------------------------------------------------------------------------------------------------------------------------------------


## 12. Setting up Eslint + Prettier with Airbnb Style Guide.


type the following into Terminal:

 
```
cd
```

### [press Enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into Terminal:


```
mkdir eslint
```

### [press Enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into Terminal:


```
cd eslint
```

### [press Enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type all of the following into Terminal at once:

```
npm init -y

npm i -D eslint prettier eslint-plugin-prettier eslint-config-prettier eslint-plugin-node eslint-config-node

npx install-peerdeps --dev eslint-config-airbnb

eslint --init
```

### [press Enter]


------------------------------------------------------------------------------------------------------------------------------------------------------------------

Wait patiently as this may takes a while.🧐

After a little awhile all Eslint, Prettier, and Airbnb Dependencies should be installed. 😊

------------------------------------------------------------------------------------------------------------------------------------------------------------------


scroll down with arrow keys to choose

❯ To check syntax, find problems, and enforce code style


![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/eslint1.png)


### [press Enter]



------------------------------------------------------------------------------------------------------------------------------------------------------------------



choose 

❯  JavaScript modules (import/export)


![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/eslint2.png)


### [press Enter]



------------------------------------------------------------------------------------------------------------------------------------------------------------------



choose 

❯ React


![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/eslint3.png)


### [press Enter]



------------------------------------------------------------------------------------------------------------------------------------------------------------------



choose

No

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/eslint4.png)

 
### [press Enter]


------------------------------------------------------------------------------------------------------------------------------------------------------------------

 
## choose both  

to do that

### move down with arrow keys, 

### press space to select

### make sure both check marks are green
 
✅ Browser

✅ Node

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/eslint5.png)


### [press Enter]


------------------------------------------------------------------------------------------------------------------------------------------------------------------


choose 

❯ Use a popular style guide

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/eslint6.png)


### [press Enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------

choose 

❯ Airbnb: https://github.com/airbnb/javascript

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/eslint7.png)


### [press Enter]


------------------------------------------------------------------------------------------------------------------------------------------------------------------


scroll down with arrow keys to choose
 
 ❯ JSON
 
 ![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/eslint8.png)
 
 
### [press Enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------

choose
 
 Yes
 
 ![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/eslint9.png)
 
 
### [press Enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 13. Adding SSH-KEY to github account.


type the following into Terminal:

```
cd
```
### [press Enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into Terminal:

```
ssh-keygen -t ed25519 -C "your_github_acount_email_email@example.com"
```
### [press Enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------
# iTerm2 will return the following:
------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Enter a file in which to save the key (/Users/you/.ssh/id_ed25519): 

### [press Enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Enter passphrase (empty for no passphrase): 

## "CHOOSE_AND_TYPE_A_PASSWORD"

### &

### [press Enter]
------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Enter same passphrase again: 

## "WRITE_THE_SAME_PASSWORD_AGAIN"

### &

### [press Enter]
------------------------------------------------------------------------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into Terminal:

```
eval "$(ssh-agent -s)"
```

### [press Enter]
------------------------------------------------------------------------------------------------------------------------------------------------------------------
type the following into Terminal:

```
open ~/.ssh/config
```

### [press Enter]


------------------------------------------------------------------------------------------------------------------------------------------------------------------
# if ~/.ssh/config file exists and opens skip over to: in ~/.ssh/config file 
------------------------------------------------------------------------------------------------------------------------------------------------------------------
# if ~/.ssh/config file doesnt exist do the following command:
------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into Terminal:
```
touch ~/.ssh/config
```

### [press Enter]
------------------------------------------------------------------------------------------------------------------------------------------------------------------
type the following into Terminal:

```
open ~/.ssh/config
```

### [press Enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------
# in ~/.ssh/config file 
------------------------------------------------------------------------------------------------------------------------------------------------------------------

type all of the following into ~/.ssh/config:

```
Host *

  AddKeysToAgent yes
  
  UseKeychain yes
  
  IdentityFile ~/.ssh/id_ed25519
``` 
 
### [press Command + S]

## close .ssh/config by clicking red ❌ or by:

## click inside of .ssh/config

### &

### [press command + Q]

------------------------------------------------------------------------------------------------------------------------------------------------------------------
# go back to iTerm2
------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into iTerm2:
 ```
 ssh-add -K ~/.ssh/id_ed25519
 ```
 ### [press Enter]
------------------------------------------------------------------------------------------------------------------------------------------------------------------
# type in the same password you used above for Keychains
 
### [press Enter]
 
### &
 
## if prompted to input your again Password, type in the same password you used above for Keychains again

### &

### if necessary [press Enter] again

------------------------------------------------------------------------------------------------------------------------------------------------------------------
 
type the following into iTerm2:
 
 ```
 pbcopy < ~/.ssh/id_ed25519.pub
 ```
 
 ### [press Enter]
 
------------------------------------------------------------------------------------------------------------------------------------------------------------------
 # head over to your github account @ https://github.com
------------------------------------------------------------------------------------------------------------------------------------------------------------------

# login
 
 ## click on your profile picture or this icon ![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/3lines.png)
 
 ### &
 
 ## click on settings 
 
 ### &
 
 ## click on SSH and GPG key
 
 ![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/ssh1.png)
 
 ### &
  
 ## Click on New SSH key 
 
 ![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/ssh3.png)
 
------------------------------------------------------------------------------------------------------------------------------------------------------------------ 
 ![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/ssh2.png)
 
for title write: 
 
 ```
 macBook
 ```
------------------------------------------------------------------------------------------------------------------------------------------------------------------ 
## click into Key text area
 
### &
  
### [press command + V]
 
 ----------------------------------------------------------------------------------------------------------------------------------------------------------------- 
 # SSH-KEY should paste into Key text area
 -----------------------------------------------------------------------------------------------------------------------------------------------------------------
 # After you wrote the title and pasted in the SSH Key
 -----------------------------------------------------------------------------------------------------------------------------------------------------------------
 
 ## click on Add SSH key
 
-----------------------------------------------------------------------------------------------------------------------------------------------------------------

 # enter in your github password 
 
  ## click Confirm Password
  
  ### or
  
  ### [press Enter]
  
------------------------------------------------------------------------------------------------------------------------------------------------------------------ 
 # you're finished, good job 😀👍
------------------------------------------------------------------------------------------------------------------------------------------------------------------ 
