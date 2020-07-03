---
title: Iestatīt apmācību kursus
description: Personāla vadības administratori un vadītāji var izmantot šos kursu līdzekļus, lai uzturētu informāciju par darbiniekiem piedāvāto apmācību.
author: andreabichsel
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 253f0d07679b6327a0ed1e3cc20ede66249750b8
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429340"
---
# <a name="set-up-training-courses"></a>Iestatīt apmācību kursus

Personāla vadības administratori un vadītāji var izmantot šos kursu līdzekļus, lai uzturētu informāciju par darbiniekiem piedāvāto apmācību.

 <a name="set-up-prerequisites"></a>Priekšnoteikumu iestatīšana
---------------------

Pirms veidojat kursus, ir nepieciešama un ir jāiestata tālāk norādītā informācija.
-   **Kursu tipi**

Tālāk minēta izvēles informācija, ko var norādīt kursiem. Ja zināt, ka ievadīsiet šo informāciju kursiem, jums jāiestata šī informācija pirms kursu ierakstu izveidošanas.
-   **Klases grupas**
-   **Kursu grupas**
-   **Kursu atrašanās vietas**
-   **Klases telpas**
-   **Instruktori**

## <a name="course-types"></a>Kursu tipi
Kursu tipus var izmantot, lai kategorizētu kursus atbilstoši to struktūrai vai saturam. Kursu tipus varat izveidot lapā **Kursu tipi**. Veidojot kursu ierakstu, ir jāatlasa kursu veids.

## <a name="course-setup-type"></a>Kursu iestatīšanas veids
Tālāk esošajā tabulā uzskaitīti trīs kursu iestatījumu veidi. Iestatījumu veidi nosaka kursu struktūru.

<table>
<thead>
<tr class="header">
<th>Iestatījumu veidi</th>
<th>Apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Standarta</strong></td>
<td>Atlasiet šo veidu kursiem, kam nav ikdienas darba kārtības. Šis ir noklusētais iestatījumu veids, veidojot jaunus kursus.</td>
</tr>
<tr class="even">
<td><strong>Darba kārtība</strong></td>
<td>Atlasiet šo veidu, lai plānotu katras kursa dienas detalizēto informāciju tādam kursam, kas notiek vairākas dienas.</td>
</tr>
<tr class="odd">
<td><strong>Darba kārtībā + sesija</strong></td>
<td>Atlasiet šo veidu sarežģītākiem kursiem. Piemēram, kursu darba kārtību var sadalīt tēmās un sesijās.
<ul>
<li><strong>Tēma</strong> — tēmas ir kursu specifiskās jomas.</li>
<li><strong>Sesijas</strong> — tēmas ir sīkāk sadalītas sesijās, un sesijas palīdz identificēt tēmai specifiskos procesus vai metodes.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a>Kursu uzdevumi
Katram kursam var izpildīt šādus uzdevumus.
- Reģistrēt dalībniekus
- Norādīt reģistrācijas termiņu
- Definēt minimālo un maksimālo dalībnieku skaitu
- Piešķirt kursa atrašanās vietu un mācību telpu
- Kursu dalībniekiem ieteikt viesnīcas
- Veidot kursa aprakstu, ko pēc tam varat reklamēt darbinieku pašapkalpošanās pakalpojumā

  >**Piezīme.** Kursu varat dzēst tikai tad, ja tam neviens nav reģistrējies. 

## <a name="course-statuses"></a>Kursu statusi
Tālāk esošajā tabulā uzskaitīti iespējamie kursu statusi un darbības, kuras varat pabeigt, kad kursam ir specifisks statuss.

<table>
<thead>
<tr class="header">
<th>Statuss</th>
<th>Darbības</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Izveidots</strong></td>
<td><ul>
<li>Ievadiet un modificējiet kursu informāciju.</li>
<li>Kursu statusu mainiet uz <strong>Atvērts</strong>, lai darbinieki varētu reģistrēties šim kursam.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Atvērts</strong></td>
<td><ul>
<li>Reģistrējiet dalībniekus kursiem.</li>
<li>Dzēsiet kursu dalībniekus.</li>
<li>Apstipriniet kursu dalībniekus.</li>
<li>Mainiet kursa statusu uz <strong>Slēgts</strong> vai <strong>Atcelts</strong>.</li>
<li>Plānojiet anketas darbiniekiem, kuru statuss ir <strong>Apstiprināts</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Slēgts</strong></td>
<td>Kursus var atvērt atkārtoti.</td>
</tr>
<tr class="even">
<td><strong>Atcelts</strong></td>
<td>Kursus var atvērt atkārtoti.</td>
</tr>
</tbody>
</table>

## <a name="course-participants"></a>Kursu dalībnieki
Kursu dalībnieki ir darbinieki, kuri piedalās apmācības kursos vai notikumā. Dalībniekus var reģistrēt tikai atvērtiem kursiem. Minimālais un maksimālais dalībnieku skaits, ko varat reģistrēt vienam kursam, ir noteikts kopsavilkuma cilnē **Vispārīgi**, lapā **Kursi**.

<a name="workflow"></a>Darbplūsma
--------

Darbinieki, kuri kursam ir reģistrējušies, izmantojot lapu **Darbinieku pašapkalpošanās**, savu reģistrāciju var maršrutēt apstiprināšanai caur darbplūsmu. Darbplūsmu kursam varat piešķirt kopsavilkuma cilnē **Vispārīgi**, lapā **Kursi**.





