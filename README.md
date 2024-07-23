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

Example is done using a roughly 2 minute song that starts slow and somber and gets more tense and abrasive towards the end


The audio file is split into 30 second chunks. Each chunk is classified into one of four emotion classes (Exuberance, Anxiety, Depression or Contentment)

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

For each chunk a subject and style is selected
Chunk 1 - Earth, abstract style
Chunk 2 - Moon, abstract style
Chunk 3 - Stars, abstract style
Chunk 4 - Galaxy, abstract style

GPT then develops prompts for images based on the subject, style and emotion in each chunk
Chunk 1 Image Prompt:  Earth depicted in an abstract style, depressed color palette, desolate landscapes, gloomy atmosphere, tired planet, droopy shapes and forms
Chunk 2 Image Prompt:  The moon in an abstract style, distorted shapes, dark hues, a sense of loneliness, somber atmosphere, melancholic aura
Chunk 3 Image Prompt:  Stars depicted in an abstract style, chaotic constellation patterns, a sense of unease, swirling shapes and lines, an atmosphere of tension and restlessness, distorted and fragmented imagery, a feeling of disarray and disquiet
Chunk 4 Image Prompt:  A galaxy in an abstract style, swirling and chaotic, colors blending in frenzy, vastness that overwhelms, a sense of unease and tension, a turbulent and turbulent atmosphere.

AI visualizations are generated depecting the selecteed subject and style 

 Chunk 1
 
![c1](https://github.com/user-attachments/assets/46446780-74be-4eb5-be97-564a9c2c43a4)

 Chunk 2
 
![c2](https://github.com/user-attachments/assets/2d2fbf98-eb10-484c-888b-bf379b88ff79)

 Chunk 3
 
![c3](https://github.com/user-attachments/assets/5ae41843-4157-4601-ada9-9a490a42af55)

 Chunk 4
 
![c4](https://github.com/user-attachments/assets/4e9939c6-2500-4fb4-9762-809bec893b0a)

