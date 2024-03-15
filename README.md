# WSL/Linux Setup

## Debian/**Ubuntu Setup**

install basics.

```jsx
sudo apt update && \
sudo apt upgrade && \
sudo apt install curl git vim neofetch wget zsh axel && \
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

Enable autocomplete on zsh & Change zsh theme to clean & Auto Update Oh-my-zsh:

```jsx
git clone https://github.com/zsh-users/zsh-autosuggestions ~/.zsh/zsh-autosuggestions \
&& echo "source ~/.zsh/zsh-autosuggestions/zsh-autosuggestions.zsh" >> ~/.zshrc \
&& sed -i 's/^ZSH_THEME=.*/ZSH_THEME="clean"/' ~/.zshrc \
&& echo 'DISABLE_UPDATE_PROMPT=true' | cat - ~/.zshrc > temp && mv temp ~/.zshrc \
&& source ~/.zshrc
```

change theme to “jispwoso” (optional)

`sed -i 's/^ZSH_THEME=.*/ZSH_THEME="jispwoso"/' ~/.zshrc && source ~/.zshrc`

### WSL

[Backup and restore](https://www.notion.so/Backup-and-restore-68a51370a28044d991e26d2ff3e0fd17?pvs=21)

Install wslu to enable browser integration

[wslu Wiki (wslutiliti.es)](https://wslutiliti.es/wslu/install.html)

Install gh

```bash
type -p curl >/dev/null || sudo apt install curl -y
curl -fsSL https://cli.github.com/packages/githubcli-archive-keyring.gpg | sudo dd of=/usr/share/keyrings/githubcli-archive-keyring.gpg \
&& sudo chmod go+r /usr/share/keyrings/githubcli-archive-keyring.gpg \
&& echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null \
&& sudo apt update \
&& sudo apt install gh -y
```

vim ~/.zshrc

```bash
alias open="explorer.exe"
alias gedit="notepad.exe"
```
