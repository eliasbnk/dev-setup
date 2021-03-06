# How to set up Web-Dev Enviroment on M1 Mac
# In this guide I will show you
- how to install homebrew 
- how to install all necessary apps and extensions 
- how to install Spaceship theme with Oh-My-Zsh
- how to install node
- how to setup eslint with airbnb style guide
- how to add SSH-KEY to github account


## 1. Downlod dev-setup-scripts.zip

<a href='https://github.com/eliasbnk/dev-setup/blob/main/dev-setup-scripts.zip?raw=true' target="_blank" rel="noopener noreferrer">download link for dev-setup-scripts.zip</a>

------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 2. Setting Up Rosetta Terminal

#### `[press command + Space]`

that should open Spotlight

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/spotlight.png)

type the following into Spotlight:

```
/applications
```
![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/Screen%20Shot%202021-03-02%20at%205.02.14%20PM.png)

#### double click on Applications Folder



------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Applications Folder should open

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/Screen%20Shot%202021-03-02%20at%205.02.24%20PM.png)
------------------------------------------------------------------------------------------------------------------------------------------------------------------
type the following into search:
![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/Screen%20Shot%202021-03-02%20at%205.02.32%20PM.png)

```
Terminal
```

choose search Applications

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/Screen%20Shot%202021-03-02%20at%205.02.44%20PM.png)

right-click Terminal 

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/Screen%20Shot%202021-03-02%20at%205.05.00%20PM.png)

click on Duplicate

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/Screen%20Shot%202021-03-02%20at%205.05.03%20PM.png)

if asked enter your password & press ok

right-click duplicated Terminal & click on Rename

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/Screen%20Shot%202021-03-02%20at%205.05.32%20PM.png)

rename the duplicated Terminal to:

```
Rosetta Terminal
```

if asked enter your password & press ok

right-click Rosetta Terminal & click on Get Info

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/Screen%20Shot%202021-03-02%20at%205.05.57%20PM.png)

in the Rosetta Terminal Info window make sure Open using Rosetta is checked

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/Screen%20Shot%202021-03-02%20at%205.06.04%20PM.png)

#### Close Rosetta Terminal Info by clicking red ❌

double click on Rosseta Terminal

------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Rosetta Terminal should open

----------------------------------------------------------------------------------------------------------------------------------------------------------------

lets check if we are using Rosetta

type the following into Terminal: 

```
arch 
``` 

#### `[press Enter]`

if your Rosetta Terminal returned 

i386

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/Screen%20Shot%202021-03-02%20at%205.06.27%20PM.png)

Good Job you did everything correct so far. 
------------------------------------------------------------------------------------------------------------------------------------------------------------------
## 3. Installing Homebrew

type the following into Rosetta Terminal:

```
cd
```

#### `[press Enter]` 

type the following into Rosetta Terminal:

```
mkdir homebrew && curl -L https://github.com/Homebrew/brew/tarball/master | tar xz --strip 1 -C homebrew
```

#### `[press Enter]` 


type the following into Rosetta Terminal:

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

#### `[press Enter]`

#### &

### if prompted to enter your Password, enter your Password, after entering your Password `[press Enter]`   

## AFTER A LITTLE WHILE TERMINAL WILL PROMPT YOU "TO CONTINUE WITH DOWNLOADING HOMEBREW PRESS RETURN" = `[press Enter]`

## IF YOU DON'T `[press Enter]` DOWNLOAD WILL NOT BEGIN!

------------------------------------------------------------------------------------------------------------------------------------------------------------------

Wait patiently as this may takes a while (install can take around 4-5 minutes).🧐

After a little awhile Homebrew should be installed. 😊

------------------------------------------------------------------------------------------------------------------------------------------------------------------

### only continue to step 4 after Homebrew is installed 

------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 4. Setting Up Download Scripts

type the following into Rosetta Terminal:
 ```
cd /Users/`whoami`/Downloads/dev-setup-scripts
 ```
 
#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into Terminal: 

```
ls
```

#### `[press Enter]`

#### if any prompts open click on ok/allow

