---
title: "Finanšu dimensijas"
description: "Šajā tēmā ir aprakstīti dažādie finanšu dimensiju tipi un izskaidrots, kā tie tiek iestatīti."
author: aprilolson
manager: AnnBe
ms.date: 08/24/2018
ms.topic: article
ems.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: d6b7b1219974cb5de1a625d87c3bce2a4439470b
ms.openlocfilehash: 9973d03de031ad2fa5647bb167c12b9231633a22
ms.contentlocale: lv-lv
ms.lasthandoff: 10/01/2018

---

# <a name="financial-dimensions"></a>Finanšu dimensijas

[!include [banner](../includes/banner.md)]

Šajā tēmā ir paskaidroti dažādie finanšu dimensiju tipi un izskaidrots, kā tie tiek iestatīti.

Izmantojiet lapu **Finanšu dimensijas**, lai izveidotu finanšu dimensijas, ko varat izmantot kā kontu segmentus kontu plānos. Ir divu veidu finanšu dimensijas: pielāgotas dimensijas un uz elementu balstītas dimensijas. Pielāgotās dimensijas tiek kopīgi izmantotas dažādās juridiskajās personās, un to vērtības ievada un uztur lietotāji. Attiecībā uz elementu balstītajām dimensijām to vērtības sistēmā tiek definētas kaut kur citur, piemēram, elementā Klienti vai Veikali. Dažas uz elementu balstītas dimensijas tiek kopīgi izmantotas dažādās juridiskajās personās, bet citas uz elementu balstītas dimensijas ir paredzētas tikai noteiktam uzņēmumam.

Kad esat izveidojis finanšu dimensijas, izmantojiet lapu **Finanšu dimensiju vērtības**, lai katrai finanšu dimensijai piešķirtu papildu rekvizītus.

Finanšu dimensijas varat izmantot, lai attēlotu juridiskās personas. Programmā Microsoft Dynamics 365 for Finance and Operations nav jāizveido juridiskās personas. Taču finanšu dimensijas nav paredzēts izmantot, lai risinātu juridisko personu operāciju vai biznesa prasības. Programmatūras Finance and Operations starpvienību uzskaites funkcionalitāte ir paredzēta darbam tikai ar katras transakcijas ietvaros izveidotajiem uzskaites ierakstiem.

Pirms finanšu dimensijas iestatāt kā juridiskas personas, nosakiet, vai šie iestatījumi ir piemēroti jūsu organizācijai, novērtējot savas uzņēmējdarbības procesus tālāk norādītajās jomās.

- Krājums
- Pārdošanas un pirkšanas darījumi starp finanšu dimensijām un juridiskām personām
- PVN aprēķins un pārskatu izveide
- Operāciju pārskatu izveide

Lūk, daži no ierobežojumiem.

- PVN funkcijas var lietot tikai juridiskām personām, nevis finanšu dimensijām.
- Dažos pārskatos finanšu dimensijas nav ietvertas. Tādēļ, lai ziņotu pēc finanšu dimensijas, jums, iespējams, ir jāmodificē pārskati.

## <a name="custom-dimensions"></a>Pielāgotas dimensijas

Lai izveidotu lietotāja definētu finanšu dimensiju, laukā **Izmantot vērtības no** atlasiet **&lt;&nbsp;Pielāgota dimensija&nbsp;&gt;**.

