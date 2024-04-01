---
layout: page
title: model reconciliation
description:
img: assets/img/tom.jpeg
importance: 1
category: Explainable Planning & Scheduling
related_publications: true
---





<div class="row justify-content-sm-center">
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/tom.jpeg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>     

The *Model Reconciliation Problem* (MRP) is a paradigm originated in the planning community as a method for explaining plans to human users. It has gained a lot of success due to the fact that it is rooted in the understanding of the importance of the so-called *Theory of mind*. This (normative) theory is used to explain some operations of the human mind and behavior in social and collaborative (or even adversarial) scenarios. In  a  nutshell, the Theory of Mind is the ability to attribute mental models to others while recognizing that these models may differ from one’s own. Now, in the context of MRP and planning, an AI agent and a human user typically have their own models that characterize the particular planning problem (e.g., fluents, actions, etc.). When these two models diverge, such that a valid plan in the agent's model is invalid in the human's model, the agent seeks to generate an *explanation* to reconcile these differences. The explanation is then used to update the human model, thus making the agent's plan valid in the human's (updated) model.

In my research, we have approached MRP from the perspective of knowledge representation and reasoning, where now the models of the agent and the human user are expressed in an appropriate logical formalism. By using logic, we have generalized MRP to problems beyond planning, so long as these problems can be expressed in some logic for which satisfiability of subsets can be decided.

<!-- {% cite please-ecai %} -->
<!-- {% cite vas-jair22 %} -->
<!-- {% cite vizxp %} -->
<!-- {% cite MRPLP %} -->
<!-- {% cite vas21 %} -->