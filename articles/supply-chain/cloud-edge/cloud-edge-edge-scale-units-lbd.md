---
title: Malas mēroga vienību izvietošana pielāgotajā aparatūrā, izmantojot LBD
description: Šajā tēmā skaidrots, kā nodrošināt lokālās malas skalas vienības, izmantojot pielāgotu aparatūru un izvietošanu, kas ir balstīta uz vietējiem uzņēmuma datiem (LBD).
author: cabeln
ms.date: 04/22/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: f1ab0a2c289f48dd8bfb7529f0dcc694a97f18ea
ms.sourcegitcommit: e91a1797192fd9bc4048b445bb5c1ad5d333d87d
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/01/2021
ms.locfileid: "7729079"
---
# <a name="deploy-edge-scale-units-on-custom-hardware-using-lbd"></a>Malas mēroga vienību izvietošana pielāgotajā aparatūrā, izmantojot LBD

[!include [banner](../includes/banner.md)]

Malas apjoma vienībām ir svarīga loma sadalītajā topoloģijā piegādes ķēžu pārvaldībai. Tālākajā topoloģijā varat sadalīt darba slodzi starp Supply Chain Management mākoņa pārkraušanas vietu un papildu mēroga vienībām mākonī vai malā.

Malu skalas vienības var izvietot, izveidojot vietējos biznesa datus (LBD) [lokālajā vidē](../../fin-ops-core/dev-itpro/deployment/on-premises-deployment-landing-page.md) un pēc tam konfigurējot to, lai darbotos kā mēroga vienība jūsu sadalītajā topoloģijā piegādes ķēdes pārvaldībai. To var sasniegt, saistot lokālo LBD vidi ar Supply Chain Management vidi mākonī, kas konfigurēta tā, lai darbotos kā pārkraušanas mezgls.  

Šajā tēmā ir aprakstīts, kā iestatīt lokālas LBD vidi kā malas skalas vienību un pēc tam saistīt to ar pārkraušanas punktu.

## <a name="deployment-overview"></a>Izvietošanas pārskats

Tālāk ir sniegts pārskats par izvietošanas darbībām.

1. **Iespējojiet LBD slotu savā LBD projektā Microsoft Dynamics Lifecycle Services (LCS).**

