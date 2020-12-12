------------------------------------------------------------------------------------------------------------------------------------------------------------------

# This file contains info on how to setup your web development enviroment. 

## In this file I cover:

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

# All information provided in this manual is for general informational purposes only. You agree that you use such information entirely at your own risk. Under no circumstances will I be held responsible or liable in any way for any claims, damages, losses, expenses, costs or liabilities whatsoever (including, without limitation, any direct or indirect damages for loss of profits, business interruption or loss of information) resulting or arising directly or indirectly from your use of or inability to use this manual. 

# This manual is dumbed done to my granny's level. So if you mess your machine up, you must be a talented genius 😂

------------------------------------------------------------------------------------------------------------------------------------------------------------------


## 1. Installing Homebrew

First thing you want to do is open your Terminal 

to open terminal

##### [press command + SPACE]

in Spotlight type:

```
Terminal 
```

to download Homebrew you need paste the following link into Terminal:

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

##### [press Enter]

##### &

#### when/if prompted [press Enter] again 

Wait patiently as this may takes a while.🧐

After a little awhile Homebrew should be installed. 😊

------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 2. Installing Packages & Applications

type the following into Terminal: 
 
 ```
cd Desktop
 ```
##### [press Enter]
 
type the following into Terminal: 
 
 ```
 touch packages.txt
 ```
 
##### [press Enter]
 
type the following into Terminal:
  
  ```
  open packages.txt
  ```
  
##### [press Enter]
  
type the following into packages.txt:
 
 ```
 --cask alfred 
 
 --cask flux
 
 --cask visual-studio-code 
 
 --cask bartender  
 
 --cask google-chrome 
 
 --cask spectacle 
 
 --cask cheatsheet 
 
 --cask iterm2 
 
 --cask hyperswitch
 
 --cask spotify
 
 --cask iterm2
 
git

yarn

zsh

nvm

```

##### [press command + S] 

close packages.txt by clicking red ❌ or by:

##### click inside of packages.txt

##### &

##### [press command + Q]


type all of the following into Terminal at once: 

```
brew install $(<packages.txt)
brew tap homebrew/cask-fonts
brew install --cask font-fira-code
```

##### [press Enter]

Wait patiently as this may takes a while.🧐

After a little awhile all Packages & Applications should be installed. 😊

------------------------------------------------------------------------------------------------------------------------------------------------------------------

Also I really reccomend geting:
- RedQuits:
(if you press ❌ it preform command+Q on that Application, which unfortunately Apple did add. As if you press ❌ current Application window closes, but app is minimized into the Application Icon)

To download RedQuits: http://redquits.s3.amazonaws.com/RedQuits_v2.pkg

- Amphetamine:
(Keeps display awake. Very useful if you're downloading or uploading a large file, and dont want your computer to go to sleep, and end/pause the process)

To download Amphetamine:

##### [press command + SPACE]

type in Spotlight:

```
App Store
```

##### [press Enter]
 
in Search bar type:

```Amphetamine```

##### [press Enter]

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/amphetamine.png)

##### &
 
##### click on get

##### &

#### (if needed type in your iCloud password)

Amphetamine should begin download

------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 3. Installing Oh-My-Zsh

type the following into Terminal: 

```
open -a iTerm
```

##### [press enter]


#### iTerm2 should be open. We will use iTerm2 from now on. you can close Terminal by clicking red ❌ or by:

##### click inside of Terminal

##### &

##### [press command + Q]

to install oh-my-zsh type the following link into iTerm2: 

```
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

##### [press Enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 4. Installing Spaceship Prompt Theme for iTerm2(Terminal)

to install Spaceship Prompt Theme type the following link into iTerm2:

```
git clone https://github.com/denysdovhan/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt" --depth=1
```

##### [press Enter]

type the following link into iTerm2: 

```
ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme" 
```

##### [press Enter]

type the following into iTerm2: 

```
code ~/.zshrc
```

#### .zshrc should open in Visual Studio Code

##### click inside Visual Studio Code

##### &

##### [press command + F]

type in Find bar:

```
ZSH_THEME
```


#### VS CODE should highlight ZSH_THEME 

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/ZSH_THEME.png)

change your ZSH_THEME 

from:
 
ZSH_THEME="robbyrussell" 
 
to: 
 
 ```ZSH_THEME="spaceship"```

------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 5. Adding aliases & nvm to .zshrc, and Changing Visual Studio Font & Settings.

while we are in ~/.zshrc lets add couple more things:

### Adding nvm

type the following right under ZSH_THEME:

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/nvm.png)

```
 export NVM_DIR="$HOME/.nvm"
  [ -s "/usr/local/opt/nvm/nvm.sh" ] && . "/usr/local/opt/nvm/nvm.sh"  
  [ -s "/usr/local/opt/nvm/etc/bash_completion.d/nvm" ] && . "/usr/local/opt/nvm/etc/bash_completion.d/nvm"  
