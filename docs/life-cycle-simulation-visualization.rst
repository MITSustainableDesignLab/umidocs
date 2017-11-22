
Life Cycle - Simulation and Visualization
=========================================

Once all modeled buildings have templates assigned, Life Cycle simulation for Embodied Energy and Carbon are launched and visualized through the “Simulate” tab in the umi panel, which can be opened by clicking on the “Simulate” button of the umi toolbar, or the command “UmiOpenSimulatePanel”.

The umi panel will open with the “Simulate” tab open. In order to access the Life Cycle module controls you can click its logo in the side tabs:

1. Running a calculation
````````````````````````

The Life Cycle umi module offers two modes for running calculations: Either running all possible models in the Buildings layer or only running those specifically selected. You can run a calculation by clicking the “Run” button located in the first section of the panel. When no building objects are selected in the Rhino viewport the button will show the text “Run all” and will trigger the first mode. You can run only specific buildings by selecting them in Rhino. In that case the button will change its text into “Run selected” triggering the second mode. The progress bar in the panel will show the evolution of the calculation which will take from seconds in the case of 1 building to minutes in the case of more than 100.

2. Visualizing results
``````````````````````

Once one or more buildings have been calculated, umi allows for the visualization of results directly on the model by false coloring their volumes according to their performance, through second half of the “Simulate” panel. In visualization mode umi will duplicate brep geometry into the “Results” layer. Again, the module offers two modes of visualization (All buildings or selected buildings) controlled through the “False color” button in the second section of the panel. Note that in order for the visualization to work the “Buildings” layer will have to be active.

The type of results visualized can be modified through the controls in the umi panel, in order to change the metric, the component, the normalization and the year of the building lifetime. You can choose between Embodied Energy or Embodied Carbon results by clicking in the corresponding logo in the top of the “Results” section (1).

You can modify the result type (Between results for the complete building or only envelope), the normalization (Total results or normalized by floor area) and the year to visualize (Results are given as a cumulative value taking into account replacement cycles). To do so, choose the desired type using the dropdown and text boxes in the control (2). Whenever you make a change, the false color will automatically re-render.

The umi “Simulate” panel also incorporates a color scale which will automatically show the min and max of the visualization (3) as well as an info text (4) that will show the specific value associated with selected buildings. The color bar limits can be modified to suit the color range to the needs of the user just by typing in new limits. In order to keep the new limits fixed for a new false color you can block them by clicking the “Lock” icons located besides. The info text located on top of the color bar will show one value if one building is selected, and the addition of all selected if it is a multiple selection.

3. Exporting results into CSV
`````````````````````````````

Within the results visualization controls in the “Simulate” panel in umi it is possible to directly export results in a comma separated value (CSV) format which can later be easily manipulated as a spreadsheet in Excel or similar software. To do so you can click the ‘Export” button in the bottom of the panel which again offers “AllBuildings” and “SelectedBuildings” modes. Then a new file called “Results” will be created in your desktop. This file will only contain results for the metric, unit, normalization, etc. currently selected in the controls.

.. raw:: html

   <iframe width="100%" max-height="315" height="315" src="https://www.youtube-nocookie.com/embed/b5-L3sgW8lA?rel=0" frameborder="0" allowfullscreen></iframe>
