---
title: Sistēmas prasības
description: Šajā tēmā uzskaitītas prasības sistēmai Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 15770595a0639c03df1138ec25010ca8168bd9a8
ms.sourcegitcommit: 49f7528d3268abe15e40f719956e1ec8696a6f4e
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/18/2021
ms.locfileid: "7393477"
---
# <a name="system-requirements"></a>Sistēmas prasības

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā tēmā uzskaitītas prasības sistēmai Microsoft Dynamics 365 Human Resources. Tajā ir arī norādītas valstis un reģioni, kur ir pieejama Human Resources, un informācija par valodām un lokalizāciju, kas jāizmanto Human Resources datiem.

## <a name="supported-web-browsers"></a>Atbalstītās tīmekļa pārlūkprogrammas

Lietotāji var piekļūt Microsoft Dynamics 365 Human Resources, izmantojot jebkuru no tālāk uzskaitītajām tīmekļa pārlūkprogrammām, kas darbojas norādītajās operētājsistēmās: 

*   Microsoft Edge (jaunākā publiski pieejamā versija) operētājsistēmā Windows 10
*   Internet Explorer 11 operētājsistēmā Windows 10, Windows 8.1 vai Windows 7
*   Google Chrome (jaunākā publiski pieejamā versija)
*   Apple Safari (jaunākā publiski pieejamā versija)

Lai atrastu katras tīmekļa pārlūkprogrammas visjaunāko laidienu, dodieties uz programmatūras ražotāja vietni. 

## <a name="special-considerations"></a>Īpaši apsvērumi

* Lai uzdevumu ierakstītājam atļautu ekrānuzņēmuma attēlu tveršanu un iekļaušanu ģenerētajos Microsoft Word dokumentos, jāinstalē Chrome paplašinājuma pirmsizlaides versija
* Darbplūsmas redaktors tiek startēts kā ClickOnce programma. ClickOnce programmas atbalsta tikai Microsoft Edge un Internet Explorer (atbalstītā Microsoft Windowsversijā). Darbplūsmas redaktora ClickOnce programmai ir nepieciešama 64 bitu saderīga operētājsistēma.
* Lai priekšskatītu PDF failus, ieteicams izmantot modernas pārlūkprogrammas, piemēram, Microsoft Edge (jaunāko publiski pieejamo versiju) operētājsistēmā Windows 10 vai Google Chrome (jaunāko publiski pieejamo versiju) operētājsistēmā Windows 10, Windows 8.1, Windows 8, Windows 7 vai Google Nexus 10 planšetdatoros.

## <a name="network-requirements"></a>Tīkla prasības

* Human Resources ir izstrādāta tīkliem, kuru latentums nepārsniedz 250–300 milisekundes (ms). Tas ir latentums no pārlūkprogrammas klienta līdz Microsoft Azure datu centram, kurā tiek viesota Human Resources. Ieteicams pārbaudīt tīkla latentumu vietnē [www.azurespeed.com](https://www.azurespeed.com "Azure latentuma pārbaude").
* Joslas platuma prasības Human Resources ir atkarīgas no jūsu scenārija. Tipiskākajiem scenārijiem ir nepieciešams joslas platums, kas ir lielāks par 50 kilobaitiem sekundē (KB/s).
 
> [!WARNING]
> Neaprēķiniet nepieciešamo joslas platumu no klienta novietojuma, reizinot lietotāju skaitu ar minimālo nepieciešamo joslas platumu. Noteikta novietojuma vienlaicīgu izmantošanu ir ļoti grūti aprēķināt. Debitoriem, kurus uztrauc joslas platuma prasības, izmantojiet Human Resources izmēģinājuma versiju.

## <a name="supported-microsoft-office-applications"></a>Atbalstītās Microsoft Office programmas

* Lai palaistu Microsoft Excel un Word pievienojumprogrammas, jābūt instalētai programmai Microsoft Office 2016 operētājsistēmai Windows vai Mac. Plašāku informāciju par versijas prasībām skatiet sadaļā [Office integrācijas problēmu novēršana](../fin-ops-core/dev-itpro/office-integration/office-integration-troubleshooting.md "Office integrācijas problēmu novēršana").
* Lai skatītu dokumentus, kas izveidoti, izmantojot funkcijas Eksportēt programmā Excel vai Eksportēt programmā Word, ir jābūt instalētai programmai Microsoft Office 2007 vai jaunākai versijai.

## <a name="regional-availability-languages-and-localization"></a>Reģionālā pieejamība, valodas un lokalizācija

Varat lejupielādēt PDF failu ar valstīm, reģioniem un valodām, ko atbalsta Human Resources, lapā [Pakalpojuma Microsoft Dynamics 365 starptautiskā pieejamība](/dynamics365/get-started/availability). 

> [!NOTE]
> Lietotāja interfeiss ir lokalizēts citās valodās, bet visi lietotāja dati tiek saglabāti tajā valodā, kādā tika ievadīti. Varat izveidot e-pasta ziņojumus un veidnes citās valodās, taču dati, piemēram, plānošanas informācija, pagaidām ir pieejami tikai angļu valodā.

Ja esat izstrādātājs un vēlaties izveidot valstij vai reģionam specifiskus pielāgojumus vai izveidot risinājumu valstij vai reģionam, ko Microsoft pašlaik neatbalsta, skatiet lapu [Globalizācija](/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
