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



## p.s. When I say type, I actually mean copy [press command + C] + paste [press command + V] 😁

## Had to say "type" because there are people who don't know how to use copy + paste.

## On that note, 

# Disclaimer:

# All information provided in this guide is for general informational purposes only. You agree that you use such information entirely at your own risk. Under no circumstances will I be held responsible or liable in any way for any claims, damages, losses, expenses, costs or liabilities whatsoever (including, without limitation, any direct or indirect damages for loss of profits, business interruption or loss of information) resulting or arising directly or indirectly from your use of or inability to use this manual. 

# This guide is dumbed done to my granny's level. So if you mess your machine up, you must be a talented genius 😂

------------------------------------------------------------------------------------------------------------------------------------------------------------------


## 1. Installing Homebrew

First thing you want to do is open your Terminal 

to open terminal

### [press command + SPACE]

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/spotlight.png)

in Spotlight type:

```
Terminal 
```
### [press Enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------

to download Homebrew you need paste the following link into Terminal:

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### [press Enter]

### &

## if prompted to input your Password, after inputing your Password [press Enter] again  

# after a little while Terminal will prompt you "to continue with downloading Homebrew press return" = [press Enter] 

Wait patiently as this may takes a while (install can take around 4-5 minutes).🧐

After a little awhile Homebrew should be installed. 😊

------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 2. Installing Packages & Applications

type the following into Terminal: 
 
 ```
cd Desktop
 ```
 
### [press Enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------
 
type the following into Terminal: 
 
 ```
 touch packages.txt
 ```
 
### click on open/ok/allow
 
### [press Enter]
 
 -----------------------------------------------------------------------------------------------------------------------------------------------------------------
 
type the following into Terminal:
  
  ```
  open packages.txt
  ```
  
### [press Enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------
  
type the following into packages.txt:
 
 ```
 --cask alfred 
 
 --cask flux
 
 --cask slack
 
 --cask visual-studio-code 
 
 --cask bartender  
 
 --cask google-chrome 
 
 --cask spectacle 
 
 --cask cheatsheet 
 
 --cask iterm2 
 
 --cask hyperswitch
 
 --cask spotify
 
```

### [press command + S] 

don't close packages.txt just yet we will need it in a minute:

------------------------------------------------------------------------------------------------------------------------------------------------------------------
# go back into Terminal
------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into Terminal: 

```
brew install $(<packages.txt)
```

### [press Enter]

### if prompted to input your Password, after inputing your Password [press Enter]  

------------------------------------------------------------------------------------------------------------------------------------------------------------------


Wait patiently as this may takes a while.🧐

After a little awhile all Packages & Applications should be installed. 😊


------------------------------------------------------------------------------------------------------------------------------------------------------------------
# after all Packages & Applications install
------------------------------------------------------------------------------------------------------------------------------------------------------------------
# go back into packages.txt
------------------------------------------------------------------------------------------------------------------------------------------------------------------
## remove everything that is inside of packages.txt to do that:

### [press Command + A]

## everything in packages.txt should be highlighted

### [press delete/backspace]
 
## packages.txt should now be empty.

type the following into packages.txt:

```
git

yarn

zsh

nvm
```
### [press command + S] 

## Close packages.txt by clicking red ❌ or by:

## click inside of packages.txt

### &

### [press command + Q]

------------------------------------------------------------------------------------------------------------------------------------------------------------------
# go back into Terminal
------------------------------------------------------------------------------------------------------------------------------------------------------------------

### [press UP(⬆) arrow key]

### &

### [press Enter]

### if prompted to input your Password, after inputing your Password [press Enter]  

## or

type the following into Terminal: 

```
brew install $(<packages.txt)
```

### [press Enter]

## if prompted to input your Password, after inputing your Password [press Enter]  
------------------------------------------------------------------------------------------------------------------------------------------------------------------
# after all Packages & Applications install
------------------------------------------------------------------------------------------------------------------------------------------------------------------
type the following into Terminal:

```
brew tap homebrew/cask-fonts
brew install --cask font-fira-code
```

### [press Enter]

## if prompted to input your Password, after inputing your Password [press Enter] 

------------------------------------------------------------------------------------------------------------------------------------------------------------------
# after all Packages install
------------------------------------------------------------------------------------------------------------------------------------------------------------------
type the following into Terminal:

```
rm -rf packages.txt
```

### [press Enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------------------------------------------------------------------------
# This is optional. 
## If your dock is set to auto-hide I really reccommend running these 2 commands it will make your dock appear and disappear much faster.
------------------------------------------------------------------------------------------------------------------------------------------------------------------
type the following into Terminal: 

