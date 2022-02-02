---
title: Sinhronizēt nodokļu iestatījumus no nodokļu aprēķina pakalpojuma uz Dynamics 365 Finance
description: Šajā tēmā skaidrots, kā sinhronizēt nodokļu iestatījumu pamatdatus no nodokļu aprēķina pakalpojuma uz Microsoft Dynamics 365 Finance.
author: wangchen
ms.date: 01/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegration, TaxServiceParameters
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: d5d994934014a146f825431cb53dfbef8fe20bc8
ms.sourcegitcommit: 27475081f3d2d96cf655b6afdc97be9fb719c04d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/12/2022
ms.locfileid: "7965109"
---
# <a name="sync-the-tax-setup-from-the-tax-calculation-service-to-dynamics-365-finance"></a>Sinhronizēt nodokļu iestatījumus no nodokļu aprēķina pakalpojuma uz Dynamics 365 Finance

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidrots, kā sinhronizēt nodokļu iestatījumu pamatdatus no nodokļu aprēķina pakalpojuma uz Microsoft Dynamics 365 Finance.

Kad esat izpildījis nepieciešamās iestatīšanas darbības sadaļā Sākt ar nodokļu aprēķinu, šie nodokļu iestatījumu dati automātiski tiek sinhronizēti no [nodokļu aprēķina pakalpojuma uz](global-get-started-with-tax-calculation-service.md) Finanses.

## <a name="sales-tax-code"></a>PVN kods

| Nodokļu aprēķināšanas pakalpojums           | Finance                             |
| --------------------------------- | ----------------------------------- |
| Nodokļa kods                          | PVN kods                      |
| Apraksts                       | Nosaukums                                |
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
