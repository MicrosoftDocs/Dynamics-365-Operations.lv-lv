---
title: Seguma iestatījumi
description: Šajā tēmā ir sniegta informācija par vajadzību iestatījumiem, kurus vispārējā plānošana izmanto, lai aprēķinātu krājumu vajadzības.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqItemTableWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2494
ms.assetid: 5a95ae4f-ca75-47d9-a1c3-68c97b42f166
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 99e094a7131b6d3a299fc72abd0141529908ddd2
ms.sourcegitcommit: 9e50bee6a67f0fe2fa6f86e02c7e8de16d0e2482
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538898"
---
# <a name="coverage-settings"></a>Seguma iestatījumi

[!include [banner](../includes/banner.md)]

Vispārējā plānošana izmanto vajadzības iestatījumus, lai aprēķinātu krājumu vajadzības.

Jūs varat norādīt vajadzības iestatījumus vairākos veidos:

- Norādiet vajadzību grupas vajadzības iestatījumus.

    Varat izveidot vajadzību grupu, kas satur iestatījumus visām precēm, kuras ir saistītas ar šo vajadzību grupu. Lai izveidotu seguma grupu, noklikšķiniet uz **Vispārējā plānošana &gt; Iestatīšana &gt; Vajadzība &gt; Vajadzības grupas**. Vajadzību grupu varat saistīt ar preci. Ja saite attiecas uz noteiktu vietu, noliktavu vai preces dimensiju, izmantojiet lauku **Vajadzības grupa** lapā **Krājumu vajadzība**. Ja saite ir vispārīga un nav atkarīga no preču dimensijām, izmantojiet lauku **Vajadzības grupa** lapas **Detalizēta informācija par preci** FastTab cilnē **Plāns**. Ja vajadzību grupa netiek saistīta ar preci, vispārējai plānošanai pēc noklusējuma tiek izmantota vispārējā vajadzību grupa, kas ir norādīta lapā **Vispārējās plānošanas parametri**.

- Norādiet preces vajadzības iestatījumus.

    Varat izveidot vajadzību iestatījumus noteiktai precei. Pārejiet uz sadaļu **Preču informācijas pārvaldība &gt; Preces &gt; Izlaistās preces**. Atlasiet preci un pēc tam lapas sadaļā Darbību rūts, cilnē **Plāns**, grupā **Vajadzība** noklikšķiniet uz **Krājumu vajadzība** , lai atvērtu lapu **Krājumu vajadzība**. Ja prece jau ir saistīta ar vajadzību grupu, varat ignorēt vajadzību grupas iestatījumus, izmantojot lauku **Ignorēt**. Vajadzības iestatījumiem lapā **Krājumu vajadzība** ir augstāka prioritāte nekā iestatījumiem lapā **Vajadzības grupa**.

- Norādiet preces vajadzības iestatījumus, izmantojot vedni.

    Vednī soli pa solim ir izskaidrots primāro krājumu vajadzību parametru iestatīšanas process. Lapas **Krājumu vajadzība** darbību rūtī noklikšķiniet uz **Vednis**, lai atvērtu sadaļu **Krājumu vajadzību vednis**.

- Norādiet dimensiju grupas vajadzības iestatījumus.

    Pārejiet uz sadaļu **Preču informācijas pārvaldība &gt; Preces &gt; Izlaistās preces**. Lapas **Detalizēta informācija par izlaistajām precēm** FasTab cilnes **Vispārīgi** sadaļā **Administrēšana** atlasiet saiti laukā **Noliktavas izmēru grupa**. Lapā **Noliktavas dimensiju grupas** atlasiet izvēles rūtiņu **Vajadzības plāns pa dimensijām**, lai izveidotu vajadzības iestatījumus dimensijai noliktavas dimensiju grupā. Lauks **Vajadzības plāns pa dimensijām** ir jāatlasa visām preces dimensijām, piemēram, konfigurācijai, krāsai, izmēram un stilam.

## <a name="additional-resources"></a>Papildu resursi

[Vispārējie plāni](master-plans.md)
