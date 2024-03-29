---
title: Piegādes adreses modulis
description: Šajā rakstā ir apskatīts piegādes adreses modulis un skaidrots, kā to konfigurēt Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 48e6909b4dac9722830a83ec3a63a58876768d7e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275010"
---
# <a name="shipping-address-module"></a>Piegādes adreses modulis

[!include [banner](includes/banner.md)]

Šajā rakstā ir apskatīts piegādes adreses modulis un skaidrots, kā to konfigurēt Microsoft Dynamics 365 Commerce.

Piegādes adreses modulis ļauj klientiem pievienot vai atlasīt pasūtījuma piegādes adresi norēķināšanās plūsmas laikā. Ja klients ir pierakstījies, tiek rādītas visas adreses, kas iepriekš tika saglabātas šim klientam, un klients var atlasīt kādu no tām. Klients var arī pievienot jaunu adresi. Piegādes adreses modulis tiek izmantots visām precēm pasūtījumā, kuras nepieciešams piegādāt.

Piegādes adreses formātus var definēt Commerce Headquarters katrai valstij vai reģionam, un piegādes adreses modulis tad ievieš valsts/reģiona specifiskos nosacījumus.

Kad debitori ievada piegādes adresi izrakstīšanās plūsmā, tiem ir opcija saglabāt adresi kā primāro adresi. Šī opcija tiek rādīta tikai tad, ja debitors ir pieteicies.

Kaut arī piegādes adreses modulis nenodrošina adrešu validāciju, šī funkcionalitāte var tikt īstenota ar pielāgošanu.

Ilustrācijā zemāk redzams jauns piegādes adreses moduļa piemērs norēķināšanās lapā.

![Piegādes adreses moduļa piemērs norēķināšanās lapā.](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a>Moduļa rekvizīti

| Rekvizīta nosaukums | Vērtības | Apraksts |
|---------------|--------|-------------|
| Virsraksts | Virsraksta teksts un virsraksta etiķete (**H1**, **H2**, **H3**, **H4**, **H5** vai **H6**) | Izvēles virsraksts piegādes adreses modulim. |
| Rādīt adreses veidu | **Patiess** vai **Nepatiess** | Ja šis neobligātais rekvizīts ir iestatīts kā **Patiess**, tiks parādīts adreses tips, piemēram, **Sākums** vai **Uzņēmums**. Ja nav norādīts adreses tips, adrese automātiski tiks saglabāta kā **Tips**=**Cits**. |
| Iespējot automātisko ieteikumu| **Patiess** vai **Nepatiess** | Ja šis neobligātais rekvizīts ir iestatīts uz **Patiess**, tiek sniegti automātiski adrešu ieteikumi. Šos ieteikumus nodrošina Bing kartes. Informāciju par to, kā iestatīt Bing karšu integrāciju jūsu vietnē, skatiet sadaļu [Veikalu atlasītāja modulis](store-selector.md). Šis līdzeklis ir pieejams kā Commerce versijas 10.0.15 laidiens.|
|Automātiskās ieteikšanas opcijas| Skaits| Ja iespējoti automātiskie adrešu ieteikumi, varat norādīt papildu opcijas, piemēram, maksimālo nodrošināmo ieteikumu skaitu.|

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a>Piegādes adreses moduļa pievienošana norēķināšanās lapā un nepieciešamo rekvizītu iestatīšana

Piegādes adreses moduli var pievienot tikai norēķināšanās modulim. Lai iegūtu papildu informāciju par to, kā konfigurēt piegādes adreses moduli un pievienot to norēķinu lapai, skatiet sadaļu [Norēķināšanās modulis](add-checkout-module.md).

## <a name="additional-resources"></a>Papildu resursi

[Groza modulis](add-cart-module.md)

[Groza ikonas modulis](cart-icon-module.md)

[Norēķināšanās modulis](add-checkout-module.md)

[Maksājumu modulis](payment-module.md)

[Piegādes opciju modulis](delivery-options-module.md)

[Saņemšanas informācijas modulis](pickup-info-module.md)

[Pasūtījumu informācijas modulis](order-confirmation-module.md)

[Dāvanu kartes modulis](add-giftcard.md)

[Veikalu atlasītāja modulis](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
