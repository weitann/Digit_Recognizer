# Digit Recognizer

This notebook uses 2D-CONV in Keras to predict digits on 28x28 pixels images.

## Neural Network and Data augmentation

The pixels are first normalized by dividing each pixel by 255.0 (maximum value of pixels), then a comparison between the accuracy with and without data augmentation is plotted.

**Without data augmentation**

Using a series of Conv2D, MaxPooling, Dropout and Dense layers, the neural network was run with 25 epochs to achieve the following plots. Accuracy maximizes at around 3 epochs and do not have significant improvement after.

![img1a](https://user-images.githubusercontent.com/42630569/52918627-120c3900-32ae-11e9-922d-db5685a3cbab.png)
![img1b](https://user-images.githubusercontent.com/42630569/52918628-13d5fc80-32ae-11e9-8310-459066ada52f.png)


**With data augmentation**

Next, using Keras ImageDataGenerator, image data with data augmentation was generated, like inducing random rotations with a defined angle range. Using 5 epochs, the following graphs are plotted.

![img2a](https://user-images.githubusercontent.com/42630569/52918717-0a00c900-32af-11e9-90cb-35523a49405b.png)
![img2b](https://user-images.githubusercontent.com/42630569/52918718-0a995f80-32af-11e9-89ab-4dedf5c05bba.png)

Since the loss can be further reduced, number of epochs was increased to 10.

![img3a](https://user-images.githubusercontent.com/42630569/52919079-4e8e6380-32b3-11e9-9fca-3ba513b2a4f4.png)
![img3b](https://user-images.githubusercontent.com/42630569/52919078-4e8e6380-32b3-11e9-8b00-747b70eae049.png)

Accuracy on validation set is approximately 97%.
