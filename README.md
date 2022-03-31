# ReviTab
WIP toolbar for Revit. 

![image](https://user-images.githubusercontent.com/27025848/160990246-d376e8cd-b8a3-4b4b-b5c7-de72a09704a3.png)

## DOCUMENTATION
![image](https://user-images.githubusercontent.com/27025848/160990371-f87d7a4a-1ff2-45b7-9494-cc4150e89d4c.png)

![image](https://user-images.githubusercontent.com/27025848/160990610-2ce33976-22ff-424e-9a5e-ac59f5f10a22.png)

![image](https://user-images.githubusercontent.com/27025848/160991215-4b6a412d-351d-43d1-8e04-91f47bbff651.png)

## TOOLS

![image](https://user-images.githubusercontent.com/27025848/160991351-4eb6b5ba-05b1-4e7d-a668-f3c0080e7374.png)

![image](https://user-images.githubusercontent.com/27025848/160991591-3fed961c-4991-4388-914d-1e98174b55ac.png)

![image](https://user-images.githubusercontent.com/27025848/160991727-dc0fd5bb-4647-4040-aaaa-283b4f6ba4f7.png)

![image](https://user-images.githubusercontent.com/27025848/160991938-ef3b65a7-5064-478a-a96a-494f07f9f5d1.png)

# STRUCTURAL FRAMINGS

## Place Void By Face
Add one ore more voids to a beam face providing the distance(s) from the beam start, mid or end point and its size.

[![Watch the video](https://img.youtube.com/vi/fi9HgS9kjw4/maxresdefault.jpg)](https://drive.google.com/open?id=1bFOfLDT6K9uV7vxEvi5O8D7sZDU91_z4)
<iframe src="https://drive.google.com/file/d/1bFOfLDT6K9uV7vxEvi5O8D7sZDU91_z4/preview" width="640" height="480"></iframe>

## Void By Line
Place a void by face at the intersection between a 2d line (on plan) and a beam. The opening will acquire distance and size from the line style name.

[![Watch the video](https://img.youtube.com/vi/jvsqUJG3uHA/maxresdefault.jpg)](https://youtu.be/jvsqUJG3uHA)

## Place Tags
Modeless window that calculates the distance from the origin to the beam centerpoint and saves it as Mark. The user can accept or refuse the changes.

## Move beam end
Move a beam or multiple beams end point to another element location curve closest point.

## Change Beam Location
![alt text](images/ChangeBeamLocation.gif)

## Edit Beam End Join
![alt text](images/EditBeamJoins.gif)

# WALLS

## Split Wall by Levels
Copy a wall in place and set its Top and Base constraints to the level it intersects. 
Note: 
1. The wall should not have a top/bottom offset applied; 
2. The original wall will be deleted. 

[![Watch the video](https://img.youtube.com/vi/gcMeTedRd2o/maxresdefault.jpg)](https://youtu.be/gcMeTedRd2o)

# GEOMETRY

## Element to DirectShape
![alt text](images/Flatten.gif)

## Project Lines to Surface

## Draw Axis

# COMMAND LINE

Call methods directly:
keywords: 
* select
+ create
- delete

\> larger

< shorter

= equal

! not equal

examples:

\*Structural Framing -> select all structural framings in the active view.

\*Structural Framing+Length>10000 -> select all structural framings in the active view longer than 10m. 

\*Walls+Mark=aa -> select all walls with a Mark equal to 'aa'

sheets: all -> select all Sheets

sheets: A101 A103 A201 -> select Sheets by Sheet Number

tblocks: all -> select all Title Blocks

[![Watch the video](https://img.youtube.com/vi/axukGCgBRys/maxresdefault.jpg)](https://youtu.be/axukGCgBRys)

[![Watch the video](https://img.youtube.com/vi/56_nDryHPzA/maxresdefault.jpg)](https://youtu.be/56_nDryHPzA)

# ZERO STATE

## Push to DB
Export selected parameters to a [db](https://remotemysql.com)

![IMG](https://i.imgur.com/DLuhkuM.png)

Data can be then visualized with online dashboards like [grafana](https://giobel.grafana.net/d/TS8vWBriz/project-2?orgId=1) 

![IMG](https://i.imgur.com/QzCrmAW.png)

or [desktop](https://github.com/giobel/rvtDashboard) apps

![IMG](https://i.imgur.com/NFat1uW.png)

## Background Print
Open a model in background and print its drawings. The printer setting should be already defined in the Revit model. The default printer should be Bluebeam.
[![Watch the video](https://img.youtube.com/vi/dBtYdCITQhw/maxresdefault.jpg)](https://youtu.be/dBtYdCITQhw)

## Purge Families
Purge families and leave only a type called Default. Requires the Purge Unused that can be found in the Revit Purge Unused branch. Credits: Matt Taylor https://gitlab.com/MattTaylor/RevitPurgeUnused/blob/master/PurgeTool.vb

## Installation
Extract the content of the release zip file in %AppData%\Autodesk\Revit\AddIns\20xx