Lai ierobežotu summas un tipa informāciju, ko var ievadīt dimensiju vērtībām, var norādīt arī konta masku. Varat ievadīt rakstzīmes, kas paliek tādas pašas katrai dimensijas vērtībai, piemēram, burtus vai defisi (-). Numura zīmes (\#) un zīmes (&) var ievadīt arī kā to rakstzīmju vietturus, kuras mainīsies ikreiz, izveidojot dimensijas vērtību. Numura zīmi (\#) izmantojiet kā vietturi cipariem un zīmi & izmantojiet kā vietturi burtiem. Formāta maskas lauks ir pieejams tikai tad, ja laukā **Izmantot vērtības no** tiek atlasīta opcija **&lt;&nbsp;Pielāgota dimensija&nbsp;&gt;**.

**Piemērs**

Lai dimensijas vērtību noteiktu kā burtus “CC” un trīs ciparus, kā formāta maska ir jāieraksta **CC-\#\#\#**.

## <a name="entity-backed-dimensions"></a>Uz elementu balstītas dimensijas

Lai izveidotu uz elementu balstītu finanšu dimensiju, laukā **Izmantot vērtības no** atlasiet sistēmas definētu elementu, uz kuru balstīt šo finanšu dimensiju. Pēc tam finanšu dimensijas vērtības tiek veidotas no šī elementa. Piemēram, lai izveidotu dimensiju vērtības projektiem, atlasiet vienumu **Projekti**. Pēc tam dimensijas vērtība tiek izveidota katram projekta nosaukumam. Lapā **Finanšu dimensiju vērtības** tiek rādītas vērtības šim elementam. Ja šīs vērtības ir atkarīgas no uzņēmuma, tad lapā tiek rādīts arī uzņēmums.

## <a name="activating-dimensions"></a>Dimensiju aktivizēšana

Kad aktivizējat kādu finanšu dimensiju, tabula tiek atjaunināta tā, lai tajā būtu ietverts finanšu dimensijas nosaukums. Dzēstās dimensijas tiek noņemtas. Dimensiju vērtības varat ievadīt, pirms aktivizējat kādu finanšu dimensiju. Taču finanšu dimensiju nekur nevar patērēt, kamēr tā nav aktivizēta. Jūs nevarat finanšu dimensiju, piemēram, pievienot konta struktūrai, kamēr šī finanšu dimensija nav aktivizēta. Atlasot opciju **Aktivizēt**, visas dimensijas tiek atjauninātas un tiek parādītas statusa izmaiņas.

## <a name="translations"></a>Tulkojumi

Lapā **Teksta tulkojums** atlasītajai finanšu dimensijai varat ievadīt tekstu dažādās valodās. Lapā **Galvenā konta tulkojums** attiecīgajam galvenajam kontam varat ievadīt tekstu dažādās valodās. 

## <a name="legal-entity-overrides"></a>Juridiskas personas prioritātes

Ne visas dimensijas ir derīgas visām juridiskajām personām. Turklāt dažas dimensijas var attiekties tikai uz noteiktu periodu. Tādos gadījumos varat izmantot sadaļu **Juridiskas personas prioritātes**, lai norādītu uzņēmumus, attiecībā uz kuriem šī dimensija ir jāaiztur, kā arī īpašnieku un periodu, kad šī dimensija ir aktīva.

## <a name="deleting-financial-dimensions"></a>Finanšu dimensiju dzēšana

Lai palīdzētu uzturēt atsauču datu integritāti, finanšu dimensijas dzēst ir iespējams reti. Ja mēģināt dzēst kādu finanšu dimensiju, tiek izvērtēti tālāk norādītie kritēriji.

- Vai šī finanšu dimensija ir izmantota kādā iegrāmatotā un neiegrāmatotā transakcijā vai kādā dimensiju vērtību kombinācijā?
- Vai šī finanšu dimensija ir izmantota kādā aktīvā konta struktūrā, papildu kārtulas struktūrā vai finanšu dimensiju kopā?
- Vai šī finanšu dimensija veido daļu no noklusējuma finanšu dimensiju integrācijas formāta?
- Vai šī finanšu dimensija ir iestatīta kā noklusējuma dimensija?

Ja finanšu dimensija atbilst kādam no šiem kritērijiem, tad šo finanšu dimensiju nevar izdzēst.

## <a name="default-dimension-values"></a>Noklusējuma dimensijas vērtības

Šablona ierakstu vērtības, piemēram, debitoru un kreditoru, var izmantot kā noklusējuma vērtības jaunās dimensijās. Ja tiek izveidotas jaunas dimensijas, šablona ieraksta ID tiek ievadīts šo šablona ierakstu dimensijas vērtībās. Piemēram, izveidojot jaunu debitoru, debitora ID tiek ievadīts debitora dimensijā. Izveidojot pārdošanas pasūtījumus, rēķinus vai citus dokumentus, kuros ir jānorāda debitora ID, tiek izmantotas esošās noklusējuma kārtulas un dokumentos tiek pievienots debitora ID.

Šo līdzekli kontrolē dimensijas iestatījums. Šī iestatījuma nosaukums ir **Kopēt vērtības uz šo dimensiju katrā no jauna izveidotājā vienumā DimensionName**, kur **DimensionName** ir dimensijas nosaukums. Pēc noklusējuma līdzeklis ir izslēgts. Tomēr to var ieslēgt jebkurā laikā.

Ja ieraksti dimensijai jau pastāv, šablona ieraksti tiek atjaunināti, aktivizējot līdzekli. Tomēr esošie dokumenti un transakcijas netiek atjauninātas.

## <a name="derived-dimensions"></a>Atvasinātās dimensijas

Dimensiju var konfigurēt tā, lai, ievadot šo dimensiju dokumentā, tiek automātiski ievadīta informācija par citām dimensijām. Piemēram, ja tiek ievadīts izmaksu centrs 10, vērtību **20** var automātiski ievadīt nodaļas dimensijā.

Dimensiju lapā var iestatīt atvasinātās vērtības.

1. Atlasiet dimensiju un pēc tam atlasiet **Atvasinātās dimensijas**.

    Lapā **Atvasinātas dimensijas** ir ietverts režģi. Atlasītās dimensijas segments ir šī režģa pirmā kolonna.

2. Pievienojiet atvasināmos segmentus. Katrs segments tiek parādīts kā kolonna.

Ievadiet dimensiju kombinācijas, kas ir jāatvasina no dimensijas pirmajā kolonnā. Piemēram, lai varētu izmantot izmaksu centru kā dimensiju, no kuras ir atvasināta nodaļa un vieta, ievadiet izmaksas centra vērtību 10, nodaļas vērtību 20 un vietas vērtību 30. Pēc tam, ievadot izmaksu centru 10 šablona ierakstā vai transakciju lapā, nodaļa 20 un vieta 30 tiek ievadīta pēc noklusējuma.

Atvasinātās dimensijas process neignorē esošās atvasināto dimensiju vērtības. Piemēram, ja ievada izmaksu centru 10 un citas dimensijas netiek ievadītas, pēc noklusējuma tiek ievadīta nodaļas 20 un vieta 30. Tomēr, ja izmaksu centrs tiek mainīts, jau izveidotās vērtības netiek mainītas. Tāpēc šablona ierakstos var izveidot noklusējuma dimensijas, un atvasinātās dimensijas šīs dimensijas neizmaina.

### <a name="derived-dimensions-and-entities"></a>Atvasinātās dimensijas un elementi

Atvasināto dimensiju segmentus un vērtības var iestatīt, izmantojot elementus.

- Atvasināts dimensijas elements iestata vadošo dimensiju un segmentus, kurus izmanto šīm dimensijām.
- Elements DerivedDimensionValue ļauj importēt vērtības, kuras jāatvasina visām vadošajām dimensijām.

Ja elementu tiek izmantots datu importēšanai un šis elements importē dimensijas, importēšanas laikā stājas spēkā atvasinātās dimensijas kārtulas, ja vien elements īpaši neignorē šīs dimensijas.

Lai iegūtu papildu informāciju, skatiet šādas tēmas:

- [Finanšu dimensiju definēšana](tasks/define-financial-dimensions.md)
- [Finanšu dimensijas noklusējuma veidņu uzturēšana](tasks/maintain-financial-dimension-default-templates.md)

