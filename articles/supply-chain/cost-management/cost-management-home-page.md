---
title: "Izmaksu pārvaldības sākumlapa"
description: "Izmantojot izmaksu pārvaldību, varat veikt izejmateriālu, daļēji pabeigto preču, nepabeigto preču, pabeigto preču un nepabeigtās ražošanas līdzekļu novērtēšanu un uzskaiti."
author: AndersGirke
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cab2f165a70e5ce8f09f0391282e055e51afb225
ms.openlocfilehash: b1513e5a7cb3a19fd3743a5aac8efd211aa02ce8
ms.contentlocale: lv-lv
ms.lasthandoff: 02/21/2018

---

# <a name="cost-management-home-page"></a>Izmaksu pārvaldības sākumlapa

[!INCLUDE [banner](../includes/banner.md)]

Izmantojot [izmaksu pārvaldību (video)](https://www.youtube.com/watch?v=vXzlC-mOBcg&feature=youtu.be), varat veikt izejmateriālu, daļēji pabeigto preču, nepabeigto preču, pabeigto preču un nepabeigtās ražošanas līdzekļu novērtēšanu un uzskaiti. Šī process ietvaros tiek definēta un pārvaldīta [krājumu uzskaite](cost-object.md) un [ražošanas uzskaite](bom-calculations.md), kā arī veidoti pārskati šīm uzskaitēm.

Izmaksu politikas var definēt šādās zonās: 
-  [Iepriekš noteiktas izmaksas](costing-versions.md)
-  [Krājumu uzskaite](cost-object.md)
-  [Ražošanas uzskaite](bom-calculations.md)
-  [Netiešā izmaksu uzskaite](costing-sheets.md)
-  [Virsgrāmatas integrācija](production-order-cost-analysis.md)

Piemēram, varat noteikt, kuras krājumu vērtēšanas metodes, piemēram, [FIFO](fifo-physical-value-marking.md), [svērto vidējo](weighted-average-physical-value-marking.md), [standarta izmaksas](prerequisites-standard-costs.md) vai [mainīgo vidējo](moving-average.md) vēlaties piemērot precēm [krājumu modeļu grupā](../inventory/reserve-inventory-quantities.md) krājumu uzskaitē.

Krājumu uzskaitei un ražošanas uzskaitei varat piekļūt no darbvietām **Izmaksu administrēšana** un **Izmaksu analīze**. Šīs darbvietas nodrošina visaptverošu pārskatu par pašreizējo statusu, izpildes pamatrādītājiem (KPI) un novirzes noteikšanu. 

Izmantojot ražošanas uzskaiti, varat apstrādēt [darbu pasūtījuma cenu](production-order-cost-analysis.md) ražošanas pasūtījumos un partijas pasūtījumos, kā arī veikt [atgriezenisko izmaksu aprēķināšanu](backflush-costing.md) LEAN ražošanas procesā.

[Power BI satura pakotnē Izmaksu pārvaldība](../../dev-itpro/analytics/cost-management-content-pack.md) ir sniegti pārvaldības ieskati par krājumiem un nepabeigto darbu (NP) krājumiem, kā arī par izmaksu plūsmu caur tiem pēc kategorijas laika gaitā. Šo informāciju var arī izmantot kā finanšu pārskata detalizētu papildinājumu.

### <a name="additional-resources"></a>Papildu resursi

#### <a name="whats-new-and-in-development"></a>Jaunumi un drīzumā

Lai apskatītu, kādi jauni līdzekļi ir izlaisti un kādi līdzekļi vēl tiek izstrādāti, dodieties uz [Microsoft Dynamics 365 rīcības plānu](https://roadmap.dynamics.com/). 

#### <a name="white-paper"></a>Tehniskais dokuments
Tēmā [MK aprēķināšana, izmantojot izmaksu aprēķina lapu](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/white-papers/365operationsbomcalsheet) ir aprakstīts, kā iestatīt izmaksu aprēķināšanas lapu, kurā ir ietverti materiāli un ražošana, un kā šī iestatīšana ietekmē MK aprēķina rezultātus. Lai labāk izskaidrotu šo tēmu, tajā ir aprakstīti konkrēti scenāriji un iekļauti dati, kas attēlo dažādu iestatījumu un konfigurāciju ietekmi. Jums nav obligāti jāseko šiem scenārijiem, jo šajā dokumentā nav sniegts pietiekami daudz informācijas to konfigurēšanai. Tomēr, ja jums ir pamatzināšanas, varat mēģināt atskaņot tālāk norādītos uzdevumu ceļvežus to rādīšanas secībā. Izmantojot zināšanas, ko ieguvāt, izlasot so dokumentu, veiciet MK aprēķinu analīzi. 

-  [Izveidot pabeigtu preci](tasks/create-finished-product-2016-02.md)
-  [Izveidot daļēji pabeigtu preci](tasks/create-semi-finished-product-2016-02.md)
-  [Izveidot izejmateriālus](tasks/create-raw-materials-2016-02.md)
-  [Izveidot MK](tasks/create-boms-2016-02.md)
-  [Izveidot maršrutus](tasks/create-routes-2016-02.md)
-  [MK aprēķināšana, izmantojot viena līmeņa struktūru](tasks/calculate-bom-single-level-structure-2016-02.md)
-  [MK aprēķināšana, izmantojot vairāklīmeņu struktūru](tasks/calculate-bom-multilevel-structure-2016-02.md)


#### <a name="blogs"></a>Emuāri
Viedokļi, jaunumi un cita informācija par moduli Izmaksu pārvaldība ir pieejami šeit: [Dynamics AX Manufacturing R&D darba grupas emuārs](https://blogs.msdn.microsoft.com/axmfg) un šeit: [Piegādes ķēdes pārvaldības programmā Dynamics AX R&D darba grupas emuārs](https://blogs.msdn.microsoft.com/dynamicsaxscm). Lai gan daži no šiem rakstiem tika rakstīti iepriekšējai moduļa Izmaksu pārvaldība versijai, joprojām ir spēkā tie paši jēdzieni, un arī procedūras pašreizējā versijā ir līdzīgas.

#### <a name="task-guides"></a>Uzdevumu ceļveži
Papildu palīdzībai programmā Finance and Operations ir pieejami uzdevumu ceļveži. Lai piekļūtu uzdevumu ceļvežiem, jebkurā lapā noklikšķiniet uz pogas Palīdzība.