```
defaults write com.apple.dock autohide-time-modifier -float 0 && Killall Dock
```

##### [press enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into Terminal: 

```
defaults write com.apple.Dock autohide-delay -float 0 && Killall Dock
```

### [press enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------
------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 3. Installing Oh-My-Zsh

type the following into Terminal: 

```
open -a iTerm
```

### [press enter]

### click on open/ok/allow
------------------------------------------------------------------------------------------------------------------------------------------------------------------
# iTerm2 should be open. We will use iTerm2 from now on. 
------------------------------------------------------------------------------------------------------------------------------------------------------------------
## Close Terminal by clicking red ❌ or by:

## click inside of Terminal

### &

### [press command + Q]

------------------------------------------------------------------------------------------------------------------------------------------------------------------

to install oh-my-zsh type the following link into iTerm2: 

```
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

### [press Enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 4. Installing Spaceship Prompt Theme for iTerm2(Terminal)

to install Spaceship Prompt Theme type the following link into iTerm2:

```
git clone https://github.com/denysdovhan/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt" --depth=1
```

### [press Enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following link into iTerm2: 

```
ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme" 
```

### [press Enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into iTerm2: 

```
code ~/.zshrc
```
### [press Enter]

### click on open/ok/allow

------------------------------------------------------------------------------------------------------------------------------------------------------------------
# .zshrc should open in Visual Studio Code
------------------------------------------------------------------------------------------------------------------------------------------------------------------

### click inside Visual Studio Code

### &

### [press command + F]

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/find.png)

type in Find bar:

```
ZSH_THEME
```


## VS CODE should highlight ZSH_THEME 

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/ZSH_THEME.png)

change your ZSH_THEME 

from:
 
ZSH_THEME="robbyrussell" 
 
to: 
 
 ```ZSH_THEME="spaceship"```

------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 5. Adding aliases & nvm to .zshrc, and Changing Visual Studio Font & Settings.

while we are in ~/.zshrc lets add couple more things:

## Adding nvm

type the following right under ZSH_THEME:

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/nvm.png)

```
 export NVM_DIR="$HOME/.nvm"
  [ -s "/usr/local/opt/nvm/nvm.sh" ] && . "/usr/local/opt/nvm/nvm.sh"  
  [ -s "/usr/local/opt/nvm/etc/bash_completion.d/nvm" ] && . "/usr/local/opt/nvm/etc/bash_completion.d/nvm"  
```

## (note: next step: removing git plugin is optional, but it tends to clash with my aliases, so i remove it.)

to remove git plugin:

### [press command + F]

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/find.png)

type in Find bar:

```
plugins 
```

## VS CODE should highlight plugins 

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/plugins1.png)

remove everything inside of the brackets () after plugins=

plugins should look like: 

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/plugins2.png)

```
plugins=()
```

------------------------------------------------------------------------------------------------------------------------------------------------------------------

## Adding Aliases

scroll all the way down to the bottom/end of the .zshrc file, and type all of the following:

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/aliases.png)

```
alias gap="git add -p"

alias gaa="git add ."

alias gd="git diff"

alias gi="git init"

alias gl="git log"

alias gpll="git pull"

alias gp="git push"

alias gpom="git push origin master"

alias gss="git status -s"

alias path='echo -e ${PATH//:/\\n}'

alias ns="npm install"

alias yad="yarn add"

alias ni="npm init -y"

alias sp="open -a Spotify"

alias sl="open -a Slack"

alias sett='open -a "System Preferences"'

alias vs='open -a "Visual Studio Code"'

alias apst='open -a "App Store"'

alias a="code"

alias aa="code ."

alias ns="npm start"

alias nr="npm run"

alias l="ls" # List files in current directory

alias ll="ls -al" # List all files in current directory in long list format

alias oo="open ."

alias o="open" # Open the current directory in Finder

alias c="clear"

alias e="exit"

alias dd="cd /Users/`whoami`/project"

alias $="sudo"

alias vsn="code -n"

alias gcb='echo -e "\033[1;32m New branch name?" && read branchname &&git checkout -b $branchname'

alias gc='echo -e "\033[1;32m To what branch do you want to switch?" && read branchname && git checkout $branchname'

alias gcl='echo -e "\033[1;32m Link to Repository you want to clone/download?" && read link && git clone $link'

alias app='echo -e "\033[1;32m React App Name?" && read name && cd /Users/`whoami`/project && npx create-react-app $name &&  cd $name &&  code . && npm start'

alias gra='echo -e "\033[1;32m Repository Link?" && read link &&  git remote add origin $link'

