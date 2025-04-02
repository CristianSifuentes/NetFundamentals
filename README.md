# .NET Fundamentals - Professional Mastery Guide

## Table of Contents

1. [Introduction to .NET](#introduction-to-net)
2. [Architecture and Compilation Process](#architecture-and-compilation-process)
3. [CLR - Common Language Runtime](#clr-common-language-runtime)
4. [Roslyn Compiler](#roslyn-compiler)
5. [Common Language Specifications (CLS) and CIL](#common-language-specifications-cls-and-cil)
6. [Common Type System (CTS)](#common-type-system-cts)
7. [Tools and IDEs](#tools-and-ides)
8. [Project Structure and SDKs](#project-structure-and-sdks)
9. [Compilation Modes](#compilation-modes)
10. [Important CLI Commands](#important-cli-commands)
11. [Package Management with NuGet](#package-management-with-nuget)
12. [.NET Framework vs .NET Core](#net-framework-vs-net-core)
13. [Use Cases and Advantages](#use-cases-and-advantages)
14. [Timeline and Evolution](#timeline-and-evolution)

---

## Introduction to .NET

.NET is a free, open-source developer platform developed by Microsoft, designed for building many types of applications including web, mobile, desktop, gaming, IoT, and more. Initially known as .NET Core, it evolved from the older .NET Framework.

- Cross-platform: Works on Windows, macOS, and Linux.
- Open source under the MIT License.
- Designed for high performance and cloud integration.
- Built with C# and C++.
- Features a mascot: the .NET Bot.

Official Docs: [Microsoft Learn](https://docs.microsoft.com/es-es/dotnet/)  
Source: [GitHub Repo](https://github.com/dotnet/core)

---

## Architecture and Compilation Process

1. High-level source code (C#, VB.NET, etc.) is compiled using specific compilers (`csc.exe`, `vbc.exe`, etc.)
2. The result is IL (Intermediate Language), stored in `.dll` or `.exe` files.
3. At runtime, the JIT (Just-In-Time) compiler converts IL to native machine code.
4. Native code is executed by the OS.

Visual summary:
- Source Code -> IL/MSIL -> JIT -> Native Code -> OS

---

## CLR - Common Language Runtime

- Core of .NET, executes IL code.
- Handles memory management, security, and exception handling.
- Converts CIL (Common Intermediate Language) to native code.
- JIT compiler optimizes at runtime.

---

## Roslyn Compiler

Roslyn is the modern .NET compiler platform supporting C# and Visual Basic.

**Features:**
- Compiles source to CIL (MSIL).
- Offers rich APIs for code analysis and transformation.
- Powers Visual Studio intellisense and error diagnostics.

**Uses:**
- Code analysis
- Refactoring tools
- Custom code generation
- DSL support

---

## Common Language Specifications (CLS) and CIL

- CLS defines rules for .NET languages to ensure interoperability.
- Source code is compiled to CIL, a CPU-independent set of instructions.
- Ensures applications can work together regardless of the language used.

---

## Common Type System (CTS)

- Defines all data types used in .NET languages.
- Ensures type safety and compatibility.
- Supports object-oriented features like inheritance and polymorphism.

Example types: `int`, `float`, `char`, `byte`, `string`, `object`

---

## Tools and IDEs

- **Visual Studio:** Full-featured IDE, Windows-only (Mac version exists but limited).
- **Visual Studio Code:** Lightweight, extensible, cross-platform.
- **RIDER:** Premium IDE from JetBrains, cross-platform.

---

## Project Structure and SDKs

### .csproj File
```xml
<Project Sdk="Microsoft.NET.Sdk">
  <PropertyGroup>
    <OutputType>Exe</OutputType>
    <TargetFramework>net6.0</TargetFramework>
    <ImplicitUsings>enable</ImplicitUsings>
  </PropertyGroup>
</Project>
```

### SDK Types
- `.NET SDK`: General-purpose
- `ASP.NET Core SDK`: Web apps & APIs
- `.NET Desktop SDK`: WPF, WinForms
- `.NET MAUI SDK`: Mobile & desktop UI
- `Blazor WebAssembly SDK`: Web in-browser
- `Worker Service SDK`: Background tasks
- `Azure Functions SDK`: Serverless
- `IoT SDK`: Embedded systems

---

## Compilation Modes

- **Debug Mode:** For development. Includes debug symbols, not optimized.
- **Release Mode:** Optimized for production. Smaller, faster, more secure.

Folders:
- `/bin`: Final output (`.dll`, `.exe`)
- `/obj`: Intermediate files

Command:
```bash
dotnet build --configuration release
```

---

## Important CLI Commands

```bash
dotnet new console -n MyApp      # Create console project
dotnet run                       # Run project
dotnet build                     # Compile project
dotnet restore                   # Restore dependencies
dotnet watch run                 # Auto-run on code changes
dotnet clean                     # Clean build output
dotnet --info                    # Info about .NET installation
dotnet --list-sdks               # List installed SDKs
```

---

## Package Management with NuGet

NuGet is the official package manager for .NET.

- Provides libraries, tools, and extensions.
- Custom NuGet servers can be created.

Command:
```bash
dotnet add package <PackageName>
```

---

## .NET Framework vs .NET Core

| Feature | .NET Framework | .NET Core (.NET 5+) |
|--------|----------------|----------------------|
| Platform | Windows only | Cross-platform |
| Performance | Moderate | High |
| App Types | Desktop, Web | All + Cloud & Mobile |
| IDE Dependency | Visual Studio | None (CLI friendly) |
| Support | Legacy | Modern & evolving |

---

## Use Cases and Advantages

**Use Cases:**
- Console apps
- Desktop (WPF, WinForms)
- Mobile (Xamarin, MAUI)
- Web (ASP.NET, Blazor)
- Cloud & Serverless (Azure)

**Advantages:**
- Cross-platform
- Interoperability
- Large ecosystem and community
- Free & Open Source
- Seamless Azure integration

---

## Timeline and Evolution

| Year | .NET | C# |
|------|------|----|
| 2000 | .NET Framework 1.0 | C# 1.0 |
| 2016 | .NET Core 1.0 | C# 7.0 |
| 2020 | .NET 5.0 | C# 9.0 |
| 2021 | .NET 6.0 | C# 10.0 |
| 2022 | .NET 7.0 | C# 11.0 |
| 2023 | .NET 8.0 | — |

---

For further learning, visit [Microsoft Learn](https://learn.microsoft.com/en-us/training/dotnet/) and the official [GitHub Repository](https://github.com/dotnet/core).

---

**End of Document**

