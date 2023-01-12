# Speech-emotion-recognition
Since its inception, speech emotion recognition has developed into a crucial part of Human-Computer 
Interaction (HCI). Instead of using conventional devices as input to comprehend vocal information and making 
it simple for human listeners to respond, these systems strive to facilitate the natural interaction between 
humans and machines through direct voice contact. Dialogue systems for spoken languages are used in a 
variety of applications, including call centre discussions, onboard car driving systems, and the use of emotion 
patterns from speech in medical settings. However, there are still a lot of issues with HCI systems that need 
to be fixed, especially as these systems transition from lab testing to real-world implementation. Therefore, 
efforts are needed to properly address these issues and improve machine recognition of emotions. 
Determining the emotional state of humans is an idiosyncratic task and may be used as a standard for any 
emotion recognition model . A discrete emotional approach is regarded as one of the fundamental approaches 
among the many models used for categorising various emotions. It makes use of a range of emotions, including 
grief, boredom, neutrality, surprise, disgust, and fury. 
The feature extraction and features classification phases make up the majority of the speech emotion 
recognition (SER) technique. Feature classification using linear and non-linear classifiers is part of the second 
step. The Maximum Likelihood Principle (MLP) and Support Vector Machine are the most widely used linear 
classifiers for emotion recognition (SVM). The speech signal is typically regarded as non-stationary. As a 
result, it is believed that SER benefits from non-linear classifiers. Many non-linear classifiers, including as 
the Gaussian Mixture Model (GMM) and Hidden Markov Model (HMM), are available for SER. For accurate 
emotion recognition from speech, energy-based features like Mel-Frequency Cepstrum Coefficients (MFCC) 
are frequently employed. For emotion recognition, other classifiers such as K-Nearest Neighbor (KNN), 
Principal Component Analysis (PCA), and Decision Trees are also used. 
The three core elements of emotion detection systems based on digitised speech are signal preprocessing, 
feature extraction, and classification. To establish evaluation purposes of the signal, acoustic preprocessing 
techniques like denoising and segmentation are used. To find the pertinent features present in the signal, 
feature extraction is used. Finally, classifiers perform the mapping of extracted feature feature vector to 
relevant emotions. Speech signal processing, feature extraction, and classification are all covered in-depth in 
this section. Due to their importance to the subject, the distinctions between spontaneous and performed 
speech are also examined.
In the first stage of speech-based signal processing, speech enhancement is carried out where the noisy 
components are removed. The second stage involves two parts, feature extraction, and feature selection. The 
required features are extracted from the preprocessed speech signal and the selection is made from the 
7 extracted features. Such feature extraction and selection is usually based on the analysis of speech signals in 
the time and frequency domains. During the third stage, various classifiers such as GMM and HMM, etc. are 
utilized for classification of these features. Lastly, based on feature classification different emotions are 
recognized. 
A. Enhancement of Speech Input Data in SER 
The input data gathered for emotion recognition is frequently tainted by noise when it is being captured. The 
feature extraction and classification lose accuracy as a result of these flaws. This means that in order for 
emotion detection and recognition systems to function properly, the input data must be enhanced. The speaker 
and recording variation are removed during this preprocessing stage, while the emotional discrimination is 
retained. 
B. Selection and Extraction of Features in SER 
Segments are used to describe the enhanced speech signal as meaningful units. Based on the information 
gathered, pertinent traits are extracted and divided into several groups. Short-term classification, which is 
based on characteristics like energy, formants, and pitch, is one type of classification. The other is known as 
long term classification; mean and standard deviation are two of the often-used long term features. Among 
prosodic features, the intensity, pitch, rate of spoken words and variance are usually important to identify 
various types of emotions from the input speech signal.
C. Measures for Acoustics in SER 
Every feature of language and its variations encodes the availability of emotional information. Among the 
most studied cases in this area are the vocal parameters and how they relate to emotion identification. Many 
times, factors like voice quality, pitch, intensity, and rate of speech are taken into account. The assumption 
that emotions are separate categories with independent existence is a common one in the simple view of 
emotion. Some of these discrete emotions, as shown in Table for a subset of emotions, have rather obvious 
connections with acoustic characteristics. Pitch and intensity are frequently connected with activation, 
meaning that the intensity value rises with high pitch and falls with low pitch. Factors that affect the mapping 
from acoustic variables to emotion include whether the speaker is acting, there are high speaker variations, 
and the mood or personality of the individual. 
D. Classification of Features in SER 
Numerous classifiers have been researched in the literature in order to create systems like SER, speech 
recognition, and speaker verification, to name a few. On the other hand, the reasons for selecting a specific 
classifier for a given speech task are frequently left out of most applications. Typically, one of these two rules 
of thumb is used to choose classifiers. 
Ordinarily, the two primary types of pattern recognition classifiers used for SER can be broadly divided into 
linear classifiers and non-linear classifiers. The most common way that linear classifiers are evaluated is as an 
array called a feature vector. On the other hand, non-linear classifiers are used to characterise the objects in 
order to create a non-linear weighted combination of them.
Dataset Used: 
The Ryerson Audio-Visual Database of Emotional Speech and Song (RAVDESS) dataset the Toronto 
emotional speech set (TESS) dataset samples include: 
1440 speech files and 1012 Song files from RAVDESS. This dataset includes recordings of 24 professional 
actors (12 female, 12 male), vocalizing two lexically-matched statements in a neutral North American accent. 
Speech includes calm, happy, sad, angry, fearful, surprise, and disgust expressions, and song contains calm, 
happy, sad, angry, and fearful emotions. Each file was rated 10 times on emotional validity, intensity, and 
genuineness. Ratings were provided by 247 individuals who were characteristic of untrained adult research 
participants from North America. A further set of 72 participants provided test-retest data. High levels of 
emotional validity, interrater reliability, and test-retest intrarater reliability were reported. 
2800 files from TESS. A set of 200 target words were spoken in the carrier phrase "Say the word _____' by 
two actresses (aged 26 and 64 years) and recordings were made of the set portraying each of seven emotions 
(anger, disgust, fear, happiness, pleasant surprise, sadness, and neutral). There are 2800 stimuli in total. Two 
actresses were recruited from the Toronto area. Both actresses speak English as their first language, are 
university educated, and have musical training. Audiometric testing indicated that both actresses have 
thresholds within the normal range.
The classification model of emotion recognition here proposed is based on a deep learning strategy based on 
convolutional neural networks (CNN), Support Vector Machine (SVM) classifier, MLP Classifier. The key 
idea is considering the MFCC commonly referred to as the “spectrum of a spectrum”, as the only feature to 
train the model. 
The most common machine learning application treats the MFCC itself as an 'image' and becomes feature. 
The benefit of treating it as an image is that it provides more information, and gives one the ability to draw 
on transfer learning. This is certainly legit and yields good accuracy. However, research has also shown that 
statistics relating to MFCCs (or any other time or frequency domain) can carry good amount of information 
as well.
It has been established that the MFCC, a variant of the Mel-frequency cepstrum (MFC), is the state of the art 
for sound formalisation in automatic speech recognition tasks. The MFC coefficients have mostly been 
utilised as a result of their ability to compactly and vectorially depict the amplitude spectrum of the sound 
wave. To obtain statistically steady waves, the audio file is segmented into frames, often using a set window 
size. The "Mel" frequency scale is shrunk to equalise the amplitude spectrum. This procedure is carried out 
to empathise the frequency more meaningfully in order to recreate the wave as accurately as the human 
auditory system is capable of doing. Forty features have been retrieved for each audio file. Each audio 
recording was converted into a floating-point time series to create the functionality. The time series was then 
turned into an MFCC sequence. 
1. CNN (Convolution neural network) 
2. MLP(Multilayer perceptron) 
3. SVM (support vector machine) 
