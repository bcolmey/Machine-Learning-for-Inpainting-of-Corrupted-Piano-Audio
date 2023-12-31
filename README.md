# Machine-Learning-for-Inpainting-of-Corrupted-Piano-Audio
I recently digitized some old VHS cassette tapes and stumbled upon a recording of my first piano recital. Unfortunately, the audio was significantly corrupted. To remedy this, I turned to machine learning for audio inpainting, aiming to restore the corrupted sections. The process started by analyzing the original piano recording to identify and characterize silences and gaps. I then pre-processed the piano recording to standardize the gaps sizes, before performing data acquisition to obtain training and testing datasets with similar gaps for a controlled study. 

By employing the Short-Time Fourier Transform (STFT) technique, the audio is transformed into a format conducive to deep learning. I experimented with a variety of loss functions and tested different machine learning models, comparing their effectiveness in inpainting the audio. This endeavor was a fascinating journey into the intersection of digital audio restoration and machine learning. 

A full description of the code can be found [here](https://medium.com/@benjamincolmey/using-machine-learning-to-inpaint-corrupted-piano-audio-5bab24db17f1)

## Original audio:

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/ifMcBhQmidI/0.jpg)](https://www.youtube.com/watch?v=ifMcBhQmidI)


## Audio after inpainting:
[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/R4eWZ_TFa4E/0.jpg)](https://www.youtube.com/watch?v=R4eWZ_TFa4E)


## Running

To run this code simply clone this repository and run the main.py script with python (the pydub, keras, tenserflow modules are required):
 
```
$ git clone https://github.com/bcolmey/Machine-Learning-for-Inpainting-of-Corrupted-Piano-Audio
$ cd Machine-Learning-for-Inpainting-of-Corrupted-Piano-Audio
$ python main.py 
```


## Some important steps and plots from the code:

#### Original audio waveform with gaps marked:
<img src="https://github.com/bcolmey/Machine-Learning-for-Inpainting-of-Corrupted-Piano-Audio/blob/main/Images/original_audio.jpg" width="700" height="500">

#### Train and test data with newly added gaps and relevant contexts shown:
<img src="https://github.com/bcolmey/Machine-Learning-for-Inpainting-of-Corrupted-Piano-Audio/blob/main/Images/train_test_data.jpg" width="700" height="500">


#### Spectrogram of first gap and contexts after performing STFT:
<img src="https://github.com/bcolmey/Machine-Learning-for-Inpainting-of-Corrupted-Piano-Audio/blob/main/Images/stft.jpg" width="400" height="300">


#### Spectrogram and waveform of the first gap predicted using UNET model:

<img src="https://github.com/bcolmey/Machine-Learning-for-Inpainting-of-Corrupted-Piano-Audio/blob/main/Images/Unet.jpg" width="800" height="600">


#### Spectrogram and waveform of the first gap predicted using CNN model:

<img src="https://github.com/bcolmey/Machine-Learning-for-Inpainting-of-Corrupted-Piano-Audio/blob/main/Images/cnn_gap.jpg" width="800" height="200">


#### Spectrogram and waveform of the first gap predicted using the encoder-decoder model:

<img src="https://github.com/bcolmey/Machine-Learning-for-Inpainting-of-Corrupted-Piano-Audio/blob/main/Images/encoder_decoder_gap.jpg" width="800" height="200">


#### Final audio filled-in using model predictions:

<img src="https://github.com/bcolmey/Machine-Learning-for-Impainting-of-Corrupted-Piano-Audio/blob/main/Images/final_audio.jpg" width="700" height="500">

