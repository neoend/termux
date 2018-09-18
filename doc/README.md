## /system/bin
~~~
$ cd /system/bin
$ ./dumpsys
CANNOT LINK EXECUTABLE "./dumpsys": cannot locate symbol "XzUnpacker_Construct" referenced by "/system/lib64/libunwind.so"...
Aborted
$ export LD_LIBRARY_PATH=/system/lib64:$LD_LIBRARY_PATH
$ ./dumpsys
...
DUMP OF SERVICE backup:
Permission Denial: can't dump BackupManagerService from from pid=15581, uid=10131 due to missing android.permission.DUMP permission
...
~~~
Only system app can have DUMP permission. :(


## clang
~~~
clang/stable 6.0.1 aarch64
  C language frontend for LLVM

libclang/stable 6.0.1 aarch64
  C language frontend library for LLVM

libclang-dev/stable 6.0.1 aarch64
  C language frontend library for LLVM
~~~

## nmap
~~~
$ pkg install openssl
$ pkg install nmap
$ nmap -sS -p 1-65535 127.0.0.1
You requested a scan type which requires root privileges.
QUITTING!
$ pkg install tsu
$ tsu
/data/data/com.termux/files/usr/bin/tsu: 139: exec: : Permission denied
$ 
~~~
Rooting is required for tsu.

[PRoot](https://wiki.termux.com/wiki/PRoot)
