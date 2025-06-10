# Lung-Sound-Classification-using-Deep-Learning-for-lung-disease-detection
# FYI this is the pre version of original research where we achieved more than 93 percent accuracy. 
Created a diseases detection system from sound of lung in one of the 10 classes including healthy subjects. USed datasets ICBHI and Fraiwan

1.  After using datasets ICBHI and Fraiwan , merging preprocessing we obtain these 10 classes.
Conditions: 
copd 820 
healthy 140 
asthma 97 
pneumonia 52 
urti 23 
bronchiectasis 16 
bronchiolitis 13 
lung fibrosis 12 
bronchitis 9 
plueral effusion 6 
Name: count, dtype: int64 
2.	Standardized the audio files in 6sec duration, 44100HZ SR, stereo channel configuration, 16-bit depth and saved them in a standardized folder. 
3.	Segmented long audio files of under-represented classes into smaller files of 6 sec duration and saved them in a folder. Also made new csv files related to those audio files.
4.	Standardized the new segmented audio files in 6sec duration, 44100HZ SR, stereo channel configuration, 16-bit depth and save in a folder and merge metadata files with other files and merge standardized audio files. 
5.	Merged_files>>filtered(1234)>>>updated(570_segmented_audio_files)>>>standardized1(filtered) + standardized2(updated) >>> standardized_merged (1728 files)>>resampled_audio(960)>>augmented_audio(170)>>Final_audio(resampled_audio+augmented_audio)(1161)
6.	Merged_audio>>>standardized>>segmented>>>segmented_standardized>>standardized_merged(segmented_std+standardized) >>>balanced(1100)>>>augmented(1270)
7.	Augment three classes lung fibrosis, bronchitis and pleural effusion using pitch shifting of 1 semitone to each audio sample, with SR 22050 and number of steps 1. Normalization is applied to maintain numerical stability during processing and training.
8.	We do feature extraction and obtain top 5 features using PCA
9.  We create a CNN model and apply it and get validation accuracy on test data.

