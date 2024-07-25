MAC Address Changer
This Python script allows you to change the MAC address of a network interface on a Unix-based system.

Description
The script takes in the network interface and the new MAC address as arguments and changes the MAC address of the specified network interface to the new MAC address.

Prerequisites
Python 3.x
Unix-based operating system (Linux, macOS, etc.)
Administrative (root) privileges
Installation
Clone the repository or download the script to your local machine:


git clone https://github.com/yourusername/mac-changer.git
cd mac-changer
Usage
To use the script, run it with the necessary options:


./mac_changer.py -i <interface> -m <new_mac_address>
For example:

./mac_changer.py -i eth0 -m 00:11:22:33:44:55
Options
-i, --interface : The network interface whose MAC address you want to change.
-m, --mac : The new MAC address you want to assign to the interface.

Example

sudo ./mac_changer.py -i eth0 -m 00:11:22:33:44:55

Script Explanation
Import Libraries: The script uses subprocess for executing shell commands, optparse for parsing command-line options, and re for regular expressions.

Get Arguments: The get_arguments function parses the command-line options for the interface and the new MAC address.

Change MAC Address: The change_mac function takes the interface and the new MAC address, brings the interface down, changes the MAC address, and brings the interface back up using the ifconfig command.

Get Current MAC Address: The get_current_mac function retrieves the current MAC address of the specified interface using ifconfig and regular expressions.

Main Execution: The script first retrieves and prints the current MAC address of the specified interface, then changes it to the new MAC address, and finally verifies and prints the new MAC address.

Note
This script requires root privileges to change the MAC address. Make sure to run it with sudo if you're not logged in as the root user.
Changing MAC addresses might not be allowed on all network interfaces or systems, depending on your hardware and operating system configurations.
License
This project is licensed under the MIT License - see the LICENSE file for details.

Acknowledgments
Inspired by ethical hacking and network security tutorials.
