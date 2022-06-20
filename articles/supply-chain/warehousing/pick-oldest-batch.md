---
title: Vecākās partijas izdošana ar mobilo ierīci
description: Šajā rakstā ir aprakstīts, kā iestatīt un lietot opcijas, lai izdotu vecāko paketi no mobilās ierīces.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad1f2cfd029d71784d5efcc169178a791f0ae077
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885643"
---
# <a name="pick-oldest-batch-on-a-mobile-device"></a>Vecākās partijas izdošana ar mobilo ierīci

[!include [banner](../includes/banner.md)]

Konfigurācijai **Izdot vecāko partiju** varat piekļūt no mobilās ierīces izvēlnes, un tā jums ļauj piespiest vai brīdināt noliktavas darbiniekus, ka viņu pašreizējā novietojumā ir jāizdod vecākā partija.  

## <a name="where-it-applies"></a>Darbības tvērums
Vecākās partijas izdošana tiek konfigurēta mobilās ierīces izvēlnes vienumos, un tā ietekmē izdošanu partijā iekļautajiem krājumiem.

## <a name="how-to-set-up-the-configuration-for-pick-oldest-batch"></a>Kā iestatīt konfigurāciju Izdot vecāko partiju 
Krājumiem, kas ir iestatīti lietot pastāvošu darbu **Izdot vecāko partiju**, no mobilās ierīces izvēlnes varat iestatīt opciju **Nav**, **Brīdināt** vai **Piespiest**.

**Nav**: darbinieki nesaņem nekādus ziņojumus, un viņiem ir atļauts izdot jebkādu partiju savā novietojumā.

**Brīdināt** un **Piespiest**: kad darbinieks atlasa kādu partiju, virs šīs partijas vadīklas tiek parādīts saraksts ar partijām, kurām ir visvecākais beigu datums. Ja novietojums ir atkarīgs no noliktavas vienības, tad virs noliktavas vienības vadīklas tiek parādīts saraksts ar noliktavas vienībām, kurām ir visvecākā partija. 
-   **Brīdināt**: ja darbinieks izvēlas noliktavas vienību vai partiju, kas netiek rādīta sarakstā, tad vadīkla kļūst tukša un tiek parādīts brīdinājums, ka var izvēlēties vecāku partiju. Ļaut varētu turpināt darbu, darbinieks var vēlreiz atlasīt to pašu noliktavas vienību vai partiju.  
-   **Piespiest**: darbinieki turpina saņemt ziņojumu, ka var izvēlēties vecāku partiju.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]