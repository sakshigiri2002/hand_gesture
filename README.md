# Hand Gesture Recognition
To detect the hand gesture using OpenCv and Python
## Required libraries 
cv2 
``` pip install opencv ```

numpy
``` pip install numpy ```
## Methodology
- Capture the video frame:

Capture the video from camera using 

  ```cap = cv2.VideoCapture(0)```
- Hand Segmentation: 

Convert the frame from RGB to Grayscale

  ```gray = cv2.cvtColor(crop_img,cv2.COLOR_RGB2GRAY)```
- Apply Gaussian Blur to smooth the image.
- Apply thresholding to frame.

    ![Screenshot from 2021-10-11 17-35-04](https://user-images.githubusercontent.com/85958512/136789989-e232fd76-4c27-47e4-ab08-710117c34e54.png)
- Apply morphogical Transformations.

- Find the maximum contour.

    ![Screenshot from 2021-10-11 17-39-29](https://user-images.githubusercontent.com/85958512/136790374-69f1f5ed-ca6d-4ff5-b2f3-22cfde4c6c62.png)
    
    Contours is a curve joining all continous points along the boundary having same colour or intensity.
- Find convex-hull

    ![Screenshot from 2021-10-11 17-39-29(1)](https://user-images.githubusercontent.com/85958512/136790830-a74043e6-cf1f-49e2-a785-f491549986b2.png)
    
Find the convex points
 
- Count no of convexity defects

    ![Screenshot from 2021-10-11 17-45-23](https://user-images.githubusercontent.com/85958512/136791158-49750d8f-1114-4b7b-b65a-5241fab6a573.png)
    
Find the points

- Display the gesture
