---
title: "Audita ierobežojuma nosacījumi"
description: "Audita politiku var izmantot, lai novērtētu izdevumu pārskatus, kreditoru rēķinus un pirkšanas pasūtījumus, lai pārliecinātos, ka tie atbilst izveidotajiem politikas nosacījumiem. Visi ar audita politiku saistītie nosacījumi tiek izpildīti pakešuzdevuma režīmā saskaņā ar norādīto grafiku.  Katras politikas nosacījums ir politikas nosacījumu veida instance. Katram politikas nosacījumu veidam vienlaikus var būt aktīvs tikai viens politikas nosacījums."
author: ryansandness
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 12991
ms.assetid: 8d787017-71dc-418f-b8c2-4ea9763d9978
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: c4f5dae90c5fcaaa52a7087d7c20b2de343b7da0
ms.openlocfilehash: 68f31f00a30513b7d2f3f36a39eaf1cfe7a219a1
ms.contentlocale: lv-lv
ms.lasthandoff: 08/01/2017

---

# <a name="audit-policy-rules"></a>Audita ierobežojuma nosacījumi

[!include[banner](../includes/banner.md)]


Audita politiku var izmantot, lai novērtētu izdevumu pārskatus, kreditoru rēķinus un pirkšanas pasūtījumus, lai pārliecinātos, ka tie atbilst izveidotajiem politikas nosacījumiem. Visi ar audita politiku saistītie nosacījumi tiek izpildīti pakešuzdevuma režīmā saskaņā ar norādīto grafiku.  Katras politikas nosacījums ir politikas nosacījumu veida instance. Katram politikas nosacījumu veidam vienlaikus var būt aktīvs tikai viens politikas nosacījums. 

<a name="queries-and-query-types"></a>Vaicājumi un vaicājumu veidi
-----------------------

Veidojot audita politikas nosacījumu, vispirms ir jāatlasa politikas nosacījuma veids. Politikas nosacījuma veids nosaka lietojumprogrammas objektu koka (AOT) vaicājumu, ar ko sāk politikas nosacījuma izveidi. Tas arī norāda vaicājuma veidu, ko izmanto politikas nosacījumam. Vaicājums nosaka pirmdokumentu, kuru novērtē politikas nosacījums. Tas arī norāda laukus pirmdokumentā, kas identificē gan juridisku personu, gan datumu, kas jāizmanto, kad auditam tiek atlasīti dokumenti. Vaicājuma veids kontrolē noklusējuma laukus vaicājuma lapā un lapā Audita ierobežojuma nosacījumi. Šajā tabulā ir parādīti vaicājumu veidi, kas pieejami audita politikas nosacījumiem.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Vaicājuma tips</th>
<th>Mērķis</th>
<th>Papildinformācija</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Nosacījuma</td>
<td>Novērtējiet pirmdokumenta atribūtus, salīdzinot tos ar norādītām vērtībām.</td>
<td></td>
</tr>
<tr class="even">
<td>Apkopot</td>
<td>Novērtējiet vairākus pirmdokumentus vai pirmdokumentu rindas, salīdzinot tos ar politikas nosacījumu, apkopojot skaitliskās vērtības.</td>
<td></td>
</tr>
<tr class="odd">
<td>Iztveršana</td>
<td>Nejaušā secībā atlasiet noteiktu pirmdokumentu procentuālo daļu, lai novērtētu politikas pārkāpumus.</td>
<td>Kad šī opcija ir atlasīta, jālieto lapa Audita ierobežojuma nosacījumi, lai norādītu dokumentu procentuālo vērtību, kas nejaušā secībā jāatlasa auditam.</td>
</tr>
<tr class="even">
<td>Dublēt</td>
<td>Novērtējiet pirmdokumentus, lai noteiktu, vai tie satur dublējošos ierakstus norādītajos laukos.</td>
<td>Ja šī opcija ir atlasīta, izmantojiet lapu Audita ierobežojuma nosacījumi, lai norādītu dienu skaitu, kas jāpievieno dokumentu atlases datumu diapazona sākumam, kad dokumenti tiek novērtēti uz dublējošo ierakstu klātbūtni.</td>
</tr>
<tr class="odd">
<td>Meklēšana sarakstā</td>
<td>Novērtējiet pirmdokumentus uz noteikto entītiju klātbūtni.</td>
<td>Vaicājuma saknes dokuments nosaka dokumentu, kuram tiek veikts audits. Vaicājumam jābūt saraksta formā, kurā ietverta atsauce uz tabulu DirPartyTable. Šo opciju var izmantot tikai šādiem AOT vaicājumiem:
<ul>
<li><span class="ui">AuditPolicyExpenseList</span> (Izdevumu pārskatā pārraudzītie darbinieki)</li>
<li><span class="ui">AuditPolicyPurchList</span> (Pirkšanas pasūtījumā pārraudzītie kreditori)</li>
<li><span class="ui">AuditPolicyVendInvoiceList</span> (Kreditora rēķinā pārraudzītie kreditori)</li>
</ul>
Atlasot šo opciju, norādiet uzraugāmās entītijas lapā Audita ierobežojuma nosacījumi.</td>
</tr>
<tr class="even">
<td>Meklēšana pēc atslēgvārdiem</td>
<td>Novērtējiet pirmdokumentus, lai noteiktu, vai tie satur noteiktus vārdus.</td>
<td>Atlasot šo opciju, ievadiet meklējamos terminus lapā Audita ierobežojuma nosacījumi. Lapā Audita ierobežojuma nosacījumi ir ietvertas arī opcijas, kas ļauj norādīt tabulas un laukus, kurām novērtēt ievadītos vārdus.</td>
</tr>
</tbody>
</table>

## <a name="common-parameters"></a>Vispārīgie parametri
Visiem noteiktas audita politikas nosacījumiem ir vienādi pakešuzdevumu parametri un vienāds dokumentu atlases datumu diapazons. Šie parametri tiek norādīti politikai lapā Audita ierobežojuma nosacījumi.



<a name="see-also"></a>Skatiet arī
--------

[Audita ierobežojuma nosacījumu pārkāpumi un gadījumi](audit-policy-violations-cases.md)
[Definēt pirmdokumentu audita politikas](tasks/define-audit-policies-source-documents.md)



