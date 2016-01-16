# *nix Scavenger Hunt

Complete the following challenges using the command-line interface on your favorite
Unix or Linux operating system. You are welcome and encouraged to consult any
additional documentation online or in books.

Please add your answers/responses/text pastes to the document after each prompt.

Note: For some of the challenges you will need to reference files included with
this repository, so you will need to fork the repo into your own Github account
and then clone it to your development environment.

## The Challenges

### Navigating the Filesystem

* Get an idea of where you are in the operating system. Use the `pwd` command to find your "path to working directory"--your current location in the filesystem of your devbox. 
*Paste the output of the `pwd` command here:*

/home/cabox/workspace                                     




* Discover more about this filesystem. Use `ls` (the "list" command)to see what is in this directory. 
*What directories and files do you see when you run `ls`?*

LICENSE          nix_scavenger_hunt.md                   
README.md        nix_scavenger_hunt_stretch.md           
challenge_files 




* You can use *options* to modify how a command runs. Try using `ls -alh` to see the contents of your current directory. 
*How are the results different when you use the `-alh` options?*

Result includes files sizes and timestamps:
total 36K                                                   
drwxrwxr-x 4 cabox cabox 4.0K Jan 15 19:37 .                
drwxr-xr-x 9 cabox cabox 4.0K Jan 15 19:37 ..               
drwxrwxr-x 8 cabox cabox 4.0K Jan 15 19:37 .git             
-rw-rw-r-- 1 cabox cabox 1.1K Jan 15 19:37 LICENSE          
-rw-rw-r-- 1 cabox cabox 1.4K Jan 15 19:37 README.md        
drwxrwxr-x 7 cabox cabox 4.0K Jan 15 19:37 challenge_file   
s                                                           
-rw-rw-r-- 1 cabox cabox 5.7K Jan 15 19:56 nix_scavenger_   
hunt.md                                                     
-rw-rw-r-- 1 cabox cabox  317 Jan 15 19:37 nix_scavenger_   
hunt_stretch.md    




