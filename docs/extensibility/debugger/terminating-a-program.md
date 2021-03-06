---
title: Beenden eines Programms | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords:
- programs, termination events
- debugging [Debugging SDK], terminating a program
ms.assetid: eedda0a3-5e05-44fe-841d-a2f4866ac72d
caps.latest.revision: "7"
author: gregvanl
ms.author: gregvanl
manager: ghogen
ms.workload: vssdk
ms.openlocfilehash: 4d1cb3176585dce135b19f125af55db799fed4b9
ms.sourcegitcommit: 32f1a690fc445f9586d53698fc82c7debd784eeb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/22/2017
---
# <a name="terminating-a-program"></a>Beenden eines Programms
Im folgenden ist eine Beschreibung des Beendens der ein einzelnes Programm mit einem Thread.  
  
## <a name="termination-process"></a>Beendigungsprozess  
  
1.  Sendet die DE ein [IDebugThreadDestroyEvent2](../../extensibility/debugger/reference/idebugthreaddestroyevent2.md) durch einen gültigen [IDebugThread2](../../extensibility/debugger/reference/idebugthread2.md).  
  
2.  Sendet die DE ein [IDebugProgramDestroyEvent2](../../extensibility/debugger/reference/idebugprogramdestroyevent2.md) durch einen gültigen [IDebugProgram2](../../extensibility/debugger/reference/idebugprogram2.md).  
  
 Die IDE wechselt in den Entwurfsmodus zu wechseln. Die Debugging-Modul oder eine Umgebung zur Laufzeit ruft [IDebugPortNotify2::RemoveProgramNode](../../extensibility/debugger/reference/idebugportnotify2-removeprogramnode.md) Sie das Programm den Port aufheben.  
  
## <a name="see-also"></a>Siehe auch  
 [Aufrufen von Debuggerereignissen](../../extensibility/debugger/calling-debugger-events.md)