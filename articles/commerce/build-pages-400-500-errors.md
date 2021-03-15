---
title: Pielāgotu atbilžu lapu izveide 4xx/5xx statusa koda kļūdām
description: Šajā tēmā ir aprakstīts, kā izveidot pielāgotas atbilžu lapas 4xx un 5xx statusa koda kļūdām, izmantojot autorēšanas rīkus programmā Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d21ce20b2c7ac8c656a718749dabd76f33893da8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991469"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a>Pielāgotu atbilžu lapu izveide 4xx/5xx statusa koda kļūdām


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

1. Dodieties uz **Veidnes**.
1. Atlasiet **Jauns**, lai izveidotu lapas veidni.
1. Dialoglodziņā **Jauna veidne** zem **Veidnes nosaukuma** ievadiet jaunās veidnes nosaukumu un pēc tam atlasiet **Labi**.
1. Izveidojiet veidni, pamatojoties uz struktūru, ko vēlaties izmantot statusa koda kļūdas atbildes lapā.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu veidnē, un pēc tam atlasiet **Publicēt**, lai publicētu to. 

### <a name="build-the-status-code-error-response-page"></a>Statusa koda kļūdas atbildes lapas izveide

Lai izveidotu statusa koda kļūdas atbildes lapu, veiciet tālāk norādītās darbības.

1. Doties uz **Lapas**.
1. Atlasiet **Jauns**, lai izveidotu lapu.
1. Dialoglodziņā **Izvēlēties veidni** atlasiet veidni un pēc tam sadaļā **Lapas nosaukums** ievadiet nosaukumu statusa koda kļūdas atbildei. Atstājiet lauku **Lapas vietrādis URL** tukšu.
1. Veidojiet lapu.
1. Atlasiet **Saglabāt**, atlasiet **Pabeigt rediģēšanu**, lai to pārbaudītu lapā, un pēc tam atlasiet **Publicēt**, lai publicētu to.

> [!NOTE]
> Varat izveidot atsevišķas statusa koda kļūdas atbildes lapas 4xx un 5xx statusa koda kļūdām. Alternatīvi varat izmantot vienu un to pašu vispārīgā statusa koda kļūdas atbildes lapu abām kļūdu kategorijām.

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a>Novirzīšanas iestatīšana statusa koda kļūdas atbildes lapai

Lai iestatītu novirzīšanu statusa koda kļūdas atbildes lapai, veiciet tālāk norādītās darbības.

1. Dodieties uz **vietrāži URL \> Jauns \> Jauns aizstājvārds** un atlasiet iepriekš izveidoto statusa koda kļūdas atbildes lapu.
1. Laukā **Aizstājvārds** ievadiet vai nu **default-4xx**, vai **default-5xx**, atkarībā no statusa koda kļūdas atbildes lapas, kam iestatāt novirzīšanu. Šie aizstājvārdi ir jāpublicē. Pretējā gadījumā novirzīšana nedarbosies.
1. Atlasiet **Labi**, lai izpildītu saistīšanu.

> [!NOTE]
> Ja izmantojat vienu statusa koda kļūdas atbildes lapu abām kļūdu kategorijām, atkārtojiet šo procedūru, lai ar to pašu lapu saistītu aizstājvārdu citai kļūdas kategorijai.

## <a name="additional-resources"></a>Papildu resursi

[Darbs ar veidnēm](work-with-templates.md)

[Jaunas vietnes lapas pievienošana](add-new-page.md)

[Lapas vietrāža URL izveide](create-page-url.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]