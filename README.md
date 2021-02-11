# catsvsdogs
> Binary Classification using Pre-trained CNN network
Using Transfer Learning technique, I implemented CNN to classify Cats and dogs.

## Transfer Learning
To train a neural network, we need huge amount of data and computational power which can't afford by general mass. To mitigate this problem we can use transfer learning. Here we can download pretrained model which is trained on huge amount of data and modify the few layers at the end of the model architecture for example modify last neural network according to our output.

Using this technique, I have done my project to classify the cats and dogs

## Install Dependency
To clone and run this project we need to install some dependency
- pytorch
- torchvision
- matplotlib
- numpy
- PIL

To install `pytorch` and `torchvision` navigate to [this](https://pytorch.org/get-started/locally/)
To install `matplotlib`, `numpy`, `PIL` run the following command
```bash
$ pip install numpy matplotlib pillow
``` 
## File Description
`catvdog.pth` is the pre-trained `DenseNet` model with trained custom classifier which is trained on this [dataset](https://www.kaggle.com/c/dogs-vs-cats/data)
`DenseNet_CatsVSDogs.ipynb` is for training the custom classifier and save the model
`LoadModelAndTest.ipynb` is for testing with custom image of cats or dogs. You can load any cats or dogs image and run the model

## How to Use
### Data preparation for training part
1. Create folder `data`
2. Download data from [here](https://www.kaggle.com/c/dogs-vs-cats/data)
3. copy all cats image from `train` folder and paste it to `data/train/cat/`
4. copy all dogs image from `train` folder and paste it to `data/train/dog/`
5. Copy 20% image from `cat` and `dog` folder inside `train` folder and paste it to respective folder of `validation` folder
6. Inside `test` folder keep all image as it is and tested in `LoadModelAndTest.ipynb`

Now run `DenseNet_CatsVSDogs.ipynb` for training model

For testing and inference run `LoadModelAndTest.ipynb`