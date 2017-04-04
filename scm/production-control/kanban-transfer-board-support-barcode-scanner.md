---
title: "Kanban nodošanu valdes atbalsts par Svītrkods skeneri"
description: "Kanban pārsūtīšanas panelis nodrošina skenera ievadi, izmantojot logrīka svītrkoda skeneri, lai atlasītu, sāktu, pabeigtu un iztukšotu Kanban darbu."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: f393efaf011de103fc172af625816eef5915c642
ms.lasthandoff: 03/31/2017


---

# <a name="kanban-transfer-board-support-for-barcode-scanners"></a>Kanban nodošanu valdes atbalsts par Svītrkods skeneri

Kanban pārsūtīšanas panelis nodrošina skenera ievadi, izmantojot logrīka svītrkoda skeneri, lai atlasītu, sāktu, pabeigtu un iztukšotu Kanban darbu.

<a name="registration-modes"></a>Reģistrācijas režīmi
------------------

Kopsavilkuma cilnē **Skenera reģistrācija** varat atlasīt reģistrācijas režīmu, kas nosaka to, kāda darbība tiek veikta, skenējot Kanban kartes numuru vai manuāli ievadot numuru laukā Kanban kartes numurs.
| Iestatīt reģistrācijas režīmu | Apraksts                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| Sākums                 | Kanban pārsūtīšanas darbs tiek reģistrēts kā notiekošs.                                                 |
| Pabeigt              | Kanban pārsūtīšanas darbs tiek reģistrēts kā pabeigts.                                                   |
| Tukšs                 | Materiālu apstrādes vienība, uz ko ir atsauces Kanban kartē, tiek reģistrēta kā tukša.              |
| Atlasīt                | Tiek reģistrēts Kanban kartes numurs, un Kanban sarakstā tiek automātiski atlasīts atsauces darbs. |

 
<a name="registration-mode-select"></a>Reģistrācijas režīms Atlasīt
------------------------

Ja izmantojat svītrkoda lasītājs izvēlēties darbu, tā parādīšanas režīma kanban valdes izmaiņas. Šajā režīmā, piemēro šādus nosacījumus:

-   Tiek rādīts tikai ieskenētais Kanban darbs.
-   Kopsavilkuma cilnē **Detalizēti** tiek rādīta detalizēta informācija par atlasīto darbu.
-   Kopsavilkuma cilnē **Ziņojumi** tiek rādīti tikai ar atlasīto darbu saistītie ziņojumi.
-   Darba statusu var mainīt, izmantojot darbību rūti pieejamās funkcijas. Šajā laikā Kanban pārsūtīšanas panelī joprojām tiek rādīts tikai viens darbs.
-   Informāciju sarakstā darba vietu var atjaunināt manuāli, noklikšķinot uz **atsvaidzināt** (Shift + F5) darbību rūtī. Pēc informācijas atsvaidzināšanas atkal tiek rādīti visi darbu filtra rezultāti.

## <a name="job-status-and-possible-actions"></a>Darbu statuss un iespējamās darbības
Atlasīta darba statuss un jebkuru notikumu Kanban piesaistīto darbu statuss nosaka, vai varat turpināt darba apstrādi. Tālāk esošajā tabulā ir sniegta informācija par šiem statusiem un uzdevumiem.
-   Statusi, kas ir pieejami darbiem vai materiālu apstrādes vienībām, uz kurām ir atsauces šajos darbos.
-   Katrs uzdevums, ko varat veikt konkrētajam darbam.

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th>Darba tips</th>
<th>Darba statuss vai materiālu apstrādes vienības statuss</th>
<th>Atjauniniet izdošanas sarakstu</th>
<th>Sākums</th>
<th>Atjaunināt reģistrāciju</th>
<th>Pabeigt</th>
<th>Tukšs</th>
<th>Izveidot notikumu Kanban</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Pārcelšana</td>
<td><ul>
<li>Neplānots</li>
<li>Nav piesaistīto darbu, vai piesaistītie darbi ir pabeigti</li>
</ul></td>
<td>Jā</td>
<td>Jā</td>
<td>Jā</td>
<td>Jā</td>
<td>Nē</td>
<td>Jā</td>
</tr>
<tr class="even">
<td>Pārcelšana</td>
<td><ul>
<li>Neplānots</li>
<li>Piesaistītais darbs nav pabeigts</li>
</ul></td>
<td>Jā</td>
<td>Nē</td>
<td>Jā</td>
<td>Nē</td>
<td>Nē</td>
<td>Nē</td>
</tr>
<tr class="odd">
<td>Pārcelšana</td>
<td>Notiek</td>
<td>Jā</td>
<td>Nē</td>
<td>Jā</td>
<td>Jā</td>
<td>Nē</td>
<td>Nē</td>
</tr>
<tr class="even">
<td>Pārcelšana</td>
<td>Pabeigts</td>
<td>Nē</td>
<td>Nē</td>
<td>Nē</td>
<td>Nē</td>
<td>Jā</td>
<td>Nē</td>
</tr>
<tr class="odd">
<td>Pārsūtīšana vai apstrāde</td>
<td>Tukšs</td>
<td>Nē</td>
<td>Nē</td>
<td>Nē</td>
<td>Nē</td>
<td>Nē</td>
<td>Nē</td>
</tr>
<tr class="even">
<td>Pārsūtīšana vai apstrāde</td>
<td>Nav atrasta Kanban karte</td>
<td>Nē</td>
<td>Nē</td>
<td>Nē</td>
<td>Nē</td>
<td>Nē</td>
<td>Nē</td>
</tr>
<tr class="odd">
<td>Pārsūtīšana vai apstrāde</td>
<td>Ir atrasta Kanban karte, taču tā nav piešķirta Kanban</td>
<td>Nē</td>
<td>Nē</td>
<td>Nē</td>
<td>Nē</td>
<td>Nē</td>
<td>Nē</td>
</tr>
<tr class="even">
<td>Apstrādāšana</td>
<td><ul>
<li>Neplānots</li>
<li>Sagatavots</li>
<li>Notiek</li>
</ul></td>
<td>Nē</td>
<td>Nē</td>
<td>Nē</td>
<td>Nē</td>
<td>Nē</td>
<td>Nē</td>
</tr>
<tr class="odd">
<td>Apstrādāšana</td>
<td>Pabeigts</td>
<td>Nē</td>
<td>Nē</td>
<td>Nē</td>
<td>Nē</td>
<td>Nē</td>
<td>Nē</td>
</tr>
</tbody>
</table>




