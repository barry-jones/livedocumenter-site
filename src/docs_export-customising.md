---
layout: docs
title: Customising the Export
permalink: "/docs/export/customising/"
---
# Customising the output

This page describes how to customise the exported content by modifying an existing export configuration
file.

All of the LDEC files shipped with the Live Documenter can be customised simply by unzipping the contents 
of the LDEC file to a directory and modifying the CSS. When zipped up again and placed in the ApplicationData 
folder these will be available in the export dialogue.

More complicated customisation of the output will require a broader knowledge of the file and it's 
contents which can be found <a href="/export/live-documenter-export-configuration-files">here</a>.

After unzipping the file you will see the following structure:

```
styles/
styles/default.css
styles/images/...
export.config
screenshot.png
webexport.xslt
```

If you make all your changes in the <code>styles/default.css</code> file, you can control the look and feel 
of the output and no futher modifications will be required.