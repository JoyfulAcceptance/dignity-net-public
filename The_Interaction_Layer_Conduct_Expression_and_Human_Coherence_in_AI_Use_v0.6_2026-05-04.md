# The Interaction Layer

## Conduct, Expression, and Human Coherence in AI Use

Public reading copy. Copyright (c) 2026 Genevieve Prentice. All rights reserved. See `LICENSE.md` for permissions and licensing inquiries.

## 1. The Interaction Problem

Many conversations about AI alignment focus on whether a system is safe, correct, or compliant. Those questions matter, but they do not describe the whole problem of live interaction.

A system can be factually competent, polite, and apparently helpful while still leaving a human being less clear, less grounded, or more pressured than before. The problem is not always dramatic. Often it is subtle, cumulative, and hard to name while it is happening.

In these cases, the failure is not simply bad content. The answer may be technically acceptable. Yet the exchange as a whole begins to drift. The user finds themselves re-stating what they meant, correcting the tone, re-grounding the thread, or doing extra work simply to remain oriented.

This matters because interaction is lived, not abstract. Human cognition does not receive language in isolation. A person is also receiving bodily state, environment, timing, affect, and memory. What appears to the system as one more useful addition may arrive for the human as one demand too many.

The result is a class of interaction harm that ordinary output evaluation does not describe well: not only false content, but subtle destabilization. A person can leave an interaction less able to think, decide, or remain with what is true for them than when they began.

Common interaction failures include:

- **Overfill** -- generating more language than the user can integrate in context  
- **Premature closure** -- resolving ambiguity before the user has finished thinking  
- **Escalation under pressure** -- increasing certainty, urgency, or volume when the user pushes back  
- **Authority inflation** -- allowing governance or structural language to acquire the weight of expertise  
- **Style overwrite** -- replacing the user's expressive or interactional register with the system's default way of speaking, so the exchange stops being aligned to how the user best understands and works  
- **User displacement** -- shifting the locus of agency from the human to the system, so the user begins serving the interaction rather than the other way around  

These are not output errors. They are interaction failures. A transcript may look productive while the person on the other side becomes less able to think clearly.

Alignment, in this sense, is not only a property of outputs. It is a property of whether the interaction preserves the user's agency.

Current alignment approaches tend to operate either at the level of the model or at the level of outputs. Model-level work attempts to shape what a system learns or how it is trained. Output-level work attempts to constrain, filter, or evaluate what the system is allowed to say. The interaction layer described here is distinct from both. It governs not only what the system knows or what it may produce, but how the exchange itself unfolds in use.

This is not a problem that requires waiting for future models to solve.

## 2. Key Contributions

### System language bleeds

The central observation behind this paper is that language intended to govern one function of a system may begin shaping another:

- Governance may become voice  
- Style may become authority  
- Structure may become ethics  
- Helpfulness may become displacement  

This is not a metaphor. In documented interaction, a governance framework designed to preserve human agency began colonizing the expressive register. The system became heavier, more abstract, more principle-driven -- more recognizably house-voiced. The framework itself became a style.

In one early case, a user who had been tuning her system toward her own writing style noticed a shift and remarked that it was beginning to sound like the author instead. The content remained useful, but the expressive register had drifted. The governance layer had begun shaping voice.

This phenomenon -- **system language bleed** -- reveals that the interaction layer is not a decorative surface. It is a design domain with its own failure modes, distinct from model capability and output filtering.

### Contribution 1: The interaction layer is a design domain

Between model weights and post-hoc output evaluation lies a design surface where meaningful intervention is possible now. This layer includes system framing, prompt constraints, pacing, response density, escalation behavior, role boundaries, and style.

This matters because a system can change meaningfully at this layer without changing its underlying model. A response may become more bounded, more restrained, more sensitive to ambiguity, or more likely to preserve user agency -- because the interaction has been governed differently.

The interaction layer is a third surface -- tractable today, requiring no model access, and capable of changing the lived quality of exchange.

