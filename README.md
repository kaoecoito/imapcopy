imapcopy
========

Copy recursively all email messages and folders from 1 imap account to another

Installation Instructions
-------------------------

### Linux and other Unixes
* Download the application from the repository
* build de jar

        mvn clean package

* go to target folder

#### Run with command line tool
* Run as a command line tool:

        ./imapCopy.sh sourceImapAccount targetImapAccount [-y yearUntil] [-e exlcuded folder] [-i only folder]
        (ex: ./imapCopy.sh imap://peter:mypassword@foo.com imaps://peter%40gmail.com:myotherpasword@imap.gmail.com) 2018 Spam INBOX
The yearUntil parameter limits the messages to be copied by filtering by the year of the sent-date.
The exlcuded folder and only folder use RegEx and could be called multiple times      
* Run using (very basic) Gui

        ./imapCopyGui.sh
        
        
### Imap accounts url format

        {protocol}://[user:password@]{host}[:port]
        
Where 
* protocol can be imap or imaps
* user and password are optional and must be url scaped (ex: peter@gmail.com becomes peter%40gmail.com)
* host: host of the imap server
* port: port of the imap server
