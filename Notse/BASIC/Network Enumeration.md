### Nmap
Best for network enumeration.


### Rustscan
used to find open port

nmap 10.10.93.132 -sT -vv -T4 -Pn --packet-trace
common used ports

## ffuf
**ffuf** stands for fast web fuzzer
Directory fuzzing is faster in ffuf.

```ffuf
ffuf -u http://10.10.131.17/FUZZ -w wordlists/seclists/Usernames/xato-net-10-million-usernames-dup.txt

here flag,-u indentifies the host where FUZZ is the main part. 
FUZZ is placed for Fuzzing the part you need. 
-w defines wordlist  
```

## enum4linux

https://www.kali.org/tools/enum4linux/

```

enum4linux -a 10.10.105.160 > file 
-a = aggresive scan
redirecting result to file 
```

