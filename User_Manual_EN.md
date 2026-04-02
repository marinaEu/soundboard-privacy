# Liutalab - User Manual

## Introduction

The app you are using is designed to correctly define the size, shape, and number of braces—the reinforcements glued under the guitar's soundboard—as well as the thickness of the soundboard itself, taking into account the woods used and any carbon fiber or other reinforcements.

In Liutalab, in addition to the section dedicated to designing the soundboard components, you will also find a section dedicated to instrumental verification of the soundboard before gluing it to the ribs. This check allows for final adjustments to the soundboard's structural braces.

In the following text, the term "guitar" will often be used to describe the instrument used in this application. Consider this simplification a way to identify all those stringed instruments that structurally resemble a guitar and that can fit within the design and verification parameters used in Liutalab—in other words, acoustic instruments with a flat soundboard and tensioned strings.

---

## Instrument Statics

Before describing in detail the various parts of the soundboard sizing and verification program, we'll review some issues related to the statics of the guitar instrument, in relation to the mechanical stresses that the strings impart to the instrument's structure, and in particular to the soundboard.

There are two main types of guitar: the metal-stringed acoustic guitar and the nylon-stringed classical guitar.

The two, in terms of mechanical stresses due to the different types of string materials and their thickness, are subjected to stresses of the order of 25-35 kgf for classical guitars and 40-80 kgf for acoustic guitars.

For ukuleles or other specific instruments other than classical or acoustic guitars, before proceeding with the soundboard sizing, it is necessary to determine (from the number of strings, the material and the length of the tuning fork) the stress load on the instrument's soundboard during the design phase.

From the perspective of designing based on the instrument's specific characteristics, it's essential to define reference numbers that can be used to determine the most appropriate dimensions for the soundboard-braces assembly.

As is well known, the mechanical resistance of any tensioned structure depends on the geometric characteristics of the cross-section subjected to stress and the mechanical characteristics of the materials from which the structure is composed (in addition to the type of tension, in our case static).

The guitar, in particular, must not collapse under the load of the strings, but at the same time, the mobile mass of the soundboard-braces assembly must be as low as possible, as the soundboard vibrates, and by vibrating, it produces sound. The lighter and more mobile it is, the louder and better it sounds.

