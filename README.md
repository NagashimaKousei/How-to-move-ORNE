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
 
 __roslaunch orne_navigation_executor play_waypoints_nav_(alpha/beta).launch map_file:=(フルパスでmapのyamlファイルを指定※拡張子な)waypoints_file:=(フルパスでwaypointsのyamlファイルを指定※拡張子あり)__
 
 __最後に自律移動の開始 Rviz上にあるstart_waypoint_navigationボタンを押すと自律移動を開始します__
 
 __メモ__
 
 pwdを行うと自分のディレクトリーを知ることが出来る
 
 フルパスとは、自分のいるディレクトリーを指定してあげることを指す
 
 __0822で動かした際のエラー__
 
$ roslaunch orne_waypoints_editor edit_waypoints_viz.launch map_file:={mapファイル名} waypoints_file:={waypointsファイル名}.yaml
 
 ファイル名に注意して実行する
 
 __0824野外で動かした際に扱ったコマンド__
 
 rosbag record -a -O ファイル名
 
 rosbagを取ることが出来る
 
 # Referenced sites #
 https://github.com/open-rdc/orne_navigation/wiki/ORNE%E7%92%B0%E5%A2%83%E5%8B%95%E4%BD%9C%E3%81%AE%E6%89%8B%E9%A0%86
 
 https://qiita.com/srs/items/f6e2c36996e34bcc4d73
