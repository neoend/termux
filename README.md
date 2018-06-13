# termux

~~~sh
$ pwd
/data/data/com.termux/files/home
~~~

.bash_profile

external storage 접근  
https://termux.com/storage.html
~~~sh
$ termux-setup-storage
~~~

https://github.com/termux/termux-app/issues/449  
It's possible to create the symlink to storage manually:
~~~sh
$ ln -s /storage/emulated/0 storage
~~~

SSH 서버
~~~sh
$ pkg install dropbear
~~~
~/.ssh/authorized_keys 에 private key 추가하면 login 없이 접속 가능.

HTTPD  
http://redmine.lighttpd.net/projects/lighttpd/wiki/TutorialConfiguration
~~~sh
$ pkg install lighttpd
~~~

How To Install Metasploit-Framework In Android via Termux [Without Root](Termux-tutorial:#11)  
https://www.youtube.com/watch?v=yn9T4M0IpSc


https://stackoverflow.com/questions/36539308/is-it-possible-to-install-the-jdk-on-an-android-device

busy box
/data/data/ru.meefik.busybox/files/bin
export PATH=/data/data/ru.meefik.busybox/files/bin:$PATH
