# ExplodingViewDiagram
A small Unity project that demonstrates a workflow to create an exploding view diagram with labels. [The video below](https://youtu.be/eG5sZKun9mQ) explains the project including the 3D animation needed, importing it from Cinema 4D and how the scripts hook up to buttons and mouse-clicks to make things happen. I include two camera orbit scripts, toggle them on/off to see the difference. Feel free to use this as a stub for your own project!

If your browser supports WebGL 2.0, you can run this [online demo](http://www.bryanleister.com/explode/)

[![Tutorial Video](https://github.com/bryanrtboy/ExplodingViewDiagram/blob/master/preview.gif)](https://youtu.be/eG5sZKun9mQ)

### Notes

You might notice the Mesh colliders created on the cube are very thin and can't be selected from the back. Check the [Convex](https://docs.unity3d.com/2017.4/Documentation/Manual/class-MeshCollider.html) option to make them bulkier and easier to select.

IMPORTANT: The names of the GameObjects imported from C4D correspond to the Layers in the Animation Controller, i.e. "Top", "Front", etc. If you read the CubeController.cs script you'll see that I grab the name of the object with a Collider attached and then tell the Animator to blend to that layer. This requires that the GameObject be named the same as the layers created in the Animator. Don't just rename in Unity, this breaks the links to the animation. Make sure your names are properly set up in C4D before import.

My project includes [Post-Processing Effects](https://docs.unity3d.com/2018.2/Documentation/Manual/PostProcessing-Stack.html). These are under active development, so it's kind of hard to find them and instructions. I used the [Package Manager](https://blogs.unity3d.com/2018/05/04/project-management-is-evolving-unity-package-manager-overview/) to load the package from Unity>WIndows>Package Manager. You can probably use that to check if this version is current.

You can also just select the Camera in the project and play around with the Color Effects or add new Effects like Depth of Field to see how it affects the scene.

The other thing worth looking at is the Look At Constraint that I attached to the labels. This seems to be a new option in Components>Miscelaneous>Look At Constraint in 2018.2. The slider on the labels allow you to decide how aggressively the label looks at the camera. This may or may not be related to the new [Cinemachine Camera](https://docs.unity3d.com/Packages/com.unity.cinemachine@2.1/manual/index.html) systems for film editing, but it's pretty useful!

### Additional Resources

Unity [Tutorials](https://unity3d.com/learn/tutorials)

There are a lot of great tutorials at the link above, if you are brand new to Unity, I'm going to suggest these from the Topics section to get you started and that relate to this project:
[Interface and Essentials](https://unity3d.com/learn/tutorials/topics/interface-essentials)
The [Animator Component](https://unity3d.com/learn/tutorials/topics/animation/animator-component?playlist=17099) and [Animation Layers](https://unity3d.com/learn/tutorials/topics/animation/animator-controller-layers?playlist=17099) explain more about the Animator. To customize the UI elements, you will need to look at the [UI Tutorials](https://unity3d.com/learn/tutorials/s/user-interface-ui), pay particular attention to the [UI Canvas](https://unity3d.com/learn/tutorials/topics/user-interface-ui/ui-canvas?playlist=17111) and the [UI Rect Transform](https://unity3d.com/learn/tutorials/modules/beginner/ui/rect-transform?playlist=17111).


This tutorial is geared for artist/designers. The [Artist Tutorials](https://unity3d.com/learn/tutorials/s/unity-artists) go into more detail about how to further improve the final look of the application.

