---
title: Transakciju apstiprināšanas procesā lietoto kārtulu atspējošana
description: Šajā rakstā ir aprakstīta transakciju apstiprināšanas kārtulu atspējošanas funkcionalitāte produktā Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 12/11/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7d566aa3b829dad281528925a341382f9637fdba
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884881"
---
# <a name="disable-rules-used-in-the-transaction-validation-process"></a>Transakciju apstiprināšanas procesā lietoto kārtulu atspējošana

[!include [banner](../includes/banner.md)]

Mazumtirgotājiem var būt unikāli biznesa scenāriji un procesi. Tāpēc ne visas kārtulas, kas iekļautas tirdzniecības transakciju apstiprināšanas procesā, ir piemērojamas visiem mazumtirgotājiem. Lai pielāgotu atšķirības, Microsoft Dynamics 365 Commerce nodrošina funkcionalitāti, ko var izmantot, lai atspējotu nepiemērojamas kārtulas.

Lai skatītu kārtulas, kas pieejamas transakcijas apstiprināšanas procesam jūsu vidē, un skatītu katras kārtulas statusu, dodieties uz **Retail un Commerce \> Headquarters iestatīšana \> Parametri \> Commerce parametri** un atlasiet cilni **Transakciju apstiprināšana**. Visas iespējotās kārtulas tiek izmantotas, lai apstiprinātu transakcijas procesa **Veikala transakciju apstiprināšana** laikā, un šis process ir jāizpilda, lai transakcijas tiktu apkopotas un izliktas transakciju paziņojumā.

Pēc noklusējuma katras kārtulas statuss ir iestatīts uz **Iespējots**. Tāpēc visas kārtulas tiek izmantotas, lai apstiprinātu transakcijas, pirms tās tiek importētas tirdzniecības transakciju pārskatos. Lai atspējotu kārtulu, mainiet tās statusu uz **Atspējots**. Atspējotās kārtulas netiek ņemtas vērā, kad transakcijas tiek apstiprinātas procesa **Veikala transakciju apstiprināšana** laikā.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
