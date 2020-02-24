---
title: Instances noņemšana
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5c5f875ad9361c31af4fbe863488b881cdd97a6e
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009759"
---
# <a name="remove-an-instance"></a>Instances noņemšana

Šajā rakstā ir detalizēti aprakstīts, kā noņemt izmēģinājuma vai ražošanas vidi Microsoft Dynamics 365 Human Resources.

## <a name="remove-a-test-drive-environment"></a>Izmēģinājuma vides noņemšana

Human Resources izmēģinājuma vides tiek nodrošinātas, izmantojot 60 dienu derīguma termiņa politiku. Taču izmēģinājuma vides īpašnieki var ātrāk beigt izmēģinājumu, veicot tālāk norādītās darbības. 

1. Pāriet uz [Power Apps Administrēšanas centru](https://admin.businessplatform.microsoft.com/).
2. Atlasiet **Vides**.
3. Atlasiet izmēģinājuma vidi, kuras nosaukuma formāts līdzinās šim: TestDrive — aizstājvārds@domēns.
4. Atlasiet **Dzēst** un apstipriniet dzēšanu. 

Esošā izmēģinājuma vide tiek noņemta. Kad tā ir noņemta, jūs varat reģistrēties jaunas izmēģinājuma vides saņemšanai. 

## <a name="remove-a-production-environment"></a>Ražošanas vides noņemšana

Šajā rakstā tiek pieņemts, ka esat iegādājies Human Resources, noslēdzot mākoņpakalpojumu nodrošinātāja (Cloud Solution Provider — CSP) vai uzņēmuma arhitektūras (enterprise architecture — EA) līgumu. 

Tā kā katra Human Resources vide ir ietverta atsevišķā Power Apps vidē, ir pieejamas divas iespējas. Pirmā iespēja ietver visas Power Apps vides noņemšanu, bet otrā iespēja ietver tikai Human Resources vides noņemšanu. Pirmo iespēju ir ieteicams izvēlēties gadījumā, ja esat izveidojis Power Apps vidi tikai Human Resources nodrošināšanai un esat tikko sācis ieviešanu vai vēl nav izveidota neviena integrācija. Otrā iespēja ir piemērota gadījumā, ja jums ir izveidota Power Apps vide ar bagātīgiem datiem, kas ir saistīti ar Power Apps un Power Automate.

> [!Important]
> Pirms Power Apps vides noņemšanas pārliecinieties, vai tā netiek izmantota vērtīgu datu integrācijai ārpus Human Resources tvēruma. Ņemiet arī vērā, ka noklusējuma Power Apps vides nevar noņemt. 

Lai noņemtu visu Power Apps vidi, tostarp Human Resources vidi un saistītās programmas un plūsmas, veiciet tālāk minētās darbības.

1. Pāriet uz [Power Apps Administrēšanas centru](https://admin.businessplatform.microsoft.com/).
2. Atlasiet **Vides**.
3. Atlasiet noņemamo vidi.
4. Atlasiet **Dzēst** un apstipriniet dzēšanu. 
5. Uzgaidiet, līdz ir pabeigta dzēšana.
6. Pierakstieties [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS), izmantojot kontu, ko izmantojāt, lai abonētu Human Resources. 
7. Atlasiet Human Resources projektu, kurā ir ietverta vide. 
8. Savā LCS projektā atlasiet elementu **Human Resources programmas pārvaldība**. 
9. Atlasiet noņemamo instanci. 
10. Atlasiet **Noņemt instanci** un apstipriniet savu lēmumu.  

Lai noņemtu Human Resources vidi no esošas Power Apps vides, veiciet tālāk minētās darbības. Ņemiet vērā, ka nepieciešamība sazināties ar atbalsta dienestu un Human Resources DevOps grupu ir pagaidu prasība, kas ir jāizpilda, līdz šis līdzeklis tiks tiešā veidā iespējots LCS.

1. Sazinieties ar atbalsta dienestu, lai iesniegtu noņemšanas pieprasījumu.
2. Atbalsta dienesta grupa iesniedz noņemšanas pieprasījumu Human Resources DevOps grupai. 
3. Turpiniet darbu, kad saņemat paziņojumu par vides noņemšanu.
4.  Pierakstieties LCS, izmantojot to pašu kontu, ko lietojat Human Resources abonēšanai. 
5. Atlasiet Human Resources projektu, kurā ir ietverta vide. 
6. Savā LCS projektā atlasiet elementu **Human Resources programmas pārvaldība**. 
7. Atlasiet noņemamo instanci, kam ir jānorāda izvietošanas statuss **Neizdevās**.
8. Atlasiet **Noņemt instanci** un apstipriniet savu lēmumu. 
