# A10 – Lead Screw Translating System

**Team Section Contributions:**
* **Calculations / Free Body Diagrams:** Brian Jones
* **Parametrically Model (CAD):** Antonio Goodson
* **FEA Analysis:** Jarek Hernandez Acaba

---

## Objective
Design and perform structural analysis for a mechanically driven lead-screw crosshead system for a tensile testing machine. The system must support a total tensile load of 2kN (2000N) evenly divided between two lead screws (1000N per screw), maintain a linear crosshead speed range of 1mm/min to 50mm/min, meet a structural Design Safety Factor (Nsf) of 4, and limit maximum crosshead deflection to 0.1mm.

---

## Section 1: Lead Screw Calculations & Selection - Brian Jones

### Task 1.1 — Minimum Lead Screw Diameter (d)
* **a. Knowns and Unknowns:**
  * **Knowns:**
    * Total tensile load (Ftotal): 2000N
    * Number of lead screws (n): 2
    * Load per lead screw (Fscrew): 1000N
    * Safety Factor (Nsf): 4
    * Material Yield Strength (Sy, AISI 1018 Steel): 300MPa (300106Pa)
  * **Unknowns:**
    * Allowable tensile stress (allow)
    * Minimum tensile stress area (Amin)
    * Minimum minor diameter (dmin)

