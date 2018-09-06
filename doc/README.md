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
Only system app can have DUMP permission. :)

