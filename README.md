# aggregate app

A proof-of-concept solution that publishes multiple apps into a single folder
using a single aggretate project that depends on 2 projects that produce 
self-contained dotnet console apps.


## Commands

```dotnet publish -self-contained true -f net8.0 -r win-x64 -o .publish aggregate/aggregate.csproj```

The command above is expected to produce a single folder that contains 2 runnable
self-contained apps:

* App.One.exe
* App.Two.exe

with their respective .deps.json files.

This is confirmed on Windows.
