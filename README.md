This repo is deprecated, see [play-from-disk-h264](https://github.com/pion/example-webrtc-applications/tree/master/play-from-disk-h264) for a maintained version.

------

This repo demonstrates how you can use Pion WebRTC to play H264 and Ogg from disk. These same APIs
can be used to pull from other sources.

### You can use the follow command to create inputs
* ffmpeg -i $INPUT_FILE -an -c:v libx264 -bsf:v h264_mp4toannexb -b:v 2M -max_delay 0 -bf 0 output.h264
* ffmpeg -i $INPUT_FILE -c:a libopus -page_duration 20000 -vn output.ogg

### Or pull from my website
* wget https://siobud.com/output.ogg
* wget https://siobud.com/output.h264

# Open play-from-disk-h264 example page
[jsfiddle.net](https://jsfiddle.net/tve5x2oc/) you should see two text-areas and a 'Start Session' button

### Run play-from-disk-h264 with your browsers SessionDescription as stdin
The `output.ogg` and `output.h264` you created should be in the same directory as `play-from-disk-h264`. In the jsfiddle the top textarea is your browser, copy that and:

#### Linux/macOS
Run `echo $BROWSER_SDP | play-from-disk-h264`
#### Windows
1. Paste the SessionDescription into a file.
1. Run `play-from-disk-h264 < my_file`

### Input play-from-disk-h264's SessionDescription into your browser
Copy the text that `play-from-disk-h264` just emitted and copy into second text area

### Hit 'Start Session' in jsfiddle, enjoy your video!
A video should start playing in your browser above the input boxes. `play-from-disk-h264` will exit when the file reaches the end

Congrats, you have used Pion WebRTC! Now start building something cool
