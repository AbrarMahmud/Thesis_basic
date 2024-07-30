# Thesis_basic

## Week 6
## -->Problem faced: 
Windows ffmpeg compatibility issue

--> probable fix:
https://github.com/huggingface/transformers/issues/25183#issuecomment-1769312607

**My soln1**: 

initiate separate env (conda create --name Thesis_basic_code1 python=3.10)

then copy audioutils.py and edit it locally , save it ae custom_audioutils.py

then run "from custom_audio_utils import custom_ffmpeg_microphone_live" in jupyter sketch

Then inside the anaconda enviroment run:conda install conda-forge::ffmpeg

Then after run:ffmpeg -list_devices true -f dshow -i dummy to find the device name

for my machine :--->Microphone Array (Realtek High Definition Audio)

replace this name according to:https://github.com/huggingface/transformers/issues/25183#issuecomment-1769312607 in my custom_audioutils.py

and finally the code ran..................


**My soln2**:(linux)--->this will not work with py torch
first install ffmpeg in original linux terminal using the command:
*sudo apt install ffmpeg libasound2 alsa-utils*


then create a separate conda env using pytho n 3.8.10(not the base coda python 3.11)
*conda create -n ug_thesis python=3.8.10*

activate the conda env but do not use cona install ffmpeg(the base env ffmpeg is already available here)

## **My soln2**
but then after following this ,i got the proper result:

 https://github.com/pytorch/vision/issues/7508#issuecomment-1803100199



## -->Problem faced: 
The kernel for OneDrive - BUET/L-4_T-1/Thesis/basic_code1/Hugging_face_unit7.ipynb appears to have died. It will restart automatically.

**My soln1**:
In my system ,The mic requires initialiazion time so by adding some delay (running the mic without transcriber() for few iteration) i was able to by pass the error *"UnboundLocalError: local variable 'item' referenced before assignment"*


## -->Problem faced:
while trying to run TTS(Test-To-Speech) This erroe is shown:  cannot load library 'libsndfile.dll': error 0x7e




**My soln1**:
followed this:
https://github.com/bastibe/python-soundfile/issues/373#issuecomment-1475274115

then pip uninstall soundfile

pip install soundfile


## -->Problem faced:
in linux pyaudio conda was not working

**My soln1**
follow this link:
https://github.com/ContinuumIO/anaconda-issues/issues/4139#issuecomment-479684029

## Week 7:

## -->Trying out Conversational NLPs:

## --> Voice Activity Detection(incomplete):
I plan to use VAD from pyannote.audio
https://herve.niderb.fr/fastpages/2022/10/23/One-speaker-segmentation-model-to-rule-them-all

The link given below is on Training a voice activity detection pipeline from scratch with pyannote.audio

https://github.com/pyannote/pyannote-audio/blob/9e4ec5f6e0b0f5d60c557981fc680e8cebf78f5b/tutorials/voice_activity_detection.ipynb


A problem that i am facing is pyannote/voice-activity-detection pipeline uses "x.wav" file format but mic outputs np.arrray()


## -->Energy based approach:


**Note:** Hugging Face Transformers pipelines, by design, consume the input data provided to them, and they are typically designed for one-time use. Once the data has been processed, the pipeline object is no longer usable for further inferences with the same input data. This design choice ensures that the pipeline state is clean for each new inference.

## -->Problem faced:
linux jupyter notebook is blank

**My sol1**
after opening jupyter notebook on broswer press "ctrl+f5" to force restart the page. 

**My sol2**(better)
delete browser history


