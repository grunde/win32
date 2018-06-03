---
title: Packages Overview
description: This topic describes the basics of using Packaging APIs to interact with packages.
ms.assetid: f42a8581-dcaa-43a6-997f-984303a32ff3
keywords:
- Packaging APIs,packages
- packaging,packages
- packages,about
- packages,objects
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# Packages Overview

This topic describes the basics of using Packaging APIs to interact with packages.

This topic contains the following sections.

-   [Introduction](#introduction)
-   [Prerequisites](#prerequisites)
-   [Package Objects](#package-objects)
-   [Related topics](#related-topics)

## Introduction

A package is an aggregate of data components, like the filing cabinet is an aggregate of an individual or business's paperwork.

Unlike real–world filing systems, packages must conform to a predictable, conceptual organizational system (called the logical model), and predicatable physical characteristics (called the physical model). These standardized conformance requirements are described in the *ECMA-376 OpenXML, 1st Edition, Part 2: Open Packaging Conventions (OPC)*.

To interact with a specific package, the caller uses the Packaging APIs to create a package object that represents the package (a conceptual filing cabinet). All interactions which a package are performed using this package object.

## Prerequisites

For a table of prerequisites, see [Packaging](packaging.md).

## Package Objects

Windows 7 provides the package object implementation of the [**IOpcPackage**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpackage) interface.

A package object is instantiated to represent a package when the [**IOpcFactory::CreatePackage**](/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcfactory-createpackage) or [**IOpcFactory::ReadPackageFromStream**](/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcfactory-readpackagefromstream) method is called.

A pointer to the [**IOpcPackage**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpackage) interface of a package object provides access to the [**IOpcRelationshipSet**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationshipset) and [**IOpcPartSet**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpartset) interface pointers of a relationship set object and a part set object, respectively.

The following diagram shows a package object and the relationship set and part set objects that can be retrieved from it.

![illustration showing a package object and the relationship set and part set objects that can be retrieved from it](https://www.bing.com/search?q=illustration showing a package object and the relationship set and part set objects that can be retrieved from it)

A relationship set object that is retrieved by calling [**IOpcPackage::GetRelationshipSet**](/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcpackage-getrelationshipset) represents the Relationships part that stores package relationships. This object is an unordered set of [**IOpcRelationship**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcrelationship) interface pointers to relationship objects. Each relationship object represents one package relationship. For more information about relationship objects and relationship set objects, see the [Relationships Overview](relationships-overview.md) topic.

The target of a package relationship is often an important part, and it is described by the package format designer or in the *OPC*. For example, a package relationship can provide access to the Core Properties part that stores package metadata, or to a part containing format-specific data, where the part and data are described by the package designer. The Main Document part of the word processing OpenXML format is one such format-specific part, described in Part 1: Fundamentals in [ECMA-376 OpenXML](http://go.microsoft.com/fwlink/p/?linkid=123375) (http://go.microsoft.com/fwlink/p/?linkid=123375).

A part set object, which can only be retrieved by calling the [**IOpcPackage::GetPartSet**](/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcpackage-getpartset) method, represents all parts contained in the package that are not Relationships parts. The set is an unordered set of [**IOpcPart**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcpart) interface pointers to part objects. Each part object represents one part (which is not a Relationships part) in the package. For more information about part objects, see the [Parts Overview](parts-overview.md).

For information about how to create a package object, see the [Loading a Package to be Read](loading-a-package.md) how-to topic and the [**IOpcFactory::CreatePackage**](/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcfactory-createpackage) method.

## Related topics

<dl> <dt>

[Packages Fundamentals](packages.md)
</dt> <dt>

**Overviews**
</dt> <dt>

[Open Packaging Conventions Fundamentals](open-packaging-conventions-overview.md)
</dt> <dt>

[Packages How-To Topics](packages-how-to-topics.md)
</dt> <dt>

[Getting Started with the Packaging API](packaging-api-overview.md)
</dt> <dt>

**Reference**
</dt> <dt>

[Packaging API Reference](packaging-programming-reference.md)
</dt> <dt>

[Packaging API Samples](packaging-programming-samples.md)
</dt> <dt>

**External**
</dt> <dt>

[ECMA-376 OpenXML](http://go.microsoft.com/fwlink/p/?linkid=123375)
</dt> </dl>

 

 



