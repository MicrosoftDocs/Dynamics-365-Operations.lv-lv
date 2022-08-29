---
title: Sinhronizēt nodokļu iestatījumus no nodokļu aprēķināšanas pakalpojuma uz Dynamics 365 finansēm
description: Šajā rakstā ir izskaidrots, kā sinhronizēt nodokļu iestatījumu pamatdatus no nodokļu aprēķināšanas pakalpojuma līdz Microsoft Dynamics 365 Finanses.
author: EricWangChen
ms.date: 01/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.21
ms.custom: intro-internal
ms.search.form: TaxIntegration, TaxServiceParameters
ms.openlocfilehash: 315f2b27a64906ca0fc404d704d0b170dbfa48c5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283859"
---
# <a name="sync-the-tax-setup-from-the-tax-calculation-service-to-dynamics-365-finance"></a>Sinhronizēt nodokļu iestatījumus no nodokļu aprēķināšanas pakalpojuma uz Dynamics 365 finansēm

[!include [banner](../includes/banner.md)]

Šajā rakstā ir izskaidrots, kā sinhronizēt nodokļu iestatījumu pamatdatus no nodokļu aprēķināšanas pakalpojuma līdz Microsoft Dynamics 365 Finanses.

Kad esat izpildījis [nepieciešamās](global-get-started-with-tax-calculation-service.md) iestatīšanas darbības sadaļā Sākt ar nodokļu aprēķinu, šie nodokļu iestatījumu dati automātiski tiek sinhronizēti no nodokļu aprēķina pakalpojuma uz Finanses.

## <a name="sales-tax-code"></a>PVN kods

| Nodokļu aprēķināšanas pakalpojums           | Finance                             |
| --------------------------------- | ----------------------------------- |
| Nodokļa kods                          | PVN kods                      |
| Apraksts                       | Vārds/nosaukums                                |
| Lietotāja ievadne                        | Nosegšanas periods                   |
| Lietotāja ievadne                        | Virsgrāmatas grāmatošanas grupa                |
| Lietotāja ievadne                        | PVN valūta                  |
| Ir konfigurēta negatīva nodokļu likme | Atļaut negatīvu PVN likmi |

## <a name="tax-value"></a>Nodokļa vērtība

| Nodokļu aprēķināšanas pakalpojums | Finance                   |
| ----------------------- | ------------------------- |
| No darbības datuma   | No datuma                 |
| Līdz darbības datumam     | Līdz datumam                   |
| Minimālā summa          | Minimālā robeža             |
| Maksimālais apjoms          | Maksimālā robeža             |
| Nodokļa likme                | Vērtība                     |
| Neatskaitāma likme     | Neatskaitāmā procentuālā vērtība |

## <a name="tax-limits"></a>Nodokļu ierobežojumi

| Nodokļu aprēķināšanas pakalpojums | Finance           |
| ----------------------- | ----------------- |
| No darbības datuma   | No datuma         |
| Līdz darbības datumam     | Līdz datumam           |
| Minimālā nodokļa summa      | Minimālais PVN |
| Maksimālā nodokļa summa      | Maksimālā PVN summa |

## <a name="sales-tax-group"></a>PVN grupa

| Nodokļu aprēķināšanas pakalpojums                         | Finance                                    |
| ----------------------------------------------- | ------------------------------------------ |
| Nodokļu grupa                                       | PVN grupa                            |
| Nodokļu kodi šajā nodokļu grupā                  | PVN kodi šajā PVN grupā |
| Nodokļa kods ir atzīmēts kā **neapliekams**         | Neapliekams                                     |
| Nodokļa kods ir atzīmēts kā **neapliekams**         | Reģistrācijas kods                                |
| Nodokļa kods ir atzīmēts kā **Atgriezes maksa** | Apgrieztais                             |
| Nodokļa kods ir atzīmēts kā **"Izmantošanas nodoklis"**        | Importa nodoklis                                    |

## <a name="item-sales-tax-group"></a>Krājumu PVN grupa

| Nodokļu aprēķināšanas pakalpojums             | Finance                                         |
| ----------------------------------- | ----------------------------------------------- |
| Krājumu nodokļu grupa                      | Krājumu PVN grupa                            |
| Nodokļu kodi šajā krājumu nodokļu grupā | PVN kodi šajā krājumu PVN grupā |

Pēc sinhronizācijas pabeigšanas turpiniet uzturēt atlikušos parametrus Finansēs grāmatošanas un pārskatu sniegšanas nolūkos.

> [!NOTE]
> Nodokļu iestatījumu sinhronizācija no finanšu uz nodokļu aprēķina pakalpojumu netiek atbalstīta. Esošai finanšu videi vispirms izveidojiet nodokļu iestatījumus nodokļu aprēķināšanas pakalpojumā. Pēc tam sinhronizējiet iestatīšanas datus atpakaļ Finanšu vidē.
