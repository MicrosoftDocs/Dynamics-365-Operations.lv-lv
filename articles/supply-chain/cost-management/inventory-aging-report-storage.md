---
title: Krājumu vecumstruktūru pārskats
description: Šajā tēmā aprakstīta funkcionalitāte, kas ļauj palaist krājuma novecošanas pārskatu un padarīt rezultātu pieejamu veidlapas un diagrammas veidā.
author: AndersGirke
manager: AnnBe
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 21411c104c854224ff3689dc8e080b88d9fc7d23
ms.sourcegitcommit: 9267608347c9781fb4ba70f1384ca24da69c716d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/15/2019
ms.locfileid: "2810255"
---
# <a name="inventory-aging-report"></a>Krājumu vecumstruktūru pārskats


[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Programmā Microsoft Dynamics 365 Supply Chain Management var palaist **Krājumu novecošanas ziņojumu** un padarīt rezultātu pieejamu veidlapas un diagrammas veidā. Veidlapā kolonnas un uzkrātās bilances tiek dinamiski pielāgotas atkarībā no konfigurētā izkārtojuma. Diagramma sniedz vizuālu apskatu, kas atbalsta filtrēšanu, un ļauj detalizēti apskatīt detalizētu informāciju. Turklāt datu elements, kura nosaukums ir **Krājumu novecošanas pārskats**, ļauj eksportēt **Krājumu novecošanas pārskata** rezultātus, kas tiek palaisti, piemēram, Microsoft Excel faila vai PDF faila formātā.

Šī **Krājumu novecošanas** palaišanas metode pārskatam noder gadījumos, ja izlaidē ir daudz rindu. Piemēram, izlaide saturēs daudzas rindas, ja jums ir 50 000 preces un 300 veikali, kas ir izveidoti kā noliktavas, un jūs pieprasāt krājumu novecošanu pēc preces, vietas un noliktavas.

## <a name="run-an-inventory-aging-report"></a>Krājuma novecošanas pārskats

1. Dodieties uz **Izmaksu pārvaldība \>Vaicājumi un pārskati\>Krājuma novecošanas ziņojuma glabātuve**.
1. Atlasiet **Jauns**.
1. Laukā **Procesa identifikators - nosaukums** ievadiet unikālu pārskata apstiprināšanas nosaukumu.
1. Atlasiet pārskatu **Identifikācija – ID** un pēc vajadzības to filtrējiet.

    Pārskata izpilde vienmēr tiek veikta pakešuzdevumā.

1. Kad pakešuzdevums ir pabeigts, izvade tiek rādīta lapā **Krājumu novecošanas pārskata glabātuve**.
1. Lai skatītu izlaidi kā formu, kurai ir tradicionāls režģa izkārtojums, atlasiet **Skatīt papildinformāciju**. Lai skatītu izlaidi kā apkopotu diagrammu, atlasiet **Skatīt diagrammu.**

    > [!NOTE]
    > Veidlapā netiek iekļautas starpsummas, kas definētas pārskata izkārtojumā.

Datu elements **Krājumu novecošanas pārskats** ļauj eksportēt **Krājuma novecošanas** pārskata rezultātu, lietojot filtru laukam **Procesa identifikators – nosaukums** jebkurā formātā, ko atbalsta datu pārvaldība.
