# Computer Networks (CN)

## Part 1: Quick Short Notes (Fundamentals)

### 1. Computer Networks Fundamentals
*   **Definition:** A set of computers sharing resources located on or provided by network nodes.
*   **Topology:** The physical or logical arrangement of a network (Bus, Star, Ring, Mesh, Tree). Mesh is most reliable but most expensive.
*   **LAN, MAN, WAN:** Local Area Network (office/building), Metropolitan Area Network (city), Wide Area Network (country/global like the Internet).

### 2. OSI Model (Open Systems Interconnection)
*   A 7-layer theoretical reference model for network communication.
    1.  **Physical Layer:** Transmission of raw bits over a physical medium (Hubs, Cables).
    2.  **Data Link Layer:** Node-to-node data transfer, error detection (MAC addresses, Switches). Data units are *Frames*.
    3.  **Network Layer:** Routing packets from source to destination (IP addresses, Routers). Data units are *Packets*.
    4.  **Transport Layer:** End-to-end communication, reliability, multiplexing (TCP, UDP). Data units are *Segments*.
    5.  **Session Layer:** Establishing, managing, and terminating sessions.
    6.  **Presentation Layer:** Data translation, encryption, compression.
    7.  **Application Layer:** Network applications (HTTP, FTP, SMTP).

### 3. TCP/IP Model
*   The practical model used for the Internet, consisting of 4 layers:
    1.  **Network Access (Link) Layer:** Corresponds to OSI Physical + Data Link.
    2.  **Internet Layer:** Corresponds to OSI Network (IP Protocol).
    3.  **Transport Layer:** Corresponds to OSI Transport (TCP, UDP).
    4.  **Application Layer:** Corresponds to OSI Session + Presentation + Application.

### 4. IP Addressing
*   **IPv4:** 32-bit address, formatted as 4 octets separated by dots (e.g., 192.168.1.1). Total $2^{32}$ addresses.
*   **IPv6:** 128-bit address, formatted as 8 groups of 4 hexadecimal digits. Solves IPv4 exhaustion.
*   **Classes (IPv4):**
    *   Class A: 1.0.0.0 to 126.255.255.255 (Large networks)
    *   Class B: 128.0.0.0 to 191.255.255.255 (Medium networks)
    *   Class C: 192.0.0.0 to 223.255.255.255 (Small networks)
    *   Class D: Multicasting. Class E: Experimental.
*   **Subnetting:** Dividing a larger network into smaller, manageable sub-networks.

### 5. Routing & Switching
*   **Switching:** Happens at Layer 2 (Data Link). Forwards frames based on MAC addresses within the same network.
*   **Routing:** Happens at Layer 3 (Network). Forwards packets between different networks based on IP addresses using routing tables.
*   **MAC Address:** 48-bit physical address assigned by the manufacturer. Hardcoded on the NIC.

### 6. TCP & UDP Protocols
*   **TCP (Transmission Control Protocol):** Connection-oriented, reliable, guarantees delivery, in-order delivery, uses 3-way handshake (SYN, SYN-ACK, ACK). Used for HTTP, FTP, Email. Slower but safer.
*   **UDP (User Datagram Protocol):** Connectionless, unreliable, no guarantee of delivery, out-of-order. Used for video streaming, VoIP, DNS. Faster but risky.

### 7. HTTP/HTTPS
*   **HTTP (Hypertext Transfer Protocol):** Port 80. Used to load webpages. Plaintext communication (insecure).
*   **HTTPS (HTTP Secure):** Port 443. Uses TLS/SSL to encrypt HTTP requests and responses. Ensures confidentiality and integrity.

### 8. DNS & DHCP
*   **DNS (Domain Name System):** Port 53. The "phonebook" of the Internet. Translates human-readable domain names (www.google.com) to machine-readable IP addresses (142.250.190.46).
*   **DHCP (Dynamic Host Configuration Protocol):** Port 67/68. Automatically assigns IP addresses and other network configuration parameters to devices on a network.

---

## Part 2: Placement-Related MCQs

