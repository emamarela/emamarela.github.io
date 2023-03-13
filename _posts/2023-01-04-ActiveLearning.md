---
title: Active Learning for Multi-label Text Classiﬁcation with Transformers
layout: default
modal-id: 6
image: img/active.png
description: 
---
My thesis tested the feasibility of combining active learning (AL) with transformer models for multi-label text classification. Specifically, I investigated whether it was beneficial to use AL when the labeling budget was very small while retaining the powerful capabilities of BERT-like models. I chose multi-label classification instead of single-label because the benefits would be significant given the cost of an expert needed to spend time deciding all the possible labels that could apply to one data point. This was particularly an issue when labeling expansive text covering several pages and documents.

My focus was on practical real-world scenarios of multi-label text classification. Choosing the right classifier/learner in machine learning is challenging. This is even more difficult in the AL setting because:

The right learner needs to be selected using a very small amount of labeled data.

The learner's role is twofold: to make predictions and to work with a query strategy that helps refine it.

Choosing the right multi-label text classifier faces an output space being the power set of the set of classes, as it exponentially grows with the number of classes.

The growth of the output space more than often translates to a high class imbalance with the distribution of data per each class being unequal. Furthermore, characteristics of multi-label datasets like cardinality and density have been proven to be related to the difficulty of learning a multi-label classifier. [Bernardini et al., 2014]

Another facet of my research was a systematic investigation of different sampling strategies for pool-based active learning with a focus on uncertainty-based methods. Uncertainty-based query strategies are a computationally inexpensive alternative. Despite their relative disadvantages in traditional active learning, when paired with transformers, they are highly effective as well as efficient. [Schroder et al., 2021]

In classical AL strategies, the prediction probability of a model was used as a representation for how confident the model was. Deep neural networks are very complex and have many parameters. It is not a good predictor of model uncertainty because it tends to produce probabilities with very high confidence.

With this in mind, I compared different uncertainty selection strategies to assess their capabilities of choosing samples that were good representatives of the distribution of the pool of unlabeled data. Detailed information on my research and the full report can be found on my [GitHub](https://github.com/emamarela/ActiveLearning).





