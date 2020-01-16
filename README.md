# Galaxy Zoo - The Galaxy Challenge
### A Multi-Regression model for classification of Morphology of Galaxies.

This repository showcases the work I did for the  [Galaxy Zoo Challenge](https://www.kaggle.com/c/galaxy-zoo-the-galaxy-challenge)  on Kaggle. I took up this challenge as a personal project much later after it's completion. My submission **beat the 3rd ranked submission**, coming very close to the 2nd ranked submission.

|Private Score| 0.07788 |
|--|--|
|**Public Score**| **0.07794** |


## The Challenge

[Galaxy Zoo](http://www.galaxyzoo.org/) is a crowd sourcing project, where users are asked to describe the morphology of galaxies based on images. They are asked questions szuch as “How rounded is the galaxy” and “Does it have a central bulge”, and the users’ answers determine which question will be asked next. The questions form a decision tree which is shown in the figure below, taken from [Willett et al. 2013](http://arxiv.org/abs/1308.3496).

![alt text](https://storage.googleapis.com/kaggle-competitions/kaggle/3175/media/Screen%20Shot%202013-09-25%20at%2010.08.17.png)

The goal of the  Galaxy Zoo challenge is to predict these probabilities from the galaxy images that are shown to the users. In other words, build a model of how “the crowd” perceive and classify these images.

This means that we’re looking at a  **regression  problem**, not a classification problem: we don’t have to determine which classes the galaxies belong to, but rather the fraction of people who would classify them as such.



## My Solution

I made the model using **Fastai Library** which runs on a PyTorch backend. I used **transfer learning** from a pre-trained Resnet 34 using **Binary Cross Entropy Loss** as loss function and **One-cycle policy training**.  

The [Final Project Notebook](https://github.com/the-catalyst/Galaxy-Zoo---The-Galaxy-Challenge/blob/master/Galaxy%20Zoo%20%5BFinal%20Project%20Notebook%5D.ipynb) has step-by-step description and walks you through the project well. 

The model solution beat 3rd submission and can be compared via visual inspection [here.](https://storage.googleapis.com/kaggle-competitions/kaggle/3175/media/Screen%20Shot%202013-09-25%20at%2010.08.17.png)
![](https://github.com/the-catalyst/Galaxy-Zoo---The-Galaxy-Challenge/blob/master/Final%20Kaggle%20Score.png)
