# Keypoints
Apparel Keypoints Localization Model - Alibaba Fashion Dataset


**Introduction**

Machine analysis of apparel could easily be affected by the dimension and shape of clothes, the distance and angle of camera shooting, and even how the apparel is displayed or the model is posing. Detection of apparel keypoints in images can help to improve the performance of applications such as alignment of clothes, recognition of clothes local attributes and auto-editing of apparel images.

We provide a dataset for key point localization of the apparel in practical scenarios. In this dataset, a set of clothing keypoints is defined on the basis of fashion design. The set is further refined into six subsets according to the following six women apparel categories: blouse, outwear, trousers, skirt, dress and jumpsuit, respectively. Currently, the dataset of the first five categories is open for download (the jumpsuit category is omitted since it is uncommon in the real-world scenario), including 41 sub-categories and 24 kinds of keypoints in total. There are altogether 100,000 annotated images in this dataset.


![Key_Points](https://work.alibaba-inc.com/aliwork_tfs/g01_alibaba-inc_com/tfscom/TB16Z8fXQCWBuNjy0FaXXXUlXXa.tfsprivate.jpg)


**Data Description**

*Image data*

All image data are from Alibaba e-Commerce platform. We randomly collected data with the following three standards:
1) The images fall into the five aforementioned categories as evenly as possible;
2) There are approximately an even number of single-model images and tiled single-piece images;
3) There are approximately an even number of simple-background and complex-background images.

*Keypoint Definition*

There are totally 24 type of keypoints, but not every cloth category needs to cover all those keypoints. For example, there are only 7 keypoints in trousers, with other keypoints inexistent, such as left/right necklines.

*Annotation Format*

Annotation file is saved in a csv-format table with a total of 26 columns: the first column (image_id) contains image file name, the second column (image_category) denotes the category that an image belongs to, and the remaining 24 columns record the positions of the aforementioned 24 keypoints, respectively.

Each keypoint is represented by a triple whoes elements are connected by underscores, denoted as "x_y_v", where the x and y are coordinates, and v is visibility. Visibility equals 1 if a keypoint is visible, 0 if it is occluded, and -1 if it is inexistent or undefined in the category.

*Training Data*

One folder and an annotation file can be found after decompressing the training data package.
- *Images* folder contains test images in jpeg format.
- *train.csv* contains annotation of training images. 
