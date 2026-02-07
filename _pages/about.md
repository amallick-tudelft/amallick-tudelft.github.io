---
permalink: /
title: "Welcome to my digital home!"
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

<style>
.page__content {
  position: relative;
}

.page__content::before {
  content: "";
  position: fixed;
  top: 0;
  right: 0%;  /* Shift left to show more of the image */
  width: 45%;  /* Increased width to show full image */
  height: 100vh;
  background-image: url('/images/apj_3.png');
  background-size: cover;  /* Changed from 'cover' to 'contain' to show full image */
  background-position: center;  /* Align to the right side */
  background-repeat: no-repeat;
  opacity: 0.2;  /* Increased opacity (was 0.12) */
  z-index: -1;
  pointer-events: none;
}

@media (prefers-color-scheme: dark) {
  .page__content::before {
    opacity: 0.15;  /* Slightly higher for dark mode */
  }
}

@media (max-width: 968px) {
  .page__content::before {
    display: none;
  }
}
</style>

I occasionally conduct research in the broad area of sequential decision-making and, at other times, teach myself, supervise students, manage projects, assist in technical courses, play chess, and roam the world.

## Brief bio

- **PhD (2023- )**, @ [TU Delft, DCSC](https://www.tudelft.nl/me/over/afdelingen/delft-center-for-systems-and-control), joint-advisors: [Peyman Mohajerin Esfahani](https://mohajerinesfahani.github.io/) and [Sergio Grammatico](https://sites.google.com/site/grammaticosergio/)
- **MS (by Research) (2021-2023)** in electrical engineering, @ [IIT Kharagpur, India](https://www.iitkgp.ac.in/), joint-supervisors: [Ashish R. Hota](https://facweb.iitkgp.ac.in/~ahota/index.html) and [Prabodh Bajpai](https://home.iitk.ac.in/~pbajpai/)
- **B.Tech (2015-2019)** in electrical engineering, @ [Jalpaiguri Government Engineering College](https://jgec.ac.in/)
  
## Research interests

Although I struggle to understand a meaningful research direction, I find myself attached to the following areas:

1. Sequential decision-making in static and dynamic environments (e.g., Model predictive control, Multi-armed bandits, Online learning, etc.)
2. Nash equilibrium prediction (aka Inverse game theory)
3. Applications to real-world complex systems like modern power systems, electric vehicle charging infrastructure, etc.

## Breaking news!

1. **July 2025**, an article ["A User-centric Game for Balancing V2G Benefits with Battery Degradation of Electric Vehicles"](https://ieeexplore.ieee.org/document/11104074) accepted in ***IEEE Transactions on Transportation Electrification***

2. **May 2025**, an article ["User-centric Vehicle-to-Grid Optimization with an Input Convex Neural Network-based Battery Degradation Model"](https://ieeexplore.ieee.org/document/11163818) accepted in ***IEEE International Conference on Automation Science and Engineering (CASE), 2025***

3. **November 2024**, an article ["Hybrid Model Predictive Control Framework for Efficient Operation of a Five-Port Converter Interfaced DC Microgrid"](https://ieeexplore.ieee.org/document/10791340) accepted in ***IEEE Transactions on Industrial Electronics***

4. **May 2024**, an article ["Distributed Coordination of Multi-Microgrids in Active Distribution Networks for Provisioning Ancillary Services"](https://ieeexplore.ieee.org/abstract/document/10559492) accepted in ***IEEE Systems Journal***

5. **December 2023**, received ***12th Grid India Power System Award*** by [**Grid-India**](https://www.linkedin.com/company/grid-controller-of-india-limited/posts/?feedView=all) for outstanding master's degree thesis in the area of power systems
