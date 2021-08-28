# Image Blending 

## Objective:
### To blend a bunch of x-ray threat object images onto the given x-ray bag images.


## Method :
### Threat Object Extraction
1) The first part of the method was image pre-processing: This involved thresholding, smoothening, edge detection and contour extraction. 


2) After finding the contour, the ROI had to be extracted from the image.


3) Next, the contour area was masked with 255('white') in a array of 0s (Black), and the ROI was extracted from the original image with mask as reference.


4) The Threat Image was converted to PNG and the background was made transparent by adding an alpha channel and making it 0. Hence retrieving the Threat Object.


5) The Threat object was then rotated by 45 degrees and scaled down to 0.5 of its size using the imutils library.


6) The Threat object was then stored on the disk.


### Blending the threat object onto the baggage image

1) The background image and the threat object were loaded from disk

2) A new format of the image is created for Pillow using the size of the threat object image. 

3) The Threat image is then pasted onto the Baggage image.


4) Final image is achieved.

