# Transfer Learning 

A pre-trained model is a saved network that was previously trained on a large dataset, typically on a large-scale image-classification task. You either use the pre-trained model as is or use transfer learning to customize this model to a given task. The intuition behind transfer learning for image classification is that if a model is trained on a large and general enough dataset, this model will effectively serve as a generic model of the visual world. You can then take advantage of these learned feature maps without having to start from scratch by training a large model on a large dataset.

In this Lab, you will try two ways to customize a pre-trained model:

1. **Feature Extraction**: Use the representations learned by a previous network to extract meaningful features from new samples. You simply add a new classifier, which will be trained from scratch, on top of the pre-trained model so that you can repurpose the feature maps learned previously for the dataset. You do not need to (re)train the entire model. The base convolutional network already contains features that are generically useful for classifying pictures. However, the final, classification part of the pre-trained model is specific to the original classification task, and subsequently specific to the set of classes on which the model was trained. Please read [Example 1: Transfer Learning as Feature Extractor](https://github.com/sagihaider/CE888_2021/blob/main/Lab_8/transfer_learning_FE.ipynb)

2. **Fine-Tuning**: Unfreeze a few of the top layers of a frozen model base and jointly train both the newly-added classifier layers and the last layers of the base model. This allows us to "fine-tune" the higher-order feature representations in the base model in order to make them more relevant for the specific task. Please read [Example 2: Transfer Learning as Fine-Tuning](https://github.com/sagihaider/CE888_2021/blob/main/Lab_8/transfer_learning_FT.ipynb)

**Note**: We will be using [VGG-16](https://www.tensorflow.org/api_docs/python/tf/keras/applications/VGG16) pre-trained model in our lab work for both feature extraction and fine-tuning. 

## Task: 

In your Lab_8 folder, we have stored data under <data.zip> file. This is an image dataset with 4 classes (i.e. cats, dogs, humans, horses). Please implement both Feature Extractor and Fine-Tuning methods on data.zip. Please ignore use VG166 and you are free to use any other pre-trained models https://keras.io/api/applications/

Good luck! 
