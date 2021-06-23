## Detecção e Classificação de Doenças no Papaya Usando Deep Learning
In recent years, approaches based on machine learning, more specifically Deep Neural Networks (DNN), have gained prominence as a solution to computer vision problems in the most diverse areas. However, this type of approach requires a large number of samples of the problem to be treated, which often makes this type of approach difficult. In computer vision appli-cations aimed at fruit growing, this problem is even more noticeable, as the performance of computer vision approaches in this segment is still well be-low the performance achieved in other areas. One of the main reasons listed by the literature for the little evolution in this area is the lack of large data sets duly and manually annotated, which are mandatory for applications that use cutting-edge computer vision techniques such as DNNs. The present work aims to leverage research in this domain, creating a new dataset of im-ages, of an unparalleled size in the literature, with the main diseases and damages of papaya fruit (Carica Papaya). The proposed data set in this work consists of 15,179 RGB images duly and manually annotated with the posi-tion of the fruit and the disease/damage found within it.
To validate our dataset, we use it to train a DNN-based classifier in the task of detecting diseases and defects in a papaya image. We recreated the old challenge “Man vs. Machine” comparing our classifier with a human ex-pert in a real environment. Our model reached an f1-score of 80.01%, while the overall performance obtained by the human expert was 67.3%

### Pré-Requisitos
- Ubuntu 18
- Cuda 10.1
- Cudnn 8.0
- OpenCV 4.5

## DataSet
-  Description: Complete base composed of 17964 images with the following class distributions:
<img src=https://github.com/jhony2507/Base_doencas_mamao/blob/main/tabela%20classes.png height=300 e width=450>

### Neural network model and examples for inference
Download the folder below, it has all the files needed for testing with the model.
To download the complete dataset, see the Dataset Papaya item.
https://drive.google.com/drive/folders/13A2Dj1Fj8B4aKiAqn1xvUWiKRBBeE15P?usp=sharing


## Treinar / Testar Rede
- Hardware utilizado: Gpu Nvidia 1060 com 6gb de memória
- Tempo de Treinamento: 
  * DataSet B128  : 1:40 horas
  * DataSet B1024 : ~59 horas
  * DataSet Bcompleta : xxx
- Para treinar: ./darknet detector train data/obj.data cfg/yolov4.cfg yolov4.conv.137 -map
- Para testar : ./darknet detector test data/obj.data cfg/yolov4.cfg yolov4.weights

## Resultados
- [Gráfico mAP Dataset B128](results/chartb128.png)
* precision = 1.0, 
* Recall    = 1.0, 
* F1-score  = 1.0
* mean average precision (mAP) = 1.000, or 100.00 %
#### Por classe:
* class_id = 0, name = FRUTO_SEM_DOENÇA, ap = 100.00%  (TP = 44, FP = 0) 
* class_id = 1, name = Antracnose,       ap = 100.00%  (TP = 12, FP = 0) 
* class_id = 2, name = Phytoftora,       ap = 100.00%  (TP = 12, FP = 0) 
* class_id = 3, name = Dano_Mecânico,    ap = 100.00%  (TP = 12, FP = 0) 
* class_id = 4, name = Mancha_Chocolate, ap = 100.00%  (TP = 12, FP = 0) 
* class_id = 5, name = Meleira,          ap = 100.00%  (TP = 12, FP = 0) 
* class_id = 6, name = Mancha_Fisiologica, ap = 100 %  (TP = 12, FP = 0) 
* class_id = 7, name = Pinta_Preta,      ap = 100.00%  (TP = 12, FP = 0)

### B1024
- [Gráfico mAP DataSet B1024](results/chart.png)
* precision = 0.83, 
* Recall    = 0.91, 
* F1-score  = 0.87
* mean average precision (mAP) = 0.896401, or 89.64 %

#### Por classe:
* class_id = 0, name = FRUTO_SEM_DOENÇA,     ap = 93.78%        (TP = 334, FP = 72)
* class_id = 1, name = Antracnose,             ap = 75.93%        (TP = 76, FP = 36)
* class_id = 2, name = Phytoftora,             ap = 98.87%        (TP = 99, FP = 16)
* class_id = 3, name = Dano_Mecânico,         ap = 80.99%        (TP = 72, FP = 15)
* class_id = 4, name = Mancha_Chocolate,         ap = 87.15%        (TP = 71, FP = 3)
* class_id = 5, name = Meleira,             ap = 91.73%        (TP = 74, FP = 3)
* class_id = 6, name = Mancha_Fisiologica,         ap = 84.34%        (TP = 89, FP = 57)
* class_id = 7, name = Pinta_Preta,             ap = 96.33%        (TP = 100, FP = 19


- [Gráfico mAP Dataset Bcompleta](results/chartCompleta.png)
