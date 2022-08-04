---
title: Bieži uzdotie jautājumi par cilvēkresursu klientu migrāciju
description: Šajā rakstu atbildēs bieži uzdotie jautājumi par Microsoft Dynamics 365 Human Resources migrāciju uz finanšu un operāciju sapludināto infrastruktūru.
author: twheeloc
ms.date: 07/06/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8a6f883da07bd1d3a6b0379f1582dc8556e166ff
ms.sourcegitcommit: 9310c943ac76896663e5604209034da9f8d6139c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151098"
---
# <a name="human-resources-customer-migration"></a>Cilvēkresursu debitoru migrācija

## <a name="how-should-dynamics-365-human-resources-customers-plan-to-move-to-the-finance-and-operations-infrastructure"></a>Kā debitori Dynamics 365 Human Resources plāno pāriet uz finanšu un operāciju infrastruktūru?

Tiks ietekmētas divas Microsoft Dynamics 365 Human Resources debitoru kategorijas, un jums būs jāveic izmaiņas, lai nodrošinātu, ka tie ir pēdējā finanšu un operāciju infrastruktūras kategorijās:

- Debitori, Dynamics 365 Human Resources kuri izmanto un kuriem nav nevienas citas Dynamics 365 operācijas programmas
- Debitori, kuri Dynamics 365 Human Resources izmanto gan Dynamics 365 finanses, Dynamics 365 Supply Chain Management gan Dynamics 365 Commerce arī Dynamics 365 Project Operations

Neatkarīgi no kategorijas, kurai tie pieder, debitoriem dati būs jāpārvieto uz jaunizveidotu finanšu un operāciju infrastruktūras vidi un jāpārbauda, vai sapludināšana ir veiksmīgi pabeigta.

Turpmāk programmai būs sava Dynamics 365 Human Resources finanšu un operāciju vide, kas ir atsevišķi no citām operāciju programmām. Šādā veidā debitori var izmantot paplašināmības opciju priekšrocības, sapludinot pašreizējos datus. Korporācija Microsoft nodrošina rīku un kastu vidi, ko klienti var izmantot, lai pārbaudītu un pārbaudītu datu migrāciju pirms pārvietošanas uz ražošanas vidi. Rīku rīks iespējos tuvu automatizētu procesu un būs pieejams no 2022. gada augusta līdz 2022. gada novembrim.

Klientiem, kas finanšu un operāciju infrastruktūrai izmanto citas programmas, būs iespēja apvienot personāla vadības datus ar esošo vidi. 

## <a name="when-will-customers-be-moved-to-the-finance-and-operations-infrastructure"></a>Kad debitori tiks pārvietoti uz finanšu un operāciju infrastruktūru?

Pāreja uz katru uzņēmumu būs atkarīga no uzņēmuma pašreizējās konfigurācijas un gatavības pāriet uz finanšu un operāciju infrastruktūru. Ieteicams, lai debitori strādātu ar Microsoft partneri, lai noteiktu labāko ceļu uz priekšu.

- Organizācijas, kas izmanto personāla **vadības** moduli Dynamics 365 finansēs Dynamics 365 Human Resources, varēs iespējot jaunas iespējas no parastā vienas versijas atjaunināšanas procesa. Ir plānots, ka jaunās funkcijas kļūs plaši pieejamas, sākot no 2022. gada janvāra.
- Organizācijām, kuras izmantos Dynamics 365 Human Resources, būs piekļuve rīkam, ko tās var izmantot infrastruktūras sapludināšanas pabeigšanai. Microsoft strādās ar klientiem šajā pārejā, lai palīdzētu novērst jebkādu pakalpojuma pārtraukšanu. Klientiem būs 12–18 mēneši, lai veiktu pāreju, sākot no laika, kad kļūst pieejama migrācijas rīka izmantošana.
- Organizācijas, kas izmanto gan personāla Dynamics 365 Human Resources vadības **moduli**, gan personāla vadības moduli var pārvietot savu savrupu cilvēkresursu infrastruktūru uz finanšu un operāciju infrastruktūru. Cita opcija ir izmantot sapludināšanas rīku, lai apvienotu vides vienā vidē. Divu vidi sapludināšanai nav prasības vai laikposma.

