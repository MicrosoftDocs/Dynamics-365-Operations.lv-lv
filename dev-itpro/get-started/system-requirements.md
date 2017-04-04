---
title: "Sistēmas prasības"
description: "Šajā tēmā uzskaitītas pašreizējā versijā Microsoft Dynamics 365 operāciju sistēmas prasības."
author: sericks007
manager: AnnBe
ms.date: 2017-04-04
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
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 9220c093d3f6d6700127c93651db4083be300311
ms.lasthandoff: 03/31/2017


---

# <a name="system-requirements"></a>Sistēmas prasības

Šajā tēmā uzskaitītas pašreizējā versijā Microsoft Dynamics 365 operāciju sistēmas prasības.

<a name="supported-web-browsers"></a>Atbalstītās tīmekļa pārlūkprogrammas
----------------------

Microsoft Dynamics 365 operācijas web lietojumprogrammas var palaist jebkurā no šīm web pārlūkprogrammas un kas darbojas noteiktā operētājsistēmas:

-   Microsoft Edge (jaunāko publiski pieejamā versija), Windows 10
-   Internet Explorer 11 operētājsistēmā Windows 10, Windows 8.1 vai Windows 7
-   Google Chrome (jaunāko publiski pieejamā versija) operētājsistēmā Windows 10, Windows 8.1, Windows 8, Windows 7 vai Google Nexus 10 tablet
-   Apple Safari (jaunāko publiski pieejamā versija) uz Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) vai 10.12 (Sierra) vai Apple iPad

Lai atrastu katras tīmekļa pārlūkprogrammas visjaunāko laidienu, dodieties uz programmatūras ražotāja vietni. **Piezīmes.**

-   Lai uzņemtu attēlus, kas tiek ģenerēti no uzdevuma rakstītāju un tos iekļaut Microsoft Word dokumentus, jums ir jābūt Chrome paplašinājumu instalēta. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/operations/dev-itpro/user-interface/task-recorder).-->
-   Darbplūsmas redaktors tiek sākts kā ClickOnce lietojumprogramma. Tikai Microsoft Edge un Internet Explorer (par atbalstītajiem Microsoft Windows versijai) atbalsta ClickOnce pieteikumus. Darbplūsmas redaktors ClickOnce lietojumprogramma ir nepieciešama 64 bitu saderīga operētājsistēmu.
-   Report Designer finanšu pārskatiem tiek sākts kā ClickOnce lietojumprogramma. Tā ir nepieciešama 64 bitu saderīga operētājsistēmu. Ja jūs izmantojat Chrome, lai lejupielādētu ziņojumu designer klienta jāinstalē ClickOnce paplašinājums. Ja jūs izmantojat Chrome inkognito režīmā, pārliecinieties, ka ClickOnce paplašinājumu iespējots inkognito režīmā.

### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Retail Cloud POS atbalstītās tīmekļa pārlūkprogrammas

Mazumtirdzniecības mākonis POS Dynamics 365 operācijām var palaist jebkurā no šīm web pārlūkprogrammas un kas darbojas noteiktā operētājsistēmas:

-   Microsoft Edge (jaunāko publiski pieejamā versija), Windows 10
-   Internet Explorer 11 operētājsistēmā Windows 10, Windows 8.1 vai Windows 7
-   Hroma (jaunāko publiski pieejamā versija) Windows 10, Windows 8.1 vai Windows 7

## <a name="network-requirements"></a>Tīkla prasībām.
-   Dinamika 365 operācijām ir paredzēts tīklu latentumu mazāk nekā 150 milisekundēm (ms). Tas ir Latentums no klienta pārlūkprogramma Microsoft Azure datu centrā, kas vieso Dynamics 365 operācijām. Mēs iesakām jums pārbaudīt tīkla latentumu par <http://www.azurespeed.com>.
-   Joslas platuma prasības Dynamics 365 darbības ir atkarīgas no jūsu scenārijs. Tipiskākās scenāriji pieprasa frekvenču joslas platums ir vairāk nekā 50 kilobaiti sekundē (KB/s). Tomēr gadījumi, kas ir liela celtspēja prasības, piemēram, darbvietas vai scenārijiem, kas ietver plašas pielāgošanas ir ieteicama lielāku joslas platumu.

Kopumā, Dynamics 365 operācijām ir optimizēts interneta. Reisi no pārlūkprogrammu klienta debeszils datu centru skaits ir ļoti mazs, un visa lietderīgā slodze ir saspiests. **Brīdinājums:** nav aprēķināt joslas platuma prasības no klienta atrašanās vietas lietotāju skaitu reizinot ar minimālo joslas platuma prasības. Vienlaicīgu lietošanu konkrētā vietā ir ļoti grūti aprēķināt. Klientiem, kuri uztraucas par joslas platuma prasības, izmantot priekšskatījuma versiju Dynamics 365 operācijām.

