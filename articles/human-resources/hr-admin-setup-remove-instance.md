---
title: Noņemt instanci
description: Šajā rakstā ir aprakstīts Testa diskdziņa vai ražošanas vides noņemšanas process korporācijai Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0ce676c93e133cc04ad9c49417ed2ca0d6791e93
ms.sourcegitcommit: 1401d66b6b64c590ca1f8f339d622e922920cf15
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/20/2022
ms.locfileid: "9178478"
---
# <a name="remove-an-instance"></a>Noņemt instanci

_**Attiecas uz:** savrupas infrastruktūras personāla vadība_ 

> [!NOTE]
> Sākot no 2022. gada, jaunus cilvēkresursu vides nevar nodrošināt savrupos cilvēkresursu infrastruktūras un jaunos Microsoft Dynamics Lifecycle Services (LCS) projektos nevar izveidot tajā. Klienti var izvietot cilvēkresursu vides finanšu un operāciju infrastruktūrai. Papildinformāciju skatiet finanšu [un operāciju infrastruktūras sadaļu Personāla vadības nodrošināšana](/hr-admin-setup-provision-fo.md).

> [!IMPORTANT]
> Finanšu un operāciju programmas infrastruktūra atbalsta vides dzēšanu. Papildinformāciju par vides dzēšanu skatiet sadaļā [Vides dzēšana](../fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure.md#delete-an-environment).

Šajā rakstā skaidrots testa diskdziņa vai ražošanas vides noņemšanas process korporācijai Microsoft Dynamics 365 Human Resources.

## <a name="remove-a-test-drive-environment"></a>Izmēģinājuma vides noņemšana

Human Resources izmēģinājuma vides tiek nodrošinātas, izmantojot 60 dienu derīguma termiņa politiku. Taču izmēģinājuma vides īpašnieki var ātrāk beigt izmēģinājumu, veicot tālāk norādītās darbības. 

1. Pāriet uz [Power Apps Administrēšanas centru](https://admin.businessplatform.microsoft.com/).
2. Atlasiet **Vides**.
3. Atlasiet izmēģinājuma vidi, kuras nosaukuma formāts līdzinās šim: TestDrive — aizstājvārds@domēns.
4. Atlasiet **Dzēst** un apstipriniet dzēšanu. 

Esošā izmēģinājuma vide tiek noņemta. Kad tā ir noņemta, jūs varat reģistrēties jaunas izmēģinājuma vides saņemšanai. 

## <a name="remove-a-production-environment"></a>Ražošanas vides noņemšana

Šajā rakstā tiek pieņemts, ka esat iegādājies Human Resources, noslēdzot mākoņpakalpojumu nodrošinātāja (Cloud Solution Provider — CSP) vai uzņēmuma arhitektūras (enterprise architecture — EA) līgumu. 

Tā kā viena cilvēkresursu vide ir ietverta vienā Power Apps vidē, ir divas iespējas, kas ir jāņem vērā, noņemot vidi: 
- **Noņemiet visu Power Apps vidi.** Šī opcija ir ieteicama Power Apps, kad vide tika izveidota cilvēkresursu nodrošinājumam, ieviešanai ir tikai sākusies vai arī jums nav izveidotas integrācijas.  
- **Noņemt tikai cilvēkresursus.** Šī opcija ir piemērota, ja ir izveidota vide Power Apps, kas tiek aizpildīta ar datiem, kas tiek izmantoti Microsoft Power Apps un Power Automate


> [!Important]
> Pirms vides noņemšanas Power Apps pārliecinieties, vai tā netiek izmantota datu integrācijai ārpus Cilvēkresursu sfēras. Ņemiet arī vērā, ka noklusējuma Power Apps vides nevar noņemt. 

Lai noņemtu visu Power Apps vidi, tostarp Human Resources vidi un saistītās programmas un plūsmas, veiciet tālāk minētās darbības.

1. Pāriet uz [Power Apps Administrēšanas centru](https://admin.businessplatform.microsoft.com/).
2. Atlasiet **Vides**.
3. Atlasiet noņemamo vidi.
4. Atlasiet **Dzēst** un apstipriniet dzēšanu. 
5. Uzgaidiet, līdz ir pabeigta dzēšana.
6. Pierakstieties [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS), izmantojot kontu, ko izmantojāt, lai abonētu Human Resources. 
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
7. Atlasiet noņemamo instanci, kam ir jānorāda izvietošanas statuss **Dzēsts**.
8. Atlasiet **Noņemt instanci** un apstipriniet savu lēmumu. 

## <a name="recover-a-soft-deleted-environment"></a>Atjaunot viegli izdzēsto vidi

Ja dzēšat Power Apps vidi, ar kuru saistīta jūsu personāla vadības vide, personāla vadības vides statuss LCS tiks viegli **dzēsts**. Šādā gadījumā lietotāji nevar izveidot savienojumu ar Personāla vadību.

Lai atjaunotu vidi:

1. Sekojiet norādījumiem sadaļā [Atjaunot Power Apps vidi](/power-platform/admin/recover-environment).

2. Sazinieties ar atbalsta dienestu, lai atjaunotu Personāla vadības vidi. Lai iegūtu papildinformāciju, skatiet [Iegūt atbalstu](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

> [!Warning]
> Power Apps vides tiek saglabātas tikai septiņas dienas pēc to dzēšanas. Vide ir jāatkopo septiņu dienu periodā.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
