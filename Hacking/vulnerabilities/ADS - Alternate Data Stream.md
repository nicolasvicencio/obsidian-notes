#windows 

Is a NTFS file attribute and was designed to provide compatibility with the MacOS HFS

Any file created on an NTFS formatted derive will have two different forks/streams:
- Data stream - Default stream that contains the data of the file
- Resource stream - Typically contains the metadata of the file

We can hide malicious code or executable in the file attribute resource stream( metadata ) of a legitimate file.

You can hide things in files
```powershell
executable.exe > winlog.txt:executable.exe
```