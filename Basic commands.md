#### Create/Make directory (Creates new folder)
`mkdir [directory_name]`

#### Removes directory (Deletes new folder)
`rmdir [directory_name]`

#### Creates new empty folder
`touch [file_name]`

#### Copy file. Copies a file to a new location.
`cp [source_file] [destination]`

#### Move file. Moves or renames a file.
`mv [source_file] [destination]`

#### Remove file. Deletes a file. Use with caution, as it does not send to Trash.
`rm [file_name]`

#### Usage for `rm` (forcefully)
##### Delete (remove) file bypassing confirmation prompt
`sudo rm -rf path/to/directory`

* This command is powerful and can permanently delete files and directories without sending them to the Trash. Double-check the path to ensure you are deleting the correct item, as mistakes can lead to data loss.
* The command will not work for files that are protected with *System Integrity Protection (SIP)* unless it is temporarily disabled in the recovery mode.

### Misc
#### - `pwd`: Print Working Directory. Shows the full path of your current location.
#### - `ls`: List directory contents. Shows files and folders in the current directory.

##### Sample Output/Usage:
```
adminkw@Kwr-MacBook-Pro ~ % ls /Users/adminkw/Pictures
AppIcons		                Photos Library.photoslibrary
Lightroom		                Photoshop
Lightroom Library.lrlibrary     Screenshot
Photo Booth Library	         	Wallpapers
```

##### - `ls -l`: Provides a detailed list (permissions, owner, size, date).
##### - `ls -a`: Shows all files, including hidden ones (those starting with a dot).
#### - `cd [directory_name]`: Change Directory. Moves you to a specified directory.
##### - `cd ..`: Moves up one level in the directory hierarchy.
##### - `d ~`: Returns to your home directory.
