---
title: Noteikšana, kā atbrīvoties no atgrieztiem krājumiem
description: Nosakiet, kā atbrīvoties no atgrieztiem krājumiem.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0049e47d5e0e5f8a2a6d7cc5feb29593c764d323
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991544"
---
# <a name="specify-how-to-dispose-of-returned-items"></a>Noteikšana, kā atbrīvoties no atgrieztiem krājumiem 

[!include [banner](../includes/banner.md)]


Kad apstrādājat atgriešanas pasūtījumu, jānorāda iemesla atgriešanas kods, lai noteiktu, kāpēc produkts tiek atgriezts. Ir jānorāda arī atgriešanas metodes kods un atgriešanas metodes transakcija, lai noteiktu, kas jādara ar pašu atgriezto produktu.

Izvietojuma kodu var pielietot, ja izveidojat atgriešanas pasūtījumu, reģistrējat vienības pienākšanu vai pavadzīmes atjauninājumu vienības pienākšanai un beidzat karantīnas pasūtījumu.

Varat definēt jebkādus atgriešanas metodes kodus, kas nepieciešami biznesa procesu atbalstam. Šajā tabulā sniegta parasti izmantoto kodu kopa, kas piešķirama atgriezta krājuma atgriešanas metodei.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Atgriešanas metodes veids</p></th>
<th><p>Kopējais kods</p></th>
<th><p>Apraksts</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Izslēgšana</p></td>
<td><p>SC</p></td>
<td><p>Utilizācija/Iznīcināšana</p></td>
</tr>
<tr class="even">
<td><p>Izslēgšana</p></td>
<td><p>DC</p></td>
<td><p>Ziedojuma labdarībai</p></td>
</tr>
<tr class="odd">
<td><p>Izslēgšana</p></td>
<td><p>TD</p></td>
<td><p>Trešās personas izslēgšana</p></td>
</tr>
<tr class="even">
<td><p>Izslēgšana</p></td>
<td><p>SL</p></td>
<td><p>Utilizācija izejvielām</p></td>
</tr>
<tr class="odd">
<td><p>Izslēgšana</p></td>
<td><p>TS</p></td>
<td><p>Pārdošana trešajai personai (sekundārie tirgi)</p></td>
</tr>
<tr class="even">
<td><p>Remonts/Pārveidošana</p></td>
<td><p>RW</p></td>
<td><p>Pārstrāde</p></td>
</tr>
<tr class="odd">
<td><p>Remonts/Pārveidošana</p></td>
<td><p>RF</p></td>
<td><p>Pilnīga pārstrāde/Uzlabošana</p></td>
</tr>
<tr class="even">
<td><p>Remonts/Pārveidošana</p></td>
<td><p>MD</p></td>
<td><p>Pārveidot</p></td>
</tr>
<tr class="odd">
<td><p>Remonts/Pārveidošana</p></td>
<td><p>RP</p></td>
<td><p>Remonts</p></td>
</tr>
<tr class="even">
<td><p>Remonts/Pārveidošana</p></td>
<td><p>RV</p></td>
<td><p>Atgriešana kreditoram</p></td>
</tr>
<tr class="odd">
<td><p>Citi</p></td>
<td><p>AI</p></td>
<td><p>Izmantot kā</p></td>
</tr>
<tr class="even">
<td><p>Cita</p></td>
<td><p>RS</p></td>
<td><p>Pārdot atkāroti</p></td>
</tr>
<tr class="odd">
<td><p>Cita</p></td>
<td><p>EX</p></td>
<td><p>Maiņa</p></td>
</tr>
<tr class="even">
<td><p>Cita</p></td>
<td><p>MS</p></td>
<td><p>Dažādi</p></td>
</tr>
</tbody>
</table>


Katram atgriešanas metodes kodam, ko definējat, ir jāatlasa atgriešanas metodes transakcija. Atgriešanas metodes transakcija nosaka atgriešanas metodes kodu fiziskās un finansiālās sekas. Piemēram, atgriešanas metodes transakcija nosaka atgrieztā krājuma fizisko apstrādi, atgrieztā krājuma finansiālo ietekmi un vai debitoram ir jānosūta aizvietošanas krājums. Varat definēt neierobežotu skaitu atgriešanas metožu kodu saskaņā ar jūsu uzņēmējtransakcijas vajadzībām, bet ir tikai sešas iepriekš definētas atgriešanas metožu transakcijas, kuras jūs varat izvēlēties. Tabulā ir sniegtas atgriešanas metožu transakcijas un to definīcijas.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Atgriešanas metodes transakcija</p></th>
<th><p>Apraksts</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Kredītkarte</strong></p></td>
<td><p>Atgriezt krājumu inventārā un kreditēt debitoru.</p></td>
</tr>
<tr class="even">
<td><p><strong>Tikai kredītā</strong></p></td>
<td><p>Kreditēt debitoru, nepieprasot un negaidot krājuma atgriešanu.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Norakstīt</strong></p></td>
<td><p>Norakstīt krājumu un kreditēt debitoru.</p></td>
</tr>
<tr class="even">
<td><p><strong>Aizstāt un kreditēt</strong></p></td>
<td><p>Atgriezt krājumu inventārā, veidot aizvietošanas pasūtījumu un kreditēt debitoru.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Aizstāt un izbrāķēt</strong></p></td>
<td><p>Norakstīt krājumu, veidot aizvietošanas pasūtījumu un kreditēt debitoru.</p></td>
</tr>
<tr class="even">
<td><p><strong>Atgriezt debitoram</strong></p></td>
<td><p>Noraidīt atgriezto krājumu un atgriezt to debitoram.</p></td>
</tr>
</tbody>
</table>


## <a name="select-a-disposition-code-for-a-quarantine-order"></a>Izvēlieties izvietojuma kodu karantīnas pasūtījumam

1.  Noklikšķiniet uz **Krājumu pārvaldība** \> **Periodiskās darbības** \> **Kvalitātes pārvaldība** \> **Karantīnas pasūtījumi**.

2.  Esošam karantīnas pasūtījumam atlasiet kādu darbību cilnes **Apskats** laukā **Atgriešanas metodes kods**.



## <a name="see-also"></a>Skatiet arī

[Karantīnas pasūtījums (forma)](https://technet.microsoft.com/library/aa554073(v=ax.60))

[Atgriešanas metožu kodi (forma)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]