## <a name="net-framework-requirements"></a>.NET framework prasības
Dinamika 365 operācijām ir nepieciešama .NET Framework versija 4.6.2 visus noklikšķiniet-vienreiz lietojumprogrammas, piemēram, dokumenta maršrutēšanas aģents. Instalācijas instrukcijas, skatiet [instalējot .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-microsoft-office-applications"></a>Atbalsta Microsoft Office lietojumprogrammām
-   Lai palaist Microsoft Excel un Word pievienojumprogrammas, datorā jābūt instalētai Microsoft Office 2016 Windows vai Mac uzstādīta. Plašāku informāciju par versiju prasībām skatiet [Office integrācijas problēmu novēršanas](/dynamics365/operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   Skatīt dokumentus, ko ģenerējusi eksportēt uz Excel vai Word funkcionalitāti eksportam, ir jābūt Microsoft Office 2007 vai jaunāka versija.

## <a name="retail-modern-pos-requirements"></a>Mazumtirdzniecības POS mūsdienu prasībām
### <a name="supported-operating-systems"></a>Atbalstītās operētājsistēmas

-   Mazumtirdzniecība modernas POS ir 32 bitu lietojumprogramma, bet tā darbosies gan x86 un x64 arhitektūras.
-   Mazumtirdzniecība modernas POS ir atbalstīta tikai izdevumos Windows 10 Pro, Enterprise un uzņēmuma garu terminu apkalpošanas filiāle (LTSB).

### <a name="minimum-system-requirements"></a>Minimālajām sistēmas prasībām

-   Minimālā atbalstītā izšķirtspēja ir 1280 × 1024.
-   Dators, kas darbojas mazumtirdzniecības mūsdienu POS jāatbilst šīm prasībām:
    -   Tai ir jābūt, kā minimums, dual-core procesoru, kas darbojas pie ne mazāk kā 2 gigahercu (GHz).
    -   Tai jābūt vismaz 3 gigabaitiem (GB) RAM.
    -   Tai jābūt pieejai internetam.

## <a name="retail-hardware-station-requirements"></a>Mazumtirdzniecības stacijas prasības aparatūrai
### <a name="supported-operating-systems"></a>Atbalstītās operētājsistēmas

-   Mazumtirdzniecības aparatūras stacija ir 32 bitu lietojumprogramma, bet tā darbosies gan x86 un x64 arhitektūras.
-   Mazumtirdzniecības aparatūras stacija tiek atbalstīta šādām operētājsistēmām:
    -   Izdevumos Windows 7 Professional, Enterprise un Ultimate **Piezīme:** Windows 7 tiek atbalstīta tikai, ja Internet Explorer 11 manuāli ir instalēts sistēmā.
    -   8.1. Windows Update 1 izdevumos Professional, Enterprise un iegultie
    -   Windows 10 Pro, Enterprise un Enterprise LTSB izdevumi

### <a name="minimum-system-requirements"></a>Minimālajām sistēmas prasībām

Datoram ir jāatbilst visām sistēmas prasībām, instalējot un lietojot šādus vienumus:

-   Interneta informācijas pakalpojumi (IIS)
-   Trešās puses aparatūra

## <a name="retail-store-scale-unit-requirements"></a>Mazumtirdzniecības veikala mēroga struktūrvienības prasības
### <a name="supported-operating-systems"></a>Atbalstītās operētājsistēmas

-   Mazumtirdzniecības veikalu skalas vienība ir 32 bitu lietojumprogramma, bet tā darbosies gan x86 un x64 arhitektūras.
-   Mazumtirdzniecības veikalu skalas vienība tiek atbalstīta šādām operētājsistēmām:
    -   Izdevumos Windows 7 Professional, Enterprise un Ultimate
    -   8.1. Windows Update 1 izdevumos Professional, Enterprise un iegultie
    -   Windows 10 Pro, Enterprise un Enterprise LTSB izdevumi

### <a name="minimum-system-requirements"></a>Minimālajām sistēmas prasībām

-   4 GB RAM
-   1.6 GHz pīķa CPU ātrums katram kodols (divas serdes ir minimums).
-   Vismaz 10 GB brīvas vietas (kanāla datu bāze var pieprasīt lielu daudzumu telpā.)

### <a name="recommended-system-requirements"></a>Ieteicamās sistēmas prasības

-   6 GB RAM
-   2.4 GHz i7 (vai ekvivalents) pīķa CPU ātrums katram kodols (četriem serdeņiem ir ieteicama).
-   Vismaz 10 GB brīvas vietas (kanāla datu bāze var pieprasīt lielu daudzumu telpā.)

## <a name="requirements-for-development-on-local-vms"></a>Attīstība attiecībā uz vietējo VMs prasības
Skatiet informāciju par prasībām attiecībā uz attīstības vietējās virtuālās mašīnas (VMs), [VM darbojas lokālā](/dynamics365/operations/dev-itpro/dev-tools/access-instances#vm-that-is-running-in-premises).

<a name="see-also"></a>Skatiet arī
--------

[Iegūt novērtējuma kopiju Dynamics 365 operācijām](/dynamics365/operations/dev-itpro/dev-tools/get-evaluation-copy)


