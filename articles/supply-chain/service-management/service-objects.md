---
title: Pakalpojumu objekti
description: "Pakalpojumu objekti ir klienta līdzekļi un preces, kurām jūs varat veikt pakalpojumu."
author: YuyuScheller
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceObjectTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 221b9dae7e83e7f4a535ac60f2a2011533d7861c
ms.openlocfilehash: a69fd6a1b07683383d88c7f5c7986529c7bb1875
ms.contentlocale: lv-lv
ms.lasthandoff: 02/21/2018

---

# <a name="service-objects"></a>Pakalpojumu objekti 

[!include[banner](../includes/banner.md)]

Pakalpojumu objekti ir klienta līdzekļi un preces, kurām jūs varat veikt pakalpojumu. Atkarībā no sniegtā pakalpojuma tipa, objekti var būt materiāli vai nemateriāli:

-  Taustāmie objekti ir lietas, piem., mašīnas vai ēkas, kurām variet veikt fiziskas apkalpošanas uzdevumus.

    Materiāls pakalpojuma objekts var būt arī krājuma vienība, kuru izveidojat veidlapā Nodoto preču papildinformācija. Atkarībā no krājumu dimensijas grupas, kuras pievienojat prece, varat radīt pakalpojuma objektu, kura detalizācijas līmenī ir iekļauts preces sērijas numurs. Tas ir noderīgi, ja ir jāizseko konkrēta prece, kuru pārstāv pakalpojuma objekts.

    Materiāls pakalpojuma objekts var būt arī prece, kura ir netieši saistīta ar kompānijas tiešo produkciju vai piegādes ķēdi. Piemēram, rīku komplekts, kas tiek izmantots remontdarbiem, pakalpojuma pasūtījumā var būt, piemēram, pakalpojuma objekts, kas nav iekļauts krājumos. Šajā gadījumā tas netiek reģistrēts kā krājuma vienība.

-  Nemateriāli objekti ir abstraktas lietas, piemēram konti komplekts vai juridisks dokuments, kurā varat izpildīt pakalpojuma uzdevumu.

## <a name="example-of-an-intangible-service-object"></a>Nemateriāla pakalpojuma objekta paraugs

Uzņēmums A uztur finanšu ierakstus vairākiem maziem uzņēmumiem. Viens no kompānijas A klientiem ir vietējā futbola komanda, kurai kompānija A reizi nedēļā veic grāmatvedības darbus un ikgadēja kluba kontu revīziju. Kluba konti ir iestatīti veidlapā Pakalpojumu objekti un noteikti kā pakalpojumu līguma objekts. Pastāv divas objekta pakalpojumu līgumu līnijas. 1. līnija ir iknedēļas grāmatvedība ar līnijai piešķirto nedēļas intervālu, un 2. līnija ir ikgadēja revīzija ar tai piešķirto gada intervālu.

## <a name="related-topics"></a>Saistītās tēmas

[Pakalpojumu objektu izveide](create-service-objects.md)

