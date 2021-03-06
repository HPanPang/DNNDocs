﻿---
uid: breadcrumb
locale: en
title: Breadcrumb Theme object
dnnversion: 09.02.00
previous-topic: theme-objects
next-topic: ddrmenu-overview
related-topics: theme-objects,themes,create-theme
links: 
---

# Breadcrumb Theme Object Introduction

The Breadcrumb Theme Object displays the path to the currently selected page in the menu structure like this:
RootPage > SubPage > SubSubPage
The starting level, separator and styliong are configurable.

**Current Version:** 1.0.0

> [!NOTE]
> When you need even more control, you can also create breadcrumbs using a DDR menu template.

## Include in Theme

### ASCX
```html
<%@ Register TagPrefix="dnn" TagName="Breadcrumb" Src="~/Admin/Skins/breadcrumb.ascx" %>
<dnn:Breadcrumb runat="server" id="dnnBreadcrumb" />
```

### HTML Token
\[BREADCRUMB]

### HTML Object Token
``` html
<object id="dnnBREADCRUMB" codetype="dotnetnuke/server" codebase="BREADCRUMB">
```


| Attribute | Description                              | Default    | Values                                                                                                                                                                                       | Version    |
|-----------|------------------------------------------|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| Separator | The separator between breadcrumb links\. | >          | html / text / image                                                                                                                                                                          | 01\.00\.00 |
| CssClass  | CSS Class of the SkinObject              | SkinObject | A valid CSS Class                                                                                                                                                                            | 01\.00\.00 |
| RootLevel | The root level of the breadcrumb links\. | 1          | Valid values include:<br> \-1  \-  show word “Root” and then all breadcrumb tabs<br> 0  \-  show all breadcrumb tabs<br> n \(Integer > 0\)  \-  skip n breadcrumb tabs before displaying<br> | 01\.00\.00 |
| UseTitle  | Use the PageTitle instead of PageName    | False      | True / False                                                                                                                                                                                 | 01\.00\.00 |



## Examples:

~~~html
<dnn:Breadcrumb runat="server" id="dnnBreadcrumb" Separator="++" CssClass="breadcrumb" RootLevel="2" UseTitle="true" />
~~~

