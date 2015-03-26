Pisa Hand Model
===============

If you want to use the Pisa model hand, yuo can move pisa_hand_description and pisa_hand_publisher folders in your catkin_ws and launch it with "roslaunch pisa_hand_description display.launch" by terminal.

You can select the visual mode, modifing the line #6 in pisa_hand_description/launch/display.launch :

<arg name="use_joint_state_publisher" default="false"/> : in this mode,the model hand has 18 dof (15 fot the hand), because the distal phalange of index, middle,ring and little finghers, and middle abduction are zero. You will see the visualitation of the angles data written in "data.txt" (you can modifie this file, remembering that the number of columnes must be 15 and it's better that the number of rows is equal to "campioni" variable at line #39
in pisa_hand_publisher/src/pisa_hand_publisher.cpp).

<arg name="use_joint_state_publisher" default="true"/> : in this mode, the model hand has 23 dof and you have a GUI, in which you can modify the value of each hand joint as you prefer.
