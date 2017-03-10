# Duke Description
Duke is a subset of the [DukeMTMC](http://vision.cs.duke.edu/DukeMTMC/). The original dataset contains 85-minute high-resolution videos from 8 different cameras. Hand-drawn pedestrain bounding boxes are available. In this work, we use a subset for image-based re-ID, in the format of Market-1501.

The Duke dataset has 1,812 identities in 8 cameras. We crop pedestrain images from the videos every 120 frames, yielding in total 36,411 bounding boxes with IDs. There are 1,404 identities appearing in more than two cameras and 408 identities (distractor ID) who appear in only one camera. We randomly select 702 IDs as training set and the rest 702 IDs as the testing set. In the testing set, we pick one qury images for each ID under each camera and put the rest images in the gallery. As a result, we get 16,522 training images of 702 identities, 2,228 query images of the other 702 identities and 17,661 gallery images. 

# Download Dataset
You can download the Duke dataset from [GoogleDriver](https://drive.google.com/open?id=0B0VOCNYh8HeRZ1hiSjRMRFpOaTA)
or ([BaiduYun](https://pan.baidu.com/s/1qYJcxhM) password:c7ex).

If these links are unavailable, please don't hesitate to contact me to update links. 

# Evaluation
Download the codes in this repository. To evaluate your code, please change the feature path in the `evaluation_res_duke_fast.m` and run it.

# Baseline
|Methods |   Rank@1 | mAP|
| --------   | -----  | ----  |
|Basel.  | 65.22% | 44.99%|
|Basel. + LSRO   | 67.68% | 47.13%|

# Citation
Duke dataset, Baseline [Bibtex](https://raw.githubusercontent.com/layumi/DukeMTMC_evaluation/master/citation.txt)

Duke MTMC dataset [Bibtex](http://vision.cs.duke.edu/DukeMTMC/refs/ristani2016MTMC.txt)
