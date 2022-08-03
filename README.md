# How-to-move-ORNE
This repository summarizes how ORNE works.
# Commands to use

 ・roslaunch orne_bringup orne_alpha.launch
 
 //Remember to change from alpha to beta when using this command//
 
 ・roslaunch orne_bringup orne_beta.launch
 
 ・roslaunch icart_mini_driver teleop_joy.launch
 
 //This command enables the use of the joy stick controller//

 //Map generation using joy stick controller//
 
 ・roslaunch orne_navigation_executor build_map_teleop.launch
