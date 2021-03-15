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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: b8c527e578fee6abfeeade99fba8070365c020bd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983854"
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

## <a name="an-update-conflict-occurs-when-the-inventory-valuation-method-is-either-standard-cost-or-moving-average"></a>Atjaunināšanas konflikts rodas, kad krājumu novērtēšanas metode ir Standarta izmaksas vai Pārvieto vidējo vērtību

Ja grāmatojat dokumentus, piemēram, krājumu žurnālus, pirkšanas pasūtījuma rēķinus vai pārdošanas pasūtījuma rēķinus paralēli mērogošanai un veiktspējai, var tikt parādīts kļūdas ziņojums par atjauninājumu konfliktu un daži dokumenti, iespējams, netiks grāmatoti. Šī problēma rodas, kad krājumu novērtēšanas metode ir *Standarta izmaksas* vai *Pārvieto vidējo vērtību*. Abas šīs metodes ir pastāvīgas izmaksu aprēķināšanas metodes. Citiem vārdiem sakot, gala izmaksas tiek noteiktas iegrāmatošanas laikā.

Ja izmantojat metodi *Pārvieto vidējo*, kļūdas ziņojums ir līdzīgs šim piemēram:

> Krājumu vērtība xx.xx nav paredzama pēc proporcionālo izdevumu aprēķina

Ja izmantojat metodi *Standarta izmaksas*, kļūdas ziņojums ir līdzīgs šim piemēram:

> Standarta izmaksas nesakrīt ar finanšu krājumu vērtību pēc atjaunināšanas. Vērtība = xx.xx, Daudzums = yy.yy, Standarta izmaksas = zz.zz

Kamēr Microsoft nav izlaidis risinājumu problēmas atrisināšanai, apsveriet iespēju izmantot šādus risinājumus, lai palīdzētu izvairīties no šīm kļūdām vai tās samazināt:

- Neizdevušos dokumentu atkārtota grāmatošana.
- Izveidojiet dokumentus, kam ir mazāk rindu.
- Izvairieties no decimālvērtībām standarta izmaksās. Mēģiniet definēt standarta izmaksas tā, lai lauks **Cenas daudzums** būtu iestatīts uz *1*. Ja ir jānorāda **Cenas daudzuma** vērtība, kas pārsniedz *1*, mēģiniet samazināt decimāldaļu skaitu vienības standarta izmaksās. (Ideālā gadījumā jābūt mazāk nekā diviem decimāldaļskaitļiem.) Piemēram, izvairieties no standarta izmaksu iestatījumu definēšanas, piemēram, **Cena** = *10* un **Cenas daudzums** = *3* cenas, jo tie ražos vienības standarta izmaksas 3.333333 (kur decimālskaitļa vērtība atkārtojas).
- Lielākajā daļā dokumentu izvairīties no vairākām rindām, kurās ir viena un tā pati preču un finanšu krājumu dimensiju kombinācija.
- Samaziniet paralēlošanas pakāpi. (Šādā gadījumā sistēma var kļūt ātrāka, jo notiek mazāk atjauninājumu konfliktu un mēģinājumu.)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]