---
title: Finance Insights konfigurācija publiskam priekšskatījumam (priekšskatījums) – versija 10.0.20 un jaunākas
description: Šajā tēmā ir izskaidrots, kā konfigurēt sistēmu, lai izmantotu iespējas, kas pieejamas Finance Insights publiskam priekšskatījumam versijā 10.0.20 un jaunākās.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-06-03
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 613bd4816e2f0c4fbb56cf79779a08c6a09592bd
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222616"
---
# <a name="configuration-for-finance-insights-for-public-preview-preview---version-10020-and-later"></a>Finance Insights konfigurācija publiskam priekšskatījumam (priekšskatījums) – versija 10.0.20 un jaunākas

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Finance Insights apvieno Microsoft Dynamics 365 Finance funkcionalitāti ar Dataverse, Azure un AI Builder, lai nodrošinātu jaudīgus prognozēšanas rīkus jūsu organizācijai. Šajā tēmā ir izskaidrots, kā konfigurēt Dynamics 365 Finance versiju 10.0.20, lai sistēma varētu izmantotu iespējas, kas ir pieejamas Finance Insights publiskam priekšskatījumam.

> [!NOTE]
> Šajā tēmā aprakstītās konfigurācijas darbības attiecas tikai uz Finance versiju 10.0.20 un jaunāku. 'Lai iestatītu Finance Insights versijai 10.0.19 vai jaunākai, skatiet [Finance Insights konfigurācija – versijām līdz 10.0.18](configure-for-fin-insites.md).

## <a name="deploy-finance"></a>Finance izvietošana

Lai izvietotu vides, veiciet tālāk norādītās darbības.

