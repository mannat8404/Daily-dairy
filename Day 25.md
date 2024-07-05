# Day 25
Execute wifi deauthenticaion
Executing a Wi-Fi deauthentication attack using Kali Linux requires several steps and the use of specific tools. Deauthentication attacks are typically performed using aireplay-ng, which is part of the Aircrack-ng suite. Here’s a step-by-step guide:
Disclaimer: Performing a deauthentication attack on a network without permission is illegal and unethical. This guide is provided for educational purposes only. Always obtain explicit permission from the network owner before testing network security.
Step-by-Step Guide to Execute a Wi-Fi Deauthentication Attack
Step 1: Set Up Your Environment
1.	Install Kali Linux: Ensure you have a working installation of Kali Linux. You can run it on a physical machine, a virtual machine, or a bootable USB drive.
2.	Wireless Network Adapter: You need a wireless network adapter that supports packet injection. Many built-in laptop Wi-Fi adapters do not support this feature, so you may need an external USB Wi-Fi adapter.
Step 2: Identify the Target Network
1.	Open Terminal: Start by opening a terminal in Kali Linux.
2.	Put Your Wireless Adapter in Monitor Mode:
sh
Copy code
sudo ip link set wlan0 down
sudo iw dev wlan0 set type monitor
sudo ip link set wlan0 up
3.	Start Airodump-ng to Scan for Networks:
sh
Copy code
sudo airodump-ng wlan0
o	Let it run for a while to gather information about available Wi-Fi networks.
4.	Identify Your Target:
o	Note the BSSID (MAC address) and the channel (CH) of the target network you want to deauthenticate.
Step 3: Deauthentication Attack
1.	Target a Specific Client (Optional):
o	If you want to deauthenticate a specific client (device) on the network, you need its MAC address (Station MAC).
2.	Execute the Deauthentication Attack:
o	For deauthenticating all clients on the target network:
sh
Copy code
sudo aireplay-ng --deauth 0 -a <BSSID> wlan0
o	For deauthenticating a specific client on the target network:
sh
Copy code
sudo aireplay-ng --deauth 0 -a <BSSID> -c <Client_MAC> wlan0
o	Replace <BSSID> with the BSSID of the target network and <Client_MAC> with the MAC address of the client you want to deauthenticate.
3.	Monitor the Attack:
o	You should see deauthentication packets being sent. The clients on the target network should get disconnected as a result.
Step 4: Clean Up
1.	Stop the Airodump-ng Process: If you haven't already, stop the airodump-ng process by pressing Ctrl+C in the terminal.
2.	Return Wireless Adapter to Managed Mode:
sh
Copy code
sudo ip link set wlan0 down
sudo iw dev wlan0 set type managed
sudo ip link set wlan0 up
3.	Restart Network Manager:
sh
Copy code
sudo systemctl restart NetworkManager
Important Notes
•	Legal and Ethical Considerations: Always ensure you have permission to test the network. Unauthorized attacks are illegal and can have serious consequences.
•	Purpose of Deauthentication: This type of attack is often used in penetration testing to test network security or as part of a larger attack to capture WPA handshakes.
•	Mitigation: To protect against such attacks, use WPA3, enable Protected Management Frames (802.11w), and employ network monitoring tools.
By following these steps, you can execute a Wi-Fi deauthentication attack using Kali Linux. However, always ensure you are conducting such activities in a legal and ethical manner.




