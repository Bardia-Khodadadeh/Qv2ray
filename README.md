# Installing qv2ray on Ubuntu
``` bash
mkdir ~/temp
cd temp
sudo add-apt-repository universe
sudo apt install libfuse2
wget -O ~/Qv2ray.AppImage https://github.com/Qv2ray/Qv2ray/releases/download/v2.7.0/Qv2ray-v2.7.0-linux-x64.AppImage
sudo apt update
wget -O v2ray_core.zip https://github.com/v2ray/v2ray-core/releases/download/v4.28.2/v2ray-linux-64.zip
sudo apt-get install unzip
cd ~
chmod a+x Qv2ray.AppImage
sudo ./Qv2ray.AppImage
cd /home/$(whoami)/.config
mkdir qv2ray
cd qv2ray
mkdir vcore
unzip /home/$(whoami)/temp/v2ray_core.zip -d /home/$(whoami)/.config/qv2ray/vcore
rm ~/temp/v2ray_core.zip
cd ~/Qv2ray
tar -xvzf assets.tar.gz 
mv /home/$(whoami)/Qv2ray/assets /home/$(whoami)/.config/qv2ray/
``` 
#### changing contents of .desktop file
``` bash
cd /home/$(whoami)/.config/qv2ray
sudo cp /home/$(whoami)/.config/qv2ray/assets/v2ray//icon.jpeg /home/$(whoami)/.config/qv2ray/icon.jpeg
sudo mv ~/Qv2ray.AppImage /home/$(whoami)/.config/qv2ray/Qv2ray.AppImage
sudo cp /home/$(whoami)/.config/qv2ray/assets/v2ray/qv2ray.desktop ~/.local/share/applications/qv2ray.desktop
```
