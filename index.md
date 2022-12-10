---
layout: default
---
# The Pollenbee Dataset
_"Improving pollen-bearing honey bee detection from videos captured at hive entrance by combining deep learning and handling imbalance techniques"_

The Pollenbee Dataset is built for the purpose of serving the problem of detecting pollen bees. The dataset contains more than **2000 images**, which include 2 classes of objects: pollen-bearing bees and non-pollen-bearing bees with numbers of 1758 and 59068 respectively. 

The dataset was collected at the bee farm of the Vietnam Agricultural Academy by a data acquisition system consisting of an Nvidia jetson nano development kit and an IMX477 HQ camera with a 6mm CS-Mount lens, all devices are placed in a housing surveillance weatherproof outdoor camera box. We adjust the camera along with the downward-facing view. We attach the housing surveillance weatherproof outdoor camera box within only one stage of the hive body. Our data acquisition system:

![Data acquisition system](images/system.PNG)

Example of video collected by our data acquisition system:

![Example of our collected video](images/video_dataset.gif)

# Details
We collect data as videos over many days, each video lasts **1 minute**, each day from 6 am to 5:30 pm, and each time is separate 30 minutes to obtain images at different times with different natural light conditions and a different number of bees. All videos were recorded in the resolution of **1920x1080 at 60 fps**. Next figure show some examples of dataset in different light conditions:

![Data different light condition](images/light_condition.png)

Based on observations on captured videos, pollen-bearing bees are usually present from 8:30 a.m. to 11 a.m., so we selected videos during those times to create the dataset. The pollen-bearing bees in the dataset varied in size as well as the color of pollen the bees carried. Figure below shows examples of pollen-bearing bees in our dataset:

![Examples of pollen-bearing bees in our dataset](images/pollenbee_variety.png)

The number of each object class in the dataset is shown in the following table:

| id| Label        | Object class           | Instances |
|:--|:-------------|:-----------------------|:----------|
| 1 | nonpollenbee | Non pollen-bearing bee | 59068     |
| 2 | pollenbee    | Pollen-bearing bee     | 1758      |
|   |              | **Total:**             | 60826     |

The dataset was annotated manualy first by Labelme Annotation tools and then by a object detection model trained on the annotated dataset. Next figure show the annotation process by Labelme Annotation Tool.
![Annotation](images/annotations.PNG)

<!-- # Citation
If you find useful the Pollenbee dataset for your research, please cite the paper:
```js
// Javascript code with syntax highlighting.
var fun = function lang(l) {
  dateformat.i18n = require('./lang/' + l)
  return true;
}
``` -->