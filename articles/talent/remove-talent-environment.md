---
title: Talent vižu noņemšana
description: Šajā tēmā ir detalizēti aprakstīts, kā noņemt izmēģinājuma vai ražošanas vidi programmā Microsoft Dynamics 365 Talent.
author: andreabichsel
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.openlocfilehash: d608ee3ad90d23279557e5e9be4d398ffac3a266
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/23/2019
ms.locfileid: "2010619"
---
# <a name="remove-talent-environments"></a>Talent vides noņemšana

[!include [banner](includes/banner.md)]

Šajā tēmā ir detalizēti aprakstīts, kā noņemt izmēģinājuma vai ražošanas vidi programmā Microsoft Dynamics 365 Talent.

## <a name="removing-a-test-drive-environment"></a>Izmēģinājuma vides noņemšana

Talent izmēģinājuma vides tiek nodrošinātas, izmantojot 60 dienu derīguma termiņa politiku. Taču izmēģinājuma vides īpašnieki var ātrāk beigt izmēģinājumu, veicot tālāk norādītās darbības. 

1. Pāriet uz [PowerApps Administrēšanas centru](https://admin.businessplatform.microsoft.com/).
2. Atlasiet **Vides**.
3. Atlasiet izmēģinājuma vidi, kuras nosaukuma formāts līdzinās šim: TestDrive — aizstājvārds@domēns.
4. Atlasiet **Dzēst** un apstipriniet dzēšanu. 

Esošā izmēģinājuma vide tiek noņemta. Kad tā ir noņemta, jūs varat reģistrēties jaunas izmēģinājuma vides saņemšanai. 

## <a name="removing-a-production-environment"></a>Ražošanas vides noņemšana

Šajā tēmā tiek pieņemts, ka esat iegādājies programmatūru Talent, noslēdzot mākoņpakalpojumu nodrošinātāja (Cloud Solution Provider — CSP) vai uzņēmuma arhitektūras (enterprise architecture — EA) līgumu. 

Tā kā katra Talent vide ir ietverta atsevišķā PowerApps vidē, ir pieejamas divas iespējas. Pirmā iespēja ietver visas PowerApps vides noņemšanu, bet otrā iespēja ietver tikai Talent vides noņemšanu. Pirmo iespēju ir ieteicams izvēlēties gadījumā, ja esat izveidojis PowerApps vidi tikai Talent nodrošināšanai un esat tikko sācis ieviešanu vai vēl nav izveidota neviena integrācija. Otrā iespēja ir piemērota gadījumā, ja jums ir izveidota PowerApps vide ar bagātīgiem datiem, kas ir saistīti ar PowerApps programmām un plūsmām.

> [!Important]
> Pirms PowerApps vides noņemšanas pārliecinieties, vai tā netiek izmantota bagātīgu datu integrācijai ārpus Talent tvēruma. Ņemiet arī vērā, ka noklusējuma PowerApps vides nevar noņemt. 

Lai noņemtu visu PowerApps vidi, tostarp Talent vidi un saistītās programmas un plūsmas, veiciet tālāk norādītās darbības.

1. Pāriet uz [PowerApps Administrēšanas centru](https://admin.businessplatform.microsoft.com/).
2. Atlasiet **Vides**.
3. Atlasiet noņemamo vidi.
4. Atlasiet **Dzēst** un apstipriniet dzēšanu. 
5. Uzgaidiet, līdz ir pabeigta dzēšana.
6. Pierakstieties pakalpojumā [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS), izmantojot kontu, ko izmantojāt, lai abonētu programmatūru Talent. 
7. Atlasiet Talent projektu, kurā ir ietverta vide. 
8. LCS projektā atlasiet elementu **Talent programmas pārvaldība**. 
9. Atlasiet noņemamo instanci. 
10. Atlasiet **Noņemt instanci** un apstipriniet savu lēmumu.  

Lai noņemtu Talent vidi no esošas PowerApps vides, veiciet tālāk norādītās darbības. Ņemiet vērā, ka nepieciešamība sazināties ar atbalsta dienestu un Talent DevOps darba grupu ir pagaidu prasība, kas ir jāizpilda, līdz šis līdzeklis tiks tiešā veidā iespējots LCS.

1. Sazinieties ar atbalsta dienestu, lai iesniegtu noņemšanas pieprasījumu.
2. Atbalsta dienesta darba grupa iesniedz noņemšanas pieprasījumu Talent DevOps darba grupai. 
3. Turpiniet darbu, kad saņemat paziņojumu par vides noņemšanu.
4.  Pierakstieties pakalpojumā LCS, izmantojot to pašu kontu, ko izmantojāt, lai abonētu Talent. 
5. Atlasiet Talent projektu, kurā ir ietverta vide. 
6. LCS projektā atlasiet elementu **Talent programmas pārvaldība**. 
7. Atlasiet noņemamo instanci, kam ir jānorāda izvietošanas statuss **Neizdevās**.
8. Atlasiet **Noņemt instanci** un apstipriniet savu lēmumu. 

