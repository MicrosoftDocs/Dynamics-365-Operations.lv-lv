---
title: Dynamics 365 Human Resources bieži uzdotie jautājumi par infrastruktūras sapludināšanu
description: Šī tēma sniedz atbildes uz bieži uzdotiem jautājumiem par Microsoft Dynamics 365 Human Resources un Finanšu un operāciju programmu infrastruktūras sapludināšanu.
author: twheeloc
ms.date: 08/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 766ee49c17749841d8acac6637a0262e87e52e92
ms.sourcegitcommit: d38d2fe85dc2497211ba5731617f590029d07145
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/27/2022
ms.locfileid: "8809618"
---
# <a name="dynamics-365-human-resources-infrastructure-merge-faq"></a>Dynamics 365 Human Resources bieži uzdotie jautājumi par infrastruktūras sapludināšanu

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Šī tēma sniedz atbildes uz bieži uzdotiem jautājumiem par Microsoft Dynamics 365 Human Resources un Finanšu un operāciju programmu infrastruktūras sapludināšanu.

## <a name="what-is-the-dynamics-365-human-resources-infrastructure-merge"></a>Kas ir Dynamics 365 Human Resources infrastruktūras sapludināšana?

Dynamics 365 Human Resources ir savrupa programma, kas izmanto atšķirīgu infrastruktūru nekā citas finanšu un operāciju programmas, piemēram, Dynamics 365 Finance, Dynamics 365 Supply Chain Management Dynamics 365 Commerce un Dynamics 365 Project Operations. Infrastruktūras sapludināšana apvienos tajā Dynamics 365 Human Resources pašā infrastruktūras, ko lietojumprogrammas Finanses un operācijas.

## <a name="value-and-benefits-of-the-infrastructure-merge"></a>Infrastruktūras sapludināšanas vērtība un atvieglojumi

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-what-benefits-will-we-see-from-these-changes"></a>Mana organizācija izmanto Dynamics 365 Human Resources, lai pārvaldītu savas HR operācijas. Kādus atvieglojumus mēs redzēsim no šīm izmaiņām?

- Šīs izmaiņas izslēdz vairākas personāla vadības (HR) iespējas programmā Dynamics 365.
- Tie nodrošina gan Microsoft Power Platform paplašināmību, gan biznesa loģikas un funkcionalitātes opciju paplašināšanas veidu.
- Tie nodrošina atbilstību Dynamics 365 Human Resources starp citām finanšu un operāciju programmām lietojumprogrammas Lifecycle Management (LC), Microsoft Dynamics Lifecycle Services (LCS), ģeogrāfiskā pieejamības, paplašināmības un citas informācijas ziņā.
- Tie ļauj izmantot koplietoto pakalpojumu un rīku sniegtās priekšrocības un palīdzēt samazināt izmaksas.

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-benefits-will-we-see-from-these-changes"></a>Mana organizācija izmanto Cilvēkresursu moduli Dynamics 365 Finanses, Piegādes ķēžu pārvaldība, Komercija vai Projekta operācijas. Kādus atvieglojumus mēs redzēsim no šīm izmaiņām?

Iespēja un ieguldījumi, kas ir Dynamics 365 Human Resources veikti, tagad būs pieejami debitoriem, kuri izmanto HR moduli Dynamics 365 finansēs. Dažas no šīm iespējām ir atvaļinājumu un prombūtnes pārvaldība, atvieglojumu pārvaldība un uzdevumu pārvaldība.

### <a name="will-i-lose-any-features-or-capabilities-that-i-currently-use"></a>Vai zaudēšu visus līdzekļus vai iespējas, ko es pašlaik izmantoju?

