## PPA

#### [Gnome Shell](#gnome-shell-1)
```bash
sudo add-apt-repository ppa:gnome3-team/gnome3
```
####   [Telegram](#telegram-2)
```bash
sudo add-apt-repository ppa:atareao/telegram
```
#### [numix-gtk-theme](#numix-gtk-theme-1)
```bash
sudo add-apt-repository ppa:numix/ppa
```
#### [Cinnamon](#cinnamon-1)
```bash
sudo add-apt-repository ppa:embrosyn/cinnamon
```
#### [Indicator](#indicator-1)
```bash
sudo add-apt-repository ppa:indicator-multiload/stable-daily
```
#### [grub customizer](#grub-customizer-1)
```bash
sudo add-apt-repository ppa:danielrichter2007/grub-customizer
```
#### [Oracle Java](#oracle-java-1)
```bash
sudo add-apt-repository ppa:webupd8team/java
```
#### [OBS-Studio](#obs-studio-1)
```bash
sudo add-apt-repository ppa:obsproject/obs-studio
```

---
## APPS

#### [All Applications](#all-applications) in line
```bash
sudo apt install git telegram chrome-gnome-shell numix-gtk-theme numix-icon-theme numix-icon-theme-circle gnome-alsamixer xclip indicator-multiload grub-customizer dconf-editor curl vlc gimp numlockx preload ruby-full compizconfig-settings-manager oracle-java8-installer clementine filezilla chkrootkit rkhunter gparted rawtherapee stellarium screenfetch obs-studio unity-tweak-tool wallch
```
#### Nvidia Drivers
```bash
sudo apt install nvidia-current
```
#### NVM (Node.js)
[Settings](#nvm-nodejs-settings)
```bash
sudo curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.2/install.sh | bash
nvm install <номер>
npm i -g bower browser-sync mocha gulp forever jshint pug-cli
```
#### Jekyll
```bash
sudo gem install jekyll bundler
```
#### Python 3.6.2
```bash
wget https://www.python.org/ftp/python/3.6.2/Python-3.6.2.tar.xz
tar xvf Python-3.6.2.tar.xz
cd Python-3.6.2/
./configure
sudo make altinstall
sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.5 1
sudo update-alternatives --install /usr/bin/python3 python3 /usr/bin/python3.6 2
sudo update-alternatives --config python3
```

---
## SETTINGS

#### Git
[Solved] Permission denied (publickey).
```bash
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_rsa
xclip -sel clip < ~/.ssh/id_rsa.pub
```
`Adding a new SSH key to your Git account`

#### Samba add local user
`sudo smbpasswd -a $USER`

#### on NumLock
```bash
sudo -s
echo "greeter-setup-script=/usr/bin/numlockx on" >> /usr/share/lightdm/lightdm.conf.d/50-unity-greeter.conf & exit
```

#### Add windows-1251 encoding
```bash
if [[ ! -n `grep 'windows-1251' ~/.profile` ]]; then echo 'export GST_ID3_TAG_ENCODING="windows-1251"' >> ~/.profile; fi
```
#### [NVM (Node.js)](#nvm-nodejs) Settings
```bash
nvm list
nvm use <номер>
nvm alias default node
remove

nvm deactivate <номер>
nvm uninstall <номер>
```
#### Add bash aliases
`Bash script`
```bash
#!/bin/bash
fileName=~/.bashrc
searchString='bash_aliases'

writeInFile() {
    echo 'if [ -f ~/.bash_aliases ]; then' >> $fileName
    echo '. ~/.bash_aliases' >> $fileName
    echo 'fi' >> $fileName
    cat $fileName
}

if [ -a $fileName ]; then
    if [ ! -n "$(grep $searchString $fileName)" ]; then
        writeInFile
    fi
else
    touch $fileName
    writeInFile
fi
```
#### Linux desktop managers
* GNOME3
```bash
sudo dpkg-reconfigure gdm
```
* Unity
```bash
sudo dpkg-reconfigure lightdm
```

#### Plymouth theme
`/usr/share/plymouth`
```bash
sudo update-alternatives --config default.plymouth
sudo update-initramfs -u
```

#### Preload  
```bash
sudo touch /var/lib/preload/preload.state
sudo chmod 600 /var/lib/preload/preload.state
sudo /etc/init.d/preload restart
```
Если вы хотите отредактировать настройки Preload откройте его конфигурацию данной командой:  
`sudo gedit /etc/preload.conf`  
Если нужно посмотреть логи демона воспользуйтесь командой ниже:  
`sudo tail -f /var/log/preload.log`

---
## LOCATIONS

#### Telegram
`/opt/telegram/Telegram`

#### Variables of folders in /home (~)
`~/.config/user-dirs.dirs`

#### Plymouth theme
`/usr/share/plymouth`
```bash
sudo update-alternatives --config default.plymouth
sudo update-initramfs -u
```

---
## All Applications


#### [Sublime Text 3](https://www.sublimetext.com/docs/3/linux_repositories.html#apt)
```bash
wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -
echo "deb https://download.sublimetext.com/ apt/stable/" | sudo tee /etc/apt/sources.list.d/sublime-text.list
```
#### Git
```bash
sudo apt install git
```
#### [Telegram](#telegram)
```bash
sudo apt install telegram
```
#### [Gnome Shell](#gnome-shell)
```bash
sudo apt install chrome-gnome-shell
```
#### [numix-gtk-theme](#numix-gtk-theme)
```bash
sudo apt install numix-gtk-theme numix-icon-theme numix-icon-theme-circle
```
#### Alsamixer
```bash
sudo apt install gnome-alsamixer
```
#### Clipboard
```bash
sudo apt install xclip
```
#### [Cinnamon](#cinnamon)
```bash
sudo apt install cinnamon blueberry
```
#### [Indicator](#indicator)
```bash
sudo apt install indicator-multiload
```
#### [grub customizer](#grub-customizer)
```bash
sudo apt install grub-customizer
```
#### dconf-editor
```bash
sudo apt install dconf-editor
```
#### cURL
```bash
sudo apt install curl
```
#### NumLock
```bash
sudo apt install numlockx
```
#### Preload
```bash
sudo apt install preload
```
#### Ruby
```bash
sudo apt install ruby-full
```
#### Jekyll
```bash
sudo gem install jekyll bundler
```
#### Node.js
```bash
sudo curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.2/install.sh | bash
nvm install <номер>
npm i -g bower browser-sync mocha gulp forever jshint
```
#### Gimp
```bash
sudo apt install gimp
```
#### VLC
```bash
sudo apt install vlc
```
#### ccsm
```bash
sudo apt install compizconfig-settings-manager
```
#### [Oracle Java](#oracle-java)
```bash
sudo apt install oracle-java8-installer
```
#### Clemantine Media Player
```bash
sudo apt install clemantine
```
#### FileZilla FTP-client
```bash
sudo apt install filezilla
```
#### [OBS-Studio](#obs-studio)
```bash
sudo apt install obs-studio
```
#### Wallpaper Change
```bash
sudo apt install wallch
```
#### Grub Repair
```bash
sudo add-apt-repository ppa:yannubuntu/boot-repair
sudo apt update
sudo apt install -y boot-repair && boot-repair
```

---
## CheckList

* [x] Автомонтирование дисков
* [x] Git
* [x] GitKraken
* [x] Nodejs
    * [x] bower 
    * [x] browser-sync 
    * [x] mocha 
    * [x] gulp 
    * [x] forever 
    * [x] jshint
    * [x] pug-cli
* [x] SublimeText
* [x] Browser
    * [x] Google Chrome
    * [x] Opera
* [x] Skype
* [x] Koala
* [x] TeamViewer
* [x] Gparted
* [x] VirtualBox
* [x] VLC
* [x] Gimp
* [x] Jekyll
* [x] Unity Tweak Tool
* [x] OBS-Studio
