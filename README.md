#  Task 8: VPN Setup and Privacy Test

##  Objective

Set up and test a VPN to understand its role in protecting user privacy and securing online communication.

---

##  Tools Used

- **VPN Client**: ProtonVPN (Free Tier)
- **IP Checker**: [whatismyipaddress.com](https://www.whatismyipaddress.com)
- **Device**: Windows 11 (laptop)

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
| Before VPN         | `103.25.xxx.xxx`   | India          | `screenshots/before.png`     |
| After VPN Connect  | `185.159.157.11`   | Netherlands    | `screenshots/after.png`      |

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
