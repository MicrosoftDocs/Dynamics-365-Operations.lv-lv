---
title: Brīvā režīma kredīta programmu iestatīšana
description: Varat izmantot brīvā režīma kredīta programmas Microsoft Dynamics 365 Human Resources, lai reģistrētu darbiniekus atvieglojumos atbilstoši iepriekš noteiktam brīvā režīma kredītu skaitam.
author: twheeloc
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitCreditPrograms, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ff3bd2c4d39a4411b5a5cb82e4281ff4af98ff0d
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337298"
---
# <a name="set-up-flex-credit-programs"></a>Brīvā režīma kredīta programmu iestatīšana

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Varat izmantot brīvā režīma kredīta programmas Microsoft Dynamics 365 Human Resources, lai reģistrētu darbiniekus atvieglojumos atbilstoši iepriekš noteiktam brīvā režīma kredītu skaitam. Darbinieki var izvēlēties, kā sadalīt savus brīvā režīma kredītus. Piemēram, ja darbinieks ir apdrošināts sava dzīvesbiedra veselības apdrošināšanas plānā, viņš var vēlēties izmantot citiem atvieglojumiem kredītus, ko citādi izmantotu veselības apdrošināšanai. 

1. Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Plāni** atlasiet **Brīvā režīma kredīta programmas**.

2. Atlasiet **Jauns**.

3. Norādiet vērtības tālāk minētajos laukos.

   | Lauks | Apraksts |
   | --- | --- |
   | **Atvieglojumu kredīta ID** | Brīvā režīma kredīta programmas unikālais identifikators. |
   | **Apraksts** | Brīvā režīma kredīta programmas apraksts. | 
   | **No datuma** | Datums, kad brīvā režīma kredīta programma kļūst aktīva. |
   | **Līdz datumam** | Datums, kad brīvā režīma kredīta programma beidz darboties. Varat atstāt noklusēto vērtību (12/31/2154), lai norādītu, ka brīvā režīma kredīta programmai nav ieplānota beigu termiņa. |
   | **Kopējā kredīta vērtība** | Kredītpunktu skaits, kas katram darbiniekam jāizmanto saviem atvieglojumiem. |
   | **Proporcionālas sadalīšanas kārtula** | Kārtula, ko izmanto, lai proporcionāli sadalītu brīvā režīma kredītus, ja darbinieks tiek nolīgts brīvā režīma kredīta perioda vidū. </br></br><ul><li>**Nav** — darbinieks nesaņem brīvā režīma kredītus, ja tas tiek pieņemti darbā pēc brīvā režīma kredīta programmas perioda sākuma.</li><li>**Pilns kredīts** — darbinieks saņem pilnu brīvā režīma kredītu summu, neatkarīgi no tā, kad tiek pieņemts darbā.</li><li>**Proporcionāla sadale** — darbinieks saņem proporcionālu brīvā režīma kredītu summu, pamatojoties uz pieņemšanas datumu.</li></ul> |
   | **Brīvā režīma kredīta proporcionālas sadales formula** | Kārtula, ko izmanto, lai proporcionāli sadalītu brīvā režīma kredītus darbiniekiem, kuri pieņemti darbā brīvā režīma kredīta atvieglojumu perioda vidū. Šīs proporcijas pamatā ir nodarbinātības sākuma datums. Šis lauks tiek izmantots tikai tad, ja laukā **Proporcionālās sadalīšanas kārtula** atlasāt **Proporcionāli sadalīt**. </br></br><ul><li>**Katru dienu** — proporcionāli sadala brīvā režīma kredītu skaitu, ko darbinieks saņem katru dienu. Kopējais brīvā režīma kredītu skaits tiek dalīts ar dienu skaitu periodā. Piemēram, ja atvieglojumu periods ir 400 dienas, sistēma kopējo brīvā režīma kredītu skaitu izdalīs ar 400, lai aprēķinātu brīvā režīma kredītpunktu skaitu, ko darbinieki saņems katru dienu.</li><li>**Pašreizējā mēnesī** — proporcionāli sadala brīvā režīma kredītu skaitu, ko darbinieks saņem katru mēnesi, noapaļojot līdz pašreizējam mēnesim. Kopējais brīvā režīma kredītu skaits tiek dalīts ar mēnešu skaitu periodā. Piemēram, ja atvieglojumu periods ir 15 mēneši, sistēma kopējo brīvā režīma kredītu skaitu izdalīs ar 15, lai aprēķinātu brīvā režīma kredītpunktu skaitu, ko darbinieki saņems katru mēnesi.</li><li>**Nākamajā mēnesī** — proporcionāli sadala brīvā režīma kredītu skaitu, ko darbinieks saņem katru mēnesi, noapaļojot līdz nākamajam mēnesim. Kopējais brīvā režīma kredītu skaits tiek dalīts ar mēnešu skaitu periodā. Piemēram, ja atvieglojumu periods ir 15 mēneši, sistēma kopējo brīvā režīma kredītu skaitu izdala ar 15, lai aprēķinātu brīvā režīma kredītpunktu skaitu, ko darbinieki saņems katru mēnesi.</li></ul> |
   


[!INCLUDE[footer-include](../includes/footer-banner.md)]
