# Deep-Learning
This repository contains projects for deep learning developed in python

. You will need Jupyter Notebook or Google Collab to run the code

## Bird Classification
. Before downloading you have to change the path from /content/CSC8637-Deep-Learning/Dataset to your folder's path in ! wget & ! unzip command
. After downloading the dataset you have to change the path variable with your folder path where you downloaded the dataset.
    : path -> Dataset -> train
                        test
                        valid
. You can modify this variable path_2 with the path of the folder where you want to store the model check points.
    : path_2 -> Model Checkpoint -> Model.h5
. To load the model you need to specify the path of the folder where you have stored the model in the path_3 variable
    : path_3 -> Saved Model -> InceptionResNetV2.h5
. In this varaiable path_4 you need to mention the path of the image you want to do prediction on.
    : path_4 -> Random Images -> Wood Duck.jpg 
    
## Natural Language Processing
 . You will need Jupyter Notebook or Google Collab to run the code
 . To use the file text you need to change this path Link = "/content/File.txt" with the path of your folder where you have stored the file text.
 . Out_File = 'Sequences.txt' In this you have to give the path of the folder where you want to save the 'Sequences' of the tokens.
 . F_Name = 'Sequences.txt' In this you have to give the path of the folder where you have saved the .txt file of the 'Sequences'.
 . Model.save('Model.h5') Here the path will be of that folder where you want to save the model. dump(tokenizer, open('Tokenizer.pkl', 'wb')) and the tokenizer.
 . textfile = 'Sequences.txt' This path will be same as the previous one where you stored 'Sequences.txt'.
 . saved_model = load_model('/content/Model.h5') It will be the same path where you saved the model tokenizer = load(open('/content/tokenizer.pkl', 'rb')) along with the tokenizer
 
 ## Cycle GAN
 . To download the human dataset before running this `! cp kaggle.json ~/.kaggle/` command you need to upload the kaggle.json file which will be submitted with the project.
 . '/content/archive.zip' Here you have to give the path of the folder where you want to unzio the standford dog dataset. '/content/archive.zip' this is for cat dataset, '/content/dogs-vs-cats.zip' this is for dog vs cat dataset and the last one '/content/pubfig-dataset-256x256-jpg.zip' is for the human images dataset. '/content/test1.zip' This is to unzip a subset part of dog vs cat which is 'test1'. This is an important path as all of the animal images are taken from this folder.
 . Apart from the mentioned links, there are subste links that are crucial for this model to run. As per the project requirement we have to structure all the training images in this manner:
  : dataset -> trainA -> Contains all the images of the animals 
               trainB -> Contains all the images of the human
  : test -> testA -> Contains all the images of the animals 
             testB -> Contains all the images of the human
 . For doing data preperation you need to consider the above structure.
 . For testing the model you have to follow the below mentioned structure to organize the data along with the trained weights:
    : pytorch-CycleGAN-and-pix2pix -> checkpoints (create if it's not present)
                                            |
                                  maps_cyclegan -> upload the weights
                                            |
                                  test_latest -> contains the generated images

    : test -> testA -> put the animal images for testing
          testB -> put the human images for testing
 . Apart from these structure you also have to update all of the source & target path with you folder's path.

 . After making the mentioned changes you will be able to run this code.
 
