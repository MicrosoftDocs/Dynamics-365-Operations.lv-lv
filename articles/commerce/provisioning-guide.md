---
title: Commerce priekšskatījuma vides nodrošināšana
description: Šajā tēmā ir paskaidrots, kā nodrošināt Microsoft Dynamics 365 Commerce priekšskatījuma vidi.
author: psimolin
manager: annbe
ms.date: 01/06/2020
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b77d2cbbc100aeae5dcd53ddbe69ff2e4435da13
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934752"
---
# <a name="provision-a-commerce-preview-environment"></a>Commerce priekšskatījuma vides nodrošināšana

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Šajā tēmā ir paskaidrots, kā nodrošināt Microsoft Dynamics 365 Commerce priekšskatījuma vidi.

Pirms sākt, iesakām vismaz izskatīt visu šo tēmu, lai gūtu priekšstatu par to, ko nozīmē process un ko satur šī tēma.

> [!NOTE]
> Ja jums pagaidām nav piešķirta piekļuve Dynamics 365 Commerce priekšskatījumam, varat pieprasīt priekšskatījuma piekļuvi no [Commerce vietnes](https://aka.ms/Dynamics365CommerceWebsite).

## <a name="overview"></a>Pārskats

Lai veiksmīgi nodrošinātu savu Commerce priekšskatījuma vidi, jāizveido projekts ar noteiktu preces nosaukumu un veidu. Videi un Retail Cloud Scale Unit (RCSU) arī ir daži specifiski parametri, kas jāizmanto, vēlāk nodrošinot e-tirdzniecību. Šajā tēmā sniegtās instrukcijas apraksta visas nepieciešamās darbības, kas jāizpilda, un parametrus, kas jāizmanto.

Pēc veiksmīgas savas Commerce priekšskatījuma vides nodrošināšanas ir jāpabeidz dažas pēcnodrošināšanas darbības, lai to sagatavotu. Dažas darbības nav obligātas, atkarībā no sistēmas aspektiem, ko vēlaties novērtēt. Pēc izvēles veicamās darbības vienmēr varat pabeigt vēlāk.

Informāciju par to, kā konfigurēt Commerce priekšskatījuma vidi pēc tās nodrošināšanas, skatiet [Commerce priekšskatījuma vides konfigurēšana](cpe-post-provisioning.md). Informāciju par to, kā konfigurēt neobligātos līdzekļus savai Commerce priekšskatījuma videi, skatiet [Commerce priekšskatījuma vides neobligāto līdzekļu konfigurēšana](cpe-optional-features.md).

Ja jums ir jautājumi par nodrošināšanas darbībām vai ja rodas kādas problēmas, lūdzu, paziņojiet Microsoft [Microsoft Dynamics 365 Commerce priekšskatījuma Yammer grupā](https://aka.ms/Dynamics365CommercePreviewYammer).

## <a name="prerequisites"></a>Priekšnosacījumi

Lai varētu nodrošināt savu Commerce priekšskatījuma vidi, ir jābūt nodrošinātiem tālāk norādītajiem priekšnosacījumiem.

- Jums ir piekļuve Microsoft Dynamics Lifecycle Services (LCS) portālam.
- Jūs esat akceptēts Dynamics 365 Commerce priekšskatījuma programmā.
- Jums ir nepieciešamās atļaujas, lai izveidotu projektu vienumiem **Nākamās iepriekšpārdošanas** vai **Migrēt, izveidot risinājumus un mācīties**.
- Jūs esat lomu **Vides vadītājs** vai **Projekta īpašnieks** dalībnieks projektā, kurā nodrošināsiet vidi.
- Jums ir administratora piekļuve savam Microsoft Azure abonementam vai jūs varat sazināties ar abonementu administratoru, kurš jūsu vietā var pabeigt divas darbības, kam nepieciešamas administratora atļaujas.
- Jums ir pieejams savs Azure Active Directory (Azure AD) nomnieka ID.
- Jūs esat izveidojis Azure AD drošības grupu, ko var izmantot kā e-tirdzniecības sistēmas administratora grupu, un jums ir pieejams tās ID.
- Jūs esat izveidojis Azure AD drošības grupu, ko var izmantot kā vērtējumu un pārskatu moderatora grupu, un jums ir pieejams tās ID. (Šī drošības grupa var būt tā pati, kas e-tirdzniecības sistēmas administratora grupa.)

### <a name="find-your-azure-ad-tenant-id"></a>Sava Azure AD nomnieka ID atrašana

Jūsu Azure AD nomnieka ID ir globāli unikāls identifikators (globally unique identifier — GUID), kas līdzinās šim piemēram: **72f988bf-86f1-41af-91ab-2d7cd011db47**.

#### <a name="find-your-azure-ad-tenant-id-by-using-the-azure-portal"></a>Sava Azure AD nomnieka ID atrašana, izmantojot Azure portālu

1. Pierakstieties [Azure portālā](https://portal.azure.com/).
1. Pārliecinieties, ka ir atlasīta vajadzīgā direktorija.
1. Kreisās puses izvēlnē atlasiet **Azure Active Directory**.
1. Sadaļā **Pārvaldīt** atlasiet **Rekvizīti**. Jūsu Azure AD nomnieka ID parādās sadaļā **Direktorijas ID**.

#### <a name="find-your-azure-ad-tenant-id-by-using-openid-connect-metadata"></a>Sava Azure AD nomnieka ID atrašana, izmantojot OpenID Connect metadatus

Izveidojiet OpenID URL, aizvietojot **\{YOUR\_DOMAIN\}** ar savu domēnu, piemēram, `microsoft.com`. Piemēram, `https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration` kļūs par `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration`.

1. Atveriet OpenID URL, kas satur jūsu domēnu.

    Varat atrast sava Azure AD nomnieka ID vairākās rekvizītu vērtībās.

1. Atrodiet **authorization\_endpoint** un izgūstiet GUID, kas tiek parādīts tūlīt pēc `login.microsoftonline.com/`.

### <a name="find-your-azure-ad-security-group-id"></a>Sava Azure AD drošības grupas ID atrašana

Jūsu Azure AD drošības grupas ID ir GUID, kas līdzinās šim piemēram: **436ea7f5-ee6c-40c1-9f08-825c5811066a**.

Šajā procedūrā tiek pieņemts, ka esat grupas dalībnieks, kurai mēģināt atrast ID.

1. Atveriet [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer#).
1. Atlasiet **Pierakstīties ar Microsoft** un pierakstieties, izmantojot savus akreditācijas datus.
1. Kreisajā pusē atlasiet **rādīt vairāk paraugu**.
1. Labajās puses rūtī iespējojiet **Grupas**.
1. Aizveriet labo rūti.
1. Atlasiet **visas manas grupas**.
1. Laukā **Atbildes priekšskatījums** atrodiet savu grupu. Drošības grupas ID tiek parādīts rekvizītā **id**.

## <a name="provision-your-commerce-preview-environment"></a>Savas Commerce priekšskatījuma vides nodrošināšana

Šīs procedūras izskaidro, kā nodrošināt Commerce priekšskatījuma vidi. Pēc veiksmīgas to pabeigšanas Commerce priekšskatījuma vide būs gatava konfigurēšanai. Visas šeit aprakstītās darbības notiek LCS portālā.

> [!IMPORTANT]
> Priekšskatījuma piekļuve ir piesaistīta LCS kontam un organizācijai, ko norādījāt sava priekšskatījuma pieteikumā. Jums jāizmanto tas pats konts, lai nodrošinātu Commerce priekšskatījuma vidi. Ja Commerce priekšskatījuma videi jums jāizmanto cits LCS konts vai nomnieks, jums Microsoft jānorāda šī detalizētā informācija. Kontaktinformāciju skatiet tālāk tēmā esošajā sadaļā [Commerce priekšskatījuma vides atbalsts](#commerce-preview-environment-support).

### <a name="grant-access-to-e-commerce-applications"></a>Piešķiriet piekļuvi e-tirdzniecības programmām

> [!IMPORTANT]
> Personai, kas pierakstās, jābūt Azure AD nomnieka administratoram, kuram ir Azure AD nomnieka ID. Ja šī darbība nav veiksmīgi pabeigta, pārējās nodrošināšanas darbības neizdosies.

Lai autorizētu e-tirdzniecības pieteikumus piekļuvei Azure abonementam, veiciet tālāk noradītās darbības.

1. Sastādiet URL tālāk norādītajā formātā.

    `https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345`

1. Kopējiet un ielīmējiet vietrādi URL savā pārlūkprogrammā vai teksta redaktorā, un aizstājiet **\{AAD\_TENANT\_ID\}** ar sava Azure AD nomnieka ID. Pēc tam atveriet URL.
1. Pierakstieties Azure AD pierakstīšanās dialoglodziņā un apstipriniet, ka vēlaties piešķirt **Dynamics 365 Commerce (priekšskatījums)** piekļuvi savam abonementam. Jūs tiekat novirzīts uz lapu, kas norādīs, vai operācija bija veiksmīga.

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a>Apstiprināšana, ka LCS ir pieejami un ieslēgti priekšskatījuma līdzekļi

Lai apstiprinātu, ka LCS ir pieejami un ieslēgti priekšskatījuma līdzekļi, veiciet tālāk norādītās darbības.

1. Pierakstieties [LCS portālā](https://lcs.dynamics.com), izmantojot to pašu LCS kontu, ko izmantojāt, lai pieprasītu piekļuvi priekšskatījumam.
1. LCS sākumlapā ritiniet līdz galam pa labi un atlasiet elementu **Priekšskatīt līdzekļa pārvaldību**.

    ![Priekšskatījuma pārvaldības elements](./media/preview1.png)

1. Ritiniet uz leju līdz **Privātie priekšskatīšanas līdzekļi** un apstipriniet, ka ir pieejami un ieslēgti tālāk norādītie līdzekļi.

    - E-tirdzniecības novērtēšana
    - Tirdzniecības priekšskatījuma programmas vides

    ![Privātā priekšskatījuma līdzekļi](./media/preview2.png)

1. Ja šie līdzekļi nav redzami sarakstā, sazinieties ar Microsoft un norādiet savu darba e-pasta adresi, LCS kontu un detalizētu informāciju par nomnieku. Kontaktinformāciju skatiet sadaļā [Commerce priekšskatījuma vides atbalsts](#commerce-preview-environment-support).

### <a name="create-a-new-project"></a>Izveidot jaunu projektu

Lai LCS izveidotu jaunu projektu, veiciet tālāk norādītās darbības.

1. Lai izveidotu projektu, LCS sākumlapā atlasiet pluszīmi (**+**).
1. Labās puses rūtī veiciet vienu no tālāk norādītajām darbībām.

    - Ja esat partneris, atlasiet **Migrēt, izveidot risinājumus un mācīties**.
    - Ja esat klients, atlasiet **Nākamās iepriekšpārdošanas**.

1. Ievadiet nosaukumu, aprakstu un nozari.
1. Laukā **Preces nosaukums** atlasiet **Dynamics 365 Retail**.
1. Laukā **Preces versija** atlasiet **Dynamics 365 Retail**.
1. Laukā **Metodoloģija** atlasiet **Dynamics Retail ieviešanas metodoloģija**.
1. Pēc izvēles: varat importēt lomas un lietotājus no esoša projekta.
1. Atlasiet **Izveidot**. Tiks parādīts projekta skats.

### <a name="add-the-azure-connector"></a>Azure Connector pievienošana

Lai savam LCS projektam pievienotu Azure Connector, veiciet tālāk norādītās darbības.

1. Izpildiet kādu no norādītajām transakcijām.

    - Ja esat partneris, labās puses galā atlasiet elementu **Projekta iestatījumi**.
    - Ja esat klients, augšējā izvēlnē atlasiet **Projekta iestatījumi**.

1. Atlasiet **Azure savienojumi**.
1. Lai pievienotu Azure Connector, atlasiet **Pievienot**.
1. Ievadiet nosaukumu.
1. Ievadiet savu Azure abonementa ID.
1. Ieslēdziet opciju **Konfigurēt, lai izmantotu Azure Resource Manager (ARM)**.
1. Pārbaudiet, vai vērtība **Azure abonementa AAD nomnieka domēns (vai ID)** ir pareiza. Ja nepieciešams, sazinieties ar savu Azure abonementa administratoru.
1. Atlasiet **Nākamais**.
1. Izpildiet lapā redzamos norādījumus, lai nepieciešamajiem pieteikumiem piešķirtu piekļuvi savam abonementam. Ja nepieciešams, sazinieties ar savu Azure abonementa administratoru.

    1. Pierakstieties [Azure portālā](https://portal.azure.com/).
    1. Pārliecinieties, vai ir atlasīta pareiza direktorija, un pēc tam kreisās puses izvēlnē atlasiet **Abonementi**.
    1. Sarakstā atrodiet vajadzīgo abonementu un atlasiet to. Ja nepieciešams, izmantojiet meklēšanas funkciju.
    1. Izvēlnē atlasiet **Piekļuves vadīkla (iAM)**.
    1. Labajā pusē esošajā **Pievienot lomas piešķiri** atlasiet **Pievienot**. Tiks parādīta rūts **Pievienot lomas piešķiri**.
    1. Laukā **Loma** atlasiet **Atbalstītājs**.
    1. Laukā **Piešķirt piekļuvi** atstājiet noklusējuma vērtību, **Azure AD lietotāju, grupu vai pakalpojuma vadītāju**.
    1. **Atlasīt** ievadiet **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.
    1. Sarakstā atlasiet **Dynamics Deployment Services \[wsfed-enabled\]**.
    1. Atlasiet **Saglabāt**.

1. Atlasiet **Nākamais**.
1. Izpildiet lapā redzamos norādījumus, lai nepieciešamajiem pieteikumiem piešķirtu piekļuvi savam abonementam. Ja nepieciešams, sazinieties ar savu Azure abonementa administratoru.
1. Atlasiet **Nākamais**.
1. Laukā **Azure reģions** atlasiet **Austrum ASV**, **Austrum ASV 2**, **Rietum ASV** vai **Rietum ASV 2**.
1. Atlasiet **Savienot**. Sarakstā ir jāparādās jūsu Azure Connector.

### <a name="import-the-commerce-preview-demo-base-extension"></a>Commerce priekšskatījuma demonstrācijas bāzes paplašinājuma imports

Lai sava projektā importētu Commerce priekšskatījuma demonstrācijas bāzes paplašinājumu, veiciet tālāk norādītās darbības.

1. Atveriet sava projekta sākumlapu, augšdaļā atlasot projekta nosaukumu.
1. Izpildiet kādu no norādītajām transakcijām.

    - Ja esat partneris, labās puses galā atlasiet elementu **Līdzekļu bibliotēka**.
    - Ja esat klients, augšējā izvēlnē atlasiet **Līdzekļu bibliotēka**.

1. Sarakstā kreisajā pusē atlasiet **Pakotne, ko izvieto programmatūra**.
1. Atlasiet **Importēt**.
1. **Koplietoto līdzekļu bibliotēka** līdzekļu sarakstā atlasiet **Commerce priekšskatījuma demonstrācijas bāzes paplašinājums**.
1. Atlasiet **Izdot**. Jūs atgriezīsieties līdzekļu bibliotēkā, un jums vajadzētu redzēt saraksta paplašinājumu.

Tālāk redzamajā attēlā ir parādītas darbības, kas jāveic LCS lapā **Līdzekļu bibliotēka**.

![Commerce priekšskatījuma demonstrācijas bāzes paplašinājuma importēšana](./media/import.png)

### <a name="deploy-the-environment"></a>Vides izvietošana

Lai izvietotu vidi, veiciet tālāk norādītās darbības.

> [!NOTE]
> Iespējams, jums nebūs jāveic 6., 7. un / vai 8. darbību, jo tiek izlaistas lapas, kurās ir viena opcija. Kad atrodaties skatā **Vides parametri**, apstipriniet, ka teksts **Dynamics 365 Commerce (priekšskatījums) — Demo (10.0.6 ar platformas atjauninājumu 30)** tiek parādīts tieši virs lauka **Vides nosaukums**. Skatiet attēlu, kas tiek parādīts pēc 8. darbības.

1. Augšējā izvēlnē atlasiet **Mākoņvides**.
1. Lai pievienotu vidi, atlasiet **Pievienot**.
1. Laukā **Pieteikuma versija** atlasiet **10.0.6**.
1. Laukā **Platformas versija** atlasiet **Platformas atjauninājums 30**.

    ![Pieteikumu un platformu versiju atlasīšana](./media/project1.png)

1. Atlasiet **Nākamais**.
1. Kā vides topoloģiju atlasiet **Demonstrācija**.

    ![1. vides topoloģijas atlasīšana](./media/project2.png)

1. Kā vides topoloģiju atlasiet **Dynamics 365 Commerce (priekšskatījums) — demonstrācija**. Ja iepriekš konfigurējāt vienu Azure Connector, tas tiks izmantots šai videi. Ja esat konfigurējis vairākus Azure Connector, varat izvēlēties, kuru savienotāju izmantot: **Austrum ASV**, **Austrum ASV 2**, **Rietum ASV** vai **Rietum ASV 2**. (Lai panāktu vislabāko veiktspēju visu laiku, iesakām atlasīt **Rietum ASV 2**).

    ![2. vides topoloģijas atlasīšana](./media/project3.png)

1. Lapā **Izvietot vidi** ievadiet vides nosaukumu. Atstājiet papildu iestatījumus, kādi tie ir.

    ![Vides lapas izvietošana](./media/project4.png)

1. Pielāgojiet VM lielumu pēc vajadzības. (Mēs iesakām VM noliktavas vienību \[SKU\] **D13 v2**.)
1. Pārskatiet cenu noteikšanas un licencēšanas nosacījumus un pēc tam atzīmējiet izvēles rūtiņu, lai norādītu, ka piekrītat tiem.
1. Atlasiet **Nākamais**.
1. Izvietošanas apstiprinājuma lapā pārbaudiet, vai informācija ir pareiza, un pēc tam atlasiet **Izvietot**. Jūs atgriezīsieties skatā **Mākoņvides**, un sarakstā ir jāparādās jūsu videi.

    Jūsu pieprasītā vide parādīsies kā stāvoša rindā un tad izvietota. Vides darbplūsmas prasīs kādu laiku, līdz tiks pabeigtas. Tāpēc pārbaudiet vēlreiz pēc aptuveni sešām līdz deviņām stundām.

1. Pirms turpināt, pārliecinieties, ka jūsu vides statuss ir **Izvietots**.

### <a name="initialize-rcsu"></a>RCSU inicializēšana

Lai inicializētu RCSU, veiciet tālāk norādītās darbības.

1. Skatā **Mākoņvides** atlasiet saraksta savu vidi.
1. Vides skatā labajā pusē atlasiet **Visa informācija**. Parādīsies detalizēts vides informācijas skats.
1. **Vides līdzekļi** atlasiet **Pārvaldīt**.
1. Cilnē **Mazumtirdzniecība** atlasiet **Inicializēt**. Parādīsies RCSU inicializācijas parametru skats.
1. Laukā **Reģions** atlasiet **Austrum ASV**, **Austrum ASV 2**, **Rietum ASV** vai **Rietum ASV 2**.
1. Laukā **Versija** sarakstā atlasiet **Norādīt versiju** un pēc tam laukā, kas parādās, norādiet **9.16.19262.5**. Pārliecinieties, ka norādāt tieši šeit norādīto versiju. Pretējā gadījumā jums vēlāk būs jāatjaunina RCSU uz pareizo versiju.
1. Ieslēdziet opciju **Lietot paplašinājumu**.
1. Paplašinājumu sarakstā atlasiet **Commerce priekšskatījuma demonstrāciju bāzes paplašinājums**.
1. Atlasiet **Inicializēt**.
1. Izvietošanas apstiprinājuma lapā pārbaudiet, ka informācija ir pareiza, un pēc tam atlasiet **Jā**. Jūs atgriezīsieties skatā **Mazumtirdzniecības pārvaldība**, kur atlasīta cilne **Mazumtirdzniecība**. Jūsu RCSU tika ievietota rindā uz nodrošināšanu.
1. Pirms turpināt, pārliecinieties, ka jūsu RCSU statuss ir **Veiksmīgs**. Inicializācija ilgst aptuveni divas līdz piecas stundas.

### <a name="initialize-e-commerce"></a>E-tirdzniecības inicializēšana

Lai inicializētu e-tirdzniecību, veiciet tālāk norādītās darbības.

1. Cilnē **e-tirdzniecība (priekšskatījums)** pārskatiet piekrišanu priekšskatījumam un pēc tam atlasiet **Iestatīšana**.
1. Ievadiet nosaukumu laukā **E-tirdzniecības nomnieka nosaukums**. Tomēr ņemiet vērā, ka šis nosaukums parādīsies dažos URL, kas norāda uz jūsu e-tirdzniecības instanci.
1. Laukā **Retail Cloud Scale Unit nosaukums** sarakstā atlasiet savu RCSU. (Sarakstā jābūt tikai vienai opcijai.)

    Lauks **E-tirdzniecības ģeogrāfija** tiek iestatīts automātiski, un vērtību nevar mainīt.

1. Lai turpinātu, atlasiet **Tālāk**.
1. Laukā **Atbalstītie resursdatora nosaukumi** ievadiet jebkuru derīgu domēnu, piemēram, `www.fabrikam.com`.
1.  Laukā **AAD drošības grupa sistēmas administratoram** ievadiet dažus pirmos burtu no tās drošības grupas nosaukuma, ko vēlaties izmantot. Atlasiet palielināmo klases ikonu, lai parādītu meklēšanas rezultātus. Izvēlieties drošības grupu no saraksta.
2.  Laukā **AAD drošības grupa vērtējumu un pārskatu moderatoram** ievadiet dažus pirmos burtu no tās drošības grupas nosaukuma, ko vēlaties izmantot. Atlasiet palielināmo klases ikonu, lai parādītu meklēšanas rezultātus. Izvēlieties drošības grupu no saraksta.
1. Atstājiet ieslēgtu opciju **Iespējot vērtējumu un pārskatu pakalpojumu**.
1. Ja jau esat pabeidzis Microsoft Azure Active Directory (Azure AD) piekrišanas darbību, kā aprakstīts sadaļā "Piekļuves piešķiršana e-tirdzniecības pieteikumiem", atlasiet izvēles rūtiņu, lai apstiprinātu savu piekrišanu. Ja vēl neesat pabeidzis šo darbību, jums tā jāveic pirms turpināt inicializāciju. Tekstā atlasiet saiti, kas atrodas blakus izvēles rūtiņai, lai atvērtu piekrišanas dialoglodziņu un pabeigtu darbību.
1. Atlasiet **Inicializēt**. Jūs atgriezīsieties skatā **Mazumtirdzniecības pārvaldība**, kur atlasīta cilne **E-tirdzniecība (priekšskatījums)**. Ir uzsākta e-tirdzniecības inicializēšana.
1. Pirms turpināt, uzgaidiet, līdz e-tirdzniecības inicializācijas statuss ir **Inicializācija veiksmīga**.
1. Apakšā pa labi no **Saites** norakstiet URL tālāk noradītajām saitēm.

    * **E-tirdzniecības vietne** — saite uz jūsu e-tirdzniecības vietnes sakni.
    * **E-tirdzniecības vietnes pārvaldības rīks** — saite uz vietnes pārvaldības rīku.

## <a name="commerce-preview-environment-support"></a>Commerce priekšskatījuma vides atbalsts

Ja rodas problēmas, pabeidzot nodrošināšanas darbības, lūdzu, apmeklējiet [Microsoft Dynamics 365 Commerce priekšskatījuma Yammer grupu](https://aka.ms/Dynamics365CommercePreviewYammer), lai saņemtu palīdzību.

Ja rodas problēmas, mēģinot piekļūt Yammer grupai, varat sazināties ar Microsoft, izmantojot e-pastu <Dynamics365Commerce@microsoft.com>. Šī e-pasta adrese netiek aktīvi uzraudzīta. Tādēļ rēķinieties ar novēlotu atbildi.

## <a name="next-steps"></a>Nākamās darbības

Lai turpinātu nodrošināšanas procesu un konfigurētu Commerce priekšskatījuma vidi, skatiet [Commerce priekšskatījuma vides konfigurēšana](cpe-post-provisioning.md).

## <a name="additional-resources"></a>Papildu resursi

[Commerce priekšskatījuma vides pārskats](cpe-overview.md)

[Commerce priekšskatījuma vides konfigurēšana](cpe-post-provisioning.md)

[Neobligāto līdzekļu konfigurēšana Commerce priekšskatījuma videi](cpe-optional-features.md)

[Commerce priekšskatījuma vides BUJ](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Retail Cloud Scale Unit (RCSU)](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure portāls](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce tīmekļa vietne](https://aka.ms/Dynamics365CommerceWebsite)

[Palīdzības resursi Dynamics 365 Retail](../retail/index.md)
