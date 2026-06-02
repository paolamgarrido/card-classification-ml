# Project Description

This project consists of building a machine learning model capable of classifying images of poker cards. The final objective is for the model to identify which class a card belongs to among a total of **53 classes**.

The development of the project follows the main stages of building a machine learning model: dataset selection, preprocessing, data splitting, model training, validation, tuning, prediction, and performance evaluation.

## How to Run

This project was developed in **Google Colab**. The dataset is not included directly in this repository due to the size of the images.

To run the notebook:

1. Clone this repository or upload the final notebook in Google Colab.

2. Create a folder in Google Drive using the following structure:

```text
MyDrive/
  PokerCardClassification/
    INPUT_DATASET/
      class_1/
      class_2/
      ...
```

The INPUT_DATASET folder can be accessed through the following link:

https://drive.google.com/drive/folders/1E7JMPggN6xA4cX9pXNVYd0WJR4ZT4VnH?usp=sharing

3. Verify that the path in the notebook is:

```python
BASE_DIR = Path("/content/drive/MyDrive/PokerCardClassification")
INPUT_DATASET = BASE_DIR / "INPUT_DATASET"
CARDS_DATASET = BASE_DIR / "CARDS_DATASET"
```

4. Run the cells in order.

**Note:**

The notebook will automatically generate the CARDS_DATASET folder with the following structure:

```text
CARDS_DATASET/
  train/
  validation/
  test/
```

If you experience long epoch times during training because the images are being loaded directly from Google Drive, you can upload or extract the CARDS_DATASET folder into Google Colab’s local runtime environment.

After uploading or extracting the dataset locally, you can set:

```python
LOCAL_DATASET = Path("/content/CARDS_DATASET")
```

Then use this local path instead of the Google Drive path when defining the dataset directories:

```python
train_dir = LOCAL_DATASET / "train"
validation_dir = LOCAL_DATASET / "validation"
test_dir = LOCAL_DATASET / "test"
```

## Acknowledgment of AI Use

During the development of this project, artificial intelligence was used as a support tool for the following tasks:

- Support in structuring the dataset splitting code.
- Evaluation of the code and identification of good practices, such as cleaning the output folder before copying files, using a fixed random seed for reproducibility, and organizing Keras callbacks.
- Clarification of questions about Python libraries such as `pathlib`, `shutil`, `random`, `pandas`, and TensorFlow/Keras
- Assistance in refining, grammar-checking, and translating technical documentation.

AI was used as a support and guidance tool during the development of the project. However, the final decisions were made based on the criteria covered in class, dataset analysis, and computer vision principles, including the use of 118 images per class, the dataset split, the balancing method, the dropout rate, and the layers selected for fine-tuning.
