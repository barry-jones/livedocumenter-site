---
layout: docs
title: Exporter application
permalink: "/docs/application/exporter/"
---
<h1>Live Documenter Command Line Exporter</h1>
<p>The exporter application is useful for integrating documentation generation in to existing processes; such as your 
    build scripts. An application that works on the command line can be simply called.</p>

<p>The parameters accepted by the exporter are:</p>

```shell
exporter [modifiers] <filename>

    modifiers:
    -h		 show help information
    -v           show verbose export details
    <filename>   The path to the configuration xml file
```


<h3>Commands</h3>
<table>
    <thead>
        <tr>
            <th>Action</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>-h</td>
            <td>Displays the help information above.</td>
        </tr>
        <tr>
            <td>-v</td>
            <td>Outputs the steps for the export instead of just the fact it has started an export. With or without this modifier it will always display the warnings and errors.</td>
        </tr>
        <tr>
            <td>&lt;filename></td>
            <td>The file path to the configuration file that details the export.</td>
        </tr>
    </tbody>
</table>

<h2>Export configuration files</h2>

<p>An export configuration file contains the following information.</p>

```xml
<xml version="1.0" encoding="UTF-8" ?>
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

<p>The <code>document</code> element is a path to your solution, project, .NET dll or ldproj file. Only one document can be specified.</p>

<p><code>filters</code> determine the visibility of the members that will be exported. If these are not specified it will default to Public and Protected.</p>

<p>Finally, <code>outputs</code> detail the location of published files and the LDEC file used to perform the export. One or more outputs can be defined here. Each one will be exported in turn.</p>

<p>Please <em>note</em> that, just like the desktop application, the output locations will be cleared before the new export will continue.</p>