Lai iegūtu atjaunināto informāciju, regulāri pārbaudiet Izlaišanas [plānus](/dynamics365/release-plans/).

## <a name="will-customers-still-need-custom-integrations-between-dynamics-365-human-resources-and-the-human-resources-module"></a>Vai debitoriem joprojām būs nepieciešama pielāgota integrācija starp Dynamics 365 Human Resources moduli Personāla vadība un cilvēkresursi?

- Klientiem, kuriem ir Dynamics 365 Human Resources gan finanšu, gan operāciju infrastruktūras vides, kas pašlaik ir integrētas, būs jāturpina integrēt šīs divas vides pēc saplūšanas.
- Klientiem, kas izvēlas saglabāt Dynamics 365 Human Resources vidi atsevišķi no savas esošās finanšu un operāciju programmas vides, būs jāturpina integrēt vides, lai padarītu datus pieejamus abās vidēs.
- Debitori var turpināt izmantot datu integrētāju, lai kopētu datus starp divām vidēm. Debitori, kuri apvieno datus vienā vidē pēc migrācijas, vairs nebūs jāintegrē dati, jo visi dati būs vienā datu bāzē.

## <a name="will-customer-isv-solutions-automatically-be-migrated"></a>Vai debitora ISV risinājumi tiks migrēti automātiski?

Migrācijas pieredze katram neatkarīgam programmatūras izstrādātāja (ISV) risinājumam atšķirsies atkarībā no risinājuma integrācijas metodes. Korporācija Microsoft strādās cieši ar ISVs, lai palīdzētu nodrošināt gludu pāreju uz finanšu un operāciju infrastruktūru. Daudzi ISV risinājumi ir veidoti Dataverse, izmantojot iespējas Microsoft Power Platform. Šie risinājumi ir atkarīgi Dataverse no vides Dynamics 365 Human Resources un vides Dataverse integrācijas. Integrācija Dataverse tiek novecojusi kā daļa no infrastruktūras sapludināšanas. Finanšu un operāciju infrastruktūras jaunās dubultās rakstīšanas kartes tiek plānotas, lai aizstātu integrācijas Dataverse funkcionalitāti.

## <a name="how-will-the-data-integrator-that-moves-data-between-dynamics-365-human-resources-and-other-dynamics-365-apps-be-affected"></a>Kā tiks ietekmēts datu integrētājs, kas pārvieto datus no Dynamics 365 Human Resources vienas Dynamics 365 programmas uz citu?

Kad debitori pārvietojas uz finanšu un operāciju infrastruktūru, tiem būs jāturpina integrēt datus starp abām vidēm. Debitori var turpināt izmantot datu integrētāju, lai veiktu šos datu migrācijas uzdevumus. Klientiem, kas plāno uzturēt vidi Dynamics 365 Human Resources atsevišķi no savas esošās finanšu un operāciju lietojumprogrammu vides, būs jāturpina integrēt datus starp šīm divām vidēm. Debitoriem, kuri saplūst divas vides vienā vidē, integrācija starp divām vidēm vairs nebūs nepieciešama.

## <a name="how-will-data-be-moved-between-dynamics-365-human-resources-on-the-finance-and-operations-infrastructure-and-dataverse-after-the-migration"></a>Kā dati tiks pārvietoti starp Dynamics 365 Human Resources finanšu un operāciju infrastruktūru un pēc Dataverse migrācijas?