1. Which layer of the OSI model is responsible for routing packets from the source host to the destination host over multiple networks?

A) Data Link Layer

B) Network Layer

C) Transport Layer

D) Session Layer

**Answer:** Option **B**

**Explanation:**

The Network Layer (Layer 3) is responsible for logical addressing (IP addresses) and routing data packets from a source to a destination across multiple interconnected networks. Routers operate at this layer.

---

2. Which of the following topologies requires the most amount of wiring and provides the highest reliability?

A) Star Topology

B) Ring Topology

C) Mesh Topology

D) Bus Topology

**Answer:** Option **C**

**Explanation:**

In a full Mesh Topology, every node is connected to every other node. This provides high redundancy and reliability because if one link fails, traffic can be routed through another. However, it requires the most amount of cabling ($n(n-1)/2$ links for $n$ nodes), making it expensive.

---

3. What is the size of an IPv4 address and an IPv6 address respectively?

A) 32 bits, 64 bits

B) 32 bits, 128 bits

C) 64 bits, 128 bits

D) 128 bits, 256 bits

**Answer:** Option **B**

**Explanation:**

An IPv4 address is 32 bits long (4 bytes), typically written in dotted-decimal format. An IPv6 address is 128 bits long (16 bytes), typically written in hexadecimal format to solve the address exhaustion problem of IPv4.

---

4. Which protocol is connection-oriented and ensures reliable, in-order delivery of data?

A) UDP

B) IP

C) ICMP

D) TCP

**Answer:** Option **D**

**Explanation:**

TCP (Transmission Control Protocol) is a connection-oriented protocol that establishes a session (via a 3-way handshake) before transmitting data. It uses acknowledgments and retransmissions to ensure data is delivered reliably and in the correct order.

---

5. What is the primary function of the Domain Name System (DNS)?

A) To automatically assign IP addresses to hosts.

B) To encrypt data transmitted over the internet.

C) To translate domain names into IP addresses.

D) To route packets between different networks.

**Answer:** Option **C**

**Explanation:**

DNS acts as the internet's phonebook. It translates human-readable domain names (like www.example.com) into the numerical IP addresses (like 192.0.2.1) that computers use to identify each other on the network.

---

6. In the TCP/IP model, which layer corresponds to the physical and data link layers of the OSI model?

A) Application Layer

B) Transport Layer

C) Internet Layer

D) Network Access Layer

**Answer:** Option **D**

**Explanation:**

The Network Access Layer (also called the Link Layer or Network Interface Layer) in the TCP/IP model encompasses the functions of both the Physical and Data Link layers in the OSI model.

---

7. Which of the following is a private IP address?

A) 11.0.0.1

B) 172.31.255.255

C) 192.169.1.1

D) 8.8.8.8

**Answer:** Option **B**

**Explanation:**

Private IP address ranges are:
Class A: 10.0.0.0 to 10.255.255.255
Class B: 172.16.0.0 to 172.31.255.255
Class C: 192.168.0.0 to 192.168.255.255
172.31.255.255 falls within the Class B private range.

---

8. What protocol is used to automatically assign an IP address to a client when it connects to a network?

A) DNS

B) ARP

C) DHCP

D) NAT

**Answer:** Option **C**

**Explanation:**

DHCP (Dynamic Host Configuration Protocol) automatically provides an IP address and other network configuration parameters to each device connecting to a network, preventing IP conflicts.

---

9. Which device operates at the Data Link Layer (Layer 2) and uses MAC addresses to forward frames?

A) Hub

B) Switch

C) Router

D) Repeater

**Answer:** Option **B**

**Explanation:**

A network switch operates at the Data Link Layer. It maintains a MAC address table to intelligently forward frames only to the port connected to the destination device, unlike a hub which broadcasts to all ports.

---

10. During the TCP 3-way handshake, what is the sequence of flags exchanged to establish a connection?

A) SYN $\rightarrow$ ACK $\rightarrow$ SYN-ACK

B) SYN $\rightarrow$ SYN-ACK $\rightarrow$ ACK