alias gfp='echo -e "\033[1;32m To which Repository-Branch do you want to push?" && read branch && git fetch origin $branch && git push -u origin $branch'

alias gcm='echo -e "\033[1;32m What is your commit message (what have you done, changed, or need to do) ?" && read message && git commit -m "$message"'

alias gs='git status -uno'

alias gru='git remote update'

```


### [press command + S] 

------------------------------------------------------------------------------------------------------------------------------------------------------------------
# Changing Visual Studio Code's Font, Theme, and Layout.
------------------------------------------------------------------------------------------------------------------------------------------------------------------
# inside Visual Studio Code
------------------------------------------------------------------------------------------------------------------------------------------------------------------

### press Command + ,

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
 
### settings.json should now be empty.
 
type the following into settings.json:

```
    {
    
    "workbench.colorTheme": "Monokai",
    
    "[json]": {
        
       
        "editor.quickSuggestions": {
        
            "strings": true
        },
        
        "editor.suggest.insertMode": "replace",
        
    },
    
    "window.zoomLevel": 0,
   
    "editor.formatOnType": true,
    
    "editor.fontSize": 12,
    
    "editor.fontWeight": "normal",
   
        "editor.fontFamily": "Fira Code",
        
        "editor.fontLigatures": true,
        
    "editor.tokenColorCustomizations":{
    
        "textMateRules": [
        
            {
            
                "name": "comment",
                
                "scope": [
                
                    "comment"
                    
                ],
                
                "settings": {
                
                    "fontStyle": "italic"
                    
                }
                
            },
            
            {
                "name": "Keyword Storage",
                
                "scope": [
                
                    "keyword",
                    
                    "keyword.control",
                    
                    "storage"
                    
                ],
                
                "settings": {
                
                    "fontStyle": "italic"
                    
                }
                
            },
            
            {
                "name": "Entity",
                
                "scope": [
                
                    "entity.name.method",
                    
                    "entity.name.type.class",
                    
                    "entity.other.attribute-name"
                    
                ],
                
                "settings": {
                
                    "fontStyle": "italic"
                  
                }
                
            },
            
            {
                "name": "Variable",
                
                "scope": [
                
                    "variable.language"
                    
                ],
                
                "settings": {
                
                    "fontStyle": "italic"
                    
                }
                
            }
            
        ]
        
    },
    
    "editor.matchBrackets": "always",
    
    "editor.suggestSelection": "first",
    
    "vsintellicode.modify.editor.suggestSelection": "automaticallyOverrodeDefaultValue"

    }

```

### [press Command + S]

## close Visual Studio Code by clicking red ❌ or by:

## click inside of Visual Studio Code

### &

### [press command + Q]

------------------------------------------------------------------------------------------------------------------------------------------------------------------
# go back into iTerm2 
------------------------------------------------------------------------------------------------------------------------------------------------------------------

type all of the following into iTerm2 at once : 

```

chmod 755 /usr/local/share/zsh

chmod 755 /usr/local/share/zsh/site-functions

source ~/.zshrc

```

### [press Enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------


## 6. Installing Visual Studio Extensions.


in iTerm2 type all of the following at once:

```

code --install-extension patbenatar.advanced-new-file

code --install-extension formulahendry.auto-close-tag 

code --install-extension formulahendry.auto-rename-tag

code --install-extension mgmcdermott.vscode-language-babel

code --install-extension aaron-bond.better-comments

code --install-extension coenraads.bracket-pair-colorizer-2

code --install-extension wmaurer.change-case

code --install-extension streetsidesoftware.code-spell-checker

code --install-extension vmsynkov.colonize

code --install-extension kamikillerto.vscode-colorize

code --install-extension pranaygp.vscode-css-peek

code --install-extension msjsdiag.debugger-for-chrome

code --install-extension usernamehw.errorlens

code --install-extension dbaeumer.vscode-eslint

code --install-extension toba.vsfire

code --install-extension tombonnike.vscode-status-bar-format-toggle

code --install-extension waderyan.gitblame

code --install-extension mhutchie.git-graph

code --install-extension  donjayamanne.githistory

code --install-extension  felipecaputo.git-project-manager

code --install-extension eamodio.gitlens

code --install-extension fabiospampinato.vscode-highlight

code --install-extension vincaslt.highlight-matching-tag

code --install-extension abusaidm.html-snippets

code --install-extension oderwat.indent-rainbow

code --install-extension sirtori.indenticator

code --install-extension zignd.html-css-class-completion

code --install-extension xabikos.javascriptsnippets

code --install-extension ritwickdey.liveserver

code --install-extension pkief.material-icon-theme

code --install-extension ibm.output-colorizer

