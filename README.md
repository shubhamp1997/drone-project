# drone-project
Dynamic Traffic Management and Vehicle Track and count using Drones

# 1. Connecting to DJI Tello Drone: 
1.1. Place the batteries inside the drone and press the switch on button on the drone placed on the left side.
1.2. wait for a second untill the front LED indicator on the drone starts blinking in yellowish color. 
1.3. Locate the Tello Wifi Network in your Wifi List and then connect to it. 
<img width="269" alt="tello wifi" src="https://user-images.githubusercontent.com/50179614/110765106-d7e9a780-8279-11eb-9f3f-bf2c342ecf5b.png">
 

# To see it in action:

1. Open Two Command prompts in the working directory (or just open cmd and then direct it to the folder using 'cd' command) 
2. In the first command prompt: type "python tello-command.py" and hit enter, this will initialise the tello drone. (Your DJI tello drones must be connceted for this step. refer to 1.1 Connecting the Drone topic to follow thorugh).
3. Type "command" and hit enter, this will tell the drone to operate in a command prompt way.
4. after which you should see a "response ok".
5. after this you can tell your drone to takeoff etc, simply type "takeoff" and hit enter.
6. Type "streamon" and hit enter, this will switch on the camera stream for the next process to follow.
7. Now in the second command prompt copy and paste this command:

python detect_video.py --weights ./checkpoints/yolov4-tiny-416 --size 416 --model yolov4 --video 0 --output ./data/video/output.avi --count --tiny

7. This will run the detect_video.py file and instruct it to use the camera stream as an input to detect the cars and then save the output in an "output.avi" file in the data/video folder.


