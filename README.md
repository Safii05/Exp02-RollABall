# Exp02-RollABall

## Aim :

To develop a 3D application for RollABall in unity.

## Step1 :

Create a new project.

## Step 2 :

Click Heirarchy -> 3D object -> Select the plane -> 3DObject -> Sphere.

## Step 3 :

Define the physics properties of the surface (Rigidbody).

## Step 4 :

Assets -> Create -> # Script

## Step 5 :

Create a folder name Coding and create a C# file to add the coding in it.

## Step 6 :

To add our C# Script file to our selected object, click on the C# Script file and drag it to our selected objects in the Hierarchy window nad run the application.

## Step 7 :

Stop.

## Program:


using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class RollAball : MonoBehaviour
{
    // Start is called before the first frame update
    public float xforce = 5.0f, yforce = 200.0f, zforce = 5.0f;
    void Start()
    {


    }

    // Update is called once per frame
    void Update()
    {
        float x = 0.0f, y = 0.0f, z = 0.0f;
        if (Input.GetKey(KeyCode.A))
        {
            x = x - xforce;
        }
        if (Input.GetKey(KeyCode.D))
        {
            x = x + xforce;
        }
        if (Input.GetKey(KeyCode.W))
        {
            z = z + zforce;
        }
        if (Input.GetKey(KeyCode.S))
        {
            z = z - zforce;
        }
        if (Input.GetKeyDown(KeyCode.Space))
        {
            y = yforce;
        }
        GetComponent<Rigidbody>().AddForce(x, y, z);

    }
}

## Output :

![Screenshot (4)](https://github.com/user-attachments/assets/db8c9794-444c-4e80-9b83-ea67bce08aa6)

## Result:

Thus a 3D application for RollABall objects in unity is developed successfully.
