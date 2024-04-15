
# zte_c320_unlock
Recommendations and instructions for unblocking the connection and operation of third-party ONUs for the ZTE C320 GPON terminal

> To remove blocking from OLT ZTE C320, you need to connect the computer with two ports: a console cable and Ethernet, setting ip:136.1.1.1/24.
On the OLT control board these are CLI and 10/100M ports. Additionally, you need to set up an FTP server on your computer with the necessary firmware files and patches located on it. The account for the FTP server should be as follows, login: target and password: 123456 (used by default on the ZTE C320).
> 
> It is recommended to use an FTP server as a server on Windows OS - for example Xlight FTP Server

## Procedure

 1. Stop the download process by pressing any key when prompted

     Speed: 1000,full duplex

    Hit any key to stop autoboot: 0

    =>  
 2. Delete the current firmware and reboot
     => erase all
 3. Go to ROMMON MODE again and upload the unlocked firmware for the control board

    => download img smxa0.mvr

    => download img smxa.bt

    => download img smxa.fw

 5. We check for the presence of files and reboot the OLT without stopping the download process

    => ls img
 

     -rwxrwxrwx   524288 Thu Jan 01 00:00:00 1970 smxa.bt
    
     -rwxrwxrwx  1720296 Thu Jan 01 00:00:00 1970 smxa.fw
    
     -rwxrwxrwx 24647784 Thu Jan 01 00:00:00 1970 smxa1.mvr

    => reboot
