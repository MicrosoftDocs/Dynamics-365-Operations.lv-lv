---
title: Projekta novērtējuma likvidēšana
description: Šajā tēmā sniegta informācija par projekta budžeta likvidēšanu pēc tam, kad tas ir izpildīts.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: eb323bdeb2a4701cdc9383b8da29e05a4cab107c
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410242"
---
# <a name="eliminate-a-project-estimate"></a>Projekta novērtējuma likvidēšana

[!include [banner](../includes/banner.md)]

Projekta aplēses sniedz finanšu skatījumu darbam, kas ir aplēsts un plānots projektam. Lai strādātu ar projekta budžetiem, projekts ir jāpievieno budžeta projektam. Budžeta projekts ir balstīts uz esošu projektu, taču vairāki projekti var attiekties uz vienu budžeta projektu. Budžeta projektiem var pievienot tikai fiksētas cenas un investīciju projektus, un šiem projektiem ir jāietilpst tajā pašā projektu grupā, kurā ietilpst budžeta projekts.

Lai likvidētu budžeta projektu, tam jābūt pabeigtam. Tālāk minētajās darbībās ir paskaidrots, kā likvidēt budžetu.

1. Dodieties uz **Projektu vadība un uzskaite** > **Visi projekti** un atveriet projektu. 
2. Cilnē **Pārvaldīt** atlasiet **Budžeti** un lapā **Budžets** atlasiet **Likvidēt**.
3. Cilnes **Vispārīgi** lapā **Likvidēt budžetu** iestatiet tālāk norādītās opcijas.

   - **Perioda kods**: atlasiet perioda kodu, lai izvēlētos atbilstīgos projektu budžetus. 
   - **Budžeta datums**: atlasiet likvidēšanai atbilstošu budžeta datumu.
   - **Likvidēt ar NP brīdinājumiem**: iespējojiet šo opciju, lai sniegtu paziņojumu, kad tiks likvidēts budžets, kas saistīts ar nepabeigtu darbu (NP). Ja šī opcija nav iespējota, likvidēšanu nevar turpināt, ja pastāv kādas ar budžetu nesaistītas darbības. 
   > [!NOTE]
   > Šī opcija ir pieejama tikai tad, ja likvidēšana tiek lietota budžeta projektam. Tā nav pieejama, ja izmantojat periodiskos grāmatojumus. Šis iestatījums darbojas ar iestatījumiem lapas **Projekta parametri** cilnes **Likvidēt** lauku grupā **Atļaut likvidēšanu arī tad, ja pastāv ar budžetu nesaistītas transakcijas**.
   - **Iestatīt stadiju uz Pabeigts** : iespējojiet šo opciju, lai iestatītu budžeta projekta stadiju uz **Pabeigts** pēc tam, kad esat palaidis likvidēšanu.
   - **Drukāt budžeta sarakstu**: atlasiet informāciju, kura jāiekļauj, drukājot brudžeta sarakstu.
   - **Rādīt informācijas žurnālu**: iespējojiet šo opciju, lai rādītu informācijas žurnālu.
   - **Grāmatošanas datums**: izvēlieties budžeta grāmatošanas datumu.

4.  Atlasiet **Labi**.
5. Kad likvidēšanas process ir pabeigts, likvidētais budžeta projekts tiek parādīts ar negatīvu vērtību. 

Ja neesat paredzējis likvidēt budžetu, varat atlasīt likvidēt budžetu un atlasīt **Atsaukt likvidēšanu**.   
