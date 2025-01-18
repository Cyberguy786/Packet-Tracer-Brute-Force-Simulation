# Packet Tracer Brute-Force Simulation

This project simulates brute-force attacks on HTTP, FTP, and DNS services using Cisco Packet Tracer. The purpose is to demonstrate how a small network setup can be used to understand attack vectors and mitigation techniques.

---

## Network Topology

The network consists of:
- **1 Router** (192.168.1.1)
- **1 Switch**
- **1 PC** (192.168.1.2)
- **1 Server** (192.168.1.3)

![Topology](screenshots/topology.png)

---

## Services Configured on the Server

1. **FTP Service**
   - Username: `admin`
   - Password: `12345`

2. **HTTP Service**
   - Accessible at: `http://192.168.1.3`

3. **DNS Service**
   - Resolves `www.example.com` to `192.168.1.3`

---

## Simulated Attacks

1. **FTP Brute-Force Attack**
   - Using multiple username/password combinations to gain unauthorized access.

2. **HTTP Brute-Force Attack**
   - Attempting to guess credentials on a restricted HTTP page.

3. **DNS Brute-Force Attack**
   - Sending queries for various subdomains to simulate a brute-force enumeration.

---

## How to Mitigate Brute-Force Attacks

Here are some effective strategies to prevent or mitigate brute-force attacks:

### 1. **Strong Password Policies**
   - Use long, complex passwords with a mix of uppercase, lowercase, numbers, and special characters.
   - Avoid common words or predictable patterns.

### 2. **Account Lockout Mechanisms**
   - Configure services to lock accounts temporarily after a set number of failed login attempts.
   - Example: Lock the FTP account for 15 minutes after 3 failed attempts.

### 3. **Use Multi-Factor Authentication (MFA)**
   - Add an additional layer of security, like one-time passwords (OTPs) or biometric authentication, for all user accounts.

### 4. **Implement Rate Limiting**
   - Limit the number of login attempts per minute for FTP, HTTP, and other services to slow down brute-force attempts.

### 5. **Change Default Ports**
   - Use non-standard ports for FTP, HTTP, or DNS to make automated attacks more difficult.

### 6. **Enable Captcha**
   - For HTTP services, add a Captcha to login pages to prevent automated bots from submitting multiple login attempts.

### 7. **Use Firewalls and Intrusion Prevention Systems (IPS)**
   - Configure firewalls to block suspicious traffic.
   - Use IPS to detect and block brute-force attempts.

### 8. **Monitor Logs**
   - Regularly check server logs for multiple failed login attempts or unusual activity.

### 9. **Encrypt Connections**
   - Use secure protocols like SFTP or HTTPS to prevent attackers from intercepting credentials.

### 10. **DNS Security**
   - Use DNSSEC to authenticate DNS responses and prevent attackers from spoofing records.

---

## How to Use

1. **Download Packet Tracer:**
   - Ensure you have Cisco Packet Tracer installed.

2. **Load the Simulation:**
   - Open the `BruteForceSimulation.pkt` file in Packet Tracer.

3. **Follow the Steps:**
   - Refer to `setup_instructions.txt` for detailed steps to configure and test the network.

---

## Screenshots

### Topology
![Topology](screenshots/topology.png)

### FTP Test
![FTP Test](screenshots/ftp_test.png)

### HTTP Test
![HTTP Test](screenshots/http_test.png)

### DNS Test
![DNS Test](screenshots/dns_test.png)

---

## Future Enhancements

1. Automate brute-force attacks using external tools (requires a real network setup).
2. Expand the network with additional devices for advanced testing.
3. Add intrusion detection/prevention systems (IDS/IPS).

---

## License

This project is licensed under the MIT License. Feel free to use and modify it.
