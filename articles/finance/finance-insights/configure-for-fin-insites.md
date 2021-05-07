---
title: Konfigurācija Finanšu ieskatiem (priekšskatījums)
description: Šajā tēmā ir izskaidrotas konfigurācijas darbības, kas ļaus jūsu sistēmai izmantot iespējas, kas pieejamas Finanšu ieskatos.
author: ShivamPandey-msft
ms.date: 11/25/2020
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
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 54117c009cfeb7307938cc6bd43e774ccfedcfb1
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908834"
---
# <a name="configuration-for-finance-insights-preview"></a>Konfigurācija Finanšu ieskatiem (priekšskatījums)

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Finanšu ieskati apvieno Microsoft Dynamics 365 Finance funkcionalitāti ar Microsoft Dataverse, Azure un AI Builder, lai nodrošinātu jaudīgus prognozēšanas rīkus jūsu organizācijai. Šajā tēmā ir izskaidrotas konfigurācijas darbības, kas ļaus jūsu sistēmai izmantot iespējas, kas pieejamas Finanšu ieskatos.

## <a name="deploy-dynamics-365-finance"></a>Dynamics 365 Finance izvietošana

Izvietojiet vides, veicot tālāk norādītās darbības.

1. Microsoft Dynamics Lifecycle Services (LCS) izveidojiet vai atjauniniet Dynamics 365 Finance vidi. Videi nepieciešama programmas versija 10.0.11/ platformas atjauninājums 35 vai jaunāka versija.
2. Videi ir jābūt augstas pieejamības (AP) videi smilškastē. (Šis vides veids ir pazīstams arī kā 2. līmeņa vide.) Lai iegūtu papildu informāciju, skatiet [Vides plānošana](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
3. Ja izmantojat Contoso demonstrācijas datus, būs nepieciešami papildu parauga dati, lai izmantotu Debitora maksājumu prognozes, Skaidras naudas plūsmas prognozes un Budžeta prognožu līdzekļus. 

## <a name="configure-dataverse"></a>Dataverse konfigurēšana

Varat pabeigt manuālās konfigurācijas darbības, kas norādītas tālāk, vai varat paātrināt konfigurācijas procesu, izmantojot nodrošināto Windows PowerShell skriptu. Kad PowerShell skripts ir beidzis darboties, tas sniegs vērtības, ko izmantot, lai konfigurētu Finanšu ieskatus. 

> [!NOTE]
> Datorā atveriet PowerShell, lai palaistu skriptu. Iespējams, būs nepieciešama PowerShell versija 5. Var nedarboties Microsoft Azure CLI "Izmēģini to" opcija.

# <a name="manual-configuration-steps"></a>[Manuālās konfigurācijas darbības](#tab/configuration-steps)

1. Atveriet [Power Platform administrēšanas centru](https://admin.powerplatform.microsoft.com/) un veiciet tālāk norādītās darbības, lai izveidotu jaunu Dataverse vidi tajā pašā Active Directory nomniekā.

    1. Atveriet lapu **Vides**.

        [![Lapa Vides](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)

    2. Atlasiet **Jauna vide**.
    3. Laukā **Veids** atlasiet **Smilškaste**.
    4. Iestatiet opciju **Izveidot datubāzi** uz **Jā**.
    5. Atlasiet **Nākamais**.
    6. Atlasiet jūsu organizācijas valodu un valūtu.
    7. Pieņemiet noklusējuma vērtības pārējiem laukiem.
    8. Atlasiet **Saglabāt**.
    9. Atsvaidziniet lapu **Vides**.
    10. Uzgaidiet, kamēr lauka **Stāvoklis** vērtība tiek atjaunināta uz **Gatavs**.
    11. Pierakstiet Dataverse organizācijas ID.
    12. Atlasiet vidi un pēc atlasiet **Iestatījumi**.
    13. Atlasiet **Resursi \> Visi mantotie iestatījumi**.
    14. Augšējā navigācijas joslā atlasiet **Iestatījumi** un pēc tam atlasiet **Pielāgojumi**.
    15. Atlasiet **Izstrādātāja resursi**.
    16. Kopējiet **Dataverse organizācijas ID** vērtību.
    17. Pierakstiet pārlūkprogrammas adreses joslā esošo Dataverse organizācijas URL. Piemēram, URL varētu būt `https://org42b2b3d3.crm.dynamics.com`.

2. Ja plānojat izmantot Skaidras naudas plūsmas prognožu vai Budžeta prognožu līdzekli, veiciet tālāk norādītās darbības, lai atjauninātu jūsu organizācijas anotāciju ierobežojumu līdz vismaz 50 megabaitiem (MB).

    1. Atveriet [Power Apps portālu](https://make.powerapps.com).
    2. Atlasiet tikko izveidoto vidi un pēc tam atlasiet **Papildu iestatījumi**.
    3. Atlasiet **Iestatījumi \> E-pasta konfigurācija**.
    4. Mainiet lauka **Maksimālais faila izmērs** vērtību uz **51 200**. (Šī vērtība ir izteikta kilobaitos \[KB\].)
    5. Atlasiet **Labi**, lai saglabātu izmaiņas.

# <a name="windows-powershell-configuration-script"></a>[Windows PowerShell konfigurācijas skripts](#tab/powershell-configuration-script)

```azurecli-interactive
Write-Output 'The following modules need to be present for execution of this script:'
Write-Output '  Microsoft.PowerApps.Administration.PowerShell'
Write-Output '  Microsoft.PowerApps.PowerShell'
Write-Output '  Microsoft.Xrm.Tooling.CrmConnector.PowerShell'

try {
    $moduleConsent = Read-Host 'Is it ok to install or update these modules as needed? (yes/no)'
    if ($moduleConsent -ne 'yes' -and $moduleConsent -ne 'y') {
        Write-Warning 'User declined to install required modules.'
        return
    }

    $module = 'Microsoft.PowerApps.Administration.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '2.0.61' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '2.0.61' -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    $module = 'Microsoft.PowerApps.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '1.0.9' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '1.0.9' -AllowClobber -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    $module = 'Microsoft.Xrm.Tooling.CrmConnector.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '3.3.0.892' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '3.3.0.892' -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    Write-Output '================================================================================='

    $useMfa = $false
    $useMfaPrompt = Read-Host "Does your organization require the use of multi-factor authentication? (yes/no)"
    if ($useMfaPrompt -eq 'yes' -or $useMfaPrompt -eq 'y') {
        $useMfa = $true
    }
    if(-not $useMfa) {
        $credential = Get-Credential -Message 'Power Apps Credential'
    }

    $orgFriendlyName = Read-Host "Enter the name of the CDS Organization to use or create: (blank for 'FinanceInsightsOrg')"
    if ($orgFriendlyName.Trim() -eq '') {
        $orgFriendlyName = 'FinanceInsightsOrg'
    }

    $isDefaultOrgPrompt = Read-Host ("Is '" + $orgFriendlyName + "' the default organization for your tenant? (yes/no)")
    if ($isDefaultOrgPrompt -eq 'yes' -or $isDefaultOrgPrompt -eq 'y') {
        $isDefaultOrg = $true
    }

    if ($credential) {
        Add-PowerAppsAccount -Username $credential.UserName -Password $credential.Password
    }
    else {
        Add-PowerAppsAccount
    }

    if ($isDefaultOrg) {
        $orgMatch = ('(default)')
        $environment = (Get-AdminPowerAppEnvironment | Where-Object { $_.IsDefault -eq $true })
    }
    else {
        $orgMatch = ('{0} (*)' -f $orgFriendlyName)
        $environment = (Get-AdminPowerAppEnvironment | Where-Object { ($_.IsDefault -eq $false -and ($_.DisplayName -eq $orgFriendlyName -or $_.DisplayName -like $orgMatch)) })
    }

    $getCrmOrgParams = @{ 'OnlineType' = 'Office365' }
    if ($credential) {
        $getCrmOrgParams.Credential = $credential
    }

    if ($null -eq $environment) {
        Write-Output '================================================================================='
        Write-Output 'PowerApps environment not found. A new one will be provisioned.'

        $invalid = 'invalid'

        $location = $invalid
        $cdsLocations = (Get-AdminPowerAppEnvironmentLocations | Select-Object LocationName).LocationName
        while (-not ($location -in $cdsLocations)) {
            $location = (Read-Host -Prompt "Enter the location in which to create the new PowerApps environment: ('help' to see values)")
            if ($location -eq 'help') {
                $cdsLocations
            }
        }

        $currency = $invalid
        $cdsCurrencies = (Get-AdminPowerAppCdsDatabaseCurrencies -Location $location | Select-Object CurrencyName).CurrencyName
        while ($currency -ne '' -and -not ($currency -in $cdsCurrencies)) {
            $currency = (Read-Host -Prompt "Enter the currency to use for the new PowerApps environment: ('help' to see values, blank for default)")
            if ($currency -eq 'help') {
                $cdsCurrencies
            }
        }

        $language = $invalid
        $cdsLanguages = (Get-AdminPowerAppCdsDatabaseLanguages -Location $location | Select-Object LanguageName, LanguageDisplayName)
        while ($language -ne '' -and -not ($language -in $cdsLanguages.LanguageName)) {
            $language = (Read-Host -Prompt "Enter the language name to use for the new PowerApps environment: ('help' to see values, blank for default)")
            if ($language -eq 'help') {
                $cdsLanguages | Format-Table -Property LanguageName, LanguageDisplayName
            }
        }

        Write-Output 'Provisioning PowerApps environment. This may take several minutes.'

        $sleep = 15

        $envParams = @{ 'DisplayName' = $orgFriendlyName; 'EnvironmentSku' = 'Sandbox'; 'ProvisionDatabase' = $true; 'Location' = $location; 'WaitUntilFinished' = $true }
        if ($language.Trim() -ne '') {
            $envParams.LanguageName = $language
        }
        if ($currency.Trim() -ne '') {
            $envParams.CurrencyName = $currency
        }
        $newEnvResult = New-AdminPowerAppEnvironment @envParams
        if (($null -eq $newEnvResult) -or ($newEnvResult.CommonDataServiceDatabaseProvisioningState -ne 'Succeeded')) {
            Write-Warning 'Failed to create to PowerApps environment'
            if ($null -ne $newEnvResult) {
                $newEnvResult
            }
        }
        else {
            $environment = $null
            $retryCount = 0
            while (($null -eq $environment) -and ($retryCount -lt 5)) {
                Start-Sleep -Seconds $sleep
                $environment = (Get-AdminPowerAppEnvironment | Where-Object { ($_.DisplayName -like $orgMatch) })
            }
            Write-Output ("Provisioned PowerApps environment with name: '" + $environment.DisplayName + "'")
        }

        Write-Output 'Waiting for CDS organization provisioning. This may take several minutes.'
        if (-not $credential) {
            $sleep = 120
            Write-Output 'You may be prompted for credentials multiple times while checking the status of the provisioning.'
        }

        while ($null -eq $crmOrg) {
            Start-Sleep -Seconds $sleep
            $crmOrg = (Get-CrmOrganizations @getCrmOrgParams) | Where-Object { $_.FriendlyName -eq $orgFriendlyName }
        }
    }
    else {
        $crmOrgs = Get-CrmOrganizations @getCrmOrgParams
        if ($UseDefaultOrganization -eq $true) {
            $crmOrg = $crmOrgs | Where-Object { $_.FriendlyName -match $orgMatch }
        }
        else {
            $crmOrg = $crmOrgs | Where-Object { $_.FriendlyName -eq $orgFriendlyName }
        }
    }

    Write-Output '================================================================================='
    Write-Output 'Values for PowerAI LCS Add-In:'
    Write-Output ("  CDS organization url:             " + $crmOrg.WebApplicationUrl)
    Write-Output ("  CDS organization ID:              " + $crmOrg.OrganizationId)
}
catch {
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $_.Exception.InnerException
    while ($null -ne $inner) {
        Write-Output 'Inner Exception:'
        Write-Error $_.Exception.Message
        Write-Warning $_.Exception.StackTrace
        $inner = $inner.InnerException
    }
}
```
---

## <a name="configure-the-azure-setup"></a>Azure iestatījumu konfigurēšana

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a>Ievadiet Dataverse direktorijas ID un lietotāja Azure AD objekta ID

1. Ievadiet Dataverse direktorijas ID.

    1. Atveriet [Azure portālu](https://portal.azure.com).
    2. Pierakstieties, izmantojot lietotāja ID, kas tika izmantots Dataverse vides izveidei.
    3. Dodieties uz **Azure Active Directory**.
    4. Kopējiet **Nomnieka ID** vērtību.

2. Ievadiet lietotāja Azure Active Directory (Azure AD) objekta ID.

    1. [Azure portālā](https://portal.azure.com) dodieties uz **Lietotāji** un uzmeklējiet lietotāju, izmantojot e-pasta adresi.
    2. Atlasiet lietotāja vārdu.
    3. Kopējiet **Objekta ID** vērtību.

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a>Izmantojiet Azure Cloud Shell, lai iestatītu Finanšu ieskatu Data Lake resursus

# <a name="use-a-windows-powershell-script"></a>[Windows PowerShell skripta izmantošana](#tab/use-a-powershell-script)

Windows PowerShell skripts tiek nodrošināts, lai varētu viegli iestatīt Azure resursus, kas aprakstīti sadaļā [Eksporta konfigurēšana uz Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md). Ja vēlaties veikt manuālu iestatīšanu, izlaidiet šo procedūru un turpiniet ar procedūru sadaļā [Manuālā iestatīšana](#manual-setup).

> [!NOTE]
> Izpildiet tālāk norādītās darbības, lai palaistu PowerShell skriptu. Azure CLI opcija "Izmēģiniet to" vai skripta palaišana datorā, iespējams, nedarbosies.

Izpildiet tālāk norādītās darbības, lai konfigurētu Azure, izmantojot Windows PowerShell skriptu. Jums ir jābūt tiesībām izveidot Azure resursu grupu, Azure resursus un Azure AD pieteikumu. Lai iegūtu informāciju par nepieciešamajām atļaujām, skatiet [Pakalpojuma Azure AD atļauju pārbaude](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).

1. [Azure portālā](https://portal.azure.com) dodieties uz savu mērķa Azure abonementu. Atlasiet pogu **Mākoņa čaula**, kas atrodas pa labi no lauka **Meklēt**.
2. Atlasiet **PowerShell**.
3. Izveidojiet krātuvi, ja saņemat aicinājumu to darīt. Pēc tam augšupielādējiet Windows PowerShell skriptu sesijā.
4. Palaidiet skriptu.
5. Sekojiet uzvednēm, lai palaistu skriptu.
6. Izmantojiet skripta izvades informāciju, lai LCS instalētu pievienojumprogrammu **Eksportēt uz Data Lake**.
7. Izmantojiet skripta izvades informāciju, lai iespējotu elementa krātuvi Finance lapā **Datu savienojumi** (**Sistēmas administrēšana \> Sistēmas parametri \> Datu savienojumi**).

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

1. Savā lokālajā datorā atlasiet izvēlni **Sākt** un uzmeklējiet **powershell**.
2. Atlasiet un turiet nospiestu (vai noklikšķiniet ar peles labo pogu) **Windows PowerShell** un pēc tam atlasiet **Palaist kā administratoram**.
3. Palaidiet tālāk norādīto komandu, lai instalētu **AzureAD** moduli.

    `Install-Module -Name AzureAD`

4. Ja ir nepieciešams NuGet nodrošinātājs, lai turpinātu, atlasiet **Y**, lai to instalētu.
5. Ja parādās ziņojums "Neuzticams repozitorijs", atlasiet **Y**, lai turpinātu.
6. Katram pieteikumam, kas jāpievieno, palaidiet tālāk norādītās komandas, lai pievienotu pieteikumu Azure AD. Kad saņemat aicinājumu, pierakstieties kā Azure AD administrators.

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a>Azure resursu izveidošana

> [!NOTE]
> Pārliecinieties, ka izveidojat tālāk norādītos resursus tajā pašā Azure AD instancē kā Dataverse vide. Nav iespējams izmantot resursus no citas Azure AD instances.

1. Izveidojiet jaunu krātuves kontu.

    1. [Azure portālā](https://portal.azure.com) izveidojiet krātuves kontu.
    2. Dialoglodziņā **Izveidot krātuves kontu** iestatiet tālāk norādītos laukus.

        - **Atrašanās vieta** — atlasiet datu centru, kur atrodas jūsu vide.
        - **Veiktspēja** — ieteicams atlasīt **Standarta**.
        - **Konta veids** — jāatlasa **StorageV2**.

    3. Dialoglodziņā **Papildu opcijas** opcijā **Data Lake Storage Gen2** atlasiet **Iespējot** līdzeklī **Hierarhiskās nosaukumvietas**. Deaktivizējot šo līdzekli, nevarat patērēt datus, ko Finance and Operations programmas raksta, izmantojot tādus pakalpojumus kā Power BI datu plūsmas.
    4. Atlasiet **Pārskatīt un izveidot**. Kad izvietošana ir pabeigta, jaunais resurss tiks parādīts Azure portālā.
    5. Dodieties uz izveidoto krātuves kontu.
    6. Kreisās puses izvēlnē atlasiet **Piekļuves galvenie akreditācijas dati**.
    7. Kopējiet un saglabājiet savienojuma virkni vai nu **Key1**, vai **Key2**.
    8. Kopējiet un saglabājiet krātuves konta nosaukumu.

2. Izveidojiet jaunu galveno akreditācijas datu glabātavu.

    1. [Azure portālā](https://portal.azure.com) izveidojiet galveno akreditācijas datu glabātavu.
    2. Dialoglodziņā **Izveidot galveno akreditācijas datu glabātavu** laukā **Novietojums** atlasiet datu centru, kur atrodas jūsu vide.
    3. Pēc galvenās akreditācijas datu glabātavas izveides atlasiet to sarakstā un pēc tam atlasiet **Noslēpumi**.
    4. Atlasiet **Ģenerēt/Importēt**.
    5. Dialoglodziņā **Izveidot noslēpumu** laukā **Augšupielādes opcijas** atlasiet **Manuāli**.
    6. Ievadiet noslēpuma nosaukumu. Pierakstiet nosaukumu, jo jums tas būs jānorāda vēlāk.
    7. Laukā **Vērtība** ievadiet savienojuma virkni, ko ieguvāt no krātuves konta iepriekšējā procedūrā.
    8. Atlasiet **Iespējots** un pēc tam atlasiet **Izveidot**. Noslēpums ir izveidots un pievienots Galveno akreditācijas datu glabātai.
    9. Dodieties uz **Galvenās akreditācijas datu glabātavas pārskatu** un pierakstiet DNS nosaukumu.

3. Izveidojiet un reģistrējiet Azure AD pieteikumu.

    1. [Azure portālā](https://portal.azure.com) dodieties uz **Azure Active Directory** un atlasiet **Pieteikumu reģistrācija**.
    2. Atlasiet **Jauna pieteikuma reģistrācija** un iestatiet tālāk norādītos laukus.

        - **Nosaukums** — ievadiet pieteikuma nosaukumu.
        - **Pieteikuma veids** — atlasiet **Web API**.
        - **Novirzīt URI iestatīšanu** — ievadiet savas Dynamics 365 instances URL, piemēram, `https://yourdynamicsinstance.dynamics.com/auth`.

    3. Dodieties uz tikko izveidoto pieteikumu, kopējiet un saglabājiet tās **Pieteikuma (klienta) ID** vērtību. Šī vērtība būs jānorāda vēlāk, kad iestatīsiet galveno akreditācijas datu glabātavu.
    4. Dodieties uz **API atļaujas** un veiciet tālāk norādītās darbības.

        1. Atlasiet **Pievienot atļauju**.
        2. Atlasiet **Azure Galvenā akreditācijas datu glabātava**.
        3. Pēc deleģēto atļauju atlases atlasiet **lietotājs\_personifikācija**.
        4. Atlasiet **Pievienot atļaujas**.

    5. Pieteikuma izvēlnē atlasiet **Sertifikāti \& noslēpumi** un pēc tam izpildiet tālāk norādītās darbības, lai izveidotu galvenās akreditācijas datu glabātavas noslēpumus.

        1. Atlasiet **Jauns klienta noslēpums**.
        2. Ievadiet nosaukumu laukā **Akreditācijas datu glabātavas apraksts**.
        3. Atlasiet ilgumu un pēc tam atlasiet **Pievienot**. Noslēpums tiek ģenerēts laukā **Vērtība**.
        4. Kopējiet un saglabājiet slepeno vērtību.

4. Izveidojiet Galvenās akreditācijas datu glabātavas noslēpumus.

    1. Dodieties uz galveno akreditācijas datu glabātavu, ko izveidojāt iepriekš, un atlasiet **Noslēpumi**.
    2. Katram noslēpuma nosaukumam tālāk esošajā tabulā veiciet tālāk norādītās darbības.

        1. Atlasiet **Ģenerēt/Importēt**.
        2. Dialoglodziņā **Izveidot noslēpumu** laukā **Augšupielādes opcijas** atlasiet **Manuāli**.
        3. Izveidojiet noslēpuma nosaukumu un vērtību no tālāk redzamās tabulas.
        4. Atlasiet **Iespējots** un pēc tam atlasiet **Izveidot**. Noslēpums ir izveidots un pievienots Galveno akreditācijas datu glabātai.

        | Slepenais nosaukums                       | Noslēpuma vērtība                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | app-id                            | Iepriekš izveidotā pieteikuma ID                                      |
        | app-secret                        | Iepriekš saglabātais klienta noslēpums                                                    |
        | storage-account-name              | Iepriekš izveidotā krātuves konta nosaukums, piemēram, **storageaccount1**       |
        | storage-account-connection-string | Savienojuma virkne, ko krātuves kontam kopējāt no lapas **Piekļuves galvenie akreditācijas dati** |

5. Autorizējiet pieteikumu, lai piekļūtu galveno akreditācijas datu glabātavai.

    1. [Azure portālā](https://portal.azure.com) atveriet iepriekš izveidoto galveno akreditācijas datu glabātavu.
    2. Atlasiet piekļuves politikas.
    3. Katram pieteikumam tālāk esošajā tabulā veiciet tālāk norādītās darbības.

        1. Atlasiet **Pievienot piekļuves politiku**, lai izveidotu piekļuves politiku.
        2. Laukā **Noslēpuma atļaujas** atlasiet atļaujas no tālāk redzamās tabulas.
        3. Laukā **Noslēpuma vadītājs** uzmeklējiet pieteikuma parādāmo nosaukumu no tālāk redzamās tabulas.
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

        1. Atlasiet lomu no tālāk redzamās tabulas.
        2. Atstājiet lauku **Piešķirt piekļuvi** iestatītu uz **Azure AD lietotājs, grupa vai pakalpojuma vadītājs**.
        3. Laukā **Atlasīt** ievadiet pieteikumu no tālāk redzamās tabulas.
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



## <a name="configure-the-data-lake"></a>Data Lake konfigurēšana

Veiciet tālāk norādītās darbības, lai izmantotu LCS, lai pievienotu videi Azure Data Lake pievienojumprogrammu.

1. Pierakstieties LCS un pēc tam pie vides nosaukuma lapas labajā pusē atlasiet **Pilna informācija**.
2. Sadaļā **Vides pievienojumprogrammas** atlasiet **Instalēt jaunu pievienojumprogrammu**.
3. Atlasiet pievienojumprogrammu **Eksportēt uz Data Lake**.
4. Ievadiet tālāk norādītās vērtības.

    | Vērtība                                                              | Apraksts |
    |--------------------------------------------------------------------|-------------|
    | Nomnieka ID Azure abonementam, kur atrodas Galvenās akreditācijas datu glabātava | Nomnieka ID, kur atrodas krātuves konts, pieteikumi un galvenās akreditācijas datu glabātavas. Lai atrastu šo vērtību, atveriet [Azure portālu](https://portal.azure.com), dodieties uz **Azure Active Directory** un kopējiet vērtību **Nomnieka ID**. |
    | Norādiet sava Key Vault DNS nosaukumu                             | Galvenās akreditācijas datu glabātavas DNS nosaukums, piemēram, `https://customkeyvault.vault.azure.net/`. (Šī vērtība atbilst DNS nosaukumam, kas tiek izmantots elementa krātuvē.) |
    | Norādiet noslēpumu, kas satur krātuves konta nosaukumu   | **storage-account-name** |
    | Pieteikuma ID noslēpuma nosaukums, kas jāizmanto, lai piekļūtu Data Lake          | **app-id** |
    | Noslēpuma nosaukums, kas jāizmanto ar pieteikuma ID                                 | **app-secret** |

5. Piekrītiet nosacījumiem un atlasiet **Instalēt**.

Pievienojumprogramma tiks instalēta dažu minūšu laikā.

## <a name="configure-ai-builder"></a>AI Builder konfigurēšana

1. Pierakstieties LCS un atveriet lapu **Detalizēta informācija par vidi**.
2. Ritiniet līdz sadaļai **Vides pievienojumprogrammas**. Ir jābūt redzamām pievienojumprogrammām, kas jau ir instalētas šajā vidē. Ja pievienojumprogramma **Eksportēt uz Data Lake** nav to vidū, konfigurējiet šo pievienojumprogrammu.
3. Atlasiet pievienojumprogrammu **Iegūt ieskatus**.
4. Pievienojumprogrammas detalizētās informācijas lapā **Iegūt ieskatus** ievadiet tālāk norādītās vērtības.

    | Vērtība                                                    | Apraksts |
    |----------------------------------------------------------|-------------|
    | CDS organizācijas URL                                     | Dataverse organizācijas URL Dataverse instancē. Lai atrastu šo vērtību, atveriet [Power Apps portālu](https://make.powerapps.com), atlasiet pogu **Iestatījumi** (zobrata simbols) augšējā labajā stūrī, atlasiet **Papildu iestatījumi** un kopējiet URL. (URL beidzas ar "dynamics.com.") |
    | CDS org. ID                                               | Dataverse instances vides ID. Lai atrastu šo vērtību, atveriet [Power Apps portālu](https://make.powerapps.com), atlasiet pogu **Iestatījumi** (zobrata simbols) augšējā labajā stūrī, atlasiet **Pielāgojumi \> Izstrādātāja resursi \> Instances atsauces informācija** un kopējiet vērtību **ID**. |
    | CDS nomnieka ID (direktorija ID no AAD)               | Dataverse instances nomnieka ID. Lai atrastu šo vērtību, atveriet [Azure portālu](https://portal.azure.com), dodieties uz **Azure Active Directory** un kopējiet vērtību **Nomnieka ID**. |
    | Norādiet tā lietotāja objekta ID, kam ir sistēmas administratora loma | Azure AD lietotāja objekta ID lietotājam Dataverse. Šim lietotājam jābūt Dataverse instances sistēmas administratoram. Lai atrastu šo vērtību, atveriet [Azure portālu](https://portal.azure.com), dodieties uz **Azure Active Directory \> Lietotāji**, atlasiet lietotāju un pēc tam sekcijā **Identitāte** kopējiet vērtību **Objekta ID**. |
    | Vai šī ir nomnieka noklusējuma CDS vide?      | Ja Dataverse instance bija pirmā izveidotā ražošanas instance, atzīmējiet šo izvēles rūtiņu. Ja Dataverse instance tika izveidota manuāli, izņemiet atzīmi no šīs izvēles rūtiņas. |

## <a name="configure-the-entity-store"></a>Elementu krātuves konfigurēšana

Izpildiet tālāk norādītās darbības, lai iestatītu Finanšu vides elementu krātuvi.

1. Dodieties uz **Sistēmas administrēšana \> Iestatījumi \> Sistēmas parametri \> Datu savienojumi**.
2. Iestatiet opciju **Iespējot Data Lake integrāciju** uz **Jā**.
3. Iestatiet tālāk norādītos galvenās akreditācijas datu glabātavas laukus.

    - **Pieteikuma (klienta) ID** — ievadiet iepriekš izveidoto pieteikuma klienta ID.
    - **Pieteikuma noslēpums** — ievadiet noslēpumu, ko saglabājāt iepriekš izveidotajam pieteikumam.
    - **DNS nosaukums** — varat atrast domēna nosaukuma sistēmas (DNS) nosaukumu iepriekš izveidotā pieteikuma detalizētas informācijas lapā.
    - **Noslēpuma nosaukums** — ievadiet **krātuve-konts-savienojums-virkne**.

## <a name="feedback-and-support"></a>Atsauksmes un atbalsts

Lūdzu, sūtiet e-pastu [klientu maksājumu ieskatiem (priekšskatījums)](mailto:fiap@microsoft.com), ja vēlaties sniegt atsauksmes vai ir nepieciešams atbalsts.

## <a name="privacy-notice"></a>Paziņojums par konfidencialitāti

Priekšskatījumiem (1) var tikt izmantots mazāk konfidencialitātes un drošības pasākumu nekā pakalpojumam Dynamics 365 Finance and Operations, (2) tie nav ietverti pakalpojuma līmeņa līgumā par šo pakalpojumu, (3) tos nedrīkst izmantot personas datu vai citu tādu datu apstrādei, uz kuriem attiecas juridiskās vai normatīvās prasības, un (4) tiem tiek nodrošināts ierobežots atbalsts.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
