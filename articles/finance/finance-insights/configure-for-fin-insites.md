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
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 38cdeb9110691e594b4b90fc5bc79e369c9f4707
ms.sourcegitcommit: 1cfd6e0c808341b0f5bafbde7d04b0255b27352f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/02/2020
ms.locfileid: "4664094"
---
# <a name="configuration-for-finance-insights-preview"></a><span data-ttu-id="8605e-103">Konfigurācija Finanšu ieskatiem (priekšskatījums)</span><span class="sxs-lookup"><span data-stu-id="8605e-103">Configuration for Finance insights (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="8605e-104">Finanšu ieskati apvieno Microsoft Dynamics 365 Finance funkcionalitāti ar Common Data Service, Azure un AI Builder, lai nodrošinātu jaudīgus prognozēšanas rīkus jūsu organizācijai.</span><span class="sxs-lookup"><span data-stu-id="8605e-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Common Data Service, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="8605e-105">Šajā tēmā ir izskaidrotas konfigurācijas darbības, kas ļaus jūsu sistēmai izmantot iespējas, kas pieejamas Finanšu ieskatos.</span><span class="sxs-lookup"><span data-stu-id="8605e-105">This topic explains the configuration steps that will enable your system to use the capabilities that are available in Finance insights.</span></span>

## <a name="deploy-dynamics-365-finance"></a><span data-ttu-id="8605e-106">Dynamics 365 Finance izvietošana</span><span class="sxs-lookup"><span data-stu-id="8605e-106">Deploy Dynamics 365 Finance</span></span>

<span data-ttu-id="8605e-107">Izvietojiet vides, veicot tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="8605e-107">Deploy the environments by following these steps.</span></span>

