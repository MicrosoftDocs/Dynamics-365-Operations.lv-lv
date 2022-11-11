---
title: Vizuāla un sadarbības izpilde
description: Šajā rakstā ir aprakstīts, kā pārraudzīt demand Driven Material Requirements plānošanu (DDMRP) dekompozīcijas punktus, bufera zonas, plānotos pasūtījumus un vēsturi.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ReqDDMRPWorkspace, ReqDecouplingPointsStatusByNetFlow, ReqDecouplingPointStatusByOnHand, ReqPlannedOrderForm, ReqItemDecoupledLeadTime
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: ce32a4449da8e85f958f212f2c2dfd2841ca6887
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740828"
---
# <a name="visual-and-collaborative-execution"></a>Vizuāla un sadarbības izpilde

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Šajā rakstā ir aprakstīts, kā pārraudzīt demand Driven Material Requirements plānošanu (DDMRP) dekompozīcijas punktus, bufera zonas, plānotos pasūtījumus un vēsturi.

## <a name="visually-track-buffers-and-quantities-for-a-selected-item"></a>Vizuāla buferu un daudzumu izsekošana atlasītajam krājumam

Programmā Microsoft Dynamics 365 Supply Chain Management varat vizuāli izsekot, kā kādai atlasītajai izlaistai precei laika gaitā mainās buferi, rīcībā esošie daudzumi un tīkla plūsmas līmeņi. Izpildiet šīs darbības, lai atvērtu un pārskatītu diagrammas.

1. Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.
1. Atlasiet izlaisto krājumu, kas ir iestatīts kā atšifrēšanas punkts. (Plašāku informāciju skatiet [Krājumu pozicionēšana](ddmrp-inventory-positioning.md).)
1. Darbību rūts cilnē Plāns **atlasiet** Krājumu **vajadzība**.
1. Krājumu vajadzības **lapā atlasiet** krājuma nodrošinājuma ierakstu, kas izveido atšifrēšanas punktu. (Šajā ierakstā tiks rādīts tās vajadzības grupas nosaukums, kura ir iestatīta dekompilēšanas punktu izveidojiet.)
1. Atlasiet cilni **Rīcībā esošie** krājumi. Šajā cilnē ir iekļauta diagramma, kurā parādīts, kā rīcībā esošie daudzumi laika gaitā mainīti kopā ar rīcībā esošo krājumu līmeņa vērtību, kas tika reģistrēta noteiktā periodā katru reizi, kad tiek palaista vispārējā plānošana. Cilne ietver arī tabulu, kas parāda, kuras no šādām kategorijām katra ierakstītā rīcībā esošajā līmenī ietilpst:

    - **Kritiski zems** – mazāks par pusi no perioda minimuma.
    - **Zema** – starp minimālo un minimālo.
    - **Vidējais rīcībā esošo krājumu daudzums** – starp minimālo un minimālo un zaļās zonas vērtību.
    - **Augstāks par vidējo** – Lielāks nekā vidējais.

    ![Rīcībā esošo krājumu vēsturiskie līmeņi.](media/ddmrp-on-hand-graph.png "Rīcībā esošo krājumu vēsturiskie līmeņi, kas atrodas cilnē")

    > [!NOTE]
    > Cilnē Rīcībā darbojas krāsas **, kas atšķiras no** cilnē Bufera vērtībām lietotajām līdzīgām **krāsām**.

1. Lai skatītu, kā bufera vērtības laika gaitā mainījās un kā tās tiek salīdzinātas ar rīcībā esošo un neto plūsmas līmeņiem, atlasiet **cilni Bufera** vērtības.

    ![Vēsturiskie rīcībā esošie un neto plūsmas līmeņi cilnē Bufera vērtības.](media/ddmrp-buffer-values-graph.png "Vēsturiskie rīcībā esošie un neto plūsmas līmeņi cilnē Bufera vērtības")

## <a name="track-the-status-and-planned-orders-for-all-decoupling-points"></a>Visu dekomupēšanas punktu statusa un plānoto pasūtījumu izsekošana

Uz **pieprasījumu balstīta MRP** darbvieta nodrošina vairākus rīkus kopā ar galvenajiem darba kvalitātes rādītājiem (KPI) un atšifrēšanas punktu krājumu un saistīto plānoto pasūtījumu statusa apskatu. Lai to atvērtu, dodieties uz vispārējās **plānošanas darbalauku \> pieprasījumu, \> kas virza MRP**.

