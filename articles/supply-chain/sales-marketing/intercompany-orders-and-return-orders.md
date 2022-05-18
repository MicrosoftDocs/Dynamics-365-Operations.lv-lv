---
title: Starpuzņēmumu pasūtījumi un atgriešanas pasūtījumi
description: Šajā tēmā skaidroti starpuzņēmumu pasūtījumi un atgriešanas pasūtījumi
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 1c22c021adce5f892ccb6c2ff8735f9e647e8b81
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671847"
---
# <a name="intercompany-orders-and-return-orders"></a>Starpuzņēmumu pasūtījumi un atgriešanas pasūtījumi

[!include [banner](../../includes/banner.md)]

Šajā tēmā ir aprakstīts, kā tiek izveidoti un atjaunināti starpuzņēmumu pirkšanas pasūtījumi, pārdošanas pasūtījumi, atgriešanas pasūtījumi, pirkšanas līgumi un pārdošanas līgumi.

## <a name="about-intercompany-orders"></a>Par starpuzņēmumu pasūtījumiem

Ja izveidojat starpuzņēmumu pārdošanas pasūtījumu, Microsoft Dynamics 365 Supply Chain Management automātiski izveido atbilstošu pirkšanas pasūtījumu. Līdzīgā veidā, izveidojiet starpuzņēmumu pirkšanas pasūtījumu, tiek ierosināta automātiska atbilstoša starpuzņēmumu pārdošanas pasūtījuma izveide.

Tas ir patiess divpusējiem pasūtījumiem (darbības divu saistītu uzņēmumu starpā) un vairumam trīspusēju uzņēmumu (ja starpuzņēmumu darbība sākas ar pārdošanas pasūtījumu ārējam debitoram).

## <a name="intercompany-order-example"></a>Starpuzņēmumu pasūtījuma piemērs

Jums ir divi saistīti uzņēmumi. Uzņēmums A ir pārdošanas filiāle, un uzņēmums B ir sadales departaments. Starpuzņēmumu pārdošanas un pirkšanas pasūtījumi šādos scenārijos tiek izveidoti automātiski:

- Kad uzņēmums A izveido pirkšanas pasūtījumu un kreditors ir uzņēmums B, starpuzņēmumu pārdošanas pasūtījums automātiski tiek izveidots uzņēmumā B. Divpusēja pasūtījuma ķēde sastāv no uzņēmuma A pirkšanas pasūtījuma un uzņēmuma B starpuzņēmumu pārdošanas pasūtījuma.
- Kad uzņēmums B izveido pārdošanas pasūtījumu un debitors ir uzņēmums A, starpuzņēmumu pirkšanas pasūtījums automātiski tiek izveidots uzņēmumā A. Divpusēja pasūtījuma ķēde sastāv no uzņēmuma B pārdošanas pasūtījuma un uzņēmuma A starpuzņēmumu pirkšanas pasūtījuma.
- Ja uzņēmums A vispirms izveido pārdošanas pasūtījumu ārējam debitoram, pirkšanas pasūtījums automātiski var tikt izveidots uzņēmumā A, kas ierosina automātisku starpuzņēmumu pirkšanas pasūtījuma izveidošanu uzņēmumā B. Trīspusēja pasūtījuma ķēde sastāv no pārdošanas pasūtījuma un pirkšanas pasūtījuma uzņēmumā A un starpuzņēmumu pārdošanas pasūtījuma uzņēmumā B.

## <a name="about-intercompany-return-orders"></a>Par starpuzņēmumu atgrieztajiem pasūtījumiem

Varat atgriezt starpuzņēmumu vienības līdzīgi kā parastās vienības. Tomēr ar starpuzņēmumu vienībām, atgriešanas pasūtījums no ārējā debitora izveido starpuzņēmumu pasūtījumu. Tas, savukārt, noved pie automātiskas starpuzņēmumu atgriešanas pārdošanas preču pasūtījumu izveides. Varat arī atgriezt starpuzņēmumu vienību bez ārēja debitora atgriešanas pasūtījuma.

Starpuzņēmumu atgriešanas pasūtījumi, līdzīgi kā parastie atgriešanas pasūtījumi, tiek sākti lapā **Izveidot atgriešanas pasūtījumu**.

Programmā Microsoft Dynamics 365 Supply Chain Management starpuzņēmumu pārdošanas un pirkšanas līgumi tiek automātiski atjaunināti, lai atspoguļotu atgriezto krājumu. Pārdošanas vai pirkšanas līguma saistības attiecībā uz šo krājumu tiek automātiski koriģētas, lai atspoguļotu daudzuma vai summas izmaiņas, kad krājums tiek atgriezts.

## <a name="intercompany-return-order-example"></a>Starpuzņēmumu atgriešanas pasūtījuma piemērs

Uzņēmums A izveido pirkšanas pasūtījumu, kas ir piesaistīts starpuzņēmumu krājuma pirkšanas līgumam. Starpuzņēmumu pārdošanas pasūtījums tiek automātiski izveidots uzņēmumā B, kas ir piesaistīts atbilstošajam pārdošanas līgumam. Pirkšanas līgums un pārdošanas līgums ir saistīti kā starpuzņēmumu līgumi.

Uzņēmums A atgriež starpuzņēmumu krājumu uzņēmumam B. Uzņēmums B izveido krājuma atgriešanas pasūtījumu, un uzņēmumā A automātiski tiek izveidots pirkuma atgriešanas pasūtījums. Saistības pirkšanas līgumā un pārdošanas līgumā, kas saistīti ar sākotnējiem pasūtījumiem, automātiski tiek pielāgotas, lai atspoguļotu daudzuma vai summas izmaiņas.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
