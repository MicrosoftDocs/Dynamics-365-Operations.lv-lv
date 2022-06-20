---
title: Virsgrāmatas noklusētie apraksti
description: Noklusētos aprakstus var izmantot, lai atjauninātu lauka Apraksts dokumentu grāmatojumus Virsgrāmatā.
author: Weijiesa
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TransactionTexts
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 7020c39dd599be047e07caa391d6d4c69c426328
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889553"
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