![Pieprasījumam balstīta MRP darbvieta.](media/ddmrp-workspace.png "Pieprasījumam balstīta MRP darbvieta")

## <a name="get-overviews-of-decoupling-points-and-planned-orders"></a>Iegūstiet pārskatu par atšifrēšanas punktiem un plānotajiem pasūtījumiem

Papildus uz pieprasījumu **balstītai MRP** darbvietai Piegādes ķēžu pārvaldība nodrošina vairākas lapas, kur varat skatīt informāciju par jūsu DDMRP iestatīšanu, dekompozīcijas punktiem un plānotajiem pasūtījumiem. Dažas no šīm lapām arī nodrošina ērtas pogas Darbību rūtī, kas ļauj pārvaldīt buferus, palaist vispārējo plānošanu un atvērt citus saistītos skatus.

- Lai skatītu atšifrēšanas punktu statusu pēc neto plūsmas līmeņa, **\>\> pārejiet uz vispārējās plānošanas vispārējo plānošanu DDMRP \> atšifrēšanas punktu statusu pēc neto plūsmas**.
- Lai skatītu atšifrēšanas punktu statusu pēc rīcībā esošo krājumu līmeņa, **\>\> pārejiet uz vispārējās plānošanas vispārējo plānošanu DDMRP \> atšifrēšanas punktu statusu pēc rīcībā esošo krājumu.**
- Lai skatītu plānotos pasūtījumus atšifrēšanas punktiem, **\>\> pārejiet uz vispārējās plānošanas vispārējo plānošanu DDMRP plānotajiem \> pasūtījumiem atšifrēšanas punktiem.**
- Lai skatītu atšifrēto izpildes laikus, dodieties uz vispārējās **plānošanas vispārējo plānošanu \> DDMRP \> dekompozīcijas izpildes laiku \>**.

## <a name="clean-up-decoupling-point-buffer-values"></a>Tīrīt atšifrēšanas punktu bufera vērtības

Laika gaitā sistēma izveidos lielu vēsturisko datu daudzumu, kas ir saistīts ar notiekošajiem buferu aprēķiniem. Šie vēsturiskie dati izraisīs datu apjoma palielināšanos un visbeidzot var ietekmēt jūsu sistēmas veiktspēju. Tāpēc ieteicams reizēm iztīrīt vecās atšifrēšanas punkta bufera vērtības.

> [!WARNING]
> Tīrīšanas darbs noņems vēsturisko bufera vērtības iestatījumus un vēsturisko rīcībā esošo/neto plūsmas informāciju. Tas nav neatgriezeniski.

Izpildiet šīs darbības, lai iztīrītu dekompilēšanas punktu bufera vērtības.

1. Pārejiet uz **vispārējās plānošanas \> vispārējās plānošanas \> DDMRP \> tīrīšanas atšifrēšanas punktu bufera vērtībām**.
1. Dialoglodziņā Tīrīšanas **atšifrēšanas bufera vērtības** iestatiet šādus laukus:

    - **Dzēst ierakstus, kas vecāki par (dienām)** – norādiet vistāko saglabāto ierakstu vecumu dienās. Visi atšifrēšanas punkta bufera vērtību ieraksti, kas ir vecāki par šo vērtību, tiks dzēsti.
    - **Vispārējais** plāns – atlasiet vispārējo plānu, kas ietver krājumus, kurus šī tīrīšana ir ietekmējusi. Tīrīšana tiks piemērota visiem krājumiem plānā pēc tam, kad **ir** lietoti šajā dialoglodziņā norādītie filtra iestatījumi.

1. Lai ierobežotu ierakstu kopu, kam jāpalaiž pakešuzdevums, **kopsavilkuma** cilnē Ieraksti, kas jāiekļauj, atlasiet **·** **Filtrēt, lai atvērtu dialoglodziņu** Uzziņas. Šis dialoglodziņš darbojas tāpat, kā citiem fona darbu [tipiem](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) Piegādes ķēžu pārvaldībā.
1. Kopsavilkuma cilnes **Fonā cilnē** Palaist norādiet, kā un cik bieži tīrīšana jāveic. Lauki darbojas tāpat, kā citi [fona darbu](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) veidi pakalpojumā Supply Chain Management.
1. Atlasiet **Labi**, lai pievienotu jauno darbu pakešuzdevumu rindai izpildei.
