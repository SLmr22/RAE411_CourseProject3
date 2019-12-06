# RAE411_CourseProject3

Through this project we will launch a VLC stream in HD (720p, 30 fps) from the command prompt. 
We therefore need a data rate of about 2500 kbps.
To do this, we will launch a script with the VLC parameters: movie to stream, videom codec, audio codec, bit rate, 
standard ab value, transcoding quality, access method, audio/video format, stream access link with ip and port

vlc -vvvv film.mp4 --sout '#transcode{vcodec=mp4v,acodec=mpga,vb=2500,hq,ab=128}:standard{access=http,mux=ogg,dst=192.168.1.101:8080}'

In parallel we observe the exchanges on the network with TCPDUMP
