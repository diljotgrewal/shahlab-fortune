# shahlab-fortune
fortune database of quotes from shahlab members


## Usage:

These instructions are for ubuntu systems.

#### Clone this repo 

```
git clone https://github.com/diljotgrewal/shahlab-fortune.git
cd shahlab-fortune
```


#### Install cowsay and fortune on your machine:

```
apt install fortune cowsay
```

#### prep database for fortune

run:
```
strfile shahlab_fortune
```

#### copy database to fortune dir

```
sudo cp shahlab_fortune*  /usr/share/games/fortunes/
```


#### check if the installation worked

```
/usr/games/fortune shahlab_fortune | /usr/games/cowsay -n
```

should print a quote.


#### add it to MOTD

create a shell script:
```
sudo vim  /etc/profile.d/motd.sh
```

and add the following to the file.
```
/usr/games/fortune shahlab_fortune | /usr/games/cowsay -n
```


The MOTD will now be displayed on sign in.

````

Your Ubuntu release is not supported anymore.
For upgrade information, please visit:
http://www.ubuntu.com/releaseendoflife

New release '19.04' available.
Run 'do-release-upgrade' to upgrade to it.


Last login: Mon Sep  9 21:14:20 2019 from 140.163.254.133
 _________________________________________________
/ Tyler:                                          \
\ "communal suffering is a form of team building" /
 -------------------------------------------------
        \   ^__^
         \  (oo)\_______
            (__)\       )\/\
                ||----w |
                ||     ||
``` 