* **b. Free Body Diagram (FBD):**
  ![Lead Screw Axial Tension FBD](https://github.com/user-attachments/assets/8d0d00af-2789-4b7b-85b8-dfc44eb85bd5)

* **c. Symbolic Solution:**


allow=SyNsf

$$\sigma = \frac{F_{screw}}{A} \le \sigma_{allow} \implies A_{min} = \frac{F_{screw}}{\sigma_{allow}} = \frac{N_{sf} \cdot F_{screw}}{S_y}$$

$$A_{min} = \frac{\pi d_{min}^2}{4} \implies d_{min} = \sqrt{\frac{4 \cdot N_{sf} \cdot F_{screw}}{\pi S_y}}$$

* **d. Numerical Solution:**


allow=300106Pa4=75106Pa=75MPa


dmin=4(4)1000N(300106N/m2)0.00412m=4.12mm(0.162in)

---

### Task 1.2 — Rotational Speed Range ( / RPM)
* **a. Knowns and Unknowns:**
  * **Knowns:**
    * Linear crosshead speed range (v): 1mm/min to 50mm/min
    * Selected screw lead (L): 2.54mm/rev (0.100in/rev, standard 1/2"-10 Acme screw)
  * **Unknowns:**
    * Minimum rotational speed (RPMmin)
    * Maximum rotational speed (RPMmax)

* **b. Free Body Diagram (FBD):**
    ![Rotational Speed to Velocity Diagram](https://github.com/user-attachments/assets/a7acc801-67f2-4e0e-a50e-7812e7562daa)


* **c. Symbolic Solution:**

$$v = RPM \cdot L \implies RPM = \frac{v}{L}$$


RPMmin=vminL,RPMmax=vmaxL

* **d. Numerical Solution:**


RPMmin=1mm/min2.54mm/rev0.394RPM


RPMmax=50mm/min2.54mm/rev19.69RPM

---

### Task 1.3 — Maximum Torque (Tmax)
* **a. Knowns and Unknowns:**
  * **Knowns:**
    * Axial load per screw (Fscrew): 1000N
    * Major diameter (d): 12.7mm (0.500in)
    * Mean diameter (dm): 11.43mm (0.01143m)
    * Lead (L): 2.54mm (0.00254m)
    * Thread angle (, Acme 29): $14.5^\circ \implies \sec\alpha = 1.033$
    * Coefficient of friction (, steel on bronze): 0.15
  * **Unknowns:**
    * Required driving torque per screw (Tscrew)

* **b. Free Body Diagram (FBD):**
  ![Lead Screw Thread Friction and Torque FBD](fbd_leadscrew_torque.JPG)

* **c. Symbolic Solution:**


Tscrew=Fscrewdm2L+dmdm-L

* **d. Numerical Solution:**

$$T_{screw} = \frac{1000 \cdot 0.01143}{2} \left[ \frac{0.00254 + \pi (0.15)(0.01143)(1.033)}{\pi (0.01143) - (0.15)(0.00254)(1.033)} \right] \approx 1.305\text{ N}\cdot\text{m} \quad (11.55\text{ in-lbf})$$

---

### Task 1.4 — Lead Screw Selection
* **Selected Component:** Standard 1/2"-10 Single-Start Acme Lead Screw (18-inch length minimum).
* **Specifications:** Major Diameter =0.500in, Lead =0.100in/rev, Pitch =0.100in.

---

## Section 2: Nut & Flange Thread Bearing Analysis

* **a. Knowns and Unknowns:**
  * **Knowns:**
    * Axial load per nut (Fscrew): 1000N
    * Major thread diameter (d): 12.7mm
    * Minor thread diameter (dr): 9.75mm
    * Pitch (p): 2.54mm
    * Engaged threads (nt): 6
    * Bronze Yield Strength (Sy): 120MPa
    * Allowable bearing stress (b,allow): 120MPa4=30MPa
  * **Unknowns:**
    * Total bearing area (Ab)
    * Actual thread bearing stress (b)

* **b. Free Body Diagram (FBD):**
  ![Nut Thread Bearing Stress FBD](images/fbd_nut_bearing.png)

* **c. Symbolic Solution:**


Ab=4(d2-dr2)nt


b=FscrewAb=4Fscrewnt(d2-dr2)b,allow

* **d. Numerical Solution:**


Ab=4(0.0127)2-(0.00975)263.1210-4m2


b=1000N3.1210-4m23.20MPa

* **Conclusion:** Since b=3.20MPa30MPa, thread bearing strength is verified with Nsf>4.

---

## Section 3: Crosshead Structural Design & Analysis

### Task 3.2 — Beam Stress & Strength Analysis
* **a. Knowns and Unknowns:**
  * **Knowns:**
    * Total force (Ftotal): 2000N
    * Beam span (Lb): 200mm=0.20m
    * Material (Aluminum 6061-T6): Sy=276MPa, E=68.9GPa
    * Allowable stress (allow): 2764=69MPa
    * Crosshead width (b): 40mm=0.040m
  * **Unknowns:**
    * Maximum bending moment (Mmax)
    * Minimum required height for strength (hmin,strength)

* **b. Free Body Diagram (FBD):**
  ![Crosshead Beam Bending FBD and Shear Moment Diagram](images/fbd_crosshead_beam.png)

* **c. Symbolic Solution:**


Mmax=FtotalLb4

$$\sigma_{max} = \frac{M_{max} \cdot c}{I} = \frac{6 M_{max}}{b h^2} \le \sigma_{allow} \implies h_{min, strength} = \sqrt{\frac{6 M_{max}}{b \cdot \sigma_{allow}}}$$

* **d. Numerical Solution:**

$$M_{max} = \frac{2000\text{ N} \cdot 0.20\text{ m}}{4} = 100\text{ N}\cdot\text{m}$$


hmin,strength=61000.040(69106)0.0147m=14.7mm

---

### Task 3.3 — Beam Deflection Analysis
* **a. Knowns and Unknowns:**
  * **Knowns:**
    * Total force (Ftotal): 2000N, Span (Lb): 0.20m
    * Modulus of Elasticity (E): 68.9GPa
    * Maximum allowable deflection (max): 0.1mm=1.010-4m
    * Width (b): 40mm=0.040m
  * **Unknowns:**
    * Required moment of inertia (Ireq)
    * Minimum required height for stiffness (hmin,stiffness)

* **b. Free Body Diagram (FBD):**
  ![Crosshead Beam Deflection FBD](images/fbd_crosshead_deflection.png)

* **c. Symbolic Solution:**

$$\delta_{max} = \frac{F_{total} \cdot L_b^3}{48 E I} \le 0.1\text{ mm} \implies I_{req} = \frac{F_{total} \cdot L_b^3}{48 E \cdot \delta_{max}}$$

$$I = \frac{b h^3}{12} \implies h_{min, stiffness} = \sqrt[3]{\frac{12 \cdot I_{req}}{b}}$$

* **d. Numerical Solution:**


Ireq=2000(0.20)348(68.9109)(1.010-4)4.83810-8m4


hmin,stiffness=312(4.83810-8)0.0400.0244m=24.4mm

* **Final Selected Dimensions:** h=25mm (1.0in), b=40mm (1.57in). Deflection under 2kN is =0.093mm0.1mm.

---

### Task 3.4 — Multiview Paper Sketch of Crosshead - Antonio Goodson


---

## Section 4: Parametrically Model (CAD) - Antonio Goodson

Before I begin modeling, the most important thing is to gather the necessary components as knowing them and having their dimensions were greatly help everything work together. <br>

<table>
  <thead>
    <tr>
      <th>Item Number</th>
      <th>Quantity</th>
      <th>Name</th>
      <th>Cost Per 3</th>
      <th>Cost</th>
      <th>Link</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>2</td>
      <td>1/2"-10 Lead Screw</td>
      <td>$9.90</td>
      <td>$19.80</td>
      <td>www.mcmaster.com/98935A823</td>
    </tr>
    <tr>
      <td>2</td>
      <td>2</td>
      <td>1/2"-10 Lead Screw</td>
      <td>$125.72 each</td>
      <td>$251.44</td>
      <td>www.mcmaster.com/95120A111/</td>
    </tr>
    <tr>
      <td>3</td>
      <td>1</td>
      <td>T-Slot Framing System</td>
      <td>$245.87</td>
      <td>$245.87</td>
      <td>www.grainger.com/product/80-20-T-Slot-Framing-System-Rectangle-804T48</td>
    </tr>
  </tbody>
</table>
  <br>
I first started with the initial sketch with two rectangles 14 the overall length and the second for the distance between features. I made two holes, one for the flange diameter, and the other for the hole needed to hold the flange as shown in the flange drawing.

<img width="1050" height="811" alt="Flange_Drawing" src="https://github.com/user-attachments/assets/e0ea8727-476a-4cf3-9faa-7f379edb883f" />

  <br>












<br>
---

## Section 5: FEA Analysis - Jarek Hernandez Acaba



