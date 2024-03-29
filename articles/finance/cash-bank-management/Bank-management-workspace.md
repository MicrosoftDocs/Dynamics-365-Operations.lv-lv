---
title: Bankas pārvaldības darbvieta
description: Šajā rakstā ir sniegta informācija par bankas pārvaldības darbalauku. Šī darbvieta rāda informāciju, kas saistīta ar uzņēmuma bankas kontiem.
author: angelad116
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: f9880928281e704edcd24a75f99d4562761b7c82
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151557"
---
# <a name="bank-management-workspace"></a>Bankas pārvaldības darbvieta

[!include [banner](../includes/banner.md)]

Darbvietā **Banku vadība** tiek rādīta informācija, kas ir saistīta ar uzņēmuma bankas kontiem. Darbvietā ir ietverts skats **Kopsavilkums** un lapa **Analīze**. Skatā **Kopsavilkums** tiek rādīti kopsavilkuma elementi, bankas konta informācija, bilances diagramma un saistītā informācija. Lapā **Analītika** tiek izmantotas Microsoft Power BI iespējas, lai rādītu vizuālos elementus, kuri ir saistīti ar bankas konta bilanci.

## <a name="summary-view"></a>Skats Kopsavilkums

### <a name="summary"></a>Kopsavilkums

Sadaļā **Kopsavilkums** esošie elementi sniedz pārskatu par jūsu bankas kontiem un nodrošina ātru piekļuvi lapām, kas jums ir visbiežāk jāizmanto. Bankas darbību saskaņošanas informācija ir specifiska detalizētās bankas darbību saskaņošanas funkcionalitātei. Ir ietverta informācija tikai par tiem bankas kontiem, kuriem lapā **Bankas konts** ir iestatīta opcijas **Detalizēta bankas darbību saskaņošana** vērtība **Jā**. Sadaļā **Kopsavilkums** varat importēt visu juridisko personu bankas kontu elektroniskos bankas failus.

### <a name="bank-accounts"></a>Bankas konti

Katram juridiskās personas bankas kontam atbilst kartiņa sadaļā **Bankas konti**. Tiek rādīta pašreizējā bilance, un varat skatīt detalizētu informāciju par transakcijām, kas veido šo bilances kopsummu. Arī lauks **Pagaidu darbības** sniedz iespēju skatīt detalizētu informāciju par transakcijām, kas veido šo kopsummu. Pagaidu darbības ir jebkuras nepabeigtās transakcijas, kas ir grāmatotas, izmantojot pagaidu funkcionalitāti, taču vēl nav dzēstas. Laukā **Nenoslēgta bilance** norādītā summa ir pašreizējās bilances un pagaidu jeb neizpildīto transakciju summas starpība.

Kartē tiek rādīts arī bankas konta pēdējās saskaņošanas laiks. Šī informācija tiek rādīta tikai tad, ja bankas kontam ir iespējota opcija Detalizēta bankas darbību saskaņošana.

### <a name="balance"></a>Bilance

Diagrammā **Bilance** tiek rādīta vēsturiskā informācija par sadaļā **Bankas konti** atlasītā bankas konta bilanci vai vēsturiskās informācijas kopsavilkums par visu juridiskās personas bankas kontu bilanci. Šī informācija ir pieejama par dažādiem periodiem: pašreizējo nedēļu, pašreizējo mēnesi, pašreizējo gadu, pagājušajiem pieciem gadiem un visiem periodiem (pilna bankas konta vēsture). 

Ja skatāt atsevišķa bankas konta diagrammu **Bilance**, vēsturiskā informācija par bilancēm tiek rādīta bankas konta valūtā. Ja skatāt visu juridiskās personas bankas kontu diagrammu, vēsturiskā informācija par bilancēm tiek rādīta uzskaites valūtā.

Diagrammas augšpusē tiek rādīta informācija par datu pēdējās atjaunināšanas laiku. Varat atjaunināt datus pēc nepieciešamības.

### <a name="related-information"></a>Saistītā informācija

Sadaļā **Saistītā informācija** varat atvērt lapu **Virsgrāmatas žurnāls**, lai pabeigtu bankas pārskaitījumus. Varat arī ātri atvērt lapas **Bankas darbības** un **Pagaidu darbības**.

## <a name="analytics-view"></a>Skats Analīze

Lapā **Analīze** ir sniegti svarīgi rādītāji par pašreizējā uzņēmuma bankas kontiem. Lapā ir pieejamas tālāk norādītās vizualizācijas.

-   Kopējā bankas bilance sistēmas valūtā
-   Bilance pēc juridiskās personas
-   Šodienas faktiskās un prognozētās bilances salīdzinājums bankas konta valūtā
-   Bilance pēc bankas konta
-   Bilance pēc valūtas

Darbvietā **Naudas pārskats — visi uzņēmumi** varat skatīt bankas informācijas analīzi par visiem uzņēmumiem. Plašāku informāciju skatiet sadaļā [Skaidras naudas pārskata Power BI saturs](Cash-Overview-Power-BI-content.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
