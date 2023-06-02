# Hopf Fibration
Blender Geometry Nodes: Hopf Fibration w/ Python Enabled Animations

![Segments of $S^2$ and their Fibers](https://i.imgur.com/OMfcS3s.png)


Shown above is a \textit{Blender Geometry Nodes} modifier that accepts elements of $S^2$ and instances corresponding \href{https://en.wikipedia.org/wiki/Villarceau_circles}{Villarceau circles} (the stereographically projected Hopf fibers of $S^3$) on each input element via the \href{https://docs.blender.org/manual/en/latest/modeling/geometry_nodes/instances/instance_on_points.html}{``Instance on Points''} geometry node. Rather than stereographically projecting each point of a Hopf fiber from $S^3$ to $\mathbb{R}^3 \cup \{\infty\}$ in a parametric-point-plot approach, it is more effective to determine the center, radius, and normal vector of each Villarceau circle and adjust the circle instances in terms of position, scale, and alignment. This fibration of $S^3$ will be approached from a complex $\mathbb{C}^2$ interpretation, rather than quaternionic $\mathbb{H}$.


\begin{center}
$g^{-1}(q_1 + q_2i) = (\frac{2(q_1 + iq_2)}{q_1^{\:2} + q_2^{\:2} + 1}, \frac{q_1^{\:2} + q_2^{\:2} - 1 }{q_1^{\:2} + q_2^{\:2} + 1}) \in \mathbb{C} \times \mathbb{R}$
\end{center}
and $g^{-1}(\infty) = (0, 0, 1)$. The composition $g^{-1}\circ f$ yields a direct map $h: S^3 \to S^2$, where

\begin{center}
$h(z_1, z_2) = (2z_2z_1^{\:*}, r_2^{\:2} - r_1^{\:2}) \in \mathbb{C} \times \mathbb{R}$
\end{center}


[View the full document](./Nodes_Explanation.pdf)