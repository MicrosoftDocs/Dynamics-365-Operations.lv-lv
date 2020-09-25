---
title: Projekta resursu iestatīšana
description: Šajā tēmā sniegta informācija par projekta resursu iestatīšanu vai pieprasīšanu.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c882e23794e3937f85b3e73774b36deaf28ac3ed
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760608"
---
# <a name="set-up-project-resources"></a>Projekta resursu iestatīšana

[!include [banner](../includes/banner.md)]

Ir jāiestata kalendārs un jāsaista tas ar darbinieku vai nodarbināto. Kalendārs tiek izmantots, lai plānotu projektu un projektam rezervēto resursu darba laiku. Kalendāra iestatīšanas laikā projektu vadītāji resursu optimizēšanas ietvaros var veikt resursu izlīdzināšanu. Pamatojoties uz kalendāra grafiku, resursiem var noteikt ierobežojumus. Kalendāru varat iestatīt lapā **Kalendāri**.

Kad kādu nodarbināto iestatāt kā projekta resursu, varat atlasīt no nodarbinātajiem, kuri strādā uzņēmumā, kam iestatāt resursus. Varat arī atlasīt nodarbinātos no citiem uzņēmumiem jūsu organizācijā. Šie nodarbinātie tiek saukti par starpuzņēmumu resursiem.

Tālāk sniegtajos procedūru aprakstos ir paskaidrots, kā nodarbināto iestatīt kā projekta resursu jūsu uzņēmumā un kā iestatīt starpuzņēmumu projekta resursu.

## <a name="set-up-a-worker-as-a-project-resource"></a>Nodarbinātā kā projekta resursa iestatīšana

1. Lapas **Darbinieki** sarakstā **Nodarbinātie** atlasiet nodarbināto, kuru pievienojat kā projekta resursu, un atveriet nodarbinātā ierakstu.
2. Darbību rūtī atlasiet **Projekts** &gt; **Iestatījumi** &gt; **Projektu iestatījumi**.
3. Atlasiet kalendāru un pēc tam aizveriet lapu.

Jūs varat arī norādīt resursam noklusējuma projektus kā iepriekšēju piešķiri. Iepriekšējas piešķires var izmantot, ja resursu pārvaldnieks vai projektu vadītājs iepriekš zina, kurā projektā resurss veiks darbu. Iepriekšējas piešķires arī var balstīties uz projekta sponsora vai debitora pieprasījumu. Lai veiktu projekta iepriekšēju piešķiri, lapas **Piešķirt projektus** cilnes **Projekti** sarakstā **Atlikušie projekti** atlasiet attiecīgo projektu.

## <a name="set-up-an-intercompany-resource"></a>Starpuzņēmumu resursa iestatīšana

Kad nodarbināto iestatāt kā starpuzņēmumu resursu, iestatīšana ir jāveic gan patapināšanas uzņēmumā, gan piesaistīšanas uzņēmumā.

### <a name="in-the-lending-company"></a>Patapināšanas uzņēmumā

1. Programmā Finance pārbaudiet, vai ir atlasīts patapināšanas uzņēmums, un pēc tam veiciet iepriekšējā sadaļā “Nodarbinātā kā projekta resursa iestatīšana” aprakstīto procedūru.
2. Lapā **Starpuzņēmumu uzskaite** atlasiet **Jauns**.
3. Laukā **Juridiskās personas ID** atlasiet patapināšanas uzņēmumu. Aizpildiet pārējos laukus ar atbilstošu informāciju un pēc tam atlasiet **Saglabāt**.
4. Lapā **Transfertcena** atlasiet **Jauns**.
5. Laukā **Piesaistīšanas juridiskā persona** atlasiet atbilstošo uzņēmumu.
6. Lai piesaistīšanas uzņēmumam aizdotu tikai to resursu, kuru izveidojāt šīs sadaļas sākumā, laukā **Resurss** atlasiet izveidotā resursa nosaukumu. Lai piesaistīšanas uzņēmumam būtu pieejami visi patapināšanas uzņēmuma resursi, lauks **Resurss** ir jāatstāj tukšs.
7. Lapā **Projektu vadības un uzskaites parametri**, cilnē **Starpuzņēmumu** opciju **Aktivizēt starpuzņēmumu resursu plānošanu un laika grafikus** iestatiet uz **Jā**.

### <a name="in-the-borrowing-company"></a>Piesaistīšanas uzņēmumā

- Lapā **Resursu saraksts**, meklēšanas filtrā ievadiet tā resursu nosaukumu, kuru izveidojāt patapināšanas uzņēmumam, lai pārbaudītu, vai šis nosaukums ir ietverts piesaistīšanas uzņēmuma resursu sarakstā.

## <a name="request-project-resources"></a>Projekta resursu pieprasīšana
Projekta resursu plānošanas funkcionalitāte resursu pārvaldniekiem pa piesaistēm vai projektiem ļauj sadalīt tikai nokomplektētos resursus. Lai iespējoto šo funkcionalitāti, izpildiet tālāk norādītos uzdevumus vai pārliecinieties, ka tie jau ir izpildīti.

- Iestatiet numuru sērijas.
- Iestatiet projektu vadības un uzskaites darbplūsmas.
- Iespējojiet resursu pieprasījumu darbplūsmas.

Kad iepriekš norādītie uzdevumi ir izpildīti, pēc nepieciešamības varat izpildīt tālāk norādītos uzdevumus.

- Izveidojiet resursa pieprasījumu, izmantojot viegli rezervētu personāla resursu.
- Pārraugiet resursu pieprasījumus.
- Izpildiet resursu pieprasījumus.
- Pieprasiet nokomplektētu resursu no WBS.
- Rezervējiet projektam resursus bez nepieciešamības pieprasīt nokomplektētu resursu.
