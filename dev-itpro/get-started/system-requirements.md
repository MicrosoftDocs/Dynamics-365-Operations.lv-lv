---
title: "Sistēmas prasības"
description: "Šajā tēmā ir uzskaitītas sistēmas prasības pašreizējai Microsoft Dynamics 365 for Finance and Operations izdevuma Enterprise versijai."
author: sericks007
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
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
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 724ee7ec29f8a9c4e8cc0b244193cd6c83c37f03
ms.contentlocale: lv-lv
ms.lasthandoff: 06/13/2017


---

# <a name="system-requirements"></a>Sistēmas prasības

[!include[banner](../includes/banner.md)]


Šajā tēmā ir uzskaitītas sistēmas prasības pašreizējai Microsoft Dynamics 365 for Finance and Operations izdevuma Enterprise versijai.

<a name="supported-web-browsers"></a>Atbalstītās tīmekļa pārlūkprogrammas
----------------------

Tīmekļa programmu var palaist jebkurā no tālāk uzskaitītajām tīmekļa pārlūkprogrammām, kas darbojas norādītajās operētājsistēmās.

-   Microsoft Edge (jaunākā publiski pieejamā versija) operētājsistēmā Windows 10
-   Internet Explorer 11 operētājsistēmā Windows 10, Windows 8.1 vai Windows 7
-   Google Chrome (jaunākā publiski pieejamā versija) operētājsistēmā Windows 10, Windows 8.1, Windows 8, Windows 7 vai Google Nexus 10 planšetdatorā
-   Apple Safari (jaunākā publiski pieejamā versija) operētājsistēmā Mac OS X 10.10 (Yosemite), 10.11 (El Capitan), 10.12 (Sierra) vai Apple iPad

Lai atrastu katras tīmekļa pārlūkprogrammas visjaunāko laidienu, dodieties uz programmatūras ražotāja vietni. 

**Piezīmes.**

-   Lai uzdevumu ierakstītājam atļautu ekrānuzņēmuma attēlu tveršanu un iekļaušanu ģenerētajos Microsoft Word dokumentos, jāinstalē Chrome paplašinājuma pirmsizlaides versija. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/unified-operations/dev-itpro/user-interface/task-recorder).-->
-   Darbplūsmas redaktors tiek startēts kā ClickOnce programma. ClickOnce programmas atbalsta tikai Microsoft Edge un Internet Explorer (atbalstītā Microsoft Windows versijā). Darbplūsmas redaktora ClickOnce programmai ir nepieciešama 64 bitu saderīga operētājsistēma.
-   Pārskatu noformētājs finanšu pārskatiem tiek startēts kā ClickOnce programma. Tam ir nepieciešama 64 bitu saderīga operētājsistēma. Ja lietojat pārlūkprogrammu Chrome, lai varētu lejupielādēt pārskatu veidošanas klientu, ir jāinstalē paplašinājums ClickOnce. Ja lietojat pārlūkprogrammu Chrome inkognito režīmā, pārliecinieties, ka paplašinājums ClickOnce ir arī iespējots inkognito režīmā.
-   Lai priekšskatītu PDF failus, ieteicams izmantot modernas pārlūkprogrammas, piemēram, Microsoft Edge (jaunāko publiski pieejamo versiju) operētājsistēmā Windows 10 vai Google Chrome (jaunāko publiski pieejamo versiju) operētājsistēmā Windows 10, Windows 8.1, Windows 8, Windows 7 vai Google Nexus 10 planšetdatoros.


### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Retail Cloud POS atbalstītās tīmekļa pārlūkprogrammas

Retail Cloud POS var palaist jebkurā no tālāk uzskaitītajām tīmekļa pārlūkprogrammām, kas darbojas norādītajās operētājsistēmās.

-   Microsoft Edge (jaunākā publiski pieejamā versija) operētājsistēmā Windows 10
-   Internet Explorer 11 operētājsistēmā Windows 10, Windows 8.1 vai Windows 7
-   Chrome (jaunākā publiski pieejamā versija) operētājsistēmā Windows 10, Windows 8.1 vai Windows 7

