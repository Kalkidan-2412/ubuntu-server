# *SYSTEM CALL*

## Contents
- [System call](#system-call)
- [Shutdown system call](#shutdown-system-call)
  - [Common options used in conjunction with the shutdown command](#common-options-used-in-conjunction-with-the-shutdown-command)
  - [Abnormal system shutdowns and reboots](#abnormal-system-shutdowns-and-reboots)
- [C program to shut down a Linux PC](#c-program-to-shut-down-a-linux-pc)
- [C program to shut down a Windows PC](#c-program-to-shut-down-a-windows-pc)
- [Reference](#reference)






# System call
A system call is a programmatic way in which a computer program requests a service from the 
kernel of the operating system on which it is executed. A system call is a way for programs 
to interact with the operating system. A computer program makes a system call when it 
requests the operating system’s kernel. System call provides the services of the operating system 
to the user programs via the Application Program Interface(API). System calls are the only entry 
points into the kernel system and are executed in kernel mode.

# Shutdown system call 
A shutdown is a mechanism for safely shutting down the system. In this process, all logged-in 
users are first notified that the system will be turned off, and in the last five minutes, new logins 
are prevented. 
A simple C program is displayed that shuts down a PC by calling internal OS features. This type 
of functionality can be helpful where sometimes you have to shut down or restart the PC due to 
some requirement, like after updating the system driver. 
shutdown [options] [time] [message] 
• Options: This specifies the action to be taken (e.g., halt, reboot). 
• Time: Defines when the specified action should occur. 
• Message: A custom message to display to actively logged in users before the shutdown
