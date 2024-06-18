The objective is to develop classifiers for music genre classification using PyTorch. The dataset includes audio samples for 10 different music genres, and each audio sample has a visual representation constructed using MEL spectrograms.
This will involve creating:

1. A Convolutional Neural Network (CNN) using spectrograms as input:
Data augmentation was implemented to improve the models ability to generalise inputs. Aside from the specified resizing of images, transformations such as image flips, rotations, and colour changes were imple- mented. While regularisation techniques such as Dropout layers and Early Stopping was also trailed using the validation sets, they decreased performance. This may be due to the specified networks not being complex enough to benefit from this type of regularisation. Across Net2, Net3, and Net4, kernel size of 3 was used, with most layers using 128- 256 channels.This model includes variations of networks of differing complexity. The best model (Net3) achieved an accuracy of 77%.

2. A Recurrent Neural Network (RNN) with Long Short-Term Memory (LSTM) units using audio as input:
The library ‘li- brosa’ was used for most pre-processing steps. Feature extraction was implemented using Mel-Frequency Cepstral Coefficients (MFCCs). This is a common method of feature extraction for audio processing - only the most useful characteristics of the audio will be carried forward, while also reducing the feature space. These extracted features were written to a dictionary, then exported into a JSON file, then reloaded as needed. The RNN model was created with the LSTM layer fed 3 layers, and one linear layer. This simple model worked best. Adam and Cross Entropy Loss was used for the optimiser and loss function respectively, with a learning rate of 0.0001 through out all training. 
This model acheived an accuracy of 82%.
