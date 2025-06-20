# Brain Tumor MRI Classification

A PyTorch-based Convolutional Neural Network (CNN) to classify brain MRI images into four tumor classes: Glioma, Meningioma, No Tumor, and Pituitary.

## Dataset: Brain Tumor MRI Dataset by Masoud Nickparvar on Kaggle
The dataset is structured as follows:

/Data <br>
├── Training<br>
│ ├── Glioma<br>
│ ├── Meningioma<br>
│ ├── No Tumor<br>
│ └── Pituitary<br>
└── Testing<br>
├── Glioma<br>
├── Meningioma<br>
├── No Tumor<br>
└── Pituitary<br>

Images are:
- Resized to 64×64
- Converted to grayscale
- Normalized with mean=0.5 and std=0.5

## Model Architecture

The CNN consists of:
- 3 convolutional layers with ReLU activations and max pooling
- Flattening followed by fully connected layers
- Dropout regularization
- Output layer with 4 units corresponding to the tumor classes

## Training Details

- **Loss Function**: CrossEntropyLoss
- **Optimizer**: Adam (lr=0.001, weight_decay=1e-4)
- **Metric**: Accuracy (using `torchmetrics`)
- **Batch Size**: 32
- **Device**: GPU (e.g., Tesla T4 on Colab)

## Performance

After 10 epochs, the model achieved:
- **Train Accuracy**: 97.26%
- **Test Accuracy**: 95.20%

## Setup & Usage
- Download Dataset from here: https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset
- Mount Google Drive in Colab:
   python
   from google.colab import drive
   drive.mount('/content/drive')
- Set the data path:
/content/drive/MyDrive/"YourDirectory"/Data
- Install dependencies:
-pip install torch torchvision torchmetrics
- Run the training script (multiclass-classification.ipynb)

License
MIT License

Acknowledgements
Dataset: Brain Tumor MRI Dataset by Masoud Nickparvar on Kaggle


 
