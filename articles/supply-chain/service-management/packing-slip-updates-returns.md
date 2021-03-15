---
title: Pavadzīmju atjauninājumi atgrieztajiem krājumiem
description: Pirms atgriezto krājumu saņemšanas noliktavā, tiem piederošā pasūtījuma pavadzīme ir jāatjaunina.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPackingSlipJournalHistory, SalesParmPackingSlipTrackingInformation
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c82e43beddb8bae0a56b0894ce484ca7605b42e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006720"
---
# <a name="packing-slip-updates-for-returns"></a>Pavadzīmju atjauninājumi atgrieztajiem krājumiem  

[!include [banner](../includes/banner.md)]


Pirms atgriezto krājumu saņemšanas noliktavā, tiem piederošā pasūtījuma pavadzīme ir jāatjaunina. Tāpat kā rēķinu atjaunināšanas process ir atjaunināšana uz finanšu darījumu, pavadzīmju atjaunināšanas process ir fiziska krājumu ierakstu atjaunināšana. Tas nozīmē, ka tiek veiktas izmaiņas krājumos. Atgriešanas gadījumā darbības, kas ir piešķirtas atgriešanas metodes darbībai, tiek ieviestas pavadzīmes atjaunināšanas laikā.

Pavadzīmju atjaunināšanu ir iespējams apstrādāt krājumu saņemšanas žurnālā vai atgriešanas pasūtījumā.

Kā daļa no pavadzīmju iegrāmatošanas procesa pavadzīmju atsauces numurs no klienta piegādes dokumentiem var tikt saistīts ar pasūtījuma rindām. Šī saistīšana nav obligāta un tiek izmantota tikai kā atsauce. Tā neizraisa nekādus transakcijas atjauninājumus.

Ja nav tikuši saņemti visi paredzētie atgrieztie krājumi, pavadzīmes atjaunināšanā jāiekļauj tikai tas daudzums, kas ticis saņemts. Atlikušie krājumi jāatstāj pasūtījumā, līdz tiek saņemta pārējā kravas daļa.

Ja krājums ticis atsūtīts atpakaļ no karantīnas uz Nosūtīšanas un Saņemšanas nodaļu, piemēram, kad karantīnas inspektors nezina, kur noliktavā uzglabāt šo krājumu, attiecīgā pavadzīme ir jāatjaunina, lai pareizi reģistrētu un rīkotos pēc izvietojuma koda, kas ir noteikts kā karantīnas rezultāts.

Atjauninot pavadzīmi atgrieztajam krājumam, kas ir no pārdošanas līguma, attiecīgā krājuma pārdošanas līguma saistības tiek automātiski atjauninātas, lai atspoguļotu daudzuma vai summas izmaiņas. 

## <a name="see-also"></a>Skatiet arī

[Rēķinu atjauninājumu veikšana atgrieztajiem krājumiem](perform-invoice-updates-for-returns.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]