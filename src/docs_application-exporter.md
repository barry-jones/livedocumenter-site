---
layout: docs
title: Exporter application
permalink: "/docs/application/exporter/"
---
# Command Line Exporter

This page describes how to use the command line application to export documentation.

The exporter application is useful for integrating documentation generation in to existing 
processes; such as your build scripts. An application that works on the command line can be
simply called.

The parameters accepted by the exporter are:

```shell
The exporter takes the following arguments
   exporter <filename> mmodifiers

   [e.g.] exporter theboxsoftware.reflection.dll -to c:\temp\web -filters "public|protected"

   <filename>  The path to the configuration file, library, project or solution.
   modifiers:
     -h        show help information
     -v        show verbose export details
     -to       the directory to export to
     -format   the ldec file format to export content. Defaults to web-msdn.ldec
     -filters  the visibilty filters (public|protected etc) defaults to public
               "all" can be provided as a shortcut to:-
                  "public|protected|internal|interalprotected|private"


`-to`, `-format` and `-filters` are only used when the file provided is not a
configuration xml file.
```


### Commands

<table>
    <thead>
        <tr>
            <th>Action</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>&lt;filename></td>
            <td>The file path to the configuration file that details the export.</td>
        </tr>    
        <tr>
            <td>-h</td>
            <td>Displays the help information above.</td>
        </tr>
        <tr>
            <td>-v</td>
            <td>Outputs the steps for the export instead of just the fact it has started an export. With or without this modifier it will always display the warnings and errors.</td>
        </tr>
        <tr>
            <td>-to</td>
            <td>Specified a location to export the documentation to. Is only valid when <em>filename</em> is not a configuration file.</td>
        </tr>
        <tr>
            <td>-format</td>
            <td>The name of the ldec exporter to use. E.g. web-msdn.ldec, this file should be in the ApplicationData folder. Is only valid when <em>filename</em> is not a configuration file.</td>
        </tr>
        <tr>
            <td>-filters</td>
            <td><p>Specifies the list of visibilty modifiers which will be exporter. Default is public. Is only valid when <em>filename</em> is not a configuration file.</p>
            <p>The filters can be one or all of the following:</p>
            <ul>
                <li>public</li>
                <li>internal</li>
                <li>internalprotected</li>
                <li>protected</li>
                <li>private</li>
            </ul>
            <p>When specifying more than one ensure they are seperated by the | character and enclosed in quotes. <em>"public|protected"</em></p>
            <p><code>all</code> can be provided as a shortcut to all available filters listed above.</p>
            </td>
        </tr>
    </tbody>
</table>

## Export configuration files

An export configuration file contains the following information.

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

The `document` element is a path to your solution, project, .NET dll or ldproj file. Only one document 
can be specified.

`filters` determine the visibility of the members that will be exported. If these are not specified it 
will default to Public and Protected.

Finally, `outputs` detail the location of published files and the LDEC file used to perform the export. 
One or more outputs can be defined here. Each one will be exported in turn.

Please _note_ that, just like the desktop application, a new timestamped folder will be created to hold
the new exported content in the directory selected.