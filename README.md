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