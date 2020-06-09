# Rtmp_Stream
Using opencv and ffmpeg library to stream the capture card output in vlc 

## Requirements
ffmpeg , opencv

## Execution command
sudo g++ -g opencv_rtmp.cpp -lavcodec -lavformat -lavutil -lswscale  -lavutil  `pkg-config opencv --cflags --libs`

sudo ./a.out 3 30 640 480 300000

ctrl + c to exit

To view video, open vlc then File->Open Network Stream, Enter Ip: "rtmp://localhost/live/stream" 

    Argument list
    * argv[1] = capture card device no
    * argv[2] = frames per second
    * argv[3] = width
    * argv[4] = height
    * argv[5] = bitrate

## Issues

when executed for first time, able to start and stream in vlc, but when tried to run again with same parameters getting an segmentation fault error, after repeating 3 or 4 times, I am able to stream again


