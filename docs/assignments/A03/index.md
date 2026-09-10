# A3 – Parametric and FEA

## Objective
  The objective in this assignment is to design and create an aluminum bar with a circular cross-section to find the length and create a Finite Element Analysis of the bar.

## Analyze
  The bar we were tasked to create is one of a circular cross area, the assignment mentions thickness and it being hollow, however, those parts also mentioned it being a box beam so to incorporate that information into my assignment I decided to do a hollow beam with a circular cross-section. The given for this assignment is that one side is connected to a fixed support and the other has force P on its front face. We were to choose a force between 300 Lbf and 500 Lbf. The material was to be made out of aluminum with a Modulus of Elasticity between 8*10^6 and 11*10^6 psi and the bar had a maximum axial deflection of 0.009. For this, the dimensions that I chose were 1.0 in for outside diameter and 0.3 in thickness.
    <br>
The first thing we were tasked to do was to find the necessary length of the material with the given parameters. After solving symbolically and plugging in the numbers, I got a length of 148.55 in.
    <br>
    <img width="5000" height="1500" alt="Work" src="https://github.com/user-attachments/assets/a5066150-e447-4ca6-8efd-912f0aece6f6" />
    <br>

## CAD
  After doing things by hand I opened my CAD software and set my global parameters. I first set up “E”, “d1”, “delt”, “t”, and “P”. After this I solved for “d2” and “A” so I can plug into the equation to find the minimum length needed. The end result matched my hand calculations.
      <br>
    <img width="925" height="421" alt="Screenshot 2026-09-08 183656" src="https://github.com/user-attachments/assets/d1222eb7-5977-4cf9-86f6-f69bba10c59c" />
      <br>
      <br>
After setting my parameters, I went to model the bar first, I created a sketch in two circles, one inside and one outside. I define the circles to be “d1” and “d2” from the global parameters. After this, I extruded the faces to be the length of “L”.
      <br>
    <img width="700" height="500" alt="Screenshot 2026-09-08 183732" src="https://github.com/user-attachments/assets/8d53510c-7546-4e9e-be72-df43303ebd09" />
      <br>
      <br>



## Download
 <a href="2157_A3_SLDPT.zip.001" download>Download zip File A</a>
 <a href="2157_A3_SLDPT.zip.002" download>Download zip File B</a>
## Communicate

