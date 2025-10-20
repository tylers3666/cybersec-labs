# tk-elevator

**Platform:** DAMSEC  
**Category:** Misc  
**Difficulty:** 100 points (2 flags)  
**Date Completed:** 2025-10-13

---

## 1. Summary
Basic Linux commands/navigation

## 2. Methodology
Level 0:
- The level 0 credentials are just stored in a text file within the creds_level1 folder

Level 1:
- Level 1 has lots of randomly named directories, so I just ran `find ./ -name "*creds*"` to find a file with "creds" in the name
- This showed the directory, which I could just cat from there

Level 2:
- creds_level3.txt is a very large text file with a bunch of random text, so I used grep
- Originally I tried grep pass, but this showed up a lot in the text, so I had to narrow to grep password

Level 3:
- Level 3 has a bash file named `creds_level4.sh`, but the file does not have execution permissions by default
- Running `chmod +x` gives the file execute permissions, and from this point I can run the file which gives the next password

Level 4:
- There is no visible creds file in level 4, and the README file has a hint that says "ls has a lot of options"
- Running `ls -a` shows a .hidden_creds_level5 directory with another hidden text file inside of it, which has the next credentials

Level 5:
- The README file gives a hint about a flag at the root, and there is infact a flag_1.txt file at the root directory. flag_2.txt is also here, but we do not have permissions to read it yet
- The credentials for this level are just in a folder in the home directory, the only issue being the spaces in the directory and file names

Level 6:
- Level 6 has a `server.sh` file that doesn't seem to do anything, and running cat on this file just shows a bash script that sleeps forever
- The README for this level says the password was exposed when starting the server, so I originally looked for a log file but couldn't find anything
- Running `ps -aux` shows a bunch of running processes, some that seem to correspond to all of the different users in the CTF 
- Greping for password gives a bunch of results, but each one has a unique username, and you are unable to login to different users, only different levels
- Greping for `level6_54235` in my case shows only one result for my 'ID', which shows the credentials for level 7

Level 7:
- Level 7 opens VIM, which I had to exit (magic)
- After exiting VIM, the creds are just in the home directory

Level 8:
- Level 8 wants me to make a git commit, but I didn't want to do this
- Reading project/.git/logs/HEAD gives the password for the next level

Level 9:
- The creds file in level 9 is incomplete, and the README claims the credentials were lost and need to be recovered
- Running `ls -la` shows a .creds_level10.txt.swp file, a file created by VIM to save changes in case of unexpected crashes
- This file shows the level 10 password

Level 10:
- On this level, I can read /flag_2.txt to find the second flag

## 3. Commands & Tools Used
`find`: used to find files  
`grep`: used to find specific text within a file  
`ls -a`: used to show hidden files  
`ps -aux`: ps to list processes, -a shows processes for all users, -u shows who owns each process, and -x includes processes without a controlling terminal. I am in the habit of using -aux when looking for most information  
`chmod +x`: chmod is used to change permissions for a file, +x gives execute permission

## 4. Lessons Learned
This CTF wasn't super complicated or challenging in any specific way, especially as someone who has previously used Linux. However, I am becoming more comfortable with Linux and CLIs in general the more I practice with them.