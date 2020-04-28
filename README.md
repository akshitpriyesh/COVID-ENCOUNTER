# COVID-ENCOUNTER
The standard COVID-19 tests are called PCR (Polymerase chain reaction) tests which look for the existence of antibodies of a given infection. But there are a few issues with the test. Pathogenic laboratory testing is the diagnostic gold standard but it is time-consuming with significant false-negative results as mentioned in this paper.
Moreover, large scale implementation of the COVID-19 tests which are extremely expensive cannot be afforded by many of the developing & underdeveloped countries hence if we can have some parallel diagnosis/testing procedures using Artificial Intelligence & Machine Learning and leveraging the historical data, it will be extremely helpful. This can also help in the process to select the ones to be tested primarily.
Fast and accurate diagnostic methods are urgently needed to combat the disease. In a very recent paper ‘A deep learning algorithm using CT images to screen for Corona Virus Disease (COVID-19)’ published by Shuai Wang et. al they have used Deep Learning in extracting COVID-19’s graphical features from Computerized Tomography (CT) scans (images) in order to provide a clinical diagnosis ahead of the pathogenic test, thus saving critical time for disease control.
The study used transfer learning with an Inception Convolutional Neural Network (CNN) on 1,119 CT scans. The internal and external validation accuracy of the model was recorded at 89.5% and 79.3%, respectively.
In my experiment, I have performed a similar analysis but on Chest X-ray images and the major reason is that getting CXRs is more accessible for people than getting CT scans especially in rural and isolated areas. There will also be more potential data available.
Now let’s come to the dataset that has been used by me. So, Dr.Joseph Paul Cohen (Postdoctoral Fellow at the University of Montreal), recently open-sourced a database containing chest X-ray images of patients suffering from the COVID-19 disease. The dataset used is an open-source dataset which consists of COVID-19 images from publicly available research, as well as lung images with different pneumonia-causing diseases such as SARS, Streptococcus, and Pneumocystis.
So, the dataset consists of COVID-19 X-ray scan images and also the angle when the scan is taken. It turns out that the most frequently used view is the Posteroanterior view and I have considered the COVID-19 PA view X-ray scans for my analysis.
Recent research mostly from China, where the new coronavirus disease 2019 (COVID-19) outbreak originated, has cited the usefulness of chest CT in early disease diagnosis. CT protocols are now used for assessing pulmonary damage in COVID-19 patients. 

Results

There were 64 patients (26 men, mean age 56±19 years). Of these, 58, 44 and 38 patients had positive initial RT-PCR (91%, [CI: 81-96%]), abnormal baseline CXR (69%, [CI: 56-80%]) and positive initial RT-PCR with abnormal baseline CXR (59 [CI:46-71%]) respectively. Six patients (9%) showed CXR abnormalities before eventually testing positive on RT-PCR. Sensitivity of initial RT-PCR (91% [95% CI: 83-97%]) was higher than baseline CXR (69% [95% CI: 56-80%]) (p = 0.009). Radiographic (mean 6 ± 5 days) and virologic recovery (mean 8 ± 6 days) were not significantly different (p= 0.33). Consolidation was the most common finding (30/64, 47%), followed by GGO (21/64, 33%). CXR abnormalities had a peripheral (26/64, 41%) and lower zone distribution (32/64, 50%) with bilateral involvement (32/64, 50%). Pleural effusion was uncommon (2/64, 3%). The severity of CXR findings peaked at 10-12 days from the date of symptom onset.


Conclusion
Chest x-ray findings in COVID-19 patients frequently showed bilateral lower zone consolidation which peaked at 10-12 days from symptom onset.
Summary
Chest x-ray abnormalities in COVID-19 mirror those of CT, demonstrating bilateral peripheral consolidation. Chest x-ray findings have a lower sensitivity than initial RT-PCR testing (69% versus 91%, respectively).

We have created a software that can test a individual for SAR-COV-2, using some user input, chest X-rays and ultrasound.
We have segmented our model into 3 parts.
1st. Machine learning model:
We have trained our model using the data sets containing following features:
I. Fever
II. Body Pain
III. Age
IV. Running Nose
V. Difficulty in breathing.
We have considered 2888 samples of patients having above mentioned symptoms.
The output of this model will be a probability score. If The output of above model is greater than 0.5 means the person is more likely to be SARS- COV positive.
2nd Deep learning model:
Here we have taken the individual whose probability score is greater than 0.5 which came from our machine learning model.
Here we have trained our model using X-ray images of COVID positive and covid negative. A X-ray model was used in honkong. Brief of the model is present in the video. Here the output will be 0 for Covid negative individual. 1 for covid positive patients.
3rd. Deep learning model :
Here we have trained our model using ultrasound data of covid negative and covid positive individual. Here the output will be 0 of non negative and 1 for positive.
For our initial machine learning model we actually get a likelihood of an individual inflected by SARS-COV-2.
The internal and external validation accuracy of the for our chest X-ray model, was recorded 89.5 and 79.3% respectively 
The X-Ray data sets contains 1000+ chest X-rays of positive and negative cases across the world.
And for our 3rd deep learning model which is ultrasound segmentation, we are using it for verification. In order to reduce false positives and false negatives.
![SA](https://user-images.githubusercontent.com/51361052/80447325-bec45a80-8936-11ea-9070-a9f6185f3fd4.JPG)

![future Architecture](https://user-images.githubusercontent.com/51361052/80447322-bcfa9700-8936-11ea-8aea-fa738092a2f1.jpg)