code --install-extension ionutvmi.path-autocomplete

code --install-extension christian-kohler.path-intellisense

code --install-extension esbenp.prettier-vscode

code --install-extension rvest.vs-code-prettier-eslint

code --install-extension jundat95.react-native-snippet

code --install-extension joeberria.statusbarerror

code --install-extension rafamel.subtle-brackets

code --install-extension  wayou.vscode-todo-highlight

code --install-extension  britesnow.vscode-toggle-quotes

code --install-extension  chakrounanas.turbo-console-log

code --install-extension  visualstudioexptteam.vscodeintellicode

code --install-extension shyykoserhiy.vscode-spotify

code --install-extension  jpoissonnier.vscode-styled-components

code --install-extension  midnightsyntax.vscode-wrap-console-log

```

### [press Enter]

Wait patiently as this may takes awhile.🧐

After a little awhile all Visual Studio Extensions should be installed. 😊


------------------------------------------------------------------------------------------------------------------------------------------------------------------


## 7. Setting up Node with nvm.


next we will setup node with nvm 


## (note: I use node version 12.16.2 if you want to use the latest version, or any other version of node you're welcome to do so.)

------------------------------------------------------------------------------------------------------------------------------------------------------------------
## example 1: for node version 12.16.2 preform 2 following commands 
#  if you're going to set your node to verion 12.16.2 skip example 2 & 3
------------------------------------------------------------------------------------------------------------------------------------------------------------------
type the following into iTerm2:
```
nvm install "v12.16.2"
```

### press Enter
------------------------------------------------------------------------------------------------------------------------------------------------------------------
type the following into iTerm2:

```
nvm use "v12.16.2"
```

### [press Enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------
## example 2: for your desired version of node preform 2 following commands 
# if you're going to set your node version to your desired version skip example 1 & 3
------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into iTerm2:

```
nvm install "{YOUR_DESIRED_NODE_VERSION_NUMBER}"
```

### [press Enter]
------------------------------------------------------------------------------------------------------------------------------------------------------------------
type the following into iTerm2:

```
nvm use "{YOUR_DESIRED_NODE_VERSION_NUMBER}"
```

### [press Enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------
## example 3: for the latest available version of node preform 2 following commands 
# if you're going to set your node to the latest available version skip example 1 & 2
------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into iTerm2:

```
 nvm install node
 ```
### [press Enter]
------------------------------------------------------------------------------------------------------------------------------------------------------------------
type the following into iTerm2:
 
 ```
  nvm use node
  
 ```
### [press Enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------
# to check node version
------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into iTerm2 :

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


## 8. Setting up Eslint + Prettier with Airbnb Style Guide.


type the following into iTerm2:

 
```
cd
```

### [press Enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into iTerm2:


```
mkdir eslint
```

### [press Enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into iTerm2:


```
cd eslint
```

### [press Enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type all of the following into iTerm2 at once:

```
npm init -y

npm install -g eslint

npm i -D eslint prettier eslint-plugin-prettier eslint-config-prettier eslint-plugin-node eslint-config-node

npx install-peerdeps --dev eslint-config-airbnb

eslint --init
```

### [press Enter]


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

 
## choose both  ( move down with arrow keys,  press space to select, make sure both check marks are green)
 
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

## 9. Adding SSH-KEY to github account.


type the following into iTerm2:

```
cd
```
### [press Enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into iTerm2:

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

type the following into iTerm2:

```
eval "$(ssh-agent -s)"
```

### [press Enter]
------------------------------------------------------------------------------------------------------------------------------------------------------------------
type the following into iTerm2:

```
open ~/.ssh/config
```

### [press Enter]


------------------------------------------------------------------------------------------------------------------------------------------------------------------
# if ~/.ssh/config file exists and opens skip over to: in ~/.ssh/config file 
------------------------------------------------------------------------------------------------------------------------------------------------------------------
# if ~/.ssh/config file doesnt exist do the following command:
------------------------------------------------------------------------------------------------------------------------------------------------------------------

type the following into iTerm2:
```
touch ~/.ssh/config
```

### [press Enter]
------------------------------------------------------------------------------------------------------------------------------------------------------------------
type the following into iTerm2:

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
 # head over to your github account https://github.com
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
  
  
  ![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/ssh2.png)
  

 -----------------------------------------------------------------------------------------------------------------------------------------------------------------

 # enter in your github password 
 
  ## click Confirm Password
  
  ### or
  
  ### [press Enter]
  
------------------------------------------------------------------------------------------------------------------------------------------------------------------ 
 # you're finished, good job 😀👍
------------------------------------------------------------------------------------------------------------------------------------------------------------------ 
