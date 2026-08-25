# cehpractical
Ceh practical notes

https://github.com/mzeeshanzafar28/CEH-Practical-CheatSheet 

https://github.com/infovault-Ytube/CEH-Practical-Notes

https://github.com/hunterxxx/CEH-v12-Practical

https://github.com/aniket2912/All-CEHv13-Module-wise-PDF-Reports

https://github.com/dhabaleshwar/CEHPractical/blob/main/Everything%20You%20Need.md

https://github.com/DarkLycn1976/CEH-Practical-Notes-and-Tools



Step 1: Scan for Android Devices
Quick scan of all networks for Android-specific indicators:
bash
# Scan for ADB port (5555) across all networks
nmap -p 5555 10.22.99.0/24 172.16.32.0/24 10.100.50.0/24 --open
Look for Android fingerprint:
bash
# More detailed scan looking for Android
nmap -sV -p 5555,5037,8080 10.22.99.0/24 172.16.32.0/24 10.100.50.0/24 --open
