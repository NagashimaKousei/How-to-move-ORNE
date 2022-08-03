# How-to-move-ORNE
This repository summarizes how ORNE works.
## Commands to use

 ・roslaunch orne_bringup orne_alpha.launch
 
 __Remember to change from alpha to beta when using this command__
 
 ・roslaunch orne_bringup orne_beta.launch
 
 ・roslaunch icart_mini_driver teleop_joy.launch
 
 **This command enables the use of the joy stick controller**

 __Map generation using joy stick controller__
 
 ・roslaunch orne_navigation_executor build_map_teleop.launch
 
 __Next, name the generated map__
 
 ・rosrun map_server map_saver -f 地図の名前
 
 __At this time, two files are created, one that is actually used for autonomous movement and one that is not__
 
 
 
