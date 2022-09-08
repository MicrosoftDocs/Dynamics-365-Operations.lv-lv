---
title: Atsauces uz sākotnējiem rēķiniem kredīta notās (kreditoru rēķini)
description: Šajā rakstā ir aprakstīts, kā izveidot atsauci uz oriģinālo rēķinu, veidojot kredīta notu.
author: AdamTrukawka
ms.date: 09/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2021-09-23
ms.dyn365.ops.version: 10.0.20
ms.search.form: ''
ms.openlocfilehash: 39cf4eb7eef1a83abeb7bd44fa7b2abefee0806e
ms.sourcegitcommit: 8eb0cafe5ad20be2c4fff684e88d7d3f2249f820
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/06/2022
ms.locfileid: "9409669"
---
# <a name="reference-original-invoices-in-credit-notes-vendor-invoices"></a>Atsauces uz sākotnējiem rēķiniem kredīta notās (kreditoru rēķini)

[!include [banner](../includes/banner.md)]

Dažās valstīs un reģionos pastāv juridiska prasība, lai drukātās kredīta notas vai pārskata rutīnas ietvertu atsauces uz sākotnējiem rēķiniem. Šajā rakstā ir aprakstīts, kā izveidot atsauci uz oriģinālo rēķinu, veidojot kredīta notu.

## <a name="prerequisites"></a>Priekšnosacījumi

**Līdzekļu pārvaldības** darbvietā iespējojiet līdzekli **Iespējot kredīta rēķinu izrakstīšanu kreditoru rēķiniem**. Papildinformāciju skatiet [Līdzekļu pārvaldības pārskatā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Šajā rakstā aprakstītā funkcionalitāte attiecas uz tālāk minētajiem biznesa dokumentiem.

**Kreditori:**

- Pirkšanas pasūtījums
- Rēķinu žurnāls
- Rēķinu reģistrs

**Virsgrāmata:**

- Virsgrāmatas žurnāls

## <a name="define-a-reference-to-an-original-invoice"></a>Atsauces definēšana sākotnējam rēķinam

Atsauces uz oriģinālo rēķinu definēšana ietver sekojošos augsta līmeņa soļus:
1. Izveidojiet un grāmatojiet kreditora rēķinu.
2. Izveidojiet kreditora kredīta notu.
3. Izmantojiet kredīta rēķina izrakstīšanas fumu, lai sasaistītu rēķinu ar kredīta notu.
4. Grāmatojiet kredīta notu.

Izmantojiet tālāk uzskaitītās procedūras, lai definētu atsauces sākotnējiem rēķiniem, pamatojoties uz konkrēto uzņēmumu dokumentu veidiem.

### <a name="vendor-credit-note-purchase-order"></a>Kreditora kredīta nota (pirkšanas pasūtījums)

1. Atveriet **Kreditori** > **Pirkšanas pasūtījumi** > **Visi pirkšanas pasūtījumi**.
2. Izveidojiet jaunu pirkšanas pasūtījumu vai izmantojiet esošo, lai izveidotu kredīta notu.
3. Darbību rūts cilnes **Rēķins**, grupā **Ieviest** atlasiet **Kredīta rēķinu izrakstīšana**.
4. Ievadiet atsauci uz sākotnējo rēķinu un atlasiet labojuma pamatojumu.

### <a name="vendor-credit-note-ledger-journals"></a>Kreditora kredīta nota (Virsgrāmatas žurnāli)

1. Izpildiet kādu no šīm darbībām:

    - Pārejiet uz sadaļu **Kreditori** \> **Rēķinu žurnāls**.
    - Pārejiet uz sadaļu **Kreditori** \> **Rēķinu žurnāls**.
    - Ejiet uz **Virsgrāmata** \> **Žurnāla ieraksti** \> **Vispārējie žurnāli**.

2. Jauna žurnāla un jaunu žurnāla rindu izveide.
3. Transakciju rūtī atlasiet **Funkcijas** \> **Kredīta rēķina izrakstīšana**.
4. Ievadiet atsauci uz sākotnējo rēķinu un atlasiet labojuma pamatojumu.

> [!NOTE]
> **Kredīta rēķinu izrakstīšanas** komanda ir redzama Virsgrāmatas žurnāla dokumentā, ja **Konta tipa** lauks ir iestatīts kā **Kreditors**.
