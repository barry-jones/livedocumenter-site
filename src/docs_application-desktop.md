---
layout: docs
permalink: "/docs/application/desktop/"
title: Live Documenter Desktop Application
---

# Live Documenter Desktop

The desktop application enables a live view of your current project documentation and exporting your content to web, compiled help and other formats. Helping developers get up to speed on projects quicker.

## Get Started

Use the _Open file..._ button to navigate to your solution, project or dll file and open it. You will be immediately shown the documentation.

<div class="row justify-content-center p-3">
    <img class="fluid-img image_border" style="max-width: 800px" src="/assets/images/documentation/ld_desktop_loaded.png" alt="Live Documenter toolbar" />
</div>


You can now use the left hand pane to navigate through the namespaces, classes and members and view the documentation for your selection on the right.

Have a look around and enjoy. If you need more details, the interface and available functionality are below.

## Getting around the application

The toolbar provides a quick way to access the major functionality available in Live Documenter.

<div class="row justify-content-center p-3">
    <img class="fluid-img image_border" src="/assets/images/documentation/ld-manage-documentation.png" alt="Live Documenter toolbar" />
</div>

The options from left to right are:

<ul>
    <li>
        <p>File open - this allows you to open a new project for viewing.</p>
    </li>
    <li>
        <p>Save - Saving, allows you to store your current settings and configuration as a Live Documenter project file. These files
        can be used as a basis for exporting in the command line application.</p>
    </li>
    <li>
        <p>Print - prints the currently viewed document.</p>
    </li>
    <li>
        <p>Export - produce a static version of the documentation for the entire project you are viewing. Examples of export functionality can be found <a href="/docs/export/examples/">here</a>.
        </p>
    </li>
    <li>
        <p>Go back - navigate to the previously viewed page.</p>
    </li>
    <li>
        <p>Go forward - navigate forward through your navigation history.</p>
    </li>
    <li>
        <p>Add files to project - adds additional projects, solutions or libraries to your current documentation set.</p>
    </li>
    <li>
        <p>Remove files from project - removes libraries from your current project. See <a href="/application/desktop/ldproj-files">here</a> for more information about ldproj files.</p>
    </li>
</ul>


### View settings

At the bottom of the page of the document a number of settings are available that control how you view the documentation. These  settings are saved in your user profile so only need to be changed once.

<div class="row justify-content-center p-3">
    <img class="fluid-img" src="/assets/images/documentation/view-options.png" alt="View options" />
</div>

From left to right these settings are:

<ul>
    <li>
        <p>Page view - view all content for this entry as a collection of single pages which can be navigated.</p>
    </li>
    <li>
        <p>Multi coloumn view - View the current entry in multiple columns.</p>
    </li>
    <li>
        <p>Single scrollable view - view the docuementation for the current entry as a single contigous page that can be scrolled.</p>
    </li>
    <li>
        <p>Font size - change the size (decreease and increase) of the font used.</p>
    </li>
</ul>

### Live updating
One of the many features of the Live Documenter is that it continually displays a live up-to-date representation of your project documentation. Every time you perform a build of your software in Visual Studio (or otherwise modify the binaries) Live Documenter will automatically reload the documentation so your view is up to date.

This feature happens automatically and requires no configuration.

## Overview

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

## More information
* [Live Documenter Project Files][ldproj-files]
* [Options][desktop-options]

[ldproj-files]: /docs/application/desktop/ldproj-files/
[desktop-options]: /docs/application/desktop/options/