* The `man` ("manual") command tells you more about how any given command works. (*WARNING:* CodeAnywhere does not support the man command. You can click the following link to complete this task: http://linux.die.net/man/)Run `man` to see instructions about how to use `man`. Then use `man` to learn what the `a`, `l`, and `h` options mean when used with the `ls` command. 
*Write down what those options do?*

ls -a: do not ignore entries starting with .
Result:
-bash: man: command not found               
cabox@box-codeanywhere:~/workspace$ ls -a   
.        README.md                          
..       challenge_files                    
.git     nix_scavenger_hunt.md              
LICENSE  nix_scavenger_hunt_stretch.md  

l: use a long listing format
Result:
total 24                                    
-rw-rw-r-- 1 cabox cabox 1086 Jan 15 19:37 L
ICENSE                                      
-rw-rw-r-- 1 cabox cabox 1367 Jan 15 19:37 R
EADME.md                                    
drwxrwxr-x 7 cabox cabox 4096 Jan 15 19:37 c
hallenge_files                              
-rw-rw-r-- 1 cabox cabox 6870 Jan 15 20:15 n
ix_scavenger_hunt.md                        
-rw-rw-r-- 1 cabox cabox  317 Jan 15 19:37 n
ix_scavenger_hunt_stretch.md 

h: -human-readable
with -l, print sizes in human readable format (e.g., 1K 234M 2G)
Result:
LICENSE                                     
README.md                                   
challenge_files                             
nix_scavenger_hunt.md                       
nix_scavenger_hunt_stretch.md 




* Commands can also take *arguments*, which are usually the names of files or locations that you want the command to work with. Try running `ls /` to see what files are in the *root* directory of the filesystem. 
*What files and directories do you see listed?*

bin   etc       lib    mnt   root  srv  usr 
boot  fastboot  lib64  opt   run   sys  var 
dev   home      media  proc  sbin  tmp 




* A Unix filesystem has a few special shortcuts to refer to specific locations. `/` indicates the *root* of the filesystem, meaning the top-most directory in the filesystem hierarchy. Use the `cd` ("change directory") command to move to the root directory. 
(Hint: Use `man` to look up the `cd` command if you have any issues) *Then run `pwd` and paste the output here:*

/




* Another special shortcut in Unix is the `~` location. This indicates the *user root* directory, meaning the top-most directory in the hierarchy that comes below your user account. Use `cd` to move to `~`. 
*Run `pwd` and paste the response here:*

/home/cabox                                 




* Change directory into the `challenge_files` directory. Use `ls` to find only the files with a `.demo` pattern. 
*How many files do you find?*

3



* Use the `cd` command to move "up" one directory. 
*Where are you in the filesystem now?*

/home/cabox/workspace                                    




* Press the up arrow on your keyboard. 
*What just happened?*

Brought up the last entered command:
cabox@box-codeanywhere:~/workspace$ pwd




* Press the up arrow a few more times. 
*What do you see?*

Each press of the up arrow brings up the next command previously entered in reverse order.




* Run the `history` command. 
*What do you see?*

History of my last 40 entered commands.




### Observing the System

* Discover what account you are logged into using the `whoami` command. 
*What username are you currently using?*

cabox



* Discover who else is on your system with the `who` command. 
*Are any other users using your system? If so, list them here:*

No other users
Result:  cabox    pts/0        Jan 15 19:40 (54.69.152.243) 




* How long has your system been running? 
Use `uptime` to see, and *paste the result here:*

21:33:19 up  1:56,  1 user,  load average: 0.00, 0.00, 0
.00 




* Run `ps aux` and review the results. (Hint: Use `man` to learn more about the `ps` command and options.) 
*How do you interpret what you see here?*

Command stands for Process Status and displays process history including user (from user ID), PID (process ID), %CPU (percentage of CPU usage), %MEM (percentage og memory usage), VSZ (virtual size in Kbytes), RSS (resident set size), TTY (full name of control terminal), STAT (symbolic process state), START (time started), TIME (accumulated CPU time, user + system), and COMMAND (command and arguments).




* Run `top` and review the results. (Hint: You may need to use `ctrl-c` to get out of this app.) 
*How do you interpret what you see here?*

Command displays and updates sorted information about processes. Displays much the same information as 'ps aux' command but continually updates live processes rather than history.




### Finding and Viewing Files

* Make sure you are in the `challenge_files` directory. Use the `*` wildcard to find all the files that have the word "credit" in the filename. 
*How many files did you find?*

2




* Use the `more` command to view one of the `credit_cards` files you just discovered. (Hint: Type `q` to quit viewing the file. Press the `spacebar` to page down. Use your keyboard arrows to move up/down.) 
*What is the date in the file you have viewed?*

01-15-2015




* Use the `find` command to search for files more effectively. Search the sub-directories under `challenge_files` to find the location of the file named `modi_laboriosam.txt`. 
*Where is that file located?*

/home/cabox/workspace/challenge_files/tmp/modi
_laboriosam.txt 




* Use the `grep` command to search for text within a file. Use `grep` on all the `.user` files in `challenge_files` to find which files contain "WA" (the abbreviation for Washington state). 
*How many files did you find?*

2




* Use the `-r` option of `grep` to *recursively* find the text "Waldo" hidden in a file somewhere under the `challenge_files` directory. 
*Paste the result showing the file and line where the word "Waldo" shows up.*

serial-numbers/eaque_molestiae.txt:  Ut est maio
res quia autem. Nisi modi Waldo sed corporis s
it explicabo ut est. Et est placeat ea sunt su
nt consectetur sunt incidunt. Explicabo vel es
se blanditiis dolorem culpa non quia.




### Pipes and Connecting Commands

* Sometimes it's useful to output the results of a command to a text file for further analysis, reference, or processing. Try running `ls > files.txt`. Notice that the file `files.txt` was created. View that file using `more`. 
*What do you see in the `files.txt` file?*

Usage: more [options] file...                   
                                                
Options:                                        
  -d        display help instead of ring bell   
  -f        count logical, rather than screen li
nes                                             
  -l        suppress pause after form feed      
  -p        suppress scroll, clean screen and di
sblay text                                      
  -c        suppress scroll, display text and cl
ean line ends                                   
  -u        suppress underlining                
  -s        squeeze multiple blank lines into on
e                                               
  -NUM      specify the number of lines per scre
enful                                           
  +NUM      display file beginning from line num
ber NUM                                         
  +/STRING  display file beginning from search s
tring match                                     
  -V        output version information and exit




* Notice that if you run `ls -alh` in the `challenge_files` directory, the files scroll by very quickly. Sometimes it would be better to get the results in a paginated format. Try running `ls -alh | more`. 
*Describe what you see when you run `ls -alh | more`.*

Shows my user name, file name, file size, creation date, and timestamps for files in directory.




* Earlier, when you viewed the list of active processes on your devbox using `ps aux`, the list was probably really long. You can make this list more manageable by using the pipe (`|`) to filter the results of `ps` using `grep`. Run `ps aux | grep <your_username>` to see what processes are running for your specific user. 
*Paste the list of processes that reference your username here:*

root       557  0.0  0.6  63876  3484 ?        Ss   19:40   0:00 sshd: 
cabox [priv]                                                           
cabox      559  0.0  0.2  64012  1484 ?        S    19:40   0:00 sshd: 
cabox@pts/0                                                            
cabox      560  0.0  0.3  18140  2044 pts/0    Ss   19:40   0:00 -bash 
root       602  0.0  0.6  63876  3488 ?        Ss   22:40   0:00 sshd: 
cabox [priv]                                                           
cabox      604  0.0  0.2  63876  1468 ?        S    22:40   0:00 sshd: 
cabox@pts/1                                                            
cabox      605  0.0  0.3  18124  2004 pts/1    Ss+  22:40   0:00 -bash 
root       615  0.0  0.6  63876  3344 ?        Ss   22:44   0:00 sshd: 
cabox [priv]                                                           
cabox      617  0.0  0.2  64008  1496 ?        S    22:44   0:00 sshd: 
cabox@notty                                                            
cabox      618  0.0  0.1  12780   868 ?        Ss   22:44   0:00 /usr/l
ib/openssh/sftp-server                                                 
cabox      625  0.0  0.2  15520  1140 pts/0    R+   23:03   0:00 ps aux
cabox      626  0.0  0.1   8816   764 pts/0    S+   23:03   0:00 grep -
-color=auto cabox 


