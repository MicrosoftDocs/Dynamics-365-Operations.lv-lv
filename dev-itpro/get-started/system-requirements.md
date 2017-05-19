---
title: "Sistēmas prasības"
description: "Šajā tēmā ir uzskaitītas sistēmas prasības pašreizējai Microsoft Dynamics 365 for Operations versijai."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 86053196a3aad6b7b5d7830860e1af347dd969d8
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="system-requirements"></a>Sistēmas prasības

[!include[banner](../includes/banner.md)]


Šajā tēmā ir uzskaitītas sistēmas prasības pašreizējai Microsoft Dynamics 365 for Operations versijai.

<a name="supported-web-browsers"></a>Atbalstītās tīmekļa pārlūkprogrammas
----------------------

Microsoft Dynamics 365 for Operations tīmekļa programmu var palaist jebkurā no tālāk uzskaitītajām tīmekļa pārlūkprogrammām, kas darbojas norādītajās operētājsistēmās.

-   Microsoft Edge (jaunākā publiski pieejamā versija) operētājsistēmā Windows 10
-   Internet Explorer 11 operētājsistēmā Windows 10, Windows 8.1 vai Windows 7
-   Google Chrome (jaunākā publiski pieejamā versija) operētājsistēmā Windows 10, Windows 8.1, Windows 8, Windows 7 vai Google Nexus 10 planšetdatorā
-   Apple Safari (jaunākā publiski pieejamā versija) operētājsistēmā Mac OS X 10.10 (Yosemite), 10.11 (El Capitan), 10.12 (Sierra) vai Apple iPad

Lai atrastu katras tīmekļa pārlūkprogrammas visjaunāko laidienu, dodieties uz programmatūras ražotāja vietni. **Piezīmes.**

-   Lai tvertu attēlus, kas izveidoti Uzdevumu reģistrētājā un iekļautu tos Microsoft Word dokumentos, ir jābūt instalētam Chrome paplašinājumam. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/operations/dev-itpro/user-interface/task-recorder).-->
-   Darbplūsmas redaktors tiek startēts kā ClickOnce programma. ClickOnce programmas atbalsta tikai Microsoft Edge un Internet Explorer (atbalstītā Microsoft Windows versijā). Darbplūsmas redaktora ClickOnce programmai ir nepieciešama 64 bitu saderīga operētājsistēma.
-   Pārskatu noformētājs finanšu pārskatiem tiek startēts kā ClickOnce programma. Tam ir nepieciešama 64 bitu saderīga operētājsistēma. Ja lietojat pārlūkprogrammu Chrome, lai varētu lejupielādēt pārskatu veidošanas klientu, ir jāinstalē paplašinājums ClickOnce. Ja lietojat pārlūkprogrammu Chrome inkognito režīmā, pārliecinieties, ka paplašinājums ClickOnce ir arī iespējots inkognito režīmā.
-   Lai priekšskatītu PDF failus, ieteicams izmantot modernas pārlūkprogrammas, piemēram, Microsoft Edge (jaunāko publiski pieejamo versiju) operētājsistēmā Windows 10 vai Google Chrome (jaunāko publiski pieejamo versiju) operētājsistēmā Windows 10, Windows 8.1, Windows 8, Windows 7 vai Google Nexus 10 planšetdatoros.


### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Retail Cloud POS atbalstītās tīmekļa pārlūkprogrammas

Retail Cloud POS programmatūrai Microsoft Dynamics 365 for Operations var palaist jebkurā no tālāk uzskaitītajām tīmekļa pārlūkprogrammām, kas darbojas norādītajās operētājsistēmās.

-   Microsoft Edge (jaunākā publiski pieejamā versija) operētājsistēmā Windows 10
-   Internet Explorer 11 operētājsistēmā Windows 10, Windows 8.1 vai Windows 7
-   Chrome (jaunākā publiski pieejamā versija) operētājsistēmā Windows 10, Windows 8.1 vai Windows 7

## <a name="network-requirements"></a>Tīkla prasības
-   Programma Dynamics 365 for Operations ir izstrādāta tīkliem, kuru latentums ir mazāks par 150 milisekundēm (ms). Tas ir latentums no pārlūkprogrammas klienta līdz Microsoft Azure datu centram, kurā tiek viesota programma Microsoft Dynamics 365 for Operations. Ieteicams pārbaudīt tīkla latentumu vietnē <http://www.azurespeed.com>.
-   Joslas platuma prasības programmai Dynamics 365 for Operations ir atkarīgas no scenārija. Tipiskākajiem scenārijiem ir nepieciešams joslas platums, kas ir lielāks par 50 kilobaitiem sekundē (KB/s). Tomēr scenārijiem, kuriem ir augstas lietderīgās slodzes prasības, piemēram, darbvietām, vai scenārijiem, kuru ietvaros tiek veikta plaša pielāgošana, ieteicams izmantot lielāku joslas platumu.

Parasti programma Dynamics 365 for Operations ir optimizēta internetam. Ciklu skaits no pārlūkprogrammas klienta uz Azure datu centru ir pavisam neliels, un visa lietderīgā slodze tiek saspiesta. **Brīdinājums.** Neaprēķiniet nepieciešamo joslas platumu no klienta novietojuma, reizinot lietotāju skaitu ar minimālo nepieciešamo joslas platumu. Noteikta novietojuma vienlaicīgu izmantošanu ir ļoti grūti aprēķināt. Debitoriem, kurus uztrauc joslas platuma prasības, izmantojiet Dynamics 365 for Operations priekšskatījuma versiju.

