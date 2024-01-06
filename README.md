# Thesis_basic

## Week 5(after) 
## -->Problem faced: Windows ffmpeg compatibility issue

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


## Problem faced: 
The kernel for OneDrive - BUET/L-4_T-1/Thesis/basic_code1/Hugging_face_unit7.ipynb appears to have died. It will restart automatically.

