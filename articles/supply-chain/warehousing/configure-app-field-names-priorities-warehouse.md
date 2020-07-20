---
title: Konfigurēt programmas lauku nosaukumus programmā Noliktava
description: Šajā tēmā ir aprakstīts, kā definēt un konfigurēt noliktavu programmas lauku nosaukumus un prioritātes programmatūrā Dynamics 365 Supply Chain Management.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7a4cfe62aa50c423adfd116a81d7962c30b25fcf
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530493"
---
# <a name="configure-app-field-names-in-the-warehouse-app"></a>Konfigurēt programmas lauku nosaukumus programmā Noliktava

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā definēt un konfigurēt noliktavu programmas lauku nosaukumus un prioritātes programmatūrā Dynamics 365 Supply Chain Management. 

> [!NOTE]
> Šī tēma attiecas uz moduļa Noliktavas vadība līdzekļiem. Tā neattiecas uz moduļa Krājumu vadība līdzekļiem. Noliktava ir lietojumprogramma, ko varat izmantot noliktavas uzdevumu veikšanai. Varat definēt un konfigurēt programmā lietoto lauku nosaukumus, kā arī konfigurēt prioritāti, kādai šie lauku nosaukumi ir jāpiešķir. Šajā tēmā ir paskaidrots, kā definēt un konfigurēt šos noliktavu programmas lauku nosaukumus un prioritātes un kā tie tiek izmantoti programmā Noliktava. Detalizētu informāciju par to, kā konfigurēt savienojumu ar programmu Noliktava, skatiet apmācībā [Noliktavas programmas instalēšanas un konfigurēšanas pārskats](install-configure-warehousing-app.md).

## <a name="configure-warehouse-app-field-names"></a>Konfigurēt noliktavas programmas lauku nosaukumus

Kad lietojat programmu Noliktava mobilajā ierīcē, lapā **Noliktavas programmu lauku nosaukumi** varat konfigurēt to, kā ierīcē ir jārāda metadati. Jaunā uzņēmumā atlasiet opciju **Izveidot noklusējuma iestatījumus**, lai ģenerētu visus lauku nosaukumus, kas tiks izmantoti noliktavas mobilo ierīču darbplūsmās, un pēc tam piešķiriet tiem vajadzīgo ievades režīmu un ievades veidu. Kad ir ģenerēti visi lauku nosaukumi, varat atlasīt tālāk norādītās ievades opcijas.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opcija</th>
<th>Apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Vēlamais ievades režīms</td>
<td>Šī opcija nosaka, vai atlasītajam lauka nosaukumam ir jārāda skenēšanas lauks vai manuālas ievades lauks. Šī opcija noder, lai laukus nodalītu atkarībā no tā, vai laukam ir jāizmanto svītrkodi. <strong>Piezīme.</strong> Ja svītrkods ir nenolasāms vai bojāts, tad lauku nosaukumiem, kuru vēlamais ievades režīms ir iestatīts uz <strong>Skenēšana</strong>, informāciju varat ievadīt arī manuāli.</td>
</tr>
<tr class="even">
<td>Ievades tips</td>
<td>Šī opcija nosaka, kāds ievades tips ir jālieto atlasītajam lauka nosaukumam. Ir pieejamas četras tālāk aprakstītās opcijas.
<ul>
<li><strong>Atlase</strong> - ietver sarakstu ar opcijām, no kurām varat izvēlēties. Izmantojot šo opciju, lauku nosaukumus nevar rediģēt.</li>
<li><strong>Datums</strong> - lauku nosaukumi, kas ir norādīti kā datumi, rādīs datuma formātu ar etiķeti. Šī opcija noliktavas darbiniekiem palīdz ieraudzīt, kādā formātā ir jāievada datums. Izmantojot šo opciju, lauku nosaukumus nevar rediģēt.</li>
<li><strong>Alfa</strong> - ja ir atlasīta šī opcija, tad tiek izmantota ierīces tastatūra, programmā manuāli ievadot informāciju. Tastatūras funkcionalitāti var mainīt atkarībā no tā, kura ierīce tiek lietota.</li>
<li><strong>Skaitlisks</strong> - lauku nosaukumiem, kas izmanto tikai skaitlisko ievadi, varat atlasīt šo opciju, lai ar ievades lauku rādītu pielāgotu cipartastatūru, nevis ierīces tastatūru.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a>Konfigurēt noliktavas programmas lauku prioritāti

Lapā **Noliktavas programmas lauku prioritāte** lauku nosaukumus varat salikt dažādās prioritāšu grupās. Šādi varat izlemt, kāda informācija ir jārāda galvenajā uzdevumu lapā, kad noliktavas darbinieki izpilda uzdevumus, izmantojot šo programmu. Ja noklikšķināt uz **Izveidot noklusējuma iestatījumus**, tiek ģenerēta prioritāšu grupu noklusējuma kopa. Varat izveidot tik prioritāšu grupu, cik vien nepieciešams, bet uzdevumu lapā tiks rādītas tikai trīs prioritāšu grupas. Kad no sistēmas uz programmu tiek sūtīti metadati, katram laukam tiek piešķirta relatīva prioritāte atkarībā no lauka prioritāšu grupas un programmas uzdevumu lapā tiek parādītas pirmās trīs metadatos ietvertās prioritāšu grupas. Pārējie metadati tiks rādīti sekundārās informācijas lapā. Nākamajā tabulā ir parādīts piemērs ar piecām prioritāšu grupām.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Prioritātes grupa</th>
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

Piemēram, kad noliktavas darbinieks izpilda kādu uzdevumu mobilajā ierīcē, ja programmā rādītie metadati sastāv no šādiem laukiem:

-   Objekts
-   Daudzums
-   Mērvienība
-   Preces apraksts
-   Izmērs un novietojums

Pamatojoties uz iepriekšējā tabulā iestatīto noliktavas programmas lauku prioritāti, uzdevumu lapā tiek rādītas šādas 3 informācijas rindas:

-   1. rinda: Prece, Daudzums, Mērvienība
-   2. rinda: Preces apraksts
-   3. rinda: Izmērs

Atlikušie metadati, piemēram, Novietojums, netiks rādīti uzdevumu lapā, bet tiks rādīti informācijas lapā. Papildinformāciju un lietotāja interfeisa piemērus skatiet emuāra ziņā [Paziņojums par Finance and Operations — Noliktava](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).

<a name="additional-resources"></a>Papildu resursi
--------

[Instalēt un konfigurēt noliktavas programmas pārskatu](install-configure-warehousing-app.md)
