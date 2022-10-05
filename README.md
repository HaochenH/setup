# setup
setup of terminal and others

# .zshrc setup
# .zshrc

**enable auto suggestions:** 

`git clone [https://github.com/zsh-users/zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions) ~/.zsh/zsh-autosuggestions`

Finally, add the following command to your .zshrc file:

`source ~/.zsh/zsh-autosuggestions/zsh-autosuggestions.zsh`

---

`vim ~/.zshrc`

alias startconda='export PATH="/home/$USER/anaconda3/bin:$PATH"’

alias ztheme='(){ export ZSH_THEME="$@" && source $ZSH/oh-my-zsh.sh }'

ztheme simple

---

export BROWSER=wslview

alias dev="cd ~/dev"

dev
alias push="git push"
alias pull="git fetch && git pull"