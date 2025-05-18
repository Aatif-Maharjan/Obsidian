https://tryhackme.com/room/ninjaskills

Here find command plays a very important role on finding all the files

![[Pasted image 20250512134108.png]]
```
/ alocates the location for search 
-type f = defines the type of binary we are searchinf for (d can be used for directory searching)
\( \) = used for working multiple thing at once
-o = or logic gate
-name = flag for name of file
```

```
found files
/mnt/D8B3
/mnt/c4ZX
/var/FHl1
/var/log/uqyw
/opt/PFbD
/opt/oiMO
/media/rmfX
/etc/8V2L
/etc/ssh/SRSq
/home/v2Vb
/X1Uy

```


**Which of the above files are owned by the best-group group(enter the answer separated by spaces in alphabetical order)**
```
find -type f -group best-group
```

**Which of these files contain an IP address?**

Using Regex
> **Link:-** [https://www.shellhacks.com/regex-find-ip-addresses-file-grep/](https://www.shellhacks.com/regex-find-ip-addresses-file-grep/)
![[Pasted image 20250512141152.png]]


**Which file has the SHA1 hash of 9d54da7584015647ba052173b84d45e8007eba94**
![[Pasted image 20250512140636.png]]

**Which file contains 230 lines?**
All the files had 209 lines but later a file was not found which was bny0.

```
find / -type f \( -name 8V2L -o -name bny0 -o -name c4ZX -o -name D8B3 -o -name FHl1 -o -name oiMO -o -name PFbD -o -name rmfX -o -name SRSq -o -name uqyw -o -name v2Vb -o -name X1Uy \) -exec ls -lahn {} \; 2>>/dev/null

```


- `-exec ls -ln {} \;`: For each matching file, it runs `ls -ln` (long listing with numeric UID/GID).
    
- `{}` is replaced with the current filename.
    
- `\;` marks the end of the `-exec` command.
    
- `2>>/dev/null` discards errors (like permission denied).

**Which file's owner has an ID of 502?**
![[Pasted image 20250512140046.png]]
