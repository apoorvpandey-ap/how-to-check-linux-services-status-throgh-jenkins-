# how-to-check-linux-services-status-throgh-jenkins

### Step 1. Write a **sh** file on your Linux machine and write the below script. 
```
#!/bin/bash
SERVICE="wildfly"
STATUS="$(systemctl is-active wildfly.service)"
if [ "${STATUS}" = "active" ]; then
    echo "Execute your tasks ....."
else
    echo " Service not running.... so exiting "
    exit 1
fi
```
#
### Step 2. Make on a free-style project on Jenkins and give the path where you kept a sh script 
![image](https://user-images.githubusercontent.com/66588814/191163006-cd1d4727-feb1-4de6-a7d0-d8ebe50e3207.png)
#
### Step 3. Send an email if the service is not running so configure email notification, link https://youtu.be/R1zIU2HXq9c
![image](https://user-images.githubusercontent.com/66588814/191163272-7f2d25eb-6de3-441b-83e0-2d96cfa9b8e6.png)



