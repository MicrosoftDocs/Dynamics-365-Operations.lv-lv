---
title: Procesa reģistrācijas piemērojamība
description: Šajā rakstā ir paskaidrots, kā izpildīt reģistrācijas piemērotības apstrādi.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 78a7de6dbb8d8ed13392eb7eb9aa02b15db2e009
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693176"
---
# <a name="process-enrollment-eligibility"></a>Procesa reģistrācijas piemērojamība


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā rakstā ir paskaidrots, kā izpildīt reģistrācijas piemērotības apstrādi.

1. Darbvietā **Atvieglojumu pārvaldība** sadaļā **Apstrāde** atlasiet **Reģistrācijas piemērotības apstrāde**.

2. Dialoglodziņā **Izpildīt atvieglojumu reģistrācijas piemērotības apstrādi** norādiet vērtības tālāk minētajiem laukiem.

   | Lauks | Apraksts |
   | --- | --- |
   | **Reģistrācijas periods** | Reģistrācijas periods, kuram apstrādāt reģistrācijas piemērotību. |
   | **Juridiska persona** | Juridiskā persona, kam apstrādāt reģistrācijas piemērotību. |
   | **Nodarbinātais** | Nodarbinātais, kuram apstrādāt reģistrācijas piemērotību. Ja šo lauku atstāsiet tukšu, reģistrācijas piemērotība tiks apstrādāta visiem nodarbinātajiem. |
   | **Atvieglojumu plāns** | Atvieglojumu plāns, kam apstrādāt reģistrācijas piemērotību.

3. Ja vēlaties izpildīt apstrādi fonā, atlasiet **Izpildīt fonā** un veiciet tālāk minētos uzdevumus.

   1. Ievadiet informāciju apstrādei.

   2. Lai iestatītu periodisku darbu, atlasiet **Periodiskums**, ievadiet periodiskuma informāciju un atlasiet **Labi**.

   3. Lai iestatītu darba brīdinājumu, atlasiet **Brīdinājumi**, atlasiet saņemamos brīdinājumus un pēc tam atlasiet **Labi**.

   4. Atlasiet **Labi**. Apstrāde tiks izpildīta ar iestatītajiem parametriem.

4. Atlasiet **Labi**.

## <a name="view-process-results"></a>Skatīt procesa rezultātus

Šajā rakstā ir paskaidrots, kā skatīt piemērotības procesa rezultātus.

1.  Darbvietā **Atvieglojumu pārvaldība** sadaļā **Apstrāde** atlasiet **Procesa rezultāti**.

2.  Lapā **Procesa rezultāti** ir norādīti šādi lauki:

   | Lauks | Apraksts |
   | --- | --- |
   | **Procesa ID** | Unikālais ID darbinieku, juridisko personu un procesa izpildes kombinācijai. |
   | **Procesu tips** | Tas identificē procesu, kas tika palaists. Piemēram: Uzņemšana. |
   | **Laikspiedols** | Laiks, kad tika palaists atbilstības process. |
   | **Juridiska persona** | Juridiskā persona, kas norādīta uzņemšanas procesa laikā. |
   | **Darbinieks** | Darbinieks, kurš tika apstrādāts. |
   | **Plāns | Atvieglojumu plāns, kuram tika mēģināts veikt uzņemšanu. |
   | **Piemērojamības kārtula** | Piemērojamības kārtula, kas tika apstrādāta. Ja radās kļūda, pirms tika palaista piemērojamība, šis lauks būs tukšs. Piemēram, ja darbiniekam nav noteikta kompensācija, piemērojamības process netiks izpildīts, un šis lauks tiks atstāts tukšs. |
   | **Rezultāta statuss** | Tas būs atbilstīgs vai neatbilstīgs. Rezultāta statuss būs neatbilstīgs, ja darbinieks neatbilst piemērojamības nosacījumu kritērijam, ja darbiniekam trūkst nepieciešamās informācijas, piemēram, atalgojuma biežums vai fiksēta kompensācija, vai ja atvieglojumu plānā trūkst informācijas, kas liedz darbiniekiem tikt iesaistītam. |
   | **Rezultāta ziņojums** | Norāda, kāpēc darbiniekam nav tiesību saņemt atvieglojumu plānu vai ja piemērojamības kārtula ir pieņemta. |



[!INCLUDE[footer-include](../includes/footer-banner.md)]
