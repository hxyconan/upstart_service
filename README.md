## Intro
- Ansible role for prepare a customized upstart service which will be boot up automatically during system startup and auto restart when crashed
- The example there is running as webdriver with a TCP port
- The service will be run each time when server reboot
- The service will be restart automatically if crashed, try 5 times within 30 seconds, then giveup

## Commands
- The service can be stop/start via command
- Start and stop: 
``` sh
sudo service myservice start|stop|status|restart
```
- Manually kill process:
``` sh
sudo fuser -k [THE_RUNNING_PORT]/tcp
```
- Service log file: /var/log/myservice.log
- Process id logged at in: /var/run/myservice.pid
