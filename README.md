# Linux Customization

Created this for my own personal use, in case I need to format my computer again. These are a few basic extra features/apps/etc I always install.

Feel free to check out my computer setup.

## Basic commands

* snap
```
sudo apt install snapd

``` 

* curl
```
sudo apt-get install curl
```

* gedit
```
sudo snap install gedit
``` 

* graphic libs
```
sudo apt-get install gcc-multilib lib32z1 lib32stdc++6
```

## Telegram desktop

``` 
sudo snap install telegram-desktop

``` 

## Guake Terminal

```
sudo apt-get install guake -y

```

## Icon Theme

```
sudo add-apt-repository ppa:papirus/papirus

sudo apt update

sudo apt-get install papirus-icon-theme

```

## Caffeine Extension

```
sudo add-apt-repository ppa:caffeine-developers/ppa

sudo apt-get update

sudo apt-get install caffeine

``` 

## VSCode

```
sudo snap install --classic code

```

## McOs-Mint-Cinnamon Theme

https://www.cinnamon-look.org/p/1247470/

## NodeJs

```
sudo apt-get install nodejs

```

# Yarn 

```
curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -

echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list

sudo apt update && sudo apt install yarn

```

Add to gedit ~/.bashrc : 
´´´
export PATH="$PATH:$(yarn global bin)" 

´´´

## React Native Cli

```
yarn global add react-native-cli

```

## JDK 8
```
sudo add-apt-repository ppa:openjdk-r/ppa

sudo apt-get update

sudo apt-get install openjdk-8-jdk

```

## Check Java version and change to version 8 if necessary
``` 
java -version

sudo update-alternatives --config java

```

## Pacapt/Pacman
```
sudo wget -O /usr/local/bin/pacapt https://github.com/icy/pacapt/raw/ng/pacapt

sudo chmod 755 /usr/local/bin/pacapt

sudo ln -sv /usr/local/bin/pacapt /usr/local/bin/pacman || true

```

## Android SDK Command Line Tools Only

https://developer.android.com/studio/#downloads

## Setup SDK
```
mkdir Android
cd Android
mkdir Sdk
cd
cd Downloads
unzip sdk-tools-linux-4333796.zip -d /home/usr/Android/Sdk


