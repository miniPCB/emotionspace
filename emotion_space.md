# Emotion Space

## 1. Core Definition

Emotion space is modeled as a **productive evaluation** over three component spaces:

- Ability space
- Ambition space
- Feelings space

Let the composite state be:

$$
\mathbf{e}_t = [a_t, b_t, f_t]^\top
$$

where:

- $a_t \in \mathcal{A}$ is ability-state at time $t$
- $b_t \in \mathcal{B}$ is ambition-state at time $t$
- $f_t \in \mathcal{F}$ is feeling-state at time $t$

A productive evaluation function maps these to an emotion value or vector:

$$
\Phi: \mathcal{A} \times \mathcal{B} \times \mathcal{F} \to \mathcal{E}
$$

$$
\mathbf{e}_t = \Phi(a_t, b_t, f_t)
$$

## 2. Component Spaces

### 2.1 Ability Space ($\mathcal{A}$)

Ability space represents competence, skill execution, and capacity.

Example state form:

$$
a_t = [s_t, c_t, r_t]^\top
$$

- $s_t$: skill level
- $c_t$: confidence in execution
- $r_t$: resource-readiness

### 2.2 Ambition Space ($\mathcal{B}$)

Ambition space represents goal intensity, growth orientation, and persistence.

Example state form:

$$
b_t = [g_t, o_t, p_t]^\top
$$

- $g_t$: goal magnitude
- $o_t$: optimism about outcomes
- $p_t$: persistence

### 2.3 Feelings Space ($\mathcal{F}$)

Feelings space captures affective tone and activation.

Example state form:

$$
f_t = [v_t, u_t, d_t]^\top
$$

- $v_t$: valence
- $u_t$: arousal
- $d_t$: emotional stability (or dysregulation inverse)

## 3. Logical Motion Framework

Each space evolves by a state-transition rule with constraints and feedback.

General motion template:

$$
x_{t+1} = T_x(x_t, i_t, q_t)
$$

where:

- $x_t$ is current state in a space
- $i_t$ is input/evidence
- $q_t$ is internal policy or logic

### 3.1 Motion in Ability Space

$$
a_{t+1} = T_A(a_t, \ell_t, \epsilon_t)
$$

- $\ell_t$: learning/practice input
- $\epsilon_t$: error feedback

One simple linear form:

$$
a_{t+1} = a_t + \eta_A \ell_t - \lambda_A \epsilon_t
$$

### 3.2 Motion in Ambition Space

$$
b_{t+1} = T_B(b_t, \kappa_t, \pi_t)
$$

- $\kappa_t$: perceived opportunities
- $\pi_t$: progress signal

One simple form:

$$
b_{t+1} = b_t + \eta_B \kappa_t + \rho_B \pi_t - \delta_B \text{friction}_t
$$

### 3.3 Motion in Feelings Space

$$
f_{t+1} = T_F(f_t, \sigma_t, \mu_t)
$$

- $\sigma_t$: external stimuli
- $\mu_t$: regulation process

One simple form:

$$
f_{t+1} = f_t + \eta_F \sigma_t - \lambda_F \mu_t
$$

## 4. Coupled Emotion Update

Emotion is updated by combining the moved component states:

$$
\mathbf{e}_{t+1} = \Phi(a_{t+1}, b_{t+1}, f_{t+1})
$$

A weighted productive form:

$$
\mathbf{e}_{t+1} = W_A a_{t+1} + W_B b_{t+1} + W_F f_{t+1}
$$

with optional nonlinearity:

$$
\mathbf{e}_{t+1} = \tanh\!\left(W_A a_{t+1} + W_B b_{t+1} + W_F f_{t+1} + \mathbf{c}\right)
$$

## 5. Logical Conditions (Example)

A minimal logic policy can be encoded as:

1. If ability increases and ambition is stable, positive emotion trend increases.
2. If ambition exceeds ability for sustained periods, frustration risk increases.
3. If feelings regulation improves, volatility decreases even under high ambition.

These conditions can gate updates by adjusting $\eta_A, \eta_B, \eta_F$ over time.
