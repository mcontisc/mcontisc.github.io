---
layout: page
title: Higher-order data
description: Perform inference on systems involving interactions between groups of nodes of any arbitrary size.
img: assets/img/project_2.jpg
importance: 2
category: work
related_publications: true
---

In recent years, real-world data from diverse domains, including social and biological systems, have revealed interactions that go beyond pairwise connections, involving groups of nodes of various sizes. <b>Hypergraphs</b> provide a versatile and comprehensive framework for characterizing systems where such higher-order interactions are relevant. Consequently, the models used to analyse such data must extend beyond conventional dyadic interactions (represented as $$ A_{ij} $$) and instead focus on <b>hyperedges</b>, referred to as $$ d $$-dimensional interactions $$ A_e $$, where $$ d = \|e\| $$.

The inherent higher-order structure within these hypergraphs offers <b>more realistic representations</b> of real-world data, and their analysis can yield a <b>deeper comprehension of the complex structure</b> underlying these systems. 

To this aim, we developed two distinct <b>probabilistic models</b> designed to perform <b>inference on hypergraphs</b> while capturing their hidden structural organization. These models, named <code>Hypergraph-MT</code> {% cite contisciani2022inference %} and <code>Hy-MMSBM</code> {% cite ruggeri2023community %}, posit the existence of a <b>mixed-membership community structure</b> as the main generative process, and utilize Poisson distributions to model the hyperedges. The main difference between the two approaches lies in how they integrate latent variables into the model, leading to two different assumptions about data generation. 

Specifically, <code>Hypergraph-MT</code> describes a hyperedge through the product of the memberships of all nodes involved, assuming exclusively assortative community structures to make this computation feasible. On the other hand, <code>Hy-MMSBM</code> relaxes the assortativity constraint and flexibly captures various community structures, such as disassortative and core-periphery. It achieves this by employing a bilinear form to link hyperedge probabilities and node community memberships.

These models, along with a broad range of other tools and algorithms for handling data with higher-order interactions, are available in the Python library <code>hypergraphx</code> {% cite lotito2023hypergraphx %}.

<h3>Main takeaways</h3>
<ul>
  <li>Our models reliably predict the existence of higher-order interactions of arbitrary size.</li>
  <li><code>Hypergraph-MT</code> detects communities that reliable depict the information carried by hyperedges and exhibit robustness against the addition of noisy interactions.</li>
  <li><code>Hy-MMSBM</code> consistently and accurately retrieves the planted communities in scenarios with varying hyperedges sizes. It also effectively captures assortative and disassortative community structures and correctly represents core-periphery configurations.</li>
</ul>

