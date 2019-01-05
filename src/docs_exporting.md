---
layout: docs
permalink: "/docs/export/"
---

# Exporting quick start

This page describes the process of exporting documentation via both the desktop application
and the command line application.

Exporting is a simple process in Live Documenter, you can export generated documentation from
the desktop and command line applications. The steps to export from both of these starts 
differently but the results are always the same.

## Exporting from the desktop application
Lets start by loading a project and exporting it to a web site.

<ol>
    <li><p>Firstly, open the Live Documenter application (default install path is c:\Program Files (x86)\The Box Software\Live Documenter).</p></li>
    <li><p>From the start screen click the `Open File...` button and navigate to a project or solution you have been working on.</p></li>
    <li><p>Now you can see the documentation from your project. The toolbar has a number of icons; click the icon indicated below to open
        the export dialogue.</p>
        <div class="row justify-content-center p-3">
            <img class="img-fluid" src="/assets/images/documentation/ld-manage-documentation-export.png">
        </div>
    </li>
    <li>
        <p>There are a number of settings here, but to keep it simple we are only going to change the `Export` option list to `Web Export: MSDN Lo Band Style`.</p>
        <div class="row justify-content-center p-3">
            <img class="img-fluid" src="/assets/images/documentation/ld-export-dialogue.png">
        </div>
    </li>
    <li>
        <p>Click the export button, you will see the progress dialogue. The time taken to export your documentation depends on the size of the project. But it
        will be nice and quick.</p>
    </li>
    <li><p>The default location for exported content is in your Documents folder in Live Documenter\Documentation. Navigate to that folder and open the index.htm file.</p></li>
    <li><p>You have just exported your first set of documentation using the Live Documenter. Congratulations.</p></li>
</ol>

## Exporting from the command line application
Exporting from the command line is a simpler process, as it is intended to run without user 
interaction.

Create a export configuration file. This simply details the project you wish to export, the 
members to export and the formats to export in. An example file is provided in the application's 
install directory. Open this for editing.

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<configuration>
    <document>c:\your-path\mysolution.sln</document>
    <!-- can be Public|Internal|Protected|ProtectedInternal|Private only those detailed will be output,
        not specifiying a filter section will result in only the Public members being exported.
    If these are specified and the document is an ldproj file then these will override the
    ldproj files filters. In the event that the document is not an ldprof file these will
    need to specified.
    -->
    <filters>
        <filter>Public</filter>
        <filter>Protected</filter>
        <filter>Internal</filter>
        <filter>InternalProtected</filter>
        <filter>Private</filter>
    </filters>
    <!-- the application will always check the ApplicationData folder for LDEC files -->
    <outputs>
        <!-- the locations being output to will be cleared without warning -->
        <ldec location="c:\temp\web\">web-msdn.ldec</ldec>
        <ldec location="c:\temp\htmlhelp-1\">htmlhelp1-msdn.ldec</ldec>
        <ldec location="c:\temp\htmlhelp-2\">htmlhelp2-msdn.ldec</ldec>
        <ldec location="c:\temp\helpviewer-1\">helpviewer1-msdn.ldec</ldec>
        <ldec location="c:\temp\xml\">xml.ldec</ldec>
    </outputs>
</configuration>
```

Modify the `document` entry to point to a project you wish to export. Leave the rest of the content 
the same, this will export all members to multiple outputs in a `c:\temp directory`.

Open the command prompt and navigate to the install directory.

Run the command `exporter -v example-configuration.xml`. The `-v` option simply increases the amount
of information displayed during the export.

<div class="row justify-content-center p-3">
    <img class="img-fluid" src="/assets/images/documentation/command-line-output.png">
</div>

After the export has complete navigte to the `c:\temp` directory to view your exported files.
