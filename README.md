# WaveFunctionCollapse3D
 
This is a personal project about procedural generation using the Wave Function Collapse algorithm. Project also includes a script for detecting and labeling models with sockets for easier use.

## HOW TO USE ?

First be sure that your FBX file is in your Assets/Resources folder. Than in an empty scane attatch the "FindSockets.cs" script to an empty objects. Enter the FBX file name and all the seperate models will be listed in a JSON format and also script will create a Objects file inside the Resources folder. In the objects folder there will be seperate foldrs for all the different types of meshes. If you want to add a different variation for a module, add its mesh seperately to its corresponding folder.

If you wish to assign a different weight value to a certain module, be sure to add it as a gameobject with a MeshFilter component to the scane that your FindSocket folder is running and add a "PrototypePreferences.cs" script to it. With this script you can assign a weight value to the spesfic module. All the weights will be 1 by defult.

## GENERATİON PROCCESS 

After all the modules are created and the json is set you can add the Generator script to a new scane and generate your structure.

Generator script will have some values to be filled before generation.

- DimX, DimY, DimZ is the X, Y ,Z dimensions of the area you want to generate.
- Render Interval is the speed which the generation is shown (note that this feature can be changed so the script renders the objects at a different time. this is only added for the purpose of demonstration.)
- Empty Mesh is the name of the empty mesh that represents empty space.
- Underground Mesh is the name of the mesh that represents the underground parts.
- Initilize Choice is the ID of the module which your desire to be the endge of the map. ( Can be calculated by counting the order of the mesh in the FBX file, multiply it by 4 and decrement it by 1)

