# Research on defect detection algorithms based on generative models
  A Tensorflow implementation of "**Research on defect detection algorithms based on generative models**"
  The author submitted the paper to  Journal of Intelligent Manufacturing (https://link.springer.com/article/10.1007/s10845-019-01476-x), where it was published In May 2019 . 
# The test environment
```
python 3.9
cuda 12.0
cudnn 7.1.4
Tensorflow 1.2
```
# You should know

  I used the Dataset used in the papar, you can download [KolektorSDD](https://www.vicos.si/Downloads/KolektorSDD) here.
  If you train you own datset ,you should change the dataset interfence for you dataset.

  You can refer to the [paper](https://link.springer.com/article/10.1007/s10845-019-01476-x) for details of the experiment.
 


# my experimental results on this model
  **Notes:**  the first 30 subfolders are used as training sets, the remaining 20 for testing.    Although, I did not strictly follow the   params of the papar , I still got a good result.

**visualization:**
![image](https://github.com/user-attachments/assets/e42bbd4d-be86-4247-ab26-f28c71bbda3d)
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
 
