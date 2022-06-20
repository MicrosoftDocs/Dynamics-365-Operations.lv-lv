---
title: TDS aprēķins starpuzņēmumu darījumiem
description: Šajā rakstā ir aprakstīts process, kas tiek izmantots, lai aprēķinātu ieturēto nodokli avotā (TDS) starpuzņēmumu darbībām fāzēs.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: c27bea997804f2c5eff6be2b20064b272ccd062f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8888978"
---
# <a name="tds-calculation-on-intercompany-transactions"></a>TDS aprēķins starpuzņēmumu darījumiem

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts process, kas tiek izmantots, lai aprēķinātu ieturēto nodokli avotā (TDS) starpuzņēmumu darbībām fāzēs.

Kad starpuzņēmuma pirkšanas pasūtījums vai pārdošanas pasūtījums ir izveidots, TDS noklusējuma grupa, kas noteikta debitoram vai kreditoram, tiek izmantota TDS summas aprēķinam. TDS summa tiek grāmatota atgūstamajiem vai maksājamajiem kontiem pēc rēķina iegrāmatošanas.

Oriģinālajam pirkšanas pasūtījumam vai pārdošanas pasūtījumam automātiski tiek izveidots starpuzņēmumu pārdošanas pasūtījums vai pirkšanas pasūtījums. Noklusējuma TDS grupa tiek parādīta starpuzņēmumu pasūtījumā, lai var aprēķināt TDS. Jūs varat izmainīt TDS grupu. Rēķinu var grāmatot tikai tad, ja rēķina neto summa starpuzņēmumu pasūtījumā, kas tiek automātiski izveidots, atbilst rēķina neto summai oriģinālajā pasūtījumā. (Neto summa ir rēķina summa pēc TDS atskaitījuma.)

Piemēram, pārdošanas rēķins ir izveidots 50 000 un tam ir pievienota **10%** TDS grupa. Grāmatotā rēķina summa ir 45 000, un iegrāmatotā TDS summa pārdošanas rēķinam ir 5000. Pirkšanas pasūtījums tiek automātiski izveidots starpuzņēmumu pārdošanas pasūtījumam un tam tiek pievienota **10%** TDS grupa. Ja maināt TDS grupu uz **15%**, rēķinu nevar grāmatot, jo automātiski izveidotā starpuzņēmumu pārdošanas pasūtījuma rēķina neto summa neatbilst sākotnējā pārdošanas pasūtījuma neto rēķina summai.

Maksājumu žurnāls, kas izveidots starpuzņēmumu rēķinam, tiek grāmatots automātiski. Šo maksājumu žurnālu var grāmatot tikai tad, ja tā neto maksājuma summa atbilst neto maksājuma summai oriģinālajā maksājumu žurnālā.
