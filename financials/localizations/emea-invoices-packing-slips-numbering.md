---
title: "Rēķinu un pavadzīmju numurēšanai, Latvija un Lietuva"
description: "Šajā tēmā ir paskaidrots, kā iestatīt numuru sērijas, rēķiniem un pavadzīmēm un kā uzstādīt self-numerācijas diapazoni dokumentiem."
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

# <a name="invoice-and-packing-slip-numbering-for-latvia-and-lithuania"></a>Rēķinu un pavadzīmju numurēšanai, Latvija un Lietuva

Šajā tēmā ir paskaidrots, kā iestatīt numuru sērijas, rēķiniem un pavadzīmēm un kā uzstādīt self-numerācijas diapazoni dokumentiem.

Juridiskām personām, kas ir primārā adrese, Latvija vai Lietuva, var iestatīt nosacījuma numerācijas rēķiniem un pavadzīmēm, ko ir balstīts uz piešķirtais lietotājs vai lietotāju grupa.

## <a name="set-up-number-sequences-for-invoices-and-packing-slips"></a>Iestatiet numuru sērijas rēķiniem un pavadzīmēm
Unikāla dokumentu numuru sērijas pamatdatu ierakstus un transakciju ierakstus var iestatīt. Ja nodokļu iestādes jūsu valstī vai reģionā piešķirtu jūsu organizācijai konkrētu dokumentu numuru sēriju vai formātā, numuru sēriju var saistīt ar dokumenta tipu. Katra numuru sērijas dokumenta numurs var piešķirt lietotājam vai lietotāju grupai. Šādā veidā, tikai izraudzītās lietotājam vai lietotāju grupai var piešķirt numuru sērijas dokumentu. Varat iestatīt numuru sērijas rēķinu un pavadzīmju par **rēķinu numerācijas iestatīšanas** lapā. (Noklikšķiniet uz **organizācijas administrācija**&gt;**numuru sērijas**&gt;**rēķinu numerācijas iestatīšanas**.) Izmantot informāciju tabulā pabeigšanai laukos par **rēķinu numerācijas iestatīšanas** lapā.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Lauks</th>
<th>apraksts</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Numerācija</td>
<td>Ievadītu prefiksa dokumenta numuru sērijai.</td>
</tr>
<tr class="even">
<td>Modulis</td>
<td>Atlasiet moduli, ko izmanto numuru sērijas. Moduli, ko atlasāt, nosaka opcijas, kas pieejamas programmā <strong>tipa</strong> lauks. Klienta rēķiniem un izmantoti par pamatu Klienta pavadzīmes nosūtīšanai, izvēlieties <strong>pārdošanas</strong> šajā jomā.</td>
</tr>
<tr class="odd">
<td>Numura sērijas kods</td>
<td>Atlasiet numuru sērijas kodu datu apgabalā, kurā piemēro numuru sērijas.</td>
</tr>
<tr class="even">
<td>tips</td>
<td>Atlasiet, vai numuru sērijas, kas attiecas uz rēķinos vai pavadzīmēs.</td>
</tr>
<tr class="odd">
<td>Konta kods</td>
<td>Atlasiet, cik numuru sērija tiek lietota rēķinus. Pieejamas šādas opcijas
<ul>
<li><strong>Galda</strong> – būs pieejama tikai tam lietotājam, kas atlasīts elementā numuru sērijas <strong>koda</strong> lauks.</li>
<li><strong>Grupas</strong> -numuru sērija ir pieejama uz lietotāju grupu, kas atlasīta <strong>koda</strong> lauks.</li>
<li><strong>Visas</strong> -numuru sērija ir pieejama visiem lietotājiem.</li>
</ul></td>
</tr>
<tr class="even">
<td>Kods</td>
<td>Atlasiet ID lietotājam vai lietotāju grupai, kas numuru sērijas tiek piešķirta rēķinu numurēšanai.</td>
</tr>
<tr class="odd">
<td>Pēdējais datums</td>
<td>Datums, kurā pēdējo reizi tika atjaunināts numuru sērijas.</td>
</tr>
<tr class="even">
<td>Turpināt</td>
<td>Atlasiet šo opciju, lai meklētu numuru sērijai, kura ir piešķirta atlasītajam lietotājam vai lietotāju grupai.</td>
</tr>
</tbody>
</table>

