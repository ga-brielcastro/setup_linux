# My dotfiles for linux
### Ubuntu (apt)
Instalar os pacotes iniciais
```sudo apt install git zsh curl```

#### OhMyZsh

Configurar OhMyZsh
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
Configurar o zinit para OhMyZsh
```
bash -c "$(curl --fail --show-error --silent --location https://raw.githubusercontent.com/zdharma-continuum/zinit/HEAD/scripts/install.sh)"
```

Adicionar o código abaixo no .zshrc (obs: estas são minhas configurações, pode substituir para o caminho das suas)

```
# Plugins
zinit light zsh-users/zsh-autosuggestions
zinit light zsh-users/zsh-completions
zinit light zdharma-continuum/fast-syntax-highlighting

# Hide % on start
unsetopt PROMPT_SP

# Flutter
export PATH="/home/gabriel/DevTools/flutter/bin:$PATH"

# Java
export JAVA_HOME=/usr/lib/jvm/java-11-openjdk-11.0.12.0.7-4.fc35.x86_64

# Android Studio
export ANDROID_HOME=~/Android/Sdk
export PATH=$PATH:$ANDROID_HOME/emulator
export PATH=$PATH:$ANDROID_HOME/tools
export PATH=$PATH:$ANDROID_HOME/tools/bin
export PATH=$PATH:$ANDROID_HOME/platform-tools

# NVM
export NVM_DIR=~/.nvm
 [ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh"

```

Definir o zsh como padrão
```chsh -s $(which zsh)```

Agora pode reiniciar ou logout que o zsh estará setado como padrão ou pode rodar ```source .zshrc``` que ele irá trocar também.

#### NVM

Instalar o nvm
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
```

Instalar a versão LTS do node
```nvm install --lts```

#### Angular CLI

Instalar a versão do angular globalmente
```
npm install @angular/cli --localhost=global
```