Pašreizējā integrācija Dataverse starp Dynamics 365 Human Resources finanšu Dataverse un operāciju infrastruktūru un tiek amortizēta kā daļa no finanšu un operāciju. Ir plānots ieviest dubultās rakstīšanas kartes, lai kartētu finanšu un operāciju elementus uz tabulām Dataverse. Debitoriem būs jāizlemj, kuras dubultās rakstīšanas kartes ir nepieciešamas to ieviešanai. Lai palaistu biznesa loģiku, ieteicams izmantot virtuālās tabulas integrācijai un ISV risinājumiem, ja vien nav īpašas biznesa nepieciešamības pēc tā, Dataverse lai dati tiktu dublēti.

## <a name="how-does-the-migration-affect-dataverse-extensions-for-dynamics-365-human-resources"></a>Kā migrācija ietekmē paplašinājumus Dataverse Dynamics 365 Human Resources?

Pirms klientu ražošanas vides migrēšanas debitori būs jāmigrē uz kastu vidi. Kad debitori migrē savas sūtnes vidi, Dataverse tiem būs jāizveido savas vides kopija, lai izveidotu savienojumu ar jauno finanšu un operāciju migrēto vidi. Mēs iesakām debitoram kopēt gan datus, gan vides risinājumus, lai tie atbilstu debitora pašreizējai ražošanas videi.

Kad debitori ir gatavi migrēt savus ražošanas Dynamics 365 Human Resources vidi, Microsoft automātiski migrēs datu bāzi un Azure BLOB krātuvi. Migrētā datu bāze un krātuve norādīs jauno vidi finanšu un operāciju infrastruktūrai uz to pašu ražošanas Dataverse vidi. Pirms datu Dataverse kopēšanas klientiem būs jāiespējo visas duālās rakstīšanas kartes, kas nepieciešamas to integrācijai, paplašinājumiem un ISV risinājumiem, kas ir veidotas Dataverse.

## <a name="will-microsoft-power-platform-components-that-were-built-for-dynamics-365-human-resources-automatically-work-after-the-infrastructure-migration-is-completed"></a>Vai Microsoft Power Platform komponenti, kas tika veidoti Dynamics 365 Human Resources automātiskai darbiem pēc infrastruktūras migrācijas pabeigšanas?

Programmas, kas ir izveidotas Power Apps, plūsmās, kas izveidotas Power Automate, un citi pielāgojumi Microsoft Power Platform ir kā paplašinājumi Dataverse. Debitora ražošanas vides migrācijas laikā vides, tostarp paplašinājumi Dataverse, netiek ietekmētas. Lietojumprogrammām, plūsmām un citiem Power Microsoft platformas pielāgojumiem ir jāturpina darbs, neprasot papildu konfigurāciju.

## <a name="what-will-happen-to-dataverse-virtual-table-entities-for-dynamics-365-human-resources-during-the-migration"></a>Kas migrācijas laikā Dataverse tiks darīts ar virtuālās Dynamics 365 Human Resources tabulas elementiem?

Kad debitori migrē Dynamics 365 Human Resources savas vides finanšu un operāciju infrastruktūru, vide paliek saistīta ar Dataverse vidi, kas pašlaik ir saistīta ar.Dynamics 365 Human Resources Vidē Dataverse ģenerētās virtuālās tabulas turpinās darbu, neprasot papildu konfigurāciju. Virtuālās tabulas, iespējams, ir jāģenerē Dataverse vidē, kas ir saistīta ar klienta esošo finanšu un operāciju vidi.

## <a name="how-will-an-integration-that-uses-the-applicant-tracking-system-ats-api-payroll-api-dataverse-virtual-tables-for-dynamics-365-human-resources-or-other-entities-in-the-dataverse-web-api-work-after-the-infrastructure-merge-is-completed"></a>Kā integrācijai, kas izmantos Kandidātu izsekošanas sistēmas (ATS) API, Algas API, Dataverse Dynamics 365 Human Resources Dataverse virtuālās tabulas vai citām Web API entītijām, pēc infrastruktūras sapludināšanas pabeigšanas?

