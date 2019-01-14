---
permalink: "/docs/"
title: Getting Started with Live Documenter
layout: docs
---

# Getting Started

__Live Documenter__ is a suite of applications and libraries that enable the live viewing and automatic generation of documentation from .NET code and xml comment files. Learn what Live Documenter is from our [homepage](/) and [download](/download) the latest version.

## Let's quickly generate some documentation

Live Documenter makes it quick and easy to create a basic documentation site, much like MSDN, 
in a matter of seconds. There are a couple of ways to start, but let's use the console application.

Navigate, in a terminal, to the install location of the application and type the following:

```shell
exporter example-configuration.xml
```

You will see output like the following:

```shell
Live Documenter Exporter Version: 2.1

Details:
  Visible members: (Public|Protected|Internal|InternalProtected|Private)
  theboxsoftware.reflection.dll contains 2443 members and types.

Exporting with web-msdn.ldec to location c:\temp\web\.
The export began at 06/01/2019 15:04:28.
Export started
  Export as XML...
```

Documentation will have been created in the `c:\temp` directory. You will see that a number of folders exist, in this instance we are interested in `c:\temp\web\LD Export - <timestamp>\`. Open the `index.htm` file in your favourite browser.

We have used the example configuration file so far, which generated documentation for the `TheBoxSoftware.Reflection.dll` library. You can modify the file to work with your own code.

```xml
<xml version="1.0" encoding="UTF-8" ?>
<configuration>
    <document>c:\your-path\mysolution.sln</document>

    <filters>
        <filter>Public</filter>
        <filter>Protected</filter>
        <filter>Internal</filter>
        <filter>InternalProtected</filter>
        <filter>Private</filter>
    </filters>

    <outputs>
        <ldec location="c:\temp\web\">web-msdn.ldec</ldec>
        <ldec location="c:\temp\htmlhelp-1\">htmlhelp1-msdn.ldec</ldec>
        <ldec location="c:\temp\htmlhelp-2\">htmlhelp2-msdn.ldec</ldec>
        <ldec location="c:\temp\helpviewer-1\">helpviewer1-msdn.ldec</ldec>
        <ldec location="c:\temp\xml\">xml.ldec</ldec>
    </outputs>
</configuration>
```

Simply change the `document` element to point to a library, project or solution of your choosing. More details for configuring and using the console application can be found in the [documentation](/docs/application/exporter/).

## Getting to know Live Documenter

Live Documenter is a desktop application, command line utility and API library. All designed to make it easy to use Live Documenter to utilise the XML code comments in .NET applications. Live view, static help files and more dynamic implementations via the API.

Three ways to utilise your documentation that fits your work style, projects and organisation.

### Desktop

The desktop application provides a live view of your project, this updates every time the library is recompiled or the solution/project changes. 

Have Live Documenter open on your next project and have the entire project documentation available to you. Quickly search through for specific members. Print pages or export the entire site to a compiled help or website.

<div class="row justify-content-center p-3">
    <img class="fluid-img image_border" style="max-width: 841px" src="/assets/images/documentation/ld_desktop_preview.png" alt="Preview of desktop application" />
</div>

For a full description of the desktop application and its features, be sure to [view](/docs/application/desktop/) the more detailed docs.

### Command line utility

A utility for exporting documentation to static content. Export your docs to a web site or to the web, xml and compiled help in one go. Integrate in to build steps or use ad-hoc, flexible fast access to documentation generation.

<div class="row justify-content-center p-3">
    <img class="fluid-img image_border" style="max-width: 594px" src="/assets/images/documentation/ld_console_preview.png" alt="Preview of console application" />
</div>

For a full description of the command line application and its features, be sure to [view](/docs/application/exporter/) the more detailed docs.

### API library

For a full description of the API library and how to utilise it, be sure to [view](/docs/api/index.html) the API section of the documentation.

The API (application programming interface) provided by the Live Documenter enables you to have more flexibility over documentation that is generated. In essence it allows you to load a library or project and produce documentation on request a single page at a time.

This would allow you to, for example, create a web site which watches a .NET library and associated XML comments. Displaying the latest documentation all the time. The API is used to provide this functionality for the Live Documenter API documentation.

```cs
Documentation docs = new Documentation("myfile.dll");
docs.Load();

// get a page of documentation
XmlDocument xmlDocument = new XmlDocument();
xmlDocument.LoadXml(
	docs.Find("T:System.String"); // searching can be performed using cref paths
	);
```

## Thanks

Thanks for showing an interest in the Live Documenter. We hope you enjoy the application and find it useful. We are always looking for feedback and help, if you are interested you can help make Live Documenter better on [GitHub](https://github.com/barry-jones/live-documenter).