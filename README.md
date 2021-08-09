https://jsfiddle.net/tve5x2oc/


You can use the follow command to create inputs
* ffmpeg -i $INPUT_FILE -g 30  -preset fast -profile:v baseline -bsf h264_mp4toannexb output.h264
* ffmpeg -i $INPUT_FILE -c:a libopus -page_duration 20000 -vn output.ogg

Or pull from my website
* wget https://siobud.com/output.ogg
* wget https://siobud.com/output.h264
