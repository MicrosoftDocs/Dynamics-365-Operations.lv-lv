---
title: Instalēt krājumu uztveramības pievienojumprogrammu
description: Šajā rakstā ir aprakstīts, kā instalēt krājumu redzamības pievienojumprogrammu programmai Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 42c2c287e2a813f8bb07ce0c7f21f4224a217946
ms.sourcegitcommit: f2175fe5e900d39f34167d671aab5074b09cc1b8
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/17/2022
ms.locfileid: "9306060"
---
# <a name="install-and-set-up-inventory-visibility"></a>Inventory Visibility instalēšana un iestatīšana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā instalēt krājumu redzamības pievienojumprogrammu programmai Microsoft Dynamics 365 Supply Chain Management.

Lai instalētu Krājumu uztveramības pievienojumprogrammu, izmantojot Microsoft Dynamics Lifecycle Services (LCS). LCS ir sadarbības portāls, kas nodrošina vides un regulāri atjauninātu pakalpojumu kopu, kas palīdz pārvaldīt jūsu Finance and Operations programmu dzīves ciklu. Papildinformāciju skatiet šeit: [Lifecycle Services resursi](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

> [!TIP]
> Ieteicams pievienoties lietotāju grupai Krājumu redzamība– pievienojumprogramma, kurā varat atrast noderīgas ceļvežus, iegūt visjaunākos atjauninājumus un grāmatot visus jautājumus, kas jums varētu rasties par krājumu redzamības redzamību. Lai pievienoties, lūdzu, nosūtiet e-pasta ziņojumu krājumu redzamības [produktu inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) un ietveriet jūsu Piegādes ķēžu pārvaldības vides ID.

## <a name="inventory-visibility-prerequisites"></a>Krājumu redzamības priekšnosacījumi

Pirms instalējat Krājumu redzamību, jums ir jārīkojas šādi:

- Iegūt LCS ieviešanas projektu, kurā ir izvietota vismaz viena vide.
- Pārliecinieties, ka pievienojumprogrammu iestatīšanas priekšnoteikumi ir pabeigti. Plašāku informāciju par šiem priekšnosacījumiem skatiet [Pievienojumprogrammu pārskats](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Krājumu redzamībai nav nepieciešama dubultās rakstīšanas saistīšana.

> [!NOTE]
> Pašlaik atbalstītas valstis un reģioni: Kanāda (CCA, ECA), ASV (WUS, EUS), Eiropas Savienība (NEU, WEU), Apvienotā Karaliste (SUK, WUK), Austrālija (EAU, SEAU), Japāna (EJP, WJP) un Brazīlija (SBR, SCUS).

Ja jums ir kādi jautājumi par šiem priekšnosacījumiem, lūdzu, sazinieties ar Krājumu redzamības preču darba grupu [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com).

## <a name="install-the-inventory-visibility-add-in"></a><a name="install-add-in"></a>Instalēt krājumu uztveramības pievienojumprogrammu

Pirms pievienojumprogrammas instalēšanas reģistrējiet programmu un pievienojiet klienta slepeno informāciju Azure Active Directory (Azure AD) jūsu Azure abonementā. Norādījumus skatiet sadaļā [Pieteikuma reģistrēšana](/azure/active-directory/develop/quickstart-register-app) un [Klienta slepenās informācijas pievienošana](/azure/active-directory/develop/quickstart-register-app#add-a-certificate). Noteikti atzīmējiet programmas **(klienta) ID**, **klienta** noslēpumu un nomnieka ID **vērtības,** jo jums tās vēlāk būs nepieciešamas.

> [!IMPORTANT]
> Ja ir vairāk nekā viena LCS vide, izveidojiet katrai Azure AD no tām atšķirīgu programmu. Ja lietojat vienu lietojumprogrammas ID un nomnieka ID, lai instalētu Inventory Visibility lietojumprogrammu atšķirīgām vidēm, vecākām vidēm tiks rādīta marķiera problēma. Tādēļ būs derīga tikai pēdējā instalēšana.

Pēc pieteikuma reģistrēšanas un klienta noslēpuma pievienošanas Azure AD izpildiet šīs darbības, lai instalētu Krājumu redzamības pievienojumprogrammu.

1. Pierakstieties [LCS](https://lcs.dynamics.com/Logon/Index).
1. Sākumlapā atlasiet projektu, kurā tiek izvietota jūsu vide.
1. Projekta lapā atlasiet vidi, kurā vēlaties instalēt pievienojumprogrammu.
1. Vides lapā ritiniet uz leju, līdz redzat sadaļu **Vides pievienojumprogrammas** sadaļā **Power Platform integrācija**. Tad varat atrast Dataverse vides nosaukumu. Apstipriniet, ka Dataverse vides nosaukums ir tas, ko vēlaties izmantot Krājumu redzamībai.

    > [!NOTE]
    > Pašlaik tiek atbalstītas tikai Dataverse vides, kas izveidotas, izmantojot LCS. Ja jūsu Dataverse vide tika izveidota citādi (piemēram, izmantojot Power Apps administrēšanas centru) un ja tā ir saistīta ar Supply Chain Management vidi, vispirms ir jāsazinās ar Krājumu redzamības produktu grupu, lai novērstu kartēšanas problēmu [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com). Tad instalējiet Krājumu uztveramības pievienojumprogrammu.

1. Sadaļā **Vides pievienojumprogrammas** atlasiet **Instalēt jaunu pievienojumprogrammu**.

    ![Vides lapa portālā LCS](media/inventory-visibility-environment.png "Vides lapa portālā LCS")

1. Atlasiet saiti **Instalēt jaunu pievienojumprogrammu**. Tiek atvērts pieejamo pievienojumprogrammu saraksts.
1. Atlasiet no saraksta **Krājuma redzamība**.
1. Iestatiet savā vidē šādus laukus:

    - **AAD pieteikuma (klienta) ID** — ievadiet iepriekš izveidoto Azure AD pieteikuma klienta ID, kuru atzīmējāt.
    - **AAD nomnieka ID**: Ievadiet nomnieka ID, kuru iepriekš atzīmējāt.

    ![Pievienojumprogrammas iestatīšana lapā](media/inventory-visibility-setup.png "Pievienojumprogrammas iestatīšanas lapa")

1. Piekrist noteikumiem un nosacījumam, atlasot izvēles rūtiņu **Noteikumi un nosacījumi**.
1. Atlasiet **Instalēt**. Pievienojumprogrammas statuss tiks rādīts kā **Instalē**. Pēc tam, kad instalēšana ir pabeigta, atsvaidziniet lapu. Statusam ir jāmainās uz **Instalēts**.
1. Programmas Dataverse kreisās navigācijas rūtī izvēlieties sadaļu **Programmas** un pārbaudiet, vai **Krājumu redzamība** ir veiksmīgi instalēta Power Apps. Ja nav sadaļas **Programmas**, sazinieties ar Krājumu redzamības preču grupu [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com).

> [!NOTE]
> Ja no LCS lapas instalēšanai ir nepieciešama vairāk nekā viena stunda, iespējams, jūsu lietotāja kontam, iespējams, trūkst atļaujas instalēt risinājumus Dataverse vidē. Lai atrisinātu problēmu, izpildiet šīs darbības:
>
> 1. Atceliet krājumu redzamības pievienojumprogrammu instalēšanas procesu no LCS lapas.
> 1. Piesakieties [Microsoft 365 administrēšanas](https://admin.microsoft.com) centrā un pārliecinieties, vai lietotāja kontam, kuru vēlaties izmantot, lai instalētu pievienojumprogrammu, ir piešķirta licence "Dynamics 365 Unified Operations Plāns". Ja nepieciešams, piešķiriet licenci.
> 1. Piesakieties administratora [Power Platform centrā,](https://admin.powerplatform.microsoft.com) izmantojot attiecīgo lietotāja kontu. Pēc tam instalējiet krājumu redzamības pievienojumprogrammu, veicot šādas darbības:
>     1. Atlasiet vidi, kurā vēlaties instalēt pievienojumprogrammu.
>     1. Atlasiet **Dynamics 365 programmas**.
>     1. Atlasiet **programmu Instalēšana**.
>     1. Atlasīt **krājumu redzamību**
>
> 1. Kad instalēšana pabeigta, atgriezieties lapā LCS un mēģiniet vēlreiz atkārtoti **instalēt krājumu redzamības** pievienojumprogrammu.

## <a name="set-up-inventory-visibility-in-supply-chain-management"></a><a name="setup-dynamics-scm"></a>Inventory Visibility iestatīšana pakalpojumā Supply Chain Management

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>Izvietot Krājumu redzamības integrācijas pakotni

Ja jūs palaidāt Supply Chain Management versiju 10.0.17 vai agrāk, sazinieties ar Krājumu redzamības standarta atbalsta komandu [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com), lai iegūtu iepakojuma failu. Pēc tam izvietojiet pakotni LCS.

> [!NOTE]
> Ja izvietošanas laikā rodas versiju neatbilstības kļūda, X++ projekts ir jāimportē manuāli izstrādes vidē. Pēc tam izveidojiet izvietojamu pakotni savā izstrādes vidē un izvietojiet to ražošanas vidē.
>
> Kods ir iekļauts Supply Chain Management versijā 10.0.18. Ja izmantojat šo versiju vai jaunāku, izvietošana nav nepieciešama.

Pārliecinieties, ka jūsu Supply Chain Management vidē ir ieslēgtas šādas funkcijas. (Pēc noklusējuma tās ir ieslēgtas.)

| Līdzekļa apraksts | Koda versija | Pārslēgt klasi |
|---|---|---|
| Iespējot vai atspējot krājumu dimensiju izmantošana InventSum tabulā      | 10.0.11 | InventUseDimOfInventSumToggle      |
| Iespējot vai atspējot krājumu dimensiju izmantošana InventSumDelta tabulā | 10.0.12 | InventUseDimOfInventSumDeltaToggle |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a>Pievienojumprogrammas Krājumu redzamība integrācijas iestatīšana

Kad pievienojumprogramma ir instalēta, sagatavojiet jūsu Piegādes ķēdes pārvaldības sistēmu, lai tā darbotos ar to, rīkojoties tālāk minētajiem soļiem.

1. Pakalpojumā Supply Chain Management atveriet darbvietu **[Līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** un iespējojiet šādus līdzekļus:
    - *Inventory Visibility integrācija* — obligāti.
    - *Inventory Visibility integrācija ar rezervāciju nobīdi* — ieteicama, bet ne obligāta. Vajadzīga 10.0.22. vai jaunāka versija. Papildinformāciju skatiet [Krājumu uztveramības pievienojumprogrammas rezervācijas](inventory-visibility-reservations.md).

1. Dodieties uz **Krājumu pārvaldība \> Iestatījumi \> Inventory Visibility integrācijas parametri**.
1. Atveriet cilni **Vispārīgi** un veiciet tālāk norādītos iestatījumus.
    - **Inventory Visibility gala punkts** — Ievadiet URL videi, kurā palaižat Inventory Visibility. Papildinformāciju skatiet rakstā [Atrast pakalpojuma galamērķi](inventory-visibility-configuration.md#get-service-endpoint).
    - **Maksimālais ierakstu skaits vienā pieprasījumā** — Iestatīts uz maksimālo ierakstu skaitu, kuru ietvert vienā pieprasījumā. Ir jāievada pozitīvs veselais skaitlis, kas ir mazāks vai vienāds ar 1000. Noklusējuma vērtība ir 512. Stingri iesakām paturēt noklusējuma vērtību, ja vien neesat saņēmuši ieteikumi no Microsoft Support vai citu iemeslu dēļ neesat droši, ka tā ir jāmaina.

1. Ja iespējojāt neobligāto līdzekli *Inventory Visibility integrācija ar rezervāciju nobīdi*, atveriet cilni **Rezervāciju nobīde** un veiciet šādus iestatījumus:
    - **Iespējot rezervāciju nobīdi** — Iestatiet uz *Jā*, lai iespējotu šo funkcionalitāti.
    - **Rezervāciju nobīdes pārveidotājs** — Atlasiet krājuma transakcijas statusu, kas nobīdīs Inventory Visibility veiktās rezervācijas. Šis iestatījums nosaka pasūtījuma apstrādes posmu, kurš aktivizē nobīdes. Statusu izseko pasūtījuma krājumu darbības statuss. Izvēlieties vienu no šīm opcijām:
        - *Pasūtījumā* – statusam *On transaction* pasūtījums pēc izveidošanas nosūta korespondējošo pieprasījumu. Nobīžu daudzums būs izveidotā pasūtījuma daudzums.
        - *Rezervēšana* – Pasūtījuma statuss *Rezervēt pasūtītajā pasūtījumā* pēc tā rezervētā, izdotā, pavadzīmes grāmatošanas vai rēķina izrakstīšanas pasūtījums nosūta korespondējošo pieprasījumu. Pieprasījums tiks parādīts tikai vienu reizi, pirmajam solim, kad notiks iepriekš minētais process. Novīdes daudzums būs daudzums, kurā krājuma transakcijas statuss atbilstoŠajā pasūtījuma rindā tiek mainīts no *Pasūtījumā* uz *Rezervēts pasūtījums* (vai uz vēlāku statusu).

1. Dodieties uz **Krājumu pārvaldība \> Periodiskie \> Krājumu redzamības integrāciju** un iespējojiet darbu. Visi krājumu izmaiņu notikumi no Supply Chain Management tagad tiks grāmatoti Krājumu redzamībai.

## <a name="uninstall-the-inventory-visibility-add-in"></a><a name="uninstall-add-in"></a>Atinstalēt Krājumu redzamības pievienojumprogrammu

Lai atinstalētu krājumu redzamības pievienojumprogrammu, rīkojieties šādi:

1. Pierakstieties Supply Chain Management.
1. Dodieties uz **krājumu pārvaldības \> periodisko \> krājumu redzamības** integrāciju un deaktivizējiet darbu.
1. Dodieties uz LCS un atveriet lapu videi, kurā vēlaties atinstalēt pievienojumprogrammu ([skatiet arī sadaļu Krājumu redzamības pievienojumprogramma](#install-add-in)).
1. Atlasiet **atinstalēšanu**.
1. Atinstalēšanas process tagad pārtrauc krājumu redzamības pievienojumprogrammu, noņemiet pievienojumprogrammas reģistrāciju no LCS un dzēš visus pagaidu datus, kas ir saglabāti krājumu redzamības pievienojumprogrammas datu kešatmiņā. Tomēr tur joprojām tiek glabāti primārie krājumu dati Dataverse, kas tika sinhronizēti ar jūsu abonementu. Lai dzēstu šos datus, izpildiet atlikušo procedūru.
1. Atveriet [Power Apps](https://make.powerapps.com).
1. **Vides** atlase navigācijas joslā
1. Atlasiet vidi Dataverse, kas ir piesaistīta jūsu LCS videi.
1. Dodieties **uz** risinājumu un izdzēsiet šādus risinājumus šādā secībā:
    1. Enkura risinājums programmai Inventory Visibility Dynamics 365 risinājumos
    1. Dynamics 365 FNO SCM Krājumu redzamības Applications risinājums
    1. Krājumu pakalpojuma konfigurēšana
    1. Krājumu redzamības savrupā programma
    1. Dynamics 365 FNO SCM Krājumu redzamības pamata risinājums

    Pēc šo risinājumu dzēšanas arī tabulās saglabātie dati arī tiks dzēsti.

> [!NOTE]
> Ja pēc krājumu redzamības pievienojumprogrammas atinstalēšanas atjaunosit Piegādes ķēdes pārvaldības datu bāzi un pēc tam vēlaties atkārtoti instalēt pievienojumprogrammu, pirms pievienojumprogrammas instalēšanas pārliecinieties, Dataverse vai ir izdzēsti vecie abonementā uzglabātie krājumu redzamības dati (kā aprakstīts iepriekšējā procedūrā). Tas novērsīs datu nesakritības problēmas, kas citādi var rasties.

## <a name="clean-inventory-visibility-data-from-dataverse-before-restoring-the-supply-chain-management-database"></a><a name="restore-environment-database"></a> Pirms piegādes ķēdes pārvaldības datu bāzes Dataverse atjaunošanas notīriet krājumu redzamības datus

Ja esat izmantojis krājumu redzamību un pēc tam atjaunojiet Piegādes ķēdes pārvaldības datu bāzi, tad atjaunotā datu bāze var saturēt datus, kas vairs neatbilst datiem, kas iepriekš tika sinhronizēti, izmantojot Krājumu redzamību Dataverse. Šī datu neatbilstība var izraisīt sistēmas kļūdas un citas problēmas. Tāpēc ir svarīgi vienmēr iztīrīt visus krājumu redzamības datus no Dataverse pirms piegādes ķēdes pārvaldības datu bāzes atjaunošanas.

Ja jums ir jāatjauno Piegādes ķēžu pārvaldības datu bāze, izmantojiet sekojošo procedūru:

1. Atinstalēt krājumu redzamības pievienojumprogrammu un noņemt visus saistītos Dataverse datus, kā [aprakstīts krājumu redzamības pievienojumprogrammas atinstalēšanas sadaļā](#uninstall-add-in)
1. Atjaunojiet piegādes ķēdes pārvaldības datu bāzi, piemēram, [kā aprakstīts datu bāzes punkta-laika atjaunot (PITR)](../../fin-ops-core/dev-itpro/database/database-point-in-time-restore.md)[vai laika punktā atjaunot ražošanas datu bāzi uz lodziņlodziņa vidi](../../fin-ops-core/dev-itpro/database/database-pitr-prod-sandbox.md).
1. Ja joprojām vēlaties to izmantot, [atkārtoti instalējiet un iestatiet krājumu redzamības pievienojumprogrammu, kā aprakstīts sadaļā Krājumu redzamības pievienojumprogramma](#install-add-in)[un Iestatiet krājumu redzamības integrāciju](#setup-inventory-visibility-integration)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
