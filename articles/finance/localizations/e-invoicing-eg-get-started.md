---
title: Elektroniskā rēķinu izrakstīšana Ēģiptei
description: Šajā rakstā sniegta informācija, kas palīdzēs jums sākt darbu ar elektronisko rēķinu izrakstīšanu Ēģiptei Microsoft Dynamics 365 Finansēs un Dynamics 365 Supply Chain Management.
author: gionoder
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: c2a46ef938c5dee62c0d0acd1648584df344c81a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904417"
---
# <a name="electronic-invoicing-for-egypt"></a>Elektroniskā rēķinu izrakstīšana Ēģiptei

[!include [banner](../includes/banner.md)]

Šajā rakstā sniegta informācija, kas palīdzēs jums sākt darbu ar elektronisko rēķinu izrakstīšanu Ēģiptei. Tas palīdz veikt konfigurācijas darbības, kas ir atkarīgas no valsts regulēšanas konfigurācijas pakalpojumā (RCS). Šīs darbības papildina darbības, kas aprakstītas Sadaļā [Elektronisko rēķinu izrakstīšanas iestatīšana](e-invoicing-set-up-overview.md).

## <a name="prerequisites"></a>Priekšnosacījumi

Pirms sākat procedūras šajā rakstā, izpildiet tālāk norādītos priekšnosacījumus:

- Iepazīsties ar elektronisko rēķinu izrakstīšanu, kā tas ir aprakstīts Elektronisko [rēķinu izrakstīšanas pārskatā](e-invoicing-service-overview.md).
- Reģistrēties RCS un iestatīt elektronisko rēķinu izrakstīšanu. Papildinformāciju skatiet tālāk norādītajās tēmās.

    - [Reģistrēties elektronisko rēķinu izrakstīšanas pakalpojumā un instalēt to](e-invoicing-sign-up-install.md)
    - [Iestatīt Azure resursus elektroniskajai rēķinu izrakstīšanai](e-invoicing-set-up-azure-resources.md)
    - [Instalējiet programmu Microservices pievienojumprogrammu pakalpojumam Lifecycle Services](e-invoicing-install-add-in-microservices-lcs.md)
    
