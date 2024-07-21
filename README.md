# Belp.Formatting
An unofficial bundle of formatting tools that strives for closeness to conventional C#.

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
