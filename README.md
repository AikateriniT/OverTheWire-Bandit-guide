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

-- Level 3 --

Open a new session with same host name and port. U: bandit3 and password the one that we found.

     ls -la
     
With the l"a" we are asking to get the names of all the files and directories even the hidden ones. The hidden names are marked with blue color. We can see that the blue "inhere" directory exists and then we use the:

    cd inhere ( change directory inhere)
    ls - la - To get list of files in this hidden directory.
    cat .hidden 
    
And the password is written there.
__________________________________________________________________________________________

-- Level 4 -- 

Open a new session with same host name and port. U: bandit4 and password the one that we found. When we are at the home directory:

    ls -la
    cd inhere
    ls -la
  
We start searching which is the correct file, and since there are files which are not human-redable they mess up the SSH and we need to reset. The password is found in the 8th file.

    Ctrl + d
___________________________________________________________________________________________

-- Level 5 --

Open a new session with same host name and port. U: bandit5 and password the one that we found. When we are at the home directory:

     ls -la
     cd inhere
     find /home/bandit5/inhere -type f -size 1033c 
  
And it writes the exact file which meets the requirements we asked it for.

    cd maybehere07
    cat .file2
    
And we get the password.
_____________________________________________________________________________________________

-- Level 6 --

Open a new session with same host name and port. U: bandit6 and password the one that we found. When we are at the home directory since the password is hidden somewhere in the server we will search the entire server and set the requirments. So:

     find / -type f -size 33c -user bandit7 -group bandit6 2>/dev/null
     
we search the entire server for a file which is 33bytes owned by user bandit7 (which can be replaced by the numerical 11007) and owned by group bandit 6 ( 11006). with the 2>/dev/null we are asking it to drop the files we dont have access to a blackhole so that our terminal is not full of errors.

The search returns one result which we open it and the password is there.
______________________________________________________________________________________________

-- Level 7 --

Open a new session with same host name and port. U: bandit7 and password the one that we found. When we are at the home directory since the password is hidden in the data.txt file we will use the grep. So:

    grep 'millionth' data.txt
    

