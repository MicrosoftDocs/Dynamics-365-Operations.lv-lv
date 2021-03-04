---
title: Failu robots.txt pārvaldība
description: Šajā tēmā aprakstīts, kā pārvaldīt Microsoft Dynamics 365 Commerce robots.txt failus.
author: BrianShook
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: ad87594b9c20d0c2b53e8d4e7c1170a78babe74b
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517456"
---
# <a name="manage-robotstxt-files"></a>Failu robots.txt pārvaldība


[!include [banner](includes/banner.md)]

Šajā tēmā aprakstīts, kā pārvaldīt Microsoft Dynamics 365 Commerce robots.txt failus.

## <a name="overview"></a>Pārskats

Robotu izslēgšanas standarts jeb robots.txt ir standarts, kuru tīmekļa vietnes izmanto, lai sazinātos ar tīmekļa robotiem. Tas instruē tīmekļa robotus par jebkuru mājas lapas apgabalu, kuru nedrīkst apmeklēt. Robotus bieži izmanto meklētājprogrammas, lai apzīmētu tīmekļa vietnes.

Lai izslēgtu robotus no servera, izveidojiet failu serverī. Šajā failā jūs norādāt robotu piekļuves politiku. Failam jābūt pieejamam, izmantojot HTTP lokālo URL **/robots.txt.** robots.txt fails palīdz meklētājprogrammām indeksēt saturu jūsu vietnē.

Dynamics 365 Commerce ļauj augšupielādēt failu robots.txt jūsu domēnam. Katram domēnam jūsu Commerce vidē varat augšupielādēt vienu robots.txt failu un saistīt to ar šo domēnu.

