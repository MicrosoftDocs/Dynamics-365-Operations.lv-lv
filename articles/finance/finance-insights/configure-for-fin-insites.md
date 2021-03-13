---
title: Konfigurācija Finanšu ieskatiem (priekšskatījums)
description: Šajā tēmā ir izskaidrotas konfigurācijas darbības, kas ļaus jūsu sistēmai izmantot iespējas, kas pieejamas Finanšu ieskatos.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: bb887bbff5eb5b92f588d3fa966ea204633575db
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115636"
---
# <a name="configuration-for-finance-insights-preview"></a><span data-ttu-id="46e58-103">Konfigurācija Finanšu ieskatiem (priekšskatījums)</span><span class="sxs-lookup"><span data-stu-id="46e58-103">Configuration for Finance insights (preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="46e58-104">Finanšu ieskati apvieno Microsoft Dynamics 365 Finance funkcionalitāti ar Microsoft Dataverse, Azure un AI Builder, lai nodrošinātu jaudīgus prognozēšanas rīkus jūsu organizācijai.</span><span class="sxs-lookup"><span data-stu-id="46e58-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Microsoft Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="46e58-105">Šajā tēmā ir izskaidrotas konfigurācijas darbības, kas ļaus jūsu sistēmai izmantot iespējas, kas pieejamas Finanšu ieskatos.</span><span class="sxs-lookup"><span data-stu-id="46e58-105">This topic explains the configuration steps that will enable your system to use the capabilities that are available in Finance insights.</span></span>

## <a name="deploy-dynamics-365-finance"></a><span data-ttu-id="46e58-106">Dynamics 365 Finance izvietošana</span><span class="sxs-lookup"><span data-stu-id="46e58-106">Deploy Dynamics 365 Finance</span></span>

<span data-ttu-id="46e58-107">Izvietojiet vides, veicot tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="46e58-107">Deploy the environments by following these steps.</span></span>

