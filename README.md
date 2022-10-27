# My dotfiles for linux

### Ubuntu (apt)
 - Copy the bash code below, create a file with an extension .sh you can run
 - Make it executable with the chmod sudo command +x NOME_DO_ARQUIVO
 - Run by placing a ./ before the file and it will run automatically, for example: ./script.sh

---

#!/bin/bash

sudo apt update -y
sudo apt upgrade -y

sudo apt install git curl zsh -y

sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)" -y

bash -c "$(curl --fail --show-error --silent --location https://raw.githubusercontent.com/zdharma-continuum/zinit/HEAD/scripts/install.sh)" -y

git clone https://github.com/spaceship-prompt/spaceship-prompt.git "$ZSH_CUSTOM/themes/spaceship-prompt" --depth=1

ln -s "$ZSH_CUSTOM/themes/spaceship-prompt/spaceship.zsh-theme" "$ZSH_CUSTOM/themes/spaceship.zsh-theme"

echo zinit light zsh-users/zsh-autosuggestions >> ~/.zshrc

echo zinit light zsh-users/zsh-completions >> ~/.zshrc

echo zinit light zdharma-continuum/fast-syntax-highlighting >> ~/.zshrc

echo unsetopt PROMPT_SP >> ~/.zshrc

sudo chsh -s $(which zsh) -Y

curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.2/install.sh | bash
nvm install --lts

#END

---
