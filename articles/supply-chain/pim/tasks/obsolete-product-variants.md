---
title: Novecojušu preces variantu atrašana
description: Šajā procedūrā ir parādīts, kā atrast novecojušas izlaistās preces vai preces variantus un kā preces dzīves cikla stāvokli saistīt ar novecojušām precēm.
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4641d24cfa24722f5411da8943bfe4095a9546a4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "360191"
---
# <a name="find-obsolete-product-variants"></a>Novecojušu preces variantu atrašana 

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir parādīts, kā atrast novecojušas izlaistās preces vai preces variantus un kā preces dzīves cikla stāvokli saistīt ar novecojušām precēm. Priekšnosacījums: pirms šī uzdevuma ceļveža atskaņošanas ir jādefinē vismaz viens preces dzīves cikla stāvoklis, kas ir neaktīvs plānošanai.


## <a name="run-a-simulation"></a>Simulācijas izpilde
1. Dodieties uz Preču informācijas pārvaldība > Periodiskie uzdevumi > Mainīt dzīves cikla stāvokli novecojušām precēm.
2. Laukā Jauns preces dzīves cikla stāvoklis ievadiet vai atlasiet kādu vērtību.
3. Atlasiet Jā laukā Palaist simulāciju bez preču datu atjaunināšanas.
4. Ievadiet skaitli laukā Izslēgt preces, kas izveidotas šādā dienu skaita diapazonā.
5. Ievadiet skaitli laukā Izslēgt transakcijās lietotās preces (dienu skaitā).
6. Izvērsiet sadaļu Iekļaujamie ieraksti.
7. Noklikšķiniet uz Filtrēt.
8. Sarakstā atzīmējiet atlasīto rindu.
9. Laukā Kritēriji ierakstiet kādu vērtību.
10. Noklikšķiniet uz OK.
11. Noklikšķiniet uz OK.

> [!NOTE]
> Ieteicams izpildīt simulāciju partijā, ja ir paredzama liela preču skaita meklēšana. Turklāt pārliecinieties, ka simulācija netiek palaista uzņēmuma aktīvākajā darba laikā.  

## <a name="review-the-simulation-results"></a>Simulācijas rezultātu skatīšana
1. Dodieties uz Preču informācijas pārvaldība > Pieprasījumi un pārskati > Preču dzīves cikla stāvokļa uzturēšanas vēsture.
   
> [!NOTE]
> Šajā lapā varat apskatīt simulācijas rezultātus un novērtēt, cik preču un preces variantu tiks saistīti ar jaunu preces dzīves cikla stāvokli, izpildot atjauninājumu bez simulācijas.  

## <a name="run-the-update-of-the-product-lifecycle-state-for-obsolete-products"></a>Palaidiet atjaunināšanas procesu preces dzīves cikla stāvoklim novecojušām precēm
1. Aizvērt lapu.
2. Dodieties uz Preču informācijas pārvaldība > Periodiskie uzdevumi > Mainīt dzīves cikla stāvokli novecojušām precēm.
3. Izvērsiet sadaļu Iekļaujamie ieraksti.

> [!NOTE]
> Ņemiet vērā, ka ir saglabāta pēdējā atlase.  

4. Atlasiet Nē laukā Palaist simulāciju bez preču datu atjaunināšanas.
5. Izvērsiet sadaļu Palaist fonā.

> [!NOTE]
> Atkarībā no tā, cik daudz preču un preces variantu ir ietekmēti, apsveriet iespēju palaist šo darbu kā pakešuzdevumu. Pārliecinieties, ka liels atjaunināšanas darbs netiek palaists uzņēmuma aktīvākajā darba laikā.  

6. Noklikšķiniet uz OK.
7. Dodieties uz Preču informācijas pārvaldība > Pieprasījumi un pārskati > Preču dzīves cikla stāvokļa uzturēšanas vēsture.

> [!NOTE]
> Apskatiet mainītās izlaistās preces un preču variantus.  

8. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.

