---
layout: papers
title: Multimodality Pain and related Behaviors Recognition based on Attention Learning
description: 15th IEEE International Conference on Automatic Face and Gesture Recognition (FG 2020), pp. 814 -- 818, Nov 2020
---

### Abstract:

Our work aimed to study facial data as well as movement data for recognition of pain and related behaviors in the context of everyday physical activities, which was provided as three tasks in EmoPain 2020 challenge. We explored deep visual representation and geometric features, which included head pose, facial landmarks, and action units in facial data with a combination of fully connected layers for estimating pain from facial data. In tasks with movement data, we employed long short-term memory layers to learn temporal information in each segment of 180 frames. We examined attention mechanism to investigate the relationship and gather data from multiple sources together. Experiments on EmoPain dataset showed that our methods significantly outperformed baseline results on pain recognition tasks.

[Full paper](https://ieeexplore.ieee.org/document/9320185) \| Code
<br/>

#### Evaluation

**EmoPain 2020** Pain Intensity Estimation from Facial Expression

Evaluation metric:  concordance correlation coefficient ($$\rho_{c}$$)

$$ \rho_{c}(y,\hat{y}) = \frac{2\sigma(y,\hat{y})}{\sigma(y,y) + \sigma(\hat{y},\hat{y}) + (\mu-\hat{\mu})^{2}} $$

<figure class="figure">
    <img class="rounded mx-auto d-block" src="/assets/img/papers/emopain_fg20_results.png" alt="EmoPain validation set results" width="90%" height="auto"/>
    <figcaption class="figure-caption" style="text-align:center;">Validation set results for pain estimation from facial features (EmoPain 2020).</figcaption>
</figure>

Our team won *1st place* :1st_place_medal: in EmoPain 2020 - Pain Intensity Estimation from Facial Expression.
<figure class="figure">
    <img class="rounded mx-auto d-block" src="/assets/img/papers/emopain_fg20_results_test.png" alt="EmoPain test set results" width="60%" height="auto"/>
    <figcaption class="figure-caption" style="text-align:center;">Test set results for pain estimation from facial features (EmoPain 2020) </figcaption>
</figure>

#### Citation

V. T. Huynh, H. -J. Yang, G. -S. Lee and S. -H. Kim, "Multimodality Pain and related Behaviors Recognition based on Attention Learning," *2020 15th IEEE International Conference on Automatic Face and Gesture Recognition (FG 2020)*, 2020, pp. 814-818, doi: 10.1109/FG47880.2020.00034.

**BibTeX**
```
@INPROCEEDINGS{9320185,
    author={Huynh, Van Thong and Yang, Hyung-Jeong and Lee, Guee-Sang and Kim, Soo-Hyung},
    booktitle={2020 15th IEEE International Conference on Automatic Face and Gesture Recognition (FG 2020)},
    title={Multimodality Pain and related Behaviors Recognition based on Attention Learning},
    year={2020},
    pages={814-818},
    doi={10.1109/FG47880.2020.00034}}
```