Kad debitori migrē Dynamics 365 Human Resources savas vides finanšu un operāciju infrastruktūru, vide paliek saistīta ar Dataverse vidi, kas pašlaik ir saistīta ar.Dynamics 365 Human Resources Visas integrācijas, kas tika izstrādātas attiecībā uz Dataverse tīmekļa API, turpinās darbu pēc migrācijas pabeigšanas.

## <a name="our-organization-has-configured-custom-security-in-dynamics-365-human-resources-will-it-still-be-applied-after-the-infrastructure-migration-is-completed"></a>Mūsu organizācija ir konfigurējusi pielāgotu drošību Dynamics 365 Human Resources. Vai tas joprojām tiks lietots pēc infrastruktūras migrācijas pabeigšanas?

Jā, pielāgotas drošības konfigurācijas tiks ietvertas datu migrācijā.

## <a name="will-workflows-in-dynamics-365-human-resources-automatically-be-migrated"></a>Vai darbplūsmas tiks Dynamics 365 Human Resources migrētas automātiski?

Jā, darbplūsmas konfigurācijas, darbplūsmas vēsture un pašreizējās procesā esošās darbplūsmas tiks migrētas uz sapludināto infrastruktūru.

## <a name="will-saved-views-in-dynamics-365-human-resources-automatically-be-migrated"></a>Vai saglabātie skati Dynamics 365 Human Resources tiks migrēti automātiski?

Jā, saglabātie skati tiks migrēti uz sapludināto infrastruktūru.

## <a name="will-features-that-are-enabled-in-dynamics-365-human-resources-automatically-be-available-after-the-infrastructure-merge"></a>Vai līdzekļi, kas tiks aktivizēti Dynamics 365 Human Resources automātiski, būs pieejami pēc infrastruktūras sapludināšanas?

- Debitoriem, kuri izmanto cilvēkresursu **moduli**, funkcijas, kas ir pieejamas tikai modulī Dynamics 365 Human Resources Līdzekļi, tiks pārvaldītas, izmantojot līdzekļu pārvaldību. Parasti šīs funkcijas netiek aktivizētas pēc noklusējuma. Visi līdzekļi, kas jāaktivizē pēc noklusējuma, tiks dokumentēti.
- Debitoriem, kuri Dynamics 365 Human Resources izmanto šos līdzekļus, līdzekļi būs pieejami infrastruktūras vajadzībām. Visi līdzekļi, kas nav pieejami, tiks dokumentēti. Katra pašreizējā vidē aktivizētā līdzekļu pārvaldības atslēga Dynamics 365 Human Resources tiks iespējota sapludinātajā infrastruktūra. Papildinformāciju skatiet [Līdzekļu pārvaldības pārskatā](/fin-ops/get-started/feature-management-overview.md).

## <a name="what-happens-to-byod-databases-during-the-migration"></a>Kas migrācijas laikā notiek ar BYOD datu bāzēm?

Importējiet un eksportējiet konfigurācijas, lai paņemtu savu datu bāzi (BYOD), tiks migrētas uz finanšu un operāciju infrastruktūru.

## <a name="is-there-an-impact-on-the-azure-region-when-the-customer-environment-is-migrated"></a>Vai, migrējot debitora vidi, pastāv ietekme uz Azure reģionu?

Migrācijai Dynamics 365 Human Resources vide būs vienā Azure reģionā. Ja ir nepieciešams pārvietot vidi uz citu Azure reģionu, debitoriem būs jāievēro standarta darbības, lai migrētu uz jaunu reģionu pēc migrācijas pabeigšanas.

## <a name="what-happens-to-azure-data-lakes-during-the-migration"></a>Kas notiek ar Azure datu pārsūtīšanas laikā?

