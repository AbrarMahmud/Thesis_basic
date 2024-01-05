# Thesis_basic

## Week 5(after) 
-->Problem faced: Windows ffmpeg compatibility issue

--> probable fix:
https://github.com/huggingface/transformers/issues/25183#issuecomment-1769312607
*My soln1*: initiate separate env (conda create --name your_environment_name python=3.10)

            then try to edit the src filr audioutils.py from transformers lib(Within the env)