------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Compare this list to what your Terminal returned (if you are in dev-setup-scripts folder you should have all of these files)

------------------------------------------------------------------------------------------------------------------------------------------------------------------

- brew-install-cask.txt

- brew-install.txt

- vscode-settings.txt

- zshrc.txt


------------------------------------------------------------------------------------------------------------------------------------------------------------------

### If you indeed have all those files skip over to step 5 Installing Packages & Applications

------------------------------------------------------------------------------------------------------------------------------------------------------------------

### if your Terminal didn't return that or you dont have those files do the following

------------------------------------------------------------------------------------------------------------------------------------------------------------------

#### `[press command + SPACE]`

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/spotlight.png)

in Spotlight type:

```
dev-setup-scripts
```

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Finder should open where dev-setup-scripts folder has been downloded

------------------------------------------------------------------------------------------------------------------------------------------------------------------

#### click on dev-setup-scripts folder

#### &

#### `[press command + C]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

### go back into Terminal

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into Terminal: 

```
cd
```

#### `[press Space]`

#### &

#### `[press command + V]`

### it should like something like this

cd /Users/{YOUR_USERNAME}/{FOLDER_NAME_THE_FILE_IS_IN}/dev-setup-scripts

### if it does great, if not redownload the dev-setup-scripts.zip file into Downloads folder and repeat step 3 from beginning.

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

### you should now be in dev-setup-scripts folder

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into Terminal: 

```
ls
```

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Compare this list to what your Terminal returned (if you are in dev-setup-scripts folder you should have all of these files)

------------------------------------------------------------------------------------------------------------------------------------------------------------------

- brew-install-cask.txt

- brew-install.txt

- vscode-settings.txt

- zshrc.txt

------------------------------------------------------------------------------------------------------------------------------------------------------------------

### If Terminal still doesnt return this repeat step 4 from beginning again.

------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 5. Installing Packages & Applications

type all of the following into Terminal at once : 

```
sudo chown -R $(whoami) /usr/local/Homebrew /usr/local/etc/bash_completion.d /usr/local/share/doc /usr/local/share/man /usr/local/share/man/man1 /usr/local/var/homebrew/locks &&
chmod u+w /usr/local/Homebrew /usr/local/etc/bash_completion.d /usr/local/share/doc /usr/local/share/man /usr/local/share/man/man1 /usr/local/var/homebrew/locks
```

#### `[press Enter]`

#### if prompted to input your Password, after inputing your Password `[press Enter]`  

type all of the following into Terminal at once : 

```
brew tap homebrew/cask-fonts
brew install $(<brew-install.txt)
brew install $(<brew-install-cask.txt)
```
#### `[press Enter]`

#### if prompted to input your Password, after inputing your Password `[press Enter]`  

------------------------------------------------------------------------------------------------------------------------------------------------------------------

Wait patiently as this may takes a while.🧐

After a little awhile all Packages & Applications should be installed. 😊

------------------------------------------------------------------------------------------------------------------------------------------------------------------

### only continue to step 6, after all Packages & Applications are installed 

------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 6. Downloading Visual Studio Code Extensions

type all of the following into Terminal at once : 

```
code --install-extension JSMel.web-dev-pack
```

#### enter your Password, after inputing your Password `[press Enter]`  

------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Visual Studio Code Extesions should begin downloading

------------------------------------------------------------------------------------------------------------------------------------------------------------------

Wait patiently as this may takes a while.🧐

After a little awhile all Extensions should be installed. 😊

------------------------------------------------------------------------------------------------------------------------------------------------------------------

### only continue to step 7, after all Extensions are installed 

------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 6. Installing Oh-My-Zsh

to install oh-my-zsh type the following link into Terminal: 

