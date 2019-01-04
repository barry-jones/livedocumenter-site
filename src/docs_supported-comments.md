---
layout: docs
title: Supported XML Code Comments
permalink: "/docs/supported-xml-comments/"
---

## Supported XML Code Comments

This page contains a full list of all of the suppored XML code comments with examples of usage.

The Live Documenter supports all of the recommended tags for XML code comments.

* <a href="#c">&lt;c></a>
* <a href="#code">&lt;code></a>
* <a href="#example">&lt;example></a>
* <a href="#exception">&lt;exception></a>
* <a href="#list">&lt;list></a>
* <a href="#para">&lt;para></a>
* <a href="#param">&lt;param></a>
* <a href="#paramref">&lt;paramref></a>
* <a href="#remarks">&lt;remarks></a>
* <a href="#returns">&lt;returns></a>
* <a href="#see">&lt;see></a>
* <a href="#seealso">&lt;seealso></a>
* <a href="#summary">&lt;summary></a>
* <a href="#typeparam">&lt;typeparam></a>
* <a href="#typeparamref">&lt;typeparamref></a>
* <a href="#value">&lt;value></a>

Further the following elements are supported by Live Documenter to enable more control over your documentation.

* <a href="#b">&lt;b></a>
* <a href="#i">&lt;i></a>

### &lt;c>
An inline element that represents text that should be considered as code.

```xml
<c>text</c>
```

__Parameters__

text
: The text to be treated as inline code.

__Example__

```xml
/// <remarks>
///   <para>This is an <c>inline text</c> c element in a remark.</para>
/// </remarks>
```

### &lt;code>
Element that describes a multi-line code block.

```xml
<code>content</code>
```

__Parameters__

content
: The text to be treated as code.

__Example__

```xml
/// <remarks>
///   <code>
/// // an example of code block
/// public void SomeCode { get; set; }
///   </code>
/// </remarks>
public void TestMethod() { }
```




### &lt;example>
Element that describes a code example.

```xml
<example>content</example>
```

__Parameters__

example
: The description and code sample.

__Example__
```xml
/// <example>
///   <para>A description of the following code block.</para>
///   <code>
/// // an example of code block
/// public void SomeCode { get; set; }
///   </code>
/// </example>
public void TestMethod() { }
```




### &lt;exception>
Element that describes a an exception that can be thrown.

```xml
<exception cref="member">description</exception>
```

__Parameters__

cref="member"
: A reference to an exception that is available from the current compilation environment.
description
: The description of the exception

__Example__
```xml
/// <exception cref="MyNamespace.CustomException">A description of the exception.</exception>
public void TestMethod() { }
```




### &lt;list>
Element that describes a list of items or tabular data.

```xml
<list type="bullet | number | table">
  <listheader>
    <term>term</term>
    <description>description</description>
  </listheader>
  <item>
    <term></term>
    <description></description>
  </item>
</list>
```

__Parameters__

term
: A term to define which will be described in the description.
description
: A description of the term

__Example__
```xml
/// <remarks>
///   <list type="number">
///     <item>
///       <term>Item 1.</term>
///     </item>
///     <item>
///       <term>Item 2.</term>
///     </item>
///   </list>
/// </remarks>
public void TestMethod() { }
```

Live Documenter supports simplified versions of the list element when you are defining simple lists. Further when no type attribute is specified Live Documenter will default to the `<code>bullet</code>` type.

```xml
/// <remarks>
///   <list>
///     <item>Bulleted item 1</item>
///     <item>Bulleted itme 2</item>
///   </list>
/// </remarks>
public void TestMethod() { }
```




### &lt;para>
Element that describes a paragraph.

```xml
<para>content</para>
```

__Parameters__
<dl>
    <dt>content</dt>
    <dd>The content of the paragraph.</dd>
</dl>

__Example__
```xml
/// <remarks>
///   <para>A paragraph of text.</para>
/// </remarks>
public void TestMethod() { }
```




### &lt;param>
Element that allows the description of a parameter.

```xml
<param name="name">description</param>
```

__Parameters__
<dl>
    <dt>name="name"</dt>
    <dd>The name of the parameter to describe.</dd>
    <dt>description</dt>
    <dd>The description of the parameter.</dd>
</dl>

__Example__
```xml
/// <param name="aString">A string.</param>
public void TestMethod(string aString) { }
```




### &lt;paramref>
An inline element that refers to a parameter.

```xml
<paramref name="name" />
```

