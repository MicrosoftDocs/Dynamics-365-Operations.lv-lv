---
title: Starpuzņēmumu pasūtījumu filtrēšana, lai novērstu pasūtījumu un pasūtījumu rindu sinhronizāciju
description: Šajā tēmā ir izskaidrots, kā filtrēt starpuzņēmumu pasūtījumus, lai pasūtījumu un pasūtījumu rindu elementi nebūtu sinhronizēti.
author: negudava
ms.date: 11/09/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: negudava
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 8575f38ca23ef245947a41c35846983604662ef2
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782557"
---
# <a name="filter-intercompany-orders-to-avoid-syncing-orders-and-orderlines"></a>Starpuzņēmumu pasūtījumu filtrēšana, lai novērstu pasūtījumu un pasūtījumu rindu sinhronizāciju

[!include [banner](../../includes/banner.md)]

Varat filtrēt starpuzņēmumu pasūtījumus, lai novērstu elementu **Pasūtījumi** un **Pasūtījumu rindas** sinhronizāciju. Dažos gadījumos starpuzņēmumu pasūtījuma informācija nav nepieciešama programmā Customer Engagement.

Katra standarta Dataverse tabula tiek paplašināta ar atsaucēm uz kolonnu **IntercompanyOrder**, un duālās rakstīšanas kartes tiek modificētas, lai atsauktos uz papildu kolonnām filtros. Tādēļ starpuzņēmumu pasūtījumi vairs netiek sinhronizēti. Šis process palīdz izvairīties no nevajadzīgiem datiem programmā Customer Engagement.

1. Paplašināt **CDS pārdošanas pasūtījumu virsrakstu** tabulu, pievienojot atsauci kolonnai **IntercompanyOrder**. Šī kolonna tiek aizpildīta tikai starpuzņēmuma pasūtījumiem. Lauks **IntercompanyOrder** ir pieejams elementā **SalesTable**.

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Kartēt sagatavošanas sadaļas ar mērķa lapu CDS pārdošanas pasūtījumu galvenēm.":::

2. Kad elements **CDS pārdošanas pasūtījumu virsraksti** ir paplašināts, kolonna **IntercompanyOrder** ir pieejama kartēšanai. Lietojiet filtru ar `INTERCOMPANYORDER == ""` kā vaicājuma virkni.

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Rediģēt vaicājuma dialoglodziņu CDS pārdošanas pasūtījumu galvenēm.":::

3. Paplašināt **CDS pārdošanas pasūtījumu virsrakstu** tabulu, pievienojot atsauci kolonnai **IntercompanyOrder**. Šī kolonna tiek aizpildīta tikai starpuzņēmuma pasūtījumiem. Kolonna **IntercompanyOrder** ir pieejama tabulā **SalesTable**.

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Kartēt sagatavošanas sadaļas ar mērķa lapu CDS pārdošanas pasūtījumu līnijām.":::

4. Kad ir paplašināta tabula **CDS pārdošanas pasūtījumu rindas**, kolonna **IntercompanyInventTransId** ir pieejama kartēšanai. Lietojiet filtru ar `INTERCOMPANYINVENTTRANSID == ""` kā vaicājuma virkni.

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Rediģēt vaicājuma dialoglodziņu CDS pārdošanas pasūtījumu līnijām.":::

5. Atkārtojiet 1. un 2. darbību, lai paplašinātu tabulu **Pārdošanas rēķina galvene V2** un pievienotu filtra vaicājumu. Šajā gadījumā izmantojiet `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")` filtra vaicājuma virkni.

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Kartēt sagatavošanas sadaļas ar mērķa lapu Pārdošanas pasūtījumu galvene V2.":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Rediģēt vaicājuma dialoglodziņu Pārdošanas pasūtījumu galvene V2.":::

6. Atkārtojiet 3. un 4. darbību, lai paplašinātu tabulu **Pārdošanas rēķina līnijas V2** un pievienotu filtra vaicājumu. Šajā gadījumā izmantojiet `INTERCOMPANYINVENTTRANSID == ""` filtra vaicājuma virkni.

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Rediģēt vaicājuma dialoglodziņu Pārdošanas pasūtījumu līnijas V2.":::

7. Tabulai **Piedāvājumi** nav starpuzņēmumu attiecību. Ja kāds izveido piedāvājumu vienam no starpuzņēmumu debitoriem, visus šos debitorus var ievietot vienā debitoru grupā, izmantojot kolonnu **CustGroup**. Virsrakstu un rindas var paplašināt, pievienojot kolonnu **CustGroup** un pēc tam filtrējiet tā, lai grupa nebūtu iekļauta.

    :::image type="content" source="media/filter-cust-group.png" alt-text="Kartēt sagatavošanas sadaļas ar mērķa lapu Pārdošanas pasūtījumu galvene CDS.":::

8. Pēc tabulas **Piedāvājumi** paplašināšanas lietojiet filtru `CUSTGROUP != "<company>"` kā vaicājumu virkni.

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Rediģēt vaicājuma dialoglodziņu Pārdošanas pasūtījumu galvene CDS.":::


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]