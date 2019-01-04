---
layout: docs
permalink: "/docs/export/create-own-ldec-file/"
title: Create your own LDEC files
---

# Creating your own LDEC files

Live Documenter Export Configuration files are self contained files which describe how the underlying documentation
XML will be exported. 

Creating your own LDEC files requires knowledge of XSLT, however if you want to simply re-use and restyle one of the existing LDEC files you should only need to modify the stylsheets. Either way this document will provide you with some insight in to modifying and creating your own export configurations.

## Basic LDEC file
At it's most basic a LDEC file is a zipped set of content with an <code>.ldec</code> extension, containing an <code>export.config</code> and <code>xslt</code> file.

The contents of the <code>export.config</code> file should be as follows.

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<export xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
    <name>Web Export: MSDN Lo Band Style</name>
    <description>A wesbite export of the documentation in the MSDN Lo Band web style.</description>
    <author>The Box Software</author>
    <version>1.0</version>
    <exporter>web</exporter>
    <xslt>webexport.xslt</xslt>
    <screenshot>screenshot.png</screenshot>
    <properties>
        <property name="extension" value="htm" />
    </properties>
    <outputfiles>
        <file internal="styles/default.css" output="\styles\default.css" />
        <file internal="styles/images/" output="\styles\images\" />
    </outputfiles>
</export>
```

Above is the <code>export.config</code> file for the Web Export - MSDN Lo Band. Only the <code>name</code> and <code>xslt</code> elements are required. The following config file contents will create a valid working LDEC file that will be read by the Live Documenter.

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<export xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
    <name>A name</name>
    <xslt>export.xslt</xslt>
</export>
```

## Process
### Generation of an intermediate XML
The first part of the export process is that Live Documenter will generate an intermediate XML file, which contains all of the information from the library and the XML comments. This XML content can be viewed by exporting documentation with the XML ldec file, which simply outputs the internmediate XML content.

Note there is also <code>toc.xml</code> file created which contains information about all of the types and members being exported.

### Transformation
The next step is to run the transform on each XML file. The intermediate XML exists as files at this point. The resulting content is saved as a file to a temp output directory.

### Compiling
Some exporters at this stage will compile to a final file, such as the HTML Help 1 exporter. However for the web and XML exporters this step is not required and is not run.

### Publishing
Finally the files from the <code>outputFiles</code> section are saved to the output directory specified by the user along with all of the transformed content files.

<code>file</code> entries can either be a single file or directory. In the event a directory is specified then the full contents of that directory are output. The internal reference is the location in the zipped ldec file, the external is the location from the users specified export directory as a base.

### Comments
The most noteworthy sections above are the transform and publishing sections. These can be controlled via the LDEC file through the <code>xslt</code> and <code>outputfiles</code> elements.

## Modifying the output
XSLT is a transformation language that converts one XML source in to something else. To that end, what you can do here is limited only by your imagination and skill. Exporting to xsl:fo for later transformation to PDF or a text format such as Markdown are just a couple of ideas.