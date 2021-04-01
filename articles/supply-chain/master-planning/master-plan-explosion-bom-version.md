---
title: MK versijas izvēršana
description: Šajā rakstā ir paskaidrots vispārējās plānošanas scenārijs, kas ietver materiālu komplekta (MK) versijas izvēršanu.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 617d9c3f05f2db30ec075a07b54c4827e668c20e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220852"
---
# <a name="explosion-of-a-bom-version"></a>MK versijas izvēršana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir paskaidrots vispārējās plānošanas scenārijs, kas ietver materiālu komplekta (MK) versijas izvēršanu.

Izvēršanas pieprasīšana materiālu komplekta (MK) versijas izveido pieprasījuma katram MK rindas krājumam noteiktā vietā, un, iespējams, konkrētajā noliktavā. Vietai specifisku MK noteiktā noliktavā var definēt katrai MK rindai. Turklāt par katru MK rindu, krājuma dimensiju iestatījumi nosaka, vai noliktava ir nepieciešama. Iegūtais pieprasījums par katru MK rindas vienību tad kļūst par papildu pieprasījuma izvēršana sākumpunktu. Šis vispārējās plānošanas scenārijs ietver šādus nosacījumus:

-   Vietas dimensija ir obligāta un tā ir jāievada pieprasījuma darbībā.
-   Vietas dimensija ir saskaņota. Tādēļ vieta zemāka līmeņa prasībai ir tāda pati kā vietai sākotnējā prasības darbībā.

Šis grafiks ilustrē, kā turpinās vispārējās plānošanas prasības izvēršana. ![Pieprasīt izvēršanu, lietojot MK versiju](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="additional-resources"></a>Papildu resursi
--------

[MK versijas noteikšana](master-plan-bom-version-determined.md)

[Vispārēja plānošanas un vairākvietu funkcionalitātes pārskats](master-plan-multisite-functionality.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]