Finanšu un operāciju programmās starp moduli Dynamics 365 Human Resources UN HR būs funkcionāla pārība. Dynamics 365 Human Resources funkcijām būs augstāka prioritāte. Papildinformāciju skatiet [Līdzekļu pārvaldības pārskatā](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="will-the-experience-change-for-my-users"></a>Vai pieredzes izmaiņas radīsies maniem lietotājiem?

Jaunās HR iespējas tiks pārvaldītas, izmantojot līdzekļu pārvaldību. Debitori izlems, vai viņi vēlas tos izmantot. Dažos gadījumos var tikt mainītas iespējas. Šajos gadījumos tiks sniegta dokumentācija.

### <a name="how-does-this-change-affect-me-if-i-am-an-existing-customer-and-i-use-both-the-hr-module-on-the-finance-and-operations-infrastructure-and-dynamics-365-human-resources-through-custom-integrations"></a>Kā šīs izmaiņas ietekmē mani, ja es esmu esošs debitors, un es izmantoju gan Finanšu Dynamics 365 Human Resources un operāciju infrastruktūras MODULI, gan ar pielāgotām integrācijām?

Pielāgotas integrācijas starp Dynamics 365 Human Resources moduli HR un programmatūrā Dynamics 365 Finanses vairs nebūs nepieciešamas. Visi HR dati atrodas tajā pašā datu bāzē, kurā atrodas pārējās Finanšu un operāciju programmas.

## <a name="migration-from-dynamics-365-human-resources-to-finance-and-operations-apps"></a>Migrācija no Dynamics 365 Human Resources finanšu un operāciju programmām

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-hr-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>Mana organizācija izmanto Dynamics 365 Human Resources, lai pārvaldītu HR operācijas. Kas mums ir jāplāno, lai pārietu uz jauno pieredzi?

Ja jūsu organizācija izmanto Dynamics 365 Human Resources, bet neizmanto citas finanšu un operāciju programmas, jūsu Cilvēkresursu vide tiks migrēta uz jauno infrastruktūru. Liela daļa šī migrācijas procesa tiks automatizēta. Tiks veikti procesi, lai migrētu datu bāzi un sinhronizētu to ar jauno infrastruktūru.

Turklāt, izmantojot rīkus, varat pārbaudīt migrācijas procesu un pārbaudīt datus un pieredzi pirms ražošanas vides migrēšanas.

Ja jūsu organizācija izmanto gan finanšu Dynamics 365 Human Resources, gan operāciju programmas, jums jāplāno vairāk laika validācijai, lai nodrošinātu, ka dati tiek pareizi migrēti jaunajā vidē. Migrācija uz jauno infrastruktūru saplūdīs ar jūsu Cilvēkresursu vides datiem finanšu un operāciju vidē. Tomēr konfliktējošu datu gadījumā būs nepieciešama lietotāja ievadne, lai noteiktu, kā konflikts jāatrisina. Lietotājiem un administratoriem būs jāpārvalda datu kartēšana, kur ir konflikti, un jātestē migrācija smilškastu vidēs pirms ražošanas vides migrācijas.

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-what-do-we-have-to-plan-for-to-migrate-to-the-new-experience"></a>Mana organizācija izmanto Cilvēkresursu moduli Dynamics 365 Finanses, Piegādes ķēžu pārvaldība, Komercija vai Projekta operācijas. Kas mums ir jāplāno, lai pārietu uz jauno pieredzi?

Organizācijām, kas izmanto HR moduli Finanšu un operāciju programmās, jūsu videi tiks pielietota jaunā funkcionalitāte, Dynamics 365 Human Resources izmantojot standarta vienas versijas atjaunināšanas procesu. Ir paredzams, ka jūsu vidē jaunā funkcionalitāte būs pieejama katrā atjauninājumā. Funkciju pārvaldību var izmantot, lai ieslēgtu jaunas funkcijas, tomēr šo funkciju pār validēšanas plāns. Ievērojiet procesus, kas jums ir pieejami citu vides atjauninājumu validēšana. Papildinformāciju par atjauninājumu piemērošanu Finanšu un operāciju programmām skatiet sadaļā Vienas [versijas apskats](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="when-will-my-organization-be-migrated"></a>Kad mana organizācija tiks migrēta?

Katras organizācijas migrācija būs atkarīga no tās pašreizējās konfigurācijas un gatavības migrēt uz jauno infrastruktūru. Šos datumus var mainīt.

- Organizācijas, kas izmanto moduli HR finanšu un operāciju programmās, saņems HR funkcionalitāti Dynamics 365 Human Resources kā daļu no parastā vienas versijas atjaunināšanas procesa. Ir plānots, ka jaunās funkcijas kļūs plaši pieejamas, sākot no 2022. gada janvāra.
- Organizācijām, kas pašlaik izmanto tikai Dynamics 365 Human Resources būs piekļuve migrācijas rīkiem, lai tie varētu sākt testēšanu un sākt migrāciju, kas sāksies 2022. gada vidū. Datums, kad jāveic migrācija uz jauno infrastruktūru, vēl nav noteikts. Tomēr tas būs vismaz gadu pēc dienas, kad būs pieejami migrācijas rīki.
- Organizācijām, kas izmanto gan finanšu Dynamics 365 Human Resources, gan operāciju programmas, būs piekļuve migrācijas rīkam, lai tās varētu sākt pārbaudi un sākt migrācijas sākumu 2022. gada beigās. Datums, kad jāveic migrācija uz jauno infrastruktūru, vēl nav noteikts. Tomēr tas būs vismaz gadu pēc dienas, kad būs pieejami migrācijas rīki.

Papildinformāciju par jaunajām Dynamics 365 Human Resources funkcijām skatiet sadaļā [Jaunumi vai izmaiņas programmā Human Resources](./hr-admin-whats-new.md).

### <a name="my-organization-has-not-yet-gone-live-on-dynamics-365-human-resources-should-we-go-live-with-the-human-resources-module-in-the-finance-and-operations-apps-or-with-the-dynamics-365-human-resources-app-on-the-legacy-infrastructure"></a>Mana organizācija vēl nav pārgājusi Dynamics 365 Human Resources tiešsaistē. Vai mēs ejam kopā ar cilvēkresursu moduli, kas atrodas Finanšu un operāciju programmās vai Dynamics 365 Human Resources ar programmu mantojuma infrastruktūrai?

Svarīgi elementi ir apsvērt, kāda HR funkcionalitāte ir nepieciešama un kad šī funkcionalitāte būs pieejama jaunajā infrastruktūrai. Ja organizācijai ir nepieciešama personāla vadības pamatfunkcionalitāte, kas pašlaik ir pieejama jaunā infrastruktūras finanšu un operāciju programmu HR modulī. Līdzekļu pārība starp Finanšu un operāciju programmu HR Dynamics 365 Human Resources moduli un programmu ir paredzēta 10.0.25. laidienā, kas ir plānots kā plaši pieejams 2022. gada martā. Vēlākos laidienos būs pieejami programmas Teams un Dataverse entītijas integrācijas līdzekļi.

Ja organizācijas HR funkcionalitātei būs jābūt pieejamai jaunajā infrastruktūrai laika periodā, kurā organizācija ietu, var būt vieglāk atrast Cilvēkresursu moduli Finanšu un operāciju programmās. Tā rezultātā radīsies vieglāka migrācija, jo tā būs programmas standarta jaunināšana uz Dynamics 365 Human Resources programmu, un klients jau būs jaunajā infrastruktūrā. Ja organizācija izlemj doties tiešsaistē Dynamics 365 Human Resources programmā, tad, lai pārietu uz jauno infrastruktūru, nepieciešama vides migrācija. Tas var izvairīties, veicot jaunās infrastruktūras nosācāmo darbību.

### <a name="i-am-using-new-capabilities-that-are-available-only-in-dynamics-365-human-resources-such-as-leave-and-absence-and-benefits-management-will-these-capabilities-now-be-available-in-the-human-resources-module-on-the-finance-and-operations-infrastructure-too"></a>Es izmantoju jaunas iespējas, kas pieejamas tikai programmā Dynamics 365 Human Resources (piemēram, **Atvaļinājums un prombūtne** un **Atvieglojumu pārvaldība**). Vai šīs iespējas tagad būs pieejamas arī Finanšu un operāciju infrastruktūras modulī Personāla vadība?

Jā, visi moduļi no Dynamics 365 Human Resources darbosies tāpat kā Finanšu un operāciju programmās, un būs 100 procentu funkcionalitātes pārība. Kā daļa no vispārējās migrācijas stratēģijas klientiem, kas pašlaik izmanto šīs iespējas HR, debitoru dati tiks migrēti tā, lai tie turpina darbu finanšu un operāciju infrastruktūrai.

### <a name="i-use-the-new-dynamics-365-human-resources-benefits-management-capabilities-ive-built-custom-integrations-with-the-hr-module-on-the-finance-and-operations-infrastructure-so-that-i-can-take-advantage-of-the-payroll-capabilities-by-using-benefits-data-will-these-custom-integrations-be-required-going-forward"></a>Es izmantoju jaunās Dynamics 365 Human Resources atvieglojumu pārvaldības iespējas. Es esmu izveidojis pielāgotas integrācijas ar Finanšu un operāciju infrastruktūras moduli HR, lai varētu izmantot algu spēju priekšrocības, izmantojot atvieglojumu datus. Vai šīs pielāgotās integrācijas būs nepieciešamas turpmāk?

Kā daļa no infrastruktūras sapludināšanas HR dati tiek ievadīti tajā pašā datu bāzē, kurā atrodas pārējās finanšu un operāciju programmas. Integrācija starp moduļiem Finanšu un operāciju programmās vairs nebūs nepieciešama.

### <a name="my-organization-uses-one-or-more-isv-solutions-with-dynamics-365-human-resources-will-our-isv-solutions-be-migrated-automatically"></a>Mana organizācija izmanto vienu vai vairākus ISV risinājumus ar Dynamics 365 Human Resources. Vai mūsu ISV risinājumi tiks migrēti automātiski?

Migrācijas pieredze katram neatkarīgam programmatūras izstrādātāja (ISV) risinājumam atšķirsies atkarībā no risinājuma integrācijas metodes. Korporācija Microsoft strādās cieši ar ISVs, lai nodrošinātu gludu pāreju uz jauno infrastruktūru.

### <a name="my-organization-uses-linkedin-talent-hub-integration-with-dynamics-365-human-resources-will-this-integration-continue-to-work-after-the-infrastructure-change-is-completed"></a>Mana organizācija izmanto LinkedIn Talantu Hub integrāciju ar Dynamics 365 Human Resources. Vai šī integrācija turpinās darbu pēc infrastruktūras izmaiņu pabeigšanas?

Nē, LinkedIn Talent Hub integrācija neturpinās darbu pēc migrācijas uz jauno infrastruktūru. Pakalpojums LinkedIn Talent Hub integrācijai tiks noņemts ar mantojuma Dynamics 365 Human Resources infrastruktūru.

### <a name="my-organization-uses-the-human-resources-app-for-teams-will-the-app-continue-to-work-after-the-infrastructure-change-is-completed"></a>Mana organizācija izmanto Human Resourcesprogrammu programmai Teams. Vai šī programma turpinās darbu pēc infrastruktūras izmaiņu pabeigšanas?

Jā, Human Resources programma programmai Teams turpinās darbu pēc migrācijas uz jauno infrastruktūru.

### <a name="my-organization-has-configured-custom-security-in-dynamics-365-human-resources-will-our-custom-security-still-be-applied-after-the-infrastructure-change-is-completed"></a>Mana organizācija ir konfigurējusi pielāgotu drošību programmā Dynamics 365 Human Resources. Vai mūsu pielāgotā drošība joprojām tiks pielietota pēc infrastruktūras izmaiņu pabeigšanas?

Jā, pielāgotās drošības konfigurācijas tiks ietvertas datu migrācijā uz jauno infrastruktūru.

### <a name="we-are-using-data-integrator-to-move-data-between-dynamics-365-human-resources-and-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected"></a>Mēs izmantojam datu integrētāju, lai pārvietotu datus starp programmām Finanses Dynamics 365 Human Resources un Operācijas. Kā dati, kas pašlaik tiek integrēti, tiks ietekmēti?

HR dati, kas pašlaik ir šablonēti Dynamics 365 Human Resources, ir sinhronizēti ar Dataverse. Pēc tam datu integrētāju var izmantot vienvirziena sinhronizācijai ar finanšu un operāciju programmām. Pēc migrācijas uz jauno infrastruktūru HR dati būs pamatdati finanšu un operāciju programmām. Datu integrētājs vairs nebūs nepieciešams datu sinhronizēšanai starp Finanšu un operāciju programmām un Cilvēkresursiem.

Pašreizējās Dataverse Human Resources pamatdatu tabulas turpinās sinhronizēt vides datus jaunajai infrastruktūrai. Entītijas tiks konvertētas, lai atbalstītu dubulto rakstīšanu. Jebkuras citas datu integrācijas, kas ar šo tabulu ir konfigurētas, izmantojot datu integrētāju, citās Dynamics 365 programmās turpinās darboties tāpat, kā tās pašreiz tiek konfigurētas.

### <a name="we-are-using-dual-write-to-move-hr-data-between-dataverse-and-other-finance-and-operations-apps-how-will-the-data-that-is-currently-being-integrated-be-affected-by-the-migration-to-the-new-infrastructure"></a>Mēs izmantojam dubultās rakstīšanas funkciju, lai pārvietotu HR datus starp citām Dataverse finanšu un operāciju programmām. Kā datus, kas pašlaik tiek integrēti, ietekmēs migrācija uz jauno infrastruktūru?

HR dati būs pamatā Finanšu un operāciju programmām jaunās infrastruktūras vidē. Duālā rakstīšana tiks izmantota HR datu pārvietošanai starp jauno vidi un Dataverse vidi.

### <a name="we-have-built-custom-integrations-from-dynamics-365-human-resources-to-one-or-more-external-systems-will-we-have-to-develop-new-integrations-after-the-infrastructure-change-is-completed"></a>Mēs esam izveidojuši pielāgotas integrācijas no Dynamics 365 Human Resources uz vienu vai vairākām ārējām sistēmām. Vai mums būs jāattīsta jaunas integrācijas pēc infrastruktūras izmaiņu pabeigšanas?

Tas ir atkarīgs no integrācijas galapunkta. Plašāku informāciju par integrācijas tehnoloģijas, kas ir pieejamas Finanšu un operāciju programmās, un par to, kā izvēlēties labāko integrācijas tehnoloģiju, skatiet Integrācijas [pārskatu](../fin-ops-core/dev-itpro/data-entities/integration-overview.md).

### <a name="we-have-extended-dataverse-for-dynamics-365-human-resources-will-these-extensions-be-migrated-automatically"></a>Mums jāpaplašina Dataverse programmai Dynamics 365 Human Resources. Vai šie paplašinājumi tiks migrēti automātiski?

Ja finanšu Dynamics 365 Human Resources un operāciju vides, kas tiks apvienotas vidē ar jauno infrastruktūru, ir saistītas ar vienu un to pašu vidi, šīs divas programmas turpinās savienoties ar vienu un to Dataverse Dataverse pašu vidi pēc migrācijas. Tāpēc visiem Dataverse paplašinājumiem migrācija nav nepieciešama.

Tomēr, Dynamics 365 Human Resources Dataverse ja finanšu un operāciju vides pašlaik ir saistītas ar atsevišķām vidēm, Dataverse šīs divas vides būs jāapvieno, lai tās būtu saistītas ar vienu jaunās infrastruktūras vidi. Šai Dataverse migrācijai Dataverse tabulas, kas ir Human Resources risinājumu standarts, var savienot ar jauno Dataverse vidi un unsinhronizēt ar to. Tomēr visi Dataverse vides paplašinājumi netiks migrēti automātiski, bet ir atkārtoti jāizvieto jaunajā vidē. Ir ieteicams izmantot pārvaldītus risinājumus, lai pārvaldītu Dataverse paplašinājumus. Papildinformāciju skatiet sadaļā [Ievads risinājumos](/powerapps/developer/data-platform/introduction-solutions).

### <a name="we-have-utilized-the-custom-field-functionality-within-dynamics-365-human-resources-will-those-custom-fields-migrate-automatically"></a>Ietvaros esam izmantojuši pielāgoto lauka funkcionalitāti, vai Dynamics 365 Human Resources šie pielāgotie lauki tiks migrēti automātiski?
Jā, pievienotie pielāgotie lauki tiks migrēti uz jauno infrastruktūru.

### <a name="we-have-configured-microsoft-power-automate-flows-andor-microsoft-power-apps-to-work-with-dynamics-365-human-resources-will-these-microsoft-power-platform-components-be-migrated-and-work-automatically-after-the-infrastructure-change-is-completed"></a>Ir konfigurētas Microsoft Power Automate plūsmas un/vai Microsoft Power Apps darbam ar Dynamics 365 Human Resources. Vai šie Microsoft Power Platform komponenti tiks migrēti un darbojas automātiski pēc infrastruktūras izmaiņu pabeigšanas?

Power Apps, Power Automate plūsmas un citi Microsoft Power Platform pielāgojumi ir līdzīgi Dataverse paplašinājumiem. Tas, vai tās automātiski darbojas pēc migrācijas uz jauno infrastruktūru, ir atkarīgs no tā, vai cilvēkresursu programma un finanšu un operāciju programmas ir saistītas ar vienu Power Apps vidi pirms migrācijas.

Ja programmas pašlaik ir saistītas ar vienu Power Apps vidi, tās turpinās būt saistītas ar šo Power Apps vidi pēc jaunās infrastruktūras migrācijas. Šajā gadījumā Power Apps, Power Automate plūsmas un citi Microsoft Power Platform pielāgojumi turpinās darbu, nekonfigurējot papildu konfigurāciju. Ir ieteicams izmantot pārvaldītus risinājumus, lai pārvaldītu programmu paplašinājumus Dataverse. Papildinformāciju skatiet sadaļā [Ievads risinājumos](/powerapps/developer/data-platform/introduction-solutions).

Tomēr, ja Cilvēkresursu programma un Finanšu un operāciju programmas Power Apps ir saistītas ar atsevišķām vidēm, tās būs jāapvieno kā daļa no migrācijas. Šim uzdevumam būs nepieciešams, lai visi Power Apps un citi pielāgojumi tiktu atkārtoti izvietoti jaunajā vidē.

### <a name="we-have-enabled-dataverse-virtual-tables-for-dynamics-365-human-resources-what-will-happen-to-these-tables-during-the-migration"></a>Mums ir iespējotas Dataverse virtuālās tabulas programmai Dynamics 365 Human Resources. Kas ar šīm tabulām notiks migrācijas laikā?

Pēc migrācijas, ja jaunās infrastruktūras vide joprojām ir saistīta ar Dataverse vidi, kas pašreiz ir saistīta ar Dynamics 365 Human Resources, šajā vidē ģenerētās Dataverse virtuālās tabulas turpinās darbu, nekonfigurējot papildu konfigurāciju.

Tomēr, ja jaunās infrastruktūras vide ir saistīta ar citu Dataverse vidi pēc migrācijas, virtuālās tabulas būs jāģenerē jaunā Dataverse vidē.

### <a name="we-have-developed-an-integration-by-using-the-applicant-tracking-system-ats-api-payroll-api-dataverse-virtual-tables-for-dynamics-365-human-resources-or-other-entities-in-the-dataverse-web-api-will-these-integrations-continue-to-work-after-the-infrastructure-change-is-completed"></a>Esam izveidojuši integrāciju, izmantojot Kandidātu izsekošanas sistēmas (ATS) API, Algas API, Dataverse virtuālās tabulas Dynamics 365 Human Resources vai citas entītijas Dataverse tīmekļa API. Vai šīs integrācijas turpinās darbu pēc infrastruktūras izmaiņu pabeigšanas?

Pēc migrācijas, ja jaunās infrastruktūras vide joprojām ir saistīta ar Dataverse vidi, kas pašreiz ir saistīta ar Dynamics 365 Human Resources, visas integrācijas, kas ir izstrādātas pret Dataverse tīmekļa API turpinās darbu pēc migrācijas pabeigšanas.

Tomēr, ja jaunās infrastruktūras vide joprojām ir saistīta ar citu Dataverse vidi pēc migrācijas, visas integrācijas, kas ir izstrādātas pret Dataverse tīmekļa API būs jāpārkonfigurē, lai izveidotu savienojumu ar jauno Dataverse vidi.

### <a name="is-there-an-impact-on-the-azure-region-when-my-environment-is-migrated"></a>Vai, migrējot vidi, pastāv Azure reģiona ietekme?

Ir paredzams, ka migrācijas laikā Human Resources vide parasti paliks tajā pašā Azure reģionā. Vienīgais izņēmums ir, ja cilvēkresursu vide tiks sapludināta ar finanšu un operāciju vidi, kas atrodas citā reģionā. Šādā gadījumā cilvēkresursu vide tiks migrēta uz Finanšu un operāciju vides Azure reģionu.

### <a name="my-organization-depends-on-workflows-in-dynamics-365-human-resources-for-one-or-more-business-processes-will-the-workflows-be-migrated-automatically"></a>Mana organizācija ir atkarīga no darbplūsmām programmā Dynamics 365 Human Resources vienam vai vairākiem biznesa procesiem. Vai darbplūsmas tiks migrētas automātiski?

Jā, darbplūsmas konfigurācijas, darbplūsmas vēsture un pašreizējās procesā esošās darbplūsmas tiks migrētas.

### <a name="what-training-and-resources-will-be-available-to-help-with-the-migration-process"></a>Kādas apmācības un resursi būs pieejami, lai palīdzētu migrācijas procesā?

Tiks sniegta pilna dokumentācija, lai detalizēti aprakstītu katru migrācijas procesa darbību. Atkarībā no nepieciešamības var būt pieejami arī papildu apmācības resursi, piemēram, video un darbnīcas.

### <a name="my-organization-has-created-saved-views-in-dynamics-365-human-resources-to-improve-the-usability-of-the-interface-will-the-saved-views-be-migrated-automatically"></a>Mana organizācija ir izveidojusi saglabātos skatus programmā Dynamics 365 Human Resources, lai uzlabotu interfeisa izmantojamību. Vai Saglabātie skati tiks migrēti automātiski?

Jā, saglabātie skati tiks migrēti uz jauno infrastruktūru.

### <a name="we-are-using-ceridian-with-dynamics-365-human-resources-will-the-ceridian-integration-be-available-after-the-infrastructure-change-is-completed"></a>Mēs izmantojam Ceridian ar Dynamics 365 Human Resources. Vai Ceridian integrācija būs pieejama pēc infrastruktūras izmaiņu pabeigšanas? 

Integrācija ar Ceridian tiks migrēta uz algas API balstīto integrāciju. Uz failu balstīta integrācija, kas pašlaik Dynamics 365 Human Resources pastāv, netiks migrēta uz Finanšu un operāciju infrastruktūru. Papildinformāciju skatiet sadaļā [Algas API ievads](./hr-admin-integration-payroll-api-introduction.md).

### <a name="how-will-the-migration-affect-the-service-update-process"></a>Kā migrācija ietekmēs pakalpojuma atjaunināšanas procesu?

Pēc migrācijas debitori būs daudz elastīgāki attiecībā uz ALM un pakalpojumu atjauninājumiem. Human Resources vidēs pakalpojumu atjauninājumi vairs netiks lietoti automātiski. Tā vietā pakalpojums sekos Vienas versijas pakalpojuma atjaunināšanas procesiem un funkcionalitātei. Tādēļ konfigurācijas opcijas atjauninājumiem būs pieejamas, izmantojot LCS. Papildinformāciju skatiet tēmā [Vienas versijas pārskats](../fin-ops-core/dev-itpro/lifecycle-services/oneversion-overview.md).

### <a name="how-will-the-migration-affect-my-lcs-project-for-dynamics-365-human-resources"></a>Kā migrācija ietekmēs manu LCS projektu Dynamics 365 Human Resources?

Migrācija uz jauno infrastruktūru pārvietos jūsu vides Dynamics 365 Human Resources pārvaldību finanšu un operāciju ieviešanas projektā LCS. Ja migrācija tiek sapludināta Dynamics 365 Human Resources ar esošu finanšu un operāciju vidi, personāla vadības LCS projekts tiks sapludināts LCS ieviešanas projektā programmai Finanses un operācijas. Ja pašlaik izmantojat tikai Dynamics 365 Human Resources, tiks izveidots jauns LCS ieviešanas projekts un esošais Human Resources LCS projekts tiks migrēts uz jauno projektu.

Jaunais projekts būs tas pats projekta tips, ko izmanto Finanšu un operāciju programmas. Tam būs tādas pašas funkcijas un funkcionalitāte vides pārvaldībai. Papildinformāciju skatiet šeit: [Lifecycle Services resursi](../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

### <a name="we-have-linked-our-task-recordings-to-the-business-process-modeler-in-human-resources-how-will-the-business-process-modeler-be-migrated-and-merged-into-lcs"></a>Mēs esam saistījuši savus uzdevumu ierakstus ar biznesa procesu modelētāju programmā Human Resources. Kā biznesa procesa modelētājs tiks migrēts un sapludināts LCS?

LCS projekta biznesa procesu bibliotēkas tiks migrētas uz Human Resources jauno LCS projektu.

### <a name="my-organization-currently-uses-only-dynamics-365-human-resources-what-resources-are-available-so-that-we-can-learn-more-about-the-development-capabilities-after-the-infrastructure-change-is-completed"></a>Mana organizācija pašlaik izmanto tikai Dynamics 365 Human Resources. Kādi resursi ir pieejami, lai mēs varētu vairāk uzzināt par izstrādes iespējām pēc infrastruktūras izmaiņu pabeigšanas?

Gan Microsoft Power Platform paplašināmības opcijas, gan finanšu un operāciju paplašināmības opcijas būs pieejamas, un tās var izmantot izstrādei. Papildinformāciju skatiet sadaļā [Mājas lapas izstrāde un pielāgošana](../fin-ops-core/dev-itpro/dev-tools/developer-home-page.md).

### <a name="we-have-enabled-features-in-dynamics-365-human-resources-will-these-features-be-enabled-automatically-during-the-migration"></a>Mēs esam iespējojuši līdzekļus programmā Dynamics 365 Human Resources. Vai šie līdzekļi tiks automātiski iespējoti migrācijas laikā?

Tas, vai līdzeklis jaunajā infrastruktūrā ir iespējots automātiski, tiks noteikts katram līdzeklim atsevišķi. Šī informācija tiks ietverta funkcionalitātes dokumentācijā.

### <a name="what-happens-to-my-byod-database-during-the-migration"></a>Kas migrācijas laikā notiek ar manu BYOD datu bāzi?

Importa un eksporta konfigurācijas jūsu datu bāzei (BYOD) tiks migrētas uz jauno infrastruktūru.

### <a name="what-happens-to-my-azure-data-lake-during-the-migration"></a>Kas migrācijas laikā notiek ar manu Azure Data Lake?

Jebkurš eksports, kas pašlaik ir konfigurēts Finanšu Azure Data Lake Storage un operāciju programmām, uzturēs to pašu konfigurāciju pēc migrācijas.

### <a name="we-are-currently-using-dynamics-ax-2012-will-the-upgrade-tools-that-are-currently-available-be-used-to-upgrade-the-hr-module-in-ax-2012-to-dynamics-365-human-resources"></a>Pašlaik tiek izmantots Dynamics AX 2012. Vai jaunināšanas rīki, kas pašlaik ir pieejami, tiks izmantoti HR moduļa jaunināšanai AX 2012 uz Dynamics 365 Human Resources?

Jā. Dynamics 365 Human Resources tiks iekļauts sapludinātajā kodu bāzē un finanšu un operāciju programmu infrastruktūras sarakstā. Jauninājums no Dynamics AX 2012 Dynamics 365 Human Resources uz to pašu jaunināšanas ceļu un rīku, kas tiek izmantots, lai jauninātu uz jaunāko Finanšu un operāciju programmu versiju.

### <a name="we-use-document-handling-with-dynamics-365-human-resources-what-will-happen-to-the-documents-during-the-migration"></a>Mēs izmantojam Dokumentu apstrādi ar Dynamics 365 Human Resources. Kas ar dokumentiem notiks migrācijas laikā?

Dokumenti paliks esošajā dokumentu krātuvē. Tie tiks mainīti attiecībā uz vidi jaunajā infrastruktūrai.

### <a name="what-happens-to-the-batch-jobs-that-we-have-configured-in-dynamics-365-human-resources-after-the-migration"></a>Kas notiek ar pakešuzdevumiem, ko mēs esam konfigurējuši Dynamics 365 Human Resources pēc migrācijas?

Piemērojamie pakešuzdevumi automātiski tiks migrēti uz jauno infrastruktūru.

## <a name="licensing-impact"></a>Licencēšanas ietekme

Šī dokumentācija neaizstāj nevienu no juridiskajām dokumentācijām, kas ietver izmantošanas tiesības.

### <a name="my-organization-uses-dynamics-365-human-resources-to-manage-its-hr-operations-does-our-licensing-or-cost-change"></a>Mana organizācija izmanto Dynamics 365 Human Resources, lai pārvaldītu savas HR operācijas. Vai mūsu licencēšana vai izmaksas mainās?

Debitori, kas iegādājušies Dynamics 365 Human Resources licences, netiks ietekmēti. Šim debitoram nav licencēšanas migrācijas. Papildu noliktavas vienība (NV), kas bija raksturīga Human Resources, vairs netiks piemērota. Tā vietā debitori var izvēlēties iegādāties Finanšu un operāciju programmas 2. pakāpes tekstlodziņu ar nedaudz zemākām izmaksām. Esošie debitori, kas iegādājušies cilvēkresursus, būs migrēti uz finanšu un operāciju programmu 2. pakāpes vadīklu bez papildu izmaksām.

### <a name="my-organization-uses-the-human-resources-module-in-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-does-my-licensing-or-cost-change"></a>Mana organizācija izmanto Cilvēkresursu moduli Dynamics 365 Finanses, Piegādes ķēžu pārvaldība, Komercija vai Projekta operācijas. Vai mana licencēšana vai izmaksas mainās?

Esošie Dynamics 365 programmu lietotāji un lietotāji, kuriem ir savrupa Dynamics 365 finanses, piegādes ķēdes pārvaldība, komercija un projekta operācijas, var piekļūt personāla vadībai kā daļai no šīm licencēm līdz 2025. gada februārim vai līdz pašreizējā licencēšanas līguma derīguma termiņam atkarībā no tā, kas ir agrāks. Varat izvēlēties pārvietoties Human Resources licencēm agrāk, ja tas palīdz sasniegt labākus izmaksu uzkrājumus. Sākot no 2025. gada februāra visiem esošajiem CHF un EA debitoriem ir jāizvērš HR modulis un jāpērk cilvēkresursu licences, lai izmantotu jaunās iespējas, kas tiek iesniegtas Finanšu un operāciju programmām.

### <a name="my-organization-is-live-with-dynamics-365-finance-supply-chain-management-commerce-or-project-operations-will-we-be-required-to-purchase-an-additional-environment-to-support-the-infrastructure-merge"></a>Mana organizācija dzīvo ar Dynamics 365 Finansēm, Piegādes ķēžu pārvaldību, Uzņēmumu vai Projektu operācijām. Vai tiks pieprasīts iegādāties papildu vidi, lai atbalstītu infrastruktūras sapludināšanu?

Papildu vides nav nepieciešamas, lai atbalstītu infrastruktūras izmaiņas.

