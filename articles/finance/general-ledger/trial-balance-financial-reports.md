---
title: Apgrozījuma bilances finanšu pārskati
description: Šajā rakstā ir aprakstīti noklusējuma pārskati apgrozījuma bilancēm. Tajā ir aprakstīti arī ar šiem pārskatiem saistītie veidošanas bloki un veids, kā šos pārskatus varat modificēt, lai tie atbilstu jūsu biznesa prasībām.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1b48510febf5a5f9f4a01728b242d9750b3c62c2
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771732"
---
# <a name="trial-balance-financial-reports"></a>Apgrozījuma bilances finanšu pārskati

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīti noklusējuma pārskati apgrozījuma bilancēm. Tajā ir aprakstīti arī ar šiem pārskatiem saistītie veidošanas bloki un veids, kā šos pārskatus varat modificēt, lai tie atbilstu jūsu biznesa prasībām. 

<a name="default-trial-balance-reports"></a>Noklusējuma apgrozījuma bilances pārskati
-----------------------------

Finanšu pārskatu veidošanas vidē pieejami trīs apgrozījuma bilances pārskati.

| Noklusējuma pārskats                                 | Ko tā dara                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Detalizēta apgrozījuma bilance — noklusējums               | Sniedz informāciju par bilanci visiem kontiem un iekļauj debeta un kredīta bilances, kā arī šo bilanču neto summu kopā ar transakcijas datumu, dokumentu un žurnāla aprakstu.                  |
| Kopsavilkuma apgrozījuma bilance — noklusējums                | Sniedz bilances informāciju visiem kontiem un iekļauj sākuma un beigu bilances, kā arī debeta un kredīta bilances kopā ar to neto starpību.                                        |
| Kopsavilkuma apgrozījuma bilance gadu gaitā — noklusējums | Sniedz bilances informāciju visiem kontiem, un iekļauj sākuma un beigu bilances, kā arī debeta un kredīta bilances kopā ar to neto starpību attiecībā uz pašreizējo gadu un iepriekšējo gadu. |

## <a name="building-blocks"></a>Veidošanas bloki
Apgrozījuma bilances finanšu pārskati izmanto tālāk aprakstītos veidošanas blokus.

| Noklusējuma atskaite                                 | Rindas definīcija          | Kolonnas definīcija                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| Detalizēta apgrozījuma bilance — noklusējums               | Apgrozījuma bilance — noklusējums | Detalizēta apgrozījuma bilance — noklusējums               |
| Kopsavilkuma apgrozījuma bilance — noklusējums                | Apgrozījuma bilance — noklusējums | Kopsavilkuma apgrozījuma bilance — noklusējums                |
| Kopsavilkuma apgrozījuma bilance gadu gaitā — noklusējums | Apgrozījuma bilance — noklusējums | Kopsavilkuma apgrozījuma bilance gadu gaitā — noklusējums |

### <a name="row-definition"></a>Rindas definīcija

Rindas definīcija, Apgrozījuma bilance – Noklusējums, ietver vienu rindu, kas apkopo datus no visiem galvenajiem kontiem. Tāpēc ikviens var ģenerēt pārskatu bez nepieciešamības veikt modifikācijas. Kad apskatāt atskaiti, detalizējiet vienu rindu, lai apskatītu detalizētu informāciju par katru kontu. Rindas definīciju varat modificēt, lai iekļautu vairāk informācijas. Lai modificētu rindas definīciju "apgrozījuma bilance — noklusējuma" un iekļautu rindas visiem kontiem, rīkojieties kā aprakstīts tālāk.

1.  Noklikšķiniet uz **Rediģēšana** un tad noklikšķiniet uz **Ievietot rindas no dimensijām**. Komanda **Ievietot rindas no dimensijām** ļauj izvēlēties, kuras dimensijas vēlaties iekļaut rindas definīcijā. Šai rindas definīcijai izmantojiet **Galvenais konts**.
2.  Pārliecinieties, vai sadaļā **Galvenais konts** ir iekļautas visas rakstzīmes "&", un noklikšķiniet uz **Labi**.

Tagad rindas definīcija satur visus noklusējuma juridiskās personas galvenos kontus.

### <a name="column-definition"></a>Kolonnas definīcija

Katrā apgrozījuma bilances pārskatā izmantota cita kolonnas definīcija. Šīs kolonnu definīcijas satur dažādu veidu kolonnas, lai sniegtu dažāda līmeņa detaļas un finanšu datus.

-   **Detalizēta apgrozījuma bilance — noklusējuma kolonnu tipi**
    -   **DESC** — apraksts no rindas definīcijas.
    -   **ACCT** — kontu kodi.
    -   **ATTR (3)** — atribūti:
        -   Transakcijas datums
        -   Dokuments
        -   Žurnāla apraksts
    -   **FD** — finanšu dati, kas satur tikai debetu.
    -   **FD** — finanšu dati, kas satur tikai kredītu.
    -   **CALC** — neto starpība.
-   **Kopsavilkuma apgrozījuma bilance — noklusējuma kolonnu tipi**
    -   **ACCT** — kontu kodi.
    -   **DESC** — apraksts no rindas definīcijas.
    -   **ATTR** — atribūts:
        -   Dokuments
    -   **FD** — sākuma bilances finanšu dati.
    -   **FD** — finanšu dati, kas satur tikai debetu.
    -   **FD** — finanšu dati, kas satur tikai kredītu.
    -   **CALC** — neto starpība.
    -   **CALC** — beigu atlikums.
-   **Kopsavilkuma apgrozījuma bilance gadu gaitā — noklusējums**
    -   **ACCT** — kontu kodi.
    -   **DESC** — apraksts no rindas definīcijas.
    -   **ATTR** — atribūts:
        -   Dokuments
    -   **FD** — sākuma bilances finanšu dati pašreizējam gadam.
    -   **FD** — finanšu dati, kas satur tikai debetu pašreizējam gadam.
    -   **FD** — finanšu dati, kas satur tikai kredītu pašreizējam gadam.
    -   **CALC** — neto starpība.
    -   **CALC** — beigu atlikums.
    -   **FD** — finanšu dati, kas satur tikai debetu pagājušajam gadam.
    -   **FD** — finanšu dati, kas satur tikai kredītu pagājušajam gadam.



<a name="additional-resources"></a>Papildu resursi
--------

[Finanšu pārskatu veidošanas apskats](financial-reporting-getting-started.md)

[Finanšu pārskatu skatīšana](view-financial-reports.md)

[Dynamics finanšu pārskatu veidošanas emuārs](https://blogs.msdn.com/b/dynamics_financial_reporting/)



