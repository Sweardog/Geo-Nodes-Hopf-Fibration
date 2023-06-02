# Hopf Fibration
Blender Geometry Nodes: Hopf Fibration w/ Python Enabled Animations

_OVERVIEW_
The provided Hopf Fibration modifier is a versatile tool, designed to recieve and display any set of points of a 2-sphere along with the corresponding Hopf fibers. While I've primarily used Python to generate my own animations of 2-sphere points, the modifier isn't bound to a specific method; you're free to use any method that suits your requirements to animate points of $S^2$. There are countless ways to achieve this.

Once your animation is complete, simply feed the points into the Hopf Fibration modifier. For animations comprising a single object, use the modifier's "Object Info" node. If your animation involves multiple objects, store them in a collection first and then feed this collection to the modifier's "Collection Info" node.

_HOW TO EXPLORE A STANDARD UV-SPHERE AND ITS FIBERS_ 
If you don't want to explore animations and simply want see a UV-sphere's Hopf fibers, start by adding a "dummy" mesh object (so-called because its geometry will be ignored). I recommend using a primitive vert mesh object, which can be enabled with the built-in add-on "Add Mesh: Extra Objects". Next, assign the dummy object the "Hopf Fibration Mod" modifier. When you have your object selected, navigate to the "Geometry Nodes" workspace. Here, connect the "UV Sphere" mesh output from the pink box to the "Merge by Distance" node's "Geometry" input. This should display the UV-sphere points and their corresponding Hopf fibers.

In the "Geometry Nodes" workspace, you'll notice a wire leading from the "Group Input" to the "Transform Geometry" node's "Rotation" input. This provides the ability to manipulate the sphere's rotation around the x, y, or z axis directly from the editor's "Modifier Properties" panel.

_HOW TO RUN PROVIDED PYTHON ANIMATIONS_
If you do want to explore animations, to run the included Python animations, head to the "Scripting" workspace. Ensure that the "___SphereAnimations" file is open in the text editor. This file contains helper functions and various algorithms, each associated with a different animation and enclosed in triple quotes to prevent them from being executed by the interpreter.

To run a specific algorithm, remove the surrounding triple quotes and select the "Scene Collection" in the "Outliner" panel to make it the active collection. Then, hit the "Run Script" button at the top of the text editor (or use the Alt-P shortcut). This will generate a new collection within the scene collection, containing all the objects required for the animation, along with the dummy object, whose geometry now represents the final animation. I've included ample comments within the Python scripts to aid understanding of how these animations are generated. Enjoy exploring the fascinating world of Hopf fibers!

_SAMPLE ANIMATION RENDERS_
[Shoot Rotating Segments of $S^2$](https://www.overleaf.com/read/cnchjmcvnpqt)
[Points Following Spiral of $S^2$](https://www.overleaf.com/read/cnchjmcvnpqt)
[Rotating Circles of $S^2$](https://www.overleaf.com/read/cnchjmcvnpqt)

_EXPLANATION OF THE NODES_
[Geometry and Shading Nodes Explanation](https://www.overleaf.com/read/cnchjmcvnpqt)

_CONTRIBUTIONS_
If you'd like to contribute to this project, here are some potential options: reduce the number of nodes used, simplify the python algorithms, submit your own python animation, alter wiring structure or node placement, fix my grammar, etc...

