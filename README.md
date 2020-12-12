First thing you want to do is open your terminal and download Homebrew.

to do that paste this into your terminal

/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

press Enter

Homebrew should be installed 

 
type this into your terminal 

brew install —cask alfred ; brew install —cask flux ; brew install —cask oversight ;  brew install —cask visual-studio-code ; brew install —cask bartender ;  brew install —cask font-fira-code ;   brew install —cask slack  ;   brew install —cask brave-browser ;   brew install —cask google-chrome ;      brew install —cask spectacle ;  brew install —cask zoomus ; brew install —cask cheatsheet  ;  brew install —cask iterm2 ;   brew install —cask hyperswitch ;   brew install —cask spotify ; brew install —cask expressvpn ;  brew install —cask iterm2  ;     brew install —cask viber ; brew install git ;	brew install node ;	 brew install nvm ;	 brew install yarn ; brew install zsh ;


press Enter


open iTerm2.

now we will install oh-my-zsh.

type this into your terminal 


sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

press Enter


next we will install spaceship prompt theme

type this into your terminal 

git clone https://github.com/denysdovhan/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt" --depth=1

press Enter

type this into your terminal 

ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme" 

press Enter

type this into your terminal 

code ~/.zshrc

that should open .zshrc in vscode

press command + f

type in ZSH_THEME

VS CODE should highlight ZSH_THEME 

change your theme from

ZSH_THEME="robbyrussell"

to

ZSH_THEME="spaceship"

while we are in ~/.zshrc lets add couple more things

this is for nvm, type this under ZSH_THEME

 export NVM_DIR="$HOME/.nvm"
  [ -s "/usr/local/opt/nvm/nvm.sh" ] && . "/usr/local/opt/nvm/nvm.sh"  # This loads nvm
  [ -s "/usr/local/opt/nvm/etc/bash_completion.d/nvm" ] && . "/usr/local/opt/nvm/etc/bash_completion.d/nvm"  # This loads nvm bash_completion

next press command + F plugins 

and remove everything inside the brackets

it should look like this 

plugins=()

next scroll all the way down to the end of the file and add these aliases

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

alias dd="cd /Users/elias/project"

alias S="sudo"

alias vsn="code -n"

alias sl="lite-server"

alias app='echo -e "\033[1;32m React App Name?" && read name && cd /Users/elias/project && npx create-react-app $name &&  cd $name &&  code . && npm start'

alias gra='echo -e "\033[1;32m Repository Link?" && read link &&  git remote add origin $link'

alias gfp='echo -e "\033[1;32m To which Repository-Branch do you want to push?" && read branch && git fetch origin $branch && git push -uf origin $branch'

alias gcm='echo -e "\033[1;32m What is your commit message (what have you done, changed, or need to do) ?" && read message && git commit -m "$message"'

alias gs='git status -uno'

alias gru='git remote update'

press command+S 

close file and go back to terminal 

type in

source ~/.zshrc

press Enter

next in terminal type in

cd Desktop

press Enter

type in terminal 

touch vscode-extensions.txt

press Enter

next type in Terminal 

open vscode-extensions.txt

press Enter

copy and paste the following into vscode-extensions.txt :

