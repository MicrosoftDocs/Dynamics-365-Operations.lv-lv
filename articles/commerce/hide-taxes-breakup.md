---
title: Nodokļu pārtraukuma informācijas slēpšana pasūtījumu kopsavilkumos
description: Šajā rakstā ir aprakstīts, kā slēpt nodokļu pārtraukuma informāciju pasūtījuma kopsavilkumus par grozu, pārbaudi, pasūtījuma apstiprināšanu un pasūtījuma informācijas lapām Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 05/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-03-28
ms.openlocfilehash: fe1f6c5875444f4f91ee1dfb01b3fdaa527c52e5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881794"
---
# <a name="hide-tax-breakup-information-in-order-summaries"></a>Nodokļu pārtraukuma informācijas slēpšana pasūtījumu kopsavilkumos

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šajā rakstā ir aprakstīts, kā slēpt nodokļu pārtraukuma informāciju pasūtījuma kopsavilkumus par grozu, pārbaudi, pasūtījuma apstiprināšanu un pasūtījuma informācijas lapām Microsoft Dynamics 365 Commerce.

Pēc noklusējuma tiek Dynamics 365 Commerce parādīta nodokļu pārtraukuma informācija, lai apkopotu informāciju par grozu, čeku, pasūtījuma apstiprināšanu un detalizētas informācijas par pasūtījumu lapām. Attiecībā uz Commerce versijas 10.0.27 izlaidi Commerce Site Builder ietver opciju, kas ļauj jums slēpt nodokļu pārtraukuma informāciju pasūtījuma kopsavilkumos.

Šajā attēlā parādīts divu pasūtījumu kopsavilkumu piemērs. Pirmais parāda informāciju par nodokļu pārtraukumu, un otrais to paslēpj.

![Piemēri groziem, kur tiek rādīta un paslēpta nodokļu pārtraukuma informācija.](media/prices-include-sales-tax-e-Commerce.png)

> [!NOTE]
> - Opcija, lai **ar** pasūtījumu kopsavilkumu slēptu nodokļu pārtraukuma informāciju, ir pieejama tikai tad, ja e-komercijas kanāla e-komercijas **kanāla** opcijai Cenās ir iekļauts PVN, kas ir iestatīts uz Jā programmā Commerce Headquarters, **mazumtirdzniecības un commerce \> kanālu \>\> veikalos visi veikali**. 
> - Pēc noklusējuma opcija **Rādīt nodokļu pārtraukumu pasūtījuma kopsavilkumā ir** iespējota vietas veidotājā.

## <a name="hide-tax-breakup-information-in-order-summaries"></a>Nodokļu pārtraukuma informācijas slēpšana pasūtījumu kopsavilkumos

Lai pasūtījumu kopsavilkumos slēptu nodokļu pārtraukuma informāciju, sekojiet šiem soļiem.

1. Komercijas vietņu veidotājā dodieties uz vietu, ko vēlaties atjaunināt.
1. Dodieties uz **Vietnes iestatījumi \> Paplašinājumi**.
1. Notīriet **izvēles rūtiņu Rādīt nodokļu pārtraukumu pasūtījuma kopsavilkumā**.

Lai pasūtījumu kopsavilkumos parādītu nodokļu pārtraukuma informāciju, atzīmējiet **izvēles rūtiņu Rādīt nodokļu pārtraukumu pasūtījumu** kopsavilkumā.  

Šajā ilustrācijā parādīta izvēles **rūtiņa Rādīt nodokļu pārtraukumu pasūtījuma kopsavilkumā, kas** atzīmēta un atzīmēta vietas veidotājā.

![Rādīt nodokļu pārtraukumu pasūtījuma kopsavilkuma opcijā vietas veidotājā.](media/prices-include-sales-tax-e-Commerce-site-settings.png)

> [!NOTE]
> Ja esat pielāgojis pasūtījuma kopsavilkuma moduļus un nevēlaties pārmantot "slēpt nodokļu pārtraukuma informāciju pasūtījumu kopsavilkumu" funkcionalitātē Commerce versijā 10.0.27 vai vēlāk, skatiet pasūtījuma kopsavilkuma apakšsummu, kas neietver maksu nodokļus, [ja tiek lietoti pielāgoti pasūtījuma kopsavilkuma moduļi](troubleshoot/summary-taxes-custom-modules-10.0.27.md#resolution).

## <a name="additional-resources"></a>Papildu resursi

[PVN pārskats](/finance/general-ledger/indirect-taxes-overview)

[PVN tiešsaistes pasūtījumiem konfigurēšana](sales-tax-config.md)

[Problēmu novēršana: nodokļi tiešsaistes pasūtījumos ir nepareizi aprēķināti](troubleshoot/tax-miscalculated-online-order.md)
