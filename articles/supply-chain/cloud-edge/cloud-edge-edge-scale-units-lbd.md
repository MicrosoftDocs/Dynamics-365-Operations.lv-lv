---
title: Malas mēroga vienību izvietošana pielāgotajā aparatūrā, izmantojot LBD (priekšskatījums)
description: Šajā tēmā skaidrots, kā nodrošināt lokālās malas skalas vienības, izmantojot pielāgotu aparatūru un izvietošanu, kas ir balstīta uz vietējiem uzņēmuma datiem (LBD).
author: cabeln
ms.date: 04/22/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 0ebbdaab9d6f040497d3158db2712e102b6e9aa8
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/25/2021
ms.locfileid: "7678985"
---
# <a name="deploy-edge-scale-units-on-custom-hardware-using-lbd-preview"></a>Malas mēroga vienību izvietošana pielāgotajā aparatūrā, izmantojot LBD (priekšskatījums)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)] <!--KFM: Until 11/1/2021 -->

Malas apjoma vienībām ir svarīga loma sadalītajā topoloģijā piegādes ķēžu pārvaldībai. Tālākajā topoloģijā varat sadalīt darba slodzi starp Supply Chain Management mākoņa pārkraušanas vietu un papildu mēroga vienībām mākonī vai malā.

Malu skalas vienības var izvietot, izveidojot vietējos biznesa datus (LBD) [lokālajā vidē](../../fin-ops-core/dev-itpro/deployment/on-premises-deployment-landing-page.md) un pēc tam konfigurējot to, lai darbotos kā mēroga vienība jūsu sadalītajā topoloģijā piegādes ķēdes pārvaldībai. To var sasniegt, saistot lokālo LBD vidi ar Supply Chain Management vidi mākonī, kas konfigurēta tā, lai darbotos kā pārkraušanas mezgls.  

