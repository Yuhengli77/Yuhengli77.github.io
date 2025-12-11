---
layout: page
title: Research Project on Generative Engine Optimization
description: Yuheng Li, Stephen Liu, Victoria Jin, Simaran Malik
img: 
importance: 1
category: academic
related_publications: false
---
>
The transition from traditional blue links to AI-powered answer engines has spurred the emergence of Generative Engine Optimization (GEO). GEO improves content visibility in generative models, but it can introduce integrity concerns and contribute to a less transparent “AI dark funnel.” 
Our research approached this challenge in two main ways. First, we worked to increase the generative visibility of high-ranking search pages that are often overlooked by large language models. Second, we focused on identifying which types of content receive disproportionate attention from AI engines. To address the lack of a definitive ground truth, we used the discrepancy between Search Engine and Generative Engine rankings as an indicator of visibility differences.
We implemented and tested a Multi-Agent Content Optimization (MACO) pipeline. Through iterative, content-driven edits, we observed an increase in actual citations in live generative engine deployments. On the detection side, basic binary classifiers had difficulty distinguishing optimized content, but our application of a ListNet ranking model achieved an accuracy of 90.3%.

You can click [here](https://github.com/CSE291A-GEO/GEO) to see the GEO optimization Github Repository.