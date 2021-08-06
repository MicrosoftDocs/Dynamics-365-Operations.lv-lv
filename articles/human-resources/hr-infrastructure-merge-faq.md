---
title: Dynamics 365 Human Resources bieži uzdotie jautājumi par infrastruktūras sapludināšanu
description: Šī tēma sniedz atbildes uz bieži uzdotiem jautājumiem par Microsoft Dynamics 365 Human Resources un Finance and Operations infrastruktūras sapludināšanu.
author: rachel-profitt
ms.date: 07/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fee4fea9b67ff8a0c8d813940a65cf882bd13abe
ms.sourcegitcommit: bf2daeccbe3f2826e734f409bfc823820144aa23
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/15/2021
ms.locfileid: "6617995"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-faq"></a>Dynamics 365 Human Resources bieži uzdotie jautājumi par infrastruktūras sapludināšanu

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šī tēma sniedz atbildes uz bieži uzdotiem jautājumiem par Microsoft Dynamics 365 Human Resources un Finance and Operations infrastruktūras sapludināšanu.

## <a name="what-is-the-dynamics-365-human-resources-infrastructure-merge"></a>Kas ir Dynamics 365 Human Resources infrastruktūras sapludināšana?

Dynamics 365 Human Resources ir savrupa programma, kas izmanto dažādas infrastruktūras, nevis citas Finance and Operations programmas, piemēram Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce un Dynamics 365 Project Operations. Infrastruktūras sapludināšana apvienos Dynamics 365 Human Resources tajā pašā infrastruktūra kā citas Finance and Operations programmas.

## <a name="value-and-benefits-of-the-infrastructure-merge"></a>Infrastruktūras sapludināšanas vērtība un atvieglojumi

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-what-benefits-will-we-see-from-these-changes"></a>Mana organizācija izmanto Dynamics 365 Human Resources, lai pārvaldītu savas HR operācijas. Kādus atvieglojumus mēs redzēsim no šīm izmaiņām?

- Šīs izmaiņas izslēdz vairākas personāla vadības (HR) iespējas programmā Dynamics 365.
- Tie nodrošina gan Microsoft Power Platform paplašināmību, gan biznesa loģikas un funkcionalitātes opciju paplašināšanas veidu.
- Tās nodrošina atbilstību starp Dynamics 365 Human Resources un citām Finance and Operations programmām Application Lifecycle Management (ALM), Microsoft Dynamics Lifecycle Services (LCS), ģeogrāfiskās pieejamības, paplašināmības un citas informācijas ziņā.
- Tie ļauj izmantot koplietoto pakalpojumu un rīku sniegtās priekšrocības un palīdzēt samazināt izmaksas.

### <a name="my-organization-uses-dynamics-365-human-resources-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-benefits-will-we-see-from-these-changes"></a>Mana organizācija izmanto Dynamics 365 Human Resources programmās Dynamics 365 Finance, Supply Chain Management, Commerce vai Project Operations. Kādus atvieglojumus mēs redzēsim no šīm izmaiņām?

Iespējas un ieguldījumi, kas ir veikti Dynamics 365 Human Resources, tagad būs pieejami debitoriem, kuri izmanto HR moduli programmā Dynamics 365 Finance. Dažas no šīm iespējām ir atvaļinājumu un prombūtnes pārvaldība, atvieglojumu pārvaldība un uzdevumu pārvaldība.

### <a name="will-i-lose-any-features-or-capabilities-that-i-currently-use"></a>Vai zaudēšu visus līdzekļus vai iespējas, ko es pašlaik izmantoju?

