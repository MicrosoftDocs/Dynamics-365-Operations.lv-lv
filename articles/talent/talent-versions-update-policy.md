---
title: Talent sistēmas prasības un atjaunināšanas politika
description: Šajā tēmā uzskaitītas prasības sistēmai Dynamics 365 for Talent. Turklāt ir ieskicēta atjaunināšanas politika.
author: andreabichsel
manager: AnnBe
ms.date: 05/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 6c881bf25e7145228ccf7ef73a7ef3637c115a49
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741779"
---
# <a name="talent-system-requirements-and-update-policy"></a>Talent sistēmas prasības un atjaunināšanas politika

[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstītas pakalpojuma Microsoft Dynamics 365 for Talent prasības, ieskaitot programmas Attract, Onboard un Core HR. Tajā ir arī norādītas valstis un reģioni, kur ir pieejama programma Talent, kā arī informācija par valodām un lokalizāciju, kas jāizmanto programmas Talent datiem. Turklāt šajā tēmā ir nodrošināta programmas Talent atjaunināšanas politika.

## <a name="supported-web-browsers"></a>Atbalstītās tīmekļa pārlūkprogrammas

Microsoft Dynamics 365 for Talent tīmekļa programmu var palaist jebkurā no tālāk uzskaitītajām tīmekļa pārlūkprogrammām, kas darbojas norādītajās operētājsistēmās. 

*   Microsoft Edge (jaunākā publiski pieejamā versija) operētājsistēmā Windows 10
*   Internet Explorer 11 operētājsistēmā Windows 10, Windows 8.1 vai Windows 7
*   Google Chrome (jaunākā publiski pieejamā versija)
*   Apple Safari (jaunākā publiski pieejamā versija)

Lai atrastu katras tīmekļa pārlūkprogrammas visjaunāko laidienu, dodieties uz programmatūras ražotāja vietni. 

> [!NOTE]
> * Lai tvertu attēlus, kas izveidoti Uzdevumu reģistrētājā un iekļautu tos Microsoft Word dokumentos, ir jābūt instalētam Chrome paplašinājumam. 
> * Darbplūsmas redaktors tiek startēts kā ClickOnce programma. ClickOnce programmas atbalsta tikai Microsoft Edge un Internet Explorer (atbalstītā Microsoft Windows versijā). Darbplūsmas redaktora ClickOnce programmai ir nepieciešama 64 bitu saderīga operētājsistēma.
> * Lai priekšskatītu PDF failus, ieteicams izmantot modernas pārlūkprogrammas, piemēram, Microsoft Edge (jaunāko publiski pieejamo versiju) operētājsistēmā Windows 10 vai Google Chrome (jaunāko publiski pieejamo versiju) operētājsistēmā Windows 10, Windows 8.1, Windows 8, Windows 7 vai Google Nexus 10 planšetdatoros.
>   Tīkla prasības
> * Dynamics 365 for Talent ir izstrādāta tīkliem, kuru latentums nepārsniedz 250–300 milisekundes (ms). Tas ir latentums no pārlūkprogrammas klienta līdz Microsoft Azure datu centram, kurā tiek viesota programma Dynamics 365 for Talent. Ieteicams pārbaudīt tīkla latentumu vietnē [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test").
> * Joslas platuma prasības programmai Dynamics 365 for Talent ir atkarīgas no jūsu scenārija. Tipiskākajiem scenārijiem ir nepieciešams joslas platums, kas ir lielāks par 50 kilobaitiem sekundē (KB/s).
> 
> [!WARNING]
> Neaprēķiniet nepieciešamo joslas platumu no klienta novietojuma, reizinot lietotāju skaitu ar minimālo nepieciešamo joslas platumu. Noteikta novietojuma vienlaicīgu izmantošanu ir ļoti grūti aprēķināt. Debitoriem, kurus uztrauc joslas platuma prasības, izmantojiet Dynamics 365 for Talent izmēģinājuma versiju.

## <a name="supported-microsoft-office-applications"></a>Atbalstītās Microsoft Office programmas

* Lai palaistu Microsoft Excel un Word pievienojumprogrammas, jābūt instalētai programmai Microsoft Office 2016 operētājsistēmai Windows vai Mac. Plašāku informāciju par versijas prasībām skatiet tēmā [Office integrācijas problēmu novēršana](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office integrācijas problēmu novēršana").
* Lai skatītu dokumentus, kas izveidoti, izmantojot funkcijas Eksportēt programmā Excel vai Eksportēt programmā Word, ir jābūt instalētai programmai Microsoft Office 2007 vai jaunākai versijai.

## <a name="regional-availability-languages-and-localization"></a>Reģionālā pieejamība, valodas un lokalizācija

Jūs varat lejupielādēt PDF failu ar valstīm, reģioniem un valodām, ko atbalsta programma Talent, lapā [Microsoft Dynamics 365 starptautiskā pieejamība](https://docs.microsoft.com/dynamics365/get-started/availability). 

> [!NOTE]
> Lietotāja interfeiss ir lokalizēts citās valodās, bet visi lietotāja dati tiek saglabāti tajā valodā, kādā tika ievadīti. Varat izveidot e-pasta ziņojumus un veidnes citās valodās, taču dati, piemēram, plānošanas informācija, pagaidām ir pieejami tikai angļu valodā.

Ja esat izstrādātājs un vēlaties izveidot valstij vai reģionam specifiskus pielāgojumus vai izveidot risinājumu valstij vai reģionam, ko Microsoft pašlaik neatbalsta, skatiet lapu [Globalizācija](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).

## <a name="update-policy"></a>Atjaunināšanas politika

Microsoft Dynamics 365 for Talent tiek apkalpots kā mākoņa piedāvājums. Dynamics 365 for Talent atjauninājumus pastāvīgi un automātiski piemēro Microsoft.

Atjauninājumi tiek izlaisti ar regulāru kadenci un tiek ieviesti visās vidēs. Dynamics 365 for Talent atbalsts tiek nodrošināts saskaņā ar [Microsoft Support Lifecycle politiku](https://support.microsoft.com/gp/lifecycle#gp/OSSLpolicy "Microsoft Support Lifecycle"), kas nodrošina pastāvīgas un prognozējamas vadlīnijas produkta atbalsta pieejamībai.