1. <span data-ttu-id="8605e-108">Microsoft Dynamics Lifecycle Services (LCS) izveidojiet vai atjauniniet Dynamics 365 Finance vidi.</span><span class="sxs-lookup"><span data-stu-id="8605e-108">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Dynamics 365 Finance environment.</span></span> <span data-ttu-id="8605e-109">Videi nepieciešama programmas versija 10.0.11/ platformas atjauninājums 35 vai jaunāka versija.</span><span class="sxs-lookup"><span data-stu-id="8605e-109">The environment requires app version 10.0.11/Platform update 35 or later.</span></span>
2. <span data-ttu-id="8605e-110">Videi ir jābūt augstas pieejamības (AP) videi smilškastē.</span><span class="sxs-lookup"><span data-stu-id="8605e-110">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="8605e-111">(Šis vides veids ir pazīstams arī kā 2. līmeņa vide.) Lai iegūtu papildu informāciju, skatiet [Vides plānošana](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="8605e-111">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="8605e-112">Ja izmantojat Contoso demonstrācijas datus, būs nepieciešami papildu parauga dati, lai izmantotu Debitora maksājumu prognozes, Skaidras naudas plūsmas prognozes un Budžeta prognožu līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="8605e-112">If you're using Contoso demo data, you will require additional sample data to use the Customer payment predictions, Cash flow forecasts, and Budget forecasts features.</span></span> 

## <a name="configure-common-data-service"></a><span data-ttu-id="8605e-113">Common Data Service konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="8605e-113">Configure Common Data Service</span></span>

<span data-ttu-id="8605e-114">Varat pabeigt manuālās konfigurācijas darbības, kas norādītas tālāk, vai varat paātrināt konfigurācijas procesu, izmantojot nodrošināto Windows PowerShell skriptu.</span><span class="sxs-lookup"><span data-stu-id="8605e-114">You can complete the manual configuration steps that follow, or you can speed up the configuration process by using the Windows PowerShell script that is provided.</span></span> <span data-ttu-id="8605e-115">Kad PowerShell skripts ir beidzis darboties, tas sniegs vērtības, ko izmantot, lai konfigurētu Finanšu ieskatus.</span><span class="sxs-lookup"><span data-stu-id="8605e-115">When the PowerShell script has finished running, it will give you values to use to configure Finance insights.</span></span> 

> [!NOTE]
> <span data-ttu-id="8605e-116">Datorā atveriet PowerShell, lai palaistu skriptu.</span><span class="sxs-lookup"><span data-stu-id="8605e-116">Open PowerShell on your PC to run the script.</span></span> <span data-ttu-id="8605e-117">Iespējams, būs nepieciešama PowerShell versija 5.</span><span class="sxs-lookup"><span data-stu-id="8605e-117">You may need PowerShell version 5.</span></span> <span data-ttu-id="8605e-118">Var nedarboties Microsoft Azure CLI "Izmēģini to" opcija.</span><span class="sxs-lookup"><span data-stu-id="8605e-118">The Microsoft Azure CLI "Try it" option may not work.</span></span>

# <a name="manual-configuration-steps"></a>[<span data-ttu-id="8605e-119">Manuālās konfigurācijas darbības</span><span class="sxs-lookup"><span data-stu-id="8605e-119">Manual configuration steps</span></span>](#tab/configuration-steps)

1. <span data-ttu-id="8605e-120">Atveriet [Power Platform administrēšanas centru](https://admin.powerplatform.microsoft.com/) un veiciet tālāk norādītās darbības, lai izveidotu jaunu Common Data Service vidi tajā pašā Active Directory nomniekā.</span><span class="sxs-lookup"><span data-stu-id="8605e-120">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), and follow these steps to create a new Common Data Service environment in the same Active Directory tenant:</span></span>

    1. <span data-ttu-id="8605e-121">Atveriet lapu **Vides**.</span><span class="sxs-lookup"><span data-stu-id="8605e-121">Open the **Environments** page.</span></span>

        <span data-ttu-id="8605e-122">[![Lapa Vides](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span><span class="sxs-lookup"><span data-stu-id="8605e-122">[![Environments page](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span></span>

    2. <span data-ttu-id="8605e-123">Atlasiet **Jauna vide**.</span><span class="sxs-lookup"><span data-stu-id="8605e-123">Select **New environment**.</span></span>
    3. <span data-ttu-id="8605e-124">Laukā **Veids** atlasiet **Smilškaste**.</span><span class="sxs-lookup"><span data-stu-id="8605e-124">In the **Type** field, select **Sandbox**.</span></span>
    4. <span data-ttu-id="8605e-125">Iestatiet opciju **Izveidot datubāzi** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="8605e-125">Set the **Create Database** option to **Yes**.</span></span>
    5. <span data-ttu-id="8605e-126">Atlasiet **Nākamais**.</span><span class="sxs-lookup"><span data-stu-id="8605e-126">Select **Next**.</span></span>
    6. <span data-ttu-id="8605e-127">Atlasiet jūsu organizācijas valodu un valūtu.</span><span class="sxs-lookup"><span data-stu-id="8605e-127">Select the language and currency for your organization.</span></span>
    7. <span data-ttu-id="8605e-128">Pieņemiet noklusējuma vērtības pārējiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="8605e-128">Accept the default values for the other fields.</span></span>
    8. <span data-ttu-id="8605e-129">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="8605e-129">Select **Save**.</span></span>
    9. <span data-ttu-id="8605e-130">Atsvaidziniet lapu **Vides**.</span><span class="sxs-lookup"><span data-stu-id="8605e-130">Refresh the **Environments** page.</span></span>
    10. <span data-ttu-id="8605e-131">Uzgaidiet, kamēr lauka **Stāvoklis** vērtība tiek atjaunināta uz **Gatavs**.</span><span class="sxs-lookup"><span data-stu-id="8605e-131">Wait until the value of the **State** field is updated to **Ready**.</span></span>
    11. <span data-ttu-id="8605e-132">Pierakstiet Common Data Service organizācijas ID.</span><span class="sxs-lookup"><span data-stu-id="8605e-132">Make a note of the Common Data Service organization ID.</span></span>
    12. <span data-ttu-id="8605e-133">Atlasiet vidi un pēc atlasiet **Iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="8605e-133">Select the environment, and then select **Settings**.</span></span>
    13. <span data-ttu-id="8605e-134">Atlasiet **Resursi \> Visi mantotie iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="8605e-134">Select **Resources \> All Legacy Settings**.</span></span>
    14. <span data-ttu-id="8605e-135">Augšējā navigācijas joslā atlasiet **Iestatījumi** un pēc tam atlasiet **Pielāgojumi**.</span><span class="sxs-lookup"><span data-stu-id="8605e-135">On the top navigation bar, select **Settings**, and then select **Customizations**.</span></span>
    15. <span data-ttu-id="8605e-136">Atlasiet **Izstrādātāja resursi**.</span><span class="sxs-lookup"><span data-stu-id="8605e-136">Select **Developer Resources**.</span></span>
    16. <span data-ttu-id="8605e-137">Iestatiet laukā **Instances atsauces informācijas ID** Common Data Service organizācijas ID vērtību, ko pierakstījāt iepriekš.</span><span class="sxs-lookup"><span data-stu-id="8605e-137">Set the **Instance Reference Information ID** field to the Common Data Service organization ID value that you made a note of earlier.</span></span>
    17. <span data-ttu-id="8605e-138">Pierakstiet pārlūkprogrammas adreses joslā esošo Common Data Service organizācijas URL.</span><span class="sxs-lookup"><span data-stu-id="8605e-138">In the browser's address bar, make a note of the URL for the Common Data Service organization.</span></span> <span data-ttu-id="8605e-139">Piemēram, URL varētu būt `https://org42b2b3d3.crm.dynamics.com`.</span><span class="sxs-lookup"><span data-stu-id="8605e-139">For example, the URL might be `https://org42b2b3d3.crm.dynamics.com`.</span></span>

2. <span data-ttu-id="8605e-140">Ja plānojat izmantot Skaidras naudas plūsmas prognožu vai Budžeta prognožu līdzekli, veiciet tālāk norādītās darbības, lai atjauninātu jūsu organizācijas anotāciju ierobežojumu līdz vismaz 50 megabaitiem (MB).</span><span class="sxs-lookup"><span data-stu-id="8605e-140">If you plan to use the Cash flow forecasts or Budget forecasts feature, follow these steps to update the annotation limit for your organization to at least 50 megabytes (MB):</span></span>

    1. <span data-ttu-id="8605e-141">Atveriet [Power Apps portālu](https://make.powerapps.com).</span><span class="sxs-lookup"><span data-stu-id="8605e-141">Open the [Power Apps portal](https://make.powerapps.com).</span></span>
    2. <span data-ttu-id="8605e-142">Atlasiet tikko izveidoto vidi un pēc tam atlasiet **Papildu iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="8605e-142">Select the environment that you just created, and then select **Advanced settings**.</span></span>
    3. <span data-ttu-id="8605e-143">Atlasiet **Iestatījumi \> E-pasta konfigurācija**.</span><span class="sxs-lookup"><span data-stu-id="8605e-143">Select **Settings \> Email Configuration**.</span></span>
    4. <span data-ttu-id="8605e-144">Mainiet lauka **Maksimālais faila izmērs** vērtību uz **51 200**.</span><span class="sxs-lookup"><span data-stu-id="8605e-144">Change the value of the **Maximum file size** field to **51,200**.</span></span> <span data-ttu-id="8605e-145">(Šī vērtība ir izteikta kilobaitos \[KB\].)</span><span class="sxs-lookup"><span data-stu-id="8605e-145">(The value is expressed in kilobytes \[KB\].)</span></span>
    5. <span data-ttu-id="8605e-146">Atlasiet **Labi**, lai saglabātu izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="8605e-146">Select **OK** to save your changes.</span></span>

# <a name="windows-powershell-configuration-script"></a>[<span data-ttu-id="8605e-147">Windows PowerShell konfigurācijas skripts</span><span class="sxs-lookup"><span data-stu-id="8605e-147">Windows PowerShell configuration script</span></span>](#tab/powershell-configuration-script)

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

## <a name="configure-the-azure-setup"></a><span data-ttu-id="8605e-148">Azure iestatījumu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="8605e-148">Configure the Azure setup</span></span>

### <a name="enter-the-common-data-service-directory-id-and-the-users-azure-ad-object-id"></a><span data-ttu-id="8605e-149">Ievadiet Common Data Service direktorijas ID un lietotāja Azure AD objekta ID</span><span class="sxs-lookup"><span data-stu-id="8605e-149">Enter the Common Data Service directory ID and the user's Azure AD object ID</span></span>

1. <span data-ttu-id="8605e-150">Ievadiet Common Data Service direktorijas ID.</span><span class="sxs-lookup"><span data-stu-id="8605e-150">Enter the Common Data Service directory ID:</span></span>

    1. <span data-ttu-id="8605e-151">Atveriet [Azure portālu](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="8605e-151">Open the [Azure portal](https://portal.azure.com).</span></span>
    2. <span data-ttu-id="8605e-152">Pierakstieties, izmantojot lietotāja ID, kas tika izmantots Common Data Service vides izveidei.</span><span class="sxs-lookup"><span data-stu-id="8605e-152">Sign in by using the user ID that was used to create the Common Data Service environment.</span></span>
    3. <span data-ttu-id="8605e-153">Dodieties uz **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="8605e-153">Go to **Azure Active Directory**.</span></span>
    4. <span data-ttu-id="8605e-154">Kopējiet **Nomnieka ID** vērtību.</span><span class="sxs-lookup"><span data-stu-id="8605e-154">Copy the **Tenant ID** value.</span></span>

2. <span data-ttu-id="8605e-155">Ievadiet lietotāja Azure Active Directory (Azure AD) objekta ID.</span><span class="sxs-lookup"><span data-stu-id="8605e-155">Enter the user's Azure Active Directory (Azure AD) object ID:</span></span>

    1. <span data-ttu-id="8605e-156">[Azure portālā](https://portal.azure.com) dodieties uz **Lietotāji** un uzmeklējiet lietotāju, izmantojot e-pasta adresi.</span><span class="sxs-lookup"><span data-stu-id="8605e-156">In the [Azure portal](https://portal.azure.com), go to **Users**, and search for the user by email address.</span></span>
    2. <span data-ttu-id="8605e-157">Atlasiet lietotāja vārdu.</span><span class="sxs-lookup"><span data-stu-id="8605e-157">Select the user's name.</span></span>
    3. <span data-ttu-id="8605e-158">Kopējiet **Objekta ID** vērtību.</span><span class="sxs-lookup"><span data-stu-id="8605e-158">Copy the **Object ID** value.</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="8605e-159">Izmantojiet Azure Cloud Shell, lai iestatītu Finanšu ieskatu Data Lake resursus</span><span class="sxs-lookup"><span data-stu-id="8605e-159">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="8605e-160">Windows PowerShell skripta izmantošana</span><span class="sxs-lookup"><span data-stu-id="8605e-160">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="8605e-161">Windows PowerShell skripts tiek nodrošināts, lai varētu viegli iestatīt Azure resursus, kas aprakstīti sadaļā [Eksporta konfigurēšana uz Azure Data Lake](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/configure-export-data-lake).</span><span class="sxs-lookup"><span data-stu-id="8605e-161">A Windows PowerShell script has been provided, so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/configure-export-data-lake).</span></span> <span data-ttu-id="8605e-162">Ja vēlaties veikt manuālu iestatīšanu, izlaidiet šo procedūru un turpiniet ar procedūru sadaļā [Manuālā iestatīšana](#manual-setup).</span><span class="sxs-lookup"><span data-stu-id="8605e-162">If you prefer to do manual setup, skip this procedure, and continue with the procedure in the [Manual setup](#manual-setup) section.</span></span>

> [!NOTE]
> <span data-ttu-id="8605e-163">Izpildiet tālāk norādītās darbības, lai palaistu PowerShell skriptu.</span><span class="sxs-lookup"><span data-stu-id="8605e-163">Follow the steps below to run the PowerShell script.</span></span> <span data-ttu-id="8605e-164">Azure CLI opcija "Izmēģiniet to" vai skripta palaišana datorā, iespējams, nedarbosies.</span><span class="sxs-lookup"><span data-stu-id="8605e-164">The Azure CLI "Try it" option, or running the script on your PC may not work.</span></span>

<span data-ttu-id="8605e-165">Izpildiet tālāk norādītās darbības, lai konfigurētu Azure, izmantojot Windows PowerShell skriptu.</span><span class="sxs-lookup"><span data-stu-id="8605e-165">Follow these steps to configure Azure by using the Windows PowerShell script.</span></span> <span data-ttu-id="8605e-166">Jums ir jābūt tiesībām izveidot Azure resursu grupu, Azure resursus un Azure AD pieteikumu.</span><span class="sxs-lookup"><span data-stu-id="8605e-166">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="8605e-167">Lai iegūtu informāciju par nepieciešamajām atļaujām, skatiet [Azure AD atļauju pārbaude](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="8605e-167">For information about the required permissions, see [Check Azure AD permissions](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="8605e-168">[Azure portālā](https://portal.azure.com) dodieties uz savu mērķa Azure abonementu.</span><span class="sxs-lookup"><span data-stu-id="8605e-168">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span> <span data-ttu-id="8605e-169">Atlasiet pogu **Mākoņa čaula**, kas atrodas pa labi no lauka **Meklēt**.</span><span class="sxs-lookup"><span data-stu-id="8605e-169">Select the **Cloud Shell** button to the right of the **Search** field.</span></span>
2. <span data-ttu-id="8605e-170">Atlasiet **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="8605e-170">Select **PowerShell**.</span></span>
3. <span data-ttu-id="8605e-171">Izveidojiet krātuvi, ja saņemat aicinājumu to darīt.</span><span class="sxs-lookup"><span data-stu-id="8605e-171">Create storage, if you're prompted to do so.</span></span> <span data-ttu-id="8605e-172">Pēc tam augšupielādējiet Windows PowerShell skriptu sesijā.</span><span class="sxs-lookup"><span data-stu-id="8605e-172">Then upload the Windows PowerShell script to the session.</span></span>
4. <span data-ttu-id="8605e-173">Palaidiet skriptu.</span><span class="sxs-lookup"><span data-stu-id="8605e-173">Run the script.</span></span>
5. <span data-ttu-id="8605e-174">Sekojiet uzvednēm, lai palaistu skriptu.</span><span class="sxs-lookup"><span data-stu-id="8605e-174">Follow the prompts to run the script.</span></span>
6. <span data-ttu-id="8605e-175">Izmantojiet skripta izvades informāciju, lai LCS instalētu pievienojumprogrammu **Eksportēt uz Data Lake**.</span><span class="sxs-lookup"><span data-stu-id="8605e-175">Use the information from the script output to install the **Export to Data Lake** add-in in LCS.</span></span>
7. <span data-ttu-id="8605e-176">Izmantojiet skripta izvades informāciju, lai iespējotu elementa krātuvi Finance lapā **Datu savienojumi** (**Sistēmas administrēšana \> Sistēmas parametri \> Datu savienojumi**).</span><span class="sxs-lookup"><span data-stu-id="8605e-176">Use the information from the script output to enable the entity store on the **Data connections** page in Finance (**System administration \> System parameters \> Data connections**).</span></span>

### <a name="manual-setup"></a><span data-ttu-id="8605e-177">Manuāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="8605e-177">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="8605e-178">Pieteikumu pievienošana Azure AD nomniekam</span><span class="sxs-lookup"><span data-stu-id="8605e-178">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="8605e-179">[Azure portālā](https://portal.azure.com) dodieties uz **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="8605e-179">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="8605e-180">Atlasiet **Pārvaldīt \> Uzņēmuma pieteikumi**.</span><span class="sxs-lookup"><span data-stu-id="8605e-180">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="8605e-181">Uzmeklējiet tālāk norādītos pieteikumus, izmantojot pieteikuma ID.</span><span class="sxs-lookup"><span data-stu-id="8605e-181">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="8605e-182">Pieteikums</span><span class="sxs-lookup"><span data-stu-id="8605e-182">Application</span></span>                              | <span data-ttu-id="8605e-183">Programmas ID</span><span class="sxs-lookup"><span data-stu-id="8605e-183">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="8605e-184">Microsoft Dynamics ERP apakšpakalpojumi</span><span class="sxs-lookup"><span data-stu-id="8605e-184">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="8605e-185">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="8605e-185">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="8605e-186">Microsoft Dynamics ERP apakšpakalpojumi CDS</span><span class="sxs-lookup"><span data-stu-id="8605e-186">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="8605e-187">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="8605e-187">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="8605e-188">AI Builder autorizācijas pakalpojums</span><span class="sxs-lookup"><span data-stu-id="8605e-188">AI Builder Authorization Service</span></span>         | <span data-ttu-id="8605e-189">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="8605e-189">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="8605e-190">Ja nevarat atrast nevienu no iepriekšējiem pieteikumiem, izmēģiniet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="8605e-190">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="8605e-191">Savā lokālajā datorā atlasiet izvēlni **Sākt** un uzmeklējiet **powershell**.</span><span class="sxs-lookup"><span data-stu-id="8605e-191">On your local machine, select the **Start** menu, and search for **powershell**.</span></span>
2. <span data-ttu-id="8605e-192">Atlasiet un turiet nospiestu (vai noklikšķiniet ar peles labo pogu) **Windows PowerShell** un pēc tam atlasiet **Palaist kā administratoram**.</span><span class="sxs-lookup"><span data-stu-id="8605e-192">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="8605e-193">Palaidiet tālāk norādīto komandu, lai instalētu **AzureAD** moduli.</span><span class="sxs-lookup"><span data-stu-id="8605e-193">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="8605e-194">Ja ir nepieciešams NuGet nodrošinātājs, lai turpinātu, atlasiet **Y**, lai to instalētu.</span><span class="sxs-lookup"><span data-stu-id="8605e-194">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="8605e-195">Ja parādās ziņojums "Neuzticams repozitorijs", atlasiet **Y**, lai turpinātu.</span><span class="sxs-lookup"><span data-stu-id="8605e-195">If an "Untrusted repository" message appears, select **Y** to continue.</span></span>
6. <span data-ttu-id="8605e-196">Katram pieteikumam, kas jāpievieno, palaidiet tālāk norādītās komandas, lai pievienotu pieteikumu Azure AD.</span><span class="sxs-lookup"><span data-stu-id="8605e-196">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="8605e-197">Kad saņemat aicinājumu, pierakstieties kā Azure AD administrators.</span><span class="sxs-lookup"><span data-stu-id="8605e-197">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="8605e-198">Azure resursu izveidošana</span><span class="sxs-lookup"><span data-stu-id="8605e-198">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="8605e-199">Pārliecinieties, ka izveidojat tālāk norādītos resursus tajā pašā Azure AD instancē kā Common Data Service vide.</span><span class="sxs-lookup"><span data-stu-id="8605e-199">Make sure that you create the following resources in the same Azure AD instance as the Common Data Service environment.</span></span> <span data-ttu-id="8605e-200">Nav iespējams izmantot resursus no citas Azure AD instances.</span><span class="sxs-lookup"><span data-stu-id="8605e-200">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="8605e-201">Izveidojiet jaunu krātuves kontu.</span><span class="sxs-lookup"><span data-stu-id="8605e-201">Create a new storage account:</span></span>

    1. <span data-ttu-id="8605e-202">[Azure portālā](https://portal.azure.com) izveidojiet krātuves kontu.</span><span class="sxs-lookup"><span data-stu-id="8605e-202">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="8605e-203">Dialoglodziņā **Izveidot krātuves kontu** iestatiet tālāk norādītos laukus.</span><span class="sxs-lookup"><span data-stu-id="8605e-203">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="8605e-204">**Atrašanās vieta** — atlasiet datu centru, kur atrodas jūsu vide.</span><span class="sxs-lookup"><span data-stu-id="8605e-204">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="8605e-205">**Veiktspēja** — ieteicams atlasīt **Standarta**.</span><span class="sxs-lookup"><span data-stu-id="8605e-205">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="8605e-206">**Konta veids** — jāatlasa **StorageV2**.</span><span class="sxs-lookup"><span data-stu-id="8605e-206">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="8605e-207">Dialoglodziņā **Papildu opcijas** opcijā **Data Lake Storage Gen2** atlasiet **Iespējot** līdzeklī **Hierarhiskās nosaukumvietas**.</span><span class="sxs-lookup"><span data-stu-id="8605e-207">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="8605e-208">Deaktivizējot šo līdzekli, nevarat patērēt datus, ko Finance and Operations programmas raksta, izmantojot tādus pakalpojumus kā Power BI datu plūsmas.</span><span class="sxs-lookup"><span data-stu-id="8605e-208">If you disable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="8605e-209">Atlasiet **Pārskatīt un izveidot**.</span><span class="sxs-lookup"><span data-stu-id="8605e-209">Select **Review and create**.</span></span> <span data-ttu-id="8605e-210">Kad izvietošana ir pabeigta, jaunais resurss tiks parādīts Azure portālā.</span><span class="sxs-lookup"><span data-stu-id="8605e-210">When the deployment is completed, the new resource will be shown in the Azure portal.</span></span>
    5. <span data-ttu-id="8605e-211">Dodieties uz izveidoto krātuves kontu.</span><span class="sxs-lookup"><span data-stu-id="8605e-211">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="8605e-212">Kreisās puses izvēlnē atlasiet **Piekļuves galvenie akreditācijas dati**.</span><span class="sxs-lookup"><span data-stu-id="8605e-212">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="8605e-213">Kopējiet un saglabājiet savienojuma virkni vai nu **Key1**, vai **Key2**.</span><span class="sxs-lookup"><span data-stu-id="8605e-213">Copy and save the connection string for either **Key1** or **Key2**.</span></span>
    8. <span data-ttu-id="8605e-214">Kopējiet un saglabājiet krātuves konta nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="8605e-214">Copy and save the storage account name.</span></span>

2. <span data-ttu-id="8605e-215">Izveidojiet jaunu galveno akreditācijas datu glabātavu.</span><span class="sxs-lookup"><span data-stu-id="8605e-215">Create a new key vault:</span></span>

    1. <span data-ttu-id="8605e-216">[Azure portālā](https://portal.azure.com) izveidojiet galveno akreditācijas datu glabātavu.</span><span class="sxs-lookup"><span data-stu-id="8605e-216">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="8605e-217">Dialoglodziņā **Izveidot galveno akreditācijas datu glabātavu** laukā **Novietojums** atlasiet datu centru, kur atrodas jūsu vide.</span><span class="sxs-lookup"><span data-stu-id="8605e-217">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="8605e-218">Pēc galvenās akreditācijas datu glabātavas izveides atlasiet to sarakstā un pēc tam atlasiet **Noslēpumi**.</span><span class="sxs-lookup"><span data-stu-id="8605e-218">After key vault is created, select it in the list, and then select **Secrets**.</span></span>
    4. <span data-ttu-id="8605e-219">Atlasiet **Ģenerēt/Importēt**.</span><span class="sxs-lookup"><span data-stu-id="8605e-219">Select **Generate/Import**.</span></span>
    5. <span data-ttu-id="8605e-220">Dialoglodziņā **Izveidot noslēpumu** laukā **Augšupielādes opcijas** atlasiet **Manuāli**.</span><span class="sxs-lookup"><span data-stu-id="8605e-220">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
    6. <span data-ttu-id="8605e-221">Ievadiet noslēpuma nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="8605e-221">Enter a name for the secret.</span></span> <span data-ttu-id="8605e-222">Pierakstiet nosaukumu, jo jums tas būs jānorāda vēlāk.</span><span class="sxs-lookup"><span data-stu-id="8605e-222">Make a note of the name, because you will have to provide it later.</span></span>
    7. <span data-ttu-id="8605e-223">Laukā **Vērtība** ievadiet savienojuma virkni, ko ieguvāt no krātuves konta iepriekšējā procedūrā.</span><span class="sxs-lookup"><span data-stu-id="8605e-223">In the **Value** field, enter the connection string that you obtained from the storage account in the previous procedure.</span></span>
    8. <span data-ttu-id="8605e-224">Atlasiet **Iespējots** un pēc tam atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="8605e-224">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="8605e-225">Noslēpums ir izveidots un pievienots Galveno akreditācijas datu glabātai.</span><span class="sxs-lookup"><span data-stu-id="8605e-225">The secret is created and added to Key Vault.</span></span>
    9. <span data-ttu-id="8605e-226">Dodieties uz **Galvenās akreditācijas datu glabātavas pārskatu** un pierakstiet DNS nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="8605e-226">Go to the **Key Vault Overview**, and make a note of the DNS name.</span></span>

3. <span data-ttu-id="8605e-227">Izveidojiet un reģistrējiet Azure AD pieteikumu.</span><span class="sxs-lookup"><span data-stu-id="8605e-227">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="8605e-228">[Azure portālā](https://portal.azure.com) dodieties uz **Azure Active Directory** un atlasiet **Pieteikumu reģistrācija**.</span><span class="sxs-lookup"><span data-stu-id="8605e-228">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="8605e-229">Atlasiet **Jauna pieteikuma reģistrācija** un iestatiet tālāk norādītos laukus.</span><span class="sxs-lookup"><span data-stu-id="8605e-229">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="8605e-230">**Nosaukums** — ievadiet pieteikuma nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="8605e-230">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="8605e-231">**Pieteikuma veids** — atlasiet **Web API**.</span><span class="sxs-lookup"><span data-stu-id="8605e-231">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="8605e-232">**Novirzīt URI iestatīšanu** — ievadiet savas Dynamics 365 instances URL, piemēram, `https://yourdynamicsinstance.dynamics.com/auth`.</span><span class="sxs-lookup"><span data-stu-id="8605e-232">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as, `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="8605e-233">Dodieties uz tikko izveidoto pieteikumu, kopējiet un saglabājiet tās **Pieteikuma (klienta) ID** vērtību.</span><span class="sxs-lookup"><span data-stu-id="8605e-233">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="8605e-234">Šī vērtība būs jānorāda vēlāk, kad iestatīsiet galveno akreditācijas datu glabātavu.</span><span class="sxs-lookup"><span data-stu-id="8605e-234">You will have to provide this value later, when you set up the key vault.</span></span>
    4. <span data-ttu-id="8605e-235">Dodieties uz **API atļaujas** un veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="8605e-235">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="8605e-236">Atlasiet **Pievienot atļauju**.</span><span class="sxs-lookup"><span data-stu-id="8605e-236">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="8605e-237">Atlasiet **Azure Galvenā akreditācijas datu glabātava**.</span><span class="sxs-lookup"><span data-stu-id="8605e-237">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="8605e-238">Pēc deleģēto atļauju atlases atlasiet **lietotājs\_personifikācija**.</span><span class="sxs-lookup"><span data-stu-id="8605e-238">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="8605e-239">Atlasiet **Pievienot atļaujas**.</span><span class="sxs-lookup"><span data-stu-id="8605e-239">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="8605e-240">Pieteikuma izvēlnē atlasiet **Sertifikāti \& noslēpumi** un pēc tam izpildiet tālāk norādītās darbības, lai izveidotu galvenās akreditācijas datu glabātavas noslēpumus.</span><span class="sxs-lookup"><span data-stu-id="8605e-240">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="8605e-241">Atlasiet **Jauns klienta noslēpums**.</span><span class="sxs-lookup"><span data-stu-id="8605e-241">Select **New client secret**.</span></span>
        2. <span data-ttu-id="8605e-242">Ievadiet nosaukumu laukā **Akreditācijas datu glabātavas apraksts**.</span><span class="sxs-lookup"><span data-stu-id="8605e-242">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="8605e-243">Atlasiet ilgumu un pēc tam atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="8605e-243">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="8605e-244">Noslēpums tiek ģenerēts laukā **Vērtība**.</span><span class="sxs-lookup"><span data-stu-id="8605e-244">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="8605e-245">Kopējiet un saglabājiet slepeno vērtību.</span><span class="sxs-lookup"><span data-stu-id="8605e-245">Copy and save the secret value.</span></span>

4. <span data-ttu-id="8605e-246">Izveidojiet Galvenās akreditācijas datu glabātavas noslēpumus.</span><span class="sxs-lookup"><span data-stu-id="8605e-246">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="8605e-247">Dodieties uz galveno akreditācijas datu glabātavu, ko izveidojāt iepriekš, un atlasiet **Noslēpumi**.</span><span class="sxs-lookup"><span data-stu-id="8605e-247">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="8605e-248">Katram noslēpuma nosaukumam tālāk esošajā tabulā veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="8605e-248">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="8605e-249">Atlasiet **Ģenerēt/Importēt**.</span><span class="sxs-lookup"><span data-stu-id="8605e-249">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="8605e-250">Dialoglodziņā **Izveidot noslēpumu** laukā **Augšupielādes opcijas** atlasiet **Manuāli**.</span><span class="sxs-lookup"><span data-stu-id="8605e-250">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="8605e-251">Izveidojiet noslēpuma nosaukumu un vērtību no tālāk redzamās tabulas.</span><span class="sxs-lookup"><span data-stu-id="8605e-251">Create the secret name and value from the following table.</span></span>
        4. <span data-ttu-id="8605e-252">Atlasiet **Iespējots** un pēc tam atlasiet **Izveidot**.</span><span class="sxs-lookup"><span data-stu-id="8605e-252">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="8605e-253">Noslēpums ir izveidots un pievienots Galveno akreditācijas datu glabātai.</span><span class="sxs-lookup"><span data-stu-id="8605e-253">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="8605e-254">Slepenais nosaukums</span><span class="sxs-lookup"><span data-stu-id="8605e-254">Secret name</span></span>                       | <span data-ttu-id="8605e-255">Noslēpuma vērtība</span><span class="sxs-lookup"><span data-stu-id="8605e-255">Secret value</span></span>                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | <span data-ttu-id="8605e-256">app-id</span><span class="sxs-lookup"><span data-stu-id="8605e-256">app-id</span></span>                            | <span data-ttu-id="8605e-257">Iepriekš izveidotā pieteikuma ID</span><span class="sxs-lookup"><span data-stu-id="8605e-257">The app ID of the application that you created earlier</span></span>                                      |
        | <span data-ttu-id="8605e-258">app-secret</span><span class="sxs-lookup"><span data-stu-id="8605e-258">app-secret</span></span>                        | <span data-ttu-id="8605e-259">Iepriekš saglabātais klienta noslēpums</span><span class="sxs-lookup"><span data-stu-id="8605e-259">The client secret that you saved earlier</span></span>                                                    |
        | <span data-ttu-id="8605e-260">storage-account-name</span><span class="sxs-lookup"><span data-stu-id="8605e-260">storage-account-name</span></span>              | <span data-ttu-id="8605e-261">Iepriekš izveidotā krātuves konta nosaukums, piemēram, **storageaccount1**</span><span class="sxs-lookup"><span data-stu-id="8605e-261">The name of the storage account that you created earlier, such as **storageaccount1**</span></span>       |
        | <span data-ttu-id="8605e-262">storage-account-connection-string</span><span class="sxs-lookup"><span data-stu-id="8605e-262">storage-account-connection-string</span></span> | <span data-ttu-id="8605e-263">Savienojuma virkne, ko krātuves kontam kopējāt no lapas **Piekļuves galvenie akreditācijas dati**</span><span class="sxs-lookup"><span data-stu-id="8605e-263">The connection string that you copied from the **Access keys** page for the storage account</span></span> |

5. <span data-ttu-id="8605e-264">Autorizējiet pieteikumu, lai piekļūtu galveno akreditācijas datu glabātavai.</span><span class="sxs-lookup"><span data-stu-id="8605e-264">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="8605e-265">[Azure portālā](https://portal.azure.com) atveriet iepriekš izveidoto galveno akreditācijas datu glabātavu.</span><span class="sxs-lookup"><span data-stu-id="8605e-265">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="8605e-266">Atlasiet piekļuves politikas.</span><span class="sxs-lookup"><span data-stu-id="8605e-266">Select the access policies.</span></span>
    3. <span data-ttu-id="8605e-267">Katram pieteikumam tālāk esošajā tabulā veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="8605e-267">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="8605e-268">Atlasiet **Pievienot piekļuves politiku**, lai izveidotu piekļuves politiku.</span><span class="sxs-lookup"><span data-stu-id="8605e-268">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="8605e-269">Laukā **Noslēpuma atļaujas** atlasiet atļaujas no tālāk redzamās tabulas.</span><span class="sxs-lookup"><span data-stu-id="8605e-269">In the **Secret permissions** field, select the permissions from the following table.</span></span>
        3. <span data-ttu-id="8605e-270">Laukā **Noslēpuma vadītājs** uzmeklējiet pieteikuma parādāmo nosaukumu no tālāk redzamās tabulas.</span><span class="sxs-lookup"><span data-stu-id="8605e-270">In the **Select principal** field, search for the application display name from the following table.</span></span>
        4. <span data-ttu-id="8605e-271">Atlasiet **Atlasīt**.</span><span class="sxs-lookup"><span data-stu-id="8605e-271">Select **Select**.</span></span>
        5. <span data-ttu-id="8605e-272">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="8605e-272">Select **Add**.</span></span>
        6. <span data-ttu-id="8605e-273">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="8605e-273">Select **Save**.</span></span>

        | <span data-ttu-id="8605e-274">Pieteikums</span><span class="sxs-lookup"><span data-stu-id="8605e-274">Application</span></span>                                              | <span data-ttu-id="8605e-275">Tiesības</span><span class="sxs-lookup"><span data-stu-id="8605e-275">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="8605e-276">Parādāmais nosaukums jaunajā izveidotajā pieteikumā</span><span class="sxs-lookup"><span data-stu-id="8605e-276">The display name of the new application that you created</span></span> | <span data-ttu-id="8605e-277">Iegūt, saraksts</span><span class="sxs-lookup"><span data-stu-id="8605e-277">Get, List</span></span>   |
        | <span data-ttu-id="8605e-278">**Microsoft Dynamics ERP apakšpakalpojumi**</span><span class="sxs-lookup"><span data-stu-id="8605e-278">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="8605e-279">Iegūt, saraksts</span><span class="sxs-lookup"><span data-stu-id="8605e-279">Get, List</span></span>   |

6. <span data-ttu-id="8605e-280">Piešķiriet lomas, lai piekļūtu krātuves kontam.</span><span class="sxs-lookup"><span data-stu-id="8605e-280">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="8605e-281">[Azure portālā](https://portal.azure.com) atveriet iepriekš izveidoto krātuves kontu.</span><span class="sxs-lookup"><span data-stu-id="8605e-281">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="8605e-282">Atlasiet **Piekļuves kontrole (IAM)** un pēc tam atlasiet **Lomu piešķires**.</span><span class="sxs-lookup"><span data-stu-id="8605e-282">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="8605e-283">Atlasiet **Pievienot, pievienot lomas piešķiri**.</span><span class="sxs-lookup"><span data-stu-id="8605e-283">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="8605e-284">Katram pieteikumam tālāk esošajā tabulā veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="8605e-284">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="8605e-285">Atlasiet lomu no tālāk redzamās tabulas.</span><span class="sxs-lookup"><span data-stu-id="8605e-285">Select the role from the following table.</span></span>
        2. <span data-ttu-id="8605e-286">Atstājiet lauku **Piešķirt piekļuvi** iestatītu uz **Azure AD lietotājs, grupa vai pakalpojuma vadītājs**.</span><span class="sxs-lookup"><span data-stu-id="8605e-286">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="8605e-287">Laukā **Atlasīt** ievadiet pieteikumu no tālāk redzamās tabulas.</span><span class="sxs-lookup"><span data-stu-id="8605e-287">In the **Select** field, enter the application from the following table.</span></span>
        4. <span data-ttu-id="8605e-288">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="8605e-288">Select **Save**.</span></span>

        | <span data-ttu-id="8605e-289">Pieteikums</span><span class="sxs-lookup"><span data-stu-id="8605e-289">Application</span></span>                                              | <span data-ttu-id="8605e-290">Loma</span><span class="sxs-lookup"><span data-stu-id="8605e-290">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="8605e-291">Parādāmais nosaukums jaunajā izveidotajā pieteikumā</span><span class="sxs-lookup"><span data-stu-id="8605e-291">The display name of the new application that you created</span></span> | <span data-ttu-id="8605e-292">Īpašnieks</span><span class="sxs-lookup"><span data-stu-id="8605e-292">Owner</span></span>                       |
        | <span data-ttu-id="8605e-293">Parādāmais nosaukums jaunajā izveidotajā pieteikumā</span><span class="sxs-lookup"><span data-stu-id="8605e-293">The display name of the new application that you created</span></span> | <span data-ttu-id="8605e-294">Līdzstrādnieks</span><span class="sxs-lookup"><span data-stu-id="8605e-294">Contributor</span></span>                 |
        | <span data-ttu-id="8605e-295">Parādāmais nosaukums jaunajā izveidotajā pieteikumā</span><span class="sxs-lookup"><span data-stu-id="8605e-295">The display name of the new application that you created</span></span> | <span data-ttu-id="8605e-296">Krātuves konta līdzstrādnieks</span><span class="sxs-lookup"><span data-stu-id="8605e-296">Storage Account Contributor</span></span> |
        | <span data-ttu-id="8605e-297">Parādāmais nosaukums jaunajā izveidotajā pieteikumā</span><span class="sxs-lookup"><span data-stu-id="8605e-297">The display name of the new application that you created</span></span> | <span data-ttu-id="8605e-298">Krātuves BLOB datu īpašnieks</span><span class="sxs-lookup"><span data-stu-id="8605e-298">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="8605e-299">**AI Builder autorizācijas pakalpojums**</span><span class="sxs-lookup"><span data-stu-id="8605e-299">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="8605e-300">Krātuves BLOB datu lasītājs</span><span class="sxs-lookup"><span data-stu-id="8605e-300">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="8605e-301">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="8605e-301">Azure CLI</span></span>](#tab/azure-azure-cli)

```
function New-FinanceDataLakeAzureResources {
    $defaultSecretExpiryInYear = 1

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

    $subscriptionId = (Read-Host -Prompt "Enter the Azure Subscription ID: (blank for default)")
    if ($subscriptionId.Trim() -ne '') {
        $azSubscription = Select-AzSubscription -SubscriptionId $subscriptionId
    }

    $resourceGroupName = (Read-Host -Prompt "Enter the Azure Resource Group name: (blank for 'FinanceDataLake')")
    if ($null -eq $resourceGroupName -or $resourceGroupName.Trim() -eq '') {
        $resourceGroupName = 'FinanceDataLake'
    }
    $resourceGroup = Get-AzResourceGroup -Name $resourceGroupName -ErrorAction SilentlyContinue

    if (-not ($resourceGroup)) {
        $resourceLocation = ''
        $azResourceLocations = (Get-AzLocation | Select-Object Location).Location
        while ($resourceLocation.Trim() -eq '' -or (-not ($resourceLocation -in $azResourceLocations))) {
            $resourceLocation = (Read-Host -Prompt "Enter the location in which to create the Azure Resource Group: ('help' to see values)")
            if ($resourceLocation -eq 'help') {
                $azResourceLocations
                $resourceLocation = ''
            }
        }
        $resourceGroup = New-AzResourceGroup -Name $resourceGroupName -Location $resourceLocation
    }
    else {
        $resourceLocation = $resourceGroup.Location
    }

    $clientAppName = (Read-Host -Prompt "Enter the name of the application registration: (blank for 'Finance Data Lake Application')")
    if ($clientAppName.Trim() -eq '') {
        $clientAppName = 'Finance Data Lake Application'
    }

    Write-Output '================================================================================='

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $MicrosoftDynamicsERPMicroservicesAppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesAppId | Format-Table -AutoSize
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $MicrosoftDynamicsERPMicroservicesAppId + "'")
        Write-Output ("Added AAD Enterprise Application 'Microsoft Dynamics ERP Microservices' with Application ID {0}" -f $MicrosoftDynamicsERPMicroservicesAppId)
    }
    else {
        Write-Output ("Found AAD Enterprise Application 'Microsoft Dynamics ERP Microservices' with Application ID {0}" -f $MicrosoftDynamicsERPMicroservicesAppId)
    }
    $MicrosoftDynamicsERPMicroservicesAppObjectId = $service.ObjectId

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $MicrosoftDynamicsERPMicroservicesCDSAppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesCDSAppId | Format-Table -AutoSize
        Write-Output ("Added AAD Enterprise Application 'Microsoft Dynamics ERP Microservices CDS' with Application ID {0}" -f $MicrosoftDynamicsERPMicroservicesCDSAppId)
    }
    else {
        Write-Output ("Found AAD Enterprise Application 'Microsoft Dynamics ERP Microservices CDS' with Application ID {0}" -f $MicrosoftDynamicsERPMicroservicesCDSAppId)
    }

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AIBuilderAuthorizationServiceAppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $AIBuilderAuthorizationServiceAppId | Format-Table -AutoSize
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AIBuilderAuthorizationServiceAppId + "'")
        Write-Output ("Added AAD Enterprise Application 'AI Builder Authorization Service' with Application ID {0}" -f $AIBuilderAuthorizationServiceAppId)
    }
    else {
        Write-Output ("Found AAD Enterprise Application 'AI Builder Authorization Service' with Application ID {0}" -f $AIBuilderAuthorizationServiceAppId)
    }
    $aibuilderAuthorizationServiceObjectId = $service.ObjectId

    Write-Output '================================================================================='

    $clientAppSPN = Get-AzureADServicePrincipal -Filter ("DisplayName eq '" + $clientAppName + "'")
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

        $clientApp = New-AzureADApplication -DisplayName $clientAppName -RequiredResourceAccess @($keyVaultAccess, $graphAccess)
        $clientAppSPN = New-AzureADServicePrincipal -AppId $clientApp.AppId -Tags @($clientAppName)
        $clientAppId = $clientApp.AppId
        Write-Output ('Created App Registration "' + $clientAppName + '" with Application Id: ' + $clientAppId)
    }
    else {
        $clientApp = Get-AzureADApplication -Filter ("DisplayName eq '" + $clientAppName + "'")
        $clientAppId = $clientApp.AppId
        Write-Output ('Found App Registration "' + $clientAppName + '" with Application Id: ' + $clientAppId)
    }
            
    $clientAppSecretCredential = New-AzureADApplicationPasswordCredential -ObjectId $clientApp.ObjectId -CustomKeyIdentifier "ClientAppAccessKey" -EndDate (get-date).AddYears($defaultSecretExpiryInYear)
    $ClientAppSecret = $clientAppSecretCredential.Value
    $clientAppSpId = $clientAppSPN.ObjectId

    Write-Output ('Generated application secret: ' + $ClientAppSecret)
    Write-Output '================================================================================='

    $templateObject = ConvertFrom-Json $azureTemplate -AsHashtable
    $templateObject.{$schema} = "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#"
    Write-Output 'Provisioning Azure resources. This may take a few minutes.'
    $deployment = New-AzResourceGroupDeployment -ResourceGroupName $resourceGroupName -TemplateObject $templateObject -aibuilderAppObjectId $aibuilderAuthorizationServiceObjectId -clientAppId $clientAppId -clientAppSecret $ClientAppSecret -clientAppSpObjectId  $clientAppSpId -microserviceSpObjectId $MicrosoftDynamicsERPMicroservicesAppObjectId -userSpObjectId $user.ObjectId

    if ($deployment.ProvisioningState -eq 'Succeeded') {
        Write-Output "Successfully deployed the following resources to Azure:"
        Write-Output ("  Key Vault:                         " + $deployment.Outputs.keyVaultName.Value)
        Write-Output ("  Storage Account:                   " + $deployment.Outputs.storageAccountName.Value)
    }
    else {
        Write-Output ("Provisioning Azure resources failed with the following state: " + $deployment.ProvisioningState)
        Write-Output ("Some of the resources may have been created in resource group: " + $resourceGroupName)
    }

    Write-Output '================================================================================='

    $keyVault = Get-AzKeyVault -VaultName $deployment.Outputs.keyVaultName.Value
    Write-Output "Values for LCS Data Lake Add-In:"
    Write-Output ("  Tenant ID:                         " + $subscriptionContext.Context.Subscription.TenantId)
    Write-Output ("  DNS Name:                          " + $keyVault.VaultUri)
    Write-Output "  Storage account secret name:       storage-account-name"
    Write-Output "  Application ID secret name:        app-id"
    Write-Output "  Application Secret secret name:    app-secret"
    Write-Warning "Copy this information for the LCS Add-in as it is not saved. Azure Cloud Shell will eventually time out and close."

    Write-Output '================================================================================='
    Write-Output "Values for System parameters > Data connections:"
    Write-Output ("  Application ID:                    " + $clientAppId)
    Write-Output ("  Application Secret:                " + $ClientAppSecret)
    Write-Output ("  DNS name:                          " + $keyVault.VaultUri)
    Write-Output "  Secret name:                       storage-account-connection-string"
    Write-Warning "Copy this information for the System parameters as it is not saved. Azure Cloud Shell will eventually time out and close."
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
  New-FinanceDataLakeAzureResources
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

## <a name="configure-the-entity-store"></a><span data-ttu-id="8605e-302">Elementu krātuves konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="8605e-302">Configure the entity store</span></span>

<span data-ttu-id="8605e-303">Izpildiet tālāk norādītās darbības, lai iestatītu Finanšu vides elementu krātuvi.</span><span class="sxs-lookup"><span data-stu-id="8605e-303">Follow these steps to set up the entity store in your Finance environment.</span></span>

1. <span data-ttu-id="8605e-304">Dodieties uz **Sistēmas administrēšana \> Iestatījumi \> Sistēmas parametri \> Datu savienojumi**.</span><span class="sxs-lookup"><span data-stu-id="8605e-304">Go to **System administration \> Setup \> System parameters \> Data connections**.</span></span>
2. <span data-ttu-id="8605e-305">Iestatiet opciju **Iespējot Data Lake integrāciju** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="8605e-305">Set the **Enable Data Lake integration** option to **Yes**.</span></span>
3. <span data-ttu-id="8605e-306">Iestatiet tālāk norādītos Galvenās akreditācijas datu glabātavas laukus.</span><span class="sxs-lookup"><span data-stu-id="8605e-306">Set the following Key Vault fields:</span></span>

    - <span data-ttu-id="8605e-307">**Pieteikuma (klienta) ID** — ievadiet iepriekš izveidoto pieteikuma klienta ID.</span><span class="sxs-lookup"><span data-stu-id="8605e-307">**Application (client) ID** – Enter the application client ID that you created earlier.</span></span>
    - <span data-ttu-id="8605e-308">**Pieteikuma noslēpums** — ievadiet noslēpumu, ko saglabājāt iepriekš izveidotajam pieteikumam.</span><span class="sxs-lookup"><span data-stu-id="8605e-308">**Application Secret** – Enter the secret that you saved for the application that you created earlier.</span></span>
    - <span data-ttu-id="8605e-309">**DNS nosaukums** — varat atrast domēna nosaukuma sistēmas (DNS) nosaukumu iepriekš izveidotā pieteikuma detalizētas informācijas lapā.</span><span class="sxs-lookup"><span data-stu-id="8605e-309">**DNS name** – You can find the Domain Name System (DNS) name on the application details page for the application that you created earlier.</span></span>
    - <span data-ttu-id="8605e-310">**Noslēpuma nosaukums** — ievadiet **krātuve-konts-savienojums-virkne**.</span><span class="sxs-lookup"><span data-stu-id="8605e-310">**Secret name** – Enter **storage-account-connection-string**.</span></span>

## <a name="configure-the-data-lake"></a><span data-ttu-id="8605e-311">Data Lake konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="8605e-311">Configure the data lake</span></span>

<span data-ttu-id="8605e-312">Veiciet tālāk norādītās darbības, lai izmantotu LCS, lai pievienotu videi Azure Data Lake pievienojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="8605e-312">Follow these steps to use LCS to add the Azure Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="8605e-313">Pierakstieties LCS un pēc tam pie vides nosaukuma lapas labajā pusē atlasiet **Pilna informācija**.</span><span class="sxs-lookup"><span data-stu-id="8605e-313">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="8605e-314">Sadaļā **Vides pievienojumprogrammas** atlasiet **Instalēt jaunu pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="8605e-314">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="8605e-315">Atlasiet pievienojumprogrammu **Eksportēt uz Data Lake**.</span><span class="sxs-lookup"><span data-stu-id="8605e-315">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="8605e-316">Ievadiet tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="8605e-316">Enter the following values.</span></span>

    | <span data-ttu-id="8605e-317">Vērtība</span><span class="sxs-lookup"><span data-stu-id="8605e-317">Value</span></span>                                                              | <span data-ttu-id="8605e-318">Apraksts</span><span class="sxs-lookup"><span data-stu-id="8605e-318">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="8605e-319">Nomnieka ID Azure abonementam, kur atrodas Galvenās akreditācijas datu glabātava</span><span class="sxs-lookup"><span data-stu-id="8605e-319">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="8605e-320">Nomnieka ID, kur atrodas krātuves konts, pieteikumi un galvenās akreditācijas datu glabātavas.</span><span class="sxs-lookup"><span data-stu-id="8605e-320">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="8605e-321">Lai atrastu šo vērtību, atveriet [Azure portālu](https://portal.azure.com), dodieties uz **Azure Active Directory** un kopējiet vērtību **Nomnieka ID**.</span><span class="sxs-lookup"><span data-stu-id="8605e-321">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="8605e-322">Norādiet sava Key Vault DNS nosaukumu</span><span class="sxs-lookup"><span data-stu-id="8605e-322">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="8605e-323">Galvenās akreditācijas datu glabātavas DNS nosaukums, piemēram, `https://customkeyvault.vault.azure.net/`.</span><span class="sxs-lookup"><span data-stu-id="8605e-323">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> <span data-ttu-id="8605e-324">(Šī vērtība atbilst DNS nosaukumam, kas tiek izmantots elementa krātuvē.)</span><span class="sxs-lookup"><span data-stu-id="8605e-324">(This value matches the DNS name that is used in the entity store.)</span></span> |
    | <span data-ttu-id="8605e-325">Norādiet noslēpumu, kas satur krātuves konta nosaukumu</span><span class="sxs-lookup"><span data-stu-id="8605e-325">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="8605e-326">**storage-account-name**</span><span class="sxs-lookup"><span data-stu-id="8605e-326">**storage-account-name**</span></span> |
    | <span data-ttu-id="8605e-327">Pieteikuma ID noslēpuma nosaukums, kas jāizmanto, lai piekļūtu Data Lake</span><span class="sxs-lookup"><span data-stu-id="8605e-327">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="8605e-328">**app-id**</span><span class="sxs-lookup"><span data-stu-id="8605e-328">**app-id**</span></span> |
    | <span data-ttu-id="8605e-329">Noslēpuma nosaukums, kas jāizmanto ar pieteikuma ID</span><span class="sxs-lookup"><span data-stu-id="8605e-329">Secret name to be used with App ID</span></span>                                 | <span data-ttu-id="8605e-330">**app-secret**</span><span class="sxs-lookup"><span data-stu-id="8605e-330">**app-secret**</span></span> |

5. <span data-ttu-id="8605e-331">Piekrītiet nosacījumiem un atlasiet **Instalēt**.</span><span class="sxs-lookup"><span data-stu-id="8605e-331">Agree to the terms, and select **Install**.</span></span>

<span data-ttu-id="8605e-332">Pievienojumprogramma tiks instalēta dažu minūšu laikā.</span><span class="sxs-lookup"><span data-stu-id="8605e-332">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-ai-builder"></a><span data-ttu-id="8605e-333">AI Builder konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="8605e-333">Configure AI Builder</span></span>

1. <span data-ttu-id="8605e-334">Pierakstieties LCS un atveriet lapu **Detalizēta informācija par vidi**.</span><span class="sxs-lookup"><span data-stu-id="8605e-334">Sign in to LCS, and open the **Environment details** page.</span></span>
2. <span data-ttu-id="8605e-335">Ritiniet līdz sadaļai **Vides pievienojumprogrammas**.</span><span class="sxs-lookup"><span data-stu-id="8605e-335">Scroll to the **Environment add-ins** section.</span></span> <span data-ttu-id="8605e-336">Ir jābūt redzamām pievienojumprogrammām, kas jau ir instalētas šajā vidē.</span><span class="sxs-lookup"><span data-stu-id="8605e-336">You should see the add-ins that are already installed in this environment.</span></span> <span data-ttu-id="8605e-337">Ja pievienojumprogramma **Eksportēt uz Data Lake** nav to vidū, konfigurējiet šo pievienojumprogrammu.</span><span class="sxs-lookup"><span data-stu-id="8605e-337">If the **Export to Data Lake** add-in isn't among them, configure this add-in.</span></span>
3. <span data-ttu-id="8605e-338">Atlasiet pievienojumprogrammu **Iegūt ieskatus**.</span><span class="sxs-lookup"><span data-stu-id="8605e-338">Select the **Get insights** add-in.</span></span>
4. <span data-ttu-id="8605e-339">Pievienojumprogrammas detalizētās informācijas lapā **Iegūt ieskatus** ievadiet tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="8605e-339">On the **Get insights** add-in details page, enter the following values.</span></span>

    | <span data-ttu-id="8605e-340">Vērtība</span><span class="sxs-lookup"><span data-stu-id="8605e-340">Value</span></span>                                                    | <span data-ttu-id="8605e-341">Apraksts</span><span class="sxs-lookup"><span data-stu-id="8605e-341">Description</span></span> |
    |----------------------------------------------------------|-------------|
    | <span data-ttu-id="8605e-342">CDS organizācijas URL</span><span class="sxs-lookup"><span data-stu-id="8605e-342">CDS Organization URL</span></span>                                     | <span data-ttu-id="8605e-343">Common Data Service organizācijas URL Common Data Service instancē.</span><span class="sxs-lookup"><span data-stu-id="8605e-343">The Common Data Service organization URL of the Common Data Service instance.</span></span> <span data-ttu-id="8605e-344">Lai atrastu šo vērtību, atveriet [Power Apps portālu](https://make.powerapps.com), atlasiet pogu **Iestatījumi** (zobrata simbols) augšējā labajā stūrī, atlasiet **Papildu iestatījumi** un kopējiet URL.</span><span class="sxs-lookup"><span data-stu-id="8605e-344">To find this value, open the [Power Apps portal](https://make.powerapps.com), select the **Settings** button (gear symbol) in the upper-right upper corner, select **Advanced settings**, and copy the URL.</span></span> <span data-ttu-id="8605e-345">(URL beidzas ar "dynamics.com.")</span><span class="sxs-lookup"><span data-stu-id="8605e-345">(The URL ends with "dynamics.com.")</span></span> |
    | <span data-ttu-id="8605e-346">CDS org. ID</span><span class="sxs-lookup"><span data-stu-id="8605e-346">CDS Org ID</span></span>                                               | <span data-ttu-id="8605e-347">Common Data Service instances vides ID.</span><span class="sxs-lookup"><span data-stu-id="8605e-347">The environment ID of the Common Data Service instance.</span></span> <span data-ttu-id="8605e-348">Lai atrastu šo vērtību, atveriet [Power Apps portālu](https://make.powerapps.com), atlasiet pogu **Iestatījumi** (zobrata simbols) augšējā labajā stūrī, atlasiet **Pielāgojumi \> Izstrādātāja resursi \> Instances atsauces informācija** un kopējiet vērtību **ID**.</span><span class="sxs-lookup"><span data-stu-id="8605e-348">To find this value, open the [Power Apps portal](https://make.powerapps.com), select the **Settings** button (gear symbol) in the upper-right upper corner, select **Customizations \> Developer resources \> Instance Reference Information**, and copy the **ID** value.</span></span> |
    | <span data-ttu-id="8605e-349">CDS nomnieka ID (direktorija ID no AAD)</span><span class="sxs-lookup"><span data-stu-id="8605e-349">CDS Tenant ID (Directory ID from AAD)</span></span>               | <span data-ttu-id="8605e-350">Common Data Service instances nomnieka ID.</span><span class="sxs-lookup"><span data-stu-id="8605e-350">The tenant ID of the Common Data Service instance.</span></span> <span data-ttu-id="8605e-351">Lai atrastu šo vērtību, atveriet [Azure portālu](https://portal.azure.com), dodieties uz **Azure Active Directory** un kopējiet vērtību **Nomnieka ID**.</span><span class="sxs-lookup"><span data-stu-id="8605e-351">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="8605e-352">Norādiet tā lietotāja objekta ID, kam ir sistēmas administratora loma</span><span class="sxs-lookup"><span data-stu-id="8605e-352">Provide user object ID who has system administrator role</span></span> | <span data-ttu-id="8605e-353">Azure AD lietotāja objekta ID lietotājam Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="8605e-353">The Azure AD user object ID of the user in Common Data Service.</span></span> <span data-ttu-id="8605e-354">Šim lietotājam jābūt Common Data Service instances sistēmas administratoram.</span><span class="sxs-lookup"><span data-stu-id="8605e-354">This user must be a system administrator of the Common Data Service instance.</span></span> <span data-ttu-id="8605e-355">Lai atrastu šo vērtību, atveriet [Azure portālu](https://portal.azure.com), dodieties uz **Azure Active Directory \> Lietotāji**, atlasiet lietotāju un pēc tam sekcijā **Identitāte** kopējiet vērtību **Objekta ID**.</span><span class="sxs-lookup"><span data-stu-id="8605e-355">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory \> Users**, select the user, and then, in the **Identity** section, copy the **Object ID** value.</span></span> |
    | <span data-ttu-id="8605e-356">Vai šī ir nomnieka noklusējuma CDS vide?</span><span class="sxs-lookup"><span data-stu-id="8605e-356">Is this the default CDS environment for the tenant?</span></span>      | <span data-ttu-id="8605e-357">Ja Common Data Service instance bija pirmā izveidotā ražošanas instance, atzīmējiet šo izvēles rūtiņu.</span><span class="sxs-lookup"><span data-stu-id="8605e-357">If the Common Data Service instance was the first production instance that was created, select this check box.</span></span> <span data-ttu-id="8605e-358">Ja Common Data Service instance tika izveidota manuāli, izņemiet atzīmi no šīs izvēles rūtiņas.</span><span class="sxs-lookup"><span data-stu-id="8605e-358">If the Common Data Service instance was manually created, clear this check box.</span></span> |

## <a name="feedback-and-support"></a><span data-ttu-id="8605e-359">Atsauksmes un atbalsts</span><span class="sxs-lookup"><span data-stu-id="8605e-359">Feedback and support</span></span>

<span data-ttu-id="8605e-360">Lūdzu, sūtiet e-pastu [klientu maksājumu ieskatiem (priekšskatījums)](mailto:fiap@microsoft.com), ja vēlaties sniegt atsauksmes vai ir nepieciešams atbalsts.</span><span class="sxs-lookup"><span data-stu-id="8605e-360">Please send an email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in providing feedback or need support.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="8605e-361">Paziņojums par konfidencialitāti</span><span class="sxs-lookup"><span data-stu-id="8605e-361">Privacy notice</span></span>

<span data-ttu-id="8605e-362">Priekšskatījumiem (1) var tikt izmantots mazāk konfidencialitātes un drošības pasākumu nekā pakalpojumam Dynamics 365 Finance and Operations, (2) tie nav ietverti pakalpojuma līmeņa līgumā par šo pakalpojumu, (3) tos nedrīkst izmantot personas datu vai citu tādu datu apstrādei, uz kuriem attiecas juridiskās vai normatīvās prasības, un (4) tiem tiek nodrošināts ierobežots atbalsts.</span><span class="sxs-lookup"><span data-stu-id="8605e-362">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>