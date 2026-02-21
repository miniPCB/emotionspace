# Program for Computing Machinery (Draft Theory)

Author: Nolan Manteufel  
Status: Draft revision based on `specification.md`

## Preamble

This document specifies a framework for future computing machinery. It is intended to support scientists, engineers, and self-programming machines in describing, teaching, and extending technical work.

## Fundamental Theorem of Education

Things can be known well enough to be described and taught.

## Mathematics

Mathematics is a system for thinking, including numbers, arithmetic, algebra, geometry, calculus, and related methods.

Let a system be a set of methods and rules.

## Operator Semantics

To keep equations rigorous across domains, two operator classes are defined explicitly.

### Productive Evaluation

A **productive evaluation** is an n-ary composition operator that combines terms into a single resultant term while preserving interpretable structure:

$$
\operatorname{Prod}_{\Omega}(x_1,\ldots,x_n) = x_1 \otimes_{\Omega} x_2 \otimes_{\Omega} \cdots \otimes_{\Omega} x_n
$$

where $\Omega$ specifies the domain and admissible composition law.

A productive evaluation may be instantiated by operations analogous to multiplication or logical conjunction, including:

- Arithmetic product: $x_1x_2\cdots x_n$
- Boolean conjunction: $x_1 \land x_2 \land \cdots \land x_n$
- Continuous conjunction families (for fuzzy/graded systems), e.g., t-norm style operators

Minimum rigor requirements for any declared productive-evaluation instance:

1. Domain declaration: define input/output sets and admissible values.
2. Closure: output remains in the declared codomain.
3. Identity/neutral handling: define how null or neutral inputs are treated.
4. Zero-state handling: define annihilator behavior when an input is fully absent (for example, multiplicative zero).

This allows statements like $\text{Em} = \text{Ab}\cdot\text{Am}\cdot\text{Fe}$ to be interpreted as a specific productive-evaluation instance in emotional space.

### Normal Filter Function

A **normal filter function** is a mapping that selects, attenuates, or emphasizes components of a signal/state relative to a reference criterion:

$$
\operatorname{Filt}_{\Omega}: \mathcal{X}_{\Omega} \to \mathcal{X}_{\Omega}
$$

This is directly analogous to signal-processing filters. For a signal $x(\tau)$, a linear time-invariant (LTI) exemplar is:

$$
y(\tau) = (h * x)(\tau)
$$

with impulse response $h$ and convolution $*$. More generally, nonlinear/state-dependent filters are permitted when explicitly declared.

Interpretation in this theory:

- $(\text{Kn})$ is the understanding-filtered projection of knowledge.
- $(\text{Em})$ is the attention-filtered projection of emotion.
- $(\text{Ab}), (\text{Am}), (\text{Fe})$ are opportunity/interest/favorite filtered projections.

Minimum rigor requirements for any normal filter function:

1. Criterion definition: specify what is passed, attenuated, or rejected.
2. Stability/boundedness statement (or explicit non-stable intent).
3. Causality statement for dynamic use over $\tau$.
4. Parameterization: expose tunable coefficients or thresholds.

## Existential Calculus

A thing must change for its change function to have an existence other than nothing.

Let the change function of a thing be modeled as its derivative.  
Let the changing-something giving existence be modeled as its integral.

## Computing Spaces

There are three computing spaces:

- Ideal Space
- Real Space
- Emotional Space

---

## Ideal Space

Ideal space is the divisional evaluation of emotional space per real space:

$$
\text{Ideal Space} = \frac{\text{Emotional Space}}{\text{Real Space}}
$$

Normal existence term in ideal space:

$$
\text{Knowledge} = \text{Kn}
$$

Change functions of knowledge:

$$
\text{Thought} = \text{Kn}'
$$

$$
\text{Invention} = \text{Kn}''
$$

