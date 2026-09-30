# A6 – Bracket Drawing

## Objective

The objective is to create a parametrically CAD file and drawing of the T beam bracket where the dimensions were previously found in A5. The drawing of the file is to be in ASME and have the listed tolerances.

## Design

When designing the bracket I first needed to define all the parameters and equations. <br>
When doing this I realized I would have to adjust the significant figures from 10 thou to a tenth of a thou (0.01 –> 0.0001). Doing this helped parameters display a value rather than 0, (ex. 0.00 >> 0.0020). 
  <br>
  <img width="550" height="675" alt="Screenshot 2026-09-29 112828" src="https://github.com/user-attachments/assets/6039675a-2f5b-4cbf-aed8-481fb5d78296"  style="width: 40%; height: auto;"/>
  <br>
I started designing in the same order I did the calculations with a part A. A was the only feature I used the calculated stress value rather than the stiffness value due to it being the larger value. When designing I started with the circle sketch and assigned the “r1” parameter.
  <br>
  <img width="912" height="785" alt="Screenshot 2026-09-29 105739" src="https://github.com/user-attachments/assets/2014f000-15ba-4b8d-b578-8bfcbdfa2ead" style="width: 40%; height: auto;"/>
  <br>
After that first step I then extruded it to the length of “L1”  and created a sketch on the back for feature B.
  <br>
  <img width="756" height="487" alt="Screenshot 2026-09-29 105911" src="https://github.com/user-attachments/assets/7caf1f87-b17d-4087-bc27-a1f10a986047" style="width: 40%; height: auto;"/>
  <img width="533" height="792" alt="Screenshot 2026-09-29 105954" src="https://github.com/user-attachments/assets/b543a038-f70c-4cd7-8cf8-e6a45e58eaa7" style="width: 20%; height: auto;"/>
  <br>
Now that the B sketch is created I extrude the thickness of “t2” and prepare the sketch for the height of part C. For the sketch I aligned the new sketch with B by creating center lines for the existing part and the sketch and making them coincident while making the bottom of the sketch collinear.
  <br>
  <img width="810" height="793" alt="Screenshot 2026-09-29 110101" src="https://github.com/user-attachments/assets/e81dd964-eaaa-4033-a435-4daf3f7e0d17" style="width: 40%; height: auto;"/>
  <img width="1015" height="585" alt="Screenshot 2026-09-29 112305" src="https://github.com/user-attachments/assets/6ec62e90-1e25-4a23-a909-01a2566bf812" style="width: 40%; height: auto;"/>
  <br>
The process is largely the same going forward with extruding C and preparing for part D by making a sketch on the side of C.
  <br>
  <img width="798" height="808" alt="Screenshot 2026-09-30 104623" src="https://github.com/user-attachments/assets/fd469437-414c-4038-8ecc-8680b60e4714" style="width: 40%; height: auto;"/>
  <br>
After extruding up to D, then create a sketch and extrude the D feature. Repeat these steps for feature E
  <br>
  <img width="687" height="306" alt="Screenshot 2026-09-30 104527" src="https://github.com/user-attachments/assets/321091e1-b9c9-4acf-a9ce-e4c97e8d7bf9" style="width: 40%; height: auto;"/>
  <img width="885" height="583" alt="Screenshot 2026-09-30 104503" src="https://github.com/user-attachments/assets/6b983bc9-79a6-49d1-821c-b174883185db" style="width: 40%; height: auto;"/>
  <br>
One would see that the bracket was made asymmetrical, instead of repeating the above steps it’s good to make use of the mirror feature. To mirror it I selected all my asymmetrical extrusions and mirrored them about the vertical plane.
  <br>
  <img width="662" height="742" alt="Screenshot 2026-09-29 112701" src="https://github.com/user-attachments/assets/a1a164d7-14da-437d-bd1b-5600a24a013e" style="width: 40%; height: auto;"/>
  <img width="603" height="690" alt="Screenshot 2026-09-29 112732" src="https://github.com/user-attachments/assets/94ae5ce0-2d92-4568-b6f9-b3d4e84bddd7" style="width: 40%; height: auto;"/>


## Drawing

<img width="1310" height="883" alt="A6" src="https://github.com/user-attachments/assets/d946edc0-c4a6-4f72-95db-62c44e113fc7" style="width: 90%; height: auto;"/>

## 2157

<h4>Design</h4>

When creating the parameters for the link I found an error in my calculations that changes a number of things. The error was using the diameter of 1 in as the radius, this caused my outside diameter and length to be larger than intended and with that it made the width / thickness shallower than needed.
  <br>
  <img width="588" height="460" alt="Screenshot 2026-09-30 184844" src="https://github.com/user-attachments/assets/e155a441-9f08-4bfd-a03d-5bbd62977d1a" style="width: 40%; height: auto;"/>
  <br>
With the fixed values I found the minimum width to be the one found with stiffness, w = 0.0895 in. 
  <br>
  <img width="677" height="677" alt="Screenshot 2026-09-30 185012" src="https://github.com/user-attachments/assets/22526c96-90d8-4126-8d45-7208a10df7da" style="width: 45%; height: auto;"/>
  <img width="452" height="713" alt="Screenshot 2026-09-30 182302" src="https://github.com/user-attachments/assets/30ae003f-4cc0-439d-b642-967a62f52da2"  style="width: 30%; height: auto;"/>

<h4>Drawing</h4>

<img width="1310" height="883" alt="2157link" src="https://github.com/user-attachments/assets/d4ed7e05-b690-4153-96c5-700cb10a7faa" style="width: 90%; height: auto;"/>

## Communicate

This assignment held to be the most straightforward so far this is due to already having the calculations mostly finished and having already done CAD modeling and parametrics. This assignment helped me work on time management as the other previous assignments took longer than  the time I set aside for it so instead of climbing, all the documentation in one setting I was able to space things out better. I also found that I needed to examine my work more thoroughly as I found that I labeled diameter as radius, which threw off my calculations for the linkage, though this was fixed during modeling. With the holes from the linkage I referenced the tolerances from the book. One thing I wish to improve is to be more detailed or refined when making drawings as I was unable to create the angle projection symbols on this assignment.


## Files

<a href="A6.SLDPRT" download>Bracket CAD File</a>  <br>
<a href="A6.pdf" download>Bracket PDF</a>
<br>
<a href="2157Link.SLDPRT" download>Link CAD File</a>  <br>
<a href="2157Link.pdf" download>Link PDF</a>
<br><br>

