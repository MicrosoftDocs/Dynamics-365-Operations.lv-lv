---
title: Starpuzņēmumu pasūtījumu filtrēšana, lai novērstu pasūtījumu un pasūtījumu rindu sinhronizāciju
description: Šajā tēmā tiek aprakstīts, kā filtrēt starpuzņēmumu pasūtījumus, lai novērstu pasūtījumu un pasūtījumu rindu sinhronizāciju.
author: negudava
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: negudava
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 6c5e1e2467673badd20366d3bd8e1b93b8078b26
ms.sourcegitcommit: 0eb33909a419d526eb84b4e4b64d3595d01731ef
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/08/2020
ms.locfileid: "4701037"
---
# <a name="filter-intercompany-orders-to-avoid-synchronizing-orders-and-orderlines"></a>Starpuzņēmumu pasūtījumu filtrēšana, lai novērstu pasūtījumu un pasūtījumu rindu sinhronizāciju

[!include [banner](../../includes/banner.md)]

Varat filtrēt starpuzņēmumu pasūtījumus, lai novērstu elementu **Pasūtījumi** un **Pasūtījumu rindas** sinhronizāciju. Dažos gadījumos starpuzņēmumu pasūtījuma informācija nav nepieciešama klientu iesaistīšanās programmā.

Katrs standarta Common Data Service elements tiek paplašināts ar atsaucēm uz lauku **IntercompanyOrder**, un duālās rakstīšanas kartes tiek modificētas, lai atsauktos uz papildu laukiem filtros. Rezultāts ir tāds, ka starpuzņēmumu pasūtījumi vairs netiek sinhronizēti. Šis process palīdz izvairīties no nevajadzīgiem datiem Customer Engagement programmā.

1. Pievienojiet atsauci uz **IntercompanyOrder** kā **CDS pārdošanas pasūtījumu virsraksti**. Tā tiek aizpildīta tikai starpuzņēmumu pasūtījumos. Lauks **IntercompanyOrder** ir pieejams elementā **SalesTable**.

    :::image type="content" source="media/filter-sales-order-header-field-display.png" alt-text="Kartes iestatīšana mērķim, SalesOrderHeader":::
    
2. Kad elements **CDS pārdošanas pasūtījumu virsraksti** ir paplašināts, lauks **IntercompanyOrder** ir pieejams kartē. Lietojiet filtru ar `INTERCOMPANYORDER == ""` kā vaicājuma virkni.

    :::image type="content" source="media/filter-sales-order-header.png" alt-text="Pārdošanas pasūtījumu virsraksti, vaicājuma rediģēšana":::

3. Pievienojiet atsauci uz **IntercompanyInventTransId** kā **CDS pārdošanas pasūtījumu rindas**.  Tā tiek aizpildīta tikai starpuzņēmumu pasūtījumos. Lauks **InterCompanyInventTransID** ir pieejams elementā **SalesLine**.

    :::image type="content" source="media/filter-sales-order-line-field-display.png" alt-text="Kartes iestatīšana mērķim, SalesOrderLine":::

4. Kad elements **CDS pārdošanas pasūtījumu rindas** ir paplašināts, lauks **IntercompanyInventTransId** ir pieejams kartē. Lietojiet filtru ar `INTERCOMPANYINVENTTRANSID == ""` kā vaicājuma virkni.

    :::image type="content" source="media/filter-sales-order-lines.png" alt-text="Pārdošanas pasūtījuma rindas, vaicājuma rediģēšana":::

5. Paplašiniet elementu **Pārdošanas rēķina virsraksta V2** un **Pārdošanas rēķina rindas V2** tādā pašā veidā, kā jūs paplašinājāt Common Data Service elementus 1. un 2. darbībā. Pēc tam pievienojiet filtra vaicājumus. Filtra virkne elementam **Pārdošanas rēķina virsraksta V2** ir `(INTERCOMPANYORDER == "") && (SALESORDERNUMBER != "")`. Filtra virkne elementam **Pārdošanas rēķina rindu V2** ir `INTERCOMPANYINVENTTRANSID == ""`.

    :::image type="content" source="media/filter-sales-invoice-header-field-display.png" alt-text="Kartes iestatīšana mērķim, pāŗdošanas rēķina virsraksti":::

    :::image type="content" source="media/filter-sales-invoice-header-filter.png" alt-text="Pārdošanas rēķinu virsraksti, vaicājuma rediģēšana":::

    :::image type="content" source="media/filter-sales-invoice-lines-filter.png" alt-text="Pārdošanas rēķinu rindas, vaicājuma rediģēšana":::

6. Elementam **Piedāvājumi** nav starpuzņēmumu attiecību. Ja kāds izveido piedāvājumu vienam no starpuzņēmumu debitoriem, visus šos debitorus var ievietot vienā debitoru grupā, izmantojot lauku **Klientgrupa**.  Virsrakstu un rindas var paplašināt, lai pievienotu lauku **Klientgrupa**, un pēc tam filtrēt, lai neiekļautu šo grupu.

    :::image type="content" source="media/filter-cust-group.png" alt-text="Kartes iestatīšana mērķim, pāŗdošanas piedāvājuma virsraksts":::

7. Pēc tam, kad pagarināt elementu **Piedāvājumi**, lietojiet filtru `CUSTGROUP !=  "<company>"` kā vaicājumu virkni.

    :::image type="content" source="media/filter-cust-group-edit.png" alt-text="Pārdošanas piedāvājuma virsraksts, vaicājuma rediģēšana":::
