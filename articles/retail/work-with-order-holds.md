---
title: "Pasūtījumu aizturēšana"
description: "Šajā tēmā ir aprakstīts, kā aizturēt pasūtījumus, izmantojot Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: MCRHoldCodeTable, MCRSalesTableOrderHistory, MCRHoldCodeTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79132
ms.assetid: 7c00dc35-73e5-400a-8587-22f37ddfc0e0
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8b4c8ecbef1dc667d3b60411a53f0c63686529c2
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="order-holds"></a>Pasūtījumu aizturēšana

[!include[banner](includes/banner.md)]


Šajā tēmā ir aprakstīts, kā aizturēt pasūtījumus, izmantojot Dynamics 365 for Retail.

Pasūtījumu var aizturēt dažādu iemeslu dēļ. Piemēram, pasūtījumu var aizturēt līdz debitora adresi vai maksājuma metodi būs iespējams pārbaudīt vai līdz vadītājs varēs pārskatīt debitora kredīta limitu. Gadās, ka pārdošanas procesa laikā pārdošanas pasūtījumi ir jāaiztur. Piemēram, pārdošanas pasūtījums varētu tikt aizturēts, ja radušās problēmas ar debitora maksājumu sakarā ar aizdomām par pārkāpumu, vai tāpēc, ka vadītājam jāpārskata pasūtījums. Kad pārdošanas pasūtījums ir aizturēts, pārdošanas pasūtījumam tiek piešķirts pasūtījuma aizturēšanas kods, ar kuru norāda aizturēšanas iemeslu. Pārdošanas pasūtījuma aizturēšanas kodus var konfigurēt sadaļā **Pārdošana un mārketings** &gt; **Iestatījumi** &gt; **Pārdošanas pasūtījumi** &gt; **Pasūtījumu aizturēšanas kodi**. Aizturēt pārdošanas pasūtījumu var manuāli pasūtījuma izveides brīdī vai vēlāk. Turklāt var pasūtījumu aizturēt automātiski, pamatojoties uz pārkāpumu kārtulām. Kamēr pārdošanas pasūtījums ir aizturēts, iespējams, vajadzēs tam pievienot papildu informāciju. Vai arī varat izrakstīt pārdošanas pasūtījumu, turpinot strādāt pie tā. Varat izrakstīt pārdošanas pasūtījumu, to atkal ierakstīt vai pat ignorēt cita lietotāja veiktu izrakstīšanu, izmantojot pasūtījumu aizturēšanas rīku (**Mazumtirdzniecība** &gt; **Debitori** &gt; **Pasūtījumu aizturēšana**). Ja pasūtījums ir gatavs pabeigšanai, aizturēšana ir jānoņem pirms pasūtījuma procesa pabeigšanas.




