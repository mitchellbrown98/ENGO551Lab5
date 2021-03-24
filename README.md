**Index.html:**

- This page contains a leaflet map with a light style stadia maps tilelayer, centered on Calgary, with 3 buttons. Only the 'Draw' button is enabled when you first load the page:

  ![](https://github.com/mitchellbrown98/ENGO551Lab5/blob/main/screenshots/2021-03-23_18h33_49.png)

- When you hover your mouse over the 'Draw' button, you will see instructions on how to draw a line on the map:

  ![](https://github.com/mitchellbrown98/ENGO551Lab5/blob/main/screenshots/2021-03-23_18h33_59.png) 

- After selecting 'Draw', you can click and hold, and move your mouse to draw the line on the map. When 'Draw' is pressed, the map dragging becomes disabled, and a  `mousedown` event listener is added. When the mouse is pressed down, a `mousemove` even listener is added. The mouse coordinates are added to an array each time the mouse moves, and those coordinates are added to the geojson linestring feature, which is updated each time the mouse moves, to display the line being drawn. To finish drawing, you can let go of the mouse click. 

  ![](https://github.com/mitchellbrown98/ENGO551Lab5/blob/main/screenshots/drawing.gif)

- After you have finished drawing the line, the 'Simplify Line' and 'Delete Line' buttons will become enabled. Pressing 'Delete Line' will remove the line from the map, and reset the layer and array so you can draw a new line. Pressing 'Simplify Line' will use the Turf.js Simplify function to straighten the line:

  ![](https://github.com/mitchellbrown98/ENGO551Lab5/blob/main/screenshots/simplify.gif)
  
- After the line has been simplified, the only button available is 'Delete Line'. Pressing this will remove the straightened line, and clear out the layers and coordinate array, so a new line can be drawn. The 'Draw' button will become enabled again once 'Delete Line' has been pressed:

  ![](https://github.com/mitchellbrown98/ENGO551Lab5/blob/main/screenshots/2021-03-23_18h35_57.png)
  
- Video Walkthrough: https://youtu.be/IzNvF5ORS_A

