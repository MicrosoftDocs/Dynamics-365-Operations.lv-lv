---
title: Elektronisko pārskatu kreditoru čeku paraugi
description: Šajā rakstā ir sniegta vispārīga informācija par elektronisko pārskatu parauga čeku formātu izmantošanu.
author: sunfzam
ms.date: 06/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: d2b26a083540924d2368a298632aea90ecf95e9b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908188"
---
# <a name="electronic-reporting-sample-vendor-checks"></a>Elektronisko pārskatu kreditoru čeku paraugi

[!include [banner](../includes/banner.md)]

Varat izmantot elektronisko pārskatu (ER) veidošanas rīku, lai formatētu kreditoru čekus. Tirgū ir pieejami daudzi bankām specifiski un čeka nodrošinātājiem specifiski čeku formāti. ER rīka repozitorija maksājumu čeku modelī ir ietverti čeku paraugu formāti. Šiem čeku paraugiem ir šādi apzīmējumi: **Čeks vidū (ASV)** un **Čeks augšpusē, aprēķins apakšpusē (ASV)**.

## <a name="what-check-formats-are-currently-supported"></a>Kādi čeku formāti pašlaik tiek atbalstīti?

Vienmēr apmeklējiet koplietojamo līdzekļu bibliotēku portālā Microsoft Dynamics Lifecycle Services (LCS) un skatiet jaunāko pieejamo pamatlīdzekļa tipa **GER konfigurācija** failu sarakstu. Nākamajā sadaļā "Kas man ir jāiestata?" ir saite uz rakstu, kurā izskaidrots, kā izveidot LCS repozitoriju, lai varētu pārskatīt pieejamās konfigurācijas un importēt atlasītās konfigurācijas.

Microsoft Dynamics 365 Finanses ietver parauga formātu, kur pārbaude ir augšā, un pēc tam divas pārskaitījumu sadaļas. Tajā ir ietverts arī čeka parauga formāts, kurā čeks atrodas pa vidu starp divām pārskaitījuma sadaļām. Šie čeku paraugu formāti atbilst Deluxe uzņēmējdarbības čeku formātiem.

## <a name="what-do-i-have-to-set-up"></a>Kas man ir jāiestata?

- Pirms čeku drukāšanas, izmantojot ER izveides rīku, ER konfigurāciju kopā ir jāimportē vismaz viena aktīva čeka konfigurācija. Norādījumus skatiet sadaļā [Elektronisko atskaišu veidošanas konfigurāciju lejupielāde no Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).
- Konfigurējot bankas konta skaidras naudas un bankas vadības čekus, atzīmējiet izvēles rūtiņu **Vispārīgs elektroniskās eksportēšanas formāts** un pēc tam kā eksportēšanas formāta konfigurāciju atlasiet atbilstošo čeka formātu.
- Ir jānorāda arī pārskaitījuma sadaļā drukājamo kvīts rindu skaits. Aprēķinot šo skaitu, noteikti pieskaitiet galvenes rindas. Abiem čeku paraugu formātiem ieteicamais kvīts rindu skaits ir 17. Taču šis skaits mainīsies atkarībā no jūsu čeku kopas un printera draiveriem.
- Ir ieteicams izdrukāt izmēģinājuma čeku, lai pārbaudītu čeka izkārtojumu. Lai izdrukātu izmēģinājuma čeku, atlasiet opciju **Drukāt paraugu**. Čeku formātu paraugi vislabāk darbojas tad, ja programmas Microsoft Excel printera papildu rekvizītu sadaļā ir iestatīta opcijas **Piemales** vērtība **Nav**. Pēc izmēģinājuma čeka izdrukāšanas iespējojiet Excel izvades rediģēšanu un konfigurējiet lapas izkārtojumu, visām piemalēm iestatot vērtību **0** (nulle). Salīdziniet čeku izmēģinājuma kopijas ar čeku kopu un pielāgojiet iestatījumus, līdz izkārtojums jūs apmierina.
- Kad maksājumu žurnālā ģenerējat konfigurētā bankas konta maksājumus, tiek drukāti norādītā formāta čeki.

Papildinformāciju skatiet tēmā [Elektronisko pārskatu veidošanas formāta mainīšana](../../fin-ops-core/dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