Lai iegūtu papildinformāciju par failu robots.txt, apmeklējiet [Tīmekļa robotu lapas](https://www.robotstxt.org/)

## <a name="upload-a-robotstxt-file"></a>Faila robots.txt augšupielāde

Pēc tam, kad esat izveidojis un rediģējis failu robots.txt saskaņā ar [robotu izslēgšanas standartu](https://www.robotstxt.org/orig.html), pārliecinieties, vai fails ir pieejams datorā, kurā izmantosiet tirdzniecības autorēšanas rīkus. Faila nosaukumam ir jābūt **robots.txt**. Lai iegūtu vislabākos rezultātus, tam jābūt formātā, kas norādīts standartā. Katrs Commerce klients ir atbildīgs par tā robots.txt faila satura apstiprināšanu un uzturēšanu. Lai augšupielādētu robots.txt failu, jums ir jāpierakstās Commerce kā sistēmas administratoram.

Lai Commerce vietnē augšupielādētu robots.txt failu, veiciet tālāk norādītās darbības.

1. Pierakstieties Commerce kā sistēmas administrators.
2. Kreisās puses navigācijas rūtī atlasiet **Nomnieka iestatījumi** (blakus zobrata simbolam), lai to izvērstu.
3. Sadaļā **Nomnieka iestatījumi** atlasiet **Robots.txt**. Galvenajā loga daļā tiek parādīts visu ar vidi saistīto domēnu saraksts.
4. Atlasiet **Pārvaldīt**, lai augšupielādētu failu robots.txt domēnam jūsu vidē.
5. Labajā pusē esošajā izvēlnē atlasiet pogu **Augšupielādēt** (augšupvērstā bultiņa) blakus domēnam, kas ir saistīts ar failu robots.txt. Tiek parādīts failu pārlūka dialoglodziņš.
6. Dialoglodziņā pārlūkojiet un atlasiet failu robots.txt, kuru vēlaties augšupielādēt saistītajam domēnam, un pēc tam atlasiet **Atvērt**, lai pabeigtu augšupielādi.

> [!NOTE] 
> Augšupielādes laikā Commerce pārbauda, vai fails ir teksta fails, bet tas neapliecina faila saturu.

## <a name="download-a-robotstxt-file"></a>Faila robots.txt lejupielāde

Lai Commerce vietnē lejupielādētu robots.txt failu, veiciet tālāk norādītās darbības.

1. Pierakstieties Commerce kā sistēmas administrators.
2. Kreisās puses navigācijas rūtī atlasiet **Nomnieka iestatījumi** (blakus zobrata simbolam), lai to izvērstu.
3. Sadaļā **Nomnieka iestatījumi** atlasiet **Robots.txt**. Galvenajā loga daļā tiek parādīts visu ar vidi saistīto domēnu saraksts.
4. Atlasiet **Pārvaldīt**, lai lejupielādētu failu robots.txt domēnam jūsu vidē.
5. Labajā pusē esošajā izvēlnē atlasiet pogu **Lejupielādēt** (lejupvērstā bultiņa) blakus domēnam, kas ir saistīts ar failu robots.txt. Tiek parādīts failu pārlūka dialoglodziņš.
6. Dialoglodziņā pārejiet uz vēlamo atrašanās vietu lokālajā diskā, apstipriniet vai ievadiet faila nosaukumu un pēc tam atlasiet **Saglabāt**, lai pabeigtu lejupielādi.

> [!NOTE]
> Šo procedūru var izmantot, lai lejupielādētu tikai failus robots.txt, kas iepriekš tika augšupielādēti, izmantojot Commerce autorēšanas rīkus.

## <a name="delete-a-robotstxt-file"></a>Faila robots.txt dzēšana

Lai Commerce vietnē dzēstu robots.txt failu, veiciet tālāk norādītās darbības.

1. Pierakstieties Commerce kā sistēmas administrators.
2. Kreisās puses navigācijas rūtī atlasiet **Nomnieka iestatījumi** (blakus zobrata simbolam), lai to izvērstu.
3. Sadaļā **Nomnieka iestatījumi** atlasiet **Robots.txt**. Galvenajā loga daļā tiek parādīts visu ar vidi saistīto domēnu saraksts.
4. Atlasiet **Pārvaldīt**, lai dzēstu failu robots.txt domēnam jūsu vidē.
5. Labajā pusē esošajā izvēlnē atlasiet pogu **Dzēst** (atkritumu urnas simbols) blakus domēnam, kas ir saistīts ar failu robots.txt. Tiek parādīts failu pārlūka logs.
6. Faila pārlūka logā pārlūkojiet un atlasiet failu robots.txt, kuru vēlaties dzēst saistītajam domēnam, un pēc tam atlasiet **Atvērt**. Tiek parādīts brīdinājuma ziņojuma lodziņš.
7. Ziņojuma lodziņā atlasiet **Dzēst**, lai apstiprinātu faila robots.txt dzēšanu.

> [!NOTE] 
> Šo procedūru var izmantot, lai dzēstu tikai failus robots.txt, kas iepriekš tika augšupielādēti, izmantojot Commerce autorēšanas rīkus.

## <a name="additional-resources"></a>Papildu resursi

[Domēna nosaukuma konfigurēšana](configure-your-domain-name.md)

[Jauna e-tirdzniecības nomnieka izvietošana](deploy-ecommerce-site.md)

[E-komercijas vietnes izveide](create-ecommerce-site.md)

[Vietnes Dynamics 365 Commerce saistīšana ar tiešsaistes kanālu](associate-site-online-store.md)

[Novirzīšanas URL lielapjoma augšupielāde](upload-bulk-redirects.md)

[B2C nomnieka iestatīšana programmā Commerce](set-up-B2C-tenant.md)

[Pielāgotu lapu iestatīšana lietotāja pieteikumiem](custom-pages-user-logins.md)

[Vairāku B2C nomnieku konfigurēšana Commerce vidē](configure-multi-B2C-tenants.md)

[Atbalsta pievienošana satura piegādes tīklam (CDN)](add-cdn-support.md)

[Veikala noteikšanas iespējošana pēc atrašanās vietas](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]