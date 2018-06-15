# CleverbotIO.Net

### A simple way to use the Cleverbot.io API with .NET Core!

This project uses [cleverbot.io](https://cleverbot.io/)

It's also **heavily** based off [Cleverbot.Net](https://github.com/Sorashi/Cleverbot.Net), just updated for .NET Core

### Some simple code to get you started:
```csharp
using System;
using Cleverbot.Net;

class Program
{
    static void Main()
    {
        var session = CleverbotSession.NewSession("apiUser", "apiKey");
        Console.Write("You: ");
        message = Console.ReadLine();
        Console.WriteLine($"Bot: {session.Send(message)}");
    }
}
```

### It also supports asynchronous requests by adding *ASync* to the end
```csharp
var session  = await CleverbotSession.NewSessionAsync("apiUser", "apiKey");
var response = await session.SendAsync("Hello.");
```