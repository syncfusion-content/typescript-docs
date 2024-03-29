---
layout: post
title: TypeScript NuGet Packages | Syncfusion
description: NuGet Packages manager for the .NET framework. The NuGet client tools simplify the process of installing and upgrading packages.
platform: typescript
control: NuGet Packages
documentation: ug
---

# NuGet Packages

NuGet is a package manager for the .NET framework. The NuGet client tools simplify the process of installing and upgrading packages. This can be used to automatically add files and references to your Visual Studio projects.

N> You can use the Syncfusion TypeScript NuGet packages without installing the Essential Studio or TypeScript platform installation to implement the Syncfusion TypeScript controls.

## Get the Syncfusion NuGet feed URL

You should get the private Syncfusion JavaScript NuGet feed URL to install or upgrade the Syncfusion TypeScript NuGet packages. To get the URL from Syncfusion website use the following steps:

1. Navigate to [nuget.syncfusion.com](https://nuget.syncfusion.com/), and select **WEB** tab.     

2. Navigate to **WEB(Essential JS1)**, click the Copy URL label under JavaScript platform to copy the Syncfusion JavaScript platform NuGet feed to clipboard or directly use the following URL: 

    [https://nuget.syncfusion.com/nuget_javascript/nuget/getsyncfusionpackages/javascript](https://nuget.syncfusion.com/nuget_javascript/nuget/getsyncfusionpackages/javascript) 

    ![NuGet feed URL in Typescript NuGet Packages](nuget_packages_images/typescript-nuget-packages-feed-url.png)

3. Now, use this NuGet feed URL to access the Syncfusion NuGet Packages in Visual Studio. 

## Add the Syncfusion NuGet feed URL

### Windows

1.	Open your Visual Studio application. 

2.	On the **Tools** menu, select **Options**.

3.	Expand the **NuGet Package Manager** and select **Package Sources**.

4.	Click the **Add** button (green plus), and enter the ‘Package Name’ and ‘Package Source URL’ of the Syncfusion TypeScript NuGet packages.
    
    **Name:** Name of the package listed in the available package sources.
    
    **Source:** Syncfusion JavaScript NuGet Feed URL      
    [https://nuget.syncfusion.com/nuget_javascript/nuget/getsyncfusionpackages/javascript](https://nuget.syncfusion.com/nuget_javascript/nuget/getsyncfusionpackages/javascript).

5.	Click the **Update** button to add the name and source details to package sources. 

    ![Package Sources in Typescript NuGet Packages](nuget_packages_images/typescript-nuget-packages-sources.png)

### macOS 

1.	Open your Visual Studio application. 

2.	Right-click on the Packages folder in the project, and then select **Add Packages…**
 
    ![Add Packages in Typescript NuGet Packages](nuget_packages_images/typescript-nuget-packages-add-packages.png)

3.	Choose the **Configure Sources…** from the dropdown that appears in the left corner of the Add Packages dialog. 

    ![Configure Sources in Typescript NuGet Packages](nuget_packages_images/typescript-nuget-packages-configure-sources.png)

4.	At the bottom right corner of the dialog, click the **Add** button to enter the feed name and the URL. 
   
    **Name:** Enter the name (For e.g., Syncfusion TypeScript Packages).
   
    **Location:** Enter the following URL – [https://nuget.syncfusion.com/nuget_javascript/nuget/getsyncfusionpackages/javascript](https://nuget.syncfusion.com/nuget_javascript/nuget/getsyncfusionpackages/javascript).

    ![Syncfusion TypeScript Packages](nuget_packages_images/typescript-nuget-packages-syncfusion-source.png)
 
5.	Now, click **Add Source** and then click **OK**.

## Installing NuGet Packages

### Using NuGet Package Manager

The NuGet Package Manager can be used to search and install NuGet packages in the Visual Studio solution or project:

1.	On the **Tools**, menu, NuGet `Package Manager | Manage NuGet Packages for Solution...`

    ![Manage NuGet Packages in Typescript](nuget_packages_images/typescript-nuget-packages-manage.png)

    Alternatively, right-click on the project/solution in Solution Explorer tab, and choose **Manage NuGet Packages…**

2.	By default, the NuGet.org package is selected in the **Package source** drop-down. Select your appropriate feed name that you configured. 

     ![Install NuGet Packages in Typescript](nuget_packages_images/typescript-nuget-packages-installation.png)             

3.	The NuGet Packages are listed and available in the package source feed URL. Search and install the required packages in your application, by clicking **Install** button.

### Using Package Manager Console

To reference the Syncfusion TypeScript component using the Package Manager Console as NuGet packages, 

1.	On the **Tools** menu, select **NuGet Package Manager** and then **Package Manager Console**. 

2.	Run the following NuGet installation commands: 

    ~~~
    #install specified package in default project
    Install-Package <Package Name>

    #install specified package in default project with specified package source
    Install-Package <Package Name> -Source <Source Location>

    #install specified package in specified project 
    Install-Package <Package Name> - ProjectName <Project Name>
    ~~~

    **For example:**

    ~~~
    #install specified package in default project
    Install-Package Syncfusion.Ej.Web.TypeScript.DefinitelyTyped

    #install specified package in default project with specified Package Source
    Install-Package Syncfusion.Ej.Web.TypeScript.DefinitelyTyped -Source “http://nuget.syncfusion.com/nuget_javascript/nuget/getsyncfusionpackages/javascript”

    #install specified package in specified project 
    Install-Package Syncfusion.Ej.Web.TypeScript.DefinitelyTyped -ProjectName SyncfusionDemoApplication
    ~~~

### Using Visual Studio for macOS

Add packages can be used to search and install NuGet packages to the Visual Studio project in macOS:

1.	Right-click on the folder in the project, and then select **Add Packages…** 

    ![Add Packages in macOS Typescript](nuget_packages_images/typescript-nuget-packages-project-folder.png)  
              
2.	By default, the NuGet.org package is selected in the **Package source** drop-down. Select the appropriate feed name. 

    ![Install Packages in macOS Typescript](nuget_packages_images/typescript-nuget-packages-feed-name.png)  

3.	The Syncfusion TypeScript NuGet Packages available in the package source location will be listed. Search and install the required packages in your application, by clicking **Add Package** button.

## Managing NuGet package using NuGet CLI

The NuGet Command Line Interface (CLI), nuget.exe, provides the full extent of NuGet functionality to install, create, publish, and manage packages without making any change to the project files.

### Configure NuGet feed URL 

1.	Download the latest NuGet CLI from [here](https://dist.nuget.org/win-x86-commandline/latest/nuget.exe).

    N> To update the existing nuget.exe to latest version use the following command:

    ~~~
    nuget update -self
    ~~~

2.	Open the downloaded executable location in the command window, and run the following commands to configure the Syncfusion TypeScript NuGet packages: 

    ~~~
    #Add specified package source in NuGet.config file for Windows platform
    nuget.exe Sources Add –Name <Source name> –Source <Source location>

    #Add specified Package Source in Nuget.config file for MAC/Linux platform
    mono nuget.exe Sources Add –Name <Source name> –Source <Source location>
    ~~~

    **For example:**

    ~~~
    #For Windows platform
    nuget.exe Sources Add –Name “Syncfusion Source” –Source “http://nuget.syncfusion.com/nuget_javascript/nuget/getsyncfusionpackages/javascript”

    #For MAC/Linux platform
    mono nuget.exe Sources Add –Name “Syncfusion Source” –Source “http://nuget.syncfusion.com/nuget_javascript/nuget/getsyncfusionpackages/javascript”
    ~~~

### NuGet installation

Download and install the required NuGet packages to a project specified in the package.config. 

~~~
#install specified package in default project from specified package source for Windows Platform 
nuget.exe install <Package name | ConfigFilePath > <Options>

#install specified package in default project from specified package source for MAC/Linux Platform 
mono nuget.exe install <Package name | ConfigFilePath > <Options>
~~~

N> configPath is optional. This identifies the packages.config or solutions file that lists the packages utilized in the project. 

**For example:**

~~~
#install specific package for Windows 
nuget.exe install “Syncfusion.Ej.Web.TypeScript.DefinitelyTyped”

#install all package which mention in package.config path for Windows 
nuget.exe install “C:\Users\SyncfusionApplication\package.config”

#install specific Syncfusion TypeScript NuGet package with Syncfusion JavaScript NuGet feed for Windows 
nuget.exe install “Syncfusion.Ej.Web.TypeScript.DefinitelyTyped” –Source “http://nuget.syncfusion.com/nuget_javascript/nuget/getsyncfusionpackages/javascript”

#install specific package for Mac and Linux 
mono nuget.exe install “Syncfusion.Ej.Web.TypeScript.DefinitelyTyped”

#install all package which mention in package.config path for Mac and Linux 
mono nuget.exe install “C:\Users\SyncfusionApplication\package.config”

#install specific Syncfusion TypeScript NuGet package with Syncfusion JavaScript NuGet feed for Mac and Linux 
mono nuget.exe install “Syncfusion.Ej.Web.TypeScript.DefinitelyTyped” –Source “http://nuget.syncfusion.com/nuget_javascript/nuget/getsyncfusionpackages/javascript”
~~~

## Upgrading NuGet packages

### Using NuGet Package Manger 

NuGet packages can be updated to their specific version or latest version available in the Visual Studio solution or project:

1. On the **Tools** menu, `NuGet Package Manager | Manage NuGet Packages for Solution...`
    Alternatively, right-click on project/solution in the Solution Explorer tab, and choose **Manage NuGet Packages…**

2. Select the **Updates** tab to see the packages available for update from the desired package sources. Select the required packages and the specific version from the dropdown, and click the **Update** button.

### Using Visual Studio for macOS

Using **Update** context menu from Visual Studio for Mac application, NuGet packages can be updated:

1.	Right-click on the Packages folder in the project, and select **Update**. 

    ![NuGet packages update in macOS Typescript](nuget_packages_images/typescript-nuget-packages-update.png) 

2.	This will update the NuGet package to the latest version. You can double-click Add packages and choose the specific version.

N> To update all the projects from solution, use update option in the solution level. 

### Using Package Manger Console

To update the installed Syncfusion TypeScript NuGet packages using the Package Manager Console: 

1.	On the **Tools** menu, select **NuGet Package Manager**, and then **Package Manager Console.** 

2.	Run the following NuGet installation commands:

    ~~~ 
    #Update specific NuGet package in default project
    Update-Package <Package Name>

    #Update all the packages in default project
    Update-Package 

    #Update specified package in default project with specified package source
    Update-Package <Package Name> -Source <Source Location>

    #Update specified package in specified project 
    Update-Package <Package Name> - ProjectName <Project Name>
    ~~~

    **For example:**

    ~~~
    #Update specified Syncfusion TypeScript NuGet package 
    Update-Package Syncfusion.Ej.Web.TypeScript.DefinitelyTyped

    #Update specified package in default project with specified Package Source
    Update-Package Syncfusion.Ej.Web.TypeScript.DefinitelyTyped –Source “http://nuget.syncfusion.com/nuget_javascript/nuget/getsyncfusionpackages/javascript” 

    #Update specified package in specified project 
    Update-Package Syncfusion.Ej.Web.TypeScript.DefinitelyTyped -ProjectName SyncfusionDemoApplication

    ~~~

### Using NuGet CLI

Using the NuGet CLI, all the NuGet packages in the project can be updated to the available latest version: 

1.	Download the latest NuGet CLI from [here](https://dist.nuget.org/win-x86-commandline/latest/nuget.exe).

    N> To update the existing nuget.exe to latest version use the following command: 

    ~~~
    nuget update -self
    ~~~

2.	Open the downloaded executable location in the command window. Run the following “update commands” to update the Syncfusion JavaScript NuGet packages.

    ~~~ 
    #update all NuGet packages from config file
    nuget update <configPath> [options]

    #update all NuGet packages from specified Packages Source
    nuget update -Source <Source Location> [optional]
    ~~~      

    N> configPath is optional. This identifies the packages.config or solutions file lists the packages utilized in the project. 
	
    **For example:**

    ~~~          
    #Update all NuGet packages from config file
    nuget update “C:\Users\SyncfusionApplication\package.config”

    #Update all NuGet packages from specified Packages Source
    nuget update -Source “http://nuget.syncfusion.com/nuget_javascript/nuget/getsyncfusionpackages/javascript”
    ~~~

    N> Update command is not working as expected in Mono (Mac and Linux) and projects using PackageReference format.
   





