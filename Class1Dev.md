# Basic Networking of Docker
## Network Interface
### Kernel Space
#### User Space
##### Docker file
**Network Interface::**
In a computer network, a network interface is a software or hardware interface that connects two pieces of equipment or protocol layers. A network interface will almost always have a network address. This can be a combination of a node identifier and a port number, or it can be a separate node ID. Network interfaces perform standardized tasks such as sending and receiving messages, connecting and disconnecting, and so on. **Network interface manages packets**

**Network interface Card (NIC)::**
A network interface card (NIC) is a hardware component without which a computer cannot be connected over a network. It is a circuit board installed in a computer that provides a dedicated network connection to the computer. It is also called network interface controller, network adapter or LAN adapter.
**Purpose of NIC::**
1.NIC allows both wired and wireless communications.

2.NIC allows communications between computers connected via local area network (LAN) as well as communications over large-scale network through Internet Protocol (IP).

3.NIC is both a physical layer and a data link layer device, i.e. it provides the necessary hardware circuitry so that the physical layer processes and some data link layer processes can run on it.

**Two types of NIC cards::**

*1. Internal Network card  
2.External Network cards*

Internal network cards have a slot on the motherboard into which they can be put. Network access requires the use of network cables. External network cards are of two types: Wireless and USB based. Wireless network card needs to be inserted into the motherboard, however no network cable is required to connect to the network. They are useful while traveling or accessing a wireless signal.

>**What is Kernel Space & User Spece?**

**Kernel space is only used to operate the privileged operating system kernel, kernel extensions, and the majority of device drivers. User space, on the other hand, is the memory location where application applications and some drivers run.**

>**What is kernel?**

An Operating System's Kernel is a computer program that serves as the heart and soul of the system. The Kernel has power over everything in the system because the Operating System has control over it. It is the most crucial component of a computer operating system. The Kernel is the first program loaded after the bootloader when a system starts since it is responsible for the rest of the system's functions for the Operating System. Until the Operating System is shut down, the Kernel remains in memory.

*Low-level tasks including as disk management, memory management, task management, and so on are handled by the Kernel. It serves as a link between the user and the system's hardware components. A System Call occurs when a process makes a request to the Kernel.*

>**Functions of a Kernel:**

Following are the functions of a Kernel:

**Access Computer resource:** A Kernel can access various computer resources like the CPU, I/O devices and other resources. It acts as a bridge between the user and the resources of the system.
**Resource Management:** It is the duty of a Kernel to share the resources between various process in such a way that there is uniform access to the resources by every process.
**Memory Management:** Every process needs some memory space. So, memory must be allocated and deallocated for its execution. All these memory management is done by a Kernel.
**Device Management:** The peripheral devices connected in the system are used by the processes. So, the allocation of these devices is managed by the Kernel.

>**User Space:**

All code that runs outside the kernel of an operating system is referred to as user space). User Space refers to the numerous programs and libraries that the operating system employs to interface with the kernel: input/output software, file system object manipulation software, application software, and so on.

NIC:- Layer 2 : Data link layer: Works with MAC Address. For example: Switch

>**Gateway:**

A gateway is a network node used in telecommunications that connects two networks with different transmission protocols together. Gateways serve as an entry and exit point for a network as all data must pass through or communicate with the gateway prior to being routed.

>**DHCP**

A DHCP Server is a network server that assigns IP addresses, default gateways, and other network information to client devices on a regular basis. To reply to broadcast inquiries from clients, it uses the Dynamic Host Configuration Protocol, or DHCP, as a common protocol. Network tables and a dhcptab configuration macros table are the two types of databases used by DHCP.

>**DOCKER:**How to install docker 

I used EC2 instance (Free Tier) to install docker. I took help from below link-  https://docs.aws.amazon.com/AmazonECS/latest/developerguide/docker-basics.html

`sudo yum update -y` [Update the installed packages and package cache on your instance.]

`sudo amazon-linux-extras install docker` [Install the most recent Docker Engine package.]

`sudo yum install docker` [Linux Installation]

`sudo service docker start` [After installation, we need to start Docker]

`sudo usermod -a -G docker ec2-user` [I can use Docker commands without requiring sudo if I add the ec2-user to the docker group]

# Docker Image Creation

I Created a directory where I established a docker image or Contaianer using following command

`mkdir redis`

`cd redis`

`touch Dockerfile`