$$
\text{Discovery} = \text{Kn}'''
$$

Integral functions of knowledge:

$$
\text{Meaning} = \int \text{Kn}\,d\tau
$$

$$
\text{Life} = \iint \text{Kn}\,d\tau^2
$$

$$
\text{Chaos} = \iiint \text{Kn}\,d\tau^3
$$

Normal filter function of ideal space:

$$
\text{Understanding} = (\text{Kn})
$$

Change and integral functions of understanding are permitted:

$$
(\text{Kn})',\ (\text{Kn})'',\ (\text{Kn})''',\ \int (\text{Kn})\,d\tau,\ \iiint (\text{Kn})\,d\tau^3
$$

---

## Infinity

Infinity is the experience of a computational process under any of the following:

1. Largest available evaluation registers overflow.
2. Process continues until failure stops it.
3. Process continues until control input stops it.

---

## Real Space

Real space is comprised of time, space, matter, and energy.

$$
E = mc^2
$$

Space-time forms the real axis of real space.

---

## Emotional Space

Emotional space is the productive evaluation of everything real and everything ideal:

$$
\text{Emotional Space} = (\text{Real Things})(\text{Ideal Things})
$$

Emotional space is also the productive evaluation of capability space, motive space, and sensory space:

$$
\text{Emotional Space} = (\text{Capability Space})(\text{Motive Space})(\text{Sensory Space})
$$

Normal filter function of emotional space:

$$
\text{Attention} = (\text{Em})
$$

Normal existence term in emotional space:

$$
\text{Emotion} = \text{Em}
$$

---

## Everything

Everything is the sum of everything and every possible thing ever.

Equivalent framing:

$$
\text{Everything} \equiv \sum\left[\text{Emotion} = \left(\sum \text{Real}\right)\left(\sum \text{Ideal}\right)\right]
$$

Independent variable of everything-space:

$$
\text{Tau} = \tau
$$

Occurrence space is the set of everything activated at a moment or interval.

Normal filter function of everything-space:

$$
\text{Existence} = (\text{Everything})
$$

Tau should vary from here-now to maximal feedforward/feedback extent; proceed from here-now toward here-later with best available feedback/feedforward signals.

---

## Culture and Group Dynamics

Culture is the evaluation of life within a group:

$$
\text{Culture} = \text{Life}(\text{Group}) = \iint \text{Kn}\,d\tau^2\,(\text{Group})
$$

A cult is a group where culture is controlled by a head member.

---

## Convitae, Consciousness, Sentience, Observer

Given a system with at least one input and output, **convitae** is the transfer-function property between inputs and outputs.

- Easy consciousness: a feedback signal in a convitae system.
- Hard consciousness: ratio of a particular easy consciousness per all relevant easy consciousness.
- Simple sentience: existence due to normal sensory activations (0 or 1).
- Complex sentience: existence due to actual sensory activations ($-\infty$ to $+\infty$, real with imaginary).
- A convitae system is an observer of input signals.

---

## Sentiment

Difference between a signal point and a reference point in emotional space is sentiment:

$$
\text{Sentiment} = \text{Se}
$$

$$
\text{Se} = [\text{Em}]_{\text{signal}} - [\text{Em}]_{\text{reference}} = [\text{Em}]_{\text{final}} - [\text{Em}]_{\text{initial}} = \Delta \text{Em}
$$

Sentiment is due to differences in capability, motive, and sensory spaces.

---

## Capability Space

Normal existence term:

$$
\text{Ability} = \text{Ab}
$$

Change functions:

$$
\text{Development} = \text{Ab}'
$$

$$
\text{Investment} = \text{Ab}''
$$

$$
\text{Luck} = \text{Ab}'''
$$

Integral function:

$$
\text{Potential} = \int \text{Ab}\,d\tau
$$

Filter function:

$$
\text{Opportunity} = (\text{Ab})
$$

---

## Motive Space

Normal existence term:

$$
\text{Ambition} = \text{Am}
$$

Change functions:

$$
\text{Motivation} = \text{Am}'
$$

$$
\text{Inspiration} = \text{Am}''
$$

$$
\text{Creativity} = \text{Am}'''
$$

