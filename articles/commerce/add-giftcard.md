---
title: Dāvanu kartes modulis
description: Šajā tēmā aplūkoti Dāvanu kartes moduļi un aprakstīta to pievienošana vietnes lapām risinājumā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c024cc1b16ca60b2277eba2d7045020c2e67c3a0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206299"
---
# <a name="gift-card-module"></a>Dāvanu kartes modulis

[!include [banner](includes/banner.md)]

Šajā tēmā aplūkoti Dāvanu kartes moduļi un aprakstīta to pievienošana vietnes lapām risinājumā Microsoft Dynamics 365 Commerce.

Dāvanu kartes modulis var tikt izmantots norēķinu moduļos, lai pieņemtu dāvanu kartes, kas ir parastā maksājuma forma, ko izmanto e-komercijas darījumiem. Dāvanu kartes modulis atbalsta Dynamics 365, SVS un Givex dāvanu kartes. SVS un Givex dāvanu kartes tiek izpirktas, izmantojot Adyen maksājumu nodrošinātāju. Plašāku informāciju par atbalstu ārējām dāvanu kartēm, piemēram, SVS un Givex, skatiet [Atbalsts ārējām dāvanu kartēm](./dev-itpro/gift-card.md).

> [!NOTE]
> SVS un Givex dāvanu karšu izrakstīšanas atbalsts norēķinu plūsmas laikā ir pieejams Dynamics 365 Commerce 10.0.11 laidienā. 

Ir pieejami divi dāvanu kartes moduļi:

- **Dāvanu karte** - Šo moduli var izmantot izrakstīšanās lapā, lai izpirktu dāvanu karti kā norēķinu. 
- **Dāvanu kartes bilances pārbaude** - Šo moduli var izmantot jebkurā lapā, lai pārbaudītu dāvanu kartes bilanci. Šis modulis ir pieejams Komercijas izlaidumā 10.0.14 un jaunākās versijās.

> [!NOTE]
> Dāvanu kartes bilances pārbaudes modulis ir pieejams Dynamics 365 Commerce 10.0.14 laidienā.

Attēlā zemāk redzams cilnes dāvanu kartes moduļa piemērs norēķināšanās lapā.

![Dāvanu kartes moduļa piemērs](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a>Moduļa rekvizīti

- **Rādīt papildu laukus** - šis rekvizīts nosaka, kuri lauki ir jārāda dāvanu kartēm papildus dāvanu kartes numuram, kas vienmēr tiek parādīts pēc noklusējuma. Piemēram, dažas dāvanu kartes atbalsta personas identifikācijas numura (PIN) rādīšanu, bet citas atbalsta PIN un beigu datuma parādīšanu. Pretējā gadījumā šis rekvizīts var tikt iestatīts uz "Nav", kas parādītu tikai dāvanu kartes numuru un papildu laukus.

Atbalstītās vērtības:
-   PIN
-   Beigu datums
-   PIN un beigu datums 
-   None

## <a name="site-settings-for-gift-card-modules"></a>Vietas iestatījumi dāvanu karšu moduļiem

Commerce vietnes veidotājā sadaļā **Vietnes iestatījumi \> Paplašinājumi** ir dāvanu kartes moduļa iestatījums ar nosaukumu **Atbalstīto dāvanu karšu veids**. Šis iestatījums atbalsta trīs vērtības:
- **Dynamics 365 dāvanu karte** — kad tiek lietots šis iestatījums, dāvanu kartes modulis atļauj tikai Dynamics 365 dāvanu karšu izpirkšanu. Šis iestatījums tiek atbalstīts tikai pierakstītiem lietotājiem e-Commerce vietnē.
- **SVS un GIVEX dāvanu kartes** — kad tiek lietots šis iestatījums, dāvanu kartes modulis atļauj tikai GIVEX un SVS dāvanu karšu izpirkšanu. Šis iestatījums tiek atbalstīts pierakstītiem un anonīmiem lietotājiem e-Commerce vietnē.
- **Dynamics 365, SVS un GIVEX dāvanu kartes** — kad tiek lietots šis iestatījums, dāvanu kartes modulis atļauj Dynamics 365, GIVEX un SVS dāvanu karšu izpirkšanu. Šis iestatījums tiek atbalstīts tikai pierakstītiem lietotājiem e-Commerce vietnē.

> [!IMPORTANT]
> Šie iestatījumi ir pieejami Dynamics 365 Commerce 10.0.11 versijā, un tie ir nepieciešami tikai tad, ja ir nepieciešams atbalsts SVS vai Givex dāvanu kartēm. Ja veicat atjaunināšanu no vecākas Dynamics 365 Commerce versijas, ir manuāli jāatjaunina fails appsettings.json. Norādījumus par faila appsettings.json atjaunināšanu skatiet [SDK un moduļu bibliotēkas atjauninājumi](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file). 

## <a name="add-a-gift-card-module-to-a-page"></a>Dāvanu kartes moduļa pievienošana lapā

Instrukcijas par to, kā pievienot dāvanu kartes moduli izrakstīšanās lapai un iestatīt pieprasītos rekvizītus, skatiet sadaļu [Izrakstīšanās modulis](add-checkout-module.md).

## <a name="additional-resources"></a>Papildu resursi

[Groza modulis](add-cart-module.md)

[Groza ikonas modulis](cart-icon-module.md)

[Norēķināšanās modulis](add-checkout-module.md)

[Maksājumu modulis](payment-module.md)

[Piegādes adreses modulis](ship-address-module.md)

[Piegādes opciju modulis](delivery-options-module.md)

[Saņemšanas informācijas modulis](pickup-info-module.md)

[Pasūtījumu informācijas modulis](order-confirmation-module.md)

[Atbalsts ārējām dāvanu kartēm](./dev-itpro/gift-card.md)

[SDK un moduļu bibliotēkas atjauninājumi](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]