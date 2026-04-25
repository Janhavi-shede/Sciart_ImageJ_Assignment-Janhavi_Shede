**ImageJ Particle Counting Assignment Protocol**

**Step 1: Data sorcing and Documentation**

I began by retrieving a raw AATF image from the OpenCell online database, prioritizing a sample with distinct objects and minimal pre-processing. I made sure that the particles in the image were clearly distinguishable from the background.

**Step 1: Opening and Preparation of the Image**

I first copied the image by right clicking on the image and selecting 'copy'.
Then I pasted the image in ImageJ by using: Edit → Paste.

I converted the image to 8-bit grayscale to standardize the format by using: Image → Type → 8-bit.

Then I removed background noise with the help of subtract background function: Process → Subtract Background.
'Rolling Ball Radius' was adjusted to *12 pixels* and 'Light background' option was *deselected*

Later I adjusted the brightness and contrast: Image → Adjust → Brightness/Contrast.
I applied 'Auto' about 6-7 times till I found the result satisfactory and the clicked 'Apply'.

**Step 3: Thresholding the image**

I applied threshold to separate particles from the background by using: Image → Adjust → Threshold.
Method used was set to *Default*, Lower threshold value was *96*, Upper threshold value was *255* and, 'Dark background' and 'Don't reset range' was *selected*.

I adjusted the threshold by clicking on 'Auto' until the particles appeared clearly highlighted while minimizing backgroun.
After achieving a result to my liking, I applied the threshold by clicking on 'Apply'.

Then, I applied watershed segmentation by using: Process → Binary → Watershed.

**Step 4: Particle Analysis of the Image**

I performed particle analysis using: Analyze → Analyze Particles
The parameters used were: Size range as*50 – Infinity pixels* and Circularity as *0.40 – 1.00*
And 'Display Results', 'Summarize', 'Exclude on Edges', 'Add to Manager' and 'Overlay' options were *selected*.

After analysis was done, a results table was generated along with an overlay that showed the detected particles.

**Step 5: Saving the Assignment Results**

The results table was saved as a CSV file: Results → File → Save As
It was saved as 'particle_count_result_aatf.csv'

The processed image was then saved as a TIFF file: File → Save As → TIFF
It was saved as 'result_image_aatf.tif'

### The Final Result

The final result of the assignment was a CSV file containing quantitative measurements of all detected particles and an image with particle boundaries that were clearly marked.

This protocol ensures reproducible particle detection and analysis in ImageJ, with parameter selection tailored to the specific image.
