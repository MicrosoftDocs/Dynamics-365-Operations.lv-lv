---
title: "Samazināšanas principi"
description: "Šajā rakstā ir sniegti piemēri, kas izskaidro, kā iestatīt samazināšanas principu. Šeit iekļauta informācija par dažādiem samazināšanas principa iestatījumiem un to visu rezultātiem. Samazināšanas principu var izmantot, lai noteiktu, kā samazināt budžeta vajadzības."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqPlanSched
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: ce3ff2ac0a5bd9bd342baa05425d7d0957ab8a09
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="reduction-keys"></a>Samazināšanas principi

[!include[banner](../includes/banner.md)]


Šajā rakstā ir sniegti piemēri, kas izskaidro, kā iestatīt samazināšanas principu. Šeit iekļauta informācija par dažādiem samazināšanas principa iestatījumiem un to visu rezultātiem. Samazināšanas principu var izmantot, lai noteiktu, kā samazināt budžeta vajadzības.

<a name="example-1-percent---reduction-key-forecast-reduction-principle"></a>1. piemērs: Procenti — samazināšanas princips prognozes samazināšanai
---------------------------------------------------------------

Šis piemērs parāda, kā samazināšanas princips samazina pieprasījuma apjoma prognozes prasības atbilstoši samazināšanas principa noteiktajiem procentiem un laika periodiem.

1.  Lapā **Samazināšanas principi** iestatiet šādas rindas.
    | Izdodamais atlikums | Vienība  | Procenti |
    |--------|-------|---------|
    | formāts 1. proc.      | Mēnesis | 100     |
    | 2      | Mēnesis | 75      |
    | 3      | Mēnesis | 50      |
    | 4.      | Mēnesis | 25      |

2.  Piesaistiet samazināšanas principu krājuma vajadzību grupai.
3.  Lapas **Vispārējie plāni** laukā **Samazināšanas princips** atlasiet **Procenti — samazināšanas princips**.
4.  Izveidojiet pieprasījuma apjoma prognozi 1000 gabaliem mēnesī.

Sākot budžeta plānošanu 1. janvārī, pieprasījuma apjoma prognozes vajadzības tiek patērētas atbilstoši procentiem, ko iestatāt lapā **Samazināšanas principi**. Uz vispārējo plānu tiek pārsūtīti šādi vajadzību daudzumi.

| Mēnesis                | Vajadzīgo gabalu skaits |
|----------------------|---------------------------|
| janvāris              | 0                         |
| Februārī             | 250                       |
| Martā                | 500                       |
| Aprīlī                | 750                       |
| Maijs – decembris | 1000                     |

## <a name="example-2-transactions--reduction-key-forecast-reduction-principle"></a>2. piemērs. Transakciju samazināšanas principa prognozes samazināšanas princips
Šis piemērs parāda, kā faktiskie pasūtījumi, ko samazināšanas princips noteicis noteiktos periodos, samazina pieprasījuma apjoma prognozes vajadzības.

-   Lapas **Vispārējie plāni** laukā **Samazināšanas princips** atlasiet **Transakcijas — samazināšanas princips**.

Šādi pārdošanas pasūtījumi ir 1. janvārī.

| Mēnesis    | Pasūtīto gabalu skaits |
|----------|--------------------------|
| janvāris  | 956                      |
| Februārī | 1176                    |
| Martā    | 451                      |
| Aprīlī    | 119                      |

Ja izmantojat to pašu pieprasījuma apjoma prognozi 1000 gabaliem mēnesī, uz vispārējo plānu tiek pārsūtīti šādi vajadzību daudzumi.

| Mēnesis                | Vajadzīgo gabalu skaits |
|----------------------|---------------------------|
| janvāris              | 44                        |
| Februārī             | 0                         |
| Martā                | 549                       |
| Aprīlī                | 881                       |
| Maijs – decembris | 1000                     |

## <a name="example-3-transactions--dynamic-period-forecast-reduction-principle"></a>3. piemērs:. Transakciju dinamiskā perioda prognozes samazināšanas princips
Vairāmā gadījumu sistēmas ir iestatītas tā, lai darbības samazina pieprasījuma apjoma prognozi noteiktos prognozes periodos: nedēļās, mēnešus utt. Šie periodi ir definēti samazināšanas principā. Tomēr laiks starp divām pieprasījuma apjoma prognozes rindām var arī *nozīmēt* periodu.

1.  Izveidojiet pieprasījuma apjoma prognozi šādiem datumiem un daudzumiem.
    | Datums       | Pieprasījuma apjoma prognoze |
    |------------|-----------------|
    | 1. janvāris  | 1000           |
    | 5. janvāris  | 500             |
    | 12. janvāris | 1000           |

    Šajā prognozē nav skaidri izteikta perioda starp prognozes datumiem: starp pirmo un otro datumu ir četru dienu ilgs posms, un starp otro un trešo datumu ir septiņu ilgs dienu posms. Šie dažādie posmi ir dinamiskais periods.
2.  Izveidojiet pārdošanas pasūtījuma rindas, kā norādīts tālāk.
    | Datums                             | Pārdošanas pasūtījumu daudzums |
    |----------------------------------|----------------------|
    | Iepriekšējā gada 15. decembris | 500                  |
    | 3. janvāris                        | 100                  |
    | 10. janvāris                       | 200                  |

Prognoze tiks samazināta šādi.

-   Pirmais pārdošanas pasūtījums nav nevienā periodā, tādēļ tas nesamazinās nevienu prognozi.
-   Otrais pārdošanas pasūtījums ir no 1. līdz 5. janvārim, tāpēc prognoze tiks samazināta 1. janvārī par 100.
-   Trešais pārdošanas pasūtījums ir no 5. līdz 12. janvārim, tāpēc prognoze tiks samazināta 5. janvārī par 200.

Lai izpildītu prognozi, tiks izveidots šāds plānotais pasūtījums.

| Pieprasījuma apjoma prognozes datums | Samazināts daudzums |
|----------------------|------------------|
| 1. janvāris            | 900              |
| 5. janvāris            | 300              |
| 12. janvāris           | 1000            |

Kopsavilkums par **Transakcijas — dinamiskais periods** samazinājumu:

-   Prognozes vajadzības samazina faktisko pasūtījumu darbības, kas tiek veiktas dinamiskajā periodā. Dinamiskais periods attiecas uz pašreizējiem prognozes datumiem un beidzas nākamās prognozes sākumā.
-   Šī metode neizmanto un nepieprasa samazināšanas principu.
-   Izmantojot šo opciju, notiek šādas darbības.
    -   Ja prognoze ir pilnībā samazināta, prognozes vajadzības pašreizējai prognozei ir 0 (nulle).
    -   Ja nav nevienas turpmākas prognozes, tiek samazinātas prognozes vajadzības no pēdējās ievadītās prognozes.
    -   Prognozes samazināšanas aprēķinā tiek iekļauti laika periodi.
    -   Prognozes samazināšanas aprēķinā tiek iekļautas dienas(+).
    -   Ja faktiskā pasūtījuma transakcijas pārsniedz prognozes vajadzības, atlikušās transakcijas netiek pārsūtītas uz nākamo prognozes periodu.


<a name="see-also"></a>Skatiet arī
--------

[Vispārējie plāni](master-plans.md)




