---
title: Vecāko partiju rādīšanas noliktavā konfigurēšana, izmantojot mobilo ierīci
description: Šajā rakstā ir aprakstīts, kā iestatīt mobilo ierīci, lai tiktu parādīts to atrašanās vietu saraksts, kuru partijas ir vecākas par pašreizējo darba rindas atrašanās vietu.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5788b42483f2c3046b0d20f45115b98d62cce213
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900540"
---
# <a name="configure-display-older-batches-within-warehouse-on-a-mobile-device"></a>Vecāko partiju rādīšanas noliktavā konfigurēšana, izmantojot mobilo ierīci

[!include [banner](../includes/banner.md)]

Konfigurācija **Rādīt vecākās partijas noliktavā** ļauj parādīt sarakstu ar novietojumiem, kuru partijas ir vecākas par pašreizējo darba rindas novietojumu. Parādītajā novietojumu sarakstā ir iekļauta informācija par vecākajām partijām novietojumā, katrai partijai norādot beigu datumu un fiziskos krājumus. Varat izvēlēties izdot no jauna novietojuma vai turpināt izdot no pašreizējā novietojuma. 
- Izdot no jauna novietojuma — ja atlasāt jaunu novietojumu, no kura izdot, pašreizējā darba rinda tiks atjaunināta jaunā novietojuma izmantošanai un darbs turpināsies jaunajā novietojumā, kā parasti. Lai jaunais novietojums būtu derīgs, tajā ir jābūt pietiekamam pieejamajam daudzumam visai darba rindai. Ja nepieciešamais daudzums nebūs pieejams, darba rinda netiks atjaunināta un tiks parādīts saraksts. 
- Turpināt izdot no pašreizējā novietojuma — ja turpināsit izmantot pašreizējo darba rindas novietojumu, darba rindas daudzumus turpinās izdot no sākotnējā novietojuma.

## <a name="where-it-applies"></a>Darbības tvērums
Vecāko partiju rādīšana noliktavā tiek konfigurēta mobilās ierīces izvēlnes vienumos, un tā ietekmē izdošanu partijā iekļautajiem krājumiem.

## <a name="set-up-display-older-batches-within-warehouse"></a>Vecāko partiju rādīšanas noliktavā iestatīšana
Konfigurācija **Rādīt vecākās partijas noliktavā** ir pieejama mobilās ierīces izvēlnes vienumiem, ja opcija **Izdot vecāko partiju** ir iestatīta uz **Brīdināt**.

- Sadaļā **Noliktavas pārvaldība** > **Iestatīšana** > **Mobilā ierīce** > **Mobilās ierīces izvēlnes vienumi** iestatiet opciju **Izmantot esošo darbu** uz **Jā** izvēlnes vienumam un laukā **Izdot vecāko partiju** atlasiet **Brīdināt**. 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]