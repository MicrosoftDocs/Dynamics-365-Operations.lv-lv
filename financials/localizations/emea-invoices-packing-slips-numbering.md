---
title: "Rēķinu un pavadzīmju numurēšana Latvijai un Lietuvai"
description: "Šajā tēmā ir paskaidrots, kā iestatīt numuru sērijas rēķiniem un pavadzīmēm un kā dokumentiem iestatīt pašnumerācijas diapazonus."
author: ShylaThompson
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LtInvoiceAutoNumberingGroups, LtInvoiceAutonumberingTable, NumberSequenceTableListPage
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 268484
ms.assetid: d7ff8162-bd5c-4582-a18a-144ce5e4c06f
ms.search.region: Latvia, Lithuania
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: c36db28260fc081f5667149bb52f9d3df0369490
ms.lasthandoff: 03/31/2017


---

# <a name="invoice-and-packing-slip-numbering-for-latvia-and-lithuania"></a>Rēķinu un pavadzīmju numurēšana Latvijai un Lietuvai

Šajā tēmā ir paskaidrots, kā iestatīt numuru sērijas rēķiniem un pavadzīmēm un kā dokumentiem iestatīt pašnumerācijas diapazonus.

Juridiskajām personām, kuru primārā adrese atrodas Latvijā vai Lietuvā, rēķiniem un pavadzīmēm varat iestatīt nosacījuma numerāciju, kas ir atkarīga no piešķirtā lietotāja vai lietotāju grupas.

## <a name="set-up-number-sequences-for-invoices-and-packing-slips"></a>Iestatīt numuru sērijas rēķiniem un pavadzīmēm
Pamatdatu ierakstiem un transakciju ierakstiem varat iestatīt unikālas dokumentu numuru sērijas. Ja jūsu valsts vai reģiona nodokļu iestādes jūsu organizācijai piešķir specifisku dokumentu numuru sēriju vai formātu, šo numuru sēriju varat saistīt ar kādu dokumentu tipu. Katru dokumentu numuru sēriju varat piešķirt kādam lietotājam vai lietotāju grupai. Šādi tikai norādītais lietotājs vai lietotāju grupa var dokumentam piešķirt sērijā iekļautos numurus. Numuru sērijas rēķiniem un pavadzīmēm varat iestatīt lapā **Rēķinu numerācijas iestatīšana**. (Noklikšķiniet uz **Organizācijas administrēšana** &gt; **Numuru sērijas** &gt; **Rēķinu numerācijas iestatīšana**.) Izmantojiet nākamajā tabulā sniegto informāciju, lai aizpildītu laukus lapā **Rēķinu numerācijas iestatīšana**.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Lauks</th>
<th>Apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Numerācija</td>
<td>Ievadiet dokumentu numuru sērijas prefiksu.</td>
</tr>
<tr class="even">
<td>Modulis</td>
<td>Atlasiet moduli, ko izmantos numuru sērijas. Jūsu atlasītais modulis nosaka, kādas opcijas ir pieejamas laukā <strong>Tips</strong>. Debitoru rēķiniem un debitoru pavadzīmēm šajā laukā atlasiet <strong>Pārdošana</strong>.</td>
</tr>
<tr class="odd">
<td>Numuru sērijas kods</td>
<td>Atlasiet numuru sērijas kodu datu apgabalam, kur šī numuru sērija tiek lietota.</td>
</tr>
<tr class="even">
<td>Tips</td>
<td>Atlasiet, vai numuru sērija attiecas uz rēķiniem vai uz pavadzīmēm.</td>
</tr>
<tr class="odd">
<td>Konta kods</td>
<td>Atlasiet, kā šī numuru sērija tiek lietota rēķiniem. Pieejamas šādas opcijas
<ul>
<li><strong>Tabula</strong> — šī numuru sērija ir pieejama tikai lietotājam, kurš ir atlasīts laukā <strong>Kods</strong>.</li>
<li><strong>Grupa</strong> — šī numuru sērija ir pieejama tikai grupai, kura ir atlasīta laukā <strong>Kods</strong>.</li>
<li><strong>Visi</strong> — šī numuru sērija ir pieejama visiem lietotājiem.</li>
</ul></td>
</tr>
<tr class="even">
<td>Kods</td>
<td>Atlasiet tā lietotāja vai lietotāju grupas ID, kuriem šī numuru sērija ir piešķirta rēķinu numurēšanai.</td>
</tr>
<tr class="odd">
<td>Pēdējais datums</td>
<td>Datums, kad numuru sērija tika atjaunināta pēdējo reizi.</td>
</tr>
<tr class="even">
<td>Turpināt</td>
<td>Atzīmējiet šo opciju, lai meklētu numuru sērijas, kas ir piešķirtas atlasītajam lietotājam vai lietotāju grupai.</td>
</tr>
</tbody>
</table>

