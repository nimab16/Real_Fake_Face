# Real_Fake_Face
## 1 Introduction
The task is regarding to Real VS Fake faces that is called Facial anti-spoofing.Facial anti-spoofingis the task
of preventing false facial verification by using a photo, video, mask or a different substitute for an authorized
person’s face. The goal is to train a model that can detect the face is real or fake. For this task I used Real
and Fake Face Detection that is exist in kaggle website. I splited the data to train and validation part
(80 percent train and 20 percent validation). In addition, I used pre-trained MobileNetV2 and by using the
transfer learning and changing a bit the top layer I created my model. The reason that I used this pre-trained
model to transfer learning is that, I know you are making the application for mobile and the MobileNetV2 is
a model that is nuilt to use in mobile phone because it allows to significantly reduce the memory footprint
needed during inference by never fully materializing large intermediate tensors.Also, I used Fine tuning part
to improve the accuracy of model. In addition, there is an Augmentation to increase the number of train
images to overcome to the Overfit. Also, I test this dataset on VGGFace model to see the difference with
MobileNetV2.
2 Materials and Methods
2.1 Software and Libraries
I use the Google Colab to run the code and the libraries that are used for this task are:
tensorflow, keras, cv2, numpy, matplotlib
2.2 Database
For the machine learning task the most important part is regarding to the database. In first attempt, I tried to
access to the REPLAY-ATTACK database that the link was exist to the Pdf file. It seems that this database
is a suitable option to train data with 1300 video clips of photo and video attack attempts to 50 clients. However,
I could not access to this dataset because it needs an enrolment and waiting for access.
Therefore, I used the Real and Fake Face Detection in the Kaggle website. This dataset has 2041 images
for real and fake face images. However, for this task this number of images is not enough and we can see the
effect of that in result part. I separated this dataset to 80 percent training (1633 images) with two classes(real
and fake) and 20 percent for validation (408 images).
2.3 Pre-trained Models (Transfer learning)
I used the MobileNetV2 as a main part of my test. This model is for mobile and resource constrained
environments. As I know that you are working on mobile application I know the importance of resources. In
addition, based on my previous experiences as a mobile developer I know the limitation of process and the
variety of devices.
The other model that I used for transfer learning is VggFace. VggFace is one of the model that is trained
for face recognition and I thought that it is possible that this model also be capable for this test.
The last model I checked was based on Multi neural network . It has two CNN that train based on
YCbCr and ’Luv’ color images. These two model concatenate at the end and we will have a full model.
