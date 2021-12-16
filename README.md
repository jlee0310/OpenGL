# OpenGL-C++
I created realistic, interactive, 3D objects by using of application programming interface (API) libraries and C++.  For this project I picked a tea box, Christmas glove, a Yeti cup, and a vitamin bottle on a black leather pad. The reason I chose these items is that it was easy to clearly demonstrate primitive shapes.  The tea box is cube, the Christmas glove is a sphere, the Yeti cup is a cylinder, and a vitamin bottle is a cylinder with the black leather pad as a plane. 

Here are the project requirements and how I approached to program these shapes. 
1.	Create low-polygon 3D representations of real-world objects.
Based on the objects that I choose, I used cylinder.cpp file and sphere.cpp file to draw objects.  

2.	Apply accurately projected textures to a 3D model. 
I tried to apply textures to 3D models that I created by using two shaders:
Multiple_lights and light_cube. For some reason if I apply the light source the texture function fails. 

3.	Apply lighting to create a polished visualization of 3D models. 
I used the multiple_lights shaders to create lights into the scene. Since the project required me to not causing parts of the objects to appear dark when moving the camera around them, I decided to use the directional light, 4 point lights and 1 spot light with green color. 

4.	Place objects appropriately, using the X, Y, and Z coordinates, relative to one another in the 3D world. 
I placed the objects to match the photograph I submitted as closely as possible by manipulating the glm::translate(model, glm::vec3(x, y, z)). 

5.	Apply horizontal, vertical, and depth camera navigation around the 3D scene. 
A user can navigate my world using WSAD and QE keys. WSAD key are programmed to control the forward, backward, left, and right motion. QE keys are programmed to control the upward and downward movement. I managed the glfwGetKey function to achieve this. 

6.	Apply nuanced camera controls to effectively view the 3D objects in the application. 
I embedded the camera speed at 2.5f for default value, mouse_callback function that allow the orientation of the camera to change the look up and down or right and left. I also utilized scroll_callback function that adjust the speed of the speed the camera travels around the scene. I programmed to output the current speed when user change the speed. 

7.	Create perspective and orthographic display of the 3D world. 
By using the P key, a user can change the viewport display of all objects in the scene between orthographic(2D) and perspective(3D) views at will. I made an if statement that uses a flag which is set to true/false when a user type P it changes the bool value.

Although I only implemented 5 objects, my code became surprisingly long and voluminous. This is where I realized the importance of modularizing and reusing code. My code has a lot of repetitive parts, so I wanted to apply a reusable function, but I didn’t want to mess with it because I failed to apply the texture. Except for reusable functions, code with similar functions was modularized to improve readability. I gained the knowledge of how computer graphic works and how C++ works with multiple files throughout this project that I can continue to apply in my future educational pathway. 
  


