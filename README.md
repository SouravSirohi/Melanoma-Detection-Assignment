# Project Name
Melanoma Detection Problem

To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.


## Table of Contents
* [General Info](#general-information)
* [Technologies Used]Python
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
- What is the background of your project?
	- Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.
- What is the business problem that your project is trying to solve?
	- The business problem that we are trying to solve here is to detect the melanoma cancer so that the patients can be given the right treatment at the right time
- What is the dataset that is being used?
	- - The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.

## Dataset

The dataset consists of 2,357 images, each depicting different types of skin cancer. These images are grouped into 9 categories within both training and testing sets. Each folder corresponds to one of the 9 distinct skin cancer types.

## Model

The model employed is a Convolutional Neural Network (CNN) specifically crafted to detect melanoma with a high degree of accuracy.

## Model Architecture

The CNN is structured as follows:
- A **Rescaling layer** for normalizing pixel values to a range between 0 and 1.
- Two **Conv2D layers**, each with 32 filters, a kernel size of 5, 'Same' padding, and 'relu' activation.
- A **MaxPool2D layer** with a pooling size of (2,2).
- Another **Conv2D layer** with 64 filters, kernel size of 5, 'Same' padding, and 'relu' activation.
- A second **MaxPool2D layer** with a pool size of (2,2).
- Another **Conv2D layer** with 64 filters, kernel size of 5, 'Same' padding, and 'relu' activation.
- A final **MaxPool2D layer** with a pool size of (2,2).
- A **Dropout layer** with a 0.25 dropout rate to prevent overfitting.
- A **Flatten layer** to convert the 2D matrix into a vector.
- A **Dense layer** with 9 units and a 'softmax' activation for classification.

## Model Compilation

The model is compiled with the following configuration:
- **Optimizer**: Adam
- **Loss Function**: Sparse Categorical Crossentropy
- **Evaluation Metric**: Accuracy

## Model Training

The model is trained with these parameters:
- **Batch Size**: 32
- **Image Resolution**: 180x180 pixels
- **Number of Epochs**: 50

## Model Evaluation

For evaluation, the model's performance is measured on the validation set using:
- **Accuracy**
- **Loss**
## Analyzing Results

The model shows signs of overfitting. Adding more layers, increasing the number of neurons, or incorporating additional dropout layers may help address this. Further hyperparameter tuning could also improve performance.

## Class Rebalance

To address class imbalance, the Augmentor library is used to generate additional images across the classes, ensuring a more balanced dataset.

## Visualizing Class Rebalance

Matplotlib is used to visualize the impact of the class rebalancing process.

## Analyzing Class Rebalance

After applying the Augmentor library, the model's accuracy on the training data improved, indicating a better representation across classes.

## Conclusion

This CNN model represents a strong foundation for detecting skin cancer. Nonetheless, overfitting needs to be managed, and further optimization could lead to better overall performance.


## Contact
Created by [@SouravSirohi] - feel free to contact me!


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->
