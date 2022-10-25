---
layout: page
title: SpacePhish
tagline: Description and Resources
description: Website for SpacePhish
---


Welcome to the website related to the paper "_SpacePhish: The Evasion-space of Evasion Attacks against Phishing Website Detectors using Machine Learning_" accepted to [ACSAC22](https://www.acsac.org/).

We will [present the paper](https://www.openconf.org/acsac2022/modules/request.php?module=oc_program&action=program.php&p=program) in Austin (TX, USA) on Wednesday, Dec. 7th, 2022 (@13:30)!


---

### Summary: what did we do?

Our paper tackles the broad problem of adversarial attacks against Machine Learning (ML) systems---and specifically those for Phishing Website Detection (PWD). Put simply, we make two contributions: a conceptual one, and an empirical one.

* **(conceptual) We formalize the "evasion-space" of adversarial perturbations.** Our formalization focuses on the _capabilities_ of an attacker: instead of the common "[white-/black-box](https://www.sciencedirect.com/science/article/pii/S0031320318302565)" threat models (focusing on the _knowledge_), we envision an attacker that can influence the ML-PWD in three different spaces: either _outside_ the ML-PWD (i.e., the "website-space"), or _inside_ the ML-PWD (i.e., either in the "preprocessing-space", or in the "machine learning-space").
  * **Why is this relevant?** Because, up until this day, there was a stark contrast between attacks entailing perturbations created in the "feature-space" and those in the "[problem-space](https://ieeexplore.ieee.org/abstract/document/9152781)": typically, papers that considered the former were deemed to be unreliable due to the well-known "inverse mapping problem" which -- if not addressed -- could yield "[unrealizable perturbations](https://www.usenix.org/conference/usenixsecurity19/presentation/tong)". _Our formalization shows that both cases are likely to occur_: it is simply necessary to assume that perturbations created in the "feature-space" are harder to apply (i.e., they have a higher cost).
* **(empirical) We perform a massive evaluation of evasion attacks against ML-PWD.** We make a fair comparison of attacks entailing perturbations crafted in different "spaces". We assess the robustness of 900 ML models (using diverse datasets, ML algorithms, and feature sets), and we derive statistically significant conclusions by assessing each of these against 1200 adversarial examples. 
  * **What did we find?** Our results show that, in some cases, _cheap perturbations_ (i.e., adding some fake links to the HTML) can induce a statistically significant degradation. Of course, perturbations in the feature space are more disruptive, but they require a compromise of the ML-PWD. Moreover, we also attack the "real" ML-PWDs of a well-known evasion competition, [MLSEC](https://mlsec.io/). We found out that our _cheap perturbations_ were enough to significantly decrease their confidence (sometimes by over 50%!).

**So what?** The evaluations of *any* paper whose perturbations were crafted in the "feature-space" can be considered 100% reliable---under the condition that the attacker is stronger because they can access the _internal_ elements of a ML-PWD. Furthermore, the fact that _cheap perturbations_ are effective raises an important alarm: in the context of phishing websites, such perturbations are way more likely to appear in reality due to their low barrier of entry (compared to traditional "gradient-based" techniques). 

### Demonstrative Video

**But what do we mean by _cheap perturbations_?** On the very last day of the MLSEC challenge, we recorded a demonstrative video showing the entire attack. Specifically:
* from its conception ("what is the first thing that an attacker would do?" → probably a Google search!)...
* ...to its execution ("how would an attacker implement their strategy?" → write some simple code!)...
* ...and, finally, to its impact ("will it really work?").

You can see the results yourself in the video below (watch it in 1080p for better details)!

<iframe width="560" height="315" src="https://www.youtube.com/embed/06G24tM3SPE?rel=0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

---

### Artifact and Resources

We submitted an Artifact of our paper to the ACSAC [Artifact Evaluation](https://www.acsac.org/2022/program/artifacts/), and we received a "Reusable" badge! Moreover, during the evaluation, the reviewers were able to replicate the results achieved in our paper. 

<a href="https://www.acm.org/publications/policies/artifact-review-badging" target="_blank"><img src="{{ BASE_PATH }}/assets/artifacts_evaluated_reusable.png" alt="ACM Reusable Artifact" width="100"/></a>


We publicly release all the material  of our Artifact. Specifically:
* [GitHub repository](https://github.com/hihey54/acsac22_spacephish), containing the source-code and instructions to replicate our results;
* [Supplementary Document]({{ BASE_PATH }}/docs/ACSAC22_SpacePhish-supp.pdf) containing the complete results (including those on the ML-PWDs of [MLSEC](https://mlsec.io/));
* [Preprint]({{ BASE_PATH }}/docs/ACSAC22_SpacePhish.pdf) of the main paper.

If you use any of such resources, we kindly ask you to cite our paper  with the following BibTeX entry:
```
@inproceedings{apruzzese2022spacephish,
  title={SpacePhish: The Evasion-space of Evasion Attacks against Phishing Website Detectors using Machine Learning},
  author={Apruzzese, Giovanni and Conti, Mauro and Yuan, Ying},
  booktitle={Proceedings of the Annual Computer Security Applications Conference (ACSAC)},
  year={2022},
  publisher={ACM, New York, USA},
  doi={10.1145/3564625.3567980}
} 
```

#### Contact
Feel free to reach out to us! You can contact either [Giovanni Apruzzese](mailto:giovanni.apruzzese@uni.li) or [Ying Yuan](mailto:ying.yuan@studenti.unipd.it). You can also post a comment on the [discussion page](https://github.com/hihey54/acsac22_spacephish/discussions/) of the GitHub repository.