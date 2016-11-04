# Connecting to EE

Connecting to the game is the next step after we've created the project for our bot.

### Logging in

In order to join a world, we clearly need to log in to the game first. This can easily be done with one single line of code.

```
PlayerIO.QuickConnect.SimpleConnect ("everybody-edits-su9rn58o40itdbnw69plyw", email, password, null);
```

This will log in to EE, but will not join any world. However, there are some things we have to define.

```
string email = "hello@fake.email";
string password = "password123";
PlayerIO.QuickConnect.SimpleConnect ("everybody-edits-su9rn58o40itdbnw69plyw", email, password, null);
```

We have defined the strings **email** and **password** to be used at the moment of logging in.
Now we need to determine whether the user could log in or there was an error.

```
PlayerIO.QuickConnect.SimpleConnect ("everybody-edits-su9rn58o40itdbnw69plyw", email, password, null, loggedIn, loginError);
```

Here we have 2 voids, **loggedIn** and **loginError**, which will allow us to do whatever we want after user logged in of if they got an error.
We have to define them, outside the Main void.

```
static void loggedIn (Client cli) {
  // User has logged in
}
static void loginError (PlayerIOError error) {
  // Error while logging in
}
```

Congrats, you can now log in to EE and check log in errors!

## Example

Here's a console app that will ask for your e-mail and password, and will show you a message whether you logged in or failed to log in.

```
using System;
using PlayerIOClient;

namespace TestBot {
  class Program {
    static void loggedIn (Client cli) {
      Console.Clear ();
      Console.WriteLine ("Logged in!");
    }
    static void loginError (PlayerIOError error) {
      Console.Clear ();
      Console.WriteLine ("Error while logging in.");
      Console.WriteLine (error.Message);
    }
    static void Main(string[] args) {
      Console.WriteLine ("E-mail:");
      string email = Console.ReadLine ();
      Console.Clear ();
      Console.WriteLine ("Password:");
      string password = Console.ReadLine ();
      Console.Clear ();
      Console.WriteLine ("Logging in...");
      PlayerIO.QuickConnect.SimpleConnect ("everybody-edits-su9rn58o40itdbnw69plyw", email, password, null, loggedIn, loginError);
      Console.ReadKey (true);
    }
  }
}
```
