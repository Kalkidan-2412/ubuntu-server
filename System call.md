# *SYSTEM CALL*

## Contents
- [System call](#system-call)
- [Shutdown system call](#shutdown-system-call)
  - [Common options used in conjunction with the shutdown command](#common-options-used-in-conjunction-with-the-shutdown-command)
  - [Abnormal system shutdowns and reboots](#abnormal-system-shutdowns-and-reboots)
- [C program to shut down a Windows PC](#c-program-to-shut-down-a-windows-pc)
- [C program to shut down a Linux PC](#c-program-to-shut-down-a-linux-pc)
- [Reference](#reference)






# System call
A system call is a programmatic way in which a computer program requests a service from the 
kernel of the operating system on which it is executed. A system call is a way for programs 
to interact with the operating system. A computer program makes a system call when it 
requests the operating system’s kernel. System call provides the services of the operating system 
to the user programs via the Application Program Interface(API). System calls are the only entry 
points into the kernel system and are executed in kernel mode.

# Shutdown system call 
A shutdown is a mechanism for safely shutting down the system. In this process, all logged-in users are first notified that the system will be turned off, and in the last five minutes, new logins are prevented. 
A simple C program is displayed that shuts down a PC by calling internal OS features. This type of functionality can be helpful where sometimes you have to shut down or restart the PC due to some requirement, like after updating the system driver.

<mark> shutdown [options] [time] [message] </mark>

  • **Options**: This specifies the action to be taken (e.g., halt, reboot).
  
  • **Time**: Defines when the specified action should occur. 
  
  • **Message**: A custom message to display to actively logged in users before the shutdown.

### Common options used in conjunction with the shutdown command:
The shutdown command in Linux is versatile, allowing for various operations related to shutting down the system.  
- **h or --halt**: Halts the system by stopping all the CPU functions immediately.
- **r or --reboot**: Reboots the system after shutting down.
- **c or --cancel**: Cancels a scheduled shutdown or reboot. 
- **k or --kmsg**: Sends a warning message to all logged-in users without actually shutting down.
- **-n or --no-wait**: Instructs the system to shut down without waiting for processes to terminate gracefully.
- **-t or --time**: Specifies the time at which the system should be shut down. 

Here's a complete breakdown of the different commands used to shut down your Linux system: 

1) Shutting the system down immediately
    
 `sudo shutdown -h now` 

The command "sudo shutdown -h now" initiates an immediate system shutdown on a Linux system.
 
2) Restarting the system on Linux
   
`sudo shutdown -r now ` 

The command "sudo shutdown -r now" is used to initiate a system shutdown and restartimmediately on Linux. 

3) Scheduling a shutdown on Linux
   
You might need to reboot machines at odd hours. Being able to instruct the machine to shut down on its own will save you the trouble of manually doing so. 

There are two ways to go about scheduling a shutdown on Linux systems. You can either specify the exact time at which the system needs to be shut down, or shut down the system in "n" minutes from a particular time. 

`sudo shutdown -h +10`

The above command will schedule a shutdown in 10 minutes from the moment the command is executed. 

`sudo shutdown -h 09:00 `

In this command, the timestamp "09:00" indicates the specific time at which the system should be shut down. 

4) Force shutting and force starting the system on Linux
    
You'll inevitably have situations where the systems will act up and refuse to shut down. In such cases, you can execute the following command to enable a force shutdown of your system. 

`sudo systemctl poweroff --force` 

or

`sudo systemctl reboot --force `

If this does not work, you can use the command with the --force option twice. 

`sudo systemctl poweroff --force --force`

The above command is akin to unplugging the machine and should only be used as a last resort, as it bypasses standard shutdown procedures.

5) Broadcasting a custom message at the time of shutdown
   
This option allows you to send out a message to all system users notifying them of when the shutdown will take place. This gives everyone the chance to save their work and log off safely before the system shuts down. 

`sudo shutdown +30 "System will shut down in 20 minutes. Please save your work."`

6) Canceling a scheduled shutdown 

`sudo shutdown -c`

By executing this command, you can cancel a previously scheduled shutdown.

### Abnormal system shutdowns and reboots:

Unexpected shutdowns and reboots are the last thing you want as an administrator. If a critical system experiences this, any unsaved data in the applications will be lost. This includes documents and files that were open at the time of a shutdown. 

You can check the shutdown history of a system using the following command: 

`last shutdown -x | more`

This command used to display a list of the most recent login sessions and system shutdowns, providing a summary of user activity and system events. 

• **last:** This command retrieves the login history of users on the system by reading from the /var/log/wtmp file. It shows information such as usernames,terminal names, login times, and durations of sessions. 

• **-x:** This option extends the output to include system shutdowns and run level changes, allowing you to see when the system was shut down or rebooted alongside user logins. 

• **| more:** Sends the output of the last -x command to more, which allows you to view the output one screen at a time. This is particularly useful for long outputs that exceed the terminal's display capacity. 

The entries in the output show two timestamps, where the first timestamp is for system shutdown and the second is for system startup.
### C program to shut down a Windows PC

A simple C program to shuts down a Windows PC by calling internal Windows features:
```
#include <stdio.h> 
#include <stdlib.h> 
int main() 
{ 
system("c:\\windows\\system32\\shutdown /i"); 
return 0; 
} 

```

### C program to shut down a Linux PC

To do the same thing in Linux, you have to change the command parameter; the rest of the code will remain the same. 
```
#include <stdio.h> 
#include <stdlib.h> 
int main() 
{ 
// Running Linux OS command using system 
system("shutdown -P now"); 
return 0; 
}
```
### Reference

https://www.manageengine.com/products/eventlog/kb/linux/linux-shutdown-command.html

https://www.geeksforgeeks.org/introduction-of-system-call/

https://www.w3schools.in/c-programming/examples/c-program-to-shutdown-windows-and-linux-systems

