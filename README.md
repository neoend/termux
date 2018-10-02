# termux

~~~sh
Welcome to Termux!

Wiki:            https://wiki.termux.com
Community forum: https://termux.com/community
IRC channel:     #termux on freenode
Gitter chat:     https://gitter.im/termux/termux
Mailing list:    termux+subscribe@groups.io

Search packages:   pkg search <query>
Install a package: pkg install <package>
Upgrade packages:  pkg upgrade
Learn more:        pkg help

$ pwd
/data/data/com.termux/files/home
~~~



## external storage 접근  
https://termux.com/storage.html
~~~sh
$ termux-setup-storage
~~~

https://github.com/termux/termux-app/issues/449  
It's possible to create the symlink to storage manually:
~~~sh
$ ln -s /storage/emulated/0 storage
~~~

## SSH 서버
~~~sh
$ pkg install dropbear
~~~
~/.ssh/authorized_keys 에 private key 추가하면 login 없이 접속 가능.

no supported authentication methods available 에러가 발생할 경우
https://superuser.com/questions/310522/disconnected-no-supported-authentication-methods-available
~~~sh
chmod g-w ~/
chmod 700 ~/.ssh
chmod 600 ~/.ssh/authorized_keys
~~~

## JAVA
https://archive.org/details/openjdk-9-jre-headless_9.2017.8.20-1_x86_64
~~~sh
$ dpkg -i openjdk9_9.2017.8.20_aarch64.deb
~~~

## busy box
~~~
/data/data/ru.meefik.busybox/files/bin
export PATH=/data/data/ru.meefik.busybox/files/bin:$PATH
~~~

## HTTPD  
http://redmine.lighttpd.net/projects/lighttpd/wiki/TutorialConfiguration
~~~sh
$ pkg install lighttpd
~~~
~~~sh
server.document-root = "/data/data/com.termux/files/home/www" 

server.port = 8080

server.username = "www" 
server.groupname = "www" 

mimetype.assign = (
  ".html" => "text/html", 
  ".txt" => "text/plain",
  ".jpg" => "image/jpeg",
  ".png" => "image/png" 
)

static-file.exclude-extensions = ( ".fcgi", ".php", ".rb", "~", ".inc" )
index-file.names = ( "index.html" )
~~~


How To Install Metasploit-Framework In Android via Termux [Without Root](Termux-tutorial:#11)  
https://www.youtube.com/watch?v=yn9T4M0IpSc

