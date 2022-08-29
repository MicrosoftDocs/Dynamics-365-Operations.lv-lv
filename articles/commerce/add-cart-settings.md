---
title: Iestātījumu Pievienot preci grozam lietošana
description: Šajā rakstā ir ietverti iestatījumi "Pievienot preci grozam" un aprakstīts, kā tos piemērot Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 16644e6746d182cd86a40861c4e30a85a9d3d478
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277032"
---
# <a name="apply-add-product-to-cart-settings"></a>Iestātījumu Pievienot preci grozam lietošana

[!include [banner](includes/banner.md)]

Šajā rakstā ir apskatīti **sadaļā Pievienot preci groza iestatījumiem** un aprakstīts, kā tos piemērot Microsoft Dynamics 365 Commerce.

Ja prece tiek pievienota grozam Dynamics 365 Commerce e-komercijas vietnē, tiek atbalstītas dažādas darbplūsmas. Piemēram, vietnes lietotājs var tikt aizvests uz groza lapu. Vai arī lietotājs var palikt pašreizējā lapā, bet saņem paziņojumu, kas apstiprina, ka prece tika pievienota grozam.

Lai atbalstītu dažādas darbplūsmas, Commerce vietņu veidotājā **Iestatījumi \> Paplašinājumi** ir pieejams lauks **Pievienot preci grozam**. Izvēlieties vienu no šīm iestatīšanas opcijām, lai ieviestu atbilstošu darbplūsmu:

- **Doties uz lapu Grozs**– Lietotājs, pievienojot grozam krājumu, tiek aizvests uz lapu Grozs.
- **Rādīt paziņojumu** – Lietotājs, pievienojot grozam vienumu, saņem apstiprinājuma paziņojumu un var turpināt pārlūkot preces informācijas lapā (PDP).
- **Parādīt mini grozu** - Kad lietotāji pievieno krājumu grozam, tiek parādīts mini groza saturs. Lietotāji var pārskatīt visas grozā esošās preces un pāriet uz izrakstīšanos, ja tās ir gatavas.
- **Parādīt paziņojumus, izmantojot Paziņojumu moduli** - Kad lietotāji pievieno krājumu grozam, paziņojumu modulis tiek izmantots, lai parādītu apstiprinājuma paziņojumu. Lai darbotos šī iestatījuma opcija, paziņojumu modulis ir jāpievieno lapas virsrakstam.
- **Nepārejiet uz lapu Grozs**– Lietotājs, pievienojot grozam krājumu, paliek pašreizējā lapā..

Šajā attēlā parādīts piemērs iestatīšanas opcijām **Pievienot preci grozam** vietnes veidotājā.

![Piemērs iestatīšanas opcijām Pievienot preci grozam vietnes veidotājā](./media/AW_sitesettings.PNG)

> [!IMPORTANT]
> - Vietas iestatījums **Pievienot produktu grozam** ir pieejams kā Dynamics 365 Commerce versija 10.0.11 laidienā. Ja veicat atjaunināšanu no vecākas Dynamics 365 Commerce versijas, ir manuāli jāatjaunina fails appsettings.json. Lai iegūtu informāciju par faila appsettings.json atjaunināšanu skatiet [SDK un moduļu bibliotēkas atjauninājumi](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).
> - Iestatīšanas opcija **Rādīt mini grozu** ir pieejama Dynamics 365 Commerce versijas 10.0.20 izlaidē. Ja veicat atjaunināšanu no vecākas Dynamics 365 Commerce versijas, ir manuāli jāatjaunina fails appsettings.json. Lai iegūtu informāciju par faila appsettings.json atjaunināšanu skatiet [SDK un moduļu bibliotēkas atjauninājumi](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

Attēlā zemāk redzams "pievienots grozam" apstiprinājuma paziņojuma piemērs Fabrikam vietnē.

!["Pievienots grozam" apstiprinājuma paziņojuma piemērs Fabrikam vietnē](./media/ecommerce-addtocart-notifications.PNG)

Attēlā zemāk redzams "pievienots grozam" apstiprinājuma paziņojuma piemērs Adventure Works vietnē.

!["Pievienots grozam" apstiprinājuma paziņojuma piemērs Adventure Works vietnē](./media/AW_minicart.PNG)

## <a name="additional-resources"></a>Papildu resursi

[Moduļu bibliotēkas pārskats](starter-kit-overview.md)

[Pirkšanas lodziņa modulis](add-buy-box.md)

[Veikalu atlasītāja modulis](store-selector.md)