- Aktivizējiet integrāciju starp jūsu Microsoft Dynamics 365 Finansēm Dynamics 365 Supply Chain Management [vai programmu un Elektronisko rēķinu izrakstīšanas pakalpojumu](e-invoicing-activate-setup-integration.md), kā aprakstīts Sadaļā Aktivizēt un iestatīt integrāciju ar Elektronisko rēķinu izrakstīšanu.
- Izveidojiet ciparsertifikātu noslēpumu Azure atslēgas to un iestatiet to, kā aprakstīts Debitoru [sertifi kā noslēpumos](e-invoicing-customer-certificates-secrets.md). Testēšanas nolūkos Ēģiptes nodokļu iestāde nodrošina konkrētus testa ciparsertifikātus, kas jāizmanto tikai testēšanas un risinājuma apstiprināšanas posmu laikā. Lai iegūtu plašāku informāciju, dodieties uz Ēģiptes nodokļu iestādes vietni, izmantojot saiti, kas ir sniegta [Ēģiptes e-rēķinu izrakstīšanas SDK](https://sdk.invoicing.eta.gov.eg/faq/).

## <a name="country-specific-configuration-for-the-egyptian-electronic-invoice-eg-feature"></a>Valstij specifiskā konfigurācija Ēģiptes elektroniskā rēķina (DEBITORA) funkcijai

Daži parametri No Ēģiptes elektroniskā rēķina **(DEBITORA) elektroniskās** rēķinu izrakstīšanas funkcijas tiek publicēti ar noklusētajām vērtībām. Pirms izvietojat elektronisko rēķinu izrakstīšanas līdzekli pakalpojumu vidē, pārskatiet noklusējuma vērtības un atjauniniet tās pēc vajadzības, lai tās labāk atspoguļotu jūsu biznesa operāciju.

1. Importējiet Ēģiptes elektroniskā rēķina **(DEBITORA)**[globalizācijas funkcijas jaunāko versiju, kā aprakstīts Globālā repozitorija importa funkcijām](e-invoicing-import-feature-global-repository.md).
2. Izveidojiet importētā globalizācijas līdzekļa kopiju un izvēlieties tam savu konfigurācijas nodrošinātāju, [kā aprakstīts sadaļā Izveidot globalizācijas līdzekli](e-invoicing-create-new-globalization-feature.md).
3. Cilnē **Versijas** pārbaudiet, vai ir atlasīta versija **Melnraksts** .
4. Iestatījumu cilnes **režģī** atlasiet atvasinātā funkcionalitātes **iestatījuma Pārdošanas** rēķins.
5. Atlasiet **Rediģēt**.
6. Cilnes Apstrādes **konveijers** sadaļā Konveijera **apstrāde** izvēlieties **Zīmju json dokumentu Ēģiptes nodokļu iestādei**.
7. **Sadaļā Parametri** atlasiet sertifikāta **nosaukumu un** pēc tam atlasiet izveidotā ciparsertifikāla nosaukumu.
8. Sadaļā Apstrādes **konveijers** izvēlieties **Integrēt ar Ēģiptes ETA pakalpojumu**. Atkārtojiet šo darbību abiem šīs darbības gadījumiem.
9. Sadaļā Parametri **atlasiet** Tīmekļa pakalpojuma **URL un** Pieteikšanās **pakalpojuma URL**. Pēc tam pārskatiet URL parametrus. Lai saņemtu testēšanas un ražošanas URL, dodieties uz Ēģiptes nodokļu iestādes vietni, izmantojot saiti, kas ir sniegta [Ēģiptes e-rēķinu izrakstīšanas SDK](https://sdk.invoicing.eta.gov.eg/faq/).
10. Atlasiet **Saglabāt** un aizveriet lapu.
11. Atkārtojiet no 4. līdz 10. solim projekta rēķina **atvasinātās funkcionalitātes** iestatījumam.

## <a name="country-specific-configuration-for-the-egyptian-electronic-invoice-eg-application-setup"></a>Valstij noteiktā konfigurācija Ēģiptes elektroniskā rēķina (DEBITORA) programmas iestatījumam

Ir parametri, kas jāiestata jūsu Finanšu vai Piegādes ķēžu pārvaldības vidē. Šo iestatījumu var aizpildīt vienā no divām vietām:

- Tieši finanšu vai piegādes ķēdes pārvaldības vidē; Plašāku informāciju skatiet Iestatīšanas elektronisko [rēķinu izrakstīšanas parametros](e-invoicing-set-up-parameters.md).
- In RCS. Elektronisko rēķinu izrakstīšanas funkciju iestatīšanas ietvaros varat noteikt visus parametrus un pēc tam izvietot tos tieši jūsu Finanšu vai piegādes ķēdes pārvaldības vidē, kad izvietojat elektronisko rēķinu izrakstīšanas līdzekli.

Abām opcijām parametri ir vienādi. Iestatot pirmo funkcionalitāti Elektronisko rēķinu izrakstīšanas pakalpojumā, ieteicams sekot šiem soļiem, lai iestatītu parametrus RCS un izvietotu tos savienotajā programmā.

> [!NOTE]
> Dažas elektronisko rēķinu izrakstīšanas līdzekļu versijas var ietvert iepriekš noteiktu programmai noteiktu parametru kopu Finanšu vai piegādes ķēžu pārvaldībai. Šādā gadījumā jāpārbauda, vai dati ir pareizi. Pretējā gadījumā manuāli iestatiet parametrus.

1. Atrast kopiju Ēģiptes **elektroniskā rēķina (MAKS) globalizācijas** līdzeklim, ko izveidojāt.
2. Cilnē **Versijas** pārbaudiet, vai ir atlasīta versija **Melnraksts** .
3. Cilnē **Iestatījumi** atlasiet **Lietojumprogrammas iestatīšana**.
4. Laukā **Saistītās** programmas atlasiet programmu, kurā vēlaties izvietot parametrus.
5. Lapā Elektronisko **dokumentu tipi** atlasiet **Pievienot**, lai izveidotu ierakstu.
6. Laukā **Tabulas** nosaukums pievienojiet **CustInvoiceJour**.
7. Laukā **Konteksts** pievienojiet atsauci debitora rēķina konteksta **kartēšanas** nosaukumam. Konfigurācija ir debitora **rēķina konteksta modelis**.
8. Laukā **Elektronisko dokumentu kartēšana** pievienojiet atsauci debitora rēķina kartēšanas **nosaukumam**. Konfigurācija ir rēķina **modeļa kartēšana**.
9. Atlasiet **Saglabāt**.
10. Atbilžu **tipu** lapā atlasiet **Pievienot**.
11. Laukā **Atbildes tips** ievadiet **Atbilde**.
12. Laukā **Apraksts ievadiet** Procesa **atbilde**.
13. Laukā **Iesniegšanas statuss** atlasiet **Neizlemts**.
14. Laukā **Modeļa kartēšana** atlasiet Atbildes **ziņojuma imports**. Konfigurācija ir Ēģiptes **atbildes ziņojuma imports (PLKST.**).
15. Atlasiet **Saglabāt**.
16. Atlasiet **Pievienot**.
17. Laukā **Atbildes tips** ievadiet **ResponseData**.
18. Laukā **Apraksts ievadiet** Procesa atbildes **dati**.
19. Laukā **Iesniegšanas statuss** atlasiet **Neizlemts**.
20. Laukā **Datu elementa** nosaukums atlasiet **SalesInvoiceHeaderV2Entity**.
21. Laukā **Modeļa kartēšana** atlasiet Atbildes **datu imports**. Konfigurācija ir **Ēģiptes atbildes datu importa formāts (ĒĢIPTE).**
22. Atlasiet **Saglabāt** un aizveriet lapu.
23. Aizvērt lapu.

Lai izvietotu līdzekli pakalpojumu videi un programmas iestatījumus lietojumprogrammai, kas saistīta ar finanšu vai piegādes ķēžu pārvaldību, [skatiet sadaļu Pabeigt, publicēt un izvietot globalizācijas līdzekli](e-invoicing-complete-publish-deploy-globalization-feature.md)

## <a name="privacy-notice"></a>Paziņojums par konfidencialitāti

Ēģiptes **elektroniskā rēķina (Ēģiptes elektroniskā rēķina) funkcionalitātes** iespējošanai var būt nepieciešams, lai nosūtītu ierobežotus datus. Šie dati ietver organizācijas nodokļu reģistrācijas ID. Dati tiks pārsūtīti trešās personas iestādēm, ko nodokļu iestāde ir pilnvarota nosūtīt elektroniskos rēķinus šī nodokļu iestādei iepriekš definētajā formātā, kas nepieciešams integrācijai ar valdības tīmekļa pakalpojumiem. Administrators var iespējot un atspējot šo līdzekli, ejot uz Organizācijas administrēšanas **iestatīšanas** \> **elektronisko** \> **dokumentu parametrus.** Cilnē **Līdzekļi** atlasiet rindu, kurā ir **Ēģiptes elektroniskā rēķina (EG)** līdzeklis, un pēc tam veiciet attiecīgo atlasi. Uz datiem, kas no ārējām sistēmām importēti šajā Dynamics 365 tiešsaistes pakalpojumā, attiecas mūsu paziņojums par [konfidencialitāti](https://go.microsoft.com/fwlink/?LinkId=512132). Papildinformāciju skatiet valstij raksturīgās funkcionalitātes dokumentācijas sadaļā "Paziņojums par konfidencialitāti".

## <a name="additional-resources"></a>Papildu resursi

- [Elektroniskās rēķinu izveides pārskats](e-invoicing-service-overview.md)
- [Darba sākšana ar elektroniskās rēķinu izveides servisa administrēšanu](e-invoicing-get-started-service-administration.md)
- [Darba sākšana ar elektroniskās rēķinu izveidi](e-invoicing-get-started.md)
- [Klientu elektroniskie rēķini Ēģiptē](emea-egy-e-invoices.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
