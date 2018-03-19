# windows-container-help
Snippets, known issues, examples for windows docker containers

* with microsoft/aspnet

this one shows running in the unmodified aspnet container interactively, and mapping a host disk folder to a folder in the container:

`docker run -it -v c:\temp:c:\philtemp --rm microsoft/aspnet:3.5`
to view
```
docker ps
docker exec -it <container id from previous command> cmd /c dir
```
will show output like 
```
 Volume in drive C has no label.
 Volume Serial Number is EC9B-9EAC

 Directory of C:\

03/19/2018  11:38 AM    <DIR>          inetpub
11/22/2016  05:45 PM             1,894 License.txt
07/16/2016  08:18 AM    <DIR>          PerfLogs
03/19/2018  11:37 AM    <SYMLINKD>     philtemp [\\?\ContainerMappedDirectories\60E00399-DF1D-4EB0-94BB-C15EBCDA26F7]
02/13/2018  06:40 PM    <DIR>          Program Files
02/13/2018  06:40 PM    <DIR>          Program Files (x86)
02/13/2018  08:07 PM           176,736 ServiceMonitor.exe
02/13/2018  08:07 PM    <DIR>          Users
02/13/2018  08:06 PM    <DIR>          Windows
               2 File(s)        178,630 bytes
               7 Dir(s)  21,123,121,152 bytes free
```
