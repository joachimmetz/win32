---
title: Returning Error Information
description: Describes how to return error information.
ms.assetid: 0da07034-4585-4fad-8d20-b65bfe9c560e
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# Returning Error Information

## To return error information

1.  Implement the [**ISupportErrorInfo**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-isupporterrorinfo)interface.

2.  To create an instance of the generic error object, call the [CreateErrorInfo](https://msdn.microsoft.com/windows/desktop/6A9DD862-754A-48E3-8BE5-D1FBD1D38F2B) function.

3.  To set its contents, use the [**ICreateErrorInfo**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreateerrorinfo)methods.

4.  To associate the error object with the current logical thread, call the [SetErrorInfo](https://msdn.microsoft.com/windows/desktop/8EAACFAC-FC37-4EAA-870B-10B99D598D66) function.

The following figure illustrates this procedure.

![](images/oa05-01.png)

The error handling interfaces create and manage an error object, which provides information about the error. The error object is not the same as the object that encountered the error. It is a separate object associated with the current thread of execution.

## Related topics

<dl> <dt>

[Error Handling Interfaces](error-handling-interfaces.md)
</dt> </dl>

 

 



