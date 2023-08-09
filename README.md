# Dog-Classifier
# Description
Main goal of this project is to classifiy dog along with its bread. The model can be provided with variety of images such as images of animals form any kind 
and bread also images of objects or any other kind of images. the model can be easily identify ig the image is contain a dog or not .


# Getting Started
## 1- Put the image that you want to classify in the directroy ` uploaded_images'

## 2- CLI options:
```
python check_images.py --dir uploaded_images/ --arch resnet  --dogfile dognames.txt
python check_images.py --dir uploaded_images/ --arch alexnet --dogfile dognames.txt 
python check_images.py --dir uploaded_images/ --arch vgg  --dogfile dognames.txt
```
### Details about options
**check_images.py:** The file that contains the code for checking and classify the uploaded images.<br/>
**--dir uploaded_images:** Refer to the file that contains the images that are intended to be classified.<br/>
**--arch resnet:** Here we can choose what a pretrained model to use for classification.
**--dogfile dognames.txt:** this file is used as a reference for identify the bread of dogs.<br/>

## Sample of output

```
Pet Image Label Dictionary has 4 key-value pairs.
Below are 4 of them:
 1 key:    Pembroke_Welsh_Corgi_01.jpg  label:       pembroke welsh corgi
 2 key:                     cat_01.jpg  label:                        cat
 3 key:    Pembroke_Welsh_Corgi_02.jpg  label:       pembroke welsh corgi
 4 key:                football_01.jpg  label:                   football

     MATCH:

   Pembroke_Welsh_Corgi_01.jpg: 
Real:       pembroke welsh corgi   Classifier: pembroke, pembroke welsh corgi, corgi

   Pembroke_Welsh_Corgi_02.jpg: 
Real:       pembroke welsh corgi   Classifier: pembroke, pembroke welsh corgi, corgi

 NOT A MATCH:

                    cat_01.jpg: 
Real:                        cat   Classifier: snow leopard, ounce, panthera uncia

               football_01.jpg: 
Real:                   football   Classifier:                    soccer ball

# Total Images 4 # Matches: 2 # NOT Matches: 2

     MATCH:

   Pembroke_Welsh_Corgi_01.jpg: 
Real:       pembroke welsh corgi   Classifier: pembroke, pembroke welsh corgi, corgi  
PetLabelDog: 1  ClassLabelDog: 1

   Pembroke_Welsh_Corgi_02.jpg: 
Real:       pembroke welsh corgi   Classifier: pembroke, pembroke welsh corgi, corgi  
PetLabelDog: 1  ClassLabelDog: 1

 NOT A MATCH:

                    cat_01.jpg: 
Real:                        cat   Classifier: snow leopard, ounce, panthera uncia  
PetLabelDog: 0  ClassLabelDog: 0

               football_01.jpg: 
Real:                   football   Classifier:                    soccer ball  
PetLabelDog: 0  ClassLabelDog: 0

# Total Images 4 # Matches: 2 # NOT Matches: 2

 ** Statistics from calculates_results_stats() function:
N Images:  4  N Dog Images:  2  N NotDog Images:  2 
Pct Corr dog: 100.0 Pct Corr NOTdog: 100.0  Pct Corr Breed: 100.0

 ** Check Statistics - calculated from this function as a check:
N Images:  4  N Dog Images:  2  N NotDog Images:  2 
Pct Corr dog: 100.0 Pct Corr NOTdog: 100.0  Pct Corr Breed: 100.0


*** Results Summary for CNN Model Architecture VGG ***
N Images            :   4
N Dog Images        :   2
N Not-Dog Images    :   2
pct_match:  50.0
pct_correct_dogs:  100.0
pct_correct_notdogs:  100.0
pct_correct_breed:  100.0

Total Elapsed Time: 00 : 00 : 09
```

## Important Note :
**in each file in the model there is a thorough explaination about each steps, you're recommeded to read each of them carefully 
before you go through the code**

## License
Distributed under the MIT License. See `LICENSE.txt` for more information.



