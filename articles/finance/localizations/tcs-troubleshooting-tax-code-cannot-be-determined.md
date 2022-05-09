---
title: Nevar noteikt nodokļa kodu.
description: Šajā tēmā skaidrots, kā novērst nodokļu aprēķina pakalpojuma kļūdu "Nodokļu kodu nevar noteikt".
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
ms.openlocfilehash: 3c0914f0013ad2de61cd5a59e3092fef149742e4
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/27/2022
ms.locfileid: "8648151"
---
# <a name="tax-code-cannot-be-determined"></a>Nevar noteikt nodokļa kodu.

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidroti problēmu novēršanas soļi, ko varat veikt, ja nodokļu aprēķināšanas pakalpojumā saņemat kļūdu "Nodokļu kodu nevar noteikt".

## <a name="symptom"></a>Simptoms

Tiek saņemts šāds kļūdas ziņojums: "Virsraksts/rindas - 1, nodokļu kodu nevar noteikt." Pēc izvēles problēmu novēršanas failā varat atrast kļūdu, kā parādīts šajā piemērā. Papildinformāciju skatiet atkļūdošanas [režīma iespējošana problēmu novēršanai](tcs-troubleshooting-enable-debug-mode.md).

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
                                "Code": "TaxSetup20001",
                                "Message": "Header/Lines - 1, tax code cannot be determined."
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

Problēma, iespējams, rodas, jo nodokļu grupa un krājumu nodokļu grupa nekomaktivē.

## <a name="troubleshoot"></a>Novērst problēmu

Izpildiet šīs darbības, lai novērstu problēmu.

1. Traucējummeklēšanas failā pārbaudiet, vai ir noteikta nodokļu grupa un krājumu PVN grupa. Ja nodokļu grupas **un krājumu** nodokļu **grupas vērtības ir** tukšas, nav noteiktas nodokļu grupas un krājumu nodokļu grupas. Ja tie ir noteikti, rezultāti, iespējams, būs nepareizi.

    Šeit parādīts problēmu novēršanas faila piemērs.

    ```json
    ======================Tax service calculation result JSON:===========================
    {
        "taxDocument": {
            "Header": [
                {
                    "Lines": [
                        {
                            "Tax Codes": {},
                            "Measures": {
                                "Tax Group": "Group A",
                                "Item Tax Group": "Group B"
                            },
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

2. Pārbaudiet, vai **pārdošanas pasūtījuma** rindas informācijas **cilnē** Iestatījumi ir aktivizēta opcija Ignorēt PVN.

    - Ja aktivizēts, nodokļu kodus nosaka nodokļu **grupa** **un krājumu nodokļu** grupas vērtības, ko ievadāt darbības rindā. Pārbaudiet, vai šīs vērtības ir ievadītas pareizi.
    - Ja šī opcija nav iespējota, pārbaudiet, vai nodokļu grupas **piemērojamības** **un krājumu nodokļu grupas piemērojamības laukiem ir iestatītas pareizas** vērtības. Papildinformāciju skatiet šeit: [Nav atrasts neviens atbilstošs](tcs-troubleshooting-no-matching-result.md) rezultāts.

3. Ja nodokļu grupa un krājumu nodokļu grupa ir pareizi noteikta, nosakiet, vai tiem ir kāds krustpunkts.

    1. RCS atveriet nodokļu līdzekļus **nodokļu** \> **kodus un grupas** \> **nodokļu grupu.**

        | Rinda. Nodokļu grupa | Nodokļu kodi |
        |----------------|-----------|
        | Grupa A        | A         |

    2. Dodieties uz **nodokļu** \> **funkcijām nodokļu kodiem un grupām** \> **Krājuma NODOKĻU grupa.**

        | Rinda. Krājumu PVN grupa | Nodokļu kodi |
        |---------------------|-----------|
        | B grupa             | mljrd.         |

    Ja nodokļu grupai un krājumu nodokļu grupai nav krusta, nodokļa kods netiks noteikts.

## <a name="mitigation"></a>Mazinājums

1. Dodieties cauri katrai šīs tēmas sadaļas [Problēmu](#troubleshoot) novēršanas sadaļai un novērsiet iestatījumu, kā nepieciešams. Ja nodokļu grupa un krājumu nodokļu grupa nav pareizi noteikta, [skatiet sadaļu Atbilstošs rezultāts nav atrasts](tcs-troubleshooting-no-matching-result.md).
2. Ja nodokļu grupai un krājumu nodokļu grupai nav krustpunkta, izveidojiet jaunu funkcionalitātes versiju RCS un novērsiet iestatījumu.

    - Doties uz **nodokļu funkcijām** \> **nodokļu kodiem un groupsItem** > **nodokļu grupu.**

        | Rinda. Krājumu PVN grupa | Nodokļu kodi |
        |---------------------|-----------|
        | B grupa             | A; B       |

    Nodokļa kods tiks noteikts kā **A**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
