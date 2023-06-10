
# <p align="center">Roll a Ball</p>

## Aim:
To Roll a Ball using C# program in unity .
## Algorithm:
### Step 1:
* File -> Scene -> Select the scene -> Save as-> New folder(Scenes)-> File name (MiniGame)
### Step 1:
* Heirarchy -> 3D Object-> Plane 
* [ Right side-> Inspector-> Change the name of plane (Name: Ground)
* Transform -> Reset
* Edit -> FrameSelected ]

### Step 3:
* Scale the ground by giving the scaling value as x=4 y=1 z=4

### Step 4:
* Heirarchy -> 3D Object-> Sphere
* [ Right side-> Inspector-> Change the name of plane (Name: Player)
* Transform -> Reset
* Edit -> FrameSelected 
* Transform -> Position -> y=0.5]

### Step 5:
* Hierarchy -> DirectionalLight
* [ Inspector -> Change the color to white (255,255,255)]

### Step 6:
* Create a folder in project and name as Materials
* Background
  * [Material folder -> Create -> Material (Name: Background)
  * Inspector ->Surface Inputs ->BaseMAp (Choose the color)
  * Metallic map-> 0, Smoothness -> 0.25
  * Drag the Background to the plane and release the mouse
* Sphere
  * Material folder -> Create -> Material (Name: Sphere)
  * Inspector ->Surface Inputs ->BaseMAp (Choose the color)
  * Metallic map-> 0 , Smoothness -> 0.75
  * Drag the Sphere material to the ball and release the mouse

### Step 7:
* Hierarchy -> Player-> Inspector ->Add component-> Rigidbody

### Step 8:
* Create a new script -> Create a folder in project (Name: Scripts)
* Hierarchy -> Player -> Inspector-> AddComponent-> NewScripts-> PlayerController( Click create and Add)
* Copy the PlayerController and drag to Script folder
* Double click the PlayerController file and type the coding
## Program:
Developed By: **Shafeeq Ahamed.S**
</br>

Register No: **212221230092**
```
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class script : MonoBehaviour
{
    public float Xforce = 2.0f, Yforce = 2.0f, Zforce = 2.0f;
    // Start is called before the first frame update
    void Start()
    {

    }

    // Update is called once per frame
    void Update()
    {
        float x = 0.0f, y = 0.0f, z = 0.0f;
        if (Input.GetKey(KeyCode.LeftArrow))
        {
            x = x - Xforce;
        }
        if (Input.GetKey(KeyCode.UpArrow))
        {
            z = z + Zforce;
        }
        if (Input.GetKey(KeyCode.RightArrow))
        {
            x = x + Xforce;
        }
        if (Input.GetKey(KeyCode.DownArrow))
        {
            z = z - Zforce;
        }
        if (Input.GetKeyDown(KeyCode.UpArrow))
        {
            y = Yforce;
        }
        GetComponent<Rigidbody>().AddForce(x, y, z);
    }
}

```
## Output:
![image](https://github.com/ShafeeqAhamedS/RollaBall/assets/93427246/e30a0bb8-2e1a-46ba-8493-c50015243f81)

## Result:
Thus, The 3D application for Roll the Ball objects in unity is developed successfully.
