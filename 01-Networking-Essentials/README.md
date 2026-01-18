# Networking Essentials

## The OSI Model

The OSI Model is a seven-layer model that defines the functions of a network device.


### Layer 7: Application Layer
Function: The layer the user (or your Python script) sees. It interacts directly with the software application.

Key Concept: It is not the browser itself (Chrome), but the protocols the browser uses to talk to the network.

Examples: HTTP, HTTPS, FTP, DNS, SSH.

Your Context: This is where requests.get() in Python lives.

### Layer 6: Presentation Layer
Function: Formatting and translation. It ensures the data is in a readable format for the application.

Key Concept: Encryption and Decryption happen here. Character encoding (ASCII, UTF-8) happens here.

Examples: SSL/TLS (the 'S' in HTTPS), JPEG, GIF.

Your Context: When your script sends a password, Layer 6 encrypts it into unreadable gibberish.

### Layer 5: Session Layer
Function: "Traffic Control." It establishes, manages, and terminates connections between applications.

Key Concept: It controls the dialogue (who talks when?).

Examples: SQL (database) session management, API calls, NetBIOS.

Your Context: If you log into a server and stay logged in for 5 minutes, Layer 5 is keeping that "session" active.

### Layer 4: Transport Layer (CRITICAL FOR SCANNING)
Function: Breaking data into manageable chunks and ensuring it gets to the right application (Port).

Key Concept: TCP (Reliable, "Receipt required") vs. UDP (Fast, "Fire and forget").

PDU (Unit of Data): Segment (TCP) or Datagram (UDP).

Examples: Port 80 (HTTP), Port 443 (HTTPS), Port 22 (SSH).

Your Context: Your Port Scanner script operates here. It knocks on "doors" (ports) to see if anyone answers.

### Layer 3: Network Layer
Function: Addressing and Routing. Moving data between different networks.

Key Concept: Logical Addressing (IP Addresses).

PDU (Unit of Data): Packet.

Hardware: Routers, Layer 3 Switches.

Your Context: The IP address 192.168.1.5 lives here. The ping command uses ICMP, which lives here.

### Layer 2: Data Link Layer
Function: Moving data between devices on the same network (LAN).

Key Concept: Physical Addressing (MAC Addresses). Checking for errors (FCS - Frame Check Sequence).

PDU (Unit of Data): Frame.

Hardware: Switches, Network Cards (NICs), WiFi Access Points.

Your Context: Your MAC address 00:1A:2B:3C:4D:5E lives here.

### Layer 1: Physical Layer
Function: The physics. Sending raw bits (1s and 0s) over a physical medium.

Key Concept: Signaling (Light, Electricity, Radio Waves).

PDU (Unit of Data): Bit.

Hardware: Cables (Ethernet, Fiber), Hubs, Repeaters.

Your Context: The actual copper wire or the radio wave carrying your WiFi signal.