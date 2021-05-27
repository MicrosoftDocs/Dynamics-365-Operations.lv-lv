---
title: Sadalīt rēķina funkcionalitāti
description: Šajā tēmā aprakstīta rēķinu sadalījuma iestatīšana un funkcionalitāte pēc piegādes adreses un nodokļu konta numura (TAN).
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
ms.openlocfilehash: 7dddbb9f69a9735c2a03d2b23928f5cb92d4e0fd
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023423"
---
# <a name="split-invoice-functionality"></a>Sadalīt rēķina funkcionalitāti

[!include [banner](../includes/banner.md)]

Šajā tēmā aprakstīta rēķinu sadalījuma iestatīšana un funkcionalitāte pēc piegādes adreses un nodokļu konta numura (TAN).

Lapas **Kreditoru parametri** cilnē **Vispārīgi** atlasiet izvēles rūtiņu **Produktu kvīts** vai **Rēķins** lai grāmatotu un sadalītu preču kvīti vai rēķinu, kuram ir atšķirīgas piegādes adreses un TAN lapā **Pirkšanas pasūtījums**. Iegrāmatotais rēķins tiks sadalīts pēc piegādes adreses un TAN.

Cilnē **Kopsavilkuma atjauninājums**, kopsavilkuma cilnē **Sadalīt, pamatojoties uz**, rindā **Piegādes informācija** iestatiet opcijas **Apstiprinājums**, **Izdošanas saraksts**, **Pavadzīme** vai **Rēķins** uz **Jā**, lai grāmatotu un sadalītu apstiprinājumu, izdošanas sarakstu, pavadzīmi vai rēķinu, kur dažādas piegādes adreses un rēķini ir definēti dažādām rēķina rindām lapā **Pārdošanas pasūtījums**. Iegrāmatotais rēķins tiks sadalīts vispirms pēc piegādes adreses un tad pēc TAN.

> [!IMPORTANT]
> - Ja **Piegādes informācijas** opcijas nav iestatītas uz **Jā**, rēķins tiks grāmatots kā viens rēķins. Netiek veikta rēķinu sadalīšana.
> - Lai sadalītu un grāmatotu pavadzīmi, kur rēķina rindām ir dažādas piegādes adreses un TAN, jums jāiestata **Pavadzīmes** opcija **Piegādes informācijai** uz **Jā**.
> - Lai sadalītu un grāmatotu rēķinu, kur rēķina rindām ir dažādas piegādes adreses un TAN, jums jāiestata **Rēķina** opcija **Piegādes informācijai** uz **Jā**.
> - Lai sadalītu un grāmatotu rēķinu, kur rēķina rindām ir dažādas piegādes adreses, bet viens un tas pats TAN, jums jāiestata **Rēķina** opcija **Piegādes informācijai** uz **Nē**. Iegrāmatotais rēķins tiks sadalīts pēc piegādes adreses.

## <a name="example"></a>Paraugs

Šajā piemērā **Rēķina** opcija **Piegādes informācijai** tiek iestatīta uz **Jā** cilnes **Kopsavilkuma atjauninājums** lapā **Debitoru parametri**. Tiek grāmatots pirkšanas rēķins, kam rindās ir šādi iestatījumi piegādes adresēm un TAN:

- **1. krājumu rinda:** piegādes adrese 1, TAN-ABCD12345A
- **2. krājumu rinda:** piegādes adrese 1, TAN-ABCD12345A
- **3. krājumu rinda:** piegādes adrese 2, TAN-ABCE12345B
- **4. krājumu rinda:** piegādes adrese 3, TAN-ABCD12345A

Šajā gadījumā oriģinālais rēķins tiek sadalīts divos rēķinos un grāmatots šādā veidā:

- 1. rēķins tiek grāmatots 1. krājuma rindai un 2. krājuma rindai, jo abām rindām ir viena piegādes adrese un TAN.
- 2. rēķins ir grāmatots 3. krājuma rindai.
- 3. rēķins ir grāmatots 4. krājuma rindai.
