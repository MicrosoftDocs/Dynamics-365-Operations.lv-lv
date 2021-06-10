---
title: Integrācijas konfigurēšana ar Dayforce
description: Integrācija starp Microsoft Dynamics 365 Human Resources un Ceridian Dayforce balstās uz vairākām konfigurācijas darbībām, kas ir aprakstītas šajā rakstā. Pirms maksājuma izpildes apstrādes vispirms ir jākonfigurē integrācija gan Human Resources, gan Dayforce.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PersonnelIntegrationConfiguration
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d150daa92fe79cf6620ce5ddf1a01f369c64053
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051501"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="d8dda-104">Integrācijas konfigurēšana ar Dayforce</span><span class="sxs-lookup"><span data-stu-id="d8dda-104">Configure integration with Dayforce</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="d8dda-105">Integrācija starp Microsoft Dynamics 365 Human Resources un Ceridian Dayforce balstās uz vairākām konfigurācijas darbībām, kas ir aprakstītas šajā rakstā.</span><span class="sxs-lookup"><span data-stu-id="d8dda-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="d8dda-106">Pirms maksājuma izpildes apstrādes vispirms ir jākonfigurē integrācija gan Human Resources, gan Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d8dda-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="d8dda-107">Ja maksājumu izpildei izmantojat tādu pakalpojumu kā Dayforce, jāiespējo integrācija Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d8dda-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="d8dda-108">Integrācijai ir nepieciešami noteikti Human Resources dati.</span><span class="sxs-lookup"><span data-stu-id="d8dda-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="d8dda-109">Tādēļ ir jāpārliecinās, vai uz Dayforce kartētie dati Human Resources ir konfigurēti veidā, kas atbalsta integrāciju.</span><span class="sxs-lookup"><span data-stu-id="d8dda-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="d8dda-110">Integrācija izmanto tālāk norādītās vispārējās datu kategorijas.</span><span class="sxs-lookup"><span data-stu-id="d8dda-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="d8dda-111">Personāla vadības dati</span><span class="sxs-lookup"><span data-stu-id="d8dda-111">Human resources data</span></span>
- <span data-ttu-id="d8dda-112">Atlīdzības dati</span><span class="sxs-lookup"><span data-stu-id="d8dda-112">Compensation data</span></span>
- <span data-ttu-id="d8dda-113">Algu dati, piemēram, apmaksas cikli, apmaksas periodi un ienākumu veidu kodi</span><span class="sxs-lookup"><span data-stu-id="d8dda-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="d8dda-114">Nodarbināto dati</span><span class="sxs-lookup"><span data-stu-id="d8dda-114">Worker data</span></span>

<span data-ttu-id="d8dda-115">Šajā rakstā ir aprakstītas darbības, kas jāveic, lai iespējotu integrāciju.</span><span class="sxs-lookup"><span data-stu-id="d8dda-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="d8dda-116">Tajā ir arī izskaidrots, kādu veidu dati un konfigurācijas informācija ir nepieciešama integrācijai.</span><span class="sxs-lookup"><span data-stu-id="d8dda-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="d8dda-117">Integrācijas iespējošana</span><span class="sxs-lookup"><span data-stu-id="d8dda-117">Enable the integration</span></span>

