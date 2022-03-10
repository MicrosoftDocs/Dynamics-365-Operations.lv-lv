---
title: Dynamics 365 Commerce novērtēšanas vides nodrošinājums
description: Šajā tēmā ir paskaidrots, kā nodrošināt programmas Microsoft Dynamics 365 Commerce novērtējuma vidi.
author: psimolin
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: c8241c31e82d124398189666c3a1709d25884b8acd9c8f3b1068529cbd216684
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6777504"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a>Dynamics 365 Commerce novērtēšanas vides nodrošinājums

[!include [banner](includes/banner.md)]

Šajā tēmā ir paskaidrots, kā nodrošināt programmas Microsoft Dynamics 365 Commerce novērtējuma vidi.

Pirms sākat, iesakām ātri iziet caur šai tēmai, lai iegūtu priekšstatu par to, kas ir nepieciešams procesam.

> [!NOTE]
> Commerce novērtējuma vides nav vispārpieejamas, un tās tiek piešķirtas partneriem un klientiem pēc pieprasījuma. Lai iegūtu plašāku informāciju, sazinieties ar sava Microsoft partnera kontaktpersonu.

Lai veiksmīgi nodrošinātu Commerce novērtējuma vidi, ir jāizveido projekts ar noteiktu preces nosaukumu un veidu. Videi un Commerce Scale Unit (CSU) arī ir daži specifiski parametri, kas jāizmanto, vēloties nodrošināt e-tirdzniecību. Šajā tēmā sniegtās instrukcijas apraksta visas nepieciešamās darbības, lai pabeigtu nodrošināšanu, un parametrus, kas jāizmanto.

Pēc veiksmīgas Commerce novērtējuma vides nodrošināšanas ir jāpabeidz dažas pēc nodrošināšanas darbības, lai to sagatavotu izmantošanai. Dažas darbības nav obligātas, atkarībā no sistēmas aspektiem, ko vēlaties novērtēt. Pēc izvēles veicamās darbības vienmēr varat pabeigt vēlāk.

Informāciju par to, kā konfigurēt Commerce novērtējuma vidi pēc tās nodrošināšanas, skatiet [Commerce novērtējuma vides konfigurācija](cpe-post-provisioning.md). Informāciju par to, kā konfigurēt neobligātos līdzekļus Commerce novērtējuma videi, skatiet [Commerce novērtējuma vides neobligāto līdzekļu konfigurācija](cpe-optional-features.md).

## <a name="prerequisites"></a>Priekšnosacījumi

Lai varētu nodrošināt Commerce novērtējuma vidi, ir jābūt ieviestiem tālāk norādītajiem priekšnoteikumiem.

- Jūs esat iekāpis novērtēšanas programmā un jums piešķirta novērtēšanas vides noslodze.
- Jums ir piekļuve Microsoft Dynamics Lifecycle Services (LCS) portālam.
- Jūs esat esošs Microsoft Dynamics 365 partneris vai debitors un varat izveidot Dynamics 365 Commerce projektu.
- Jums ir administratora piekļuve Microsoft Azure abonementam, vai arī jūs kontaktējaties ar abonementa administratoru, kurš nepieciešamības gadījumā var jums palīdzēt.
- Jums ir pieejams savs Azure Active Directory (Azure AD) nomnieka ID.
- Jūs esat izveidojis Azure AD drošības grupu, ko var izmantot kā e-tirdzniecības sistēmas administratora grupu, un jums ir pieejams tās ID.
- Jūs esat izveidojis Azure AD drošības grupu, ko var izmantot kā vērtējumu un pārskatu moderatora grupu, un jums ir pieejams tās ID. (Šī drošības grupa var būt tā pati, kas e-tirdzniecības sistēmas administratora grupa.)

Ņemiet vērā, ka šis saraksts nav pilnīgs. Ja rodas kādas problēmas, sazinieties ar Microsoft partnera kontaktpersonu, lai saņemtu palīdzību.

## <a name="provision-your-commerce-evaluation-environment"></a>Commerce novērtējuma vides nodrošināšana

Šīs procedūras izskaidro, kā nodrošināt Commerce novērtējuma vidi. Pēc to veiksmīgas pabeigšanas Commerce novērtējuma vide būs gatava konfigurēšanai. Visas šeit aprakstītās darbības notiek LCS portālā.

### <a name="create-a-new-project"></a>Izveidot jaunu projektu

Lai LCS izveidotu jaunu projektu, veiciet tālāk norādītās darbības.

1. Lai izveidotu projektu, LCS sākumlapā atlasiet pluszīmi (**+**).
1. Labās puses rūtī veiciet vienu no tālāk norādītajām darbībām.

    - Ja esat partneris, atlasiet **Migrēt, izveidot risinājumus un mācīties**.
    - Ja esat klients, atlasiet **Nākamās iepriekšpārdošanas**.