patbenatar.advanced-new-file
gluons.vscode-atom-javascript-snippet
formulahendry.auto-close-tag
formulahendry.auto-rename-tag
mgmcdermott.vscode-language-babel
aaron-bond.better-comments
thekalinga.bootstrap4-vscode
coenraads.bracket-pair-colorizer-2
wmaurer.change-case
streetsidesoftware.code-spell-checker
vmsynkov.colonize
kamikillerto.vscode-colorize
pranaygp.vscode-css-peek
msjsdiag.debugger-for-chrome
usernamehw.errorlens
dbaeumer.vscode-eslint
toba.vsfire
tombonnike.vscode-status-bar-format-toggle
waderyan.gitblame
mhutchie.git-graph
donjayamanne.githistory
felipecaputo.git-project-manager
eamodio.gitlens
fabiospampinato.vscode-highlight
vincaslt.highlight-matching-tag
abusaidm.html-snippets
oderwat.indent-rainbow
sirtori.indenticator
zignd.html-css-class-completion
xabikos.javascriptsnippets
akamud.vscode-javascript-snippet-pack
ritwickdey.liveserver
pkief.material-icon-theme
ibm.output-colorizer
ionutvmi.path-autocomplete
christian-kohler.path-intellisense
esbenp.prettier-vscode
rvest.vs-code-prettier-eslint
jundat95.react-native-snippet
equimper.react-native-react-redux
burkeholland.simple-react-snippets
joeberria.statusbarerror
rafamel.subtle-brackets
wayou.vscode-todo-highlight
britesnow.vscode-toggle-quotes
chakrounanas.turbo-console-log
visualstudioexptteam.vscodeintellicode
shyykoserhiy.vscode-spotify
jpoissonnier.vscode-styled-components
midnightsyntax.vscode-wrap-console-log

press command+S

go back to terminal and type in


while read line; do code --install-extension "$line";done < vscode-extensions.txt

press enter

type in terminal

nvm install "v12.16.2"

press Enter

type in terminal

nvm use "v12.16.2"

press Enter

check node version by typing in

node --version

press Enter

Terminal Should return

v12.16.2

next type in terminal

vs

press Enter

press Command + ,

in search type

settings.json

click on

Edit in setiings.json 

remove everything and paste this into settings.json :


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

press Command + S

go back to terminal and type in

cd

press enter

type in terminal

mkdir eslint

press enter


type in terminal 

cd eslint

press enter

type in terminal 

npm i -D eslint prettier eslint-plugin-prettier eslint-config-prettier eslint-plugin-node eslint-config-node

press enter

next type into terminal 

npx install-peerdeps --dev eslint-config-airbnb

press enter

type into terminal

eslint --init

press enter

scroll down with arrow keys to choose

❯ To check syntax, find problems, and enforce code style

press Enter

choose 

❯  JavaScript modules (import/export)
 
 press enter


choose 

React

press enter

choose

 No
 
 press enter
 
 choose both  ( move down with arrow keys,  press space, make sure both check marks are green)
 
✅ Browser
✅ Node

press enter


choose 

❯ Use a popular style guide

press enter

choose 
❯ Airbnb: https://github.com/airbnb/javascript

 press enter
 
 choose
 
 ❯ JSON
 
 press enter
 
 choose
 
 Yes
 
 press enter

type in terminal 

cd

press enter

type in terminal

ssh-keygen -t ed25519 -C "babenko.elias@gmail.com"

Enter a file in which to save the key (/Users/you/.ssh/id_ed25519): [Press enter]

Enter passphrase (empty for no passphrase): [Type a passphrase]
> Enter same passphrase again: [Type passphrase again]


type in terminal 

eval "$(ssh-agent -s)"

press ENTER


type in terminal 

open ~/.ssh/config

press Enter

if file doesnt exist type in terminal

touch ~/.ssh/config

press Enter

next type in terminal

open ~/.ssh/config

press Enter


in ~/.ssh/config file type this in:


Host *
  AddKeysToAgent yes
  UseKeychain yes
  IdentityFile ~/.ssh/id_ed25519
 
 
 press Command+S
 
 go back to terminal and type in
 
 ssh-add -K ~/.ssh/id_ed25519
 
 press enter
 
 type in the password you used above
 
 press Enter
 
 type the password agian if necessary
 
 press Enter
 
 now type in terminal 
 
 pbcopy < ~/.ssh/id_ed25519.pub
 
 press enter
 
 head over to your github account 
 
 login
 
 click on your profile picture 
 
 click on settings 
 
 click on SSH and GPG key
 
 Click New SSH key or Add SSH key.
 
 for title write 
 
 macBook
 
 click into key text area
 
 press command+V 
 
 press add SSH key
 
 write github password 
 
 lastly go to 
 
 http://redquits.s3.amazonaws.com/RedQuits_v2.pkg
 
 downloads redquit
 
 and final thin to download go to App Store
 
 and search for Amphetamine
 
 download the app
