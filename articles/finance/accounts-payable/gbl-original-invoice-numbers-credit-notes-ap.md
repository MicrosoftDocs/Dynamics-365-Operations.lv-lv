---
title: Atsauces uz sākotnējiem rēķiniem kredīta notās (kreditoru rēķini)
description: Šajā tēmā ir aprakstīts, kā izveidot atsauci uz oriģinālo rēķinu, veidojot kredīta notu.
author: v-oloski
ms.date: 09/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-oloski
ms.search.validFrom: 2021-09-23
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6114ffb4d3b9e942887cbfa10c6039b0d73af7e1
ms.sourcegitcommit: 86f0574363fb869482ef73ff294f345f81d17c5b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7562230"
---
# <a name="reference-original-invoices-in-credit-notes-vendor-invoices"></a>Atsauces uz sākotnējiem rēķiniem kredīta notās (kreditoru rēķini)

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā izveidot atsauci uz oriģinālo rēķinu, veidojot kredīta notu.

## <a name="prerequisites"></a>Priekšnosacījumi

**Līdzekļu pārvaldības** darbvietā iespējojiet līdzekli **Iespējot kredīta rēķinu izrakstīšanu kreditoru rēķiniem**. Papildinformāciju skatiet [Līdzekļu pārvaldības pārskatā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Šajā tēmā aprakstītā funkcionalitāte attiecas uz šādiem uzņēmuma dokumentiem.

**Kreditori:**

- Pirkšanas pasūtījums
- Rēķinu žurnāls
- Rēķinu reģistrs

**Virsgrāmata:**

- Virsgrāmatas žurnāls

## <a name="define-a-reference-to-an-original-invoice"></a>Atsauces definēšana sākotnējam rēķinam

Izmantojiet tālāk uzskaitītās procedūras, lai definētu atsauces sākotnējiem rēķiniem, pamatojoties uz konkrēto uzņēmumu dokumentu veidiem.

### <a name="vendor-credit-note-purchase-order"></a>Kreditora kredīta nota (pirkšanas pasūtījums)

1. Dodieties uz **Kreditori** \> **Pirkšanas pasūtījumi** \> **Visi pirkšanas pasūtījumi**.
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
