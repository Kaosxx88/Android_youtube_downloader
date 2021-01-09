# Android_youtube_downloader (Termux - terminal)

# Manual installation
Install Termux from the google store

Open Termux and write the following commands:
```
termux-setup-storage
```
```
apt-get install python
```
```
pip install youtube-dl
```
```
apt-get install ffmpeg
```
#### Create a new file and edit it: 
```
nano yt-down.sh
```
#### Write the follow code inside
```
# bring the user in the main folder
cd
# move the user on the music folder
cd storage/music
# start yt downloader in audio only mode conversion
youtube-dl --extract-audio --audio-format mp3 $1
```
#### Give the permission to the app 
```
chmod +x yt-down.sh
```

#### Add the aliasis to the bashrc file:
open the file
```
nano /data/data/com.termux/files/usr/etc/bash.bashrc
```
write the aliases at the end of the file
```
alias dl='./yt-down.sh'

alias xclip='xclip -selection v'

```
press (ctrl + x) to save the changes
press (y) to accept
press (Enter)
restart Termux
``` 
exit
```
#### Sample

Go on youtube chose your video and copy the link
open termux
```
dl {link from youtube}
```
```
dl https://www.youtube.com/watch?v=A16VcQdTL80
```
The mp3 file will be store on storage/music
Open myfile android app on the device
Go to internal storage/music
Select the mp3 -> select move -> move here (needed to update the library)
Now any music app will see the mp3 file

#### Screenshot
<p align="center">
  <img src="https://github.com/Kaosxx88/Android_youtube_downloader/blob/main/Screenshots/downloading_process.jpg?raw=true">
</p>

### Upgrade
```
pip install --upgrade youtube-dl
```

# Automatic  installation

...Coming soon...
