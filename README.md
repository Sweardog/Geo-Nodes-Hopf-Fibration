# Blender Geometry Nodes: Hopf Fibration w/ Python Animations (3.5.1 Tested)

## Renders of Python Animations 
* [My Favorite](https://imgur.com/sJMVRzE)
* [Second Favorite](https://imgur.com/4EQyjGZ)
* [Third Favorite](https://imgur.com/ZjD5ThF)

## Detailed Insights: Mathematics, Node Structure
* [Detailed Explanation of Math (in LaTeX) and Geometry/Shading Nodes](https://www.overleaf.com/read/cnchjmcvnpqt)

## Overview
The "Hopf Fibration Modifier" is a versatile tool, designed to display any set of points of $S^2$ along with their corresponding Hopf fibers in a color-coordinated manner. My primary method for generating animations of $S^2$ points used is Python. However, this modifier is not restricted to any particular approach. Feel free to use any method that suits your requirements to animate points of $S^2$. In the primary collectiom of the "Scene Collection", there exist certain "Dummy" objects. Their function is to prevent the modifiers from being orphaned, by keeping them in active use. It's advised to interact with duplicates of the "Hopf Fibration Modifier" as this action ensures its original state remains unchanged.

## Exploring a UV-Sphere (No Animations Required)
1. Create a copy of the "Hopf Fibration Dummy Object" object, locatied in the main collection. Store this copy wherever you please. 
2. Navigate to this copy object's geometry nodes workspace to modify the copied modifier, which, unless named otherwise, should be named "Hopf Fibration Modifier.001". 
3. Ensure the "Geometry" output wire of the "UV-Sphere" leads into "Merge by Distance" node

## Sphere Rotations
In the "Hopf Fibration Modifier", a wire leads from the "Group Input" to the "Transform Geometry" node's "Rotation" input. This allows you to manipulate the sphere's rotation around the $x$, $y$, or $z$ axis directly from the editor's "Modifier Properties" panel.

## Displaying Animations w/o Python
1. After completing an animation of $S^2$ points, create a copy of the "Hopf Fibration Dummy Object" object. 
2. Navigate to this copy object's geometry nodes workspace to modify the copied modifier, which, unless named otherwise, should be named "Hopf Fibration Modifier.001". 
3. Feed the animated points of $S^2$ into this copy modifier. 
   * If your animation involves a single object, use the modifier's "Object Info" node.
   * If your animation includes multiple objects, first group them into a collection and then feed this collection into the modifier's "Collection Info" node. 
4. Ensure the output wire of the correct Info node ultimately leads into the "Merge by Distance" node, with the Collection Info instances needing to be realized initially.

## Running Provided Python Animations
1. If you want to explore animations with Python, first ensure the "___SphereAnimations" file is open in the text editor in the "Scripting" workspace. 
2. Also verify that the built in add-ons "Add Mesh: Extra Objects" and "Add Curve: Extra Objects" are enabled. 

***Note***: This text file contains helper functions towards the top and various algorithms below, each producing a unique animation. These algorithms are enclosed in triple quotes to prevent their execution. 

3. To run a specific algorithm, remove the triple quotes and select the "Scene Collection" in the "Outliner" panel to make it active. Then, press the "Run Script" button at the top of the text editor or use the "Alt-P" shortcut. This will generate a new collection within the "Scene Collection", which I name "Stuff", containing all the objects required for the animation, along with the dummy object. The geometry and name of the dummy object now represents the final animation.

## Contributions
If you would like to contribute to this project, you're more than welcome! Possible contributions include reducing the number of nodes used in the "Sphere Rainbow" material's upper path, altering the node layout/wiring structure, simplifying/troubleshooting Python algorithms, submitting your own Python animation, and correcting grammar, math, formatting, etc.

## Donations 
If you appreciate this project and would like to leave a tip:

* **Ethereum Address:** 0x8D9c56b61e4F7d2d77f24d0e7274Ec1caFd0246C

* **Venmo:** @Adam-Swearingen-1

* **PayPal:** paypal.me/abswearingen97

* **Cash App:** $adamswear










