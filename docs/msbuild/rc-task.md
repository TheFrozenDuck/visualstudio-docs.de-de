---
title: RC-Aufgabe | Microsoft-Dokumentation
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-sdk
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- VC.Project.VCResourceCompilerTool.UndefineProcessorDefinitions
- vc.task.rc
- VC.Project.VCResourceCompilerTool.SuppressStartupBanner
- VC.Project.VCResourceCompilerTool.NullTerminateStrings
dev_langs:
- VB
- CSharp
- C++
- jsharp
- C++
helpviewer_keywords:
- RC task (MSBuild (Visual C++))
- MSBuild (Visual C++), RC task
ms.assetid: 2fd26c75-a056-4dda-9f7e-2f90d3748d88
caps.latest.revision: "10"
author: kempb
ms.author: kempb
manager: ghogen
ms.workload: multiple
ms.openlocfilehash: 5398f3eb1aa140ed53d6734734528d5c89a104c8
ms.sourcegitcommit: 32f1a690fc445f9586d53698fc82c7debd784eeb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/22/2017
---
# <a name="rc-task"></a>RC-Aufgabe
Umschließt das Microsoft Windows-Ressourcencompilertool („rc.exe“). Die **RC**-Aufgabe kompiliert Ressourcen in eine RES-Datei, z.B. Cursors, Symbole, Bitmaps, Dialogfelder und Schriftarten. Weitere Informationen finden Sie unter „Ressourcencompiler“ auf der [MSDN](http://go.microsoft.com/fwlink/?LinkId=737)-Website.  
  
## <a name="parameters"></a>Parameter  
 In der folgenden Tabelle werden die Parameter der RC-Aufgabe beschrieben. Die meisten Aufgabenparameter und einige Parametersätze entsprechen einer Befehlszeilenoption.  
  
|Parameter|description|  
|---------------|-----------------|  
|**AdditionalIncludeDirectories**|Optionaler **String[]**-Parameter.<br /><br /> Fügt ein Verzeichnis zur Liste der Verzeichnisse hinzu, die nach Includedateien durchsucht werden.<br /><br /> Weitere Informationen finden Sie auf der MSDN-Website unter der **/I**-Option im Artikel [Using RC (The RC Command Line) (Verwenden von RC (RC-Befehlszeile))](http://go.microsoft.com/fwlink/?LinkId=155730).|  
|**AdditionalOptions**|Optionaler **String**-Parameter.<br /><br /> Eine Liste der Befehlszeilenoptionen, z.B. **„***/option1 /option2 /option#*“. Verwenden Sie diesen Parameter, um Befehlszeilenoptionen anzugeben, die nicht durch einen anderen **RC**-Aufgabenparameter dargestellt werden.<br /><br /> Weitere Informationen finden Sie auf der MSDN-Website unter den Optionen im Artikel [Using RC (The RC Command Line) (Verwenden von RC (RC-Befehlszeile))](http://go.microsoft.com/fwlink/?LinkId=155730).|  
|**Kultur**|Optionaler **String**-Parameter.<br /><br /> Gibt eine lokale ID an, die die in den Ressourcen verwendete Kultur darstellt.<br /><br /> Weitere Informationen finden Sie auf der MSDN-Website unter der **/l**-Option im Artikel [Using RC (The RC Command Line) (Verwenden von RC (RC-Befehlszeile))](http://go.microsoft.com/fwlink/?LinkId=155730).|  
|**IgnoreStandardIncludePath**|Optionaler **Boolean**-Parameter.<br /><br /> Wenn dieser `true` ist, wird verhindert, dass der Ressourcencompiler die INCLUDE-Umgebungsvariable überprüft, wenn nach Header- oder Ressourcendateien gesucht wird.<br /><br /> Weitere Informationen finden Sie auf der MSDN-Website unter der **/x**-Option im Artikel [Using RC (The RC Command Line) (Verwenden von RC (RC-Befehlszeile))](http://go.microsoft.com/fwlink/?LinkId=155730).|  
|**NullTerminateStrings**|Optionaler **Boolean**-Parameter.<br /><br /> Wenn dieser `true` ist, lässt er alle Zeichenfolgen in der Zeichenfolgentabelle auf NULL enden.<br /><br /> Weitere Informationen finden Sie auf der MSDN-Website unter der **/n**-Option im Artikel [Using RC (The RC Command Line) (Verwenden von RC (RC-Befehlszeile))](http://go.microsoft.com/fwlink/?LinkId=155730).|  
|**PreprocessorDefinitions**|Optionaler **String[]**-Parameter.<br /><br /> Definieren Sie ein oder mehrere Präprozessorsymbole für den Ressourcencompiler. Geben Sie eine Liste von Makrosymbolen an.<br /><br /> Weitere Informationen finden Sie auf der MSDN-Website unter der **/d**-Option im Artikel [Using RC (The RC Command Line) (Verwenden von RC (RC-Befehlszeile))](http://go.microsoft.com/fwlink/?LinkId=155730). Weitere Informationen finden Sie ebenfalls unter **UndefinePreprocessorDefinitions** in dieser Tabelle.|  
|**ResourceOutputFileName**|Optionaler **String**-Parameter.<br /><br /> Gibt den Namen der Ressourcendatei an. Geben Sie einen Namen für die Ressourcendatei an.<br /><br /> Weitere Informationen finden Sie auf der MSDN-Website unter der **/fo**-Option im Artikel [Using RC (The RC Command Line) (Verwenden von RC (RC-Befehlszeile))](http://go.microsoft.com/fwlink/?LinkId=155730).|  
|**ShowProgress**|Optionaler **Boolean**-Parameter.<br /><br /> Wenn dieser `true` ist, werden Meldungen angezeigt, die über den Fortschritt des Compilers berichten.<br /><br /> Weitere Informationen finden Sie auf der MSDN-Website unter der **/v**-Option im Artikel [Using RC (The RC Command Line) (Verwenden von RC (RC-Befehlszeile))](http://go.microsoft.com/fwlink/?LinkId=155730).|  
|**Quelle**|Erforderlicher `ITaskItem[]` -Parameter.<br /><br /> Definiert ein Array von MSBuild-Quelldateielementen, die verbraucht und von Aufgaben ausgegeben werden können.|  
|**SuppressStartupBanner**|Optionaler **Boolean**-Parameter.<br /><br /> Bei `true` wird die Anzeige der Copyright- und Versionsnummernmeldung bei Aufgabenstart verhindert.<br /><br /> Geben Sie für weitere Informationen die Befehlszeilenoption **/?** ein, und klicken Sie auf die Option **/nologo**.|  
|**TrackerLogDirectory**|Optionaler **String**-Parameter.<br /><br /> Gibt das Verzeichnis des Nachverfolgungsprotokolls an.|  
|**UndefinePreprocessorDefinitions**|Hebt ein Präprozessorsymbol auf.<br /><br /> Weitere Informationen finden Sie auf der MSDN-Website unter der **/u**-Option im Artikel [Using RC (The RC Command Line) (Verwenden von RC (RC-Befehlszeile))](http://go.microsoft.com/fwlink/?LinkId=155730). Weitere Informationen finden Sie ebenfalls unter **PreprocessorDefinitions** in dieser Tabelle.|  
  
## <a name="remarks"></a>Hinweise  
  
## <a name="see-also"></a>Siehe auch  
 [Aufgabenreferenz](../msbuild/msbuild-task-reference.md)