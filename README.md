https://coding-mechanism.github.io/nonPlanarPostProcessor/

# nonPlanarPostProcessor
minimal non planar post processor, experimental

Only works with prusaSlicer for now

You need Exclude Object definitions enabled in prusaSlicer, and verbose Gcode enabled (ex ";LAYER CHANGE").

-------------------
The Hard part:

First in CAD you create a ~0.2mm surface that lies on top of your part.
It will be the non-planar surface.
Then you export and slice it in prusaSlicer on its side:


<img width="1913" height="947" alt="image" src="https://github.com/user-attachments/assets/e3dc7e19-1da8-4cf3-ac3e-579dd6ecf6e4" />





Then in CAD you export the rest of the object excluding that top surface, and slice it like normal


<img width="1913" height="947" alt="image" src="https://github.com/user-attachments/assets/025bbabd-eded-4e7c-b30e-3c8c65d34ebf" />


Upload both files into script:

<img width="728" height="905" alt="image" src="https://github.com/user-attachments/assets/842e1741-9caa-410e-a7fe-7b73507ad7a1" />

It rotates and centers the top surface on top of the rest of the object. 
Also changes the gcode paths to zig zag on the top surface instead of moving through the object on travel moves
 
<img width="1920" height="677" alt="image" src="https://github.com/user-attachments/assets/d6991625-e38b-4501-ad6e-464e3f3c5e60" />
