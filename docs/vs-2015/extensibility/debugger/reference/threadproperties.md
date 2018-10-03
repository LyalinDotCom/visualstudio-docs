---
title: "THREADPROPERTIES | Microsoft Docs"
ms.custom: ""
ms.date: "2018-06-30"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "THREADPROPERTIES"
helpviewer_keywords: 
  - "THREADPROPERTIES structure"
ms.assetid: 7d397207-db03-4ec0-9f79-3794056ed89f
caps.latest.revision: 9
ms.author: "gregvanl"
manager: "ghogen"
---
# THREADPROPERTIES
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

The latest version of this topic can be found at [THREADPROPERTIES](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/threadproperties).  
  
Describes the properties of a thread.  
  
## Syntax  
  
```cpp#  
typedef struct _tagTHREADPROPERTIES {   
   THREADPROPERTY_FIELDS dwFields;  
   DWORD                 dwThreadId;  
   DWORD                 dwSuspendCount;  
   DWORD                 dwThreadState;  
   BSTR                  bstrPriority;  
   BSTR                  bstrName;  
   BSTR                  bstrLocation;  
} THREADPROPERTIES;  
```  
  
```csharp  
public struct THREADPROPERTIES {   
   public uint   dwFields;  
   public uint   dwThreadId;  
   public uint   dwSuspendCount;  
   public uint   dwThreadState;  
   public string bstrPriority;  
   public string bstrName;  
   public string bstrLocation;  
};  
```  
  
## Members  
 dwFields  
 A combination of flags from the [THREADPROPERTY_FIELDS](../../../extensibility/debugger/reference/threadproperty-fields.md) enumeration, describing which fields in this structure are valid.  
  
 dwThreadId  
 The thread ID.  
  
 dwSuspendCount  
 The thread suspend count.  
  
 dwThreadState  
 A value from the [THREADSTATE](../../../extensibility/debugger/reference/threadstate.md) enumeration indicating the state of the operating thread.  
  
 bstrPriority  
 A string specifying the thread priority; for example, "Above Normal", "Normal", or "Time Critical".  
  
 bstName  
 The thread name.  
  
 bstrLocation  
 The thread location (usually the topmost stack frame), typically expressed as the name of the method where execution is currently halted.  
  
## Remarks  
 This structure is filled in by a call to the [GetThreadProperties](../../../extensibility/debugger/reference/idebugthread2-getthreadproperties.md) method. The information so returned is typically used in populating the **Threads** window.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Structures and Unions](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [GetThreadProperties](../../../extensibility/debugger/reference/idebugthread2-getthreadproperties.md)   
 [THREADPROPERTY_FIELDS](../../../extensibility/debugger/reference/threadproperty-fields.md)   
 [THREADSTATE](../../../extensibility/debugger/reference/threadstate.md)