## <a name="set-up-document-selfnumbering-ranges"></a>Iestatīt dokumenta selfnumbering diapazonus
Rēķiniem un pavadzīmēm, kas tiek veidotas, var piešķirt īpašu numuru sērijas **Debitori**, **kreditoru parādi**, **krājumu vadība**, un **projekta vadības un grāmatvedības** moduļi. Varat arī norādīt individuālu numuru sērijas dažādiem lietotājiem un lietotāju grupām, klientu grupas un kreditoru grupām vai noliktavas. Iestatiet numuru sērijas debitoru un kreditoru rēķini, izmantojiet **skaitītāju pārvaldība** lapā. (Noklikšķiniet uz **organizācijas administrācija**&gt;**numuru sērijas**&gt;**skaitītāju pārvaldība**.) Var definēt lietotājam vai lietotāju grupai vai noteiktai debitoru un kreditoru grupas numuru sēriju. Izmantot informāciju tabulā pabeigšanai laukos par **skaitītāju pārvaldība** lapā.

| Lauks          | apraksts                                                                                                                                     |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Modulis         | Atlasiet moduli, uz kuru attiecas atlasītajā numuru sērijā.                                                                                 |
| Konta kods   | Atlasiet, vai numuru sērijas kodu, kas attiecas uz visiem ierakstiem atlasītā modulī vai konkrēta grupa modulī.                     |
| Kods           | Atlasiet kodu atlasītajai modulim. **Piezīme:****koda** lauks ir pieejams tikai tad, ja **grupas** atlasīta **konta kods** lauks. |
| tips           | Atlasiet dokumenta tipu, lai numuru: **rēķina** vai **pavadzīmes**.                                                                         |
| Automātiska numerācija | Atlasiet šo opciju, lai automātiski piešķirtu dokumenta numuru. Varat manuāli atzīmējiet vai notīriet šo opciju, lai atsevišķus dokumentus.       |

Lai uzzinātu, kā manuāli numuru rēķiniem un pavadzīmēm, sk [(EEK) rediģēt rēķinu ID pārdošanas pasūtījumos](https://ax.help.dynamics.com/en/?post_type=incsub_wiki&p=1162853&preview=true).

## <a name="affected-processes"></a>Ietekmē procesus
Šādus dokumentus galvenes tiek atjaunināts ar pavadzīmes rēķini un pavadzīmes numerāciju:

-   Pārdošanas pasūtījumi
-   Pirkšanas pasūtījumi
-   Brīvā teksta rēķini
-   Projekta rēķinu priekšlikumi

Kad jūs publicējat šādus dokumentus, varat atlasīt īpašu numuru sērijai elementā **numerācija** jomā:

-   Pārdošanas pavadzīmi
-   Pārdošanas grāmatošana rēķinu
-   Pirkšanas grāmatošana produkta saņemšanas
-   Iegādājoties kreditoru rēķinus
-   Grāmatojiet projekta rēķinu priekšlikumus
-   Grāmatot brīva teksta rēķinu

Turklāt formu zemāk doti arī **dokumentus, lai atjauninātu** jomā:

-   Iepirkuma piegādātāja rēķinu veidlapas,
-   Pārdošanas pavadzīmes grāmatošanas formā,
-   Pārdošanas rēķinu grāmatošanas formā,
-   Pirkšanas grāmatošana produkta saņemšanas veidlapu.

"**Dokumentus, lai atjauninātu**" lauka ietekme uz "**dokumenta statusu**"laukā"**iepakošanas slīdēšanas žurnāla**"un"**rēķinu žurnāla**". Par **pavadzīmes** radīšanu, "**dokumenta statusu**"lauka vērtība ir vienāda ar"**neviens**". Ja tādi **pavadzīmes** tika izvēlēts lauks "**dokumentus, lai atjauninātu**", tad tās"**dokumenta statusu**"būtu"**Broken**"un"**dokumenta statusu**" par **pavadzīmes** kur tas tika darīts, būs "**atcelts**".


