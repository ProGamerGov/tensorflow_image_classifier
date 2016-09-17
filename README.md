# Tensorflow Image Classifier

This is the code for 'Image Classifier in TensorFlow in 5 Min on [YouTube](https://youtu.be/QfNvhPx5Px8). Use this [CodeLab](https://codelabs.developers.google.com/codelabs/tensorflow-for-poets/?utm_campaign=chrome_series_machinelearning_063016&utm_source=gdev&utm_medium=yt-desc#0) by Google as a guide. Also this [tutorial](https://www.tensorflow.org/versions/r0.9/how_tos/image_retraining/index.html) is quite helpful.

##Requirements

* [docker](https://www.docker.com/products/docker-toolbox)

##Usage 

You just need to make a "classifier" directory with a directory "data" inside it with all your images
For example
```
 [any_path]/my_own_classifier/
 [any_path]/my_own_classifier/data
 [any_path]/my_own_classifier/data/car
 [any_path]/my_own_classifier/data/moto
 [any_path]/my_own_classifier/data/bus
```
 and then put your image on it. 
 This "classifier" directory will have your samples but also trained classifier after execution of "train.sh". 

##Train process
 
Just type
```
 ./train.sh [any_path]/my_own_classifier
``` 
And it will do anything for you !

##Guess process

Just type for a single guess
```
 ./guess.sh [any_path]/my_own_classifier /yourfile.jpg
```

To guess an entire directory
```
./guessDir.sh [any_path]/classifier [any_path]/srcDir [any_path]/destDir
```

## Example of result
```
# ./guess.sh /synced/tensor-lib/moto-classifier/ /synced/imagesToTest/moto21.jpg
moto (score = 0.88331)
car (score = 0.11669)
```

Use an absolute file path for classifier and images because the script dos not support relative path (volume mounting)

#The Challenge

Make your own classifier for scientists, then post a clone of this repo with your retrained model in it. (you can name it retrained_graph.pb and it will be around 80 MB. If it's too big for GitHub, upload it to DropBox and post the link to it in your README)

#Credits

Credit goes to [Xblaster](https://github.com/xblaster) for the majority of this code. I've merely created a wrapper. 

---

Models 1-4 were trained to guess which neural network art service an image was created with. Model 5 was trained on idenfiying two neural network art services, and a specific artist.


#1. Model 1 has an accuracy of between 70-80%. 

- Categories: Dreamscope, Prisma, Ostagram

- Model Download: https://drive.google.com/open?id=0B--sVcawvPKfMHY3UkpKVkxTUWc

#2. Model 2 has a Final test accuracy = 61.0%. 

- Categories: Deepart, Pikazo, Prisma, Dreamscopeapp, Ostagram

- Model Download: https://drive.google.com/open?id=0B--sVcawvPKfTkI0TFR6ZXRwbjQ

#3. Model 3 has a Final test accuracy = 90.2%. 

- Categories: Deepart, Ostagram

- Model Download: https://drive.google.com/open?id=0B--sVcawvPKfclB6T21jVlA4Tkk

#4. Model 4 has a Final test accuracy = 66.0%. 

- Categories: Deepart, Prisma, Pikazo, Ostagram
 
- Model Download: https://drive.google.com/open?id=0B--sVcawvPKfN2QtUkRQd1JpVGc

#5. Model 5 has a . 

- Categories: Deepart, Ostagram, Simon_Stalenhag 

- Model Download:


#Datasets:

- The Deepart category had 432 images for training.
- The Pikazo category had 144 images for training.
- The Prisma category had 128 image for training.
- The Dreamscopeapp category had 923 images for training.
- The Ostagram category had 401 images for training.
- The Simon Stålenhag category had 725 images for training.