1. **Iestatiet un izvietojiet LBD vidi ar *tukšu* datu bāzi.**

    Izmantojiet LCS, lai izvietotu LBD vidi ar jaunāko topoloģiju un tukšu datu bāzi. Papildinformāciju skatiet tālāk šīs tēmas sadaļā sadaļā Iestatījumi un [izvietojiet LBD vidi ar tukšu datu bāzes sadaļu](#set-up-deploy). Jums jāizmanto Piegādes ķēdes pārvaldības versija 10.0.21 vai jaunāka tās versija pārkraušanas punkta un mēroga vienības vidēs.

1. **Augšupielādēt mērķa pakotnes LBD projekta aktīvos LCS.**

    Sagatavojiet programmu, platformu un pielāgošanas pakotnes, ko izmantojat pārkraušanas centrā un malu skalas vienībā. Papildinformāciju skatiet tālāk šīs tēmas sadaļā [Augšupielādes mērķa iepakojumos LBD projekta līdzekļa sadaļā LCS](#upload-packages).

1. **Pakalpojumu LBD vidē ar mērķa pakotnēm.**

    Šis solis nodrošina, ka viens un tas pats būvējums un pielāgojumi tiek izvietoti pārkraušanas mezglā un centrā. Papildinformāciju skatiet tālāk šīs tēmas sadaļā [Pakalpojums LBD vide ar mērķa pakotnēm](#service-target-packages).

1. **Pabeidziet mēroga vienības konfigurāciju un darba noslodzes piešķiri.**

    Papildinformāciju skatiet tālāk šīs tēmas sadaļā [Piešķirt savu LBD malas skalas vienību pārkraušanas mezglu](#assign-edge-to-hub).

Atlikušajās šīs tēmas sadaļās ir sniegta plašāka informāciju par katru šī procesa posmu.

## <a name="set-up-and-deploy-an-lbd-environment-with-an-empty-database"></a><a name="set-up-deploy"></a> Iestatiet un izvietojiet LBD vidi ar tukšu datu bāzi

Šis solis izveido funkcionālu LBD vidi. Tomēr videi nav nepieciešama tāda pati lietojumprogrammas un platformas versija kā pārkraušanas mezgla videi. Turklāt tam joprojām trūkst pielāgojumu, un tie vēl nav iespējoti darbam kā mēroga vienība.

1. Sekojiet instrukcijām [Iestatījumi un lokālo vižu izvietošana (Platformas atjauninājums 41 vai jaunāks)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md). Jums jāizmanto Piegādes ķēdes pārvaldības versija 10.0.21 vai jaunāka tās versija pārkraušanas punkta un mēroga vienības vidēs. Turklāt infrastruktūras skriptiem jālieto versija 2.12.0 vai jaunāka. 

    > [!IMPORTANT]
    > **Pirms** izpildāt šajā tēmā aprakstītās darbības, izlasiet pārējās šīs sadaļas darbības.

1. Pirms aprakstīt konfigurāciju infrastruktūras \\ ConfigTemplate.xml failā, palaidiet šādu skriptu:

    ```powershell
    .\Configure-ScriptsForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > Šajā skriptā tiks noņemta konfigurācija, kas nav nepieciešama malu skalas vienību izvietošanai.

1. Iestatiet datu bāzi, kas satur tukšus datus, kā aprakstīts sadaļā [Datu bāzu konfigurēšana](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb). Izmantojiet šo darbību tukšā datus.bak failā.
1. Pēc datu bāzu konfigurēšanas soļa izpildes izpildiet tālāk norādīto skriptu, lai konfigurētu Mēroga vienības [...](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) Instrument Instrumenttor datu bāzi.

    > [!NOTE]
    > Konfigurējiet finanšu pārskatu datu bāzi datu bāzes [konfigurēšanas darbības](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) laikā.

    ```powershell
    .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName EdgeScaleUnit
    ```

    Skripts Initialize-Database.ps1 veic šādas darbības:

    1. Izveidojiet tukšu datu bāzi ar nosaukumu **ScaleUnitAlmDb**.
    2. Kartējiet lietotājus uz datu bāzes lomām, pamatojoties uz norādīto tabulu.

        | Lietotājs            | Veids | Datu bāzes loma |
        |-----------------|------|---------------|
        | svc-LocalAgent$ | gMSA (datu) | Db \_ īpašnieks     |

1. Turpiniet sekot instrukcijām [iestatīšanas un lokālas vides izvietošanā (platformas atjaunināšana 41 vai jaunāka)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md).
1. Pēc TAM, kad esat [pabeidzis AD FS konfigurēšanas](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) darbību, sekojiet šiem soļiem:

    1. Izveidojiet jaunu Active Directory federācijas pakalpojumu (AD FS) programmu, kas iespējos Neplānotās instrumentācijas pakalpojumu komunicēt ar savu Application Object Server (AOS).

        ```powershell
        # Host URL is your DNS record\host name for accessing the AOS
        .\Create-ADFSServerApplicationForEdgeScaleUnits.ps1 -HostUrl 'https://ax.d365ffo.onprem.contoso.com'
        ```

    1. Izveidot jaunu Azure Active Directory ( ) Azure AD programmu, kas iespējos Neplānotās instrumentācijas pakalpojumu komunicēt ar Mēroga vienību pārvaldības pakalpojumu.

        ```powershell
        # Example .\Create-SumAADApplication.ps1 -ConfigurationFilePath ..\ConfigTemplate.xml -TenantId '6240a19e-86f1-41af-91ab-dbe29dbcfb95' -ApplicationDisplayName 'EdgeAgent-SUMCommunication-EN01'
        .\Create-SumAADApplication.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                       -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                       -ApplicationDisplayName '<Whichever name you want the Azure AD app to have>'
        ```

1. Turpiniet sekot instrukcijām [iestatīšanas un lokālas vides izvietošanā (platformas atjaunināšana 41 vai jaunāka)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md). Kad ir jāievada lokālā aģenta konfigurācija, pārliecinieties, ka iespējojat malas skalas vienības līdzekļus un nodrošināt visus nepieciešamos parametrus.

    ![Malas skalas vienības līdzekļu iespējošana.](media/EnableEdgeScaleUnitFeatures.png "Malas skalas vienības līdzekļu iespējošana.")

1. Pirms vides izvietošanas no LCS iestatiet pirmsizvēršanas skriptu. Papildinformācija: [Vietējā aģenta pirmsizvietošanas un pēcizvietošanas skripti](../../fin-ops-core/dev-itpro/lifecycle-services/pre-post-scripts.md).

    1. Kopējiet skriptu Configure-CloudAndEdge.ps1 no mapes ScaleUnit infrastruktūras skriptos uz mapi Skripti aģenta failu glabāšanas koplietojumā, kas tika iestatīts **·** **·** **·** vidē. Tipisks ceļš ir \\\\ lbdiscsi01\\ aģents\\ Skripti.
    2. Izveidojiet skriptu **PreDeployment.ps1**, kas izsauks skriptus, izmantojot nepieciešamos parametrus. Pirmsizvēršanas skripts ir jāizvieto **Skriptu** mapē aģenta faila glabāšanas koplietojumā. Pretējā gadījumā to nevar palaist. Tipisks ceļš ir \\\\ lbdiscsi01\\ aģents\\ Skripti\\ PreDeployment.ps1.

        Skripta PreDeployment.ps1 saturs būs līdzīgs šim piemēram.

        ```powershell
        $agentShare = '\\lbdiscsi01\agent'
        
        Write-Output "AgentShare is set to $agentShare" 
        . $PSScriptRoot\Configure-CloudAndEdge.ps1 -AgentShare $agentShare -InstanceId '@A'
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
1. Pēc vides izvietošanas izpildiet tālāk minētās darbības.

    1. Izpildiet šādas SQL komandas savā biznesa datu bāzē (AXDB).

        ```sql
        ALTER TABLE dbo.NUMBERSEQUENCETABLE ENABLE CHANGE_TRACKING WITH (TRACK_COLUMNS_UPDATED = ON)
        delete from NumberSequenceTable
        delete from NumberSequenceReference
        delete from NumberSequenceScope
        delete from FeatureManagementMetadata
        delete from FeatureManagementState
        delete from SysFeatureStateV0
        ```

    1. Palielināt vienlaicīgu maksimālo partijas sesiju par vērtību, kas ir lielāka par 4.

        ```sql
        Update batchserverconfig set maxbatchsessions = '<Replace with number of concurrent batch tasks you want>'
        ```

    1. Pārbaudiet, vai izmaiņu izsekošana ir iespējota jūsu biznesa datu bāzē (AXDB).

        1. Atveriet SQL Server Management Studio (SSMS).
        1. Atlasiet un turiet (vai noklikšķiniet ar peles labo pogu) savu biznesa datu bāzi (AXDB) un pēc tam atlasiet **·** Rekvizīti.
        1. Redzamajā logā atlasiet Izmaiņu izsekošana **un pēc tam iestatiet šādas** vērtības:

            - **Izmaiņu izsekošana:** *Patiess*
            - **Saglabāšanas periods:** *7*
            - **Ieturējumu vienības:** *Dienas*
            - **Automātiskā tīrīšana:** *Patiess*

    1. Pievienojiet iepriekš izveidoto AD FS programmas ID (izmantojot skriptu Create-ADFSServerApplicationForEdgeScaleUnits.ps1) apjoma mērvienību lietojumprogrammu Azure AD tabulai. Šo darbību var manuāli pabeigt, izmantojot lietotāja interfeisu (UI). Alternatīvi to var pabeigt, izmantojot datu bāzi, izmantojot šādu skriptu.

        ```sql
        DECLARE @ALMOrchestratorId NVARCHAR(76) = '<Replace with the ADFS Application ID created in a previous step>';

        IF NOT EXISTS (SELECT TOP 1 1 FROM SysAADClientTable WHERE AADClientId = @ALMOrchestratorId)
        BEGIN
            INSERT INTO SysAADClientTable (AADClientId, UserId, Name, ModifiedBy, CreatedBy)
            VALUES (@ALMOrchestratorId, 'ScaleUnitManagement', 'Scale Unit Management', 'Admin', 'Admin');
        END
        ```

## <a name="set-up-an-azure-key-vault-and-an-azure-ad-application-to-enable-communication-between-scale-units"></a><a name="set-up-keyvault"></a> Iestatīt Azure atslēgu Windows un Azure AD programmu, lai iespējotu sakarus starp mēroga vienībām

1. Pēc vides izvietošanas izveidojiet papildu programmu, lai iespējotu uzticamus sakarus Azure AD starp pārkraušanas punktu un mēroga vienību.

    ```powershell
    .\Create-SpokeToHubAADApplication.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                          -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                          -ApplicationDisplayName '<Whichever name you want the Azure AD app to have>'
    ```

1. Pēc programmas izveides ir jāizveido klienta noslēpums un jāsaglabā informācija Azure atslēgā. Turklāt jums ir jāpiešķir piekļuve izveidotajām programmai, lai varētu izgūt Azure AD noslēpumus, kas tiek glabāti atslēgas krātuvē. Jūsu ērtību gadījumā šis skripts automātiski izpildīs visas nepieciešamās darbības.

    ```powershell
    .\Create-SpokeToHubAADAppSecrets.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                         -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                         -SubscriptionName '<Any subscription within your tenant>' `
                                         -ResourceGroupName '<Any resource group within your subscription>' `
                                         -KeyVaultName '<Any key vault within your resource group>' `
                                         -Location '<Any Azure location where Azure Key Vault is available>' `
                                         -LCSEnvironmentId '<The LCS environment ID of your deployed scale unit>' `
    ```

    > [!NOTE]
    > Ja nav atslēgas, kam ir **norādītā KeyVaultName** vērtība, skripts automātiski izveido jaunu.

1. Pievienojiet tikko Azure AD izveidoto programmas ID (izmantojot skriptu Create-PpabAADApplication.ps1) programmu tabulai jūsu Azure AD pārkraušanas punktā. Šo darbību varat manuāli pabeigt, izmantojot UI.

## <a name="upload-target-packages-into-lbd-project-assets-in-lcs"></a><a name="upload-packages"></a> Augšupielādēt mērķa pakotnes LBD projekta aktīvos LCS

Šis solis sagatavo programmas versiju, platformas versiju un pielāgojumus, kas tiks pārieti uz LBD mēroga vienības vidi.

1. Augšupielādējiet to pašu kombinēto lietojumprogrammas/platformas pakotni, kas tika lietota pārkraušanas centra vidē, LCS lokālo projektu līdzekļu bibliotēkā.
1. Augšupielādējiet to pašu kombinēto lietojumprogrammas/platformas pakotni, kas tika lietota pārkraušanas centra vidē, LCS lokālo projektu līdzekļu bibliotēkā.

## <a name="service-the-lbd-environment-with-target-packages"></a><a name="service-target-packages"></a> Pakalpojumi LBD vidē ar mērķa pakotnēm

Šis solis sagatavo programmas versiju, platformas versiju un pielāgojumus, kas tiks pārieti uz LBD mēroga vienības vidi.

1. Pakalpojumu LBD vidē ar kombinēto lietojumprogrammu/platformu pakotni, ko augšupielādējat iepriekšējā darbībā.
1. Pakalpojumu LBD vidē ar kombinēto lietojumprogrammu/platformu pakotni, ko augšupielādējat iepriekšējā darbībā.

    ![Piemēro atjauninājumus LCS.](media/cloud_edge-LBD-LCS-ServiceLBDEnv1.png "Piemēro atjauninājumus LCS")

    ![Pielāgošanas pakotnes atlasīšana.](media/cloud_edge-LBD-LCS-ServiceLBDEnv2.png "Pielāgošanas pakotnes atlasīšana")

## <a name="assign-your-lbd-edge-scale-unit-to-a-hub"></a><a name="assign-edge-to-hub"></a> LBD malas skalas vienības piešķiršana pārkraušanas centram

Jūs konfigurējat un pārvaldāt savu malu skalas vienību, izmantojot Mēroga vienību pārvaldības portālu. Papildinformāciju skatiet mēroga [vienību un darba noslodzi pārvaldība, izmantojot mēroga vienību pārvaldnieka](./cloud-edge-landing-page.md#scale-unit-manager-portal) portālu.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
