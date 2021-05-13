---
title: Lietot mērvienības iestatījumus
description: Šajā tēmā ir ietverti mērvienību iestatījumi un aprakstīts, kā tos lietot programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/23/2021
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2c5750ae506978dfac842eebf4ba6036322bdd7f
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937602"
---
# <a name="apply-unit-of-measure-settings"></a>Lietot mērvienības iestatījumus

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Šajā tēmā ir ietverti mērvienību iestatījumi un aprakstīts, kā tos lietot programmā Microsoft Dynamics 365 Commerce.

Preci var pārdot dažādās vienībās, piemēram, "katrs", "pāris" un "ducis." Programmā Commerce Headquarters precei var definēt mērvienību pēc pārdošanas un parādīt e-komercijas vietnē. Piemēram, ja mazumtirgotājs pārdod preci gan atsevišķi, gan dučos, pieejamās mērvienības var rādīt kopā ar citu informāciju par preci.

Šajā ilustrācijā parādīts, ka precei programmā Commerce Headquarters ir konfigurēta pārdošanas mērvienība **kt** (katrs).

![Tās preces piemērs, kas ir konfigurēta ar mērvienību programmā Commerce Headquarters](./media/Productunit-headquarters.PNG)

> [!NOTE]
> Atbalsts mērvienības pielietošanai un rādīšanai ir pieejams Commerce versijā 10.0.19 laidienā.

## <a name="unit-of-measure-settings"></a>Mērvienības iestatījumi

Mērvienības rādīšanas iestatījumi ir noteikti Commerce vietņu veidotājā **Vietnes iestatījumu \> Paplašinājumi \> Parādīt mērvienību precēm**. Pastāv trīs atbalstīti iestatījumi:

- **Nerādīt** - ja šis iestatījums ir atlasīts, e-komercijas vietne nerādīs preces mērvienību. Šī darbība ir noklusējuma darbība.
- **Rādīt preču iepirkšanas pieredzi** – ja ir atlasīts šis iestatījums, mērvienība tiek parādīta detalizētā informācijā par preci, grozu, norēķināšanos, pasūtījumu vēsturi un pasūtījumu detalizētās informācijas lapām.
- **Rādīt preču pārlūkošanas un pirkšanas pieredzi** – ja ir atlasīts šis iestatījums, mērvienība tiek parādīta preču pirkšanas pieredzes lapās un arī preču pārlūkošanas pieredzes laikā. Kā daļa no šīs uzvedības mērvienības tiek parādītas meklēšanas rezultātos un preču kolekcijas moduļos.

> [!IMPORTANT]
> Mērvienības rādīšanas iestatījumi ir pieejami Commerce versijā 10.0.19 laidienā. Ja veicat atjaunināšanu no vecākas Commerce versijas, ir manuāli jāatjaunina fails appsettings.json. Instrukcijas skatiet [SDK un moduļu bibliotēkas atjauninājumi](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="modules-that-use-unit-of-measure-settings"></a>Moduļi, kas izmanto mērvienības iestatījumus

Moduļi, kas izmanto mērvienības iestatījumus, ietver pirkšanas kasti, vēlmju sarakstu, grozu, groza ikonu, meklēšanas rezultātu konteineru, preču kolekciju, pārbaudi un pasūtījuma informācijas moduļus.

Piemērā šajā attēlā, preču informācijas lapa (product details page - PDP) parāda preces mērvienību (**kt**).

![PDP piemērs, kurā parādīta mērvienība](./media/Productunit-PDP.png)

Piemērā šajā attēlā, preču kolekcijas modulis parāda preces mērvienību (**kt**).

![Preču kolekcijas moduļa piemērs, kurā parādīta mērvienība](./media/Productunit-productcollection.png)

## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Groza modulis](add-cart-module.md)

[Pirkšanas lodziņa modulis](add-buy-box.md)

[Konta pārvaldības lapas un moduļi](account-management.md)

[SDK un moduļu bibliotēkas atjauninājumi](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
