# Karvinen 2021 — Install Debian on VirtualBox (Updated 2024)

I already installed Debian and reading this helped me understand why we choose these settings and what each step does.

# Karvinen 2020 — Command Line Basics Revisited

This is very useful because I often forget command syntax, and the article explains it clearly.
+ It introduces navigation commands like:
  * pwd (shows current location)
  * ls (lists files)
  * cd (moves between folders)
+ It explains how to read files using "less" which is better than opening big files in the editor.
+ It reviews basic file/folder actions like creating folders (mkdir), copying (cp), moving (mv), and removing (rm) directly.
+ It also mentions useful habits like tab completion and using history so beginners make fewer typing mistakes.
+ Even though I know some commands, this article helped me understand them more clearly and practice the correct way.

# Disable networking

+ When networking was enabled, ping worked and received replies. I stopped ping using Ctrl+C, because ping keeps sending packets until stop it. After disabling the network adapter, ping failed, proving the VM could not send packets to the internet.

# Port scan localhost

+ At first, the nmap command was not found because it was not installed. Next, I made sure my  network adapter is enable to install nmap, and then disabled the network again before scanning. This is "sudo nmap -A localhost" the command i used for testing.
+ At the end of the scan, Nmap prints something like: Nmap done: 1 IP address (1 host up) scanned in 8.42 seconds.
+ It is confirmed Nmap reported that one host was up and the scan finished successfully.

# Daemon scan

+ I installed a daemon (Apache web server) and scanned localhost again to see how the open ports change.
+ Install commands (with internet ON): sudo apt-get update and sudo apt-get -y install apache2
+ A daemon is a web server daemon that runs in the background and listens for HTTP connections.
+ After installing, I disabled the VirtualBox network adapter to disconnect from the internet before scanning command with sudo nmap -A localhost.
+ Before installing Daemon: Since i had the scanning result before which was "631/tcp open ipp — CUPS 2.4".
+ After installing Daemon: I saw a new open port: 80/tcp open http. So, this port was not open before installing Apache.
+ Eventually, before Apache, most “doors” were closed. After Apache, the web server opened a new door (port 80).

# Bandit oh-five

## Bandit Level 0

+ Initially, I did not find the ssh command because the SSH client was not installed on my system. I installed the OpenSSH client package with command "sudo apt-get -y install openssh-client" and then successfully connected to the Bandit server using SSH.
+ I connected to the Bandit server using SSH: ssh -p 2220 bandit0@bandit.labs.overthewire.org
+ The password for level 0 was bandit0 which was given in instructions.

## Bandit Level 0 to 1

+ I was instructed to find the next password in readme file.
+ After listing the file with ls command, i saw the file named with readme.
+ then, I entered using cat readme and I got the password for bandit1

## Bandit Level 1 to 2

+ In this level, the password for the next level is stored in a file called "-" located in the home directory.
+ i used the password that i found from the readme file for bandit1 and made list of all files.
+ Then i saw the "-" file and opened the file to get the next password.

## Bandit Level 2 to 3

+ In this level, the password was stored in a file named (--spaces in this filename--) also with dashes before and after the name.
+ At first I got “No such file or directory” because I did not type the exact filename. And i tried to look for in Youtube videos and also searched on Google but did not find the solution. Then I used chatgpt to look for the solution and I got the password. So the command was cat -- "--spaces in this filename--". But I do not understand why I used -- double dashes after cat. Eventually this printed the password for bandit2.

## Bandit Level 3 to 4

+ In this level, the password was stored in a hidden file in the "inhere" directory as "...Hiding-From-You".
+ Then used cat ...Hiding-From-You to open it and it printed the password.

## Bandit Level 4 to 5

+ Here the next password was stored in the only human-readable file in the "inhere" directory.
+ After making a list of all files using the ls -la command inside the inhere directory, I saw so many files named with -file00, -file01 etc.
+ Then I used this command file ./* to look for human readable file and that said -file07 (ASCII text) human readable.
+ Then i used the cat command to get inside the file and got the password.
 
## References

+ baeldung, blog, URL: https://www.baeldung.com/linux/daemon-guide
+ HackerSpolit, Youtube channel, URL: https://www.youtube.com/watch?v=ff2Au8BIy_A
