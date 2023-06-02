# Hopf Fibration
Blender Geometry Nodes: Hopf Fibration w/ Python Enabled Animations

Shown above is a \textit{Blender Geometry Nodes} modifier that accepts elements of $S^2$ and instances corresponding \href{https://en.wikipedia.org/wiki/Villarceau_circles}{Villarceau circles} (the stereographically projected Hopf fibers of $S^3$) on each input element via the \href{https://docs.blender.org/manual/en/latest/modeling/geometry_nodes/instances/instance_on_points.html}{``Instance on Points''} geometry node. Rather than stereographically projecting each point of a Hopf fiber from $S^3$ to $\mathbb{R}^3 \cup \{\infty\}$ in a parametric-point-plot approach, it is more effective to determine the center, radius, and normal vector of each Villarceau circle and adjust the circle instances in terms of position, scale, and alignment. This fibration of $S^3$ will be approached from a complex $\mathbb{C}^2$ interpretation, rather than quaternionic $\mathbb{H}$.


[View the full document](./Nodes_Explanation.pdf)