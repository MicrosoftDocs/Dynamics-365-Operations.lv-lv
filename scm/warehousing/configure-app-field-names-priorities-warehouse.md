---
title: "Konfigurēt Warehousing app app lauku nosaukumus"
description: "Šajā tēmā ir aprakstīts, kā noteikt un konfigurēšana noliktavā app lauku nosaukumus un prioritātes Dynamics 365 operācijām."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: ce8f6d6f7090995bc44db1ba0103a7d6c0416620
ms.lasthandoff: 03/31/2017


---

# <a name="configure-app-field-names-in-warehousing-app"></a>Konfigurēt Warehousing app app lauku nosaukumus

Šajā tēmā ir aprakstīts, kā noteikt un konfigurēšana noliktavā app lauku nosaukumus un prioritātes Dynamics 365 operācijām. 

**Piezīme:** šī tēma attiecas uz noliktavu pārvaldības līdzekļus. Tas neattiecas uz līdzekļiem krājumu vadība. Dynamics 365 operācijām - noliktavas ir lietojumprogramma, kas var izmantot noliktavas uzdevumu veikšanai. Jūs varat definēt un konfigurēt lauku nosaukumi, ko izmanto app, kā arī konfigurēt prioritāte būtu jāpiešķir lauku nosaukumus. Šajā tēmā ir paskaidrots, kā noteikt un konfigurēt šīs noliktavas app lauku nosaukumus un prioritātes un kā tās tiek lietotas Dynamics 365 operācijām - noliktavas. Pamācību skatiet detalizētu informāciju par to, kā konfigurēt savienojumu dinamika 365 operācijām - noliktavas, [instalēt un konfigurēt Dynamics 365 operācijām - noliktavas](install-configure-warehousing-app.md).

<a name="configure-warehouse-app-field-names"></a>Konfigurēšana noliktavā app lauku nosaukumus
===================================

Lietojot Dynamics 365 operācijām - noliktavas mobilajā ierīcē, var konfigurēt kā Rādīt metadatus ierīcē par **noliktavas app lauku nosaukumus** lapā. Jaunu uzņēmumu dinamiku 365 operācijām, atlasiet **izveidot noklusēto iestatījumu** visi lauku nosaukumi, kuri tiks izmantoti noliktavas mobilās ierīces darbplūsmām, un pēc tam piešķirt vēlamā ievades režīmā un ievades tips tās ģenerēt. Pēc tam, kad visi lauku nosaukumi ir izveidoti, varat atlasīt opcijas ievades.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opcija</th>
<th>apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Vēlamais ievades režīms</td>
<td>Šī opcija nosaka, vai skenēšanas lauks vai manuālā ieraksta ievades lauks ir jāparāda atlasītā lauka nosaukumu. Tas ir noderīgi atšķirt laukus atkarībā, ja lauks tiek izmantoti svītrkodi. <strong>Piezīme:</strong> lauku nosaukumus ar vēlamā ievades režīms iestatīts <strong>skenēšanas</strong>, informāciju var ievadīt manuāli, ja svītrkods ir nav lasāms vai ir bojāts.</td>
</tr>
<tr class="even">
<td>Ievades tips</td>
<td>Šī opcija nosaka, ir jāizmanto kāda ievades tips atlasītā lauka nosaukumu. Ir pieejamas četras opcijas:
<ul>
<li><strong>Atlases</strong> - ietver opcijas, lai izvēlētos no saraksta. Lauku nosaukumi, ja šī opcija nav rediģējams.</li>
<li><strong>Datums</strong> - lauku nosaukumi norādīti kā datumu parāda datuma formātu ar etiķeti. Tas palīdz redzēt kādā formātā ievadīt datumu noliktavas darbiniekiem. Lauku nosaukumi, ja šī opcija nav rediģējams.</li>
<li><strong>Alfa</strong> - ja izvēlēts, ievadot informāciju manuāli app tiks izmantots ierīces tastatūru. Tastatūras pieredze var tikt mainīts atkarībā no tā, kas tiek izmantota ierīcē.</li>
<li><strong>Ciparu</strong> - par lauku nosaukumus, lietot ciparu ievades tikai, atlasiet šo opciju, lai rādītu pielāgotu cipartastatūru, nevis ierīces tastatūras ievades laukam.</li>
</ul></td>
</tr>
</tbody>
</table>

<a name="configure-warehouse-app-field-priority"></a>Konfigurēšana noliktavā app laukā Prioritāte
======================================

Par **noliktavas app lauku prioritāti** lapu, varat ievietot lauku nosaukumi dažādām prioritārajām grupām. Tas dod iespēju izlemt, kāda informācija jāparāda lapā galvenais uzdevums, kad noliktavas darbiniekiem veikt uzdevumus, izmantojot app. Ja noklikšķināsit uz **izveidot noklusēto iestatījumu**, tiks ģenerēti noklusējuma kopu prioritārajām grupām. Ir iespējams izveidot tik daudz prioritārās grupas, pēc vajadzības, bet tikai trīs prioritārās grupas tiks parādīta lapā uzdevums. Kad Dynamics 365 operācijām metadatus nosūta uz app, tā piešķir katram laukam relatīvā prioritāte, atkarībā no tās prioritāro grupu un app rādīs pirmo trīs prioritārās grupas ietverto uzdevumu lapas metadatus. Pārpildītā metadatu pārējo parādās sekundārās informācijas lapā. Nākamā tabula rāda piemēru no piecām prioritārajām grupām.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Prioritārās grupas</th>
<th>Piešķirtie lauki</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> 10. prioritāte</td>
<td><ul>
<li>Objekts</li>
<li>Daudzums</li>
<li>Mērvienība</li>
</ul></td>
</tr>
<tr class="even">
<td> 20. prioritāte</td>
<td><ul>
<li>Klastera pozīcija</li>
<li>Klasteris</li>
</ul></td>
</tr>
<tr class="odd">
<td> 30. prioritāte</td>
<td><ul>
<li>Preces apraksts</li>
</ul></td>
</tr>
<tr class="even">
<td> 40. prioritāte</td>
<td><ul>
<li>Konfigurācija</li>
<li>krāsa</li>
<li>izmērs</li>
<li>Stils</li>
</ul></td>
</tr>
<tr class="odd">
<td> 50. prioritāte</td>
<td><ul>
<li>Novietojums</li>
<li>Numura zīme</li>
</ul></td>
</tr>
</tbody>
</table>

Piemēram, ja noliktavas darbinieks veic uzdevumu mobilajās ierīcēs, ja metadatus, kas tiks rādīts app, kas sastāv no šādiem laukiem:

-   Objekts
-   Daudzums
-   Mērvienība
-   Preces apraksts
-   Lielumu un atrašanās vietu

Balstoties uz iepriekš tabulā noliktavas app lauku prioritāti, 3 rindas informācija tiks parādīti uzdevumu lapā:

-   1. rindā: Krājums, daudzums, mērvienība
-   2. rindā: Krājuma aprakstu
-   3. rindu: lielums

Atlikušos metadatus, piemēram, atrašanās vietu, netiks rādīti uzdevumu lapas, bet detaļu lappuse tiks parādīta. Lai uzzinātu vairāk un redzēt piemērus lietotāja interfeisu, atsaukties uz blog post [paziņojot Dynamics 365 operācijām - noliktavas](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).

<a name="see-also"></a>Skatiet arī
--------

[Jāinstalē un jākonfigurē Microsoft Dynamics 365 operācijām – noliktavas](install-configure-warehousing-app.md)


