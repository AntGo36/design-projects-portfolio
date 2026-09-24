# A5 – Bracket Design

## Objective

For this assignment we were tasked to create a bracket for a T beam to hold a 
  <a href="https://www.uline.com/Product/Detail/S-12925/Poly-Cord-Strapping/Heavy-Duty-Polyester-Cord-Strapping-3-4-x-2500?pricode=WA9239&gadtype=pla&id=S-12925">polyester strap.</a>
The Bracket should be able to hold the force F distributed on both sides of the strap mount. The bracket is to be made of Aluminum 6061 T6, Steel (ASTM A36), or Titanium (Ti-6Al-V4). For the purpose of this assignment I chose Ti-6A-V4. The safety factor is 4.

## Analyze

The bracket shape is already provided. It has three known dimensions “a”, “b”, & “c”.
<ul>
   <li>“a” = 0.498 in with a tolerance of -0.001</li>
   <li>“b” = 0.9992 in with a tolerance of -0.0005</li>
   <li>“c” = 1.499 in with a tolerance of -0.001</li>
 </ul>
 
  <img width="323" height="238" alt="image" src="https://github.com/user-attachments/assets/28f104fc-e429-487c-b76b-f583a1d889e2" />
    <br> 
As seen in the image, the dimensions form a “T” shape, one could also see how the strap is to be mounted. The strap has two forces “F” that act on a circular part, more context could be seen from the full bracket design.
      <br>
    <img width="382" height="345" alt="image" src="https://github.com/user-attachments/assets/c6397057-fffc-4f20-85d9-f33401369198" />
      <br>
As the image above shows, the bracket is broken up into five different parts, A, B, C,D, & E. We're instructed to analyze the dimensions of these parts first by using stress analysis and second by using stiffness analysis.



## Stress Analysis

I first started with part eight as that's where the straps distributed force is. I think the length by analyzing the product page for the strap seeing that it was 3/4 an inch I made the length 1 inch. I first created a diagram and solved it symbolically. After fully solving, I found r (radius) to be 0.2942 in.

   <img width="5767" height="2051" alt="IMG_4210" src="https://github.com/user-attachments/assets/a952fd34-374f-4c6a-97e1-1b1695b3346a" />

I next moved to part B where I used the previously found Radius to find the thickness of the part which was 0.03399 in.
  
  <img width="3657" height="1347" alt="IMG_4210 2" src="https://github.com/user-attachments/assets/25514372-ec29-4f0b-b98f-d88592f15f1d" />

Part C is a similar process to B, for the base (b) I chose to use the thickness of part B and the length of part A to find the height. h = 0.03868 in.

  <img width="3453" height="1118" alt="IMG_4211" src="https://github.com/user-attachments/assets/ef2829a4-d0cd-4b46-85bf-f8bac55c90be" />

Part D once again is the same process as seen to find the width its height was previously  defined in the first diagram shown, “c” = 1.499 in.  I found its width to be w = 0.01334 in.

   <img width="3513" height="1253" alt="IMG_4211 3" src="https://github.com/user-attachments/assets/f4e88bd9-3167-4147-8d02-bd75d5840acf" />

As seen in parts, E one of the dimensions was previously defined. “b” = 0.9992 in. I solved for its height, which was h = 0.0200 in

  <img width="3202" height="1053" alt="IMG_4211 2" src="https://github.com/user-attachments/assets/0c3d2693-cea7-4a10-b1ee-7d52e0196778" />


## Stiffness Analysis


The stiffness analysis uses the  max deflection of 0.005 in. Finding the dimensions for the parts act differently than with the stress analysis.

With part A you would use the distributed load formula for max deflection. With it being a cylinder, you will also use a different formula for I.

<img width="5306" height="1232" alt="IMG_4217" src="https://github.com/user-attachments/assets/82c738a3-c646-4a63-b40c-1dde3d70cb1f" />

Part B uses the standard deflection formula, I found length L to be four times the previously found radius. when using the standard formula you would use area to solve for “t” which was found to be t = 0.06316 in.

<img width="5469" height="1321" alt="IMG_4217 2" src="https://github.com/user-attachments/assets/995bb4ff-7771-42d2-b879-2f40f6b98f70" />

Because C uses all its dimensions in the formula I found left L to be (“a” + 2(“b”)), and the base to be the thickness previously found in part B plus the length of part A. Part three uses the distributed load formula and the stemmed formula for eye to find the height which is h_3 = 0.168103 in

<img width="5321" height="1230" alt="IMG_4217 3" src="https://github.com/user-attachments/assets/3a0ba082-da86-49e5-a0e9-679b6ee48027" />

Like part B Part D uses the standard formula while using the preset dimension “c” as its height. This time the dimension to be found is its width which ended up being w = 0.02486 in.

<img width="4657" height="1261" alt="IMG_4218" src="https://github.com/user-attachments/assets/56c9dafc-8c76-4384-b980-6753f9c36a4f" />

Following suit part E does the same, it has the dimension “b” for its width. Solving for its height, h = 0.03729 in.

<img width="4362" height="1269" alt="IMG_4218 2" src="https://github.com/user-attachments/assets/e29eabb8-2a1b-4e55-ae01-acea651e536c" />


## Multiview sketches

<img width="1323" height="731" alt="IMG_4224" src="https://github.com/user-attachments/assets/cb8e87e9-5c24-4b7d-86b4-6c5b73b54500" />

<img width="1323" height="731" alt="IMG_4226" src="https://github.com/user-attachments/assets/b0a37ab5-e8db-4695-88c1-59d5e29bb8e8" />


## 2157

The objective was to create a connector that would have two holes, one having a diameter of 1 inch with a slight interference connection and the other to fit on part A with a slide connection.
<img width="5391" height="2436" alt="IMG_4228" src="https://github.com/user-attachments/assets/ae430218-36e8-4383-8aa2-888780eed152" />

<br>
For hole A I chose RC2 because while it did match with RC1 I thought it to be better with a larger tolerance. For the 1 inch diameter hole I chose FN1.
<img width="3429" height="977" alt="IMG_4228 2" src="https://github.com/user-attachments/assets/4c81dcba-aca7-4f51-83a9-865cd3385999" />


## Communicate

Overall, this assignment was the second most difficult for me. This is due to time management and constant errors within my numbers, for example in parts C for the stiffness analyzation, I must stuck the length to be “a” However, it was meant to be “a” + 2*”b”. Another example is that I got the wrong significant figures for my modulus of elasticity in the early stages. Without these mistakes, this assignment would've taken around four hours; however, with the mistakes I had to rewrite a whole page and redo my calculations which added an additional hour.
<br><br>

