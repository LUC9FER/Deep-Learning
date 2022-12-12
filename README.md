# Deep-Learning
This repository contains projects for deep learning developed in python. You will need Jupyter Notebook or Google Collab to run the code. 

## Classification of the projects as follows:

### Bird Classification <br>
* Before downloading you have to change the path from /content/CSC8637-Deep-Learning/Dataset to your folder's path in ! wget & ! unzip command <br>
* After downloading the dataset you have to change the path variable with your folder path where you downloaded the dataset. <br>
    : path -> Dataset -> train / test / valid 
* You can modify this variable path_2 with the path of the folder where you want to store the model check points. <br><br>
    : path_2 -> Model Checkpoint -> Model.h5 <br>
* To load the model you need to specify the path of the folder where you have stored the model in the path_3 variable <br>
    : path_3 -> Saved Model -> InceptionResNetV2.h5 <br>
* In this varaiable path_4 you need to mention the path of the image you want to do prediction on. <br>
    : path_4 -> Random Images -> Wood Duck.jpg <br>
    
### Natural Language Processing <br>
 * You will need Jupyter Notebook or Google Collab to run the code <br>
 * To use the file text you need to change this path Link = "/content/File.txt" with the path of your folder where you have stored the file text. <br>
 * Out_File = 'Sequences.txt' In this you have to give the path of the folder where you want to save the 'Sequences' of the tokens. <br>
 * F_Name = 'Sequences.txt' In this you have to give the path of the folder where you have saved the .txt file of the 'Sequences'. <br>
 * Model.save('Model.h5') Here the path will be of that folder where you want to save the model. dump(tokenizer, open('Tokenizer.pkl', 'wb')) and the tokenizer. <br>
 * textfile = 'Sequences.txt' This path will be same as the previous one where you stored 'Sequences.txt'. <br>
 * saved_model = load_model('/content/Model.h5') It will be the same path where you saved the model tokenizer = load(open('/content/tokenizer.pkl', 'rb')) along with      the tokenizer <br>
 
 ### Cycle GAN <br>
 * To download the human dataset before running this `! cp kaggle.json ~/.kaggle/` command you need to upload the kaggle.json file which will be submitted with the         project. <br>
 * /content/test1.zip' This is to unzip a subset part of dog vs cat which is 'test1'. This is an important path as all of the animal images are taken from this folder.    <br> 
 * Apart from the mentioned links, there are subste links that are crucial for this model to run. As per the project requirement we have to structure all the training    images in this manner: <br> 
  : dataset -> trainA -> Contains all the images of the animals <br>
               trainB -> Contains all the images of the human <br>
  : test -> testA -> Contains all the images of the animals  <br>
             testB -> Contains all the images of the human <br>
 * For doing data preperation you need to consider the above structure. <br>
 * For testing the model you have to follow the below mentioned structure to organize the data along with the trained weights: <br>
    : pytorch-CycleGAN-and-pix2pix -> checkpoints (create if it's not present) / maps_cyclegan -> upload the weights / test_latest -> contains the generated images 

    : test -> testA -> put the animal images for testing / testB -> put the human images for testing <br>
 * Apart from these structure you also have to update all of the source & target path with you folder's path. <br>

 * After making the mentioned changes you will be able to run this code. <br>
 
