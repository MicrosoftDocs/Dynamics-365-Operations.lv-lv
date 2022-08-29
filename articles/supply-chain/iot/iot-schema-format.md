---
title: Shēmas formāti IoT Hub ziņojumiem
description: Šajā rakstā skaidrots, kā jums jānoformē ziņojumu shēma, ko varat izmantot Iot Intelligence.
author: johanhoffmann
ms.date: 08/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b6d133d520ce0a1dccb2575e352f63e6ceb2bd3f
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2022
ms.locfileid: "9228638"
---
# <a name="schema-formats-for-iot-hub-messages"></a>Shēmas formāti IoT Hub ziņojumiem

[!include [banner](../../includes/banner.md)]
[!INCLUDE [iot-sdi-announcement](../../includes/iot-sdi-announcement.md)]

Šajā rakstā skaidrots, kā jums jānoformē ziņojumu shēma, ko varat izmantot Iot Intelligence.

## <a name="message-requirements"></a>Ziņojuma prasības

Uz ziņojumu pārraudzīšanu Iot Informācijā attiecas šādi noteikumi:

+ Ziņojumu shēmu formātam jābūt JavaScript Object Notation (JSON).
+ UNIX rekvizītam **laikspiedols**, kur vērtība ir izteikta milisekundēs (ms), ir jāatrodas Microsoft Azure IoT Hub ziņojumā.
+ Ziņojums tiek izsekots tikai tad, ja tas satur visus rekvizītus, kas ir definēti scenārija iestatījumos. Piemēram, ja tiek definēti **ID**, **laikspiedola** un **vērtības** rekvizīti, tiek pārraudzīts šis ziņojums.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True
    }
    ```

    Šis ziņojums netiek pārraudzīts, jo trūkst **vērtības** rekvizīta.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
    }
    ```

+ Lietiskā interneta informācijas ignorē rekvizītus ziņojumā, kas nav definēti scenārija konfigurācijā. Piemēram, ja tiek definēti **ID**, **laikspiedola** un **vērtības** rekvizīti, Lietiskā interneta informācija pārraudzīs šos ziņojumus.

    ```json
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True
    },
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True,
        "machine" : "Machine1225",
    },
    {
        "id": "IoTInt.Machine1225.PartOut",
        "timestamp": 1576016821614,
        "value": True,
         "activity": "PartOut"
    },
    ```

+ Lietiskā interneta informācija klusi ignorē ziņojumus, kas neatbilst scenārija konfigurācijas kritērijiem.
+ Jūs varat definēt un izmantot vairākus ziņojumu shēmu tipus.
+ Nav jādefinē visi ziņojumu shēmu tipi. Jādefinē tikai shēmas, kas tiks izmantotas Lietiskā interneta informācijas scenārijiem.

## <a name="id-value-pair-schema"></a>ID vērtību pāra shēma

ID vērtību pāris ir vienotais Lietiskā interneta informācijas ziņojumu shēmu modelis. Izmantojot ID vērtību pāri, pārliecinieties, vai visos scenārijos ziņojumu shēma ir vienāda. Piemēram, šeit ir ziņojums **Aprīkojuma dīkstāves** vai **Ražošanas aizkaves** scenārijam.

```json
{
    "id": "IoTInt.Machine1225.PartOut",
    "timestamp": 1576016821614,
    "value": True
}
```

Šeit ir ziņojums **Preces kvalitātes** scenārijam.

```json
{
    "id": "IoTInt.Machine1225.Temperature",
    "timestamp": 1576016821614,
    "value": 105
}
```

Abi iepriekšējie ziņojumi satur **ID** un **vērtības** rekvizītus. **ID** vērtības var kartēt **Signāla datu vērtību** tabulā, iestatot scenāriju. **Aprīkojuma dīkstāves** scenārijam jūs kartēsiet **IoTInt.Machine1225.PartOut** vērtību. **Preces kvalitātes** scenārijam jūs kartēsiet **IoTInt.Machine1225.Temperature** vērtību.

Papildinformācijai skatiet [Azure IoT Hub dokumentācija](/azure/iot-hub/).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]