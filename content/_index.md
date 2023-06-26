###

[//]: # ({{<image src1="logos/Logo_KIT.svg" src2= "logos/IRL_Logo_Light_blue.svg" src3="logos/canvas.png">}})
{{< doublevideo src1="img/bbrl_beerpong.mp4" src2="img/TableTennis4D_1-43.mp4">}}
# Abstract
We introduce a novel deep reinforcement learning (RL) approach called Movement Primitive-
based Planning Policy (MP3). By integrating movement primitives (MPs) into the deep RL
framework, MP3 enables the generation of smooth trajectories throughout the whole learning 
process while effectively learning from sparse and non-Markovian rewards. Additionally,
MP3 maintains the capability to adapt to changes in the environment during execution.
Although many early successes in robot RL have been achieved by combining RL with
MPs, these approaches are often limited to learning single stroke-based motions, lacking
the ability to adapt to task variations or adjust motions during execution. Building upon
our previous work, which introduced an episode-based RL method for the non-linear adaptation of 
MP parameters to different task variations, this paper extends the approach to
incorporating replanning strategies. This allows adaptation of the MP parameters throughout 
motion execution, addressing the lack of online motion adaptation in stochastic domains
requiring feedback. We compared our approach against state-of-the-art deep RL and RL
with MPs methods. The results demonstrated improved performance in sophisticated,
sparse reward settings and in domains requiring replanning.


## MP3-BB: Black-Box Reinforcement Learning
Instead of generating atomic action for each state, we generate a whole trajectory of actions at once using movement primitives.
This enables us to efficiently handle sparse and even non-Markovian rewards. In this setting, reinforcement learning is treated
as a black-box optimization problem. We refer this setting as **MP3-BB**.
### Hopper Jump (Maximum Height)
{{< triplevideo src1="img/Videos/hopper/hopper_ppo.mp4" title1="PPO" 
                src2="img/Videos/hopper/hopper_bbrl_ppo.mp4" title2="MP3-PPO-BB"
                src3="img/Videos/hopper/hopper_bbrl_trpl.mp4" title3="MP3-BB">}}
### Box-Pushing (Dense Reward)
{{< triplevideo src1="img/Videos/boxpush/bpdense-ppo.mp4" title1="PPO" 
                src2="img/Videos/boxpush/bpdense_bbrl_ppo.mp4" title2="MP3-PPO-BB"
                src3="img/Videos/boxpush/bpdense_bbrl_trpl.mp4" title3="MP3-BB">}}
### Box-Pushing (Sparse Reward)
{{< triplevideo src1="img/Videos/boxpushingsparse/BPsparse1_ppo_1.mp4" title1="PPO" 
                src2="img/Videos/boxpushingsparse/BPsparse1_mp3_bb_ppo.mp4" title2="MP3-PPO-BB"
                src3="img/Videos/boxpushingsparse/BPsparse1_mp3_bb_2.mp4" title3="MP3-BB">}}
### Beerpong
{{< triplevideo src1="img/Videos/beerpong/Beerpong_PPO.mp4" title1="PPO" 
                src2="img/Videos/beerpong/Beerpong_BBRL_PPO.mp4" title2="MP3-PPO-BB"
                src3="img/Videos/beerpong/Beerpong_BBRL_TRPL.mp4" title3="MP3-BB">}}
### Table Tennis
{{< triplevideo src1="img/Videos/table_tennis/TT4D_PPO.mp4" title1="PPO" 
                src2="img/Videos/table_tennis/TT4D_BBRL_PPO.mp4" title2="MP3-PPO-BB"
                src3="img/Videos/table_tennis/TT4D_BBRL_TRPL.mp4" title3="MP3-BB">}}
## MP3-Replan: Replanning with Movement Primititves
By incorperating dynamic-based movement primitives, such as DMPs (Dynamic Movement Primitives) and ProDMPs (Probabilistic Dynamic Movement Primitives),
into our framework, we gain the ability to adapt the motion during online execution. This capability enables us to effectively 
handle unforeseen changes in the environment, such as shifting target positions or external perturbations. 
In constrat to the black-box setting **MP3-BB**, we specifically designate this setting as **MP3-Replan**.
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