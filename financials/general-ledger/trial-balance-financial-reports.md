---
title: "Apgrozījuma bilances finanšu pārskati"
description: "Šajā rakstā ir aprakstīts šo noklusējuma ziņojumus par izmēģinājuma bilances. Tā arī apraksta veidošanas blokus, kas ir saistīti ar šiem ziņojumiem un cik var modificēt atskaites, lai atbilstu jūsu biznesa vajadzībām."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 750e2975eb75511afd75b6be0c8dfe90c8a9c89c
ms.lasthandoff: 03/31/2017


---

# <a name="trial-balance-financial-reports"></a>Apgrozījuma bilances finanšu pārskati

Šajā rakstā ir aprakstīts šo noklusējuma ziņojumus par izmēģinājuma bilances. Tā arī apraksta veidošanas blokus, kas ir saistīti ar šiem ziņojumiem un cik var modificēt atskaites, lai atbilstu jūsu biznesa vajadzībām. 

<a name="default-trial-balance-reports"></a>Noklusējuma apgrozījuma bilances pārskati
-----------------------------

Microsoft Dynamics 'AX 7 finanšu pārskatu veidošanas vidē pieejami trīs apgrozījuma bilances pārskati.

| Noklusējuma atskaite                                 | Ko tā dara                                                                                                                                                                                        |
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

Rindas definīcijas izmēģinājuma bilance-noklusējuma ir viena rinda, kas velk visu galveno kontu. Tāpēc ikviens var ģenerēt pārskatu bez nepieciešamības veikt modifikācijas. Kad apskatāt atskaiti, detalizējiet vienu rindu, lai apskatītu detalizētu informāciju par katru kontu. Rindas definīciju varat modificēt, lai iekļautu vairāk informācijas. Lai modificētu rindas definīciju "apgrozījuma bilance — noklusējuma" un iekļautu rindas visiem kontiem, rīkojieties kā aprakstīts tālāk.

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

 

<a name="see-also"></a>Skatiet arī
--------

[Financial reporting](financial-reporting-getting-started.md)

[View financial reports](view-financial-reports.md)

[Dinamika finanšu pārskata Blog](http://blogs.msdn.com/b/dynamics_financial_reporting/)


