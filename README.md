https://jsfiddle.net/9s10amwL/

* ffmpeg -i $INPUT_FILE -g 30  -preset fast -profile:v baseline -bsf h264_mp4toannexb output.h264
* ffmpeg -i $INPUT_FILE -c:a libopus -page_duration 20000 -vn output.ogg
