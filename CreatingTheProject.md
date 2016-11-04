# Creating the project

The very first part of any C# project is to create the solution.

In order to keep simplicity with all the examples to be shown, we will work with console apps using MonoDevelop.
But you can create GUI apps if that's what you want.

To create a solution, press **File - New Project**.
Choose the type of program you want to create according to your compiler.
Name it, and go ahead.

## Adding references

EE servers are powered by [PlayerIO](http://playerio.com), and so you need to use their SDK in order to perform any communication with it and therefore the game.
You can download [PlayerIOClient.dll](https://github.com/HabboGame/EEBotTutorials/raw/master/PlayerIOClient.dll) directly from this repository, or from the [PlayerIO](https://playerio.com/download/PlayerIO%20SDK.zip) website.

Once you've downloaded PlayerIOClient.dll, it's time to add it as a reference on the project.
Right-click the solution on the solution explorer, and press "Edit References".
Go to the ".NET Assembly" tab. Then browse for PlayerIOClient.dll where you download it.

Congrats, you have successfully added a reference! It's now the time to **use** it on the project.

Add a simple line at the start of the code that allows use of PlayerIOClient.

```
using PlayerIOClient;
```

You can now continue with the rest of the project.
