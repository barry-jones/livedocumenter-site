---
permalink: "/docs/"
title: Getting Started with Live Documenter
layout: docs
---

# Getting Started

This page is an overview of the Live Documenter and its basic uses.

__Live Documenter__ is a suite of applications and libraries that enable the automatic generation of documentation
from .NET code and xml comment files. Learn what Live Documenter is about from our [homepage](/) and [download](https://github.com/barry-jones/live-documenter/releases/tag/v2.0.5) the latest version from GitHub.

## Let's quickly generate a website

Live Documenter makes it quick and easy to create a basic documentation site, much like MSDN, in a matter of seconds. There are many
ways to start but we will use the console application first.

```shell
exporter example-configuration.xml
```

Running the above will create documentation in the `c:\temp` directory for the TheBoxSoftware.Reflection.dll library. You will see that a number of folders exist, in this instance we are interested in `c:\temp\web\LD Export - 20190104 1359\`. Open the `index.htm` file in your favourite browser.

Using the example-configuration.xml file we are able to change which members and types we want to appear in the documentation by changing the
visibility filters. We are able to control the formats the documentation will be output in. Currently, documentation can be exported in web, XML,
Compiled Help (HTML Help1), and HTML Help 2 and Help Viewer 1 formats.

We are also able to select a .NET library, project of solution which contains the code we want to produce documentation for.

More details for configuring and using the console application can be found in the [documentation](/docs/application/exporter/).

## Desktop application
Starting up the desktop application will present you with the start screen. Here we can open projects, solutions or individual libraries. Click the open dialogue and select a project you are currently working on.

<div class="row justify-content-center">
    <img class="img-fluid" src="/assets/images/documentation/ld-start-screen.png" alt="Live Documenter start screen">
</div>

You will be presented with a screen that shows in the left hand panel the namespaces that are defined in your project and in the right hand panel the documentation. Expanding namespaces and selecting items on the left hand side is a simple way to navigate through a project to find documentation.

<div class="row justify-content-center">
<img class="img-fluid" src="/assets/images/documentation/ld-open-docs.png" alt="Live Documenter documentation screen">
</div>

### Searching
A more convenient way of finding information is to use the search bar at the top of the left hand panel. Typing here will present you with a list of all the types and members that match your criteria.

<div class="row justify-content-center">
<img class="img-fluid" src="/assets/images/documentation/ld-search.png" alt="Searching in Live Documenter">
</div>

### Exporting
Live Documenter is packaged with a number of pre-built export configurations. Selecting the export option will present you with a dialogue to export your documentation.

<div class="row justify-content-center">
<img class="img-fluid" src="/assets/images/documentation/ld-export-dialogue.png" alt="Documentation export">
</div>

For now select the Web MSDN export, and note the location that it is being exported to. <em>Be careful not to output to an existing directory as the contents are cleaned prior to  exporting</em>. Hit the go button.

In a small amount of time the success message will be shown and your documentation is complete. Navigate to the folder and select the index.htm file to browse the documentation you have just created.

## More information
* [Live Documenter Project Files][ldproj-files]
* [Options][desktop-options]

[ldproj-files]: /docs/application/desktop/ldproj-files/
[desktop-options]: /docs/application/desktop/options/