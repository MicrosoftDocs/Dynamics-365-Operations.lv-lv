---
title: Iespējot atkļūdošanas režīmu nodokļu aprēķināšanas pakalpojumā
description: Šajā tēmā skaidrots, kā iespējot atkļūdošanas režīmu nodokļu aprēķināšanas pakalpojumā, lai izpētītu problēmas.
author: hangwan
ms.date: 03/25/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: ''
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 03/23/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 2f526a2341c7ef682209ed979fe686e31ad62a37
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/27/2022
ms.locfileid: "8648160"
---
# <a name="enable-debug-mode-in-the-tax-calculation-service"></a>Iespējot atkļūdošanas režīmu nodokļu aprēķināšanas pakalpojumā

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidrots, kā iespējot atkļūdošanas režīmu nodokļu aprēķināšanas pakalpojumā, lai izpētītu problēmas.

1. Pievienojiet **&atkļūdot=vsCconfirmExit%2&** gt programmas objektu servera (AOS) vietrādim URL un pēc tam atsvaidziniet lapu.
2. Atlasot PVN **PVN aprēķinam**, **tiek atvērts teksta fails ar nosaukumu TaxServiceTroubleshootingLog.txt**. Failā **TaxServiceTroubleshootingLog.txt** ir iekļauts **TaxableDocument** un aprēķina parametrs. Šie rezultāti tiek atgriezti no nodokļu servisa un izņēmuma informācijas problēmu novēršanai.

## <a name="sample"></a>Paraugs

```json
===============================Tax service calculation input JSON:=====================================
{
    "TaxableDocument": {
    "Header": [
        {
        "Lines": [
            {
            "Transaction Line ID": "5816,68719677391",
            ...
            }
        ],
        "Transaction Header ID": "2022,68719506302",
        ...
        }
    ]
    },
    "Parameter": {
    "ContinueOnErrors": true,
    ...
    },
    "Adjustment": {
    "Lines": {}
    }
}
===========================Tax service calculation result JSON:=================================
{
    "taxDocument": {
    "Header": [
        {
        "Lines": [
            {
            "Tax Codes": {
                ...
            }
        ],
        "Measures": {
            "List Code": "EUTrade"
        },
        "Tax Registration ID": null,
        "Transaction Header ID": "2022,68719506302",
        "Errors": null
        }
    ]
    },
    "solutionId": "b51e0025-cbbe-4d37-bf0b-90d7be4f214d|1",
    "isPartialSuccess": false
}
=============================CorrelationId:==============================
"21f3a8a1-ee9a-477b-b44e-b8ec79e74d16"
```

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
