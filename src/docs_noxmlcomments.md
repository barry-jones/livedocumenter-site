---
layout: docs
permalink: "/docs/issues/no-xml-comments/"
title: No XML Comments Displayed
---

# No XML comments message displayed

This page describes what to do in the event a no xml comments message is displayed in the application.

You may be presented with the following message in the desktop application, or not see the comments in the exported content.

<div class="info mb-3">
No XML comments file found for declaring assembly 'DocumentationTest.dll'.
</div>

To resolve this issue, first verify that the XML comments are being generated. This can be checked via the properties dialogue in visual studio.

<div class="row justify-content-center p-3">
    <img class="img-fluid image_border" src="/assets/images/documentation/xmlcomments_output.png">
</div>

This will need to be set for all build configurations you are using.
