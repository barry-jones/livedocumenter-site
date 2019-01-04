---
layout: docs
permalink: "/docs/export/exporters/"
title: Create your own LDEC files
---

<h1>Exporters</h1>

<p>The following exporters are provided to generate documentation in various formats.</p>

<p>The Live Documenter application provides the following internal processors for generating documentation. Any details regarding the installation and use of the exporters are detailed in the pages below.</p>

<ul>
    <li><a href="#web">Web exporter</a></li>
    <li><a href="#xml">XML exporter</a></li>
    <li><a href="#htmlhelp1">HTML Help 1 exporter</a></li>
    <li><a href="#htmlhelp2">HTML Help 2 exporter</a></li>
    <li><a href="#helpviewer1">Help Viewer 1 exporter</a></li>
</ul>

<h2 id="web">Web Exporter</h2>
<p>The web exporter is an internal processor for converting files from one source to another using 
    the specified LDEC XSLT file. Web is a bit of a misnomer as the processor does not really care
     what you convert the originating XML to.</p>

<p>This processor then is the most flexible, it can be used to convert to file formats such as static
     HTM files, dynamic PHP, .NET or even Markdown. Conceviably you could also generate XSL:FO files
     for later processing in to PDF files.</p>

<h2 id="xml">XML Exporter</h2>
<p>This a basic processor, the one out of the box simply outputs the basic XML that the Live 
Documenter uses as an intermediate rich XML document for later processing to other formats.</p>

<p>Specifying extra information in an XML LDEC file such as an XSLT will not do anything. The 
processor does not perform any extra transform processing steps. If you want to convert from 
our base XML format to another, then the [web exporter](exporter-web) is what you will need.</p>

<p>This exporter is provided to enable you to quickly see an entire XML output for a project for
developing your own custom LDEC files, or for processing a standardised output in other applications.</p>

<h2 id="htmlhelp1">HTML Help 1 Exporter</h2>
<p>The HTML Help 1 exporter is an internal processor in the Live Documenter, for compiling content transformed by an LDEC XSLT file in to a HTML 1 file. The HTML Help file is a proprietory format developed by Microsoft.</p>

<h3>Where to get it</h3>
<p>THe Microsoft HTML Help 1.x compiler can be downloaded from <a href="http://go.microsoft.com/fwlink/?LinkId=14188">http://go.microsoft.com/fwlink/?LinkId=14188</a>. Please note that it may be necessary to run the HTML Help Workshop once before it is correctly registered.</p>

<h2 id="htmlhelp2">HTML Help 2 Exporter</h2>
<p>The HTML Help 2 exporter is an internal processor for compiling transformed files form the LDEC specified XSLT file in to a compiled HTML Help 2 file.</p>

<h3>Where to get it</h3>
<p>Please note that the only viewer for this format is in Visual Studio 2002-2008 and so producing in this format should only be necessary
    if you are intending to integrate with those version of Visual Studio.</p>

<h3>Visual Studio 2008</h3>
<p>If you have this version installed you can download the compiler from <a href="http://www.microsoft.com/en-us/download/details.aspx?id=21827">http://www.microsoft.com/en-us/download/details.aspx?id=21827</a></p>

<h3>Visual Studio 2005</h3>
<p>You will need to install the Visual Studio SDK. The download is no longer available on the Microsoft site.</p>

<h3>Visual Studio 2003</h3>
<p>If you have Visual Studio 2003 installed, install the Microsoft Help 2.x Compiler by installing the 
    Microsoft Visual Studio .NET Help Integration Kit, a Microsoft provided free Add-In to Visual Studio 
    2003 that provides the functionality for compiling Microsoft Help 2.x projects.</p>

<p>You can freely download the Visual Studio .NET Help Integration kit from this MSDN download page 
    <a href="http://www.microsoft.com/en-us/download/details.aspx?id=13644">http://www.microsoft.com/en-us/download/details.aspx?id=13644</a></p>

<h2 id="helpviewer1">Help Viewer 1 Exporter</h2>
<p>The Help Viewer 1 exporter is an internal processor for compiling transformed files from the LDEC XSLT in to a Help Viewer 1 file.</p>
