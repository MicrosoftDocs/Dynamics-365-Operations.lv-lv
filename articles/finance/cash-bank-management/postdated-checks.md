---
title: Ar iepriekšēju datumu datēti čeki
description: Šajā rakstā ir sniegta informācija par ar iepriekšēju datumu datētu čeku atbalstu programmā Microsoft Dynamics 365 Finance. Ar iepriekšēju datumu datēti čeki ir čeki, kas tiek izsniegti, lai veiktu vai saņemtu maksājumus nākotnes datumā. Tāpēc šādu čeku nevar iekasēt pirms norādītā datuma.
author: ShylaThompson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPostDatedChecks, CustPostDatedChecks
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 38ee6c5b3d258c313a2066b388a83330bf696d39
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178869"
---
# <a name="postdated-checks"></a>Ar iepriekšēju datumu datēti čeki

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija par ar iepriekšēju datumu datētu čeku atbalstu. Ar iepriekšēju datumu datēti čeki ir čeki, kas tiek izsniegti, lai veiktu vai saņemtu maksājumus nākotnes datumā. Tāpēc šādu čeku nevar iekasēt pirms norādītā datuma.

Programma Dynamics 365 Finance atbalsta pilnu pārvaldības ciklu ar iepriekšēju datumu datētiem čekiem gan modulī, Debitori, gan modulī Kreditori, kā tas ir parādīts tālāk redzamajā tabulā.
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
<td>Reģistrējiet informāciju par kreditoram izsniegto čeku, kas datēts ar iepriekšēju datumu. Grāmatojot maksājumu, tiek atzītas kreditora saistības, taču vēl netiek kreditēts bankas konts. Tā vietā šim nolūkam tiek lietots klīringa konts. </td>
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
<td>Varat atcelt ar iepriekšēju datumu datētu čeku tālāk norādītajās situācijās: - Banka ir atgriezusi čeku.
- Čeks ir lietots nepareizam rēķinam.
- Čeks ir apmaksāts skaidrā naudā.
  </td>
  </tr>
  <tr class="even">
  <td>Apturiet ar iepriekšēju datumu datēta čeka maksājumu.</td>
  <td>Kreditoram izsniegtam ar iepriekšēju datumu datētam čekam maksājumu varat apturēt tādu iemeslu dēļ kā nepietiekami naudas līdzekļi, ar kreditoru noslēgtā līguma izmaiņas, kreditors piegādā preces ar defektiem vai kreditoram preces tiek atgrieztas. Varat apturēt tikai tādu čeku maksājumu, kam nav veikts klīrings.</td>
  </tr>
  </tbody>
  </table>



Lai iegūtu papildu informāciju, skatiet šādas tēmas:

[Ar iepriekšēju datumu datētu čeku iestatīšana](tasks/set-up-postdated-checks.md)

[Ar iepriekšēju datumu datētu čeku reģistrēšana un grāmatošana debitoram](tasks/register-post-postdated-check-customer.md)

[Ar iepriekšēju datumu datētu čeku no debitora apmaksa](tasks/settle-postdated-check-customer.md)

[Ar iepriekšēju datumu datētu čeku reģistrēšana un grāmatošana kreditoram](tasks/register-post-postdated-check-vendor.md) 

[Ar iepriekšēju datumu datētu čeku no kreditora apmaksa](tasks/settle-postdated-check-vendor.md)



