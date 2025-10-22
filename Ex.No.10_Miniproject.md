# Ex.No: 10  Implementation of 2D/3D game Cube Catcher
### DATE:  22-10-2025                                                               
### REGISTER NUMBER : 212223240077
### AIM: 
To develop a game Cube Catcherin Unity 
### Algorithm:
```
1. Initialize player, spawner, cube prefab, and score variables.

2. Move the player left or right based on keyboard input.

3. Spawn cubes at random X positions at fixed time intervals.

4. Detect collision between player and cubes to increase score.

5. End or reset the game when a cube touches the ground.
```  
### Program:
```
1.cube catcher

using UnityEngine;

public class CubeCatcher : MonoBehaviour
{
    public int score = 0;

    void OnTriggerEnter(Collider other)
    {
        if (other.CompareTag("Cube"))
        {
            score++;
            Destroy(other.gameObject);
            Debug.Log("Score: " + score);
        }
    }
}

2.Player control

using UnityEngine;

public class PlayerController : MonoBehaviour
{
    public float speed = 10f;

    void Update()
    {
        float move = Input.GetAxis("Horizontal") * speed * Time.deltaTime;
        transform.Translate(move, 0, 0);
    }
}

```
### Output:
<img width="1917" height="966" alt="Screenshot 2025-10-22 093216" src="https://github.com/user-attachments/assets/104ed015-7106-4b19-a8a9-537d44df9480" />


### Result:
Thus the game was developed using Unity and adopted AI technology.
