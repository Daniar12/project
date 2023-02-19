












Project Report
Made by: Nukushev Daniar
Course instructor: Yeleu Sultanmurat






























Introduction:

	Problem:
	The main objective of this project is to add colors to the black and white photo’s thus creating the colorized versions of them using machine learning. And the goal is to train a machine learning model that can effectively use given dataset of black and white photos as input and output colorized versions.
	
	Literature review with links:
	Using autoencoders and transfer learning
https://becominghuman.ai/auto-colorization-of-black-and-white-images-using-machine-learning-auto-encoders-technique-a213b47f7339
	Black and white image colorization with OpenCV and Deep Learning
https://www.geeksforgeeks.org/black-and-white-image-colorization-with-opencv-and-deep-learning/ 
	Image colorization with U-Net and GAN tutorial(The version I used the most)
https://colab.research.google.com/github/moein-shariatnia/Deep-Learning/blob/main/Image%20Colorization%20Tutorial/Image%20Colorization%20with%20U-Net%20and%20GAN%20Tutorial.ipynb#scrollTo=03r38eU2Ezyt
	Current work:
	In this project I have developed a machine learning model that can take as input the image dataset and return the colorized version of images. The code was written and ran in the Google Colab notebook. The dataset was taken from the one of the links I wrote above.

Data and methods:
	Information about data:
	As you might know, the images consist of RGB color space red, green, and blue colors. But in the work that I’ve studied, most of the codes used the L*a*b color space. L*a*b color space consist of 3 channels, the first channel L encodes the Lightness of each pixel, the channels *a and *b encode green-red and yellow-blue, respectively. Here is an example:
 	Description of the ML models you used with some theory:
	In this project the main problem is to create the ML model that use black and white image and colorize them. And to do these two losses are used: L1 loss, which makes it a regression task, and adversarial (GAN) loss, which solves the problem of the unsupervised model (by assigning the outputs the number indicating how “real” they look). The L1 loss is preferred over L2 loss because it reduces the effect of producing gray-ish images. 
	Results:
	After testing and training the model here’s some images:
Epoch1
![epoch1](https://user-images.githubusercontent.com/98156588/219938554-7204f9fa-04ee-45c6-9c19-9295f9cdcf16.png)
![epoch1 1](https://user-images.githubusercontent.com/98156588/219938559-f04dc5d7-3cfa-4a67-9165-2afa517ff3e5.png)
Epoch20
![epoch20](https://user-images.githubusercontent.com/98156588/219938568-cca6c559-37a5-46cd-bec0-910ea72bbf9d.png)
![epoch20 1](https://user-images.githubusercontent.com/98156588/219938572-10fa7a83-04d6-40d7-9326-5a18b4f2c116.png)
As you might have noticed, at the first epoch the colors look a lot blurrier and sometimes not fitting the image. But at the end in 20th epoch the images have less gray and more colors. The colors themselves look nice and fit the image as it is real colors. The results are quite promising.

	Discussion:
	Critical review of the results:
	The results are looking very good and doesn’t have much of the problems. The problem that I’ve noticed are times when the back of the chair is gray, but the actual color is brown. Some of the objects take the color from other objects near them, and that looks quite unfitting. Overall, to me the model can be viewed as success.
	Next steps:
	The model for sure can be improved and take less time or train more effectively, but the results of the model I used is quite promising and satisfying. Especially, since this project isn’t the scientific research.
