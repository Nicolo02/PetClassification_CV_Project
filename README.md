# Cat and Dog Breed Classification

## Project Overview
This Universisty project for ***Computer Vision and Image Processing*** course focuses on building and training a CNN to classify images of 37 different breeds of cats and dogs. The primary goal is to achieve an accuracy of approximately 60% on the validation set. The task is splitted in two subtasks:
- 1) building from scratch a new CNN reaching at least 60% of accuracy 
- 2) fine tunining an existing ResNet-18 model reaching at least 80% accuracy

Based on the [Oxford-IIIT Pet Dataset](https://www.robots.ox.ac.uk/~vgg/data/pets/).

## Project Structure
```text
.
├── notebooks/
│   ├── 1.02_modelImplementation.ipynb
│   └── 1.03_modelImplementation.ipynb
├── README.md
└── Tasks.ipynb
```

- `Tasks.ipynb`: The main notebook containing the complete workflow, data preprocessing, and the final model architecture.
- `notebooks/`: A directory containing the iterative steps and intermediate model implementations.


### Data Split
The original dataset split was modified to ensure a robust training and evaluation process:
- **Train split:** 80% of original train + 60% of original test
- **Validation split:** 20% of original train + 20% of original test
- **Test split:** 20% of original test

## Workflow

The complete step-by-step implementation is detailed in the `Tasks.ipynb` notebook. The core pipeline includes:

- **Data Processing:** Images are resized to 256x256, normalized, and augmented (via flipping, cropping, and color jittering) to prevent overfitting.
- **Model Architecture:** An iterative approach was used, starting from a basic 3-block CNN and evolving into a more complex VGG16-like structure.
- **Training Configuration:** Models are trained with a batch size of 32, using SGD or Adam optimizers, along with callbacks like Early Stopping to optimize performance.

## Requirements
The following libraries are required to run the notebook:
- Python 3.x
- TensorFlow (and `tensorflow_datasets`)
- Keras
- NumPy
- Pandas
- Matplotlib
- OpenCV (`cv2`)

## How to Run
1. It is highly recommended to run this notebook in an environment with hardware acceleration (GPU) enabled.
2. Install the required libraries using pip.
3. Execute the notebook sequentially. The dataset will be downloaded and prepared automatically during the data import step.