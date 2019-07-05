# Dynamic-Lexicon-Generation-for-Natural-Scene-Images
### Introduction
Many scene text understanding methods approach the endto-end recognition problem from a word-spotting perspective and take
huge benefit from using small per-image lexicons. Such customized lexicons are normally assumed as given and their source is rarely discussed.
In this project we propose a method that generates contextualized lexicons for scene images using only visual information. For this, we exploit the correlation between visual and textual information in a dataset consisting of images and textual content associated with them. Using the topic modeling framework to discover a set of latent topics in such a
dataset allows us to re-rank a fixed dictionary in a way that prioritizes
the words that are more likely to appear in a given image. Moreover,
we train a CNN that is able to reproduce those word rankings but using
only the image raw pixels as input. We demonstrate that the quality
of the automatically obtained custom lexicons is superior to a generic
frequency-based baseline.

#### Here is the link for the presentation on prezi
https://prezi.com/view/vvklNORa4kEiHcX3lA5z/

## Results
![alt text](https://github.com/vishalbidawatka/Dynamic-Lexicon-Generation-for-Natural-Scene-Images/blob/master/smai_project_images/1.png)
![alt text](https://github.com/vishalbidawatka/Dynamic-Lexicon-Generation-for-Natural-Scene-Images/blob/master/smai_project_images/download.png)
![alt text](https://github.com/vishalbidawatka/Dynamic-Lexicon-Generation-for-Natural-Scene-Images/blob/master/smai_project_images/download%20(1).png)


Dependencies
-----
1. gensim library
2. keras 
3. pickle 

### Reference of ResearchPaper
https://github.com/vishalbidawatka/Dynamic-Lexicon-Generation-for-Natural-Scene-Images/blob/master/PGR2016.pdf

##### Firstly, we will suggest you to go through the research paper

How to Run
----
1. First you should download the dataset from MS-COCO site and links is given in data.txt
2. Change the path appropriately, and read the data.
3. First you have to run the LDA -> data.ipynb(Final LDA model), it will produce the two output file 
    *  first file have P(topic/document) in dictionary form   --> it will used as class label to train CNN model.
    *  second file have P(word/topic)    ---> with help of this, we will able to calculate the Probabilty (word/image).
4. CNN model ouput gives us the Probabilty(topic/image) just from the raw pixels without the textual information.



#### If you don't want to train the model
We have already dumped the model object , you can read the model object and run the code.







