---
title: Manuāli izveidot pārraudzītus ieteikumus
description: Šajā rakstā skaidrots, kā preču tirgūētāji var manuāli izveidot un pārvaldīt debitoru preču sarakstus Microsoft Dynamics 365 Commerce.
author: bebeale
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e1a1b402165c5cb35696cf1cf6630770ad07508a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892682"
---
# <a name="manually-create-curated-recommendations"></a>Manuāli izveidot pārraudzītus ieteikumus

[!include [banner](includes/banner.md)]

Šajā rakstā skaidrots, kā tirgūētāji var manuāli izveidot un pārvaldīt produktu rekomendāciju sarakstus debitoriem Microsoft Dynamics 365 Commerce.

Pārraudzīti saraksti ir atsevišķa satura kolekcijas, ko veido un pārrauga cilvēki.  

## <a name="create-a-new-list"></a>Jauna saraksta izveide

Lai izveidotu pārvaldītu preču rekomendāciju sarakstu, veiciet šādas darbības.

1. Pärejiet uz **Mazumtirdzniecība un komercija &gt; Preču ieteikumi &gt; Ieteikumu saraksti**.
1. Atlasiet **Jauns**.
1. Ievadiet vērtību laukā **Saraksta ID**.
1. Ievadiet vērtību laukā **Saraksta nosaukums**.
    - **Saraksta nosaukums** ir tā saraksta nosaukums, kas parādīsies moduļa **Preču kolekcijas** pārraudzītu sarakstu sadaļā.
1. Lai pievienotu preces sarakstam , atlasiet **Pievienot preces**.
1. Lai sarakstā mainītu preču secību, ievadiet vērtību kolonnā **Rādīšanas secība**.
    - Ja divām precēm ir tāda pati rādīšanas secības vērtība, tad šo divu rezultātu gala secība var atšķirties no tās, kas ir operāciju uzskaites daļā.
1. Atlasiet **Saglabāt**, lai saglabātu sarakstu.

## <a name="example-list"></a>Saraksta piemērs

![Pārraudzīta saraksta piemērs operāciju uzskaites daļā.](./media/examplecuratedrecolist.png)

## <a name="additional-resources"></a>Papildu resursi

[Preču ieteikumu apskats](product-recommendations.md)

[Iespējojiet Azure Data Lake Storage pakalpojuma Dynamics 365 Commerce vidē](enable-adls-environment.md)

[Iespējot preču ieteikumus](enable-product-recommendations.md)

[Personalizētu ieteikumu iespējošana](personalized-recommendations.md)

[Atteikšanās no personalizētiem ieteikumiem](personalization-gdpr.md)

[Iespējot "veikala līdzīgie izskati" rekomendācijas](shop-similar-looks.md)

[Preču ieteikumu pievienošana punktā POS](product.md)

[Ieteikumu pievienošana transakciju ekrānam](add-recommendations-control-pos-screen.md)

[AI-ML ieteikumu rezultātu pielāgošana](modify-product-recommendation-results.md)

[Izveidot ieteikumus ar demonstrācijas datiem](product-recommendations-demo-data.md)

[Bieži uzdotie jautājumi par preču ieteikumiem](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]