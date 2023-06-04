---

<h1 align="center">KVMD Armbian</h1>
<h3 align="center">Open and inexpensive DIY IP-KVM</h3>

---

<p align="center">
<img alt="Logo Banner" src="https://pikvm.org/img/site.svg"/>
</p>

---

KVMD Armbian merupakan software PiKVM yang bertujuan untuk membantu mengelola server atau workstation dari jarak jauh, terlepas dari kesehatan sistem operasi atau apakah sudah diinstal sistem operasi. Anda dapat memperbaiki masalah apa pun, mengonfigurasi BIOS, dan bahkan menginstal ulang OS menggunakan CD-ROM atau Flash Drive virtual. Karena harga Raspberry Pi yang tidak baik-baik saja, beberapa orang memulai project KVMD-ARMBIAN agar PiKVM dapat berjalan di Armbian.

Sumber KVMD Armbian dapat di akses ke halaman <a href="https://github.com/xe5700/kvmd-armbian" target="_blank">KVMD-ARMBIAN</a>.

---

## Syarat Install
- STB HG680P
- OS Armbian Debian Bookworm yang dapat di download pada halaman <a href="https://github.com/ophub/amlogic-s9xxx-armbian/releases" target="_blank">amlogic-s9xxx</a>.
<br> Note : cari dengan code name `amlogic_s905x`
- USB HDMI Capture
- Kabel USB to USB

---

## Step by Step Install KVMD Armbian

1. Update dan upgrade sistem
```
apt update && apt upgrade -y
```

2. Install software pendukung dan restart
```
apt install -y avahi-daemon ntp && reboot
```

3. Clone project kvmd-armbian dan masuk ke folder clone
```
git clone https://github.com/xe5700/kvmd-armbian.git && cd kvmd-armbian
```

4. Backup install.sh dan config.sh dari project kvmd-armbian
```
mv install.sh install.sh.bak && mv config.sh config.sh.bak
```

5. Download install.sh dan config.sh untuk STB Armbian
```
wget https://raw.githubusercontent.com/animegasan/kvmd/main/install.sh && wget https://raw.githubusercontent.com/animegasan/kvmd/main/config.sh && chmod +x install.sh
```

6. Install part 1 KVMD Armbian
```
./install.sh
```
Note : Pada bagian `Do you want to apply custom patches?  [y/n]` pilih N

7. Install part 2 KVMD Armbian
```
cd kvmd-armbian && ./install.sh
```
Note : Pada bagian `Did kvmd -m run properly?  [y/n]` pilih Y

---
