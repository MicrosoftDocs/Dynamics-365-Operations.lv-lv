---
title: Ārējo datu izmantošana naudas plūsmas prognozēs (priekšskatījums)
description: Šajā tēmā ir aprakstītas iestatīšanas darbības, kas jāveic, lai ārējos datus varētu ievadīt vai importēt naudas plūsmas prognozēs.
author: rcarlson
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: b728314f4c4e18543e4f3b75fe1e7dcddc448ea0
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638540"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a>Ārējo datu izmantošana naudas plūsmas prognozēs (priekšskatījums)

[!include [banner](../includes/banner.md)]

Ārējos datus var ievadīt vai importēt naudas plūsmas prognozēs. Šajā tēmā ir aprakstītas iestatīšanas darbības, kas ir raksturīgas ārējo datu izmantošanai un kas ļauj ārējos datus iekļaut naudas plūsmas prognozē.

## <a name="external-data-setup"></a>Ārējo datu iestatīšana

Lietojiet cilni **Ārējais avots** lapā **Skaidras naudas plūsmas prognozes iestatījumi** (**Skaidras naudas un bankas pārvaldība \> Skaidras naudas plūsmas prognozēšana**), lai ievadītu iestatījumus, kas atbalsta ārējo datu izmantošanu naudas plūsmas prognozēs.

Papildinformāciju par skaitītāju iestatīšanu skatiet sadaļā [Skaidras naudas plūsmas prognozēšana](../cash-bank-management/cash-flow-forecasting.md).

Lai ievadītu ārējos datus naudas plūsmas prognozēm, varat izmantot Atvēršanas Excel programmā pieredzi, lai ievadītu mainītu ārējos datus. Atlasiet pogu **Ārējie dati** un pēc tam atlasiet opciju **Pievienot ārējos datus** vai **Rediģēt esošos ārējos datus**. Kad Microsoft Excel fails tiek atvērts, varat ievadīt informāciju šādos laukos:

- **Ieraksta ID**
- **Apraksts** (nav obligāts)
- **Ārējais avota nosaukums** — atlasiet vienu no vērtībām sarakstā, kuru definējāt, iestatot finanšu ieskatus.
- **Juridiska persona**
- **Datums**
- **Summa darījuma valūtā**
- **Valūtas kods**
- **Noklusējuma dimensija** (nav obligāts)
- **Dokumenta numurs** (nav obligāts)
- **Konta numurs** (nav obligāts)
- **Konta nosaukums** (nav obligāts)

## <a name="importing-external-data-by-using-the-data-management-framework"></a>Ārējo datu importēšana, izmantojot datu pārvaldības struktūru

Varat importēt ārējos datus naudas plūsmas prognozēm, izmantojot **datu pārvaldības** darbvietu un elementu, kam ir nosaukums **Naudas plūsmas prognozes ārējā avota ieraksts**.

Ja ir jāpārvieto iestatījumu dati no vienas vides uz citu, ir pieejamas šādas elementu apgabalam nepieciešamās iestatījumu tabulas:

- Skaidras naudas plūsmas prognozes ārējā avota iestatīšana
- Skaidras naudas plūsmas prognozes ārējā avota juridiskās personas iestatīšana

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
