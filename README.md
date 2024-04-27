# DSA5204 Project

This repository hosts the code for our NUS DSA5204 Project, which aims to reproduce and extend the work done in [Masked Autoencoders Are Scalable Vision Learners](https://arxiv.org/abs/2111.06377).
This diagram shows the model architecture for the paper. The encoder is a ViT and decoder is a set of transformer blocks.
![alt text] (https://github.com/liawzhengkai/dsa5204-project/blob/main/imgs/mae_architecture.png)

## Development Setup

### Setting up environment

#### pip

To set up using pip, run the following:

    cd <project_root>
    pip install -r requirements.txt

### Project Structure
    .
    ├── src                     # Source code
    │   ├── dataset             # Dataloaders
    │   ├── model               # Model architectures
    │   └── scripts             # Training, Evaluation scripts  
    ├── inference_notebook_examples # Quick look on our model inference results after training
    ├── .gitignore
    ├── README.md
    └── requirements.txt

## Datasets

We make use of the following datasets:
- ImageNet1K (IN1K): Download the following files from [here](https://image-net.org/challenges/LSVRC/2012/2012-downloads.php): (1) Development kit (Tasks 1 & 2), (2) Training images (Task 1 & 2), and (3) Validation images (all tasks), place them in the `data/imagenet1k` folder and run the following code from root folder:

        from torchvision.datasets import ImageNet
        train = ImageNet(root='./data/imagenet1k', split='train')
        val = ImageNet(root='./data/imagenet1k', split='val')

- ADE20k: Data is available at: http://data.csail.mit.edu/places/ADEchallenge/ADEChallengeData2016.zip. Unzip and place directly in data folder as is
- Time Series: Data is available at: https://github.com/zhouhaoyi/ETDataset

## References 

Upernet: https://github.com/CSAILVision/semantic-segmentation-pytorch
Time Series: https://github.com/asmodaay/ti-mae
