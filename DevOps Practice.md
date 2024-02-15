Session-1
----------------------------------------------------------------------------------------------------------------
1)Create key's from the git bash by using ssh-keygen -f devops
2)By using public key create a instance from AWS
3)By using git bash connected to instance -- ssh -i path of pem key ec2-user@ipaddress
4)created a file---- > touch example.txt
5)create a directory --->mkdir example
6)ls - list the files and directory
7)ls -l lenghty list
8)ls -lr reverese order list
9)ls -lt time based list
10)ls -ltr reverse time based list
11)cd/ - come to the base location
12)d - directory
13)- -> file

CRUD - Create Read Update Delete
----------------------------------------------------------------------------------------------------------------
1)touch <file-name>
2)mkdir <directory-name>
3)cat > <file-name> --> we can enter to the file and we can wrote after ctrl+d to come out
4)cat <file-name> --> We can read the file 
5)cat >> <file-name> --> to append for already existed file
6)cp <file-name> <directory-name> --> copy the files to directory
7)mv <file-name> <directory-name> --> cut the files and move to the desired directory
8)mv <file-name> <renamed-file-name>  --> This will rename the file
9)rm <file-name> --> This will remove the file
10)rm -r <directory-name> -->  This will remove the directory (-r -- recursive means removes inside the directory)
11)rm <directory-name> --> Removes the empty directory
12)cp -r <directory-name1> <directory-name2> --> We can copy one directory to another directory


Session-2
----------------------------------------------------------------------------------------------------------------
Grep - to find the text in a  file

1)a simple file we can take ---> cp /etc/passwd passwvd
2)then we can read the file by using ---> cat passwd
3)grep sbin passwd ---> To find the sbin(text) in passwd file
4)cat >> passwd ---> to append the text to passwd- google
												   GOOGLE
5)grep google passwd --> Only get google only
6)grep -i google passwd --> Then we get both -->google GOOGLE	

			
Piping
------------------------------------------------------------------------------------------------------------												
1)cat passwd | grep sbin --> In piping we can read the file and then search the text
2)cat passwd | grep google --> can get only google
3)cat passwd | grep -i google --> get the Both google and GOOGLE

Head and Tail
------------------------------------------------------------------------------------------------------------
1)head <file-name> --> First 10 lines of file by default
2)tail<file-name> --> Lat 10 lines of file by default
3)cat <file-name> | head <file-name> ---> it will also gives same as above but using piping
4)cat <file-name> | tail <file-name> ---> it will also gives same as above but using piping
5)head -n 2 <file-name> --> It will gives the 1st 2 lines in the file
6)cat <file-name> | head -n 2 <file-name> --> we can also use this in piping

Wget and curl
--------------------------------------------------------------------------------------------------------------
1)wget https://github.com/dockerfile/ubuntu/blob/master/Dockerfile ---> It will download the file
2)curl https://github.com/dockerfile/ubuntu/blob/master/Dockerfile ---> It will print the file in terminal

cut and awk
----------------------------------------------------------------------------------------------------------------
1)cut ---> cut -d / -f1 ====> d- delimiter , f- fragment
2)awk ---> awk -F "/" '{print $1F}'

3)echo --> To print in the terminal
4)echo https://github.com/dockerfile/ubuntu/blob/master/Dockerfile | cut -d / -f1 - It will give https: is ANS
5)echo https://github.com/dockerfile/ubuntu/blob/master/Dockerfile |awk -F "/" '{print $1F}' -It will give https: is ANS
6)echo https://github.com/dockerfile/ubuntu/blob/master/Dockerfile |awk -F "/" '{print $NF}' - It will give Dockerfile is ANS

Editors
---------------------------------------------------------------------------------------------------------------
1)vim <file-name>--> It will fecth locally if the file is not there then it will create a file for us and open it
2):?<word to search ---> It will search from Bottom
3):/<word to find> ---> It will search from Top
4):q!--> It will not write what you enetered and quit
5)wq --> It will write what you enetered and quit
6):q --> It will quit and come out of the file7
7) esc and then click u ----> It will undo
8):yy -->yank/copy 
9)p--> Print
10)dd --> cut the lines
11)10p --> paste it 10 times
12)click g 2 times --> you can go top if you are in middle also
13)shift+g --> you can goto bottom

Permissions
-----------------------------------------------------------------------------------------------------------------
R --> Read
W --> Write
x --> Execute

user/owner --> The one who can create the file
group --> Generally the group user belongs to or anyother group
others --> Other than this user and group
1)create touch devops
2)add permissions like chmod u+x devops
3)remove permissions --> chmod u-x devops
4)chmod ugo+rwx devops --> It will give all access to the user and groups and others

R-4
W-2
X-1
chmod 750 devops ---> for users full access and group has read and execute and no access to others

Public and private key should not have permissions more than 600.
 





