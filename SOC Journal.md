# Journal created on 9/14/26

The purpose of this is to document my journey on learning SOC using my small home lab. Note: Receiving assistance from Google Gemini

Still working on how Wazuh can log any and all Nmap scans from my Kali Linux VM to my Windows 11 VM.
| Date | Entry|
|---|---|
| 9/18/2026 | The two VMs are communicating with each other when using the 'ping' and 'nmap' commands, but Wazuh is not logging them. Still researching. |
| 10/16/2026 | Revisited this and I was able to successfully have Wazuh log the 'attack' (network scan using the 'nmap' command: nmap -Pn -F --min-rate 100 <windows_VM_IP>) from my Kali Linux VM to my Windows 11 VM (FINALLY!!!). Note: With Gemini's assistance, I had to create a custom rule for Wazuh to detect the scan and had to make a few changes of updating the local_rule.xml until it worked. I had to change 1 - 2 lines in it. |
| 10/19/2026 | Going to start automating incident response via Wazuh Active Response. Ran into a road block and got an error message with Wazuh not being able to save the updated ossec.conf file so that the Windows 11 Firewall agent can block the Kali Linux IP. Will research this more. |
