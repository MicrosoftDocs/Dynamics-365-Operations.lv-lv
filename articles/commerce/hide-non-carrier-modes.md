---
title: Paslēpt nepārvadātāja piegādes režīmus no POS sūtījuma opcijām
description: Šajā tēmā ir aprakstīta konfigurācijas opcija, kas var novērst nepārvadātāja piegādes režīmu parādīšanos atlasē, kad sūtījuma pasūtījumi tiek izveidoti pārdošanas punktā (POS) lietojumprogrammā.
author: hhainesms
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhaines
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: a5f08fc86dc093fd0ead219b808fa720a43f6b6b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797122"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a>Paslēpt nepārvadātāja piegādes režīmus no POS nosūtīšanas opcijām


[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīta konfigurācijas opcija, kas ir pieejama pārdošanas punkta (POS) lietojumprogrammai. Izmantojot šo konfigurācijas opciju, tiek mainīta piegādes režīma izvēles izturēšanās, kad sūtījuma pasūtījumi tiek izveidoti punktā POS.

Kad lietotāji izveido klientu sūtījuma pasūtījumus punktā POS, viņi var izvēlēties sūtījuma piegādes režīmu. Šī funkcionalitāte ir pieejama neatkarīgi no tā, vai tiek nosūtīts viss pasūtījums vai tikai atlasītas rindas.

Pēc noklusējuma, dialoglodziņā, kur ir atlasīts piegādes režīms, ir redzami visi derīgie piegādes režīmi kanāla, preces un piegādes adreses kombinācijai. Šie piegādes režīmi ir definēti galvenās mītnes lapā **Piegādes režīmi** (**Pārdošana un mārketings \> Iestatījumi \> Sadale \> Piegādes režīmi**). "Nepārvadātāja" piegādes režīmi, piemēram, **Carryout** vai **Pickup**, var arī parādīties atlases dialoglodziņā.

Tomēr ir pievienots līdzeklis, kas ļauj paslēpt dialoglodziņā nepārvadātāja piegādes režīmus. Lai ieslēgtu šo līdzekli, lapā **Commerce parametri** cilnē **Debitors pasūtījumi** iestatiet opciju **Parādīt tikai pārvadātāja režīma opcijas pasūtījumu nosūtīšanai** uz **Jā**. Pēc tam, kad esat ieslēdzis šo funkciju un palaidis atbilstošos sadales darbus, lai sinhronizētu informāciju kanāla datu bāzē, nepārvadātāja piegādes režīmi netiks parādīti atlasē piegādes pasūtījumu izveides procesā punktā POS.


[!INCLUDE[footer-include](../includes/footer-banner.md)]