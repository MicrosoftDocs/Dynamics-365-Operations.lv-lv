---
title: Darba sākšana ar elektronisko rēķinu izveidi lietošanai Brazīlijā
description: Šajā rakstā ir sniegta informācija, kas jums palīdzēs uzsākt elektronisko rēķinu izrakstīšanu Brazīlijai finanšu un piegādes ķēžu pārvaldībā.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 8c540daca852a8197841957c1d6d3e5c7892ce4b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279940"
---
# <a name="get-started-with-electronic-invoicing-for-brazil"></a>Darba sākšana ar elektronisko rēķinu izveidi lietošanai Brazīlijā 

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija, kas palīdzēs sākt darbu ar elektronisko rēķinu izrakstīšanu Brazīlijai. Šajā rakstā ir aprakstītas konfigurācijas darbības, kas ir atkarīgas no valsts regulēšanas konfigurācijas pakalpojumos (RCS), un ir papildinātas darbības, kas aprakstītas rakstā. [Sāciet ar elektronisko rēķinu izrakstīšanu](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-brazilian-nf-e-br-electronic-invoicing-feature"></a>Valsts konfigurācijas Brazīlijas NF-e (BR) elektronisko rēķinu līdzeklim

Daži no parametriem no **Brazīlijas NF-e (BR) elektronisko rēķinu izrakstīšanas līdzeklis** tiek publicēti ar noklusējuma vērtībām. Pārskatiet vērtības un, ja nepieciešams, atjauniniet vērtības, lai tās labāk atbilstu biznesa operācijas vajadzībām, pirms izvietojat elektronisko rēķinu izrakstīšanas līdzekli Pakalpojumu vidē.

Šī sadaļa papildina rakstu **sadaļai Elektronisko rēķinu izrakstīšana** valstij raksturīgo konfigurāciju. [Sākt ar elektronisko rēķinu izrakstīšanu](e-invoicing-get-started.md).

1. Darbvietas **Globalizācijas līdzekļi** sadaļas **Līdzekļi** RCS atlasiet elementu **Elektronisko rēķinu izrakstīšana**.
2. Lapā **Elektroniskā rēķina izveides līdzekļi** verificējiet, ka tiek atlasīts jūsu izveidotais elektronisko rēķinu līdzeklis **Brazīlijas NF-e (BR)**.
3. Cilnē **Versijas** pārbaudiet, vai ir atlasīta versija **Melnraksts** .
4. Režģa cilnē **Iestatījumi** atlasiet **Iesniegt** un pēc tam atlasiet **Rediģēt**.
5. Lauka grupas **Darbības** cilnē **Darbības** atlasiet darbību **(Priekšskatījums) Parakstīt XML dokumentu**.
6. Lauka grupā **Parametri** atlasiet **Sertifikāta nosaukums** un laukā **Vērtība** ievadiet ar jūsu galvenā atslēgu akreditācijas parametra sertifikātu saistīto nosaukumu.
7. Lauka grupas **Darbības** cilnē **Darbības** atlasiet darbību **(Priekšskatījums) Izsaukt Brazīlijas SEFAZ pakalpojumu**.
8. Lauka grupā **Parametri** atlasiet parametru **URL adrese**.
9. Ja nepieciešams, laukā **Vērtība** pārskatiet un atjauniniet SEFAZ dokumentācijas publicēto tīmekļa pakalpojumu URL jūsu valstij un pēc tam atlasiet **Saglabāt.**
10. Cilnē **Piemērojamības kārtulas**, lauka grupā **Piemērojamības kārtulas iestatīšana** pārskatiet un atjauniniet lauka kritēriju **Statuss**, atbilstoši tam pašam statusam, uz kuru attiecas tīmekļa pakalpojumu URL.
11. Atlasiet **Saglabāt** un aizveriet lapu.
12. Lai izvietotu Elektronisko rēķinu izrakstīšanas līdzekli Pakalpojuma vidē, skatiet sadaļu [Sākt darbu ar Elektronisko rēķinu izrakstīšanu](e-invoicing-get-started.md).

## <a name="country-specific-configuration-of-application-setup-for-brazilian-nf-e-br-electronic-invoicing-feature"></a>Lietojumprogrammas iestatīšanas valsts konfigurācijas Brazīlijas NF-e (BR) elektronisko rēķinu līdzeklim

Veiciet šīs darbības, pirms izvietojat programmas iestatījumus jūsu Finance vai Supply Chain Management saistītajai programmai.

Šī sadaļa papildina rakstu **sadaļas Programmas** iestatījumi valstij raksturīgo konfigurāciju. [Sākt ar elektronisko rēķinu izrakstīšanu](e-invoicing-get-started.md).

1. Darbvietas **Globalizācijas līdzekļi** sadaļas **Līdzekļi** RCS atlasiet elementu **Elektronisko rēķinu izrakstīšana**.
2. Lapā **Elektroniskā rēķina izveides līdzekļi** verificējiet, ka tiek atlasīts elektronisko rēķinu līdzeklis **Brazīlijas NF-e (BR)**.
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
13. Lai izvietotu programmas iestatījumus saistītajai programmai Finance vai Supply Chain, skatiet sadaļu [Sākt darbu ar elektronisko rēķinu izrakstīšanu](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-brazilian-nfs-e-abrasf-curitiba-br-electronic-invoicing-feature"></a>Valsts konfigurācijas Brazīlijas NFS-e ABRASF Curitiba (BR) elektronisko rēķinu līdzeklim

Daži no parametriem no **Brazīlijas NFS-e ABRASF Curitiba (BR) elektronisko rēķinu izrakstīšanas līdzeklis** tiek publicēti ar noklusējuma vērtībām. Pārskatiet un, ja nepieciešams, atjauniniet vērtības, lai tās labāk atbilstu biznesa operācijas vajadzībām, pirms izvietojat elektronisko rēķinu izrakstīšanas līdzekli Pakalpojumu vidē.

Šī sadaļa papildina rakstu **sadaļai Elektronisko rēķinu izrakstīšana** valstij raksturīgo konfigurāciju. [Sākt ar elektronisko rēķinu izrakstīšanu](e-invoicing-get-started.md).

1. Darbvietas **Globalizācijas līdzekļi** sadaļas **Līdzekļi** RCS atlasiet elementu **Elektronisko rēķinu izrakstīšana**.
2. Lapā **Elektroniskā rēķina izveides līdzekļi** verificējiet, ka tiek atlasīts jūsu izveidotais elektronisko rēķinu līdzeklis **Brazīlijas NFS-e ABRASF (BR)**.
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
18. Lai izvietotu Elektronisko rēķinu izrakstīšanas līdzekli Pakalpojuma vidē, skatiet sadaļu [Sākt darbu ar Elektronisko rēķinu izrakstīšanu](e-invoicing-get-started.md).

## <a name="country-specific-configuration-of-application-setup-for-brazilian-nfs-e-abrasf-curitiba-br-electronic-invoicing-feature"></a>Lietojumprogrammas iestatīšanas valsts konfigurācijas Brazīlijas NFS-e ABRASF Curitiba (BR) elektronisko rēķinu līdzeklim

Veiciet šīs darbības, pirms izvietojat programmas iestatījumus jūsu Finance vai Supply Chain Management saistītajai programmai.

Šī sadaļa papildina rakstu **sadaļas Pieteikuma iestatījumi valstij raksturīgo** konfigurāciju. [Sākt ar elektronisko rēķinu izrakstīšanu](e-invoicing-get-started.md).

1. Darbvietas **Globalizācijas līdzekļi** sadaļas **Līdzekļi** RCS atlasiet elementu **Elektronisko rēķinu izrakstīšana**.
2. Lapā **Elektroniskā rēķina izveides līdzekļi** verificējiet, ka tiek atlasīts elektronisko rēķinu līdzeklis **Brazīlijas NFS-e ABRASF (BR)**.
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
16. Atlasiet **Saglabāt** un aizveriet lapu.
17. Lai izvietotu programmas iestatījumus saistītajai programmai Finance vai Supply Chain, skatiet sadaļu [Sākt darbu ar elektronisko rēķinu izrakstīšanu](e-invoicing-get-started.md).

## <a name="privacy-notice"></a>Paziņojums par konfidencialitāti
Līdzekļu **NF-e Federālā — Brazīlijas elektroniskais rēķins (BR)** un **NFS-e — Brazīlijas pakalpojuma (pilsētas) elektroniskais rēķins** iespējošanai var būt nepieciešams nosūtīt ierobežotus datus, tostarp organizācijas nodokļu reģistrācijas ID. Dati tiek pārsūtīt trešo pušu aģentūrām, kuras pilnvarojusi nodokļu iestāde, lai nosūtītu elektroniskos rēķinus šai nodokļu iestādei iepriekšdefinētā formātā, kas nepieciešams integrācijai ar valdības tīmekļa pakalpojumu. Kā administrators jūs varat iespējot vai izslēgt līdzekļus **NF-e Federālā — Brazīlijas elektroniskais rēķins (BR)** un **NFS-e — Brazīlijas pakalpojuma (pilsētas) elektroniskais rēķins**. Šajās darbībās parādīts, kā to izdarīt: 

1. Dodieties uz **Organizācijas pārvaldība** > **Iestatīšana** > **Elektronisko dokumentu parametri**. 
2. Cilnē **Līdzekļi** atlasiet rindu, kas satur līdzekli **NF-e Federālā — Brazīlijas elektroniskais rēķins (BR)** vai **NFS-e — Brazīlijas pakalpojuma (pilsētas) elektroniskais rēķins**, un atlasiet līdzekli. No šīm ārējām sistēmām importētie dati šajā Dynamics 365 tiešsaistes pakalpojumā ir pakļauti mūsu [paziņojumam par privātumu](https://go.microsoft.com/fwlink/?LinkId=512132). Lai iegūtu plašāku informāciju, skatiet sadaļas Konfidencialitātes paziņojums valstij raksturīgā līdzekļa dokumentācijā.

## <a name="additional-resources"></a>Papildu resursi

- [Elektroniskās rēķinu izveides pārskats](e-invoicing-service-overview.md)
- [Darba sākšana ar elektroniskās rēķinu izveides servisa administrēšanu](e-invoicing-get-started-service-administration.md)
- [Darba sākšana ar elektroniskās rēķinu izveidi](e-invoicing-get-started.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