Starp Dynamics 365 Human Resources un HR moduli būs funkcionāla paritāte programmās Finance and Operations. Dynamics 365 Human Resources funkcijām būs augstāka prioritāte. Papildinformāciju skatiet [Līdzekļu pārvaldības pārskatā](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="will-the-experience-change-for-my-users"></a>Vai pieredzes izmaiņas radīsies maniem lietotājiem?

Jaunās HR iespējas tiks pārvaldītas, izmantojot līdzekļu pārvaldību. Debitori izlems, vai viņi vēlas tos izmantot. Dažos gadījumos var tikt mainītas iespējas. Šajos gadījumos tiks sniegta dokumentācija.

### <a name="how-does-this-change-affect-me-if-i-am-an-existing-customer-and-i-use-both-the-hr-module-on-the-finance-and-operations-infrastructure-and-dynamics-365-human-resources-through-custom-integrations"></a>Kā šīs izmaiņas ietekmē mani, ja es esmu esošs debitors un es izmantoju gan Finance and Operations infrastruktūras HR moduli, gan Dynamics 365 Human Resources no pielāgotām integrācijām?

Pielāgotās integrācijas starp Dynamics 365 Human Resources un HR moduli programmā Dynamics 365 Finance vairs nebūs nepieciešamas. Visi HR dati atrodas tajā pašā datu bāzē, kurā atrodas citas Finance and Operations programmas.

## <a name="migration-from-dynamics-365-human-resources-to-finance-and-operations-apps"></a>Migrācija no Dynamics 365 Human Resources uz Finance and Operations programmām

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-hr-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>Mana organizācija izmanto Dynamics 365 Human Resources, lai pārvaldītu HR operācijas. Kas mums ir jāplāno, lai pārietu uz jauno pieredzi?

Ja jūsu organizācija izmanto Dynamics 365 Human Resources, bet neizmanto citas Finance and Operations programmas, jūsu Human Resources vide tiks migrēta uz jauno infrastruktūru. Liela daļa šī migrācijas procesa tiks automatizēta. Tiks veikti procesi, lai migrētu datu bāzi un sinhronizētu to ar jauno infrastruktūru.

Turklāt, izmantojot rīkus, varat pārbaudīt migrācijas procesu un pārbaudīt datus un pieredzi pirms ražošanas vides migrēšanas.

Ja jūsu organizācija izmanto gan Dynamics 365 Human Resources abas programmas, gan citas Finance and Operations programmas, jums jāplāno vairāk laika validācijai, lai nodrošinātu, ka dati tiek pareizi migrēti jaunajā vidē. Migrācija uz jauno infrastruktūru saplūdīs ar jūsu Human Resources vides datiem ar Finance and Operations vidi. Būs pieejami rīki, lai automatizētu pēc iespējas vairāk datu sapludināšanas procesa. Tomēr konfliktējošu datu gadījumā būs nepieciešama lietotāja ievadne, lai noteiktu, kā konflikts jāatrisina. Lietotājiem un administratoriem būs jāpārvalda datu kartēšana, kur ir konflikti, un jātestē migrācija smilškastu vidēs pirms ražošanas vides migrācijas.

### <a name="my-organization-uses-dynamics-365-human-resources-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>Mana organizācija izmanto Dynamics 365 Human Resources programmās Dynamics 365 Finance, Supply Chain Management, Commerce vai Project Operations. Kas mums ir jāplāno, lai pārietu uz jauno pieredzi?

Organizācijām, kas izmanto HR moduli Finance and Operations programmās, jūsu videi tiks pielietota jaunā līdzekļa funkcionalitāte no Dynamics 365 Human Resources, izmantojot standarta vienas versijas atjaunināšanas procesu. Ir paredzams, ka jūsu vidē jaunā funkcionalitāte būs pieejama katrā atjauninājumā. Lai ieslēgtu jaunus līdzekļus, var izmantot līdzekļu pārvaldību. Tomēr ir jāplāno šo līdzekļu validācija. Ievērojiet procesus, kas jums ir pieejami citu vides atjauninājumu validēšana. Papildinformāciju par to, kā atjauninājumi tiek pielietoti Finance and Operations programmām, skatiet sadaļā [Vienas versijas apskats](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="when-will-my-organization-be-migrated"></a>Kad mana organizācija tiks migrēta?

Katras organizācijas migrācija būs atkarīga no tās pašreizējās konfigurācijas un gatavības migrēt uz jauno infrastruktūru. Šos datumus var mainīt.

- Organizācijas, kas Finance and Operations lietojumprogrammās pašreiz izmanto HR moduli, saņems HR funkcionalitāti programmai Dynamics 365 Human Resources kā daļu no parastā vienas versijas atjaunināšanas procesa. Ir plānots, ka jaunās funkcijas kļūs plaši pieejamas, sākot no 2021. gada oktobra.
- Organizācijām, kas pašlaik izmanto tikai Dynamics 365 Human Resources būs piekļuve migrācijas rīkiem, lai tie varētu sākt testēšanu un sākt migrāciju, kas sāksies 2022. gada vidū. Datums, kad jāveic migrācija uz jauno infrastruktūru, vēl nav noteikts. Tomēr tas būs vismaz gadu pēc dienas, kad būs pieejami migrācijas rīki.
- Organizācijām, kas pašlaik izmanto gan Dynamics 365 Human Resources, gan citas Finance and Operations programmas, būs piekļuve migrācijas rīkiem, lai tie varētu sākt testēšanu un sākt migrāciju, kas sāksies 2022. gada vidū. Datums, kad jāveic migrācija uz jauno infrastruktūru, vēl nav noteikts. Tomēr tas būs vismaz gadu pēc dienas, kad būs pieejami migrācijas rīki.

Papildinformāciju par jaunajām Dynamics 365 Human Resources funkcijām skatiet sadaļā [Jaunumi vai izmaiņas programmā Human Resources](./hr-admin-whats-new.md).

### <a name="i-am-using-new-capabilities-that-are-available-only-in-dynamics-365-human-resources-such-as-leave-and-absence-and-benefits-management-will-these-capabilities-now-be-available-in-the-human-resources-module-on-the-finance-and-operations-infrastructure-too"></a>Es izmantoju jaunas iespējas, kas pieejamas tikai programmā Dynamics 365 Human Resources (piemēram, **Atvaļinājums un prombūtne** un **Atvieglojumu pārvaldība**). Vai šīs iespējas tagad būs pieejamas arī Human Resources modulī Finance and Operations infrastruktūrā?

Jā, visi moduļi no Dynamics 365 Human Resources darbosies tāpat, kā Finance and Operations programmās, un būs 100 procentu funkcionalitātes pārība. Kā daļa no vispārējās migrācijas stratēģijas klientiem, kas pašlaik izmanto šīs iespējas HR, debitoru dati tiks migrēti tā, lai tie turpina strādāt Finance and Operations infrastruktūrai.

### <a name="i-use-the-new-dynamics-365-human-resources-benefits-management-capabilities-ive-built-custom-integrations-with-the-hr-module-on-the-finance-and-operations-infrastructure-so-that-i-can-take-advantage-of-the-payroll-capabilities-by-using-benefits-data-will-these-custom-integrations-be-required-going-forward"></a>Es izmantoju jaunās Dynamics 365 Human Resources atvieglojumu pārvaldības iespējas. Es esmu izveidojis pielāgotas integrācijas ar HR moduli Finance and Operations infrastruktūrasi, lai es varētu gūt labumu no algu iespējām, izmantojot atvieglojumu datus. Vai šīs pielāgotās integrācijas būs nepieciešamas turpmāk?

Kā daļa no infrastruktūras sapludināšanas HR dati tiek ievadīti tajā pašā datu bāzē, kurā atrodas pārējās Finance and Operations programmas. Integrēšana starp moduļiem Finance and Operations programmās vairs nebūs nepieciešama.

### <a name="my-organization-uses-one-or-more-isv-solutions-with-dynamics-365-human-resources-will-our-isv-solutions-be-migrated-automatically"></a>Mana organizācija izmanto vienu vai vairākus ISV risinājumus ar Dynamics 365 Human Resources. Vai mūsu ISV risinājumi tiks migrēti automātiski?

Migrācijas pieredze katram neatkarīgam programmatūras izstrādātāja (ISV) risinājumam atšķirsies atkarībā no risinājuma integrācijas metodes. Korporācija Microsoft strādās cieši ar ISVs, lai nodrošinātu gludu pāreju uz jauno infrastruktūru.

### <a name="my-organization-uses-linkedin-talent-hub-integration-with-dynamics-365-human-resources-will-this-integration-continue-to-work-after-the-infrastructure-change-is-completed"></a>Mana organizācija izmanto LinkedIn Talantu Hub integrāciju ar Dynamics 365 Human Resources. Vai šī integrācija turpinās darbu pēc infrastruktūras izmaiņu pabeigšanas?

Jā, LinkedIn Talantu Hub integrācija turpinās darbu pēc migrācijas uz jauno infrastruktūru.

### <a name="my-organization-uses-the-human-resources-app-for-teams-will-the-app-continue-to-work-after-the-infrastructure-change-is-completed"></a>Mana organizācija izmanto Human Resourcesprogrammu programmai Teams. Vai šī programma turpinās darbu pēc infrastruktūras izmaiņu pabeigšanas?

Jā, Human Resources programma programmai Teams turpinās darbu pēc migrācijas uz jauno infrastruktūru.

### <a name="my-organization-has-configured-custom-security-in-dynamics-365-human-resources-will-our-custom-security-still-be-applied-after-the-infrastructure-change-is-completed"></a>Mana organizācija ir konfigurējusi pielāgotu drošību programmā Dynamics 365 Human Resources. Vai mūsu pielāgotā drošība joprojām tiks pielietota pēc infrastruktūras izmaiņu pabeigšanas?

Jā, pielāgotās drošības konfigurācijas tiks ietvertas datu migrācijā uz jauno infrastruktūru.

### <a name="we-are-using-data-integrator-to-move-data-between-dynamics-365-human-resources-and-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected"></a>Datu integrētājs tiek izmantots, lai pārvietotu datus starp programmām Dynamics 365 Human Resources un Finance and Operations. Kā dati, kas pašlaik tiek integrēti, tiks ietekmēti?

HR dati, kas pašlaik ir šablonēti Dynamics 365 Human Resources, ir sinhronizēti ar Dataverse. Pēc tam datu integrētāju var izmantot vienvirziena sinhronizācijai ar Finance and Operations programmām. Pēc jaunās infrastruktūras migrācijas HR dati būs Finance and Operations programmu pamatdati. Datu integrētājs vairs nebūs nepieciešams, lai sinhronizētu datus starp Finance and Operations programmām un Human Resources.

Pašreizējās Dataverse Human Resources pamatdatu tabulas turpinās sinhronizēt vides datus jaunajai infrastruktūrai. Entītijas tiks konvertētas, lai atbalstītu dubulto rakstīšanu. Jebkuras citas datu integrācijas, kas ar šo tabulu ir konfigurētas, izmantojot datu integrētāju, citās Dynamics 365 programmās turpinās darboties tāpat, kā tās pašreiz tiek konfigurētas.

### <a name="we-are-using-dual-write-to-move-hr-data-between-dataverse-and-other-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected-by-the-migration-to-the-new-infrastructure"></a>Mēs izmantojam dubultās rakstīšanas funkciju, lai pārvietotu HR datus starp Dataverse un citām Finance and Operations programmām. Kā datus, kas pašlaik tiek integrēti, ietekmēs migrācija uz jauno infrastruktūru?

HR dati būs Finance and Operations programmu pamatdati vidē jaunajā infrastruktūrā. Duālā rakstīšana tiks izmantota HR datu pārvietošanai starp jauno vidi un Dataverse vidi.

### <a name="we-have-built-custom-integrations-from-dynamics-365-human-resources-to-one-or-more-external-systems-will-we-have-to-develop-new-integrations-after-the-infrastructure-change-is-completed"></a>Mēs esam izveidojuši pielāgotas integrācijas no Dynamics 365 Human Resources uz vienu vai vairākām ārējām sistēmām. Vai mums būs jāattīsta jaunas integrācijas pēc infrastruktūras izmaiņu pabeigšanas?

Tas ir atkarīgs no integrācijas galapunkta. Plašāku informāciju par Finance and Operations lietojumprogrammās pieejamām integrācijas tehnoloģijas un par to, kā izvēlēties labāko integrācijas tehnoloģiju, skatiet [Integrācijas pārskatu](../fin-ops-core/dev-itpro/data-entities/integration-overview.md).

### <a name="we-have-extended-dataverse-for-dynamics-365-human-resources-will-these-extensions-be-migrated-automatically"></a>Mums jāpaplašina Dataverse programmai Dynamics 365 Human Resources. Vai šie paplašinājumi tiks migrēti automātiski?

Ja Dynamics 365 Human Resources un Finance and Operations vides, kas tiks apvienotas jaunās infrastruktūras vidē, ir saistītas ar vienu un to pašu Dataverse vidi, divas programmas turpinās savienoties ar vienu un to pašu Dataverse vidi pēc migrācijas. Tāpēc visiem Dataverse paplašinājumiem migrācija nav nepieciešama.

Tomēr, ja Dynamics 365 Human Resources un Finance and Operations pašlaik ir savienoti ar atsevišķām Dataverse vidēm, divas Dataverse vides būs jāapvieno tā, lai tie būtu savienoti ar vienotu vidi jaunajā infrastruktūrā. Šai Dataverse migrācijai Dataverse tabulas, kas ir Human Resources risinājumu standarts, var savienot ar jauno Dataverse vidi un unsinhronizēt ar to. Tomēr visi Dataverse vides paplašinājumi netiks migrēti automātiski, bet ir atkārtoti jā izvietošana jaunajā vidē. Ir ieteicams izmantot pārvaldītus risinājumus, lai pārvaldītu Dataverse paplašinājumus. Papildinformāciju skatiet sadaļā [Ievads risinājumos](https://docs.microsoft.com/powerapps/developer/data-platform/introduction-solutions).

### <a name="we-have-configured-microsoft-power-automate-flows-andor-microsoft-power-apps-to-work-with-dynamics-365-human-resources-will-these-microsoft-power-platform-components-be-migrated-and-work-automatically-after-the-infrastructure-change-is-completed"></a>Ir konfigurētas Microsoft Power Automate plūsmas un/vai Microsoft Power Apps darbam ar Dynamics 365 Human Resources. Vai šie Microsoft Power Platform komponenti tiks migrēti un darbojas automātiski pēc infrastruktūras izmaiņu pabeigšanas?

Power Apps, Power Automate plūsmas un citi Microsoft Power Platform pielāgojumi ir līdzīgi Dataverse paplašinājumiem. Tas, vai pēc migrācijas uz jauno infrastruktūru tie darbojas automātiski, ir atkarīgs no tā, vai Human Resources programma un Finance and Operations programmas pirms migrācijas ir saistītas ar vienu un to pašu Power Apps vidi.

Ja programmas pašlaik ir saistītas ar vienu Power Apps vidi, tās turpinās būt saistītas ar šo Power Apps vidi pēc jaunās infrastruktūras migrācijas. Šajā gadījumā Power Apps, Power Automate plūsmas un citi Microsoft Power Platform pielāgojumi turpinās darbu, nekonfigurējot papildu konfigurāciju. Ir ieteicams izmantot pārvaldītus risinājumus, lai pārvaldītu programmu paplašinājumus Dataverse. Papildinformāciju skatiet sadaļā [Ievads risinājumos](https://docs.microsoft.com/powerapps/developer/data-platform/introduction-solutions).

Tomēr, ja Human Resources programma un Finance and Operations programmas ir saistītas ar atsevišķām Power Apps vidēm, tās būs jāapvieno kā daļa no migrācijas. Šim uzdevumam būs nepieciešams, lai visi Power Apps un citi pielāgojumi tiktu atkārtoti izvietoti jaunajā vidē.

### <a name="we-have-enabled-dataverse-virtual-tables-for-dynamics-365-human-resources-what-will-happen-to-these-tables-during-the-migration"></a>Mums ir iespējotas Dataverse virtuālās tabulas programmai Dynamics 365 Human Resources. Kas ar šīm tabulām notiks migrācijas laikā?

Pēc migrācijas, ja jaunās infrastruktūras vide joprojām ir saistīta ar Dataverse vidi, kas pašreiz ir saistīta ar Dynamics 365 Human Resources, šajā vidē ģenerētās Dataverse virtuālās tabulas turpinās darbu, nekonfigurējot papildu konfigurāciju.

Tomēr, ja jaunās infrastruktūras vide ir saistīta ar citu Dataverse vidi pēc migrācijas, virtuālās tabulas būs jāģenerē jaunā Dataverse vidē.

### <a name="we-have-developed-an-integration-by-using-the-applicant-tracking-system-ats-api-payroll-api-dataverse-virtual-tables-for-dynamics-365-human-resources-or-other-entities-in-the-dataverse-web-api-will-these-integrations-continue-to-work-after-the-infrastructure-change-is-completed"></a>Esam izveidojuši integrāciju, izmantojot Kandidātu izsekošanas sistēmas (ATS) API, Algas API, Dataverse virtuālās tabulas Dynamics 365 Human Resources vai citas entītijas Dataverse tīmekļa API. Vai šīs integrācijas turpinās darbu pēc infrastruktūras izmaiņu pabeigšanas?

Pēc migrācijas, ja jaunās infrastruktūras vide joprojām ir saistīta ar Dataverse vidi, kas pašreiz ir saistīta ar Dynamics 365 Human Resources, visas integrācijas, kas ir izstrādātas pret Dataverse tīmekļa API turpinās darbu pēc migrācijas pabeigšanas.

Tomēr, ja jaunās infrastruktūras vide joprojām ir saistīta ar citu Dataverse vidi pēc migrācijas, visas integrācijas, kas ir izstrādātas pret Dataverse tīmekļa API būs jāpārkonfigurē, lai izveidotu savienojumu ar jauno Dataverse vidi.

### <a name="is-there-an-impact-on-the-azure-region-when-my-environment-is-migrated"></a>Vai, migrējot vidi, pastāv Azure reģiona ietekme?

Ir paredzams, ka migrācijas laikā Human Resources vide parasti paliks tajā pašā Azure reģionā. Vienīgais izņēmums rodas, ja cilvēkresursu vide tiks sapludināta ar Finance and Operations vidi, kas atrodas citā reģionā. Šādā gadījumā cilvēkresursu vide tiks migrēta uz Finance and Operations vides Azure reģionu.

### <a name="my-organization-depends-on-workflows-in-dynamics-365-human-resources-for-one-or-more-business-processes-will-the-workflows-be-migrated-automatically"></a>Mana organizācija ir atkarīga no darbplūsmām programmā Dynamics 365 Human Resources vienam vai vairākiem biznesa procesiem. Vai darbplūsmas tiks migrētas automātiski?

Jā, darbplūsmas konfigurācijas, darbplūsmas vēsture un pašreizējās procesā esošās darbplūsmas tiks migrētas.

### <a name="what-training-and-resources-will-be-available-to-help-with-the-migration-process"></a>Kādas apmācības un resursi būs pieejami, lai palīdzētu migrācijas procesā?

Tiks sniegta pilna dokumentācija, lai detalizēti aprakstītu katru migrācijas procesa darbību. Atkarībā no nepieciešamības var būt pieejami arī papildu apmācības resursi, piemēram, video un darbnīcas.

### <a name="my-organization-has-created-saved-views-in-dynamics-365-human-resources-to-improve-the-usability-of-the-interface-will-the-saved-views-be-migrated-automatically"></a>Mana organizācija ir izveidojusi saglabātos skatus programmā Dynamics 365 Human Resources, lai uzlabotu interfeisa izmantojamību. Vai Saglabātie skati tiks migrēti automātiski?

Jā, saglabātie skati tiks migrēti uz jauno infrastruktūru.

### <a name="we-are-using-ceridian-with-dynamics-365-human-resources-will-the-ceridian-integration-be-available-after-the-infrastructure-change-is-completed"></a>Mēs izmantojam Ceridian ar Dynamics 365 Human Resources. Vai Ceridian integrācija būs pieejama pēc infrastruktūras izmaiņu pabeigšanas? 

Integrācija ar Ceridian tiks migrēta uz algas API balstīto integrāciju. Uz failiem balstīta integrācija, kas pašlaik pastāv Dynamics 365 Human Resources, netiks migrēta uz Finance and Operations infrastruktūru. Papildinformāciju skatiet sadaļā [Algas API ievads](./hr-admin-integration-payroll-api-introduction.md).

### <a name="how-will-the-migration-affect-the-service-update-process"></a>Kā migrācija ietekmēs pakalpojuma atjaunināšanas procesu?

Pēc migrācijas debitori būs daudz elastīgāki attiecībā uz ALM un pakalpojumu atjauninājumiem. Human Resources vidēs pakalpojumu atjauninājumi vairs netiks lietoti automātiski. Tā vietā pakalpojums sekos Vienas versijas pakalpojuma atjaunināšanas procesiem un funkcionalitātei. Tādēļ konfigurācijas opcijas atjauninājumiem būs pieejamas, izmantojot LCS. Papildinformāciju skatiet tēmā [Vienas versijas pārskats](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="how-will-the-migration-affect-my-lcs-project-for-dynamics-365-human-resources"></a>Kā migrācija ietekmēs manu LCS projektu Dynamics 365 Human Resources?

Migrācija uz jauno infrastruktūru pārvietos jūsu Dynamics 365 Human Resources vides pārvaldību uz LCS ieviešanas projektu. Ja migrācija sapludina Dynamics 365 Human Resources ar esošu Finance and Operations vidi, Human Resources LCS projekts tiks sapludināts programmas Finance and Operations LCS ieviešanas projektā. Ja pašlaik izmantojat tikai Dynamics 365 Human Resources, tiks izveidots jauns LCS ieviešanas projekts un esošais Human Resources LCS projekts tiks migrēts uz jauno projektu.

Jaunais projekts būs tas pats projekta tips, ko Finance and Operations programmas izmanto. Tam būs tādas pašas funkcijas un funkcionalitāte vides pārvaldībai. Papildinformāciju skatiet šeit: [Lifecycle Services resursi](../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

### <a name="we-have-linked-our-task-recordings-to-the-business-process-modeler-in-human-resources-how-will-the-business-process-modeler-be-migrated-and-merged-into-lcs"></a>Mēs esam saistījuši savus uzdevumu ierakstus ar biznesa procesu modelētāju programmā Human Resources. Kā biznesa procesa modelētājs tiks migrēts un sapludināts LCS?

LCS projekta biznesa procesu bibliotēkas tiks migrētas uz Human Resources jauno LCS projektu.

### <a name="my-organization-currently-uses-only-dynamics-365-human-resources-what-resources-are-available-so-that-we-can-learn-more-about-the-development-capabilities-after-the-infrastructure-change-is-completed"></a>Mana organizācija pašlaik izmanto tikai Dynamics 365 Human Resources. Kādi resursi ir pieejami, lai mēs varētu vairāk uzzināt par izstrādes iespējām pēc infrastruktūras izmaiņu pabeigšanas?

Gan Microsoft Power Platform paplašināmības opcijas, gan Finance and Operations paplašināmības opcijas būs pieejamas, un tās var izmantot izstrādei. Papildinformāciju skatiet sadaļā [Mājas lapas izstrāde un pielāgošana](../fin-ops-core/dev-itpro/dev-tools/developer-home-page.md).

### <a name="we-have-enabled-features-in-dynamics-365-human-resources-will-these-features-be-enabled-automatically-during-the-migration"></a>Mēs esam iespējojuši līdzekļus programmā Dynamics 365 Human Resources. Vai šie līdzekļi tiks automātiski iespējoti migrācijas laikā?

Tas, vai līdzeklis jaunajā infrastruktūrā ir iespējots automātiski, tiks noteikts katram līdzeklim atsevišķi. Šī informācija tiks ietverta funkcionalitātes dokumentācijā.

### <a name="what-happens-to-my-byod-database-during-the-migration"></a>Kas migrācijas laikā notiek ar manu BYOD datu bāzi?

Importa un eksporta konfigurācijas jūsu datu bāzei (BYOD) tiks migrētas uz jauno infrastruktūru.

### <a name="what-happens-to-my-azure-data-lake-during-the-migration"></a>Kas migrācijas laikā notiek ar manu Azure Data Lake?

Jebkurš eksports, kas pašlaik ir konfigurēts Azure Data Lake Storage pakalpojuma Finance and Operations programmām, pēc migrācijas uzturēs to pašu konfigurāciju.

### <a name="we-are-currently-using-dynamics-ax-2012-will-the-upgrade-tools-that-are-currently-available-be-used-to-upgrade-the-hr-module-in-ax-2012-to-dynamics-365-human-resources"></a>Pašlaik tiek izmantots Dynamics AX 2012. Vai jaunināšanas rīki, kas pašlaik ir pieejami, tiks izmantoti HR moduļa jaunināšanai AX 2012 uz Dynamics 365 Human Resources?

Jā. Dynamics 365 Human Resources tiks iekļauts sapludināto kodu bāzē un Finance and Operations programmu infrastruktūras sarakstā. Jauninājums no Dynamics AX 2012 uz Dynamics 365 Human Resources izmantos to pašu jaunināšanas ceļu un rīku, kas tiek izmantots, lai jauninātu Finance and Operations uz jaunāko programmu versiju.

### <a name="we-use-document-handling-with-dynamics-365-human-resources-what-will-happen-to-the-documents-during-the-migration"></a>Mēs izmantojam Dokumentu apstrādi ar Dynamics 365 Human Resources. Kas ar dokumentiem notiks migrācijas laikā?

Dokumenti paliks esošajā dokumentu krātuvē. Tie tiks mainīti attiecībā uz vidi jaunajā infrastruktūrai.

### <a name="what-happens-to-the-batch-jobs-that-we-have-configured-in-dynamics-365-human-resources-after-the-migration"></a>Kas notiek ar pakešuzdevumiem, ko mēs esam konfigurējuši Dynamics 365 Human Resources pēc migrācijas?

Piemērojamie pakešuzdevumi automātiski tiks migrēti uz jauno infrastruktūru.

## <a name="licensing-impact"></a>Licencēšanas ietekme

Šī dokumentācija neaizstāj nevienu no juridiskajām dokumentācijām, kas ietver izmantošanas tiesības.

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-does-our-licensing-or-cost-change"></a>Mana organizācija izmanto Dynamics 365 Human Resources, lai pārvaldītu savas HR operācijas. Vai mūsu licencēšana vai izmaksas mainās?

Debitori, kas iegādājušies Dynamics 365 Human Resources licences, netiks ietekmēti. Šim debitoram nav licencēšanas migrācijas. Papildu noliktavas vienība (NV), kas bija raksturīga Human Resources, vairs netiks piemērota. Tā vietā debitori var izvēlēties pirkt Finance and Operations lietojumprogrammu 2. līmeņa smilškasti ar nedaudz zemāku cenu. Esošie debitori, kas iegādājušies Human Resources smilškasti, būs migrēti uz Finance and Operations lietojumprogrammu 2. līmeņa smilškasti bez papildu izmaksām.

### <a name="my-organization-uses-dynamics-365-human-resources-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-does-my-licensing-or-cost-change"></a>Mana organizācija izmanto Dynamics 365 Human Resources programmās Dynamics 365 Finance, Supply Chain Management, Commerce vai Project Operations. Vai mana licencēšana vai izmaksas mainās?

Esošie Dynamics 365 programmu lietotāji un lietotāji, kuriem ir savrupa Dynamics 365 Finance, Supply Chain Management, Commerce un Project Operations, var piekļūt Human Resources kā daļai no šīm licencēm līdz 2025. gada februārim vai līdz pašreizējā licencēšanas līguma termiņa beigām neatkarīgi no tā, kas ir agrāk. Varat izvēlēties pārvietoties Human Resources licencēm agrāk, ja tas palīdz sasniegt labākus izmaksu uzkrājumus. Sākot no 2025. gada februāra visiem esošajiem CHF un EA debitoriem ir jāatrite HR modulis un jāpērk Human Resources licences, lai izmantotu jaunās iespējas, kas tiek pārdotas Finance and Operations programmām.

### <a name="my-organization-is-live-with-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-will-we-be-required-to-purchase-an-additional-environment-to-support-the-infrastructure-merge"></a>Mana organizācija ir tiešsaitē ar Dynamics 365 Finance, Supply Chain Management, Commerce vai Project Operations. Vai tiks pieprasīts iegādāties papildu vidi, lai atbalstītu infrastruktūras sapludināšanu?

Papildu vides nav nepieciešamas, lai atbalstītu infrastruktūras izmaiņas.

### <a name="where-should-i-go-if-i-have-additional-questions-about-product-licensing"></a>Kur lai es vēršos, ja man ir papildu jautājumi par produkta licencēšanu?

Ja jums ir licencēšanas jautājumi, jūs varat atrast papildu informāciju par [Biz Apps Hub – D365 cenu noteikšanu un licencēšanu](https://businessapplications.transform.microsoft.com/resources/pricing-and-licensing?tab=grandfathering). Ja šī informācija nepalīdz atrisināt problēmu, atveriet pieprasījumu ar LicencesQ.
