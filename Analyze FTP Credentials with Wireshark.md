# Analyze FTP Credentials with Wireshark

In this video, we will use Wireshark to check if any FTP packets are found.


https://github.com/user-attachments/assets/21731753-b6cb-497e-9a2d-0b8df6af6ed0


## Questions

1. *What is the name used to log into the FTP session?*
2. *What is  the password used to log into the FTP site?*
3. *What is the name of the file downloaded during the FTP session?*
4. *What is the IP address of the computer requesting an FTP Connection?*

### Walkthrough

1. Open Wireshark.
2. Select the network interface **enp2s0**
3. Click on the Blue Fin to begin capture.
4. After X amount of seconds, stop capture.
5. Use the **ftp** filter to answer the Questions.

**Alternative Filters**
1. Use **ftp.request.command==USER** to find the User account.
2. Use **ftp.request.command==PASS** to find the Password.
3. Use **ftp.request.command==RETR** to find the File Retrieved.
