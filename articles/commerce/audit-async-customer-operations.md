---
title: Audita sinhronizācija debitoru operācijām galvenajā birojā
description: Šajā rakstā ir izskaidrots, kā pārbaudīt debitora operāciju sinhronizāciju galvenajā Microsoft Dynamics 365 Commerce birojā, lai palīdzētu novērst jebkuras vietas lietotāja problēmas.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-09-28
ms.openlocfilehash: c615b0b436e01a1423b5611a72f0056b5b14f8e8
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690963"
---
# <a name="audit-synchronization-of-customer-operations-in-headquarters"></a>Audita sinhronizācija debitoru operācijām galvenajā birojā

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šajā rakstā ir izskaidrots, kā pārbaudīt debitora operāciju sinhronizāciju galvenajā Microsoft Dynamics 365 Commerce birojā, lai palīdzētu novērst jebkuras vietas lietotāja problēmas.

Kad organizācijas sāk pieņemt spēju radīt un rediģēt klientus asinhroni, vietas administratoriem ir nepieciešams veids, kā skatīt un novērst darbību problēmu, balstoties uz vietas lietotāja pieprasījumiem vai procesa kļūmēm. Šajos scenārijos vietu administratoriem vajadzētu būt iespējai auditēt debitoru izveidi un rediģēt darbības un labot visas kļūmes, izmantojot pašapkalpošanās modeli.

## <a name="customer-synchronization-status"></a>Debitora sinhronizācijas statuss

Izvēloties asinhrono debitoru pārvaldības režīmu un ar to korespondējošajiem līdzekļiem, Commerce Headquarters **administratoriem ir jāizveido un jāplāno periodisks pakešuzdevums P darbam**, **sinhronizēt debitorus un biznesa partnerus no asinhronā** režīma darba, kā arī 1010 darbs, **lai visi async debitori** tiktu konvertēti uz sinhronizētu debitorus programmā Commerce Headquarters. Debitoru pārvaldības operāciju sinhronizācija notiek vienmēr, kad šie darbi tiek palaisti. Papildinformāciju skatiet asinhronajā [debitoru izveides režīmā](async-customer-mode.md).

Kā uzņēmuma īpašnieks varat veikt šādas darbības:

- Apskatiet visas vietas lietotāju izveides/rediģēšanas operācijas. Detalizēti tiek iekļauts laikspiedols un statuss.
- Filtrējiet operācijas, izmantojot jebkuru no debitora tabulas laukiem un vērtībām, lai sašaurinātu audita žurnālu.
- Apskatiet īsus aprakstus par izmaiņām kopā ar statusa informāciju, lai saprastu operācijas augstākā līmenī.
- Neveiksmēm, rediģējiet un labojiet problemātiskos laukus un pēc tam saglabājiet un sinhronizējiet noteiktas debitora operācijas.

### <a name="elements-on-the-customer-synchronization-status-page"></a>Debitoru sinhronizācijas statusa lapas elementi

Lai skatītu visu sinhronizācijas operāciju sarakstu, programmā Commerce headquarters tiek atvērts statuss **Commerce and Retail \> Customers \> Customer synchronization**. Šajā attēlā parādīts debitoru sinhronizācijas **statusa lapas** piemērs.

![Debitoru sinhronizācijas statusa lapa programmā Commerce Headquarters.](media/D365-Commerce-Customer-Mgmt-Audi-Async-Operations.png)

Pēc noklusējuma debitoru sinhronizācijas operāciju saraksts debitoru sinhronizācijas statusa lapas kreisajā **pusē ietver** šādas kolonnas:

- Kanāla nosaukums
- Debitora konts
- Asinhrons debitora konts
- Operāciju laikspiedols
- Debitora sinhronizācijas statuss

Lapas augšējā labajā pusē ir redzama detalizēta informācija par debitora kontu, piemēram, **debitora** konts, **mazumtirdzniecības async** operācija, **debitora sinhronizācijas statuss** **un pēdējās zināmās kļūdas** vērtības.

Sadaļā **Mainīt aprakstu** ir ietverts neizpildīto debitoru pārvaldības operācijas tipa apraksts (piemēram, debitora izveide, konta atjaunināšana vai sinhronizācijas kļūme ar detalizētu informāciju).

Sadaļā **Debitora atribūti ir** režģis, kurā parādīti visi debitora atribūti kopā ar vecajām un jaunajām vērtībām. Šo sadaļu var rediģēt, ja vēlaties mainīt debitora atribūtu vērtības, lai novērstu kļūdas, un pēc tam sinhronizēt vēlreiz.
