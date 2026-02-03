# Implementing VICReg-from-scratch
### A Self-Supervised Joint-Embedding Non-Contrastive Framework for learning useful Representations.
### VICReg is a Self-Supervised Joint-Embedding Architecture that jointly implements a Variance, Invariance, and Covariance loss in an effort to prevent latent embedding collapse using a non-contrastive approach.
### Following the original VICReg paper, I replicated the proposed architecture on my dataset of choice.
## Methods:
### Dataset: CIFAR-10. 60,000 images for Self-Supervised Pretraining (without label).
### Pretrained a VICReg model on the entire dataset, with no labels.
### Pretraining took about 4 hours (see hyperparameters in code body).
### I saved the ‘.pth’ file after pretraining and loaded it back for Linear Probing.
### Linear Probing by freezing the Encoder (plus throwing out the Projector) and attaching a Linear Classifier head. Trained on a 1% subset (600 images) of the original dataset. 
### Separately trained another Simple Linear Classifier on the same 1% subset for comparison.
### Linear-Probed VICReg achieved 74.5% Accuracy.
### Simple Linear Classifier achieved 28.9% Accuracy.
### Shows that the VICReg Encoder learned useful image representations from Self-Supervised Pretraining.
