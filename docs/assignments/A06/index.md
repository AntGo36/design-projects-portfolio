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


## Communicate

## Files

<a href="A6.SLDPRT" download>Download CAD File</a>

