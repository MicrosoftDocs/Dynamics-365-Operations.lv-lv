---
title: Izlases ikonas pievienošana
description: Šajā tēmā ir paskaidrots, kā pievienot izlases ikonu jūsu vietnei.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
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
ms.openlocfilehash: 287663817232e7ce86e8fdb1fb5c2fcfeed33d20
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001545"
---
# <a name="add-a-favicon"></a>Izlases ikonas pievienošana


[!include [banner](includes/banner.md)]

Šajā tēmā ir paskaidrots, kā pievienot izlases ikonu jūsu vietnei.

## <a name="overview"></a>Pārskats

Izlases ikona ir neliels grafiskais fails, kas tiek attēlots tīmekļa pārlūkprogrammas cilnē, adreses joslā, pārlūkošanas vēsturē un grāmatzīmēs vai izlasē, kā arī citās vietās. Mēs iesakām jums pievienot izlases ikonu jūsu vietnei, jo tā pārstāv un nostiprina jūsu zīmolu, kā arī palīdz atšķirt jūsu vietni no citām jūsu klientu apmeklētajām vietnēm.

Lai gan jūs varat pievienot vairākas dažādu izmēru un failu tipu izlases ikonas jūsu vietnē, šajā tēmā ir aprakstīts, kā pievienot vienu izlases ikonu. Tomēr tas pats process un atrašanās vieta tiek izmantoti, lai pievienotu vairāk izlases ikonu.

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a>Izlases ikonas augšupielāde jūsu vietnes līdzekļu kolekcijā

Lai pievienotu izlases ikonu jūsu vietnes līdzekļu kolekcijā, veiciet šādas darbības.

1. Dodieties uz **Līdzekļi \> Augšupielādēt \> Augšupielādēt līdzekļus**.
1. Atrodiet un izvēlēties izlases ikonu jūsu vietējā failu sistēmā.
1. Ievadiet nosaukumu un pēc tam atlasiet **Labi**. 
1. Rekvizītu rūtī labajā pusē nokopējiet izlases ikonas publisko vietrādi URL.

> [!NOTE]
> Ja neizvēlaties opciju **Publicēt līdzekļus pēc augšupielādes**, atgriezieties pie lapas **Līdzekļi** un manuāli publicējiet izlases ikonu vēlāk.

## <a name="create-the-html-for-the-favicon"></a>HTML izveide izlases ikonai

Lai izveidotu HTML izlases ikonai, izmantojiet šādu HTML fragmentu. **href** atribūtam aizvietojiet **“Public\_URL\_for\_your\_favicon”** ar publisku vietrādi URL, ko kopējāt agrāk.

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="add-the-html-for-the-favicon-to-the-head-element-of-your-pages"></a>HTML pievienošana izlases ikonai jūsu lapas \<galvenajā\> elementā

Lai pievienotu izlases ikonu jūsu vietnei, izmantojiet to pašu procedūru, kas tiek izmantota, lai pievienotu jebkāda veida HTML vai skriptu **\<galvenajam\>** elementam jūsu vietnes lapās.

## <a name="additional-resources"></a>Papildu resursi

[Logotipa pievienošana](add-logo.md)

[Vietnes dizaina atlase](select-site-theme.md)

[Darbs ar CSS ignorēšanas failiem](css-override-files.md)

[Sveiciena ziņojuma pievienošana](add-welcome-message.md)

[Autortiesību paziņojuma pievienošana](add-copyright-notice.md)

[Valodu pievienošana vietnei](add-languages-to-site.md)

[Skripta koda pievienošana vietnes lapām, lai atbalstītu telemetriju](add-telemetry.md)