```
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

### only continue to step 9 after Oh-My-Zsh is installed 

------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 7. Installing Spaceship Prompt Theme for Terminal

to install Spaceship Prompt Theme type the following link into Terminal:

```
git clone https://github.com/denysdovhan/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt" --depth=1
```

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following link into Terminal: 

```
ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme" 
```

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------
## 7. Installing Syntax Highlight, Autosuggetsions and Git Open for oh my zsh.

type the following link into Terminal: 

```
cd
```
#### `[press Enter]`

type the following link into Terminal: 

```
cd ~/.oh-my-zsh/custom/plugins    
```
#### `[press Enter]`

type all of the following into Terminal at once : 

```
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions && git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting && git clone https://github.com/paulirish/git-open.git $ZSH_CUSTOM/plugins/git-open     
```

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------
## 10. Editing .zshrc file to have nvm, aliases, and Spaceship Prompt theme.

type the following into Terminal: 

```
cd /Users/`whoami`/Downloads/dev-setup-scripts && code ~/.zshrc
```

#### `[press Enter]`

#### click on open/ok/allow

------------------------------------------------------------------------------------------------------------------------------------------------------------------

### .zshrc should open in Visual Studio Code

------------------------------------------------------------------------------------------------------------------------------------------------------------------

### go back into Terminal

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into Terminal:

```
open zshrc.txt
```

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

### zshrc.txt should open in TextEdit

------------------------------------------------------------------------------------------------------------------------------------------------------------------

#### click inside of zshrc.txt

#### &

#### `[press command + A]`

everything in zshrc.txt should be highlighted

#### `[press command + C]`

#### &

#### Close zshrc.txt by clicking red ❌

------------------------------------------------------------------------------------------------------------------------------------------------------------------

### go back inside of Visual Studio Code

------------------------------------------------------------------------------------------------------------------------------------------------------------------

### you should see infront of yourself .zshrc file

------------------------------------------------------------------------------------------------------------------------------------------------------------------

we will remove everything that is inside .zshrc file and replace it with the settings we copied from zshrc.txt to do that:

#### `[press command + A]`

everything in .zshrc file should be highlighted

#### `[press delete/backspace]`

.zshrc file should now be empty

#### `[press command + V]`

if everything was done correctly this should replace the default settings to include nvm, aliases, and spaceship prompt theme.

#### `[press command + S]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 11. Changing Visual Studio Code's Font, Theme, and Layout.

------------------------------------------------------------------------------------------------------------------------------------------------------------------

### inside of Visual Studio Code

------------------------------------------------------------------------------------------------------------------------------------------------------------------

#### `[press Command + ,]`

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/settings7.png)

------------------------------------------------------------------------------------------------------------------------------------------------------------------

in Search bar type:

```
settings.json
```
![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/settings5.png)

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

#### click on Edit in setiings.json 

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/setting3.png)

#### &

remove everything that is inside of settings.json to do that:

#### `[press Command + A]`

everything in settings.json should be highlighted

#### `[press delete/backspace]`
 
settings.json should now be empty.

------------------------------------------------------------------------------------------------------------------------------------------------------------------

### go back into Terminal

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into Terminal:

```
open vscode-settings.txt
```

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

### vscode-settings.txt should open in TextEdit

------------------------------------------------------------------------------------------------------------------------------------------------------------------

#### click inside of vscode-settings.txt

#### &

#### `[press command + A]`

everything in vscode-settings.txt should be highlighted

#### `[press command + C]`

#### Close vscode-settings.txt by clicking red ❌

------------------------------------------------------------------------------------------------------------------------------------------------------------------

### go back inside of Visual Studio Code

------------------------------------------------------------------------------------------------------------------------------------------------------------------

#### click inside of settings.json

#### &

#### `[press command + V]`

if everything was done correctly this should replace the default settings to auto format on save and paste, change file theme to Material Icon Theme, change font to Fira Code, and change editors theme to Monokai.

#### `[press command + S]`

#### Close Visual Studio Code by clicking red ❌

------------------------------------------------------------------------------------------------------------------------------------------------------------------

### go back into Terminal

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into Terminal: 

```
source ~/.zshrc
```

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 12. Removing dev-setup-scripts file and dev-setup-scripts.zip from your computer.

type the following into Terminal:

```
cd ..
```

#### `[press Enter]`
  
------------------------------------------------------------------------------------------------------------------------------------------------------------------

