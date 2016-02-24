Mostly placeholders for random scripts.

bash_threader.sh -  Simple bash script to read in a file of commands over $2 threads. Best used with named pipes:

[matt@chaptop random_scripts]$ TC=8 ; CMDSTR="/usr/bin/figlet"
[matt@chaptop random_scripts]$ ./bash_threader.sh <(for val in `seq 1 $TC` ; do echo -e "$CMDSTR $val" ; done) $TC
0 3
Running bash -cl "/usr/bin/figlet 1" as PID 18942
Running bash -cl "/usr/bin/figlet 2" as PID 18947
Running bash -cl "/usr/bin/figlet 3" as PID 18949
Thread spreader done, the following threads remain: 18942
 _ 
/ |
| |
| |
|_|
   
 _____ 
|___ / 
  |_ \ 
 ___) |
|____/ 
       
 ____  
|___ \ 
  __) |
 / __/ 
|_____|
       