## <a name="network-requirements"></a>Tīkla prasības
-   Programmatūras Dynamics 365 Finance and Operations izdevums Enterprise ir izstrādāts tīkliem, kuru latentums ir 250–300 milisekundes (ms) vai mazāks. Tas ir latentums no pārlūkprogrammas klienta līdz Microsoft Azure datu centram, kurā tiek viesota programmatūra Finance and Operations. Ieteicams pārbaudīt tīkla latentumu vietnē <http://www.azurespeed.com>.
-   Joslas platumu prasības ir atkarīgas no jūsu scenārija. Tipiskākajiem scenārijiem ir nepieciešams joslas platums, kas ir lielāks par 50 kilobaitiem sekundē (KB/s). Tomēr scenārijiem, kuriem ir augstas lietderīgās slodzes prasības, piemēram, darbvietām, vai scenārijiem, kuru ietvaros tiek veikta plaša pielāgošana, ieteicams izmantot lielāku joslas platumu.

Parasti programmatūra Finance and Operations ir optimizēta internetam. Ciklu skaits no pārlūkprogrammas klienta uz Azure datu centru ir neliels, un visa lietderīgā slodze tiek saspiesta. 

**Brīdinājums.** Neaprēķiniet nepieciešamo joslas platumu no klienta novietojuma, reizinot lietotāju skaitu ar minimālo nepieciešamo joslas platumu. Noteikta novietojuma vienlaicīgu izmantošanu ir grūti aprēķināt. Debitoriem, kurus uztrauc joslas platuma prasības, izmantojiet Finance and Operations priekšskatījuma versiju.

## <a name="net-framework-requirements"></a>.NET Framework prasības
ClickOnce programmām, piemēram, dokumentu maršrutēšanas aģentam, ir nepieciešama .NET Framework versija 4.6.2. Instalācijas instrukcijas skatiet sadaļā [.NET Framework instalācija](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-microsoft-office-applications"></a>Atbalstītās Microsoft Office programmas
-   Lai palaistu Microsoft Excel un Word pievienojumprogrammas, jābūt instalētai programmai Microsoft Office 2016 operētājsistēmai Windows vai Mac. Plašāku informāciju par versijas prasībām skatiet sadaļā [Office integrācijas problēmu novēršana](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting).
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

## <a name="connector-requirements"></a>Savienotāja prasības
### <a name="supported-operating-systems"></a>Atbalstītās operētājsistēmas

-   Microsoft Dynamics AX savienotājam ir divas atsevišķas instalēšanas programmas — **Async Server Connector service** un **Real-time service for Dynamics AX 2012 R3**.
-   Abi komponenti ir 32 bitu programmas, taču tie darbojas gan x86, gan x64 arhitektūrā.
-   Abi komponenti tiek atbalstīti šādas operētājsistēmās:
    -   Windows 7 Professional, Enterprise un Ultimate versijas
    -   Windows 8.1 1. atjauninājums Professional, Enterprise un Embedded versijas
    -   Windows 10 Pro, Enterprise un Enterprise LTSB versijas
    -   Windows Server 2012 R2, Windows Server 2016

### <a name="minimum-system-requirements"></a>Minimālās sistēmas prasības

-   Ieteicams ar 2 GB vai 4 GB RAM
-   1,6 GHz maksimālais centrālā procesora ātrums katram kodolam (Ir jābūt vismaz diviem kodoliem.)
-   Vismaz 10 GB brīvās vietas (Kanāla datu bāzei var būt nepieciešams lielāks vietas daudzums.)

## <a name="requirements-for-development-on-local-vms"></a>Prasības izstrādei lokālās virtuālajās mašīnās
Informāciju par prasībām attiecībā uz izstrādi vietējās virtuālajās mašīnās (VM) skatiet sadaļā [VM, kuras darbojas lokāli](../dev-tools/access-instances.md).

<a name="see-also"></a>Skatiet arī
--------

[Iegūt Dynamics 365 for Finance and Operations izdevuma Enterprise iepazīšanās kopiju](/dynamics365/unified-operations/dev-itpro/dev-tools/get-evaluation-copy)





