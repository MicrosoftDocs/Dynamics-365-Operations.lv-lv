---
title: Vispārējās plānošanas sākumlapa
description: Vispārējā plānošana ļauj uzņēmumiem noteikt un ieplānot nākotnes nepieciešamības pēc izejmateriāliem un jaudas, lai sasniegtu uzņēmuma mērķus.
author: ChristianRytt
ms.date: 12/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7dd25fdd1549fb2fddff57dc2d9cf8762cfd6823
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416531"
---
# <a name="master-planning-home-page"></a>Vispārējās plānošanas sākumlapa

[!include [banner](../includes/banner.md)]

Būtībā Vispārējā plānošana ļauj uzņēmumiem noteikt un ieplānot nākotnes nepieciešamības pēc izejmateriāliem un jaudas, lai sasniegtu uzņēmuma mērķus. Vispārējā plānošana novērtē tālāk norādītos faktorus.

- Kādas jaudas un izejmateriāli ir pieejami pašlaik?
- Kādas jaudas un izejmateriāli ir nepieciešami, lai izpildītu ražošanu? Piemēram, kas ir jāsaražo, jāiegādājas, jāpārsūta vai jāatliek rezervei, pirms varat izpildīt ražošanu.

Vispārējā plānošana šo informāciju izmanto, lai aprēķinātu prasības un ģenerētu plānotos pasūtījumus.

Plānošanu veido trīs tālāk norādītie galvenie procesi:

- **Vispārējā plānošana** — Vispārējā plānošana aprēķina neto vajadzības. Tā ir balstīta uz pašreizējiem faktiskajiem pasūtījumiem un ļauj uzņēmumiem kontrolēt īstermiņa, ikdienas krājumu papildināšanu. Šo procesu var aprakstīt arī ar nosaukumu *Neto vajadzību plāns*. Papildinformāciju skatiet sadaļā [Vispārējais pārskats](master-plans.md).

- **Prognožu plānošana** — Prognožu grafiks aprēķina bruto vajadzības. Tas ir balstīts uz nākotnes plānošanu (jeb prognozēm) un ļauj uzņēmumiem veikt materiālu un jaudas ilgtermiņa plānošanu. Papildinformāciju skatiet rakstā [Pieprasījuma prognozēšanas pārskats](introduction-demand-forecasting.md).

- **Starpuzņēmumu vispārējā plānošana** — Starpuzņēmumu vispārējais plāns aprēķina neto vajadzības dažādās juridiskajās personās. Tas savieno pieprasījumu un piedāvājumu starp uzņēmumiem — ne tikai īstermiņa, apstiprināto pieprasījumu un piedāvājumu, bet arī ilgtermiņa, plānoto (tādu, kas vēl nav apstiprināts) pieprasījumu un piedāvājumu. Papildinformāciju skatiet šeit: [Starpuzņēmumu plānošana](planning-optimization/Intercompany-planning.md).

Uzņēmumi var mainīt plāna izvadi. Viņi var palaist reģeneratīvu plānošanu, neto izmaiņu plānošanu vai abas. Reģeneratīvie plāni atjaunina visas prasības, bet neto izmaiņu plāni atjaunina tikai plānu par krājumiem ar jaunām vajadzībām, kas ir radušās kopš pēdējās plānošanas izpildes.

Vispārējās plānošanas plāni parasti attiecas uz īsu termiņu — tas varētu būt jebkāds periods no vienas nedēļas līdz sešiem mēnešiem. Vispārējās plānošanas modulis nosaka piedāvājuma (materiāli) un jaudas (resursi) vajadzības, kas atbildīs pašreizējam pieprasījumam (neto vajadzības). Vairumā uzņēmumu tas tiek paplašināts, lai ietvertu visgarāko kumulatīvo izpildes laiku starp saņemamajiem produktiem.

## <a name="learning-map"></a>Mācību karte

Nākamajā mācību kartē ir parādītas galvenās koncepcijas un uzdevumi, kuri veido moduļa Vispārējā plānošana struktūru. Lai apgūtu šī moduļa lietošanu, noklikšķiniet uz saitēm sadaļā [Ātrās saites](#quick-links).

[![Vispārējās plānošanas mācību karte.](./media/master-planning-learning-map.png)](./media/master-planning-learning-map.png)

## <a name="quick-links"></a>Tiešās saites

- [Vispārējo plānu pārskats](master-plans.md)  
- [Ierobežotā plāna ģenerēšana](./tasks/constrained-plan.md)
- [Materiālu plāna izveide līdzproduktiem](./tasks/create-material-plan-co-products.md)
- [Vispārēja plānošanas un vairākvietu funkcionalitātes pārskats](master-plan-multisite-functionality.md)
- [Starpuzņēmumu plāna izveide](./tasks/create-intercompany-plan.md)
- [Pārskats par pieprasījuma prognozēšanu](introduction-demand-forecasting.md)
- [Prognozes samazināšanas principi](reduction-keys.md)

## <a name="additional-resources"></a>Papildu resursi

### <a name="roadmaps"></a>Rīcības plāni

Lai apskatītu, kādi jauni līdzekļi ir izlaisti un kādi līdzekļi vēl tiek izstrādāti, dodieties uz vietni [Microsoft Dynamics 365 rīcības plāns](https://roadmap.dynamics.com/).

### <a name="blogs"></a>Emuāri

Viedokļi, jaunumi un cita informācija par moduli Vispārējā plānošana un citiem risinājumiem ir pieejami [Dynamics AX ražošanas pētniecības un attīstības darba grupas emuārā](/archive/blogs/axmfg/) un [Supply Chain Management programmā Dynamics AX pētniecības un attīstības darba grupas emuārā](https://blogs.msdn.microsoft.com/dynamicsaxscm).

### <a name="task-guides"></a>Uzdevumu ceļveži

Papildu palīdzība ir pieejama uzdevumu ceļvežu formā. Lai piekļūtu uzdevumu ceļvežiem, jebkurā lapā noklikšķiniet uz pogas **Palīdzība**.

### <a name="webinars"></a>Tīmekļsemināri

[Azure algoritmiskās mācīšanās lietošana pieprasījuma prognozēšanai](https://www.youtube.com/watch?v=4nQsccdFFDA&feature=youtu.be)

### <a name="tech-conference-recordings"></a>Tehnoloģiju konferences ieraksti

- [Pieprasījuma prognozēšanas funkcionalitātes paplašināšana](https://www.youtube.com/watch?v=4OIKIXLiNjI&feature=youtu.be)
- [Vispārējā plānošana — padomi un metodes problēmu novēršanai](https://youtu.be/7v8BPmEs9Dg)
- [MRP veiktspējas uzlabošana](https://youtu.be/RLXybx20B5o)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]