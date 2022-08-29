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
ms.openlocfilehash: ed07ae9784da3ca721fcb25a9c5a14c4f75f2e59
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277376"
---
# <a name="reference-original-invoices-in-credit-notes-vendor-invoices"></a>Atsauces uz sākotnējiem rēķiniem kredīta notās (kreditoru rēķini)

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā izveidot atsauci uz oriģinālo rēķinu, veidojot kredīta notu.

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
