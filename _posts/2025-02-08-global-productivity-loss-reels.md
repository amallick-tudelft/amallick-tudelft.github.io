---
title: 'Global Productivity Loss from Watching Reels and Its Cure'
date: 2025-02-08
permalink: /posts/2025/02/global-productivity-loss-reels/
tags:
  - social-media
  - algorithms
  - productivity
  - technology
excerpt: 'A mathematical analysis of reel addiction and a proposed solution using regret maximization'
---

With the rapid development of learning-based technologies, the reel industry (YouTube, Facebook, Instagram, etc.) has taken the world into the booze of cocaine-like drugs. Even the best minds of a country are regular customers for hours every day. Let us first understand mathematically (in a very non-rigorous way) why reels are so addictive.

## The Mathematical Framework

Consider the average person watching reels as the **Audience**, and there is an **Agent** (the drug lord) who has designed an algorithm $$F(\cdot|H): \mathcal{Z} \to \mathcal{Y}$$, where $$H$$ is history, $$\mathcal{Z}$$ is the set of design parameters, and $$\mathcal{Y}$$ is the set of strategies. 

Step by step, let us define the sequence of events that take place while watching reels:

### Event Sequence

**1. Content Generation**

The Agent runs the secret algorithm and generates a particular reel at time $$t$$ (say $$x_t$$) from a pool of finitely many reels (say, set $$\mathcal{X}$$).

**2. Audience Interaction**

After the audience watches it, they give likes/comments/swipes to the next reel without watching it in full. All of these actions of the audience are formulated in terms of rewards $$r_t(x_t)$$ at time $$t$$. For example, for a given $$x_t$$:
- 'Like' $$: r_t(x_t) = 1$$
- 'Swiping without watching' $$: r_t(x_t) = 0$$

Note that the Agent always wants to maximize the reward.

**3. Regret Formulation**

We define the notion of regret ($$R_T$$) after $T$ rounds as:

$$R_T = \max_{x \in \mathcal{X}} \left(\sum_{t=1}^{T} r_t(x)\right) - \mathbb{E}\left[\sum_{t=1}^{T} r_t(x_t)\right]$$

where:
- The **first term** is the best possible achievable cumulative reward (if the Agent could have known the reward function $$r_t(\cdot)$$ beforehand every time; in other words, if the agent had known what the audience likes most before showing a reel)
- The **second term** is the actual realized cumulative reward after $$T$$ rounds

## The Addiction Mechanism

The goal of the Agent is to develop an algorithm where $$R_T$$ grows **sub-linearly** with $T$, i.e., in the order of $$\mathcal{O}(\log T)$$ (for example). 

Note that if $$R_T$$ grows sub-linearly with $$T$$, it implies asymptotically that $$R_T$$ is almost constant, which means every new $$x_t$$, as given by the algorithm, is approximately the optimal one. When this happens, it means **you like almost every reel you are watching and are under the arrest of an addiction**.

The drug lords know the secret formula to design such algorithms that want to steal away your precious time by engaging you in reels.

## Proposed Solution

With every technology, a grave amount of responsibility comes into the hands of the innovators. Therefore, each user must be given a **hyper-parameter** (say $$p$$), which will signify the time control for watching reels on any platform.

### Implementation

Once a user sets $$p = 1$$ hour (for example), the Agent behind the algorithm **changes its strategy** after 1 hour to **maximize the Regret** ($$R_T$$), which will eventually show such reels that the user starts to dislike and stay away from watching it further.

This simple modification transforms the optimization objective from:

$$\text{Current: } \min R_T \quad \text{(minimize regret = maximize engagement)}$$

to:

$$\text{Proposed: } \max R_T \quad \text{(maximize regret = minimize engagement after time } p\text{)}$$

## Summary

By introducing user-controlled time limits that trigger a strategic shift in the recommendation algorithm, we can transform addictive engagement mechanisms into self-limiting systems. This approach respects user autonomy while addressing the societal problem of attention exploitation.

---

**Copyright:** All rights reserved.

**Citation:**
```
Mallick, A. (2025). Global Productivity Loss from Watching Reels and Its Cure. 
Retrieved from https://amallick-tudelft.github.io/posts/2025/02/global-productivity-loss-reels/
```

---

*What are your thoughts on this proposal? Share your ideas in the comments below.*
