---
title: "Dynamics AX 2012 jaunināšana uz Dynamics 365 for Finance and Operations Enterprise izdevumu"
description: "Šajā tēmā ir aprakstīts process, ko klienti, kas pašlaik izmanto programmatūru Microsoft Dynamics AX 2012, var izmantot savu datu un koda pārvietošanai uz Microsoft Dynamics 365 for Finance and Operations Enterprise izdevumu."
author: tariqbell
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations Platform
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 8
ms.translationtype: Human Translation
ms.sourcegitcommit: 6816e3820ab77c71bbf9bde4a068375448331671
ms.openlocfilehash: 13507fcf9c0d626709aeb4e00a8632411204c20f
ms.contentlocale: lv-lv
ms.lasthandoff: 06/15/2017

---

# <a name="upgrade-microsoft-dynamics-ax-2012-to-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition"></a>Microsoft Dynamics AX 2012 jaunināšana uz Microsoft Dynamics 365 for Finance and Operations Enterprise izdevumu

[!include[banner](../includes/banner.md)]

8. platformas atjauninājumā Microsoft Dynamics 365 for Finance and Operations Enterprise izdevums nodrošina jaunināšanas ceļu, ko klienti, kas pašlaik lieto Microsoft Dynamics AX 2012, var izmantot savu datu un koda pārvietošanai uz Finance and Operations. Jaunināšanas procesa pamatā ir tālāk norādītie elementi.

- Rīki, kas palīdz pārnest esošo pielāgoto programmas kodu no AX 2012.
- Datu jaunināšanas process, ko varat izmantot, lai pārnestu savu datu bāzi. Tādējādi varat jauninātu visu savu transakciju vēsturi.

## <a name="overview"></a>Pārskats

Kopējo jaunināšanas procesu var vizualizēt kā trīs galvenos posmus: Analizēt, Izpildīt un Pārbaudīt.

Tālāk esošajā diagrammā parādīts jaunināšanas process no sākuma līdz beigām un darbības, ko uzskatām par katra posma daļu. 

![Jaunināšanas process](./media/upgrade-process.png)

## <a name="analyze"></a>Analizēt

Posma Analizēt darbības palīdz jums novērtēt ieguldījumu, kas nepieciešams jauninājumam. Tās arī palīdz sagatavot projekta plānu. Šīs darbības var veikt pirms programmatūras Finance and Operations iegādes. Tās palīdzēs jums veikt apzinātu izvēli par pirkumu, nodrošinot datu punktu par nepieciešamajiem ieguldījumiem un resursiem.

### <a name="sign-up-for-a-public-preview-in-lcs"></a>Reģistrācija publiskam priekšskatījumam pakalpojumā LCS

Lai veiktu posma Analizēt darbības pirms Finance and Operations iegādes, varat reģistrēties publiskam priekšskatījumam. Publiskais priekšskatījums ļauj jums izvietot savas Finance and Operations vides. Tas arī sniedz piekļuvi Microsoft Dynamics Lifecycle Services (LCS) rīkiem, kas tiek izmantoti, lai novērtētu jūsu AX 2012 vidi un esošo pielāgoto kodu.

Ja jums ir LCS projekts programmai AX 2012, jums joprojām ir jāreģistrējas papildu jaunam projektam, lai novērtētu programmatūru Finance and Operations.

Informāciju par to, kā iegūt klientiem paredzētu publisku priekšskatījumu, skatiet vietnē https://mbs.microsoft.com/customersource/global/AX/news-events/news/Microsoft_Dynamics_AX_Public_Preview.

Informāciju par to, kā iegūt partneriem paredzētu publisku priekšskatījumu, skatiet vietnē https://mbs.microsoft.com/partnersource/global/news-events/news/Microsoft_Dynamics_AX_Public_Preview.