<span data-ttu-id="d8dda-118">Lai pieslēgtos Dayforce, Human Resources ir jāieslēdz integrācija un jāievada konfigurācijas informācija.</span><span class="sxs-lookup"><span data-stu-id="d8dda-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="d8dda-119">Ja vēlaties, lai izveidotā Virsgrāmatas transakcija tiktu importēta programmā Microsoft Dynamics 365 Finance, ir jāiestata arī Microsoft Azure krātuves konts un programmā Finance jāievada Azure krātuves savienojuma virkne.</span><span class="sxs-lookup"><span data-stu-id="d8dda-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="d8dda-120">Lai Human Resources ieslēgtu integrāciju, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="d8dda-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="d8dda-121">Lapā **Sistēmas administrēšana** atlasiet opciju **Integrācijas konfigurēšana**.</span><span class="sxs-lookup"><span data-stu-id="d8dda-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="d8dda-122">Ievadiet drošo failu pārsūtīšanas protokola (FTP) galapunktu un drošo FTP mapes ceļu.</span><span class="sxs-lookup"><span data-stu-id="d8dda-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="d8dda-123">Ievadiet tā lietotāja lietotājvārdu un paroli, kurš piekļūs drošajam FTP galapunktam un mapes ceļam.</span><span class="sxs-lookup"><span data-stu-id="d8dda-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="d8dda-124">Pārbaudiet savienojumu, kā nepieciešams, un opciju **Iespējot algu aprēķina integrāciju** iestatiet uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="d8dda-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="d8dda-125">Kad integrācija ir ieslēgta, tiek izveidota datu eksportēšanas pakotne un faili, kā arī iestatīts biežums.</span><span class="sxs-lookup"><span data-stu-id="d8dda-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="d8dda-126">Biežumu varat mainīt atbilstoši vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="d8dda-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="d8dda-127">Papildinformāciju par Azure krātuves kontiem un Azure krātuves savienojuma virknēm skatiet tālāk minētajos Azure rakstos.</span><span class="sxs-lookup"><span data-stu-id="d8dda-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="d8dda-128">Par Azure krātuves kontiem</span><span class="sxs-lookup"><span data-stu-id="d8dda-128">About Azure storage accounts</span></span>](/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="d8dda-129">Azure krātuves savienojuma virkņu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="d8dda-129">Configure Azure Storage connection strings</span></span>](/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="d8dda-130">Tehniskā informācija par algu aprēķina integrācijas iespējošanu</span><span class="sxs-lookup"><span data-stu-id="d8dda-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="d8dda-131">Algu aprēķina integrācijas ieslēgšanai ir divi primārie iznākumi, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="d8dda-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="d8dda-132">Tiek izveidots datu eksportēšanas projekts ar nosaukumu “Algu aprēķina integrācijas eksportēšana”.</span><span class="sxs-lookup"><span data-stu-id="d8dda-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="d8dda-133">Šajā projektā ir iekļauti elementi un lauki, kas nepieciešami algu aprēķina integrācijai.</span><span class="sxs-lookup"><span data-stu-id="d8dda-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="d8dda-134">Lai pārbaudītu projektu, dodieties uz sadaļu **Sistēmas administrēšana**, atlasiet elementu **Datu pārvaldība** un pēc tam atveriet datu projektu no projektu saraksta.</span><span class="sxs-lookup"><span data-stu-id="d8dda-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="d8dda-135">Šis pakešuzdevums izpilda datu eksportēšanas projektu, šifrē iegūto datu pakotni un pārsūta datu pakotnes failu uz SFTP galapunktu, kas konfigurēts ekrānā **Integrācijas konfigurēšana**.</span><span class="sxs-lookup"><span data-stu-id="d8dda-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="d8dda-136">Datu pakotne, kas pārsūtīta uz SFTP galapunktu, tiek šifrēta, izmantojot pakotnes unikālo atslēgu.</span><span class="sxs-lookup"><span data-stu-id="d8dda-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="d8dda-137">Atslēga glabājas Azure Key Vault krātuvē, kam var piekļūt, tikai izmantojot Ceridian.</span><span class="sxs-lookup"><span data-stu-id="d8dda-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="d8dda-138">Nav iespējams atšifrēt un pārbaudīt datu pakotnes saturu.</span><span class="sxs-lookup"><span data-stu-id="d8dda-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="d8dda-139">Ja ir jāpārbauda datu pakotnes saturs, eksportējiet datu projektu “Algu aprēķina integrācijas eksportēšana” manuāli, lejupielādējiet to un pēc tam atveriet to.</span><span class="sxs-lookup"><span data-stu-id="d8dda-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="d8dda-140">Eksportējot manuāli, pakotne netiks šifrēta un pārsūtīta.</span><span class="sxs-lookup"><span data-stu-id="d8dda-140">Manual export will not apply encryption or transfer the package.</span></span>
> <span data-ttu-id="d8dda-141">Piemēram, ja integrācijas faili tiek sūtīti no Dynamics 365 Human Resources UAT vai smilškastes vides uz Ceridian Dayforce testa vidi, varat izmantot tālāk norādīto galveno akreditācijas datu komplekta URL: https://payrollintegrationprod.vault.azure.net.</span><span class="sxs-lookup"><span data-stu-id="d8dda-141">For instances where the integration files are sent from a Dynamics 365 Human Resources UAT or Sandbox environment to a Ceridian Dayforce Test environment, you can use the following key vault URL: https://payrollintegrationprod.vault.azure.net.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="d8dda-142">Datu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="d8dda-142">Configure your data</span></span> 

<span data-ttu-id="d8dda-143">Lai apstrādātu algas, Human Resources ir jākonfigurē personāla vadības dati.</span><span class="sxs-lookup"><span data-stu-id="d8dda-143">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="d8dda-144">Jums ir jāiestata organizācijas dati, piemēram, darbi un amati, kā arī informācija par atvieglojumiem un atlīdzību.</span><span class="sxs-lookup"><span data-stu-id="d8dda-144">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="d8dda-145">Šie dati nodrošina informāciju par nodarbinātību, samaksu un ieturējumiem, kas nepieciešama darbinieka algas ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="d8dda-145">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="d8dda-146">Personāla vadības dati</span><span class="sxs-lookup"><span data-stu-id="d8dda-146">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="d8dda-147">Atvieglojumi</span><span class="sxs-lookup"><span data-stu-id="d8dda-147">Benefits</span></span> 

<span data-ttu-id="d8dda-148">Personāla vadība nodrošina rīkus, ko var izmantot, lai iestatītu un uzturētu atvieglojumus, ieturējumus un nodarbināto atlīdzības plānus, ko organizācija piedāvā vai apstrādā saviem nodarbinātajiem.</span><span class="sxs-lookup"><span data-stu-id="d8dda-148">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="d8dda-149">Kad veidojat atvieglojumus, ņemiet vērā tālāk norādītos datus un konfigurācijas, kas tiek izmantoti pakalpojumā Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d8dda-149">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="d8dda-150">Atvieglojumu plāni</span><span class="sxs-lookup"><span data-stu-id="d8dda-150">Benefit plans</span></span>

- <span data-ttu-id="d8dda-151">Plāns (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-151">Plan (required)</span></span>
- <span data-ttu-id="d8dda-152">Tips (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-152">Type (required)</span></span>
- <span data-ttu-id="d8dda-153">Algas ietekme (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-153">Payroll impact (required)</span></span>
- <span data-ttu-id="d8dda-154">Atgūt nokavētos maksājumus</span><span class="sxs-lookup"><span data-stu-id="d8dda-154">Recover arrears</span></span>
- <span data-ttu-id="d8dda-155">Ieturējuma metode</span><span class="sxs-lookup"><span data-stu-id="d8dda-155">Deduction method</span></span>
- <span data-ttu-id="d8dda-156">Ieturējuma prioritāte</span><span class="sxs-lookup"><span data-stu-id="d8dda-156">Deduction priority</span></span>
- <span data-ttu-id="d8dda-157">Ierobežojuma periods</span><span class="sxs-lookup"><span data-stu-id="d8dda-157">Limit period</span></span>
- <span data-ttu-id="d8dda-158">Ierobežojuma summa</span><span class="sxs-lookup"><span data-stu-id="d8dda-158">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="d8dda-159">Atvieglojumi</span><span class="sxs-lookup"><span data-stu-id="d8dda-159">Benefits</span></span>

- <span data-ttu-id="d8dda-160">Plāns (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-160">Plan (required)</span></span>
- <span data-ttu-id="d8dda-161">Tips (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-161">Type (required)</span></span>
- <span data-ttu-id="d8dda-162">Opcija (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-162">Option (required)</span></span>
- <span data-ttu-id="d8dda-163">Atvieglojumu ID (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-163">Benefit ID (required)</span></span>
- <span data-ttu-id="d8dda-164">Biežums</span><span class="sxs-lookup"><span data-stu-id="d8dda-164">Frequency</span></span>
- <span data-ttu-id="d8dda-165">Pamats</span><span class="sxs-lookup"><span data-stu-id="d8dda-165">Basis</span></span>
- <span data-ttu-id="d8dda-166">Summa vai likme</span><span class="sxs-lookup"><span data-stu-id="d8dda-166">Amount or rate</span></span>
- <span data-ttu-id="d8dda-167">Ienākumu veida kods</span><span class="sxs-lookup"><span data-stu-id="d8dda-167">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="d8dda-168">Atbalstītās biežuma vērtības</span><span class="sxs-lookup"><span data-stu-id="d8dda-168">Supported frequencies</span></span> 

- <span data-ttu-id="d8dda-169">Katru nedēļu</span><span class="sxs-lookup"><span data-stu-id="d8dda-169">Weekly</span></span>
- <span data-ttu-id="d8dda-170">Katru otro nedēļu</span><span class="sxs-lookup"><span data-stu-id="d8dda-170">Bi-weekly</span></span>
- <span data-ttu-id="d8dda-171">Pusmēneša</span><span class="sxs-lookup"><span data-stu-id="d8dda-171">Semi-monthly</span></span>
- <span data-ttu-id="d8dda-172">Mēnesis</span><span class="sxs-lookup"><span data-stu-id="d8dda-172">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="d8dda-173">Atbalstītās pamata vērtības</span><span class="sxs-lookup"><span data-stu-id="d8dda-173">Supported bases</span></span> 

- <span data-ttu-id="d8dda-174">Fiksēta summa</span><span class="sxs-lookup"><span data-stu-id="d8dda-174">Fixed amount</span></span>
- <span data-ttu-id="d8dda-175">Ienākumu procentuālais daudzums</span><span class="sxs-lookup"><span data-stu-id="d8dda-175">Percent of earnings</span></span>
- <span data-ttu-id="d8dda-176">Produktīvās stundas</span><span class="sxs-lookup"><span data-stu-id="d8dda-176">Productive hours</span></span>

<span data-ttu-id="d8dda-177">Dayforce izveido tālāk norādītos ieturējumus, pamatojoties uz atvieglojumu plānā definēto algas ietekmi.</span><span class="sxs-lookup"><span data-stu-id="d8dda-177">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="d8dda-178">Atlasīšana Human Resources</span><span class="sxs-lookup"><span data-stu-id="d8dda-178">Selection in Human Resources</span></span>        | <span data-ttu-id="d8dda-179">Rezultāts pakalpojumā Dayforce</span><span class="sxs-lookup"><span data-stu-id="d8dda-179">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="d8dda-180">Nav</span><span class="sxs-lookup"><span data-stu-id="d8dda-180">None</span></span>                       | <span data-ttu-id="d8dda-181">Nav izveidots neviens ieturējums.</span><span class="sxs-lookup"><span data-stu-id="d8dda-181">No deduction is created.</span></span>                      |
| <span data-ttu-id="d8dda-182">Tikai ieturējums</span><span class="sxs-lookup"><span data-stu-id="d8dda-182">Deduction only</span></span>             | <span data-ttu-id="d8dda-183">Ir izveidots darbinieka ieturējums.</span><span class="sxs-lookup"><span data-stu-id="d8dda-183">An employee deduction is created.</span></span>             |
| <span data-ttu-id="d8dda-184">Tikai segums</span><span class="sxs-lookup"><span data-stu-id="d8dda-184">Contribution only</span></span>          | <span data-ttu-id="d8dda-185">Ir izveidots darba devēja ieturējums.</span><span class="sxs-lookup"><span data-stu-id="d8dda-185">An employer deduction is created.</span></span>             |
| <span data-ttu-id="d8dda-186">Ieturējums un segums</span><span class="sxs-lookup"><span data-stu-id="d8dda-186">Deduction and contribution</span></span> | <span data-ttu-id="d8dda-187">Ir izveidots darbinieka un darba devēja ieturējums.</span><span class="sxs-lookup"><span data-stu-id="d8dda-187">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="d8dda-188">Papildinformāciju par atvieglojumu programmas definēšanu un pārvaldību skatiet tālāk minētajos rakstos.</span><span class="sxs-lookup"><span data-stu-id="d8dda-188">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="d8dda-189">Darbinieku atvieglojumu programmas nodrošināšana</span><span class="sxs-lookup"><span data-stu-id="d8dda-189">Deliver an employee benefits program</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="d8dda-190">Izveidot jaunu atvieglojumu</span><span class="sxs-lookup"><span data-stu-id="d8dda-190">Create a new benefit</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="d8dda-191">Atvieglojumu piemērotības kārtulu un ierobežojumu definēšana</span><span class="sxs-lookup"><span data-stu-id="d8dda-191">Define benefit eligibility rules and policies</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="d8dda-192">Atvieglojumu reģistrēšana un noņemšana nodarbinātajiem</span><span class="sxs-lookup"><span data-stu-id="d8dda-192">Enroll and remove benefits from workers</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="d8dda-193">Atlīdzība</span><span class="sxs-lookup"><span data-stu-id="d8dda-193">Compensation</span></span> 

<span data-ttu-id="d8dda-194">Atlīdzību pārvaldība tiek izmantota, lai kontrolētu pamatalgas un prēmiju izsniegšanu.</span><span class="sxs-lookup"><span data-stu-id="d8dda-194">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="d8dda-195">Darbinieka fiksētā pamatalga un nopelnu palielinājumi tiek kontrolēti, izmantojot fiksētas atlīdzības plānus.</span><span class="sxs-lookup"><span data-stu-id="d8dda-195">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="d8dda-196">Veicināšanas maksājumu izsniegšana, piemēram, prēmiju maksājumi, apbalvojumi par sasniegumiem, uzņēmuma akciju iegādes iespējas un dotācijas, kā arī vienreizējas piemaksas, tiek kontrolētas ar mainīgās atlīdzības plāniem.</span><span class="sxs-lookup"><span data-stu-id="d8dda-196">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="d8dda-197">Dayforce izmanto atlīdzības informāciju, lai aprēķinātu darbinieka stundas vai gada likmi.</span><span class="sxs-lookup"><span data-stu-id="d8dda-197">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="d8dda-198">Ir jānorāda fiksētās atlīdzības plāni un apmaksas likmes konvertēšanas gadījumi.</span><span class="sxs-lookup"><span data-stu-id="d8dda-198">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="d8dda-199">Darbiniekiem ir jābūt saistītiem ar fiksētās atlīdzības plānu.</span><span class="sxs-lookup"><span data-stu-id="d8dda-199">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="d8dda-200">Papildinformāciju par atlīdzības plāniem skatiet tālāk minētajos rakstos.</span><span class="sxs-lookup"><span data-stu-id="d8dda-200">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="d8dda-201">Fiksētās atlīdzības plānu izveidošana</span><span class="sxs-lookup"><span data-stu-id="d8dda-201">Create fixed compensation plans</span></span>](/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="d8dda-202">Mainīgās atlīdzības plānu izveidošana</span><span class="sxs-lookup"><span data-stu-id="d8dda-202">Create variable compensation plans</span></span>](/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="d8dda-203">Algas/atlīdzības organizācijas un plānu izstrāde</span><span class="sxs-lookup"><span data-stu-id="d8dda-203">Develop salary/compensation structure and plans</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="d8dda-204">Procesa kompensācija</span><span class="sxs-lookup"><span data-stu-id="d8dda-204">Process compensation</span></span>](/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="d8dda-205">Atlīdzības procesa definēšana un rezultātu aprēķināšana</span><span class="sxs-lookup"><span data-stu-id="d8dda-205">Define compensation process and calculate results</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="d8dda-206">Darbinieka reģistrēšana fiksētās atlīdzības plānā</span><span class="sxs-lookup"><span data-stu-id="d8dda-206">Enroll an employee in a fixed compensation plan</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="d8dda-207">Darbinieka reģistrēšana mainīgās atlīdzības plānā</span><span class="sxs-lookup"><span data-stu-id="d8dda-207">Enroll an employee in a variable compensation plan</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="d8dda-208">Darbi</span><span class="sxs-lookup"><span data-stu-id="d8dda-208">Jobs</span></span> 

<span data-ttu-id="d8dda-209">Darbs ir uzdevumu un atbildības jomu kopums, kas ir jāizpilda personai, kura veic darbu.</span><span class="sxs-lookup"><span data-stu-id="d8dda-209">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="d8dda-210">Papildinformāciju skatiet tālāk minētajos rakstos.</span><span class="sxs-lookup"><span data-stu-id="d8dda-210">For more information, see the following articles:</span></span>

- [<span data-ttu-id="d8dda-211">Darba komponentu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="d8dda-211">Setting up the components of a job</span></span>](/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="d8dda-212">Jaunu darbu definēšana</span><span class="sxs-lookup"><span data-stu-id="d8dda-212">Define new jobs</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="d8dda-213">Amati</span><span class="sxs-lookup"><span data-stu-id="d8dda-213">Positions</span></span>

<span data-ttu-id="d8dda-214">Pozīcija ir atsevišķa darba instance.</span><span class="sxs-lookup"><span data-stu-id="d8dda-214">A position is an individual instance of a job.</span></span> <span data-ttu-id="d8dda-215">Piemēram, amats Pārdošanas daļas vadītājs (austrumu reģions) ir tikai viens no amatiem, kas ir saistīti ar darbu Pārdošanas daļas vadītājs.</span><span class="sxs-lookup"><span data-stu-id="d8dda-215">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="d8dda-216">Amats pastāv nodaļā.</span><span class="sxs-lookup"><span data-stu-id="d8dda-216">A position exists in a department.</span></span> <span data-ttu-id="d8dda-217">Ar katru amatu var būt saistīts tikai viens nodarbinātais.</span><span class="sxs-lookup"><span data-stu-id="d8dda-217">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="d8dda-218">Iestatot jaunus amatus, ņemiet vērā tālāk norādītos datus un konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="d8dda-218">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="d8dda-219">Amats (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-219">Position (required)</span></span>
- <span data-ttu-id="d8dda-220">Apraksts (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-220">Description (required)</span></span>
- <span data-ttu-id="d8dda-221">Darbs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-221">Job (required)</span></span>
- <span data-ttu-id="d8dda-222">Nodaļa (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-222">Department (required)</span></span>
- <span data-ttu-id="d8dda-223">Amata veids (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-223">Position type (required)</span></span>
- <span data-ttu-id="d8dda-224">Pilnas slodzes ekvivalents</span><span class="sxs-lookup"><span data-stu-id="d8dda-224">Full-time equivalent</span></span>
- <span data-ttu-id="d8dda-225">Ikgadējās parastās stundas (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-225">Annual regular hours (required)</span></span>
- <span data-ttu-id="d8dda-226">Apmaksātāja juridiskā persona (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-226">Paid by legal entity (required)</span></span>
- <span data-ttu-id="d8dda-227">Apmaksas cikls (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-227">Pay cycle (required)</span></span>
- <span data-ttu-id="d8dda-228">Noklusējuma finanšu dimensija — izmaksu centrs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-228">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="d8dda-229">Nodarbinātā piešķire — nodarbinātais, piešķires sākums, piešķires beigas, iemesla kods</span><span class="sxs-lookup"><span data-stu-id="d8dda-229">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="d8dda-230">Ja vienā nodaļā ar to pašu darbu ir saistīti vairāki amati, tie pakalpojumā Dayforce tiek apvienoti vienā amatā.</span><span class="sxs-lookup"><span data-stu-id="d8dda-230">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="d8dda-231">Papildinformāciju skatiet tālāk minētajos rakstos.</span><span class="sxs-lookup"><span data-stu-id="d8dda-231">For more information, see the following articles:</span></span>

- [<span data-ttu-id="d8dda-232">Darbaspēka organizēšana, izmantojot nodaļas, darbus un amatus</span><span class="sxs-lookup"><span data-stu-id="d8dda-232">Organize your workforce using departments, jobs, and positions</span></span>](/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="d8dda-233">Amatu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="d8dda-233">Set up positions</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="d8dda-234">Nodaļas</span><span class="sxs-lookup"><span data-stu-id="d8dda-234">Departments</span></span>

<span data-ttu-id="d8dda-235">Nodaļa ir pārvaldības struktūrvienība, kas pārstāv organizācijas kategoriju vai funkcionālo apgabalu.</span><span class="sxs-lookup"><span data-stu-id="d8dda-235">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="d8dda-236">Nodaļa ir atbildīga par noteiktu organizācijas jomu, piemēram, pārdošanu, uzskaiti vai personāla vadību.</span><span class="sxs-lookup"><span data-stu-id="d8dda-236">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="d8dda-237">Nodaļas var izmantot, lai ziņotu par funkcionālām jomām.</span><span class="sxs-lookup"><span data-stu-id="d8dda-237">You can use departments to report on functional areas.</span></span> <span data-ttu-id="d8dda-238">Nodaļām var būt peļņas un zaudējumu atbildība.</span><span class="sxs-lookup"><span data-stu-id="d8dda-238">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="d8dda-239">Papildinformāciju skatiet tālāk minētajos rakstos.</span><span class="sxs-lookup"><span data-stu-id="d8dda-239">For more information, see the following articles:</span></span>

- [<span data-ttu-id="d8dda-240">Nodaļas izveide un tās saistīšana ar nodaļu hierarhiju</span><span class="sxs-lookup"><span data-stu-id="d8dda-240">Create a department and associate it with the department hierarchy</span></span>](/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="d8dda-241">Jaunu nodaļu definēšana</span><span class="sxs-lookup"><span data-stu-id="d8dda-241">Define new departments</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="d8dda-242">Apmaksas cikli un apmaksas periodi</span><span class="sxs-lookup"><span data-stu-id="d8dda-242">Pay cycles and pay periods</span></span>

<span data-ttu-id="d8dda-243">Apmaksas cikls nosaka, cik bieži tiek veikts algu aprēķins, kā arī konkrētās dienas, kurās nodarbinātie saņem samaksu.</span><span class="sxs-lookup"><span data-stu-id="d8dda-243">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="d8dda-244">Apmaksas cikls var būt, piemēram, ikmēneša, un darbinieki samaksu var saņemt mēneša pēdējā dienā.</span><span class="sxs-lookup"><span data-stu-id="d8dda-244">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="d8dda-245">Vai arī apmaksas cikls var būt iknedēļas, un darbinieki samaksu var saņemt otrdienā pēc apmaksas perioda beigām.</span><span class="sxs-lookup"><span data-stu-id="d8dda-245">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="d8dda-246">Apmaksas cikli tiek piešķirti amatiem, lai kontrolētu to, kad nodarbinātie šajos amatos saņems samaksu.</span><span class="sxs-lookup"><span data-stu-id="d8dda-246">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="d8dda-247">Pēc apmaksas ciklu izveides katram ciklam varat ģenerēt apmaksas periodus.</span><span class="sxs-lookup"><span data-stu-id="d8dda-247">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="d8dda-248">Katrā apmaksas periodā ir ietverts noklusējuma maksājuma datums, kura pamatā ir jūsu sniegtā informācija.</span><span class="sxs-lookup"><span data-stu-id="d8dda-248">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="d8dda-249">Taču varat modificēt apmaksas perioda noklusējuma maksājuma datumu izņēmumu iestatīšanai, piemēram, kad maksājuma datums ir brīvdienā.</span><span class="sxs-lookup"><span data-stu-id="d8dda-249">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="d8dda-250">Dayforce izmanto tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="d8dda-250">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="d8dda-251">Apmaksas cikls (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-251">Pay cycle (required)</span></span>
- <span data-ttu-id="d8dda-252">Apmaksas cikla biežums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-252">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="d8dda-253">Perioda sākuma datums (ir jānorāda pirmais apmaksas periods)</span><span class="sxs-lookup"><span data-stu-id="d8dda-253">Period start date (first pay period required)</span></span>
- <span data-ttu-id="d8dda-254">Noklusējuma maksājuma datums (ir jānorāda pirmais apmaksas periods)</span><span class="sxs-lookup"><span data-stu-id="d8dda-254">Default payment date (first pay period required)</span></span>

<span data-ttu-id="d8dda-255">Šī informācija pakalpojumā Dayforce ir integrēta kā apmaksas grupas, un katram apmaksas ciklam to atdala valsts vai reģions.</span><span class="sxs-lookup"><span data-stu-id="d8dda-255">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="d8dda-256">Pirms integrācijas ir jābūt ģenerētam vismaz vienam apmaksas periodam.</span><span class="sxs-lookup"><span data-stu-id="d8dda-256">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="d8dda-257">Dayforce ģenerē apmaksas grupu kalendārus un maksājumu datumus atbilstoši Human Resources iestatītajam pirmā apmaksas perioda sākuma datumam un noklusējuma maksājuma datumam.</span><span class="sxs-lookup"><span data-stu-id="d8dda-257">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="d8dda-258">Ienākumu veida kodi</span><span class="sxs-lookup"><span data-stu-id="d8dda-258">Earning codes</span></span>

<span data-ttu-id="d8dda-259">Ienākumu veidu kodi unikāli identificē katra veida ienākumus, ko saņem nodarbinātie.</span><span class="sxs-lookup"><span data-stu-id="d8dda-259">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="d8dda-260">Kodiem ir dažādi ar ienākumiem saistīti parametri, piemēram, uzskaites nosacījumi, nodokļu likumi, pārskatu veidošanas prasības un bruto summas palielināšanas iespēja.</span><span class="sxs-lookup"><span data-stu-id="d8dda-260">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="d8dda-261">Dayforce izmanto tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="d8dda-261">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="d8dda-262">Ienākumu veida kods (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-262">Earning Code (required)</span></span>
- <span data-ttu-id="d8dda-263">apraksts</span><span class="sxs-lookup"><span data-stu-id="d8dda-263">Description</span></span>
- <span data-ttu-id="d8dda-264">Mērvienība</span><span class="sxs-lookup"><span data-stu-id="d8dda-264">Unit of measure</span></span>
- <span data-ttu-id="d8dda-265">Produktīvs</span><span class="sxs-lookup"><span data-stu-id="d8dda-265">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="d8dda-266">Nodarbināto dati</span><span class="sxs-lookup"><span data-stu-id="d8dda-266">Worker data</span></span>

<span data-ttu-id="d8dda-267">Dažādo veidu nodarbināto ieraksti ir svarīga informācija personāla vadības un algu sistēmās.</span><span class="sxs-lookup"><span data-stu-id="d8dda-267">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="d8dda-268">Ievadīto informāciju var izmantot, lai sekotu nodarbinātajiem un personiskajai informācijai.</span><span class="sxs-lookup"><span data-stu-id="d8dda-268">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="d8dda-269">Par darbiniekiem var saglabāt tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="d8dda-269">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="d8dda-270">**Pamata** — saglabājiet pamata informāciju par darbinieku, piemēram, kontaktinformāciju, demogrāfisko informāciju, identifikācijas informāciju, ģimenes informāciju, karadienesta statusu, ekspatriantu informāciju, kā arī personiskās un ārkārtas kontaktpersonas.</span><span class="sxs-lookup"><span data-stu-id="d8dda-270">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="d8dda-271">**Nodarbinātība** — saglabājiet informāciju par darbinieka nodarbinātību, piemēram, informāciju par piederību uzņēmumam vai organizācijai, amata piešķiri, sākuma un beigu datumiem, piemērotību darbam, nodarbinātības noteikumiem, pensiju, atvaļinājumu un pārcelšanu.</span><span class="sxs-lookup"><span data-stu-id="d8dda-271">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="d8dda-272">**Atvaļinājumi un kavējumi** — saglabājiet informāciju par nodarbinātā kavējumiem, piemēram, informāciju par darba kalendāriem, kavējumu darbībām un kavējumu iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="d8dda-272">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="d8dda-273">**Atlīdzība un alga** — saglabājiet informāciju par nodarbinātā atlīdzības plāniem un algas informāciju, piemēram, plāna reģistrāciju, piemaksām, sniegumu, komisiju, nodokļu informāciju, pensionēšanos un ieturējumiem no algas.</span><span class="sxs-lookup"><span data-stu-id="d8dda-273">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="d8dda-274">Ievadot informāciju par nodarbināto, ņemiet vērā tālāk norādītos datus un konfigurācijas, kas tiek izmantoti pakalpojumā Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d8dda-274">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="d8dda-275">Vispārīgā informācija</span><span class="sxs-lookup"><span data-stu-id="d8dda-275">General information</span></span>

- <span data-ttu-id="d8dda-276">Personāla numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-276">Personnel number (required)</span></span>
- <span data-ttu-id="d8dda-277">Vārds (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-277">First name (required)</span></span>
- <span data-ttu-id="d8dda-278">Uzvārds (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-278">Last name (required)</span></span>
- <span data-ttu-id="d8dda-279">Otrais vārds</span><span class="sxs-lookup"><span data-stu-id="d8dda-279">Middle name</span></span>
- <span data-ttu-id="d8dda-280">Darba stāža datums</span><span class="sxs-lookup"><span data-stu-id="d8dda-280">Seniority date</span></span>
- <span data-ttu-id="d8dda-281">Zināms kā</span><span class="sxs-lookup"><span data-stu-id="d8dda-281">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="d8dda-282">Personiskā informācija</span><span class="sxs-lookup"><span data-stu-id="d8dda-282">Personal information</span></span>

- <span data-ttu-id="d8dda-283">Ģimenes stāvoklis (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-283">Marital status (required)</span></span>
- <span data-ttu-id="d8dda-284">Dzimšanas datums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-284">Birth date (required)</span></span>
- <span data-ttu-id="d8dda-285">Dzimums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-285">Gender (required)</span></span>
- <span data-ttu-id="d8dda-286">Persona ar īpašām vajadzībām</span><span class="sxs-lookup"><span data-stu-id="d8dda-286">Person with disabilities</span></span>
- <span data-ttu-id="d8dda-287">Nacionalitātes valsts/reģions (tikai Meksikai)</span><span class="sxs-lookup"><span data-stu-id="d8dda-287">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="d8dda-288">Adreses informācija</span><span class="sxs-lookup"><span data-stu-id="d8dda-288">Address information</span></span>

- <span data-ttu-id="d8dda-289">Primārā (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-289">Primary (required)</span></span>
- <span data-ttu-id="d8dda-290">Valsts/reģions (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-290">Country/region (required)</span></span>
- <span data-ttu-id="d8dda-291">Pasta indekss (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-291">Postal code (required)</span></span>
- <span data-ttu-id="d8dda-292">Ielas numurs (obligāti) (tikai Meksikai)</span><span class="sxs-lookup"><span data-stu-id="d8dda-292">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="d8dda-293">Mājas numurs/nosaukums (tikai Meksikai)</span><span class="sxs-lookup"><span data-stu-id="d8dda-293">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="d8dda-294">Pilsēta (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-294">City (required)</span></span>
- <span data-ttu-id="d8dda-295">Administratīvais apgabals (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-295">State (required)</span></span>
- <span data-ttu-id="d8dda-296">Apgabals (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-296">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="d8dda-297">Kontaktinformācija</span><span class="sxs-lookup"><span data-stu-id="d8dda-297">Contact information</span></span> 

- <span data-ttu-id="d8dda-298">Primārā (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-298">Primary (required)</span></span>
- <span data-ttu-id="d8dda-299">Kontaktpersonas tālrunis (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-299">Contact number (required)</span></span>
- <span data-ttu-id="d8dda-300">Paplašinājums</span><span class="sxs-lookup"><span data-stu-id="d8dda-300">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="d8dda-301">Algas informācija un ienākumu veidu kodi</span><span class="sxs-lookup"><span data-stu-id="d8dda-301">Payroll information and earning codes</span></span>

<span data-ttu-id="d8dda-302">Darbiniekiem var būt piešķirti konkrēti ienākumu veidi konkrētajā maksājumu biežumā, kā arī var būt norādīta vēlamā maksāšanas metode.</span><span class="sxs-lookup"><span data-stu-id="d8dda-302">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="d8dda-303">Lai palīdzētu nodrošināt, ka šīs preferences un iestatījumi tiek izmantoti, pakalpojumā Dayforce ir tālāk norādītie lauki.</span><span class="sxs-lookup"><span data-stu-id="d8dda-303">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="d8dda-304">Ienākumu veida kodi</span><span class="sxs-lookup"><span data-stu-id="d8dda-304">Earning codes</span></span>

- <span data-ttu-id="d8dda-305">Amats (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-305">Position (required)</span></span>
- <span data-ttu-id="d8dda-306">Ienākumu veida kods (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-306">Earning Code (required)</span></span>
- <span data-ttu-id="d8dda-307">Biežums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-307">Frequency (required)</span></span>
- <span data-ttu-id="d8dda-308">Summa (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-308">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="d8dda-309">Algas informācija</span><span class="sxs-lookup"><span data-stu-id="d8dda-309">Payroll information</span></span>

- <span data-ttu-id="d8dda-310">Maksāšanas metode</span><span class="sxs-lookup"><span data-stu-id="d8dda-310">Payment Method</span></span>
- <span data-ttu-id="d8dda-311">Ekonomiskais reģions (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-311">Economic Region (required)</span></span>
- <span data-ttu-id="d8dda-312">Darbinieka atvieglojumu ID</span><span class="sxs-lookup"><span data-stu-id="d8dda-312">Employee Benefits ID</span></span>
- <span data-ttu-id="d8dda-313">Nacionālais ID numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-313">National ID Number (required)</span></span>
- <span data-ttu-id="d8dda-314">Karadienesta numurs</span><span class="sxs-lookup"><span data-stu-id="d8dda-314">Military Service Number</span></span>
- <span data-ttu-id="d8dda-315">Maiņas ID (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-315">Shift ID (required)</span></span>
- <span data-ttu-id="d8dda-316">Nodokļu numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-316">Tax Number (required)</span></span>
- <span data-ttu-id="d8dda-317">Arodbiedrības ID (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-317">Union ID (required)</span></span>
- <span data-ttu-id="d8dda-318">Darba dienas ID (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-318">Work Day ID (required)</span></span>
- <span data-ttu-id="d8dda-319">Darba atļaujas numurs</span><span class="sxs-lookup"><span data-stu-id="d8dda-319">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="d8dda-320">Meksika atbalsta šādas maksāšanas metodes: **Skaidra nauda**, **Čeks** (uzņēmuma fiziskais čeks) un **Elektroniskais maksājums**.</span><span class="sxs-lookup"><span data-stu-id="d8dda-320">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="d8dda-321">Ja nav norādīta neviena maksāšanas metode, pēc noklusējuma tiek izmantota opcija **Čeks**.</span><span class="sxs-lookup"><span data-stu-id="d8dda-321">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="d8dda-322">Nodarbinātības papildinformācija</span><span class="sxs-lookup"><span data-stu-id="d8dda-322">Employment details</span></span>

<span data-ttu-id="d8dda-323">Nodarbinātības datu vēsture pakalpojumā Dayforce tiek izmantota kā galvenā informācija, no kuras tiek iegūts darbinieka darbā pieņemšanas, darba attiecību izbeigšanas un atkārtotas pieņemšanas darbā statuss.</span><span class="sxs-lookup"><span data-stu-id="d8dda-323">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="d8dda-324">Dayforce vienlaikus atbalsta tikai vienu aktīvu nodarbinātības ierakstu.</span><span class="sxs-lookup"><span data-stu-id="d8dda-324">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="d8dda-325">Nodarbinātības sākuma datums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-325">Employment start date (required)</span></span>
- <span data-ttu-id="d8dda-326">Nodarbinātības beigu datums</span><span class="sxs-lookup"><span data-stu-id="d8dda-326">Employment end date</span></span>
- <span data-ttu-id="d8dda-327">Pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="d8dda-327">Start date</span></span>
- <span data-ttu-id="d8dda-328">Koriģētais pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="d8dda-328">Adjusted start date</span></span>
- <span data-ttu-id="d8dda-329">Darba attiecību pārtraukšanas datums (jānorāda, kad tiek pārtrauktas darba attiecības)</span><span class="sxs-lookup"><span data-stu-id="d8dda-329">Termination date (required upon termination)</span></span>
- <span data-ttu-id="d8dda-330">Darba attiecību pārtraukšanas iemesls (jānorāda, kad tiek pārtrauktas darba attiecības)</span><span class="sxs-lookup"><span data-stu-id="d8dda-330">Termination reason (required upon termination)</span></span>

<span data-ttu-id="d8dda-331">Darbinieka galvenie datumi tiek iegūti, izmantojot tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="d8dda-331">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="d8dda-332">Personāla vadība</span><span class="sxs-lookup"><span data-stu-id="d8dda-332">Human Resources</span></span>                | <span data-ttu-id="d8dda-333">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d8dda-333">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8dda-334">Pēdējais nomas datums</span><span class="sxs-lookup"><span data-stu-id="d8dda-334">Most recent hire date</span></span> | <span data-ttu-id="d8dda-335">Pašreizējā nepārtrauktās nodarbinātības vēstures ieraksta nodarbinātības sākums</span><span class="sxs-lookup"><span data-stu-id="d8dda-335">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="d8dda-336">Izbeigšanas datums</span><span class="sxs-lookup"><span data-stu-id="d8dda-336">Termination date</span></span>      | <span data-ttu-id="d8dda-337">Pašreizējā nepārtrauktās nodarbinātības vēstures ieraksta darba attiecību pārtraukšanas datums</span><span class="sxs-lookup"><span data-stu-id="d8dda-337">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="d8dda-338">Pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="d8dda-338">Start date</span></span>            | <span data-ttu-id="d8dda-339">Pašreizējā neaktīvā nodarbinātības vēstures ieraksta koriģētais sākuma datums, sākuma datums vai nodarbinātības sākums</span><span class="sxs-lookup"><span data-stu-id="d8dda-339">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="d8dda-340">Sākotnējais darbā pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="d8dda-340">Original hire date</span></span>    | <span data-ttu-id="d8dda-341">Agrākā nodarbinātības vēstures ieraksta nodarbinātības sākums</span><span class="sxs-lookup"><span data-stu-id="d8dda-341">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="d8dda-342">Atlīdzība</span><span class="sxs-lookup"><span data-stu-id="d8dda-342">Compensation</span></span>

<span data-ttu-id="d8dda-343">Fiksētās atlīdzības plānam ir jābūt saistītam ar katra darbinieka primāro amatu visā nodarbinātības periodā.</span><span class="sxs-lookup"><span data-stu-id="d8dda-343">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="d8dda-344">Šis periods sākas ar datumu, kurā darbinieks tika pieņemts darbā (vai nodarbinātības sākuma datumu), un turpinās līdz darba attiecību pārtraukšanai.</span><span class="sxs-lookup"><span data-stu-id="d8dda-344">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="d8dda-345">Spēkā stāšanās datums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-345">Effective Date (required)</span></span>
- <span data-ttu-id="d8dda-346">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="d8dda-346">Expiration date</span></span>
- <span data-ttu-id="d8dda-347">Apmaksas likme (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-347">Pay Rate (required)</span></span>
- <span data-ttu-id="d8dda-348">Apmaksas likmes konvertēšanas gadījumi (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-348">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="d8dda-349">Gada ekvivalents (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-349">Annual equivalent (required)</span></span>
- <span data-ttu-id="d8dda-350">Stundas ekvivalents (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-350">Hourly equivalent (required)</span></span>

<span data-ttu-id="d8dda-351">Ja darbiniekam ar stundas likmi ir vairāki amati, pakalpojumā Dayforce kā darbinieka līmeņa pamatlikme/alga tiek importēta primārā amata fiksētā atlīdzība.</span><span class="sxs-lookup"><span data-stu-id="d8dda-351">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="d8dda-352">To amatu, kas nav primārie, stundas likme tiek saglabāta pakalpojumā Dayforce attiecīgajā amatā.</span><span class="sxs-lookup"><span data-stu-id="d8dda-352">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="d8dda-353">Ja darbiniekam, kurš saņem algu, ir vairāki amati, kā darbinieka līmeņa pamatlikme/alga tiek iegūta un izmantota visu aktīvo amatu kopējā stundas likme un gada alga.</span><span class="sxs-lookup"><span data-stu-id="d8dda-353">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="d8dda-354">Identifikācijas numuri</span><span class="sxs-lookup"><span data-stu-id="d8dda-354">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="d8dda-355">Sociālās apdrošināšanas numurs</span><span class="sxs-lookup"><span data-stu-id="d8dda-355">Social Security identifier</span></span> 

<span data-ttu-id="d8dda-356">Katram darbiniekam ir jābūt vienam primārajam numuram.</span><span class="sxs-lookup"><span data-stu-id="d8dda-356">Every employee must have one primary identifier.</span></span> <span data-ttu-id="d8dda-357">Šī numura identifikācijas tipam ir jābūt **SAN**.</span><span class="sxs-lookup"><span data-stu-id="d8dda-357">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="d8dda-358">Pakalpojumā Dayforce tas tiek automātiski iegūts kā darbinieka sociālās apdrošināšanas numurs, kas ir jānorāda, kad darbinieks tiek pieņemts darbā.</span><span class="sxs-lookup"><span data-stu-id="d8dda-358">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="d8dda-359">Primārais (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-359">Primary (required)</span></span>
- <span data-ttu-id="d8dda-360">Identifikācijas tips = SAN</span><span class="sxs-lookup"><span data-stu-id="d8dda-360">Identification Type = "SSN"</span></span>
- <span data-ttu-id="d8dda-361">Izdošanas datums</span><span class="sxs-lookup"><span data-stu-id="d8dda-361">Issued Date</span></span>
- <span data-ttu-id="d8dda-362">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="d8dda-362">Expiration Date</span></span>

<span data-ttu-id="d8dda-363">Darbinieki var sniegt vairākus identifikācijas numurus, kuru identifikācijas tips ir **SAN**.</span><span class="sxs-lookup"><span data-stu-id="d8dda-363">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="d8dda-364">Taču pakalpojumā Dayforce tiek integrēts tikai ieraksts, kas ir atzīmēts kā **Primārais**, neatkarīgi no tā, vai šis numurs ir aktīvs vai tam ir beidzies derīgums.</span><span class="sxs-lookup"><span data-stu-id="d8dda-364">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="d8dda-365">Banku konti un izdevumi</span><span class="sxs-lookup"><span data-stu-id="d8dda-365">Bank accounts and disbursements</span></span>

<span data-ttu-id="d8dda-366">Jebkuram darbiniekam, kurš samaksu izvēlējies saņemt bankas konta pārskaitījuma veidā, ir jāievada derīga bankas konta informācija.</span><span class="sxs-lookup"><span data-stu-id="d8dda-366">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="d8dda-367">Personāla vadība</span><span class="sxs-lookup"><span data-stu-id="d8dda-367">Human Resources</span></span>                         | <span data-ttu-id="d8dda-368">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d8dda-368">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8dda-369">Bankas konta numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-369">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="d8dda-370">SWIFT kods (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-370">SWIFT code (required)</span></span>          | <span data-ttu-id="d8dda-371">Lauku **Bankas ID** izmanto, apstrādājot algas Meksikā.</span><span class="sxs-lookup"><span data-stu-id="d8dda-371">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="d8dda-372">Filiāles numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-372">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="d8dda-373">Bankas konta tips (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-373">Bank account type (required)</span></span>   | <span data-ttu-id="d8dda-374">Lauku **Konta tips** izmanto, apstrādājot algas Meksikā.</span><span class="sxs-lookup"><span data-stu-id="d8dda-374">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="d8dda-375">Atbalstītās vērtības ir, piemēram, **Norēķini** un **Algas**.</span><span class="sxs-lookup"><span data-stu-id="d8dda-375">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="d8dda-376">Darbiniekiem, kuri samaksu izvēlas saņemt bankas konta pārskaitījumu veidā, ir jāsniedz saite uz juridiskās personas, kuras primārā adrese ir Meksikā, atlikumu kontu, kas ir saistīts ar derīgu Meksikas bankas kontu.</span><span class="sxs-lookup"><span data-stu-id="d8dda-376">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="d8dda-377">Visi pārējie konti, kas nav atlikumu konti, tiek ignorēti.</span><span class="sxs-lookup"><span data-stu-id="d8dda-377">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="d8dda-378">Adreses informācija</span><span class="sxs-lookup"><span data-stu-id="d8dda-378">Address information</span></span>

<span data-ttu-id="d8dda-379">Katram darbiniekam ir jābūt vienai primārajai vietai.</span><span class="sxs-lookup"><span data-stu-id="d8dda-379">Every employee must have one primary location.</span></span> <span data-ttu-id="d8dda-380">Pakalpojumā Dayforce šī vieta tiek izmantota, lai nodokļu piemērošanas nolūkos noteiktu darbinieka primāro dzīvesvietu.</span><span class="sxs-lookup"><span data-stu-id="d8dda-380">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="d8dda-381">Primārā (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-381">Primary (required)</span></span>
- <span data-ttu-id="d8dda-382">Valsts/reģions (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-382">Country/region (required)</span></span>
- <span data-ttu-id="d8dda-383">Pasta indekss (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-383">Zip/postal code (required)</span></span>
- <span data-ttu-id="d8dda-384">Iela (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-384">Street (required)</span></span>
- <span data-ttu-id="d8dda-385">Ielas numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-385">Street Number (required)</span></span>
- <span data-ttu-id="d8dda-386">Mājas numurs/nosaukums</span><span class="sxs-lookup"><span data-stu-id="d8dda-386">Building Complement</span></span>
- <span data-ttu-id="d8dda-387">Pilsēta (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-387">City (required)</span></span>
- <span data-ttu-id="d8dda-388">Administratīvais apgabals (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-388">State (required)</span></span>
- <span data-ttu-id="d8dda-389">Apgabals (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-389">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="d8dda-390">Datu konfigurēšana algu ģenerēšanai Amerikas Savienotajās Valstīs un Kanādā</span><span class="sxs-lookup"><span data-stu-id="d8dda-390">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="d8dda-391">Ja ģenerējat algas darbiniekiem Amerikas Savienotajās Valstīs un Kanādā, ir jākonfigurē tālāk norādītie elementi.</span><span class="sxs-lookup"><span data-stu-id="d8dda-391">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="d8dda-392">Amatiem ir jānorāda nodaļas.</span><span class="sxs-lookup"><span data-stu-id="d8dda-392">Departments are required on positions.</span></span>
- <span data-ttu-id="d8dda-393">Izmaksu centri ir jāiestata kā finanšu dimensijas, un tiem ir jābūt pirmajiem elementiem noklusējuma finanšu dimensijas virknē.</span><span class="sxs-lookup"><span data-stu-id="d8dda-393">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="d8dda-394">Varat konfigurēt Human Resources, lai amatiem būtu jānorāda nodaļa.</span><span class="sxs-lookup"><span data-stu-id="d8dda-394">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="d8dda-395">Lai to izdarītu, pārejiet uz **Personāla vadības kopīgotie amati > Amati > Pieprasīt amatiem nodaļas**.</span><span class="sxs-lookup"><span data-stu-id="d8dda-395">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="d8dda-396">Ieteicams piemērot šo iestatījumu integrācijai.</span><span class="sxs-lookup"><span data-stu-id="d8dda-396">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="d8dda-397">Darba tipi</span><span class="sxs-lookup"><span data-stu-id="d8dda-397">Job types</span></span>

<span data-ttu-id="d8dda-398">Darbu veidi tiek izmantoti, lai līdzīgus darbus grupētu kategorijās.</span><span class="sxs-lookup"><span data-stu-id="d8dda-398">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="d8dda-399">Darbu veidi ir nepieciešami, lai apstrādātu algas Amerikas Savienotajās Valstīs un Kanādā.</span><span class="sxs-lookup"><span data-stu-id="d8dda-399">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="d8dda-400">Daži darbu veidu piemēri ir pilna laika, nepilna laika, algots un stundu apmaksas darbs.</span><span class="sxs-lookup"><span data-stu-id="d8dda-400">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="d8dda-401">Darbu veidi tiek kartēti uz pakalpojumu Dayforce kā apmaksas tipi, lai norādītu, vai darbinieks saņem stundas samaksu vai algu.</span><span class="sxs-lookup"><span data-stu-id="d8dda-401">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="d8dda-402">Ir jānorāda tālāk norādītie darbu veidi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="d8dda-402">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="d8dda-403">Darba veids</span><span class="sxs-lookup"><span data-stu-id="d8dda-403">Job type</span></span>   | <span data-ttu-id="d8dda-404">apraksts</span><span class="sxs-lookup"><span data-stu-id="d8dda-404">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="d8dda-405">Ik stundu</span><span class="sxs-lookup"><span data-stu-id="d8dda-405">Hourly</span></span>     | <span data-ttu-id="d8dda-406">Ik stundu</span><span class="sxs-lookup"><span data-stu-id="d8dda-406">Hourly</span></span>      |
| <span data-ttu-id="d8dda-407">Algots</span><span class="sxs-lookup"><span data-stu-id="d8dda-407">Salaried</span></span>   | <span data-ttu-id="d8dda-408">Algots</span><span class="sxs-lookup"><span data-stu-id="d8dda-408">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="d8dda-409">Amatu veidi</span><span class="sxs-lookup"><span data-stu-id="d8dda-409">Position types</span></span> 

<span data-ttu-id="d8dda-410">Amatu veidus izmanto, lai norādītu, vai amats ir pilna laika, nepilna laika vai cita veida darbs.</span><span class="sxs-lookup"><span data-stu-id="d8dda-410">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="d8dda-411">Amatu veidi tiek kartēti uz pakalpojumu Dayforce kā apmaksas klases, lai norādītu, vai darbinieks ir pilna laika vai nepilna laika darbinieks.</span><span class="sxs-lookup"><span data-stu-id="d8dda-411">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="d8dda-412">Ir jānorāda tālāk norādītie amatu veidi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="d8dda-412">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="d8dda-413">Amata tips</span><span class="sxs-lookup"><span data-stu-id="d8dda-413">Position type</span></span>   | <span data-ttu-id="d8dda-414">apraksts</span><span class="sxs-lookup"><span data-stu-id="d8dda-414">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="d8dda-415">Pilna laika</span><span class="sxs-lookup"><span data-stu-id="d8dda-415">Full-time</span></span>       | <span data-ttu-id="d8dda-416">Pilna laika darbinieks</span><span class="sxs-lookup"><span data-stu-id="d8dda-416">Full time employee</span></span> |
| <span data-ttu-id="d8dda-417">Nepilna laika</span><span class="sxs-lookup"><span data-stu-id="d8dda-417">Part-time</span></span>       | <span data-ttu-id="d8dda-418">Nepilna laika darbinieks</span><span class="sxs-lookup"><span data-stu-id="d8dda-418">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="d8dda-419">Iemeslu kodi</span><span class="sxs-lookup"><span data-stu-id="d8dda-419">Reason codes</span></span>

<span data-ttu-id="d8dda-420">Iemeslu kodi sniedz informāciju par darbinieka statusu.</span><span class="sxs-lookup"><span data-stu-id="d8dda-420">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="d8dda-421">Iemeslu kodu tiek kartēti uz pakalpojumu Dayforce kā statusa iemesli, kas norāda darbinieka amata vai nodarbinātības statusa izmaiņu iemeslu.</span><span class="sxs-lookup"><span data-stu-id="d8dda-421">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="d8dda-422">Ir jānorāda tālāk norādītie iemeslu kodi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="d8dda-422">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="d8dda-423">Iemeslu kodi</span><span class="sxs-lookup"><span data-stu-id="d8dda-423">Reason code</span></span>    | <span data-ttu-id="d8dda-424">apraksts</span><span class="sxs-lookup"><span data-stu-id="d8dda-424">Description</span></span>      | <span data-ttu-id="d8dda-425">Piemērojamie scenāriji</span><span class="sxs-lookup"><span data-stu-id="d8dda-425">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="d8dda-426">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="d8dda-426">RESIGNATION</span></span>    | <span data-ttu-id="d8dda-427">Atlūgums</span><span class="sxs-lookup"><span data-stu-id="d8dda-427">Resignation</span></span>      | <span data-ttu-id="d8dda-428">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="d8dda-428">Terminate worker</span></span>     |
| <span data-ttu-id="d8dda-429">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="d8dda-429">TERMINATION</span></span>    | <span data-ttu-id="d8dda-430">Izbeigšana</span><span class="sxs-lookup"><span data-stu-id="d8dda-430">Termination</span></span>      | <span data-ttu-id="d8dda-431">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="d8dda-431">Terminate worker</span></span>     |
| <span data-ttu-id="d8dda-432">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="d8dda-432">RETIREMENT</span></span>     | <span data-ttu-id="d8dda-433">Aiziešana pensijā</span><span class="sxs-lookup"><span data-stu-id="d8dda-433">Retirement</span></span>       | <span data-ttu-id="d8dda-434">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="d8dda-434">Terminate worker</span></span>     |
| <span data-ttu-id="d8dda-435">CITI</span><span class="sxs-lookup"><span data-stu-id="d8dda-435">OTHER</span></span>          | <span data-ttu-id="d8dda-436">Citi iemesli</span><span class="sxs-lookup"><span data-stu-id="d8dda-436">Other Reasons</span></span>    | <span data-ttu-id="d8dda-437">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="d8dda-437">Terminate worker</span></span>     |
| <span data-ttu-id="d8dda-438">DEATH</span><span class="sxs-lookup"><span data-stu-id="d8dda-438">DEATH</span></span>          | <span data-ttu-id="d8dda-439">Nāve</span><span class="sxs-lookup"><span data-stu-id="d8dda-439">Death</span></span>            | <span data-ttu-id="d8dda-440">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="d8dda-440">Terminate worker</span></span>     |
| <span data-ttu-id="d8dda-441">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="d8dda-441">LEAVEOFABSENCE</span></span> | <span data-ttu-id="d8dda-442">Atvaļinājums</span><span class="sxs-lookup"><span data-stu-id="d8dda-442">Leave of Absence</span></span> | <span data-ttu-id="d8dda-443">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="d8dda-443">Terminate worker</span></span>     |
| <span data-ttu-id="d8dda-444">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="d8dda-444">CONTRACTEND</span></span>    | <span data-ttu-id="d8dda-445">Līguma beigas</span><span class="sxs-lookup"><span data-stu-id="d8dda-445">End of Contract</span></span>  | <span data-ttu-id="d8dda-446">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="d8dda-446">Terminate worker</span></span>     |
| <span data-ttu-id="d8dda-447">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="d8dda-447">SALARYCHANGE</span></span>   | <span data-ttu-id="d8dda-448">Algas izmaiņas</span><span class="sxs-lookup"><span data-stu-id="d8dda-448">Change of Salary</span></span> | <span data-ttu-id="d8dda-449">Atlīdzība</span><span class="sxs-lookup"><span data-stu-id="d8dda-449">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="d8dda-450">Ģimenes stāvoklis</span><span class="sxs-lookup"><span data-stu-id="d8dda-450">Marital status</span></span>

<span data-ttu-id="d8dda-451">Ģimenes statusa vērtības tiek kartētas uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkotas uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="d8dda-451">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d8dda-452">Tālāk esošajā tabulā ir parādīts, kā ģimenes statusa vērtības tiek kartētas uz pakalpojumu Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d8dda-452">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="d8dda-453">Personāla vadība</span><span class="sxs-lookup"><span data-stu-id="d8dda-453">Human Resources</span></span>                 | <span data-ttu-id="d8dda-454">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d8dda-454">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="d8dda-455">Precējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="d8dda-455">Married</span></span>                | <span data-ttu-id="d8dda-456">Precējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="d8dda-456">Married</span></span>              |
| <span data-ttu-id="d8dda-457">Atsevišķs</span><span class="sxs-lookup"><span data-stu-id="d8dda-457">Single</span></span>                 | <span data-ttu-id="d8dda-458">Atsevišķs</span><span class="sxs-lookup"><span data-stu-id="d8dda-458">Single</span></span>               |
| <span data-ttu-id="d8dda-459">Atraitnis (-ne)</span><span class="sxs-lookup"><span data-stu-id="d8dda-459">Widowed</span></span>                | <span data-ttu-id="d8dda-460">Atraitnis (-ne)</span><span class="sxs-lookup"><span data-stu-id="d8dda-460">Widowed</span></span>              |
| <span data-ttu-id="d8dda-461">Šķīries (-usies)</span><span class="sxs-lookup"><span data-stu-id="d8dda-461">Divorced</span></span>               | <span data-ttu-id="d8dda-462">Šķīries (-usies)</span><span class="sxs-lookup"><span data-stu-id="d8dda-462">Divorced</span></span>             |
| <span data-ttu-id="d8dda-463">Reģistrētas attiecības</span><span class="sxs-lookup"><span data-stu-id="d8dda-463">Registered Partnership</span></span> | <span data-ttu-id="d8dda-464">Dzīvesbiedrs</span><span class="sxs-lookup"><span data-stu-id="d8dda-464">Domestic Partnership</span></span> |
| <span data-ttu-id="d8dda-465">Neviens</span><span class="sxs-lookup"><span data-stu-id="d8dda-465">None</span></span>                   | <span data-ttu-id="d8dda-466">Neviens</span><span class="sxs-lookup"><span data-stu-id="d8dda-466">None</span></span>                 |
| <span data-ttu-id="d8dda-467">Kopdzīve</span><span class="sxs-lookup"><span data-stu-id="d8dda-467">Cohabiting</span></span>             | <span data-ttu-id="d8dda-468">Kopdzīve</span><span class="sxs-lookup"><span data-stu-id="d8dda-468">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="d8dda-469">Dzimums</span><span class="sxs-lookup"><span data-stu-id="d8dda-469">Gender</span></span>

<span data-ttu-id="d8dda-470">Dzimuma apzīmējumi tiek kartēti uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkoti uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="d8dda-470">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d8dda-471">Tālāk esošajā tabulā ir parādīts, kā dzimuma apzīmējumi tiek kartēti uz pakalpojumu Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d8dda-471">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="d8dda-472">Personāla vadība</span><span class="sxs-lookup"><span data-stu-id="d8dda-472">Human Resources</span></span>       | <span data-ttu-id="d8dda-473">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d8dda-473">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="d8dda-474">Vīrietis</span><span class="sxs-lookup"><span data-stu-id="d8dda-474">Male</span></span>         | <span data-ttu-id="d8dda-475">Vīrietis</span><span class="sxs-lookup"><span data-stu-id="d8dda-475">Male</span></span>            |
| <span data-ttu-id="d8dda-476">Sieviete</span><span class="sxs-lookup"><span data-stu-id="d8dda-476">Female</span></span>       | <span data-ttu-id="d8dda-477">Sieviete</span><span class="sxs-lookup"><span data-stu-id="d8dda-477">Female</span></span>          |
| <span data-ttu-id="d8dda-478">Nav specifisks</span><span class="sxs-lookup"><span data-stu-id="d8dda-478">Non-specific</span></span> | <span data-ttu-id="d8dda-479">*Netiek atbalstīts*</span><span class="sxs-lookup"><span data-stu-id="d8dda-479">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="d8dda-480">Ienākumu veida kodi</span><span class="sxs-lookup"><span data-stu-id="d8dda-480">Earning codes</span></span>

<span data-ttu-id="d8dda-481">Ienākumu veidu kodi unikāli identificē katra veida ienākumus, ko saņem nodarbinātie.</span><span class="sxs-lookup"><span data-stu-id="d8dda-481">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="d8dda-482">Kodiem ir vairāki ar ienākumiem saistīti parametri, piemēram, uzskaites nosacījumi, nodokļu likumi, pārskatu veidošanas prasības un bruto summas palielināšanas iespēja.</span><span class="sxs-lookup"><span data-stu-id="d8dda-482">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="d8dda-483">Ja tiek izmantota neatbalstīta biežuma vērtība, aprēķinā pēc noklusējuma tiek lietota biežuma vērtība **Katra apmaksa**.</span><span class="sxs-lookup"><span data-stu-id="d8dda-483">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="d8dda-484">Atbalstītās biežuma vērtības</span><span class="sxs-lookup"><span data-stu-id="d8dda-484">Supported frequencies</span></span>

- <span data-ttu-id="d8dda-485">Visus</span><span class="sxs-lookup"><span data-stu-id="d8dda-485">All</span></span>
- <span data-ttu-id="d8dda-486">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="d8dda-486">EVERYPAY</span></span>
- <span data-ttu-id="d8dda-487">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="d8dda-487">EACHPAYPERIOD</span></span>
- <span data-ttu-id="d8dda-488">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="d8dda-488">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="d8dda-489">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="d8dda-489">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="d8dda-490">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="d8dda-490">1OFMTH</span></span>
- <span data-ttu-id="d8dda-491">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="d8dda-491">LASTOFMTH</span></span>
- <span data-ttu-id="d8dda-492">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="d8dda-492">2OFMTH</span></span>
- <span data-ttu-id="d8dda-493">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d8dda-493">3OFMTH</span></span>
- <span data-ttu-id="d8dda-494">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d8dda-494">4OFMTH</span></span>
- <span data-ttu-id="d8dda-495">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="d8dda-495">5OFMTH</span></span>
- <span data-ttu-id="d8dda-496">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="d8dda-496">1N2OFMTH</span></span>
- <span data-ttu-id="d8dda-497">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d8dda-497">3N4OFMTH</span></span>
- <span data-ttu-id="d8dda-498">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d8dda-498">1N3OFMTH</span></span>
- <span data-ttu-id="d8dda-499">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d8dda-499">1N4OFMTH</span></span>
- <span data-ttu-id="d8dda-500">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d8dda-500">2N3OFMTH</span></span>
- <span data-ttu-id="d8dda-501">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d8dda-501">2N4OFMTH</span></span>
- <span data-ttu-id="d8dda-502">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d8dda-502">1N2N3OFMTH</span></span>
- <span data-ttu-id="d8dda-503">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d8dda-503">1N2N4OFMTH</span></span>
- <span data-ttu-id="d8dda-504">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d8dda-504">1N3N4OFMTH</span></span>
- <span data-ttu-id="d8dda-505">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d8dda-505">2N3N4OFMTH</span></span>
- <span data-ttu-id="d8dda-506">1N2N3N4OFMTH–1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d8dda-506">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="d8dda-507">2N3N4N5OFMth–2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="d8dda-507">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="d8dda-508">1OFQTR–1OFQTR</span><span class="sxs-lookup"><span data-stu-id="d8dda-508">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="d8dda-509">LASTOFQTR–LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="d8dda-509">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="d8dda-510">LASTMTHOFQTR–LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="d8dda-510">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="d8dda-511">1OFYEAR–1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="d8dda-511">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="d8dda-512">LASTOFYEAR–LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="d8dda-512">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="d8dda-513">NOVNDECOFYEAR–NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="d8dda-513">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="d8dda-514">Adreses</span><span class="sxs-lookup"><span data-stu-id="d8dda-514">Addresses</span></span>

<span data-ttu-id="d8dda-515">Noteiktas valsts vai reģiona, administratīvā apgabala un apgabala (pašvaldības) kodu identifikācijai ir nepieciešami konkrēti formāti, ko var atpazīt pakalpojums Dayforce un valsts/reģiona pakalpojumu sniedzēji.</span><span class="sxs-lookup"><span data-stu-id="d8dda-515">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="d8dda-516">Lai gan pilsētu formāts var būt dažāds, katrai pilsētai ir jābūt saistītai ar administratīvo apgabalu.</span><span class="sxs-lookup"><span data-stu-id="d8dda-516">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="d8dda-517">Personāla vadība</span><span class="sxs-lookup"><span data-stu-id="d8dda-517">Human Resources</span></span>          | <span data-ttu-id="d8dda-518">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d8dda-518">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="d8dda-519">Valsts/reģions</span><span class="sxs-lookup"><span data-stu-id="d8dda-519">Country/Region</span></span>  | <span data-ttu-id="d8dda-520">Valsts kods</span><span class="sxs-lookup"><span data-stu-id="d8dda-520">Country Code</span></span>          |
| <span data-ttu-id="d8dda-521">Pasta indekss</span><span class="sxs-lookup"><span data-stu-id="d8dda-521">Zip/Postal Code</span></span> | <span data-ttu-id="d8dda-522">Pasta indekss</span><span class="sxs-lookup"><span data-stu-id="d8dda-522">Postal Code</span></span>           |
| <span data-ttu-id="d8dda-523">Administratīvais apgabals</span><span class="sxs-lookup"><span data-stu-id="d8dda-523">State</span></span>           | <span data-ttu-id="d8dda-524">Administratīvā apgabala kods</span><span class="sxs-lookup"><span data-stu-id="d8dda-524">State Code</span></span>            |
| <span data-ttu-id="d8dda-525">Pilsēta</span><span class="sxs-lookup"><span data-stu-id="d8dda-525">City</span></span>            | <span data-ttu-id="d8dda-526">Pilsēta</span><span class="sxs-lookup"><span data-stu-id="d8dda-526">City</span></span>                  |
| <span data-ttu-id="d8dda-527">Apgabals</span><span class="sxs-lookup"><span data-stu-id="d8dda-527">County</span></span>          | <span data-ttu-id="d8dda-528">Apgabals (pašvaldība)</span><span class="sxs-lookup"><span data-stu-id="d8dda-528">County (Municipality)</span></span> |
| <span data-ttu-id="d8dda-529">Iela</span><span class="sxs-lookup"><span data-stu-id="d8dda-529">Street</span></span>          | <span data-ttu-id="d8dda-530">Adreses 1. rinda</span><span class="sxs-lookup"><span data-stu-id="d8dda-530">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="d8dda-531">Nodokļu reģioni</span><span class="sxs-lookup"><span data-stu-id="d8dda-531">Tax regions</span></span>

<span data-ttu-id="d8dda-532">Nodokļu reģionus izmanto, lai noteiktu atbilstošos nodokļus, kas jāpiemēro, ģenerējot algu aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="d8dda-532">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="d8dda-533">Nodokļu reģioni tiek kartēti uz pakalpojumu Dayforce kā vietas adreses.</span><span class="sxs-lookup"><span data-stu-id="d8dda-533">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="d8dda-534">Noklusējuma nodokļu reģionam ir jābūt saistītam ar nodarbinātā aktīvo amatu.</span><span class="sxs-lookup"><span data-stu-id="d8dda-534">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="d8dda-535">Nodokļu reģions (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-535">Tax region (required)</span></span>
- <span data-ttu-id="d8dda-536">Valsts/reģions (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-536">Country/Region (required)</span></span>
- <span data-ttu-id="d8dda-537">Administratīvais apgabals (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-537">State (required)</span></span>
- <span data-ttu-id="d8dda-538">Apgabals</span><span class="sxs-lookup"><span data-stu-id="d8dda-538">County</span></span> 
- <span data-ttu-id="d8dda-539">Pilsēta (obligāti)</span><span class="sxs-lookup"><span data-stu-id="d8dda-539">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="d8dda-540">Datu konfigurēšana algu aprēķina ģenerēšanai Meksikā</span><span class="sxs-lookup"><span data-stu-id="d8dda-540">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="d8dda-541">Ja ģenerējat algas darbiniekiem Meksikā, ir jākonfigurē tālāk norādītie elementi.</span><span class="sxs-lookup"><span data-stu-id="d8dda-541">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="d8dda-542">Amatiem ir jānorāda nodaļas.</span><span class="sxs-lookup"><span data-stu-id="d8dda-542">Departments are required on positions.</span></span>
- <span data-ttu-id="d8dda-543">Izmaksu centri ir jāiestata kā finanšu dimensijas, un tiem ir jābūt pirmajiem elementiem noklusējuma finanšu dimensijas virknē.</span><span class="sxs-lookup"><span data-stu-id="d8dda-543">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="d8dda-544">Darba tipi</span><span class="sxs-lookup"><span data-stu-id="d8dda-544">Job types</span></span>

<span data-ttu-id="d8dda-545">Darbu veidi tiek izmantoti, lai līdzīgus darbus grupētu kategorijās.</span><span class="sxs-lookup"><span data-stu-id="d8dda-545">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="d8dda-546">Lai apstrādātu algas Meksikā, ir nepieciešami darbu veidi.</span><span class="sxs-lookup"><span data-stu-id="d8dda-546">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="d8dda-547">Daži darbu veidu piemēri ir pilna laika, nepilna laika, algots un stundu apmaksas darbs.</span><span class="sxs-lookup"><span data-stu-id="d8dda-547">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="d8dda-548">Darbu veidi tiek kartēti uz pakalpojumu Dayforce kā apmaksas tipi, lai norādītu, vai darbinieks saņem stundas samaksu vai algu.</span><span class="sxs-lookup"><span data-stu-id="d8dda-548">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="d8dda-549">Ir jānorāda tālāk norādītie darbu veidi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="d8dda-549">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="d8dda-550">Darba veids</span><span class="sxs-lookup"><span data-stu-id="d8dda-550">Job type</span></span>   | <span data-ttu-id="d8dda-551">apraksts</span><span class="sxs-lookup"><span data-stu-id="d8dda-551">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="d8dda-552">Ik stundu</span><span class="sxs-lookup"><span data-stu-id="d8dda-552">Hourly</span></span>     | <span data-ttu-id="d8dda-553">Stundu (MX)</span><span class="sxs-lookup"><span data-stu-id="d8dda-553">MX Hourly</span></span>   |
| <span data-ttu-id="d8dda-554">Algots</span><span class="sxs-lookup"><span data-stu-id="d8dda-554">Salaried</span></span>   | <span data-ttu-id="d8dda-555">Algots (MX)</span><span class="sxs-lookup"><span data-stu-id="d8dda-555">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="d8dda-556">Amatu veidi</span><span class="sxs-lookup"><span data-stu-id="d8dda-556">Position types</span></span> 

<span data-ttu-id="d8dda-557">Amatu veidus izmanto, lai norādītu, vai amats ir pilna laika, nepilna laika vai cita veida darbs.</span><span class="sxs-lookup"><span data-stu-id="d8dda-557">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="d8dda-558">Amatu veidi tiek kartēti uz pakalpojumu Dayforce kā apmaksas klases, lai norādītu, vai darbinieks ir pilna laika vai nepilna laika darbinieks.</span><span class="sxs-lookup"><span data-stu-id="d8dda-558">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="d8dda-559">Ir jānorāda tālāk norādītie amatu veidi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="d8dda-559">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="d8dda-560">Amata tips</span><span class="sxs-lookup"><span data-stu-id="d8dda-560">Position type</span></span>   | <span data-ttu-id="d8dda-561">apraksts</span><span class="sxs-lookup"><span data-stu-id="d8dda-561">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="d8dda-562">Pilna laika</span><span class="sxs-lookup"><span data-stu-id="d8dda-562">Full-time</span></span>       | <span data-ttu-id="d8dda-563">Pilna laika darbinieks</span><span class="sxs-lookup"><span data-stu-id="d8dda-563">Full time employee</span></span> |
| <span data-ttu-id="d8dda-564">Nepilna laika</span><span class="sxs-lookup"><span data-stu-id="d8dda-564">Part-time</span></span>       | <span data-ttu-id="d8dda-565">Nepilna laika darbinieks</span><span class="sxs-lookup"><span data-stu-id="d8dda-565">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="d8dda-566">Iemeslu kodi</span><span class="sxs-lookup"><span data-stu-id="d8dda-566">Reason codes</span></span>

<span data-ttu-id="d8dda-567">Iemeslu kodi sniedz informāciju par darbinieka statusu.</span><span class="sxs-lookup"><span data-stu-id="d8dda-567">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="d8dda-568">Iemeslu kodu tiek kartēti uz pakalpojumu Dayforce kā statusa iemesli, kas norāda darbinieka amata vai nodarbinātības statusa izmaiņu iemeslu.</span><span class="sxs-lookup"><span data-stu-id="d8dda-568">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="d8dda-569">Ir jānorāda tālāk norādītie iemeslu kodi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="d8dda-569">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="d8dda-570">Iemeslu kodi</span><span class="sxs-lookup"><span data-stu-id="d8dda-570">Reason code</span></span>            | <span data-ttu-id="d8dda-571">apraksts</span><span class="sxs-lookup"><span data-stu-id="d8dda-571">Description</span></span>                    | <span data-ttu-id="d8dda-572">Piemērojamie scenāriji</span><span class="sxs-lookup"><span data-stu-id="d8dda-572">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="d8dda-573">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="d8dda-573">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="d8dda-574">Aiziešana no amata pirms pirmās algas</span><span class="sxs-lookup"><span data-stu-id="d8dda-574">Departure before first payroll</span></span> | <span data-ttu-id="d8dda-575">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="d8dda-575">Terminate worker</span></span>     |
| <span data-ttu-id="d8dda-576">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="d8dda-576">RESIGNATION</span></span>            | <span data-ttu-id="d8dda-577">Atlūgums</span><span class="sxs-lookup"><span data-stu-id="d8dda-577">Resignation</span></span>                    | <span data-ttu-id="d8dda-578">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="d8dda-578">Terminate worker</span></span>     |
| <span data-ttu-id="d8dda-579">PENSION</span><span class="sxs-lookup"><span data-stu-id="d8dda-579">PENSION</span></span>                | <span data-ttu-id="d8dda-580">Pensija</span><span class="sxs-lookup"><span data-stu-id="d8dda-580">Pension</span></span>                        | <span data-ttu-id="d8dda-581">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="d8dda-581">Terminate worker</span></span>     |
| <span data-ttu-id="d8dda-582">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="d8dda-582">TERMINATION</span></span>            | <span data-ttu-id="d8dda-583">Izbeigšana</span><span class="sxs-lookup"><span data-stu-id="d8dda-583">Termination</span></span>                    | <span data-ttu-id="d8dda-584">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="d8dda-584">Terminate worker</span></span>     |
| <span data-ttu-id="d8dda-585">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="d8dda-585">RETIREMENT</span></span>             | <span data-ttu-id="d8dda-586">Aiziešana pensijā</span><span class="sxs-lookup"><span data-stu-id="d8dda-586">Retirement</span></span>                     | <span data-ttu-id="d8dda-587">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="d8dda-587">Terminate worker</span></span>     |
| <span data-ttu-id="d8dda-588">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="d8dda-588">ABSENTEE</span></span>               | <span data-ttu-id="d8dda-589">Darba kavētājs</span><span class="sxs-lookup"><span data-stu-id="d8dda-589">Absentee</span></span>                       | <span data-ttu-id="d8dda-590">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="d8dda-590">Terminate worker</span></span>     |
| <span data-ttu-id="d8dda-591">CITI</span><span class="sxs-lookup"><span data-stu-id="d8dda-591">OTHER</span></span>                  | <span data-ttu-id="d8dda-592">Citi iemesli</span><span class="sxs-lookup"><span data-stu-id="d8dda-592">Other Reasons</span></span>                  | <span data-ttu-id="d8dda-593">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="d8dda-593">Terminate worker</span></span>     |
| <span data-ttu-id="d8dda-594">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="d8dda-594">CLOSURE</span></span>                | <span data-ttu-id="d8dda-595">Uzņēmuma slēgšana</span><span class="sxs-lookup"><span data-stu-id="d8dda-595">Business Closure</span></span>               | <span data-ttu-id="d8dda-596">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="d8dda-596">Terminate worker</span></span>     |
| <span data-ttu-id="d8dda-597">DEATH</span><span class="sxs-lookup"><span data-stu-id="d8dda-597">DEATH</span></span>                  | <span data-ttu-id="d8dda-598">Nāve</span><span class="sxs-lookup"><span data-stu-id="d8dda-598">Death</span></span>                          | <span data-ttu-id="d8dda-599">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="d8dda-599">Terminate worker</span></span>     |
| <span data-ttu-id="d8dda-600">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="d8dda-600">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="d8dda-601">Atvaļinājums</span><span class="sxs-lookup"><span data-stu-id="d8dda-601">Leave of Absence</span></span>               | <span data-ttu-id="d8dda-602">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="d8dda-602">Terminate worker</span></span>     |
| <span data-ttu-id="d8dda-603">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="d8dda-603">CONTRACTEND</span></span>            | <span data-ttu-id="d8dda-604">Līguma beigas</span><span class="sxs-lookup"><span data-stu-id="d8dda-604">End of Contract</span></span>                | <span data-ttu-id="d8dda-605">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="d8dda-605">Terminate worker</span></span>     |
| <span data-ttu-id="d8dda-606">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="d8dda-606">SALARYCHANGE</span></span>           | <span data-ttu-id="d8dda-607">Algas izmaiņas</span><span class="sxs-lookup"><span data-stu-id="d8dda-607">Change of Salary</span></span>               | <span data-ttu-id="d8dda-608">Atlīdzība</span><span class="sxs-lookup"><span data-stu-id="d8dda-608">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="d8dda-609">Nodarbinātības noteikumi</span><span class="sxs-lookup"><span data-stu-id="d8dda-609">Terms of employment</span></span>

<span data-ttu-id="d8dda-610">Nodarbinātības noteikumus izmanto, lai izveidotu nodarbinātības noteikumu kategorijas.</span><span class="sxs-lookup"><span data-stu-id="d8dda-610">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="d8dda-611">Noteikumi tiek kartēti uz pakalpojumu Dayforce kā nodarbinātības rādītāju vērtības.</span><span class="sxs-lookup"><span data-stu-id="d8dda-611">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="d8dda-612">Ir nepieciešami tālāk norādītie nodarbinātības noteikumi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="d8dda-612">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="d8dda-613">Nodarbinātības noteikumi</span><span class="sxs-lookup"><span data-stu-id="d8dda-613">Terms of employment</span></span>   | <span data-ttu-id="d8dda-614">apraksts</span><span class="sxs-lookup"><span data-stu-id="d8dda-614">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="d8dda-615">Regulārs</span><span class="sxs-lookup"><span data-stu-id="d8dda-615">Regular</span></span>               | <span data-ttu-id="d8dda-616">Regulārs</span><span class="sxs-lookup"><span data-stu-id="d8dda-616">Regular</span></span>     |
| <span data-ttu-id="d8dda-617">Tieši</span><span class="sxs-lookup"><span data-stu-id="d8dda-617">Direct</span></span>                | <span data-ttu-id="d8dda-618">Tieši</span><span class="sxs-lookup"><span data-stu-id="d8dda-618">Direct</span></span>      |
| <span data-ttu-id="d8dda-619">Štažēšanās</span><span class="sxs-lookup"><span data-stu-id="d8dda-619">Internship</span></span>            | <span data-ttu-id="d8dda-620">Štažēšanās</span><span class="sxs-lookup"><span data-stu-id="d8dda-620">Internship</span></span>  |
| <span data-ttu-id="d8dda-621">Pastāvīga</span><span class="sxs-lookup"><span data-stu-id="d8dda-621">Permanent</span></span>             | <span data-ttu-id="d8dda-622">Pastāvīga</span><span class="sxs-lookup"><span data-stu-id="d8dda-622">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="d8dda-623">Ģimenes stāvoklis</span><span class="sxs-lookup"><span data-stu-id="d8dda-623">Marital status</span></span>

<span data-ttu-id="d8dda-624">Ģimenes statusa vērtības tiek kartētas uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkotas uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="d8dda-624">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d8dda-625">Tālāk esošajā tabulā ir parādīts, kā ģimenes statusa vērtības tiek kartētas uz pakalpojumu Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d8dda-625">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="d8dda-626">Personāla vadība</span><span class="sxs-lookup"><span data-stu-id="d8dda-626">Human Resources</span></span>                 | <span data-ttu-id="d8dda-627">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d8dda-627">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="d8dda-628">Precējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="d8dda-628">Married</span></span>                | <span data-ttu-id="d8dda-629">Precējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="d8dda-629">Married</span></span>                   |
| <span data-ttu-id="d8dda-630">Atsevišķs</span><span class="sxs-lookup"><span data-stu-id="d8dda-630">Single</span></span>                 | <span data-ttu-id="d8dda-631">Atsevišķs</span><span class="sxs-lookup"><span data-stu-id="d8dda-631">Single</span></span>                    |
| <span data-ttu-id="d8dda-632">Atraitnis (-ne)</span><span class="sxs-lookup"><span data-stu-id="d8dda-632">Widowed</span></span>                | <span data-ttu-id="d8dda-633">Atraitnis (-ne)</span><span class="sxs-lookup"><span data-stu-id="d8dda-633">Widowed</span></span>                   |
| <span data-ttu-id="d8dda-634">Šķīries (-usies)</span><span class="sxs-lookup"><span data-stu-id="d8dda-634">Divorced</span></span>               | <span data-ttu-id="d8dda-635">Šķīries (-usies)</span><span class="sxs-lookup"><span data-stu-id="d8dda-635">Divorced</span></span>                  |
| <span data-ttu-id="d8dda-636">Reģistrētas attiecības</span><span class="sxs-lookup"><span data-stu-id="d8dda-636">Registered Partnership</span></span> | <span data-ttu-id="d8dda-637">Dzīvesbiedrs</span><span class="sxs-lookup"><span data-stu-id="d8dda-637">Domestic Partnership</span></span>      |
| <span data-ttu-id="d8dda-638">Neviens</span><span class="sxs-lookup"><span data-stu-id="d8dda-638">None</span></span>                   | <span data-ttu-id="d8dda-639">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="d8dda-639">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="d8dda-640">Kopdzīve</span><span class="sxs-lookup"><span data-stu-id="d8dda-640">Cohabiting</span></span>             | <span data-ttu-id="d8dda-641">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="d8dda-641">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="d8dda-642">Dzimums</span><span class="sxs-lookup"><span data-stu-id="d8dda-642">Gender</span></span>

<span data-ttu-id="d8dda-643">Dzimuma apzīmējumi tiek kartēti uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkoti uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="d8dda-643">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d8dda-644">Tālāk esošajā tabulā ir parādīts, kā dzimuma apzīmējumi tiek kartēti uz pakalpojumu Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d8dda-644">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="d8dda-645">Personāla vadība</span><span class="sxs-lookup"><span data-stu-id="d8dda-645">Human Resources</span></span>       | <span data-ttu-id="d8dda-646">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d8dda-646">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="d8dda-647">Vīrietis</span><span class="sxs-lookup"><span data-stu-id="d8dda-647">Male</span></span>         | <span data-ttu-id="d8dda-648">Vīrietis</span><span class="sxs-lookup"><span data-stu-id="d8dda-648">Male</span></span>                      |
| <span data-ttu-id="d8dda-649">Sieviete</span><span class="sxs-lookup"><span data-stu-id="d8dda-649">Female</span></span>       | <span data-ttu-id="d8dda-650">Sieviete</span><span class="sxs-lookup"><span data-stu-id="d8dda-650">Female</span></span>                    |
| <span data-ttu-id="d8dda-651">Nav specifisks</span><span class="sxs-lookup"><span data-stu-id="d8dda-651">Non-specific</span></span> | <span data-ttu-id="d8dda-652">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="d8dda-652">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="d8dda-653">Maksājumu metode</span><span class="sxs-lookup"><span data-stu-id="d8dda-653">Payment method</span></span>

<span data-ttu-id="d8dda-654">Maksāšanas metodes darbiniekam un uzņēmumam ļauj aprakstīt, kā darbinieki saņems samaksu.</span><span class="sxs-lookup"><span data-stu-id="d8dda-654">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="d8dda-655">Maksāšanas metodes tiek kartētas uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkotas uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="d8dda-655">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d8dda-656">Tālāk esošajā tabulā ir parādīts, kā maksāšanas metodes tiek kartētas uz pakalpojumu Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d8dda-656">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="d8dda-657">Personāla vadība</span><span class="sxs-lookup"><span data-stu-id="d8dda-657">Human Resources</span></span>             | <span data-ttu-id="d8dda-658">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d8dda-658">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="d8dda-659">Kase</span><span class="sxs-lookup"><span data-stu-id="d8dda-659">Cash</span></span>               | <span data-ttu-id="d8dda-660">Kase</span><span class="sxs-lookup"><span data-stu-id="d8dda-660">Cash</span></span>                      |
| <span data-ttu-id="d8dda-661">Elektronisks maksājums</span><span class="sxs-lookup"><span data-stu-id="d8dda-661">Electronic Payment</span></span> | <span data-ttu-id="d8dda-662">Pārsūtījums</span><span class="sxs-lookup"><span data-stu-id="d8dda-662">Transfer</span></span>                  |
| <span data-ttu-id="d8dda-663">Pārbaudīt</span><span class="sxs-lookup"><span data-stu-id="d8dda-663">Check</span></span>              | <span data-ttu-id="d8dda-664">Čeks</span><span class="sxs-lookup"><span data-stu-id="d8dda-664">Cheque</span></span>                    |
| <span data-ttu-id="d8dda-665">Bankas vekselis</span><span class="sxs-lookup"><span data-stu-id="d8dda-665">Bank Draft</span></span>         | <span data-ttu-id="d8dda-666">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="d8dda-666">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="d8dda-667">Citi</span><span class="sxs-lookup"><span data-stu-id="d8dda-667">Other</span></span>              | <span data-ttu-id="d8dda-668">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="d8dda-668">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="d8dda-669">Bankas konta tips</span><span class="sxs-lookup"><span data-stu-id="d8dda-669">Bank account type</span></span>

<span data-ttu-id="d8dda-670">Bankas kontu tipus izmanto darbiniekiem sūtāmajiem elektroniskajiem maksājumiem.</span><span class="sxs-lookup"><span data-stu-id="d8dda-670">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="d8dda-671">Bankas kontu tipi tiek kartēti uz pakalpojumu Dayforce kā pārsūtīšanas konta informācija.</span><span class="sxs-lookup"><span data-stu-id="d8dda-671">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="d8dda-672">Bankas kontu tipi integrācijas laikā tiek atbilstoši tulkoti uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="d8dda-672">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="d8dda-673">Personāla vadība</span><span class="sxs-lookup"><span data-stu-id="d8dda-673">Human Resources</span></span>            | <span data-ttu-id="d8dda-674">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d8dda-674">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="d8dda-675">Kontroles konts</span><span class="sxs-lookup"><span data-stu-id="d8dda-675">Checking Account</span></span>  | <span data-ttu-id="d8dda-676">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="d8dda-676">CheckingAccount</span></span>           |
| <span data-ttu-id="d8dda-677">Algu konts</span><span class="sxs-lookup"><span data-stu-id="d8dda-677">Payroll Account</span></span>   | <span data-ttu-id="d8dda-678">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="d8dda-678">PayrollAccount</span></span>            |
| <span data-ttu-id="d8dda-679">Uzkrājumu konts</span><span class="sxs-lookup"><span data-stu-id="d8dda-679">Savings Account</span></span>   | <span data-ttu-id="d8dda-680">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="d8dda-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="d8dda-681">BankGirot konts</span><span class="sxs-lookup"><span data-stu-id="d8dda-681">BankGirot account</span></span> | <span data-ttu-id="d8dda-682">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="d8dda-682">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="d8dda-683">PlusGirot konts</span><span class="sxs-lookup"><span data-stu-id="d8dda-683">PlusGirot account</span></span> | <span data-ttu-id="d8dda-684">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="d8dda-684">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="d8dda-685">Ienākumu veida kodi</span><span class="sxs-lookup"><span data-stu-id="d8dda-685">Earning codes</span></span>

<span data-ttu-id="d8dda-686">Ienākumu veidu kodi unikāli identificē katra veida ienākumus, ko saņem nodarbinātie.</span><span class="sxs-lookup"><span data-stu-id="d8dda-686">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="d8dda-687">Kodiem ir vairāki ar ienākumiem saistīti parametri, piemēram, uzskaites nosacījumi, nodokļu likumi, pārskatu veidošanas prasības un bruto summas palielināšanas iespēja.</span><span class="sxs-lookup"><span data-stu-id="d8dda-687">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="d8dda-688">Ja tiek izmantota neatbalstīta biežuma vērtība, aprēķinā pēc noklusējuma tiek lietota biežuma vērtība **Katra apmaksa**.</span><span class="sxs-lookup"><span data-stu-id="d8dda-688">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="d8dda-689">Atbalstītās biežuma vērtības</span><span class="sxs-lookup"><span data-stu-id="d8dda-689">Supported frequencies</span></span>

- <span data-ttu-id="d8dda-690">Visus</span><span class="sxs-lookup"><span data-stu-id="d8dda-690">All</span></span>
- <span data-ttu-id="d8dda-691">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="d8dda-691">EVERYPAY</span></span>
- <span data-ttu-id="d8dda-692">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="d8dda-692">EACHPAYPERIOD</span></span>
- <span data-ttu-id="d8dda-693">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="d8dda-693">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="d8dda-694">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="d8dda-694">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="d8dda-695">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="d8dda-695">1OFMTH</span></span>
- <span data-ttu-id="d8dda-696">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="d8dda-696">LASTOFMTH</span></span>
- <span data-ttu-id="d8dda-697">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="d8dda-697">2OFMTH</span></span>
- <span data-ttu-id="d8dda-698">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d8dda-698">3OFMTH</span></span>
- <span data-ttu-id="d8dda-699">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d8dda-699">4OFMTH</span></span>
- <span data-ttu-id="d8dda-700">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="d8dda-700">5OFMTH</span></span>
- <span data-ttu-id="d8dda-701">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="d8dda-701">1N2OFMTH</span></span>
- <span data-ttu-id="d8dda-702">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d8dda-702">3N4OFMTH</span></span>
- <span data-ttu-id="d8dda-703">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d8dda-703">1N3OFMTH</span></span>
- <span data-ttu-id="d8dda-704">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d8dda-704">1N4OFMTH</span></span>
- <span data-ttu-id="d8dda-705">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d8dda-705">2N3OFMTH</span></span>
- <span data-ttu-id="d8dda-706">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d8dda-706">2N4OFMTH</span></span>
- <span data-ttu-id="d8dda-707">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d8dda-707">1N2N3OFMTH</span></span>
- <span data-ttu-id="d8dda-708">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d8dda-708">1N2N4OFMTH</span></span>
- <span data-ttu-id="d8dda-709">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d8dda-709">1N3N4OFMTH</span></span>
- <span data-ttu-id="d8dda-710">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d8dda-710">2N3N4OFMTH</span></span>
- <span data-ttu-id="d8dda-711">1N2N3N4OFMTH–1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d8dda-711">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="d8dda-712">2N3N4N5OFMth–2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="d8dda-712">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="d8dda-713">1OFQTR–1OFQTR</span><span class="sxs-lookup"><span data-stu-id="d8dda-713">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="d8dda-714">LASTOFQTR–LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="d8dda-714">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="d8dda-715">LASTMTHOFQTR–LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="d8dda-715">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="d8dda-716">1OFYEAR–1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="d8dda-716">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="d8dda-717">LASTOFYEAR–LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="d8dda-717">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="d8dda-718">NOVNDECOFYEAR–NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="d8dda-718">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="d8dda-719">Adreses</span><span class="sxs-lookup"><span data-stu-id="d8dda-719">Addresses</span></span>

<span data-ttu-id="d8dda-720">Noteiktas valsts vai reģiona, administratīvā apgabala un apgabala (pašvaldības) kodu identifikācijai ir nepieciešami konkrēti formāti, ko var atpazīt pakalpojums Dayforce un valsts/reģiona pakalpojumu sniedzēji.</span><span class="sxs-lookup"><span data-stu-id="d8dda-720">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="d8dda-721">Lai gan pilsētu formāts var būt dažāds, katrai pilsētai ir jābūt saistītai ar administratīvo apgabalu.</span><span class="sxs-lookup"><span data-stu-id="d8dda-721">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="d8dda-722">Personāla vadība</span><span class="sxs-lookup"><span data-stu-id="d8dda-722">Human Resources</span></span>              | <span data-ttu-id="d8dda-723">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d8dda-723">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="d8dda-724">Valsts/reģions</span><span class="sxs-lookup"><span data-stu-id="d8dda-724">Country/Region</span></span>      | <span data-ttu-id="d8dda-725">Valsts kods</span><span class="sxs-lookup"><span data-stu-id="d8dda-725">Country Code</span></span>          |
| <span data-ttu-id="d8dda-726">Pasta indekss</span><span class="sxs-lookup"><span data-stu-id="d8dda-726">Zip/Postal Code</span></span>     | <span data-ttu-id="d8dda-727">Pasta indekss</span><span class="sxs-lookup"><span data-stu-id="d8dda-727">Postal Code</span></span>           |
| <span data-ttu-id="d8dda-728">Administratīvais apgabals</span><span class="sxs-lookup"><span data-stu-id="d8dda-728">State</span></span>               | <span data-ttu-id="d8dda-729">Administratīvā apgabala kods</span><span class="sxs-lookup"><span data-stu-id="d8dda-729">State Code</span></span>            |
| <span data-ttu-id="d8dda-730">Pilsēta</span><span class="sxs-lookup"><span data-stu-id="d8dda-730">City</span></span>                | <span data-ttu-id="d8dda-731">Pilsēta</span><span class="sxs-lookup"><span data-stu-id="d8dda-731">City</span></span>                  |
| <span data-ttu-id="d8dda-732">Apgabals</span><span class="sxs-lookup"><span data-stu-id="d8dda-732">County</span></span>              | <span data-ttu-id="d8dda-733">Apgabals (pašvaldība)</span><span class="sxs-lookup"><span data-stu-id="d8dda-733">County (Municipality)</span></span> |
| <span data-ttu-id="d8dda-734">Iela</span><span class="sxs-lookup"><span data-stu-id="d8dda-734">Street</span></span>              | <span data-ttu-id="d8dda-735">Adreses 1. rinda</span><span class="sxs-lookup"><span data-stu-id="d8dda-735">Address Line 1</span></span>        |
| <span data-ttu-id="d8dda-736">Ielas numurs</span><span class="sxs-lookup"><span data-stu-id="d8dda-736">Street Number</span></span>       | <span data-ttu-id="d8dda-737">Adreses 2. rinda</span><span class="sxs-lookup"><span data-stu-id="d8dda-737">Address Line 2</span></span>        |
| <span data-ttu-id="d8dda-738">Mājas numurs/nosaukums</span><span class="sxs-lookup"><span data-stu-id="d8dda-738">Building Complement</span></span> | <span data-ttu-id="d8dda-739">Adreses 5. rinda</span><span class="sxs-lookup"><span data-stu-id="d8dda-739">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="d8dda-740">Pases numurs</span><span class="sxs-lookup"><span data-stu-id="d8dda-740">Passport number</span></span>

<span data-ttu-id="d8dda-741">Darbinieki var sniegt pases informāciju.</span><span class="sxs-lookup"><span data-stu-id="d8dda-741">Employees can declare passport information.</span></span> <span data-ttu-id="d8dda-742">Šīs informācijas identifikācijas tips ir **Pase**, un tā tiek integrēta pakalpojumā Dayforce kā daļa no darbinieka Meksikai specifiskās informācijas.</span><span class="sxs-lookup"><span data-stu-id="d8dda-742">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="d8dda-743">Identifikācijas tips = Pase</span><span class="sxs-lookup"><span data-stu-id="d8dda-743">Identification Type = "Passport"</span></span>
- <span data-ttu-id="d8dda-744">Izdošanas datums</span><span class="sxs-lookup"><span data-stu-id="d8dda-744">Issued Date</span></span>
- <span data-ttu-id="d8dda-745">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="d8dda-745">Expiration Date</span></span>

<span data-ttu-id="d8dda-746">Darbinieki var sniegt vairākus identifikācijas numurus, kuru identifikācijas tips ir **Pase**.</span><span class="sxs-lookup"><span data-stu-id="d8dda-746">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="d8dda-747">Taču pakalpojumā Dayforce tiek integrēts tikai pašreizējais aktīvais pases ieraksts.</span><span class="sxs-lookup"><span data-stu-id="d8dda-747">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="d8dda-748">Ja visiem pases ierakstiem ir beidzies derīgiem, pakalpojumā Dayforce tiek integrēta pēdējā izdotā pase.</span><span class="sxs-lookup"><span data-stu-id="d8dda-748">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]