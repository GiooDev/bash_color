bash_color
==========

This script allows you to have a shiny colored prompt.

```
┌─[13:37:00]─[gioodev@Gio-Server]─[~]
└[✓]─> $ 
```

Here is the differents colors used for the prompt :
- Green if you are logged with a standard user locally.
- Red if you are logged with root locally.
- Yellow if you are logged on a remote computer.

## Installation

Copy the bash.bash_color script under /etc/ directory with `chmod 600`

Then you just have to configure in the #Configuration part the name of your local computer.
```
local desk="<LOCAL_COMPUTER_NAME>"
```

To activate the bash_color script, you just have to source it in your .bashrc
- for root : in /etc/bash.bashrc 
- for other users in their home directory /home/.../.bashrc
```
# Activating coloration prompt
if [ -f /etc/bash.bash_color ]; then
    . /etc/bash.bash_color
fi
```

You can also copy the script once edited with the name of your local computer name on each server you want to access. Then, your prompt will be in yellow.
`scp /etc/bash.bash_color user@distant:/etc/`

Then source it also in your distant .bashrc file.
