---
layout: page
title: synergistic decision-making
description:
img: assets/img/thumb_synergistic.jpg
importance: 2
related_publications: true
---

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/asimov_triptych.jpg" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

Explanations alone do not make a person and an AI agent good partners. For decisions that remain the responsibility of a person, such as those in public policy, the agent should support the person's reasoning rather than replace it. In our AAMAS 2026 Blue Sky paper {% cite LLM+Arg26 %}, we argue for *argumentative human-AI decision-making*, in which AI agents reason *with* us, not *for* us. In this setting, the person and the agent reach a decision over a shared, explicit representation of the arguments for and against it, so that every position can be inspected, contested, and revised as the interaction unfolds.

Computational argumentation provides the formal layer for this vision, and LLMs connect it to natural language and to real-world sources. Our work along this direction includes:

- *dialectical reconciliation*, in which an agent and a person resolve differences in their understanding through structured argumentative dialogues {% cite vasDR-Arg %};
- approximating and personalizing an agent's model of the person from argumentation-based dialogue traces {% cite approximate_tang %};
- a methodology for incompleteness-tolerant and modular gradual semantics for argumentative statement graphs {% cite Arg-methodology %};
- a hybrid LLM–symbolic framework that extracts argumentation graphs from real disaster governance policy documents to support discourse-aware policy analysis {% cite vasileiou2026discourse %}.
