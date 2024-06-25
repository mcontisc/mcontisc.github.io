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

In recent years, real-world data from diverse domains, including social and biological systems, have revealed interactions that go beyond pairwise connections, involving groups of nodes of various sizes. <b>Hypergraphs</b> provide a versatile and comprehensive framework for characterizing systems where such higher-order interactions are relevant. Consequently, the models used to analyse such data must extend beyond conventional dyadic interactions (represented as $$ A_{ij} $$) and instead focus on <b>hyperedges</b>, referred to as $$ d $$-dimensional interactions $$ A_e $$, where $$ d = \|e\| $$.

The inherent higher-order structure within these hypergraphs offers <b>more realistic representations</b> of real-world data, and their analysis can yield a <b>deeper comprehension of the complex structure</b> underlying these systems. 

To this aim, we developed two distinct <b>probabilistic models</b> designed to perform <b>inference on hypergraphs</b> while capturing their hidden structural organization. These models, named `Hypergraph-MT` {% cite contisciani2022inference %} and `Hy-MMSBM` {% cite ruggeri2023community %}, posit the existence of a <b>mixed-membership community structure</b> as the main generative process, and utilize Poisson distributions to model the hyperedges. The main difference between the two approaches lies in how they integrate latent variables into the model, leading to two different assumptions about data generation. 

Specifically, `Hypergraph-MT` describes a hyperedge through the product of the memberships of all nodes belonging to it. To make this computation feasible, it assumes the existence of exclusively assortative community structures, which is a reasonable assumption in a variety of contexts. On the other hand, `Hy-MMSBM` relaxes the assortativity constraint and flexibly captures various community structures, such as disassortative and core-periphery. It achieves this by employing a bilinear form to link hyperedge probabilities and node community memberships. 

These models, along with a broad range of other tools and algorithms for handling data with higher-order interactions, are available in the Python library `hypergraphx` {% cite lotito2023hypergraphx %}.


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

You can also put regular text between your rows of images, even citations   .
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

