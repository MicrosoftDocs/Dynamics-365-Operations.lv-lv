---
title: Sākt ar elektronisko rēķinu pievienojumu Brazīlijai
description: Šajā tēmā sniegta informācija, kas jums palīdzēs sākt darbu ar elektronisko rēķinu pievienojumprogrammu Brazīlijai risinājumā Finance un Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
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
ms.openlocfilehash: eaf9433ad2d9ccf3d3c5632d0f2d4fe772ff8bde
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592674"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-brazil"></a>Sākt ar elektronisko rēķinu pievienojumu Brazīlijai 

[!include [banner](../includes/banner.md)]

Šajā tēmā izskaidrots, kā sākt darbu ar elektronisko rēķinu pievienojumporgrammu Brazīlijai. Šīs tēma procedūras iepazīstina ar konfigurēšanas darbībām, kuras ir atkarīgas no valstīm Regulatory Configuration Services (RCS) un kas papildina darbības, kas aprakstītas tēmā [Sākt darbu ar elektronisko rēķinu pievienojumprogrammu](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-brazilian-nf-e-br-electronic-invoicing-feature"></a>Valsts konfigurācijas Brazīlijas NF-e (BR) elektronisko rēķinu līdzeklim

Brazīlijas NF-e (BR) elektroniskā rēķina līdzekļa konfigurēšanai ir nepieciešams veikt konkrētas darbības. Daži no konfigurāciju parametriem tiek publicēti ar noklusējuma vērtībām, tāpēc tie ir jāpārskata un jāatjaunina, lai labāk atbilstu jūsu biznesa operācijai.

### <a name="prerequisites"></a>Priekšnosacījumi

Pirms izpildāt šajā sadaļā aprakstīto procedūru, izveidojiet savai organizācijai Brazīlijas NF-e (BR) elektroniskā rēķina līdzekli, kā aprakstīts tēmas [Sākt darbu ar elektronisko rēķinu pievienojumprogrammu](e-invoicing-get-started.md) sadaļā **Izveidojiet elektronisko rēķinu līdzekli savas organizācijas nodrošinātājam**.

1. Darbvietas **Globalizācijas līdzekļi** sadaļas **Līdzekļi** RCS atlasiet elementu **Elektronisko rēķinu izrakstīšanas pievienojumprogramma**.
2. Lapā **Elektroniskā rēķina pievienojumprogrammas līdzekļi** verificējiet, ka tiek atlasīts jūsu izveidotais elektronisko rēķinu līdzeklis **Brazīlijas NF-e (BR)**.
3. Cilnē **Versijas** pārbaudiet, vai ir atlasīta versija **Melnraksts** .
4. Režģa cilnē **Iestatījumi** atlasiet **Iesniegt** un pēc tam atlasiet **Rediģēt**.
5. Lauka grupas **Darbības** cilnē **Darbības** atlasiet darbību **(Priekšskatījums) Parakstīt XML dokumentu**.
6. Lauka grupā **Parametri** atlasiet **Sertifikāta nosaukums** un laukā **Vērtība** ievadiet ar jūsu galvenā atslēgu akreditācijas parametra sertifikātu saistīto nosaukumu.
7. Lauka grupas **Darbības** cilnē **Darbības** atlasiet darbību **(Priekšskatījums) Izsaukt Brazīlijas SEFAZ pakalpojumu**.
8. Lauka grupā **Parametri** atlasiet parametru **URL adrese**.
9. Ja nepieciešams, laukā **Vērtība** pārskatiet un atjauniniet SEFAZ dokumentācijas publicēto tīmekļa pakalpojumu URL jūsu valstij un pēc tam atlasiet **Saglabāt.**
10. Cilnē **Piemērojamības kārtulas**, lauka grupā **Piemērojamības kārtulas iestatīšana** pārskatiet un atjauniniet lauka kritēriju **Statuss**, atbilstoši tam pašam statusam, uz kuru attiecas tīmekļa pakalpojumu URL.
11. Atlasiet **Saglabāt** un aizveriet lapu.
12. Lai konfigurētu programmas iestatījumus, skatiet sadaļu [Sākt darbu ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu](e-invoicing-get-started.md).

## <a name="country-specific-configuration-of-application-setup-for-brazilian-nf-e-br-electronic-invoicing-feature"></a>Lietojumprogrammas iestatīšanas valsts konfigurācijas Brazīlijas NF-e (BR) elektronisko rēķinu līdzeklim

Lietojumprogrammas iestatīšanai Brazīlijas NF-e (BR) elektroniskā rēķina līdzekļa konfigurēšanai ir nepieciešams veikt konkrētas darbības. Izpildiet šīs darbības, pirms izvietojat elektronisko rēķinu līdzekli savā elektronisko rēķinu pievienojumprogrammas pakalpojuma vidē.

### <a name="prerequisites"></a>Priekšnosacījumi

Pirms izpildāt šajā sadaļā aprakstīto procedūru, izveidojiet un uzsāciet lietojumprogrammas konfigurēšanu savai organizācijai Brazīlijas NF-e (BR) elektroniskā rēķina līdzekli, kā aprakstīts tēmas [Sākt darbu ar elektronisko rēķinu pievienojumprogrammu](e-invoicing-get-started.md) sadaļā **Lietojumprogrammas iestatīšanas konfigurēšana**.

1. Darbvietas **Globalizācijas līdzekļi** sadaļas **Līdzekļi** RCS atlasiet elementu **Elektronisko rēķinu izrakstīšanas pievienojumprogramma**.
2. Lapā **Elektroniskā rēķina pievienojumprogrammas līdzekļi** verificējiet, ka tiek atlasīts elektronisko rēķinu līdzeklis **Brazīlijas NF-e (BR)**.
3. Cilnē **Versijas** pārbaudiet, vai ir atlasīta versija **Melnraksts** .
4. Cilnē **Iestatījumi** atlasiet **Lietojumprogrammas iestatījums** un laukā **Pievienotā lietojumprogramma** atlasiet lietojumprogrammu, kurā vēlaties izvietot.
5. Laukā **Tabulas nosaukums** pārbaudiet vai ir atlasīts lauks **Finanšu dokumenta galvene**.
6. Atlasiet **Atbilžu veidi** un pēc tam atlasiet **Jauns**.
7. Laukā **Atbildes veids** atlasiet fiksēto vērtību "Atbilde", bet laukā **Apraksts** ievadiet "Apraksts".
8. Laukā **Iesniegšanas statuss** atlasiet **Neizlemts**.
9. Laukā **Modeļa kartēšana** atlasiet **Modeļa kartēšana no atbildes ziņojumu** ar **(Priekšskatījums) Atbildes ziņojuma importēšanas formāts** un pēc tam atlasiet **Saglabāt**.
10. Atlasiet **Jauns** un laukā **Atbildes veids** fiksēto vērtību "ResponseData", bet laukā **Apraksts** ievadiet "Description".
11. Laukā **Iesniegšanas statuss** atlasiet **Neizlemts**.
12. Laukā **Modeļa kartēšana** atlasiet **Atbildes datu importēšana** ar **(Priekšskatījums) NF-e atbildes datu importēšanas formāts (BR)** un pēc tam atlasiet **Saglabāt**.
13. Lai izvietotu Elektronisko rēķinu izrakstīšanas līdzekli, skatiet sadaļu [Sākt darbu ar Elektronisko rēķinu izrakstīšanas pievienojumprogrammu](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-brazilian-nfs-e-abrasf-curitiba-br-electronic-invoicing-feature"></a>Valsts konfigurācijas Brazīlijas NFS-e ABRASF Curitiba (BR) elektronisko rēķinu līdzeklim

Brazīlijas NFS-e ABRASF Curitiba (BR) elektroniskā rēķina līdzekļa konfigurēšanai ir nepieciešams veikt konkrētas darbības. Daži no konfigurāciju parametriem tiek publicēti ar noklusējuma vērtībām, tāpēc tie ir jāpārskata un jāatjaunina, lai labāk atbilstu jūsu biznesa operācijai.

### <a name="prerequisites"></a>Priekšnosacījumi

Pirms izpildāt šajā sadaļā noteiktās darbības, savā organizācijā izveidojiet Brazīlijas NFS e-ABRASF Curitiba (BR) elektronisko rēķinu līdzekli. Tas ir aprakstīts tēmas [Sākt darbu ar elektronisko rēķinu pievienojumprogrammu](e-invoicing-get-started.md) tēmā **Elektronisko rēķinu līdzekļa konfigurēšana**.

1. Darbvietas **Globalizācijas līdzekļi** sadaļas **Līdzekļi** RCS atlasiet elementu **Elektronisko rēķinu izrakstīšanas pievienojumprogramma**.
2. Lapā **Elektroniskā rēķina pievienojumprogrammas līdzekļi** verificējiet, ka tiek atlasīts jūsu izveidotais elektronisko rēķinu līdzeklis **Brazīlijas NFS-e ABRASF (BR)**.
3. Cilnē **Versijas** pārliecinieties, ka ir atlasīta versija **Melnraksts** un cilnē **Iestatījumi** režģī atlasiet **Iesniegt**.
4. Atlasiet **Rediģēt** un cilnē **Darbības**, lauka grupā **Darbības** atlasiet pirmo **(Priekšskatījums) Parakstīt XML dokumentu**.
5. Lauka grupā **Parametri** atlasiet parametru **Sertifikāta nosaukums**.
6. Laukā **Vērtība** ievadiet ar jūsu atslēgu akreditācijas parametru saistītā sertifikāta nosaukumu.
7. Lauka grupā **Darbības** atlasiet otro **(Priekšskatījums) Parakstīt XML dokumentu**.
8. Lauka grupā **Parametri** atlasiet parametru **Sertifikāta nosaukums**.
9. Laukā **Vērtība** ievadiet ar jūsu atslēgu akreditācijas parametru saistītā sertifikāta nosaukumu.
10. Lauka grupas **Darbības** cilnē **Darbības** atlasiet darbību **(Priekšskatījums) Izsaukt Brazīlijas SEFAZ pakalpojumu**.
11. Lauka grupā **Parametri** atlasiet parametru **URL adrese**.
12. Ja nepieciešams, laukā **Vērtība** pārskatiet un atjauniniet Kuritibas pilsētas nodokļu departamenta publicēto tīmekļa pakalpojumu URL jūsu valstij un pēc tam atlasiet **Saglabāt.**
13. Režģa cilnē **Iestatījumi** atlasiet **Pieprasīt** un pēc tam atlasiet **Rediģēt**.
14. Lauka grupas **Darbības** cilnē **Darbības** atlasiet darbību **(Priekšskatījums) Izsaukt Brazīlijas SEFAZ pakalpojumu**.
15. Lauka grupā **Parametri** atlasiet parametru **URL adrese**.
16. Ja nepieciešams, laukā **Vērtība** pārskatiet un atjauniniet Kuritibas pilsētas nodokļu departamenta publicēto tīmekļa pakalpojumu URL.
17. Atlasiet **Saglabāt** un pēc tam aizveriet lapu.
18. Lai konfigurētu programmas iestatījumus, skatiet sadaļu [Sākt darbu ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu](e-invoicing-get-started.md).

## <a name="country-specific-configuration-of-application-setup-for-brazilian-nfs-e-abrasf-curitiba-br-electronic-invoicing-feature"></a>Lietojumprogrammas iestatīšanas valsts konfigurācijas Brazīlijas NFS-e ABRASF Curitiba (BR) elektronisko rēķinu līdzeklim

Lietojumprogrammas iestatīšanas konfigurēšanai Brazīlijas NFS-e ABRASF Curitiba (BR) elektronisko rēķinu līdzeklim ir nepieciešams izpildīt noteiktas darbības, pirms savu elektronisko rēķinu līdzekli izvietojat savā elektronisko rēķinu pievienojumprogrammas pakalpojuma vidē.

### <a name="prerequisites"></a>Priekšnosacījumi

Pirms izpildāt šajā sadaļā aprakstīto procedūru, izveidojiet un uzsāciet lietojumprogrammas konfigurēšanu savai organizācijai Brazīlijas NFS-e ABRAST Curitiba (BR) elektroniskā rēķina līdzekli, kā aprakstīts tēmas [Sākt darbu ar elektronisko rēķinu pievienojumprogrammu](e-invoicing-get-started.md) sadaļā **Lietojumprogrammas iestatīšanas konfigurēšana**.

1. Darbvietas **Globalizācijas līdzekļi** sadaļas **Līdzekļi** RCS atlasiet elementu **Elektronisko rēķinu izrakstīšanas pievienojumprogramma**.
2. Lapā **Elektroniskā rēķina pievienojumprogrammas līdzekļi** verificējiet, ka tiek atlasīts elektronisko rēķinu līdzeklis **Brazīlijas NFS-e ABRASF (BR)**.
3. Cilnē **Versijas** pārliecinieties, ka ir atlasīta versija **Melnraksts** un cilnē **Iestatījumi** atlasiet **Lietojumprogrammas iestatīšana**.
4. Cilnē **Pievienotā lietojumprogramma** atlasiet lietojumprogrammu, kurā vēlaties izvietot.
5. Laukā **Tabulas nosaukums** pārliecinieties, ka ir atlasīta finanšu dokumenta galvene.
6. Atlasiet **Atbilžu veidi** un atlasiet **Jauna**.
7. Laukā **Atbildes veids** atlasiet fiksēto vērtību "ABRASFCuritibaSubmitResponse", bet laukā **Apraksts** ievadiet "Description".
8. Laukā **Iesniegšanas statuss** atlasiet **Neizlemts**.
9. Laukā **Modeļa kartēšana** atlasiet **Atbildes ziņojumu importēšana** ar **(Priekšskatījums) NFS-e ABRASF Curitiba atbildes ziņojuma importēšana (BR)** un pēc tam atlasiet **Saglabāt**.
10. Atlasiet **Jauns** un laukā **Atbildes veids** fiksēto vērtību "ABRASFCuritibaSubmitResponseData", bet laukā **Apraksts** ievadiet "Description".
11. Laukā **Iesniegšanas statuss** atlasiet **Neizlemts**.
12. Laukā **Modeļa kartēšana** atlasiet **Atbildes datu importēšana** ar **(Priekšskatījums) NFS-e ABRASF atbildes datu importēšanas formāts (BR)** un pēc tam atlasiet **Saglabāt**.
13. Atlasiet **Jauns** un laukā **Atbildes veids** fiksēto vērtību "ABRASFCuritibaInquireResponse", bet laukā **Apraksts** ievadiet "Description".
14. Laukā **Iesniegšanas statuss** atlasiet **Neizlemts**.
15. Laukā **Modeļa kartēšana** atlasiet **Atbildes ziņojumu importēšana** ar **(Priekšskatījums) NFS-e ABRASF Curitiba atbildes ziņojuma importēšana (BR)**.
16. Atlasiet **Saglabāt** un pēc tam atgriezieties tēmā [Sākt darbu ar elektronisko rēķinu pievienojumprogrammu](e-invoicing-get-started.md), lai izvietotu elektronisko rēķinu līdzekli.

## <a name="privacy-notice"></a>Paziņojums par konfidencialitāti
Līdzekļu **NF-e Federālā — Brazīlijas elektroniskais rēķins (BR)** un **NFS-e — Brazīlijas pakalpojuma (pilsētas) elektroniskais rēķins** iespējošanai var būt nepieciešams nosūtīt ierobežotus datus, tostarp organizācijas nodokļu reģistrācijas ID. Dati tiek pārsūtīt trešo pušu aģentūrām, kuras pilnvarojusi nodokļu iestāde, lai nosūtītu elektroniskos rēķinus šai nodokļu iestādei iepriekšdefinētā formātā, kas nepieciešams integrācijai ar valdības tīmekļa pakalpojumu. Kā administrators jūs varat iespējot vai izslēgt līdzekļus **NF-e Federālā — Brazīlijas elektroniskais rēķins (BR)** un **NFS-e — Brazīlijas pakalpojuma (pilsētas) elektroniskais rēķins**. Šajās darbībās parādīts, kā to izdarīt: 

1. Dodieties uz **Organizācijas pārvaldība** > **Iestatīšana** > **Elektronisko dokumentu parametri**. 
2. Cilnē **Līdzekļi** atlasiet rindu, kas satur līdzekli **NF-e Federālā — Brazīlijas elektroniskais rēķins (BR)** vai **NFS-e — Brazīlijas pakalpojuma (pilsētas) elektroniskais rēķins**, un atlasiet līdzekli. No šīm ārējām sistēmām importētie dati šajā Dynamics 365 tiešsaistes pakalpojumā ir pakļauti mūsu [paziņojumam par privātumu](https://go.microsoft.com/fwlink/?LinkId=512132). Lai iegūtu plašāku informāciju, skatiet sadaļas Konfidencialitātes paziņojums valstij raksturīgā līdzekļa dokumentācijā.

## <a name="additional-resources"></a>Papildu resursi

- [Elektroniskās rēķinu izveides pievienojumprogrammas pārskats](e-invoicing-service-overview.md)
- [Darba sākšana ar elektroniskās rēķinu izveides pievienojumprogrammas servisa administrēšanu](e-invoicing-get-started-service-administration.md)
- [Darba sākšana ar elektroniskās rēķinu izveides pievienojumprogrammu](e-invoicing-get-started.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