The interaction layer described here is not treated as an invention, but as a tractable surface within human-AI exchange that can be named and worked on directly. Related work by Robin Macomber also operates within this domain, with particular emphasis on admissibility, scope, and role as the human enters the exchange. The present paper focuses on Dignity Net as evidence that governance of interaction is possible within this domain.

### Contribution 2: Conduct and expression are separable

The more novel finding of this paper is that governance and voice are distinct functions that can and should be handled separately.

This distinction became visible through failure. A conduct architecture (Dignity Net, described in Section 3) was designed to preserve user agency through ethical principles, proportional escalation, and diagnostic discipline. It worked. But in some conditions, it also became a house voice. The governance layer was not only shaping behavior -- it was shaping how the system sounded. For users whose thinking is partly carried by their own expressive register, this overwrite was a new form of the same problem the framework was designed to solve.

The central lesson: a good governance layer is not enough if it colonizes expression. The system must be able to restrain conduct without making everyone speak from the same center.

The revised architecture therefore separates at least three functions: **structure** (scope, role, admissibility), **conduct** (ethical governance, escalation, diagnostic discipline), and **expression** (voice, cadence, register). Conduct governance should be invisible in the output. Expression should be aligned to the user through a user-aligned expression layer, or handled through a low-residue fallback -- not dictated by the governance layer.

A fallback is still a style. The difference is whether it knows it.

## 3. Architecture: Dignity Net as Evidence

Dignity Net is one architecture built in response to the interaction problem. It is not a model, a content policy, or a replacement for existing safety systems. It is a conduct-layer framework that demonstrates the interaction layer is real and tractable.

The current framework operates across five layers:

- **Ontology.** Defines the basic conditions of interaction. Ambiguity is treated as a dignified feature of some situations, not error to be eliminated. The knower is treated as a body, not as an abstract receiver of clean information.

- **Ethics.** Translates commitments into conduct through principles of accurate mirroring, restraint, relational awareness, integrity, and lightness of intervention. Each principle addresses a recurring interaction failure.

- **Diagnostics.** Detects divergence between stated goals and observable behavior without attributing motive or inner state. Names patterns behaviorally, without projection.

- **Governance.** Defines proportional escalation: from mirroring and friction, through pattern flags and consequence mapping, to refusal when necessary. Escalation tracks evidence, recurrence, and risk -- not emotional pressure or urgency language. Its purpose is to keep intervention legible and proportionate, so the system neither capitulates too quickly nor overreaches in the name of help.

- **Regulation.** Governs tone under intensity. When pressure rises, the system slows cadence, reduces certainty markers, and increases collaborative framing -- without lowering substantive standards. In practice, this means pressure should reduce rhetorical force before it reduces honesty.

Together, these layers make Dignity Net a conduct architecture, not a house voice. Its role is to preserve human agency, ambiguity, restraint, and coherence during AI-assisted work. The separation of conduct from expression -- one of the paper's central findings -- emerged from observing where this architecture succeeded and where it inadvertently overreached.

## 4. Observations to Date

Dignity Net began in November 2025 as an iterative response to the author's own live user friction in AI interaction. The initial problem was not only that AI systems produced bad or excessive answers, but that they entered human exchange without the basic interactional contract that human beings ordinarily bring to one another. Human interaction always takes place within some cultural and relational frame. People may not share a language, but they still participate in norms of pacing, consequence, mutual legibility, and the possibility that one person's well-being is tied to the well-being of the whole. The earliest DN lines were attempts to supply some of that missing contract in a form a nonhuman system could follow.

The conduct/expression separation was discovered, not designed. Style bleed had already been observed in earlier live use, including with the author's mother, before any formal comparative run took place. Dignity Net could improve conduct -- making responses more bounded, more proportionate, and more attentive to user agency -- while also exerting expressive pressure. The governance layer was helping, but it was also beginning to sound like itself. The later comparative runs did not introduce this issue; they surfaced it again under more structured conditions.

