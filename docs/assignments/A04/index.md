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
  
  <br>
  I first solved it symbolically. I first solved for the max stress that would be used for the equations and laid the equations out to solve for h from the max stress and max deflection equations

### Figure 1
  For figure 1 I drew a plate and assigned the parameters to see what part needed to be solved. To solve for h I first needed to find the moment for the figure. The knowns for this figure were E, l, b, and delt, making the unknowns be M, the max stress, and “h”. The force P is on the motor shaft which was 18 mm, I found the moment to be 5400 N * mm. For the length ‘b” and “l” used the 22 mm diameter given in the diagram and added 5 inches on both sides making the total length being 32 mm for each.  After the safety factor was applied to the stress, I found the max stress to be 20 MPa. After solving for “h” I used the biggest value which was the “h” of the max displacement, which was 9.865 mm.
      <br>
  
 ### Figure 2
Figure 2 used the same equations as figure one however Some value values were different such as M and L. For this figure I found “L2” to equal the “L” for the first figure plus “h” from the first figure. With knowing the value of our new L, I found the moments to be the force P times 18 plus the new L Which was 17,959.45 N * mm. After solving for “h” I found the “h” From the max stress to be 12.976 mm and from the max displacement to be 17.614 mm. I once again use the largest value for “h”.
      <br>
 
### CAD Model




## Communicate

