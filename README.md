## Duke Description
Duke is a subset of the [DukeMTMC](http://vision.cs.duke.edu/DukeMTMC/) for image-based re-ID, in the format of the Market-1501 dataset. The original dataset contains 85-minute high-resolution videos from 8 different cameras. Hand-drawn pedestrain bounding boxes are available. 

We crop pedestrain images from the videos every 120 frames, yielding in total 36,411 bounding boxes with IDs. There are 1,404 identities appearing in more than two cameras and 408 identities (distractor ID) who appear in only one camera. We randomly select 702 IDs as training set and the remaining 702 IDs as the testing set. In the testing set, we pick one query image for each ID in each camera and put the remaining images in the gallery. 

**As a result, we get 16,522 training images of 702 identities, 2,228 query images of the other 702 identities and 17,661 gallery images.** 

### About Dataset
|File  | Description | 
| --------   | -----  |
|/bounding_box_test  | The gallery images. We retrieve a query from this image pool.|
|/bounding_box_train  | The training images. This dir contains the images from 702 different identities.|
|/query  | The query images. Each of them is from different identities in different cameras.|

**Naming Rule of the images** In bbox "0005_c2_f0046985.jpg", "0005" is the identity. "c2" means the image from Camera 2. "f0046985" is the 46985th frame in the video of Camera 2.

### Download Dataset
You can download the Duke dataset from [GoogleDriver](https://drive.google.com/open?id=0B0VOCNYh8HeRSDRwczZIT0lZTG8)
or ([BaiduYun](https://pan.baidu.com/s/1cIOYOu) password:48z4).

If these links are unavailable, please don't hesitate to contact me to update links. Thank you.

### Evaluation
Download the codes in this repository. To evaluate your code, you just need to change the image path and the feature path in the `evaluation_res_duke_fast.m` and run it.

### Baseline
|Methods |   Rank@1 | mAP|
| --------   | -----  | ----  |
|BoW+kissme | 25.13% | 12.17% |
|LOMO+XQDA | 30.75% | 17.04% |
|Basel.  | 65.22% | 44.99%|
|Basel. + LSRO   | 67.68% | 47.13%|

### Citation
Duke Dataset, Baseline [Bibtex](https://raw.githubusercontent.com/layumi/DukeMTMC_evaluation/master/citation.txt)

Duke MTMC Dataset [Bibtex](http://vision.cs.duke.edu/DukeMTMC/refs/ristani2016MTMC.txt)
