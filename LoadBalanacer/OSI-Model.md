# 🌐 OSI Model (Open Systems Interconnection)

## 📖 What is the OSI Model?

The **OSI (Open Systems Interconnection) Model** is a **7-layer networking model** that explains **how data travels from one computer to another over a network**.

Each layer has a specific job and works together to ensure data is sent and received correctly.

> **Simple Definition:**  
> **The OSI Model is a 7-layer framework that explains how data is transmitted between devices over a network.**

---
## 📊 OSI Model (7 Layers)

```text
+------------------------------+
| Layer 7 - Application         |
+------------------------------+
| Layer 6 - Presentation        |
+------------------------------+
| Layer 5 - Session             |
+------------------------------+
| Layer 4 - Transport           |
+------------------------------+
| Layer 3 - Network             |
+------------------------------+
| Layer 2 - Data Link           |
+------------------------------+
| Layer 1 - Physical            |
+------------------------------+
```
---

## 🔹 Layer 1 – Physical Layer

### 📖 Function

The **Physical Layer** transmits raw data as electrical, optical, or radio signals through cables or wireless media.

### Examples

- Network Cables,Fiber Optic Cable,  Hub , Modem.

---

## 🔹 Layer 2 – Data Link Layer

### 📖 Function

The **Data Link Layer** transfers data between devices on the same network.

It frames packets, adds MAC addresses, manages error detection, flow control, and access control.

It uses **MAC Addresses** and detects transmission errors.

### Examples

- Switch, Bridge, Ethernet

---

## 🔹 Layer 3 – Network Layer

### 📖 Function

The **Network Layer** finds the best path for data and delivers it using **IP Addresses**.

### Examples

- Router, IP Address

---

## 🔹 Layer 4 – Transport Layer

### 📖 Function

The **Transport Layer** ensures reliable data delivery.

It divides data into smaller parts and reassembles them at the destination.

### Protocols

- TCP, UDP

---

## 🔹 Layer 5 – Session Layer

### 📖 Function

The **Session Layer** starts, manages, and ends communication sessions between devices.

### Example

- Login Session, Video Call Session

---

## 🔹 Layer 6 – Presentation Layer

### 📖 Function

The **Presentation Layer** converts data into a readable format.

It also performs:

- Encryption, Decryption, Compression

### Examples

- SSL/TLS, JPEG, MPEG

---

## 🔹 Layer 7 – Application Layer

### 📖 Function

The **Application Layer** is the closest layer to the user.

It provides network services used by applications.

### Examples

- HTTP, HHTPS, FTP, SMTP, DNS
---

# 📧 Example: Sending an Email

1. ✉️ **Application Layer** → User writes the email.
2. 🔐 **Presentation Layer** → Data is encrypted and formatted.
3. 🤝 **Session Layer** → Connection is established.
4. 📦 **Transport Layer** → Data is divided into segments.
5. 🌍 **Network Layer** → IP address is added and the best route is selected.
6. 🏷️ **Data Link Layer** → MAC address is added to create frames.
7. 📡 **Physical Layer** → Data is sent as bits over the network.

At the receiver's end, the process happens in reverse to reconstruct the original email.

---
# 🧠 Easy Memory Trick

## 📌 From **Layer 1 → Layer 7**

**P D N T S P A**

> **Please Do Not Throw Sausage Pizza Away**

| Letter | Layer |
|--------|--------|
| P | ⚡ Physical |
| D | 🔗 Data Link |
| N | 🌍 Network |
| T | 📦 Transport |
| S | 🤝 Session |
| P | 🔄 Presentation |
| A | 🖥️ Application |
