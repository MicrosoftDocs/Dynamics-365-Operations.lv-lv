---
title: Atlaižu rādīšana punktā POS
description: Šajā tēmā izskaidrots, kā Microsoft Dynamics 365 Commerce palīdz pārdošanas asistentiem uzzināt par veicināšanas pasākumiem, un kā tos izmantot šķērspārdošanā un piedāvājumos.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 07/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-Commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Commerce
ms.author: asharchw
ms.search.validFrom: 2020-02-28
ms.dyn365.ops.version: Application update 10.0.10
ms.openlocfilehash: 3934390b86f821233c2620405e316cf732b3d7bf
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230620"
---
# <a name="show-discounts-in-pos"></a>Rādīt atlaides punktā POS

[!include [banner](includes/banner.md)]

Veicināšanas pasākumiem ir svarīga loma, motivējot klientus, kuri pieņem pirkšanas lēmumus. Piemēram, brīvdienas var radīt vislielāko pārdošanas apjomu mazumtirgotājiem, jo viss mazumtirdzniecības tirgus tiek pārpludināts ar vilinošiem veicināšanas pasākumiem un atlaidēm. Ja veikalu sadarbības partneri ir informēti par un izprot pieejamos veicināšanas pasākumus, viņi var viegli izmantot šos veicināšanas pasākumus, lai šķērspārdotu un piedāvātu preces. Šajā tēmā izskaidrots, kā Microsoft Dynamics 365 Commerce palīdz pārdošanas asistentiem uzzināt par veicināšanas pasākumiem, un kā tos izmantot šķērspārdošanā un piedāvājumos.

## <a name="learn-about-store-discounts"></a>Uzziniet par veikalu atlaidēm

Commerce ietver operāciju ar nosaukumu "Skatīt visas atlaides". Šī operācija parāda visas atlaides, kas pašlaik tiek darbinātas veikalā. Operāciju "Skatīt visas atlaides" var kartēt uz pogu pārdošanas punktā (POS), un šo pogu var pievienot **Sveiciena** lapai vai **Transakcijas** lapai. Nākamajā attēlā ir parādīts atvērtas lapas **Visas atlaides**.

![Visu atlaižu lapa](./media/View_all_discounts.png "Visu atlaižu lapa")

Lai parādītu atlaides, sistēma meklē visas atlaides, kas atbilst vienam vai vairākiem no šādiem nosacījumiem:

- Atlaides cenu grupa atbilst veikala cenu grupai.
- Atlaides cenu grupa tiek kartēta uz piederības vai lojalitātes programmu.
- Atlaides cenu grupa tiek kartēta uz katalogu, kas ir saistīts ar veikalu.

Lapā **Visas atlaides** tiek rādītas tikai dažas kupona atlaide, jo mazumtirgotāji parasti veido tūkstošiem kuponu un atbilstošas atlaides unikāliem klientiem, un šī lapa nav paredzēta, lai rādītu klientiem specifiskas atlaides. Kuponu atlaides tiek rādītas vienīgi tad, ja katrā kupona galvenē tiek ieslēgta opcija **Piemērot bez kupona koda**. Šādā gadījumā kasieri var piemērot kuponu bez nepieciešamības ievadīt vai skenēt kupona kodu vai svītrkodu.

Ja ir ieslēgta opcija **Piemērot bez kupona koda**, ir pieejami dažādi scenāriji. Piemēram, kasieri var piešķirt papildu atlaides klientiem viņu nomierināšanas nolūkiem vai preču defektu dēļ. Drukātajiem kuponu kodiem vai svītrkodiem nav jābūt izplatītiem kasieriem. Tā vietā kasieri var izvēlēties pogu **Lietot kuponu**. Pēc tam kupons tiek automātiski piemērots transakcijai. Ja kupona galvenei ir vairāki kuponi, sistēma automātiski atlasa pirmo aktīvo transakcijas kuponu.

Lapā **Visas atlaides** pārdošanas asistenti var arī meklēt atlaides pēc atslēgvārdiem. Atslēgvārdu meklēšana meklē laukos, kuri satur atlaides nosaukumu un atlaides aprakstu. Pārdošanas asistenti var arī filtrēt atlaides, pamatojoties uz to, vai atlaidei ir nepieciešams kupona kods.

## <a name="cross-sell-and-upsell-by-using-discounts"></a>Šķērspārdošana un piedāvājumi, izmantojot atlaides

