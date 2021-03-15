---
title: Pamatlīdzekļu pārvaldības darbvieta
description: Šajā tēmā ir sniegta informācija par darbvietu Pamatlīdzekļu pārvaldība. Šajā darbvietā tiek radīta informācija, kas attiecas uz sistēmā ievadītajiem pamatlīdzekļiem. Tā ietver kopsavilkuma skatu un analīzes skatu.
author: saraschi2
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetWorkspace
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 5822b3413a6fa4b6044a97ec320521b4d7206bad
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988981"
---
# <a name="fixed-asset-management-workspace"></a>Pamatlīdzekļu pārvaldības darbvieta

[!include [banner](../includes/banner.md)]

Darbvietā **Pamatlīdzekļu pārvaldība** tiek radīta informācija, kas attiecas uz sistēmā ievadītajiem pamatlīdzekļiem. Šajā darbvietā ir ietverts kopsavilkuma skats analīzes skats. Cilnē **Mans darbs** tiek rādīti kopsavilkuma elementi, detalizēta informācija par pamatlīdzekli un saistīta informācija par pamatlīdzekļiem pašreizējā uzņēmumā. Varat arī tiešā vieda darbvietā pievienot analīzes iespējas Power BI analīzes sadaļai. Cilnē **Analīze — visi uzņēmumi** tiek izmantotas Microsoft Power BI iespējas, lai parādītu vizuālo informāciju, kas ir saistīta ar pamatlīdzekļiem visos uzņēmumos.

## <a name="my-work"></a>Mans darbs

### <a name="summary"></a>Kopsavilkums

Elementi sadaļā **Kopsavilkums** sniedz apskatu par jūsu pamatlīdzekļiem. Informācijā ir ietverti rādītāji par līdzekļiem, kas vēl nav iegūti, par līdzekļiem, kas ir iegūti pašreizējā gada laikā, un par līdzekļiem, kas pašreizējā gada laikā ir norakstīti. Sadaļā **Kopsavilkums** ir arī ātra navigācija uz saraksta lapu **Pamatlīdzeklis**, pakešveida nolietojuma priekšlikumu un pamatlīdzekļu žurnālu.

### <a name="find-fixed-assets"></a>Atrast pamatlīdzekļus

Sadaļā **Atrast pamatlīdzekļus** līdzekļus varat ātri meklēt, norādot pamatlīdzekļa numuru, grupu, nosaukumu, novietojumu vai atbildīgo personu. Sarakstā tiek parādīti visi līdzekļi, kas atbilst meklēšanas kritērijiem.

No saraksta var skatīt tālāk norādītās lapas.

 - Lapa **Detalizēta informācija** par attiecīgo pamatlīdzekli
 - Lapa **Grāmatas** visām grāmatām, kas ir saistītas ar šo pamatlīdzekli
 - Lapa **Pamatlīdzekļu novērtējumi**

### <a name="valuations"></a>Novērtējumi

Lapā **Pamatlīdzekļu novērtējumi** varat vienā lapā skatīt vissvarīgāko informāciju par kādu pamatlīdzekli, kā arī detalizētu informāciju par visām grāmatām, kas ir saistītas ar šo pamatlīdzekli. Opcija **Bilances** lapas kreisajā augšējā pusē parāda pašreizējo novērtējumu par katru ar šo pamatlīdzekli saistīto grāmatu. No šīm vērtībām varat atpakaļgaitā detalizēti pētīt, lai redzētu detalizētu informāciju par transakcijām, kas veido šo kopsavilkuma vērtību. Opcija **Profils** lapas kreisajā augšējā pusē parāda nolietojuma grafiku katrai ar šo pamatlīdzekli saistītajai grāmatai.

Lapai **Pamatlīdzekļu novērtējumi** varat piekļūt no darbvietas **Pamatlīdzekļu pārvaldība** vai lapas **Pamatlīdzeklis**.

### <a name="related-information"></a>Saistītā informācija

Izmantojot saites darbvietas sadaļā **Saistītā informācija**, varat pāriet tieši uz lapu **Grāmatu iestatīšana**, uz lapu **Pamatlīdzekļu transakciju uzziņas** un uz vairākiem pārskatiem.

### <a name="analytics--all-companies"></a>Analīze – visi uzņēmumi

Lapā **Analīze** ir sniegti svarīgi rādītāji par pamatlīdzekļiem visās sistēmā ietvertajās juridiskajās personās. Piekļuvi šai cilnei regulē drošības privilēģijas Skatīt pamatlīdzekļu analīzi visiem uzņēmumiem.

Nākamajā tabulā ir redzama katrā pārskata lapā pieejamā vizuālā informācija.

| Pārskata lapa            | Vizualizēšana        |
|------------------------|----------------------|
| Pamatlīdzekļu novērtējumi | Kopējā atlikusī vērtība |
| Pamatlīdzekļu novērtējumi | Atlikušās vērtības pēc pamatlīdzekļu grupas |
| Pamatlīdzekļu novērtējumi | Iegādes vērtības |
| Pamatlīdzekļu novērtējumi | Norakstīšanas vērtības |
| Pamatlīdzekļu novērtējumi | Pamatlīdzekļu detalizēta informācija |
| Novērtējumu kartes        | Kopējā atlikusī vērtība |
| Novērtējumu kartes        | Pamatlīdzekļu novietojumi |
| Novērtējumu kartes        | Pamatlīdzekļu detalizēta informācija |

Lai skatītu analīzi ar datiem, vispirms ir jāatsvaidzina apkopošanas mērījums AssetTransactionMeasure lapā **Elementu krātuve**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]