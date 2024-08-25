---
layout: page
title: Handling reciprocity
description: Perform inference on networks by incorporating reciprocity as mechanism for tie formation.
img: assets/img/project_3.jpg
importance: 3
category: work
---

<b>Directed networks</b> represent real-world data where interactions have a specific direction. Traditional approaches for analyzing these networks often rely on community detection algorithms, which assume that interactions are solely determined by hidden partitions of nodes. However, many real networks exhibit other mechanisms that influence tie formation, such as <b>reciprocity</b>—the tendency of a pair of nodes to form mutual connections. To effectively account for reciprocity, standard generative models must go beyond the assumption of <b>conditional independence</b> and instead model the edges between node pairs jointly, rather than treating them as independent.

We developed several <b>probabilistic models</b> aimed at performing <b>inference in directed networks</b> by incorporating reciprocity. The foundational methods, <code>CRep</code> {% cite safdari2021generative %} and <code>JointCRep</code> {% cite contisciani2022community %}, offer two distinct approaches to <b>combine both reciprocity and community structure</b> within unique probabilistic methods for network analysis. These methods relax the conditional independence assumption and explicitly model the <b>pairwise dependencies</b> between directed edges connecting node pairs, with differences in their generative processes.

Specifically, <code>CRep</code> is designed for analyzing directed networks with nonnegative discrete weights, utilizing Poisson distributions to model the conditional distributions and a pseudo-likelihood approximation to represent the network's likelihood. In contrast, <code>JointCRep</code> uses a Bivariate Bernoulli distribution to model the joint distribution of edges between node pairs in a closed form, making it suitable for analyzing binary directed networks.

Furthermore, we extended these frameworks to address other scenarios and applications: <code>DynCRep</code> {% cite safdari2022reciprocity %} extends <code>CRep</code> to analyze <b>dynamic networks</b>, which are networks that change over time; <code>CRAD</code> {% cite safdari2023anomaly %} builds on the formalism of <code>JointCRep</code> to develop a probabilistic generative approach for <b>anomaly detection</b> on network edges; and <code>VIMuRe</code> {% cite debacco2023latent %} is a method to estimate the <b>unobserved network structure from multiply reported data</b>, incorporating a reciprocity parameter based on the principles of <code>CRep</code>, reflecting the intuition that reporters tend to nominate the same individuals in both directions of a relationship.

<h3>Main takeaways</h3>
<ul>
  <li>Explicitly modeling pairwise dependencies increases results robustness and boosts performance in prediction and network reconstruction tasks.</li>
  <li>Our frameworks accurately capture reciprocity and other model parameters, while also estimating the relative contributions of community structure and reciprocity in determining individual edges.</li>
  <li>Our methods function not only as tools for network inference but also as benchmark models, capable of generating synthetic data that align with the underlying assumptions of each algorithm.</li>
</ul>

