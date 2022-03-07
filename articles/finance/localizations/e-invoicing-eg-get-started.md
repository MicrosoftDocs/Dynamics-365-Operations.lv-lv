---
title: Darba sākšana ar elektroniskās rēķinu izveides pievienojumprogrammu lietošanai Ēģiptē
description: Šajā tēmā ir sniegta informācija, kas palīdzēs sākt darbu ar elektronisko rēķinu pievienojumprogrammu Ēģiptei programmās Finance un Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 02/26/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 68ee08226f440e850a080600dbf5e16768b45e43
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592602"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-egypt"></a>Darba sākšana ar elektroniskās rēķinu izveides pievienojumprogrammu lietošanai Ēģiptē

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Šajā tēmā ir sniegta informācija, kas palīdzēs sākt darbu ar elektronisko rēķinu pievienojumprogrammu Ēģiptei. Šajā tēmā ir aprakstītas konfigurācijas darbības, kas ir atkarīgas no Regulatory Configuration Services (RCS), un ir papildinātas darbības, kas aprakstītas sadaļā [Sākt datrbu ar Elektronisko rēķinu izrakstīšanas pievienojumprogrammu](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>Valstij specifiska konfigurācija Ēģiptes elektroniskā rēķina (EG) Elektronisko rēķinu izrakstīšanas līdzeklim

Lai konfigurētu Ēģiptes elektroniskā rēķina (EG) Elektronisko rēķinu izrakstīšanas līdzekli, ir jāveic dažas darbības. Daži no konfigurāciju parametriem tiek publicēti ar noklusējuma vērtībām, tāpēc tie ir jāpārskata un jāatjaunina, lai labāk atbilstu jūsu biznesa operācijai.

### <a name="prerequisites"></a>Priekšnosacījumi

Lai veiktu šo procedūru šajā sadaļā, jums ir jāizdara tālāk minētais.

- Izveidojiet ciparsertifikāta noslēpumu, kā aprakstīts sadaļā **Izveidot ciparsertifikāta noslēpumu** [Sākt darbu ar Elektronisko rēķinu izrakstīšanas pievienojumprogrammas pakalpojuma administrēšanu](e-invoicing-get-started-service-administration.md). Testēšanas nolūkos Ēģiptes nodokļu iestāde nodrošina konkrētus testa ciparsertifikātus, kas jāizmanto tikai testēšanas un risinājuma apstiprināšanas posmu laikā. Lai iegūtu plašāku informāciju, skatiet Ēģiptes nodokļu iestādes tīmekļa vietni, izmantojot saiti, kas norādīta [Ēģiptes e-rēķinu izrakstīšanas SDK](https://sdk.sit.invoicing.eta.gov.eg/faq/).
- Izveidojiet Ēģiptes elektronisko rēķinu (DB) Elektronisko rēķinu izrakstīšanas līdzekli jūsu organizācijai, kā aprakstīts sadaļā **Izveidot elektronisko rēķinu izrakstīšanu zem savas organizācijas nodrošinātāja** [Sākt darbu ar Elektronisko rēķinu izrakstīšanas pievienojumprogrammu](e-invoicing-get-started.md).

1. Darbvietas **Globalizācijas līdzekļi** sadaļas **Līdzekļi** RCS atlasiet elementu **Elektronisko rēķinu izrakstīšanas pievienojumprogramma**.
2. Lapā **Elektronisko rēķinu izrakstīšanas pievienojumprogrammas līdzekļi** pārbaudiet, vai ir atlasīts jūsu izveidotais **Ēģiptes elektroniskā rēķina (EG)** elektronisko rēķinu izrakstīšanas līdzeklis.
3. Cilnē **Versijas** pārbaudiet, vai ir atlasīta versija **Melnraksts**.
4. Cilnē **Iestatījumi** režģī atlasiet līdzekļa **Pārdošanas rēķins** iestatījumu.
5. Atlasiet **Rediģēt** un cilnes **Darbības** lauka grupā **Darbības** atlasiet **Parakstīt json dokumentu Ēģiptes nodokļu iestādei**.
6. Lauku grupā **Parametri** atlasiet parametru **Sertifikāta nosaukums** un atlasiet tā ciparsertifikāla nosaukumu, kas izveidots izmantošanai ar elektronisko rēķinu izrakstīšanas līdzekli.
7. Lauku grupā **Darbības** atlasiet **Integrēt ar Ēģiptes ETA pakalpojumu**. Atkārtojiet šo darbību abiem šīs darbības gadījumiem.
8. Lauku grupā **Parametri** atlasiet **Tīmekļa pakalpojuma vietrādi URL** un **Pieteikšanās pakalpojuma vietrādi URL** un vajadzības gadījumā pārskatiet vietrāža URL parametrus. Lai iegūtu testēsanas un ražošanas vietrādi URL, skatiet Ēģiptes nodokļu iestādes tīmekļa vietni, izmantojot saiti, kas norādīta [Ēģiptes e-rēķinu izrakstīšanas SDK](https://sdk.sit.invoicing.eta.gov.eg/faq/).
9. Atlasiet **Saglabāt** un aizveriet lapu.
10. Lai konfigurētu programmas iestatījumus, skatiet sadaļu [Sākt darbu ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu](e-invoicing-get-started.md).

## <a name="country-specific-configuration-of-the-application-setup-for-the-egyptian-electronic-invoice-eg-electronic-invoicing-feature"></a>Valstij specifiskās programmas iestatījuma konfigurācija Ēģiptes elektroniskā rēķina (EG) Elektronisko rēķinu izrakstīšanas līdzeklim

Programmas iestatījuma konfigurācijai **Ēģiptes elektroniskā rēķina (EG)** Elektronisko rēķinu izrakstīšanas līdzeklim ir jāizpilda konkrētas darbības. Šīs darbības jāveic pirms Elektronisko rēķinu izrakstīšanas līdzekļa izvietošanas jūsu Elektronisko rēķinu izrakstīšanas pakalpojuma vidē.

### <a name="prerequisites"></a>Priekšnosacījumi

Pirms izpildāt šajā sadaļā noteikto procedūru, izveidojiet un aktivizējiet **Ēģiptes elektroniskā rēķina (EG)** Elektroniskā rēķina izrakstīšanas līdzekli, lai konfigurētu programmas iestatījumu **Ēģiptes elektroniskā rēķina (EG)** Elektroniskā rēķina izrakstīšanas līdzeklim, kā aprakstīts sadaļā **Programmas iestatījuma konfigurēšana** tēmā [Darba sākšana ar Elektroniskā rēķina izrakstīšanas pievienojumprogrammu](e-invoicing-get-started.md).

1. Darbvietas **Globalizācijas līdzekļi** sadaļas **Līdzekļi** RCS atlasiet elementu **Elektronisko rēķinu izrakstīšanas pievienojumprogramma**.
2. Lapā **Elektronisko rēķinu izrakstīšanas pievienojumprogrammas līdzekļi** pārbaudiet, vai ir atlasīts **Ēģiptes elektroniskā rēķina (EG)** elektronisko rēķinu izrakstīšanas līdzeklis.
3. Cilnē **Versijas** pārbaudiet, vai ir atlasīta versija **Melnraksts** .
4. Cilnē **Iestatījumi** atlasiet **Programmas iestatījumi** un laukā **Savienotā programma** atlasiet programmu, kurā vēlaties izvietot.
5. Laukā **Tabulas nosaukums** pārbaudiet, vai ir atlasīts debitora rēķinu žurnāls.
6. Atlasiet **Atbilžu veidi** un pēc tam atlasiet **Jauns**.
7. Laukā **Atbilžu veidi** ievadiet "Atbilde" un laukā **Apraksts** ievadiet "Apraksts".
8. Laukā **Iesniegšanas statuss** atlasiet **Neizlemts**.
9. Laukā **Modeļa kartēšana** atlasiet **Modeļa kartēšana no atbildes ziņojuma** ar **(Priekšskatījumu) Atbildes ziņojuma importēšanas formāts** un pēc tam atlasiet **Saglabāt**.
10. Atlasiet **Jauns** un laukā **Atbilžu veids** fievadiet "ResponseData" kā fiksētu vērtību. Ievadiet "Apraksts" laukā **Apraksts**.
11. Laukā **Iesniegšanas statuss** atlasiet **Neizlemts**.
12. Laukā **Datu elementa nosaukums** atlasiet **Pārdošanas rēķina virsraksti V2**.
13. Laukā **Modeļa kartēšana** atlasiet **Ēģiptes atbildes datu imports** ar **(Priekšskatījumu) Ēģiptes atbildes datu imports** un pēc tam atlasiet **Saglabāt**.
14. Lai izvietotu Elektronisko rēķinu izrakstīšanas līdzekli, skatiet sadaļu [Sākt darbu ar Elektronisko rēķinu izrakstīšanas pievienojumprogrammu](e-invoicing-get-started.md).

## <a name="privacy-notice"></a>Paziņojums par konfidencialitāti

Iespējojot līdzekli **Ēģiptes elektroniskais rēķins (EG)**, var būt nepieciešams nosūtīt ierobežotus datus, tostarp organizācijas nodokļa reģistrācijas ID. Šie dati tiks nosūtīti trešo personu aģentūrām, ko pilnvarojusi nodokļu iestāde nolūkā nosūtīt elektroniskos rēķinus šai nodokļu iestādei iepriekš noteiktā formātā, kas nepieciešams integrācijai ar valdības tīmekļa pakalpojumu. Administrators var iespējot un atspējot līdzekli, naviģējot uz **Organizācijas administrēšana** > **Iestatījumi** > **Elektroniskā dokumenta parametri**. Cilnē **Līdzekļi** atlasiet rindu, kurā ir **Ēģiptes elektroniskā rēķina (EG)** līdzeklis, un pēc tam veiciet attiecīgo atlasi. No šīm ārējām sistēmām importētie dati šajā Dynamics 365 tiešsaistes pakalpojumā ir pakļauti mūsu [paziņojumam par privātumu](https://go.microsoft.com/fwlink/?LinkId=512132). Lai iegūtu plašāku informāciju, skatiet sadaļas Konfidencialitātes paziņojums valstij raksturīgā līdzekļa dokumentācijā.

## <a name="additional-resources"></a>Papildu resursi

- [Elektroniskās rēķinu izveides pievienojumprogrammas pārskats](e-invoicing-service-overview.md)
- [Darba sākšana ar elektroniskās rēķinu izveides pievienojumprogrammas servisa administrēšanu](e-invoicing-get-started-service-administration.md)
- [Darba sākšana ar elektroniskās rēķinu izveides pievienojumprogrammu](e-invoicing-get-started.md)
- [Klientu elektroniskie rēķini Ēģiptē](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
