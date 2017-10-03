---
title: "Konfigurēt skaidras naudas denomināciju POS vajadzībām"
description: "Skaidras naudas denomināciju banknotēm un monētām var definēt operāciju uzskaites daļā, ko izmanto kasieri, pārdevēji un vadītāji veikalā POS ietvaros."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: d280a11670b5887ae5ae582cedf30c093b4b5d7c
ms.openlocfilehash: 9abcbb706d7120c6bcd91fc759b33cb518802a5b
ms.contentlocale: lv-lv
ms.lasthandoff: 07/27/2017

---

# <a name="configure-cash-denominations-for-pos"></a>Konfigurēt skaidras naudas denomināciju POS vajadzībām

[!include[banner](includes/banner.md)]

Skaidras naudas denomināciju banknotēm un monētām var definēt operāciju uzskaites daļā, ko izmanto kasieri, pārdevēji un vadītāji veikalā POS ietvaros. Šādas denominācijas var izmantot kā palīdzību skaidras naudas skatīšanas procesā dienas beigu uzskaites darījumos vai ātram pārdošanas norēķinam.

## <a name="define-denominations"></a>Denomināciju definēšana
Denominācijas tiek iestatītas katram veikalam lapā **Iestatīšana** > **Skaidras naudas deklarēšana no veikala rekvizīta**. 

![skaidras naudas denominācijas](./media/image1-denomination.png)

Denominācijas definēšana
1. Klikšķiniet **Jauns**.
1. Norādiet tipu (monēta vai banknote).
1. Norādiet summu (vērtība).

![skaidras naudas denominācijas](./media/image2-denomination.png)

## <a name="configure-the-functionality-profile"></a>Funkcionalitātes profila konfigurēšana
Maksājot skaidrā naudā POS, lietotājs var izmantot banknotes denominācijas, lai ātri ievadītu klienta samaksāto summu. Funkcionalitātes profilā varat konfigurēt divas opcijas denominācijas rādīšanai POS.

**Lielāks vai vienāds ar summu apmaksai**: pēc noklusējuma POS parāda tikai tādu banknošu denominācijas, kas ir lielākas par summu apmaksai, ļaujot norēķināties ar vienu pieskārienu. Piemēram, ja summa apmaksai ir 7,50 USD, POS tiek rādītas šādas denominācijas: 10 USD, 20 USD, 50 USD un 100 USD. Pieskaroties kādai no šīm summām, automātiski tiek veikti norēķini par šo summu. 1 USD un 5 USD banknotes netiek rādītas, jo šīs summas ir mazākas par summu apmaksai.

**Visas denominācijas**: atlasiet šo opciju, lai POS vienmēr rādītu visas denominācijas neatkarīgi no summas apmaksai. Tas nozīmē, ka lietotājs var izmantot banknošu kombinācijas, lai sasniegtu summu apmaksai. Piemēram, ja summa apmaksai ir 25,00 USD, lietotājs var izvēlēties 20 USD un 5 USD banknotes apmaksas pabeigšanai.

