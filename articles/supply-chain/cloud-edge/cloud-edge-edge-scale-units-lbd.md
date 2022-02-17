---
title: Malas mēroga vienību izvietošana pielāgotajā aparatūrā, izmantojot LBD
description: Šajā tēmā skaidrots, kā nodrošināt lokālās malas skalas vienības, izmantojot pielāgotu aparatūru un izvietošanu, kas ir balstīta uz vietējiem uzņēmuma datiem (LBD).
author: cabeln
ms.date: 01/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 1204b65e76c107c29a94a61c321064a87c7571fb
ms.sourcegitcommit: 948978183a1da949e35585b28b8e85a63b6c12b1
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/25/2022
ms.locfileid: "8024546"
---
# <a name="deploy-edge-scale-units-on-custom-hardware-using-lbd"></a>Malas mēroga vienību izvietošana pielāgotajā aparatūrā, izmantojot LBD

[!include [banner](../includes/banner.md)]

Malas apjoma vienībām ir svarīga loma sadalītajā topoloģijā piegādes ķēžu pārvaldībai. Tālākajā topoloģijā varat sadalīt darba slodzi starp Supply Chain Management mākoņa pārkraušanas vietu un papildu mēroga vienībām mākonī vai malā.

Malu skalas vienības var izvietot, izveidojot vietējos biznesa datus (LBD) [lokālajā vidē](../../fin-ops-core/dev-itpro/deployment/on-premises-deployment-landing-page.md) un pēc tam konfigurējot to, lai darbotos kā mēroga vienība jūsu sadalītajā topoloģijā piegādes ķēdes pārvaldībai. To var sasniegt, saistot lokālo LBD vidi ar Supply Chain Management vidi mākonī, kas konfigurēta tā, lai darbotos kā pārkraušanas mezgls.  

Šajā tēmā ir aprakstīts, kā iestatīt lokālas LBD vidi kā malas skalas vienību un pēc tam saistīt to ar pārkraušanas punktu.

## <a name="infrastructure-considerations"></a>Infrastruktūras apsvērumi

Malu mēroga vienības darbojas lokālas vidēs, tāpēc infrastruktūras prasības ir diezgan līdzīgas. Tomēr ir dažas atšķirības, kas jāatzīmē:

- Edge mēroga vienības neizmanto Finanšu pārskatus, tāpēc tām nav nepieciešami Finanšu pārskatu mezgli.
- Ražošanas un noliktavu noslodze nav skaitļošanas intensīva, tāpēc apsveriet iespēju attiecīgi pielāgot skaitļošanas jaudu AOS mezgliem.

## <a name="deployment-overview"></a>Izvietošanas pārskats

Tālāk ir sniegts pārskats par izvietošanas darbībām.

1. **Iespējojiet LBD slotu savā LBD projektā Microsoft Dynamics Lifecycle Services (LCS).**