1. Programmā Microsoft Dynamics Lifecycle Services (LCS) izveidojiet vai atjauniniet Finance vidi. Videi nepieciešama Finance and Operations programmas versija 10.0.20 vai jaunāka.
2. Videi ir jābūt augstas pieejamības (AP) videi smilškastē. (Šis vides veids ir pazīstams arī kā 2. līmeņa vide.) Lai iegūtu papildu informāciju, skatiet [Vides plānošana](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
3. Konfigurējot Finance Insights, izmantojot smilškastes vidi, jums vajadzēs kopēt ražošanas datus uz šo vidi, lai varētu prognozēt darbu. Prognozēšanas modelī tiek izmantoti vairāki datu gadi, lai izveidotu prognozes. Contoso demonstrācijas dati neietver pietiekami daudz vēsturiskos datu, lai apmācītu prognozēšanas modeli. 

## <a name="configure-dataverse"></a>Dataverse konfigurēšana

Sekojiet tālāk norādītajām darbībām, lai konfigurētu Dataverse programmai Finance Insights.

1. Atveriet vides lapu LCS un pārbaudīt, vai sadaļa **Power Platform integrācija** jau ir instalēta.

    - Ja tā jau ir iestatīta, jāuzskaita ar Finance vidi saistītais Dataverse vides nosaukums.
    - Ja tā nav iestatīta, rīkojieties šādi:

        1. Sadaļā **Power Platform integrācija** atlasiet **Iestatīšana**. Vides iestatīšana var ilgt vienu stundu.
        2. Ja Dataverse vide ir veiksmīgi iestatīta, ir jāuzskaita Dataverse vides nosaukums, kas ir saistīts ar Finance vidi.

        > [!NOTE]
        > Pēc vides iestatīšanas **neatlasiet** pogu **Saite uz CDS programmām**. Šī poga nav paredzēta Finance Insights. Ja to atlasīsit, nevarēsit konfigurēt nepieciešamās vides pievienojumprogrammas LCS.

## <a name="configure-azure"></a>Azure konfigurēšana

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a>Izmantojiet Azure Cloud Shell, lai iestatītu Data Lake resursus programmā Finance Insights

# <a name="use-a-windows-powershell-script"></a>[Windows PowerShell skripta izmantošana](#tab/use-a-powershell-script)

Windows PowerShell skripts tiek nodrošināts, lai varētu viegli iestatīt Azure resursus, kas aprakstīti sadaļā [Eksporta konfigurēšana uz Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md). Ja vēlaties iestatīšanu veikt manuāli, izlaidiet šo procedūru un pabeidziet procedūru sadaļā [Manuālā iestatīšana](#manual-setup).

> [!NOTE]
> Izmantojiet šo procedūru, lai palaistu Windows PowerShell skriptu. Iespējams, iestatījums nedarbosies, ja izmantojat opciju **Izmēģināt** to Azure CLI vai palaižat skriptu datorā.

Izpildiet tālāk norādītās darbības, lai konfigurējot Azure tiktu izmantots Windows PowerShell skripts. Jums ir jābūt tiesībām izveidot Azure resursu grupu, Azure resursus un Azure AD pieteikumu. Lai iegūtu informāciju par nepieciešamajām atļaujām, skatiet [Pakalpojuma Azure AD atļauju pārbaude](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).

1. [Azure portālā](https://portal.azure.com) dodieties uz savu mērķa Azure abonementu.
2. Atlasiet **Cloud Shell**, kas atrodas pa labi no lauka **Meklēt**.
3. Atlasiet **PowerShell**.
4. Izveidojiet krātuvi, ja saņemat aicinājumu to darīt.
5. Cilnē **Azure CLI** atlasiet **Kopēt**.
6. Programmā Notepad atveriet jaunu failu un ielīmējiet Windows PowerShell skriptu.
7. Saglabājiet failu kā **ConfigureDataEzer.ps1**.
8. Augšupielādējiet Windows PowerShell skriptu sesijā, izmantojot izvēlnes opciju augšupielādei Cloud Shell.
9. Palaidiet **.\ConfigureDataLake.ps1** skriptu.
10. Sekojiet uzvednēm, lai palaistu skriptu.
11. Izmantojiet skripta izvades informāciju, lai LCS instalētu pievienojumprogrammu Eksportēt uz Data Lake.

### <a name="manual-setup"></a>Manuāla iestatīšana

#### <a name="add-applications-to-the-azure-ad-tenant"></a>Pieteikumu pievienošana Azure AD nomniekam

1. [Azure portālā](https://portal.azure.com) dodieties uz **Azure Active Directory**.
2. Atlasiet **Pārvaldīt \> Uzņēmuma pieteikumi**.
3. Uzmeklējiet tālāk norādītos pieteikumus, izmantojot pieteikuma ID.

    | Pieteikums                              | Programmas ID                               |
    |------------------------------------------|--------------------------------------|
    | Microsoft Dynamics ERP apakšpakalpojumi     | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |
    | Microsoft Dynamics ERP apakšpakalpojumi CDS | 703e2651-d3fc-48f5-942c-74274233dba8 |
    | AI Builder autorizācijas pakalpojums         | ad40333e-9910-4b61-b281-e3aeeb8c3ef3 |

Ja nevarat atrast nevienu no iepriekšējiem pieteikumiem, izmēģiniet tālāk norādītās darbības.

1. Sava lokālā datora izvēlnē **Sākt** uzmeklējiet **powershell**.
2. Atlasiet un turiet nospiestu (vai noklikšķiniet ar peles labo pogu) **Windows PowerShell** un pēc tam atlasiet **Palaist kā administratoram**.
3. Palaidiet tālāk norādīto komandu, lai instalētu **AzureAD** moduli.

    `Install-Module -Name AzureAD`

4. Ja ir nepieciešams NuGet nodrošinātājs, lai turpinātu, atlasiet **Y**, lai to instalētu.
5. Ja tiek parādīts ziņojums “Neuzticams repozitorijs”, atlasiet **Y**, lai turpinātu.
6. Katram pieteikumam, kas jāpievieno, palaidiet tālāk norādītās komandas, lai pievienotu pieteikumu Azure AD. Kad saņemat aicinājumu, pierakstieties kā Azure AD administrators.

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a>Azure resursu izveidošana

> [!NOTE]
> Pārliecinieties, ka izveidojat tālāk norādītos resursus tajā pašā Azure AD instancē, kurā ir Dataverse vide. Nav iespējams izmantot resursus no citas Azure AD instances.

1. Izveidojiet krātuves kontu:

    1. [Azure portālā](https://portal.azure.com) izveidojiet krātuves kontu.
    2. Dialoglodziņā **Izveidot krātuves kontu** iestatiet tālāk norādītos laukus.

        - **Atrašanās vieta** — atlasiet datu centru, kur atrodas jūsu vide.
        - **Veiktspēja** — ieteicams atlasīt **Standarta**.
        - **Konta veids** — jāatlasa **StorageV2**.

    3. Dialoglodziņā **Papildu opcijas** opcijā **Data Lake Storage Gen2** atlasiet **Iespējot** līdzeklī **Hierarhiskās nosaukumvietas**. Ja šis līdzeklis netiks iespējots, nevarēsit patērēt datus, ko Finance and Operations programmas raksta, izmantojot tādus pakalpojumus kā Power BI datu plūsmas.
    4. Atlasiet **Pārskatīt un izveidot**. Kad izvietošana ir pabeigta, jaunais resurss tiks parādīts Azure portālā.
    5. Dodieties uz izveidoto krātuves kontu.
    6. Kreisās puses izvēlnē atlasiet **Piekļuves galvenie akreditācijas dati**.
    7. Kopējiet un saglabājiet krātuves konta nosaukumu. Šī vērtība būs jānorāda vēlāk, kad iestatīsit galvenos akreditācijas datu glabātavas noslēpumus.

2. Izveidojiet galveno akreditācijas datu glabātavu:

    1. [Azure portālā](https://portal.azure.com) izveidojiet galveno akreditācijas datu glabātavu.
    2. Dialoglodziņā **Izveidot galveno akreditācijas datu glabātavu** laukā **Novietojums** atlasiet datu centru, kur atrodas jūsu vide.
    3. Pēc galvenās akreditācijas datu glabātavas izveidess dodieties uz **Galvenās akreditācijas datu glabātavas pārskatu** un kopējiet un saglabājiet DNS nosaukumu. Šī vērtība būs jānorāda vēlāk, kad iestatīsit Data Lake pievienojumprogrammu.

3. Izveidojiet un reģistrējiet Azure AD pieteikumu.

    1. [Azure portālā](https://portal.azure.com) dodieties uz **Azure Active Directory** un atlasiet **Pieteikumu reģistrācija**.
    2. Atlasiet **Jauna pieteikuma reģistrācija** un iestatiet tālāk norādītos laukus.

        - **Nosaukums** — ievadiet pieteikuma nosaukumu.
        - **Pieteikuma veids** — atlasiet **Web API**.
        - **Novirzīt URI iestatīšanu** — ievadiet savas Dynamics 365 instances URL, piemēram, `https://yourdynamicsinstance.dynamics.com/auth`.

    3. Dodieties uz tikko izveidoto pieteikumu, kopējiet un saglabājiet tās **Pieteikuma (klienta) ID** vērtību. Šī vērtība būs jānorāda vēlāk, kad iestatīsit galvenos akreditācijas datu glabātavas noslēpumus.
    4. Dodieties uz **API atļaujas** un veiciet tālāk norādītās darbības.

        1. Atlasiet **Pievienot atļauju**.
        2. Atlasiet **Azure Galvenā akreditācijas datu glabātava**.
        3. Pēc deleģēto atļauju atlases atlasiet **lietotājs\_personifikācija**.
        4. Atlasiet **Pievienot atļaujas**.

    5. Pieteikuma izvēlnē atlasiet **Sertifikāti \& noslēpumi** un pēc tam izpildiet tālāk norādītās darbības, lai izveidotu galvenās akreditācijas datu glabātavas noslēpumus.

        1. Atlasiet **Jauns klienta noslēpums**.
        2. Ievadiet nosaukumu laukā **Akreditācijas datu glabātavas apraksts**.
        3. Atlasiet ilgumu un pēc tam atlasiet **Pievienot**. Noslēpums tiek ģenerēts laukā **Vērtība**.
        4. Kopējiet un saglabājiet klienta slepeno vērtību. Šī vērtība būs jānorāda vēlāk, kad iestatīsit galvenos akreditācijas datu glabātavas noslēpumus.

4. Izveidojiet Galvenās akreditācijas datu glabātavas noslēpumus.

    1. Dodieties uz galveno akreditācijas datu glabātavu, ko izveidojāt iepriekš, un atlasiet **Noslēpumi**.
    2. Katram noslēpuma nosaukumam tālāk esošajā tabulā veiciet tālāk norādītās darbības.

        1. Atlasiet **Ģenerēt/Importēt**.
        2. Dialoglodziņā **Izveidot noslēpumu** laukā **Augšupielādes opcijas** atlasiet **Manuāli**.
        3. Izveidojiet noslēpuma nosaukumu un vērtību no tabulas.
        4. Atlasiet **Iespējots** un pēc tam atlasiet **Izveidot**. Noslēpums ir izveidots un pievienots Galveno akreditācijas datu glabātai.

        | Slepenais nosaukums                       | Noslēpuma vērtība                                                                                 |
        |-----------------------------------|----------------------------------------------------------------------------------------------|
        | app-id                            | Iepriekš izveidotā pieteikuma ID.                                      |
        | app-secret                        | Iepriekš saglabātais klienta noslēpums.                                                    |
        | storage-account-name              | Iepriekš izveidotā krātuves konta nosaukums, piemēram, **storageaccount1**.       |

5. Autorizējiet pieteikumu, lai piekļūtu galveno akreditācijas datu glabātavai.

    1. [Azure portālā](https://portal.azure.com) atveriet iepriekš izveidoto galveno akreditācijas datu glabātavu.
    2. Atlasiet piekļuves politikas.
    3. Katram pieteikumam tālāk esošajā tabulā veiciet tālāk norādītās darbības.

        1. Atlasiet **Pievienot piekļuves politiku**, lai izveidotu piekļuves politiku.
        2. Laukā **Noslēpuma atļaujas** atlasiet atļaujas no tabulas.
        3. Laukā **Noslēpuma vadītājs** uzmeklējiet pieteikuma parādāmo nosaukumu no tabulas.
        4. Atlasiet **Atlasīt**.
        5. Atlasiet **Pievienot**.
        6. Atlasiet **Saglabāt**.

        | Pieteikums                                              | Tiesības |
        |----------------------------------------------------------|-------------|
        | Parādāmais nosaukums jaunajā izveidotajā pieteikumā | Iegūt, saraksts   |
        | **Microsoft Dynamics ERP apakšpakalpojumi**                 | Iegūt, saraksts   |

6. Piešķiriet lomas, lai piekļūtu krātuves kontam.

    1. [Azure portālā](https://portal.azure.com) atveriet iepriekš izveidoto krātuves kontu.
    2. Atlasiet **Piekļuves kontrole (IAM)** un pēc tam atlasiet **Lomu piešķires**.
    3. Atlasiet **Pievienot, pievienot lomas piešķiri**.
    4. Katram pieteikumam tālāk esošajā tabulā veiciet tālāk norādītās darbības.

        1. Atlasiet lomu no tabulas.
        2. Atstājiet lauku **Piešķirt piekļuvi** iestatītu uz **Azure AD lietotājs, grupa vai pakalpojuma vadītājs**.
        3. Laukā **Atlasīt** ievadiet pieteikumu no tabulas.
        4. Atlasiet **Saglabāt**.

        | Pieteikums                                              | Loma                        |
        |----------------------------------------------------------|-----------------------------|
        | Parādāmais nosaukums jaunajā izveidotajā pieteikumā | Īpašnieks                       |
        | Parādāmais nosaukums jaunajā izveidotajā pieteikumā | Līdzstrādnieks                 |
        | Parādāmais nosaukums jaunajā izveidotajā pieteikumā | Krātuves konta līdzstrādnieks |
        | Parādāmais nosaukums jaunajā izveidotajā pieteikumā | Krātuves BLOB datu īpašnieks     |
        | **AI Builder autorizācijas pakalpojums**                     | Krātuves BLOB datu lasītājs    |

# <a name="azure-cli"></a>[Azure CLI](#tab/azure-azure-cli)

```
function New-FinanceDataLakeAzureResources {
    Assert-ScriptSetup

    $ClientAppName = 'Finance Data Lake Application'
    $DefaultSecretExpiryInYear = 1
    $MicrosoftDynamicsERPMicroservicesAppId = '0cdb527f-a8d1-4bf8-9436-b352c68682b2'
    $MicrosoftDynamicsERPMicroservicesCDSAppId = '703e2651-d3fc-48f5-942c-74274233dba8'
    $AIBuilderAuthorizationServiceAppId = 'ad40333e-9910-4b61-b281-e3aeeb8c3ef3'
    $KeyVaultServicePrincipalAppId = 'cfa8b339-82a2-471a-a3c9-0fc0be7a4093'
    $GraphServicePrincipalAppId = '00000003-0000-0000-c000-000000000000'

    Import-Module AzureAD.Standard.Preview
    $connectAzureADParameters = @{ 'Identity' = $true; 'TenantId' = $env:ACC_TID }
    $azContext = AzureAD.Standard.Preview\Connect-AzureAD @connectAzureADParameters
    $userContext = ConvertFrom-Json ((az ad signed-in-user show) -join '')
    $user = Get-AzureADUser -Filter ("UserPrincipalName eq '" + $userContext.UserPrincipalName + "'")

    Set-AzureSubscription
    
    $resourceGroup = $null
    $ResourceGroupName = 'D365FinanceInsightsDataLake'
    $ResourceGroupNameSuffix = ''
    $FullResourceGroupName = ''
    Write-Output ("The default Azure Resource Group name is '{0}'" -f $ResourceGroupName)
    while (-not ($resourceGroup)) {
        $ResourceGroupNameSuffix = (Read-Host -Prompt "Enter optional Azure Resource Group name suffix: (leave blank for no suffix)")
        if ([string]::IsNullOrWhitespace($ResourceGroupNameSuffix))
        {
            $FullResourceGroupName = $ResourceGroupName
        }
        else
        {
            if ($ResourceGroupNameSuffix -notmatch "^[A-Za-z0-9]+$") {
                Write-Warning "The Azure Resource Group name suffix can only include alphanumeric characters."
                continue
            }

            if ($ResourceGroupNameSuffix.Length -gt 60) {
                Write-Warning "The Azure Resource Group name suffix cannot be longer than 60 characters."
                continue
            }

            $FullResourceGroupName = $ResourceGroupName + $ResourceGroupNameSuffix
        }
        
        $resourceGroup = Get-AzResourceGroup -Name $FullResourceGroupName -ErrorAction SilentlyContinue

        if (-not ($resourceGroup)) {
            Write-Output ("Your new Azure Resource Group name is '{0}'" -f $FullResourceGroupName)
            $resourceLocation = ''
            $azResourceLocations = (Get-AzLocation | Select-Object Location).Location
            while ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations))) {
                $resourceLocation = (Read-Host -Prompt "Enter the location in which to create the Azure Resource Group: ('help' to see values)")
                if ($resourceLocation -eq 'help') {
                    Write-Output ("List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
                elseif ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations)))
                {
                    Write-Warning ("The provided location is not available for resource group. List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
            }
            $resourceGroup = New-AzResourceGroup -Name $FullResourceGroupName -Location $resourceLocation
            Write-Output ("Created Azure Resource Group '{0}'" -f $resourceGroup.ResourceGroupName)
        }
        else {
            Write-Output ("Found Azure Resource Group '{0}'" -f ($resourceGroup.ResourceGroupName))
        }
    }

    Write-Output '================================================================================='
    $MicrosoftDynamicsERPMicroservicesAppObjectId = Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesAppId
    Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesCDSAppId | Out-Null
    $aibuilderAuthorizationServiceObjectId = Create-ADServicePrincipal -AppId $AIBuilderAuthorizationServiceAppId
    Write-Output ('=================================================================================')

    $clientAppSPN = Get-AzureADServicePrincipal -Filter ("DisplayName eq '" + $ClientAppName + "'")
    if (-not ($clientAppSPN)) {
        $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        if (-not $keyVaultPrincipal)
        {
            New-AzureADServicePrincipal -AppId $KeyVaultServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Key Vault principal to AAD"
            $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        }
        $keyVaultAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $keyVaultAccess.ResourceAppId = $keyVaultPrincipal.AppId
        $keyVaultAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $keyVaultPrincipal.Oauth2Permissions.Id, "Scope")

        $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        if (-not $graphPrincipal)
        {
            New-AzureADServicePrincipal -AppId $GraphServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Graph principal to AAD"
            $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        }
        $userRead = $graphPrincipal.Oauth2Permissions | Where-Object { $_.Type -eq "User" -and $_.Value -eq "User.Read" }
        $graphAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $graphAccess.ResourceAppId = $graphPrincipal.AppId
        $graphAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $userRead.Id, "Scope")

        $clientApp = New-AzureADApplication -DisplayName $ClientAppName -RequiredResourceAccess @($keyVaultAccess, $graphAccess)
        $clientAppSPN = New-AzureADServicePrincipal -AppId $clientApp.AppId -Tags @($ClientAppName)
        $clientAppId = $clientApp.AppId
        Write-Output ('Created App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
    else {
        $clientApp = Get-AzureADApplication -Filter ("DisplayName eq '" + $ClientAppName + "'")
        $clientAppId = $clientApp.AppId
        Write-Output ('Found App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
            
    $clientAppSecretCredential = New-AzureADApplicationPasswordCredential -ObjectId $clientApp.ObjectId -CustomKeyIdentifier "ClientAppAccessKey" -EndDate (get-date).AddYears($DefaultSecretExpiryInYear)
    $ClientAppSecret = $clientAppSecretCredential.Value
    $clientAppSpId = $clientAppSPN.ObjectId

    Write-Output ('Generated application secret: ' + $ClientAppSecret)
    Write-Output '================================================================================='

    $templateObject = ConvertFrom-Json $azureTemplate -AsHashtable
    $templateObject.{$schema} = "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#"
    Write-Output 'Provisioning Azure resources. This may take a few minutes.'
    try {
        $deployment = New-AzResourceGroupDeployment -ResourceGroupName $FullResourceGroupName -TemplateObject $templateObject -aibuilderAppObjectId $aibuilderAuthorizationServiceObjectId -clientAppId $clientAppId -clientAppSecret $ClientAppSecret -clientAppSpObjectId  $clientAppSpId -microserviceSpObjectId $MicrosoftDynamicsERPMicroservicesAppObjectId -userSpObjectId $user.ObjectId -Force -ErrorAction Stop
    }
    catch {
        $ErrorMessage = $_.Exception.Message
        if ($ErrorMessage.Contains("not allowed to be updated"))
        {
            Write-Error ($ErrorMessage)
            Write-Warning "Some items in the existing resource group $FullResourceGroupName could not be updated. To resolve the issue, remove the existing resource group $FullResourceGroupName and run the script again."
        }
        else {
            throw
        }

    }
    if ($deployment.ProvisioningState -eq 'Succeeded') {
        Write-Output "Successfully deployed the following resources to Azure:"
        Write-Output ("  Key Vault:                         " + $deployment.Outputs.keyVaultName.Value)
        Write-Output ("  Storage Account:                   " + $deployment.Outputs.storageAccountName.Value)
        
        $keyVault = Get-AzKeyVault -VaultName $deployment.Outputs.keyVaultName.Value
        $tenantId = (Get-AzContext).Tenant.Id

        Write-Output "Values for LCS Data Lake Add-In:"
        Write-Output ("  Tenant ID:                         " + $tenantId)
        Write-Output ("  DNS Name:                          " + $keyVault.VaultUri)
        Write-Output "  Storage account secret name:       storage-account-name"
        Write-Output "  Application ID secret name:        app-id"
        Write-Output "  Application Secret secret name:    app-secret"
        Write-Warning "Copy this information for the LCS Add-in for easy access. Azure Cloud Shell will eventually time out and close."

        Write-Output '================================================================================='
        Write-Output "Values for System parameters > Data connections:"
        Write-Output ("  Application ID:                    " + $clientAppId)
        Write-Output ("  Application Secret:                " + $ClientAppSecret)
        Write-Output ("  DNS name:                          " + $keyVault.VaultUri)
        Write-Output "  Secret name:                       storage-account-connection-string"
        Write-Warning "Copy this information for the System parameters for easy access. Azure Cloud Shell will eventually time out and close."
    }
    else {
        Write-Output ("Provisioning Azure resources failed with the following state: " + $deployment.ProvisioningState)
        Write-Output ("Some of the resources may have been created in resource group: " + $FullResourceGroupName)
    }
}

function Assert-ScriptSetup {
    if ($PSVersionTable.PSEdition -ne 'Core' -or -not $env:ACC_TID) { 
        throw "This script needs to be uploaded and run from Azure Cloud Shell (PowerShell)." 
    }
    
    if ((Get-AzContext) -eq $null -and (Connect-AzAccount) -eq $null) {
        throw 'Unable to connect to Azure account.'
    }
}

function Set-AzureSubscription {
    $azSubscription = $null
    while (-not ($azSubscription)) {
        $subscriptionId = (Read-Host -Prompt "Enter the Azure Subscription ID: (leave blank for default)")
        if ([string]::IsNullOrWhitespace($subscriptionId)){
            break
        }
        elseif (-not [guid]::TryParse($subscriptionId, $([ref][guid]::Empty))) {
                Write-Warning "Azure Subscription ID must be a valid GUID."
                continue
        }

        $azSubscription = Select-AzSubscription -SubscriptionId $subscriptionId
    }
}

function Create-ADServicePrincipal {
    param (
        [string] $AppId
    )

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $AppId | Out-Null
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
        Write-Host ("Added AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }
    else {
        Write-Host ("Found AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }

    return $service.ObjectId
}

$azureTemplate = @"
{
    "contentVersion": "1.0.0.0",
    "parameters": {
      "aibuilderAppObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of the AI Builder application."
        }
      },
      "clientAppId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the application ID of client application."
        }
      },
      "clientAppSecret": {
        "type": "String",
        "metadata": {
          "description": "Specifies the Azure App ID client secret to in azure key vault."
        }
      },
      "clientAppSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of a client application service principal."
        }
      },
      "userSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of tenant admin service principal."
        }
      },
      "microserviceSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of Microsoft Dynamics ERP Microservices service principal."
        }
      },
      "storageAccountType": {
        "type": "string",
        "defaultValue": "Standard_LRS",
        "allowedValues": [
          "Standard_LRS",
          "Standard_GRS",
          "Standard_ZRS",
          "Premium_LRS"
        ],
        "metadata": {
          "description": "Storage Account type"
        }
      }
    },
    "variables": {
      "storageAccountApiVersion": "2019-06-01",
      "keyVaultApiVersion": "2018-02-14",
      "secretsPermissions": [
        "list",
        "get"
      ],
      "location": "[resourceGroup().location]",
      "storageAccountName": "[concat('store', uniquestring(resourceGroup().id))]",
      "keyVaultName": "[concat('keyvault', uniquestring(resourceGroup().id))]",
      "owner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '8e3af657-a8ff-443c-a75c-2fe8c4bcb635')]",
      "contributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b24988ac-6180-42a0-ab88-20f7382dd24c')]",
      "storageAccountContributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '17d1049b-9a84-46fb-8f53-869881c3d3ab')]",
      "storageBlobDataOwner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b7e6dc6d-f1e8-4753-8033-0f276bb0955b')]",
      "storageBlobDataReader": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '2a2b9908-6ea1-4ae2-8e65-a410df84e7d1')]"
    },
    "resources": [
      {
        "type": "Microsoft.Storage/storageAccounts",
        "apiVersion": "[variables('storageAccountApiVersion')]",
        "name": "[variables('storageAccountName')]",
        "location": "[variables('location')]",
        "sku": {
          "name": "[parameters('storageAccountType')]"
        },
        "kind": "StorageV2",
        "properties": {
          "accessTier": "Hot",
          "supportsHttpsTrafficOnly": true,
          "isHnsEnabled": true
        },
        "resources": [
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'1')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('owner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'2')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('contributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'3')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageAccountContributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'4')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataOwner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'5')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataReader')]",
              "principalId": "[parameters('aibuilderAppObjectId')]"
            }
          }
        ]
      },
      {
        "type": "Microsoft.KeyVault/vaults",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "name": "[variables('keyVaultName')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName'))]"
        ],
        "tags": {
        },
        "properties": {
          "enabledForDeployment": false,
          "enabledForTemplateDeployment": false,
          "enabledForDiskEncryption": false,
          "enableRbacAuthorization": false,
          "accessPolicies": [
            {
              "objectId": "[parameters('clientAppSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('microserviceSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('userSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            }
          ],
          "tenantId": "[subscription().tenantId]",
          "sku": {
            "name": "Standard",
            "family": "A"
          },
          "enableSoftDelete": false,
          "networkAcls": {
            "defaultAction": "Allow",
            "bypass": "AzureServices"
          }
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-id')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppId')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-secret')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppSecret')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-name')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[variables('storageAccountName')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-connection-string')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[concat('DefaultEndpointsProtocol=https;AccountName=', variables('storageAccountName'), ';AccountKey=', listKeys(resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName')), variables('storageAccountApiVersion')).keys[0].value, ';EndpointSuffix=core.windows.net')]"
        }
      }
    ],
    "outputs": {
      "storageAccountName": {
        "type": "string",
        "value": "[variables('storageAccountName')]"
      },
      "keyVaultName": {
        "type": "string",
        "value": "[variables('keyVaultName')]"
      }
    }
  }
"@

try {
  Start-Transcript -path (Join-Path $HOME Provision-FinInsights-Azure.log)
  New-FinanceDataLakeAzureResources
}
catch {
  Write-Error $_.Exception.Message

  if ($PSItem.Exception.StackTrace -ne $null)
  {
      Write-Warning $_.Exception.StackTrace
  }

  $inner = $_.Exception.InnerException
  while ($null -ne $inner) {
    Write-Output 'Inner Exception:'
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $inner.InnerException
  }
}
finally {
  Stop-Transcript
}
```
---

## <a name="configure-the-export-to-data-lake-add-in"></a>Konfigurēt eksportēšanu uz Data Lake pievienojumprogrammu

Veiciet tālāk norādītās darbības, lai izmantotu LCS, pievienojot videi eksportēšanu uz Data Lake pievienojumprogrammu.

1. Pierakstieties LCS un pēc tam pie vides nosaukuma lapas labajā pusē atlasiet **Pilna informācija**.
2. Sadaļā **Vides pievienojumprogrammas** atlasiet **Instalēt jaunu pievienojumprogrammu**.
3. Atlasiet pievienojumprogrammu **Eksportēt uz Data Lake**.
4. Ievadiet tālāk norādītās vērtības.

    | Vērtība                                                              | Apraksts |
    |--------------------------------------------------------------------|-------------|
    | Nomnieka ID Azure abonementam, kur atrodas Galvenās akreditācijas datu glabātava | Nomnieka ID, kur atrodas krātuves konts, pieteikumi un galvenās akreditācijas datu glabātavas. Lai iegūtu šo vērtību, atveriet [Azure portālu](https://portal.azure.com), dodieties uz **Azure Active Directory** un kopējiet vērtību **Nomnieka ID**. |
    | Norādiet sava Key Vault DNS nosaukumu                             | Galvenās akreditācijas datu glabātavas DNS nosaukums, piemēram, `https://customkeyvault.vault.azure.net/`. |
    | Norādiet noslēpumu, kas satur krātuves konta nosaukumu   | **storage-account-name** |
    | Pieteikuma ID noslēpuma nosaukums, kas jāizmanto, lai piekļūtu Data Lake          | **app-id** |
    | Programmas klienta noslēpuma nosaukums                                  | **app-secret** |

5. Piekrītiet nosacījumiem un pēc tam atlasiet **Instalēt**.

Pievienojumprogramma tiks instalēta dažu minūšu laikā.

## <a name="configure-the-finance-insights-add-in"></a>Finance Insights pievienojumprogrammas konfigurēšana

> [!NOTE]
> Ja iepriekš instalējāt pievienojumprogrammu Iegūt ieskatus, atinstalējiet to, pirms tālāk norādītās procedūras izpildes.

Izpildiet šīs darbības, lai instalētu Finance Insights pievienojumprogrammu.

1. Pierakstieties LCS un pēc tam pie vides nosaukuma lapas labajā pusē atlasiet **Pilna informācija**.
2. Sadaļā **Vides pievienojumprogrammas** atlasiet **Instalēt jaunu pievienojumprogrammu**.
3. Atlasiet pievienojumprogrammu **Finance Insights**.
4. Piekrītiet nosacījumiem un pēc tam atlasiet **Instalēt**.

## <a name="feedback-and-support"></a>Atsauksmes un atbalsts

Ja vēlaties sniegt atsauksmes vai jums nepieciešams atbalsts, sūtiet e-pastu uz [Finance Insights (priekšskatījums)](mailto:fiap@microsoft.com).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