__Parameters__
<dl>
    <dt>name="name"</dt>
    <dd>The name of the parameter to describe.</dd>
</dl>

__Example__
```xml
/// <remarks>
///   The <paramref name="aString" /> parameter is required.
/// </remarks>
/// <param name="aString">A string.</param>
public void TestMethod(string aString) { }
```




### &lt;permission>
An element that refers to a parameter.

```xml
<permission cref="member">desription</permission>
```

__Parameters__
<dl>
    <dt>cref="member"</dt>
    <dd>The name of the parameter to describe.</dd>
    <dt>description</dt>
    <dd>A description of the permission.</dd>
</dl>

__Example__
```xml
/// <permission cref="System.Security.PermissionSet">Everyone can access this method.</param>
public void TestMethod() { }
```




### &lt;remarks>
A block level element that provides supplementary remarks.

```xml
<remarks>description</remarks>
```

__Parameters__
<dl>
    <dt>description</dt>
    <dd>A description of the member.</dd>
</dl>

__Example__
```xml
/// <remarks>Everyone can access this method.</remarks>
public void TestMethod() { }
```




### &lt;returns>
A block level element that provides information about the return value.

```xml
<returns>description</returns>
```

__Parameters__
<dl>
    <dt>returns</dt>
    <dd>A description of the member.</dd>
</dl>

__Example__
```xml
/// <returns>Returns a string.</returns>
public string TestMethod() { }
```




### &lt;see>
An inline element that refers to another member in the compilation environment.

```xml
<see cref="member" />
```

__Parameters__
<dl>
    <dt>cref="member"</dt>
    <dd>The member from the current compilation environment.</dd>
</dl>

__Example__
```xml
/// <remarks>
///   <para>This is a method that uses the <see cref="System.String" /> class.</para>
/// </remarks>
public void TestMethod() { }
```




### &lt;seealso>
An element that refers to another member in the compilation environment which will be displayed in a seealso section.

```xml
<seealso cref="member" />
```

__Parameters__
<dl>
    <dt>cref="member"</dt>
    <dd>The member from the current compilation environment.</dd>
</dl>

__Example__
```xml
/// <seealso cref="System.String" />
public void TestMethod() { }
```




### &lt;summary>
A block level element that provides summary of the member.

```xml
<summary>description</summary>
```

__Parameters__
<dl>
    <dt>description</dt>
    <dd>A description of the member.</dd>
</dl>

__Example__
```xml
/// <summary>Everyone can access this method.</summary>
public void TestMethod() { }
```




### &lt;typeparam>
Element that allows the description of a parameter.

```xml
<typeparam name="name">description</typeparam>
```

__Parameters__
<dl>
    <dt>name="name"</dt>
    <dd>The name of the parameter to describe.</dd>
    <dt>description</dt>
    <dd>The description of the parameter.</dd>
</dl>

__Example__
```xml
/// <typeparam name="T">The element type to return.</typeparam>
public T TestMethod<T>() { }
```




### &lt;typeparamref>
An inline element that refers to a type parameter.

```xml
<typeparamref name="name" />
```

__Parameters__
<dl>
    <dt>name="name"</dt>
    <dd>The name of the type parameter to describe.</dd>
</dl>

__Example__
```xml
/// <remarks>
///   The <typeparamref name="element" /> parameter can be anything.
/// </remarks>
public void TestMethod<T>(T element) { }
```




### &lt;value>
A block level element that provides information about the value a property represents.

```xml
<value>description</value>
```

__Parameters__
<dl>
    <dt>description</dt>
    <dd>A description of the value the property represents.</dd>
</dl>

__Example__
```xml
/// <value>Returns a string.</value>
public string TestProperty { get; set; }
```




### &lt;b>
An inline element that represents text that should be considered strong or bold.

```xml
<b>text</b>
```

__Parameters__
<dl>
    <dt>text</dt>
    <dd>The text to be treated as bold/strong.</dd>
</dl>

__Example__
```xml
/// <summary>This <b>text</b> should be treated as important.</summary>
/// <remarks>
///   <para>This is an <b>inline text</b> b element in a remark.</para>
/// </remarks>
public void TestMethod() { }
```




### &lt;i>
An inline element that represents text that should be considered important.

```xml
<i>text</i>
```

__Parameters__
<dl>
    <dt>text</dt>
    <dd>The text to be treated as important.</dd>
</dl>

__Example__
```xml
/// <remarks>
///   <para>This is an <i>inline text</i> i element in a remark.</para>
/// </remarks>
public void TestMethod() { }
```

