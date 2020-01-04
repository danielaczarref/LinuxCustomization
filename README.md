# Linux Customization

Created this for my own personal use, in case I need to format my computer again. These are a few basic extra features/apps/etc I always install.

Feel free to check out my computer setup.

## Basic commands

* git
```
sudo apt-get install git
```

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
gedit ~/.bashrc
```

- Add do bash profile:

```
export ANDROID_HOME=~/Android/Sdk
export PATH=$PATH:$ANDROID_HOME/tools
export PATH=$PATH:$ANDROID_HOME/platform-tools

```
- Then run:
```
~/Android/Sdk/tools/bin/sdkmanager "platform-tools" "platforms;android-27" "build-tools;27.0.3"
```

## VirtualBox
```
sudo apt-get install virtualbox

```

## Genymotion

- Download: https://www.genymotion.com/fun-zone/

- Then, extract it to a folder of your preference. 

```
cd Downloads
chmod +x genymotion-2.2.2_x64.bin
./genymotion-2.2.2_x64.bin
cd genymotion
./genymotion

```

- Genymotion -> Settings -> ADB -> Use custom Android SDK Tools -> /home/daniela/Android/Sdk
 
    - Wait for "This folder is valid" message.

- Install Samsung Galaxy S8 - 7.0.0 API 24  or any other device of your preference

- Double click the device 

- Check the IP of your device emulator (it shows on the header of the device, you can expand it if necessary)

- run:
```
adb connect IP_OF_YOUR_EMULATOR:5555

adb devices

``` 
If if shows your device's name, then its successfully connected!
 
## Datagrip
```
sudo snap install datagrip --classic

```
## PostgreSQL
```
sudo apt update

sudo apt install postgresql postgresql-contrib

sudo -u postgres psql

\q

sudo -u postgres createuser --interactive

...

sudo -u postgres createdb db_name_here

sudo -u user_name psql db_name

ALTER USER user_name WITH PASSWORD 'new_password';

\q

```

Now it's possible to setup PostgreSQL connection to DataGrip!