Jebkurš eksports, kas pašlaik ir konfigurēts Azure datu krātuvē finanšu un operāciju programmās, uzturēs to pašu konfigurāciju pēc migrācijas.

> [!NOTE]
> Duālās rakstīšanas kartes būs jāiespējo, lai turpinātu rakstīt datus no Personāla vadības vides Dataverse.

Klienti, kuri vēlas eksportēt personāla vadības datus uz datu darbību, var iespējot šo funkciju pēc migrācijas uz finanšu un operāciju infrastruktūru pabeigšanas. Papildinformāciju skatiet sadaļā [Datu darbības — Azure arhitektūras centrs](/azure/architecture/data-guide/scenarios/data-lake).

Debitori var sasaistīt vairākas finanšu un operāciju vides ar vienu un to pašu datu līdzās. Tomēr katra vide norāda uz citu mapi un konteineru. Klientiem, kas plāno sapludināt vides vēlāk, ir rūpīgi jāplāno sava pieeja.
 
## <a name="what-migration-will-be-required-if-a-customer-is-currently-using-the-human-resources-module"></a>Kāda migrācija būs nepieciešama, ja debitors pašlaik izmanto Cilvēkresursu moduli?

Debitoriem, kuri **izmanto Personāla vadības** moduli, būs jaunā funkcionalitātes funkcionalitāte Dynamics 365 Human Resources no pielietotas savā vidē caur standarta versijas atjaunināšanas procesu. Klienti savā vidē redzēs jauno funkcionalitāti, it kā tā būtu pieejama katrā atjauninājumā. Debitori var izmantot Funkciju pārvaldību, lai iespējotu funkcijas. Klientiem ir jāplāno apstiprināt šīs jaunās funkcijas, izmantojot procesus, kas jau ir savā vietā, un jāizmanto, lai validētu citus atjauninājumus savā vidē.

## <a name="what-will-happen-to-custom-integrations-to-external-systems"></a>Kas tiks darīts ar pielāgotām integrācijām ārējās sistēmās?

Debitori migrēs savas integrācijas finanšu un operāciju vidē. Tā kā šīs vides galapunkts atšķiras, klientiem, iespējams, būs jāatjaunina vai jāmaina integrācijas, lai tie norāda uz jauno vidi. Šis uzdevums galvenokārt būs manuāls process, un pieprasītās izmaiņas būs atkarīgas no integrācijas arhitektūras. Klientiem ir jāsadarbojas ar Microsoft partneri, lai noteiktu labāko pieeju integrācijas pārvietošanai.

## <a name="what-will-happen-to-microsoft-power-platform-dataverse-extensions-if-customers-merge-a-dynamics-365-human-resources-environment-with-an-existing-finance-and-operations-environment"></a>Kas tiks darīts Microsoft Power Platform ar paplašinājumiem Dataverse, ja debitori sapludinās vidi Dynamics 365 Human Resources ar esošu finanšu un darbību vidi?

Ja debitori nolemj sapludināt vidi Dynamics 365 Human Resources Dataverse un esošu finanšu un operāciju vidi vienā instancē pēc migrācijas, Dataverse to vides ir jāapvieno kā daļa no sapludināšanas procesa. Šim uzdevumam būs nepieciešams, Power Apps lai visas programmas, kas izveidotas, izmantojot, un visas citas pielāgošanas tiktu atkārtoti izvietotas jaunajā vidē.

## <a name="what-will-happen-to-documents-during-the-migration"></a>Kas tiks darīts ar dokumentiem migrācijas laikā?

Kad debitori migrē Dynamics 365 Human Resources savas vides finanšu un operāciju infrastruktūru, dokumenti paliks esošajā dokumentu krātuvē un automātiski tiks kartēti uz jauno finanšu un operāciju infrastruktūras vidi.

Nākamajā laidienā tiks nodrošināti jauni datu elementi. Pēc šo izmaiņu veikšanas debitori, kas izvēlas sapludināt savu vidi ar esošu finanšu un darbību vidi, varēs eksportēt dokumentus un pārvietot tos Dynamics 365 Human Resources uz esošo vidi.

