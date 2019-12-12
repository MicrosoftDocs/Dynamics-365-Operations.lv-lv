---
title: Atvasinātās grāmatas
description: Šajā rakstā ir sniegts pārskats par atvasināto grāmatu funkcionalitāti.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5c31116ba234bd1fce445ac382fe8f8aea263a66
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769481"
---
# <a name="derived-books"></a>Atvasinātās grāmatas

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegts pārskats par atvasināto grāmatu funkcionalitāti.

Atvasināto grāmatu mērķis ir vienkāršot regulāriem intervāliem plānotu pamatlīdzekļu grāmatu transakciju grāmatošanu.  Izvēlieties vienu grāmatu kā primāro grāmatu. Tā parasti ir grāmata, ko izmanto grāmatvedības nolietojumam. Pēc tam šim modelim tiek pievienotas citas grāmatas, kas ir iestatītas darbību grāmatošanai tādos pašos intervālos kā noteikti primārajā grāmatā. PVN nolietojuma grāmatas bieži tiek iestatītas kā atvasinātās grāmatas. 

Izplatītākās iestatāmās darbības iegrāmatošanai uz atvasinātajām grāmatām ir iegādes, iegādes pielāgojumi un izslēgšanas. 

## <a name="example"></a>Paraugs

Grāmata B un grāmata C ir iestatītas kā atvasinātās grāmatas grāmatai A darbību tipam Iegāde. Grāmatā A ievadiet pamatlīdzekļa 123 iegādes darbību par summu 1500,00. 

Kad darbība ir iegrāmatota, grāmatas B pamatlīdzeklim 123 un grāmatas C pamatlīdzeklim 123 tiek ģenerēta un iegrāmatota iegādes darbība par summu 1500,00. Kad tiek sagatavotas primārās grāmatas darbības pamatlīdzekļu žurnālā, ir iespējams arī apskatīt un rediģēt atvasināto grāmatu darbības. Ja primārās grāmatas darbības tiek sagatavotas citā žurnālā, atvasināto vērtību darbības netiek parādītas. Tomēr, kad primārās grāmatas darbības ir iegrāmatotas, tās tiek iegrāmatotas atbilstošajos kontos un grāmatošanas līmeņos.

> [!NOTE]                                                                                                                               
> Grāmatas, kas iestatītas, lai grāmatotu darbības intervālos, kas atšķiras no primārās grāmatas intervāliem, jāpievieno pamatlīdzeklim kā atsevišķas grāmatas, nevis kā atvasinātas grāmatas.  

Papildu informāciju skatiet rakstā [Grāmatošana ar atvasinātām grāmatām](post-derived-value-models.md).


