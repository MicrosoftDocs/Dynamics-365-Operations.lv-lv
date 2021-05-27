---
title: Virsgrāmatas noklusētie apraksti
description: Noklusētos aprakstus var izmantot, lai atjauninātu lauka Apraksts dokumentu grāmatojumus Virsgrāmatā.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 25dd72c86b22b50eccef22a5d2cbcfcf04280684
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021616"
---
# <a name="default-descriptions-for-the-general-ledger"></a>Virsgrāmatas noklusētie apraksti

[!include [banner](../../includes/banner.md)]

Noklusētos aprakstus var izmantot, lai atjauninātu lauka **Apraksts** dokumentu grāmatojumus Virsgrāmatā. Šī funkcionalitāte ir uzlabota darbam ar Kopīgajām izmaksām.

Lai iestatītu noklusējuma aprakstus virsgrāmatas grāmatojumi, dodieties uz sadaļu **Organizācijas administrēšana \> Iestatījumi \> Noklusētie apraksti**.

Šajā tabulā uzskaitītas jaunās vērtības, kas ir pievienotas laukam **Apraksts** lapā **Noklusējuma apraksti**, lai atbalstītu Kopīgās izmaksas.

| Apraksta veids | Piezīmes |
|---|---|
| Importa izmaksu aprēķināšana - izmaksu uzkrājums | Kad pirkšanas pasūtījuma rēķins tiek grāmatots, izmaksu uzkrājums tiek apstrādāts prognozētajām reisa izmaksām. Var norādīt noklusējuma aprakstus, lai aprakstam pievienotu reisa numuru. Sūtīšanas numuram izmantojiet *%4*. |
| Importa izmaksu aprēķināšana - tranzītpreču pasūtījums | Ja izmantojat tranzīta apstrādi, pirkšanas pasūtījuma rēķins tiek grāmatots un preces tiek grāmatotas tranzītkontā. Var norādīt noklusējuma aprakstus, lai aprakstam pievienotu reisa numuru. Lietojiet *%4* tranzīta pasūtījuma numuram. |
| Krājumi - Slēgšana - Korekcija | Ja kreditoru (AP) rēķins tiek apstrādāts reisa izmaksām, krājuma korekcija tiek apstrādāta, lai novērtētu reisa izmaksas. Var norādīt noklusējuma aprakstus, lai aprakstam pievienotu reisa numuru. Sūtīšanas numuram izmantojiet *%4*. |

Papildinformāciju par to, kā strādāt ar lapu **Noklusējuma apraksti**, skatiet sadaļā [Automātiskās grāmatošanas noklusēto aprakstu iestatīšana](../../finance/general-ledger/set-up-default-descriptions-for-automatic-posting.md).
