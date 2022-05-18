---
title: Vietas izvēles modulis
description: Šī tēma aptver vietu izdošanas moduli un apraksta, kā pievienot to vietnes lapām Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/04/2022
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
ms.openlocfilehash: a1954f6b2fea35d5138218e6a2a23ab1fd04c8fc
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710307"
---
# <a name="site-picker-module"></a>Vietas izvēles modulis

[!include [banner](includes/banner.md)]

Šī tēma aptver vietu izdošanas moduli un apraksta, kā pievienot to vietnes lapām Microsoft Dynamics 365 Commerce.

Ja uzņēmumam ir dažādas vietas tirgos, reģionos un lokalizācijās, vietas lietotājiem ir nepieciešams viegls veids, kā pārslēgties starp vietām un izvēlēties savu vēlamo iepirkšanās vietu. Lai pielāgotu šo scenāriju, vietas izvēles modulis ļauj lietotājiem pārlūkot vairākās vietās. Vietņu izvēle ir [ieteicama](geo-detection-redirection.md) arī, kad jūsu e-komercijas vietnei ir ieviesta ģeogrāfiskā noteikšana un virzienmaiņa, tā, lai debitori varētu ignorēt vietas izvēli, ko tie [norāda, izmantojot valsts/reģiona atlasītāja moduli](country-region-picker-module.md). 

Vietas izvēles modulis jākonfigurē ar sarakstu ar vietām (tirgiem, reģioniem vai darbības vietām), kuras vietas lietotāji var pārlūkot. Šajā attēlā parādīts vietas atlasītāja moduļa piemērs, kas atrodas vietas lapas galvenē.

![Vietas izdošanas moduļa piemērs vietnes lapas galvenē.](./media/ecommerce-sitepicker.PNG)

## <a name="site-picker-module-properties"></a>Vietas atlasītāja moduļa rekvizīti

| Rekvizīta nosaukums | Vērtība                 | Apraksts |
|---------------|-----------------------|-------------|
| Virsraksts       | Teksts                  | Moduļa virsraksts. |
| Vietnes opcijas  | Nosaukums, attēls, vietrādis URL      | Šis rekvizīts norāda nosaukumu, saiti uz vietas mājas lapu un neobligātu attēlu, ko rādīt katrai vietai, kas ir iekļauta modulī. Attēls var būt karodziņš vai kāds tirgus, reģiona vai lokalizācijas attēlojums. |

## <a name="add-a-site-picker-module-to-a-page"></a>Vietnes atlasītāja moduļa pievienošana lapai

Vietas uztvērēja moduli var pievienot virsraksta **moduļa vietnes** atlasītāja [slotam](author-header-module.md). Pēc tam, kad vietas atlasītāja modulis ir pievienots, jūs variet definēt moduļa virsrakstu un vietas opcijas. Galvenokārt virsraksta modulis ir ietverts virsraksta fragmentā, ko var koplietot vietas e-komercijas lapās. 

Lai pievienotu vietas atlasītāja moduli virsraksta modulim, sekojiet šiem soļiem.

1. Virsraksta fragmenta **virsraksta moduļa** vietas izvēles slotā atlasiet daudzpunkti (**...**) un pēc tam atlasiet Pievienot **moduli**.
1. Dialoglodziņā Atlasīt **moduļus** pievienojiet vietnes izvēles **moduli un** pēc tam atlasiet **Labi**.
1. Vietnes izdošanas **rekvizītu rūtī** atlasiet Pievienot vietnes **opciju sarakstu**. Parādās rediģējamas **vietas opciju** saraksta opcija.
1. Atlasīt **vietnes opciju sarakstu**. Tiek **atvērts vietnes opciju** saraksta dialoglodziņš.
1. Sadaļā **Vietas** nosaukums ievadiet vietas nosaukuma tekstu, kas tiks rādīts vietas izvēles nolaižamajā sarakstā.
1. Sadaļā **Vietnes novirzīšanas VIETRĀDIs** URL **atlasiet Pievienot saiti**. Tiek **parādīta saites izdrukas** rūts.
1. Saites izdales **rūts** pievienošanas rūtī atlasiet Pielāgots **lapa un** pēc tam atlasiet **Tālāk**.
1. Vietņu vietrāžu URL sarakstā atlasiet vietrādi URL ar ceļu, ko izveidojāt, pievienojot kanālu vietnei (piemēram, `www.adventure-works.com/fr-ca`), un pēc tam atlasiet **Lietot**.
1. Atlasiet **Labi**.
1. Atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.
1. Atlasiet **Publicēt,** lai publicētu lapu.

Šajā piemērā vietas atlasītāja modulis ir pievienots virsraksta moduļa, kas atrodas virsraksta fragmentā ar nosaukumu HeaderContainer, **slotam Site picker** **.**

![Vietas izvēles moduļa piemērs virsraksta fragmentā.](./media/ecommerce-sitepicker-2.png)

## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Galvenes modulis](author-header-module.md)

[Atpakaļceļa modulis](add-breadcrumb.md)

[Navigācijas izvēlnes modulis](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
