# *UBUNTU SERVER*

# CONTENTS

- [Introduction](#introduction)
  - [What is Ubuntu Server?](#what-is-ubuntu-server)
  - [Difference between Ubuntu Desktop and Ubuntu Server](#difference-between-ubuntu-desktop-and-ubuntu-server)
  - [Key Features](#key-features)
  - [Ubuntu Meaning and History](#ubuntu-meaning-and-history)
  - [Motivation](#motivation)
- [Objectives](#objectives)
- [System Requirements](#system-requirements)
- [How to Install Ubuntu Server](#how-to-install-ubuntu-server)
- [Issues or Problems Faced](#issues-or-problems-faced)
- [Filesystem Support](#filesystem-support)
  - [Fully Supported Filesystems](#fully-supported-filesystems)
  - [Partially Supported Filesystems](#partially-supported-filesystems)
  - [Why Ext4 is Default](#why-ext4-is-default)
- [Advantages](#advantages)
- [Disadvantages and Key Limitations](#disadvantages-and-key-limitations)
- [Recommendations for Improvement](#recommendations-for-improvement)
  - [User-Centric Future Vision](#user-centric-future-vision)
- [Conclusion](#conclusion)
- [Virtualization in Modern Operating Systems](#virtualization-in-modern-operating-systems)
  - [What is Virtualization?](#what-is-virtualization)
  - [Benefits of Virtualization](#benefits-of-virtualization)
  - [Main Components of Virtualization](#main-components-of-virtualization)
    - [Physical Machine](#physical-machine)
    - [Virtual Machine](#virtual-machine)
    - [Hypervisors](#hypervisors)
- [How Virtualization Works](#how-virtualization-works)
- [Reference](#reference)
  
![Ununtu server](Images/Picture1.jpg)

# Introduction
## What is Ubuntu Server?

Ubuntu Server is a version of the Ubuntu operating system designed and engineered as a backbone for the internet. Ubuntu Server brings economic and technical scalability to your datacenter, public or private. Whether you want to deploy an OpenStack cloud, a Kubernetes cluster or a 50,000-node render farm, Ubuntu Server delivers the best value scale-out 
performance available. 

Ubuntu Server is a popular and dependable open-source operating system tailored for servers and cloud computing settings. It is a good choice for businesses and individuals seeking a reliable, ecure, and flexible operating system. Setting up Ubuntu Server in a virtual environmentprovides a versatile and economical option for businesses, developers, and IT professionals seeking to manage and implement servers without the need for dedicated physical hardware. 

Ubuntu Server is a variant of the Ubuntu operating system, specifically designed for server environments. Built on the Linux kernel, it provides a stable platform for hosting websites, running applications, and managing network services.  

 ## Difference between Ubuntu Desktop and Ubuntu Server 

 The main difference between Ubuntu Desktop and Server is the desktop environment. While Ubuntu Desktop includes a graphical user interface (GUI), Ubuntu Server does not. When choosing between Ubuntu Server and Ubuntu Desktop, the most important differences revolve around their intended use cases and interfaces. Ubuntu Desktop is designed for general personal computing, featuring a user-friendly graphical user interface (GUI) that is ideal for tasks like web browsing, office work, and media consumption. 

Ubuntu Server, on the other hand, is tailored for running network services, web hosting, and enterprise applications, relying on a command-line interface (CLI) to optimize performance and resource efficiency. Unlike the desktop version, Ubuntu Server doesn’t include a graphical user interface by default, making it lighter and more efficient for server use. Understanding these 
distinctions can help you select the appropriate version for your needs, whether it’s for everyday use, server management, or specific business applications. 

You should use Ubuntu Desktop to use your computer as a daily driver. It includes a bevy of multimedia and productivity software. There's a GUI, and installation is pretty simple. Moreover, you can install server software to use Ubuntu Desktop as a server.

## Key Features

One of its distinguishing features is its Long-Term Support (LTS) versions, which ensure stability and security updates for a minimum of five years. These attributes make Ubuntu Server particularly suited for environments requiring consistent performance and minimal downtime.

Key features of Ubuntu Server include: 

• Command-line interface for efficient remote management

• Lower resource requirements compared to desktop versions 

• Built-in security features and regular security updates 

• Support for a wide range of server applications and services 

• Scalability to meet growing business needs

## Ubuntu Meaning and History

The name “Ubuntu” comes from an African philosophy meaning “humanity to others” or “I am what I am because of who we all are.” This reflects the collaborative nature of the open-source community behind Ubuntu. Ubuntu Server is a Linux-based operating system developed by Canonical Ltd., designed for servers and cloud computing environments. It is derived from Debian and is composed mostly of free and open-source software Canonical, the company founded by South African entrepreneur Mark Shuttleworth, released the first version of Ubuntu in 2004. Ubuntu Server is built on Debian architecture and is composed mostly of free and opensource software. 

The history of Ubuntu Server dates back to the first release of Ubuntu in 2004. Initially, Ubuntu was perceived as a desktop-focused operating system, but its server capabilities were present from the beginning. Canonical, the company behind Ubuntu, emphasized its server potential by renaming the "Custom" installation mode to "Server," which marked the formal recognition ofUbuntu Server. Over time, Ubuntu Server gained popularity for its simplicity, reliability, and support for features like RAID and LVM, making it a strong choice for server users.

## Motivation

The motivation to choose Ubuntu Server stems from its compatibility with a wide range of hardware and virtualization technologies. As organizations continue transitioning to virtualized and cloud-based infrastructures, the need for an operating system that offers high scalability, cost efficiency, and robust performance becomes critical. Ubuntu Server is optimized for virtual environments such as VMware Workstation and Oracle VM VirtualBox, making it an ideal 
candidate for learning, development, and enterprise-level deployment. 

Additionally, its extensive documentation and community support lower the entry barrier for administrators, developers, and businesses looking to deploy an efficient and reliable server solution. With security at its core and support for advanced tools like Kubernetes and OpenStack, Ubuntu Server meets the demands of modern IT landscapes.

# Objectives

The objectives of the Ubuntu Server operating system are centered around providing a reliable, secure, and efficient platform for server environments. Here are some of its key objectives: 

1. **Stability and Reliability:** Ubuntu Server aims to deliver a stable and dependable operating system for hosting critical applications, ensuring minimal downtime and consistent performance. 

2. **Security:** It prioritizes robust security features, including regular updates, built-in firewalls, and support for encryption, to protect sensitive data and systems. 

3. **Scalability:** Designed to scale with growing business needs, Ubuntu Server supports a wide range of hardware and virtualization platforms, making it suitable for small-scale deployments and large enterprise infrastructures. 

4. **Flexibility:** The operating system is highly customizable, allowing users to tailor it to their specific requirements, whether for web hosting, database management, or cloud computing. 

5. **Cloud and Virtualization Support:** It is optimized for modern IT environments, offering seamless integration with cloud platforms like OpenStack and Kubernetes, as well as virtualization tools like VMware and VirtualBox. 

6. **Open-Source Philosophy:** Ubuntu Server promotes the use of free and open-source software, encouraging collaboration and innovation within the global community. 

7. **Ease of Use:** Despite being a server-focused OS, Ubuntu Server is designed to be user-friendly, with extensive documentation and community support to assist users of all skill levels.

# System Requirements

Ubuntu Server provides a flexible base for your solution that can run on a wide range of hardware, from small virtual machines to enterprise-scale computing. Hard requirements depend on the scenario.. 

Ubuntu Server 24.04 LTS (the latest version at the time of writing) has modest hardware requirements, making it suitable for a wide range of systems: 

• CPU: 1 GHz or better (x86-64 processor) 

• RAM: 1 GB (2 GB recommended for comfortable use) 

• Storage: 2.5 GB for minimal installation (10 GB or more recommended for most use 
cases) 
• Network: Ethernet adapter (for network installation)

For running Ubuntu Server 24 on VMware or other virtualization platforms, similar requirements apply. However, you may want to allocate more resources depending on your specific use case and the applications you plan to run. 
• Compatible Hardware: Ensure your hardware meets the minimum requirements 
(e.g., 2 GHz dual-core processor,). 
• Bootable Media: Create a bootable USB drive or DVD with the Ubuntu Server ISO 
file. (This is required if you are not using virtual machine environment like VMware 
workstation or Oracle virtual box.) 
• Internet Connection: A stable internet connection for downloading updates and 
additional packages. 
• Backup Data: Backup any important data before installation. 
• A tool like Rufu
