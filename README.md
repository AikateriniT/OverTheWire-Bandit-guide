OverTheWire: Bandit
------------------------------------------------------------------------------------------

Level 0 -> 1

For the first level I worked with Putty SSH. Host name was bandit.labs.overthewire.org on port 2220. Use as u: bandit0 and p:bandit0. Hint: When we write the password for the server it never shows. To get the password for the level 1 :

    ls -la (list  -list all)
    To get the names of all the files in the directory listed.
  
In order to read the readme file:

    cat readme 
    And it writes the password written in the file readme.
_______________________________________________________________________________________
Level 1 -> 2

For the level 1 we use the command Ctrl + d to disconnect and we open a new session with the same host name and port. U: bandit1 and for password we use the password we found. From the notepad we had pasted the password we copy it and paste it by right clicking.

    ls -la 
    To list the names of the files.

The file has a "-" as a name so we must use

    cat < -
    
In order to read the file. And the password is written there.

     Ctrl + d
__________________________________________________________________________________________


