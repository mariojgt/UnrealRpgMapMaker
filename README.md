![image info](https://raw.githubusercontent.com/mariojgt/UnrealRpgMapMaker/main/Art/logo.png)
# Unreal Engine Map Maker
This Project is desing to work with any project all the file you need to work is inside the folder MapSystem, there is a demo scene but if you follow the documeation is realy easy to integrate, i recoment watch the video more features in the way, update

# Tutorial [link](https://youtu.be/oxPc2iR6JJw)

### 1 Capture you scene and create a map
In Order to proper test you scene you need to create a visual representation of you level but fortunaly we have a component call **BP_MapWorldCapture** the location is inside **Actors/BP_MapWorldCapture**, to proper use this actor you need to create 2 **target points** in you scene the first one you name **LowerRightCorner** and the second one you name **UpperLeftCorner** note tha the name is not import we just using for organization, you need to place those component in a way they to a zipp line so we can create a square map of you scene, now you need to add another actor call **BP_MapBoundaries** locate at **Actors/MapBoundaries/BP_MapBoundaries** on you add this actor you need to add the **target points** references that actor will set at the center of the square buy default once you done that you can add your **BP_MapWorldCapture** actor and follow the step 2.


### 2 Create the texture of you scene
In the actor **BP_MapWorldCapture** is only required to add the reference of the **BP_MapBoundaries** you can controll the z postion of the actor but now the x or y now in your **BP_MapWorldCapture**  you need to select the **SceneCapture in game** and generate a texture

### 3 Map settings
on the folder **MapSettings** in the **DT_MapSettings** you can setup your paraments such as the texture of map you have created more information check the tooltip in the varaibles, one more important thing in the **BP_MapBoundaries** you need to set up the varaibles **Map Datable Row Id** to the row id settings you want so in this way tou can have multiple maps

### 4 Actor setup
You need to add the **BPC_WorldMap** to actor that are based in character ther is some methods that is required to start this actor in order to work right, the event **StartMap** will trigger all the the fuction and method needed to start the map fuctions and **ToogleMap**  this event will show and hide the map this method will get the owner actor cast to character and get the player controller and open the map



Features:

1. Fully rpg map
2. Display actors position on the map
3. display markers ,fast travel and fog of war points on the map
4. radar system simular to god of war
5. map regions (still working in progress) you have have multiple map boundaries and the player touch those areas will update the map

Planed features

1. Saving and loading system for the marker, player markers and possible the player position
2. Radar settings refactor, i need to update the radar config settings varaible


