---
title: "PVN maksājumi un noapaļošanas kārtulas"
description: "Šajā rakstā ir izskaidrots, kā iestatīt noapaļošanas kārtulu PVN iestādēm paredzētās atskaitēs, un sniegta informācija par PVN bilances noapaļošanu nosegšanas un PVN iegrāmatošanas darba laikā."
author: twheeloc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 13470282efc6b9135e86355cf8071b841aad3071
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="sales-tax-payments-and-rounding-rules"></a>PVN maksājumi un noapaļošanas kārtulas

[!include[banner](../includes/banner.md)]


Šajā rakstā ir izskaidrots, kā iestatīt noapaļošanas kārtulu PVN iestādēm paredzētās atskaitēs, un sniegta informācija par PVN bilances noapaļošanu nosegšanas un PVN iegrāmatošanas darba laikā.

Periodiski ir jāziņo par PVN un tas ir jāsamaksā nodokļu iestādēm. To var izdarīt, lapa PVN palaižot procesu Nosegt un grāmatot PVN. Noteikta perioda PVN tiek nosegts no PVN kontiem, un PVN apmaksas kontā tiek grāmatota PVN bilance. PVN apmaksas kontā grāmatoto PVN bilanci var noapaļot atbilstoši nodokļu iestāžu prasībām, iestatot noapaļošanas kārtulu lapā PVN. 

Noapaļošanas starpība tiek grāmatota PVN noapaļošanas kontā, kas ir atlasīts virsgrāmatas laukā Automātisko darījumu konti.

Tālāk sniegtajā piemērā ir attēlots, kā darbojas noapaļošanas kārtula nodokļu iestādei.

### <a name="example"></a>Piemērs:

Kopējā PVN summa par periodu atbilst kredīta bilancei –98 765,43. Juridiskā persona ir saņēmusi lielāku PVN summu, nekā tā ir samaksājusi. Tāpēc juridiskā persona ir parādā nodokļu iestādei. 

Juridiskā persona vēlas izmantot noapaļošanas metodi, kas noapaļo bilanci līdz tuvākajam veselam skaitlim (1,00). Lietotājs, kurš ir atbildīgs par PVN uzskaiti, veic tālāk norādītās darbības.

1.  Noklikšķiniet uz Nodokļi &gt; Netiešie nodokļi &gt; PVN &gt; Nodokļu iestādes.
2.  Kopsavilkuma cilnes Vispārīgi laukā Noapaļošanas veids atlasiet opciju Parastais.
3.  Laukā Noapaļošana ievadiet vērtību 1,00.
4.  Kad ir pienācis laiks maksāt PVN nodokļu iestādei, atveriet lapu Nosegt un grāmatot PVN. (Noklikšķiniet uz Nodokļi &gt; Deklarācijas &gt; PVN &gt; Nosegt un grāmatot PVN.)
5.  PVN apmaksas kontā nodokļu parāda suma 98 765,43 tiek noapaļota līdz 98 765.

Tālāk esošajā tabulā ir parādīts, kā summa 98 765,43 tiek noapaļota, izmantojot katru noapaļošanas metodi, kas ir pieejama lapas Nodokļu iestādes laukā Noapaļošanas veids.

| Noapaļošanas veida opcija                | Noapaļošanas vērtība = 0,01 | Noapaļošanas vērtība = 0,10 | Noapaļošanas vērtība = 1,00 | Noapaļošanas vērtība = 100,00 |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| Parastais                              | 98 765,43              | 98 765,40              | 98 765,00              | 98 800,00                |
| Uz zemāku                            | 98 765,43              | 98 765,40              | 98 765,00              | 98 700,00                |
| Noapaļošana                         | 98 765,43              | 98 765,50              | 98 766,00              | 98 800,00                |
| Pašu priekšrocība kredīta bilancei | 98 765,43              | 98 765,40              | 98 765,00              | 98 700,00                |
| Pašu priekšrocība debeta bilancei  | 98 765,43              | 98 765,50              | 98 766,00              | 98 800,00                |

> [!NOTE]                                                                                  
> Ja atlasāt opciju Pašu priekšrocība, noapaļošana vienmēr tiek veikta atbilstoši juridiskās personas interesēm. 

Lai iegūtu papildu informāciju, skatiet šādas tēmas:
- [PVN apskats](indirect-taxes-overview.md)
- [PVN maksājuma izveide](tasks/create-sales-tax-payment.md)
- [Izveidot PVN transakcijas dokumentos](tasks/create-sales-tax-transactions-documents.md)
- [Grāmatoto PVN darījumu skatīšana](tasks/view-posted-sales-tax-transactions.md)



