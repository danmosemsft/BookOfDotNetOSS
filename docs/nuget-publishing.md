﻿# Publishing a NuGet Package

NuGet is more than just NuGet.org. Here are some of the different places to publish an OSS NuGet package:

* **[NuGet.org](https://www.nuget.org/)** is the primary online repository for NuGet packages. All packages on NuGet.org are publicly available to everyone. By default, Visual Studio has nuget.org as a package source and for many developers this is the only package repository they will interact with. Stable packages and pre-release packages you want community feedback on should be published here.

* The **[MyGet](https://myget.org/)** repository service supports free custom package feeds for open source projects. A MyGet public custom feed is an ideal place to publish pre-release packages created by your CI service. MyGet also provides private feeds commercially.

* A **local feed** allows you to treat a folder like a package repository and `*.nupkg` files in the folder are accessible by NuGet. A local feed is useful for testing a NuGet package prior to publishing it to NuGet.org.

> [!NOTE]
> Nuget.org does not allow a package to be deleted once it is uploaded. A package can be unlisted so that it is not publicly visible in the UI but the `*.nupkg` can still be downloaded on restore. Also, nuget.org does not allow duplicate package versions. To correct a NuGet package with an error you have to unlist the incorrect package, increment the version number and publish a new version of the package.

**✓ DO** publish stable packages and pre-release packages you want community feedback on to NuGet.org.

**✓ CONSIDER** publishing pre-release packages to a MyGet feed from a continuous integration build.

**✓ CONSIDER** testing packages in your development environment using a local feed.

**More Information**

* [Publish a package to NuGet.org](https://docs.microsoft.com/en-us/nuget/create-packages/publish-a-package)
* [Deleting packages on NuGet.org](https://docs.microsoft.com/en-us/nuget/policies/deleting-packages)
* [MyGet open source offer](https://www.myget.org/opensource)
* [NuGet local feeds](https://docs.microsoft.com/en-us/nuget/hosting-packages/local-feeds)

## NuGet.org Security

It is important that bad actors cannot access your NuGet account and upload a malicious version of your library. NuGet.org offers two-factor authentication and email notifications when a package is published. Enable these features after logging into NuGet.org on the **Account settings** page.

![alt text](../images/nuget-2fa.png "NuGet Account Security")

**✓ DO** use a Microsoft account to login to NuGet.

**✓ DO** enable two factor authentication for accessing NuGet.

**✓ DO** enable email notification when a package is published.