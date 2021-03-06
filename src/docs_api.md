---
layout: docs
title: API Overview
permalink: "/docs/api/"
---

# API Overview

This page gives a brief overview of the Live Documenter API and how to use it.

The API (application programming interface) provided by the Live Documenter enables you to have more flexibility over documentation that is generated. In essence it allows you to load a library or project and produce documentation on request a single page at a time.

This would allow you to, for example, create a web site which watches a .NET library and associated XML comments. Displaying the latest documentation all the time. The API is used to provide this functionality for the Live Documenter API documentation.

```cs
Documentation docs = new Documentation("myfile.dll");
docs.Load();

// get a page of documentation
XmlDocument xmlDocument = new XmlDocument();
xmlDocument.LoadXml(
	docs.Find("T:System.String"); // searching can be performed using cref paths
	);
```