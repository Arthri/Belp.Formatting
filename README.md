# Belp.Formatting
An unofficial bundle of formatting tools that strives for closeness to conventional C#.

The package attempts to enforce writing C# in the most conventional manner possible. To this end, it deviates from Microsoft's conventions in several areas. For example,
- `_camelCase` for private fields

    The BCL uses conventions such as `m_camelCase` and `t_camelCase`. The convention is not popular in modern C# and is limited to the BCL and older codebases.

    Roslyn uses `this.camelCase`, which does have some usage, but isn't more popular than `_camelCase`.
- `PreEvent`/`PostEvent` or `BeforeEvent`/`AfterEvent` instead of `Eventing`/`Evented`.

Furthermore, the stance of this package on some C# disputed conventions are as follows,
- Explicit type over var unless self-evident.
    ```cs
    IEnumerable<string> x = GetNames();
    var y = (string)obj;
    var z = new object();
    object a = new();
    int b = 2;
    var c = 3L;
    ```
- All methods must use block bodies(as opposed to expression bodies) without exception.
- Properties may use expression bodies.
- All selective statements(if, switch), loop statements(while, for), and other statements which can be accompanied by curly braces must be accompanied by curly braces.
    One notable exception is a series of using statements after another.
    ```cs
    using (null)
    using (null)
    using (null)
    {
    }

    // Also allowed
    using (null)
    {
        using (null)
        {
            using (null)
            {
            }
        }
    }
    ```
- No parentheses or grouping operators unless necessary.
- Switch case contents must be wrapped in {} and must have the break statement placed outside the curly braces if possible.

## Comment Legend
```ini
#§ Analyzers section
#¶ Analyzers subsection
#: Analyzer description
#> Link to documentation
#! Per-project configuration
#? Per-user configuration
#- Removed
#X Superseded by another analyzer
#/ Miscellaneous comment
```

Some common reasons for an analyzer to be disabled is as follows,
- Situational: the analyzer is sometimes useful and sometimes not.
- Subjective: the reported issue is decided by the opinions of the developer.
- Too broad: the analyzer reports too many false positives

## Installation

### Requirements
- .NET SDK 8 or newer

### Install using an Editor
1. Locate the project file(for example, `Project.csproj`, `Project.fsproj`).
1. Open the project file in an editor.
1. Locate the an `<ItemGroup>`.
1. Add a new `PackageReference` element to the item group with the `Include` attribute set to `Belp.Formatting` and the `Version` attribute set to `0.0.1` or a version of choosing. For example, `<PackageReference Include="Belp.Formatting" Version="0.0.1" />`.
1. Run `dotnet restore`.

#### Uninstallation
1. Locate the project file(for example, `Project.csproj`, `Project.fsproj`).
1. Open the project file in an editor.
1. Locate the `PackageReference` element with an `Include` attribute set to `Belp.Formatting`.
1. Delete the element.

### Install using the .NET CLI
1. Open a terminal.
1. Navigate to the containing directory of the project file.
1. Run the command `dotnet add package Belp.Formatting`.

#### Uninstallation
1. Open a terminal.
1. Navigate to the containing directory of the project file.
1. Run the command `dotnet remove package Belp.Formatting`.

### Install using Visual Studio Package Manager
1. Open Visual Studio.
1. Right click the project in the Solution Explorer.
1. Click on "Manage NuGet Packages".
1. Go to the "Browse" tab.
1. Search for `Belp.Formatting`.
1. Install.

#### Uninstallation
1. Open Visual Studio.
1. Right click the project in the Solution Explorer.
1. Click on "Manage NuGet Packages".
1. Go to the "Installed" tab.
1. Click on `Belp.Formatting`.
1. Click on "Uninstall".

## Usage
The package automatically configures the formatting upon installation.

## Development

### Prerequisites
- Install the .NET 8.0 SDK version 8.0.100 or newer.

### Building with Visual Studio
1. Open `Belp.Formatting.sln`.
1. Open the Solution Explorer.
1. Right click on the project `Belp.Formatting` in the Solution Explorer.
1. Click on `Pack`.

### Building with .NET CLI
1. Open a terminal in the repository root.
1. Run `dotnet pack`

### Output
By default, the output is located in `src/Belp.Formatting/Belp.Formatting/bin/Release/`.
