# Recognizing Families In the Wild
<p align="justify"> 
This Github repository contains the work done for the CX4041 Machine Learning project in Nanyang Technological University, Singapore. In this project, we are required to work on one of the past Kaggle competitions by applying what we have learnt during the course of the semester. We decided to work on the 2019 Kaggle Competition: [Northeastern SMILE Lab - Recognising Faces in the Wild](https://www.kaggle.com/competitions/recognizing-faces-in-the-wild/overview), where we are provided with the Families In the Wild (link) dataset and tasked to tackle the problem of Facial Kinship Verification (FKV). The goal of FKV is to create an automatic kinship classifier to determine if two individuals are biologically related based on just their facial images. Submissions to Kaggle were evaluated on the area under the ROC curve between the predicted probability and the observed target.
</p>

<p align="justify"> 
After extensive research on the performance of traditional machine learning techniques and deep learning techniques, we decided to concentrate our efforts on transfer learning, which is well-known to generate a good performance within a relatively short period of time. The use of transfer learning in our project revolves around utilizing models previously trained for facial recognition tasks to be customized to fit our FKV needs.
</p>

  

In our experiments, we attempted various pretrained state-of-the-art face models, which include [Facebook DeepFace](https://ieeexplore.ieee.org/document/6909616), [ArcFace]( https://ieeexplore.ieee.org/document/8953658), [FaceNet](https://ieeexplore.ieee.org/document/7298682), [OpenFace](https://ieeexplore.ieee.org/document/7477553), [ResNet](https://ieeexplore.ieee.org/document/7780459), [SENet](https://ieeexplore.ieee.org/document/8578843), and [Face Transformer](https://arxiv.org/abs/2103.14803). For each model, we tried one or more feature concatenation techniques and trained on different samples of the dataset to generate uncorrelated models to build our ensemble. Ultimately, throughout the duration of the project, we trained a total of 238 different base classifiers. Our best performing ensemble consists of a combination of classifiers trained on the outputs of ArcFace, FaceNet, ResNet-50, SENet-50, and Vision Transformer to produce a public score of 91.5%, placing us in the 6th place (out of 522 teams) in the public leaderboard. 

