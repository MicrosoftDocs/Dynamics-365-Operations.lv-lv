---
title: "Atvasinātās grāmatas"
description: "Šajā rakstā ir sniegts pārskats par atvasināto grāmatu funkcionalitāti."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetBookTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3401
ms.assetid: 862d6450-187b-497f-9822-cce45f2c65a9
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 39035fe2e22987305b2ec6731e5c3b3390043a2a
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="derived-books"></a>Atvasinātās grāmatas

[!include[banner](../includes/banner.md)]


Šajā rakstā ir sniegts pārskats par atvasināto grāmatu funkcionalitāti.

Atvasināto grāmatu mērķis ir vienkāršot regulāriem intervāliem plānotu pamatlīdzekļu grāmatu transakciju grāmatošanu.  Izvēlieties vienu grāmatu kā primāro grāmatu. Tā parasti ir grāmata, ko izmanto grāmatvedības nolietojumam. Pēc tam šim modelim tiek pievienotas citas grāmatas, kas ir iestatītas darbību grāmatošanai tādos pašos intervālos kā noteikti primārajā grāmatā. PVN nolietojuma grāmatas bieži tiek iestatītas kā atvasinātās grāmatas. 

Izplatītākās iestatāmās darbības iegrāmatošanai uz atvasinātajām grāmatām ir iegādes, iegādes pielāgojumi un izslēgšanas. 

## <a name="example"></a>Paraugs

Grāmata B un grāmata C ir iestatītas kā atvasinātās grāmatas grāmatai A darbību tipam Iegāde. Grāmatā A ievadiet pamatlīdzekļa 123 iegādes darbību par summu 1500,00. 

Kad darbība ir iegrāmatota, grāmatas B pamatlīdzeklim 123 un grāmatas C pamatlīdzeklim 123 tiek ģenerēta un iegrāmatota iegādes darbība par summu 1500,00. Kad tiek sagatavotas primārās grāmatas darbības pamatlīdzekļu žurnālā, ir iespējams arī apskatīt un rediģēt atvasināto grāmatu darbības. Ja primārās grāmatas darbības tiek sagatavotas citā žurnālā, atvasināto vērtību darbības netiek parādītas. Tomēr, kad primārās grāmatas darbības ir iegrāmatotas, tās tiek iegrāmatotas atbilstošajos kontos un grāmatošanas līmeņos.

> [!NOTE]                                                                                                                               
> Grāmatas, kas iestatītas, lai grāmatotu darbības intervālos, kas atšķiras no primārās grāmatas intervāliem, jāpievieno pamatlīdzeklim kā atsevišķas grāmatas, nevis kā atvasinātas grāmatas.  

Papildu informāciju skatiet rakstā [Grāmatošana ar atvasinātām grāmatām](post-derived-value-models.md).




