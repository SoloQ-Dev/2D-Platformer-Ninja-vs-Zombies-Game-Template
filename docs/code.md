# Game logic
Editing scripts is not difficult if you are familiar with c #
****

## Namespace
```c#
namespace Platformer
{
	//class
}
```
Platformer namespace is used for all scripts to avoid conflicts with your scripts. 

## Editing
All code has comments describing each action, so editing is easy

```c#
namespace Platformer
{
    public class Custom_Item : PickUpItem
    {
        protected override void OnPickedUp()
        {
            /////////////////////////////////////////////////Here your logic
            
            Debug.Log("It's my logic");

            /////////////////////////////////////////////////
        }
    }
}
```