---
title: Pielāgotu atbilžu lapu izveide 4xx/5xx statusa koda kļūdām
description: Šajā tēmā ir aprakstīts, kā izveidot pielāgotas atbilžu lapas 4xx un 5xx statusa koda kļūdām, izmantojot autorēšanas rīkus programmā Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: bcceeb1bc68c6432442c863ca06b7ba81d0abed8
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697110"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a>Pielāgotu atbilžu lapu izveide 4xx/5xx statusa koda kļūdām

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīts, kā izveidot pielāgotas atbilžu lapas 4xx un 5xx statusa koda kļūdām, izmantojot autorēšanas rīkus programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Ja pieprasījums ir neveiksmīgs, serveris izdod HTTP statusa koda kļūdas atbildes. 404 statusa kods tiek iegūts un atgriezts, ja lapa netiek atrasta, un 500 statusa kods tiek iegūts un atgriezts servera kļūdas gadījumā. Lietojumprogrammā Dynamics 365 Commerce lietotāji var izveidot pielāgotas statusa koda kļūdas atbilžu lapas, kas tiek rādītas lietotājiem saistībā ar šīm statusa koda kļūdām.

## <a name="build-a-status-code-error-response-page"></a>Statusa koda kļūdas atbildes lapas izveide

Lai sāktu statusa koda kļūdas atbildes lapas izveidi, veiciet tālāk norādītās darbības.

1. Vēlamajā tīmekļa pārlūkā pierakstieties programmā Dynamics 365 Commerce. 
1. Atlasiet vietni, kurai vēlaties izveidot 4xx/5xx statusa koda kļūdas atbildes lapu.

### <a name="build-the-template"></a>Veidnes izveide

Lai izveidotu veidni statusa koda kļūdas atbildes lapai, veiciet tālāk norādītās darbības.

1. Dodieties uz **Veidnes \>Jauna veidne**.
1. Nosauciet jauno veidni.
1. Izveidojiet veidni, pamatojoties uz struktūru, ko vēlaties izmantot statusa koda kļūdas atbildes lapā.
1. Pārbaudiet veidni un publicējiet to.

### <a name="build-the-status-code-error-response-page"></a>Statusa koda kļūdas atbildes lapas izveide

Lai izveidotu statusa koda kļūdas atbildes lapu, veiciet tālāk norādītās darbības.

1. Dodieties uz **Lapas \>Jauna lapa**.
1. Norādiet nosaukumu statusa koda kļūdas atbildes lapai, bet **neiestatiet** vietrāža **URL** lauku.
1. Veidojiet lapu.
1. Pārbaudiet lapu un publicējiet to.

> [!NOTE]
> Varat izveidot atsevišķas statusa koda kļūdas atbildes lapas 4xx un 5xx statusa koda kļūdām. Alternatīvi varat izmantot vienu un to pašu vispārīgā statusa koda kļūdas atbildes lapu abām kļūdu kategorijām.

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a>Novirzīšanas iestatīšana statusa koda kļūdas atbildes lapai

Lai iestatītu novirzīšanu statusa koda kļūdas atbildes lapai, veiciet tālāk norādītās darbības.

1. Dodieties uz **vietrāži URL \> Jauns \> Jauns aizstājvārds** un atlasiet iepriekš izveidoto statusa koda kļūdas atbildes lapu.
1. Laukā **Aizstājvārds** ievadiet vai nu**default-4xx**, vai **default-5xx**, atkarībā no statusa koda kļūdas atbildes lapas, kam iestatāt novirzīšanu. Šie aizstājvārdi ir jāpublicē. Pretējā gadījumā novirzīšana nedarbosies.
1. Atlasiet **Labi**, lai izpildītu saistīšanu.

> [!NOTE]
> Ja izmantojat vienu statusa koda kļūdas atbildes lapu abām kļūdu kategorijām, atkārtojiet šo procedūru, lai ar to pašu lapu saistītu aizstājvārdu citai kļūdas kategorijai.

## <a name="additional-resources"></a>Papildu resursi

[Darbs ar veidnēm](work-with-templates.md)

[Jaunas vietnes lapas pievienošana](add-new-page.md)

[Lapas vietrāža URL izveide](create-page-url.md)
