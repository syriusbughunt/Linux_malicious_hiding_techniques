# PID hiding techniques
After searching on my own for clear and well detailed techniques to modify and hide processes in a Linux environment, I thought it could be a good idea to share what I've found with people who would like to learn the methods used by malicious users.

## 0x00 : Introduction on Linux processes

What Exactly is a 'process' ? A process is compiled source code that is currently running on the operating system. Today we will explore the details about a particular operating system; Linux. All processes have a process id or **PID**. Processes that start at system startup and keep running forever are called **daemon** processes or **daemons**. These **daemons** never die, unless you kill them. Those **daemon** processes  seems like a great way for malicious users to keep their malwares running :smirk:

## 0x01 : Discovering the running processes on your system

There is different ways to see the current running processes, the most common tools is named **ps**. To see the current processes running under your current user, we would use **ps xww** which should give you something similar to the screenshot below:  
  
<img src="https://github.com/syriusbughunt/PID_hiding_techniques/blob/master/img/capture01.jpg" width="1000"/>  
  
We could also use **ps auxww** to see all the running processes on the system, not only from our current user. To locate a process by his name, there is the **pgrep** command; *pgrep -l firefox* will return the following output in my shell:  
```
6839 firefox
```  
There is also the command **top** which will show you your current uptime, load average and running processes. I personally don't use it really often simply because I don't like the output that it gives me.  
  
We can choose to terminate a process by sending the **kill** command in our shell. If we wish to kill the previous PID we saw running firefox, the syntax to use would be *kill 6839* where 6839 is the PID running firefox.  
  
  
  
:point_right: CURRENTLY AWAY FROM KEYBOARD. WILL CONTINUE THIS LATER ! :point_left:
