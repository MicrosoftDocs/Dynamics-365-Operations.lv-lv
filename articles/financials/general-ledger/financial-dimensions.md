---
title: "Finanšu dimensijas"
description: "Šajā tēmā ir aprakstīti dažādie finanšu dimensiju tipi un izskaidrots, kā tie tiek iestatīti."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
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
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 3e9f00fdc32feda0a62f71a92e503a677dce35cc
ms.contentlocale: lv-lv
ms.lasthandoff: 03/26/2018

---

# <a name="financial-dimensions"></a>Finanšu dimensijas

[!include [banner](../includes/banner.md)]

Šajā tēmā ir paskaidroti dažādie finanšu dimensiju tipi un izskaidrots, kā tie tiek iestatīti.

Izmantojiet lapu **Finanšu dimensijas**, lai izveidotu finanšu dimensijas, ko varat izmantot kā kontu segmentus kontu plānos. Ir divu veidu finanšu dimensijas: pielāgotas dimensijas un uz elementu balstītas dimensijas. Pielāgotās dimensijas tiek kopīgi izmantotas dažādās juridiskajās personās, un to vērtības ievada un uztur lietotāji. Attiecībā uz elementu balstītajām dimensijām to vērtības sistēmā tiek definētas kaut kur citur, piemēram, elementos Klienti vai Veikali. Dažas uz elementu balstītas dimensijas tiek kopīgi izmantotas dažādās juridiskajās personās, bet citas uz elementu balstītas dimensijas ir paredzētas tikai noteiktam uzņēmumam. 

Kad esat izveidojis finanšu dimensijas, izmantojiet lapu **Finanšu dimensiju vērtības**, lai katrai finanšu dimensijai piešķirtu papildu rekvizītus. 

Finanšu dimensijas varat izmantot, lai attēlotu juridiskās personas. Programmā Microsoft Dynamics 365 for Finance and Operations nav jāizveido juridiskās personas. Taču finanšu dimensijas nav paredzētas tam, lai risinātu juridisko personu operāciju vai biznesa prasības. Programmatūras Finance and Operations starpvienību uzskaites funkcionalitāte ir paredzēta darbam tikai ar katras transakcijas ietvaros izveidotajiem uzskaites ierakstiem. 

Pirms finanšu dimensijas iestatāt kā juridiskas personas, nosakiet, vai šie iestatījumi ir piemēroti jūsu organizācijai, novērtējot savas uzņēmējdarbības procesus tālāk norādītajās jomās.

- Krājums
- Pārdošanas un pirkšanas darījumi starp finanšu dimensijām un juridiskām personām
- PVN aprēķins un pārskatu izveide
- Operāciju pārskatu izveide

Lūk, daži no ierobežojumiem.

- PVN funkcijas var lietot tikai juridiskām personām, nevis finanšu dimensijām.
- Dažos pārskatos finanšu dimensijas nav ietvertas. Tādēļ, lai ziņotu pēc finanšu dimensijas, jums, iespējams, ir jāmodificē pārskati.

## <a name="custom-dimensions"></a>Pielāgotas dimensijas

