# Installation First Kit for Raspberry Pi

## Root password

Define a root password

```Shell
sudo passwd root
```

## Add NAS directories

Create NAS directories

```Shell
cd mnt/
mkdir downloads
mkdir incompletes
mkdir movies
mkdir musics
mkdir tv_shows
mkdir photos
```

Add permissions to new directories

```Shell
chmod 777 *
chown nobody:nogroup *
```

Write fstab

```Shell
nano etc/fstab
```

Write fstab

```Shell
nano etc/cifspasswd
```

## How to install Plex Media Server on Debian Jessie

Edit update list

```Shell
nano /etc/apt/sources.list
```

Add new list to sources.list

```Shell
deb http://shell.ninthgate.se/packages/debian wheezy main
```

Register a new key for the new update list

```Shell
wget http://shell.ninthgate.se/packages/shell-ninthgate-se-keyring.key
apt-key add shell-ninthgate-se-keyring.key
```

Update & install Plex

```Shell
apt-get update
apt-get install plexmediaserver
```

Enable Plex service

```Shell
systemctl enable plexmediaserver.service
```

Access it with : http:192.168.0.x:324000/web/index.html

## How to add Plex Trakt Scrobbler

cd  /var/lib/plexmediaserver/Library/Application Support/Plex Media Server/Plug-ins
apt-get install git-core
git clone https://github.com/trakt/Plex-Trakt-Scrobbler
mv /Plex-Trajt-Scrobbler/Trakttv.bundle /var/lib/plexmediaserver/Library/Application Support/Plex Media Server/Plug-ins
rm -r Plex-Trakt-Scrobbler
systemctl restart plexmediaserver.service