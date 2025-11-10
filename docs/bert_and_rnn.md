---
title: BERT and RNN models
layout: default
filename: bert_and_rnn
--- 

## Steps to Take for this Section
First go to the Environment directory and perform `conda env create -f general_env.yml` and `activate general_env` to create the environment needed for this section of the project. Then proceed to the Cleaning directory and run the specialty_data_preprocessing.ipynb notebook in its entirety to populate the Data directory with all of the data required. Then proceed to the Specialty-Models directory. First focus on the bert.ipynb, file to create the BERT models of your choosing, you can quickly change MODEL to the other BERT models I trained in my documentation if you are interested in seeing the varying results for yourself. The bert_metrics.ipynb notebook will show the confusion matrix for the model of your choosing, currently it is my absolute path, but change it to your absolute path to where ever the final_model directory is located in your saved model. Then in test-bert.ipynb, you can change the absolute path to the same final_model again and then test the model with any transcript of your choosing in the bottom cell. This concludes everything required to work with the BERT models, and now I will dive into how to create the RNN models.

Go to the Environment directory and perform `conda env create -f rnn_env.yml` and `activate rnn_env` to create the environment needed for the rnn models. If you had not done this already, proceed to the Cleaning directory and run the specialty_data_preprocessing.ipynb notebook in its entirety to populate the Data directory with all of the data required. Then proceed to the Specialty-Models directory. Use the rnn.ipynb notebook to create two distinct RNN models that you can test and interact with. Then in test-rnn.ipynb, you can change the relative path to the RNN of your choosing and then test the model with any transcript of interest in the bottom cell. This concludes everything required to work with the RNN models.

## Writeup

For this dataset, it began with me inspecting, encoding, and feature engineering the data to be best interpreted by the models I planned to create within the specialty_data_preprocessing.ipynb notebooks.

<ins> Data Preprocessing Results </ins>

Within the dataset, I found some nulls which led to me dropping those entries. I then cleaned a redundant column in the dataset and inspected the dataset. It was imbalanced where the most common column dwarfed every other category, I decided to remove the category from contention and considered the columns after. I then had to decide how many categories to classify, there were 40 categories in total, I decided to see how models would perform with 10, 5, and 3 categories. By the end of my development, the 10 categories reached 60% accuracy, the 5 and 3 categories reached 80% accuracy. I believe they reached these results due to a lack of overall data, but i wanted to see where I could take the challenge despite only have approximately 1,000 text entries. I then encoded each category to labels for the model to determine what category a transcript belongs in.

Then in Figure 1, I realized that the majority of the transcripts were over 512 tokens outside of the bounds of traditional BERT models so I created a new transcript_summarized entry where I truncate the transcript from the start to the end to potentially improve accuracy in the future. I also calculated the weights of each category since there was a small imbalance and I thought that could help improve my models as well. I then stored all the data in the Data directory.

<figure style="text-align: center;">
  <img src="images/tokens_per_transcript.png" alt="Tokens per Transcript">
  <figcaption>Figure 1: Tokens per Transcripts</figcaption>
</figure>

<ins> BERT Models </ins>

After cleaning I began with a baseline leveraging distilbert-base-uncased to view how a basic BERT model will handle the data. This model helped me recognize that the performance was diminished by the very long texts and the imbalance of features that I discussed during the preprocessing. I then proceeded to looking for more specialized BERT models that would allow me to improve my accuracy and F1 score further. I settled on two models focused on biomedical data, that being emilyalsentzer/Bio_ClinicalBERT which I could reach a F1 score of 70.2% with and microsoft/BiomedNLP-PubMedBERT-base-uncased-abstract-fulltext which I could reach a marginally higher F1 score of 73.6%. I wanted to pushed thee model even further which led to me creating a modified Trainer to punish the model for misclassifying the smaller classes. Using Microsoft's PubMedBERT allowed me to reach a final F1 score of 75.5%. I wanted to squeeze out performance to an even higher 80-90% range, however, I believe this is not feasible due to the lack of data to train the models on as well as a lack of time to fine tune the model even further. I wanted to see how pretrained BERT models could compete against an RNN made from scratch to see what the comparative difference could be.

<ins> RNNs </ins>

I built 3 different RNNs, a simple RNN, a more advanced RNN, and a RNN with a pretraineed embedding layer. For the simple RNN I could achieve a respectable F1 score of 70%, but the model was much more overfit. Then the more advanced RNN dropped in performance achieving a F1 score of 61%, and the pretrained RNN achieved a close F1 score of 69%. I believe this again is due to a lack of data not allowing the model to train on enough information to go beyond 70%. The results were expected, but it is interesting exploring how a pretrained BERT model performed against a RNN built from scratch especially since the F1 score was not significantyl different between the best respective models.

There is some interesting conversations to be had about the difference and results of these models, but time constraints prevent me from diving deeper in this writeup.

These models can be recreated and tested with the above instructions, but overall I am happy with the results that I could achieve on such a challenging dataset.