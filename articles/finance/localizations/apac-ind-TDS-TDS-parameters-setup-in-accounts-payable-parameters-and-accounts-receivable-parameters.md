---
title: Iestatiet TDS parametrus Kreditoriem un Debitoriem
description: Šajā tēmā skaidrots, kā iestatīt parametrus sadaļā Kreditori un Debitori, lai atbalstītu No kopējo ienākumu summas atskaitīto nodokļu (TDS) ieturējumus.
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
ms.openlocfilehash: 4540cdfff2362d8fb7cc2b4cccf9c340be9750ce
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023418"
---
# <a name="set-tds-parameters-in-accounts-payable-and-accounts-receivable"></a>Iestatiet TDS parametrus Kreditoriem un Debitoriem

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidrots, kā iestatīt parametrus sadaļā Kreditori un Debitori, lai atbalstītu No kopējo ienākumu summas atskaitīto nodokļu (TDS) ieturējumus.

1. Dodieties uz **Nodoklis \> Iestatīšana \> Parametri \> Debitoru parādu parametri**.
2. Cilnē **Atjauninājumi** atlasiet **Atjaunināt pasūtījuma rindas**, lai atvērtu dialoglodziņu **Atjaunināt pasūtījuma rindas**.
3. Sadaļas **TDS grupa** laukā **Atjaunināt TDS grupu** norādiet metodi, ko izmantot TDS grupas atjaunināšanai rindas līmenī. Šis iestatījums tiek izmantots, kad TDS grupa tiek atjaunināta pasūtījuma galvenē. Pieejamas šādas opcijas:

    - **Nekad** – TDS grupa netiek atjaunināta pasūtījuma rindās, kad tā tiek atjaunināta pasūtījuma galvenē.
    - **Vienmēr** – TDS grupa tiek automātiski atjaunināta pasūtījuma rindās, kad tā tiek atjaunināta pasūtījuma galvenē.
    - **Uzvedne** – lietotāji saņem ziņojumu, kas pieprasa atjaunināt TDS grupu pasūtījuma rindās.
4. Atlasiet **Labi**.

    [![Atjaunināt pasūtījuma rindu dialoglodziņš](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)

5. Dodieties uz **Nodoklis \> Iestatīšana \> Parametri \> Kreditoru parādu parametri**.
6. Cilnes **Vispārīgi** kopsavilkuma cilnē **Sadalīt, pamatojoties uz piegādes informāciju** iestatiet opciju **Produkta kvīts** uz **Jā**, lai grāmatotu un sadalītu produktu kvīti ar dažādām piegādes adresēm un nodokļu konta numuriem (TAN). Ja šī opcija ir iestatīta uz **Nē**, nevar grāmatot pirkšanas pavadzīmi ar dažādām piegādes adresēm un TAN.
7. Iestatiet opciju **Rēķins** uz **Jā**, lai grāmatotu un sadalītu pirkšanas rēķinu ar dažādām piegādes adresēm un TAN.

    [![Sadalīt, pamatojoties uz kopsavilkuma cilni Piegādes informācija](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)

8. Aizvērt lapu.
