---
title: Brīdinājumi vai kļūmes ziņojumi par virsgrāmatas perioda statusu, neslēdzot krājumu
description: Brīdinājumi vai kļūmes ziņojumi par virsgrāmatas perioda statusu, neslēdzot krājumu
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 05851753e29da75f014d2cc77e2b8df259620eee
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476970"
---
# <a name="warnings-or-errors-on-changing-ledger-period-status-without-closing-inventory"></a>Brīdinājumi vai kļūmes ziņojumi par virsgrāmatas perioda statusu, neslēdzot krājumu

Korporācija Microsoft ieviesa šādas pārbaudes, lai novērstu problēmas, ko izraisījis nepareizs perioda beigu process, kas saistīts ar izmaksām. Ja rodas kāds no šiem kļūdu ziņojumiem, skatiet [KB 4561987](https://fix.lcs.dynamics.com/Issue/Details?kb=4561987&bugId=445351&dbType=3&qc=f514f2adcddcddceec43af58c26ae8a9020effdc7cdfe085d9d0deeb8cc7b6a3), lai iegūtu vairāk informācijas par šo problēmu novēršanu.

- Jūs gatavojaties izpildīt pārrēķinu ar datumu %1 (10-02-2019). Pēdējais reģistrētais pārrēķins tika izpildīts iepriekšējā periodā ar datumu %2 (20-01-2019). Nav reģistrēta neviena krājumu slēgšanas izpilde ar datumu %3 (31-01-2019) salīdzināšanas perioda beigas. Lūdzu, neaizmirstiet izpildīt krājumu slēgšanu kā %3 (31-01-2019), kas atbilst perioda beigām. Krājumu novērtējums, pārdoto preču izmaksas un novirzes apakšgrāmatās vai virsgrāmatā var nebūt pareizas, kamēr tas nav izpildītas.

- Jūs gatavojaties mainīt virsgrāmatas perioda statusu no %1 uz %2. Nav reģistrēta neviena krājumu slēgšanas izpilde ar datumu %3 salīdzināšanas perioda beigas. Lūdzu, veiciet krājumu slēgšanu atbilstoši %3 perioda beigām, pirms maināt statusu. Krājumu novērtējums, pārdoto preču izmaksas un novirzes apakšgrāmatās vai virsgrāmatā var nebūt pareizas, kamēr tas nav izpildītas. Ziņots no juridiskās personas %4. Pagaidām šis ir ziņojums ir informatīvs, taču turpmāk jums būs jāveic šāda darbība.

- Konta struktūra %1 ir mainīta. Viens vai vairāki galvenie konti %2 vairs nepastāv. Šie galvenie pārskati tiek pieprasīti līdz %3 ar %4 datumu. Lūdzu, pievienojiet šos galvenos kontus Konta struktūrai %1, pirms varat atsākt %3 darbu. Pagaidām šis ir ziņojums ir informatīvs, taču turpmāk jums būs jāveic šāda darbība.

- Jūs gatavojaties izpildīt krājumu slēgšanu ar datumu %1 (31-01-2019). Nav reģistrēta neviena atgriezeniska izmaksu aprēķināšana ar datumu %2 (31-01-2019) salīdzināšanas perioda beigas. Lūdzu atceraties veikt atgriezenisko izmaksu aprēķināšanu ar datumu %3 (31-01-2019) salīdzināšanas perioda beigas. Krājumu novērtējums, pārdoto preču izmaksas un novirzes apakšgrāmatās vai virsgrāmatā var nebūt pareizas, kamēr tas nav izpildītas.

- Jūs gatavojaties izpildīt atgriezenisko izmaksu aprēķināšanu ar datumu %1 (28-02-2019). Pēdējā reģistrētā atgriezenisko izmaksu aprēķināšana tika izpildīta iepriekšējā periodā ar datumu %2 (31-01-2019). Nav reģistrēta neviena krājumu slēgšanas izpilde ar datumu %3 (31-01-2019) salīdzināšanas perioda beigas.

Lūdzu, neaizmirstiet izpildīt krājumu slēgšanu kā %3 (31-01-2019), kas atbilst perioda beigām. Krājumu novērtējums, pārdoto preču izmaksas un novirzes apakšgrāmatās vai virsgrāmatā var nebūt pareizas, kamēr krājumu slēgšana nav izpildīta.