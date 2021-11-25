---
title: Ārējo datu izmantošana naudas plūsmas prognozēs
description: Šajā tēmā ir aprakstītas iestatīšanas darbības, kas jāveic, lai ārējos datus varētu ievadīt vai importēt naudas plūsmas prognozēs.
author: rcarlson
ms.date: 11/03/2021
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
ms.openlocfilehash: dbfa04228cf63c0874a7d69af4e2b932544c0d7f
ms.sourcegitcommit: 03fa7556840aa59f825697f6f9edeb58ea673fca
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/04/2021
ms.locfileid: "7753006"
---
# <a name="use-external-data-in-cash-flow-forecasts"></a>Ārējo datu izmantošana naudas plūsmas prognozēs

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Ārējos datus var ievadīt vai importēt naudas plūsmas prognozēs. Šajā tēmā ir aprakstītas iestatīšanas darbības, kas ir raksturīgas ārējo datu izmantošanai un kas ļauj ārējos datus iekļaut naudas plūsmas prognozē.

## <a name="external-data-setup"></a>Ārējo datu iestatīšana

Izmantojiet cilni Ārējais avots lapā Naudas plūsmas prognozes iestatīšana (Naudas plūsmas un bankas pārvaldības naudas plūsmas prognozēšana) lai ievadītu iestatījumus, kas atbalsta ārējo datu izmantošanu **·** naudas plūsmas **·** **\>\>** prognozēs.

Ārējos datus var ievadīt vai importēt naudas plūsmas prognozēs. Pirms ārējo datu ievadīšanas vai importēšanas, jāiestata ārējie avoti. Cilnē **Ārējais** avots iestatiet ārējās naudas plūsmas kategorijas. Kategorija var būt Izejošā **vai** **·** Ienākošā. **·** Kases/bankas grāmatojuma tips ir jāatlasa. Juridiskās **personas iestatījumu** režģī atlasiet juridiskās personas un atbilstošos galvenos kontus, uz kuriem attiecas ārējās naudas plūsmas kategorijas.

Papildinformāciju par to, kā iestatīt naudas plūsmas prognozes, skatiet sadaļā [Naudas plūsmas](../cash-bank-management/cash-flow-forecasting.md) prognozēšana.

## <a name="enter-external-data"></a>Ārējo datu ievadīšana

Lai naudas plūsmas prognozēm ievadītu un modificētu ārējos datus, varat izmantot programmu **Atvērt programmas Excel** pieredzi. Izvēlieties pogu Ārējie dati naudas plūsmas prognozes iestatījuma lapā un pēc tam izvēlieties Pievienot ārējos datus **·** vai Rediģēt **·** **·** **esošos ārējos** datus. Kad Microsoft Excel fails tiek atvērts, varat ievadīt informāciju šādos laukos:

- **Ieraksta ID** (unikāls)
- **Apraksts** (nav obligāts)
- **Ārējais avota** nosaukums – atlasiet vienu no vērtībām sarakstā, ko definējāt, kad iestatāt Finanšu ieskatus.
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
