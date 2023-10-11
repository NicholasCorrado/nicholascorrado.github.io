---
title: "Paper Title Number 1"
collection: publications
permalink: /publication/props
excerpt: 'This paper is about the number 1. The number 2 is left for future work.'
date: 2009-10-01
venue: 'Journal 1'
paperurl: 'http://academicpages.github.io/files/paper1.pdf'
citation: 'Your Name, You. (2009). &quot;Paper Title Number 1.&quot; <i>Journal 1</i>. 1(1).'
---

[//]: # (This paper is about the number 1. The number 2 is left for future work.)
[//]: # ([Download paper here]&#40;http://academicpages.github.io/files/paper1.pdf&#41;)


Nicholas E. Corrado & Josiah P. Hanna.  *On-Policy Policy Gradient Learning Without On-Policy Sampling*. Under Review, 2023.

**Abstract:** 
On-policy reinforcement learning RL algorithms perform policy updates using i.i.d. trajectories collected by the current policy. However, after observing only a finite number of trajectories, on-policy sampling may produce data that fails to match the expected on-policy data distribution. This sampling error leads to noisy updates and data inefficient on-policy learning. Recent work in the policy evaluation setting has shown that non-i.i.d., off-policy sampling can produce data with lower sampling error than on-policy sampling can produce~\citep{zhong2022robust}. Motivated by this observation, we introduce an adaptive, off-policy sampling method to improve the data efficiency of on-policy policy gradient algorithms. Our method, Proximal Robust On-Policy Sampling (PROPS) reduces sampling error by collecting data with a **behavior policy** that increases the probability of sampling actions that are under-sampled with respect to the current policy. Rather than discarding data from old policies -- as is commonly done in on-policy algorithms -- PROPS uses data collection to adjust the distribution of previously collected data to be approximately on-policy. We empirically evaluate PROPS on both continuous-action MuJoCo benchmark tasks as well discrete-action tasks and demonstrate that (1) PROPS decreases sampling error throughout training and (2) improves the data efficiency of on-policy policy gradient algorithms. Our work improves the RL community’s understanding of a nuance in the on-policy vs off-policy dichotomy: on-policy learning requires on-policy data, not on-policy sampling.
