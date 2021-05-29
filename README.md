# ETWNetMonv3
## ETWNetMonv3 is simple C# code for Monitoring TCP Network Connection via ETW 
-----------------
"ETWNetMonv3.exe" is Windows App for read/watching ETW Logs (which made by ETWNetMonv3Agent.exe).

"ETWNetMonv3Agent.exe" is ETW Agent C# code and with this simple code you can have realtime TCPv4/v6 Connection Logs also with this tool you can Detect Meterpreter Payload via Signature (with switch SCAN) But this Signature worked very well only on Msfv4 (tested on Kali 2018, msf v4.17), Metasploit v6 (msf6) signature is chanaged so this old signature will not work on Msf6 ;)   

"ETWNetMon3Log.exe" is Command base tool for make XML/HTML report via "Queries" from ETW Logs (which made by ETWNetMonv3Agent.exe tool).

Note; this code was for (eBook Chapter-15), so i will publish pdf file for Part1 of ch15, and C# code for "ETWNetMonv3.exe" will publish with pdf (soon), but  "ETWNetMonv3Agent.cs" & "ETWNetMon3Log.cs" Codes is ready and you can use them and both PE files should be in the "same folder" because of log file "EtwNetMonv3logs.txt". (both codes need to work with this file, this log file made by Agent & with ETWNetMon3Log.exe you can make HTML report from this file by simple Queries...

<p><a href="https://hits.seeyoufarm.com"><img src="https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FDamonMohammadbgher%2FETWNetMonv3"/></a></p>
