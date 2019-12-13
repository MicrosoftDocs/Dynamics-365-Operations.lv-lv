---
title: E-komercijas novērtējuma vides konfigurēšana
description: Šajā rokasgrāmata sniedz secīgu darbību norādījumus Microsoft Dynamics 365 Commerce priekšskatījuma vides nodrošināšanai un konfigurēšanai.
author: v-chgri
manager: annbe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b0dce2796e69cd8dee87cba176a521c26c81eb1a
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771684"
---
# <a name="configure-an-e-commerce-evaluation-environment"></a>E-komercijas novērtējuma vides konfigurēšana

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šajā rokasgrāmata sniedz secīgu darbību norādījumus Microsoft Dynamics 365 Commerce priekšskatījuma vides nodrošināšanai un konfigurēšanai. Pirms sākt, iesakām vismaz izskatīt dokumentāciju, lai gūtu priekšstatu par to, ko nozīmē process un ko satur rokasgrāmata.

*Piezīme. Ja jums pagaidām nav piešķirta piekļuve Microsoft Dynamics 365 Commerce priekšskatījumam, varat pieprasīt priekšskatījuma piekļuvi no [Commerce vietnes](https://aka.ms/Dynamics365CommerceWebsite).*

## <a name="summary"></a>Kopsavilkums
Lai veiksmīgi nodrošinātu vidi, projektu nepieciešams izveidot ar specifisku preces nosaukumu un veidu. Videi un Retail Cloud Scale Unit arī ir daži specifiski parametri, kas jāizmanto, lai vēlāk sāktu e-tirdzniecības nodrošināšanu. Šīs rokasgrāmatas norādījumi ietver visas nepieciešamās darbības, kas jāveic, un parametrus, kas jāizmanto.

Pēc veiksmīgas nodrošināšanas, ir jāveic dažas pēcnodrošināšanas darbības, lai sagatavotu priekšskatījuma vidi. Dažas darbības nav obligātas, atkarībā no tā, kādus sistēmas aspektus vēlaties novērtēt. Ja mainīsiet savas domas, vienmēr varēsiet veikt pēc izvēles veicamās darbības vēlāk.

Ja jums ir jautājumi par nodrošināšanas darbībām vai rodas kādas problēmas, lūdzu, paziņojiet mums [Microsoft Dynamics 365 Commerce priekšskatījuma Yammer grupā](https://aka.ms/Dynamics365CommercePreviewYammer). 

## <a name="prerequisites"></a>Priekšnosacījumi
Tālāk minēti priekšnosacījumi Dynamics 365 priekšskatījuma vides nodrošināšanai.
* Jums ir piekļuve **Lifecycle Services portālam (LCS)**
* Jūs esat **akceptēts Dynamics 365 Commerce priekšskatījuma programmā**
* Jums ir nepieciešamās atļaujas, lai izveidotu projektu vienumiem **Nākamās iepriekšpārdošanas** vai **Migrēt, izveidot risinājumus un mācīties**
* Jūs esat lomu **Vides vadītājs** vai **Projekta īpašnieks** dalībnieks projektā, kurā nodrošināsiet vidi
* Jums ir administratora piekļuve savam Azure abonementam vai saziņa ar abonementu administratoru, kurš jūsu vieta var veikt divas darbības, kam nepieciešamas administratora atļaujas
* Jums ir pieejams savs **AAD nomnieka ID**
* Jūs esat izveidojis **AAD drošības grupu**, kas jāizmanto kā **E-tirdzniecības sistēmas administratoru grupa**, un jums ir pieejams tās ID.
* Jūs esat izveidojis **AAD drošības grupu**, kas jāizmanto kā **Vērtējumu un apskatu moderatoru grupa**, un jums ir pieejams tās ID (var būt tas pats SG, kas iepriekš minētajai sistēmas administratoru grupai)
## <a name="provisioning-preview-environment"></a>Priekšskatījuma vides nodrošināšana
Šie norādījumi ietver Microsoft Dynamics 365 Commerce priekšskatījuma vides nodrošināšanu. Kad šīs darbības būs veiksmīgi pabeigtas, jums būs priekšskatījuma vide, kas ir gatava konfigurēšanai. Visas šeit aprakstītās darbības notiek LCS portālā.

*Lūdzu, ņemiet vērā, ka piekļuve priekšskatījumam ir saistīta ar LCS kontu un organizāciju, ko norādījāt savā priekšskatījuma pieteikumā. Jums tas pats konts ir jāizmanto nodrošināšanai. Ja jums priekšskatījuma videi ir jāizmanto cits LCS konts vai nomnieks, jums ir jāsniedz mums šī informācija. Kontaktinformāciju, lūdzu, skatiet tālāk sadaļā "Papildu resursi".*
### <a name="before-starting"></a>Pirms sākuma
##### <a name="grant-access-to-e-commerce-applications"></a>Piešķiriet piekļuvi e-tirdzniecības programmām

*Piezīme: **personai, kas piesakās, ir jābūt AAD nomnieka administratoram**. Sekmīgi neveicot šo darbību, pārējās nodrošināšanas darbības neizdosies.*

1. Šai darbībai ir nepieciešams jūsu **AAD nomnieka ID**. Jums jāautorizē e-tirdzniecības programmas, lai piekļūtu jūsu Azure abonementam. Vieglākais veids, kā to paveikt, ir izveidot URL tālāk minētajā veidā.

https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345

2. **Neklikšķiniet URL tieši**, tā vietā kopējiet un ielīmējiet to savā pārlūkprogrammā vai teksta redaktorā un nomainiet **\{AAD_TENANT_ID\}** ar savu **AAD nomnieka ID** pirms pāriešanas uz URL.
3. Jums tiks parādīts Microsoft AAD pieteikšanās dialogs, kur apstiprināt, ka vēlaties piešķirt "Dynamics 365 Commerce (priekšskatījums)" piekļuvi savam abonementam.
4. Jūs nosūtīs uz lapu, kas apstiprinās, vai operācija bijusi veiksmīga.

##### <a name="log-in-to-the-lcs"></a>Pieteikšanās LCS
1. Piesakieties LCS portālā: https://lcs.dynamics.com
1. Pārliecinieties, ka esat pieteicies ar to pašu LCS kontu, kuru izmantojāt, lai pieprasītu piekļuvi priekšskatījumam.
##### <a name="confirm-that-preview-features-are-available-and-enabled"></a>Apstipriniet, ka priekšskatījuma līdzekļi ir pieejami un iespējoti
1. LCS pirmajā lapā ritiniet līdz galam pa labi un noklikšķiniet uz elementa **Priekšskatījuma līdzekļa pārvaldība**.
1. Ritiniet uz leju līdz "PRIVĀTĀS PRIEKŠSKATĪŠANAS LĪDZEKĻI" un pārliecinieties, ka ir pieejami un iespējoti tālāk minētie līdzekļi.
    1. **E-tirdzniecības novērtēšana**
    1. **Tirdzniecības priekšskatījuma programmas vides**
1. Ja sarakstā nevarat redzēt šos līdzekļus, lūdzu, sazinieties ar mums, norādot savu darba e-pastu, LCS kontu un detalizētu informāciju par nomnieku. Lūdzu, zemāk skatiet **Papildu resursi**, lai iegūtu informāciju par to, kā sazināties ar mums.

![Priekšskatījuma pārvaldības elements](./media/preview1.png)

![Priekšskatījuma līdzekļi](./media/preview2.png)
### <a name="create-project"></a>Izveidot projektu
##### <a name="creating-new-project"></a>Jauna projekta izveidošana
1. Noklikšķiniet **+**, lai izveidotu jaunu projektu.
1. Ja esat partneris, izvēlieties **Migrēt, izveidot risinājumus un mācīties**.
1. Ja esat klients, izvēlieties **Nākamās iepriekšpārdošanas**.
1. Ievadiet atbilstošu nosaukumu, aprakstu un nozari.
1. Kā **Preces nosaukums** atlasiet **Dynamics 365 Retail**.
1. Kā **Preces versija** atlasiet **Dynamics 365 Retail**.
1. Kā **Metodoloģija** atlasiet **Dynamics Retail ieviešanas metodoloģija**.
1. Ja nepieciešams, lomas un lietotājus varat importēt no esoša projekta.
1. Noklikšķiniet uz **Izveidot**.
1. Jūs tiksiet nosūtīts uz projekta skatu.
##### <a name="add-azure-connector"></a>Azure Connector pievienošana
1. Ja esat partneris, noklikšķiniet uz **Projekta iestatījumi**, kas atrodas rīku elementā labās puses beigās.
1. Ja esat klients, augšējā izvēlnē izvēlieties **Projekta iestatījumi**.
1. Atlasiet **Azure savienojumi**.
1. Noklikšķiniet **+ pievienot**, lai pievienotu Azure Connector.
1. Ievadiet nosaukumu.
1. Ievadiet savu **Azure abonementa ID**.
1. Iespējojiet **Konfigurēt Azure Resource Manager (ARM) lietošanu**.
1. Pārbaudiet, vai ir pareizs **Azure abonementa AAD nomnieka domēns (vai ID)**. Ja nepieciešams, sazinieties ar savu Azure abonementa administratoru.
1. Noklikšķiniet uz **Tālāk**.
1. Izpildiet ekrānā redzamos norādījumus, lai piešķirtu nepieciešamajām programmām piekļuvi savam abonementam. Ja nepieciešams, sazinieties ar savu Azure abonementa administratoru.
    1. Piesakieties Azure portālā: https://portal.azure.com/
    1. Pārliecinieties, ka esat atlasījis vajadzīgo direktoriju.
    1. No izvēlnes kreisajā pusē noklikšķiniet **Abonementi**.
    1. No saraksta atrodiet vajadzīgo abonementu un atlasiet to. Ja nepieciešams, izmantojiet meklēšanu.
    1. Izvēlnē izvelieties **Piekļuves kontrole (IAM)**.
    1. Noklikšķiniet **Pievienot**, kas atrodas labajā pusē zem **Pievienot lomas piešķiri**. Atveras rūts **Pievienot lomas piešķiri**.
    1. Kā **Loma** atlasiet **Līdzstrādnieks**.
    1. **Piešķirt piekļuvi** atstājiet kā **Azure AD lietotājs, grupa vai pakalpojuma vadītājs**.
    1. **Atlasīt** ievadiet **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.
    1. No saraksts atlasiet **Dynamics Deployment Services [wsfed-Enabled]**.
    1. Noklikšķiniet uz **Saglabāt**.
1. Noklikšķiniet uz **Tālāk**.
1. Izpildiet ekrānā redzamos norādījumus, lai piešķirtu nepieciešamajām programmām piekļuvi savam abonementam. Ja nepieciešams, sazinieties ar savu Azure abonementa administratoru.
1. Noklikšķiniet uz **Tālāk**.
1. Kā **Azure reģions** izvēlieties vai nu **Austrum ASV**, **Austrum ASV 2**, **Rietum ASV** vai **Rietum ASV 2**.
1. Noklikšķiniet uz **Savienot**.
1. Sarakstā ir jāparādās jūsu Azure Connector.
### <a name="import-extension"></a>Importa paplašinājums
1. Pārejiet atpakaļ uz savu projekta sākuma lapu, noklikšķinot uz projekta nosaukuma augšpusē.
1. Ja esat partneris, noklikšķiniet uz **Līdzekļu bibliotēka**, kas atrodas rīku elementā labās puses beigās.
1. Ja esat klients, augšējā izvēlnē izvēlieties **Līdzekļu bibliotēka**.
1. No saraksta kreisajā pusē atlasiet **Pakotne, ko izvieto programmatūra**.
1. No darbību rūts noklikšķiniet **IMPORTĒT**.
1. Atlasiet **Commerce priekšskatījuma demonstrāciju bāzes paplašinājums** no līdzekļu saraksta, kas atrodas **KOPLIETOJAMO LĪDZEKĻU BIBLIOTĒKA**.
1. Noklikšķiniet **Izvēlēties**.
1. Jūs atgriezīsieties līdzekļu bibliotēkā, un jums vajadzētu redzēt saraksta paplašinājumu.

![Projekta izveide — versijas](./media/import.png)
### <a name="deploy-environment"></a>Izvietot vidi

*Piezīme. Iespējams, ka 6., 7. un / vai 8. darbība netiks rādīta, jo ekrāni ar vienu opciju tiek izlaisti. Kad esat skatā **Vides parametri**, lūdzu, apstipriniet, ka teksts "Dynamics 365 Commerce (priekšskatījums) — demonstrācija (10.0.6 ar platformas atjauninājumu 30)" ir tieši virs lauka **Vides nosaukums**. Skatiet ekrānuzņēmumu zemāk.*

1. Augšējā izvēlnē atlasiet **Mākoņvides**.
1. Lai pievienotu vidi, noklikšķiniet **+ pievienot**.
1. Kā **Programmas versija** atlasiet **10.0.6**.
1. Kā **Platformas versija**atlasiet **Platformas atjauninājums 30**.
1. Noklikšķiniet uz **Tālāk**.
1. Kā vides topoloģiju izvēlieties **DEMONSTRĀCIJA**.
1. Kā vides topoloģiju izvēlieties **Dynamics 365 Commerce (priekšskatījums) — demonstrācija**.
1. Ja iepriekš konfigurējāt vienu Azure Connector, tas tiks izmantots šai videi. Ja konfigurējāt vairākus Azure Connectors, jums ir iespēja atlasīt, kuru savienojumu vēlaties izmantot: **Austrum ASV**, **Austrum ASV 2**, **Rietum ASV** vai **Rietum ASV 2** (ieteicams, lai sasniegtu vislabāko veiktspēju līdz pašām beigām)
1. Ievadiet **Vides nosaukums**.
1. Pēc nepieciešamības pielāgojiet VM lielumu. (Mēs iesakām VM SKU **D13 v2**.)
1. Atstājiet **Papildu iestatījumi**, kādi tie ir.
1. Pēc izcenojumu un licencēšanas noteikumu pārskatīšanas ekrānā atzīmējiet izvēles lodziņu, lai izteiktu piekrišanu.
1. Noklikšķiniet uz **Tālāk**.
1. Pēc apliecināšanas, ka informācija ir pareiza, izvietošanas apstiprinājuma ekrānā noklikšķiniet **Izvietot**.
1. Jūs atgriezīsieties skatījumā **Mākoņvides**, un sarakstā ir jāparādās jūsu videi.
1. Jūsu pieprasītā vide tiks parādīta kā stāvoša rindā un tad izvietota. Būs nepieciešams ilgāks laiks, lai tiktu pabeigtas visas vides darbplūsmas, tāpēc, lūdzu, pārbaudiet pēc dažām stundām (aptuveni 6–9 stundas).
1. Pirms turpināt, pārliecinieties, ka jūsu vides statuss ir **Izvietots**.

![Projekta izveide — versijas](./media/project1.png)

![Projekta izveide — 1. topoloģija](./media/project2.png)

![Projekta izveide — 2. topoloģija](./media/project3.png)

![Projekta izveide — vides parametri](./media/project4.png)
### <a name="initialize-rcsu"></a>RCSU inicializēšana
1. Atrodoties skatā **Mākoņvides**, no saraksta atlasiet savu vidi.
1. No vides skata ekrāna labajā pusē noklikšķiniet **Visa informācija**. Tiks parādīts detalizēts vides informācijas skats.
1. **VIDES LĪDZEKĻI**noklikšķiniet **Pārvaldīt**.
1. Cilnē **Mazumtirdzniecība** noklikšķiniet **Inicializēt**. Tiks parādīts RCSU inicializācijas parametru skats.
1. Kā **REĢIONS** atlasiet **Austrum ASV**, **Austrum ASV 2**, **Rietum ASV** vai **Rietum ASV 2**.
1. Kā **VERSIJA** vispirms no nolaižamā saraksta atlasiet **Norādīt versiju**, pēc tam teksta laukā, kas parādās apakšā, norādiet **9.16.19262.5**. *Piezīme. Lūdzu, pārliecinieties, ka šeit **noradāt precīzu versiju**, lai izvairītos no nepieciešamības atjaunināt RCSU vēlāk, lai labotu versiju.*
1. Iespējojiet **Piemērot paplašinājumu**.
1. No paplašinājumu saraksta izvēlieties **Commerce priekšskatījuma demonstrāciju bāzes paplašinājums**.
1. Noklikšķiniet uz **Inicializēt**.
1. Pēc apliecināšanas, ka informācija ir pareiza, izvietošanas apstiprinājuma ekrānā noklikšķiniet **Jā**.
1. Jūs atgriezīsieties skatā **Mazumtirdzniecības pārvaldība** ar aktivizētu cilni **Mazumtirdzniecība**. Jūsu RCSU tika ievietota rindā uz nodrošināšanu.
1. Pirms turpināt, gaidiet, kamēr jūsu RCSU statuss ir **VEIKSMĪGS** (tas ilgs aptuveni 2–5 stundas).
### <a name="initialize-e-commerce"></a>E-tirdzniecības inicializēšana
1. Pārslēdzieties uz cilni **E-tirdzniecība (priekšskatījums)**.
1. Pēc priekšskatījuma piekrišanas pārskatīšanas noklikšķiniet **Iestatīt**.
1. Ievadiet nosaukumu **E-tirdzniecības nomnieka nosaukums**. Tomēr ņemiet vērā, ka tas būs redzams dažos URL, kas norāda uz jūsu e-tirdzniecības instanci.
1. Kā **Retail cloud scale unit nosaukums** atlasiet savu RCSU no saraksta (sarakstā jābūt tikai vienai opcijai).
1. **E-tirdzniecības ģeogrāfija** tiek aizpildīta automātiski, un to nevar mainīt.
1. Lai turpinātu, noklikšķiniet **Tālāk**.
1. Kā **Atbalstītie resursdatoru nosaukumi** ievadiet jebkuru derīgu domēnu (piemēram, www.fabrikam.com).
1. Kā **AAD drošības grupa sistēmas administratoram** ievadiet AAD SG ID, ko vēlaties izmantot kā e-tirdzniecības sistēmas administratoru grupu.
1. Kā **AAD drošības grupa vērtējumu un apskatu moderatoram** ievadiet AAD SG ID, ko vēlaties izmantot kā vērtējumu un apskatu moderatoru grupu.
1. Atstājiet tukšās vērības **B2C** (7 lauki, kas sākas ar B2C).
1. Atstājiet iespējotu **Iespējot vērtējumu un apskatu pakalpojumu**.
1. Noklikšķiniet uz **Inicializēt**.
1. Jūs atgriezīsieties skatā **Mazumtirdzniecības pārvaldība** ar aktivizētu cilni **E-tirdzniecība (priekšskatījums)**. Jūsu e-tirdzniecības inicializēšana ir uzsākta.
1. Pirms turpināt, uzgaidiet, līdz jūsu e-tirdzniecības inicializācijas statuss ir **INICIALIZĀCIJA IR VEIKSMĪGA**.
1. **SAITES** labajā apakšējā stūrī.
    * Pierakstiet saiti **E-tirdzniecības vietne**. Šī ir saite uz jūsu C2 vietnes sakni.
    * Pierakstiet saiti **E-tirdzniecības vietnes pārvaldības rīks**. Šī ir saite uz vietnes pārvaldības rīku (C1 autorēšanas rīku).
## <a name="post-provisioning-steps"></a>Pēcnodrošināšanas darbības
Šajā posmā vide ir nodrošināta visam procesam, bet joprojām ir konfigurācijas darbības, par ko ir jārūpējas pirms uzsākt vides novērtēšanu.
### <a name="before-starting"></a>Pirms sākuma
1. Augšējā izvēlnē atlasiet **Mākoņvides**.
1. No saraksta atlasiet savu vidi.
1. Vides informācijā labajā pusē noklikšķiniet **Visa informācija**.
1. Lai atvērtu izvēlni, noklikšķiniet **Pieteikties**, izvēlieties **Pieteikties vidē**.

Pārliecinieties, ka ir atlasīta **USRT** juridiskā persona (augšējā labajā stūrī).

### <a name="configure-pos"></a>Konfigurēt POS
##### <a name="associate-worker-with-your-identity"></a>Nodarbinātā saistīšana ar jūsu identitāti
1. Izmantojot izvēlni kreisajā pusē, dodieties uz **Moduļi > Mazumtirdzniecība > Darbinieki > Nodarbinātie**.
1. Sarakstā atrodiet un atlasiet vajadzīgo ierakstu **000713 – Endrjū Kollete**.
1. Darbību rūtī noklikšķiniet **Mazumtirdzniecība**.
1. Noklikšķiniet **Saistīt esošu identitāti**.
1. Laukā **E-pasts** (pa labi no **Meklēt, izmantojot e-pastu**) ievadiet savu e-pasta adresi.
1. Noklikšķiniet **Meklēt**.
1. Atlasiet ierakstu ar savu vārdu.
1. Noklikšķiniet uz **Labi**.
1. Noklikšķiniet uz **Saglabāt**.
##### <a name="activate-cloud-pos"></a>mākoņa POS aktivizēšana;
1. Piesakieties LCS portālā.
1. Pārejiet uz savu projektu.
1. Augšējā izvēlnē atlasiet **Mākoņvides**.
1. No saraksta atlasiet savu vidi.
1. Vides informācijā labajā pusē noklikšķiniet **Visa informācija**.
1. Lai atvērtu izvēlni, noklikšķiniet **Pieteikties**, izvēlieties **Pieteikties mākoņa pārdošanas punktā**, būtu jāielādējas POS.
1. Noklikšķiniet uz **Tālāk**.
1. Piesakieties ar savu AAD kontu.
1. **Veikala nosaukums** izvēlieties **Sanfrancisko**.
1. Noklikšķiniet uz **Tālāk**.
1. **Reģistrs un ierīce** izvēlieties **SANFRAN-1**.
1. Noklikšķiniet uz **Aktivizēt**.
1. Jums ir jāiziet no konta un jānonāk POS pieteikšanās ekrānā.
1. Tagad varat pieteikties mākoņa POS pieredzei, izmantojot operatora ID **000713** un paroli **123**.
### <a name="site-setup"></a>Vietnes iestatījumi
1. Piesakieties **vietnes pārvaldības rīkā**, izmantojot iepriekš pierakstīto URL.
1. Noklikšķiniet uz vietnes **Fabrikam**, lai atvērtu vietnes iestatīšanas dialogu.
1. Kā domēnu atlasiet domēnu, ko iepriekš ievadījāt, inicializējot e-tirdzniecību.
1. Kā noklusējuma kanālu atlasiet **Fabrikam paplašinātais tiešsaistes veikals**. *Piezīme. Pārliecinieties, ka atlasāt **paplašināto** tiešsaistes veikalu*
1. Ka noklusējuma valodu atlasiet **en-us**.
1. Atstājiet **Ceļš**, kā tas ir.
1. Noklikšķiniet uz **Labi**.
1. Jūs tiksiet nosūtīts uz vietnes lapu sarakstu.
### <a name="enable-jobs"></a>Darbu iespējošana
1. Piesakieties vidē (HQ).
1. Izmantojot izvēlni kreisajā pusē, dodieties uz **Mazumtirdzniecība > Pieprasījumi un pārskati > Pakešuzdevumi**.
1. Katram darbam zemāk esošajā sarakstā veiciet tālāk minētas darbības.
    * **Apstrādāt mazumtirdzniecības pasūtījuma e-pasta paziņojumu**.
    * **Preču pieejamība**.
    * **P-0001**.
    * **Sinhronizēt pasūtījumu darbu**.
1. Izmantojiet ātro filtru, lai meklētu darbu, izmantojot tā nosaukumu (norādīts iepriekš).
1. Ja darba statuss ir **Aizturēts**, veiciet tālāk minētās darbības.
    1. Atlasiet ierakstu.
    1. No darbību rūts atveriet rīku lenti **Pakešuzdevums** un noklikšķiniet **Mainīt statusu**.
    1. Atlasiet **Gaida** un noklikšķiniet **Labi**.
### <a name="run-full-data-sync"></a>Izpildīt pilnīgu datu sinhronizāciju
1. Izmantojot izvēlni kreisajā pusē, dodieties uz **Moduļi > Mazumtirdzniecība > Galvenās mītnes iestatīšana > Mazumtirdzniecības plānotājs > Kanāla datu bāze**.
1. Kanāls **Noklusējums** ir atlasīts no saraksta kreisajā pusē. *Atlasiet citu pieejamo kanālu (ar nosaukumu **scXXXXXXXXX**)*.
1. Darbību rūtī noklikšķiniet **Pilnīga datu sinhronizācija**.
1. Ievadiet **9999** kā sadales grafiku.
1. Noklikšķiniet uz **Labi**.
1. Noklikšķiniet uz **Labi**.
### <a name="after-these-steps-you-are-ready-to-start-evaluating-your-preview-environment"></a>Pēc šīm darbībām esat gatavs sākt izvērtēt savu priekšskatījuma vidi!
Izmantojiet URL **E-tirdzniecības vietnes pārvaldības rīks**, lai pārietu uz C1 autorēšanas pieredzi un URL **E-tirdzniecības vietne**, lai pārietu uz C2 vietnes pieredzi.

## <a name="additional-resources"></a>Papildu resursi
### <a name="how-to-find-your-aad-tenant-id"></a>Kā atrast savu AAD nomnieka ID
AAD nomnieka ID ir GUID un izskatās kā šajā piemērā: **72f988bf-86f1-41af-91ab-2d7cd011db47**
##### <a name="from-azure-portal"></a>No Azure portāla
1. Piesakieties Azure portālā: https://portal.azure.com/
1. Pārliecinieties, ka esat atlasījis vajadzīgo direktoriju.
1. Izvēlnē kreisajā pusē noklikšķiniet **Azure Active Directory**.
1. Izvēlieties **Rekvizīti** sadaļā **Pārvaldīt**.
1. AAD nomnieka ID tiek parādīts **Direktorijas ID**.
##### <a name="from-openid-connect-metadata"></a>No OpenID Connect metadatiem
Izveidojiet **OpenID URL**, aizstājot **\{YOUR_DOMAIN\}** ar savu domēnu, piemēram, microsoft.com: https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration kļūs par https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration

1. Pārejiet uz **OpenID URL** ar jūsu domēnu tajā.
1. AAD nomnieka ID var redzēt vairākās rekvizītu vērtībās.
1. Atrodiet **authorization_endpoint** un iegūstiet GUID tieši pēc **login.microsoftonline.com/**.
### <a name="how-to-find-the-id-of-your-aad-security-group"></a>Kā atrast savas AAD drošības grupas ID
AAD drošības grupas ID ir GUID un izskatās kā šajā piemērā: **436ea7f5-ee6c-40c1-9f08-825c5811066a**

Šajā darbībā tiek pieņemts, ka lietotājs ir tās grupas dalībnieks, kuras ID viņš mēģina atrast.
1. Pārejiet uz Graph Explorer: https://developer.microsoft.com/en-us/graph/graph-explorer#
1. Noklikšķiniet **Pieteikties ar Microsoft** un piesakieties, izmantojot savus akreditācijas datus.
1. Pēc pierakstīšanās kreisajā pusē noklikšķiniet **rādīt vairāk paraugu**.
1. Labajā rūtī iespējojiet **Grupas**.
1. Aizveriet labo rūti.
1. Noklikšķiniet **visas manas grupas**.
1. Atrodiet savu grupu tekstlodziņā **Atbildes priekšskatījums**.
1. Drošības grupas ID ir atzīmēts zem rekvizīta **id**.
### <a name="test-credit-card-information-to-perform-test-purchases"></a>Kredītkartes informācijas pārbaude, lai veiktu pārbaudes pirkumus
Lai vietnē veiktu pārbaudes transakcijas, varat izmantot tālāk minēto pārbaudes kredītkartes informāciju.

Kartes numurs: 4111-1111-1111-1111, termiņš: 10/20, CVV: 737

*Piezīme. Pārbaudes vietnē nekādā gadījumā nemēģiniet izmantot īstas kredītkartes informāciju!*
### <a name="useful-links"></a>Noderīgas saites
* [LCS (Lifecycle services)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)
* [RCSU (Retail Cloud Scale Unit)](https://docs.microsoft.com/en-us/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)
* [Microsoft Azure portāls](https://azure.microsoft.com/en-us/features/azure-portal)
* [Dynamics 365 Commerce tīmekļa vietne](https://aka.ms/Dynamics365CommerceWebsite)
* [Palīdzības resursi Dynamics 365 Retail](../retail/index.md)
### <a name="microsoft-dynamics-365-commerce-preview-support"></a>Microsoft Dynamics 365 Commerce priekšskatījuma atbalsts
Ja rodas problēmas, veicot nodrošināšanas darbības, lūdzu, apmeklējiet [Microsoft Dynamics 365 Commerce priekšskatījuma Yammer grupu](https://aka.ms/Dynamics365CommercePreviewYammer), lai saņemtu palīdzību. 

Ja rodas problēmas, piekļūstot Yammer grupai, varat sazināties ar mums arī, izmantojot e-pastu **Dynamics365Commerce@microsoft.com**. Šī e-pasta adrese netiek aktīvi pārraudzīta, tāpēc atbilde var kavēties.
***
## <a name="prerequisites-for-optional-features"></a>Priekšnosacījumi līdzekļiem pēc izvēles
Ja vēlaties novērtēt transakciju e-pasta līdzekļus, ir jāizpilda tālāk minētie priekšnosacījumi.
* Jums ir pieejams e-pasta serveris (SMTP serveris), ko var izmantot no Azure abonementa, kur nodrošināt priekšskatījuma vidi.
* Jums ir pieejams servera FQDN/IP, SMTP porta numurs un autentifikācijas informācija.

Ja vēlaties novērtēt Digitālās līdzekļu pārvaldības līdzekļus, jo īpaši ievadīt jaunus daudzkanālu attēlus, ir jāizpilda tālāk minētie priekšnosacījumi.
* Jums ir pieejams savs **CMS nomnieka nosaukums**. Instrukcijas, kā atrast šo nosaukumu, ir atrodamas zemāk.
### <a name="configure-image-backend-optional"></a>Attēla aizmugures konfigurēšana (pēc izvēles)
##### <a name="finding-your-media-base-url"></a>Savas multivides bāzes URL atrašana
*Piezīme. Pirms varat veikt šo darbību, ir jāpaveic **Vietnes iestatīšana**.*
1. Piesakieties vietnes pārvaldības rīkā, izmantojot iepriekš pierakstīto URL.
1. Atveriet vietni **Fabrikam**.
1. Izvēlnē kreisajā pusē izvēlieties **Līdzekļi**.
1. Atlasiet jebkuru atsevišķu attēla līdzekli.
1. Rekvizītu inspektora labajā pusē atrodiet **Publisks URL**. Tajā ir URL.
    * URL piemērs: https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC
1. Aizstājiet URL pēdējo identifikatoru (augstākminētajā URL piemērā — MA1nQC) ar šādu virkni: **search?fileName=**
    * URL piemērs pēc aizstāšanas: https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=
    * Šis ir jūsu **Multivides bāzes URL** — pierakstiet to.
##### <a name="updating-the-media-base-url"></a>Multivides bāzes URL atjaunināšana
1. Piesakieties vidē (HQ).
1. Izmantojot izvēlni kreisajā pusē, dodieties uz **Moduļi > Mazumtirdzniecība > Kanālu iestatīšana > Kanālu profili**.
1. Noklikšķiniet uz **Rediģēt**.
1. **Profila rekvizīti** aizstājiet **Multivides servera bāzes URL** rekvizītu vērtību ar iepriekš izveidoto **Multivides bāzes URL**.
1. Kanālā **Noklusējums** sarakstā pa kreisi atlasiet citu kanālu.
1. **Profila rekvizīti** noklikšķiniet **+ pievienot**.
1. Pievienotajam rekvizītam izvēlieties **Multivides servera bāzes URL**, kā rekvizīta atslēgu un rekvizīta vērtību ievadiet iepriekš izveidoto **Multivides bāzes URL**.
1. Noklikšķiniet uz **Saglabāt**.

### <a name="configure-email-server-optional"></a>E-pasta servera konfigurēšana (pēc izvēles)
Lūdzu, ņemiet vērā, ka šeit ievadītajam SMTP serverim vai e-pasta pakalpojumam jābūt pieejamam tā Azure abonementa robežās, kuru izmantojat videi.
1. Piesakieties vidē (HQ).
1. Izmantojot izvēlni kreisajā pusē, dodieties uz **Moduļi > Mazumtirdzniecība > Parametri > E-pasta parametri**.
1. Noklikšķiniet uz cilnes **SMTP iestatījumi**.
1. **Izejošā pasta servera lauks** ievadiet sava SMTP servera vai e-pasta pakalpojuma FQDN vai IP adresi.
1. Laukā **SMTP porta numurs** ievadiet porta numuru (noklusējums ir 25, kad netiek izmantots SSL).
1. Laukā **Lietotāja vārds** ievadiet vērtību (ja nepieciešama autentifikācija).
1. Laukā **Parole** ievadiet vērtību (ja nepieciešama autentifikācija).
1. Noklikšķiniet uz **Saglabāt**.
1. Noklikšķiniet **Atsvaidzināt**.
1. Noklikšķiniet cilni **E-pasta pārbaude**.
1. E-pasta nodrošinātāja laukā izvēlieties **SMTP**.
1. Laukā **Nosūtīt kam** ievadiet e-pasta adresi, kur jāpiegādā pārbaudes e-pasts.
1. Noklikšķiniet **Nosūtīt pārbaudes e-pastu**.
### <a name="configure-email-templates-optional"></a>E-pasta veidņu konfigurēšana (pēc izvēles)
E-pasta veidne katram transakcijas notikumam, kam vēlaties sūtīt e-pastu, ir jāatjaunina ar derīgu sūtītāja e-pasta adresi.
1. Izmantojot izvēlni kreisajā pusē, dodieties uz **Moduļi > Organizācijas administrācija > Iestatījumi > Organizācijas e-pasta veidnes**.
1. Noklikšķiniet **Rādīt sarakstu**.
1. Katrai no sarakstā iekļautajām veidnēm:
    1. Laukā **Sūtītāja e-pasts** ievadiet sūtītāja e-pasta adresi šai e-pasta veidnei.
    1. (Pēc izvēles) Laukā **Sūtītāja vārds** ievadiet vārdu, kas tiks izmantots kā šī e-pasta veidnes sūtītājs.
1. Noklikšķiniet uz **Saglabāt**.
### <a name="customizing-email-templates-optional"></a>E-pasta veidņu pielāgošana (pēc izvēles)
Iespējams, vēlēsieties pielāgot e-pasta veidnes, lai izmantotu dažādus attēlus vai atjauninātu saites veidnē, izveidojot saiti ar savu priekšskatījuma vidi. Tālāk norādītās darbības izskaidro, kā lejupielādēt noklusējuma veidnes, pielāgot tās un atjaunināt veidnes sistēmā.
1. Izmantojot pārlūkprogrammu, savā datorā lejupielādējiet [Microsoft Dynamics 365 Commerce priekšskatījuma noklusējuma e-pasta veidnes .zip failu](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip), kurā ir tālāk minētie HTML dokumenti.
    1. Pasūtījuma apstiprinājuma veidne
    1. Dāvanu kartes izsniegšanas veidne
    1. Jauna pasūtījuma veidne
    1. Pasūtījuma iesaiņošanas veidne
    1. Pasūtījuma saņemšanas veidne
1. Pielāgojiet veidnes, izmantojot teksta vai HTML redaktoru. Lūdzu, skatiet tālāk redzamo atbalstīto marķieru sarakstu.
1. Piesakieties vidē (HQ).
1. Izmantojot izvēlni kreisajā pusē, dodieties uz **Moduļi > Mazumtirdzniecība > Parametri > Organizācijas e-pasta veidnes**.
1. Paplašiniet sarakstu kreisajā pusē, lai redzētu visas veidnes.
1. Katrai no veidnēm, ko vēlaties pielāgot, veiciet tālāk minētās darbības.
    1. Atlasiet veidni no saraksta.
    1. **E-pasta ziņojuma saturs** no saraksta atlasiet atbilstošo valodas versiju (noklusējums **en-us**).
    1. **E-pasta ziņojuma saturs** noklikšķiniet **Rediģēt**, jums vajadzētu redzēt atveramies rūti **Augšupielādēt e-pasta veidni**.
    1. Noklikšķiniet **Pārlūkot** un atrodiet HTML failu ar pielāgoto saturu.
    1. Noklikšķiniet **Augšupielādēt**, jūsu veidne tiek augšupielādēta sistēmā, un tiek parādīts priekšskatījums.
    1. Noklikšķiniet uz **Labi**.
    1. (Pēc izvēles) Pielāgojiet veidnes rekvizītu **Temats**.
    1. Noklikšķiniet uz **Saglabāt**.

#### <a name="supported-tokens-in-the-email-template"></a>E-pasta veidnē atbalstītie marķieri
Šie marķieri e-pasta atveidošanas laikā tiks aizstāti ar faktiskajām vērtībām, kas attiecas uz klientu un tā pasūtījumu.

**Pārdošanas pasūtījums** — tālāk minētie marķieri attiecas uz vispārēju pārdošanas pasūtījumu.

|Marķējuma nosaukums|Marķieris|
|---|---|
|Pasūtījuma numurs|%salesid%|
|Debitora nosaukums|%customername%|
|Piegādes adrese|%deliveryaddress%|
|Norēķinu adrese|%customeraddress%|
|Ordera datums|%shipdate%|
|Piegādes veids|%modeofdelivery%|
|Atlaide|%discount%|
|PVN|%tax%|
|Pasūtījuma kopsumma|%total%|

**Pārdošanas rinda** — katrai pasūtījuma precei tiek aizpildīti tālāk minētie marķieri.

*Piezīme. Novietojiet marķierus **Preču saraksts — sākums** un **Preču saraksts — beigas** tā HTML bloka sākumā un beigās, kas atkārtojas katrai precei.*

|Marķējuma nosaukums|Marķieris|
|---|---|
|Preču saraksts — sākums|\<!--%tablebegin.salesline% -->|
|Preču saraksts — beigas|\<!--%tableend.salesline%-->|
|Preces nosaukums|%lineproductname%|
|Apraksts|%lineproductdescription%|
|Daudzums|%linequantity%|
|Rindas vienības cena|%lineprice% (verificēt)|
|rindas preču kopsumma|%linenetamount%|
|rindas atlaide|%linediscount%|
|Nosūtīšanas datums|%lineshipdate%|
|Iepirkuma metode|%linedeliverymode%|
|piegādes adrese|%linedeliveryaddress%|
|Rindas pārdošanas vienība|%lineunit%|

