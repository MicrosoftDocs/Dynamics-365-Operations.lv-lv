---
title: Izmaksu objekti
description: "Šajā rakstā ir sniegta informācija par izmaksu objektiem un paskaidrots, kā tiek uzkrātas izmaksas un daudzumi. Izmaksu objekts ir elements, kam ir uzkrātas izmaksas un daudzumi. Izmaksu objekta elements var būt prece vai preces varianti, piemēram, stila un krāsas varianti."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c818bfac6645b71bcc8b2249534aa80907786651
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="cost-objects"></a>Izmaksu objekti

[!include[banner](../includes/banner.md)]


Šajā rakstā ir sniegta informācija par izmaksu objektiem un paskaidrots, kā tiek uzkrātas izmaksas un daudzumi. Izmaksu objekts ir elements, kam ir uzkrātas izmaksas un daudzumi. Izmaksu objekta elements var būt prece vai preces varianti, piemēram, stila un krāsas varianti.  

<a name="cost-objects"></a>Izmaksu objekti
------------

Sarakstā **Izmaksu objekti** ir parādīts saraksts ar visiem izmaksu objektiem, kas ir reģistrēti precei. Izmaksu objektus nosaka dati no šādiem avotiem:

-   Produkts
-   Preces dimensijas grupa
-   Noliktavas dimensiju grupa
-   Izsekošanas dimensijas grupa

**Piezīme.** Izmaksu objekts norāda tikai tādu izmaksu elementu, kura tips ir **Tiešie materiāli**. Izmaksu objekts atšķiras no krājumu objekta ar to, kā izmaksu objektu nosaka krājumu dimensijas, kas atlasītas finanšu krājumiem. Piemēram, krājumam ir šāda konfigurācija:

-   **Vieta:** Fiziskie krājumi = Jā, Finanšu krājumi = Jā
-   **Noliktava:** Fiziskie krājumi = Jā, Finanšu krājumi = Nē
-   **Partijas Nr.:** Fiziskie krājumi = Jā, Finanšu krājumi = Nē

Šajā tabulā ir parādīts, kas ir izmaksu objekts un kas ir krājumu objekts.

| Objekta veids      | Krājuma kods | Vieta | Noliktava | Paketes Nr. |
|------------------|-------------|------|-----------|-----------|
| Izmaksu objekts      | x           | x    |           |           |
| Krājumu objekts | x           | x    |  x        | x         |

## <a name="accumulation-of-costs-and-quantities"></a>Izmaksu un daudzumu uzkrāšana
-   Vērtība laukā **Vērtība** ir šādu vērtību summa:
    -   Fiziskā izmaksu summa
    -   Beigu izmaksu summa
    -   Korekcijas
-   Vērtība laukā **Daudzums** ir šādu vērtību summa:
    -   Saņemts
    -   Atskaitīts
    -   Grāmatotais daudzums
-   Vērtība laukā **Vidējās vienības izmaksas** tiek aprēķināta. Vērtība tiek aprēķināta, dalot vērtību laukā **Vērtība** ar vērtību laukā **Daudzums**.

**Piezīme.** Parametrs **Iekļaut fizisko vērtību** neietekmē iepriekšējos aprēķinus.

<a name="see-also"></a>Skatiet arī
--------

[Preces dimensiju grupa](https://technet.microsoft.com/en-us/library/aa499382.aspx)

[Noliktavas dimensiju grupa](https://technet.microsoft.com/en-us/library/hh209317.aspx)

[Izsekošanas dimensiju grupa](https://technet.microsoft.com/en-us/library/hh209465.aspx)

[Jaunumi un izmaiņas programmā Microsoft Dynamics AX](/dynamics365/operations/dev-itpro/get-started/whats-new-changed)

[Izmaksu ieraksti](cost-entries.md)




