---
title: Dzīves notikumu apstrāde
description: Darbinieku dzīves cikla laikā Microsoft Dynamics 365 Human Resources katrs darbinieks var sastapties ar dažādām dzīves notikumu izmaiņām.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e6bfbb9e31a7d8973c2b993f3792a7216f41924e0ff4c24b08c0dd954ab327c7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775021"
---
# <a name="process-life-events"></a>Dzīves notikumu apstrāde

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Darbinieku dzīves cikla laikā Microsoft Dynamics 365 Human Resources katrs darbinieks var sastapties ar dažādām dzīves notikumu izmaiņām. Piemēram, laulība, izmaiņas nodarbinātībā vai apgādājamā/saņēmēja maiņa. Lai izmantotu dzīves notikumus, atvieglojumu parametru veidlapā ir jāiespējo dzīves notikumi, jāiestata dzīves notikumu veidi un dzīves notikumu opcijas plānu veidiem.

Lai varētu apstrādāt dzīves notikumus, vismaz vienu reizi darbā pieņemšanas laika periodā ir jābūt jau izpildītai atvērtai reģistrācijai. Savienotajās Valstīs atvērta reģistrācija parasti notiek reizi gadā. Ārpus Savienotajām Valstīm atvērto reģistrāciju var izpildīt darbā pieņemšanas laikā. Nodarbinātajam nav jāatlasa atvieglojumu plāns, lai varētu apstrādāt dzīves notikumus, bet tie ir jāiekļauj atvērtajā reģistrācijas apstrādē. 

Izmantojiet dzīves notikumu apstrādi, ja ir nodarbinātie, kuru dzīves notikumi notiks nākotnes datumā. Šis notikums apstrādās visus dzīves notikumus, kas nav apstrādāti (piemēram, turpmākās dzīves notikumus vai dzīves notikumus, kas ir pievienoti un kas nav raksturīgi nevienam citam darbiniekam — viens piemērs ir jauns atvieglojums). Reālā laika dzīves notikumi ir paslēpti.

Piemēram, ja šodien ir 1. februāris un 14. februārī nodarbinātajam Jānim Bērziņam jāmaina juridiskā persona, ja izpildīsiet dzīves notikumu apstrādi 15. februārim, sistēma apstrādās visus notikumus līdz 15. februārim. 

1. Darbvietā **Atvieglojumu pārvaldība** sadaļā **Apstrāde** atlasiet **Dzīves notikumu apstrāde**.

2. Dialoglodziņā **Izpildīt dzīves notikumu apstrādi** norādiet vērtības tālāk minētajiem laukiem.

   | Lauks | Apraksts |
   | --- | --- |
   | **Reģistrācijas periods** | Reģistrācijas periods, kuram apstrādāt dzīves notikumus. |
   | **Juridiska persona** | Juridiskā persona, kam apstrādāt dzīves notikumus. |
   | **Dzīves notikuma datums** | Sistēma apstrādā visus notikumus reģistrācijas periodā, kas notiek līdz šim datumam. |
   | **Nodarbinātais** | Nodarbinātais, kuram apstrādāt dzīves notikumus. Ja šo lauku atstāsiet tukšu, dzīves notikumi tiks apstrādāti visiem nodarbinātajiem. |

3. Ja vēlaties izpildīt apstrādi fonā, atlasiet **Izpildīt fonā** un veiciet tālāk minētos uzdevumus.

   1. Ievadiet informāciju apstrādei.

   2. Lai iestatītu periodisku darbu, atlasiet **Periodiskums**, ievadiet periodiskuma informāciju un atlasiet **Labi**.

   3. Lai iestatītu darba brīdinājumu, atlasiet **Brīdinājumi**, atlasiet saņemamos brīdinājumus un pēc tam atlasiet **Labi**.

   4. Atlasiet **Labi**. Apstrāde tiks izpildīta ar iestatītajiem parametriem.

4. Atlasiet **Labi**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]