that command should've made Terminal go out of dev-setup-scripts file, and into Downlods or the Folder dev-setup-scripts file and dev-setup-scripts.zip are on your computer.

type all of the following into Terminal at once : 

```
rm -rf dev-setup-scripts
rm -rf dev-setup-scripts.zip
```

#### `[press Enter]`

both file should now be deleted and moved into your Trash.

------------------------------------------------------------------------------------------------------------------------------------------------------------------

## This is optional. 
### If your dock is set to auto-hide I really reccommend running these 2 commands it will make your dock appear and disappear much faster.

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into Terminal: 

```
cd
```

#### `[press enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type all of the following into Terminal at once : 

```
defaults write com.apple.dock autohide-time-modifier -float 0 && Killall Dock
defaults write com.apple.Dock autohide-delay -float 0 && Killall Dock
```

#### `[press enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 13. Setting up Node with nvm.

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into Terminal:

```
cd
```

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into Terminal:

```
mkdir ~/.nvm
```

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Choose either to do Example 1 or Example 2.

## DO NOT DO BOTH! 

### After you're finished with either Example 1 or 2 go straight to Step 13 Checking node version.

------------------------------------------------------------------------------------------------------------------------------------------------------------------

## example 1: for your desired version of node preform 2 following commands 

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into Terminal:

```
nvm install "YOUR_DESIRED_NODE_VERSION_NUMBER"
```

example: ``nvm install "v12.16.2"``

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

Wait patiently as this may takes a while.🧐

After a little awhile node version YOUR_DESIRED_NODE_VERSION_NUMBER should be installed. 😊

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into Terminal:

```
nvm use "YOUR_DESIRED_NODE_VERSION_NUMBER"
```

example: ``nvm use "v12.16.2"``

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

## example 2: for the latest available version of node preform 2 following commands 

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into Terminal:

```
 nvm install node
 ```
 
#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

Wait patiently as this may takes a while.🧐

After a little awhile, and the latest version of node should be installed. 😊

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into Terminal:
 
 ```
  nvm use node
  
 ```
 
#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 14. Check node version

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into Terminal :

```
node --version
```

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Terminal Should return:

------------------------------------------------------------------------------------------------------------------------------------------------------------------

### vYOUR_DESIRED_NODE_VERSION_NUMBER 

example: ``v12.16.2``

or 

### vLATEST_NODE_VERSION

------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 15. Setting up Eslint + Prettier with Airbnb Style Guide.


type the following into Terminal:

```
cd
```

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into Terminal:

```
mkdir eslint-config
```

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into Terminal:

```
cd eslint-config
```

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type all of the following into Terminal at once : 

```
npm init -y
npm install -g eslint
npm i -D eslint prettier eslint-plugin-prettier eslint-config-prettier eslint-plugin-node eslint-config-node
npx install-peerdeps --dev eslint-config-airbnb
eslint --init
```

#### `[press Enter]`


------------------------------------------------------------------------------------------------------------------------------------------------------------------

Wait patiently as this may takes a while.🧐

After a little awhile all Eslint, Prettier, and Airbnb Dependencies should be installed. 😊

------------------------------------------------------------------------------------------------------------------------------------------------------------------

scroll down with arrow keys to choose

❯ To check syntax, find problems, and enforce code style

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/eslint1.png)

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

choose 

❯  JavaScript modules (import/export)

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/eslint2.png)

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

choose 

❯ React

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/eslint3.png)

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

choose

❯ No

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/eslint4.png)

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

## choose both  

to do that

### move down with arrow keys, 

### press space to select

### make sure both check marks are green
 
✅ Browser

✅ Node

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/eslint5.png)

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

choose 

❯ Use a popular style guide

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/eslint6.png)

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

choose 

❯ Airbnb: https://github.com/airbnb/javascript

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/eslint7.png)

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

scroll down with arrow keys to choose
 
 ❯ JSON
 
 ![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/eslint8.png)
 
#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

choose
 
❯ Yes
 
 ![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/eslint9.png)
 
#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

# 16. Configuring your Git username/email

type the following into Terminal:

```
cd
```

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into Terminal:

