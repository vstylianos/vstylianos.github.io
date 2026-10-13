---
layout: page
title: behavioral understanding
description:
img: assets/img/thumb_behavioral.jpg
importance: 3
related_publications: true
---

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/HAI_logo.png" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

AI agents that work with people need an accurate account of how people weigh evidence and change their minds, and this account has to come from real data on people. At the same time, the behavior of LLM-based agents cannot be derived from their design and has to be established empirically. This is the motivation behind *human-AI psychology*, where we study people and AI agents with the same experimental methods from cognitive science and cognitive psychology, both as they reason on their own and as they reason together.

**Belief revision in people and LLMs.** A central question for us is how people revise their beliefs when confronted with inconsistent information. In two human-subject experiments, we found that people do not simply make minimal changes to their beliefs, as classical belief revision theory assumes, but instead seek explanations for the inconsistency, which then guide their revision {% cite vasileiou2025explanation %}. More recently, we compared how people and LLMs revise their beliefs using a Bayesian analysis, and found that LLMs revise the same beliefs that people revise but do not extend the revision to related beliefs as people do {% cite COLMBR2026 %}.

**People interacting with AI agents.** Much of our earlier work on explainability was evaluated through user studies in which participants interact with an AI agent: correcting their plans based on an agent's explanations {% cite vas-jair22 %}, understanding explanations conveyed through visualizations {% cite vizxp %}, receiving personalized explanations {% cite please-ecai %}, engaging in argumentative dialogues with an agent {% cite vasDR-Arg %}, and choosing between privacy-aware and generic explanations from a scheduling agent {% cite lasp-ecai %}. These studies are, in essence, experiments in human-AI psychology, and their results inform how our agents model the people they interact with.
