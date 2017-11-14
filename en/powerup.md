1. You can have players get a bonus when they pick up a blue coin! Lets speed them up for 5 seconds.

2. To create a powerup you should make a method (a function in a class) in your *PlayerController* class. You will be controlling your player so it makes sense to put it there. So add this function: 
    ```csharp
    void powerupSpeedUp(Player player)
    {
        player.powerupTimeLeft -= Time.deltaTime;
        if (player.powerupTimeLeft > 0)
            player.movespeed = 5f;
        else
            player.movespeed = 2f;
    }
    ```
    
    This checks the player's powerup time left and makes the player faster if the time left is greater than 0. The first line decreases the timer.

3. Now you need to set the player's `powerupTimeLeft` to 5 seconds when you collide with it. So, you'll need to change the "Collisions" script.

4. The powerup coins are tagged as "powerup". So, you can use that to determine if a player collided with a powerup in the `OnCollisionEnter2D()` function. Like so:

    ```csharp
    if (col.gameObject.tag == "powerup")
    {
        Destroy(col.gameObject);
        if (animal == "cat")
        {
            GameObject.Find("Platform").GetComponent<PlayerController>().cat.powerupTimeLeft = powerupTime;
        }
        if (animal == "dog")
        {
            GameObject.Find("Platform").GetComponent<PlayerController>().dog.powerupTimeLeft = powerupTime;
        }
    }
    ```
    The if statements check which animal collided with the powerup then set's that animal's powerupTimeLeft to 5 seconds.
    
5. And that's it you've made the power ups do something! Test out your new speed when you pick up a powerup.