Malu skalas vienības pašlaik tiek priekšskatītas. Tāpēc šī tipa vidi var izmantot tikai atbilstoši [priekšskatījuma nosacījumiem](https://aka.ms/scmcnepreviewterms).

Šajā tēmā ir aprakstīts, kā iestatīt lokālas LBD vidi kā malas skalas vienību un pēc tam saistīt to ar pārkraušanas punktu.

## <a name="deployment-overview"></a>Izvietošanas pārskats

Tālāk ir sniegts pārskats par izvietošanas darbībām.

1. **Iespējojiet LBD slotu savā LBD projektā Microsoft Dynamics Lifecycle Services (LCS).**

    Priekšskatījuma laikā LBD malas skalas vienību mērķis ir esošie LBD debitori. Papildu 60 dienu ierobežots LBD smilškastes lodziņa slots tiks nodrošināts tikai specifiskās debitora situācijās.

1. **Iestatiet un izvietojiet LBD vidi ar *tukšu* datu bāzi.**

    Izmantojiet LCS, lai izvietotu LBD vidi ar jaunāko topoloģiju un tukšu datu bāzi. Papildinformāciju skatiet tālāk šīs tēmas sadaļā sadaļā Iestatījumi un [izvietojiet LBD vidi ar tukšu datu bāzes sadaļu](#set-up-deploy). Jums jālieto Supply Chain Management versija 10.0.19 ar platformas atjauninājumu 43 vai jaunāku pārkraušanas punkta un mēroga vienības vidē.

1. **Augšupielādēt mērķa pakotnes LBD projekta aktīvos LCS.**

    Sagatavojiet programmu, platformu un pielāgošanas pakotnes, ko izmantojat pārkraušanas centrā un malu skalas vienībā. Papildinformāciju skatiet tālāk šīs tēmas sadaļā [Augšupielādes mērķa iepakojumos LBD projekta līdzekļa sadaļā LCS](#upload-packages).

1. **Pakalpojumu LBD vidē ar mērķa pakotnēm.**

    Šis solis nodrošina, ka viens un tas pats būvējums un pielāgojumi tiek izvietoti pārkraušanas mezglā un centrā. Papildinformāciju skatiet tālāk šīs tēmas sadaļā [Pakalpojums LBD vide ar mērķa pakotnēm](#service-target-packages).

1. **Pabeidziet mēroga vienības konfigurāciju un darba noslodzes piešķiri.**

    Papildinformāciju skatiet tālāk šīs tēmas sadaļā [Piešķirt savu LBD malas skalas vienību pārkraušanas mezglu](#assign-edge-to-hub).

Atlikušajās šīs tēmas sadaļās ir sniegta plašāka informāciju par katru šī procesa posmu.

## <a name="set-up-and-deploy-an-lbd-environment-with-an-empty-database"></a><a name="set-up-deploy"></a>Iestatiet un izvietojiet LBD vidi ar tukšu datu bāzi

Šis solis izveido funkcionālu LBD vidi. Tomēr videi nav nepieciešama tāda pati lietojumprogrammas un platformas versija kā pārkraušanas mezgla videi. Turklāt tam joprojām trūkst pielāgojumu, un tie vēl nav iespējoti darbam kā mēroga vienība.

1. Sekojiet instrukcijām [Iestatījumi un lokālo vižu izvietošana (Platformas atjauninājums 41 vai jaunāks)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md). Jums jālieto Supply Chain Management versija 10.0.19 ar platformas atjauninājumu 43 vai jaunāku pārkraušanas punkta un mēroga vienības vidē

    > [!IMPORTANT]
    > **Pirms** izpildāt šajā tēmā aprakstītās darbības, izlasiet pārējās šīs sadaļas darbības.

1. Pirms aprakstīt konfigurāciju infrastruktūras \\ConfigTemplate.xml failā, palaidiet šādu skriptu:

    ```powershell
    .\Configure-ScriptsForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > Šajā skriptā tiks noņemta konfigurācija, kas nav nepieciešama malu skalas vienību izvietošanai.

1. Iestatiet datu bāzi, kas satur tukšus datus, kā aprakstīts sadaļā [Datu bāzu konfigurēšana](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb). Izmantojiet šo darbību tukšā datus.bak failā.
1. Iestatiet pirmsizvietošanas skriptu. Papildinformācija: [Vietējā aģenta pirmsizvietošanas un pēcizvietošanas skripti](../../fin-ops-core/dev-itpro/lifecycle-services/pre-post-scripts.md).

    1. Kopējiet saturu no mapes **ScaleUnit** **Infrastruktūras skriptos** uz mapi **Skripti**, kas atrodas vidē iestatītā aģenta failu glabāšanas koplietojumā. Tipisks ceļš ir \\\\lbdiscsi01\\aģents\\Skripti.
    2. Izveidojiet skriptu **PreDeployment.ps1**, kas izsauks skriptus, izmantojot nepieciešamos parametrus. Pirmsizvēršanas skripts ir jāizvieto **Skriptu** mapē aģenta faila glabāšanas koplietojumā. Pretējā gadījumā to nevar palaist. Tipisks ceļš ir \\\\lbdiscsi01\\aģents\\Skripti\\PreDeployment.ps1.

        Skripta PreDeployment.ps1 saturs būs līdzīgs šim piemēram.

        ```powershell
        $agentShare = '\\lbdiscsi01\agent'
        
        Write-Output "AgentShare is set to $agentShare" 
        & $agentShare\Scripts\Configure-CloudandEdge.ps1 -AgentShare $agentShare -InstanceId '@A' -DatabaseServer 'lbdsqla01.contoso.com' -DatabaseName 'AXDB'
        ```

        > [!NOTE]
        > Parametrā InstanceId jābūt tikai divām rakstzīmēm. Pirmā rakstzīme ir @, otra var būt jebkurš lielais angļu alfabēta burts.
        >
        > - Derīgās vērtības:
        >   - @D
        >   - @X
        > - Nederīgās vērtības:
        >   - @a
        >   - @4
        >   - @#

1. Izvietojiet vidi, izmantojot jaunāko pieejamo pamata topoloģiju.

## <a name="upload-target-packages-into-lbd-project-assets-in-lcs"></a><a name="upload-packages"></a>Augšupielādēt mērķa pakotnes LBD projekta aktīvos LCS

Šis solis sagatavo programmas versiju, platformas versiju un pielāgojumus, kas tiks pārieti uz LBD mēroga vienības vidi.

1. Augšupielādējiet to pašu kombinēto lietojumprogrammas/platformas pakotni, kas tika lietota pārkraušanas centra vidē, LCS lokālo projektu līdzekļu bibliotēkā.
1. Augšupielādējiet to pašu kombinēto lietojumprogrammas/platformas pakotni, kas tika lietota pārkraušanas centra vidē, LCS lokālo projektu līdzekļu bibliotēkā.

## <a name="service-the-lbd-environment-with-target-packages"></a><a name="service-target-packages"></a>Pakalpojumi LBD vidē ar mērķa pakotnēm

Šis solis sagatavo programmas versiju, platformas versiju un pielāgojumus, kas tiks pārieti uz LBD mēroga vienības vidi.

1. Pakalpojumu LBD vidē ar kombinēto lietojumprogrammu/platformu pakotni, ko augšupielādējat iepriekšējā darbībā.
1. Pakalpojumu LBD vidē ar kombinēto lietojumprogrammu/platformu pakotni, ko augšupielādējat iepriekšējā darbībā.

    ![Uzturēt > Lietot atjauninājumus LCS atlasīšana.](media/cloud_edge-LBD-LCS-ServiceLBDEnv1.png "Uzturēt > Lietot atjauninājumus LCS atlasīšana")

    ![Pielāgošanas pakotnes atlasīšana.](media/cloud_edge-LBD-LCS-ServiceLBDEnv2.png "Pielāgošanas pakotnes atlasīšana")

## <a name="assign-your-lbd-edge-scale-unit-to-a-hub"></a><a name="assign-edge-to-hub"></a>LBD malas skalas vienības piešķiršana pārkraušanas centram

Kamēr malu skalas vienības joprojām ir priekšskatījumā, ir jāizmanto [mēroga vienību izvietošana un konfigurācijas rīki](https://github.com/microsoft/SCMScaleUnitDevTools), kas ir pieejami GitHub, lai piešķirtu LBD malas skalas vienību pārkraušans centram. Šis process ļauj LBD konfigurāciju izmantot kā malas skalas vienību un saistīt to ar pārkraušanas centru. Šis process ir līdzīgs vienas kastes izstrādes vides konfigurēšanai.

1. Lejupielādējiet pēdējo [SCMScaleUnitDevTools](https://github.com/microsoft/SCMScaleUnitDevTools/releases) laidienu un atarhivējiet faila saturu.
1. Izveidot faila `UserConfig.sample.xml` kopiju un nosaukt to par `UserConfig.xml`.
1. Izveidojiet Microsoft Azure Active Directory (Azure AD) programmu savā Azure AD nomniekā , kā tas ir norādīts [Mēroga vienības un darba noslodzes izvietošanas rokasgrāmatā](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide#aad-application-registrations).
    1. Tiklīdz ir izveidots, dodieties uz Azure AD pieteikumu veidlapu (SysAADClientTable) pārkraušanas punktā.
    1. Izveidojiet jaunu ierakstu un iestatiet **Klienta ID** uz jūsu izveidotās programmas ID. Iestatiet **Nosaukumu** uz *ScaleUnits* un **Lietotāja ID** kā *Administrators*.

1. Izveidojiet Active Directory federācijas pakalpojuma (AD FS) programmu, kā tas ir norādīts [Mēroga vienības un darba noslodzes izvietošanas rokasgrāmatā](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide#adfs-application-registrations).
    1. Tiklīdz ir izveidots, dodieties uz Azure AD pieteikumu veidlapu (SysAADClientTable) savā malu mēroga vienībā.
    1. Izveidojiet jaunu ierakstu un iestatiet **Klienta ID** uz jūsu izveidotās programmas ID. Iestatiet **Lietotāja ID** kā *Administrators*.

1. Modificējiet `UserConfig.xml` failu.
    1. Sadaļā `InterAOSAADConfiguration` ievadiet informāciju no iepriekš izveidotās Azure AD programmas.
        - Elementā `AppId` ievadiet Azure lietojumprogrammas ID.
        - Elementā `AppSecret` ievadiet Azure lietojumprogrammas slepeno informāciju.
        - Elementam `Authority` ir jāietver URL, kas norāda jūsu nomnieka drošības iestādi.

        ```xml
        <InterAOSAADConfiguration>
            <AppId>8dab14f6-97b1-48e3-b51b-350b45f6ede5</AppId>
            <AppSecret>k6em-_7.lopty56TGUedDTVhtER-j_6anY1</AppSecret>
            <Authority>https://login.windows.net/contoso.onmicrosoft.com</Authority>
        </InterAOSAADConfiguration>
        ```

    1. Zem `ScaleUnitConfiguration` sadaļas pirmajai `ScaleUnitInstance` modificējiet `AuthConfiguration` sadaļu.
        - Elementā `AppId` ievadiet Azure lietojumprogrammas ID.
        - Elementā `AppSecret` ievadiet Azure lietojumprogrammas slepeno informāciju.
        - Elementam `Authority` ir jāietver URL, kas norāda jūsu nomnieka drošības iestādi.

        ```xml
        <AuthConfiguration>
            <AppId>8dab14f6-97b1-48e3-b51b-350b45f6ede5</AppId>
            <AppSecret>k6em-_7.lopdz.6d3DTVOtf9Lo-j_6anY1</AppSecret>
            <Authority>https://login.windows.net/contoso.onmicrosoft.com</Authority>
        </AuthConfiguration>
        ```

    1. Papildus šim pašam `ScaleUnitInstance` iestatiet šādas vērtības šai rindai:
        - Elementā `Domain` norādiet pārkraušanas centra URL. Piemēram: `https://cloudhub.sandbox.operations.dynamics.com/`
        - Elementā `EnvironmentType` pārliecinieties, vai ir iestatīta vērtība `LCSHosted`.

    1. Zem `ScaleUnitConfiguration` sadaļas pirmajai `ScaleUnitInstance` modificējiet `AuthConfiguration` sadaļu.
        - Elementā `AppId` ievadiet AD FS lietojumprogrammas ID.
        - Elementā `AppSecret` ievadiet AD FS lietojumprogrammas slepeno informāciju.
        - Elementam `Authority` ir jāietver jūsu AD FS instances URL.

        ```xml
        <AuthConfiguration>
            <AppId>26b16f25-21d8-4d36-987b-62df292895aa</AppId>
            <AppSecret>iZFfObgI6lLtY9kEbBjEFV98NqI5_YZ0e5SBcWER</AppSecret>
            <Authority>https://adfs.contoso.com/adfs</Authority>
        </AuthConfiguration>
        ```

    1. Papildus šim pašam `ScaleUnitInstance` iestatiet šādas vērtības šai rindai:
        - Elementā `Domain` norādiet savu malu mēroga vienības URL. Piemēram: https://ax.contoso.com/
        - Elementā `EnvironmentType` pārliecinieties, vai ir iestatīta vērtība LBD.
        - Elementā `ScaleUnitId` ievadiet to pašu vērtību, ko norādījāt `InstanceId`, konfigurējot `Configure-CloudandEdge.ps1` pirmsizvietošanas skriptu.

        > [!NOTE]
        > Ja neizmantojat noklusējuma ID (@A), atjauniniet ScaleUnitId katrai ConfiguredWorkload sadaļā Darba noslodzes.

1. Atveriet PowerShell un dodieties uz mapi, kurā ir `UserConfig.xml` fails.

1. Palaidiet rīku ar šo komandu.

    ```powershell
    .\CLI.exe
    ```

    > [!NOTE]
    > Pēc katras darbības būs atkal jāstartē rīks.

1. Rīkā atlasiet **2. Sagatavojiet vides darba noslodzes instalācijai**. Tad izpildiet tālākās darbības:
    1. Atlasiet **1. Sagatavojiet pārkraušanas centru**.
    1. Atlasiet **2. Sagatavojiet mēroga vienību**.

    > [!NOTE]
    > Ja šī komanda netiek palaista tīrīšanas instalācijā un tā neizdodas, veiciet šādas darbības:
    >
    > - Izņemiet visas mapes no `aos-storage` mapes (izņemot `GACAssemblies`).
    > - Izpildiet šādu SQL komandu savā biznesa datu bāzē (AXDB):
    >
    > ```sql 
    > delete from storagefoler
    > ```

1. Izpildiet šādas SQL komandas savā biznesa datu bāzē (AXDB):

    ```sql
    delete from FEATUREMANAGEMENTMETADATA
    delete from FEATUREMANAGEMENTSTATE
    delete from NUMBERSEQUENCESCOPE
    ```

1. Pārbaudiet, vai izmaiņu izsekošana ir iespējota jūsu biznesa datu bāzē (AXDB)
    1. SQL Server Management Studio (SSMS) sākšana.
    1. Ar peles labo pogu noklikšķiniet uz biznesa datu bāzes (AXDB) un atlasiet rekvizītus.
    1. Atveramajā logā atlasiet **Mainīt izsekošanu** un veiciet šādus iestatījumus:

        - **Izmaiņu izsekošana:** *Patiess*
        - **Saglabāšanas periods:** *7*
        - **Ieturējumu vienības:** *Dienas*
        - **Automātiskā tīrīšana:** *Patiess*

1. Rīkā atlasiet **3. Instalējiet darba slodzi**. Tad izpildiet tālākās darbības:
    1. Atlasiet **1. Instalējiet pārkraušanas centrā**.
    1. Atlasiet **2. Instalēt uz Mēroga vienībām**.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
