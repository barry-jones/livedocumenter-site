---
permalink: "/docs/"
title: Getting Started with Live Documenter
layout: docs
---

# Getting Started

This page is an overview of the Live Documenter and its basic uses.

__Live Documenter__ is a suite of applications and libraries that enable the automatic generation of documentation
from .NET code and xml comment files. Learn what Live Documenter is about from our [homepage](/) and [download](/download) the latest version.

## Let's quickly generate some documentation

Live Documenter makes it quick and easy to create a basic documentation site, much like MSDN, 
in a matter of seconds. There are a couple of ways to start, but let's use the console application.

Navigate, in a terminal, to the install location of the application and type the following:

```shell
exporter -v example-configuration.xml
```

You will see output like the following:

```shell
Live Documenter Exporter Version: 2.0.4.0

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

<div class="note">
The application does not currently support the new VS 2017 csproj files. In this instance select the compiled output to document instead.
</div>

## Getting to know Live Documenter

The application comprises of three seperate parts, the first is the console application you have just seen; the second is a desktop client and third is a programatic API.

### Desktop

Starting up the desktop application will present you with the start screen. Here we can open projects, solutions or individual libraries. Click the open dialogue and select a project you are currently working on.

You will be presented with a screen that shows in the left hand panel the namespaces that are defined in your project and in the right hand panel the documentation. Expanding namespaces and selecting items on the left hand side is a simple way to navigate through a project to find documentation.

<div class="row justify-content-center p-3">
<img class="img-fluid image_border" src="/assets/images/documentation/ld-open-docs.png" alt="Live Documenter documentation screen">
</div>

A more convenient way of finding information is to use the search bar at the top of the left hand panel. Typing here will present you with a list of all the types and members that match your criteria.

<div class="row justify-content-center p-3">
<img class="img-fluid image_border" src="/assets/images/documentation/ld-search.png" alt="Searching in Live Documenter">
</div>

Live Documenter is packaged with a number of pre-built export configurations. Selecting the export option will present you with a dialogue to export your documentation.

<div class="row justify-content-center p-3">
<img class="img-fluid image_border" src="/assets/images/documentation/ld-export-dialogue.png" alt="Documentation export">
</div>

For now select the Web MSDN export, and note the location that it is being exported to. <em>Be careful not to output to an existing directory as the contents are cleaned prior to  exporting</em>. Hit the go button.

In a small amount of time the success message will be shown and your documentation is complete. Navigate to the folder and select the index.htm file to browse the documentation you have just created.