Lai izveidotu lietotāja definētu finanšu dimensiju, laukā **Izmantot vērtības no** atlasiet opciju **&lt; Pielāgota dimensija &gt;**. Lai ierobežotu summas un tipa informāciju, ko var ievadīt dimensiju vērtībām, var norādīt arī konta masku. Varat ievadīt rakstzīmes, kas paliek tādas pašas katrai dimensijas vērtībai, piemēram, burtus vai defisi (-). Numura zīmes (\#) un zīmes & varat arī ievadīt kā vietturus burtiem un cipariem, kas mainīsies ikreiz, kad tiks izveidota dimensijas vērtība. Numura zīmi (\#) izmantojiet kā vietturi cipariem un zīmi & izmantojiet kā vietturi burtiem. Formāta maskai paredzētais lauks ir pieejams tikai tad, ja laukā **Izmantot vērtības no** atlasāt opciju **&lt; Pielāgota dimensija &gt;**.

**Piemērs**

Lai dimensijas vērtību noteiktu kā burtus “CC” un trīs ciparus, kā formāta maska ir jāieraksta **CC-\#\#\#**.

## <a name="entity-backed-dimensions"></a>Uz elementu balstītas dimensijas

Lai izveidotu uz elementu balstītu finanšu dimensiju, laukā **Izmantot vērtības no** atlasiet sistēmas definētu elementu, uz kuru balstīt šo finanšu dimensiju. Pēc tam finanšu dimensijas vērtības tiek veidotas no šī elementa. Piemēram, lai izveidotu dimensiju vērtības projektiem, atlasiet vienumu **Projekti**. Pēc tam dimensijas vērtība tiek izveidota katram projekta nosaukumam. Lapā **Finanšu dimensiju vērtības** tiek rādītas vērtības šim elementam. Ja šīs vērtības ir atkarīgas no uzņēmuma, tad lapā tiek rādīts arī uzņēmums.

## <a name="activating-dimensions"></a>Dimensiju aktivizēšana

Kad aktivizējat kādu finanšu dimensiju, tabula tiek atjaunināta tā, lai tajā būtu ietverts finanšu dimensijas nosaukums. Dzēstās dimensijas tiek noņemtas. Dimensiju vērtības varat ievadīt, pirms aktivizējat kādu finanšu dimensiju. Taču finanšu dimensiju nekur nevar patērēt, kamēr tā nav aktivizēta. Jūs nevarat finanšu dimensiju, piemēram, pievienot konta struktūrai, kamēr šī finanšu dimensija nav aktivizēta. Kad noklikšķināt uz **Aktivizēt**, visas dimensijas tiek atjauninātas un tām tiek rādītas statusa izmaiņas. 

## <a name="translations"></a>Tulkojumi

Lapā **Teksta tulkojums** atlasītajai finanšu dimensijai varat ievadīt tekstu dažādās valodās. Lapā **Galvenā konta tulkojums** attiecīgajam galvenajam kontam varat ievadīt tekstu dažādās valodās. 

## <a name="legal-entity-overrides"></a>Juridiskas personas prioritātes

Ne visas dimensijas ir derīgas visām juridiskajām personām. Turklāt dažas dimensijas var attiekties tikai uz noteiktu periodu. Tādos gadījumos varat izmantot sadaļu **Juridiskas personas prioritātes**, lai norādītu uzņēmumus, attiecībā uz kuriem šī dimensija ir jāaiztur, kā arī īpašnieku un periodu, kad šī dimensija ir aktīva.

## <a name="deleting-financial-dimensions"></a>Finanšu dimensiju dzēšana

Lai palīdzētu uzturēt atsauču datu integritāti, finanšu dimensijas dzēst ir iespējams reti. Ja mēģināt dzēst kādu finanšu dimensiju, tiek izvērtēti tālāk norādītie kritēriji.

- Vai šī finanšu dimensija ir izmantota kādās iegrāmatotās un neiegrāmatotās transakcijās, vai kādā dimensiju vērtību kombinācijā?
- Vai šī finanšu dimensija ir izmantota kādā aktīvā konta struktūrā, papildu kārtulas struktūrā vai finanšu dimensiju kopā?
- Vai šī finanšu dimensija veido daļu no noklusējuma finanšu dimensiju integrācijas formāta?
- Vai šī finanšu dimensija ir iestatīta kā noklusējuma dimensija?

Ja finanšu dimensija atbilst kādam no šiem kritērijiem, tad šo finanšu dimensiju nevar izdzēst.


Lai iegūtu papildu informāciju, skatiet šādas tēmas:
- [Finanšu dimensiju definēšana](tasks/define-financial-dimensions.md)
- [Finanšu dimensijas noklusējuma veidņu uzturēšana](tasks/maintain-financial-dimension-default-templates.md)

