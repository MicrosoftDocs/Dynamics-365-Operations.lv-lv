---
title: Vietas atlasītāja modulis
description: Šajā tēmā tiek stāstīts par vietas atlasītāja moduli un aprakstīts, kā to pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: b4e5f715efcac7f883df99508d282db904be0d80
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665227"
---
# <a name="site-selector-module"></a>Vietas atlasītāja modulis

[!include [banner](includes/banner.md)]

Šajā tēmā tiek stāstīts par vietas atlasītāja moduli un aprakstīts, kā to pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Ja uzņēmumam ir dažādas vietas tirgos, reģionos un lokalizācijās, vietas lietotājiem ir nepieciešams viegls veids, kā pārslēgties starp vietām un izvēlēties savu vēlamo iepirkšanās vietu. Lai pielāgotu šo scenāriju, vietas atlasītāja modulis ļauj lietotājiem pārlūkot vairākās vietās.

Vietas atlasītāja modulis ir jākonfigurē ar vietu sarakstu (tirgiem, reģioniem vai lokalizācijām), ko vietas lietotāji var pārlūkot.

> [!NOTE]
> Vietas modulis ir pieejams Dynamics 365 Commerce 10.0.14 laidienā.

Attēlā zemāk ir parādīts vietas atlasītāja moduļa piemērs, kas attēlots vietas lapas galvenē.

![Vietas atlasītāja moduļa piemērs vietas lapas galvenē](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a>Vietas atlasītāja moduļa rekvizīti

| Rekvizīta nosaukums | Vērtība                 | Apraksts |
|---------------|-----------------------|-------------|
| Virsraksts       | Teksts                  | Moduļa virsraksts. |
| Vietnes opcijas  | Nosaukums, attēls, vietrādis URL      | Šis rekvizīts norāda nosaukumu, saiti uz vietas mājas lapu un neobligātu attēlu, ko rādīt katrai vietai, kas ir iekļauta modulī. Attēls var būt karodziņš vai kāds tirgus, reģiona vai lokalizācijas attēlojums. |

## <a name="add-a-site-selector-module-to-a-page"></a>Vietas atlasītāja moduļa pievienošana lapai

Vietas atlasītāja moduli var pievienot [Galvenes modulim](author-header-module.md) vietas atlasītāja slotā. Pēc tam, kad tas ir pievienots, varat definēt moduļa virsraksta un vietas opcijas.

## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Galvenes modulis](author-header-module.md)

[Atpakaļceļa modulis](add-breadcrumb.md)

[Navigācijas izvēlnes modulis](nav-menu-module.md)