## <a name="after-the-migration-what-happens-to-the-batch-jobs-that-were-configured-in-dynamics-365-human-resources"></a>Pēc migrācijas, kas notiek ar pakešuzdevumiem, kas tika konfigurēti Dynamics 365 Human Resources?

Pakešuzdevumi būs jāpārkonfigurē finanšu un operāciju vidē. Klientiem būs jānovērtē katrs pakešuzdevums un tas jāsalīdzina ar pašreizējo pakešuzdevumu sarakstu finanšu un operāciju vidē. Klientiem ir arī jāanalizē vispārējais pakešuzdevumu grafiks, kad tie sapludina divas pakešuzdevumu kopas, lai noteiktu, vai jāveic izmaiņas pakešuzdevumu grafikā, prioritātēs vai pakešuzdevumu grupās.

## <a name="how-will-the-migration-affect-the-lcs-project-for-dynamics-365-human-resources"></a>Kā migrācija ietekmēs LCS projektu Dynamics 365 Human Resources?

Klientiem būs jāizveido Microsoft Dynamics jauns Lifecycle Service (LCS) projekts, **un** tiem kā projekta tips jāatlasa finanšu un operāciju programmas kā prece un ieviešana. Turklāt apakšprojekta tipam ir pieejams jauns lauks, kad ir izveidots LCS projekts. Klientiem būs jāizvēlas migrācijas opcija Dynamics 365 Human Resources, lai migrētu esošo cilvēkresursu LCS projektu uz finanšu un operāciju infrastruktūru.

Finanšu un operāciju LCS projektu funkcijas atšķiras no cilvēkresursu LCS projektu funkcijām.

Lai atgrieztos tiešsaistē, jauniem debitoriem būs jāveic šādi uzdevumi:

- Pabeidziet projekta izpildē.
- Pabeidziet metodoloģiju.
- Aizpildiet abonementa vērtēšanu.
- Izpildiet go-live gatavības procesu.

## <a name="how-will-the-business-process-modeler-be-migrated"></a>Kā tiks migrēts biznesa procesa modelators?

Klientiem būs nepieciešams eksportēt savu biznesa procesu modelētāja bibliotēku no cilvēkresursu LCS projekta un importēt to finanšu un operāciju LCS projektā. Turklāt klientiem lietojumprogrammas palīdzības iestatījumi būs jāatjaunina tā, lai tie norāda uz jauno LCS projektu.

## <a name="how-will-the-service-update-process-be-affected-by-the-migration"></a>Kā migrācija ietekmēs pakalpojuma atjaunināšanas procesu?

Pēc migrācijas debitori būs daudz elastīgāki programmas dzīves cikla pārvaldībai (<a0/&) un pakalpojumu atjauninājumiem. Personāla vadības vidēs pakalpojumu atjauninājumi vairs netiks automātiski pielietoti. Tā vietā pakalpojums izpildīs vienas versijas pakalpojuma atjaunināšanas procesus un funkcionalitāti, kā arī konfigurācijas opcijas atjauninājumiem, izmantojot LCS, tiks iespējoti.

## <a name="will-customers-be-eligible-for-fasttrack-assistance-with-the-infrastructure-merge"></a>Vai debitori varēs saņemt FastTrack palīdzību, sapludinot infrastruktūru?

Korporācija Microsoft joprojām definē, kādi rīki un resursi no FastTrack būs pieejami, lai palīdzētu sapludināšanas laikā.

## <a name="licensing-impact"></a>Licencēšanas ietekme

Papildinformāciju par to, kā tiek ietekmēta licencēšana, skatiet infrastruktūras sapludināšanas [Dynamics 365 Human Resources FAQ](hr-infrastructure-merge-faq.md#licensing-impact).
