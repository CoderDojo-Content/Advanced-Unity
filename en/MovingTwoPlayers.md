1. Time to use the class you just created! In the "PlayerMover" script you will find a some code already completed. This code has already been covered in previous tutorials, feel free to take a look through the code to understand what it does!

2. Creating a class is done by using the constructor you created earlier. You also need to *Instantiate* a new object. In C# this is done with the **new** keyword. Add the line `cat = new Player("cat")` in the Start() function. It will create a new player object that's variable name is cat (do the same but replace cat with dog). Add declarations for both a Player cat and a Player dog.

    * Note - Make sure your code looks like this in the PlayerMover *class*:
    ```csharp
    public Player cat;
    public Player dog;
    
    void Start()
    {
        cat = new Player("cat");
        dog = new Player("dog");
        ...
    ```

3. Now you have two objects, you need to get input from the user and assign what the user input does. You can use the `mover(Player player, KeyCode left, KeyCode right, KeyCode up)` function to do this. Put these lines of code into the `void Update()` function:
    
    ```csharp
    mover(dog, KeyCode.A, KeyCode.D, KeyCode.W);
    mover(cat, KeyCode.LeftArrow, KeyCode.RightArrow, KeyCode.UpArrow);
    ```
    ![https://docs.unity3d.com/ScriptReference/KeyCode.html](/assets/directions.png)
    
    * Note - You can change these KeyCodes to whatever keys you want them to be! Here is a list of KeyCodes: [dojo.soy/UnityKeyCodes](https://docs.unity3d.com/ScriptReference/KeyCode.html)
       
4. Now you can move the two different sprites at the same time! Try it out!