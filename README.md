## Bangla News Headlines Categorization Using Gated Recurrent Unit (GRU): Project Overview
- Created a tool that can categorizes the Bengali news headlines into six category (**`National, Politics, International, Sports, Amusement, IT`**) using deep recurrent neural network.
- A dataset of **`0.13 Million`** news headlines is created. In built chrome web scrapper used for scraping the news headlines from different Bengali online news portals such as **`Dainik Jugantor, Dainik Ittefaq, Dainik Kaler Kontho`** and so on.    
- **`Word embeeding`** feature represtations technique is used for extracting the semantic meaning of the words.
- A deep learning model has been built by using a **`bidirectional gated recurrent network`**.
- Finally, the model performance is evaluated using various evaluation measures such as **`confusion matrix, accuracy , precision, recall and f1-score`**.  

## Resources Used
- **Developement Envioronment :** Google Colab
- **Python Version :** 3.7
- **Framework and Packages :** Tensorflow, Scikit-Learn, Pandas, Numpy, Matplotlib, Seaborn
- **Scrapper :** [Chrome Web Scrapper](https://chrome.google.com/webstore/detail/web-scraper-free-web-scra/jnhgnonknehpejjnehehllkliplmbmhn?hl=en)

## Project Outline 
- Data Collection and Cleaning
- Data Summary
- Data Preparation for Model Building
- Model Development
- Model Evaluation


## Data Collection and Cleaning
Data is collected by creating a scraping graph using chrome web scarpper. Around `0.13 Million` Bengali news headlines of six categries are scrapped from different online news portals. The news portals are **`Dainik Jugantor, Dainik Ittefaq, Dainik Kaler Kontho`** and so on. The headlines distribution of each categories represents in the following figure. This dataset is an imbalanced dataset. 

![](/images/data_distribution.PNG)

As the headlines are small in length it is not mandatory to remove the stopwords from the headlines. After cleaning the sample data would look like this.

![Sample Data](/images/data_sample.PNG)

## Data Summary 

Data summary includes the information about number of documents, words and unique words have in each category class. Also, include the length distribution of the headlines in the dataset.

| ![national](/images/national.PNG) | ![international](/images/international.PNG) | ![politics](/images/politics.PNG) | ![sports](/images/sports.PNG) |![amusement](/images/amusement.PNG) |![it](/images/it.PNG) |

![length distribution](/images/len_dist.PNG)

**From this graphical information we can select the suitable  length of headlines that we have to use for making every headlines into a same length.**


## Data Preparation for Model Building

The text data are represented by a encoded sequence where the sequences are the vector of index number of the contains words in each headlines. The categories are also encoded into numeric values. After preparing the headlines and labels it looks as -
![ecoded_sequence](/images/padded.PNG)  ![labels](/images/encoded_labels.PNG)

For Model Evaluation the encoded headlines are splitted into **Train-Test-Validation Set**. The distribution has -

![split](/images/train_test_split.PNG)


## Model Development 

The used model architecture consists of a **embedding layer(`input_length = 21, embedding_dim = 64`), GRU layer(`n_units = 64`), two dense layer (`n_units = 24, 6`), a dropout  and a softmax layer**. The Architecture looks like- 

![model](/images/model_architecture.PNG)

## Model Evaluation 

In this simple model we have got **`81%`** validation accuracy which is not bad for such an multiclass imbalanced dataset. Besides Confusion Matrix and other evaluation measures have been taken to determine the effectiveness of the developed model. From the confusion matrix it is observed that the maximum number of misclassified headlines are fall in the caltegory of **`Natinal, International and Politics `** and it makes sense because this categories headlines are kind of similar in words. The accuracy, precision, recall and f1-score result also demonstrate this issue. 

![confusion](/images/confusion.PNG)

![performance](/images/performance.PNG)

**In conclusion, we have achieved a good accuracy of `84%` on this simple recurrent neural network for Bengali news headline categorization task. This accuray can be further improved by doing hyperparameter tunning and by employing more shophisticated network architecture with a large dataset.**



