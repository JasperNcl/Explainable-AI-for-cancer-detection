# Explainable-AI-for-cancer-detection
This is a project for explainable ai for cancer detection



### 1, file path

The path to the folder in my Google Drive is: "/content/drive/MyDrive/Dissertation/MyWork"

Here is the overall structure of the MyWork folder

```
MyWork
 |-- Dataset
     |-- Blood_Cancer   (Training dataset)
     |-- GT             (Training ground truth)
     |-- GT1024         (ground truth size 1024x1024)
     |-- TestBC         (Testing dataset)
     |-- TestGT         (Testing ground truth)
     |-- TestPRE        (Testing prediction result)
     |-- Best_loss.txt  (Best loss temporary document)
     |-- ious.txt       (IoU for all prediction)
     |-- weight.torch   (weight of semantic segmentation)

 |-- SAM model
     |-- sam_vit_h_4b8939.pth    (Weight of SAM)  
     |-- sam_vit_l_0b3195.pth    (Weight of SAM) 
     |-- sam_vit_b_01ec64.pth    (Weight of SAM) 

 |-- "1 - data preprocessing.ipynb"
 |-- "2 - Semantic Segmentation.ipynb"
 |-- "3 - prediction and model explain.ipynb"
 |-- "4 - analysis of the result.ipynb"
```



### 2, Before run the code

The model .pth files need to be downloaded from the Segment Anything Model repo, 

This is the official model for all three specifications, but I only use  "vit_h" in my code.

The download url are:

https://dl.fbaipublicfiles.com/segment_anything/sam_vit_h_4b8939.pth
https://dl.fbaipublicfiles.com/segment_anything/sam_vit_l_0b3195.pth
https://dl.fbaipublicfiles.com/segment_anything/sam_vit_b_01ec64.pth


where the files are stored:
b_checkpoint = "/content/drive/MyDrive/Dissertation/MyWork/SAM model/sam_vit_b_01ec64.pth"
l_checkpoint = "/content/drive/MyDrive/Dissertation/MyWork/SAM model/sam_vit_l_0b3195.pth"
h_checkpoint = "/content/drive/MyDrive/Dissertation/MyWork/SAM model/sam_vit_h_4b8939.pth"

### 3， Dataset

Due to file size, I only keep 30 images in each folder of dataset or ground truth, which is more than enough if you just want to try the code. 

If you want to run all the code, please follow the folder structure hints above and the corresponding code to complete the image data.

The dataset can be found on Kaggle at
https://www.kaggle.com/datasets/akhiljethwa/blood-cancer-image-dataset
