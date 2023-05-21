# Age Verification Model for Ensuring Compliance in Retail

## Computer Vision

Good Seed, a supermarket chain, wants to know if Data Science can help them comply with the law by ensuring they do not sell age-restricted products to underage customers. You've been asked to do the evaluation, so when you get to work, keep the following in mind:

- The stores are equipped with cameras in the checkout area that will display a signal when someone buys an age-restricted product
- Computer vision methods can be used to determine a person's age from photos
- The next task is to build and evaluate a model to verify a person's age

To start working on this task, you will get photos of people with their age captions.

## Conclusion

### 1. Data Preprocessing

- We have about 7.6k data or 7591 data in image format.


- We split the train and test data into a 75:25 ratio.

### 2. EDA

- Most images are in the age range of 10-50 years, while ages above 70 have a minimal number of images. It makes it difficult for the model to predict faces at an old age.

### 3. Modeling

- With ImageDataGenerator, in addition to homogenizing the different pixel sizes, this process is also helpful for reducing the image size to speed up the computation process.

- We used 5 layers in the model: ResNet, GlobalAveragePooling2D, Dropout, and Dense.

- The results achieved are very satisfying where our model has a very low **mae** (below 7), and most importantly, our model avoids overfitting. By setting the value of **epoch = 5**, we recorded a short training time and made the model computationally efficient.
