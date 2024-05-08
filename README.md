OMR sheet MCQ scanner and test grader using Python and OpenCV. **Project report included**.

## **Key Points**
1. Steps involved:
    1. Detect the OMR sheet
    2. Apply perspective transform to get the top-down view of the sheet
    3. Extract out all the bubbles in the sheet
    4. Sort them in rows
    5. Determine the answer bubble for each row
    6. Match with the correct answer
    7. Do this for all questions (all rows)
2. Assumptions:
    1. The app assumes that the OMR document we are scanning is the main focus of the image.
    2. All 4 edges of the OMR document are visible in the image.
    3. The largest rectangle available in the image will be the OMR document. 
3. Stored the correct answer keys in a dict in python.
4. Used Canny edge detection for detecting the edges in the document and Gussian blur for reducing high frequency noise.
5. OpenCV has the way to get the top-down view of the image. Used that methodology to get the top-down view.
6. Used Otsu’s thresholding method for thresholding.
7. Determined the bubbles using the aspect ratio of approx one (1) for it's bounding rectangle.
8. Used bitwise operations and masking to find the filled in bubble using the amount of shaded pixels in the bubble.

 ## **Requirements:**
 1. python          (3.7.3)
 2. opencv          (4.1.0)
 3. numpy           (1.61.4)
 4. imutils         (0.5.2)

 ## **Commands to run the detection:**
 python test_grader.py --image images/test_01.png
 python test_grader.py --image images/test_02.png
 python test_grader.py --image images/test_03.png
 python test_grader.py --image images/test_04.png

## **Output**

![image](https://github.com/get-aastha/OMR_grader_project_image_processing/assets/108509128/6376e26c-542e-4588-9cb6-ab53f522049b)


![image](https://github.com/get-aastha/OMR_grader_project_image_processing/assets/108509128/089fd144-d4a0-4b7b-96cc-6c4ccd28b9d1)


![image](https://github.com/get-aastha/OMR_grader_project_image_processing/assets/108509128/a68c63d4-a9bb-4c62-b828-ddb8c9623a69)


![image](https://github.com/get-aastha/OMR_grader_project_image_processing/assets/108509128/fa9de3e3-da57-4616-bb89-37a84a0810f1)

