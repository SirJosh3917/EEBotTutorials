# EEBotTutorials

The new "How to create an EE bot?" book. No videos, just text.

### What is a bot?

A bot is a tool designed to do stuff automatically. In the case of EE, a bot allows you to do things that would be annoying to have to do manually, such as snakes, digging, bosses, etc.

### What do you need to create a bot?

All what you do actually need is knowledge. There is no sense in having tools you don't know how to use.

### Tools

EE Bots are usually written in the C# programming language, because the server host [PlayerIO](http://playerio.com) provides a C# SDK for this purpose. Therefore, the best is to use this language. Let's go to the list of programs.

* .NET Framework: It's the framework that will allow you to run C# programs, as well as the bots we are going to create.
  * [Mono](http://www.mono-project.com/) (Recommended): An open-source implementation of Microsoft .NET Framework, for all the operative systems.
  * [Microsoft .NET Framework](https://www.microsoft.com/net/download): Software framework designed to run on Windows. Not cross-platform.
* Compiler: It's the tool we are going to use to create and build our bots. **Please read below before selecting a compiler**
  * [MonoDevelop](http://www.monodevelop.com/) (Recommended): An open-source, cross-platform compiler that supports C# along with Gtk#, a cross-platform GUI toolkit.
  * [Visual Studio](https://www.visualstudio.com/): A compiler for Windows programs, by Microsoft. It supports C# along with Windows Forms, Windows' default GUI toolkit.
  
#### I want to create a bot with a nice GUI

GUIs are what most of people are used to. It makes it easier and more organized for coders to create programs for novices. You may think that having a clean, good-looking GUI is the main part here, but the main part is actually which GUI toolkit you have to use.

* [Gtk#](http://www.mono-project.com/docs/gui/gtksharp/) (Recommended): An open-source, multi-platform GUI toolkit for both frameworks Mono and Microsoft .NET.
* [Windows Forms](https://msdn.microsoft.com/en-us/library/dd30h2yb(v=vs.110).aspx): The default GUI toolkit included on Microsoft .NET Framework. It only supports Windows.

If you want to create a cross-platform bot with GUI that can be used in both Windows and Linux, then your best choice is to use MonoDevelop and Gtk#. It will just require Windows users to install Gtk#, and Linux users to install Mono, which is easy and clearly better than Wine.

If you want to create a classic, Windows-only bot with Windows Forms, then your option is to download Visual Studio. You are going to need a Microsoft Account to install the software. Also note that Visual Studio is very heavy. The minimal installation weights aprox. 2 GB, compared to MonoDevelop, which just weights 200 MB. Again, I recommend you to use MonoDevelop and Gtk# for your bot with GUI.

#### I want to create a console bot

If all what you want to do is a simple console app, then you are free to choose any of the frameworks and compilers. I personally recommend Mono and MonoDevelop, but that doesn't matter since console apps will be cross-platform (**unless you somehow call the Windows API, which is in most of the cases useless, and simply annoying, so please keep a pure .NET app**).
