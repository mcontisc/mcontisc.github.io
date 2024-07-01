---
layout: page
title: Attributed multilayer networks
description: Perform inference on networks with metadata on both edges and nodes.
img: assets/img/project_1.jpg
importance: 1
category: work
related_publications: true
---

*Page under construction*

Advancements in data collection techniques have led to the acquisition of more comprehensive data, particularly by gathering additional information that characterizes the nodes and their interactions within real-world systems. These enriched data are effectively represented by <b>attributed multilayer networks</b>, which are complex network representations that describe <b>multiple types of interactions</b> among the same set of nodes, while also incorporating node information such as <b>attributes or covariates</b>. To properly analyze such data, models must integrate various sources of information in a convenient and principled manner, leveraging both the network topology and the node metadata.

We developed two distinct <b>probabilistic models</b>, named <code>MTCOV</code> {% cite contisciani2020community %} and <code>PIHAM</code> {% cite contisciani2024flexible %}, designed to perform <b>community detection</b> and broader <b>inference in attributed multilayer networks</b>. Both models posit the existence of a hidden <b>mixed-membership community structure</b> that drives the generation of both interactions and node attributes, but they differ in their model specification and inference.

Specifically, <code>MTCOV</code> is designed to handle categorical attributes and nonnegative discrete weights, specifying the likelihood of the data through a linear combination of the likelihoods from the two sources of information. Additionally, inference is performed using an efficient EM algorithm. On the other hand, <code>PIHAM</code> flexibly adapts to any combination of input data and employs a Bayesian framework combined with the Laplace matching technique to ease interpretation of inferred parameters. Furthermore, the algorithmic implementation relies on automatic differentiation, avoiding the need for explicit derivations. 

In addition to applying these methods to already explored real-world data, such as social and biological networks, we employed this methodology for the first time in the analysis of patent citation networks {% cite higham2022multilayer %}. In this context, we not only illustrated the importance of using a multilayer framework for patent citation data analysis but also emphasized the role of a node covariate in driving the inference, alongside the structural information embedded within the network.

<h3>Main takeaways</h3>
