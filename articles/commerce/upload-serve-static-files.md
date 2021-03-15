---
title: Augšupielādēt un apkalpot statiskos failus
description: Šajā tēmā ir aprakstīts, kā augšupielādēt statisku failu Microsoft Dynamics 365 Commerce vietnes veidotājā un kā izveidot pielāgotu vietrādi URL un faila nosaukumu, ko var izmantot, lai pieprasītu šo failu.
author: StuHarg
manager: annbe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 1d709d99737ad05af1fb19d9f3ef7b87a8db80d3
ms.sourcegitcommit: da17648c296b22d517eadb2f71c7803672e5648d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031824"
---
# <a name="upload-and-serve-static-files"></a>Augšupielādēt un apkalpot statiskos failus

[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīts, kā augšupielādēt statisku failu Microsoft Dynamics 365 Commerce vietnes veidotājā un kā izveidot pielāgotu vietrādi URL un faila nosaukumu, ko var izmantot, lai pieprasītu šo failu.

Daži trešās puses savienotāji pieprasa, lai fails tiktu viesots un apkalpots no e-komercijas vietnes. Šie savienotāji sagaida, ka fails tiks atgriezts pēc pieprasījumiem uz konkrētu atzvanīšanas vietrāža URL ceļu un faila nosaukumu. Tāpēc šajā tēmā ir paskaidrots, kā augšupielādēt un apkalpot statisku failu, kam ir lietotāja definējams vietrādis URL un faila nosaukums Dynamics 365 Commerce e-komercijas vietnē.

## <a name="create-a-site-url-that-returns-a-static-file"></a>Izveidot vietnes vietrādi URL, kas atgriež statisku failu

Lai izveidotu vietnes vietrādi URL, kas atgriež statisku failu Commerce vietnes veidotājā, veiciet tālāk norādītās darbības.

1. Dodieties uz savas vietnes multivides bibliotēku un augšupielādējiet failu, kas jāapkalpo, izmantojot pieprasījumus uz vietrādi URL, kuru definēsit. Ja fails jau ir augšupielādēts, varat izlaist šo darbību.
1. Dodieties uz savas vietnes **URL**.
1. Atlasiet **Jauns \> Jauns URL**.
1. Dialoglodziņā **Jauns URL** atlasiet **Multivides bibliotēkas līdzeklis**.
1. Laukā **URL ceļš** ievadiet vietrāža URL ceļu. Ceļā iekļaujiet faila nosaukumu.
1. Atlasiet **Nākamais**. Tiek atvērta multivides bibliotēka, un tajā ir parādīti visi **dokumenta** veida augšupielādētie multivides līdzekļi.
1. Atlasiet failu, kas ir jānodod pieprasījumiem uz vietrādi URL, kuru definējāt 5. darbībā.
1. Atlasiet **Saglabāt**.

Šajā brīdī vietrādis URL, kuru izveidojāt, ir melnraksta statusā. Fails, uz kuru URL norāda, netiks atgriezts, līdz publicēsit vietrādi URL. Pirms publicējat vietrādi URL, varat validēt, ka tiek atgriezti pareizie dati.

## <a name="validate-and-publish-a-url"></a>Vietrāža URL validācija un publicēšana

Lai validētu vietrādi URL pirms tā publicēšanas, veiciet tālāk norādītās darbības.

1. Dodieties uz savas vietnes **URL** un atlasiet vietrādi URL, ko priekšskatīt.
2. Rekvizītu rūtī labajā pusē zem pogas **Rediģēt** atlasiet pareizo vietrāža URL saiti. Tiek atvērts jauns pārlūkprogrammas logs, un jums ir jāsaņem kļūda 404.
3. Pievienojiet vaicājuma virkni **?preview=inprogress** vietrādim URL (piemēram, `https://yoursite.com/callback.html?preview=inprogress`) un pārlādējiet lapu. Failam, ko augšupielādējāt multivides bibliotēkā, jābūt atgrieztam atbildē.

Kad esat validējis vietrādi URL, varat to publicēt.

1. Dodieties uz savas vietnes **URL** un atlasiet vietrādi URL.
2. Komandjoslā atlasiet **Publicēt**.

## <a name="update-the-file-that-a-url-points-to"></a>Faila, uz kuru norāda vietrādis URL, atjaunināšana

Kad URL ir publicēts, to var atjaunināt, lai tas norādītu uz citu failu. Varat arī atjaunināt vietrādi URL, lai tas norādītu uz citu resursa veidu, kā aprakstīts nākamajā sadaļā. Piemēram, varat norādīt vietrādi URL uz iekšējo lapu vai novirzīt.

Lai atjauninātu failu, uz kuru norāda vietrādis URL, veiciet tālāk norādītās darbības.

1. Dodieties uz savas vietnes **URL** un atlasiet vietrādi URL, ko atjaunināt.
1. Rekvizītu rūts labajā pusē atlasiet **Rediģēt**.
1. Sadaļā **Vietrāža URL piešķire** atlasiet lodziņu **2. darbība** un pēc tam atlasiet jaunu dokumentu no multivides bibliotēkas.
1. Atlasiet **Lietot**.

## <a name="update-the-asset-type-that-a-url-points-to"></a>Līdzekļa veida, uz kuru norāda vietrādis URL, atjaunināšana

Varat arī atjaunināt vietrādi URL, lai tas norādītu uz citu līdzekļa veidu (resursu), piemēram, iekšējo lapu vai novirzīšanu.

Lai atjauninātu līdzekļa veidu, uz kuru norāda vietrādis URL, veiciet tālāk norādītās darbības.

1. Dodieties uz savas vietnes **URL** un atlasiet vietrādi URL, ko atjaunināt.
1. Rekvizītu rūts labajā pusē atlasiet **Rediģēt**.
1. Sadaļā **Vietrāža URL piešķire** zem **1. darbība** atlasiet citu līdzekļa veidu.
1. Atlasiet lodziņu **2. darbība** un pēc tam atlasiet jauno līdzekli.
1. Atlasiet **Lietot**.

## <a name="change-the-url-path"></a>Vietrāža URL ceļa mainīšana

Kad URL ir izveidots, tā ceļu nevar mainīt. Ja jāmaina vietrāža URL ceļš, kas kalpo failam vai kādam citam resursa veidam, ir jāizveido jauns vietrādis URL, jākartē tas uz esošo failu vai citu resursu un pēc tam jānoņem un jādzēš vecais vietrādis URL.

Lai mainītu vietrāža URL ceļu, veiciet tālāk norādītās darbības.

1. Lai izveidotu jaunu vietrādi URL un kartētu to uz esošo failu vai citu resursu, izpildiet norādes sadaļā [Izveidot vietnes vietrādi URL, kas atgriež statisku failu](#create-a-site-url-that-returns-a-static-file) iepriekš šajā tēmā.
1. Atlasiet jauno vietrādi URL un komandjoslā atlasiet **Publicēt**. Jaunais vietrādis URL ir publicēts.
1. Lai noņemtu veco vietrādi URL, atlasiet to un pēc tam komandjoslā atlasiet **Atsaukt publicēšanu**. Ja vēlaties, tagad varat dzēst veco vietrādi URL.

## <a name="additional-resources"></a>Papildu resursi

[Pārskats par digitālo līdzekļu pārvaldību](dam-overview.md)

[Attēlu augšupielāde](dam-upload-images.md)

[Augšupielādēt videoklipus](dam-upload-video.md)

[Failu, kas nav attēli un videoklipi, augšupielāde](dam-upload-files.md)

[Attēlu apgriešana](dam-crop-images.md)

[Attēlu fokusa punktu pielāgošana](dam-custom-focal-point.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]