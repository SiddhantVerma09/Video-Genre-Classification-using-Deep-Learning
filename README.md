# Video-Genre-Classification-using-Deep-Learning

## Abstract -
The classification of video genres is a tough and time-consuming operation that has recently piqued the interest of deep learning enthusiasts and researchers. With growing video streaming services in the modern era of online platforms, videos of numerous genres are being consumed. Such popularity of consuming videos has resulted in an excessive urge and demand for genre classification models. Thus, the multi-model approach for classification of video genres has been discussed in this study by preprocessing picture datasets from diverse genres, as well as training and evaluating deep learning models. Audio part in any video could prove to be the main distinction between video genres. Thus, in the second phase of the project dataset has been  trained and tested audio datasets including 8500+ audio files of different video genres. In conclusion, results have been analyzed and suggested a fusion strategy of both video and audio classification models to enhance the quality and accuracy of video genre classification in real-life systems and applications.

## Methodology - 
In the method framework, video and audio genre classification has been implemented separately. For video genre classification, two different base models in Keras namely ResNet-50 and MobileNet have been trained and the one giving highest accuracy (ResNet-50 in this case) has been recommended for best results. While for audio genre classification, an Artificial Neural Network (ANN) architecture has been implemented. This paper suggests a multi-model strategy that can be implemented on large computing systems by combining both the video and audio genre classification models in future. 
The entire process has been followed and performed in three phases which will be discussed in detail.

### A.	 Dataset Compilation and Pre-processing  -
Dataset for Video genre classification is a combined image dataset of primarily three video genres - Natural content, Animation i.e Cartoons and Gaming. All images are random snapshots extracted from video (source - either YouTube or other video streaming sites) of these 3 video genres. Total of video-image dataset included more than 3000 images.  In the data preprocessing step, color conversion of images in the dataset into RGB form was necessary. Additionally, color conversion was followed by resizing images with height and width as (244,244) which is the default recommended size used for ResNet and 
MobileNet models. A train and test split were performed where the test size given was 25%.

For Audio classification, a huge dataset of 8500+ audio files were extracted from Kaggle. This training dataset involved audio files of 10 different audio genres. These genres/categories were namely car horn noise, kids shouting sounds, road side dogs barking, carpentry sounds, engine idling sounds, gunshot sound, horn sound, street side music sounds and air conditioner noise. Along with the audio dataset, a (.csv) metadata file was attached and used for processing ahead. 

### B.	 Video Genre Classification –
The base model is ResNet50 where the given weights are “imagenet” as all available deep learning models have already been trained on imagenet data weights which contain millions of images and it transfers its learning to solve video classification problems.
An AveragePooling layer has been applied into the network which downsampled input into its spatial dimensions mentioned as ‘poolsize’. Flatten layer helps us to flatten data into one dimension and for Dense layer we’ve given 512 neurons which means these neurons will learn the new weights compared to the rest of hidden layers which stay the same. In this case 3, the number of neurons equals the number of genres classified.

### C. Audio Genre Classification –
The trained data for this task involves characteristics (x) which represent audio file locations, and target labels (y) which represent class names. The metadata file from the Kaggle dataset was used directly because it had the above information. The metadata file contains information about each audio file as well as its folder location.

For the actual model tuning process, since some of the audio files were mono channels whereas most of them were stereo, there was a need to convert the signal to mono meaning where the channel will always be 1 as the model trains, expecting all audio files must have the same dimensions. This was done using Librosa library in Python which is often used for such conversion related to audio files. Now there was a need to create some independent features which would represent the audio dataset. For that Mel-Frequency Cepstral Coefficients (MFCC) have been used through which makes analyzing both frequency and time characteristics of audio possible. 

## Project Sample Images -
![image](https://github.com/SiddhantVerma09/Video-Genre-Classification-using-Deep-Learning/assets/63495865/fdb1881c-6a08-41af-be9c-64502210c805)

![image](https://github.com/SiddhantVerma09/Video-Genre-Classification-using-Deep-Learning/assets/63495865/dbd55e3c-3954-462b-8acb-d2e80ea627bf)

![image](https://github.com/SiddhantVerma09/Video-Genre-Classification-using-Deep-Learning/assets/63495865/143ac1a2-6a32-4298-bbf6-347dad09ab07)

![image](https://github.com/SiddhantVerma09/Video-Genre-Classification-using-Deep-Learning/assets/63495865/7f40e399-5c1e-405a-9c92-8552184e187d)

