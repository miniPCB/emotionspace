# Emotion and Knowledge Spaces: Equations and Worked Examples

## 1. Emotion Space

We represent an agent's emotion as a vector in a low-dimensional continuous space.

$$
\mathbf{e}_t = [v_t, a_t, d_t]^\top
$$

- $v_t$: valence (negative to positive)
- $a_t$: arousal (calm to activated)
- $d_t$: dominance (submissive to in-control)

A simple linear-affine update from stimulus $\mathbf{x}_t\in\mathbb{R}^m$:

$$
\mathbf{e}_{t+1} = A\mathbf{e}_t + B\mathbf{x}_t + \mathbf{b}
$$

with clipping to bounded emotional range:

$$
\mathbf{e}_{t+1} \leftarrow \operatorname{clip}(\mathbf{e}_{t+1}, -1, 1)
$$

Emotion intensity (norm-based):

$$
I_t = \lVert \mathbf{e}_t \rVert_2
$$

Distance between emotional states:

$$
d_E(\mathbf{e}_i, \mathbf{e}_j) = \lVert \mathbf{e}_i-\mathbf{e}_j \rVert_2
$$

### Problem-Solution Example 1 (Single-step update)

Given:

$$
\mathbf{e}_0 = \begin{bmatrix}0.20\\0.10\\-0.10\end{bmatrix},\quad
A = 0.8I_3,\quad
B = \begin{bmatrix}0.6 & -0.2\\0.3 & 0.5\\0.1 & 0.4\end{bmatrix},\quad
\mathbf{x}_0 = \begin{bmatrix}0.9\\0.2\end{bmatrix},\quad
\mathbf{b}=\mathbf{0}
$$

Compute:

$$
A\mathbf{e}_0 = \begin{bmatrix}0.16\\0.08\\-0.08\end{bmatrix},\quad
B\mathbf{x}_0 = \begin{bmatrix}0.50\\0.37\\0.17\end{bmatrix}
$$

So:

$$
\mathbf{e}_1 = \begin{bmatrix}0.66\\0.45\\0.09\end{bmatrix}
$$

Intensity:

$$
I_1 = \sqrt{0.66^2+0.45^2+0.09^2} \approx 0.804
$$

### Problem-Solution Example 2 (Emotion similarity)

Given:

$$
\mathbf{e}_A = [0.6, 0.2, -0.1]^\top,\quad
\mathbf{e}_B = [0.1, -0.3, 0.2]^\top
$$

Distance:

$$
d_E(\mathbf{e}_A,\mathbf{e}_B)=\sqrt{(0.5)^2+(0.5)^2+(-0.3)^2}
=\sqrt{0.59}\approx 0.768
$$

Interpretation: The two affective states are moderately dissimilar.

## 2. Knowledge Space

Represent each concept as a vector embedding $\mathbf{k}_i\in\mathbb{R}^n$.

A learner's current knowledge state is:

$$
\mathbf{z}_t \in \mathbb{R}^n
$$

Update with learning signal $\mathbf{u}_t$:

$$
\mathbf{z}_{t+1} = \mathbf{z}_t + \eta \mathbf{u}_t
$$

where $\eta\in(0,1]$ is learning rate.

Mastery score for concept $i$ using sigmoid:

$$
M_i = \sigma(\mathbf{z}_t^\top \mathbf{k}_i)=\frac{1}{1+e^{-\mathbf{z}_t^\top \mathbf{k}_i}}
$$

Retrieval probability can be modeled similarly:

$$
P_i = \sigma(\alpha M_i - \beta \Delta t_i)
$$

- $\Delta t_i$: time since last review
- $\alpha,\beta > 0$: scaling parameters

### Problem-Solution Example 1 (Mastery computation)

Given:

$$
\mathbf{z}_t=[0.4, -0.2, 0.7]^\top,\quad
\mathbf{k}_1=[0.5, 0.1, 0.6]^\top
$$

Dot product:

$$
\mathbf{z}_t^\top\mathbf{k}_1 = 0.4(0.5)+(-0.2)(0.1)+0.7(0.6)=0.60
$$

Mastery:

$$
M_1 = \sigma(0.60) \approx 0.646
$$

Interpretation: Concept 1 is above 0.5 mastery but not yet strong.

### Problem-Solution Example 2 (Learning update + retrieval)

Given:

$$
\mathbf{z}_t=[0.2, 0.3, -0.1]^\top,\quad
\mathbf{u}_t=[0.4, -0.2, 0.5]^\top,\quad
\eta=0.5
$$

Update:

$$
\mathbf{z}_{t+1} = [0.2,0.3,-0.1]^\top + 0.5[0.4,-0.2,0.5]^\top
= [0.4,0.2,0.15]^\top
$$

Suppose concept embedding $\mathbf{k}_2=[0.6,0.2,0.3]^\top$, then:

$$
M_2=\sigma(\mathbf{z}_{t+1}^\top\mathbf{k}_2)
=\sigma(0.4(0.6)+0.2(0.2)+0.15(0.3))
=\sigma(0.325)\approx 0.581
$$

If $\alpha=4$, $\beta=0.3$, and $\Delta t_2=2$:

$$
P_2=\sigma(4(0.581)-0.3(2))=\sigma(1.724)\approx 0.849
$$

## 3. Coupling Emotion and Knowledge (Optional Extension)

Emotion can modulate learning rate:

$$
\eta_t = \eta_0\left(1 + \gamma a_t - \lambda |v_t^-|\right)
$$

- Higher arousal $(a_t)$ may increase update speed up to a point.
- Strong negative valence $(v_t^- = \min(v_t,0))$ can reduce effective learning.

Then knowledge update becomes:

$$
\mathbf{z}_{t+1}=\mathbf{z}_t+\eta_t\mathbf{u}_t
$$

This gives a compact way to model affect-cognition interaction.

