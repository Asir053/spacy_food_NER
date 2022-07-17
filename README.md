# spacy_food_NER

##Steps of building a Custom NER using spacy 3:

###Text Annotation:

The dataset is collected from this Bengali food blog:
https://www.bengalsaroma.com/category/blog/

Then annotation is done using this app:
https://tecoholic.github.io/ner-annotator/

Prepare and upload that input file.
Create text and annotate.
Export the Annotations as JSON file. 

There are total 30 sentences related to bengali food blogs
25 of them are for the training set and 5 for validation set (83-17 split)
Then annotating only with ‘food’ tags using the app.

###Training:
Importing spacy 3
Loading the spacy blank model (as we’re going to use spacy’s text classifier) and creating the docbin object
Converting the training and validation JSON files into .spacy (docbin) objects
Extracting config file using spacy config widget or the CLI 
```init config config.cfg``` 
Train using the config file after specifying training and validation file directory.
The last model and the best model are saved automatically. 

###Inference:
Test the best model using some custom sentences.
