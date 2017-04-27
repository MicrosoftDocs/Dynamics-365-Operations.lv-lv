---
title: "Pārkāpumu brīdinājumu iestatīšana"
description: "Šajā tēmā izskaidrots, kā iestatīt kārtulas, lai brīdinātu klientu apkalpošanas pārstāvjus par potenciāli krāpniecisku informāciju, kad tiek apstrādāti pasūtījumi. Var definēt īpašus izmantošanai paredzētus kodus, lai automātiski vai manuāli aizturētu aizdomīgus pasūtījumus."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: fabb7ee23e90feca818bebfa29c7048987193e4c
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-fraud-alerts"></a>Pārkāpumu brīdinājumu iestatīšana

[!include[banner](includes/banner.md)]


Šajā tēmā izskaidrots, kā iestatīt kārtulas, lai brīdinātu klientu apkalpošanas pārstāvjus par potenciāli krāpniecisku informāciju, kad tiek apstrādāti pasūtījumi. Var definēt īpašus izmantošanai paredzētus kodus, lai automātiski vai manuāli aizturētu aizdomīgus pasūtījumus. 

Pirms iestatāt un izmantojat pārkāpumu pārbaudes kārtulas, ir jāiespējo pārkāpumu pārbaude un jādefinē pamata pārkāpumu pārbaudes vērtības zvanu centra parametros. Ir divi pārkāpumu kārtulu tipi:

-   **Statiskās kārtulas** izmanto noteiktu vērtību, piemēram, tālruņa numuru, kas ir melnajā sarakstā.
-   **Dinamiskās kārtulas** var veidot no mainīgajiem un nosacījumiem.

Pirms dinamiskās kārtulas izveidošanas ir jāizveido mainīgie un nosacījumi, kas definē, uz kurām personām kārtula attiecas un kad kārtula ir jāpiemēro. Piemēram, jūs vēlaties izveidot kārtulu, lai pieprasītu to, ka, debitoram Nr. 1202 izdarot pārdošanas pasūtījumu vismaz 1000,00 vērtībā, pārdošanas pasūtījums ir jāaiztur, līdz iespējams pārbaudīt debitora maksājumu. Šajā gadījumā mainīgie ir: debitors Nr. 1202 un pasūtījuma kopējā summa 1000,00. Nosacījums norāda, ka ja debitors Nr. 1202 veic pasūtījumu un kopējā pasūtījuma summa ir 1,000.00 vai lielāka, pārdošanas pasūtījums ir jāaiztur līdz debitora maksājumu būs iespējams pārbaudīt.




