---
title: Manuāli izveidot pārraudzītus ieteikumus
description: Šajā tēmā izskaidrots, kā prečzinis var manuāli izveidot un pārvaldīt preču sarakstus Microsoft Dynamics 365 Commerce klientiem.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0b866704b419fb07dcf1ddd386af2f7d6cfa02e2
ms.sourcegitcommit: fdc5dd9eb784c7d8e75692c8cdba083fe0dd87ce
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/26/2020
ms.locfileid: "3404120"
---
# <a name="manually-create-curated-recommendations"></a>Manuāli izveidot pārraudzītus ieteikumus

[!include [banner](includes/banner.md)]

Šajā tēmā izskaidrots, kā prečzinis var manuāli izveidot un pārvaldīt preču ieteikumu sarakstus Microsoft Dynamics 365 Commerce klientiem.

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

![Pārraudzīta saraksta piemērs operāciju uzskaites daļā](./media/examplecuratedrecolist.png)

## <a name="additional-resources"></a>Papildu resursi

[Preču ieteikumu apskats](product-recommendations.md)

[Iespējojiet Azure Data Lake Storage vidē Dynamics 365 Commerce](enable-adls-environment.md)

[Iespējot preču ieteikumus](enable-product-recommendations.md)

[Personalizētu ieteikumu iespējošana](personalized-recommendations.md)

[Atteikšanās no personalizētiem ieteikumiem](personalization-gdpr.md)

[Pievienot preču ieteikumus punktā POS](product.md)

[Ieteikumu pievienošana transakciju ekrānam](add-recommendations-control-pos-screen.md)

[AI-ML ieteikumu rezultātu pielāgošana](modify-product-recommendation-results.md)

[Izveidot ieteikumus ar demonstrācijas datiem](product-recommendations-demo-data.md)

[Bieži uzdotie jautājumi par preču ieteikumiem](faq-recommendations.md)
