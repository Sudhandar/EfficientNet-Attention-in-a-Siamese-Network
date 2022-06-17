# Siamese neural network based Covid-19 Pneumonia classification using EfficientNet with attention mechanism

X-rays provide a cost-effective way to detect Covid-19 and are more readily available in many developing and under-developing countries than CT scans. In order to build a deep learning model to detect Covid-19 from X-ray images which can be deployed in the real world, this project uses the EfficientNetB0 model introduced in [1] and incorporates an attention mechanism introduced in [2] which was designed for medical images to capture the localized fea- tures in X-ray images. Furthermore, the proposed model is trained in a triplet-based Siamese neural network frame-work to segregate the closely related Pneumonia types like Viral Pneumonia, Bacterial Pneumonia and Covid-19 Induced Pneumonia. 

## Dataset

The Covid-19 Radiography database is used as the dataset to test the performance of the proposed architecture. The selected dataset is the winner of the Covid-19 dataset award by the Kaggle community. The dataset consists of X- ray images belonging to 4 classes, covid-19 positive cases (Covid-19 Pneumonia), normal cases (no lung infection), non-covid lung infection and viral pneumonia. It is an imbalanced dataset with an image size of 256 x 256 and the following is the splitup of the number of samples in each class.

|         **Class**         | **# Of samples**  | 
|:-------------------------:|:-----------------:|
|     Covid-19 Positive     |       3616        |
| Non-Covid Lung Infection  |       6012        |
|          Normal           |       10192       |
|      Viral Pneumonia      |       1345        |


### Sample Images 

![alt text](https://github.com/Sudhandar/EfficientNet-Attention-in-a-Siamese-Network/blob/main/images/sample_dataset.png)

## Model Architecture

### EfficientNetB0 with attention mechanism

![alt text](https://github.com/Sudhandar/EfficientNet-Attention-in-a-Siamese-Network/blob/main/images/efficient_net_main_model.png)

### Overall Architecture

![alt text](https://github.com/Sudhandar/EfficientNet-Attention-in-a-Siamese-Network/blob/main/images/efficient_net_siamese.png)

## Results

For evaluation, the F1 score is selected as the accuracy metric due to the imbalanced nature of the dataset. The introduction of the attention mechanism has improved the performance of the baseline EfficientNetB0 model (93.78%) and resulted in an F1 score of 94.94%. The Siamese neural network framework did not result in the improvement of the performance of the proposed model and obtained comparable results with an F1 score of 91.05%. The following two images showcase the embeddings before and after training in a Siamese neural network framework. 

![alt text](https://github.com/Sudhandar/EfficientNet-Attention-in-a-Siamese-Network/blob/main/images/siamese_before_training.png) ![alt text](https://github.com/Sudhandar/EfficientNet-Attention-in-a-Siamese-Network/blob/main/images/siamese_after_training.png)


Before training, the embeddings are randomly scattered and overlap each other. They are not grouped based on their similarities. After training, the embeddings are clustered based on their similarities and samples belonging to the same class are grouped after training. There are still a few overlaps among the classes and the model is not able to completely separate them into clusters.

## Implementation details

The repository contains two google colab notebooks. [EfficientNet with attention mechanism](https://github.com/Sudhandar/EfficientNet-Attention-in-a-Siamese-Network/blob/main/EfficientNet_with_attention_mechanism.ipynb) contains the code for the EfficientNetB0 baseline model and the EfficientNetB0 model with attention mechanism. [Siamese neural network framework](https://github.com/Sudhandar/EfficientNet-Attention-in-a-Siamese-Network/blob/main/Siamese_Networks.ipynb) contains the code for the Siamese neural network frameworks for the EfficientNetB0 baseline model and the EfficientNetB0 model with attention mechanism. Both the colab notebooks can be executed without needing to make any changes to the code.

## Reference


