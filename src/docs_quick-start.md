---
permalink: "/docs/"
title: Getting Started with Live Documenter
layout: docs
---

# Getting Started

This page is an overview of the Live Documenter application and its basic uses.

__Live Documenter__ is a suite of applications and libraries that enable the automatic generation of documentation
from .NET code and xml comment files. Learn what Live Documenter is about from our [homepage](/).

## Desktop application
Starting up the desktop application will present you with the start screen. Here we can open projects, solutions or individual libraries. Click the open dialogue and select a project you are currently working on.

<div class="row justify-content-center">
<img src="/assets/images/documentation/ld-start-screen.png" alt="Live Documenter start screen">
</div>

You will be presented with a screen that shows in the left hand panel the namespaces that are defined in your project and in the right hand panel the documentation. Expanding namespaces and selecting items on the left hand side is a simple way to navigate through a project to find documentation.

<div class="row justify-content-center">
<img src="/assets/images/documentation/ld-open-docs.png" alt="Live Documenter documentation screen">
</div>

### Searching
A more convenient way of finding information is to use the search bar at the top of the left hand panel. Typing here will present you with a list of all the types and members that match your criteria.

<div class="row justify-content-center">
<img src="/assets/images/documentation/ld-search.png" alt="Searching in Live Documenter">
</div>

### Exporting
Live Documenter is packaged with a number of pre-built export configurations. Selecting the export option will present you with a dialogue to export your documentation.

<div class="row justify-content-center">
<img src="/assets/images/documentation/ld-export-dialogue.png" alt="Documentation export">
</div>

For now select the Web MSDN export, and note the location that it is being exported to. <em>Be careful not to output to an existing directory as the contents are cleaned prior to  exporting</em>. Hit the go button.

In a small amount of time the success message will be shown and your documentation is complete. Navigate to the folder and select the index.htm file to browse the documentation you have just created.

## More information
* [Live Documenter Project Files][ldproj-files]
* [Options][desktop-options]

[ldproj-files]: /docs/application/desktop/ldproj-files/
[desktop-options]: /docs/application/desktop/options/