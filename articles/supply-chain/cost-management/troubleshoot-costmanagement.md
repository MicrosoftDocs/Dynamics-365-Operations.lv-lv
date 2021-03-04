---
title: Ar izmaksām saistīto problēmu novēršanas pārvaldība
description: Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar izmaksu pārvaldību.
author: riluan
manager: tfehr
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails, InventValueProcess, InventValueReportSetup, InventClosing
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: e84bb167395c06295b0e8ef8b9fd98aa4bc0cc14
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4433223"
---
# <a name="troubleshoot-cost-management"></a>Ar izmaksām saistīto problēmu novēršanas pārvaldība

Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar izmaksu pārvaldību.

## <a name="functional-gaps-between-the-inventory-valueaging-reports-and-their-storage-versions"></a>Funkcionālās atšķirības starp krājumu vērtību/novecošanās pārskatiem un to glabāšanas versijām

[Krājumu novecošanās pārskata uzglabāšanas](inventory-aging-report-storage.md) un [Krājumu vērtības uzglabāšanas pārskata](inventory-value-report-storage.md) līdzekļi iespējo Supply Chain Management, lai parādītu lielus krājumu darbību apjomus. Katrā gadījumā pārskata rezultāti tiek saglabāti pārlūkošanai un eksportēšanai, atšķirībā no šo pārskatu neuzglabāšanas versijām. Tomēr dažas funkcionalitātes, kas pastāv šo pārskatu neuzglabāšanas versijās, glabāšanas versijās nepastāv. Sekojošās apakšsadaļās ir apkopotas atšķirības un sniegti risinājumi.

### <a name="storage-reports-dont-include-subtotals-even-if-they-are-enabled-in-the-report-layout"></a>Krātuves pārskatos netiek iekļautas apakšsummas, pat ja tās ir iespējotas pārskata izkārtojumā

Apakšsummas var radīt problēmas, ja rezultāts tiek eksportēts, it īpaši, ja lietotāji maina ieraksta secību.

Lai pārbaudītu apakšsummas, varat eksportēt rezultātu uz Microsoft Excel. Vai arī, ja vēlaties pārbaudīt apakšsummas Supply Chain Management, izmantojiet [funkciju pārvaldību](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), lai iespējotu *Jauno režģu kontroli* un *(Priekšskatījums) Grupēšana režģos* līdzekļus, kas nodrošina daudz elastīgāku veidu, kā apskatīt jebkuras grupas apakšsummu pēc kolonnas. Plašāku informāciju skatiet sadaļā [Režģa iespējas](../../fin-ops-core/fin-ops/get-started/grid-capabilities.md).

### <a name="inventory-value-storage-report-doesnt-support-ledger-account-information"></a>Krājumu vērtības uzglabāšanas pārskats neatbalsta virsgrāmatas konta informāciju

Varat palaist apgrozījuma bilanci, lai iegūtu krājumu kontu bilanci un salīdzināt to ar **Krājumu vērtības uzglabāšanas** pārskatu.

## <a name="warnings-or-errors-are-shown-when-changing-a-ledger-period-status-without-closing-inventory"></a>Brīdinājumi vai kļūdas tiek attēlotas, mainot virsgrāmatas perioda statusu, neslēdzot krājumus

Korporācija Microsoft ieviesa šādas pārbaudes, lai novērstu problēmas, ko izraisījis nepareizs perioda beigu process, kas saistīts ar izmaksām. Ja rodas kāds no šiem kļūdu ziņojumiem, skatiet [KB 4561987](https://fix.lcs.dynamics.com/Issue/Details?kb=4561987&bugId=445351&dbType=3&qc=f514f2adcddcddceec43af58c26ae8a9020effdc7cdfe085d9d0deeb8cc7b6a3), lai iegūtu vairāk informācijas par šo problēmu novēršanu.

- Jūs gatavojaties izpildīt pārrēķinu ar datumu %1 (10-02-2019). Pēdējais reģistrētais pārrēķins tika izpildīts iepriekšējā periodā ar datumu %2 (20-01-2019). Nav reģistrēta neviena krājumu slēgšanas izpilde ar datumu %3 (31-01-2019) salīdzināšanas perioda beigas. Lūdzu, neaizmirstiet izpildīt krājumu slēgšanu kā %3 (31-01-2019), kas atbilst perioda beigām. Krājumu novērtējums, pārdoto preču izmaksas un novirzes apakšgrāmatās vai virsgrāmatā var nebūt pareizas, kamēr tas nav izpildītas.

- Jūs gatavojaties mainīt virsgrāmatas perioda statusu no %1 uz %2. Nav reģistrēta neviena krājumu slēgšanas izpilde ar datumu %3 salīdzināšanas perioda beigas. Lūdzu, veiciet krājumu slēgšanu atbilstoši %3 perioda beigām, pirms maināt statusu. Krājumu novērtējums, pārdoto preču izmaksas un novirzes apakšgrāmatās vai virsgrāmatā var nebūt pareizas, kamēr tas nav izpildītas. Ziņots no juridiskās personas %4. Pagaidām šis ir ziņojums ir informatīvs, taču turpmāk jums būs jāveic šāda darbība.

- Konta struktūra %1 ir mainīta. Viens vai vairāki galvenie konti %2 vairs nepastāv. Šie galvenie pārskati tiek pieprasīti līdz %3 ar %4 datumu. Lūdzu, pievienojiet šos galvenos kontus Konta struktūrai %1, pirms varat atsākt %3 darbu. Pagaidām šis ir ziņojums ir informatīvs, taču turpmāk jums būs jāveic šāda darbība.

- Jūs gatavojaties izpildīt krājumu slēgšanu ar datumu %1 (31-01-2019). Nav reģistrēta neviena atgriezeniska izmaksu aprēķināšana ar datumu %2 (31-01-2019) salīdzināšanas perioda beigas. Lūdzu atceraties veikt atgriezenisko izmaksu aprēķināšanu ar datumu %3 (31-01-2019) salīdzināšanas perioda beigas. Krājumu novērtējums, pārdoto preču izmaksas un novirzes apakšgrāmatās vai virsgrāmatā var nebūt pareizas, kamēr tas nav izpildītas.

- Jūs gatavojaties izpildīt atgriezenisko izmaksu aprēķināšanu ar datumu %1 (28-02-2019). Pēdējā reģistrētā atgriezenisko izmaksu aprēķināšana tika izpildīta iepriekšējā periodā ar datumu %2 (31-01-2019). Nav reģistrēta neviena krājumu slēgšanas izpilde ar datumu %3 (31-01-2019) salīdzināšanas perioda beigas.
Lūdzu, neaizmirstiet izpildīt krājumu slēgšanu kā %3 (31-01-2019), kas atbilst perioda beigām. Krājumu novērtējums, pārdoto preču izmaksas un novirzes apakšgrāmatās vai virsgrāmatā var nebūt pareizas, kamēr krājumu slēgšana nav izpildīta.

## <a name="inventory-aging-report-discrepancies"></a>Krājumu vecumstruktūru pārskata neatbilstība

**Krājumu vecumstruktūru pārskats** rāda dažādas vērtības, ja tās tiek apskatītas dažādās noliktavas dimensijās (piemēram, vietnē vai noliktavā). Lai iegūtu papildu informāciju par pārskata loģiku, skatiet [Krājumu vecumstruktūru pārskata piemēri un loģika](inventory-aging-report.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]