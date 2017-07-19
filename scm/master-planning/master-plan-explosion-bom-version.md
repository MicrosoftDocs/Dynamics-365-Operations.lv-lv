---
title: "MK versijas izvēršana"
description: "Šajā rakstā ir paskaidrots vispārējās plānošanas scenārijs, kas ietver materiālu komplekta (MK) versijas izvēršanu."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: efb184269c66483304af0589e4305a55ae08ce08
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017

---

# <a name="explosion-of-a-bom-version"></a>MK versijas izvēršana

[!include[banner](../includes/banner.md)]


Šajā rakstā ir paskaidrots vispārējās plānošanas scenārijs, kas ietver materiālu komplekta (MK) versijas izvēršanu.

Izvēršanas pieprasīšana materiālu komplekta (MK) versijas izveido pieprasījuma katram MK rindas krājumam noteiktā vietā, un, iespējams, konkrētajā noliktavā. Vietai specifisku MK noteiktā noliktavā var definēt katrai MK rindai. Turklāt par katru MK rindu, krājuma dimensiju iestatījumi nosaka, vai noliktava ir nepieciešama. Iegūtais pieprasījums par katru MK rindas vienību tad kļūst par papildu pieprasījuma izvēršana sākumpunktu. Šis vispārējās plānošanas scenārijs ietver šādus nosacījumus:

-   Vietas dimensija ir obligāta un tā ir jāievada pieprasījuma darbībā.
-   Vietas dimensija ir saskaņota. Tādēļ vieta zemāka līmeņa prasībai ir tāda pati kā vietai sākotnējā prasības darbībā.

Šis grafiks ilustrē, kā turpinās vispārējās plānošanas prasības izvēršana. ![Pieprasīt izvēršanu, lietojot MK versiju](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="see-also"></a>Skatiet arī
--------

[Vispārējā plānošana — kā tiek noteikta MK versija](master-plan-bom-version-determined.md)

[Vispārējā plānošana un vairākvietu funkcionalitāte](master-plan-multisite-functionality.md)