```

#### (note: next step: removing git plugin is optional, but it tends to clash with my aliases, so i remove it.)

to remove git plugin:

##### [press command + F]

type in Find bar:

```
plugins 
```

#### VS CODE should highlight plugins 

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/plugins1.png)

remove everything inside of the brackets () after plugins=

plugins should look like: 

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/plugins2.png)

```
plugins=()
```

------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Adding Aliases

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

alias gcl="git clone"

alias path='echo -e ${PATH//:/\\n}'

alias ns="npm install"

alias yad="yarn add"

alias ni="npm init -y"

alias spotify="open -a Spotify"

alias slack="open -a Slack"

alias sett='open -a "System Preferences"'

alias vs='open -a "Visual Studio Code"'

alias viber="open -a Viber"

alias trel="open -a Trello"

alias appst='open -a "App Store"'

alias gcb="git checkout -b"

alias gc="git checkout"

alias a="code"

alias aa="code ."

alias ns="npm start"

alias nr="npm run"

alias l="ls" # List files in current directory

alias ll="ls -al" # List all files in current directory in long list format

alias oo ="open ."

alias o="open" # Open the current directory in Finder

alias c="clear"

alias e="exit"

alias dd="cd /Users/`whoami`/project"

alias S="sudo"

alias vsn="code -n"

alias sl="lite-server"

alias app='echo -e "\033[1;32m React App Name?" && read name && cd /Users/`whoami`/project && npx create-react-app $name &&  cd $name &&  code . && npm start'

alias gra='echo -e "\033[1;32m Repository Link?" && read link &&  git remote add origin $link'

alias gfp='echo -e "\033[1;32m To which Repository-Branch do you want to push?" && read branch && git fetch origin $branch && git push -uf origin $branch'

alias gcm='echo -e "\033[1;32m What is your commit message (what have you done, changed, or need to do) ?" && read message && git commit -m "$message"'

alias gs='git status -uno'

alias gru='git remote update'
```


##### [press command + S] 

------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Changing Visual Studio Code's Font, Theme, and Layout.

inside Visual Studio Code

##### press Command + ,

in Search bar type:

```
settings.json
```

##### click on Edit in setiings.json 

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/setting3.png)

##### &

##### remove everything that is inside of settings.json to do that:

##### [press Command + A]

#### everything in settings.json should be highlighted

##### [press delete/backspace]
 
#### settings.json should now be empty.
 
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

##### [press Command + S]

 close Visual Studio Code by clicking red ❌ or by:

##### click inside of Visual Studio Code

##### &

##### [press command + Q]

go back into iTerm2 

type all of the following into iTerm2 at once : 

```

chmod 755 /usr/local/share/zsh

chmod 755 /usr/local/share/zsh/site-functions

source ~/.zshrc

```

##### [press Enter]

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

##### [press Enter]

Wait patiently as this may takes awhile.🧐

After a little awhile all Visual Studio Extensions should be installed. 😊


------------------------------------------------------------------------------------------------------------------------------------------------------------------


## 7. Setting up Node with nvm.


next we will setup node with nvm 


### (note: I use node version 12.16.2 if you want use latest version or any other version you're welcome to do so.)



##### example 1 (setting up Node with version 12.16.2) :


```
nvm install "v12.16.2"
```

##### press Enter

type the following into iTerm2:

```
nvm use "v12.16.2"
```

#### [press Enter]

### example 2 (setting up Node with your desired version) :

type the following into iTerm2:

```
nvm install "{YOUR_DESIRED_NODE_VERSION_NUMBER}"
```

##### [press Enter]

type the following into iTerm2:

```
nvm use "{YOUR_DESIRED_NODE_VERSION_NUMBER}"
```

### example 3 (setting up Node with the latest available version) :

type the following into iTerm2:

```
 nvm install node
 ```
##### [press Enter]
 
type the following into iTerm2:
 
 ```
  nvm use node
  
 ```
##### [press Enter]

to check node version type the following into iTerm2 :

```
node --version
```

