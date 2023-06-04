# kvmd

Persyaratan untuk menginstall KVMD di STB Armbian adalah menggunakan Debian Bookworm yang dapat di download pada link berikut
https://github.com/ophub/amlogic-s9xxx-armbian/releases

Cari dengan code name `amlogic_s905x`

- USB HDMI Capture
- USB to USB

1. Update dan upgrade sistem
```
apt update && apt upgrade -y
```

2. Install software pendukung dan restart STB Armbian
```
apt install -y avahi-daemon ntp && reboot
```

3. Clone project kvmd-armbian dan masuk ke folder clone
```
git clone https://github.com/xe5700/kvmd-armbian.git && cd kvmd-armbian
```

4. Backup install.sh dan config.sh
```
mv install.sh install.sh.bak && mv config.sh config.sh.bak
```

5. Download install.sh dan config.sh untuk STB Armbian
```
wget https://raw.githubusercontent.com/animegasan/kvmd/main/install.sh && wget https://raw.githubusercontent.com/animegasan/kvmd/main/config.sh && chmod +x install.sh
```

6. Install part 1 kvmd armbian
```
./install.sh
```
Note : Pada bagian `Do you want to apply custom patches?  [y/n]` pilih N

7. Install part 2 kvmd armbian
```
cd kvmd-armbian && ./install.sh
```
