This project was carried out as part of the "Data Mining and Machine Learning" course at Heriot-Watt University.


# Data_Mining_Portfolio

#### https://www.kaggle.com/andrewmvd/animal-faces

This dataset consists of 16130 images in 3 classes.

### Reasons for the choice of the dataset:
- An image dataset will teach me about the basics of image processing and will be very appropriate for convolutional neural networks at the end of the semester.
- This dataset consists of high definition (512*512) images that can be reduced if necessary, there are no error or issue with the data and there is a large number of images (16130 images in 3 classes).
- 3 classes are more interesting than 2 but it's not too overwhelming or ressource intensive and there is still a good number of images for each class.

### Visualization:
- printing a few random images from each class to get a general idea about the data
- printing the shapes and the number of image per class

### Preprocessing and normalization:
- checking for errors when loading the images
- converting the images into 3D arrays [color channel][height][width] with numpy.array()
- downscale the images arrays to a smaller resolution
- convert into 2D greyscale arrays by multiplying the RGB values by coefficients : I get 3D arrays [height][width]
- normalizing by dividing all values by 255 to get values between 0 and 1
- convert the 2D greyscale arrays into 1D arrays
- Put all the 1D arrays into a .csv file with each pixel as a column and each pixel as a row

### Naive Bayesian classification:
- Create training and testing datasets
- Apply multinomial, binomial and gaussian classifiers

### General feature correlation:
- Apply an absolute Pearson correlation on the whole dataset
- Plot the correlation values of each pixel as an image to understand which pixels are most relevant

### Run again a naive bayesian classifier on a smaller dataset of the most relevant features:
- Create a smaller dataset containing only the pixel with the higher general correlation values
- Apply multinomial, binomial and gaussian classifiers on this dataset
- Doing this results in a large drop in accuracy, with the 5 most relevant features there's a 20% drop in accuracy, and depending on the classifier almost all the images from a class can be entirely classified as a different class.
