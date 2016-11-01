# Projet_ECFS Email checker for SenseHat (Raspberry Pi 3)
A notification and check system for gmail on Raspberry Pi 3 & Sense Hat.
The aim is to use the Sense Hat module as a *visual warning*, a notification, of the state of your inbox. It works perfectly with **Gmail** and **Inbox by Google**. 
Nevertheless, it is theoretically compatible with **all email server using IMAP** without advanced connection (other than Login / Password).


_______



## Requiered

ECFS, Email checker for SenseHat Raspberry Pi 3 **require**:

+ A _Raspberry Pi_ (v.3b recommanded)
+ A _SenseHat_ 
+ Python 2.7
  + SenseHat
  + IMAPClient
+ Nano (for configuration)

## Install

Pull or exctract the repository where you whant on your rapsberry.

### Install required elements
Open your command line and, before launch any script, install the following python libraries and apt: 

    pip install imapclient
    sudo apt-get update
    sudo apt-get install sense-hat
    sudo reboot
      
### Settings
Now, you can configure ECFS (currently the comments are in french because i'm french) :

    sudo nano start.py
    
Find the followings required variables and put your own values in: 

    HOSTNAME = 'imap.gmail.com' 
    USERNAME = 'username'
    PASSWORD = 'password' 
    
You can also modify some other values like :
 
 If you want show logs in the terminal:
 
     LOG = True 
     
 Choose the folders to modify:
 
     MAILBOX = 'Inbox'
     
 check mail every x seconds:
 
     MAIL_CHECK_FREQ = 20