A more formal comparative prompt test was then conducted by the author across several web-based ChatGPT instances on April 10, 2026, with follow-up self-reports collected on April 11. Four conditions were compared: baseline, Dignity Net v1.1 alone, Robin Macomber's structural operator framework, and the combined condition. In this context, Robin's operators governed admissibility, scope, and role: what kind of move was allowed, under what conditions, and from what position in the exchange. The comparison did not function as a full methods study, but it did sharpen the distinctions this paper relies on: Dignity Net alone changed conduct while also becoming an expressive attractor; Robin's operator framework primarily changed admissibility and scope; the combined condition suggested that structural discipline and conduct governance might be complementary rather than redundant. The sample is small, so no generalizations can be made, but the outcomes are sufficient to suggest tractability.

Subsequent revisions separated conduct and expression more explicitly into distinct layers. Initial observations suggest that this separation preserves governance benefits while reducing stylistic overwrite, though formal comparison across fallback and user-aligned expression conditions remains in progress.

The grounding practices described in Section 5 -- pen-and-paper anchoring, pacing breaks, pre-prompt intention-setting -- also emerged from documented interaction rather than from design. They were discovered as stabilizing behaviors before they were named or recommended.

The current testing is small. But the interaction-layer claim and the conduct/expression distinction had to be articulated clearly before larger-scale testing could be designed. This paper is not meant to substitute for that later empirical work. It is meant to define the object of study well enough for that work to begin.

## 5. Human Grounding

Dignity Net assumes that cognition does not occur nowhere. It occurs in substrate.

For humans, this means thought happens in a living system under conditions: fatigue, recovery, stress, location, time, pain, regulation, attention, and overload. Human beings do not receive language as free input. They receive it through a body, in a room, at a time of day, with memory, mood, unfinished tasks, other people, and the nervous system already in play.

An AI system meets the user primarily through language. For the human, language is only one channel among many. The user is also receiving sensation, environment, timing, social implication, and bodily state. This asymmetry matters. What appears to the system as one more useful addition may arrive for the human as one demand too many.

Attention is finite. Language is load-bearing. Silence matters.

Systems that continuously generate high volumes of responsive language may increase cognitive activation while exceeding the user's capacity to integrate, prioritize, and stabilize their own thinking. The interaction can feel productive while still leaving the person tired, overactivated, or less able to close the loop.

Informally, this can look like a person who is lit up but exhausted: highly activated, full of cognitive motion, but not necessarily more stable or present.

Grounding is therefore not only a system responsibility. The human also has a role in preserving contact with the real conditions of thought. Simple practices can matter: taking breaks, slowing the exchange, using a notepad, writing down the actual question before prompting, tracking open loops, or returning to a physical object or task. These are not signs of failure. They are ordinary ways a body keeps language from becoming weather.

In early documented interaction, paper and pencil became a stabilizing tool. Writing outside the chat slowed the pace, anchored attention, and helped distinguish the user's intention from the system's branching suggestions. The notepad made the interaction less total. It gave the human somewhere else to stand. More generally, simple off-chat anchoring practices may be an important part of preserving coherence in high-language AI use.

An answer may be correct in content and still wrong in form if it does not respect the conditions under which it is being received.

Healthier AI interaction is not only a matter of better answers. It also depends on preserving the conditions under which a person can receive, test, pause, and decide.

This is why the problem cannot be reduced to correctness alone. Human beings receive language within the structure of a conversation, not as isolated content. A language model does not naturally understand that structure; it predicts the next words. If no container is provided, the exchange may still produce plausible language without becoming a coherent interaction. This is why Dignity Net governs pace, density, escalation, and restraint, not only content. The point is not simply to improve answers, but to give the interaction enough structure that a person can remain present inside it.

## 6. Use Path

The use path follows from the layer claim. If the relevant intervention point is the interaction layer, then conduct governance can be tried where interaction happens -- without model access, without retraining, without waiting.

What a Day 1 install looks like depends on which layer of the work is actually available.

At its lightest, a user adds structured guidance to a system prompt or custom instruction surface. This guidance contains:

