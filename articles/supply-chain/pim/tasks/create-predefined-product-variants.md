---
title: Iepriekš definētu preces variantu izveide
description: Šajā procedūrā ir aprakstīts, kā izveidot preces variantus preces šablonam, izmantojot preču dimensiju kombinācijas.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab4f43957f7c661349714dbb0933ac3c1d19ab0e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "349818"
---
# <a name="create-predefined-product-variants"></a>Iepriekš definētu preces variantu izveide

[!include [task guide banner](../../includes/task-guide-banner.md)]

Šajā procedūrā ir aprakstīts, kā izveidot preces variantus preces šablonam, izmantojot preču dimensiju kombinācijas. Demonstrācijas uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.


## <a name="create-a-product-master"></a>Preces šablona izveide
1. Pārejiet uz sadaļu Preču informācijas pārvaldība > Preces > Preces šabloni.
2. Noklikšķiniet uz Jauns.
3. Laukā Preces numurs ierakstiet vērtību.
    * Manuāla preces numura ievadīšana ir nepieciešama tikai tad, ja preces numura laukā nebija iestatīta numuru sērija. Citiem vārdiem sakot, izlaidiet šo soli, ja attiecīgajā laukā ir iestatīta numuru sērija.  
4. Laukā Preces nosaukums ierakstiet kādu vērtību.
5. Laukā Preces dimensijas grupa ievadiet vai atlasiet kādu vērtību.
    * Atlasiet preces dimensijas grupu SizeCol (izmērs un krāsa).  
6. Noklikšķiniet uz OK.

## <a name="add-product-dimensions"></a>Pievienot preces dimensijas
1. Noklikšķiniet uz Preces dimensijas.
    * Šajā piemērā parādīts, kā manuāli ievadīt preču dimensijas. Jūs varat arī atlasīt izmēru, krāsu un stilu grupu, kurā ietilpst preces dimensiju vērtības, ko vēlaties izmantot.  
2. Noklikšķiniet uz Jauns.
3. Sarakstā atzīmējiet atlasīto rindu.
4. Laukā Izmērs ievadiet vai atlasiet kādu vērtību.
5. Laukā Nosaukums ierakstiet kādu vērtību.
6. Klikšķiniet Jauns.
7. Sarakstā atzīmējiet atlasīto rindu.
8. Laukā Izmērs ievadiet vai atlasiet kādu vērtību.
9. Laukā Nosaukums ierakstiet kādu vērtību.
10. Noklikšķiniet uz cilnes Krāsas.
11. Noklikšķiniet uz Jauns.
12. Sarakstā atzīmējiet atlasīto rindu.
13. Laukā Krāsa ievadiet vai atlasiet kādu vērtību.
14. Laukā Nosaukums ierakstiet kādu vērtību.
15. Klikšķiniet Jauns.
16. Sarakstā atzīmējiet atlasīto rindu.
17. Laukā Krāsa ievadiet vai atlasiet kādu vērtību.
18. Laukā Nosaukums ierakstiet kādu vērtību.
19. Noklikšķiniet uz Saglabāt.
20. Aizvērt lapu.

## <a name="generate-product-variants"></a>Ģenerēt preces variantus
1. Noklikšķiniet uz Preces varianti.
2. Noklikšķiniet uz Variantu ieteikumi.
3. Noklikšķiniet uz Atlasīt visu.
    * Šajā piemērā ir atlasīti visi iespējamie varianti. Ja variantu izveidei tiks izmantota tikai iespējamo preces dimensiju kombināciju apakškopa, varat atlasīt atsevišķus ierakstus.  
4. Noklikšķiniet uz Izveidot.
    * Jūs varat ģenerēt aprakstus visiem variantiem, pamatojoties uz preču dimensiju vērtību kombināciju. Apraksti nav obligāti.  
5. Noklikšķiniet uz Saglabāt.