C) ACK $\rightarrow$ SYN $\rightarrow$ SYN-ACK

D) SYN-ACK $\rightarrow$ SYN $\rightarrow$ ACK

**Answer:** Option **B**

**Explanation:**

To establish a connection, the client sends a SYN (Synchronize) packet. The server responds with a SYN-ACK (Synchronize-Acknowledge) packet. Finally, the client sends an ACK (Acknowledge) packet back to the server.

---

11. Which protocol resolves an IP address to a MAC address?

A) RARP

B) ARP

C) DNS

D) DHCP

**Answer:** Option **B**

**Explanation:**

ARP (Address Resolution Protocol) is used to map a known logical IP address to an unknown physical MAC address on a local network. RARP does the reverse.

---

12. The default port number for HTTP and HTTPS are respectively:

A) 80 and 443

B) 80 and 8080

C) 443 and 80

D) 21 and 22

**Answer:** Option **A**

**Explanation:**

HTTP uses port 80 by default for unencrypted web traffic, while HTTPS uses port 443 for secure, encrypted web traffic using TLS/SSL.

---

13. What is the length of a MAC address?

A) 16 bits

B) 32 bits

C) 48 bits

D) 64 bits

**Answer:** Option **C**

**Explanation:**

A MAC (Media Access Control) address is a 48-bit unique identifier assigned to network interfaces for communications at the data link layer of a network segment.

---

14. Which OSI layer handles data formatting, compression, and encryption?

A) Application Layer

B) Presentation Layer

C) Session Layer

D) Transport Layer

**Answer:** Option **B**

**Explanation:**

The Presentation Layer (Layer 6) is responsible for data translation, compression, and encryption/decryption, ensuring that data sent by the application layer of one system can be read by the application layer of another.

---

15. What type of cable is mostly used to construct a local area network (LAN) due to its resistance to interference?

A) Coaxial Cable

B) Fiber Optic Cable

C) Twisted Pair Cable (UTP/STP)

D) Ribbon Cable

**Answer:** Option **C**

**Explanation:**

Unshielded Twisted Pair (UTP) or Shielded Twisted Pair (STP) cables are the most common media used for LANs (like Ethernet). Twisting the wires helps to cancel out electromagnetic interference (EMI).

---

16. Which network device operates at the Physical Layer and merely amplifies and regenerates the signal?

A) Router

B) Switch

C) Repeater

D) Bridge

**Answer:** Option **C**

**Explanation:**

A Repeater operates at Layer 1 (Physical Layer). Its sole purpose is to receive a weakened or distorted signal, regenerate it, and transmit it further, extending the network's range.

---

17. Which routing protocol relies on the number of 'hops' to determine the best path to a destination?

A) OSPF

B) BGP

C) RIP

D) EIGRP

**Answer:** Option **C**

**Explanation:**

Routing Information Protocol (RIP) is a distance-vector routing protocol that uses hop count as its routing metric. The path with the fewest hops is considered the best path.

---

18. What is the purpose of the Subnet Mask?

A) To encrypt the IP address.

B) To identify the MAC address of a device.

C) To divide an IP address into network and host portions.

D) To block malicious traffic from entering the network.

**Answer:** Option **C**

**Explanation:**

A subnet mask is a 32-bit number that masks an IP address, separating the IP address into a network address and a host address. This allows a large network to be divided into smaller subnets.

---

19. In IPv4, what is the loopback address used for testing the local network interface?

A) 0.0.0.0

B) 127.0.0.1

C) 192.168.1.1

D) 255.255.255.255

**Answer:** Option **B**

**Explanation:**

The IPv4 address 127.0.0.1 is the standard loopback address. It is used to test the TCP/IP suite on the local machine without sending packets out to a physical network.

---

20. Which protocol is primarily used for transferring files over the internet?

A) SMTP

B) SNMP

C) FTP

D) HTTP

**Answer:** Option **C**

**Explanation:**

FTP (File Transfer Protocol) is a standard network protocol used for the transfer of computer files between a client and server on a computer network. It typically uses ports 20 and 21.
