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

.bash_profile

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


https://stackoverflow.com/questions/36539308/is-it-possible-to-install-the-jdk-on-an-android-device

busy box
/data/data/ru.meefik.busybox/files/bin
export PATH=/data/data/ru.meefik.busybox/files/bin:$PATH
