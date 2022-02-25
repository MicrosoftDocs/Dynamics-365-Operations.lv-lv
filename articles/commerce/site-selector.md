---
title: Vietas izvēles modulis
description: Šī tēma aptver vietu izdošanas moduli un apraksta, kā pievienot to vietnes lapām Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 381163fdd6180a76def2e1bfb733f597b611c517
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109710"
---
# <a name="site-picker-module"></a>Vietas izvēles modulis

[!include [banner](includes/banner.md)]

Šī tēma aptver vietu izdošanas moduli un apraksta, kā pievienot to vietnes lapām Microsoft Dynamics 365 Commerce.

Ja uzņēmumam ir dažādas vietas tirgos, reģionos un lokalizācijās, vietas lietotājiem ir nepieciešams viegls veids, kā pārslēgties starp vietām un izvēlēties savu vēlamo iepirkšanās vietu. Lai pielāgotu šo scenāriju, vietas izvēles modulis ļauj lietotājiem pārlūkot vairākās vietās.

Vietas izvēles modulis jākonfigurē ar sarakstu ar vietām (tirgiem, reģioniem vai darbības vietām), kuras vietas lietotāji var pārlūkot.

> [!NOTE]
> Vietas izvēles modulis ir pieejams Dynamics 365 Commerce 10.0.14 izlaidē.

Šajā attēlā parādīts vietas atlasītāja moduļa piemērs, kas atrodas vietas lapas galvenē.

![Vietas izdošanas moduļa piemērs vietnes lapas galvenē.](./media/ecommerce-sitepicker.PNG)

## <a name="site-picker-module-properties"></a>Vietas atlasītāja moduļa rekvizīti

| Rekvizīta nosaukums | Vērtība                 | Apraksts |
|---------------|-----------------------|-------------|
| Virsraksts       | Teksts                  | Moduļa virsraksts. |
| Vietnes opcijas  | Nosaukums, attēls, vietrādis URL      | Šis rekvizīts norāda nosaukumu, saiti uz vietas mājas lapu un neobligātu attēlu, ko rādīt katrai vietai, kas ir iekļauta modulī. Attēls var būt karodziņš vai kāds tirgus, reģiona vai lokalizācijas attēlojums. |

## <a name="add-a-site-picker-module-to-a-page"></a>Vietnes atlasītāja moduļa pievienošana lapai

Vietas uztvērēja moduli var pievienot virsraksta **moduļa vietnes** atlasītāja [slotam](author-header-module.md). Pēc tam, kad vietas atlasītāja modulis ir pievienots, jūs variet definēt moduļa virsrakstu un vietas opcijas. Galvenokārt virsraksta modulis ir ietverts virsraksta fragmentā, ko var koplietot vietas e-komercijas lapās. Šajā piemērā vietas atlasītāja modulis ir pievienots virsraksta moduļa, kas atrodas virsraksta fragmentā ar nosaukumu HeaderContainer, **slotam Site picker** **.**

![Vietas izvēles moduļa piemērs virsraksta fragmentā.](./media/ecommerce-sitepicker-2.png)

## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Galvenes modulis](author-header-module.md)

[Atpakaļceļa modulis](add-breadcrumb.md)

[Navigācijas izvēlnes modulis](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
