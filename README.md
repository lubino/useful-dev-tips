# useful-dev-tips
A bunch of useful tips for developers

## logs over TCP/IP
Sometimes it is useful to have all logs in one place. One of simple ideas to do is to open a TCP/IP socket server and write everything what comes to a file:
```bash
nc -l -k -p 3002 >> ~/central.log
```

Then anything you want to log into that 'central.log' file just run with pipe:
```bash
./start.sh | nc localhost 13001
```
\* you can specify the real IP address or hostname of your machine, and then you can centralize your logs over more nodes or servers.

To watch the logs:
```bash
tail -f ~/central.log
```