```
git config --global user.name "FIRST_NAME LAST_NAME"
```

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into Terminal:

```
git config --global user.email "MY_NAME@example.com"
```

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 17. Adding SSH-KEY to github account.

type the following into Terminal:

```
cd
```

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into Terminal:

```
ssh-keygen -t ed25519 -C "your_github_acount_email_email@example.com"
```

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Terminal will return the following:

------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Enter a file in which to save the key (/Users/you/.ssh/id_ed25519): 

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Enter passphrase (empty for no passphrase): 

"CHOOSE_AND_TYPE_A_PASSWORD"

#### &

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Enter same passphrase again: 

"WRITE_THE_SAME_PASSWORD_AGAIN"

#### &

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into Terminal:

```
eval "$(ssh-agent -s)"
```

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into Terminal:

```
open ~/.ssh/config
```

#### `[press Enter]`


------------------------------------------------------------------------------------------------------------------------------------------------------------------

### if ~/.ssh/config file exists and opens skip over to: in ~/.ssh/config file 

------------------------------------------------------------------------------------------------------------------------------------------------------------------

### if ~/.ssh/config file doesnt exist do the following command:

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into Terminal:

```
touch ~/.ssh/config
```

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into Terminal:

```
open ~/.ssh/config
```

#### `[press Enter]`

------------------------------------------------------------------------------------------------------------------------------------------------------------------

## in ~/.ssh/config file 

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type all of the following into ~/.ssh/config:

```
Host *

  AddKeysToAgent yes
  
  UseKeychain yes
  
  IdentityFile ~/.ssh/id_ed25519
``` 
 
#### `[press Command + S]`

#### close .ssh/config by clicking red ❌

------------------------------------------------------------------------------------------------------------------------------------------------------------------

### go back to Terminal

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into Terminal:

 ```
 ssh-add -K ~/.ssh/id_ed25519
 ```
 
 #### `[press Enter]`
 
------------------------------------------------------------------------------------------------------------------------------------------------------------------

### type in the same password you used above for Keychains
 
#### `[press Enter]`
 
#### &
 
### if prompted to input your again Password, type in the same password you used above for Keychains again

#### &

#### if necessary `[press Enter]` again

------------------------------------------------------------------------------------------------------------------------------------------------------------------
 
type the following into Terminal:
 
 ```
 pbcopy < ~/.ssh/id_ed25519.pub
 ```
 
#### `[press Enter]`
 
#### close Terminal by clicking red ❌

------------------------------------------------------------------------------------------------------------------------------------------------------------------

### open a new github window in your browser, and put it side-by-side with this guide

<a href="https://github.com/login" target="_blank" rel="noopener noreferrer">GitHub Login Page</a>

------------------------------------------------------------------------------------------------------------------------------------------------------------------

### login
 
#### click on your profile picture or this icon ![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/3lines.png)
 
 #### &
 
 #### click on settings 
 
 #### &
 
 #### click on SSH and GPG key
 
 ![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/ssh1.png)
 
 #### &
  
 #### Click on New SSH key 
 
 ![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/ssh3.png)
 
------------------------------------------------------------------------------------------------------------------------------------------------------------------ 

#### click into Key text area
 
#### &
  
#### `[press command + V]`
 
------------------------------------------------------------------------------------------------------------------------------------------------------------------ 
 
 ### SSH-KEY should paste into Key text area
 
------------------------------------------------------------------------------------------------------------------------------------------------------------------
 
### for title write: 
 
 ```
 macBook
 ```
 
------------------------------------------------------------------------------------------------------------------------------------------------------------------ 

 ### After you wrote the title and pasted in the SSH Key
 
------------------------------------------------------------------------------------------------------------------------------------------------------------------
 
 #### click on Add SSH key
 
  ![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/ssh2.png)
  
------------------------------------------------------------------------------------------------------------------------------------------------------------------

#### enter in your github password 
 
#### click Confirm Password
  
------------------------------------------------------------------------------------------------------------------------------------------------------------------ 
 # you're finished, good job 😀👍
------------------------------------------------------------------------------------------------------------------------------------------------------------------ 
