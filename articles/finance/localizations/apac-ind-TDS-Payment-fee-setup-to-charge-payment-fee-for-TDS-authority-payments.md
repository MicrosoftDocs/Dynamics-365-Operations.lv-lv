---
title: TDS iestāžu maksājumu iestatīšana
description: Šajā tēmā ir paskaidrots, kā iestatīt maksājumu nodevas, kas tiek iekasētas par No kopējo ienākumu summas atskaitītā nodokļa (TDS) iestādes maksājumiem.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: b52331bb1c7a1bc2c764008112f3df9cc0385995
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023433"
---
# <a name="set-up-payment-fees-for-tds-authority-payments"></a>TDS iestāžu maksājumu iestatīšana

[!include [banner](../includes/banner.md)]

Šajā tēmā ir paskaidrots, kā iestatīt maksājumu nodevas, kas tiek iekasētas par No kopējo ienākumu summas atskaitītā nodokļa (TDS) iestādes maksājumiem.

1. Pārejiet uz sadaļu **Kreditori \> Maksājuma iestatījumi \> Komisijas maksa**.

    [![Maksājumu apmaksas lapa](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)

2. Atlasiet **Jauns**, lai izveidotu maksājumu apmaksu, un pēc tam ievadiet nepieciešamo informāciju.
3. Laukā **Maksājuma tips** atlasiet maksājuma apmaksas tipu.

    - **Neviens**
    - **Procenti** – procenti tiek aprēķināti par nokavētiem maksājumiem, kas tiek veikti TDS iestādes kreditoram.
    - **Citi** – Citi maksājumi tiek aprēķināti par kavējumiem, kas tiek veikti TDS iestādes kreditoram.

    Atlasot **Procenti** vai **Citi**, lauks **Maksa** automātiski tiek iestatīts **Virsgrāmatā**.

4. Ja atlasījāt **Procenti** vai **Citi** laukā **Lauka tips**, laukā **Galvenais konts**, atlasiet Virsgrāmatas kontu, kurā grāmatot procentus vai citas izmaksas.
5. Ievadiet pārējo nepieciešamo informāciju.
6. Darbību rūtī atlasiet **Komisijas maksu iestatījumi**, lai atvērtu lapu **Komisijas maksu iestatījumi**, kur var iestatīt maksājumu komisijas dažādām banku kombinācijām, maksāšanas metodēm, maksājumu specifikācijām, valūtām un datumu intervāliem.

    [![Maksājumu apmaksu iestatīšanas lapa](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)

7. Cilnē **Pārskats** laukā **Grupēšana** norādiet, kurām bankām jūs iestatāt maksājuma komisiju:

    - **Tabula** – komisijas maksa ir derīga noteiktam bankas kontam.
    - **Grupa** – komisijas maksa ir derīga noteiktai bankas grupai.
    - **Visi** - komisijas maksājums ir derīgs visiem bankas kontiem.

8. Ja atlasāt **Tabula** vai **Grupa** laukā **Grupēšana**, laukā **Bankas saistība**, atlasiet noteiktu bankas kontu vai bankas grupu, kam iestatāt komisijas maksu.
9. Laukā **Maksājuma metode** atlasiet metodi, kas tiks izmantota maksājumu komisijas apmaksai.
10. Laukā **Maksājuma specifikācija** atlasiet vai ievadiet maksājuma specifikācijas kodu, kas tika izveidots **Maksājumu specifikācijas** lapā.
    - Maksājuma specifikācija tiek izmantota maksāšanas metodēm, kas attiecināmas uz elektronisko līdzekļu pārsūtīšanu.
12. Laukā **Maksājuma valūta** atlasiet valūtu, kas aktivizē maksu. Tikai darījumi, kas izmanto atlasīto valūtu, var aktivizēt papildu maksu. Ja šo lauku atstājat tukšu, visas valūtas aktivizē papildu maksu.
13. Laukā **Procenti/summa** atlasiet aprēķina metodi. Opcijas ir **Summa**, **Procenti** un **Intervāls**.
14. Laukā **Papildmaksu summa** norādiet maksājuma summu kā maksājuma procentus vai kā summu vienam maksājumam.
15. Laukā **Maksas valūta** norādiet maksas valūtas kodu.
16. Atlasiet cilni **Vispārīgi**, lai skatītu vai modificētu atlasītā bankas konta detalizēto informāciju.

    [![Cilne Vispārīgi](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)

16. Laukā **Minimālais** ievadiet minimālo darījumu summu, kas aktivizē komisiju.
17. Laukā **Maksimālais** ievadiet maksimālo darījuma summu, kas aktivizē komisiju.
18. Laukos **sākuma datums** un **Beigu datums** definējiet datumu diapazonu maksu aprēķināšanai.
19. Laukā **Minimāla papildmaksa** norādiet papildmaksu summu kā maksājuma procentus vai kā summu vienam maksājumam.
20. Laukā **PVN grupa** atlasiet PVN grupu, ko izmantot, lai aprēķinātu PVN maksājuma summai.
21. Laukā **Krājuma PVN grupa** atlasiet krājuma PVN grupu, ko izmantot, lai aprēķinātu krājuma PVN maksājuma summai.
22. Atlasiet cilni **Intervāls**. 

    [![Cilne Intervāls](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)

23. Laukā **Dienas** ievadiet dienu skaitu starp maksājuma grāmatošanas datumu (atlaides datumu) un parādzīmes izpildes datumu.
24. Laukā **Procenti/summa** atlasiet, vai specifikācija ir procenti vai iestatītā summa.
25. Laukā **Papildmaksas summa** ievadiet papildmaksu summu kā maksājuma procentus vai kā summu vienam maksājumam.
26. Aizveriet lapu **Papildmaksu iestatīšana**.
27. Aizveriet lapu **Papildmaksas**.
