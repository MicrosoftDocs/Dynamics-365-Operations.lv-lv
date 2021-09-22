---
title: Instalēt krājumu uztveramības pievienojumprogrammu
description: Šajā tēmā ir aprakstīts, kā instalēt Krājumu redzamības pievienojumprogrammu programmā Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: b2b85f533a3318701ed08857b899cf9bdd103863
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474824"
---
# <a name="install-and-set-up-inventory-visibility"></a>Inventory Visibility instalēšana un iestatīšana

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Šajā tēmā ir aprakstīts, kā instalēt Krājumu redzamības pievienojumprogrammu programmā Microsoft Dynamics 365 Supply Chain Management.

Lai instalētu Krājumu uztveramības pievienojumprogrammu, izmantojot Microsoft Dynamics Lifecycle Services (LCS). LCS ir sadarbības portāls, kas nodrošina vides un regulāri atjauninātu pakalpojumu kopu, kas palīdz pārvaldīt jūsu Finance and Operations programmu dzīves ciklu.

Papildinformāciju skatiet šeit: [Lifecycle Services resursi](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

## <a name="inventory-visibility-prerequisites"></a>Krājumu redzamības priekšnosacījumi

Pirms instalējat Krājumu redzamību, jums ir jārīkojas šādi:

- Iegūt LCS ieviešanas projektu, kurā ir izvietota vismaz viena vide.
- Pārliecinieties, ka pievienojumprogrammu iestatīšanas priekšnoteikumi ir pabeigti. Plašāku informāciju par šiem priekšnosacījumiem skatiet [Pievienojumprogrammu pārskats](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Krājumu redzamībai nav nepieciešama dubultās rakstīšanas saistīšana.
- Sazinieties ar Krājumu redzamības preču grupu [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com), lai iegūtu šādus nepieciešamos failus:

    - `InventoryServiceApplication.PackageDeployer.zip`
    - `Inventory Visibility Integration.zip` (Ja jūsu darbinātā Supply Chain Management versija ir agrāka nekā versija 10.0.18)

> [!NOTE]
> Pašlaik atbalstītas valstis un reģioni: Kanāda (CCA, ECA), ASV (WUS, EUS), Eiropas Savienība (NEU, WEU), Apvienotā Karaliste (SUK, WUK), Austrālija (EAU, SEAU), Japāna (EJP, WJP) un Brazīlija (SBR, SCUS).

Ja jums ir kādi jautājumi par šiem priekšnosacījumiem, lūdzu, sazinieties ar Krājumu redzamības preču darba grupu.

## <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a>Iestātīt Dataverse

Lai iestatītu Dataverse kopā ar Krājumu redzamību, izmantojiet Package Deployer rīku, lai izvietotu Krājumu redzamības pakotni. Tālāk sniegtās apakšsadaļas apraksta, kā pabeigt katru uzdevumu.

> [!NOTE]
> Pašlaik tiek atbalstītas tikai Dataverse vides, kas izveidotas, izmantojot LCS. Ja jūsu Dataverse vide tika izveidota citādi (piemēram, izmantojot Power Apps administrēšanas centru) un ja tā ir saistīta ar Supply Chain Management vidi, vispirms ir jāsazinās ar Krājumu redzamības produktu grupu, lai novērstu kartēšanas problēmu. Tad instalējiet Krājumu uztveramības pievienojumprogrammu.

### <a name="migrate-from-an-old-version-of-the-dataverse-solution"></a>Migrēt no vecās risinājuma Dataverse versijas

Ja ir instalēta vecāka Krājumu redzamības risinājuma Dataverse versija, lietojiet šīs instrukcijas, lai atjauninātu versiju. Ir divi gadījumi:

- **1. gadījums:** ja manuāli iestatāt Dataverse, importējot `Inventory Visibility Dataverse Solution_1_0_0_2_managed.zip` risinājumu, rīkojieties šādi:

    1. Visbeidzot lejupielādējiet šos trīs failus:

        - `Inventory Visibility Dataverse Solution_1_0_0_3_managed.zip`
        - `InventoryServiceBase_managed.cab`
        - `InventoryServiceApplication.PackageDeployer.zip`

    1. Manuāli importēt `Inventory Visibility Dataverse Solution_1_0_0_3_managed.zip` un `InventoryServiceBase_managed.cab` uz Dataverse un veikt šādas darbības:

        1. Atveriet Dataverse vides URL.
        1. Doties uz lapu **Risinājumi**.
        1. Atlasiet **Importēt**.

    1. Izmantojiet Package Deployer rīku, lai izvietotu `InventoryServiceApplication.PackageDeployer.zip` pakotni. Norādījumus skatiet tālāk šīs tēmas sadaļā [Izmantot Package Deployer rīku pakotnes izvietošanai](#deploy-package).

- **2. gadījums**: ja iestatāt Dataverse, izmantojot Package Deployer rīku, pirms instalējāt vecāko `.*PackageDeployer.zip``InventoryServiceApplication.PackageDeployer.zip` pakotni, lejupielādējiet un veiciet atjauninājumu. Norādījumus skatiet tālāk šīs tēmas sadaļā [Izmantot Package Deployer rīku pakotnes izvietošanai](#deploy-package).

### <a name="use-the-package-deployer-tool-to-deploy-the-package"></a><a name="deploy-package"></a>Izmantojiet Package Deployer rīku, lai izvietotu pakotni

1. Instalējiet izstrādātāju rīkus, kā aprakstīts sadaļā [Lejupielādējiet rīkus no NuGet](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget).
1. Atbloķējiet `InventoryServiceApplication.PackageDeployer.zip` failu, ko lejupielādējāt no Teams, rīkojoties šādi:

    1. Atlasiet un turiet (vai noklikšķiniet ar peles labo pogu) failu, un pēc tam atlasiet **Rekvizīti**.
    1. Dialoglodziņa **Rekvizīti** cilnē **Vispārīgi** atrodiet sadaļu **Drošība**, atlasiet **Atbloķēt** un pielietojiet izmaiņas. Ja cilnē **Vispārīgi** nav sadaļas **Drošība**, fails netiek bloķēts. Šādā gadījumā turpiniet ar nākamo darbību.

    ![Atbloķējiet lejupielādēto failu](media/unblock-file.png "Atbloķējiet lejupielādēto failu")

1. Atarhivēt `InventoryServiceApplication.PackageDeployer.zip`, lai atrastu šādus elementus:

    - `InventoryServiceApplication` mape
    - `[Content_Types].xml` fails
    - `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll` fails

1. Kopējiet katru no šiem vienumiem `.\Tools\PackageDeployment` direktorijā. (Šis direktorijs tika izveidots, kad instalējāt izstrādātāju rīkus.)
1. Palaidiet `.\Tools\PackageDeployment\PackageDeployer.exe` un izpildiet ekrānā redzamos norādījumus, lai importētu risinājumus.

## <a name="install-the-inventory-visibility-add-in"></a><a name="install-add-in"></a>Instalēt krājumu uztveramības pievienojumprogrammu

Pirms pievienojumprogrammas instalēšanas reģistrējiet programmu un pievienojiet klienta slepeno informāciju Azure Active Directory (Azure AD) jūsu Azure abonementā. Norādījumus skatiet sadaļā [Pieteikuma reģistrēšana](/azure/active-directory/develop/quickstart-register-app) un [Klienta slepenās informācijas pievienošana](/azure/active-directory/develop/quickstart-register-app#add-a-certificate). Noteikti atzīmējiet **Programmas (klienta) ID**, **Klienta slepeno informāciju** un **Nomnieka ID** vērtības, jo jums tās būs nepieciešamas vēlāk.

Pēc pieteikuma reģistrēšanas un klienta noslēpuma pievienošanas Azure AD izpildiet šīs darbības, lai instalētu Krājumu redzamības pievienojumprogrammu.

1. Pierakstieties [LCS](https://lcs.dynamics.com/Logon/Index).
1. Sākumlapā atlasiet projektu, kurā tiek izvietota jūsu vide.
1. Projekta lapā atlasiet vidi, kurā vēlaties instalēt pievienojumprogrammu.
1. Vides lapā ritiniet uz leju, līdz redzat sadaļu **Vides pievienojumprogrammas** sadaļā **Power Platform integrācija**. Tad varat atrast Dataverse vides nosaukumu.
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

> [!IMPORTANT]
> Ja jums ir vairāk nekā viena LCS vide, izveidojiet katrai videi atšķirīgu Azure AD lietojumprogrammu. Ja lietojat vienu lietojumprogrammas ID un nomnieka ID, lai instalētu Inventory Visibility lietojumprogrammu atšķirīgām vidēm, vecākām vidēm tiks rādīta marķiera problēma. Tikai pēdējā instalētā vide būs derīga.

## <a name="uninstall-the-inventory-visibility-add-in"></a><a name="uninstall-add-in"></a>Atinstalēt Krājumu redzamības pievienojumprogrammu

Lai atinstalētu Krājumu redzamības pievienojumprogrammu, atlasiet LCS lapā **Atinstalēt**. Atinstalēšanas process pārtrauc Krājumu redzamības pievienojumprogrammu, noņem pievienojumprogrammas reģistrāciju no LCS un dzēš visus pagaidu datus, kas ir saglabāti Krājumu redzamības pievienojumprogrammas datu kešatmiņā. Tomēr jūsu Dataverse abonementā saglabātie primārie krājumu dati netiek dzēsti.

Lai atinstalētu krājumu datus, kas ir saglabāti Dataverse abonementā, atveriet [Power Apps](https://make.powerapps.com), atlasiet navigācijas joslā **Vide** un atlasiet vidi, kas ir piesaistīta jūsu Dataverse LCS videi. Pēc tam dodieties uz **Risinājumi** un izdzēsiet šos piecus risinājumus:

- Noenkurošanas risinājums Krājumu redzamības Dynamics 365 risinājumā
- Dynamics 365 FNO SCM Krājumu redzamības Applications risinājums
- Krājumu pakalpojuma konfigurēšana
- Krājumu redzamības savrupā programma
- Dynamics 365 FNO SCM Krājumu redzamības pamata risinājums

Pēc šo risinājumu dzēšanas arī tabulās saglabātie dati arī tiks dzēsti.

## <a name="set-up-inventory-visibility-in-supply-chain-management"></a><a name="setup-dynamics-scm"></a>Inventory Visibility iestatīšana pakalpojumā Supply Chain Management

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>Izvietot Krājumu redzamības integrācijas pakotni

Ja jūs palaidāt Supply Chain Management versiju 10.0.17 vai agrāk, sazinieties ar Krājumu redzamības standarta atbalsta komandu [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com), lai iegūtu iepakojuma failu. Pēc tam izvietojiet pakotni LCS.

> [!NOTE]
> Ja izvietošanas laikā rodas versiju neatbilstības kļūda, X++ projekts ir jāimportē manuāli izstrādes vidē. Pēc tam izveidojiet izvietojamu pakotni savā izstrādes vidē un izvietojiet to ražošanas vidē.
>
> Kods ir iekļauts Supply Chain Management versijā 10.0.18. Ja izmantojat šo versiju vai jaunāku, izvietošana nav nepieciešama.

Pārliecinieties, ka jūsu Supply Chain Management vidē ir ieslēgtas šādas funkcijas. (Pēc noklusējuma tās ir iespējotas.)

| Līdzekļa apraksts | Koda versija | Pārslēgt klasi |
|---|---|---|
| Iespējot vai atspējot krājumu dimensiju izmantošana InventSum tabulā      | 10.0.11 | InventUseDimOfInventSumToggle      |
| Iespējot vai atspējot krājumu dimensiju izmantošana InventSumDelta tabulā | 10.0.12 | InventUseDimOfInventSumDeltaToggle |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a>Pievienojumprogrammas Krājumu redzamība integrācijas iestatīšana

Kolīdz esat instalējuši pievienojumprogrammu, sagatavojiet Supply Chain Management sistēmu darbam ar to, izpildot tālāk norādītās darbības.

1. Pakalpojumā Supply Chain Management atveriet darbvietu **[Līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** un iespējojiet šādus līdzekļus:
    - *Inventory Visibility integrācija* — obligāti.
    - *Inventory Visibility integrācija ar rezervāciju nobīdi* — ieteicama, bet ne obligāta. Vajadzīga 10.0.22. vai jaunāka versija. Papildinformāciju skatiet [Krājumu uztveramības pievienojumprogrammas rezervācijas](inventory-visibility-reservations.md).

1. Dodieties uz **Krājumu pārvaldība \> Iestatījumi \> Inventory Visibility integrācijas parametri**.
1. Atveriet cilni **Vispārīgi** un veiciet tālāk norādītos iestatījumus.
    - **Inventory Visibility gala punkts** — Ievadiet URL videi, kurā palaižat Inventory Visibility. Papildinformāciju skatiet rakstā [Atrast pakalpojuma galamērķi](inventory-visibility-configuration.md#get-service-endpoint).
    - **Maksimālais ierakstu skaits vienā pieprasījumā** — Iestatīts uz maksimālo ierakstu skaitu, kuru ietvert vienā pieprasījumā. Ir jāievada pozitīvs veselais skaitlis, kas ir mazāks vai vienāds ar 1000. Noklusējuma vērtība ir 512. Stingri iesakām paturēt noklusējuma vērtību, ja vien neesat saņēmuši ieteikumi no Microsoft Support vai citu iemeslu dēļ neesat droši, ka tā ir jāmaina.

1. Ja iespējojāt neobligāto līdzekli *Inventory Visibility integrācija ar rezervāciju nobīdi*, atveriet cilni **Rezervāciju nobīde** un veiciet šādus iestatījumus:
    - **Iespējot rezervāciju nobīdi** — Iestatiet uz *Jā*, lai iespējotu šo funkcionalitāti.
    - **Rezervāciju nobīdes pārveidotājs** — Atlasiet krājuma transakcijas statusu, kas nobīdīs Inventory Visibility veiktās rezervācijas. Šis iestatījums nosaka pasūtījuma apstrādes posmu, kurš aktivizē nobīdes. Statusu izseko pasūtījuma krājumu darbības statuss. Izvēlieties vienu no šīm:
        - *Pasūtījumā* – statusam *On transaction* pasūtījums pēc izveidošanas nosūta korespondējošo pieprasījumu. Nobīžu daudzums būs izveidotā pasūtījuma daudzums.
        - *Rezervēšana* – Pasūtījuma statuss *Rezervēt pasūtītajā pasūtījumā* pēc tā rezervētā, izdotā, pavadzīmes grāmatošanas vai rēķina izrakstīšanas pasūtījums nosūta korespondējošo pieprasījumu. Pieprasījums tiks parādīts tikai vienu reizi, pirmajam solim, kad notiks iepriekš minētais process. Novīdes daudzums būs daudzums, kurā krājuma transakcijas statuss atbilstoŠajā pasūtījuma rindā tiek mainīts no *Pasūtījumā* uz *Rezervēts pasūtījums* (vai uz vēlāku statusu).

1. Dodieties uz **Krājumu pārvaldība \> Periodiskie \> Krājumu redzamības integrāciju** un iespējojiet darbu. Visi krājumu izmaiņu notikumi no Supply Chain Management tagad tiks grāmatoti Krājumu redzamībai.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
