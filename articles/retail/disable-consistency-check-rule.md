---
title: Kārtulu atspējošana mazumtirdzniecības transakciju konsekvences pārbaudītājā
description: Šajā tēmā ir aprakstīta mazumtirdzniecības transakciju konsekvences pārbaudītāja kārtulu atspējošanas funkcionalitāte risinājumā Microsoft Dynamics 365 Retail.
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
ms.openlocfilehash: 4bf8df2fb9f8f5c33ceb13eb012fb6879f81ec66
ms.sourcegitcommit: bdbca89bd9b328c282ebfb681f75b8f1ed96e7a8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/14/2019
ms.locfileid: "2586301"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a>Kārtulu atspējošana mazumtirdzniecības transakciju konsekvences pārbaudītājā 

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Mazumtirgotājiem var būt unikāli biznesa scenāriji un procesi. Tāpēc ne visas kārtulas, kas iekļautas mazumtirdzniecības transakciju konsekvences pārbaudītājā pēc noklusējuma, ir piemērojamas visiem mazumtirgotājiem. Lai pielāgotu atšķirības, Microsoft Dynamics 365 Retail nodrošina funkcionalitāti, ko var izmantot, lai atspējotu nepiemērojamas kārtulas.

Lai skatītu sarakstu ar mazumtirdzniecības transakciju konsekvences pārbaudītājā pieejamajām kārtulām jūsu vidē un katras kārtulas statusu, dodieties uz **Mazumtirdzniecība \> Headquarters iestatīšana \> Parametri \> Mazumtirdzniecības parametri** un atlasiet cilni **Transakciju validācija**.

Pēc noklusējuma katras kārtulas statuss ir iestatīts uz **Iespējots**. Tāpēc visas kārtulas tiek izmantotas, lai validētu mazumtirdzniecības transakcijas, pirms tās tiek importētas mazumtirdzniecības pārskatos. Lai atspējotu kārtulu, mainiet tās statusu uz **Atspējots**. Atspējotās kārtulas netiek ņemtas vērā, kad mazumtirdzniecības transakcijas tiek validētas pārskata aprēķina procesa laikā.

Lai apietu visu validācijas procesu neatkarīgi no iespējotajām kārtulām, dodieties uz **Mazumtirdzniecība \> Headquarters iestatīšana \> Parametri \> Mazumtirdzniecības parametri** un pēc tam cilnē **Transakciju validācija** iestatiet opciju **Atspējot konsekvences pārbaudītāju mazumtirdzniecības transakcijām** uz **Jā**. Pēc tam, kad šī opcija ir iestatīta uz **Nē**, to nevar iestatīt atpakaļ uz **Jā** no lietotāja interfeisa (UI).
