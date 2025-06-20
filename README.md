# DosAttack_DosDetection
Attacker program:
This program creates a TCP syn attack on a specified IP address specified by the user, and then would run different ways of attack depending on how anonymously the attackers want to proceed 

Detection program:
This program detects the Denial of Service attack in 3 cases:
-	Many SYN packets (mainly more than 15) having the same IP address are received in a short period of time. 
-	Many SYN packets having the same MAC address are received in a short period of time. 
-	Large traffic is detected within a short period of time to signal a possibility of denial of service. This would be helpful for the attacks where the IP or the MAC addresses are spoofed. 
Note that the attacks with significant time interval between consecutive packets (attacks with 3T and 4T) are hard to be detected. They could be hidden as normal traffic. 

There are 4 programs:
1.	DosAttack.py: the DOS attack program 
2.	IP_Detection.py: DOS detection according to IP Address
3.	Mac_Detection.py: DOS detection according to MAC address 
4.	DosDetection.py: Complete DOS detection 

Instructions how to run the programs:

Attacker program:
Launch the ‘DosAttack.py’ program using python(from terminal or any other IDE however make sure to have the package of scapy fully installed) like any other program and then the program would first require the user to enter the target IP address and then chose 1 of 4 types the first which is the normal attack the second would spoof the attacker’s IP the third would spoof the attacks’ mac address and the fourth would spoof the attacker’s both mac and IP address for more anonymity and then after the attack choses the mode he can also chose 1 of 4 speeds in which he specifies the interval between each packet spent to try to keep the attack hidden at first the first few packets will show warning about not finding a specific mac address and then when the mac gets found the attack would procced normally

Detection Program:
Similar to the Attack program, launch the ‘DosDetection.py’ file and the program should automatically run, and once it detects an attack it will immediately show with a print statement on the screen.
