---
title: Pakalpojumu objektu pārskats
description: Šajā tēmā sniegts pārskats par to, kā strādāt ar pakalpojumu objektiem.
author: kamaybac
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9cf5e146bb7eab4df5807c6a55f773bfb31a4c5e
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571381"
---
# <a name="service-objects-overview"></a>Pakalpojumu objektu pārskats

[!include [banner](../includes/banner.md)]

Pakalpojumu objekti ir debitora līdzekļi un preces, kurām jūs varat veikt pakalpojumu. Atkarībā no sniegtā pakalpojuma tipa, objekti var būt materiāli vai nemateriāli:

-  Taustāmie objekti ir lietas, piem., mašīnas vai ēkas, kurām variet veikt fiziskas apkalpošanas uzdevumus.

    Materiāls pakalpojuma objekts var būt arī krājuma vienība, kuru izveidojat veidlapā Nodoto preču papildinformācija. Atkarībā no krājumu dimensijas grupas, kuras pievienojat prece, varat radīt pakalpojuma objektu, kura detalizācijas līmenī ir iekļauts preces sērijas numurs. Tas ir noderīgi, ja ir jāizseko konkrēta prece, kuru pārstāv pakalpojuma objekts.

    Materiāls pakalpojuma objekts var būt arī prece, kura ir netieši saistīta ar kompānijas tiešo produkciju vai piegādes ķēdi. Piemēram, rīku komplekts, kas tiek izmantots remontdarbiem, pakalpojuma pasūtījumā var būt, piemēram, pakalpojuma objekts, kas nav iekļauts krājumos. Šajā gadījumā jūs nereģistrējat to kā krājuma vienību.

-  Nemateriāli objekti ir abstraktas lietas, piemēram konti komplekts vai juridisks dokuments, kurā varat izpildīt pakalpojuma uzdevumu.

## <a name="example-of-an-intangible-service-object"></a>Nemateriāla pakalpojuma objekta paraugs

Uzņēmums A uztur finanšu ierakstus vairākiem maziem uzņēmumiem. Viens no kompānijas A klientiem ir vietējā futbola komanda, kurai kompānija A reizi nedēļā veic grāmatvedības darbus un ikgadēja kluba kontu revīziju. Kluba konti ir iestatīti veidlapā Pakalpojumu objekti un noteikti kā pakalpojumu līguma objekts. Pastāv divas objekta pakalpojumu līgumu līnijas. 1. līnija ir iknedēļas grāmatvedība ar līnijai piešķirto nedēļas intervālu, un 2. līnija ir ikgadēja revīzija ar tai piešķirto gada intervālu.

## <a name="related-topics"></a>Saistītās tēmas

[Pakalpojumu objektu izveide](create-service-objects.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]