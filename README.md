# Chrome Window for Presenting (Mac)
---
![Screenshot 2024-08-21 at 14 31 47](https://github.com/user-attachments/assets/6aafec19-4593-41e8-b444-be4be6bd32a0)

Launches a <ins>clean</ins> Chrome window with no tabs or menu bars. Perfect for when you need to share a chrome tab or slide presentation and you want to hide the bookmarks and toolbar. 


## Quick Start Installation 
Save the window.sh file to your machine. Make it executable, and then run it from the command line.

`./window.sh paste_your_link_here`


## Walkthrough Installation


1. Open up a terminal window on your Mac
2. Type the following command to open a text editor

    `nano window.sh`

3. Copy and paste the following code into the text editor:

```
#! /bin/bash

#check to see if $1 has a value
 if [ "$#" -eq  "0" ]    
    then 
        read -p "Link:" LINK1
        /Applications/Google\ Chrome.app/Contents/MacOS/Google\ Chrome --app=$LINK1
else

    /Applications/Google\ Chrome.app/Contents/MacOS/Google\ Chrome --app=$1
fi
exit
```
4. Save and exit the text editor `Ctrl + x` then type `y` then hit `enter`
5. Make the script executable with this command `chmod +x window.sh`
6. Now you are ready to use the script. In terminal type `./window.sh` followed by your link like this `./window.sh google.com`
7. Profit
