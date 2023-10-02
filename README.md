# RollaBall

## Aim:
To Roll a Ball using C# program in unity .

## Algorithm:
File -> Scene -> Select the scene -> Save as-> New folder(Scenes)-> File name (MiniGame)

Heirarchy -> 3D Object-> Plane [ Right side-> Inspector-> Change the name of plane (Name: Ground) Transform -> Reset Edit -> FrameSelected ]

Scale the ground by giving the scaling value as x=4 y=1 z=4

Heirarchy -> 3D Object-> Sphere [ Right side-> Inspector-> Change the name of plane (Name: Player) Transform -> Reset Edit -> FrameSelected Transform -> Position -> y=0.5]

Hierarchy -> DirectionalLight [ Inspector -> Change the color to white (255,255,255)]

Create a folder in project and name as Materials [Material folder -> Create -> Material (Name: Background) Inspector ->Surface Inputs ->BaseMAp (Choose the color) Metallic map-> 0 Smoothness -> 0.25 Drag the Background to the plane and release the mouse

Material folder -> Create -> Material (Name: Sphere) Inspector ->Surface Inputs ->BaseMAp (Choose the color) Metallic map-> 0 Smoothness -> 0.75 Drag the Sphere material to the ball and release the mouse

Hierarchy -> Player-> Inspector ->Add component-> Rigidbody

Create a new script -> Create a folder in project (Name: Scripts) Hierarchy -> Player -> Inspector-> AddComponent-> NewScripts-> PlayerController( Click create and Add) Copy the PlayerController and drag to Script folder Double click the PlayerController file and type the coding

## Program:
```python
Name: harithashree.v

reg no:212222230046

using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class balls : MonoBehaviour
{
    float XForce = 5.0f;
    float zForce = 20.0f;
    float yForce = 10.0f;
    void Start()
    {
        
    }

    // Update is called once per frame
    void Update()
    {
        float x = 0.0f, y = 0.0f, z = 0.0f;
        if(Input.GetKey(KeyCode.A))
        {
            x = x - XForce;
        }
        if (Input.GetKey(KeyCode.D))
        {
            x = x + XForce;
        }
        if (Input.GetKey(KeyCode.W))
        {
            z = z - zForce;
        }
        if (Input.GetKey(KeyCode.S))
        {
            z = z + zForce;
        }
        if (Input.GetKey(KeyCode.Space))
        {
            y = yForce;
        }
        GetComponent<Rigidbody>().AddForce(x, y, z);
    }
}
```
# Output:
![image](https://github.com/haritha-venkat/RollaBall/assets/121285701/862e8a56-1ab5-4691-8e97-d177738b339d)


# Result:
Thus, The 3D application for Roll the Ball objects in unity is developed successfully.


