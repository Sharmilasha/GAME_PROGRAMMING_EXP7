# GAME_PROGRAMMING_EXP7
AIM:
To implement-chasing when AI see the player.

ALGORITHM:
~~
STEP 1: Set up the AI character Blueprint:
1)Create an AI character Blueprint (if you haven't already) following the steps mentioned earlier.
2)Add a Sphere Collision component to the AI character Blueprint.
3)Position and scale the Sphere Collision component to represent the AI's detection range.
4)Set the Sphere Collision component's collision settings to overlap with the player character.
~~~
STEP 2: Create a new AI controller Blueprint:
1)In the Content Browser, right-click in the desired folder.
2)Select Create Basic Asset > Blueprint Class.
3)Choose the AIController as the parent class.
4)Name the Blueprint (e.g., "AIController_Chase") and click Create.
~~~
STEP 3: Open the AIController Blueprint:
1)In the Blueprint editor, locate the Event Begin Play event.
2)Drag off the execution line and search for "Set Sight Radius".
3)Set the Sight Radius value to the desired range for the AI's vision.
4)Drag off the execution line again and search for "Set Peripheral Vision Angle".
5)Set the Peripheral Vision Angle value to the desired field of view for the AI's vision.
~~~
STEP 4: Implement perception for the AI:
1)Drag off the execution line in the Begin Play event and search for "Create and Configure AI Perception Component".
2)Connect the output of the AI Perception Component node to the AI Controller's AI Perception property.
3)In the AI Perception Component node, configure the settings for sight and sight sense.
4)Drag off the AI Perception Component node and search for "Update Perception".
5)Connect the output of the Update Perception node to the Event Tick event.
6)In the Update Perception node, select "Sight" as the stimulus to update.
7)Connect the output of the AI Perception Component to a "For Each Loop" node to iterate through all perceived stimuli.
~~~
STEP 5: Implement the chase behavior:
1)Inside the For Each Loop, check if the perceived stimulus is the player character.
2)If the stimulus is the player character, drag off the execution line and search for "Move To Actor".
3)Set the Move To Actor node's target to the player character.
4)Connect the output of the Move To Actor node to the AI Controller's Move To Location input.
5)STEP 6: Create blackboard keys for the AI
6)Open the AIController Blueprint.
7)In the Blueprint editor, locate the Event Begin Play event.
8)Drag off the execution line and search for "Create Blackboard".
9)Create a new blackboard object and assign it to the AIController's Blackboard property.
10)Drag off the execution line again and search for "Create Blackboard Key".
11)Create a new key for the blackboard, such as "PlayerLocation".
12)Connect the output of the Create Blackboard Key node to the AIController's Blackboard property
~~~
STEP 7: Update blackboard values:
1)In the AIController Blueprint, find the Event Tick event.
2)Drag off the execution line and search for "Get Player Character".
3)Drag off the player character reference and search for "Get Actor Location".
4)Connect the output of the Get Actor Location node to the AIController's Set Blackboard Value As Vector input.
5)Set the Blackboard Key to the "PlayerLocation" key you created earlier
~~~
STEP 8: Set up the Behavior Tree:
1)Create a Behavior Tree asset following the steps mentioned earlier.
2)Open the Behavior Tree asset in the Behavior Tree editor.
3)Drag and drop a "Blackboard Key Selector" node onto the graph.
4)Configure the Blackboard Key Selector node to use the "PlayerLocation" key
~~~
OUTPUT:
![X1](https://github.com/Sharmilasha/GAME_PROGRAMMING_EXP7/assets/94506182/cd66ac59-cb04-44cb-8a78-48824c93ead3)
![X2](https://github.com/Sharmilasha/GAME_PROGRAMMING_EXP7/assets/94506182/10fdf0f8-3df2-4575-8d24-39b1abee3e0d)
![X3](https://github.com/Sharmilasha/GAME_PROGRAMMING_EXP7/assets/94506182/9499a11e-782d-47e6-989e-ebea33ea388e)
![X4](https://github.com/Sharmilasha/GAME_PROGRAMMING_EXP7/assets/94506182/ca6ba4cf-3869-4dca-9d89-660a41fb6a33)
![X5](https://github.com/Sharmilasha/GAME_PROGRAMMING_EXP7/assets/94506182/4e4a77c6-c726-4d6c-8b41-7ff36c227b60)
![X6](https://github.com/Sharmilasha/GAME_PROGRAMMING_EXP7/assets/94506182/49e79757-b843-4e41-82ba-2b26203d8460)
![X7](https://github.com/Sharmilasha/GAME_PROGRAMMING_EXP7/assets/94506182/986b0ed3-25c6-4ba2-baea-bc2345bb5b0e)
![X8](https://github.com/Sharmilasha/GAME_PROGRAMMING_EXP7/assets/94506182/6adb5d9f-c152-4238-91dc-24a153949630)
![X10](https://github.com/Sharmilasha/GAME_PROGRAMMING_EXP7/assets/94506182/1fe36713-681b-40ab-accb-2f5b695f2d97)
![X11](https://github.com/Sharmilasha/GAME_PROGRAMMING_EXP7/assets/94506182/2ce966ed-1d08-4b8d-8196-999b5fffc4af)

RESULT:
Thus, the AI concept to the actor for chasing when AI sees the player.









