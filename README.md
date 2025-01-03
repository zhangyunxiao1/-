# Research on defect detection algorithms based on generative models
  A Tensorflow implementation of "**Research on defect detection algorithms based on generative models**"

# The test environment
```
python 3.9
cuda 12.0
cudnn 7.1.4
Tensorflow 1.2
```

 
# my experimental results on this model
  **Notes:**  the first 30 subfolders are used as training sets, the remaining 20 for testing.    Although, I did not strictly follow the   params of the papar , I still got a good result.

**visualization:**


![image](https://github.com/user-attachments/assets/e42bbd4d-be86-4247-ab26-f28c71bbda3d)

![image](https://github.com/user-attachments/assets/98eeb619-b144-4214-baff-d44888912d6b)

![image](https://github.com/user-attachments/assets/83e7ca85-d8ab-4b67-900b-ac8bdc6f2a41)


# testing the model
  After downloading the KolektorSDD and changing the param[data_dir]
  ```
  python run.py --test
  ```
  Then you can find the result in the "/visulaiation/test" and  "Log/*.txt"
  
 # training the model
 
 **First, only the segmentation network is independently trained, then the weights for the segmentation network are frozen and only the decision network layers are trained.**
 
   training the segment network
   ```
   python run.py --train_segment
   ```
   training the  decision network
   ```
   python run.py  --train_decision
   ```
   training the total network( not good）
   ```
   python run.py  --train_total
   ```
 
