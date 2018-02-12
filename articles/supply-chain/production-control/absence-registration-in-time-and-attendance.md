---
title: "Kavējuma reģistrēšana sadaļā Laiks un apmeklētība"
description: "Šajā tēmā ir paskaidros, kā reģistrēt kavējumu sadaļā Laiks un apmeklētība."
author: johanhoffmann
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 477724e6211a084638e8a0b7133f60edef07b3ad
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="absence-registration-in-time-and-attendance"></a>Kavējuma reģistrēšana sadaļā Laiks un apmeklētība

[!include[banner](../includes/banner.md)]

Šajā tēmā ir aprakstīti kavējuma jēdzieni un ir paskaidrots, kā reģistrēt kavējumu sadaļā Laiks un apmeklētība.

## <a name="absence-that-is-based-on-regular-work-hours"></a>Kavējums, pamatojoties uz parasto darba laiku

Par nodarbinātā kavējumu tiek uzskatīts viss laiks, ko nodarbinātais nestrādā savā parastajā darba laikā. Parastais darba laiks ir definēts nodarbinātā standarta laika profilā.

Piemēram, nodarbinātais strādā atbilstoši dienas profilam ar ierašanās laiku plkst. 7:00 un aiziešanas laiku plkst. 15:00. Ja nodarbinātais ierodas plkst. 9:00, tiek uzskatīts, ka viņš šajā dienā ir kavējis darbu no plkst. 7:00 līdz plkst. 9:00.

Šādā gadījumā noradinātajam tiek prasīts ievadīt kavējuma iemeslu. Viņi var norādīt iemeslu, atlasot kavējuma kodu.

## <a name="absence-codes"></a>Kavējumu kodi

Kavējumu kodi atbilst dažādajiem kavējumu veidiem. Kavējumu kodus definē uzņēmums.

Kavējumu kodiem var lietot dažādas kārtulas. Piemēram, kavējuma kodu var konfigurēt tā, lai samazinātu vai palielinātu algu.

Piemēram, uzņēmums definē kavējuma kodu **Vēlu**, ko nodarbinātie izmanto, ja ir ieradušies vēlu bez pamatota iemesla. Uzņēmums definē arī kavējuma kodu **Iekšējais mācību kurss**, ko nodarbinātie izmanto, lai reģistrētu laiku, ko viņi ir patērējuši iekšējo mācību kursu apmeklējumam. Šos kavējumu kodus var iestatīt tā, lai kods **Vēlu** izraisītu nodarbinātā algas samazināšanu, bet kods **Iekšējais mācību kurss** neizraisītu nodarbinātā algas samazināšanu.

Varat iestatīt automātiskus kavējumu kodus. Šos kavējumu kodus var izmantot, lai aprēķinātu nodarbinātā darba laiku, kad nav reģistrēti kavējumi. No nodarbinātā laika profila ir atkarīgs tas, vai tiek lietots standarta laika vai brīvā režīma kavējuma kods.

### <a name="set-up-standard-time-and-flex-time"></a>Standarta laika un brīvā režīma iestatīšana

- Konfigurējiet standarta laika un brīvā režīma parametrus, izmantojot opcijas **Automātiski ievietot kavējumu** un **Automātiski ievieto brīvo režīmu-** lapā **Laika un apmeklētības parametri**.

## <a name="absence-groups"></a>Kavējumu grupas

Kavējumi kodi tiek grupēti kavējumu grupās. Izmantojot kavējumu grupas, varat grupēt kavējumu kodus, kam ir kopīgas īpašības. Piemēram, kavējuma kodus, kas ir saistīti ar atļautiem kavējumiem vai kavējumiem ārsta apmeklējuma, zvērinātā pienākumu vai bērna saslimšanas dēļ.

## <a name="planned-absence"></a>Plānotā prombūtne

Ja zināt, ka nodarbinātais kavēs darbu noteiktu laika periodu, piemēram, gaidāma atvaļinājuma dēļ, varat izmantot plānotu kavējumu. Plānotu kavējumu var iestatīt, konfigurējot kavējuma kodu tā, lai tiktu ņemts vērā plānotais kavējums. Ja esat iestatījis plānotu kavējumu, kavējuma periodā netiek prasīts ievadīt kavējuma kodu, kad tiek aprēķinātas lietotāja laika reģistrācijas. Varat definēt viena nodarbinātā plānotu kavējumu vai pakešuzdevumu, lai atjaunotu plānotos kavējumu vairākiem nodarbinātajiem vienlaikus.

### <a name="set-up-planned-absence"></a>Plānota kavējuma iestatīšana

1. Atlasiet **Personāla vadība** &gt; **Nodarbinātie** &gt; **Darbinieki** un atlasiet darbinieku.
2. Atlasiet **Laiks** &gt; **Laika piešķires** &gt; **Kavējuma laika reģistrācija** un iestatiet plānoto kavējumu.

## <a name="interrupted-planned-absence"></a>Pārtraukts plānotais kavējums

