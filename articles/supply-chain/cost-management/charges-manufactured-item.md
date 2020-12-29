---
title: Saražoto krājumu maksu parādīšana
description: Ražota krājuma konstantas izmaksas atspoguļo operāciju iestatījumu laikus un komponentus ar konstantu daudzumu vai konstantu brāķa apjomu.
author: AndersGirke
manager: tfehr
ms.date: 04/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 274483
ms.assetid: 6f5b851b-c5a7-43ef-b380-0d316667c1ef
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: c5e0175e5743c800d8f04723d03ae503cff3a67a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432981"
---
# <a name="display-charges-for-a-manufactured-item"></a>Saražoto krājumu maksu parādīšana

[!include [banner](../includes/banner.md)]

Ražota krājuma konstantas izmaksas atspoguļo operāciju iestatījumu laikus un komponentus ar konstantu daudzumu vai konstantu brāķa apjomu.

Krājuma maksu aprēķināto summu var parādīt ar krājumu vienības izmaksām. Tomēr dažreiz maksas tiek attēlotas kā atsevišķi lauki un tās netiek iekļautas krājumu vienības izmaksās. Ja maksas tiek attēlotas atsevišķos laukos, tad vienā laukā tiek attēlota kopējā maksu summa un otrā laukā tiek attēlots uzskaites laidiena apjoms, kas izmantots summas amortizācijā. Piemēram, lapā Krājumu cena maksas ir parādītas divos atsevišķos laukos. Tomēr lapā Pabeigt ir parādītas krājumu vienības kopējās izmaksas, un amortizētās izmaksas ir iekļautas vienības izmaksās.

Maksas saražotajiem krājumiem vienmēr tiek iekļautas krājumu vienības izmaksās standarta izmaksu mērķiem. Tās pēc izvēles ir iespējams plānoto izmaksu nolūkiem. Izmaksu novērtēšanas versijas politika pastiprina maksu iekļaušanu ražoto krājumu izmaksās. Aktivizējot krājumu izmaksu ierakstu, tiek atjauninātas maksas krājumu pamata izmaksu informācijai, kas tiek parādīta lapā Krājumu cena. Dažreiz maksas tiek attēlotas kā divi atsevišķi lauki un tās netiek iekļautas krājumu vienības izmaksās. Katra aktivizācija atjaunina krājumu pamata izmaksu informāciju, pat ja aktivizācija atspoguļo dažādas vietas. Tādēļ pamata izmaksu informācija būtu jāizmanto kā atsauces informācija.





