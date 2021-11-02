---
layout: papers
title: Engagement Intensity Prediction with Facial Behavior Features
description: ICMI'19 - 2019 International Conference on Multimodal Interaction, pp. 567 -- 571, Oct 2019
---

### Abstract:

This paper describes an approach for the engagement prediction task, a sub-challenge of the 7th Emotion Recognition in the Wild Challenge (EmotiW 2019). Our method involves three fundamental steps: feature extraction, regression and model ensemble. In the first step, an input video is divided into multiple overlapped segments (instances) and the features extracted for each instance. The combinations of Long short-term memory (LSTM) and Fully connected layers deployed to capture the temporal information and regress the engagement intensity for the features in previous step. In the last step, we performed fusions to achieve better performance. Finally, our approach achieved a mean square error of 0.0597, which is 4.63% lower than the best results last year.

[Full paper](https://dl.acm.org/doi/abs/10.1145/3340555.3355714) \| [Poster](/assets/pdf/ICMI19_EG_poster.pdf) | Code
<br/>

#### Evaluation

**EmotiW 2019** Engagement prediction

<figure class="figure">
    <img class="rounded mx-auto d-block" src="/assets/img/papers/eg_emotiw19_results.png" alt="EmotiW 2019 Engagement test set results" width="60%" height="auto"/>
    <figcaption class="figure-caption" style="text-align:center;">EmotiW 2019 Engagement test set results.</figcaption>
</figure>

Our team **SML** won *1st place* :1st_place_medal: in EmotiW 2019 - Engagement prediction task.
<figure class="figure">
    <img class="rounded mx-auto d-block" src="/assets/img/papers/eg_emotiw19_results_ranked.png" alt="EmotiW 2019 Engagement test set results ranked" width="60%" height="auto"/>
    <figcaption class="figure-caption" style="text-align:center;">MSE based comparison of the EP sub-challenge participating methods. Source: https://researchmgt.monash.edu/ws/portalfiles/portal/288645367/288531253_oa.pdf </figcaption>
</figure>

#### Citation

Van Thong Huynh, Soo-Hyung Kim, Guee-Sang Lee, and Hyung-Jeong Yang. 2019. Engagement Intensity Prediction with Facial Behavior Features. In *2019 International Conference on Multimodal Interaction (ICMI '19)*. Association for Computing Machinery, New York, NY, USA, 567–571. DOI: 10.1145/3340555.3355714

**BibTeX**
```
@inproceedings{thong2019engagement,
  title = {Engagement Intensity Prediction with Facial Behavior Features},
  author = {Huynh, Van-Thong and Kim, Soo-Hyung and Lee, Guee-Sang and Yang, Hyung-Jeong},
  booktitle = {2019 International Conference on Multimodal Interaction},
  pages = {567--571},
  year = {2019},
  doi = {10.1145/3340555.3355714},
}
```
