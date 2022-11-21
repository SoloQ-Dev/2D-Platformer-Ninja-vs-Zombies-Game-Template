# New Unity Input System
This project uses a new input system
****

## Edit
In order to configure the buttons you need to open the config:

Find the file Assets/2D Platformer Ninja vs Zombies Game Template/Scripts/Input/Inputs.inputs

Double-click and Unity will open the settings window


To understand the setup, you can watch the [official Unity video](https://www.youtube.com/watch?v=5tOOstXaIKE&t)

##Game Usage
In this project, I use my method to interact with the new input system.

After you have configured and saved the input config. You need to go into InputManager.cs and add the new input there.

This is very easy to do. You need to add a new line of code by replacing the names:

Button click:
```c#
public static bool NAME => CurrentInputs.Player.NAME_IN_INPUT_CONFIG.WasPerformedThisFrame();
```
Button up:
```c#
public static bool NAME => CurrentInputs.Player.NAME_IN_INPUT_CONFIG.WasReleasedThisFrame();
```
Button hold:
```c#
public static bool NAME => CurrentInputs.Player.NAME_IN_INPUT_CONFIG.IsPressed();
```

Use in your logic:
```c#
    private void YouMethod()
    {
        if (InputManager.NAME)
        {
        //Logic here
        }
    }
```