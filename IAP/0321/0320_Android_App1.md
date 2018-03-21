1. Tera Term : Serial, Baud rate : 115200
2. root (su)
3. adbd 5555 &

Error 1 : adbd 5555 &
    cannot bind 'tcp:5037'
    Solve : Network Setting Change (wtf)

4. adbd connect 192.168.xxx.xxx:5555

Error 2 : AndroidManifest.xml
    error line : <activity android:name=".MainActivity">
    Can't download files while building projects
    Solve : Network Connect

Error 3 : adbd 5555 & / adbd connect 192.168.xxx.xxx:5555
    cannot bind 'tcp:5037'
    about 20min suffered
    PC IP : 192.168.1.11 / Device IP : 192.168.1.11
    Solve : ip has to different ip address but same band
    so i set pc ip 192.168.1.11 and device ip 192.168.1.10


Assign : Android Activity lifecycle