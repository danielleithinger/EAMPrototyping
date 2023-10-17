# HASEL Actuator Fabrication Pipeline

## Step 1: Design a Shape in CAD software

1. I am using Fusion 360 for this tutorial, but any CAD software that exports .stl files will do. Start with a new document and create a sketch on the top plane.
     
    ![Fusion360 Screenshot 1](<Images/Fusion360 Screenshot 1.png>)

2. Make the path that you want the 3D printer to follow out of construction geometry.

    ![Fusion360 Screenshot 2](<Images/Fusion360 Screenshot 2.png>)

3. Use the offset tool twice with normal geometry to make the path have a total width equal to your 3D printing wall thickness.
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

4. Click on the Preview tab and check the path of the printer nozzle. It is preferrable to have any points where the nozzle overlaps previous regions, shown with white squares, not along the edges of what will become the pouch. Then save the file onto the Ender 3’s microSD card.
    - The start and stop points of any contour overlap. By default Cura aligns the start and stop points at the back of the print, so you can rotate your part to position these where you want.

    ![Cura Screenshot 5](<Images/Cura Screenshot 5.png>)

## Step 3: Set up 3D printer for Heat Sealing (TODO)

1. Adjust bed height (number of steps)
- note that I flipped the bed

## Step 4: Perform the Heat Sealing (NEEDS UPDATING)

1. After you’ve selected a plastic type and size that is suitable and have cut two pieces of roughly equal size, tape one of the plastic pieces down to the printer bed

1. Tape the second piece of plastic down on top of the first, leaving as little air as possible between the two sheets

    ![Alt text](Images/IMG_8276.png)

1. Cut a piece of teflon using the nearby printer bed to get the correct size

    ![Alt text](Images/IMG_0492.png)

    ![Alt text](Images/IMG_0493.png)

1. Secure the teflon sheet to the actual printer bed using tape

    ![Alt text](Images/IMG_0494.png)

1. Turn on the printer and navigate to “Print from TF”

    ![Alt text](Images/IMG_0499.png)

1. Select your saved gcode file

    ![Alt text](Images/IMG_0500.png)

## Step 5: Filling The HASEL (TODO)
