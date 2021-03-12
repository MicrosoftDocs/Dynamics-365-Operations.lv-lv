---
title: Piegādes adreses modulis
description: Šajā tēmā ir apskatīti piegādes adrešu modulis un tiek paskaidrots, kā to konfigurēt programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 6a5eb69c7746be419779b1a844ee35ec375a324c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985640"
---
# <a name="shipping-address-module"></a>Piegādes adreses modulis

[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīts piegādes adrešu modulis un tiek paskaidrots, kā to konfigurēt programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Piegādes adreses modulis ļauj klientiem pievienot vai atlasīt pasūtījuma piegādes adresi norēķināšanās plūsmas laikā. Ja klients ir pierakstījies, tiek rādītas visas adreses, kas iepriekš tika saglabātas šim klientam, un klients var atlasīt kādu no tām. Klients var arī pievienot jaunu adresi. Piegādes adreses modulis tiek izmantots visām precēm pasūtījumā, kuras nepieciešams piegādāt.

Piegādes adreses formātus var definēt Commerce Headquarters katrai valstij vai reģionam, un piegādes adreses modulis tad ievieš valsts/reģiona specifiskos nosacījumus.

Kad debitori ievada piegādes adresi izrakstīšanās plūsmā, tiem ir opcija saglabāt adresi kā primāro adresi. Šī opcija tiek rādīta tikai tad, ja debitors ir pieteicies.

Kaut arī piegādes adreses modulis nenodrošina adrešu validāciju, šī funkcionalitāte var tikt īstenota ar pielāgošanu.

Ilustrācijā zemāk redzams jauns piegādes adreses moduļa piemērs norēķināšanās lapā.

![Piegādes adreses moduļa piemērs norēķināšanās lapā](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a>Moduļa rekvizīti

| Rekvizīta nosaukums | Vērtības | apraksts |
|---------------|--------|-------------|
| Virsraksts | Virsraksta teksts un virsraksta etiķete (**H1**, **H2**, **H3**, **H4**, **H5** vai **H6**) | Izvēles virsraksts piegādes adreses modulim. |
| Rādīt adreses veidu | **Patiess** vai **Nepatiess** | Ja šis neobligātais rekvizīts ir iestatīts kā **Patiess**, tiks parādīts adreses tips, piemēram, **Sākums** vai **Uzņēmums**. Ja nav norādīts adreses tips, adrese automātiski tiks saglabāta kā **Tips**=**Cits**. |

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
