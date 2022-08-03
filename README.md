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
 
 __次に作った地図にwavy_pointを置くコマンド__
 
 ・roslaunch orne_waypoints_editor edit_waypoints_viz.launch map_file:={mapファイル名} waypoints_file:={waypointsファイル名}.yaml
 
 __この際に気を付けることはwavy_pointを置く場所はカーブの曲がり角とその先に置くことを忘れない__
 
 
 __コストマップ 自律移動時のコストマップの作成を行います。作成したファイル_for_costmap.yamlを追加する__
 
 __roslaunch orne_navigation_executor play_waypoints_nav_{alpha/beta}.launch map_file:={フルパスでmapのyamlファイルを指定※拡張子なし}waypoints_file:={フルパスでwaypointsのyamlファイルを指定※拡張子あり}__
 
