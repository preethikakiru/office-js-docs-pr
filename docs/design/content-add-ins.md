---
title: Content Office Add-ins
description: Content add-ins are surfaces that can be embedded directly into Excel or PowerPoint documents that give users access to interface controls that run code to modify documents or display data from a data source.
ms.date: 05/12/2021
ms.localizationpriority: medium
---

# Content Office Add-ins

Content add-ins are surfaces that can be embedded directly into Excel or PowerPoint documents. Content add-ins give users access to interface controls that run code to modify documents or display data from a data source. Use content add-ins when you want to embed functionality directly into the document.  

*Figure 1. Typical layout for content add-ins*

![Typical layout for content add-ins in an Office application.](../images/overview-with-app-content.png)

## Best practices

- Include some navigational or commanding element such as the CommandBar or Pivot at the top of your add-in.
- Include a branding element such as the BrandBar at the bottom of your add-in (applies to Excel and PowerPoint add-ins only).

## Variants

Content add-in sizes for Excel and PowerPoint in Office desktop and in a web browser are user specified.

## Personality menu

Personality menus can obstruct navigational and commanding elements located near the top right of the add-in. The following are the current dimensions of the personality menu on Windows and Mac.

For Windows, the personality menu measures 12x32 pixels, as shown.

*Figure 2. Personality menu on Windows*

![12x32-pixel personality menu on Windows desktop.](../images/personality-menu-win.png)

For Mac, the personality menu measures 26x26 pixels, but floats 8 pixels in from the right and 6 pixels from the top, which increases the occupied space to 34x32 pixels, as shown.

*Figure 3. Personality menu on Mac*

![34x32-pixel personality menu on Mac desktop.](../images/personality-menu-mac.png)

## Implementation

For a sample that implements a content add-in, see [Excel Content Add-in Humongous Insurance](https://github.com/OfficeDev/Excel-Content-Add-in-Humongous-Insurance) in GitHub.

## Support considerations

- Check to see if your Office Add-in will work on a [specific Office application or platform](/javascript/api/requirement-sets).
- Some content add-ins may require the user to "trust" the add-in to read and write to Excel or PowerPoint. You can declare what [level of permissions](../develop/requesting-permissions-for-api-use-in-content-and-task-pane-add-ins.md) you want your user to have in the add-in's manifest.  
- Content add-ins are supported in Excel and PowerPoint in Office 2013 version and later. If you open an add-in in a version of Office that doesn't support Office web add-ins, the add-in will be displayed as an image.

## See also

- [Office client application and platform availability for Office Add-ins](/javascript/api/requirement-sets)
- [Fabric Core in Office Add-ins](fabric-core.md)
- [UX design patterns for Office Add-ins](../design/ux-design-pattern-templates.md)
- [Requesting permissions for API use in add-ins](../develop/requesting-permissions-for-api-use-in-content-and-task-pane-add-ins.md)
