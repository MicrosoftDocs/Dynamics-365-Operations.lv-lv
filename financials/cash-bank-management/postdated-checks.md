---
title: "Ar iepriekšēju datumu datēti čeki"
description: "Šajā rakstā ir sniegta informācija par programmatūrā Microsoft Dynamics 365 for Operations nodrošināto ar iepriekšēju datumu datētu čeku atbalstu. Ar iepriekšēju datumu datēti čeki ir čeki, kas tiek izsniegti, lai veiktu vai saņemtu maksājumus nākotnes datumā. Tāpēc šādu čeku nevar iekasēt pirms norādītā datuma."
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: acc147105779f3857ea66ace8537da133e4d3a5c
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="postdated-checks"></a>Ar iepriekšēju datumu datēti čeki

[!include[banner](../includes/banner.md)]


Šajā rakstā ir sniegta informācija par programmatūrā Microsoft Dynamics 365 for Operations nodrošināto ar iepriekšēju datumu datētu čeku atbalstu. Ar iepriekšēju datumu datēti čeki ir čeki, kas tiek izsniegti, lai veiktu vai saņemtu maksājumus nākotnes datumā. Tāpēc šādu čeku nevar iekasēt pirms norādītā datuma.

Microsoft Dynamics 365 for Operations atbalsta pilnu ar iepriekšēju datumu datētu čeku pārvaldības ciklu gan modulī Debitoru parādi, gan modulī Parādi kreditoriem, kā tas ir redzams tālāk esošajā tabulā.
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
<td>Reģistrējiet informāciju par kreditoram izsniegto čeku, kas datēts ar iepriekšēju datumu. Grāmatojot maksājumu, tiek atzītas kreditora saistības, taču vēl netiek kreditēts bankas konts. Tā vietā šim nolūkam tiek lietots klīringa konts.</td>
</tr>
<tr class="odd">
<td>Ar iepriekšēju datumu datētu čeku reģistrēšana un grāmatošana debitoram</td>
<td>Reģistrējiet informāciju par no debitora saņemtu čeku, kurš datēts ar iepriekšēju datumu. Grāmatojot maksājumu, tiek kreditēta no debitora saņemamā summa, taču vēl netiek debitēts bankas konts. Tā vietā šim nolūkam tiek lietots klīringa konts.</td>
</tr>
<tr class="even">
<td>Reģistrējiet un grāmatojiet ar iepriekšēju datumu datētu debitora vai kreditora aizstāšanas čeku.</td>
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
<td>Varat atcelt ar iepriekšēju datumu datētu čeku tālāk norādītajās situācijās. - Banka ir atgriezusi čeku.
- Čeks ir lietots nepareizam rēķinam.
- Čeks ir apmaksāts skaidrā naudā.
</td>
</tr>
<tr class="even">
<td>Apturiet ar iepriekšēju datumu datēta čeka maksājumu.</td>
<td>Kreditoram izsniegtam ar iepriekšēju datumu datētam čekam maksājumu varat apturēt tādu iemeslu dēļ kā nepietiekami naudas līdzekļi, ar kreditoru noslēgtā līguma izmaiņas, kreditors piegādā preces ar defektiem vai kreditoram preces tiek atgrieztas. Varat apturēt tikai tādu čeku maksājumu, kam nav veikts klīrings.</td>
</tr>
</tbody>
</table>






