# **Renders of Provided Python Animations**
(DETAILED Geometry and Shading Nodes explanation)[https://www.overleaf.com/read/cnchjmcvnpqt]
(DETAILED Geometry and Shading Nodes explanation)[https://www.overleaf.com/read/cnchjmcvnpqt]
(DETAILED Geometry and Shading Nodes explanation)[https://www.overleaf.com/read/cnchjmcvnpqt]

# **In-Depth Mathematical and Node Structure Insights**
(Math (with LaTeX) and Geometry/Shading Nodes explanation)[https://www.overleaf.com/read/cnchjmcvnpqt]

# **Overview**
The provided *Hopf Fibration Modifier* is a powerful tool that takes any set of points from a 2-sphere and displays them along with their corresponding Hopf fibers. Although my primary method for generating animations of 2-sphere points has been Python, this modifier isn't tied to a specific approach. Feel free to use any method that fits your needs to animate points on $S^2$.

## **Creating Animations**

Once your animation is complete, feed the points into the *Hopf Fibration modifier*. For animations involving a single object, use the modifier's "**Object Info**" node. If your animation includes multiple objects, first group them into a collection and then feed this collection into the modifier's "**Collection Info**" node.

## **Exploring a UV-Sphere's Hopf Fibers**

If you want to explore a basic UV-sphere's Hopf fibers without python animations, you can do this with a "dummy" mesh object (named so as its input geometry will be ignored). I use a primitive vert mesh object, enabled via the built-in add-on "*Add Mesh: Extra Objects*". Assign the dummy object the *Hopf Fibration Modifier* modifier. Then, in the "*Geometry Nodes*" workspace, connect the "*UV Sphere*" mesh output from the pink box to the "*Merge by Distance*" node's "*Geometry*" input. This should display the UV-sphere's points and their corresponding Hopf fibers.

## **Sphere Rotation**

In the "*Geometry Nodes*" workspace, there's a wire leading from the "*Group Input*" to the "*Transform Geometry*" node's "*Rotation*" input. This allows you to manipulate the sphere's rotation around the x, y, or z axis directly from the editor's "*Modifier Properties*" panel.

## **Running Python Animations**

If you want to explore animations, ensure the "*___SphereAnimations*" file is open in the text editor in the "*Scripting*" workspace. This file contains helper functions and various algorithms, each producing a unique animation. To cause the interpreter to ignore these pieces of code, these algorithms are enclosed in triple quotes.

To run a specific algorithm, remove the triple quotes and select the "*Scene Collection*" in the "*Outliner*" panel to make it active. Then, press the "*Run Script*" button at the top of the text editor or use the *Alt-P* shortcut. This will generate a new collection within the "*Scene Collection*", containing all the objects required for the animation, along with the dummy object. The geometry of the dummy object now represents the final animation.

**Note:** I've included ample comments within the Python scripts to aid in understanding how these animations are generated. Enjoy exploring the fascinating world of Hopf fibers!

## **Contributions**
I'll be happy if anyone sees this project and wants to add a contribution! Some ideas: reduce number of nodes, alter node layout/wiring structure, simplify python algorithms, submit your own python animation, correct my grammar, math, etc...




















