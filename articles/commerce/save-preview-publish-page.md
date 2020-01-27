---
title: Lapas saglabāšana, priekšskatīšana un publicēšana
description: Šajā tēmā aprakstīts, kā saglabāt, priekšskatīt un publicēt lapu Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3fff8299ecc6833890b14fa421501236830b2c61
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945678"
---
# <a name="save-preview-and-publish-a-page"></a>Lapas saglabāšana, priekšskatīšana un publicēšana

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šajā tēmā aprakstīts, kā saglabāt, priekšskatīt un publicēt lapu Microsoft Dynamics 365 Commerce.

## <a name="save-a-page"></a>Lapas saglabāšana

Lai saglabātu lapu, jums tā ir jāizraksta sev un jāatver lapas redaktorā. Lapa jāsaglabā uzreiz pēc tās modificēšanas, lai palīdzētu nodrošināt, ka izmaiņas tiek saglabātas.

Saglabājot lapu, izmaiņas ir redzamas tikai jums. Saglabāšanas operācija galvenokārt ir paredzēta, lai saglabātu izmaiņas, kamēr lapa vēl nav gatava reģistrācijai. Kad lapas modificēšana ir pabeigta, ieteicams to reģistrēt, lai izmaiņas kļūtu redzamas citiem. Šajā brīdī lapu var izrakstīt arī citi lietotāji, kuriem tā jāmodificē.

## <a name="preview-a-page"></a>Lapas priekšskatīšana

Autorēšanas rīks piedāvā divu veidu priekšskatījuma līdzekļus: "redzat to, ko iegūstat" (WYSIWYG) priekšskatījuma rūti lapas redaktorā un atsevišķu priekšskatījuma logu.

Lietojot lapas redaktoru, priekšskatījums "redzat to, ko iegūstat" (WYSIWYG) parādās centrālajā rūtī. Šis priekšskatījums tiek automātiski atjaunināts ikreiz, kad saglabājat lapu. Varat to atjaunināt arī manuāli, komandjoslā atlasot **Atsvaidzināt**. WYSIWYG priekšskatījums atveido lapu tā, kā to redzēs vietnes lietotāji, bet autorēšanas palīgi tiek atveidoti tam pa virsu.

Kad lapas modificēšana ir pabeigta, iespējams, vēlēsieties to priekšskatīt, lai redzētu, ko redzēs klienti. Lai priekšskatītu lapu, komandjoslā atlasiet **Priekšskatījums**. Priekšskatījums parādīsies atsevišķā pārlūkprogrammas logā. Priekšskatījuma logā lapa tiek atveidota tā, kā to redzēs vietnes lietotājs. Varat mainīt loga izmērus, lai pārliecinātos, ka reaģējošie moduļi ir pareizi attēloti visos skatījuma portos.

> [!NOTE]
> Lai priekšskatītu nepublicētu saturu, nepieciešama autentifikācija un pareizās atļaujas. Tāpēc, ja kopīgojat priekšskatījuma URL ar kādu personu, šai personai ir jābūt pareizajām atļaujām, lai piekļūtu saturam.

## <a name="publish-a-page"></a>Lapas publicēšana

Kad lapa ir gatava, nākamā darbība ir to publicēt, lai ārējie lietotāji varētu apskatīt saturu. Pirms lapas publicēšanas tā jāreģistrē.

Lapas varat publicēt un atsaukt publicēšanu vai nu no lapas kontroliera, vai lapas redaktora. Lapas kontrolieris parāda lapu sarakstu un ļauj veikt liela apjoma operācijas. Lapas redaktoru var izmantot, lai publicētu vai atsauktu publicēšanu vienai lapai, kas tajā atvērta.

Lai no lapas kontroliera publicētu vienu vai vairākas lapas, atlasiet lapas, pārliecinieties, ka tās ir reģistrētas, un pēc tam komandjoslā atlasiet **Publicēt**. Lapas tiek publicētas, un jūs saņemat paziņojumu par operāciju autorēšanas rīkā.

Lai publicētu vienu lapu no lapas redaktora, procedūra ir līdzīga. Kamēr lapa ir atvērta lapas redaktorā, pārliecinieties, vai tā ir reģistrēta, un pēc tam komandjoslā atlasiet **Publicēt**. Lapa tiek publicēta, un jūs saņemat paziņojumu par operāciju.

Publicējot lapu, tiek publicēts tikai lapas saturs. Jūs un citi lietotāji var doties uz lapu un skatīt to tikai pēc tam, kad ar to ir saistīts URL. URL ir jāpublicē atsevišķi.

> [!IMPORTANT]
> Pirms jūs varat publicēt lapu, visiem attēliem vai fragmentiem, uz ko lapa atsaucas, jau jābūt publicētiem.

## <a name="save-preview-and-publish-a-home-page"></a>Sākumlapas saglabāšana, priekšskatīšana un publicēšana

Lai saglabātu, priekšskatītu un publicētu sākumlapu, veiciet tālāk minētās darbības.

1. Sadaļā **Vietnes** atlasiet **Fabrikam** (vai savas vietnes nosaukumu).
1. Navigācijas rūtī kreisajā pusē atlasiet **Lapas**.
1. Atrodiet un atlasiet sākumlapu, lai to atvērtu to lapas redaktorā.
1. Atlasiet **Izrakstīt**.
1. Modificējiet lapu, kā nepieciešams.
1. Atlasiet **Saglabāt** un pēc tam **Pārbaudīt**.
1. Laukā **Komentāri** Ievadiet piezīmi par veiktajām izmaiņām un pēc tam atlasiet **Labi**.
1. Atlasiet **Priekšskatījums**, lai priekšskatītu lapu. Kad esat pabeidzis, aizveriet priekšskatījuma cilni, lai atgrieztos autorēšanas rīkā.
1. Atlasiet **Publicēt**.

## <a name="publish-a-url"></a>URL publicēšana

Lai publicētu URL, veiciet tālāk minētās darbības.

1. Sadaļā **Vietnes** atlasiet **Fabrikam** (vai savas vietnes nosaukumu).
1. Navigācijas rūtī kreisajā pusē atlasiet **Vietrāži URL**.
1. Atrodiet un atlasiet publicējamo URL.
1. Komandjoslā atlasiet **Publicēt**.

## <a name="additional-resources"></a>Papildu resursi

[Esošās vietnes lapas modificēšana](modify-existing-page.md)

[Jaunas vietnes lapas pievienošana](add-new-page.md)

[Lapas izkārtojumu atlase](select-page-layouts.md)

[SEO metadatu pārvaldība](manage-seo-metadata.md)

[Preces lapas papildināšana](enrich-product-page.md)

[Kategorijas ielādes lapas papildināšana](enrich-category-page.md)

[Lapas satura pieejamības pārbaude](verify-accessibility.md)
