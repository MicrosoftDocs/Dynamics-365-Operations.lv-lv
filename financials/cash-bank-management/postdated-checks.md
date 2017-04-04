---
title: "Ar iepriekšēju datumu datēti čeki"
description: "Šajā rakstā ir sniegta informācija par atbalstu postdated pārbaudes Microsoft Dynamics 365 operācijām. Ar iepriekšēju datumu datēti čeki ir čeki, kas tiek izsniegti, lai veiktu vai saņemtu maksājumus nākotnes datumā. Tāpēc šādu čeku nevar iekasēt pirms norādītā datuma."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4bb647cfd3f012efbffa93a81462c538a24ac850
ms.openlocfilehash: 7349771b7f9a1ad4cd5b239f1d10bd3229d2d0df
ms.lasthandoff: 03/31/2017


---

# <a name="postdated-checks"></a>Ar iepriekšēju datumu datēti čeki

Šajā rakstā ir sniegta informācija par atbalstu postdated pārbaudes Microsoft Dynamics 365 operācijām. Ar iepriekšēju datumu datēti čeki ir čeki, kas tiek izsniegti, lai veiktu vai saņemtu maksājumus nākotnes datumā. Tāpēc šādu čeku nevar iekasēt pirms norādītā datuma.

Microsoft Dynamics 365 operāciju atbalsta pilnīgu pārvaldības cikla postdated pārbaudes gan debitoru un kreditoru, kā parādīts sekojošajā tabulā.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Scenārijs</th>
<th>Detalizēta</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Iestatīt ar iepriekšēju datumu datētus čekus</td>
<td>Jums ir jāiestata jauna maksājuma metode un jānorāda maksājuma procedūra klīringa kontiem saistībā ar izsniegtajiem čekiem, saņemtajiem čekiem un ieturētajiem nodokļiem.</td>
</tr>
<tr class="even">
<td>Reģistrēt un grāmatot čeku kreditoram, kas datēts ar iepriekšēju datumu</td>
<td>Reģistrējiet informāciju par kreditoram izsniegto čeku, kas datēts ar iepriekšēju datumu. Grāmatojot maksājumu, kreditoru saistības ir atzīta, bet bankas konts nav vēl kredītu. Tā vietā šim nolūkam tiek lietots klīringa konts.</td>
</tr>
<tr class="odd">
<td>Ar iepriekšēju datumu datētu čeku reģistrēšana un grāmatošana debitoram</td>
<td>Reģistrējiet informāciju par no debitora saņemtu čeku, kurš datēts ar iepriekšēju datumu. Grāmatojot maksājumu, debitoru parādi ir kredīts, bet bankas konts nav vēl debetā. Tā vietā šim nolūkam tiek lietots klīringa konts.</td>
</tr>
<tr class="even">
<td>Reģistrētu un iegrāmatotu postdated Nomaiņa izvēles debitoru vai kreditoru</td>
<td>
Ja jūsu sākotnējais kreditoram izsniegtais vai no debitora saņemtais čeks ir pazaudēts vai bojāts, varat izsniegt ar iepriekšēju datumu datētu aizstāšanas čeku. Kad reģistrējot čeka informāciju, norādiet atsauci uz sākotnējo čeku un norādiet, ka jaunais čeks aizstāj sākotnējo. Varat arī grāmatot šo aizstāšanas čeku.</td>
</tr>
<tr class="odd">
<td>Pārsūtīt debitora ar iepriekšējo datumu datēto čeku kreditoram</td>
<td>Kad no debitora saņemat ar iepriekšēju datumu datētu čeku, šo čeku varat pārsūtīt kreditoram kā maksājumu.</td>
</tr>
<tr class="even">
<td>Segt ar iepriekšēju datumu datētu debitora vai kreditora čeku</td>
<td>Sedziet ar iepriekšēju datumu datētu čeku, kas debitoram vai kreditoram ir grāmatots pagaidu kontam, kad šim čekam beidzot pienāk beigu termiņš. Kad čeks ir segts, banka beidzot veic debitēšanu vai kreditēšanu pret klīringa kontu, kas tika izmantots iepriekš.</td>
</tr>
<tr class="odd">
<td>Atcelt kreditora čeku, kas datēts ar iepriekšēju datumu</td>
<td>Iegrāmatotās postdated izvēles šajās situācijās var atcelt:-čeks tiek atgriezta banka.
-Čeks tiek lietota pareiza rēķina.
-Skaidras naudas maksājumu veikšanas pret čeku.
</td>
</tr>
<tr class="even">
<td>Pārtraukt maksājumu postdated izvēles</td>
<td>Kreditoram izsniegtam ar iepriekšēju datumu datētam čekam maksājumu varat apturēt tādu iemeslu dēļ kā nepietiekami naudas līdzekļi, ar kreditoru noslēgtā līguma izmaiņas, kreditors piegādā preces ar defektiem vai kreditoram preces tiek atgrieztas. Jūs varat apturēt maksājumu tikai pēc pārbaudes, kas nav noskaidroti.</td>
</tr>
</tbody>
</table>