Daudzrindu atlaides, piemēram, daudzuma atlaides, komplekta piedāvājuma atlaides un sliekšņa atlaides, ir lielisks veids, kā motivēt klientus iegādāties vairāk preču, lai iegūtu lielākas atlaides. Tāpēc tās palīdz palielināt arī klienta groza un mazumtirdzniecības ieņēmumus. Šīs atlaides var tikt publicētas e-komercijas vietnēs, sociālajos medijos un reklāmkarogos veikalā.

Tomēr, pat ja tiek izmantotas visas šīs publicitātes metodes, klienti var palaist garām iespēju izmantot veicināšanas pasākumus. Lai pārdošanas asistentiem būtu vieglāk uzzināt, kādi veicināšanas pasākumi ir attiecināmi uz atlasīto rindu vai pat uz visu grozu, mazumtirgotāji var pievienot pogu **"Skatīt pieejamās atlaides"** jebkuram pogu režģim lapā **Transakcija**. Rezultātā pārdošanas asistents var atlasīt transakcijas rindu un pēc tam atlasīt pogu, lai parādītu visas atlasītajā rindā pieejamās atlaides. Pārdošanas asistents var arī atlasīt citu cilni, lai parādītu atlaides, kas attiecas uz visu transakciju. Ir svarīgi atzīmēt, ka opcija **Skatīt pieejamās atlaides** nerāda atlaides, kas jau tiek pielietotas pārdošanas rindai, jo atlaides informācija jau ir parādīta pārdošanas rindā. Šī scenārija mērķis ir parādīt tikai tās atlaides, kas vēl nav pielietotas. Izņēmums ir atlaides, kas tiek piemērotas, pamatojoties uz kuponu, kas atzīmēts kā "Lietot bez kupona koda". Tas pārdošanas partnerim atvieglo darbu viegli noņemt pielietoto kuponu.

Lapa **Visas atlaides** rāda tikai tās atlaides, kas nekonkurē ar kādu no izmantotajām atlaidēm. Šī darbība palīdz nodrošināt, ka, ja pārdošanas asistents informē klientu par atlaidi un klients veic nepieciešamo darbību (piemēram, klients pērk vēl vienu preci, lai iegūtu 10 procentu atlaidi), transakcijai tiek piemērota atlaide. Kuponā balstītas atlaides tiek rādīta vienīgi tad, ja ir ieslēgta opcija **Piemērot bez kupona koda**.

Vienkāršā scenārijā, kur visām atlaidēm ir viena un tā pati prioritāte, atlaides vienlaicīguma režīms ir **Salikts** un atlaides vienlaicīguma vadīkla ir iestatīta kā **Vislabākā cena un salikums prioritātē, nekad salikts prioritātēs**, lapa **Visas atlaides** rāda visas pieejamās atlaide precei, jo visas atlaides ir saliktas un nekonkurē cita ar citu.

Sekojošās ilustrācijās redzama loģika, kas nosaka, kuras atlaides tiek rādītas papildu scenārijos, piemēram, scenārijā, kur atlaides vienlaicīguma režīms ir **Vislabākā cena** vai **Ekskluzīvs** un tiek izmantotas divas vai vairākas prioritātes. Šajos scenārijos atlaides, kas tiek rādītas, tiek tālāk ietekmētas, pamatojoties uz to, vai atlaides vienlaicīguma vadīkla ir iestatīta uz **Labākā cena un salikums prioritātē, nekad slikts prioritātēs** vai **Labākā cena vienīgi prioritātē, vienmēr salikts prioritātē**.

Sekojošajā attēlā redzama loģika, kas tiek izmantota, kad atlaides vienlaicīguma kontrole ir iestatīta kā **Labākā cena un salikums prioritātē, nekad salikts prioritātēs**.

![Optimālas cenas un salikuma loģika prioritātes ietvaros, nekad salikts prioritātēs](./media/Model_1.png "Optimālas cenas un salikuma loģika prioritātes ietvaros, nekad salikta prioritātēs").

Sekojošajā attēlā redzama loģika, kas tiek izmantota, kad atlaides vienlaicīguma kontrole ir iestatīta kā **Labākā cena tikai prioritātē, vienmēr salikts prioritātē**.

![Optimālas cenas loģika tikai prioritātes ietvaros, vienmēr salikta prioritātē](./media/Model_2.png "Optimālas cenas loģika tikai prioritātes ietvaros, vienmēr salikta prioritātē").


[!INCLUDE[footer-include](../includes/footer-banner.md)]