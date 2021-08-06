---
title: Groza ikonas modulis
description: Šajā tēmā aplūkots groza ikonas modulis un aprakstīta tā pievienošana vietnes lapām risinājumā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d9e3850d98e716d1bbea2017f6e8c9d75f19adc9
ms.sourcegitcommit: e42c7dd495829b0853cebdf827b86a7cf655cf86
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/17/2021
ms.locfileid: "6638005"
---
# <a name="cart-icon-module"></a>Groza ikonas modulis

[!include [banner](includes/banner.md)]

Šajā tēmā aplūkots groza ikonas modulis un aprakstīta tā pievienošana vietnes lapām risinājumā Microsoft Dynamics 365 Commerce.

Groza ikonu modulis attēlo groza lapas galvenes modulī un parāda preču skaitu grozā. Groza ikonas modulis parāda arī groza kopsavilkumu (to sauc arī par mini grozu), kad atrodaties virs groza ikonas. Mini grozs sniedz lietotājam kopsavilkumu par krājumiem grozā bez nepieciešamības pāriet uz groza lapu. Turklāt tas arī ļauj lietotājam doties tieši uz izrakstīšanās lapu, ja tie ir apmierināti ar kopsavilkumu. Tas samazina lapu navigācijas skaitu un padara pasūtījumu ātrāku. 

Attēlā zemāk redzams groza ikonas moduļa piemērs,, kurā ir parādīts mini grozs Fabrikam galvenē.

![Groza ikonas moduļa piemērs.](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a>Moduļa rekvizīti

- **Rādīt mini grozu** — ja tas ir patiess, šis rekvizīts iespējo groza kopsavilkumu (mini grozs), kas tiks parādīts, kad atrodaties virs groza ikonas. Šī funkcionalitāte tiek atbalstīta tikai darbvirsmas skatu portiem.

## <a name="module-properties-in-the-adventure-works-theme"></a>Moduļa rekvizīti Adventure Works tēmā

Adventure Works tēmā groza ikonas modulis ietver divus papildu slotus mini grozam. Šie sloti ir ietverti kā moduļa definīcijas paplašinājums.

- **Tukšas groza veicināšanas pasākumi** — šis slots izmanto satura bloķēšanas moduli. Ja grozs ir tukšs, tiek rādīts norādītais satura bloķēšanas modulis. Satura bloķēšanas moduli var lietot veicināšanas pasākumiem, mārketinga saturam un saitēm uz kategoriju lapām, lai palīdzētu klientiem turpināt iepirkties.
- **Veicināšanas saturs** — šo slotu var izmantot, lai parādītu lielos veicināšanas pasākumus, piemēram, "Bezmaksas nosūtīšana pasūtījumiem virs $100." Satura bloķēšana, teksta bloķēšana un attēlu saraksta moduļi var tikt izmantoti reklāmas satura slotā.

Šajā attēlā parādīts groza ikonas moduļa piemērs Adventure Works tēmā, kas mini grozā parāda reklāmas saturu.

![Groza ikonas moduļa piemērs Adventure Works tēmā](./media/AW_minicart.PNG)

> [!IMPORTANT]
> Adventure Works tēmas sloti ir pieejami Dynamics 365 Commerce versijas 10.0.20 laidienā.

## <a name="add-a-cart-icon-module-to-a-page"></a>Groza ikonas moduļa pievienošana lapā

Lai pievienotu groza ikonas moduli, skatiet [Galvenes modulis](author-header-module.md).

## <a name="additional-resources"></a>Papildu resursi

[Groza modulis](add-cart-module.md)

[Norēķināšanās modulis](add-checkout-module.md)

[Maksājumu modulis](payment-module.md)

[Piegādes adreses modulis](ship-address-module.md)

[Piegādes opciju modulis](delivery-options-module.md)

[Saņemšanas informācijas modulis](pickup-info-module.md)

[Pasūtījumu informācijas modulis](order-confirmation-module.md)

[Dāvanu kartes modulis](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
