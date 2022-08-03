# How-to-move-ORNE
This repository summarizes how ORNE works.
## Commands to use

 ・roslaunch orne_bringup orne_alpha.launch
 
 _Remember to change from alpha to beta when using this command_
 
 ・roslaunch orne_bringup orne_beta.launch
 
 ・roslaunch icart_mini_driver teleop_joy.launch
 
 //This command enables the use of the joy stick controller//

 //Map generation using joy stick controller//
 
 ・roslaunch orne_navigation_executor build_map_teleop.launch
 
 //Next, name the generated map//
 
 ・rosrun map_server map_saver -f 地図の名前
 
 //At this time, two files are created, one that is actually used for autonomous movement and one that is not//
 
 
 
