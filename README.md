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


## Week 7:

## -->Trying out Conversational NLPs:

## --> Voice Activity Detection:
https://herve.niderb.fr/fastpages/2022/10/23/One-speaker-segmentation-model-to-rule-them-all



