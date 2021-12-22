---
title: Konfigurēt darbinieku pašapkalpošanos
description: Microsoft Dynamics 365 Human Resources varat konfigurēt darbinieku patstāvīgi izmantojamā pakalpojuma augšējā līmeņa navigācijas elementus.
author: twheeloc
ms.date: 12/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1e0c59eb8db5a97405e87922cc65f3eb74bee48e
ms.sourcegitcommit: b101c21f972fdad2667431f712222e040cd69d43
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/07/2021
ms.locfileid: "7898444"
---
# <a name="configure-employee-self-service"></a>Konfigurēt darbinieku patstāvīgi izmantojamo pakalpojumu

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources varat konfigurēt **Darbinieku patstāvīgi izmantojamā pakalpojuma** augšējā līmeņa navigācijas elementus. Atvieglojumu plāna elementi novirza lietotājus uz atvieglojumu plāniem, kuros tie ir tiesīgi reģistrēties.

## <a name="set-up-a-benefit-plans-tile"></a>Atvieglojumu plānu elementa iestatīšana

1. Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Darbinieku patstāvīgi izmantojamā pakalpojuma parametri**.

2. Atlasiet cilni **Atvieglojumu plānu elementa iestatīšana** un pēc tam atlasiet **Jauns**.

3. Norādiet vērtības tālāk minētajos laukos.

   | Lauks | Apraksts |
   | --- | --- |
   | **Plāna veida kods** | Plāna tips, kas tiek parādīts, ja šis elements ir atlasīts **opcijā Benefits pašapkalpošanās**. |
   | **Elementa ID** | Elementa unikālais identifikators. |
   | **Elementa etiķetes teksts** | Teksts, kas tiks parādīts elementam **Benefits pašapkalpošanās**. |
   | **Apraksts** | Elementa apraksts. |
   | **Elementa fona attēls** | Elementam izmantojamā attēla URL (nav obligāts). |
   | **Izsekot atvērto reģistrāciju** | Atlasiet šo opciju, lai izsekotu atvērtās reģistrācijas norisi šim plāna tipam. Piemēram, jums var būt izveidoti plāni, kur **plāna tips = Citi**. Šie plāni var būt izvēles plāni, kuriem nevēlaties izsekot reģistrācijas progresu. Ja neatlasīsit šo plāna tipu, šāda tipa plāns tiks ignorēts, izsekojot reģistrācijas norisi vai reģistrācijas pabeigšanu **cilnē Atvērta** reģistrācija. Šis iestatījums attiecas uz plāna tipu, kas atlasīts visiem periodiem un juridiskām personām. |

4. Atlasiet **Saglabāt**.

## <a name="set-up-a-flex-credit-plan-tile"></a>Brīvā režīma kredīta plāna elementa iestatīšana

1. Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Darbinieku patstāvīgi izmantojamā pakalpojuma parametri**.

2. Atlasiet cilni **Brīvā režīma kredīta plāna elementa iestatīšana** un pēc tam atlasiet **Jauns**.

3. Norādiet vērtības tālāk minētajos laukos.

   | Lauks | Apraksts |
   | --- | --- |
   | **Atvieglojumu kredīta ID** | Brīvā režīma kredīta programmu plāni, kas tiks parādīti, kad šis elements ir atlasīts **opciju pašapkalpošanās programmā Priekšrocības**. |
   | **Elementa ID** | Elementa unikālais identifikators. |
   | **Elementa etiķetes teksts** | Teksts, kas tiks parādīts elementam **Benefits pašapkalpošanās**. |
   | **Apraksts** | Elementa apraksts. |
   | **Elementa fona attēls** | Elementam izmantojamā attēla URL (nav obligāts). |
   | **Izsekot atvērto reģistrāciju** | Atlasiet šo opciju, lai izsekotu atvērtās reģistrācijas norisi šim plāna tipam. Piemēram, jums var būt izveidoti plāni, kur **plāna tips = Citi**. Šie plāni var būt izvēles plāni, kuriem nevēlaties izsekot reģistrācijas progresu. Ja neatlasīsit šo plāna tipu, šāda tipa plāns tiks ignorēts, izsekojot reģistrācijas norisi vai reģistrācijas pabeigšanu **cilnē Atvērta** reģistrācija. Šis iestatījums attiecas uz plāna tipu, kas atlasīts visiem periodiem un juridiskām personām. |

4. Atlasiet **Saglabāt**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
