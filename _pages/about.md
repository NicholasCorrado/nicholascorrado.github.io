---
permalink: /
title: "Welcome!"
excerpt: "About me"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---
[//]: # (Towards this end, I've studied data augmentation, adaptive sampling, and representation learning techniques )

I am a Computer Sciences PhD candidate at the University of Wisconsin-Madison advised by [Josiah Hanna](https://pages.cs.wisc.edu/~jphanna/). 
I am broadly interested in researching techniques to improve the data efficiency of reinforcement learning (RL).
Recently, my research has focused on 
1. Understanding the role of **data augmentation** in the context of RL, and 
2. Demonstrating how **adaptive, off-policy sampling** can make on-policy learning more data efficient.

Ultimately, my goal is to make RL a more viable tool for real-world tasks. 
Towards this end, **I've been using physical robotics tasks for my research in data augmentation**.
From 2021-2022, I was a research intern at Sandia National Laboratories working on RL for power grid management.
From 2022-2023, I transitioned to a consulting role for the same project.

During the first year of my PhD, I worked in databases with [Jignesh Patel's](https://jigneshpatel.org) group building [Hustle](https://github.com/UWHustle/hustle), 
an efficient data platform based built on top of Apache Arrow. 
I received a BPhil in physics and a B.S. in mathematics at the University of Pittsburgh where I worked with [Vladimir Savinov](https://www.physicsandastronomy.pitt.edu/people/vladimir-savinov). 
For my thesis, I designed and optimized the first search for new hadronic WbJ states in data collected by the Belle Experiment.

Outside of research, [I am a jazz guitarist](https://www.youtube.com/@nicholascorrado3891/videos) &mdash; in fact, I almost pursued music professionally after high school.
I am heavily influenced by jazz manouche (commonly called gypsy jazz) but also draw inspiration from Bossa, Dixieland, and Modal jazz styles.
When I was 13, I had the great fortune of meeting and playing with [Joe Negri](https://pittsburghsymphony.org/pso_home/biographies/guest-artists/joe-negri) (aka ["Handyman Negri" from Mister Rogers' Neighborhood](http://www.neighborhoodarchive.com/mrn/characters/handyman_negri/index.html)). 
He is a jazz legend in my hometown of Pittsburgh and arguably one of the best jazz guitarists in the US.

I am always eager to discuss research and/or music. Feel free to send an email if you're interested in discussing anything!

## Publications and Manuscripts Under Review

<ins>Guided Data Augmentation for Offline Reinforcement Learning and Imitation Learning.</ins> \
**Nicholas E. Corrado** & Josiah P. Hanna. \
*Under Review.* \
[[preprint (arxiv coming soon!)]](https://nicholascorrado.github.io/files/guda_arxiv_2023_10_13.pdf)
[[video]](https://youtu.be/CatP5PgOuzo)
<details>
<summary>
  Abstract
</summary>
    <p>
        Learning from demonstration (LfD) is a popular technique that uses expert demonstrations to learn robot control policies. However, the difficulty in acquiring expert-quality demonstrations limits the applicability of LfD methods: real- world data collection is often costly and the quality of the demonstrations depends greatly on the demonstrator’s abilities and safety concerns. A number of works have leveraged data augmentation (DA) to inexpensively generate additional demon- stration data, but most DA works generate augmented data in a random fashion and ultimately produce highly suboptimal data. In this work, we propose Guided Data Augmentation (GuDA), a human-guided DA framework that generates expert-quality augmented data. The key insight of GuDA is that while it may be difficult to demonstrate the sequence of actions required to produce expert data, a user can often easily identify when an augmented trajectory segment represents task progress. Thus, the user can impose a series of simple rules on the DA process to automatically generate augmented samples that approximate expert behavior. To extract a policy from GuDA, we use off-the-shelf offline reinforcement learning and behavior cloning algorithms. We evaluate GuDA on a physical robot soccer task as well as simulated D4RL navigation tasks, a simulated autonomous driving task, and a simulated soccer task. Empirically, we find that GuDA enables learning from a small set of potentially suboptimal demonstrations and sub- stantially outperforms a DA strategy that samples augmented data randomly.
    </p>
</details>

<p></p>
<ins>On-Policy Policy Gradient Learning Without On-Policy Sampling.</ins> \
**Nicholas E. Corrado** & Josiah P. Hanna. \
*Under Review.* \
[[preprint (arxiv coming soon!)]](https://nicholascorrado.github.io/files/props_v1.pdf)
<details>
<summary>
  Abstract
</summary>
    <p>
        On-policy reinforcement learning RL algorithms perform policy updates using i.i.d. trajectories collected by the current policy. However, after observing only a finite number of trajectories, on-policy sampling may produce data that fails to match the expected on-policy data distribution. This sampling error leads to noisy updates and data inefficient on-policy learning. Recent work in the policy evaluation setting has shown that non-i.i.d., off-policy sampling can produce data with lower sampling error than on-policy sampling can produce~\citep{zhong2022robust}. Motivated by this observation, we introduce an adaptive, off-policy sampling method to improve the data efficiency of on-policy policy gradient algorithms. Our method, Proximal Robust On-Policy Sampling (PROPS) reduces sampling error by collecting data with a **behavior policy** that increases the probability of sampling actions that are under-sampled with respect to the current policy. Rather than discarding data from old policies -- as is commonly done in on-policy algorithms -- PROPS uses data collection to adjust the distribution of previously collected data to be approximately on-policy. We empirically evaluate PROPS on both continuous-action MuJoCo benchmark tasks as well discrete-action tasks and demonstrate that (1) PROPS decreases sampling error throughout training and (2) improves the data efficiency of on-policy policy gradient algorithms. Our work improves the RL community’s understanding of a nuance in the on-policy vs off-policy dichotomy: on-policy learning requires on-policy data, not on-policy sampling.
    </p>
</details>

<p></p>
<ins>Understanding when Dynamics-Invariant Data Augmentations Benefit Model-free Reinforcement Learning Updates.</ins> \
**Nicholas E. Corrado** & Josiah P. Hanna. \
*Under Review.* \
[[preprint (arxiv coming soon!)]](https://nicholascorrado.github.io/files/understanding_da_arxiv_2023_10_12.pdf)

<details>
<summary>
  Abstract
</summary>
    <p>
        Recently, data augmentation (DA) has emerged as a method for leveraging domain knowledge to inexpensively generate additional data in reinforcement learning (RL) tasks, often yielding substantial improvements in data efficiency. While prior work has demonstrated the utility of incorporating augmented data directly into model-free RL updates, it is not well-understood when a particular DA strategy will improve data efficiency. In this paper, we seek to identify general aspects of DA responsible for observed learning improvements. Our study focuses on sparse-reward tasks with dynamics-invariant data augmentation functions, serving as an initial step towards a more general understanding of DA and its integration into RL training. Experimentally, we isolate three relevant aspects of DA: state-action coverage, reward density, and the number of augmented transitions generated per update (the augmented replay ratio). From our experiments, we draw two conclusions: (1) increasing state-action coverage often has a much greater impact on data efficiency than increasing reward density, and (2) decreasing the augmented replay ratio substantially improves data efficiency. In fact, certain tasks in our empirical study are solvable only when the replay ratio is sufficiently low.
    </p>
</details>

<p></p>
<ins>Reinforcement learning for automatic generation control using a Kuramoto-like model.</ins> \
**Nicholas E. Corrado**, Michael Livesay, Tyson Bailey, & Drew Levin. \
*Under Review.*
<details>
<summary>
  Abstract
</summary>
    <p>
    Awaiting approval from Sandia National Laboratories to share this abstract. Stay tuned!
    </p>
</details>

<p></p>
<ins>Deep Reinforcement Learning for Distribution Power System Cyber-Resilience via Distributed Energy Resource Control.</ins> \
**Nicholas E. Corrado**, Michael Livesay, Tyson Bailey, & Drew Levin. \
*To appear in IEEE International Conference on Communications, Control, and Computing Technologies for Smart Grids (IEEE SmartGridComm)*, 2023.
<details>
<summary>
  Abstract
</summary>
    <p>
    Awaiting approval from Sandia National Laboratories to share this abstract. Stay tuned!
    </p>
</details>

<p></p>
<ins>Simulation-Acquired Latent Action Spaces for Dynamics Generalization.</ins> \
**Nicholas E. Corrado**, Yuxiao Qu, & Josiah P. Hanna. \
*Proceedings of The 1st Conference on Lifelong Learning Agents, 2022.* \
[[paper]](https://proceedings.mlr.press/v199/corrado22a/corrado22a.pdf)
[[website + video]](https://sites.google.com/wisc.edu/salas?usp=sharing)
<details>
<summary>
  Abstract
</summary>
    <p>
    Deep reinforcement learning has shown incredible promise at training high-performing agents to solve high-dimensional continuous control tasks in a particular training environment. However, to be useful in real-world settings, long-lived agents must perform well across a range of environmental conditions. Naively applying deep RL to a task where environment conditions may vary from episode to episode can be data inefficient. To address this inefficiency, we introduce a method that discovers structure in an agent’s high-dimensional continuous action space to speed up learning across a range of environmental conditions. Whereas prior work on finding so-called latent action spaces requires expert demonstrations or on-task experience, we instead propose to discover the latent, lower-dimensional action space in a simulated source environment and then transfer the learned action space for training in the target environment. We evaluate our novel method on randomized variants of simulated MuJoCo environments and find that, when there is a lower-dimensional action-space to exploit, our method significantly increases data efficiency. For instance, in the Ant environment, our method reduces the 8-dimensional action-space to a 3-dimensional action-space and doubles the average return achieved after a training budget of 2 million timesteps.
    </p>
</details>