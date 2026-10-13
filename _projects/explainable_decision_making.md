---
layout: page
title: explainable decision-making
description:
img: assets/img/thumb_explainable.png
importance: 1
related_publications: true
---

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/explainability_layer.png" title="The logic-based explainability layer" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The logic-based explainability layer. Given a decision <i>d</i> from an AI model, a <i>monolithic explanation</i> is generated with respect to the AI system's knowledge base, while a <i>human-aware explanation</i> is generated with respect to both the AI system's and the human user's knowledge bases.
</div>

At its core, explaining a decision is a process of reverse inference: it involves backtracking from the decision to the reasons that support it. My PhD work argues that formal logic can serve as an *explainability layer* atop AI systems (see figure above). The idea is not to replace data-driven or other AI approaches with purely logical ones. Instead, the decisions of an AI system, whether symbolic or sub-symbolic, are captured in a formal logical language, which, thanks to its structured semantics, expressivity, and scrutability, supports exactly this kind of inference and reasoning. The result is explanations that are rigorous, flexible, and human-aware.

Within this layer, we distinguish between two kinds of explanations:

- A **monolithic explanation** is generated with respect to the AI system's knowledge base alone. It is a minimal set of the system's knowledge that entails the decision.
- A **human-aware explanation** is generated with respect to both the AI system's knowledge base and the human user's knowledge base. The user may reason about the problem with a different model than the system, so a decision that follows from the system's knowledge may not follow from the user's. A human-aware explanation updates the user's knowledge base so that the decision follows from it. This notion is rooted in *theory of mind*, the ability to attribute mental models to others while recognizing that these models may differ from one's own, and it generalizes the *model reconciliation problem* from the planning community to any problem that can be expressed in a logic for which satisfiability of subsets can be decided {% cite vas-jair22 %}.

Building on this foundation, we developed:

- efficient algorithms for computing explanations by exploiting hitting sets {% cite vas21 %};
- extensions to logic programs {% cite MRPLP %} and to probabilistic scenarios {% cite vas-jair25 tang2025PMRP %};
- personalized explanations via knowledge forgetting {% cite please-ecai %};
- visualizations for conveying explanations to users {% cite vizxp %};
- dialectical explanations through structured argumentative dialogues {% cite vasDR-Arg %};
- explanations for agent scheduling problems, including a hybrid logic–LLM system for course scheduling {% cite lasp-ecai trace-cs %}.

This work is collected in my dissertation, *[Explainable Decision-Making: From Formal Logic to AI Systems with Explainable Behavior](https://repository.library.washu.edu/cgi/viewcontent.cgi?article=2310&context=eng_etds)*, which received the [ICAPS Outstanding Dissertation Award](https://www.icaps-conference.org/icaps-awards/) and the [Turner Best Dissertation Award](https://cse.washu.edu/academics/graduate/Turner-Dissertation-Award.html) from Washington University in St. Louis.
