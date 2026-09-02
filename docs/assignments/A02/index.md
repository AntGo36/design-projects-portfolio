# A2 – Truss Stress Analysis

## Objective
The objective of this assignment is to create a truss with given points, forces, and more physical properties.

## Analyze
<img width="320" height="218" alt="Figure1" src="https://github.com/user-attachments/assets/e6ce96a8-fe05-4209-af17-9f2c4065407a" />
<br>
The figure given consists of 4 points, A, B, C, & D. "A" is defined as a pin support, and "B" as a roller. There are two forces P which act on points C and D, up and down respectively. The points are separated horizontally by a distance "a", and points C & D are separated from A & B by a distance "b".
<br>
The instructions require all sides to have the same cross sectional area, this applies to the pins as well. The force P is defined as 20 KN (chosen from force between 20-30 KN) and distances are defined as 0.4m for "a" & 0.3m for "b". The material for the truss that was instructed to use was A500 Structural steel, however, Fusion360 (the software I'm using) doesn't have it, so I used A36 Steel as a replacement.
<br>



## Decide
<!--_Which geometry did you select, and why? This is your first open design choice in the course — defend it._-->

The first step was to create a sketch of the truss. I chose to use a trapezoid as the main shape, this is because it is the best shape to connect all the points. I included webbing to provide more support by adding two more joints "E" & "F", I later changed this after finding the forces within the joints.
<br>
<img width="5570" height="1188" alt="HW2Img1" src="https://github.com/user-attachments/assets/b28e6fa7-36ab-485c-852d-5fb526afa3f2" />
<br>

### Finding Internal Forces
After creating the sketch I used the joint method on all members. After doing this I could instantly one of the redundancies in my first design in point F. This is because I could see that the y component would be a zero force member, I then found that points E & F where not necessary for the given requirements. After making a free body diagram of all the joints I was able to find symmetry within the internal forces.
<br>
<img width="4920" height="1051" alt="HW2Img2" src="https://github.com/user-attachments/assets/3a1b730e-872a-4bce-b551-ad05905f9808" />
<br> 
After creating the free body diagrams I solve for all internal forces without using numerical values. This is where I noticed the webbing wasn't needed. For this section I used ratios to solve for the diagonal forces such as the value "d" standing for the hypotenuse  between the points "a" and "b". I was able to find whether my arrows are correct and adjusted appropriately. I was also able to find what best thing to solve for first was, I found it was F_AD.
<br>
<img width="4920" height="1264" alt="HW2Img3" src="https://github.com/user-attachments/assets/4c57d5eb-3224-42d5-9e05-a68117baf9b0" />
<br>
I then solved for all the forces numerically. I found the highest internal forces where 33.33 KN within BC and AD. I found the other forces between members to be 26.67 KN and the y component for both A & B to be 20 KN.
<br>
<img width="4920" height="1111" alt="HW2Img4" src="https://github.com/user-attachments/assets/e3c75265-5484-4d70-92ec-5c056d9c5088" />
<br>

### Find Cross-Sectional Area of Truss
Now that I have the internal forces I can determine the cross-sectional area. The area could be found by dividing the largest internal force by the yield strength of the truss material. The yield strength was found online from <a href="https://beamdimensions.com/materials/Steel/ASTM/ASTM_A36/">beamdimensions.com</a> for A36 Steel which was 250 MPa. I applied the given safety factor of "3.5" given to the stress and got a resulting area of 466.7 mm^2.
<br>
<img width="2019" height="462" alt="HW_Img5" src="https://github.com/user-attachments/assets/77e1fe05-225d-4527-8e6d-580430f42951" />
<br>
This is where I redrew the frame, this shouldn't pose any big changes. I found the weight of the truss frame by using the density provided by beamdimensions.com as 7850 Kg/m^3. I found the total length of material the truss uses by adding the lengths of each beam and multiplyed by the area to find the volume. After finding the volume I multiply with the Density to find the mass in kilograms and convert to newtons with a end weight of 93.4 newtons, this was before subtracting the holes needed for the pins.
<br>
<img width="2019" height="431" alt="HW_Img6" src="https://github.com/user-attachments/assets/59f73df9-8d09-47ab-a8b0-736e9affeefc" />
<br>

### Find Cross-Sectional Area of Pins
I now had to find the cross-sectional area for the pins. The pins where to be made of hardened tool steel with a yield shear strength of 170 ksi and density of 0.278 Lb/in^3. The first step I took was setting up the equations. Since 33.33 KN is the largest force on the pins I use that. The given was in imperial units so I had to convert. After converting and using the safety factor on the given yield shear strength I found the area to be 0.1763 in^2. After finding the area I needed to find the weight of the combined pins, but first I needed to know how long they needed to be. To find the length I found the square root of the area of the truss, this is if the truss was made of square beams. after finding the length I just needed to multiply by the pin area and by the density to get the weight of 1 pin, 0.04169 Lb, the weight of all four was 0.1667 Lb (0.7417 N).
<br>
<img width="1997" height="939" alt="HW_Img7" src="https://github.com/user-attachments/assets/59d6d0c6-5c03-40cc-8429-cf792b703ae1" />
<br>

### CAD 3D Model
When creating the CAD model I start with sketching the points and connect them with lines. After getting the general shape I define the lengths, for the top I make it 1.2 m, the bottom 400 mm, the diagonal 500 mm, and the height 300 mm. One thing I had to avoid was over defining the structure as it will cause errors.
<br>
<img width="1709" height="685" alt="Truss_Sketch" src="https://github.com/user-attachments/assets/c22dfcba-1b7f-4224-b846-cd4fff43a94d" />
<br>
My next step was creating the thickness. I went through a few iterations as how to thicken but I decided to surface extrude the square root of the truss area and apply a symmetrical thicken which was half the extrusion. Doing this ensured that the pin holes where in the correct distance apart.
<br>
<img width="1034" height="625" alt="Truss_Extrustion" src="https://github.com/user-attachments/assets/7cf86afc-7969-4778-a1b8-97dee896ddb9" />
<br>
After creating the thickness I created the holes. I realized that I didn't previously find the diameter but after a simple equation I found it to be 12.034 mm. Now that I knew the diameter I just needed to create a new sketch and overlay circles on the corners of the truss sketch. I then applied a extrusion subtract to make the holes. I then applied the A36 Steel material to the truss to find the properties that was very close to the weight that I found before.
<br>
<img width="1200" height="250" alt="HW_Img8" src="https://github.com/user-attachments/assets/042365d2-bca6-4d79-bc19-23100025eb43" />
<img width="300" height="100" alt="Truss_Hole" src="https://github.com/user-attachments/assets/48289367-d1f6-4058-bb07-a63ef1189b98" />
<img width="300" height="150" alt="Truss_Properties" src="https://github.com/user-attachments/assets/4bbdb075-c13b-47e6-9d2e-b4feec0887d3" />
<br>
Because I couldn't find something equivalent to the hardened tool steel presented I decided to create a duplicate of a existing steel material and edit the density to the given. Creating the pin was simple as I just created a sketch of a circle that matched the diameter and extruded it to the thickness of the truss. The weight closely matched the weight previously found. 
<br>
<img width="300" height="125" alt="Hardened_Tool_steel" src="https://github.com/user-attachments/assets/1628ea27-a63d-4ff9-9a15-c62f6ec67b23" />
<img width="300" height="200" alt="Pin_Properties" src="https://github.com/user-attachments/assets/fd058534-034b-4e43-a931-ff77b536cdfb" />
<br>

<!--<a href="models/part_v2_final.step" download="Truss_Assembly.step">Download Truss Assembly STEP File</a>-->


## Communicate
The CAD software I was most familiar with was Solidworks however I didn't have it at hand so I used Fusion 360 as it was free.
<br>
In the end this assignment took the span of 5 days and in total ~10 hours. I believe that I could have taken more time to complete because I feel I ran too close to the assignment date. I also feel that I should have spent more time on the CAD model. For planning I spent around a hour and a half in a small sketchbook, when I did this the original plan matched the final more closely when I officially started.

