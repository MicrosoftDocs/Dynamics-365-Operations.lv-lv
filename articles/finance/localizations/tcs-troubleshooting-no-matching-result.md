---
title: Nav atrasts neviens atbilstošs rezultāts
description: Šajā tēmā skaidrots, kā novērst problēmu, kas rodas "Nav atrodams neviens atbilstošs rezultāts" kļūda nodokļu aprēķina serivē.
author: hangwan
ms.date: 03/25/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 03/23/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: c1a343b0b74645d40b0a2582749968cc0a56afd7
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/27/2022
ms.locfileid: "8648154"
---
# <a name="no-matching-result-could-be-found"></a>Nav atrasts neviens atbilstošs rezultāts

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidroti problēmu novēršanas soļi, ko varat veikt, ja nodokļu aprēķināšanas pakalpojumā saņemat kļūdu "Nav atrasts atbilstošs rezultāts".

## <a name="symptom"></a>Simptoms

Tiek saņemts šāds kļūdas ziņojums: "Virsraksts/rindas - 1, nodokļu grupa, neviens atbilstošs rezultāts nav atrasts."

```json
======================Tax service calculation result JSON:===========================
{
    "taxDocument": {
        "Header": [
            {
                "Lines": [
                    {
                        ...
                        "Errors": [
                            {
                                "Code": "TaxSetup20000",
                                "Message": "Header/Lines - 1, Tax group applicability, no matching result could be found."
                            }
                        ],
                        "Adjustment": null
                    }
                ],
                "Measures": {
                    ...
                },
                ...
            }
        ]
    },
    ...
}
```

## <a name="cause"></a>Iemesls

Problēma rodas, ja līdzekli iestatījums regulēšanas konfigurācijas pakalpojumā (RCS) ir nepareizs.

## <a name="troubleshoot"></a>Novērst problēmu

1. Lejupielādējiet traucējummeklēšanas failu. Papildinformāciju skatiet atkļūdošanas [režīma iespējošana problēmu novēršanai](tcs-troubleshooting-enable-debug-mode.md).
2. Salīdziniet nodokļu pakalpojuma aprēķina ievadi ar līdzekļa iestatījumiem, lai novērstu iestatījumu problēmu.

    Šajā piemērā parādīta ievade nodokļu pakalpojuma aprēķinā.

    ```json
    ===============================Tax service calculation input JSON:=====================================
    {
        "TaxableDocument": {
            "Header": [
                {
                    "Lines": [
                        {
                            ...
                        }
                    ],
                    "Business Process": "Sales",
                    "Ship From Zip Code": "30159",
                }
            ]
        },
        "Parameter": {
            ...
        },
        "Adjustment": {
            "Lines": {}
        }
    }
    ```

    Šajā tabulā ir minētas nodokļu grupas piemērojamība RCS.

    | Virsraksts. Biznesa process | Rindas. Biznesa vienība | Virsraksts. Nosūtīt no pasta indeksa | Nodokļu grupa |
    |-------------------------|---------------------|---------------------------|-----------|
    | Žurnāls                 |                     |                           | Grupa A   |
    | Pārdošana                   |                     | 30160                     | B grupa   |

    Atbilstoši nodokļu pakalpojuma **aprēķina** **ievadei** biznesa procesa vērtība virsrakstā ir Pārdošana, **un** vērtība Nosūtīt no pasta indeksa virsrakstā ir **30159**. Šī ievade ir balstīta uz piemērojamības noteikumu iestatījumiem RCS. Tā kā nav atbilstoša rindas, rodas kļūda.

    > [!NOTE]
    > Ja piemērojamības noteikuma vērtība ir tukša, kārtula ir piemērojama jebkurai vērtībai.

## <a name="mitigation"></a>Mazinājums

Sekojiet šiem soļiem, lai mazinātu kļūdu.

1. RCS, dodieties uz **Globalizācijas līdzeklis** \> **Nodokļa aprēķins**.
2. Izveidojiet jaunu funkcijas versiju.
3. Pievienojiet rindu atbilstošai informācijai.

    | Virsraksts. Biznesa process | Rindas. Biznesa vienība | Virsraksts. Nosūtīt no pasta indeksa| Nodokļu grupa |
    |-------------------------|---------------------|--------------------------|-----------|
    | Žurnāls                 |                     |                          | Grupa A   |
    | Pārdošana                   |                     | 30160                    | B grupa   |
    | Pārdošana                   |                     | 30159                    | B grupa   |

4. Publicējiet līdzekļa iestatīšanas versiju.
5. Microsoft Dynamics 365 Finansēs dodieties uz **nodokļu** \> **iestatījumu nodokļa** \> **konfigurācijas** \> **nodokļa aprēķina** parametrus un atlasiet jauno versiju.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
