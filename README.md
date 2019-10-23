## **THIS PROJECT AND REPOSITORY ARE NO-LONGER MAINTAINED**

Since August 2019 I've modified this project to use `Microsoft.Extensions.DependencyInjection` instead of Unity (so that I can eventually transition my ASP.NET projects to ASP.NET Core) and I've reposted the project to https://github.com/Jehoel/AspNetDependencyInjection where all active development is.

I've since added significantly more functionality to the `AspNetDependencyInjection` project (such as support for SignalR, MVC and WebAPI (and a WCF sample)) so I don't recommend anyone uses this project anymore. If you are using Unity then you should still use `AspNetDependencyInjection` because you can adapt Unity for use with `Microsoft.Extensions.DependencyInjection` (see https://github.com/unitycontainer/microsoft-dependency-injection ).

What follows is this project's README (which is now obsolete)


# Unity.WebForms

(Currently listed on NuGet.org as `Jehoel.Unity.AspNetWebForms`)

**Unity.WebForms** is a collection of various ideas on Dependency Injection utilizing the [Unity](http://unity.codeplex.com/) container in ASP.NET WebForm applications, formalized into a single NuGet package for easy integration into an existing application.

This package was inspired by similar packages from DevTrends, specifically:

* [DevTrends Unity.MVC3](http://nuget.org/packages/Unity.Mvc3/)
* [DevTrends Unity.WCF](http://nuget.org/packages/Unity.Wcf/)

The only difference is that this packages is a DLL integration with minimal source code added. The only source file added is to allow the configuration of the Unity container with your types.

This particular package (`Jehoel.Unity.AspNetWebForms`) and repo (at [https://github.com/Jehoel/Unity.WebForms](https://github.com/Jehoel/Unity.WebForms)) is a git fork of S. Kyle Korndoerfer's original project at [https://bitbucket.org/KyleK/unity.webforms](https://bitbucket.org/KyleK/unity.webforms) with a main objective of supporting ASP.NET WebForms 4.7.2's new `WebObjectActivator` which means that `Page`, `UserControl` and other types can use true constructor dependency injection.

This repo's objectives are:
* Update to .NET Framework 4.7.2 (done)
* Update existing dependencies, including Unity 5 (done)
* Add in support for WebObjectActivator, as per Microsoft's example at https://github.com/aspnet/AspNetWebFormsDependencyInjection (done)
* Update the sample project (done)
* Publish to NuGet (`Jehoel.Unity.AspNetWebForms`) (done)
* Add more tests (in progress)
* Add support for DI constructor injection for `HttpModule`s

## Current Version
* 1.4 (S. Kyle Korndoerfer's most recent version, released in 2015)
* 2.0 (this repo and project, updated in 2019 for ASP.NET 4.7.2 and WebObjectActivator)

## NuGet Gallery

### Version 1.4 (.NET 4.5, no support for WebObjectActivator)

[http://nuget.org/packages/Unity.WebForms](http://nuget.org/packages/Unity.WebForms)

### Version 2.0 (.NET 4.7.2, with support for WebObjectActivator)

[http://nuget.org/packages/Jehoel.Unity.AspNetWebForms](http://nuget.org/packages/Jehoel.Unity.AspNetWebForms)

## Installation and Getting Started

Please see the `GETTING_STARTED.md` file in the GitHub repository: [https://github.com/Jehoel/Unity.WebForms/blob/master/GETTING_STARTED.md](https://github.com/Jehoel/Unity.WebForms/blob/master/GETTING_STARTED.md)

## References / Links
Here are some of the sources used for building out this package:

* `Unity.WebForms`:
	* [Dependency Injection in ASP.NET WebForms](http://litemedia.info/dependency-injection-in-asp.net-webforms) - Mikael Lundin
	* [Unity: How to registerType with a PARAMETER constructor](http://stackoverflow.com/a/4007337)
	* [Unity.MVC3](http://unitymvc3.codeplex.com/) - The linked articles on the bottom helped a lot with infrastructure
* `Jehoel.Unity.AspNetWebForms`:
	* [Announcing the .NET Framework 4.7.2](https://devblogs.microsoft.com/dotnet/announcing-the-net-framework-4-7-2/) - This article announced support for constructor-based DI.
	* [Use Dependency Injection In WebForms Application](https://devblogs.microsoft.com/aspnet/use-dependency-injection-in-webforms-application/)
	* [AspNetWebFormsDependencyInjection on Github](https://github.com/aspnet/AspNetWebFormsDependencyInjection)
	* [Sample example of using AspNetWebFormsDependencyInjection](https://github.com/Jinhuafei/examples/tree/master/DependencyInjection) - ([Repository snapshot](https://github.com/Jinhuafei/examples/tree/c6ddec606c710dde3a3c8747067d088c261d0cff))
	* [Official Unity project for ASP.NET MVC](https://github.com/unitycontainer/aspnet-mvc)

## Copyright
* Copyright 2013 - 2015 [S. Kyle Korndoerfer](https://bitbucket.org/KyleK)
* Copyright 2019 [Dai Rees](https://github.com/Jehoel)


## License
Unity.WebForms is under the MIT license - [http://www.opensource.org/licenses/mit-license](http://www.opensource.org/licenses/mit-license)

[wiki]:https://bitbucket.org/KyleK/unity.webforms/wiki/