1. Ievadiet nosaukumu, aprakstu un nozari.
1. Laukā **Preces nosaukums** atlasiet **Dynamics 365 Commerce**.
1. Laukā **Preces versija** atlasiet **Dynamics 365 Commerce**.
1. Laukā **Metodoloģija** atlasiet **Dynamics Retail ieviešanas metodoloģija**.
1. Pēc izvēles: varat importēt lomas un lietotājus no esoša projekta.
1. Atlasiet **Izveidot**. Tiks parādīts projekta skats.

### <a name="add-the-azure-connector"></a>Azure Connector pievienošana

Lai Azure savienotāju pievienotu LCS projektam, veiciet darbības, kas norādītas sadaļā [Pabeigt Azure Resource Manager (ARM) pievienošanas procesu](../fin-ops-core/dev-itpro/deployment/arm-onboarding.md).

### <a name="deploy-the-environment"></a>Vides izvietošana

Lai izvietotu vidi, veiciet tālāk norādītās darbības.

> [!NOTE]
> Iespējams, jums nebūs jāveic 6., 7. un / vai 8. darbību, jo tiek izlaistas lapas, kurās ir viena opcija. Kad atrodaties skatā **Vides parametri**, apstipriniet, ka teksts **Dynamics 365 Commerce - Demo (10.0.* x* ar Platform update *xx*)** parādās tieši virs lauka **Vides nosaukums**. Detalizētu informāciju skatiet attēlā, kas tiek parādīts pēc 8. darbības.

1. Augšējā izvēlnē atlasiet **Mākoņvides**.
1. Lai pievienotu vidi, atlasiet **Pievienot**.
1. Laukā **Programmas versija** atlasiet visjaunāko versiju. Ja jums ir īpaša nepieciešamība atlasīt programmas versiju, kas nav visjaunākā versija, neatlasiet versiju pirms **10.0.14**.
1. Laukā **Platformas versija** izmantojiet platformas versiju, kas tiek automātiski izvēlēta jūsu izvēlētajai programmas versijai. 

    ![Pieteikumu un platformu versiju atlasīšana.](./media/project1.png)

1. Atlasiet **Nākamais**.
1. Kā vides topoloģiju atlasiet **Demonstrācija**.

    ![1. vides topoloģijas atlasīšana.](./media/project2.png)

1. Lapā **Izvietot vidi** ievadiet vides nosaukumu. Atstājiet papildu iestatījumus, kādi tie ir.

    ![Vides lapas izvietošana.](./media/project4.png)

1. Pielāgojiet VM lielumu pēc vajadzības. (Mēs iesakām VM noliktavas vienību \[SKU\] **D13 v2**.)
1. Pārskatiet cenu noteikšanas un licencēšanas nosacījumus un pēc tam atzīmējiet izvēles rūtiņu, lai norādītu, ka piekrītat tiem.
1. Atlasiet **Nākamais**.
1. Izvietošanas apstiprinājuma lapā pārbaudiet, vai informācija ir pareiza, un pēc tam atlasiet **Izvietot**. Jūs atgriezīsieties skatā **Mākoņvides**, un sarakstā ir jāparādās jūsu videi.

    Jūsu pieprasītā vide parādīsies kā stāvoša rindā un tad izvietota. Vides darbplūsmas prasīs kādu laiku, līdz tiks pabeigtas. Tāpēc pārbaudiet vēlreiz pēc aptuveni sešām līdz deviņām stundām.

1. Pirms turpināt, pārliecinieties, ka jūsu vides statuss ir **Izvietots**.

### <a name="initialize-the-commerce-scale-unit-cloud"></a>Commerce Scale Unit (mākoņa) inicializēšana

Lai inicializētu CSU, veiciet tālāk norādītās darbības.

1. Skatā **Mākoņvides** atlasiet saraksta savu vidi.
1. Vides skatā labajā pusē atlasiet **Visa informācija**. Parādīsies detalizēts vides informācijas skats.
1. **Vides līdzekļi** atlasiet **Pārvaldīt**.
1. Cilnē **Komercija** atlasiet **Inicializēt**. Parādīsies CSU inicializācijas parametru skats.
1. Laukā **Reģions** atlasiet reģionu, kas ir tāds pats vai tuvu reģionam, kurā tika izvietota vide.
1. Atstājiet lauku **Versija**, kā tas ir.
1. Atlasiet **Inicializēt**.
1. Izvietošanas apstiprinājuma lapā pārbaudiet, ka informācija ir pareiza, un pēc tam atlasiet **Jā**. **Commerce pārvaldības** skats tie atkal parādīts tur, kur ir atlasīt cilne **Commerce**. Jūsu CSU tika ievietota rindā uz nodrošināšanu.
1. Pirms turpināt, pārliecinieties, ka jūsu CSU statuss ir **Veiksmīgs**. Inicializācija ilgst aptuveni divas līdz piecas stundas.

Ja nevarat atrast saiti **Pārvaldība** vides informācijas skatā, sazinieties ar Microsoft kontaktpersonu, lai saņemtu palīdzību.

Izvietošanas procesa laikā, iespējams, saņemsit šādu kļūdas ziņojumu:

> Novērtējuma (demonstrācijas/testa) vidēm jāreģistrē mēroga vienību savienotāja programma \<application ID\> galvenajā birojā.

Ja CSU inicializācija neizdodas un saņemat šo kļūdas ziņojumu, pierakstiet programmas ID, kas ir vispārēji unikāls identifikators (GUID), un pēc tam izpildiet nākamajā sadaļā norādītās darbības, lai reģistrētu CSU izvietošanas programmu komponentā Commerce Headquarters.

### <a name="register-the-csu-deployment-application-in-commerce-headquarters-if-required"></a>CSU izvietošanas programmas reģistrācija Commerce Headquarters (ja nepieciešams)

Lai reģistrētu CSU izvietošanas programmu Commerce Headquarters, veiciet tālāk norādītās darbības.

1. Komponentā Commerce Headquarters dodieties uz **Sistēmas administrēšana \> Iestatīšana \> Azure Active Directory programmas**.
1. Kolonnā **Klienta ID** ievadiet programmas ID no saņemtā CSU inicializēšanas kļūdas ziņojuma.
1. Kolonnā **Nosaukums** ievadiet jebkādu apraksta tekstu (piemēram, **CSU novērtējums**).
1. Kolonnā **Lietotāja ID** ievadiet **RetailServiceAccount**.
1. Atkārtoti mēģiniet CSU inicializāciju un izvietošanu no LCS.

### <a name="initialize-e-commerce"></a>E-tirdzniecības inicializēšana

Lai inicializētu e-tirdzniecību, veiciet tālāk norādītās darbības.

1. Cilnē **E-tirdzniecība** pārskatiet piekrišanu novērtējumam un pēc tam atlasiet **Iestatīšana**.
1. Laukā **E-tirdzniecības novērtējuma nosaukums** ievadiet nosaukumu. Ņemiet vērā, ka šis nosaukums parādīsies dažos URL vietrāžos, kas norāda uz jūsu e-tirdzniecības instanci.
1. Laukā **Commerce Scale Unit nosaukums** atlasiet savu CSU. (Sarakstā jābūt tikai vienai opcijai.)

    Lauks **E-tirdzniecības ģeogrāfija** tiek iestatīts automātiski.

1. Lai turpinātu, atlasiet **Tālāk**.
1. Laukā **Atbalstītie resursdatora nosaukumi** ievadiet jebkuru derīgu domēnu, piemēram, `www.fabrikam.com`.
1. Laukā **Sistēmas administratora AAD drošības grupa** ievadiet tās drošības grupas nosaukuma pirmos dažus burtus, ko vēlaties izmantot, un pēc tam atlasiet lupas simbolu, lai skatītu meklēšanas rezultātus. Sarakstā atlasiet pareizo drošības grupu.
1.  Laukā **Vērtējumu un pārskatu moderatora AAD drošības grupa** ievadiet tās drošības grupas nosaukuma pirmos dažus burtus, ko vēlaties izmantot, un pēc tam atlasiet lupas simbolu, lai skatītu meklēšanas rezultātus. Sarakstā atlasiet pareizo drošības grupu.
1. Atstājiet opciju **Iespējot vērtējumu un pārskatu pakalpojumu** iestatītu uz **Jā**.
1. Atlasiet **Inicializēt**. **Commerce pārvaldības** skats tie atkal parādīts tur, kur ir atlasīt cilne **e-komercija**. Ir uzsākta e-tirdzniecības inicializēšana.
1. Pirms turpināt, uzgaidiet, līdz e-tirdzniecības inicializācijas statuss ir **Inicializācija veiksmīga**.
1. Apakšā pa labi no **Saites** norakstiet URL tālāk noradītajām saitēm.

    * **E-tirdzniecības vietne** — saite uz jūsu e-tirdzniecības vietnes sakni.
    * **Commerce vietņu veidotājs** – saite uz vietnes pārvaldības rīku.

## <a name="next-steps"></a>Turpmākās darbības

Lai turpinātu nodrošināšanas procesu un konfigurētu Commerce novērtējuma vidi, skatiet sadaļu [Commerce novērtējuma vides konfigurācija](cpe-post-provisioning.md).

## <a name="additional-resources"></a>Papildu resursi

[Dynamics 365 Commerce novērtējuma vides pārskats](cpe-overview.md)

[Konfigurēt Dynamics 365 Commerce novērtējuma vidi](cpe-post-provisioning.md)

[BOPIS konfigurācija Dynamics 365 Commerce novērtējuma videi](cpe-bopis.md)

[Izvēles funkciju konfigurācija Dynamics 365 Commerce novērtējuma videi](cpe-optional-features.md)

[Dynamics 365 Commerce novērtējuma vide Bieži uzdotie jautājumi](cpe-faq.md)

[Microsoft Lifecycle Services (LCS)](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[Commerce Scale Unit (mākonis)](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[Microsoft Azure portāls](https://azure.microsoft.com/features/azure-portal)

[Dynamics 365 Commerce tīmekļa vietne](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]