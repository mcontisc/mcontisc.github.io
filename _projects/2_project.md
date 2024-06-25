---
layout: page
title: Higher-order data
description: Perform inference on systems involving interactions between groups of nodes of any arbitrary size.
img: assets/img/project_2.jpg
importance: 2
category: work
related_publications: true
---

*Page under construction*

Over the past few years, real-world data from diverse domains, including social and biological systems, have revealed interactions that go beyond pairwise connections, involving groups of nodes of various sizes. <b>Hypergraphs</b> provide a versatile and comprehensive framework for characterizing systems where such higher-order interactions are relevant. As a result, the models used to analyse such data must extend beyond conventional dyadic interactions (represented as $$ A_{ij} $$) and instead focus on <b>hyperedges</b>, referred to as $$ d $$-dimensional interactions $$ A_e $$, where $$ d = \|e\| $$.

The inherent higher-order structure within these hypergraphs offers <b>more realistic representations</b> of real-world data, and their analysis can yield a <b>deeper comprehension of the complex structure</b> underlying these systems. 


This understanding can be achieved through the application of community detection algorithms, which are capable of identifying the mesoscale organization of real-world data


In Section 3.3, we describe techniques to characterize the structural organization of higher- order data. This section includes three peer-reviewed publications. Two of these present mathematical approaches for performing inference on hypergraphs, while the third work introduces a Python library that offers a broad range of tools and algorithms to handle data with higher-order interactions.

The first two publications introduce distinct frameworks aimed at characterizing the structural organization of hypergraphs. Both methods adopt a mixed-membership structure as generative process, and utilize Poisson distributions to model the hyperedges. Nevertheless, they diverge in their approach to defining the mean of the marginal distributions. Specifically, Hypergraph-MT describes a hyperedge by considering the product of the node memberships belonging to it, whereas Hy-MMSBM employs a bilinear form for capturing dependencies within the hyperedges.
The third work is computational and introduces the Python library hypergraphx, which is openly available and serves as a valuable resource for analyzing networked systems with higher-order interactions. This library offers a broad range of tools and algorithms for constructing, visualizing, and analyzing data with higher-order interactions.


In Section 3.3.1 and Section 3.3.2, we expounded two distinct probabilistic models designed to perform inference on hypergraphs while capturing their hidden organization. These models, named Hypergraph-MT [37] and Hy-MMSBM [134], posit the existence of a mixed-membership community structure as the main mechanism driving hyperedge formation. Such assumption was not explored in the analysis of hypergraphs before. In particular, our models are well-suited for analyzing nonnegative discrete weighted hyperedges, which are mathematically represented using Poisson distributions. The main difference between the two approaches lies in how they integrate latent variables into the model, leading to two different assumptions about data generation. Specifically, Hypergraph-MT expands upon Multitensor– the model presented in Section 2.3.3 – and describes a hyperedge through the product of the memberships of all nodes belonging to it. To make this computation feasible, Hypergraph-MT assumes the existence of exclusively assortative community structures, which is a reasonable assumption in a variety of contexts. On the other hand, Hy-MMSBM relaxes the assortativity constraint and flexibly captures various community structures that were not tackled in the literature, such as disassortative and core-periphery, among others. To achieve this, it employs a bilinear form to link hyperedge probabilities and node community memberships. In addition to introducing these foundational models, we have also developed a new Python library, named hypergraphx [96], which provides a wide range of tools and algorithms for handling higher-order data. This computational effort, combined with comprehensive and user-friendly tutorials, enhances the usability of our methods. Furthermore, together with a few other recent and existing packages [6, 7, 93, 128], our contribution makes the analysis of real-world higher-order data more accessible, thus advancing our understanding of these complex systems.

<!---
Briefly explain the models and the library. Hypergraph-MT, Hy-MMSBM, HGX

Present some results with some plots.

--->

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/3.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Caption photos easily. On the left, a road goes through a tunnel. Middle, leaves artistically fall in a hipster photoshoot. Right, in another hipster photoshoot, a lumberjack grasps a handful of pine needles.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/5.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This image can also have a caption. It's like magic.
</div>

You can also put regular text between your rows of images, even citations {% cite contisciani2022inference %} {% cite lotito2023hypergraphx %} {% cite ruggeri2023community %}.
Say you wanted to write a little bit about your project before you posted the rest of the images.
You describe how you toiled, sweated, _bled_ for your project, and then... you reveal its glory in the next row of images.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    You can also have artistically styled 2/3 + 1/3 images, like these.
</div>

The code is simple.
Just wrap your images with `<div class="col-sm">` and place them inside `<div class="row">` (read more about the <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a> system).
To make images responsive, add `img-fluid` class to each; for rounded corners and shadows use `rounded` and `z-depth-1` classes.
Here's the code for the last row of images above:

{% raw %}

```html
<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/6.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
  <div class="col-sm-4 mt-3 mt-md-0">
    {% include figure.liquid path="assets/img/11.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
  </div>
</div>
```

{% endraw %}