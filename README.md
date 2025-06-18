Two Models :  HaarCascade(Non-ML) vs YOLO(Deep Learning) and Deep Face for emotion detection:
 Face Detection Accuracy: YOLO performs little better than HarrCascade for certain occulated frames.
![image](https://github.com/user-attachments/assets/ecce7435-4097-4d0f-a56e-a4c46a2516cc)

 
				HarrCascade
![image](https://github.com/user-attachments/assets/38f51fd6-99da-4f51-a6f0-6265a0fdbf42)



![image](https://github.com/user-attachments/assets/5382ee00-07e7-4d65-85b0-112c80c7bcbe)

YOLO Face detection approach:
Used the existing model from Github to detect the face. I found some issue related to version. Same project was not working on my machine because of some version mismatch.
Step-1 Detect the face and create the Bounding Box.
Step-2 Store all the images in output folder
Step-3 : Create a json file of all the bounding boxes for a given image. Following is the structure:
![image](https://github.com/user-attachments/assets/3c1cd397-5e7d-428b-a38a-67c821260779)

<img width="468" alt="image" src="https://github.com/user-attachments/assets/113480e2-3f16-4b05-b5fc-852ec2e6d73f" />

Step-4 Manual Annotation:
RoboFlow was the tool used to annotate the face with different emotion classes. Extracted the corresponding json. 
Below is the structure of the Ground Truth Bounding Boxes:
![image](https://github.com/user-attachments/assets/77c3f2db-a065-441d-ac1e-f03f2a76fc97)

<img width="468" alt="image" src="https://github.com/user-attachments/assets/0062f549-d022-47ba-ac16-6c31c6c768af" />

All Predicted Images: ![image](https://github.com/user-attachments/assets/2266c8a2-1188-46a5-a17b-787e11302e80)

<img width="200" alt="image" src="https://github.com/user-attachments/assets/3e39c80e-b0b5-4444-ab0d-767cc17979b7" />

<img width="468" alt="image" src="https://github.com/user-attachments/assets/bf439aa1-d504-4c19-8a75-592874264835" />

<img width="468" alt="image" src="https://github.com/user-attachments/assets/b740e6d4-d19a-4617-b588-d7469d0c1d20" />

<img width="468" alt="image" src="https://github.com/user-attachments/assets/8c8a7e1f-fc91-4bb3-bb6c-541174cff704" />

<img width="468" alt="image" src="https://github.com/user-attachments/assets/d6131770-2b29-4486-a77b-11f4fb452d96" />

<img width="432" alt="image" src="https://github.com/user-attachments/assets/2241493f-927d-4455-bced-c83f8315d5d2" />


<img width="468" alt="image" src="https://github.com/user-attachments/assets/e9b74d2d-30e8-4ad0-8db2-d01a004fba4f" />

Calculate Statistical Measurements like IOU, F1 Score, Accuracy:
 

**Challenges**:
•	Manual Annotation learning curve
•	Not perfect weights to calculate the emotions
•	Bounding box matching between GT and Predicted images because of not the uniform formatting
•	Time constraint 

**Improvement** :
Train the model against the given images
Use some more Ground truths to improve the statistical measures.
Show some graphs
![image](https://github.com/user-attachments/assets/bf50adb4-49a9-4221-97cf-851830914261)









