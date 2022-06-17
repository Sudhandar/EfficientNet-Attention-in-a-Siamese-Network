# Siamese neural network based Covid-19 Pneumonia classification using EfficientNet with attention mechanism

X-rays provide a cost-effective way to detect Covid-19 and are more readily available in many developing and under-developing countries than CT scans. In order to build a deep learning model to detect Covid-19 from X-ray images which can be deployed in the real world, this project uses the EfficientNet model introduced in [1] and incorporates an attention mechanism introduced in [2] which was designed for medical images to capture the localized fea- tures in X-ray images. Furthermore, the proposed model is trained in a triplet-based Siamese neural network frame-work to segregate the closely related Pneumonia types like Viral Pneumonia, Bacterial Pneumonia and Covid-19 Induced Pneumonia. 

## Dataset

The Covid-19 Radiography database is used as the dataset to test the performance of the proposed architecture. The selected dataset is the winner of the Covid-19 dataset award by the Kaggle community. The dataset consists of X- ray images belonging to 4 classes, covid-19 positive cases (Covid-19 Pneumonia), normal cases (no lung infection), non-covid lung infection and viral pneumonia. It is an imbalanced dataset with an image size of 256 x 256 and the following is the splitup of the number of samples in each class.

|         **Class **        | **# Of samples ** |
|:-------------------------:|:-----------------:|
|     Covid-19 Positive     |       3616        |
| Non-Covid Lung Infection  |       6012        |
|          Normal           |       10192       |
|      Viral Pneumonia      |       1345        |


### Sample Images 

![alt text](https://github.com/Sudhandar/EfficientNet-Attention-in-a-Siamese-Network/blob/main/images/Viral%20Pneumonia-1.png)

## Model Architecture

## Results

## Implementation details

## Reference


