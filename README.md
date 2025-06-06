#  Task 8: VPN Setup and Privacy Test

##  Objective

Set up and test a VPN to understand its role in protecting user privacy and securing online communication.

---

##  Tools Used

- **VPN Client**: ProtonVPN (Free Tier)
- **IP Checker**: [whatismyipaddress.com](https://www.whatismyipaddress.com)
- **Device**: Windows 10 (laptop)

---

##  Setup Steps

1. **Signed up** at [https://protonvpn.com](https://protonvpn.com)
2. **Downloaded** and **installed** ProtonVPN Windows client
3. Logged in with free tier account
4. **Connected** to a Netherlands VPN server (free option)
5. Verified VPN was active and traffic encrypted

---

##  IP Address Verification

| State               | IP Address         | Location       | Screenshot                   |
|--------------------|--------------------|----------------|------------------------------|
| Before VPN         | `157.51.xxx.xxx`   | India          | `screenshots/before.png`     |
| After VPN Connect  | `185.107.80.68`   | Netherlands    | `screenshots/after.png`      |

 Verified IP address changed using `whatismyipaddress.com`

---

##  Traffic Encryption Check

- Visited several HTTPS websites (Google, GitHub, ProtonMail)
- Confirmed secure (padlock icon present)
- Used browser dev tools to view encrypted TLS connection details

---

##  Speed Comparison (Subjective)

| Action                     | With VPN         | Without VPN     |
|----------------------------|------------------|-----------------|
| Website load speed         | Slightly slower  | Normal          |
| YouTube 720p video         | Buffered 2s delay| Smooth          |
| DNS resolution             | Normal           | Normal          |

---

##  Summary Report

###  Benefits of VPNs

- Encrypts all internet traffic, especially useful on public Wi-Fi
- Hides real IP and location
- Bypasses geo-blocked or censored content
- Stops ISP tracking

###  Limitations

- Slower speeds on free servers
- VPN provider can see traffic (must be trusted)
- Some websites block VPN traffic
- Doesn’t make you anonymous — just private

---

##  VPN Encryption

When connected to a VPN, all of your internet traffic is encrypted **from your device to the VPN server**. This process involves several components working together to ensure privacy and security.

---

###  How VPN Encryption Works

1. **Tunneling Protocol Initiates a Secure Tunnel**
   - Protocols like **OpenVPN**, **WireGuard**, or **IKEv2** are used to create a secure “tunnel” between your device and the VPN server.
   - This tunnel ensures no one can “look inside” the traffic even if they intercept it.

2. **Traffic is Encrypted Locally**
   - Before your data leaves your device, it is encrypted using strong algorithms (like AES-256).
   - Example: When you visit `https://example.com`, even the domain name is hidden if DNS over HTTPS or encrypted DNS is used.

3. **Data Travels Encrypted**
   - Encrypted packets are sent through your ISP and other nodes on the internet, but they **cannot be read** without the VPN key.
   - The VPN server then **decrypts** the traffic and forwards it to the destination (e.g., example.com).

4. **Response is Re-Encrypted**
   - The response from the website is encrypted again by the VPN server and sent back through the tunnel to your device.

---

###  Encryption Algorithms Used

| Protocol     | Common Encryption         | Security Level     |
|--------------|---------------------------|--------------------|
| OpenVPN      | AES-256-GCM, RSA 2048+    | Strong (Military-grade) |
| WireGuard    | ChaCha20, Poly1305        | Fast & Secure       |
| IKEv2/IPSec  | AES-128/256, SHA-2        | Enterprise-grade    |

---

###  Example with ProtonVPN (Free Tier)

- **Protocol Used**: OpenVPN (UDP)
- **Encryption**: AES-256-CBC with SHA-512 authentication
- **Handshake**: RSA-4096 for key exchange

This means:
- Even your **ISP cannot see** the websites you visit.
- Your **real IP address is hidden** from destination websites.
- The **data payload** (like login forms, messages, emails) is fully encrypted in transit.

---

###  Key Terms

| Term             | Definition                                                               |
|------------------|---------------------------------------------------------------------------|
| Encryption       | Process of encoding information so only authorized parties can read it   |
| Tunnel           | Encrypted connection between your device and VPN server                  |
| AES-256          | Advanced Encryption Standard with 256-bit key (very strong encryption)    |
| Handshake        | Initial secure key exchange between your device and the VPN               |
| Obfuscation      | Some VPNs disguise traffic to look like regular web browsing              |

---

###  Without a VPN

Without a VPN:
- ISPs and attackers can see DNS queries, IP addresses, and metadata.
- Your IP address is exposed.
- Public Wi-Fi risks increase (MITM attacks, sniffing, DNS spoofing).

---

###  With a VPN

With a VPN:
- All data is encrypted in transit.
- You appear to browse from a different location.
- Attackers can’t intercept readable data.

