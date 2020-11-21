# Deep Learning Food Recognition Project
_There's nothing I wanted more than to write a ML model that detects different foods in an image._

## Motivation
Personal learning goal was to figure out how object recognition and detection works (high level understanding). I had experience using PyTorch and TensorFlow though courses I've taken in school, but I wanted to try a hands on project.

## Project Description
This Food Recognition Project is able to detect different foods on images by using a Faster R-CNN with a "testing accuracy" of 70.6% (more on this later).

There are **30** different food categories.

All images used in this project were retrieved from Google Open Images V6 (scraped using Python scraper). They were pre-labelled images, but I had to do some manual cleanup to delete irrelvant pictures (ex. the fruit apple is different than the company Apple). Images augmentation was performed using Numpy and Open CV. After cleaning and augmenting images, approximately 30000 images were used to train, 10000 were used in validation, and 10000 were used for testing.

## How I trained
I read a lot of Medium posts and consulted some friends to help me (s/o to Thomas and Alex). I also had to refresh Google Colab too many times in order to get a Tesla P100 since it was the only GPU with enough memory to allow me to train in a decent amount of time. 
 
## Results
After 5 days of training, I achieved a testing accuracy of 70.6%, which refers specifically to the accuracy of the model to detect a _single_ food item on the image (since images only had 1 food on them). However, since I wanted to do detection of _multiple_ foods, I did an eyeball on the accuracy (images below), in which case, the performance was _good enough_ for my standards 😎.

## Sample Images
### Sometimes it was good...
![Good Image 1](/readme-images/good1.png)

### Other times, it was pretty much correct?
![Good Image 2](/readme-images/good2.png)

### And, well, sometimes it got it completely wrong.
![Bad Image 1](/readme-images/bad1.png)