# mp3split
Split mp3 file by timestamps listed in file


## Installation


 Install ffmpeg to convert videos into mp3 using yt-dlp
```
sudo apt install ffmpeg
```

Grab yt-dlp to download videos
```
wget https://github.com/yt-dlp/yt-dlp/releases/download/2023.03.03/yt-dlp_linux -O yt-dlp
chmod +x yt-dlp
```

Grab this script to split mp3s
```
wget https://raw.githubusercontent.com/somik123/mp3split/main/mp3split.sh -O mp3split.sh
chmod +x ~/mp3split.sh
```


### Usage:

Create a file with the timestamps
```
nano track.txt
```

It should be in the format:
```
00:00 Song name A
02:31 Song name B
05:05 Song name C
...
...
...
```

Then download/transfer the mp3 file into the folder and run mp3 split.

Download from youtube:
```
~/yt-dlp -x -f ba --audio-quality 0 --audio-format mp3 -o music.mp3 https://www.youtube.com/watch?v=T7GgcrTqZj4
```

Split songs
```
~/mp3split.sh music.mp3 track.txt
```
