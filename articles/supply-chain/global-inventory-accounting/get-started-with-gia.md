---
title: Darba sākšana ar Globālo krājumu uzskaiti
description: Šajā tēmā ir aprakstīts, kā sākt darbu ar Globālo krājumu uzskaiti.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 59f9db309312bbbc88b4fa47c12c4c02f09e7c6d
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301702"
---
# <a name="get-started-with-global-inventory-accounting"></a><span data-ttu-id="7b056-103">Darba sākšana ar Globālo krājumu uzskaiti</span><span class="sxs-lookup"><span data-stu-id="7b056-103">Get started with Global Inventory Accounting</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="7b056-104">Globālā krājumu uzskaite ļauj veikt vairāku krājumu uzskaites Globālās krājumu uzskaites virsgrāmatās, kas iestatītas.</span><span class="sxs-lookup"><span data-stu-id="7b056-104">Global Inventory Accounting lets you do multiple inventory accountings in the Global Inventory Accounting ledgers that you've set up.</span></span> <span data-ttu-id="7b056-105">Katru Globālās krājumu uzskaites virsgrāmatu jāsaista ar *konvenciju*.</span><span class="sxs-lookup"><span data-stu-id="7b056-105">You must associate each Global Inventory Accounting ledger with a *convention*.</span></span> <span data-ttu-id="7b056-106">Konvencija ir šādu uzskaites ierobežojumu tipu apkopojums:</span><span class="sxs-lookup"><span data-stu-id="7b056-106">A convention is a collection of the following types of accounting policies:</span></span>

- <span data-ttu-id="7b056-107">Izmaksu objekts</span><span class="sxs-lookup"><span data-stu-id="7b056-107">Cost object</span></span>
- <span data-ttu-id="7b056-108">Ievades mērījumu bāze</span><span class="sxs-lookup"><span data-stu-id="7b056-108">Input measurement basis</span></span>
- <span data-ttu-id="7b056-109">Izmaksu plūsmas pieņēmums</span><span class="sxs-lookup"><span data-stu-id="7b056-109">Cost flow assumption</span></span>
- <span data-ttu-id="7b056-110">Izmaksu elements</span><span class="sxs-lookup"><span data-stu-id="7b056-110">Cost element</span></span>

> [!NOTE]
> <span data-ttu-id="7b056-111">Pat pēc tam, kad esat ieslēdzis Globālo krājumu uzskaiti, jūs joprojām varat veikt krājumu uzskaiti programmā Microsoft Dynamics 365 Supply Chain Management, kā parasti.</span><span class="sxs-lookup"><span data-stu-id="7b056-111">Even after you turn on Global Inventory Accounting, you can still do inventory accounting in Microsoft Dynamics 365 Supply Chain Management in the usual way.</span></span>

<span data-ttu-id="7b056-112">Globālā krājumu uzskaite ir pievienojumprogramma.</span><span class="sxs-lookup"><span data-stu-id="7b056-112">Global Inventory Accounting is an add-in.</span></span> <span data-ttu-id="7b056-113">Lai padarītu šīs funkcijas pieejamas, tās ir jāinstalē no Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="7b056-113">To make its features available, you must install it from Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="7b056-114">Varat izvēlēties to novērtēt testa vidē pirms tā ieslēgšanas ražošanas vidē.</span><span class="sxs-lookup"><span data-stu-id="7b056-114">You can choose to evaluate it in a test environment before you turn it on for production environments.</span></span>

<span data-ttu-id="7b056-115">Globālā krājumu uzskaite šobrīd neatbalsta visus izmaksu pārvaldības līdzekļus, kas ir iebūvēti Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7b056-115">Global Inventory Accounting doesn't currently support all the cost management features that are built into Supply Chain Management.</span></span> <span data-ttu-id="7b056-116">Tāpēc ir svarīgi novērtēt, vai līdzekļu kopa, kas pašlaik ir pieejama, atbilst jūsu prasībām.</span><span class="sxs-lookup"><span data-stu-id="7b056-116">Therefore, it's important that you evaluate whether the set of features that is currently available will meet your requirements.</span></span>