## <a name="set-up-document-selfnumbering-ranges"></a>Iestatīt dokumentu pašnumerācijas diapazonus
Rēķiniem un pavadzīmēm, kas tiek ģenerēti moduļos **Debitoru parādi**, **Parādi kreditoriem**, **Krājumu vadība** un **Projektu vadība un uzskaite**, varat piešķirt specifiskas numuru sērijas. Atsevišķas numuru sērijas varat norādīt arī dažādiem lietotājiem un lietotāju grupām, debitoru grupām un kreditoru grupām, vai noliktavām. Lai iestatītu numuru sērijas debitoru rēķiniem un kreditoru rēķiniem, izmantojiet lapu **Skaitītāju pārvaldība**. (Noklikšķiniet uz **Organizācijas administrēšana** &gt; **Numuru sērijas** &gt; **Skaitītāju pārvaldība**.) Numuru sēriju varat definēt pēc lietotāja vai lietotāju grupas vai specifiskām debitoru grupām un kreditoru grupām. Lai aizpildītu laukus lapā **Skaitītāju pārvaldība**, izmantojiet nākamajā tabulā sniegto informāciju.

| Lauks          | Apraksts                                                                                                                                     |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Modulis         | Atlasiet moduli, uz ko attiecas atlasītā numuru sērija.                                                                                 |
| Konta kods   | Atlasiet, vai numuru sērijas kods attiecas uz visiem ierakstiem atlasītajā modulī vai tikai uz specifisku grupu šajā modulī.                     |
| Kods           | Atlasiet kodu atlasītajam modulim. **Piezīme.** Lauks **Kods** ir pieejams tikai tad, ja laukā **Konta kods** ir atlasīta opcija **Grupa**. |
| Tips           | Atlasiet numurējamo dokumentu tipu: **Rēķins** vai **Pavadzīme**.                                                                         |
| Automātiska numerācija | Atzīmējiet šo opciju, lai numuru dokumentam piešķirtu automātiski. Atsevišķiem dokumentiem šo opciju varat manuāli atzīmēt vai noņemt tās atzīmi.       |

Papildinformāciju par to, ka manuāli numurēt rēķinus un pavadzīmes, skatiet rakstā [(EEU) Labot rēķina ID pārdošanas pasūtījumos](https://ax.help.dynamics.com/en/?post_type=incsub_wiki&p=1162853&preview=true).

## <a name="affected-processes"></a>Ietekmētie procesi
Izmantojot rēķinu un pavadzīmju numurēšanu, tiek atjauninātas tālāk uzskaitīto dokumentu galvenes.

-   Pārdošanas pasūtījumi
-   Pirkšanas pasūtījumi
-   Brīvā teksta rēķini
-   Projekta rēķinu priekšlikumi

Kad grāmatojat tālāk norādītos dokumentus, laukā **Numerācija** varat atlasīt specifisku numuru sēriju.

-   Pārdošanas pavadzīme
-   Pārdošanai grāmatojot rēķinu
-   Pirkšanai grāmatojot produktu ieejas plūsmu
-   Pirkšanas kreditora rēķini
-   Grāmatojiet projekta rēķinu priekšlikumus
-   Grāmatot brīva teksta rēķinu

Turklāt tālāk norādītās formas tiek papildinātas ar lauku **Atjaunināmie dokumenti**.

-   Pirkšanas kreditora rēķinu forma
-   Pārdošanas pavadzīmes grāmatošanas forma
-   Pārdošanas rēķina grāmatošanas forma
-   Pirkšanas produktu ieejas plūsmas grāmatošanas forma

Lauks “**Atjaunināmie dokumenti**” ietekmē lauku “**Dokumenta statuss**” žurnālā “**Pavadzīmju žurnāls**” un "**Rēķinu žurnāls**". Veidojot dokumentu **Pavadzīme**, lauka “**Dokumenta statuss**”vērtība ir vienāda ar vērtību “**Nav**”. Ja laukā “**Atjaunināmie dokumenti**” tika izvēlēta kāda **Pavadzīme**, tad tās “**Dokumenta statuss**” ir “**Bojāts**”, bet “**Dokumenta statuss**” tādam dokumentam **Pavadzīme**, kur tas tika izdarīts, ir “**Atcelts**”.