1. **Iestatiet un izvietojiet LBD vidi ar *tukšu* datu bāzi.**

    Izmantojiet LCS, lai izvietotu LBD vidi ar jaunāko topoloģiju un tukšu datu bāzi. Papildinformāciju skatiet tālāk šīs tēmas sadaļā sadaļā Iestatījumi un [izvietojiet LBD vidi ar tukšu datu bāzes sadaļu](#set-up-deploy). Piegādes ķēdes pārvaldības versija 10.0.21 vai jaunāka ir jāizmanto centrmezgla un mēroga vienību vidēs.

1. **Augšupielādēt mērķa pakotnes LBD projekta aktīvos LCS.**

    Sagatavojiet programmu, platformu un pielāgošanas pakotnes, ko izmantojat pārkraušanas centrā un malu skalas vienībā. Papildinformāciju skatiet tālāk šīs tēmas sadaļā [Augšupielādes mērķa iepakojumos LBD projekta līdzekļa sadaļā LCS](#upload-packages).

1. **Pakalpojumu LBD vidē ar mērķa pakotnēm.**

    Šis solis nodrošina, ka viens un tas pats būvējums un pielāgojumi tiek izvietoti pārkraušanas mezglā un centrā. Papildinformāciju skatiet tālāk šīs tēmas sadaļā [Pakalpojums LBD vide ar mērķa pakotnēm](#service-target-packages).

1. **Pabeidziet mēroga vienības konfigurāciju un darba noslodzes piešķiri.**

    Papildinformāciju skatiet tālāk šīs tēmas sadaļā [Piešķirt savu LBD malas skalas vienību pārkraušanas mezglu](#assign-edge-to-hub).

Atlikušajās šīs tēmas sadaļās ir sniegta plašāka informāciju par katru šī procesa posmu.

## <a name="set-up-and-deploy-an-lbd-environment-with-an-empty-database"></a><a name="set-up-deploy"></a>Iestatiet un izvietojiet LBD vidi ar tukšu datu bāzi

Šis solis izveido funkcionālu LBD vidi. Tomēr videi nav nepieciešama tāda pati lietojumprogrammas un platformas versija kā pārkraušanas mezgla videi. Turklāt tam joprojām trūkst pielāgojumu, un tie vēl nav iespējoti darbam kā mēroga vienība.

1. Sekojiet instrukcijām [Iestatījumi un lokālo vižu izvietošana (Platformas atjauninājums 41 vai jaunāks)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md). Piegādes ķēdes pārvaldības versija 10.0.21 vai jaunāka ir jāizmanto centrmezgla un mēroga vienību vidēs. Turklāt jāizmanto infrastruktūras skriptu versija 2.12.0 vai jaunāka versija. 

    > [!IMPORTANT]
    > **Pirms** izpildāt šajā tēmā aprakstītās darbības, izlasiet pārējās šīs sadaļas darbības.

1. Pirms aprakstīt konfigurāciju infrastruktūras \\ConfigTemplate.xml failā, palaidiet šādu skriptu:

    ```powershell
    .\Configure-ScriptsForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > Šajā skriptā tiks noņemta konfigurācija, kas nav nepieciešama malu skalas vienību izvietošanai.

1. Iestatiet datu bāzi, kas satur tukšus datus, kā aprakstīts sadaļā [Datu bāzu konfigurēšana](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb). Izmantojiet šo darbību tukšā datus.bak failā.
1. Kad esat pabeidzis datu bāzu [konfigurēšanas](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) darbību, palaidiet šo skriptu, lai konfigurētu skalas vienības Alm Orchestrator datu bāzi.

    > [!NOTE]
    > Nekonfigurējiet finanšu pārskatu datu bāzi datu bāzu [konfigurēšanas](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) soļa laikā.

    ```powershell
    .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName EdgeScaleUnit
    ```

    Skripts Initialize-Database.ps1 veic šādas darbības:

    1. Izveidojiet tukšu datu bāzi ar nosaukumu **ScaleUnitAlmDb**.
    2. Kartējiet lietotājus uz datu bāzes lomām, pamatojoties uz šo tabulu.

        | Lietotājs            | Veids | Datu bāzes loma |
        |-----------------|------|---------------|
        | svc-LocalAgent$ | gMSA | dbowner\_     |

1. Turpiniet ievērot uzstādīšanas un lokālās vides izvietošanas norādījumus [(41. un jaunāka versija)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md).
1. Kad esat pabeidzis AD FS [konfigurēšanas](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) darbību, rīkojieties šādi:

    1. Izveidojiet jaunu Active Directory federācijas pakalpojumu (AD FS) lietojumprogrammu, kas ļaus Alm orķestrācijas pakalpojumam sazināties ar jūsu application object server (AOS).

        ```powershell
        # Host URL is your DNS record\host name for accessing the AOS
        .\Create-ADFSServerApplicationForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -HostUrl 'https://ax.d365ffo.onprem.contoso.com'
        ```

    1. Izveidojiet jaunu Azure Active Directory (Azure AD) lietojumprogrammu, kas ļaus Alm orķestrācijas pakalpojumam sazināties ar mēroga vienību pārvaldības pakalpojumu.

        ```powershell
        # Example .\Create-SumAADApplication.ps1 -ConfigurationFilePath ..\ConfigTemplate.xml -TenantId '6240a19e-86f1-41af-91ab-dbe29dbcfb95' -ApplicationDisplayName 'EdgeAgent-SUMCommunication-EN01'
        .\Create-SumAADApplication.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                       -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                       -ApplicationDisplayName '<Whichever name you want the Azure AD app to have>'
        ```

1. Turpiniet ievērot uzstādīšanas un lokālās vides izvietošanas norādījumus [(41. un jaunāka versija)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md). Ievadot vietējā aģenta konfigurāciju, pārliecinieties, vai iespējojat edge mēroga vienības funkcijas un norādiet visus nepieciešamos parametrus.

    ![Edge Scale vienības līdzekļu iespējošana.](media/EnableEdgeScaleUnitFeatures.png "Edge Scale vienības līdzekļu iespējošana.")

1. Pirms vides izvietošanas no LCS iestatiet pirms izvietošanas skriptu. Papildinformācija: [Vietējā aģenta pirmsizvietošanas un pēcizvietošanas skripti](../../fin-ops-core/dev-itpro/lifecycle-services/pre-post-scripts.md).

    1. Kopējiet skriptu Configure-CloudAndEdge.ps1 no **infrastruktūras skriptu** mapes **ScaleUnit** uz **vidē iestatītās aģenta failu krātuves koplietojuma mapi Skripti**. Tipisks ceļš ir \\\\lbdiscsi01\\aģents\\Skripti.
    2. Izveidojiet skriptu **PreDeployment.ps1**, kas izsauks skriptus, izmantojot nepieciešamos parametrus. Pirmsizvēršanas skripts ir jāizvieto **Skriptu** mapē aģenta faila glabāšanas koplietojumā. Pretējā gadījumā to nevar palaist. Tipisks ceļš ir \\\\lbdiscsi01\\aģents\\Skripti\\PreDeployment.ps1.

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
1. Pēc vides izvietošanas veiciet tālāk norādītās darbības.

    1. Biznesa datu bāzē (AXDB) palaidiet šādas SQL komandas.

        ```sql
        ALTER TABLE dbo.NUMBERSEQUENCETABLE ENABLE CHANGE_TRACKING WITH (TRACK_COLUMNS_UPDATED = ON)
        delete from NumberSequenceTable
        delete from NumberSequenceReference
        delete from NumberSequenceScope
        delete from FeatureManagementMetadata
        delete from FeatureManagementState
        delete from SysFeatureStateV0
        ```

    1. Palieliniet vienlaicīgu maksimālo pakešsēni līdz vērtībai, kas ir lielāka par 4.

        ```sql
        Update batchserverconfig set maxbatchsessions = '<Replace with number of concurrent batch tasks you want>'
        ```

    1. Pārbaudiet, vai jūsu uzņēmuma datu bāzē (AXDB) ir iespējota izmaiņu reģistrēšana.

        1. Atveriet SQL Server Management Studio (SSMS).
        1. Atlasiet un turiet nospiestu (vai noklikšķiniet ar peles labo pogu) savu biznesa datu bāzi (AXDB) un pēc tam atlasiet **Rekvizīti**.
        1. Logā, kas tiek parādīts, atlasiet **Mainīt izsekošanu** un pēc tam iestatiet šādas vērtības:

            - **Izmaiņu izsekošana:** *Patiess*
            - **Saglabāšanas periods:** *7*
            - **Ieturējumu vienības:** *Dienas*
            - **Automātiskā tīrīšana:** *Patiess*

    1. Pievienojiet iepriekš izveidoto AD FS lietojumprogrammas ID (izmantojot skriptu Create-ADFSServerApplicationForEdgeScaleUnits.ps1) Azure AD lietojumprogrammu tabulai savā skalas vienībā. Šo darbību var veikt manuāli, izmantojot lietotāja interfeisu (UI). Varat arī to pabeigt, izmantojot datu bāzi, izmantojot šādu skriptu.

        ```sql
        DECLARE @ALMOrchestratorId NVARCHAR(76) = '<Replace with the ADFS Application ID created in a previous step>';

        IF NOT EXISTS (SELECT TOP 1 1 FROM SysAADClientTable WHERE AADClientId = @ALMOrchestratorId)
        BEGIN
            INSERT INTO SysAADClientTable (AADClientId, UserId, Name, ModifiedBy, CreatedBy)
            VALUES (@ALMOrchestratorId, 'ScaleUnitManagement', 'Scale Unit Management', 'Admin', 'Admin');
        END
        ```

## <a name="set-up-an-azure-key-vault-and-an-azure-ad-application-to-enable-communication-between-scale-units"></a><a name="set-up-keyvault"></a> Azure atslēgas velves un lietojumprogrammas Azure AD iestatīšana, lai iespējotu saziņu starp mēroga vienībām

1. Kad vide ir izvietota, izveidojiet papildu Azure AD lietojumprogrammu, lai iespējotu uzticamu saziņu starp centrmezglu un mēroga vienību.

    ```powershell
    .\Create-SpokeToHubAADApplication.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                          -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                          -ApplicationDisplayName '<Whichever name you want the Azure AD app to have>'
    ```

1. Pēc lietojumprogrammas izveides ir jāizveido klienta noslēpums un jāsaglabā informācija Azure atslēgu glabātuvē. Turklāt jums ir jāpiešķir piekļuve izveidotajai Azure AD lietojumprogrammai, lai tā varētu izgūt atslēgas seifā glabātos noslēpumus. Jūsu ērtībai nākamais skripts automātiski veiks visas nepieciešamās darbības.

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
    > Ja nav nevienas atslēgas velves, kurai ir norādītā **KeyVaultName** vērtība, skripts to automātiski izveido.

1. Azure AD Pievienojiet tikko izveidoto lietojumprogrammas ID (izmantojot skriptu Create-SpokeToHubAADApplication.ps1) Azure AD centrmezgla lietojumprogrammu tabulai. Šo darbību var manuāli pabeigt, izmantojot lietotāja interfeisu.

## <a name="upload-target-packages-into-lbd-project-assets-in-lcs"></a><a name="upload-packages"></a>Augšupielādēt mērķa pakotnes LBD projekta aktīvos LCS

Šis solis sagatavo programmas versiju, platformas versiju un pielāgojumus, kas tiks pārieti uz LBD mēroga vienības vidi.

1. Augšupielādējiet to pašu kombinēto lietojumprogrammas/platformas pakotni, kas tika lietota pārkraušanas centra vidē, LCS lokālo projektu līdzekļu bibliotēkā.
1. Augšupielādējiet to pašu kombinēto lietojumprogrammas/platformas pakotni, kas tika lietota pārkraušanas centra vidē, LCS lokālo projektu līdzekļu bibliotēkā.

## <a name="service-the-lbd-environment-with-target-packages"></a><a name="service-target-packages"></a>Pakalpojumi LBD vidē ar mērķa pakotnēm

Šis solis sagatavo programmas versiju, platformas versiju un pielāgojumus, kas tiks pārieti uz LBD mēroga vienības vidi.

1. Pakalpojumu LBD vidē ar kombinēto lietojumprogrammu/platformu pakotni, ko augšupielādējat iepriekšējā darbībā.
1. Pakalpojumu LBD vidē ar kombinēto lietojumprogrammu/platformu pakotni, ko augšupielādējat iepriekšējā darbībā.

    ![Atjauninājumu lietošana LKS.](media/cloud_edge-LBD-LCS-ServiceLBDEnv1.png "Atjauninājumu lietošana LCS")

    ![Pielāgošanas pakotnes atlasīšana.](media/cloud_edge-LBD-LCS-ServiceLBDEnv2.png "Pielāgošanas pakotnes atlasīšana")

## <a name="assign-your-lbd-edge-scale-unit-to-a-hub"></a><a name="assign-edge-to-hub"></a>LBD malas skalas vienības piešķiršana pārkraušanas centram

Jūs konfigurējat un pārvaldāt savu malu skalas vienību, izmantojot mēroga vienību pārvaldības portālu. Papildinformāciju skatiet [skalu vienību un darba slodžu pārvaldība, izmantojot mēroga vienību pārvaldnieka portālu](./cloud-edge-landing-page.md#scale-unit-manager-portal).

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