#### [press Enter]

### iTerm2 Should return:

#### v12.16.2 

or 

#### v"YOUR_DESIRED_NODE_VERSION_NUMBER" 

or 

#### v"LATEST_NODE_VERSION"


------------------------------------------------------------------------------------------------------------------------------------------------------------------


## 8. Setting up Eslint + Prettier with Airbnb Style Guide.


type the following into iTerm2:

 
```
cd
```

##### [press Enter]

type the following into iTerm2:


```
mkdir eslint
```

##### [press Enter]


type the following into iTerm2:


```
cd eslint
```

##### [press Enter]

type all of the following into iTerm2 at once:

```
npm i -D eslint prettier eslint-plugin-prettier eslint-config-prettier eslint-plugin-node eslint-config-node

npx install-peerdeps --dev eslint-config-airbnb

npm init -y

eslint --init
```

##### [press Enter]

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/eslint1.png)

scroll down with arrow keys to choose

❯ To check syntax, find problems, and enforce code style


##### [press Enter]

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/eslint2.png)

choose 

❯  JavaScript modules (import/export)


##### [press Enter]

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/eslint3.png)

choose 

❯ React

##### [press Enter]

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/eslint4.png)

choose

No
 
##### [press Enter]
 
![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/eslint5.png)
 
#### choose both  ( move down with arrow keys,  press space to select, make sure both check marks are green)
 
✅ Browser

✅ Node

##### [press Enter]

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/eslint6.png)

choose 

❯ Use a popular style guide

##### [press Enter]

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/eslint7.png)

choose 

❯ Airbnb: https://github.com/airbnb/javascript

##### [press Enter]

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/eslint8.png)
 
choose
 
 ❯ JSON
 
##### [press Enter]

![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/eslint9.png)

choose
 
 Yes
 
##### [press Enter]

------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 9. Adding SSH-KEY to github account.


type the following into iTerm2:

```
cd
```
##### [press Enter]

type the following into iTerm2:

```
ssh-keygen -t ed25519 -C "your_github_acount_email_email@example.com"
```

#### Enter a file in which to save the key (/Users/you/.ssh/id_ed25519): [press Enter]

#### Enter passphrase (empty for no passphrase): "CHOOSE_A_PASSWORD"
#### Enter same passphrase again: "WRITE_THE_PASSWORD_AGAIN"


type the following into iTerm2:

```
eval "$(ssh-agent -s)"
```

##### [press Enter]


type the following into iTerm2:

```
open ~/.ssh/config
```

##### [press Enter]

#### if file doesnt exist type the following into iTerm2:

```
touch ~/.ssh/config
```

##### [press Enter]

type the following into iTerm2:

```
open ~/.ssh/config
```

##### [press Enter]


#### in ~/.ssh/config file type the following all:

```
Host *

  AddKeysToAgent yes
  
  UseKeychain yes
  
  IdentityFile ~/.ssh/id_ed25519
``` 
 
##### [press Command + S]

close .ssh/config by clicking red ❌ or by:

##### click inside of .ssh/config

##### &

##### [press command + Q]

 
go back to iTerm2 and type the following :
 ```
 ssh-add -K ~/.ssh/id_ed25519
 ```
 ##### [press Enter]
 
type in the same password you used above for Keychains
 
 ##### [press Enter]
 
 ##### &
 
 #### if necessary type the password agian
 
 ##### &
 
 ##### if necessary [press Enter] again
 
type the following into iTerm2:
 
 ```
 pbcopy < ~/.ssh/id_ed25519.pub
 ```
 
 ##### [press Enter]
 
 #### head over to your github account 
 
login
 
 ##### click on your profile picture 
 
 ##### &
 
 ##### click on settings 
 
 ##### &
 
 ![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/ssh1.png)
 
 ##### click on SSH and GPG key
 
 ##### &
 
  ![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/ssh3.png)
 ##### Click New SSH key or Add SSH key
 
for title write: 
 
 ```
 macBook
 ```
   ![alt text](https://raw.githubusercontent.com/eliasbnk/dev-setup/main/img/ssh2.png)
 ##### click into key text area
 
  ##### &
 
 ##### [press command + V]
 
  ##### &
 
 #### SSH-KEY should paste into key text area
 
  ##### &
 
 ##### press add SSH key
 
 enter in your github password 
 
  ##### [press Enter]
 
 
 ## you're finished, good job 😀👍
------------------------------------------------------------------------------------------------------------------------------------------------------------------

