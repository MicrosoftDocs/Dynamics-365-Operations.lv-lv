---
title: Budžeta priekšlikumu iespējošana
description: Šajā tēmā skaidrots, kā ieslēgt budžeta priekšlikuma līdzekli Finanšu ieskatos.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: ab65d1b0e366bfe6bdb07688f89d440662165063
ms.sourcegitcommit: 822aea26c5da259efe11ff3b3dc4cf1598425689
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/16/2021
ms.locfileid: "7386490"
---
# <a name="enable-budget-proposals"></a>Budžeta priekšlikumu iespējošana

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidrots, kā ieslēgt budžeta priekšlikuma līdzekli Finanšu ieskatos.

1. Izmantojiet informāciju no vides lapas Microsoft Dynamics Lifecycle Services (LCS), lai izveidotu savienojumu ar Azure SQL primāro instanci šai videi. Palaidiet tālāk norādīto Transact-SQL (T-SQL) komandu, lai ieslēgtu ierobežotos līdzekļus smilškastes videi. (Iespējams, būs LCS jāieslēdz piekļuve savai IP adresei pirms varēsiet izveidot attilināto savienojumu ar programmas objektu serveri \[AOS\].)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > Izlaidiet šo darbību, ja izmantojat versiju 10.0.20 vai jaunāku versiju, vai, ja izmantojat Service Fabric izvietojumu. Finanšu ieskatu grupai jau vajadzētu ieslēgt jums šo ierobežoto līdzekli. Ja neredzat līdzekli darbvietā **Līdzekļu pārvaldība** vai ja rodas problēmas, mēģinot to ieslēgt, sazinieties ar <fiap@microsoft.com>.

2. Atveriet darbvietu **Līdzekļu pārvaldība** un veiciet tālāk norādītās darbības.

    1. Atlasiet **Pārbaudīt atjauninājumus**.
    2. Sameklējiet **Budžeta priekšlikums** un ieslēdziet šo līdzekli.

3. Doties uz **Budžeta veidošana \> Iestatīšana \> Pamata budžeta veidošana \> Budžeta priekšlikums (priekšskatījums)** un atlasiet **Iespējot līdzekli**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
