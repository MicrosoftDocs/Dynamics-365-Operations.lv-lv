---
title: Skaidras naudas plūsmas prognozēšanas iespējošana (priekšskatījums)
description: Šajā tēmā skaidrots, kā ieslēgt skaidras naudas plūsmas prognozēšanas līdzekli Finanšu ieskatos.
author: ShivamPandey-msft
ms.date: 06/03/2021
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
ms.openlocfilehash: ba8acb2191291e2abed5cabf234c19fe09e6c8ff
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222562"
---
# <a name="enable-cash-flow-forecasting-preview"></a>Skaidras naudas plūsmas prognozēšanas iespējošana (priekšskatījums)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šajā tēmā skaidrots, kā ieslēgt skaidras naudas plūsmas prognozēšanas līdzekli Finanšu ieskatos.

> [!NOTE]
> Lai izmantotu maksājumu prognozes skaidras naudas plūsmā, jāiestata debitora maksājumu prognožu līdzeklis, kā tas aprakstīts [Debitora maksājumu prognožu iespējošana](enable-cust-paymnt-prediction.md).

1. Izmantojiet informāciju no vides lapas Microsoft Dynamics Lifecycle Services (LCS), lai izveidotu savienojumu ar Azure SQL primāro instanci šai videi. Palaidiet tālāk norādīto Transact-SQL (T-SQL) komandu, lai ieslēgtu ierobežotos līdzekļus smilškastes videi. (Iespējams, būs LCS jāieslēdz piekļuve savai IP adresei pirms varēsiet izveidot attilināto savienojumu ar programmas objektu serveri \[AOS\].)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > Izlaidiet šo darbību, ja izmantojat versiju 10.0.20 vai jaunāku versiju, vai, ja izmantojat Service Fabric izvietojumu. Finanšu ieskatu grupai jau vajadzētu ieslēgt jums šo ierobežoto līdzekli. Ja neredzat līdzekli darbvietā **Līdzekļu pārvaldība** vai ja rodas problēmas, mēģinot to ieslēgt, sazinieties ar <fiap@microsoft.com>.
  
2. Atveriet darbvietu **Līdzekļu pārvaldība** un veiciet tālāk norādītās darbības.

    1. Atlasiet **Pārbaudīt atjauninājumus**.
    2. Ieslēdziet tālāk norādītos līdzekļus.

        - Jauna režģa vadīkla
        - Grupēšana režģos (priekšskatījums) 
        - Debitoru maksājumu prognozes (priekšskatījums)
        - Skaidras naudas plūsmas prognozēšana (priekšskatījums)

3. Dodieties uz **Skaidras naudas un bankas pārvaldība \> Skaidras naudas plūsmas prognozes iestatīšana** un pievienojiet likviditātes kontus, kas jāiekļauj prognozēs.

    > [!NOTE]
    > Ja likviditātes konti nav iestatīti, skaidras naudas plūsmu nevar ģenerēt.

4. Dodieties uz **Skaidras naudas un bankas pārvaldība \> Iestatīšana \> Finanšu ieskati (priekšskatījums) \> Skaidras naudas plūsmas prognozes (priekšskatījums)** un veiciet tālāk norādītās darbības.

    1. Cilnē **Skaidras naudas plūsmas prognoze** atlasiet **Iespējot līdzekli**.
    2. Atlasiet **Izveidot prognozēšanas modeli**.

Plašāku informāciju par to, kā iestatīt skaidras naudas plūsmas prognozēšanas iespēju, skatiet [Skaidras naudas plūsmas prognozēšana](cash-flow-forecast-intro.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
