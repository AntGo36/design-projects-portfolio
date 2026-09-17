# A4 – Motor Mount

## Objective
 The objective was to create a mount for a 
<a href="https://www.omc-stepperonline.com/brushed-24v-dc-gear-motor-3-6kg-cm-46rpm-w-99-5-1-planetary-gearbox-pa28-28245800-g100">brushed 24V DC gear motor.</a>
 The mount should be able to attach to the DC motor via 4 M3 screws, it should also be able to attach to a rigid wall using 4 M3 screws. The amount is to be made of ABS, PETG or PLA, For the purpose of this assignment, I chose PLA. 
 
## Analyze
  The given for this assignment were the force P = 300 N, S.F. of 3, max deflection of 0.3 mm, and the motor diagram. The primes I chose were a modulus of elasticity of 3600 MPa, yield stress of 60 MPa and base length of 32 mm which is equal to the length.
      <br>
    <img width="1625" height="505" alt="image" src="https://github.com/user-attachments/assets/65d2f6d7-1b14-4f29-b4d5-56a27c0e486f" />
      <br>

## Decide
  After analyzing the diagram, I knew the mentions needed for clearance of the motor, such as the motor shaft, screws, and the inset where the motor sits. I found the motor shaft to have a length of 18 mm where the tip is where P is acting.
    <br>
   <img width="4391" height="1039" alt="IMG_4151" src="https://github.com/user-attachments/assets/260dd59e-e1d6-48a0-85e7-571a7e3d7a51" />
    <br>
  I first solved it symbolically. I first solved for the max stress that would be used for the equations and laid the equations out to solve for h from the max stress and max deflection equations.
    <br>
   <img width="3568" height="761" alt="IMG_4151 2" src="https://github.com/user-attachments/assets/fe361c89-3d98-4467-80a1-140d07d389f2" />


### Figure 1
  For figure 1 I drew a plate and assigned the parameters to see what part needed to be solved. To solve for h I first needed to find the moment for the figure. The knowns for this figure were E, l, b, and delt, making the unknowns be M, the max stress, and “h”. The force P is on the motor shaft which was 18 mm, I found the moment to be 5400 N * mm. For the length ‘b” and “l” used the 22 mm diameter given in the diagram and added 5 inches on both sides making the total length being 32 mm for each.  After the safety factor was applied to the stress, I found the max stress to be 20 MPa. After solving for “h” I used the biggest value which was the “h” of the max displacement, which was 9.865 mm.
      <br>
     <img width="4480" height="956" alt="IMG_4151 3" src="https://github.com/user-attachments/assets/4ef75f1b-43e3-4515-b049-0a06f49e2ad8" />

  
### Figure 2
 Figure 2 used the same equations as figure one however Some value values were different such as M and L. For this figure I found “L2” to equal the “L” for the first figure plus “h” from the first figure. With knowing the value of our new L, I found the moments to be the force P times 18 plus the new L Which was 17,959.45 N * mm. After solving for “h” I found the “h” From the max stress to be 12.976 mm and from the max displacement to be 17.614 mm. I once again use the largest value for “h”.
      <br>
     <img width="4566" height="1144" alt="IMG_4151 4" src="https://github.com/user-attachments/assets/c4c9255d-b83c-424b-b66b-645c84d9e170" />

 
## CAD Model
   <img width="700" height="700" alt="IMG_4152" src="https://github.com/user-attachments/assets/5c7d3101-f923-4739-b220-bf4fe5e66326" />
    <br>
 For the CAD model I first set up the parameters. These parameters will help me assign the dimensions and solve for the unknowns through the software. I made sure to set up the extra ones needed later on such as the screw diameter and the diameter of the needed holes and insets for the motor.
    <br>
   <img width="617" height="463" alt="Screenshot 2026-09-16 193518" src="https://github.com/user-attachments/assets/b77e103c-704a-4ba4-84e8-a0e2b55c71c6" />
    <br>
  The first thing I did when sketching the CAD model was creating figure 1, to do this I created the circles which represent the holes needed for the motor. I first did the shaft hole, the inset hole and then the diameter circle which the screws are aligned on. After doing this I assigned the parameters to the circles. After doing this I created a circle 45° from the vertical on the outermost circle and created a pattern for four holes around that circle after which I defined. I created the square representing the base and length of the mount.
   <br>
  <img width="726" height="678" alt="Screenshot 2026-09-16 154901" src="https://github.com/user-attachments/assets/5eb5a2ed-b45e-4a67-a8cc-8a1d3aec180c" />
   <br>
 I've then extruded the figure to the height “h1” set in the parameters. After creating this extrusion, I made sure to extrude cut the inset to hold the motor. Making sure to keep the holes for the shaft and screws I moved onto the next figure.
   <br>
  <img width="702" height="537" alt="Screenshot 2026-09-16 152640" src="https://github.com/user-attachments/assets/e4995179-20de-4a7c-8964-1d47a1af2e7c" />
   <br>
 I wanted to create a new extrusion on the side of figure one so I created a sketch at that site. After I extruded the value for “h2” found in the parameter equations I continued creating sketches and extruding.
    <br>
   <img width="800" height="500" alt="Screenshot 2026-09-16 153655" src="https://github.com/user-attachments/assets/9dd80533-3a46-4311-8a8a-3106bc7eeff9" />
    <br>
 I then came to the main face for figure 2 where I created a similar circle, as in figure 1. I lay down one screw hole by placing one circle on the edge of the 22 mm circle. I then created a circular pattern, where they’re all being distributed with the diameter of M3.
    <br>
   <img width="300" height="400" alt="Screenshot 2026-09-16 154736" src="https://github.com/user-attachments/assets/5b7c809c-189e-4c85-8228-24a3edc0a8e7" />
    <br>
 I then end up with the completed mount. I made sure to check that all my dimensions were parameterized and correct as they matched all my calculations.
    <br>
   <img width="858" height="826" alt="Screenshot 2026-09-16 154936" src="https://github.com/user-attachments/assets/bf78562a-2e14-4778-833b-fece420a2022" />
   
## 2157
<h3>Multiview Drawing</h4>
 <ul>
   <li>Right</li>
   <li>Top</li>
   <li>Front</li>
   <li>Isometric</li>
 </ul>
   <img width="1310" height="883" alt="A4" src="https://github.com/user-attachments/assets/0488a3c0-2243-46f1-bc4f-1e2844b9c377" />
    <br>

## Files
<a href="A4.SLDPRT" download>Download CAD File</a>
<a href="A4_drawing.pdf" download>Download Drawing PDF</a>
<br>

## Communicate
 Overall, this assignment took a total of about 4 hours spread out. This is the first assignment within this class where I didn't have many major drawbacks and hangups. This is mostly due to me recognizing the limitations of my previous setup of Fusion 360 as there are many things like behind pay wall, so I got to familiarize myself with Solidworks after an amount of time without using it. When I first created the parameters of the base and length I made the error of mistaking the 22 mm to be the diameter of the motor. I also gained a better understanding of the CAD software as when I first used Solidworks I struggled with making extra extrusions off my object however, this was mainly due to a very non-standard setup I was using before.
<br><br><br>