Ņemiet vērā, ka šis publiskais priekšskatījums atšķiras no [30 dienu izmēģinājumversijas](https://aka.ms/D365OperationTrials). Trīsdesmit dienu izmēģinājumversijas nodrošina izvietotu Finance and Operations instanci, ko varat izmantot, lai izpētītu un novērtētu programmu. Tomēr posma Analizēt darbībām ir nepieciešamas visas LCS iespējas un rīki.

### <a name="select-the-upgrade-methodology"></a>Jaunināšanas metodikas atlase
Savā jaunajā LCS projektā iestatiet projekta metodiku uz **Jaunināt AX 2012 uz Dynamics 365 for Operations**. Šī metodika ir īpaši izstrādāta AX 2012 klientiem, kas veic jaunināšanu. Tajā ir detalizēti aprakstīti trīs posmi un sniegtas saites uz visiem pavaddokumentiem par procesu.

![Upgrade methodology(./media/methodology.png)
 
### <a name="run-the-upgrade-analyzer"></a>Jaunināšanas analizētāja palaišana
Jaunināšanas analizētāja rīks tiek palaists jūsu AX 2012 videi un nosaka uzdevumus, kas jums jāveic AX 2012 vides sagatavošanai, lai jaunināšanas procesu padarītu vienkāršāku un samazinātu ar to saistītās izmaksas.

- **Datu tīrīšana** — šis process palīdz jums identificēt datus, ko varat noņemt, nezaudējot funkcionalitāti. Šis rīks identificē dažādu tipu datus, ko varat samazināt, palaižot tīrīšanas procesu. Katram datu tipam ir sniegts paskaidrojums par tīrīšanas ietekmi. Jūs izlemjat, vai palaist tīrīšanas procesu. Daļu jūsu Finance and Operations abonementa izmaksām veido datu bāzes lielums. Tādēļ, samazinot lielumu, varat samazināt šī abonementa komponenta izmaksas un arī palīdzēt samazināt laiku, kas nepieciešams jaunināšanas ieviešanas procesam. Mazāka datu bāze palīdz garantēt ātrāku jaunināšanu.
- **SQL konfigurācija** — šis process pārskata SQL konfigurāciju un iesaka optimizāciju. Pārliecinoties, vai SQL darbojas optimāli, šis process palīdz samazināt laiku, kas ir nepieciešams jaunināšanas ieviešanas procesam.
- **Novecojušie līdzekļi** — šis process identificē līdzekļus, ko pašlaik izmantojat, bet kas nav pieejami programmatūrā Finance and Operations. Tādējādi process palīdz laikus atklāt nepilnības funkcionalitātē. Tas arī sniedz ieteikumus alternatīvām.

Veicot šo darbību, ir jāinstalē KBXXXXXXX AX 2012 vidē. Šis labojumfails nodrošina pirmsjaunināšanas kontrolsarakstu. AX 2012 vidē varat izmantot šo kontrolsarakstu, lai ievadītu datus, kas būs nepieciešami jaunināšanas procedūrai. Piemēram, vienā no pirmsjaunināšanas kontrolsaraksta uzdevumiem jūs sniedzat Microsoft Azure Active Directory (Azure AD) pierakstīšanās informāciju katram pašreizējam AX 2012 lietotājam, lai katrs lietotājs varētu pieteikties programmatūrā Finance and Operations.

Šīs darbības rezultāts ir darbplūsma jaunināšanas projekta plānā jūsu AX 2012 sistēmas administratoriem.

Papildinformāciju skatiet sadaļā [Analīze: jaunināšanas analizētāja izmantošana migrācijas darba plānošanai](upgrade-analyzer-tool.md).

### <a name="run-the-code-upgrade-estimation-tools"></a>Koda jaunināšanas novērtēšanas rīku palaišana
Šajā darbībā jūsu kods tiek paņemts no AX 2012 un pārveidots jaunā formātā, kā arī tiek sniegtas atsauksmes par konfliktiem, kas būs vēlāk jārisina izstrādātājam. Šī darbība nodrošina pamatu jūsu koda jaunināšanas izmaksu aprēķinam.

Lai pabeigtu šo darbību, jums ir jāeksportē kods no AX 2012 kā modeļu krātuves eksports un jāaugšupielādē LCS kodu jaunināšanas rīkā. Kodu jaunināšanas rīks izveidos jauninātu koda versiju un sniegs pārskatu par atlikušajiem konfliktiem, kas jārisina. Izstrādātājs pēc tam var pārskatīt gan jaunināto kodu, gan pārskatu, lai noteiktu ieguldījumu, kas būs nepieciešams koda bāzes jaunināšanai.

Šīs darbības rezultāts ir darbplūsma jaunināšanas projekta plānā jūsu Microsoft Dynamics AX izstrādātājiem.

Papildinformāciju skatiet sadaļā [Analīze: koda jaunināšanai nepieciešamā ieguldījuma novērtēšana](analyze-code-upgrade.md).

### <a name="deploy-a-demo-environment"></a>Izvietot demonstrācijas vidi
Demonstrācijas vides ir noklusējuma vides, kas satur demonstrācijas datus (nevis jūsu datus) un standarta kodu (bez pielāgojumiem). Demonstrācijas vidi ieteicams izvietot, lai novērtētu jaunus līdzekļus un veiktu pamata atbilstības kompetenču analīzi standarta procesiem, kas tiek izmantoti programmā AX 2012, bet kas varētu tikt mainīti programmatūrā Finance and Operations. Šīs demonstrācijas vides varat izvietot pakalpojumā Azure vai lejupielādēt tās kā virtuālo mašīnu (VM) palaišanai savā aparatūrā. Ja izvietojat tās pakalpojumā Azure, jums ir jānorāda Azure abonements, jo jūs joprojām izmantojat publiskā priekšskatījuma projektu un vēl neesat iegādājies Finance and Operations abonementu.

Šīs darbības rezultāts ir darbplūsma jaunināšanas projekta plānā jūsu funkcionālajiem lietotājiem vai biznesa lietotājiem.

Papildinformāciju skatiet sadaļā [Analīze: smilškastes vides izvietošana](analysis-sandbox.md)

### <a name="create-a-project-plan"></a>Projekta plāna izveide
Projekta plāna veidne ir nodrošināta jaunināšanas metodikā. Šajā darbībā tiek izmantota iepriekšējo posma Analizēt darbību rezultāts, lai aizpildītu jaunināšanas projekta plānu. Projekta plānā būs iekļauta arī visa detalizētā informācija par testēšanu: datu jaunināšanas testēšana, pārslēgšanas testēšana, funkcionālo testu izpildes atkārtojumi un informācija par dažādām resursu piešķirēm šiem uzdevumiem.

Šajā posmā projekta plānā tiek sniegts datu punkts, kas var palīdzēt jums saprast laiku un izmaksas, kas nepieciešami jaunināšanai uz Finance and Operations.

## <a name="execute"></a>Izpildīt
Posma Izpildīt laikā jūs strādājat ar uzdevumiem, ko ieplānojāt posmā Analizēt. Lai pārietu uz posmu Izpildīt, jums ir jāiegādājas programmatūra Finance and Operations, kā arī jums ir jābūt pieejamiem resursiem, kas var strādāt ar jaunināšanu.

### <a name="switch-to-the-lcs-implementation-project"></a>Pāriešana uz LCS ieviešanas projektu
Publiskā priekšskatījuma projekts, ko izmantojāt posmā Analizēt, vairs nebūs nepieciešams. To tagad var atmest. Atlikušajām darbībām ir nepieciešams tikai projekta plāns, ko izveidojāt posma Analizēt pēdējā darbībā.

Kad iegādāsities Finance and Operations abonementu, saņemsit informāciju par to, kā reģistrēties jaunam LCS projektam. Šis projekts ir pazīstams kā ieviešanas projekts, un tas būs jaunais, pastāvīgais jūsu abonementa LCS projekts visā abonementa darbības laikā. Šis projekts atšķiras no publiskā priekšskatījuma projekta tādējādi, ka to pārvalda Microsoft. Tāpēc šim projektam ir tālāk norādītās īpašības.

- Visas vides projektā tiek viesotas pakalpojumā Azure.
- Ar projektu saistīto Azure abonementu pārvalda Microsoft. Tāpēc par Azure izmaksām nav atsevišķu norēķinu. Izmaksas sedz jūsu Finance and Operations abonements.
- Ražošanas vidi projektā uztur Microsoft. Tādēļ kodu izvietošanu, jaunināšanu un infrastruktūras uzturēšanu veic tieši Microsoft, nevis jūsu darbinieki. 

### <a name="perform-the-ax-2012-preparation-tasks"></a>AX 2012 sagatavošanas uzdevumu veikšana
Veiciet uzdevumus, ko ir atklājis jauninājumu analizētāja rīks un kas ir dokumentēti jūsu jaunināšanas projekta plānā. Šie uzdevumi ir jāveic Microsoft Dynamics AX sistēmas administratoram un datu bāzes administratoram (DBA).

[Datu jaunināšana no AX 2012 uz Dynamics 365 for Operations — pirmsjaunināšanas kontrolsaraksts programmā AX 2012](prepare-data-upgrade.md)

### <a name="perform-code-upgrade"></a>Koda jaunināšana
Veiciet uzdevumus, kas tika ieplānoti posma Analizēt koda jaunināšanas novērtēšanas darbībā. Šie uzdevumi ir jāizpilda jūsu izstrādātājiem.

No šī brīža kodu izmaiņas programmā AX 2012 ir jāiesaldē. Programmā AX 2012 koda izmaiņas drīkst veikt tikai ārkārtas gadījumos. Ja tiek veiktas izmaiņas, tās ir manuāli jāpārnes uz jauno koda bāzi.

### <a name="develop-new-code"></a>Jauna koda izstrāde
Veiciet uzdevumus no atbilstības kompetenču analīzes, kas tika veikta posma Analizēt darbībā Izvietot demonstrācijas vidi. Šie uzdevumi, iespējams, ietvers gan funkcionālos uzdevumus, kas definē konfigurāciju, gan izstrādes uzdevumus pielāgojumiem, kas ir saistīti ar jauniem līdzekļiem, ko sāk izmantot.

### <a name="data-upgrade-development-environment"></a>Datu jaunināšana (izstrādes vide)
Kad ir pabeigti koda jaunināšanas uzdevumi, varat pirmoreiz jaunināt savu AX 2012 datu bāzi uz Finance and Operations. Šī pirmā jaunināšana notiek izstrādes vidē, lai jūs varētu vieglāk novērst vai atkļūdot jebkādas šajā posmā atrastās problēmas. Izstrādes vidē problēmu var acumirklī atkļūdot, kodu var pielāgot un jaunināšanu var atkārtoti palaist minūšu laikā. Lielākās smilškastes vidēs šāds ātrums nav iespējams, un tajās problēmu atkļūdošanai un novēršanai, koda atjaunināšanai, atjauninātā koda izvietošanai un jaunināšanas atkārtotai palaišanai būs nepieciešamas vismaz vairākas stundas.

Tālāk esošajā attēlā ir parādīts šis process. Dublējiet AX 2012 datu bāzi, augšupielādējiet to pakalpojumā Azure, atjaunojiet to uz Finance and Operations vidi un pēc tam palaidiet datu jaunināšanu.

![Datu jaunināšana izstrādes vidē](./media/data-upgrade-dev.png)
 
Datu jaunināšana tiek veikta, izmantojot īpaša tipa izvietojamo pakotni. Tas pats mehānisms tiek izmantots, lai izvietotu jaunu Finance and Operations kodu no vienas vides citā vidē.

Pamatā esošā struktūra, kas tiek izmantota, lai konvertētu datu bāzes datus šī procesa laikā, ir gandrīz tāda pati kā jaunināšanas struktūra programmā AX 2012, kuras pamatā ir X++ pakešuzdevumi, kas darbina **ReleaseUpdatexxx** klases.

Detalizētu informāciju skatiet sadaļā [Datu jaunināšana no AX 2012 uz Dynamics 365 for Operations izstrādes vidē](data-upgrade-2012.md).

### <a name="data-upgrade-sandbox-environments"></a>Datu jaunināšana (smilškastes vides)
Kad ir pabeigta datu jaunināšana izstrādes vidē, to pašu procesu var veikt smilškastes vidē. Smilškastes vide ir vide, kurā biznesa lietotāji un funkcionālās grupas dalībnieki var testēt biznesa procesus, izmantojot jauninātos AX 2012 datus un kodu.

Tālāk esošajā attēlā parādīts datu jaunināšanas process smilškastes vidē. Šis process atšķiras ar to, ka tradicionālā SQL dublējuma vietā tiek izmantots bacpac rīks. Šis rīks ir nepieciešams, lai veiktu konvertēšanu starp Microsoft SQL Server un Azure SQL datu bāzi. Tas ir standarta SQL rīks, un tas netiek izmantots tikai programmatūrai Finance and Operations.

![Datu jaunināšana smilškastes vidē](./media/data-upgrade-sandbox.png)

Detalizētu informāciju skatiet sadaļā [Datu jaunināšana no AX 2012 uz Dynamics 365 for Operations smilškastes vidē](upgrade-data-sandbox.md).
 
## <a name="validate"></a>Pārbaudīt
Kad nonāksit posmā Pārbaudīt, jums būs pieejamas vides, kas ietver jaunināto pielāgoto kodu un jauninātos datus. Šajā posmā aprakstīts pārbaudes un testēšanas process, kura mērķis ir noteikt, vai jauninātā vide darbojas, kā paredzēts. Tajā ir aprakstīts arī ieviešanas sagatavošanas process.

### <a name="perform-cutover-testing-and-create-a-cutover-plan"></a>Pārslēgšanas testēšanas veikšana un pārslēgšanas plāna izveide
Termins _pārslēgšana_ šajā kontekstā apraksta beigu procesu, kurā jaunā sistēma tiek ieviesta. Šis process sastāv no uzdevumiem, kas notiek pēc AX 2012 izslēgšanas un pirms Finance and Operations ieslēgšanas. 

Testēšanas mērķis ir izmēģināt pārslēgšanas procesu. Šādi varat palīdzēt garantēt, ka visi, kas ir iesaistīti faktiskajā pārslēgšanas procesā, varēs viegli veikt ieviešanu.

Ir divas galvenās darbplūsmas.

- **Tehniskā darbplūsma** — šī darbplūsma ir datu jaunināšanas izpildes process. Jūsu uzņēmumam būs jāievieš atļautā dīkstāves ilguma ierobežojums. Šajā dīkstāves laikā nebūs pieejams ne AX 2012, ne Finance and Operations. Tehniskajai darbplūsmai, iespējams, vajadzēs pielāgot datu jaunināšanas procedūru, lai tā atbilstu uzņēmuma darbības pārtraukuma ierobežojumam. 
- **Funkcionālā darbplūsma** — pēc datu jaunināšanas Finance and Operations vidē būs jāveic vairāki konfigurācijas uzdevumi. Visi šie uzdevumi ir jādokumentē, jānorāda to daudzums, kā arī tiem jāpiešķir resurss, jo tiem ir jāatbilst tehniskajiem uzdevumiem attiecībā uz uzņēmuma darbības pārtraukuma ierobežojumu.

Papildinformāciju skatiet 
- [Pārbaudīt: pārslēgšanas testēšana](upgrade-cutover-testing.md)
- [Pārbaudīt: programmas pārbaudes process](app-validation-process.md)

### <a name="functional-test-pass"></a>Funkcionālā testa izpilde
Veiciet pilnu funkcionālā testa izpildi visiem biznesa procesiem. Šī testa izpilde būs plaša visu to biznesa procesu atkārtota pārbaude, kas ietver programmatūru Finance and Operations. Šie biznesa procesi ietver gan vecos procesus, kas tika pārnesti no AX 2012, gan jaunos procesus, kas ietver jaunus līdzekļus, kuri tika pirmoreiz paņemti programmatūrā Finance and Operations. 

Atkarībā no koda kvalitātes problēmu novēršanai un atkārtotai pārbaudei var būt nepieciešami vairāki funkcionālā testa izpildes atkārtojumi. Kad problēma ir labota, noteikti atkārtoti pārbaudiet visus iesaistītos procesus, lai palīdzētu garantēt, ka izmaiņas neietekmē lejupstraumes vai augšupstraumes procesu.

Detalizētu informāciju skatiet sadaļā [Pārbaudīt: funkcionālā testēšana](upgrade-functional-validation.md).

### <a name="pre-go-live-checklist"></a>Pirmsieviešanas kontrolsaraksts
Pirmsieviešanas kontrolsaraksts ir ieteicama procedūra, kas var palīdzēt samazināt kļūdu iespējamību galīgās pārnešanas laikā ieviešanai. Vienu nedēļu pirms ieviešanas termiņa pārtrauciet konfigurācijas izmaiņas programmā AX 2012 (sadaļā \<modulis\>\Iestatīšana). Šis konfigurācijas izmaiņu ierobežojums ir tikai procesuāls. Microsoft Dynamics AX sistēmas administratori vienojas šajā brīdī aizturēt šāda tipa izmaiņas.

Ieteicams arī iesaldēt koda izmaiņas Finance and Operations koda bāzē. Turpmākas izmaiņas nav atļautas, ja vien tās nav novērtētas un nav pierādīts, ka tās nebloķē ieviešanu.  

Kad ir nodrošināts konfigurācijas ierobežojums un koda iesaldēšana, ir jāpalaiž datu jaunināšana pēdējoreiz pirms pārslēgšanas. Šādā veidā varat pārliecināties, ka viss joprojām darbojas, kā paredzēts. 

Detalizētu informāciju skatiet sadaļā [Pārbaudīt: sagatavošana ieviešanai](upgrade-go-live-prep.md).



### <a name="supported-upgrade-paths"></a>Atbalstītie jaunināšanas ceļi
Kopš 2017. gada jūnija tiek atbalstīta jaunināšana uz Microsoft Dynamics 365 for Finance and Operations Enterprise izdevumu (versiju 0617) no Microsoft Dynamics AX 2012 R3. Tiek atbalstīti visi AX 2012 R3 kumulatīvie atjauninājumi (CU).

Microsoft Dynamics AX 2012 R2 un Microsoft Dynamics AX 2012 RTM izdevumi pašlaik netiek atbalstīti. Atbalsts tiks pievienots vēlāk 2017. gadā.

Tiek atbalstīta tikai jaunināšana uz mākonī izvietoto Finance and Operations versiju. Jaunināšana uz lokālo versiju netiek atbalstīta. Atbalsts jaunināšanai uz lokālo versiju tiks pievienots vēlāk 2017. gadā.

