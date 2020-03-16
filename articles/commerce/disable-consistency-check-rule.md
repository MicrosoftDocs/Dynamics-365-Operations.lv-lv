---
title: Kārtulu atspējošana mazumtirdzniecības transakciju konsekvences pārbaudītājā
description: Šajā tēmā ir aprakstīta transakciju konsekvences pārbaudītāja kārtulu atspējošanas funkcionalitāte risinājumā Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 51a02d6f305cbad9784cf1b811188d0e06b6f15b
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057641"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a>Kārtulu atspējošana mazumtirdzniecības transakciju konsekvences pārbaudītājā 

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Mazumtirgotājiem var būt unikāli biznesa scenāriji un procesi. Tāpēc ne visas kārtulas, kas iekļautas tirdzniecības transakciju konsekvences pārbaudītājā pēc noklusējuma, ir piemērojamas visiem mazumtirgotājiem. Lai pielāgotu atšķirības, Microsoft Dynamics 365 Commerce nodrošina funkcionalitāti, ko var izmantot, lai atspējotu nepiemērojamas kārtulas.

Lai skatītu sarakstu ar transakciju konsekvences pārbaudītājā pieejamajām kārtulām jūsu vidē un katras kārtulas statusu, dodieties uz **Mazumtirdzniecība un tirdzniecība \> Headquarters iestatīšana \> Parametri \> Tirdzniecības parametri** un atlasiet cilni **Transakciju validācija**.

Pēc noklusējuma katras kārtulas statuss ir iestatīts uz **Iespējots**. Tāpēc visas kārtulas tiek izmantotas, lai validētu transakcijas, pirms tās tiek importētas tirdzniecības pārskatos. Lai atspējotu kārtulu, mainiet tās statusu uz **Atspējots**. Atspējotās kārtulas netiek ņemtas vērā, kad transakcijas tiek validētas pārskata aprēķina procesa laikā.

Lai apietu visu validācijas procesu neatkarīgi no iespējotajām kārtulām, dodieties uz **Mazumtirdzniecība un tirdzniecība \> Headquarters iestatīšana \> Parametri \> Tirdzniecības parametri** un pēc tam cilnē **Transakciju validācija** iestatiet opciju **Atspējot konsekvences pārbaudītāju tirdzniecības transakcijām** uz **Jā**. Pēc tam, kad šī opcija ir iestatīta uz **Nē**, to nevar iestatīt atpakaļ uz **Jā** no lietotāja interfeisa (UI).