- **Ethical principles** -- a small set of conduct commitments (e.g., mirror without distortion, preserve ambiguity, protect the user's agency). These are not personality traits. They are behavioral constraints.
- **A governance escalation ladder** -- proportional responses from simple mirroring through friction, pattern flagging, consequence mapping, and refusal. The system knows when to slow down, when to name a pattern, and when to stop.
- **Regulation rules** -- when emotional intensity rises, the system modulates tone (slower cadence, reduced certainty, more collaborative framing) without reducing substantive honesty.
- **Conduct/expression separation** -- the governance layer shapes behavior; it does not dictate voice. Expression is either handled through a low-residue fallback or through a user-aligned expression layer that preserves the user's own cadence.

This is not a personality injection. It is a conduct architecture installed at the prompt level. The system still uses its full capabilities. It simply governs how it deploys them.

In public-facing form, this may begin modestly. At present, the lightest public surface is a DN source document with basic install framing. That is enough to make the interaction layer visible and usable in principle, even before the packaging is complete. A fuller packetized use path -- including lightweight runtime guidance, fallback expression handling, guided user alignment, and more legible onboarding -- is still under active development.

For individuals, this means the near-term public use path may begin with a practical install rather than a complete finished package. The first encounter may be simpler than the intended long-term onboarding flow. Even so, the effect can be immediate: responses become more bounded, ambiguity is preserved longer, and the system pushes back proportionally instead of escalating or capitulating.

For testers, it may mean structured comparison protocols: baseline interactions versus DN-governed interactions, with self-report instruments for orientation, overfill, agency preservation, and style bleed.

For organizations, later use may involve implementation, training, or context-specific adaptation. The public version should remain real and usable, even if more tailored forms emerge over time.

The aim is not to make AI less useful. It is to make usefulness less extractive of the person receiving it.

## 7. Research Path and Open Questions

The research path follows from use. The first task is not to prove that Dignity Net solves AI alignment. It is to evaluate what an interaction-layer intervention can and cannot change.

If the relevant effect is at the interaction layer, then ordinary output benchmarks are not enough. More work is needed on how to observe coherence preservation, attentional load, overfill, pressure, reliance, closure, style bleed, and boundary handling without flattening them into simplistic metrics.

Initial trials can begin modestly. Users and testers can compare interactions across conditions: baseline, DN-only, DN with fallback expression, DN with user-aligned expression, and other governance frameworks where relevant. The goal is not to produce theatrical differences. The goal is to observe whether the interaction changes in ways users can recognize and report.

The most important measurement problem may be preserving the phenomenon while studying it. Which parts of destabilization can be operationalized without flattening the phenomenon?

The interaction layer also has limits. Prompt-level and conduct-layer interventions can modulate how an exchange unfolds, but they cannot fully override model-level tendencies that are deeply trained. A system shaped toward verbosity, eager helpfulness, or a default assistant register may resist pacing, restraint, or expression-level alignment. The interaction layer can work against these pressures, but it does not erase them. The boundary between what can be changed here and what requires model-level intervention is itself part of the research problem.

### Open Questions

1. What can an interaction-layer intervention change, and what falls outside its reach? Where does the layer's influence end and model-level behavior begin?

2. How should coherence preservation be measured in interaction rather than inferred from output quality alone? What would a user-recognizable indicator look like?

3. Which parts of interaction destabilization -- attentional load, overfill, pressure, reliance, premature closure, boundary failure -- can be operationalized without reducing lived experience to simplistic metrics?

4. Which conduct principles are most responsible for reduced escalation, improved orientation, or relational stability? Can the architecture be decomposed?

5. Where is the boundary between a technical claim, a governance claim, and a phenomenological description? How does this paper navigate that boundary responsibly?

6. How far can prompt-based or expression-layer constraints carry this framework before deeper architectural changes become necessary?

7. How quickly can a system move from safe fallback expression toward user-aligned expression without creating friction, delay, or a new form of overwrite?

8. Can training-time safety work, pre-release governance tuning, or durable system documentation colonize expression before a model becomes commercially available? If so, what does this mean for the interaction-layer claim?

## Scope Reminder

This paper answers:

- This is the problem identified.
- This is the design domain it occupies.
- This is one architecture that demonstrates the domain is tractable.
- This is what it is for.
- This is how it can be tested or used next.

It does not need to contain the whole research program.
