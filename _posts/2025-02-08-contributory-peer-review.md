---
title: 'Contributory Peer Review: A Fairer Academic Review System'
date: 2025-02-08
permalink: /posts/2025/02/contributory-peer-review/
tags:
  - academia
  - peer-review
  - research
excerpt: 'Proposing an equitable framework to assign reviewers based on authors' contribution to the peer review system.'
---

In this article, I propose a peer-review mechanism to provide a better alternative to the existing fragile peer review system in academia. In the following, I provide an equitable framework to assign reviewers of the submitted articles to a journal.

Let me first define a few notations that I will use later in this article (the reader can directly jump to the methodology section and come back here once required).

Suppose $N$ researchers write an article together and decide to submit it to a journal of their choice.

## Notation

1. **Author's score:** $a_i \in \mathbb{R}$ where $i \in [N]$ with $N$ being the total number of authors in a submitted article. This score signifies the expertise level of an academic researcher in a particular research area.

2. **Expertise threshold:** $a'$ - A threshold level of expertise of a researcher in a research area as decided by the editorial board of a journal.

3. **Review criterion:** $c_i \in \mathbb{R}$ where $i \in [N]$. It will be used as a criterion for evaluating the author's participation level in the peer review process.

4. **Author's contribution level:** $v_i \in (0,1]$ where $i \in [N]$. This is the level of the author's contribution to creating a research article, and it will be provided by the authors while submitting it to any journal.

5. **Historical contribution average:** $v'_i$ - the historical average of contribution level for author $i$ to the journal.

6. **Total submissions:** $p_i$ - total number of articles submitted by $i$ to a journal.

7. **Total publications:** $x_i$ - total number of articles published by $i$ in the same journal.

8. **Historical review score:** $r'_i$ - the historical average review score in $[0,1]$ received for $p_i$ articles of author $i$.

We define the author's score as:

$$a_i = \left(\frac{x_i}{p_i}\right) \times r'_i$$

## Methodology

The main idea of the Contributory Peer Review (CPR) mechanism is that every author is obliged to contribute to the peer review system of the journal where he/she wants to submit a research article. In other words, the submitted article will enter the peer review process of a journal only if the authors agree to contribute to the peer review system of that journal. I will now particularly focus on developing an algorithm to automate the reviewer allocation process among the authors.

## Algorithm

The following algorithm assigns research articles among the authors who have submitted their article to a journal.

**Input:** $\{v_i, v'_i, a_i, c_i, r'_i\}, \forall i \in [N]$
```
1:  for i in [N]:
2:      if a_i > a':
3:          c_i = c_i + v_i + v'_i × (x_i / p_i)
4:          if c_i ≥ 1:
5:              Send one article from similar research area to author i for reviewing
6:              Set c_i = 0
7:          end if
8:      end if
9:  end for
```

**Update:** Update and store $\{v'_i, p_i, a_i, c_i, r'_i\}$.

### Rationale

The rationale of **line 2** in the algorithm is obvious: a novice researcher should not review a paper. The idea behind the update of $c_i$ in **line 3** of the algorithm can be understood in two steps:

1. **First part:** The level of contribution for author $i$ of the submitted article should be proportionally reflected in his/her level of contribution in the peer review system.

2. **Second part:** The more an author's articles get published in a journal, the more he/she should review other articles.

## Summary

The above idea, if implemented with fairness, is expected to greatly regulate the scarcity of reviewers. Any further ideas for improvement are welcome in the comment section.

---

**Note:** Please cite this article if you use it for further research.

**Citation:**
```
Mallick, A. (2025). Contributory Peer Review: A Fairer Academic Review System. 
Retrieved from https://amallick-tudelft.github.io/posts/2025/02/contributory-peer-review/
```
