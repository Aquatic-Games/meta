# Aquatic Games Codex
This document contains the official Aquatic Games codex, describing our code style and naming conventions.

## Naming Conventions
This guide follows the [Microsoft recommended coding style](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/coding-style/identifier-names) with some modifications. We will require this convention for all code submitted via pull requests, or directly.

- `PascalCase` for ALL methods, public fields and properties (both static and instance), ALL constants, class names and namespaces
- `_camelCaseWithUnderscore` for private fields
- `camelCase` for local variables, including local constants.

### Valid Example
```cs
namespace MyProject;

public class MyClass
{
    private const uint FloatsLength = 16;

    private float[] _myFloats;

    public int SomeField;

    public float[] MyFloats => _myFloats;

    public int MyMethod(int myVar)
    {
        const int anotherVar = 10;
        return anotherVar + myVar;
    }
}
```

### Recommendations
We recommend the following:
- Prefix local pointer variables with `p`, so for example `pData` (only for C#)

## Coding Style
The Aquatic Games file structure is what we recommend a file should be structured like. Some changes can be made, and these are not enforced as heavily as the naming conventions.

### General file structure
Here is the general file structure we recommend, starting from the top of the file:
- Constants
- Private fields
- Internal fields
- Public fields
- Properties
- Constructors
- Public Methods
- Internal Methods
- Private Methods
- Dispose method
- Statics, in the same order as above