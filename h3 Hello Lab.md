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

#
