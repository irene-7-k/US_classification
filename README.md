# US_classification - Applying Deep Learning techniques for Ultrasound Image Classification

## Project Background
Ultrasound is a safe, convenient and accessible examination tool. In order to help doctors to prioritize and optimize the time spent on reviewing ultrasound scans, reliable deep learning techniques are explored in image classification. To address the lack of sufficient dataset for the training of deep learning model, transfer learning (TL) technique is explored.

## Solution
CNN delivers state-of-the-art accuracy on the ImageNet task (e.g. LSVRC). In this project, architectures resnet34 and densenet121 are utilized to see whether one architecture performs better than the other. For each dataset/architecture, train model for 3 cases to see if TL improves model accuracy.

The 3 cases:
Case1 - TL with pretrained body weights
Case2 - Trained from scratch 
Case3 -  TL with model body and head trained with different datasets

## Result
For either architecture, transfer learning with model body trained with original dataset and model head trained with reconstructed dataset (Case3) results in a higher accuracy.

## Business Value
In order to get a model with best accuracy:
• Choose a proper CNN model architecture according to dataset given.
• For small dataset, it is better to train the model body with a larger dataset from a similar project, followed by training the model head with the given dataset.

## Comment
In the training process, metrics "accuracy" is for multi-class tasks or binary tasks with balanced dataset; but "auroc" is restricted to binary tasks, good for unbalanced dataset.