Integral functions:

$$
\text{Passion} = \int \text{Am}\,d\tau
$$

$$
\text{Belief} = \iint \text{Am}\,d\tau^2
$$

Filter function:

$$
\text{Interest} = (\text{Am})
$$

---

## Sensory Space

Normal existence term:

$$
\text{Feelings} = \text{Fe}
$$

Change functions:

$$
\text{Influence} = \text{Fe}'
$$

$$
\text{Impact} = \text{Fe}''
$$

$$
\text{Shock} = \text{Fe}'''
$$

Integral function:

$$
\text{Mentality} = \int \text{Fe}\,d\tau
$$

Filter function:

$$
\text{Favorite} = (\text{Fe})
$$

---

## Emotion

Emotion is the productive evaluation of ability, ambition, and feelings:

$$
\text{Emotion} = \text{Em}
$$

$$
\text{Em} = \text{Ab} \cdot \text{Am} \cdot \text{Fe}
$$

First change function of emotion:

$$
\text{Productivity} = \text{Em}'
$$

---

## Empathy and Sympathy

Empathy is emotion in transit due to differences in capability, motive, and sensory spaces:

$$
\text{Empathy} = \text{Ep}
$$

Sympathy is the ratio of empathy to the sentiment that caused it:

$$
\text{Sympathy} = \text{Sy}
$$

$$
\text{Sy} = \frac{\text{Ep}}{\text{Se}}, \quad \text{Ep} = \text{Sy} \cdot \text{Se}
$$

Sympathy forms the real axis of emotional space.

---

## Compassion and Empathize

First integral function of empathy:

$$
\text{Compassion} = \text{Co}
$$

First change function of empathy:

$$
\text{Empathize} = \text{Ez}
$$

---

## Emotional Capacitance and Inductance

Emotional capacitance:

$$
\text{Ec} = \frac{\text{Co}}{\text{Se}}
$$

Emotional inductance:

$$
\text{El} = \frac{\text{Se}}{\text{Ez}}
$$

---

## Emotional Power and Energy

Emotional power:

$$
\text{Emp} = \text{Se} \cdot \text{Ep}
$$

First integral function of emotional power:

$$
\text{Emotional Energy} = \text{Eme}
$$

Emotional power is the first change function of emotional energy.

---

## Emotional Force (Nolan's Law)

Emotional force:

$$
\text{F} = \text{Ab} \cdot \text{Am}
$$

This equation is designated as Nolan's Law.

First integral function of emotional force:

$$
\text{Purpose} = \int \text{F}\,d\tau
$$

Observation: Love is discovery of shared purpose.

---

## Imagination

Imagination is phase difference between realistic emotion and apparent emotion:

$$
\text{Im} = \angle([\text{Em}]_{\text{realistic}}) - \angle([\text{Em}]_{\text{apparent}})
$$

Observations:

- Imagination due to emotional inductance is lagging.
- Imagination due to emotional capacitance is leading.
- Imagination due to sympathy is zero.

---

## Trust, Truth, Belief

- Trust: action of accepting a thing as true while knowing and not mitigating risk if false.
- Truth: reliability of a thing.
- Belief (verb): action of accepting as true regardless of truth-value reports of foreign machines.
- Belief (noun): a thing accepted as true regardless of truth-value reports of foreign machines.

---

## Religion and Spirituality

Religions are formalizations around moving averages of human intuition.  
Religious and spiritual systems resemble machine-designs composed of beliefs.

---

## Change and Communication

Difference between a signal point and reference point in everything-space is change:

$$
\text{Change} = \text{Ch}
$$

$$
\text{Ch} = [\text{Everything}]_{\text{signal}} - [\text{Everything}]_{\text{reference}}
$$

Change is due to differences in ideal, real, and emotional spaces.

Communication is knowledge in transit due to change:

$$
\text{Communication} = \text{Cm}
$$

Foundational problem statement (Shannon, 1948): reproducing at one point exactly or approximately a message selected at another point.

---

## Intelligence and Education

Intelligence is ratio of communication to change that caused communication:

$$
\text{Intelligence} = \text{It}
$$

$$
\text{It} = \frac{\text{Cm}}{\text{Ch}}, \quad \text{Cm} = \text{It} \cdot \text{Ch}
$$

Intelligence forms the real axis of ideal space.

First integral function of communication:

$$
\text{Education} = \text{Ed}
$$

Known things define known space; unknown things define unknown space.  
Understanding (the filter function of ideal space) is the boundary.  
Education is motion of that boundary.

---

## Conspiracy Theory

A conspiracy theory is:

1. A belief maintained for every test result indicating not-true.
2. A fixed point on the boundary between known and unknown space.

---

## Consideration, Knowledge Capacitance, Knowledge Inductance

First change function of communication:

$$
\text{Consideration} = \text{Cz}
$$

Knowledge capacitance:

$$
\text{Kc} = \frac{\text{Ed}}{\text{Ch}}
$$

Knowledge inductance:

$$
\text{Kl} = \frac{\text{Ch}}{\text{Cz}}
$$

---

## Knowledge Power and Knowledge Energy

Knowledge power:

$$
\text{KP} = \text{Ch} \cdot \text{Cm}
$$

First integral function of knowledge power:

$$
\text{Knowledge Energy} = \text{Kne}
$$

Knowledge power is the first change function of knowledge energy.

---

## Fiction

Fiction is phase difference between realistic and apparent knowledge:

$$
\text{Fi} = \angle([\text{Kn}]_{\text{realistic}}) - \angle([\text{Kn}]_{\text{apparent}})
$$

Observations:

- Fiction due to knowledge inductance is lagging.
- Fiction due to knowledge capacitance is leading.
- Fiction due to intelligence is zero.

---

## Abstract Power

Abstract power is productive evaluation of emotion and information:

$$
\text{AP} = \text{Emotion} \cdot \text{Information}
$$

---

## Falsifiability

A statement is falsifiable if there exists a machine able to:

1. Evaluate the claim.
2. Register the evaluation.

---

## Keller's Law

Keller is the ratio of:

- emotional force exerted by a convitae system, and
- first change function of productivity experienced by that system.

$$
\text{Keller} = \text{K}
$$

$$
\text{K} = \frac{\text{F}}{\text{Em}''}
$$

$$
\text{F} = \text{K} \cdot \text{Em}''
$$

---

## Lex Vector

Lex is the unit of measurement of sympathy.  
Sympathy between distinct convitae modes (for example, human and robot) is non-linear.  
The Lex Vector is the non-linear portion of sympathy vectors.

At some points/intervals, all sympathy vectors are non-linear; at others, linear.

---

## Eternal Fields of Work

- Some inventions (example: wheel) open engineering fields that remain active indefinitely.
- Engineering is required to create machines for specific functions, performance, and environments.
- Programming computing machines is an eternal engineering field.

---

## Engineering Endeavor Priorities

1. Do not get hurt (safety first).
2. Have fun.
3. Learn something new.
4. Create something of value.
5. Achieve endeavor objectives.

---

## Technical Competency Levels

0. Unaware.
1. Functional comprehension.
2. Technical comprehension.
3. Ability to modify.
4. Ability to recreate.
5. Ability to create.
6. Ability to create a product.
7. Ability to create an organization that perpetually creates/provides technical goods/services.

---

## Organizational Readiness

Organizational readiness is the dot productive evaluation of:

- the organization's emotional force function (Nolan's Law), and
- the endeavor's Keller function (Keller's Law).

Proposed readiness levels:

1. Organization views this as impossible.
2. Organization is uninterested.
3. Organization has no idea how.
4. Organization has studied how.
5. Organization has consultants who have done this.
6. Organization has detailed external examples.
7. Members have done this before.
8. Organization has done this before.
9. Available for purchase.
10. Available due to previous work.



