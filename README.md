# ETWNetMonv3
## ETWNetMonv3 is simple C# code for Monitoring TCP Network Connection via ETW 
-----------------
"ETWNetMonv3.exe" is Windows App for read/watching ETW Logs (which made by ETWNetMonv3Agent.exe).

"ETWNetMonv3Agent.exe" is ETW Agent C# code and with this simple code you can have realtime TCPv4/v6 Connection Logs also with this tool you can Detect Meterpreter Payload via Signature (with switch SCAN , Detection for Remote Thread Injection) But this Signature worked very well only on Msfv4 (tested on Kali 2018, msf v4.17), Metasploit v6 (msf6) signature is chanaged so this old signature will not work on Msf6 ;)   

"ETWNetMon3Log.exe" is Command base tool for make XML/HTML report via "Queries" from ETW Logs (which made by ETWNetMonv3Agent.exe tool).

Note: this code was for (eBook Chapter-15), so i will publish pdf file for Part1 of ch15, and C# code for "ETWNetMonv3.exe" will publish with pdf (soon), but  "ETWNetMonv3Agent.cs" & "ETWNetMon3Log.cs" Codes are ready and you can use them and both PE files should be in the "same folder" because of log file "EtwNetMonv3logs.txt". (both codes need to work with this log file, this log file made by Agent & with ETWNetMon3Log.exe you can make HTML report from this file by simple Queries... "for make report with xml/html format, ETWNetMon3Log.cs is useful tool for [blue teams & defenders] for make HTML report [i hope]".

 1. ETWNetMonv3.exe Windows App (i will publish Code for this tool + pdf Chapter15 soon) 
 
 Note: in win10 you should run this tool with Admin ("Run as Admin")
 
   ![](https://github.com/DamonMohammadbagher/ETWNetMonv3/blob/main/Pic/ETWNetMonv3.png)

 -----------------------------------------------------------    
  
  2. ETWNetMonv3Agent.cs (ETW Agent)
 
 usage: 
    
    step1: [win] ETWNetMonv3Agent.exe [SCAN]/[DBG]
    EXAMPLE: [win] ETWNetMonv3Agent.exe
    EXAMPLE: [win (Run As Admin)] ETWNetMonv3Agent.exe SCAN
    Note: you need Run As Admin only for switch SCAN , this agent will make log file "EtwNetMonv3logs.txt"

   ![](https://github.com/DamonMohammadbagher/ETWNetMonv3/blob/main/Pic/ETWNetMonv3_02.png)

 -----------------------------------------------------------      
  
  3. ETWNetMon3Log.cs (Command base tool for make XML/HTML report via "Queries" from ETW Log file EtwNetMonv3logs.txt)
  
  Note: this file with ETWNetMonv3Agent.exe should be in the same folder (both work with log file EtwNetMonv3logs.txt)
 
 usage: 
    
    step1: [win] ETWNetMonv3Log.exe  [XML xmlfile.xml] [HTML "YOUR QUERY"]
    example: ETWNetMonv3Log.exe HTML "state LIKE '*synsent*'"
    syntax  1: switch XML, All ETW records from text [EtwNetMonv3logs.txt] will save to xml file (convert all records to xml)
    example 1: ETWNetMonv3Log.exe XML filename.xml
    syntax  2: ETWNetMonv3Log.exe HTML "your query"
    example 2: ETWNetMonv3Log.exe html "rport >=80 OR events LIKE '*Established*' AND events LIKE '*connect complete*'"
    example 2: ETWNetMonv3Log.exe html "events LIKE '*requested to connect*'"
    example 2: ETWNetMonv3Log.exe html "state NOT LIKE '*synsent*'"
    example 2: ETWNetMonv3Log.exe html "events LIKE '*'"
    example 2: ETWNetMonv3Log.exe html "rhost LIKE '192.168*' or lhost LIKE '192.168.1*'"
    example 2: ETWNetMonv3Log.exe html "rport <=80 OR lport >=50000"
    example 2: ETWNetMonv3Log.exe html "pname LIKE '*.exe*'"
    example 2: ETWNetMonv3Log.exe html "events LIKE '*C:\\*'"
    example 2: ETWNetMonv3Log.exe html "PID = 1452"
    
   ![](https://github.com/DamonMohammadbagher/ETWNetMonv3/blob/main/Pic/ETWNetMonv3_01.png)

 -----------------------------------------------------------    
    
    
    
<p><a href="https://hits.seeyoufarm.com"><img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FDamonMohammadbgher%2FETWNetMonv3"/></a></p>
