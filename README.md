# Race-Prediction
Race prediction using facial images

Dataset used here is UTKFace Dataset:
UTKFace dataset is a large-scale face dataset with long age span (range from 0 to 116 years old). The dataset consists of over 20,000 face images with annotations of age, gender, and ethnicity. The images cover large variation in pose, facial expression, illumination, occlusion, resolution, etc. This dataset could be used on a variety of tasks, e.g., face detection, age estimation, age progression/regression, landmark localization, etc.

The labels of each face image is embedded in the file name, formated like [age][gender][race]_[date&time].jpg

[age] is an integer from 0 to 116, indicating the age [gender] is either 0 (male) or 1 (female) [race] is an integer from 0 to 4, denoting White, Black, Asian, Indian, and Others (like Hispanic, Latino, Middle Eastern) respectively. [date&time] is in the format of yyyymmddHHMMSSFFF, showing the date and time an image was collected to UTKFace

We are only interested in Race prediction hence rest all the data is ignored.

We tried the race prediction using 2 deep learning models:
1. A CNN model trained from scratch
2. A Transfer learning CNN model trained on Imagenet and finetuned on our dataset.

The results are as follows:
1. Model trained from scratch:

![scratch](https://github.com/shreyshah97/Race-Prediction/blob/master/Images/scratch.png)

2. Fine tuned Model:

![transfer](https://github.com/shreyshah97/Race-Prediction/blob/master/Images/transfer.png)

The transfer learning model took less time to train and increased accuracy by 4-5%.
The errors looked as follows:

![output](https://github.com/shreyshah97/Race-Prediction/blob/master/Images/output.png)