The two quantities that define the structural properties of any mechanically stressed object are the modulus of elasticity "E" (or Young's modulus) and the moment of inertia "I".

These two quantities, which can be expressed through specific numbers and units of measurement, are combined through their product called "E*I" flexural rigidity, which is our most important reference when sizing the soundboard.

Regarding the various types of bracing for classical and acoustic guitars and the various soundboard support schemes (vented, X-bracing, falcate, lattice, double top, V bracing, etc.), beyond the color of the sound that each type of bracing imparts to the instrument and placing ourselves solely on the level of the correct sizing of the soundboard, there is a sizing criterion, the result of tests and comparisons by the leading experts in the sector, which emerges in particular that the statically best condition for the acoustics of the instrument is to have the bridge on the soundboard rotated forward by approximately 1.5-2° under the pulling action of the strings.

To achieve this, we found that the so-called flexural rigidity (E*I) of the soundboard should be approximately 15 for classical guitars and 50 for acoustic guitars, and in any case, have a value proportional to the structural load due to the strings depending on the instrument being built.

The purpose of Liutalab, the smartphone application you will use, is to correctly size the soundboard with regard to the flexural rigidity value.

---

## Using Liutalab

The program is structured into four submenus: Overall, Braces, Carbon Fiber, and Results.

The first three menus define the variables needed to calculate the E*I value.

In practice, based on the final flexural rigidity (E*I) we intend to achieve, we will adjust the various values for board thickness, number of braces, brace dimensions, materials, etc., to achieve the target value.

It is important to note that this tool, designed to assist the luthier, must be used wisely, ensuring that the data entered complies with good practice.

It is also important to pay attention to the units of measurement used, which can be set to meters, centimeters, millimeters, or inches.

To fully exploit Liutalab's potential and obtain reliable data regarding the soundboard measurements (based on the target E*I), we recommend following the instructions in the following pages of this manual, following the step-by-step description of the correct use of each menu item.

Good luck!

---

## Use of the manual

### SETTINGS

The menu can be found on every Liutalab page by clicking on the three dots at the top right.

* **Length units:** We recommend using millimeters as the main unit of length measurement to ensure greater precision after the decimal point.
* **Theme:** concerns the appearance of the graphics, light or dark.

![Settings Menu and Length Units](images/settings_menu.png)

---

### OVERALL

* **Board width:** width of the soundboard in mm measured 50mm above the bridge.
* **Board thickness:** thickness of the soundboard in mm with precision to the nearest tenth of a mm.
* **Board material:** When selecting the soundboard material, the program applies the elastic modulus shown in the table in parentheses. You can enter the elastic modulus value "by measure" after having measured it experimentally or obtained it from the wood certification.
* **Would you like to craft a double top with honeycomb?:** if you want to calculate this type of board, click on the "Yes" button; otherwise, leave the default "No".

This second part of the "overall" menu is activated by clicking "Yes" to the box "Would you like to craft Double Top with honeycomb?"

* **Honeycomb Thickness:** consider the thickness in mm with precision to the tenth of a mm of the honeycomb (typically made of aramid material) placed between the top board (specified in the "Board thickness" box) and the "Inner soundboard thickness" (specified below).
* **Inner soundboard thickness:** is the thickness of the board glued under the board and the honeycomb.
* **Board ratio:** This is the ratio between the width of the inner soundboard and the width of the guitar board. It's typically best to set this number less than 1, also to account for the reduction in the thickness of the honeycomb at the edges.
* **Inner soundboard material:** The wood used for the inner soundboard may be different from that used for the upper board. Choose the material used or enter the value measured "by measure."

![Overall Menu Screenshots](images/overall_menu.png)

---

### BRACES

* **Braces number:** This is the number of braces that serve a structural purpose. In the case of X-bracing, the value is 2; in vented classical guitar braces, it can be 5 or 7 depending on the construction choice; in V-types, the number is 2; in lattices, it depends on how many braces intersect the plane located 50mm above the bridge (typically 8), etc.
* **Average brace orientation:** This is the average angle of inclination of the braces with respect to the strings. For example, in X-bracing, the value will be around 35-45°, in vented braces it will be around 5-10°, etc.
* **Transverse brace shape:** The program supports two types of bracing shapes: trapezoidal and parabolic. In reality, the trapezoidal shape also covers rectangular or square shapes, as well as triangular ones, depending on the dimensions of the trapezoid's smaller base.
    * **Max base (B):** is the size of the base of the trapezoidal braces glued to the board.
    * **Min base (b):** This is the dimension of the smaller base of the trapezoid. If this value is "1" then we would have braces that are almost triangular in shape. If the value is equal to the Max base value then we will have a rectangular or square cross-section depending on the height of the trapezoid.
    * **Height (H):** height in mm of the trapezoidal braces.
* **Braces Material:** in Liutalab it is possible to define the material of the braces, which can be different from that of the soundboard, to give the luthier maximum design flexibility.

![Trapezoidal Brace Shape Diagram](images/braces_shape_diagram.png)
![Braces Menu Screenshots](images/braces_menu.png)

---

### CARBON FIBER

This menu allows you to manage the possible addition of carbon fiber reinforcements, or other materials stronger than the basic wood, to significantly increase the flexural rigidity without excessively weighing down the structure. These reinforcements are made from laminates (epoxy + fiber, for example) of calibrated thickness (not loose fibers) glued to the braces.

* **Brace reinforcement material:** you can choose the material from those present in the list or you can enter a value "by measure" based on the reinforcement material data found in the manufacturer's datasheet.
* **Reinforcement thickness on max base:** Enter the thickness of reinforcement applied between the soundboard and the bases of the braces (trapezoidal). Please note that this refers to a thickness applied to the base of all braces with a width equal to the base of the trapezoidal braces.
* **Reinforcement thickness on min base:** This is the thickness of reinforcement glued above the smaller base of the trapezoid, with a width equal to the width of the smaller base of the trapezoid. Note that gluing the thickness to the smaller base rather than the larger base is a much more effective way to increase the rigidity of the structure.
* **Reinforcement thickness on each slope side:** This is the reinforcement thickness applied to both edges of the trapezoidal braces. This means that the thickness value you enter is automatically calculated twice for all braces.

![Carbon Fiber Menu Screenshot](images/carbon_fiber_menu.png)

---

### RESULTS

* **Flexural rigidity:** These are the flexural rigidity results for the soundboard including braces and the double-top soundboard, respectively, if you have chosen to calculate it in the dedicated menu. The numbers you see are the result of the calculations obtained with the geometric and resistance (E) values entered. Depending on whether the E I value is higher or lower than what we consider correct, to get as close as possible, simply modify the numerical data entered (e.g., size and number of braces, board thickness, materials used, etc.). The flexural rigidity calculation is automatically updated when you return to the results menu.

**Deflection-based stiffness check:** This section is particularly useful for instrumentally verifying a soundboard equipped with braces, after calculating and sizing the board and braces. In practice, the soundboard is placed on two supports set at a certain distance ("L" span length), applying a preload and a load (load applied) at the center of the board, and measuring the deflection (measured deflection) under the load according to the diagram shown in the figure. The resulting number is the flexural stiffness value. If this number is higher than the target value, the cross-section of the structural braces will be reduced until the desired value is reached; if it is lower, additional reinforcements will need to be added to the soundboard.

* **Suggested flexural rigidity:** These are reference numbers that will be used depending on the instrument being designed. Please note that there is no specific correct stiffness number for every instrument, as this number may vary depending on the thickness of the strings used.

![Deflection Check Setup Diagram](images/deflection_check_diagram.png)
![Results Menu and Suggested Rigidity Table](images/results_menu.png)
![Suggested Rigidity Reference Values](images/suggested_rigidity_table.png)
