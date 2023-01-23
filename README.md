# web-htop
HTOP with web interface 
```
apt install shellinabox -y
service shellinabox stop
update-rc.d -f shellinabox remove
shellinaboxd -t -b -p 8080 --no-beep -s '/htop/:nobody:nogroup:/:htop -d 10'
```

Опции:
```
Options:
-t — disable ssl (if necessary, not recommended for public servers)
-b — run in background
-p — web server port number
--no-beep — disable annoying beeps
-s '…commands…' — session configurstion, where
/htop/ — URL
nobody:nogroup — user and group for session (nobody:no group chosen for security reasons)
htop -d 10 — command (actually session shell): run htop with -d 10 argument (means update every second)
```
Now go to browser and navigate to
```
http://you_server_address:8080/htop/
```
