## Bangla News Headlines Categorization Using Gated Recurrent Unit (GRU): Project Overview
- Created a tool that can categorizes the Bengali news headlines into six category (**`National, Politics, International, Sports, Amusement, IT`**) using deep recurrent neural network.
- A dataset of **`0.13 Million`** news headlines is created. In built chrome web scrapper used for scraping the news headlines from different Bengali online news portals such as **`Dainik Jugantor, Dainik Ittefaq, Dainik Kaler Kontho`** and so on.    
- **`Word embeeding`** feature represtations technique is used for extracting the semantic meaning of the words.
- A deep learning model has been built by using a **`bidirectional gated recurrent network`**.
- Finally, the model performance  evaluated using various evaluation measures such as **`confusion matrix, accuracy , precision, recall and f1-score`**.  

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
