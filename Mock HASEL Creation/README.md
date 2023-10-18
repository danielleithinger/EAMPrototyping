# HASEL Actuator Fabrication Pipeline

## Step 1: Design a Shape in CAD software

1. I am using Fusion 360 for this tutorial, but any CAD software that exports .stl files will do. Start with a new document and create a sketch on the top plane.
     
    ![Fusion360 Screenshot 1](<Images/Fusion360 Screenshot 1.png>)

2. Make the path that you want the 3D printer to follow out of construction geometry.

    ![Fusion360 Screenshot 2](<Images/Fusion360 Screenshot 2.png>)

3. Use the offset tool twice with normal geometry to make the path have a total width equal to your 3D printing wall thickness. My wall thickness is set to 0.4 mm.
    - If you don't know what your wall thickness is, you can find it in your slicing software. In Cura it is labled as "Wall Thickness" in the print settings.
    - If you want to heat seal multiple times around your HASEL chamber, make the total width that multiple of your wall thickness. I am heat sealing twice around in this example.

    ![Fusion360 Screenshot 3](<Images/Fusion360 Screenshot 3.png>)

4. Use the line tool with normal geometry to close the gaps on any endpoints of the path. The final sketch should be pale blue inside the path.

    ![Fusion360 Screenshot 4](<Images/Fusion360 Screenshot 4.png>)

5. Finish the sketch and extrude it by a distance equivalent to your 3D printing layer height.
    - If you don't know what your layer height is, you can find it in your slicing software. In Cura it is labled as "Layer Height" in the print settings.

    ![Fusion360 Screenshot 5](<Images/Fusion360 Screenshot 5.png>)

4. Export your shape as an .stl file.
    
    ![Fusion360 Screenshot 6](<Images/Fusion360 Screenshot 6.png>)
        

 

## Step 2: Prepare your .stl file in Cura

1. Download the [Ultimaker Cura](https://ultimaker.com/software/ultimaker-cura/) application to your computer.

2. Make sure the build plate is empty, and set your printer to Creality Ender-3 Pro in the upper left by clicking "Add printer".

    ![Cura Screenshot 1](<Images/Cura Screenshot 1.png>)

2. Click on the print settings in the upper right. Set the "Printing Temperature" to 260 °C, and "Bed Plate Temperature" to 0 °C, and the "Initial Layer Speed" to 2 mm/s. You can use the search box to find these specific settings.
    - These values may need to be adjusted for different types and thicknesses of plastic, but 260 °C is the maximum printing temperature for the Ender-3 Pro.
    - I would also like to print with no fillament being extruded, but I have not figured out how to do that yet. The heat sealing does still work with filament being extruded.

    ![Cura Screenshot 2](<Images/Cura Screenshot 2.png>)
    ![Cura Screenshot 3](<Images/Cura Screenshot 3.png>)

3. Add your .stl file into Cura by either clicking the folder icon or dragging and dropping it in. Make sure it is aligned properly on the build plate, and then hit slice.

    
    ![Cura Screenshot 4](<Images/Cura Screenshot 4.png>)

4. Click on the Preview tab and check the path of the printer nozzle. It is preferrable to have any points where the nozzle overlaps previous regions, shown with white squares, not along the edges of what will become the pouch. Then save the file onto the Ender-3’s microSD card.
    - The start and stop points of any contour overlap. By default Cura aligns the start and stop points at the back of the print, so you can rotate your part to position these where you want.

    ![Cura Screenshot 5](<Images/Cura Screenshot 5.png>)

## Step 3: Set up 3D printer for Heat Sealing (PENDING IMAGES)

1. Adjust the bed height so that the nozzle contacts the teflon while heat sealing.
    1. Acquire a section of teflon and two layers of plastic that you will be using for heat sealing.

    2. Turn on the Ender-3 and go to the "Prepare" menu. Select "Auto Home" and then, within "Move Axis", use "Move X" and "Move Y" to position the extruder in the following steps. The move axis commands function by selecting a displacement such as "Move 10mm" and then turning the dial to move the extruder in those increments.

    3. Near each corner of the print bed, position the stack of teflon with two plastic layers underneath below the nozzle. Turn the bed height adjusting knob at that corner until the nozzle contacts the teflon. Adjust until the teflon can be slid back and forth under the nozzle with a small amount amount of friction. Make sure that the bed is not being pushed downwards and that the nozzle assembly is not being deflected upwards.

2. I also flipped the bed upside down to get a smoother surface to heat seal on. I am unsure if this is necessary.

## Step 4: Perform the Heat Sealing (PENDING UPDATED IMAGES)

1. Cut a piece of teflon to the size of the print bed. A printer bed can be used as a template to get the correct size.

    ![Alt text](Images/IMG_0492.png)

    ![Alt text](Images/IMG_0493.png)

2. Cut a 9.5 inch strip of plastic, equivalent to the length of the print bed, off the end of the roll of plastic, and fold it in half to get a double layered sheet of plastic to heat seal. Make sure that the inside of the plastic is folded together so that the two heat sealable layers are contacting each other.
- The heat sealable plastic we are using is Tekra MYLAR® 850H 0.48 mil, with a width of 13 inches.

1. Tape the tape the double layer of plastic onto the print bed, leaving as few wrinkles and as little air between the two sheets as possible.

    ![Alt text](Images/IMG_8276.png)

1. Tape the teflon sheet to the print bed on top of the plastic.

    ![Alt text](Images/IMG_0494.png)

1. Turn on the printer and navigate to "Print from TF".

    ![Alt text](Images/IMG_0499.png)

1. Select your saved gcode file and wait for the heat sealing to complete.

    ![Alt text](Images/IMG_0500.png)

## Step 5: Filling The HASEL (TODO)
