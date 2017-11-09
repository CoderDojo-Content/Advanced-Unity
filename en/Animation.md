1. *Animation* is using multiple images and playing them in a sequence. Unity has a built in **Animator** that allows you to easily create your own *animations*. 

2. Creating your own *animations* is easy in Unity! To create an **Animator** all you need to do is shift click all ten of the Idle images and drag them all into the inspector. You will have to save the *animation*, give it a name like "Idle". 

    Now hit play and watch your new animation!
    
3. Now lets open the animator. When you created your animation it will have made an **Animator** and an **Animation** files. These are what the files look like in the **Project** window.  
The animator file looks like: ![](en/assets/animator.png) The animation file looks like: ![](en/assets/animation.png)

4. Open up the **Animator** by double clicking the animator file and a window should open up and look like this: ![](en/assets/animatorWindow.png)

5. To create more *animations* for your sprite, do the same as in step 2 for the Walk and Jump images. Delete both of the new **Animators** for these two *animations*. You only need an **Animator** to control all of the *animations* for one sprite.

6. You can add more *animations* to the **Animator** by dragging the animation file into the **Animator**.

7. You can right click the different animations in an **Animator** and set them to "Set as Layer Default State" and run the program to see your different animations!

8. To play different *animations* with scripts, you just need to get a sprite's **Animator** and use the code `Animator.Play('the name of the animation')`.
