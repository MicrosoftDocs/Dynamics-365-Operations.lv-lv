---
title: Pasūtījuma kopsavilkuma apakšsummā nav iekļauti maksu nodokļi, izmantojot pielāgotos pasūtījuma kopsavilkuma moduļus
description: Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt izmantot pielāgotos pasūtījumu kopsavilkuma moduļus un pasūtījuma kopsavilkuma apakšsummā nav ietverti maksu nodokļi scenārijā "cena ietver PVN".
author: gvrmohanreddy
ms.date: 05/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-04-22
ms.openlocfilehash: 1a47561a3ac984bc554b5b93546592237c16cf18
ms.sourcegitcommit: 48d094d083c1bd45c3d72f8b666926b48ec7ae35
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2022
ms.locfileid: "8767928"
---
# <a name="order-summary-subtotal-doesnt-include-taxes-on-charges-when-using-customized-order-summary-modules"></a>Pasūtījuma kopsavilkuma apakšsummā nav iekļauti maksu nodokļi, izmantojot pielāgotos pasūtījuma kopsavilkuma moduļus

Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt izmantot pielāgotos pasūtījumu kopsavilkuma moduļus un pasūtījuma kopsavilkuma apakšsummā nav ietverti maksu nodokļi scenārijā "cena ietver PVN".

## <a name="description"></a>Apraksts

Attiecībā uz Microsoft Dynamics 365 Commerce 10.0.27 versijas laidienu, scenārijā "cena ietver PVN", ir veiktas šādas izmaiņas, lai nodrošinātu konsekventu pieredzi pasūtījumu kopsavilkuma moduļos e-komercijas vietnes lapās.

- Ir pievienoti divi jauni lauki: **TaxOnShippingCharge un** **TaxOnNonShippingCharges**.
- Programmas **GetSalesOrderBySalesId** **un GetSalesOrderByTransactionId** (API) ir precīzas vērtības tālāk minētajiem laukiem scenārijā "cena ietver PVN":

    - ApakšsummaPārdošanasAmount
    - SubtotalAmountWithoutTax
    - Apakšsumma
    - Para& ShippingChargeAmount
    - Cita chargeAmount

Tomēr, ja izmantojat pielāgotus pasūtījumu kopsavilkuma moduļus, šīs izmaiņas var ietekmēt pasūtījumu kopsavilkuma apakšsummas vērtības, neskaitot maksu nodokļus.

## <a name="resolution"></a>Novēršana

Ja izmantojat pielāgotus pasūtījumu kopsavilkuma moduļus un nevēlaties pārmantot izmaiņas, kas ir veiktas scenārijā "cena ietver PVN" versijā 10.0.27 vai jaunākā versijā, izpildiet šīs sadaļas norādījumus.

Atgriežaties uz iepriekšējo (pirms versijas 10.0.27) **salesTransaction.SubtotalAmount** **un salesTransaction.SubtotalAmountWithoutTax** lauku, tiek atjaunota kopsummas maksas nodokļu summas (**TaxOnShippingCharge** **un TaxOnNonShippingCharges**) iekļaušanas apakšsummās (**SubtotalAmount** **un SubtotalAmountWithoutTax).**

Lai atgrieztu iepriekšējā pasūtījuma kopsavilkuma darbību, sekojiet šiem soļiem.

1. Programmā Commerce headquarters atveriet lapu Commerce parameters (**Retail un Commerce \> Headquarters iestatīšanas parametri \>\> Commerce parametri**).
1. Kreisajā navigācijas rūtī atlasiet Konfigurācijas **parametrus**.
1. Pievienojiet šādus konfigurācijas parametrus un iestatiet katra parametra vērtību kā **patiesu**:

    - IsLegacyTaxOnChargeInSubtotalAmountIncludedInTaxIncusiveEnabled
    - IsLegacyOrderSummaryMidationEnabled

> [!NOTE]
> Ja iepriekš izmantots **IsUpdatedPriceIncludesTaxSubtotalCalculationEnabled** konfigurācijas parametrs un vēlaties saglabāt to pašu uzvedību šim pasūtījumam **. Rekvizīts NetAmountWithoutTax ir jāpievieno arī konfigurācijas parametrs IsLegacyPriceIncludesTaxNetAmountWithoutTaxCalculationEnabled** **un iestatiet tā vērtību kā patiesu**.**·**

## <a name="additional-resources"></a>Papildu resursi

[Nodokļu pārtraukuma informācijas slēpšana pasūtījumu kopsavilkumos](../hide-taxes-breakup.md)
