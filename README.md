# ECNG 3020 – SPECIAL PROJECT
## Sentiment Analysis and Visualization/Video Generation Using Generative AI for Modern Music Genres

## Project Background and Results:

Musical artists continuously work hard to push the boundaries of musical creativity through experimentation with various sounds, genres, and visuals to better connect with their listeners and improve the success of their music. However, they face challenges in gauging the perceived sentiment of their music and developing the right visualizations that fully convey the sentiment of their songs. Recent advancements in the accessibility and capabilities of generative Artificial Intelligence (AI), Machine Learning (ML), and Deep Learning (DL) technologies provide a new perspective for solutions to these challenges. Leveraging these technologies can redefine the creative process for musicians and expand the insights they can attain from their music.

Sentiment analysis is the process of identifying the attitudes and opinions expressed in subjective material. Music Emotion Recognition (MER) can be considered a form of sentiment analysis in the music domain. MER aims to use audio features derived from music to extract emotional information by applying ML and DL techniques. The approach taken to derive emotional information is defined by verified musical emotional models and taxonomies used to map songs to emotions/sentiments.

The goal of this project was to develop a music sentiment analysis and visualization generation tool driven by generative AI and ML. This tool utilized a Support Vector Machine (SVM) ML model as the foundation for a sentiment analysis system that used extracted audio features to classify music into sentiment classes. AI technologies, GPT 3.5 turbo and DALL-E 3 were employed to generate prompts and images to visualize music based on the derived sentiment class. Modern music genres contain music that conveys a variety of sentiments and emotions. By using the developed sentiment classification system on a verified music genre dataset, a comparison of song sentiments was done, giving insight into sentiment trends within and between music genres.
 
The model achieved an accuracy of 65.4% and a macro F1 score of 65%. Analysis of the sentiment trends within modern music genres shows that Jazz, Blues, Country, Classical, and Reggae; HipHop and Metal; and Disco, Rock, and Pop have similar sentiment distributions. The survey results indicate that the intended sentiment is correctly perceived with an accuracy rate of
64.5% and the sentiment is conveyed well with an average conveyance score of 3.87 out of 5. These findings show that ML and generative AI tools can streamline the music creation process
by assisting artists to create music and visuals that better resonate with audiences. However further work is needed to improve the model performance and editing capabilities in visualization generation.

## File Descriptions
| File | Description |
| ------ | ------ |
|BottomHalf_Classifier_Model.pkl|SVM3 model for classification between Q3 and Q4|
|Feature_Extraction.ipynb|Feature extraction notebook using Librosa and Essentia|
|Feature_Selection.ipynb|Feature selection notebook using RFECV|
|Features_bottomhalf.csv|Feature data for SVM3|
|Features_bottomhalf_test.csv|Testing feature data for SVM3|
|Features_bottomhalf_train.csv|Training feature data for SVM3|
|Features_half.csv|Feature data for SVM1|
|Features_half_test.csv|Testing feature data for SVM1|
|Features_half_train.csv|Training feature data for SVM1|
|Features_tophalf.csv|Feature data for SVM2|
|Features_tophalf_test.csv|Testing feature data for SVM2|
|Features_tophalf_train.csv|Training feature data for SVM2|
|Half_Classifier_Model.pkl|SVM1 model for classification between Q1/Q2 and Q3/Q4|
|Model_Training.ipynb|Model Training notebook using GridSearchCV|
|Music_Sentiment_Analyzer.ipynb|Music sentiment and visualization generation tool notebook|
|SelectedHeaders.JSON|Selected features for each SVM|
|TopHalf_Classifier_Model.pkl|SVM2 model for classification between Q1 and Q2|

## Example 

Example is done using the follow song, Promenade IV by modest Modest Mussorgsky. The song starts slow and somber and gets more tense and abrasive towards the end
https://github.com/user-attachments/assets/a2ef5cd6-a271-48d5-88b0-2d335b2f5282
```
Chunk: 1 From 0:00:00 To 0:00:30

Music Sentiment: Q3-Depression
Emotions in this quadrant: Miserable, Depressed, Sad, Gloomy, Bored, Droopy, Tired, Sleepy

Chunk: 2 From 0:00:30 To 0:01:00

Music Sentiment: Q3-Depression
Emotions in this quadrant: Miserable, Depressed, Sad, Gloomy, Bored, Droopy, Tired, Sleepy

Chunk: 3 From 0:01:00 To 0:01:30

Music Sentiment: Q2-Anxiety
Emotions in this quadrant: Alarmed, Afraid, Angry, Tense, Distressed, Frustrated, Annoyed

Chunk: 4 From 0:01:30 To 0:01:54.965986

Music Sentiment: Q2-Anxiety
Emotions in this quadrant: Alarmed, Afraid, Angry, Tense, Distressed, Frustrated, Annoyed
```

