###

[//]: # ({{<image src1="logos/Logo_KIT.svg" src2= "logos/IRL_Logo_Light_blue.svg" src3="logos/canvas.png">}})
{{< doublevideo src1="img/bbrl_beerpong.mp4" src2="img/TableTennis4D_1-43.mp4">}}
# Abstract
Movement primitives (MPs) have been a popular tool for motion generation in reinforcement learning (RL). 
MPs offer a concise representation of motion through desired trajectories, 
facilitating efficient exploration in the MP’s parameter space and producing smooth
motions. Although many early successes in robot RL have been achieved by combining
RL with MPs, these approaches are often limited to learning a single stroke-based motion
that can not be adapted to task variations or during motion execution. As a result, the
research community has lost interest in RL with MPs and shifted its focus to the development 
of deep RL methods with atomic action spaces. Recently, we presented a new deep
RL method for the non-linear adaptation of MP parameters to different task variations
while leveraging efficient parameter-based exploration. Here, the problem of selecting the
movement primitive parameters was treated as a black box, in other word, the selected
parameters were executed throughout the whole episode and the resulting return was collected. 
While this method outperformed standard step-based RL in many domains, it does
not allow for online adaptation of the motion which rules out stochastic domains where
feedback is required. This paper is an extension of this work where we generalize this
approach to learning replanning strategies that allow for adaptation of the MP parameters 
throughout motion execution. To do so, our method uses a recent reformulation of the dynamic 
movement primitives (DMPs) which provides a simple integration of DMPs
into deep architectures while it allows smooth replanning as opposed to the probabilistic
movement primitives (ProMPs) used in the original paper. We conduct a comparative
analysis of our approach against state-of-the-art deep RL and RL with MPs methods, and
demonstrate improved performance with fewer samples in sophisticated, sparse rewarded
settings, as well as settings that require replanning.


## MP3-BB: Black-Box Reinforcement Learning
### Hopper Jump (Maximum Height)
{{< triplevideo src1="img/Videos/hopper/hopper_ppo.mp4" title1="PPO" 
                src2="img/Videos/hopper/hopper_bbrl_ppo.mp4" title2="MP3-PPO-BB"
                src3="img/Videos/hopper/hopper_bbrl_trpl.mp4" title3="MP3-BB">}}
### Box-Pushing
{{< triplevideo src1="img/Videos/boxpush/bpdense-ppo.mp4" title1="PPO" 
                src2="img/Videos/boxpush/bpdense_bbrl_ppo.mp4" title2="MP3-PPO-BB"
                src3="img/Videos/boxpush/bpdense_bbrl_trpl.mp4" title3="MP3-BB">}}
### Beerpong
{{< triplevideo src1="img/Videos/beerpong/Beerpong_PPO.mp4" title1="PPO" 
                src2="img/Videos/beerpong/Beerpong_BBRL_PPO.mp4" title2="MP3-PPO-BB"
                src3="img/Videos/beerpong/Beerpong_BBRL_TRPL.mp4" title3="MP3-BB">}}
### Table Tennis
{{< triplevideo src1="img/Videos/table_tennis/TT4D_PPO.mp4" title1="PPO" 
                src2="img/Videos/table_tennis/TT4D_BBRL_PPO.mp4" title2="MP3-PPO-BB"
                src3="img/Videos/table_tennis/TT4D_BBRL_TRPL.mp4" title3="MP3-BB">}}
## MP3-Replan: Replanning with Movement Primititves
### Box-Pushing with Changing Targets
{{< doublevideo src1="img/BoxPushingGC20_ppo.mp4" title1="PPO" 
    src2="img/BoxPushingGC20_mp3_replan.mp4" title2="MP3-Replan">}}
### Table Tennis with Changing Targets
{{< doublevideo src1="img/TableTennisGoalSwitchingBBRL.mp4" title1="MP3-BB" 
    src2="img/TableTennisGoalSwitching_MP3.mp4" title2="MP3-Replan">}}
### Table Tennis with Wind
{{< doublevideo src1="img/TableTennisWindBBRL.mp4" title1="MP3-BB" 
    src2="img/TableTennisWindReplan1.mp4" title2="MP3-Replan">}}

[//]: # (## Citation)

[//]: # (If you find our work useful, please consider citing:)

[//]: # (```BibTeX)

[//]: # (@INPROCEEDINGS{Li2023Curriculum,)

[//]: # (  author = {Li, Maximilian Xiling )

[//]: # (            and Celik, Onur )

[//]: # (            and Becker, Philipp )

[//]: # (            and Blessing, Denis )

[//]: # (            and Lioutikov, Rudolf )

[//]: # (            and Neumann, Gerhard},)

[//]: # (  title  = {Curriculum-Based Imitation of Versatile Skills},)

[//]: # (  booktitle={2023 International Conference on Robotics and Automation &#40;ICRA&#41;},)

[//]: # (  year   = {2023},)

[//]: # (})

[//]: # (```)