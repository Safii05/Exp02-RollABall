# Exp02-RollABall
## Aim:
To develop a 3D application for Roll A Ball in unity.

## Procedure:
### Step1:
Create a new project.

### Step 2:
Click Heirarchy -> 3D object -> Select the plane -> 3DObject -> Sphere.

### Step 3:
Define the physics properties of the surface (Rigidbody).

### Step 4:
Assets -> Create -> # Script

### Step 5:
Create a folder name Coding and create a C# file to add the coding in it.

### Step 6:
To add our C# Script file to our selected object, click on the C# Script file and drag it to our selected objects in the Hierarchy window nad run the application.

### Step 7:
Stop.

## Program:
```
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class Move : MonoBehaviour
{
    public float xForce = 5.0f;
    public float zForce = 5.0f;
    public float yForce = 100.0f;
    // Start is called before the first frame update
    void Start()
    {
        
    }

    // Update is called once per frame
    void Update()
    {
        float x = 0.0f, y = 0.0f, z = 0.0f;
        if (Input.GetKey(KeyCode.A))
        {
           x = x - xForce; 
        }
        if (Input.GetKey(KeyCode.D))
        {
           x = x + xForce; 
        }
        if (Input.GetKey(KeyCode.W))
        {
           z = z + zForce; 
        }
        if (Input.GetKey(KeyCode.S))
        {
           z = z - zForce; 
        }
        if (Input.GetKeyDown(KeyCode.Space))
        {
           y = yForce;
        }
        

        GetComponent<Rigidbody>().AddForce(x,y,z);
    }
}

```
## output:
![Screenshot 2025-03-21 124003](https://github.com/user-attachments/assets/9e0a5b1c-ed54-4c28-b28f-a1b2182cd0c2)
![Screenshot 2025-03-21 124201](https://github.com/user-attachments/assets/6b4ce29a-aa31-41a9-958b-a6b82c09abc6)

## Result:
Thus, a 3D application for RollABall objects in unity is developed successfully.
