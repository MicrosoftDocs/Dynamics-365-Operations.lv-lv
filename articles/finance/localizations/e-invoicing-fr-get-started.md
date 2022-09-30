---
title: Sāciet ar Elektronisko rēķinu izrakstīšanas pievienojumprogrammu Francijai
description: Šajā rakstā ir sniegta informācija, kas palīdzēs jums sākt darbu ar Elektronisko rēķinu izrakstīšanas pievienojumprogrammu Francijai.
author: dkalyuzh
ms.date: 07/07/2022
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2022-00-02
ms.dyn365.ops.version: AX 10.0.29
ms.openlocfilehash: 3ac4af8c131e35d9a499d0d558c7cce1d4872b37
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573283"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-france"></a>Sāciet ar Elektronisko rēķinu izrakstīšanas pievienojumprogrammu Francijai

[!include [banner](../includes/banner.md)]

Šajā rakstā ir sniegta informācija, kas palīdzēs sākt darbu ar elektronisko rēķinu izrakstīšanu Francijai. Tas palīdz veikt konfigurācijas darbības, kas ir atkarīgas no valsts regulēšanas konfigurācijas pakalpojumā (RCS). Šīs darbības papildina darbības, kas aprakstītas sadaļā [Sākt darbu ar elektronisko rēķinu izrakstīšanas pievienojumprogrammu](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-french-chorus-pro-submission-fr-electronic-invoicing-feature"></a>Valstij raksturīgā konfigurācija Francijas Chorus Pro iesniegšanas (FR) Elektronisko rēķinu izrakstīšanas līdzeklim

Daži soļi ir nepieciešami, lai konfigurētu **Francijas Chorus Pro iesniegšanas (FR) Elektronisko** rēķinu izrakstīšanas līdzekli. Daži no konfigurācijas parametriem ir publicēti ar noklusējuma vērtībām. Šīs vērtības ir jāpārskata un jāatjaunina, lai tās labāk atspoguļotu jūsu biznesa operācijas.

### <a name="prerequisites"></a>Priekšnosacījumi

Pirms sākat procedūras šajā rakstā, izpildiet tālāk norādītos priekšnosacījumus:

- Iepazīsties ar elektronisko rēķinu izrakstīšanu. Plašāku informāciju skatiet Elektronisko [rēķinu izrakstīšanas apskats](e-invoicing-service-overview.md).
- Reģistrēties RCS un iestatīt elektronisko rēķinu izrakstīšanu. Papildinformāciju skatiet tālāk minētajos rakstos.

    - [Reģistrēties elektronisko rēķinu izrakstīšanas pakalpojumā un instalēt to](e-invoicing-sign-up-install.md)
    - [Iestatīt Azure resursus elektroniskajai rēķinu izrakstīšanai](e-invoicing-set-up-azure-resources.md)
    - [Instalējiet programmu Microservices pievienojumprogrammu pakalpojumam Lifecycle Services](e-invoicing-install-add-in-microservices-lcs.md)
    - [Aktivizēt un iestatīt integrāciju ar elektronisko](e-invoicing-activate-setup-integration.md) rēķinu izrakstīšanu - Microsoft Dynamics izmantojiet informāciju šajā rakstu, lai aktivizētu integrāciju starp jūsu 365 Finansēm Dynamics 365 Supply Chain Management vai programmu un Elektronisko rēķinu izrakstīšanas pakalpojumu.
    - [NAF kodi un siret numuri](emea-fra-naf-codes-siret-numbers.md)[un Iestatīt NAF kodus un Siret numurus](tasks/fr-00003-naf-codes-siret-numbers.md) – izmantojiet informāciju šajos rakstos, lai iestatītu NAF kodus un Siret numurus jūsu juridiskajām personām. 

- Jūsu organizācijai jābūt reģistrētai darbībai ar Chorus Pro. Microsoft nodrošina integrāciju ar Chorus pro režīmā OAuth2, izmantojot programmas programmēšanas interfeisu (API). Plašāku informāciju par Chorus Pro reģistrāciju un programmas aktivizāciju skatiet oficiālajā [dokumentācijā](https://communaute.chorus-pro.gouv.fr/documentation/help-for-api-developers-in-oauth2-mode/).

    Sekojiet šiem soļiem, lai reģistrētos Chorus Pro.

    1. Lai sāktu reģistrāciju [, dodieties](https://piste.gouv.fr/en/component/apiportal/registration) uz PISTE portālu. 
    2. Reģistrējiet programmu un aktivizējiet atvērtos autorizācijas (OAuth) akreditācijas datus.
    3. Kopējiet un saglabājiet OAuth akreditācijas datu klienta ID un slepeno atslēgu. Šo informāciju izmantosiet turpmākajās darbībās.
    4. Dodieties uz portālu [Chorus Pro, lai](https://portail.chorus-pro.gouv.fr/aife_csm/?id=aife_enrollment) reģistrētos. 
    5. Izveidojiet tehnisko kontu API piekļuvei. Papildinformāciju skatiet api [piekļuves ražošanas tehniskās konta izveidošanai](https://communaute.chorus-pro.gouv.fr/documentation/creation-of-a-technical-account-for-an-api-access-in-production/).
    6. Kopējiet tehniskā konta lietotāja ID un paroli. Šo informāciju izmantosiet turpmākajās darbībās.

## <a name="country-specific-configuration-of-the-application-setup-for-the-french-chorus-pro-submission-fr-electronic-invoicing-feature"></a>Valstij raksturīgā programmas iestatījumu konfigurācija Francijas Chorus Pro iesniegšanai (FR) Elektronisko rēķinu izrakstīšanas līdzeklim

Daži parametri no Francijas **Chorus Pro iesniegšanas (FR)** elektroniskās rēķinu izrakstīšanas funkcijas tiek publicēti ar noklusējuma vērtībām. Pirms izvietojat elektronisko rēķinu izrakstīšanas līdzekli pakalpojumu vidē, pārskatiet un atjauniniet noklusētās vērtības, kā nepieciešams, lai tās labāk atspoguļotu jūsu biznesa operācijas.

1. Azure atslēgā izveidojiet noslēpumus un atbilstošo atsauci uz tiem. Papildinformāciju skatiet Debitora [sertififikātus un noslēpumus](e-invoicing-customer-certificates-secrets.md).
2. Importējiet pēdējo Francijas **Chorus Pro iesniegšanas (FR)** globalizācijas [funkcijas versiju, kā aprakstīts Globālā repozitorija importa funkcijām](e-invoicing-import-feature-global-repository.md).
3. Izveidojiet importētā globalizācijas līdzekļa kopiju un atlasiet konfigurācijas nodrošinātāju. Papildinformāciju skatiet sadaļā [Globalizācijas līdzekļa izveide](e-invoicing-create-new-globalization-feature.md).
4. Cilnē **Versijas** pārbaudiet, vai ir atlasīta versija **Melnraksts** .
5. Cilnē Iestatījumi **režģī atlasiet UBL pārdošanas** rēķina atvasinātās funkcionalitātes **iestatījumu**.
6. Atlasiet **Rediģēt** un **pēc** **·** **tam cilnē Konveijera apstrāde sadaļā Apstrādes konveijers atlasiet (priekšskatījums) Integrēt ar Francijas Chorus Pro** **ar darbības nosaukumu Francijas Chorus Pro iesniegšanu.**
7. Sadaļas **Parametri** **laukā Klienta ID** noslēpuma vārds izvēlieties slepeno vārdu, ko izveidojāt klienta ID atslēgas laikā.
8. Laukā **Klienta noslēpuma noslēpuma** vārds atlasiet atslēgas noslēpuma vārdu, ko izveidojāt klienta noslēpumam.
9. Tehniskās pieteikšanās **slepenā vārda** laukā atlasiet slepeno vārdu, ko izveidojāt tehniskajai konta pierakstīšanās atslēgai.
10. Tehniskās paroles **slepenā vārda** laukā atlasiet slepeno vārdu, ko izveidojāt tehniskās konta parolei atslēgas krātuvē.
11. Cilnē Apstrādes **konveijers** sadaļā **·** **Konveijera apstrāde atlasiet Integrēt ar Francijas Chorus Pro** **ar darbības nosaukumu Francijas Chorus Pro pieprasījuma statusu.**
12. Sadaļas **Parametri** **laukā Klienta ID** noslēpuma vārds izvēlieties slepeno vārdu, ko izveidojāt klienta ID atslēgas laikā.
13. Laukā **Klienta noslēpuma noslēpuma** vārds atlasiet atslēgas noslēpuma vārdu, ko izveidojāt klienta noslēpumam.
14. Tehniskās pieteikšanās **slepenā vārda** laukā atlasiet slepeno vārdu, ko izveidojāt tehniskajai konta pierakstīšanās atslēgai.
15. Tehniskās paroles **slepenā vārda** laukā atlasiet slepeno vārdu, ko izveidojāt tehniskās konta parolei atslēgas krātuvē.
16. Atlasiet **Saglabāt** un pēc tam aizveriet lapu.
17. Atkārtojiet no 6. līdz 16 **. solim UBL** projekta rēķina atvasinātās funkcionalitātes iestatījumam, **UBL** pārdošanas kredīta notas atvasinātās funkcionalitātes iestatījumam **un UBL projekta kredīta notas atvasinātās** funkcionalitātes iestatījumam.

## <a name="additional-resources"></a>Papildu resursi

- [Elektroniskās rēķinu izveides pievienojumprogrammas pārskats](e-invoicing-service-overview.md)
- [Darba sākšana ar elektroniskās rēķinu izveides pievienojumprogrammas servisa administrēšanu](e-invoicing-get-started-service-administration.md)
- [Darba sākšana ar elektroniskās rēķinu izveides pievienojumprogrammu](e-invoicing-get-started.md)