1. <span data-ttu-id="46e58-108">Microsoft Dynamics Lifecycle Services (LCS) izveidojiet vai atjauniniet Dynamics 365 Finance vidi.</span><span class="sxs-lookup"><span data-stu-id="46e58-108">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Dynamics 365 Finance environment.</span></span> <span data-ttu-id="46e58-109">Videi nepieciešama programmas versija 10.0.11/ platformas atjauninājums 35 vai jaunāka versija.</span><span class="sxs-lookup"><span data-stu-id="46e58-109">The environment requires app version 10.0.11/Platform update 35 or later.</span></span>
2. <span data-ttu-id="46e58-110">Videi ir jābūt augstas pieejamības (AP) videi smilškastē.</span><span class="sxs-lookup"><span data-stu-id="46e58-110">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="46e58-111">(Šis vides veids ir pazīstams arī kā 2. līmeņa vide.) Lai iegūtu papildu informāciju, skatiet [Vides plānošana](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="46e58-111">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="46e58-112">Ja izmantojat Contoso demonstrācijas datus, būs nepieciešami papildu parauga dati, lai izmantotu Debitora maksājumu prognozes, Skaidras naudas plūsmas prognozes un Budžeta prognožu līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="46e58-112">If you're using Contoso demo data, you will require additional sample data to use the Customer payment predictions, Cash flow forecasts, and Budget forecasts features.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="46e58-113">Dataverse konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="46e58-113">Configure Dataverse</span></span>

<span data-ttu-id="46e58-114">Varat pabeigt manuālās konfigurācijas darbības, kas norādītas tālāk, vai varat paātrināt konfigurācijas procesu, izmantojot nodrošināto Windows PowerShell skriptu.</span><span class="sxs-lookup"><span data-stu-id="46e58-114">You can complete the manual configuration steps that follow, or you can speed up the configuration process by using the Windows PowerShell script that is provided.</span></span> <span data-ttu-id="46e58-115">Kad PowerShell skripts ir beidzis darboties, tas sniegs vērtības, ko izmantot, lai konfigurētu Finanšu ieskatus.</span><span class="sxs-lookup"><span data-stu-id="46e58-115">When the PowerShell script has finished running, it will give you values to use to configure Finance insights.</span></span> 

> [!NOTE]
> <span data-ttu-id="46e58-116">Datorā atveriet PowerShell, lai palaistu skriptu.</span><span class="sxs-lookup"><span data-stu-id="46e58-116">Open PowerShell on your PC to run the script.</span></span> <span data-ttu-id="46e58-117">Iespējams, būs nepieciešama PowerShell versija 5.</span><span class="sxs-lookup"><span data-stu-id="46e58-117">You may need PowerShell version 5.</span></span> <span data-ttu-id="46e58-118">Var nedarboties Microsoft Azure CLI "Izmēģini to" opcija.</span><span class="sxs-lookup"><span data-stu-id="46e58-118">The Microsoft Azure CLI "Try it" option may not work.</span></span>

# <a name="manual-configuration-steps"></a>[<span data-ttu-id="46e58-119">Manuālās konfigurācijas darbības</span><span class="sxs-lookup"><span data-stu-id="46e58-119">Manual configuration steps</span></span>](#tab/configuration-steps)

1. <span data-ttu-id="46e58-120">Atveriet [Power Platform administrēšanas centru](https://admin.powerplatform.microsoft.com/) un veiciet tālāk norādītās darbības, lai izveidotu jaunu Dataverse vidi tajā pašā Active Directory nomniekā.</span><span class="sxs-lookup"><span data-stu-id="46e58-120">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), and follow these steps to create a new Dataverse environment in the same Active Directory tenant:</span></span>

    1. <span data-ttu-id="46e58-121">Atveriet lapu **Vides**.</span><span class="sxs-lookup"><span data-stu-id="46e58-121">Open the **Environments** page.</span></span>

        <span data-ttu-id="46e58-122">[![Lapa Vides](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span><span class="sxs-lookup"><span data-stu-id="46e58-122">[![Environments page](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span></span>

    2. <span data-ttu-id="46e58-123">Atlasiet **Jauna vide**.</span><span class="sxs-lookup"><span data-stu-id="46e58-123">Select **New environment**.</span></span>
    3. <span data-ttu-id="46e58-124">Laukā **Veids** atlasiet **Smilškaste**.</span><span class="sxs-lookup"><span data-stu-id="46e58-124">In the **Type** field, select **Sandbox**.</span></span>
    4. <span data-ttu-id="46e58-125">Iestatiet opciju **Izveidot datubāzi** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="46e58-125">Set the **Create Database** option to **Yes**.</span></span>
    5. <span data-ttu-id="46e58-126">Atlasiet **Nākamais**.</span><span class="sxs-lookup"><span data-stu-id="46e58-126">Select **Next**.</span></span>
    6. <span data-ttu-id="46e58-127">Atlasiet jūsu organizācijas valodu un valūtu.</span><span class="sxs-lookup"><span data-stu-id="46e58-127">Select the language and currency for your organization.</span></span>
    7. <span data-ttu-id="46e58-128">Pieņemiet noklusējuma vērtības pārējiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="46e58-128">Accept the default values for the other fields.</span></span>
    8. <span data-ttu-id="46e58-129">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="46e58-129">Select **Save**.</span></span>
    9. <span data-ttu-id="46e58-130">Atsvaidziniet lapu **Vides**.</span><span class="sxs-lookup"><span data-stu-id="46e58-130">Refresh the **Environments** page.</span></span>
    10. <span data-ttu-id="46e58-131">Uzgaidiet, kamēr lauka **Stāvoklis** vērtība tiek atjaunināta uz **Gatavs**.</span><span class="sxs-lookup"><span data-stu-id="46e58-131">Wait until the value of the **State** field is updated to **Ready**.</span></span>
    11. <span data-ttu-id="46e58-132">Pierakstiet Dataverse organizācijas ID.</span><span class="sxs-lookup"><span data-stu-id="46e58-132">Make a note of the Dataverse organization ID.</span></span>
    12. <span data-ttu-id="46e58-133">Atlasiet vidi un pēc atlasiet **Iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="46e58-133">Select the environment, and then select **Settings**.</span></span>
    13. <span data-ttu-id="46e58-134">Atlasiet **Resursi \> Visi mantotie iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="46e58-134">Select **Resources \> All Legacy Settings**.</span></span>
    14. <span data-ttu-id="46e58-135">Augšējā navigācijas joslā atlasiet **Iestatījumi** un pēc tam atlasiet **Pielāgojumi**.</span><span class="sxs-lookup"><span data-stu-id="46e58-135">On the top navigation bar, select **Settings**, and then select **Customizations**.</span></span>
    15. <span data-ttu-id="46e58-136">Atlasiet **Izstrādātāja resursi**.</span><span class="sxs-lookup"><span data-stu-id="46e58-136">Select **Developer Resources**.</span></span>
    16. <span data-ttu-id="46e58-137">Iestatiet laukā **Instances atsauces informācijas ID** Dataverse organizācijas ID vērtību, ko pierakstījāt iepriekš.</span><span class="sxs-lookup"><span data-stu-id="46e58-137">Set the **Instance Reference Information ID** field to the Dataverse organization ID value that you made a note of earlier.</span></span>
    17. <span data-ttu-id="46e58-138">Pierakstiet pārlūkprogrammas adreses joslā esošo Dataverse organizācijas URL.</span><span class="sxs-lookup"><span data-stu-id="46e58-138">In the browser's address bar, make a note of the URL for the Dataverse organization.</span></span> <span data-ttu-id="46e58-139">Piemēram, URL varētu būt `https://org42b2b3d3.crm.dynamics.com`.</span><span class="sxs-lookup"><span data-stu-id="46e58-139">For example, the URL might be `https://org42b2b3d3.crm.dynamics.com`.</span></span>

2. <span data-ttu-id="46e58-140">Ja plānojat izmantot Skaidras naudas plūsmas prognožu vai Budžeta prognožu līdzekli, veiciet tālāk norādītās darbības, lai atjauninātu jūsu organizācijas anotāciju ierobežojumu līdz vismaz 50 megabaitiem (MB).</span><span class="sxs-lookup"><span data-stu-id="46e58-140">If you plan to use the Cash flow forecasts or Budget forecasts feature, follow these steps to update the annotation limit for your organization to at least 50 megabytes (MB):</span></span>

    1. <span data-ttu-id="46e58-141">Atveriet [Power Apps portālu](https://make.powerapps.com).</span><span class="sxs-lookup"><span data-stu-id="46e58-141">Open the [Power Apps portal](https://make.powerapps.com).</span></span>
    2. <span data-ttu-id="46e58-142">Atlasiet tikko izveidoto vidi un pēc tam atlasiet **Papildu iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="46e58-142">Select the environment that you just created, and then select **Advanced settings**.</span></span>
    3. <span data-ttu-id="46e58-143">Atlasiet **Iestatījumi \> E-pasta konfigurācija**.</span><span class="sxs-lookup"><span data-stu-id="46e58-143">Select **Settings \> Email Configuration**.</span></span>
    4. <span data-ttu-id="46e58-144">Mainiet lauka **Maksimālais faila izmērs** vērtību uz **51 200**.</span><span class="sxs-lookup"><span data-stu-id="46e58-144">Change the value of the **Maximum file size** field to **51,200**.</span></span> <span data-ttu-id="46e58-145">(Šī vērtība ir izteikta kilobaitos \[KB\].)</span><span class="sxs-lookup"><span data-stu-id="46e58-145">(The value is expressed in kilobytes \[KB\].)</span></span>
    5. <span data-ttu-id="46e58-146">Atlasiet **Labi**, lai saglabātu izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="46e58-146">Select **OK** to save your changes.</span></span>

# <a name="windows-powershell-configuration-script"></a>[<span data-ttu-id="46e58-147">Windows PowerShell konfigurācijas skripts</span><span class="sxs-lookup"><span data-stu-id="46e58-147">Windows PowerShell configuration script</span></span>](#tab/powershell-configuration-script)

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

## <a name="configure-the-azure-setup"></a><span data-ttu-id="46e58-148">Azure iestatījumu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="46e58-148">Configure the Azure setup</span></span>

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a><span data-ttu-id="46e58-149">Ievadiet Dataverse direktorijas ID un lietotāja Azure AD objekta ID</span><span class="sxs-lookup"><span data-stu-id="46e58-149">Enter the Dataverse directory ID and the user's Azure AD object ID</span></span>

1. <span data-ttu-id="46e58-150">Ievadiet Dataverse direktorijas ID.</span><span class="sxs-lookup"><span data-stu-id="46e58-150">Enter the Dataverse directory ID:</span></span>

    1. <span data-ttu-id="46e58-151">Atveriet [Azure portālu](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="46e58-151">Open the [Azure portal](https://portal.azure.com).</span></span>
    2. <span data-ttu-id="46e58-152">Pierakstieties, izmantojot lietotāja ID, kas tika izmantots Dataverse vides izveidei.</span><span class="sxs-lookup"><span data-stu-id="46e58-152">Sign in by using the user ID that was used to create the Dataverse environment.</span></span>
    3. <span data-ttu-id="46e58-153">Dodieties uz **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="46e58-153">Go to **Azure Active Directory**.</span></span>
    4. <span data-ttu-id="46e58-154">Kopējiet **Nomnieka ID** vērtību.</span><span class="sxs-lookup"><span data-stu-id="46e58-154">Copy the **Tenant ID** value.</span></span>

2. <span data-ttu-id="46e58-155">Ievadiet lietotāja Azure Active Directory (Azure AD) objekta ID.</span><span class="sxs-lookup"><span data-stu-id="46e58-155">Enter the user's Azure Active Directory (Azure AD) object ID:</span></span>

    1. <span data-ttu-id="46e58-156">[Azure portālā](https://portal.azure.com) dodieties uz **Lietotāji** un uzmeklējiet lietotāju, izmantojot e-pasta adresi.</span><span class="sxs-lookup"><span data-stu-id="46e58-156">In the [Azure portal](https://portal.azure.com), go to **Users**, and search for the user by email address.</span></span>
    2. <span data-ttu-id="46e58-157">Atlasiet lietotāja vārdu.</span><span class="sxs-lookup"><span data-stu-id="46e58-157">Select the user's name.</span></span>
    3. <span data-ttu-id="46e58-158">Kopējiet **Objekta ID** vērtību.</span><span class="sxs-lookup"><span data-stu-id="46e58-158">Copy the **Object ID** value.</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="46e58-159">Izmantojiet Azure Cloud Shell, lai iestatītu Finanšu ieskatu Data Lake resursus</span><span class="sxs-lookup"><span data-stu-id="46e58-159">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="46e58-160">Windows PowerShell skripta izmantošana</span><span class="sxs-lookup"><span data-stu-id="46e58-160">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="46e58-161">Windows PowerShell skripts tiek nodrošināts, lai varētu viegli iestatīt Azure resursus, kas aprakstīti sadaļā [Eksporta konfigurēšana uz Azure Data Lake](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/configure-export-data-lake).</span><span class="sxs-lookup"><span data-stu-id="46e58-161">A Windows PowerShell script has been provided, so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/configure-export-data-lake).</span></span> <span data-ttu-id="46e58-162">Ja vēlaties veikt manuālu iestatīšanu, izlaidiet šo procedūru un turpiniet ar procedūru sadaļā [Manuālā iestatīšana](#manual-setup).</span><span class="sxs-lookup"><span data-stu-id="46e58-162">If you prefer to do manual setup, skip this procedure, and continue with the procedure in the [Manual setup](#manual-setup) section.</span></span>

> [!NOTE]
> <span data-ttu-id="46e58-163">Izpildiet tālāk norādītās darbības, lai palaistu PowerShell skriptu.</span><span class="sxs-lookup"><span data-stu-id="46e58-163">Follow the steps below to run the PowerShell script.</span></span> <span data-ttu-id="46e58-164">Azure CLI opcija "Izmēģiniet to" vai skripta palaišana datorā, iespējams, nedarbosies.</span><span class="sxs-lookup"><span data-stu-id="46e58-164">The Azure CLI "Try it" option, or running the script on your PC may not work.</span></span>

<span data-ttu-id="46e58-165">Izpildiet tālāk norādītās darbības, lai konfigurētu Azure, izmantojot Windows PowerShell skriptu.</span><span class="sxs-lookup"><span data-stu-id="46e58-165">Follow these steps to configure Azure by using the Windows PowerShell script.</span></span> <span data-ttu-id="46e58-166">Jums ir jābūt tiesībām izveidot Azure resursu grupu, Azure resursus un Azure AD pieteikumu.</span><span class="sxs-lookup"><span data-stu-id="46e58-166">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="46e58-167">Lai iegūtu informāciju par nepieciešamajām atļaujām, skatiet [Azure AD atļauju pārbaude](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="46e58-167">For information about the required permissions, see [Check Azure AD permissions](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="46e58-168">[Azure portālā](https://portal.azure.com) dodieties uz savu mērķa Azure abonementu.</span><span class="sxs-lookup"><span data-stu-id="46e58-168">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span> <span data-ttu-id="46e58-169">Atlasiet pogu **Mākoņa čaula**, kas atrodas pa labi no lauka **Meklēt**.</span><span class="sxs-lookup"><span data-stu-id="46e58-169">Select the **Cloud Shell** button to the right of the **Search** field.</span></span>
2. <span data-ttu-id="46e58-170">Atlasiet **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="46e58-170">Select **PowerShell**.</span></span>
3. <span data-ttu-id="46e58-171">Izveidojiet krātuvi, ja saņemat aicinājumu to darīt.</span><span class="sxs-lookup"><span data-stu-id="46e58-171">Create storage, if you're prompted to do so.</span></span> <span data-ttu-id="46e58-172">Pēc tam augšupielādējiet Windows PowerShell skriptu sesijā.</span><span class="sxs-lookup"><span data-stu-id="46e58-172">Then upload the Windows PowerShell script to the session.</span></span>
4. <span data-ttu-id="46e58-173">Palaidiet skriptu.</span><span class="sxs-lookup"><span data-stu-id="46e58-173">Run the script.</span></span>
5. <span data-ttu-id="46e58-174">Sekojiet uzvednēm, lai palaistu skriptu.</span><span class="sxs-lookup"><span data-stu-id="46e58-174">Follow the prompts to run the script.</span></span>
6. <span data-ttu-id="46e58-175">Izmantojiet skripta izvades informāciju, lai LCS instalētu pievienojumprogrammu **Eksportēt uz Data Lake**.</span><span class="sxs-lookup"><span data-stu-id="46e58-175">Use the information from the script output to install the **Export to Data Lake** add-in in LCS.</span></span>
7. <span data-ttu-id="46e58-176">Izmantojiet skripta izvades informāciju, lai iespējotu elementa krātuvi Finance lapā **Datu savienojumi** (**Sistēmas administrēšana \> Sistēmas parametri \> Datu savienojumi**).</span><span class="sxs-lookup"><span data-stu-id="46e58-176">Use the information from the script output to enable the entity store on the **Data connections** page in Finance (**System administration \> System parameters \> Data connections**).</span></span>

### <a name="manual-setup"></a><span data-ttu-id="46e58-177">Manuāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="46e58-177">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="46e58-178">Pieteikumu pievienošana Azure AD nomniekam</span><span class="sxs-lookup"><span data-stu-id="46e58-178">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="46e58-179">[Azure portālā](https://portal.azure.com) dodieties uz **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="46e58-179">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="46e58-180">Atlasiet **Pārvaldīt \> Uzņēmuma pieteikumi**.</span><span class="sxs-lookup"><span data-stu-id="46e58-180">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="46e58-181">Uzmeklējiet tālāk norādītos pieteikumus, izmantojot pieteikuma ID.</span><span class="sxs-lookup"><span data-stu-id="46e58-181">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="46e58-182">Pieteikums</span><span class="sxs-lookup"><span data-stu-id="46e58-182">Application</span></span>                              | <span data-ttu-id="46e58-183">Programmas ID</span><span class="sxs-lookup"><span data-stu-id="46e58-183">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="46e58-184">Microsoft Dynamics ERP apakšpakalpojumi</span><span class="sxs-lookup"><span data-stu-id="46e58-184">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="46e58-185">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="46e58-185">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="46e58-186">Microsoft Dynamics ERP apakšpakalpojumi CDS</span><span class="sxs-lookup"><span data-stu-id="46e58-186">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="46e58-187">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="46e58-187">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="46e58-188">AI Builder autorizācijas pakalpojums</span><span class="sxs-lookup"><span data-stu-id="46e58-188">AI Builder Authorization Service</span></span>         | <span data-ttu-id="46e58-189">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="46e58-189">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="46e58-190">Ja nevarat atrast nevienu no iepriekšējiem pieteikumiem, izmēģiniet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="46e58-190">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="46e58-191">Savā lokālajā datorā atlasiet izvēlni **Sākt** un uzmeklējiet **powershell**.</span><span class="sxs-lookup"><span data-stu-id="46e58-191">On your local machine, select the **Start** menu, and search for **powershell**.</span></span>
2. <span data-ttu-id="46e58-192">Atlasiet un turiet nospiestu (vai noklikšķiniet ar peles labo pogu) **Windows PowerShell** un pēc tam atlasiet **Palaist kā administratoram**.</span><span class="sxs-lookup"><span data-stu-id="46e58-192">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="46e58-193">Palaidiet tālāk norādīto komandu, lai instalētu **AzureAD** moduli.</span><span class="sxs-lookup"><span data-stu-id="46e58-193">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="46e58-194">Ja ir nepieciešams NuGet nodrošinātājs, lai turpinātu, atlasiet **Y**, lai to instalētu.</span><span class="sxs-lookup"><span data-stu-id="46e58-194">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="46e58-195">Ja parādās ziņojums "Neuzticams repozitorijs", atlasiet **Y**, lai turpinātu.</span><span class="sxs-lookup"><span data-stu-id="46e58-195">If an "Untrusted repository" message appears, select **Y** to continue.</span></span>
6. <span data-ttu-id="46e58-196">Katram pieteikumam, kas jāpievieno, palaidiet tālāk norādītās komandas, lai pievienotu pieteikumu Azure AD.</span><span class="sxs-lookup"><span data-stu-id="46e58-196">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="46e58-197">Kad saņemat aicinājumu, pierakstieties kā Azure AD administrators.</span><span class="sxs-lookup"><span data-stu-id="46e58-197">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="46e58-198">Azure resursu izveidošana</span><span class="sxs-lookup"><span data-stu-id="46e58-198">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="46e58-199">Pārliecinieties, ka izveidojat tālāk norādītos resursus tajā pašā Azure AD instancē kā Dataverse vide.</span><span class="sxs-lookup"><span data-stu-id="46e58-199">Make sure that you create the following resources in the same Azure AD instance as the Dataverse environment.</span></span> <span data-ttu-id="46e58-200">Nav iespējams izmantot resursus no citas Azure AD instances.</span><span class="sxs-lookup"><span data-stu-id="46e58-200">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="46e58-201">Izveidojiet jaunu krātuves kontu.</span><span class="sxs-lookup"><span data-stu-id="46e58-201">Create a new storage account:</span></span>

    1. <span data-ttu-id="46e58-202">[Azure portālā](https://portal.azure.com) izveidojiet krātuves kontu.</span><span class="sxs-lookup"><span data-stu-id="46e58-202">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="46e58-203">Dialoglodziņā **Izveidot krātuves kontu** iestatiet tālāk norādītos laukus.</span><span class="sxs-lookup"><span data-stu-id="46e58-203">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="46e58-204">**Atrašanās vieta** — atlasiet datu centru, kur atrodas jūsu vide.</span><span class="sxs-lookup"><span data-stu-id="46e58-204">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="46e58-205">**Veiktspēja** — ieteicams atlasīt **Standarta**.</span><span class="sxs-lookup"><span data-stu-id="46e58-205">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="46e58-206">**Konta veids** — jāatlasa **StorageV2**.</span><span class="sxs-lookup"><span data-stu-id="46e58-206">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="46e58-207">Dialoglodziņā **Papildu opcijas** opcijā **Data Lake Storage Gen2** atlasiet **Iespējot** līdzeklī **Hierarhiskās nosaukumvietas**.</span><span class="sxs-lookup"><span data-stu-id="46e58-207">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="46e58-208">Deaktivizējot šo līdzekli, nevarat patērēt datus, ko Finance and Operations programmas raksta, izmantojot tādus pakalpojumus kā Power BI datu plūsmas.</span><span class="sxs-lookup"><span data-stu-id="46e58-208">If you disable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="46e58-209">Atlasiet **Pārskatīt un izveidot**.</span><span class="sxs-lookup"><span data-stu-id="46e58-209">Select **Review and create**.</span></span> <span data-ttu-id="46e58-210">Kad izvietošana ir pabeigta, jaunais resurss tiks parādīts Azure portālā.</span><span class="sxs-lookup"><span data-stu-id="46e58-210">When the deployment is completed, the new resource will be shown in the Azure portal.</span></span>
    5. <span data-ttu-id="46e58-211">Dodieties uz izveidoto krātuves kontu.</span><span class="sxs-lookup"><span data-stu-id="46e58-211">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="46e58-212">Kreisās puses izvēlnē atlasiet **Piekļuves galvenie akreditācijas dati**.</span><span class="sxs-lookup"><span data-stu-id="46e58-212">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="46e58-213">Kopējiet un saglabājiet savienojuma virkni vai nu **Key1**, vai **Key2**.</span><span class="sxs-lookup"><span data-stu-id="46e58-213">Copy and save the connection string for either **Key1** or **Key2**.</span></span>
    8. <span data-ttu-id="46e58-214">Kopējiet un saglabājiet krātuves konta nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="46e58-214">Copy and save the storage account name.</span></span>

2. <span data-ttu-id="46e58-215">Izveidojiet jaunu galveno akreditācijas datu glabātavu.</span><span class="sxs-lookup"><span data-stu-id="46e58-215">Create a new key vault:</span></span>

    1. <span data-ttu-id="46e58-216">[Azure portālā](https://portal.azure.com) izveidojiet galveno akreditācijas datu glabātavu.</span><span class="sxs-lookup"><span data-stu-id="46e58-216">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="46e58-217">Dialoglodziņā **Izveidot galveno akreditācijas datu glabātavu** laukā **Novietojums** atlasiet datu centru, kur atrodas jūsu vide.</span><span class="sxs-lookup"><span data-stu-id="46e58-217">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="46e58-218">Pēc galvenās akreditācijas datu glabātavas izveides atlasiet to sarakstā un pēc tam atlasiet **Noslēpumi**.</span><span class="sxs-lookup"><span data-stu-id="46e58-218">After key vault is created, select it in the list, and then select **Secrets**.</span></span>
    4. <span data-ttu-id="46e58-219">Atlasiet **Ģenerēt/Importēt**.</span><span class="sxs-lookup"><span data-stu-id="46e58-219">Select **Generate/Import**.</span></span>
    5. <span data-ttu-id="46e58-220">Dialoglodziņā **Izveidot noslēpumu** laukā **Augšupielādes opcijas** atlasiet **Manuāli**.</span><span class="sxs-lookup"><span data-stu-id="46e58-220">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
    6. <span data-ttu-id="46e58-221">Ievadiet noslēpuma nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="46e58-221">Enter a name for the secret.</span></span> <span data-ttu-id="46e58-222">Pierakstiet nosaukumu, jo jums tas būs jānorāda vēlāk.</span><span class="sxs-lookup"><span data-stu-id="46e58-222">Make a note of the name, because you will have to provide it later.</span></span>
    7. <span data-ttu-id="46e58-223">Laukā **Vērtība** ievadiet savienojuma virkni, ko ieguvāt no krātuves konta iepriekšējā procedūrā.</span><span class="sxs-lookup"><span data-stu-id="46e58-223">In the **Value** field, enter the connection string that you obtained from the storage account in the previous procedure.</span></span>
    8. <span data-ttu-id="46e58-224">Atlasiet **Iespējots** un pēc tam atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="46e58-224">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="46e58-225">Noslēpums ir izveidots un pievienots Galveno akreditācijas datu glabātai.</span><span class="sxs-lookup"><span data-stu-id="46e58-225">The secret is created and added to Key Vault.</span></span>
    9. <span data-ttu-id="46e58-226">Dodieties uz **Galvenās akreditācijas datu glabātavas pārskatu** un pierakstiet DNS nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="46e58-226">Go to the **Key Vault Overview**, and make a note of the DNS name.</span></span>

3. <span data-ttu-id="46e58-227">Izveidojiet un reģistrējiet Azure AD pieteikumu.</span><span class="sxs-lookup"><span data-stu-id="46e58-227">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="46e58-228">[Azure portālā](https://portal.azure.com) dodieties uz **Azure Active Directory** un atlasiet **Pieteikumu reģistrācija**.</span><span class="sxs-lookup"><span data-stu-id="46e58-228">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="46e58-229">Atlasiet **Jauna pieteikuma reģistrācija** un iestatiet tālāk norādītos laukus.</span><span class="sxs-lookup"><span data-stu-id="46e58-229">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="46e58-230">**Nosaukums** — ievadiet pieteikuma nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="46e58-230">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="46e58-231">**Pieteikuma veids** — atlasiet **Web API**.</span><span class="sxs-lookup"><span data-stu-id="46e58-231">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="46e58-232">**Novirzīt URI iestatīšanu** — ievadiet savas Dynamics 365 instances URL, piemēram, `https://yourdynamicsinstance.dynamics.com/auth`.</span><span class="sxs-lookup"><span data-stu-id="46e58-232">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as, `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="46e58-233">Dodieties uz tikko izveidoto pieteikumu, kopējiet un saglabājiet tās **Pieteikuma (klienta) ID** vērtību.</span><span class="sxs-lookup"><span data-stu-id="46e58-233">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="46e58-234">Šī vērtība būs jānorāda vēlāk, kad iestatīsiet galveno akreditācijas datu glabātavu.</span><span class="sxs-lookup"><span data-stu-id="46e58-234">You will have to provide this value later, when you set up the key vault.</span></span>
    4. <span data-ttu-id="46e58-235">Dodieties uz **API atļaujas** un veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="46e58-235">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="46e58-236">Atlasiet **Pievienot atļauju**.</span><span class="sxs-lookup"><span data-stu-id="46e58-236">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="46e58-237">Atlasiet **Azure Galvenā akreditācijas datu glabātava**.</span><span class="sxs-lookup"><span data-stu-id="46e58-237">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="46e58-238">Pēc deleģēto atļauju atlases atlasiet **lietotājs\_personifikācija**.</span><span class="sxs-lookup"><span data-stu-id="46e58-238">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="46e58-239">Atlasiet **Pievienot atļaujas**.</span><span class="sxs-lookup"><span data-stu-id="46e58-239">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="46e58-240">Pieteikuma izvēlnē atlasiet **Sertifikāti \& noslēpumi** un pēc tam izpildiet tālāk norādītās darbības, lai izveidotu galvenās akreditācijas datu glabātavas noslēpumus.</span><span class="sxs-lookup"><span data-stu-id="46e58-240">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="46e58-241">Atlasiet **Jauns klienta noslēpums**.</span><span class="sxs-lookup"><span data-stu-id="46e58-241">Select **New client secret**.</span></span>
        2. <span data-ttu-id="46e58-242">Ievadiet nosaukumu laukā **Akreditācijas datu glabātavas apraksts**.</span><span class="sxs-lookup"><span data-stu-id="46e58-242">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="46e58-243">Atlasiet ilgumu un pēc tam atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="46e58-243">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="46e58-244">Noslēpums tiek ģenerēts laukā **Vērtība**.</span><span class="sxs-lookup"><span data-stu-id="46e58-244">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="46e58-245">Kopējiet un saglabājiet slepeno vērtību.</span><span class="sxs-lookup"><span data-stu-id="46e58-245">Copy and save the secret value.</span></span>

4. <span data-ttu-id="46e58-246">Izveidojiet Galvenās akreditācijas datu glabātavas noslēpumus.</span><span class="sxs-lookup"><span data-stu-id="46e58-246">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="46e58-247">Dodieties uz galveno akreditācijas datu glabātavu, ko izveidojāt iepriekš, un atlasiet **Noslēpumi**.</span><span class="sxs-lookup"><span data-stu-id="46e58-247">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="46e58-248">Katram noslēpuma nosaukumam tālāk esošajā tabulā veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="46e58-248">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="46e58-249">Atlasiet **Ģenerēt/Importēt**.</span><span class="sxs-lookup"><span data-stu-id="46e58-249">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="46e58-250">Dialoglodziņā **Izveidot noslēpumu** laukā **Augšupielādes opcijas** atlasiet **Manuāli**.</span><span class="sxs-lookup"><span data-stu-id="46e58-250">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="46e58-251">Izveidojiet noslēpuma nosaukumu un vērtību no tālāk redzamās tabulas.</span><span class="sxs-lookup"><span data-stu-id="46e58-251">Create the secret name and value from the following table.</span></span>
        4. <span data-ttu-id="46e58-252">Atlasiet **Iespējots** un pēc tam atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="46e58-252">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="46e58-253">Noslēpums ir izveidots un pievienots Galveno akreditācijas datu glabātai.</span><span class="sxs-lookup"><span data-stu-id="46e58-253">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="46e58-254">Slepenais nosaukums</span><span class="sxs-lookup"><span data-stu-id="46e58-254">Secret name</span></span>                       | <span data-ttu-id="46e58-255">Noslēpuma vērtība</span><span class="sxs-lookup"><span data-stu-id="46e58-255">Secret value</span></span>                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | <span data-ttu-id="46e58-256">app-id</span><span class="sxs-lookup"><span data-stu-id="46e58-256">app-id</span></span>                            | <span data-ttu-id="46e58-257">Iepriekš izveidotā pieteikuma ID</span><span class="sxs-lookup"><span data-stu-id="46e58-257">The app ID of the application that you created earlier</span></span>                                      |
        | <span data-ttu-id="46e58-258">app-secret</span><span class="sxs-lookup"><span data-stu-id="46e58-258">app-secret</span></span>                        | <span data-ttu-id="46e58-259">Iepriekš saglabātais klienta noslēpums</span><span class="sxs-lookup"><span data-stu-id="46e58-259">The client secret that you saved earlier</span></span>                                                    |
        | <span data-ttu-id="46e58-260">storage-account-name</span><span class="sxs-lookup"><span data-stu-id="46e58-260">storage-account-name</span></span>              | <span data-ttu-id="46e58-261">Iepriekš izveidotā krātuves konta nosaukums, piemēram, **storageaccount1**</span><span class="sxs-lookup"><span data-stu-id="46e58-261">The name of the storage account that you created earlier, such as **storageaccount1**</span></span>       |
        | <span data-ttu-id="46e58-262">storage-account-connection-string</span><span class="sxs-lookup"><span data-stu-id="46e58-262">storage-account-connection-string</span></span> | <span data-ttu-id="46e58-263">Savienojuma virkne, ko krātuves kontam kopējāt no lapas **Piekļuves galvenie akreditācijas dati**</span><span class="sxs-lookup"><span data-stu-id="46e58-263">The connection string that you copied from the **Access keys** page for the storage account</span></span> |

5. <span data-ttu-id="46e58-264">Autorizējiet pieteikumu, lai piekļūtu galveno akreditācijas datu glabātavai.</span><span class="sxs-lookup"><span data-stu-id="46e58-264">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="46e58-265">[Azure portālā](https://portal.azure.com) atveriet iepriekš izveidoto galveno akreditācijas datu glabātavu.</span><span class="sxs-lookup"><span data-stu-id="46e58-265">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="46e58-266">Atlasiet piekļuves politikas.</span><span class="sxs-lookup"><span data-stu-id="46e58-266">Select the access policies.</span></span>
    3. <span data-ttu-id="46e58-267">Katram pieteikumam tālāk esošajā tabulā veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="46e58-267">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="46e58-268">Atlasiet **Pievienot piekļuves politiku**, lai izveidotu piekļuves politiku.</span><span class="sxs-lookup"><span data-stu-id="46e58-268">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="46e58-269">Laukā **Noslēpuma atļaujas** atlasiet atļaujas no tālāk redzamās tabulas.</span><span class="sxs-lookup"><span data-stu-id="46e58-269">In the **Secret permissions** field, select the permissions from the following table.</span></span>
        3. <span data-ttu-id="46e58-270">Laukā **Noslēpuma vadītājs** uzmeklējiet pieteikuma parādāmo nosaukumu no tālāk redzamās tabulas.</span><span class="sxs-lookup"><span data-stu-id="46e58-270">In the **Select principal** field, search for the application display name from the following table.</span></span>
        4. <span data-ttu-id="46e58-271">Atlasiet **Atlasīt**.</span><span class="sxs-lookup"><span data-stu-id="46e58-271">Select **Select**.</span></span>
        5. <span data-ttu-id="46e58-272">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="46e58-272">Select **Add**.</span></span>
        6. <span data-ttu-id="46e58-273">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="46e58-273">Select **Save**.</span></span>

        | <span data-ttu-id="46e58-274">Pieteikums</span><span class="sxs-lookup"><span data-stu-id="46e58-274">Application</span></span>                                              | <span data-ttu-id="46e58-275">Tiesības</span><span class="sxs-lookup"><span data-stu-id="46e58-275">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="46e58-276">Parādāmais nosaukums jaunajā izveidotajā pieteikumā</span><span class="sxs-lookup"><span data-stu-id="46e58-276">The display name of the new application that you created</span></span> | <span data-ttu-id="46e58-277">Iegūt, saraksts</span><span class="sxs-lookup"><span data-stu-id="46e58-277">Get, List</span></span>   |
        | <span data-ttu-id="46e58-278">**Microsoft Dynamics ERP apakšpakalpojumi**</span><span class="sxs-lookup"><span data-stu-id="46e58-278">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="46e58-279">Iegūt, saraksts</span><span class="sxs-lookup"><span data-stu-id="46e58-279">Get, List</span></span>   |

6. <span data-ttu-id="46e58-280">Piešķiriet lomas, lai piekļūtu krātuves kontam.</span><span class="sxs-lookup"><span data-stu-id="46e58-280">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="46e58-281">[Azure portālā](https://portal.azure.com) atveriet iepriekš izveidoto krātuves kontu.</span><span class="sxs-lookup"><span data-stu-id="46e58-281">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="46e58-282">Atlasiet **Piekļuves kontrole (IAM)** un pēc tam atlasiet **Lomu piešķires**.</span><span class="sxs-lookup"><span data-stu-id="46e58-282">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="46e58-283">Atlasiet **Pievienot, pievienot lomas piešķiri**.</span><span class="sxs-lookup"><span data-stu-id="46e58-283">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="46e58-284">Katram pieteikumam tālāk esošajā tabulā veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="46e58-284">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="46e58-285">Atlasiet lomu no tālāk redzamās tabulas.</span><span class="sxs-lookup"><span data-stu-id="46e58-285">Select the role from the following table.</span></span>
        2. <span data-ttu-id="46e58-286">Atstājiet lauku **Piešķirt piekļuvi** iestatītu uz **Azure AD lietotājs, grupa vai pakalpojuma vadītājs**.</span><span class="sxs-lookup"><span data-stu-id="46e58-286">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="46e58-287">Laukā **Atlasīt** ievadiet pieteikumu no tālāk redzamās tabulas.</span><span class="sxs-lookup"><span data-stu-id="46e58-287">In the **Select** field, enter the application from the following table.</span></span>
        4. <span data-ttu-id="46e58-288">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="46e58-288">Select **Save**.</span></span>

        | <span data-ttu-id="46e58-289">Pieteikums</span><span class="sxs-lookup"><span data-stu-id="46e58-289">Application</span></span>                                              | <span data-ttu-id="46e58-290">Loma</span><span class="sxs-lookup"><span data-stu-id="46e58-290">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="46e58-291">Parādāmais nosaukums jaunajā izveidotajā pieteikumā</span><span class="sxs-lookup"><span data-stu-id="46e58-291">The display name of the new application that you created</span></span> | <span data-ttu-id="46e58-292">Īpašnieks</span><span class="sxs-lookup"><span data-stu-id="46e58-292">Owner</span></span>                       |
        | <span data-ttu-id="46e58-293">Parādāmais nosaukums jaunajā izveidotajā pieteikumā</span><span class="sxs-lookup"><span data-stu-id="46e58-293">The display name of the new application that you created</span></span> | <span data-ttu-id="46e58-294">Līdzstrādnieks</span><span class="sxs-lookup"><span data-stu-id="46e58-294">Contributor</span></span>                 |
        | <span data-ttu-id="46e58-295">Parādāmais nosaukums jaunajā izveidotajā pieteikumā</span><span class="sxs-lookup"><span data-stu-id="46e58-295">The display name of the new application that you created</span></span> | <span data-ttu-id="46e58-296">Krātuves konta līdzstrādnieks</span><span class="sxs-lookup"><span data-stu-id="46e58-296">Storage Account Contributor</span></span> |
        | <span data-ttu-id="46e58-297">Parādāmais nosaukums jaunajā izveidotajā pieteikumā</span><span class="sxs-lookup"><span data-stu-id="46e58-297">The display name of the new application that you created</span></span> | <span data-ttu-id="46e58-298">Krātuves BLOB datu īpašnieks</span><span class="sxs-lookup"><span data-stu-id="46e58-298">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="46e58-299">**AI Builder autorizācijas pakalpojums**</span><span class="sxs-lookup"><span data-stu-id="46e58-299">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="46e58-300">Krātuves BLOB datu lasītājs</span><span class="sxs-lookup"><span data-stu-id="46e58-300">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="46e58-301">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="46e58-301">Azure CLI</span></span>](#tab/azure-azure-cli)

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

## <a name="configure-the-entity-store"></a><span data-ttu-id="46e58-302">Elementu krātuves konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="46e58-302">Configure the entity store</span></span>

<span data-ttu-id="46e58-303">Izpildiet tālāk norādītās darbības, lai iestatītu Finanšu vides elementu krātuvi.</span><span class="sxs-lookup"><span data-stu-id="46e58-303">Follow these steps to set up the entity store in your Finance environment.</span></span>

1. <span data-ttu-id="46e58-304">Dodieties uz **Sistēmas administrēšana \> Iestatījumi \> Sistēmas parametri \> Datu savienojumi**.</span><span class="sxs-lookup"><span data-stu-id="46e58-304">Go to **System administration \> Setup \> System parameters \> Data connections**.</span></span>
2. <span data-ttu-id="46e58-305">Iestatiet opciju **Iespējot Data Lake integrāciju** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="46e58-305">Set the **Enable Data Lake integration** option to **Yes**.</span></span>
3. <span data-ttu-id="46e58-306">Iestatiet tālāk norādītos Galvenās akreditācijas datu glabātavas laukus.</span><span class="sxs-lookup"><span data-stu-id="46e58-306">Set the following Key Vault fields:</span></span>

    - <span data-ttu-id="46e58-307">**Pieteikuma (klienta) ID** — ievadiet iepriekš izveidoto pieteikuma klienta ID.</span><span class="sxs-lookup"><span data-stu-id="46e58-307">**Application (client) ID** – Enter the application client ID that you created earlier.</span></span>
    - <span data-ttu-id="46e58-308">**Pieteikuma noslēpums** — ievadiet noslēpumu, ko saglabājāt iepriekš izveidotajam pieteikumam.</span><span class="sxs-lookup"><span data-stu-id="46e58-308">**Application Secret** – Enter the secret that you saved for the application that you created earlier.</span></span>
    - <span data-ttu-id="46e58-309">**DNS nosaukums** — varat atrast domēna nosaukuma sistēmas (DNS) nosaukumu iepriekš izveidotā pieteikuma detalizētas informācijas lapā.</span><span class="sxs-lookup"><span data-stu-id="46e58-309">**DNS name** – You can find the Domain Name System (DNS) name on the application details page for the application that you created earlier.</span></span>
    - <span data-ttu-id="46e58-310">**Noslēpuma nosaukums** — ievadiet **krātuve-konts-savienojums-virkne**.</span><span class="sxs-lookup"><span data-stu-id="46e58-310">**Secret name** – Enter **storage-account-connection-string**.</span></span>

## <a name="configure-the-data-lake"></a><span data-ttu-id="46e58-311">Data Lake konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="46e58-311">Configure the data lake</span></span>

<span data-ttu-id="46e58-312">Veiciet tālāk norādītās darbības, lai izmantotu LCS, lai pievienotu videi Azure Data Lake pievienojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="46e58-312">Follow these steps to use LCS to add the Azure Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="46e58-313">Pierakstieties LCS un pēc tam pie vides nosaukuma lapas labajā pusē atlasiet **Pilna informācija**.</span><span class="sxs-lookup"><span data-stu-id="46e58-313">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="46e58-314">Sadaļā **Vides pievienojumprogrammas** atlasiet **Instalēt jaunu pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="46e58-314">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="46e58-315">Atlasiet pievienojumprogrammu **Eksportēt uz Data Lake**.</span><span class="sxs-lookup"><span data-stu-id="46e58-315">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="46e58-316">Ievadiet tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="46e58-316">Enter the following values.</span></span>

    | <span data-ttu-id="46e58-317">Vērtība</span><span class="sxs-lookup"><span data-stu-id="46e58-317">Value</span></span>                                                              | <span data-ttu-id="46e58-318">Apraksts</span><span class="sxs-lookup"><span data-stu-id="46e58-318">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="46e58-319">Nomnieka ID Azure abonementam, kur atrodas Galvenās akreditācijas datu glabātava</span><span class="sxs-lookup"><span data-stu-id="46e58-319">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="46e58-320">Nomnieka ID, kur atrodas krātuves konts, pieteikumi un galvenās akreditācijas datu glabātavas.</span><span class="sxs-lookup"><span data-stu-id="46e58-320">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="46e58-321">Lai atrastu šo vērtību, atveriet [Azure portālu](https://portal.azure.com), dodieties uz **Azure Active Directory** un kopējiet vērtību **Nomnieka ID**.</span><span class="sxs-lookup"><span data-stu-id="46e58-321">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="46e58-322">Norādiet sava Key Vault DNS nosaukumu</span><span class="sxs-lookup"><span data-stu-id="46e58-322">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="46e58-323">Galvenās akreditācijas datu glabātavas DNS nosaukums, piemēram, `https://customkeyvault.vault.azure.net/`.</span><span class="sxs-lookup"><span data-stu-id="46e58-323">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> <span data-ttu-id="46e58-324">(Šī vērtība atbilst DNS nosaukumam, kas tiek izmantots elementa krātuvē.)</span><span class="sxs-lookup"><span data-stu-id="46e58-324">(This value matches the DNS name that is used in the entity store.)</span></span> |
    | <span data-ttu-id="46e58-325">Norādiet noslēpumu, kas satur krātuves konta nosaukumu</span><span class="sxs-lookup"><span data-stu-id="46e58-325">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="46e58-326">**storage-account-name**</span><span class="sxs-lookup"><span data-stu-id="46e58-326">**storage-account-name**</span></span> |
    | <span data-ttu-id="46e58-327">Pieteikuma ID noslēpuma nosaukums, kas jāizmanto, lai piekļūtu Data Lake</span><span class="sxs-lookup"><span data-stu-id="46e58-327">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="46e58-328">**app-id**</span><span class="sxs-lookup"><span data-stu-id="46e58-328">**app-id**</span></span> |
    | <span data-ttu-id="46e58-329">Noslēpuma nosaukums, kas jāizmanto ar pieteikuma ID</span><span class="sxs-lookup"><span data-stu-id="46e58-329">Secret name to be used with App ID</span></span>                                 | <span data-ttu-id="46e58-330">**app-secret**</span><span class="sxs-lookup"><span data-stu-id="46e58-330">**app-secret**</span></span> |

5. <span data-ttu-id="46e58-331">Piekrītiet nosacījumiem un atlasiet **Instalēt**.</span><span class="sxs-lookup"><span data-stu-id="46e58-331">Agree to the terms, and select **Install**.</span></span>

<span data-ttu-id="46e58-332">Pievienojumprogramma tiks instalēta dažu minūšu laikā.</span><span class="sxs-lookup"><span data-stu-id="46e58-332">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-ai-builder"></a><span data-ttu-id="46e58-333">AI Builder konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="46e58-333">Configure AI Builder</span></span>

1. <span data-ttu-id="46e58-334">Pierakstieties LCS un atveriet lapu **Detalizēta informācija par vidi**.</span><span class="sxs-lookup"><span data-stu-id="46e58-334">Sign in to LCS, and open the **Environment details** page.</span></span>
2. <span data-ttu-id="46e58-335">Ritiniet līdz sadaļai **Vides pievienojumprogrammas**.</span><span class="sxs-lookup"><span data-stu-id="46e58-335">Scroll to the **Environment add-ins** section.</span></span> <span data-ttu-id="46e58-336">Ir jābūt redzamām pievienojumprogrammām, kas jau ir instalētas šajā vidē.</span><span class="sxs-lookup"><span data-stu-id="46e58-336">You should see the add-ins that are already installed in this environment.</span></span> <span data-ttu-id="46e58-337">Ja pievienojumprogramma **Eksportēt uz Data Lake** nav to vidū, konfigurējiet šo pievienojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="46e58-337">If the **Export to Data Lake** add-in isn't among them, configure this add-in.</span></span>
3. <span data-ttu-id="46e58-338">Atlasiet pievienojumprogrammu **Iegūt ieskatus**.</span><span class="sxs-lookup"><span data-stu-id="46e58-338">Select the **Get insights** add-in.</span></span>
4. <span data-ttu-id="46e58-339">Pievienojumprogrammas detalizētās informācijas lapā **Iegūt ieskatus** ievadiet tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="46e58-339">On the **Get insights** add-in details page, enter the following values.</span></span>

    | <span data-ttu-id="46e58-340">Vērtība</span><span class="sxs-lookup"><span data-stu-id="46e58-340">Value</span></span>                                                    | <span data-ttu-id="46e58-341">Apraksts</span><span class="sxs-lookup"><span data-stu-id="46e58-341">Description</span></span> |
    |----------------------------------------------------------|-------------|
    | <span data-ttu-id="46e58-342">CDS organizācijas URL</span><span class="sxs-lookup"><span data-stu-id="46e58-342">CDS Organization URL</span></span>                                     | <span data-ttu-id="46e58-343">Dataverse organizācijas URL Dataverse instancē.</span><span class="sxs-lookup"><span data-stu-id="46e58-343">The Dataverse organization URL of the Dataverse instance.</span></span> <span data-ttu-id="46e58-344">Lai atrastu šo vērtību, atveriet [Power Apps portālu](https://make.powerapps.com), atlasiet pogu **Iestatījumi** (zobrata simbols) augšējā labajā stūrī, atlasiet **Papildu iestatījumi** un kopējiet URL.</span><span class="sxs-lookup"><span data-stu-id="46e58-344">To find this value, open the [Power Apps portal](https://make.powerapps.com), select the **Settings** button (gear symbol) in the upper-right upper corner, select **Advanced settings**, and copy the URL.</span></span> <span data-ttu-id="46e58-345">(URL beidzas ar "dynamics.com.")</span><span class="sxs-lookup"><span data-stu-id="46e58-345">(The URL ends with "dynamics.com.")</span></span> |
    | <span data-ttu-id="46e58-346">CDS org. ID</span><span class="sxs-lookup"><span data-stu-id="46e58-346">CDS Org ID</span></span>                                               | <span data-ttu-id="46e58-347">Dataverse instances vides ID.</span><span class="sxs-lookup"><span data-stu-id="46e58-347">The environment ID of the Dataverse instance.</span></span> <span data-ttu-id="46e58-348">Lai atrastu šo vērtību, atveriet [Power Apps portālu](https://make.powerapps.com), atlasiet pogu **Iestatījumi** (zobrata simbols) augšējā labajā stūrī, atlasiet **Pielāgojumi \> Izstrādātāja resursi \> Instances atsauces informācija** un kopējiet vērtību **ID**.</span><span class="sxs-lookup"><span data-stu-id="46e58-348">To find this value, open the [Power Apps portal](https://make.powerapps.com), select the **Settings** button (gear symbol) in the upper-right upper corner, select **Customizations \> Developer resources \> Instance Reference Information**, and copy the **ID** value.</span></span> |
    | <span data-ttu-id="46e58-349">CDS nomnieka ID (direktorija ID no AAD)</span><span class="sxs-lookup"><span data-stu-id="46e58-349">CDS Tenant ID (Directory ID from AAD)</span></span>               | <span data-ttu-id="46e58-350">Dataverse instances nomnieka ID.</span><span class="sxs-lookup"><span data-stu-id="46e58-350">The tenant ID of the Dataverse instance.</span></span> <span data-ttu-id="46e58-351">Lai atrastu šo vērtību, atveriet [Azure portālu](https://portal.azure.com), dodieties uz **Azure Active Directory** un kopējiet vērtību **Nomnieka ID**.</span><span class="sxs-lookup"><span data-stu-id="46e58-351">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="46e58-352">Norādiet tā lietotāja objekta ID, kam ir sistēmas administratora loma</span><span class="sxs-lookup"><span data-stu-id="46e58-352">Provide user object ID who has system administrator role</span></span> | <span data-ttu-id="46e58-353">Azure AD lietotāja objekta ID lietotājam Dataverse.</span><span class="sxs-lookup"><span data-stu-id="46e58-353">The Azure AD user object ID of the user in Dataverse.</span></span> <span data-ttu-id="46e58-354">Šim lietotājam jābūt Dataverse instances sistēmas administratoram.</span><span class="sxs-lookup"><span data-stu-id="46e58-354">This user must be a system administrator of the Dataverse instance.</span></span> <span data-ttu-id="46e58-355">Lai atrastu šo vērtību, atveriet [Azure portālu](https://portal.azure.com), dodieties uz **Azure Active Directory \> Lietotāji**, atlasiet lietotāju un pēc tam sekcijā **Identitāte** kopējiet vērtību **Objekta ID**.</span><span class="sxs-lookup"><span data-stu-id="46e58-355">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory \> Users**, select the user, and then, in the **Identity** section, copy the **Object ID** value.</span></span> |
    | <span data-ttu-id="46e58-356">Vai šī ir nomnieka noklusējuma CDS vide?</span><span class="sxs-lookup"><span data-stu-id="46e58-356">Is this the default CDS environment for the tenant?</span></span>      | <span data-ttu-id="46e58-357">Ja Dataverse instance bija pirmā izveidotā ražošanas instance, atzīmējiet šo izvēles rūtiņu.</span><span class="sxs-lookup"><span data-stu-id="46e58-357">If the Dataverse instance was the first production instance that was created, select this check box.</span></span> <span data-ttu-id="46e58-358">Ja Dataverse instance tika izveidota manuāli, izņemiet atzīmi no šīs izvēles rūtiņas.</span><span class="sxs-lookup"><span data-stu-id="46e58-358">If the Dataverse instance was manually created, clear this check box.</span></span> |

## <a name="feedback-and-support"></a><span data-ttu-id="46e58-359">Atsauksmes un atbalsts</span><span class="sxs-lookup"><span data-stu-id="46e58-359">Feedback and support</span></span>

<span data-ttu-id="46e58-360">Lūdzu, sūtiet e-pastu [klientu maksājumu ieskatiem (priekšskatījums)](mailto:fiap@microsoft.com), ja vēlaties sniegt atsauksmes vai ir nepieciešams atbalsts.</span><span class="sxs-lookup"><span data-stu-id="46e58-360">Please send an email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in providing feedback or need support.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="46e58-361">Paziņojums par konfidencialitāti</span><span class="sxs-lookup"><span data-stu-id="46e58-361">Privacy notice</span></span>

<span data-ttu-id="46e58-362">Priekšskatījumiem (1) var tikt izmantots mazāk konfidencialitātes un drošības pasākumu nekā pakalpojumam Dynamics 365 Finance and Operations, (2) tie nav ietverti pakalpojuma līmeņa līgumā par šo pakalpojumu, (3) tos nedrīkst izmantot personas datu vai citu tādu datu apstrādei, uz kuriem attiecas juridiskās vai normatīvās prasības, un (4) tiem tiek nodrošināts ierobežots atbalsts.</span><span class="sxs-lookup"><span data-stu-id="46e58-362">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
