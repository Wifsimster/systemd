# Installation First Kit for Raspberry Pie

## Root password

<!-- Define a root password -->
```shell
$ sudo passwd root
```

## Add NAS directories

<!-- Create NAS directories -->
```
cd mnt/
mkdir downloads
mkdir incompletes
mkdir movies
mkdir musics
mkdir tv_shows
mkdir photos
```

<!-- Add permissions to new directories -->
```
chmod 777 *
chown nobody:nogroup *
```

<!-- Write fstab -->
```
nano etc/fstab
```

<!-- Write fstab -->
```
nano etc/cifspasswd
```