## <a name="how-to-get-the-global-inventory-accounting-public-preview"></a><a name="sign-up"></a><span data-ttu-id="7b056-117">Kā iegūt Globālās krājuma uzskaites publisku priekšskatījumu</span><span class="sxs-lookup"><span data-stu-id="7b056-117">How to get the Global Inventory Accounting public preview</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7b056-118">Lai izmantotu Globālo krājumu uzskaiti, ir jābūt LCS iespējotai augstas pieejamības videi (nevis OneBox videi).</span><span class="sxs-lookup"><span data-stu-id="7b056-118">To use Global Inventory Accounting, you must have an LCS-enabled high-availability environment (not a OneBox environment).</span></span> <span data-ttu-id="7b056-119">Turklāt jāizmanto Supply Chain Management versiju 10.0.19 vai jaunāku.</span><span class="sxs-lookup"><span data-stu-id="7b056-119">Additionally, you must be running Supply Chain Management version 10.0.19 or later.</span></span>

<span data-ttu-id="7b056-120">Lai pieteiktos Globālās krājumu uzskaites publiskajam priekšskatījumam, nosūtiet savu LCS vides ID pa e-pastu [Globālās krājumu uzskaites grupai](mailto:GlobalInventoryAccounting@service.microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="7b056-120">To sign up for the Global Inventory Accounting public preview, send your LCS environment ID by email to the [Global Inventory Accounting team](mailto:GlobalInventoryAccounting@service.microsoft.com).</span></span> <span data-ttu-id="7b056-121">Pēc programmas apstiprināšanas grupa nosūtīs jums e-pasta ziņojumu, kas ietvers Globālās krājumu uzskaites beta atslēgu un jūsu pakalpojuma galapunktus.</span><span class="sxs-lookup"><span data-stu-id="7b056-121">After you're approved for the program, the team will send you a follow-up email that contains a Global Inventory Accounting beta key and your service endpoints.</span></span> <span data-ttu-id="7b056-122">Pēc beta atslēgas saņemšanas varat [instalēt pievienojumprogrammu](#install).</span><span class="sxs-lookup"><span data-stu-id="7b056-122">After you receive the beta key, you can [install the add-in](#install).</span></span>

## <a name="licensing"></a><span data-ttu-id="7b056-123">Licencēšana</span><span class="sxs-lookup"><span data-stu-id="7b056-123">Licensing</span></span>

<span data-ttu-id="7b056-124">Globālā krājumu uzskaite ir licencēta kopā ar krājumu uzskaites standarta līdzekļiem, kas ir pieejami Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7b056-124">Global Inventory Accounting is licensed together with the standard features of inventory accounting that are available for Supply Chain Management.</span></span> <span data-ttu-id="7b056-125">Jums nav jāiegādājas papildu licence, lai izmantotu Globālo krājumu uzskaiti.</span><span class="sxs-lookup"><span data-stu-id="7b056-125">You don't have to purchase an additional license to use Global Inventory Accounting.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7b056-126">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="7b056-126">Prerequisites</span></span>

### <a name="set-up-microsoft-power-platform-integration"></a><span data-ttu-id="7b056-127">Iestatiet integrāciju ar Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="7b056-127">Set up Microsoft Power Platform integration</span></span>

<span data-ttu-id="7b056-128">Pirms iespējot pievienojumprogrammas funkcionalitāti, jums jāintegrē ar Microsoft Power Platform, veicot šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="7b056-128">Before you can enable add-in functionality, you must integrate with Microsoft Power Platform by following these steps.</span></span>

1. <span data-ttu-id="7b056-129">Atveriet LCS vidi, kurā vēlaties pievienot pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="7b056-129">Open the LCS environment where you want to add the service.</span></span>
1. <span data-ttu-id="7b056-130">Doties **Pilna detalizēta informācija**.</span><span class="sxs-lookup"><span data-stu-id="7b056-130">Go to **Full details**.</span></span>
1. <span data-ttu-id="7b056-131">Sadaļā **Power Platform integrācija** atlasiet **Iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="7b056-131">In the **Power Platform Integration** section, select **Setup**.</span></span>
1. <span data-ttu-id="7b056-132">Dialoglodziņā **Power Platform vides iestatīšana** atzīmējiet izvēles rūtiņu un pēc tam atlasiet **Iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="7b056-132">In the **Power platform environment setup** dialog box, select the checkbox, and then select **Setup**.</span></span> <span data-ttu-id="7b056-133">Parasti iestatīšana ilgst no 60 līdz 90 minūtēm.</span><span class="sxs-lookup"><span data-stu-id="7b056-133">Typically, setup takes between 60 and 90 minutes.</span></span>
1. <span data-ttu-id="7b056-134">Kad Microsoft Power Platform vides iestatīšana ir pabeigta, lapa parāda jūsu vides nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="7b056-134">After setup of the Microsoft Power Platform environment is completed, the page shows the name of your environment.</span></span> <span data-ttu-id="7b056-135">Turklāt sadaļā **Power Platform Integrācija** ir parādīts paziņojums "Power Platform vides iestatīšana ir pabeigta."</span><span class="sxs-lookup"><span data-stu-id="7b056-135">Additionally, the **Power Platform Integration** section shows the statement, "Power Platform environment setup is complete."</span></span> <span data-ttu-id="7b056-136">Globālajai krājumu uzskaitei nav nepieciešama dubultās rakstīšanas programma.</span><span class="sxs-lookup"><span data-stu-id="7b056-136">Global Inventory Accounting doesn't require a dual-write application.</span></span>

<span data-ttu-id="7b056-137">Papildinformāciju skatiet rakstā [Iestatīt pēc vides izvietošanas](../../fin-ops-core/dev-itpro/power-platform/overview.md#set-up-after-environment-deployment).</span><span class="sxs-lookup"><span data-stu-id="7b056-137">For more information, see [Set up after environment deployment](../../fin-ops-core/dev-itpro/power-platform/overview.md#set-up-after-environment-deployment).</span></span>

### <a name="set-up-dataverse"></a><span data-ttu-id="7b056-138">Iestatīt Dataverse</span><span class="sxs-lookup"><span data-stu-id="7b056-138">Set up Dataverse</span></span>

<span data-ttu-id="7b056-139">Pirms Dataverse iestatīšanas, pievienojiet nomniekam Globālās krājumu uzskaites pakalpojumu principus, izpildot šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="7b056-139">Before you set up Dataverse, add the Global Inventory Accounting service principles to your tenant by following these steps.</span></span>

1. <span data-ttu-id="7b056-140">Instalējiet Azure AD moduli Windows PowerShell v2, kā aprakstīts [Pakalpojuma Azure Active Directory instalēšana PowerShell grafikam](/powershell/azure/active-directory/install-adv2).</span><span class="sxs-lookup"><span data-stu-id="7b056-140">Install Azure AD Module for Windows PowerShell v2 as described in [Install Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).</span></span>
1. <span data-ttu-id="7b056-141">Izpildiet šādu PowerShell komandu.</span><span class="sxs-lookup"><span data-stu-id="7b056-141">Run the following PowerShell command.</span></span>

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)

    New-AzureADServicePrincipal -AppId "7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9" -DisplayName "d365-scm-costaccountingservice"

    New-AzureADServicePrincipal -AppId "5f58fc56-0202-49a8-ac9e-0946b049718b" -DisplayName "d365-scm-operationdataservice"
    ```

<span data-ttu-id="7b056-142">Pēc tam izveidojiet programmas lietotājus Globālajā krājumu uzskaitē programmā Dataverse, veicot šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="7b056-142">Next, create application users for Global Inventory Accounting in Dataverse by following these steps.</span></span>

1. <span data-ttu-id="7b056-143">Atveriet Dataverse vides URL.</span><span class="sxs-lookup"><span data-stu-id="7b056-143">Open the URL of your Dataverse environment.</span></span>
1. <span data-ttu-id="7b056-144">Dodieties uz **Papildu iestatījumi \> Sistēma \> Drošība \> Lietotāji** un izveidojiet programmas lietotāju.</span><span class="sxs-lookup"><span data-stu-id="7b056-144">Go to **Advanced Setting \> System \> Security \> Users**, and create an application user.</span></span> <span data-ttu-id="7b056-145">Izmantojiet lauku **Skats**, lai mainītu lapas skatu uz *Programmas lietotāji*.</span><span class="sxs-lookup"><span data-stu-id="7b056-145">Use the **View** field to change the page view to *Application users*.</span></span>
1. <span data-ttu-id="7b056-146">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="7b056-146">Select **New**.</span></span>
1. <span data-ttu-id="7b056-147">Iestatiet lauku **Programmas ID** uz *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*.</span><span class="sxs-lookup"><span data-stu-id="7b056-147">Set the **Application ID** field to *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*.</span></span>
1. <span data-ttu-id="7b056-148">Atlasiet **Piešķirt lomu** un pēc tam atlasiet *Sistēmas administrators*.</span><span class="sxs-lookup"><span data-stu-id="7b056-148">Select **Assign Role**, and then select *System Administrator*.</span></span> <span data-ttu-id="7b056-149">Ja ir loma ar nosaukumu *Common Data Service Lietotājs*, atlasiet to arī.</span><span class="sxs-lookup"><span data-stu-id="7b056-149">If there is a role that is named *Common Data Service User*, select it too.</span></span>
1. <span data-ttu-id="7b056-150">Atkārtojiet iepriekšējās darbības, bet iestatiet lauku **Pieteikuma ID** uz *5f58fc56-0202-49a8-ac9e-0946b049718b*.</span><span class="sxs-lookup"><span data-stu-id="7b056-150">Repeat the preceding steps, but set the **Application ID** field to *5f58fc56-0202-49a8-ac9e-0946b049718b*.</span></span>

<span data-ttu-id="7b056-151">Papildinformāciju skatiet nodaļā [Programmas lietotāja izveide](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span><span class="sxs-lookup"><span data-stu-id="7b056-151">For more information, see [Create an application user](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).</span></span>

<span data-ttu-id="7b056-152">Ja jūsu Dataverse instalācijas noklusējuma valoda nav angļu valoda, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="7b056-152">If the default language of your Dataverse installation isn't English, follow these steps.</span></span>

1. <span data-ttu-id="7b056-153">Pārejiet uz **Papildu iestatījums \> Administrēšana \> Valodas**.</span><span class="sxs-lookup"><span data-stu-id="7b056-153">Go to **Advanced Setting \> Administration \> Languages**.</span></span>
1. <span data-ttu-id="7b056-154">Atlasiet *Angļu* (*ValodasKods=1033*) un pēc tam atlasiet **Lietot**.</span><span class="sxs-lookup"><span data-stu-id="7b056-154">Select *English* (*LanguageCode=1033*), and then select **Apply**.</span></span>

## <a name="install-the-add-in"></a><a name="install"></a><span data-ttu-id="7b056-155">Pievienojumprogrammas instalēšana</span><span class="sxs-lookup"><span data-stu-id="7b056-155">Install the add-in</span></span>

<span data-ttu-id="7b056-156">Izpildiet šīs darbības, lai instalētu pievienojumprogrammu, kuru var izmantot Globālajai krājumu uzskaitei.</span><span class="sxs-lookup"><span data-stu-id="7b056-156">Follow these steps to install the add-in so that you can use Global Inventory Accounting.</span></span>

1. <span data-ttu-id="7b056-157">[Parakstīties](#sign-up) Globālās krājuma uzskaites publiskam priekšskatījumam.</span><span class="sxs-lookup"><span data-stu-id="7b056-157">[Sign up](#sign-up) for the Global Inventory Accounting public preview.</span></span>
1. <span data-ttu-id="7b056-158">Pierakstieties [LCS](https://lcs.dynamics.com/Logon/Index).</span><span class="sxs-lookup"><span data-stu-id="7b056-158">Sign in to [LCS](https://lcs.dynamics.com/Logon/Index).</span></span>
1. <span data-ttu-id="7b056-159">Dodieties uz **Priekšskatīt līdzekļu pārvaldību**.</span><span class="sxs-lookup"><span data-stu-id="7b056-159">Go to **Preview feature management**.</span></span>
1. <span data-ttu-id="7b056-160">Atlasiet plus zīmi (**+**).</span><span class="sxs-lookup"><span data-stu-id="7b056-160">Select the plus sign (**+**).</span></span>
1. <span data-ttu-id="7b056-161">Laukā **Kods** ievadiet savu papildinājuma beta atslēgu Globālajai krājuma uzskaitei.</span><span class="sxs-lookup"><span data-stu-id="7b056-161">In the **Code** field, enter your add-in beta key for Global Inventory Accounting.</span></span> <span data-ttu-id="7b056-162">(Kad pierakstījieties, jums vajadzētu saņemt beta atslēgu ar e-pasta ziņojumu.)</span><span class="sxs-lookup"><span data-stu-id="7b056-162">(You should have received your beta key by email when you signed up.)</span></span>
1. <span data-ttu-id="7b056-163">Atlasiet **Atbloķēt**.</span><span class="sxs-lookup"><span data-stu-id="7b056-163">Select **Unblock**.</span></span>
1. <span data-ttu-id="7b056-164">Atveriet LCS vidi, kurā vēlaties pievienot pakalpojumu.</span><span class="sxs-lookup"><span data-stu-id="7b056-164">Open the LCS environment where you want to add the service.</span></span>
1. <span data-ttu-id="7b056-165">Doties **Pilna detalizēta informācija**.</span><span class="sxs-lookup"><span data-stu-id="7b056-165">Go to **Full details**.</span></span>
1. <span data-ttu-id="7b056-166">Dodieties uz **Power Platform integrāciju** un atlasiet **Iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="7b056-166">Go to **Power Platform Integration**, and select **Setup**.</span></span>
1. <span data-ttu-id="7b056-167">Dialoglodziņā **Power Platform vides iestatīšana** atzīmējiet izvēles rūtiņu un pēc tam atlasiet **Iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="7b056-167">In the **Power platform environment setup** dialog box, select the checkbox, and then select **Setup**.</span></span> <span data-ttu-id="7b056-168">Parasti iestatīšana ilgst no 60 līdz 90 minūtēm.</span><span class="sxs-lookup"><span data-stu-id="7b056-168">Typically, setup takes between 60 and 90 minutes.</span></span>
1. <span data-ttu-id="7b056-169">Kad Microsoft Power Platform vides iestatīšana ir pabeigta, kopsavilkuma cilnē **Vides pievienojumprogrammas** atlasiet **Instalēt jaunu pievienojumprogrammu**.</span><span class="sxs-lookup"><span data-stu-id="7b056-169">After setup of the Microsoft Power Platform environment is completed, on the **Environment add-ins** FastTab, select **Install a new add-in**.</span></span>
1. <span data-ttu-id="7b056-170">Atlasiet **Globālā krājumu uzskaite**.</span><span class="sxs-lookup"><span data-stu-id="7b056-170">Select **Global inventory accounting**.</span></span>
1. <span data-ttu-id="7b056-171">Izpildiet instalācijas rokasgrāmatas darbības un akceptējiet nosacījumus un nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="7b056-171">Follow the installation guide, and agree to the terms and conditions.</span></span>
1. <span data-ttu-id="7b056-172">Atlasiet **Instalēt**.</span><span class="sxs-lookup"><span data-stu-id="7b056-172">Select **Install**.</span></span>
1. <span data-ttu-id="7b056-173">Kopsavilkuma cilnē **Vides pievienojumprogramma** jūs redzēsiet, ka tiek instalēta Globālā krājumu uzskaite.</span><span class="sxs-lookup"><span data-stu-id="7b056-173">On the **Environment add-ins** FastTab, you should see that Global Inventory Accounting is being installed.</span></span> <span data-ttu-id="7b056-174">Pēc dažām minūtēm statusam jāmainās no *Instalē* uz *Instalēts*.</span><span class="sxs-lookup"><span data-stu-id="7b056-174">After a few minutes, the status should change from *Installing* to *Installed*.</span></span> <span data-ttu-id="7b056-175">(Iespējams, ka ir jāatsvaidzina lapa, lai skatītu šīs izmaiņas.) Šajā brīdī Globālā krājumu uzskaite ir gatava lietošanai.</span><span class="sxs-lookup"><span data-stu-id="7b056-175">(You might have to refresh the page to see this change.) At that point, Global Inventory Accounting is ready to use.</span></span>

## <a name="set-up-the-integration"></a><span data-ttu-id="7b056-176">Iestatiet integrēšanu</span><span class="sxs-lookup"><span data-stu-id="7b056-176">Set up the integration</span></span>

<span data-ttu-id="7b056-177">Veiciet šīs darbības, lai iestatītu integrāciju starp Globālo krājumu uzskaiti un Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7b056-177">Follow these steps to set up the integration between Global Inventory Accounting and Supply Chain Management.</span></span>

1. <span data-ttu-id="7b056-178">Pierakstieties Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7b056-178">Sign in to Supply Chain Management.</span></span>
1. <span data-ttu-id="7b056-179">Dodieties uz **Sistēmas administrēšana \> Līdzekļu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="7b056-179">Go to **System administration \> Feature Management**.</span></span>
1. <span data-ttu-id="7b056-180">Atlasiet **Pārbaudīt atjauninājumus**.</span><span class="sxs-lookup"><span data-stu-id="7b056-180">Select **Check for updates**.</span></span>
1. <span data-ttu-id="7b056-181">Cilnē **Viss** meklējiet līdzekli ar nosaukumu *Globāla krājumu uzskaite*.</span><span class="sxs-lookup"><span data-stu-id="7b056-181">On the **All** tab, search for the feature that is named *Global inventory accounting*.</span></span>
1. <span data-ttu-id="7b056-182">Atlasiet **Iespējot tagad**.</span><span class="sxs-lookup"><span data-stu-id="7b056-182">Select **Enable now**.</span></span>
1. <span data-ttu-id="7b056-183">Dodieties uz sadaļu **Globālā krājumu uzskaite \> Iestatīšana \> Globālās krājumu uzskaites parametri \> Integrācijas parametri**.</span><span class="sxs-lookup"><span data-stu-id="7b056-183">Go to **Global inventory accounting \> Setup \> Global inventory accounting parameters \> Integrations parameters**.</span></span>
1. <span data-ttu-id="7b056-184">Laukos **Datu pakalpojuma galapunkts** un **Globālās krājumu uzskaites galapunkts** ievadiet vietrāžus URL no e-pasta ziņojuma, ko Globālās krājumu uzskaites grupa nosūtīja, kad pierakstījieties priekšskatījumā.</span><span class="sxs-lookup"><span data-stu-id="7b056-184">In the **Data service endpoint** and **Global inventory accounting endpoint** fields, enter the URLs from the email that the Global Inventory Accounting team sent when you signed up for the preview.</span></span>

<span data-ttu-id="7b056-185">Globālā krājumu uzskaite tagad ir gatava lietošanai.</span><span class="sxs-lookup"><span data-stu-id="7b056-185">Global Inventory Accounting is now ready to use.</span></span>
