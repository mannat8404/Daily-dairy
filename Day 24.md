#Day 24 
#introduction to wifi attacks
Wi-Fi, or wireless fidelity, is a technology that allows devices to connect to the internet or communicate wirelessly within a local area network (LAN). While Wi-Fi networks are convenient and widely used, they are also vulnerable to various types of attacks. Understanding these attacks is crucial for implementing effective security measures.
Types of Wi-Fi Attacks
1.	Eavesdropping
o	Description: Also known as sniffing, this attack involves intercepting and capturing data packets transmitted over the Wi-Fi network.
o	Tools: Wireshark, tcpdump, Aircrack-ng
o	Prevention: Use strong encryption (WPA3), VPNs, and secure protocols (HTTPS).
2.	Man-in-the-Middle (MitM) Attacks
o	Description: The attacker intercepts communication between two parties, allowing them to read and potentially alter the messages.
o	Tools: Ettercap, Bettercap, SSLstrip
o	Prevention: Use end-to-end encryption, SSL/TLS, and verify network certificates.
3.	Rogue Access Points
o	Description: An unauthorized access point set up to mimic a legitimate one, tricking users into connecting and exposing their data.
o	Tools: Airbase-ng, Karmetasploit
o	Prevention: Implement network monitoring, disable auto-connect features, and use WPA3.
4.	Deauthentication Attacks
o	Description: The attacker sends deauthentication frames to disconnect users from a Wi-Fi network, often as a precursor to other attacks like MitM.
o	Tools: Aireplay-ng, MDK3
o	Prevention: Use WPA3, enable 802.11w (Protected Management Frames), and monitor for unusual activity.
5.	Evil Twin Attacks
o	Description: A type of rogue access point where the attacker sets up a fake Wi-Fi network with the same SSID as a legitimate one, capturing data from unsuspecting users.
o	Tools: Airbase-ng, Karmetasploit
o	Prevention: Train users to recognize fake networks, use WPA3, and disable auto-connect.
6.	Wi-Fi Protected Setup (WPS) Attacks
o	Description: Exploits vulnerabilities in the WPS protocol, allowing attackers to gain access to the network without the password.
o	Tools: Reaver, Bully
o	Prevention: Disable WPS, use strong passwords, and keep firmware updated.
7.	KRACK Attacks
o	Description: Key Reinstallation Attacks exploit vulnerabilities in the WPA2 protocol, allowing attackers to decrypt Wi-Fi traffic.
o	Tools: KrackAttack
o	Prevention: Update devices and routers with patches, use WPA3.
8.	Dictionary and Brute Force Attacks
o	Description: Attackers attempt to guess the Wi-Fi password using a list of common passwords (dictionary) or by trying all possible combinations (brute force).
o	Tools: Aircrack-ng, Hashcat
o	Prevention: Use complex and unique passwords, enable WPA3.
Best Practices for Securing Wi-Fi Networks
1.	Use Strong Encryption: Always use the latest and strongest encryption standard, WPA3, to protect your Wi-Fi network.
2.	Regularly Update Firmware: Keep your router’s firmware updated to patch any known vulnerabilities.
3.	Change Default Settings: Change default usernames, passwords, and SSID names to something unique and not easily guessable.
4.	Disable WPS: Disable Wi-Fi Protected Setup (WPS) to prevent attacks exploiting its vulnerabilities.
5.	Network Segmentation: Separate your network into segments (e.g., guest and internal networks) to limit access and potential damage from an attack.
6.	Monitor Network Traffic: Regularly monitor your network for unusual activity or unauthorized devices.
7.	Use VPNs: Encourage the use of Virtual Private Networks (VPNs) for an added layer of encryption and security, especially on public Wi-Fi.
8.	Educate Users: Train users on the dangers of connecting to unknown or suspicious Wi-Fi networks and the importance of using secure practices.
By understanding these common Wi-Fi attacks and implementing robust security measures, you can significantly reduce the risk of unauthorized access and data breaches on your wireless networks.
