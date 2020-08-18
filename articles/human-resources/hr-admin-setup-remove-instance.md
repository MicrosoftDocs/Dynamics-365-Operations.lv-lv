---
title: Noņemt instanci
description: Šajā rakstā ir detalizēti aprakstīts, kā noņemt izmēģinājuma vai ražošanas vidi Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a384801060b2b684f7908daaac2311edd27c773a
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621384"
---
# <a name="remove-an-instance"></a>Noņemt instanci

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
4. Pierakstieties LCS, izmantojot to pašu kontu, ko lietojat Human Resources abonēšanai. 
5. Atlasiet Human Resources projektu, kurā ir ietverta vide. 
6. Savā LCS projektā atlasiet elementu **Human Resources programmas pārvaldība**. 
7. Atlasiet noņemamo instanci, kam ir jānorāda izvietošanas statuss **Neizdevās**.
8. Atlasiet **Noņemt instanci** un apstipriniet savu lēmumu. 

## <a name="recover-a-soft-deleted-environment"></a>Atjaunot viegli izdzēsto vidi

Ja izdzēsīsit Power Apps vidi, ar kuru ir saistīta jūsu Personāla vadības vide, Personāla vadības vides stāvoklis Lifecycle Services tiks **viegli dzēsts**. Šādā gadījumā lietotāji nevar izveidot savienojumu ar Personāla vadību.

Lai atjaunotu vidi:

1. Sekojiet norādījumiem sadaļā [Atjaunot Power Apps vidi](/power-platform/admin/recover-environment.md).

2. Sazinieties ar atbalsta dienestu, lai atjaunotu Personāla vadības vidi. Lai iegūtu papildinformāciju, skatiet [Iegūt atbalstu](hr-admin-troubleshooting-support.md).

> [!Warning]
> Power Apps vides tiek saglabātas tikai septiņas dienas pēc to dzēšanas. Jums ir jāatjauno vide septiņu dienu laikā.
