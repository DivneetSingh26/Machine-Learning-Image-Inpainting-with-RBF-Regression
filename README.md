# Machine-Learning-Image-Inpainting-with-RBF-Regression
- Using a machine learning algorithm with RBF Regression and trains the algorithm on the training data, then evaluates its performance on the test set, this algorithm model takes in a corrupted image with missing pixels or text overtop as an example and can remove the text and imperfections by blending, cropping image patches, reshaping the pixels values into vectors of the correct dimensions by inpainting (process of predicting the corrupted pixels).
- Figure 1 contains a visual example of what this algorithm does
![image](https://user-images.githubusercontent.com/35879872/109435913-e4087600-79ea-11eb-946f-25ee70e623bb.png)

Figure 1: From left to right: (a) The original image. (b) An image corrupted with red text. (c) A badly restored
image. (d) A well restored image.
- First this machine learning algorithm recognizes the image and converts it into a 2D array.
- It then models an image as a function I(x) that specifies brightness as a function of position with a value from 0 to 1 using radial basis functions.
- Then finds the grid spacing and the RBF width, and then finds the weights wk (including the bias) using regularized least squares regression on image patches similar to Figure 2.
![image](https://user-images.githubusercontent.com/35879872/109435838-73615980-79ea-11eb-882b-67ec8ec9cadc.png)

Figure 2: (left) An RBF model with all weight wk = 1. (middle) A model with 3 × 3 RBFs with LS regression
weights. (right) A model with 8 × 8 RBFs with LS regression weights.
-  Once it has the model, it uses it to evaluate and predict the image values at any pixel (eg. corrupted pixels), or in between two pixels to "correct" the image via inpainting.

