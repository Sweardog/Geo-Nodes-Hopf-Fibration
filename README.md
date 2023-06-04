--- most recently tested in Blender 3.5.1 ---

# **Renders of Provided Python Animations (cooking)**
[My Favorite](https://www.overleaf.com/read/cnchjmcvnpqt)

[2nd Favorite](https://www.overleaf.com/read/cnchjmcvnpqt)

[3rd Favorite](https://www.overleaf.com/read/cnchjmcvnpqt)

# **In-Depth Mathematical and Node Structure Insights**
[Math (with LaTeX) and Geometry/Shading Nodes explanation](https://www.overleaf.com/read/cnchjmcvnpqt)

# **Overview**
The provided *Hopf Fibration Modifier* is a versatile tool, designed to receive any set of points of $S^2$ and color-coordinate them along with their corresponding Hopf fibers. Although my primary method for generating animations of 2-sphere points has been Python, this modifier isn't tied to a specific approach. Feel free to use any method that fits your needs to animate points of $S^2$.

## **Creating Animations**

Once your animation is complete, feed the points into the *Hopf Fibration Modifier*. For animations involving a single object, use the modifier's **Object Info** node. If your animation includes multiple objects, first group them into a collection and then feed this collection into the modifier's **Collection Info** node.

## **Exploring a UV-Sphere's Hopf Fibers**

If you want to explore the Hopf fibers of a basic UV-sphere without Python animations, you can use the **Dummy Hopf Mod Object** located in the scene collection's main collection. The purpose of the existence of the dummy objects in the main collection is to unorphanize their equipped modifiers. I recommend unaltering these modifiers, so I suggest creating a copy of the **Dummy Hopf Mod Object** to have a copy modifier on a copy object. In the copy modifier's **Geometry Nodes** workspace, connect the **UV Sphere** mesh output wire from the pink box to the **Merge by Distance** node's **Geometry** input. This setup will display a UV-sphere's points and their corresponding Hopf fibers.

## **Sphere Rotation**

In the **Hopf Fibration Modifier**, there's a wire leading from the **Group Input** to the **Transform Geometry** node's **Rotation** input. This allows you to manipulate the sphere's rotation around the x, y, or z axis directly from the editor's **Modifier Properties** panel.

## **Running Provided Python Animations**

If you want to explore animations with Python, ensure the **___SphereAnimations** file is open in the text editor in the **Scripting** workspace. You may also run into errors for my algorithms if you don't enable **Add Mesh: Extra Objects** and **Add Curve: Extra Objects**. This text file contains helper functions towards the top and various algorithms below, each producing a unique animation. To cause the interpreter to ignore these pieces of code, these algorithms are enclosed in triple quotes.

To run a specific algorithm, remove the triple quotes and select the **Scene Collection** in the **Outliner** panel to make it active. Then, press the **Run Script** button at the top of the text editor or use the **Alt-P** shortcut. This will generate a new collection within the **Scene Collection**, containing all the objects required for the animation, along with the dummy object. The geometry of the dummy object now represents the final animation.

**Note:** I've included many comments within the Python scripts to aid in understanding how these animations are generated. Enjoy exploring the fascinating world of Hopf fibers!

## **Contributions**

If anyone would like to contribute to this project, you are more than welcome! I suspect that the number of nodes used in the **Sphere Rainbow** material's upper path can be reduced. Apart from flipping the x-coordinate when instancing the dots of S^2, I believe the Hopf Fibration modifier has very few unnecessary nodes. Some other ideas for contributions include altering the node layout/wiring structure, simplifying/troubleshooting Python algorithms, submitting your own Python animation, and correcting grammar, math, etc...












