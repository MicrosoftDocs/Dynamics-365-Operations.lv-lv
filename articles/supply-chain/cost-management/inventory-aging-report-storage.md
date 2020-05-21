---
title: Krājumu vecumstruktūru pārskata glabāšana
description: Šajā tēmā aprakstīta funkcionalitāte, kas ļauj palaist krājuma novecošanas pārskatu un padarīt rezultātu pieejamu veidlapas un diagrammas veidā.
author: AndersGirke
manager: tfehr
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2019-01-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1e68833cc2b4430f66419a67b1cba5f6c8c209f4
ms.sourcegitcommit: 68092ed283bfbb7b6f611cce1b62c791f9b6a208
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/30/2020
ms.locfileid: "3323627"
---
# <a name="inventory-aging-report-storage"></a>Krājumu vecumstruktūru pārskata glabāšana

[!include [banner](../includes/banner.md)]

Programmā Microsoft Dynamics 365 Supply Chain Management var palaist **Krājumu vecumstruktūru pārskata glabāšanas** rezultātus un padarīt tos pieejamus veidlapas un diagrammas veidā. Veidlapā kolonnas un uzkrātās bilances tiek dinamiski pielāgotas atkarībā no konfigurētā izkārtojuma. Diagramma sniedz vizuālu apskatu, kas atbalsta filtrēšanu, un ļauj detalizēti apskatīt detalizētu informāciju. Turklāt datu elements, kura nosaukums ir **Krājumu vecumstruktūru pārskats**, ļauj eksportēt **Krājumu vecumstruktūru pārskata glabāšana** rezultātus, kas tiek palaisti, piemēram, Microsoft Excel faila vai PDF faila formātā.

Šī **Krājumu vecumstruktūru pārskata glabāšanas** rezultātu palaišanas metode pārskatam noder gadījumos, ja izlaidē ir daudz rindu. Piemēram, izlaide saturēs daudzas rindas, ja jums ir 50 000 preces un 300 veikali, kas ir izveidoti kā noliktavas, un jūs pieprasāt krājumu novecošanu pēc preces, vietas un noliktavas.

## <a name="enable-the-inventory-value-storage-report-feature"></a>Iespējot Krājumu vērtības uzglabāšanas pārskata līdzekli

Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo sistēmā. Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un iespējotu to pēc nepieciešamības. Šeit līdzeklis tiek norādīts kā:

- **Modulis** - Izmaksu pārvaldība
- **Līdzekļa nosaukums** - krājumu vecumstruktūru pārskata uzglabāšana

## <a name="run-an-inventory-aging-report-storage"></a>Palaist Krājumu vecumstruktūru pārskata glabāšanu

1. Dodieties uz **Izmaksu pārvaldība \>Vaicājumi un pārskati\>Krājuma novecošanas ziņojuma glabātuve**.
1. Atlasiet **Jauns**.
1. Laukā **Procesa identifikators - nosaukums** ievadiet unikālu pārskata apstiprināšanas nosaukumu.
1. Atlasiet pārskatu **Identifikācija – ID** un pēc vajadzības to filtrējiet.

    Pārskata izpilde vienmēr tiek veikta pakešuzdevumā.

1. Kad pakešuzdevums ir pabeigts, izvade tiek rādīta lapā **Krājumu novecošanas pārskata glabātuve**.
1. Lai skatītu izlaidi kā formu, kurai ir tradicionāls režģa izkārtojums, atlasiet **Skatīt papildinformāciju**. Lai skatītu izlaidi kā apkopotu diagrammu, atlasiet **Skatīt diagrammu.**

    > [!NOTE]
    > Veidlapā netiek iekļautas starpsummas, kas definētas pārskata izkārtojumā.

Datu elements **Krājumu novecošanas pārskats** ļauj eksportēt **Krājumu vecumstruktūru pārskata glabāšana** pārskatu, lietojot filtru laukam **Procesa identifikators – nosaukums** jebkurā formātā, ko atbalsta datu pārvaldība.
