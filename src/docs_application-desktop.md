---
layout: docs
permalink: "/docs/application/desktop/"
title: Live Documenter Desktop Application
---

<h1>Live Documenter Desktop Application</h1>

<p>This document describes the desktop application which provides a live, up-to-date view of a your documentation. It also allows you to export documentation as a one-off.</p>

<p>The application can be started from your installation directory or from the desktop icon. On opening the application you will be presented with the start screen. This allows you to select from a recent list of files you have opened or to open a new file to view the documentation.</p>

<p>Files that can be opened are, sln, dll, vs project files and Live Documenter project files (ldproj).</p>

<h2>Toolbar</h2>
<div class="image">
    <img src="/assets/images/documentation/ld-manage-documentation.png" alt="Live Documenter toolbar" />
</div>
<p>The options from left to right are:</p>
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
        <p>Export - produce a static version of the documentation for the entire project you are viewing.</p>
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

<h2>View settings</h2>
<p>At the bottom of the page of the document a number of settings are available that control how you view the documentation. These 
    settings are saved in your user profile so only need to be changed once.</p>
<div class="image">
    <img src="/assets/images/documentation/view-options.png" alt="View options" />
</div>
<p>From left to right these settings are:</p>
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

<h2>Live updating</h2>
<p>One of the many features of the Live Documenter is that it continually displays a live up-to-date representation of your project documentation. 
    Every time you peform a build of your software in Visual Studio (or otherwise modify the binaries) Live Documenter will automatically reload
    the documentation so your view is up to date.</p>
<p>This feature happens automatically and requires no configuration.</p>