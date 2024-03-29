---
title: Opcija Saņemt šo neparādās groza vai preces informācijas lapās
description: Šajā dokumentā ir sniegti norādījumi par problēmu novēršanas iespējām, kas var palīdzēt, ja veikala izdošanas opcija netiek parādīta groza lapās vai preču informācijas lapās.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 85d102d3442e19377912cb9562010778a0575db8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284608"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a>Opcija "Saņemt šo" neparādās groza vai preces informācijas lapās

[!include [banner](../../includes/banner.md)]

Šajā dokumentā ir sniegti norādījumi par problēmu novēršanas iespējām, kas var palīdzēt, ja veikala izdošanas opcija netiek parādīta groza lapās vai preču informācijas lapās.

## <a name="description"></a>Apraksts

Poga **Saņemt šo** netiek parādīta groza vai preces informācijas lapās.

Attēlā zemāk parādīts lapas piemērs, kurā iekļauta poga **Saņemt šo**.

![Poga Saņemt šo.](media/pickup-button-missing.jpg)

## <a name="resolution"></a>Novēršana

### <a name="enable-the-bopis-extension-in-commerce-site-builder"></a>Iespējot BTOPS paplašinājumu Commerce vietnes veidotājā

Lai iespējotu "pirkt tiešsaistē, saņemt veikalā" (BOPIS) paplašinājumu Commerce vietnes veidotājā, veiciet tālāk minētās darbības.

1. Atlasiet savu vietni.
1. Atlasiet **Vietnes iestatījumi** un pēc tam atlasiet **Paplašinājumi**.
1. Pārliecinieties, vai opcija **Atspējot BOPIS** ir notīrīta.

### <a name="configure-modes-of-delivery-in-commerce-headquarters"></a>Piegādes veidu konfigurēšana programmā Commerce Headquarters

Lai konfigurētu piegādes veidus Commerce Headquarters, veiciet tālāk norādītās darbības.

1. Pārejiet uz sadaļu **Sagāde un avoti \> Iestatīšana \> Piegādes veidi**.
1. Pārliecinieties, ka ir izveidots piegādes veids **Izsniegšana klientam** un vai tam ir piešķirtas preces un adreses.
1. Pārejiet uz sadaļu **Mazumtirdzniecība un komercija \> Headquarters iestatīšana \> Parametri**.
1. Kreisās puses navigācijā atlasiet **Klienta pasūtījumi**.
1. Pārliecinieties, vai **Piegādes savākšanas veids** ir konfigurēts pareizi.

### <a name="configure-customer-orders-payments"></a>Klienta pasūtījumu maksājumu konfigurēšana

Lai konfigurētu klienta pasūtījumu maksājumus Commerce Headquarters, veiciet tālāk norādītās darbības.

1. Pārejiet uz sadaļu **Mazumtirdzniecība un komercija \> Headquarters iestatīšana \> Parametri**.
1. Kreisās puses navigācijā atlasiet **Klienta pasūtījumi**.
1. Kopsavilkuma cilnē **Maksājumi** pārliecinieties, vai lauki **Apmaksas nosacījumi** un **Maksāšanas metode** ir iestatīti pareizi.

## <a name="additional-resources"></a>Papildu resursi

[Konfigurēt BOPIS](../cpe-bopis.md)

[Iespējot vairākus pasūtījuma piegādes veidus klientu pasūtījumiem](../multiple-pickup-modes.md)

[Universālā kanāla Commerce pasūtījumu maksājumi](../dev-itpro/commerce-payments.md)

[Veikalu atlasītāja modulis](../store-selector.md)
