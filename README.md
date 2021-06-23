## Sisfrutos Papaya: a Dataset for Detection and Classification of Diseases in Papaya
In recent years, approaches based on machine learning, more specifically Deep Neural Networks (DNN), have gained prominence as a solution to computer vision problems in the most diverse areas. However, this type of approach requires a large number of samples of the problem to be treated, which often makes this type of approach difficult. In computer vision appli-cations aimed at fruit growing, this problem is even more noticeable, as the performance of computer vision approaches in this segment is still well be-low the performance achieved in other areas. One of the main reasons listed by the literature for the little evolution in this area is the lack of large data sets duly and manually annotated, which are mandatory for applications that use cutting-edge computer vision techniques such as DNNs. The present work aims to leverage research in this domain, creating a new dataset of im-ages, of an unparalleled size in the literature, with the main diseases and damages of papaya fruit (Carica Papaya). The proposed data set in this work consists of 15,179 RGB images duly and manually annotated with the posi-tion of the fruit and the disease/damage found within it.
To validate our dataset, we use it to train a DNN-based classifier in the task of detecting diseases and defects in a papaya image. We recreated the old challenge “Man vs. Machine” comparing our classifier with a human ex-pert in a real environment. Our model reached an f1-score of 80.01%, while the overall performance obtained by the human expert was 67.3%

### Requisitos
- Ubuntu 18
- Cuda 10.1
- Cudnn 8.0
- OpenCV 4.5

## Neural network model and examples for inference
Download the folder below, it has all the files needed for testing with the model.
To download the complete dataset, see the Dataset Papaya item.
https://drive.google.com/drive/folders/13A2Dj1Fj8B4aKiAqn1xvUWiKRBBeE15P?usp=sharing

## DataSet
-  Description: Complete base composed of 15179 images with the following class distributions:
<img src=https://github.com/jairolucas/Sisfrutos-Papaya/blob/main/classes%20icann.png height=300 e width=450>

### Inference
- to make inferences :  ./darknet detector test data/obj.data cfg/yolov4.cfg  nameimage  yolov4.weights


### Sample images for inference testing
https://drive.google.com/drive/folders/1GhCxUPzlfXBJRIXsuwiDwkZY8aNduu1_?usp=sharing

## Results
### F1-score 0.801
<img src=https://github.com/jairolucas/Sisfrutos-Papaya/blob/main/graf%20icann.png height=300 e width=450>
