# Bash-Script-a-honeypot-or-honeyport-
Bash Script that dynamically blocks incoming IPs attempting to connect to a specific port 


The script in the image is a "honeypot" or "honeyport" script that dynamically blocks incoming IPs attempting to connect to a specific port. 
Explanation
	1. Netcat Listener:
		○ The script uses nc (netcat) to listen on port 1025.
		○ Any connection attempt is logged and processed in real-time.
	2. Extract IP Address:
		○ When an IP connects to the port, its address is extracted using awk and grep.
	3. Add iptables Rule:
		○ The script dynamically adds an iptables rule to block the offending IP.
	4. Continuous Execution:
The while [ 1 ] loop ensures the script keeps running indefinitely.
