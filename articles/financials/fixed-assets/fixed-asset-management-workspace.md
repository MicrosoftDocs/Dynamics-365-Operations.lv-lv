---
title: "Pamatlīdzekļu pārvaldības darbvieta"
description: "Šajā tēmā ir sniegta informācija par darbvietu Pamatlīdzekļu pārvaldība. Šajā darbvietā tiek radīta informācija, kas attiecas uz sistēmā ievadītajiem pamatlīdzekļiem. Tā ietver kopsavilkuma skatu un analīzes skatu."
author: saraschi2
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.assetid: 
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c544ae60433dd14d061bc1a78d5cad6577cf579d
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="fixed-asset-management-workspace"></a>Pamatlīdzekļu pārvaldības darbvieta

[!include[banner](../includes/banner.md)]

Darbvietā **Pamatlīdzekļu pārvaldība** tiek radīta informācija, kas attiecas uz sistēmā ievadītajiem pamatlīdzekļiem. Šajā darbvietā ir ietverts kopsavilkuma skats analīzes skats. Cilnē **Mans darbs** tiek rādīti kopsavilkuma elementi, detalizēta informācija par pamatlīdzekli un saistīta informācija par pamatlīdzekļiem pašreizējā uzņēmumā. Power BI analīzes sadaļai tieši darbvietā varat pievienot arī analīzes iespējas. Cilnē **Analīze – visi uzņēmumi** izmanto Microsoft Power BI iespējas, lai rādītu ar pamatlīdzekļiem visos uzņēmumos saistīto vizuālo informāciju.

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