Ja, iestatot plānotu kavējumu, izmantojat opciju **Pārtraukt**, plānotais kavējums tiek pārtraukts gadījumā, ja nodarbinātais pierakstās plānotā kavējuma perioda laikā. Plānotais kavējums tiek apzīmēts kā **Pārtraukts** un neietekmē turpmākos aprēķinus.

### <a name="set-up-a-planned-absence-for-interruption"></a>Pārtraucama plānota kavējuma iestatīšana

1. Atveriet lapu **Kavējuma laika reģistrācija**, kā tas ir norādīts plānota kavējuma iestatīšanas procedūras aprakstā.
2. Atlasiet **Pārtraukt**.

Opcija **Pārtraukt** tiek lietota, ja ražotnes terminālī vai ražotnes ierīcē tiek reģistrēts laiks. Šī opcija netiek lietota, ja reģistrācija tiek veikta aprēķina un apstiprinājuma lapās vai lapā **Elektroniskā darba laika uzskaites karte**.

## <a name="examples-of-the-use-of-absence-in-a-flex-profile"></a>Piemēri kavējumu lietošanai brīvā režīma profilā

Tālāk ir sniegti trīs piemēri tam, kā kavējumi tiek aprēķināti profilā, kam ir iestatīti brīvā grafika periodi.

Piemēros ir izmantots tālāk norādītais profils.

| Ierašanās | Standarta laiks    | Pārtraukums             | Standarta laiks | Brīvais režīms-        | Aiziešana | Brīvais režīms +        |
|----------|------------------|-------------------|---------------|--------------|-----------|--------------|
| 8:00     | No 9:00 līdz 11:30 | No 11:30 līdz 12:00 | No 12:00 līdz 15:00 | No 15:00 līdz 16:00 | 16:00      | No 16:00 līdz 18:00 |

### <a name="example-1-signing-out-during-a-flex--period"></a>1. piemērs: izrakstīšanās brīvā režīma- periodā

Nodarbinātais ierodas darbā plkst. 8:00 un aiziet plkst. 15:30. Šāda gadījumā netiek aprēķināts kavējums un no nodarbinātā brīvā režīma bilances tiek noņemta pusstunda, jo nodarbinātais ir aizgājis brīvā režīma- periodā.

### <a name="example-2-signing-out-in-during-standard-time-period"></a>2. piemērs: izrakstīšanās standarta laika periodā

Nodarbinātais ierodas darbā plkst. 8:00 un aiziet plkst. 14:30. Šādā gadījumā tiek aprēķināts kavējums no plkst. 14:30 līdz plkst. 16:00 un tiek reģistrēts 1,5 stundas ilgs kavējuma periods, jo nodarbinātais ir aizgājis standarta laika periodā. Šim periodam ir jānorāda kavējuma kods.

### <a name="example-3-signing-out-during-a-flex-period"></a>3. piemērs: izrakstīšanās brīvā režīma+ periodā

Nodarbinātais ierodas darbā plkst. 8:00 un aiziet plkst. 16:30. Šāda gadījumā netiek aprēķināts kavējums un nodarbinātā brīvā režīma bilancei tiek pievienota pusstunda, jo nodarbinātais ir aizgājis brīvā režīma+ periodā.

## <a name="absence-in-the-calculation-and-approval-process"></a>Darbs ar kavējumiem aprēķināšanas un apstiprināšanas procesa laikā

Darbinieku laika reģistrācijas ir jāaprēķina un jāapstiprina, pirms tās var pārsūtīt uz algu sistēmu kā apmaksas elementus.

Apstiprinātājs var mainīt nodarbinātā laika reģistrācijas. Apstiprinātājs var pat mainīt jebkuru nodarbinātā reģistrēto kavējumu. Ja apstiprinātājs manuāli ievada laika periodu ar kavējuma kodu, šī perioda kavējuma kods netiek aizstāts ar noklusējuma apmeklējuma kodu, kas ir norādīts sadaļā Laika un apmeklētības parametri.

Piemēram, nodarbinātā ierodas darbā plkst. 10:00 un atlasa kavējuma kodu, kas norāda, ka viņa ir ieradusies vēlu. Vēlāk darbiniece informē vadītāju, ka laikā no plkst. 8:00 līdz plkst. 10:00 viņa apmeklēja ārstu. Ārsta apmeklējums nedrīkst izraisīt nodarbinātās algas samazināšanu. Tāpēc šajā gadījumā vadītājs var pielāgot divas kavējuma stundas no plkst. 8:00 līdz plkst. 10:00, šīm divām stundām manuāli ievadot kavējuma kodu, kas norāda saslimšanu.

### <a name="calculate-and-approve-absence"></a>Kavējuma aprēķināšana un apstiprināšana

- Atlasiet **Apmeklētības laiks** &gt; **Pārskatīt un apstiprināt** &gt; **Apstiprināt vai aprēķināt**.

