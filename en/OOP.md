1. Object Oriented Programming (OOP) is focusing on the *objects* that you will be programming. An *object* is an instance of a *class*. A class is a template and the object is the product. Using the analogy of baking a cake, the class is the recipe and the object is the cake. 

2. When working with an OOP language, such as C#, you need to decide which objects you will be programming. Our game will have two players, so you need two player objects. These players will control two sprites that do the same thing. So, you can use a single class or struct as a template for both of these objects.

    ![](/assets/movement.png)

3. When you create a template, you need to choose between a *Structure* (struct) or a *class*. The most important difference is that a *class* is a *reference type* and a *struct* is a *value type*. Basically, this means you can access a value in a struct, and in a *class* you can access the value and change it. 

4. You want to use a *class* because you will be changing different variables  of the players. To create a class, open the script "PlayerMover". Underneath the `using` statements and above the `public class playerMover : MonoBehavior` you will create a class. This code will create a class: 

    ``` csharp
    public class Player
    {
        
    }
    ```
5. 