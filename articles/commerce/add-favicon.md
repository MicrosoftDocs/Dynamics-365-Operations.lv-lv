---
title: Izlases ikonas pievienošana
description: Šajā tēmā ir paskaidrots, kā pievienot izlases ikonu jūsu vietnei.
author: bicyclingfool
manager: annbe
ms.date: 08/31/2020
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 262e478d426fd913130b21a3434331c7d27b54b2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413984"
---
# <a name="add-a-favicon"></a>Izlases ikonas pievienošana

[!include [banner](includes/banner.md)]

Šajā tēmā ir paskaidrots, kā pievienot izlases ikonu jūsu vietnei.

## <a name="overview"></a>Pārskats

Izlases ikona ir neliels grafiskais fails, kas tiek attēlots tīmekļa pārlūkprogrammas cilnē, adreses joslā, pārlūkošanas vēsturē un grāmatzīmēs vai izlasē, kā arī citās vietās. Mēs iesakām jums pievienot izlases ikonu jūsu vietnei, jo tā pārstāv un nostiprina jūsu zīmolu, kā arī palīdz atšķirt jūsu vietni no citām jūsu klientu apmeklētajām vietnēm.

Lai gan jūs varat pievienot vairākas dažādu izmēru un failu tipu izlases ikonas jūsu vietnē, šajā tēmā ir aprakstīts, kā pievienot vienu izlases ikonu. Tomēr tas pats process un atrašanās vieta tiek izmantoti, lai pievienotu vairāk izlases ikonu.

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a>Izlases ikonas augšupielāde jūsu vietnes līdzekļu kolekcijā

Lai pievienotu izlases ikonu jūsu vietnes līdzekļu kolekcijā, veiciet šādas darbības.

1. Kreisās puses navigācijas rūtī atlasiet **Mediju bibliotēka**.
1. Komandu joslā atlasiet **Augšupielādēt \> Augšupielādēt mediju vienumus**.
1. Failu pārlūka logā pārlūkojiet izlases attēla failu, kuru vēlaties augšupielādēt, atlasiet to un pēc tam atlasiet **Atvērt**.
1. Dialoglodziņā **Augšupielādēt multivides vienumu** ievadiet nepieciešamo nosaukumu un alternatīvo tekstu.
1. Ja vēlaties publicēt attēlu tūlīt pēc augšupielādes, atzīmējiet izvēles rūtiņu **Publicēt multivides vienumus pēc augšupielādes**.

    > [!NOTE]
    > Ja neizvēlaties izvēles rūtiņu **Publicēt multivides vienumus pēc augšupielādes**, atgriezieties pie lapas **Multivides vienumi** un manuāli publicējiet izlases ikonu vēlāk.

1. Atlasiet **Labi**.
1. Rekvizītu rūtī labajā pusē nokopējiet izlases ikonas publisko vietrādi URL. Šo vietrādi URL izmantosiet vēlāk.

## <a name="create-the-html-for-your-favicon"></a>HTML izveide jūsu izlases ikonai

Lai izveidotu HTML izlases ikonai, izmantojiet šādu HTML virkni. **href** atribūtam aizvietojiet **Public\_URL\_for\_your\_favicon** ar publisku vietrādi URL, ko kopējāt agrāk.

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="create-a-fragment-that-contains-a-metatag-for-your-favicon"></a>Izveidot fragmentu, kas satur metatagu jūsu favicon

Lai izveidotu fragmentu, kas satur metatagu jūsu favicon, sekojiet šiem soļiem.

1. Dodieties uz **Fragmenti** un atlasiet **Jauns**.
1. Dialoglodziņā **Jauns fragments** atlasiet **Metatagi** kā moduli, uz kā balstās fragments.
1. Ievadiet fragmenta nosaukumu un pēc tam atlasiet **Labi**.
1. Fragmentu hierarhijas kokā atlasiet **Noklusējuma metatagi** elementu.
1. Labajā rūtī zem sadaļas **Metatagi** atlasiet **Pievienot** un pēc tam ievadiet HTML virkni, ko iepriekš izveidojāt izlases ikonai. 
1. Atlasiet **Pabeigt rediģēšanu** un pēc tam atlasiet **Publicēt**, lai publicētu fragmentu.

## <a name="add-the-metatag-fragment-to-the-html-head-section-of-your-pages"></a>Pievienot metataga fragmentu jūsu lapu HTML galvenei

Lai pievienotu metataga fragmentu jūsu lapu HTML **galvenei**, sekojiet šiem soļiem.

1. Dodieties uz **Veidnes**, atveriet veidni lapām, kurām vēlaties pievienot izlases ikonu, un tad atlasiet **Rediģēt**.
1. Veidnes hierarhijas kokā atlasiet daudzpunktes (**...**) pogu pa labi no **HTML galvenes** konteinera un pēc tam atlasiet **Pievienot fragmentu**.
1. Dialoglodziņā **Atlasīt fragmentu** atlasiet iepriekš izveidoto metataga fragmentu un pēc tam atlasiet **Labi**.
1. Atlasiet **Pabeigt rediģēšanu** un pēc tam atlasiet **Publicēt**, lai publicētu veidni.

> [!NOTE]
> Ja jūsu vietne izmanto vairāk nekā vienu veidni, jums ir jāpievieno metatagu fragments tiem visiem.

Priekšskatot lapas, kas ir balstītas uz veidni, kurai pievienojāt metatagu fragmentu, jums vajadzētu ieraudzīt izlases ikonu pārlūka cilnē.

## <a name="additional-resources"></a>Papildu resursi

[Logotipa pievienošana](add-logo.md)

[Vietnes dizaina atlase](select-site-theme.md)

[Darbs ar CSS ignorēšanas failiem](css-override-files.md)

[Sveiciena ziņojuma pievienošana](add-welcome-message.md)

[Autortiesību paziņojuma pievienošana](add-copyright-notice.md)

[Valodu pievienošana vietnei](add-languages-to-site.md)

[Skripta koda pievienošana vietnes lapām, lai atbalstītu telemetriju](add-telemetry.md)