## <a name="net-framework-requirements"></a>.NET Framework prasības
Programmai Dynamics 365 for Operations ir nepieciešama .NET Framework versija 4.6.2 visām viena klikšķa programmām, piemēram, dokumentu maršrutēšanas aģentam. Instalācijas instrukcijas skatiet sadaļā [.NET Framework instalācija](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-microsoft-office-applications"></a>Atbalstītās Microsoft Office programmas
-   Lai palaistu Microsoft Excel un Word pievienojumprogrammas, jābūt instalētai programmai Microsoft Office 2016 operētājsistēmai Windows vai Mac. Plašāku informāciju par versijas prasībām skatiet sadaļā [Office integrācijas problēmu novēršana](/dynamics365/operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   Lai skatītu dokumentus, kas izveidoti, izmantojot funkcijas Eksportēt programmā Excel vai Eksportēt programmā Word, ir jābūt instalētai programmai Microsoft Office 2007 vai jaunākai versijai.

## <a name="retail-modern-pos-requirements"></a>Retail Modern POS prasības
### <a name="supported-operating-systems"></a>Atbalstītās operētājsistēmas

-   Retail Modern POS ir 32 bitu programma, taču tā darbojas gan x86, gan x64 arhitektūrā.
-   Programma Retail Modern POS tiek atbalstīta tikai operētājsistēmā Windows 10 Pro, Enterprise un Enterprise Long Term Servicing Branch (LTSB) versijās.

### <a name="minimum-system-requirements"></a>Minimālās sistēmas prasības

-   Minimālā atbalstītā izšķirtspēja ir 1280 × 1024.
-   Datoram, kurā tiek izmantota programma Retail Modern POS, jāatbilst šādām prasībām:
    -   Tam jābūt vismaz divkodolu procesoram, kura takts frekvence ir vismaz 2 gigaherci (GHz).
    -   Tam jābūt vismaz 3 gigabaitiem (GB) RAM.
    -   Tam jābūt piekļuvei internetam.

## <a name="retail-hardware-station-requirements"></a>Retail hardware station prasības
### <a name="supported-operating-systems"></a>Atbalstītās operētājsistēmas

-   Retail hardware station ir 32 bitu programma, taču tā darbojas gan x86, gan x64 arhitektūrā.
-   Programma Retail hardware station tiek atbalstīta šādās operētājsistēmās:
    -   Windows 7 Professional, Enterprise, un Ultimate versijas **Piezīme.** Windows 7 tiek atbalstīta tikai tad, ja pārlūkprogramma Internet Explorer 11 ir manuāli instalēta sistēmā.
    -   Windows 8.1 1. atjauninājums Professional, Enterprise un Embedded versijas
    -   Windows 10 Pro, Enterprise un Enterprise LTSB versijas

### <a name="minimum-system-requirements"></a>Minimālās sistēmas prasības

Datoram ir jāatbilst visām sistēmas prasībām tālāk minēto vienumu instalēšanai un izmantošanai:

-   Interneta informācijas pakalpojumi (IIS)
-   Trešās puses aparatūra

## <a name="retail-store-scale-unit-requirements"></a>Retail Store Scale Unit prasības
### <a name="supported-operating-systems"></a>Atbalstītās operētājsistēmas

-   Retail Store Scale Unit ir 32 bitu programma, taču tā darbojas gan x86, gan x64 arhitektūrā.
-   Programma Retail Store Scale Unit tiek atbalstīta šādās operētājsistēmās:
    -   Windows 7 Professional, Enterprise un Ultimate versijas
    -   Windows 8.1 1. atjauninājums Professional, Enterprise un Embedded versijas
    -   Windows 10 Pro, Enterprise un Enterprise LTSB versijas

### <a name="minimum-system-requirements"></a>Minimālās sistēmas prasības

-   4 GB RAM
-   1,6 GHz maksimālais centrālā procesora ātrums katram kodolam (Ir jābūt vismaz diviem kodoliem.)
-   Vismaz 10 GB brīvās vietas (Kanāla datu bāzei var būt nepieciešams lielāks vietas daudzums.)

### <a name="recommended-system-requirements"></a>Ieteicamās sistēmas prasības

-   6 GB RAM
-   2,4 GHz i7 (vai ekvivalents) maksimālais centrālā procesora ātrums katram kodolam (Ieteicami vismaz četri kodoli.)
-   Vismaz 10 GB brīvās vietas (Kanāla datu bāzei var būt nepieciešams lielāks vietas daudzums.)

## <a name="requirements-for-development-on-local-vms"></a>Prasības izstrādei lokālās virtuālajās mašīnās
Informāciju par prasībām attiecībā uz izstrādi vietējās virtuālajās mašīnās (VM) skatiet sadaļā [VM, kuras darbojas lokāli](../dev-tools/access-instances.md).

<a name="see-also"></a>Skatiet arī
--------

[Iegūt Dynamics 365 for Operations iepazīšanās versiju](/dynamics365/operations/dev-itpro/dev-tools/get-evaluation-copy)




