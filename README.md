# How-to-move-ORNE
This repository summarizes how ORNE works.
## Commands to use

 ・roslaunch orne_bringup orne_alpha.launch
 
 __ここでalphaからbetaに変更することを忘れない__
 
 ・roslaunch orne_bringup orne_beta.launch
 
 ・roslaunch icart_mini_driver teleop_joy.launch
 
 **このコマンドはjoy stick controllerで地図を生成したい際に使います**

 __joy stick controllerを使って地図を生成するコマンドである__
 
 ・roslaunch orne_navigation_executor build_map_teleop.launch
 
 __次に地図の名前を決める__
 
 ・rosrun map_server map_saver -f 地図の名前
 
 __この際に地図を2つ作る__
 
 __1つは自律移動をする際に必要となるコマンドであり、２つ目はテスト用のものである__
 
 
 
