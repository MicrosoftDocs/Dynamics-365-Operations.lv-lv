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
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1647b7fbf84a78051e745e918954df32a2e7e1dd
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890008"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="beb10-104">Integrācijas konfigurēšana ar Dayforce</span><span class="sxs-lookup"><span data-stu-id="beb10-104">Configure integration with Dayforce</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="beb10-105">Integrācija starp Microsoft Dynamics 365 Human Resources un Ceridian Dayforce balstās uz vairākām konfigurācijas darbībām, kas ir aprakstītas šajā rakstā.</span><span class="sxs-lookup"><span data-stu-id="beb10-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="beb10-106">Pirms maksājuma izpildes apstrādes vispirms ir jākonfigurē integrācija gan Human Resources, gan Dayforce.</span><span class="sxs-lookup"><span data-stu-id="beb10-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="beb10-107">Ja maksājumu izpildei izmantojat tādu pakalpojumu kā Dayforce, jāiespējo integrācija Human Resources.</span><span class="sxs-lookup"><span data-stu-id="beb10-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="beb10-108">Integrācijai ir nepieciešami noteikti Human Resources dati.</span><span class="sxs-lookup"><span data-stu-id="beb10-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="beb10-109">Tādēļ ir jāpārliecinās, vai uz Dayforce kartētie dati Human Resources ir konfigurēti veidā, kas atbalsta integrāciju.</span><span class="sxs-lookup"><span data-stu-id="beb10-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="beb10-110">Integrācija izmanto tālāk norādītās vispārējās datu kategorijas.</span><span class="sxs-lookup"><span data-stu-id="beb10-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="beb10-111">Personāla vadības dati</span><span class="sxs-lookup"><span data-stu-id="beb10-111">Human resources data</span></span>
- <span data-ttu-id="beb10-112">Atlīdzības dati</span><span class="sxs-lookup"><span data-stu-id="beb10-112">Compensation data</span></span>
- <span data-ttu-id="beb10-113">Algu dati, piemēram, apmaksas cikli, apmaksas periodi un ienākumu veidu kodi</span><span class="sxs-lookup"><span data-stu-id="beb10-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="beb10-114">Nodarbināto dati</span><span class="sxs-lookup"><span data-stu-id="beb10-114">Worker data</span></span>

<span data-ttu-id="beb10-115">Šajā rakstā ir aprakstītas darbības, kas jāveic, lai iespējotu integrāciju.</span><span class="sxs-lookup"><span data-stu-id="beb10-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="beb10-116">Tajā ir arī izskaidrots, kādu veidu dati un konfigurācijas informācija ir nepieciešama integrācijai.</span><span class="sxs-lookup"><span data-stu-id="beb10-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="beb10-117">Integrācijas iespējošana</span><span class="sxs-lookup"><span data-stu-id="beb10-117">Enable the integration</span></span>

<span data-ttu-id="beb10-118">Lai pieslēgtos Dayforce, Human Resources ir jāieslēdz integrācija un jāievada konfigurācijas informācija.</span><span class="sxs-lookup"><span data-stu-id="beb10-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="beb10-119">Ja vēlaties, lai izveidotā Virsgrāmatas transakcija tiktu importēta programmā Microsoft Dynamics 365 Finance, ir jāiestata arī Microsoft Azure krātuves konts un programmā Finance jāievada Azure krātuves savienojuma virkne.</span><span class="sxs-lookup"><span data-stu-id="beb10-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="beb10-120">Lai Human Resources ieslēgtu integrāciju, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="beb10-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="beb10-121">Lapā **Sistēmas administrēšana** atlasiet opciju **Integrācijas konfigurēšana**.</span><span class="sxs-lookup"><span data-stu-id="beb10-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="beb10-122">Ievadiet drošo failu pārsūtīšanas protokola (FTP) galapunktu un drošo FTP mapes ceļu.</span><span class="sxs-lookup"><span data-stu-id="beb10-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="beb10-123">Ievadiet tā lietotāja lietotājvārdu un paroli, kurš piekļūs drošajam FTP galapunktam un mapes ceļam.</span><span class="sxs-lookup"><span data-stu-id="beb10-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="beb10-124">Pārbaudiet savienojumu, kā nepieciešams, un opciju **Iespējot algu aprēķina integrāciju** iestatiet uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="beb10-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="beb10-125">Kad integrācija ir ieslēgta, tiek izveidota datu eksportēšanas pakotne un faili, kā arī iestatīts biežums.</span><span class="sxs-lookup"><span data-stu-id="beb10-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="beb10-126">Biežumu varat mainīt atbilstoši vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="beb10-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="beb10-127">Papildinformāciju par Azure krātuves kontiem un Azure krātuves savienojuma virknēm skatiet tālāk minētajos Azure rakstos.</span><span class="sxs-lookup"><span data-stu-id="beb10-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="beb10-128">Par Azure krātuves kontiem</span><span class="sxs-lookup"><span data-stu-id="beb10-128">About Azure storage accounts</span></span>](/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="beb10-129">Azure krātuves savienojuma virkņu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="beb10-129">Configure Azure Storage connection strings</span></span>](/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="beb10-130">Tehniskā informācija par algu aprēķina integrācijas iespējošanu</span><span class="sxs-lookup"><span data-stu-id="beb10-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="beb10-131">Algu aprēķina integrācijas ieslēgšanai ir divi primārie iznākumi, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="beb10-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="beb10-132">Tiek izveidots datu eksportēšanas projekts ar nosaukumu “Algu aprēķina integrācijas eksportēšana”.</span><span class="sxs-lookup"><span data-stu-id="beb10-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="beb10-133">Šajā projektā ir iekļauti elementi un lauki, kas nepieciešami algu aprēķina integrācijai.</span><span class="sxs-lookup"><span data-stu-id="beb10-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="beb10-134">Lai pārbaudītu projektu, dodieties uz sadaļu **Sistēmas administrēšana**, atlasiet elementu **Datu pārvaldība** un pēc tam atveriet datu projektu no projektu saraksta.</span><span class="sxs-lookup"><span data-stu-id="beb10-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="beb10-135">Šis pakešuzdevums izpilda datu eksportēšanas projektu, šifrē iegūto datu pakotni un pārsūta datu pakotnes failu uz SFTP galapunktu, kas konfigurēts ekrānā **Integrācijas konfigurēšana**.</span><span class="sxs-lookup"><span data-stu-id="beb10-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="beb10-136">Datu pakotne, kas pārsūtīta uz SFTP galapunktu, tiek šifrēta, izmantojot pakotnes unikālo atslēgu.</span><span class="sxs-lookup"><span data-stu-id="beb10-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="beb10-137">Atslēga glabājas Azure Key Vault krātuvē, kam var piekļūt, tikai izmantojot Ceridian.</span><span class="sxs-lookup"><span data-stu-id="beb10-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="beb10-138">Nav iespējams atšifrēt un pārbaudīt datu pakotnes saturu.</span><span class="sxs-lookup"><span data-stu-id="beb10-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="beb10-139">Ja ir jāpārbauda datu pakotnes saturs, eksportējiet datu projektu “Algu aprēķina integrācijas eksportēšana” manuāli, lejupielādējiet to un pēc tam atveriet to.</span><span class="sxs-lookup"><span data-stu-id="beb10-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="beb10-140">Eksportējot manuāli, pakotne netiks šifrēta un pārsūtīta.</span><span class="sxs-lookup"><span data-stu-id="beb10-140">Manual export will not apply encryption or transfer the package.</span></span>
> <span data-ttu-id="beb10-141">Piemēram, ja integrācijas faili tiek sūtīti no Dynamics 365 Human Resources UAT vai smilškastes vides uz Ceridian Dayforce testa vidi, varat izmantot tālāk norādīto galveno akreditācijas datu komplekta URL: https://payrollintegrationprod.vault.azure.net.</span><span class="sxs-lookup"><span data-stu-id="beb10-141">For instances where the integration files are sent from a Dynamics 365 Human Resources UAT or Sandbox environment to a Ceridian Dayforce Test environment, you can use the following key vault URL: https://payrollintegrationprod.vault.azure.net.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="beb10-142">Datu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="beb10-142">Configure your data</span></span> 

<span data-ttu-id="beb10-143">Lai apstrādātu algas, Human Resources ir jākonfigurē personāla vadības dati.</span><span class="sxs-lookup"><span data-stu-id="beb10-143">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="beb10-144">Jums ir jāiestata organizācijas dati, piemēram, darbi un amati, kā arī informācija par atvieglojumiem un atlīdzību.</span><span class="sxs-lookup"><span data-stu-id="beb10-144">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="beb10-145">Šie dati nodrošina informāciju par nodarbinātību, samaksu un ieturējumiem, kas nepieciešama darbinieka algas ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="beb10-145">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="beb10-146">Personāla vadības dati</span><span class="sxs-lookup"><span data-stu-id="beb10-146">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="beb10-147">Atvieglojumi</span><span class="sxs-lookup"><span data-stu-id="beb10-147">Benefits</span></span> 

<span data-ttu-id="beb10-148">Personāla vadība nodrošina rīkus, ko var izmantot, lai iestatītu un uzturētu atvieglojumus, ieturējumus un nodarbināto atlīdzības plānus, ko organizācija piedāvā vai apstrādā saviem nodarbinātajiem.</span><span class="sxs-lookup"><span data-stu-id="beb10-148">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="beb10-149">Kad veidojat atvieglojumus, ņemiet vērā tālāk norādītos datus un konfigurācijas, kas tiek izmantoti pakalpojumā Dayforce.</span><span class="sxs-lookup"><span data-stu-id="beb10-149">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="beb10-150">Atvieglojumu plāni</span><span class="sxs-lookup"><span data-stu-id="beb10-150">Benefit plans</span></span>

- <span data-ttu-id="beb10-151">Plāns (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-151">Plan (required)</span></span>
- <span data-ttu-id="beb10-152">Tips (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-152">Type (required)</span></span>
- <span data-ttu-id="beb10-153">Algas ietekme (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-153">Payroll impact (required)</span></span>
- <span data-ttu-id="beb10-154">Atgūt nokavētos maksājumus</span><span class="sxs-lookup"><span data-stu-id="beb10-154">Recover arrears</span></span>
- <span data-ttu-id="beb10-155">Ieturējuma metode</span><span class="sxs-lookup"><span data-stu-id="beb10-155">Deduction method</span></span>
- <span data-ttu-id="beb10-156">Ieturējuma prioritāte</span><span class="sxs-lookup"><span data-stu-id="beb10-156">Deduction priority</span></span>
- <span data-ttu-id="beb10-157">Ierobežojuma periods</span><span class="sxs-lookup"><span data-stu-id="beb10-157">Limit period</span></span>
- <span data-ttu-id="beb10-158">Ierobežojuma summa</span><span class="sxs-lookup"><span data-stu-id="beb10-158">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="beb10-159">Atvieglojumi</span><span class="sxs-lookup"><span data-stu-id="beb10-159">Benefits</span></span>

- <span data-ttu-id="beb10-160">Plāns (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-160">Plan (required)</span></span>
- <span data-ttu-id="beb10-161">Tips (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-161">Type (required)</span></span>
- <span data-ttu-id="beb10-162">Opcija (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-162">Option (required)</span></span>
- <span data-ttu-id="beb10-163">Atvieglojumu ID (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-163">Benefit ID (required)</span></span>
- <span data-ttu-id="beb10-164">Biežums</span><span class="sxs-lookup"><span data-stu-id="beb10-164">Frequency</span></span>
- <span data-ttu-id="beb10-165">Pamats</span><span class="sxs-lookup"><span data-stu-id="beb10-165">Basis</span></span>
- <span data-ttu-id="beb10-166">Summa vai likme</span><span class="sxs-lookup"><span data-stu-id="beb10-166">Amount or rate</span></span>
- <span data-ttu-id="beb10-167">Ienākumu veida kods</span><span class="sxs-lookup"><span data-stu-id="beb10-167">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="beb10-168">Atbalstītās biežuma vērtības</span><span class="sxs-lookup"><span data-stu-id="beb10-168">Supported frequencies</span></span> 

- <span data-ttu-id="beb10-169">Katru nedēļu</span><span class="sxs-lookup"><span data-stu-id="beb10-169">Weekly</span></span>
- <span data-ttu-id="beb10-170">Katru otro nedēļu</span><span class="sxs-lookup"><span data-stu-id="beb10-170">Bi-weekly</span></span>
- <span data-ttu-id="beb10-171">Pusmēneša</span><span class="sxs-lookup"><span data-stu-id="beb10-171">Semi-monthly</span></span>
- <span data-ttu-id="beb10-172">Mēnesis</span><span class="sxs-lookup"><span data-stu-id="beb10-172">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="beb10-173">Atbalstītās pamata vērtības</span><span class="sxs-lookup"><span data-stu-id="beb10-173">Supported bases</span></span> 

- <span data-ttu-id="beb10-174">Fiksēta summa</span><span class="sxs-lookup"><span data-stu-id="beb10-174">Fixed amount</span></span>
- <span data-ttu-id="beb10-175">Ienākumu procentuālais daudzums</span><span class="sxs-lookup"><span data-stu-id="beb10-175">Percent of earnings</span></span>
- <span data-ttu-id="beb10-176">Produktīvās stundas</span><span class="sxs-lookup"><span data-stu-id="beb10-176">Productive hours</span></span>

<span data-ttu-id="beb10-177">Dayforce izveido tālāk norādītos ieturējumus, pamatojoties uz atvieglojumu plānā definēto algas ietekmi.</span><span class="sxs-lookup"><span data-stu-id="beb10-177">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="beb10-178">Atlasīšana Human Resources</span><span class="sxs-lookup"><span data-stu-id="beb10-178">Selection in Human Resources</span></span>        | <span data-ttu-id="beb10-179">Rezultāts pakalpojumā Dayforce</span><span class="sxs-lookup"><span data-stu-id="beb10-179">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="beb10-180">Nav</span><span class="sxs-lookup"><span data-stu-id="beb10-180">None</span></span>                       | <span data-ttu-id="beb10-181">Nav izveidots neviens ieturējums.</span><span class="sxs-lookup"><span data-stu-id="beb10-181">No deduction is created.</span></span>                      |
| <span data-ttu-id="beb10-182">Tikai ieturējums</span><span class="sxs-lookup"><span data-stu-id="beb10-182">Deduction only</span></span>             | <span data-ttu-id="beb10-183">Ir izveidots darbinieka ieturējums.</span><span class="sxs-lookup"><span data-stu-id="beb10-183">An employee deduction is created.</span></span>             |
| <span data-ttu-id="beb10-184">Tikai segums</span><span class="sxs-lookup"><span data-stu-id="beb10-184">Contribution only</span></span>          | <span data-ttu-id="beb10-185">Ir izveidots darba devēja ieturējums.</span><span class="sxs-lookup"><span data-stu-id="beb10-185">An employer deduction is created.</span></span>             |
| <span data-ttu-id="beb10-186">Ieturējums un segums</span><span class="sxs-lookup"><span data-stu-id="beb10-186">Deduction and contribution</span></span> | <span data-ttu-id="beb10-187">Ir izveidots darbinieka un darba devēja ieturējums.</span><span class="sxs-lookup"><span data-stu-id="beb10-187">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="beb10-188">Papildinformāciju par atvieglojumu programmas definēšanu un pārvaldību skatiet tālāk minētajos rakstos.</span><span class="sxs-lookup"><span data-stu-id="beb10-188">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="beb10-189">Darbinieku atvieglojumu programmas nodrošināšana</span><span class="sxs-lookup"><span data-stu-id="beb10-189">Deliver an employee benefits program</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="beb10-190">Izveidot jaunu atvieglojumu</span><span class="sxs-lookup"><span data-stu-id="beb10-190">Create a new benefit</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="beb10-191">Atvieglojumu piemērotības kārtulu un ierobežojumu definēšana</span><span class="sxs-lookup"><span data-stu-id="beb10-191">Define benefit eligibility rules and policies</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="beb10-192">Atvieglojumu reģistrēšana un noņemšana nodarbinātajiem</span><span class="sxs-lookup"><span data-stu-id="beb10-192">Enroll and remove benefits from workers</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="beb10-193">Atlīdzība</span><span class="sxs-lookup"><span data-stu-id="beb10-193">Compensation</span></span> 

<span data-ttu-id="beb10-194">Atlīdzību pārvaldība tiek izmantota, lai kontrolētu pamatalgas un prēmiju izsniegšanu.</span><span class="sxs-lookup"><span data-stu-id="beb10-194">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="beb10-195">Darbinieka fiksētā pamatalga un nopelnu palielinājumi tiek kontrolēti, izmantojot fiksētas atlīdzības plānus.</span><span class="sxs-lookup"><span data-stu-id="beb10-195">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="beb10-196">Veicināšanas maksājumu izsniegšana, piemēram, prēmiju maksājumi, apbalvojumi par sasniegumiem, uzņēmuma akciju iegādes iespējas un dotācijas, kā arī vienreizējas piemaksas, tiek kontrolētas ar mainīgās atlīdzības plāniem.</span><span class="sxs-lookup"><span data-stu-id="beb10-196">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="beb10-197">Dayforce izmanto atlīdzības informāciju, lai aprēķinātu darbinieka stundas vai gada likmi.</span><span class="sxs-lookup"><span data-stu-id="beb10-197">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="beb10-198">Ir jānorāda fiksētās atlīdzības plāni un apmaksas likmes konvertēšanas gadījumi.</span><span class="sxs-lookup"><span data-stu-id="beb10-198">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="beb10-199">Darbiniekiem ir jābūt saistītiem ar fiksētās atlīdzības plānu.</span><span class="sxs-lookup"><span data-stu-id="beb10-199">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="beb10-200">Papildinformāciju par atlīdzības plāniem skatiet tālāk minētajos rakstos.</span><span class="sxs-lookup"><span data-stu-id="beb10-200">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="beb10-201">Fiksētās atlīdzības plānu izveidošana</span><span class="sxs-lookup"><span data-stu-id="beb10-201">Create fixed compensation plans</span></span>](/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="beb10-202">Mainīgās atlīdzības plānu izveidošana</span><span class="sxs-lookup"><span data-stu-id="beb10-202">Create variable compensation plans</span></span>](/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="beb10-203">Algas/atlīdzības organizācijas un plānu izstrāde</span><span class="sxs-lookup"><span data-stu-id="beb10-203">Develop salary/compensation structure and plans</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="beb10-204">Procesa kompensācija</span><span class="sxs-lookup"><span data-stu-id="beb10-204">Process compensation</span></span>](/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="beb10-205">Atlīdzības procesa definēšana un rezultātu aprēķināšana</span><span class="sxs-lookup"><span data-stu-id="beb10-205">Define compensation process and calculate results</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="beb10-206">Darbinieka reģistrēšana fiksētās atlīdzības plānā</span><span class="sxs-lookup"><span data-stu-id="beb10-206">Enroll an employee in a fixed compensation plan</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="beb10-207">Darbinieka reģistrēšana mainīgās atlīdzības plānā</span><span class="sxs-lookup"><span data-stu-id="beb10-207">Enroll an employee in a variable compensation plan</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="beb10-208">Darbi</span><span class="sxs-lookup"><span data-stu-id="beb10-208">Jobs</span></span> 

<span data-ttu-id="beb10-209">Darbs ir uzdevumu un atbildības jomu kopums, kas ir jāizpilda personai, kura veic darbu.</span><span class="sxs-lookup"><span data-stu-id="beb10-209">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="beb10-210">Papildinformāciju skatiet tālāk minētajos rakstos.</span><span class="sxs-lookup"><span data-stu-id="beb10-210">For more information, see the following articles:</span></span>

- [<span data-ttu-id="beb10-211">Darba komponentu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="beb10-211">Setting up the components of a job</span></span>](/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="beb10-212">Jaunu darbu definēšana</span><span class="sxs-lookup"><span data-stu-id="beb10-212">Define new jobs</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="beb10-213">Amati</span><span class="sxs-lookup"><span data-stu-id="beb10-213">Positions</span></span>

<span data-ttu-id="beb10-214">Pozīcija ir atsevišķa darba instance.</span><span class="sxs-lookup"><span data-stu-id="beb10-214">A position is an individual instance of a job.</span></span> <span data-ttu-id="beb10-215">Piemēram, amats Pārdošanas daļas vadītājs (austrumu reģions) ir tikai viens no amatiem, kas ir saistīti ar darbu Pārdošanas daļas vadītājs.</span><span class="sxs-lookup"><span data-stu-id="beb10-215">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="beb10-216">Amats pastāv nodaļā.</span><span class="sxs-lookup"><span data-stu-id="beb10-216">A position exists in a department.</span></span> <span data-ttu-id="beb10-217">Ar katru amatu var būt saistīts tikai viens nodarbinātais.</span><span class="sxs-lookup"><span data-stu-id="beb10-217">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="beb10-218">Iestatot jaunus amatus, ņemiet vērā tālāk norādītos datus un konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="beb10-218">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="beb10-219">Amats (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-219">Position (required)</span></span>
- <span data-ttu-id="beb10-220">Apraksts (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-220">Description (required)</span></span>
- <span data-ttu-id="beb10-221">Darbs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-221">Job (required)</span></span>
- <span data-ttu-id="beb10-222">Nodaļa (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-222">Department (required)</span></span>
- <span data-ttu-id="beb10-223">Amata veids (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-223">Position type (required)</span></span>
- <span data-ttu-id="beb10-224">Pilnas slodzes ekvivalents</span><span class="sxs-lookup"><span data-stu-id="beb10-224">Full-time equivalent</span></span>
- <span data-ttu-id="beb10-225">Ikgadējās parastās stundas (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-225">Annual regular hours (required)</span></span>
- <span data-ttu-id="beb10-226">Apmaksātāja juridiskā persona (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-226">Paid by legal entity (required)</span></span>
- <span data-ttu-id="beb10-227">Apmaksas cikls (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-227">Pay cycle (required)</span></span>
- <span data-ttu-id="beb10-228">Noklusējuma finanšu dimensija — izmaksu centrs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-228">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="beb10-229">Nodarbinātā piešķire — nodarbinātais, piešķires sākums, piešķires beigas, iemesla kods</span><span class="sxs-lookup"><span data-stu-id="beb10-229">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="beb10-230">Ja vienā nodaļā ar to pašu darbu ir saistīti vairāki amati, tie pakalpojumā Dayforce tiek apvienoti vienā amatā.</span><span class="sxs-lookup"><span data-stu-id="beb10-230">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="beb10-231">Papildinformāciju skatiet tālāk minētajos rakstos.</span><span class="sxs-lookup"><span data-stu-id="beb10-231">For more information, see the following articles:</span></span>

- [<span data-ttu-id="beb10-232">Darbaspēka organizēšana, izmantojot nodaļas, darbus un amatus</span><span class="sxs-lookup"><span data-stu-id="beb10-232">Organize your workforce using departments, jobs, and positions</span></span>](/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="beb10-233">Amatu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="beb10-233">Set up positions</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="beb10-234">Nodaļas</span><span class="sxs-lookup"><span data-stu-id="beb10-234">Departments</span></span>

<span data-ttu-id="beb10-235">Nodaļa ir pārvaldības struktūrvienība, kas pārstāv organizācijas kategoriju vai funkcionālo apgabalu.</span><span class="sxs-lookup"><span data-stu-id="beb10-235">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="beb10-236">Nodaļa ir atbildīga par noteiktu organizācijas jomu, piemēram, pārdošanu, uzskaiti vai personāla vadību.</span><span class="sxs-lookup"><span data-stu-id="beb10-236">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="beb10-237">Nodaļas var izmantot, lai ziņotu par funkcionālām jomām.</span><span class="sxs-lookup"><span data-stu-id="beb10-237">You can use departments to report on functional areas.</span></span> <span data-ttu-id="beb10-238">Nodaļām var būt peļņas un zaudējumu atbildība.</span><span class="sxs-lookup"><span data-stu-id="beb10-238">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="beb10-239">Papildinformāciju skatiet tālāk minētajos rakstos.</span><span class="sxs-lookup"><span data-stu-id="beb10-239">For more information, see the following articles:</span></span>

- [<span data-ttu-id="beb10-240">Nodaļas izveide un tās saistīšana ar nodaļu hierarhiju</span><span class="sxs-lookup"><span data-stu-id="beb10-240">Create a department and associate it with the department hierarchy</span></span>](/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="beb10-241">Jaunu nodaļu definēšana</span><span class="sxs-lookup"><span data-stu-id="beb10-241">Define new departments</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="beb10-242">Apmaksas cikli un apmaksas periodi</span><span class="sxs-lookup"><span data-stu-id="beb10-242">Pay cycles and pay periods</span></span>

<span data-ttu-id="beb10-243">Apmaksas cikls nosaka, cik bieži tiek veikts algu aprēķins, kā arī konkrētās dienas, kurās nodarbinātie saņem samaksu.</span><span class="sxs-lookup"><span data-stu-id="beb10-243">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="beb10-244">Apmaksas cikls var būt, piemēram, ikmēneša, un darbinieki samaksu var saņemt mēneša pēdējā dienā.</span><span class="sxs-lookup"><span data-stu-id="beb10-244">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="beb10-245">Vai arī apmaksas cikls var būt iknedēļas, un darbinieki samaksu var saņemt otrdienā pēc apmaksas perioda beigām.</span><span class="sxs-lookup"><span data-stu-id="beb10-245">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="beb10-246">Apmaksas cikli tiek piešķirti amatiem, lai kontrolētu to, kad nodarbinātie šajos amatos saņems samaksu.</span><span class="sxs-lookup"><span data-stu-id="beb10-246">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="beb10-247">Pēc apmaksas ciklu izveides katram ciklam varat ģenerēt apmaksas periodus.</span><span class="sxs-lookup"><span data-stu-id="beb10-247">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="beb10-248">Katrā apmaksas periodā ir ietverts noklusējuma maksājuma datums, kura pamatā ir jūsu sniegtā informācija.</span><span class="sxs-lookup"><span data-stu-id="beb10-248">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="beb10-249">Taču varat modificēt apmaksas perioda noklusējuma maksājuma datumu izņēmumu iestatīšanai, piemēram, kad maksājuma datums ir brīvdienā.</span><span class="sxs-lookup"><span data-stu-id="beb10-249">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="beb10-250">Dayforce izmanto tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="beb10-250">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="beb10-251">Apmaksas cikls (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-251">Pay cycle (required)</span></span>
- <span data-ttu-id="beb10-252">Apmaksas cikla biežums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-252">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="beb10-253">Perioda sākuma datums (ir jānorāda pirmais apmaksas periods)</span><span class="sxs-lookup"><span data-stu-id="beb10-253">Period start date (first pay period required)</span></span>
- <span data-ttu-id="beb10-254">Noklusējuma maksājuma datums (ir jānorāda pirmais apmaksas periods)</span><span class="sxs-lookup"><span data-stu-id="beb10-254">Default payment date (first pay period required)</span></span>

<span data-ttu-id="beb10-255">Šī informācija pakalpojumā Dayforce ir integrēta kā apmaksas grupas, un katram apmaksas ciklam to atdala valsts vai reģions.</span><span class="sxs-lookup"><span data-stu-id="beb10-255">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="beb10-256">Pirms integrācijas ir jābūt ģenerētam vismaz vienam apmaksas periodam.</span><span class="sxs-lookup"><span data-stu-id="beb10-256">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="beb10-257">Dayforce ģenerē apmaksas grupu kalendārus un maksājumu datumus atbilstoši Human Resources iestatītajam pirmā apmaksas perioda sākuma datumam un noklusējuma maksājuma datumam.</span><span class="sxs-lookup"><span data-stu-id="beb10-257">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="beb10-258">Ienākumu veida kodi</span><span class="sxs-lookup"><span data-stu-id="beb10-258">Earning codes</span></span>

<span data-ttu-id="beb10-259">Ienākumu veidu kodi unikāli identificē katra veida ienākumus, ko saņem nodarbinātie.</span><span class="sxs-lookup"><span data-stu-id="beb10-259">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="beb10-260">Kodiem ir dažādi ar ienākumiem saistīti parametri, piemēram, uzskaites nosacījumi, nodokļu likumi, pārskatu veidošanas prasības un bruto summas palielināšanas iespēja.</span><span class="sxs-lookup"><span data-stu-id="beb10-260">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="beb10-261">Dayforce izmanto tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="beb10-261">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="beb10-262">Ienākumu veida kods (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-262">Earning Code (required)</span></span>
- <span data-ttu-id="beb10-263">apraksts</span><span class="sxs-lookup"><span data-stu-id="beb10-263">Description</span></span>
- <span data-ttu-id="beb10-264">Mērvienība</span><span class="sxs-lookup"><span data-stu-id="beb10-264">Unit of measure</span></span>
- <span data-ttu-id="beb10-265">Produktīvs</span><span class="sxs-lookup"><span data-stu-id="beb10-265">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="beb10-266">Nodarbināto dati</span><span class="sxs-lookup"><span data-stu-id="beb10-266">Worker data</span></span>

<span data-ttu-id="beb10-267">Dažādo veidu nodarbināto ieraksti ir svarīga informācija personāla vadības un algu sistēmās.</span><span class="sxs-lookup"><span data-stu-id="beb10-267">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="beb10-268">Ievadīto informāciju var izmantot, lai sekotu nodarbinātajiem un personiskajai informācijai.</span><span class="sxs-lookup"><span data-stu-id="beb10-268">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="beb10-269">Par darbiniekiem var saglabāt tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="beb10-269">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="beb10-270">**Pamata** — saglabājiet pamata informāciju par darbinieku, piemēram, kontaktinformāciju, demogrāfisko informāciju, identifikācijas informāciju, ģimenes informāciju, karadienesta statusu, ekspatriantu informāciju, kā arī personiskās un ārkārtas kontaktpersonas.</span><span class="sxs-lookup"><span data-stu-id="beb10-270">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="beb10-271">**Nodarbinātība** — saglabājiet informāciju par darbinieka nodarbinātību, piemēram, informāciju par piederību uzņēmumam vai organizācijai, amata piešķiri, sākuma un beigu datumiem, piemērotību darbam, nodarbinātības noteikumiem, pensiju, atvaļinājumu un pārcelšanu.</span><span class="sxs-lookup"><span data-stu-id="beb10-271">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="beb10-272">**Atvaļinājumi un kavējumi** — saglabājiet informāciju par nodarbinātā kavējumiem, piemēram, informāciju par darba kalendāriem, kavējumu darbībām un kavējumu iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="beb10-272">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="beb10-273">**Atlīdzība un alga** — saglabājiet informāciju par nodarbinātā atlīdzības plāniem un algas informāciju, piemēram, plāna reģistrāciju, piemaksām, sniegumu, komisiju, nodokļu informāciju, pensionēšanos un ieturējumiem no algas.</span><span class="sxs-lookup"><span data-stu-id="beb10-273">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="beb10-274">Ievadot informāciju par nodarbināto, ņemiet vērā tālāk norādītos datus un konfigurācijas, kas tiek izmantoti pakalpojumā Dayforce.</span><span class="sxs-lookup"><span data-stu-id="beb10-274">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="beb10-275">Vispārīgā informācija</span><span class="sxs-lookup"><span data-stu-id="beb10-275">General information</span></span>

- <span data-ttu-id="beb10-276">Personāla numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-276">Personnel number (required)</span></span>
- <span data-ttu-id="beb10-277">Vārds (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-277">First name (required)</span></span>
- <span data-ttu-id="beb10-278">Uzvārds (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-278">Last name (required)</span></span>
- <span data-ttu-id="beb10-279">Otrais vārds</span><span class="sxs-lookup"><span data-stu-id="beb10-279">Middle name</span></span>
- <span data-ttu-id="beb10-280">Darba stāža datums</span><span class="sxs-lookup"><span data-stu-id="beb10-280">Seniority date</span></span>
- <span data-ttu-id="beb10-281">Zināms kā</span><span class="sxs-lookup"><span data-stu-id="beb10-281">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="beb10-282">Personiskā informācija</span><span class="sxs-lookup"><span data-stu-id="beb10-282">Personal information</span></span>

- <span data-ttu-id="beb10-283">Ģimenes stāvoklis (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-283">Marital status (required)</span></span>
- <span data-ttu-id="beb10-284">Dzimšanas datums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-284">Birth date (required)</span></span>
- <span data-ttu-id="beb10-285">Dzimums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-285">Gender (required)</span></span>
- <span data-ttu-id="beb10-286">Persona ar īpašām vajadzībām</span><span class="sxs-lookup"><span data-stu-id="beb10-286">Person with disabilities</span></span>
- <span data-ttu-id="beb10-287">Nacionalitātes valsts/reģions (tikai Meksikai)</span><span class="sxs-lookup"><span data-stu-id="beb10-287">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="beb10-288">Adreses informācija</span><span class="sxs-lookup"><span data-stu-id="beb10-288">Address information</span></span>

- <span data-ttu-id="beb10-289">Primārā (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-289">Primary (required)</span></span>
- <span data-ttu-id="beb10-290">Valsts/reģions (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-290">Country/region (required)</span></span>
- <span data-ttu-id="beb10-291">Pasta indekss (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-291">Postal code (required)</span></span>
- <span data-ttu-id="beb10-292">Ielas numurs (obligāti) (tikai Meksikai)</span><span class="sxs-lookup"><span data-stu-id="beb10-292">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="beb10-293">Mājas numurs/nosaukums (tikai Meksikai)</span><span class="sxs-lookup"><span data-stu-id="beb10-293">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="beb10-294">Pilsēta (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-294">City (required)</span></span>
- <span data-ttu-id="beb10-295">Administratīvais apgabals (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-295">State (required)</span></span>
- <span data-ttu-id="beb10-296">Apgabals (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-296">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="beb10-297">Kontaktinformācija</span><span class="sxs-lookup"><span data-stu-id="beb10-297">Contact information</span></span> 

- <span data-ttu-id="beb10-298">Primārā (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-298">Primary (required)</span></span>
- <span data-ttu-id="beb10-299">Kontaktpersonas tālrunis (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-299">Contact number (required)</span></span>
- <span data-ttu-id="beb10-300">Paplašinājums</span><span class="sxs-lookup"><span data-stu-id="beb10-300">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="beb10-301">Algas informācija un ienākumu veidu kodi</span><span class="sxs-lookup"><span data-stu-id="beb10-301">Payroll information and earning codes</span></span>

<span data-ttu-id="beb10-302">Darbiniekiem var būt piešķirti konkrēti ienākumu veidi konkrētajā maksājumu biežumā, kā arī var būt norādīta vēlamā maksāšanas metode.</span><span class="sxs-lookup"><span data-stu-id="beb10-302">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="beb10-303">Lai palīdzētu nodrošināt, ka šīs preferences un iestatījumi tiek izmantoti, pakalpojumā Dayforce ir tālāk norādītie lauki.</span><span class="sxs-lookup"><span data-stu-id="beb10-303">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="beb10-304">Ienākumu veida kodi</span><span class="sxs-lookup"><span data-stu-id="beb10-304">Earning codes</span></span>

- <span data-ttu-id="beb10-305">Amats (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-305">Position (required)</span></span>
- <span data-ttu-id="beb10-306">Ienākumu veida kods (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-306">Earning Code (required)</span></span>
- <span data-ttu-id="beb10-307">Biežums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-307">Frequency (required)</span></span>
- <span data-ttu-id="beb10-308">Summa (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-308">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="beb10-309">Algas informācija</span><span class="sxs-lookup"><span data-stu-id="beb10-309">Payroll information</span></span>

- <span data-ttu-id="beb10-310">Maksāšanas metode</span><span class="sxs-lookup"><span data-stu-id="beb10-310">Payment Method</span></span>
- <span data-ttu-id="beb10-311">Ekonomiskais reģions (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-311">Economic Region (required)</span></span>
- <span data-ttu-id="beb10-312">Darbinieka atvieglojumu ID</span><span class="sxs-lookup"><span data-stu-id="beb10-312">Employee Benefits ID</span></span>
- <span data-ttu-id="beb10-313">Nacionālais ID numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-313">National ID Number (required)</span></span>
- <span data-ttu-id="beb10-314">Karadienesta numurs</span><span class="sxs-lookup"><span data-stu-id="beb10-314">Military Service Number</span></span>
- <span data-ttu-id="beb10-315">Maiņas ID (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-315">Shift ID (required)</span></span>
- <span data-ttu-id="beb10-316">Nodokļu numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-316">Tax Number (required)</span></span>
- <span data-ttu-id="beb10-317">Arodbiedrības ID (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-317">Union ID (required)</span></span>
- <span data-ttu-id="beb10-318">Darba dienas ID (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-318">Work Day ID (required)</span></span>
- <span data-ttu-id="beb10-319">Darba atļaujas numurs</span><span class="sxs-lookup"><span data-stu-id="beb10-319">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="beb10-320">Meksika atbalsta šādas maksāšanas metodes: **Skaidra nauda**, **Čeks** (uzņēmuma fiziskais čeks) un **Elektroniskais maksājums**.</span><span class="sxs-lookup"><span data-stu-id="beb10-320">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="beb10-321">Ja nav norādīta neviena maksāšanas metode, pēc noklusējuma tiek izmantota opcija **Čeks**.</span><span class="sxs-lookup"><span data-stu-id="beb10-321">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="beb10-322">Nodarbinātības papildinformācija</span><span class="sxs-lookup"><span data-stu-id="beb10-322">Employment details</span></span>

<span data-ttu-id="beb10-323">Nodarbinātības datu vēsture pakalpojumā Dayforce tiek izmantota kā galvenā informācija, no kuras tiek iegūts darbinieka darbā pieņemšanas, darba attiecību izbeigšanas un atkārtotas pieņemšanas darbā statuss.</span><span class="sxs-lookup"><span data-stu-id="beb10-323">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="beb10-324">Dayforce vienlaikus atbalsta tikai vienu aktīvu nodarbinātības ierakstu.</span><span class="sxs-lookup"><span data-stu-id="beb10-324">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="beb10-325">Nodarbinātības sākuma datums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-325">Employment start date (required)</span></span>
- <span data-ttu-id="beb10-326">Nodarbinātības beigu datums</span><span class="sxs-lookup"><span data-stu-id="beb10-326">Employment end date</span></span>
- <span data-ttu-id="beb10-327">Pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="beb10-327">Start date</span></span>
- <span data-ttu-id="beb10-328">Koriģētais pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="beb10-328">Adjusted start date</span></span>
- <span data-ttu-id="beb10-329">Darba attiecību pārtraukšanas datums (jānorāda, kad tiek pārtrauktas darba attiecības)</span><span class="sxs-lookup"><span data-stu-id="beb10-329">Termination date (required upon termination)</span></span>
- <span data-ttu-id="beb10-330">Darba attiecību pārtraukšanas iemesls (jānorāda, kad tiek pārtrauktas darba attiecības)</span><span class="sxs-lookup"><span data-stu-id="beb10-330">Termination reason (required upon termination)</span></span>

<span data-ttu-id="beb10-331">Darbinieka galvenie datumi tiek iegūti, izmantojot tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="beb10-331">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="beb10-332">Personāla vadība</span><span class="sxs-lookup"><span data-stu-id="beb10-332">Human Resources</span></span>                | <span data-ttu-id="beb10-333">Dayforce</span><span class="sxs-lookup"><span data-stu-id="beb10-333">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="beb10-334">Pēdējais nomas datums</span><span class="sxs-lookup"><span data-stu-id="beb10-334">Most recent hire date</span></span> | <span data-ttu-id="beb10-335">Pašreizējā nepārtrauktās nodarbinātības vēstures ieraksta nodarbinātības sākums</span><span class="sxs-lookup"><span data-stu-id="beb10-335">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="beb10-336">Izbeigšanas datums</span><span class="sxs-lookup"><span data-stu-id="beb10-336">Termination date</span></span>      | <span data-ttu-id="beb10-337">Pašreizējā nepārtrauktās nodarbinātības vēstures ieraksta darba attiecību pārtraukšanas datums</span><span class="sxs-lookup"><span data-stu-id="beb10-337">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="beb10-338">Pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="beb10-338">Start date</span></span>            | <span data-ttu-id="beb10-339">Pašreizējā neaktīvā nodarbinātības vēstures ieraksta koriģētais sākuma datums, sākuma datums vai nodarbinātības sākums</span><span class="sxs-lookup"><span data-stu-id="beb10-339">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="beb10-340">Sākotnējais darbā pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="beb10-340">Original hire date</span></span>    | <span data-ttu-id="beb10-341">Agrākā nodarbinātības vēstures ieraksta nodarbinātības sākums</span><span class="sxs-lookup"><span data-stu-id="beb10-341">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="beb10-342">Atlīdzība</span><span class="sxs-lookup"><span data-stu-id="beb10-342">Compensation</span></span>

<span data-ttu-id="beb10-343">Fiksētās atlīdzības plānam ir jābūt saistītam ar katra darbinieka primāro amatu visā nodarbinātības periodā.</span><span class="sxs-lookup"><span data-stu-id="beb10-343">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="beb10-344">Šis periods sākas ar datumu, kurā darbinieks tika pieņemts darbā (vai nodarbinātības sākuma datumu), un turpinās līdz darba attiecību pārtraukšanai.</span><span class="sxs-lookup"><span data-stu-id="beb10-344">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="beb10-345">Spēkā stāšanās datums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-345">Effective Date (required)</span></span>
- <span data-ttu-id="beb10-346">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="beb10-346">Expiration date</span></span>
- <span data-ttu-id="beb10-347">Apmaksas likme (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-347">Pay Rate (required)</span></span>
- <span data-ttu-id="beb10-348">Apmaksas likmes konvertēšanas gadījumi (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-348">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="beb10-349">Gada ekvivalents (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-349">Annual equivalent (required)</span></span>
- <span data-ttu-id="beb10-350">Stundas ekvivalents (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-350">Hourly equivalent (required)</span></span>

<span data-ttu-id="beb10-351">Ja darbiniekam ar stundas likmi ir vairāki amati, pakalpojumā Dayforce kā darbinieka līmeņa pamatlikme/alga tiek importēta primārā amata fiksētā atlīdzība.</span><span class="sxs-lookup"><span data-stu-id="beb10-351">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="beb10-352">To amatu, kas nav primārie, stundas likme tiek saglabāta pakalpojumā Dayforce attiecīgajā amatā.</span><span class="sxs-lookup"><span data-stu-id="beb10-352">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="beb10-353">Ja darbiniekam, kurš saņem algu, ir vairāki amati, kā darbinieka līmeņa pamatlikme/alga tiek iegūta un izmantota visu aktīvo amatu kopējā stundas likme un gada alga.</span><span class="sxs-lookup"><span data-stu-id="beb10-353">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="beb10-354">Identifikācijas numuri</span><span class="sxs-lookup"><span data-stu-id="beb10-354">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="beb10-355">Sociālās apdrošināšanas numurs</span><span class="sxs-lookup"><span data-stu-id="beb10-355">Social Security identifier</span></span> 

<span data-ttu-id="beb10-356">Katram darbiniekam ir jābūt vienam primārajam numuram.</span><span class="sxs-lookup"><span data-stu-id="beb10-356">Every employee must have one primary identifier.</span></span> <span data-ttu-id="beb10-357">Šī numura identifikācijas tipam ir jābūt **SAN**.</span><span class="sxs-lookup"><span data-stu-id="beb10-357">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="beb10-358">Pakalpojumā Dayforce tas tiek automātiski iegūts kā darbinieka sociālās apdrošināšanas numurs, kas ir jānorāda, kad darbinieks tiek pieņemts darbā.</span><span class="sxs-lookup"><span data-stu-id="beb10-358">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="beb10-359">Primārais (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-359">Primary (required)</span></span>
- <span data-ttu-id="beb10-360">Identifikācijas tips = SAN</span><span class="sxs-lookup"><span data-stu-id="beb10-360">Identification Type = "SSN"</span></span>
- <span data-ttu-id="beb10-361">Izdošanas datums</span><span class="sxs-lookup"><span data-stu-id="beb10-361">Issued Date</span></span>
- <span data-ttu-id="beb10-362">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="beb10-362">Expiration Date</span></span>

<span data-ttu-id="beb10-363">Darbinieki var sniegt vairākus identifikācijas numurus, kuru identifikācijas tips ir **SAN**.</span><span class="sxs-lookup"><span data-stu-id="beb10-363">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="beb10-364">Taču pakalpojumā Dayforce tiek integrēts tikai ieraksts, kas ir atzīmēts kā **Primārais**, neatkarīgi no tā, vai šis numurs ir aktīvs vai tam ir beidzies derīgums.</span><span class="sxs-lookup"><span data-stu-id="beb10-364">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="beb10-365">Banku konti un izdevumi</span><span class="sxs-lookup"><span data-stu-id="beb10-365">Bank accounts and disbursements</span></span>

<span data-ttu-id="beb10-366">Jebkuram darbiniekam, kurš samaksu izvēlējies saņemt bankas konta pārskaitījuma veidā, ir jāievada derīga bankas konta informācija.</span><span class="sxs-lookup"><span data-stu-id="beb10-366">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="beb10-367">Personāla vadība</span><span class="sxs-lookup"><span data-stu-id="beb10-367">Human Resources</span></span>                         | <span data-ttu-id="beb10-368">Dayforce</span><span class="sxs-lookup"><span data-stu-id="beb10-368">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="beb10-369">Bankas konta numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-369">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="beb10-370">SWIFT kods (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-370">SWIFT code (required)</span></span>          | <span data-ttu-id="beb10-371">Lauku **Bankas ID** izmanto, apstrādājot algas Meksikā.</span><span class="sxs-lookup"><span data-stu-id="beb10-371">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="beb10-372">Filiāles numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-372">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="beb10-373">Bankas konta tips (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-373">Bank account type (required)</span></span>   | <span data-ttu-id="beb10-374">Lauku **Konta tips** izmanto, apstrādājot algas Meksikā.</span><span class="sxs-lookup"><span data-stu-id="beb10-374">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="beb10-375">Atbalstītās vērtības ir, piemēram, **Norēķini** un **Algas**.</span><span class="sxs-lookup"><span data-stu-id="beb10-375">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="beb10-376">Darbiniekiem, kuri samaksu izvēlas saņemt bankas konta pārskaitījumu veidā, ir jāsniedz saite uz juridiskās personas, kuras primārā adrese ir Meksikā, atlikumu kontu, kas ir saistīts ar derīgu Meksikas bankas kontu.</span><span class="sxs-lookup"><span data-stu-id="beb10-376">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="beb10-377">Visi pārējie konti, kas nav atlikumu konti, tiek ignorēti.</span><span class="sxs-lookup"><span data-stu-id="beb10-377">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="beb10-378">Adreses informācija</span><span class="sxs-lookup"><span data-stu-id="beb10-378">Address information</span></span>

<span data-ttu-id="beb10-379">Katram darbiniekam ir jābūt vienai primārajai vietai.</span><span class="sxs-lookup"><span data-stu-id="beb10-379">Every employee must have one primary location.</span></span> <span data-ttu-id="beb10-380">Pakalpojumā Dayforce šī vieta tiek izmantota, lai nodokļu piemērošanas nolūkos noteiktu darbinieka primāro dzīvesvietu.</span><span class="sxs-lookup"><span data-stu-id="beb10-380">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="beb10-381">Primārā (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-381">Primary (required)</span></span>
- <span data-ttu-id="beb10-382">Valsts/reģions (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-382">Country/region (required)</span></span>
- <span data-ttu-id="beb10-383">Pasta indekss (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-383">Zip/postal code (required)</span></span>
- <span data-ttu-id="beb10-384">Iela (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-384">Street (required)</span></span>
- <span data-ttu-id="beb10-385">Ielas numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-385">Street Number (required)</span></span>
- <span data-ttu-id="beb10-386">Mājas numurs/nosaukums</span><span class="sxs-lookup"><span data-stu-id="beb10-386">Building Complement</span></span>
- <span data-ttu-id="beb10-387">Pilsēta (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-387">City (required)</span></span>
- <span data-ttu-id="beb10-388">Administratīvais apgabals (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-388">State (required)</span></span>
- <span data-ttu-id="beb10-389">Apgabals (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-389">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="beb10-390">Datu konfigurēšana algu ģenerēšanai Amerikas Savienotajās Valstīs un Kanādā</span><span class="sxs-lookup"><span data-stu-id="beb10-390">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="beb10-391">Ja ģenerējat algas darbiniekiem Amerikas Savienotajās Valstīs un Kanādā, ir jākonfigurē tālāk norādītie elementi.</span><span class="sxs-lookup"><span data-stu-id="beb10-391">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="beb10-392">Amatiem ir jānorāda nodaļas.</span><span class="sxs-lookup"><span data-stu-id="beb10-392">Departments are required on positions.</span></span>
- <span data-ttu-id="beb10-393">Izmaksu centri ir jāiestata kā finanšu dimensijas, un tiem ir jābūt pirmajiem elementiem noklusējuma finanšu dimensijas virknē.</span><span class="sxs-lookup"><span data-stu-id="beb10-393">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="beb10-394">Varat konfigurēt Human Resources, lai amatiem būtu jānorāda nodaļa.</span><span class="sxs-lookup"><span data-stu-id="beb10-394">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="beb10-395">Lai to izdarītu, pārejiet uz **Personāla vadības kopīgotie amati > Amati > Pieprasīt amatiem nodaļas**.</span><span class="sxs-lookup"><span data-stu-id="beb10-395">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="beb10-396">Ieteicams piemērot šo iestatījumu integrācijai.</span><span class="sxs-lookup"><span data-stu-id="beb10-396">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="beb10-397">Darba tipi</span><span class="sxs-lookup"><span data-stu-id="beb10-397">Job types</span></span>

<span data-ttu-id="beb10-398">Darbu veidi tiek izmantoti, lai līdzīgus darbus grupētu kategorijās.</span><span class="sxs-lookup"><span data-stu-id="beb10-398">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="beb10-399">Darbu veidi ir nepieciešami, lai apstrādātu algas Amerikas Savienotajās Valstīs un Kanādā.</span><span class="sxs-lookup"><span data-stu-id="beb10-399">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="beb10-400">Daži darbu veidu piemēri ir pilna laika, nepilna laika, algots un stundu apmaksas darbs.</span><span class="sxs-lookup"><span data-stu-id="beb10-400">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="beb10-401">Darbu veidi tiek kartēti uz pakalpojumu Dayforce kā apmaksas tipi, lai norādītu, vai darbinieks saņem stundas samaksu vai algu.</span><span class="sxs-lookup"><span data-stu-id="beb10-401">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="beb10-402">Ir jānorāda tālāk norādītie darbu veidi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="beb10-402">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="beb10-403">Darba veids</span><span class="sxs-lookup"><span data-stu-id="beb10-403">Job type</span></span>   | <span data-ttu-id="beb10-404">apraksts</span><span class="sxs-lookup"><span data-stu-id="beb10-404">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="beb10-405">Ik stundu</span><span class="sxs-lookup"><span data-stu-id="beb10-405">Hourly</span></span>     | <span data-ttu-id="beb10-406">Ik stundu</span><span class="sxs-lookup"><span data-stu-id="beb10-406">Hourly</span></span>      |
| <span data-ttu-id="beb10-407">Algots</span><span class="sxs-lookup"><span data-stu-id="beb10-407">Salaried</span></span>   | <span data-ttu-id="beb10-408">Algots</span><span class="sxs-lookup"><span data-stu-id="beb10-408">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="beb10-409">Amatu veidi</span><span class="sxs-lookup"><span data-stu-id="beb10-409">Position types</span></span> 

<span data-ttu-id="beb10-410">Amatu veidus izmanto, lai norādītu, vai amats ir pilna laika, nepilna laika vai cita veida darbs.</span><span class="sxs-lookup"><span data-stu-id="beb10-410">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="beb10-411">Amatu veidi tiek kartēti uz pakalpojumu Dayforce kā apmaksas klases, lai norādītu, vai darbinieks ir pilna laika vai nepilna laika darbinieks.</span><span class="sxs-lookup"><span data-stu-id="beb10-411">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="beb10-412">Ir jānorāda tālāk norādītie amatu veidi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="beb10-412">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="beb10-413">Amata tips</span><span class="sxs-lookup"><span data-stu-id="beb10-413">Position type</span></span>   | <span data-ttu-id="beb10-414">apraksts</span><span class="sxs-lookup"><span data-stu-id="beb10-414">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="beb10-415">Pilna laika</span><span class="sxs-lookup"><span data-stu-id="beb10-415">Full-time</span></span>       | <span data-ttu-id="beb10-416">Pilna laika darbinieks</span><span class="sxs-lookup"><span data-stu-id="beb10-416">Full time employee</span></span> |
| <span data-ttu-id="beb10-417">Nepilna laika</span><span class="sxs-lookup"><span data-stu-id="beb10-417">Part-time</span></span>       | <span data-ttu-id="beb10-418">Nepilna laika darbinieks</span><span class="sxs-lookup"><span data-stu-id="beb10-418">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="beb10-419">Iemeslu kodi</span><span class="sxs-lookup"><span data-stu-id="beb10-419">Reason codes</span></span>

<span data-ttu-id="beb10-420">Iemeslu kodi sniedz informāciju par darbinieka statusu.</span><span class="sxs-lookup"><span data-stu-id="beb10-420">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="beb10-421">Iemeslu kodu tiek kartēti uz pakalpojumu Dayforce kā statusa iemesli, kas norāda darbinieka amata vai nodarbinātības statusa izmaiņu iemeslu.</span><span class="sxs-lookup"><span data-stu-id="beb10-421">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="beb10-422">Ir jānorāda tālāk norādītie iemeslu kodi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="beb10-422">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="beb10-423">Iemeslu kodi</span><span class="sxs-lookup"><span data-stu-id="beb10-423">Reason code</span></span>    | <span data-ttu-id="beb10-424">apraksts</span><span class="sxs-lookup"><span data-stu-id="beb10-424">Description</span></span>      | <span data-ttu-id="beb10-425">Piemērojamie scenāriji</span><span class="sxs-lookup"><span data-stu-id="beb10-425">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="beb10-426">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="beb10-426">RESIGNATION</span></span>    | <span data-ttu-id="beb10-427">Atlūgums</span><span class="sxs-lookup"><span data-stu-id="beb10-427">Resignation</span></span>      | <span data-ttu-id="beb10-428">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="beb10-428">Terminate worker</span></span>     |
| <span data-ttu-id="beb10-429">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="beb10-429">TERMINATION</span></span>    | <span data-ttu-id="beb10-430">Izbeigšana</span><span class="sxs-lookup"><span data-stu-id="beb10-430">Termination</span></span>      | <span data-ttu-id="beb10-431">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="beb10-431">Terminate worker</span></span>     |
| <span data-ttu-id="beb10-432">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="beb10-432">RETIREMENT</span></span>     | <span data-ttu-id="beb10-433">Aiziešana pensijā</span><span class="sxs-lookup"><span data-stu-id="beb10-433">Retirement</span></span>       | <span data-ttu-id="beb10-434">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="beb10-434">Terminate worker</span></span>     |
| <span data-ttu-id="beb10-435">CITI</span><span class="sxs-lookup"><span data-stu-id="beb10-435">OTHER</span></span>          | <span data-ttu-id="beb10-436">Citi iemesli</span><span class="sxs-lookup"><span data-stu-id="beb10-436">Other Reasons</span></span>    | <span data-ttu-id="beb10-437">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="beb10-437">Terminate worker</span></span>     |
| <span data-ttu-id="beb10-438">DEATH</span><span class="sxs-lookup"><span data-stu-id="beb10-438">DEATH</span></span>          | <span data-ttu-id="beb10-439">Nāve</span><span class="sxs-lookup"><span data-stu-id="beb10-439">Death</span></span>            | <span data-ttu-id="beb10-440">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="beb10-440">Terminate worker</span></span>     |
| <span data-ttu-id="beb10-441">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="beb10-441">LEAVEOFABSENCE</span></span> | <span data-ttu-id="beb10-442">Atvaļinājums</span><span class="sxs-lookup"><span data-stu-id="beb10-442">Leave of Absence</span></span> | <span data-ttu-id="beb10-443">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="beb10-443">Terminate worker</span></span>     |
| <span data-ttu-id="beb10-444">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="beb10-444">CONTRACTEND</span></span>    | <span data-ttu-id="beb10-445">Līguma beigas</span><span class="sxs-lookup"><span data-stu-id="beb10-445">End of Contract</span></span>  | <span data-ttu-id="beb10-446">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="beb10-446">Terminate worker</span></span>     |
| <span data-ttu-id="beb10-447">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="beb10-447">SALARYCHANGE</span></span>   | <span data-ttu-id="beb10-448">Algas izmaiņas</span><span class="sxs-lookup"><span data-stu-id="beb10-448">Change of Salary</span></span> | <span data-ttu-id="beb10-449">Atlīdzība</span><span class="sxs-lookup"><span data-stu-id="beb10-449">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="beb10-450">Ģimenes stāvoklis</span><span class="sxs-lookup"><span data-stu-id="beb10-450">Marital status</span></span>

<span data-ttu-id="beb10-451">Ģimenes statusa vērtības tiek kartētas uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkotas uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="beb10-451">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="beb10-452">Tālāk esošajā tabulā ir parādīts, kā ģimenes statusa vērtības tiek kartētas uz pakalpojumu Dayforce.</span><span class="sxs-lookup"><span data-stu-id="beb10-452">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="beb10-453">Personāla vadība</span><span class="sxs-lookup"><span data-stu-id="beb10-453">Human Resources</span></span>                 | <span data-ttu-id="beb10-454">Dayforce</span><span class="sxs-lookup"><span data-stu-id="beb10-454">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="beb10-455">Precējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="beb10-455">Married</span></span>                | <span data-ttu-id="beb10-456">Precējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="beb10-456">Married</span></span>              |
| <span data-ttu-id="beb10-457">Atsevišķs</span><span class="sxs-lookup"><span data-stu-id="beb10-457">Single</span></span>                 | <span data-ttu-id="beb10-458">Atsevišķs</span><span class="sxs-lookup"><span data-stu-id="beb10-458">Single</span></span>               |
| <span data-ttu-id="beb10-459">Atraitnis (-ne)</span><span class="sxs-lookup"><span data-stu-id="beb10-459">Widowed</span></span>                | <span data-ttu-id="beb10-460">Atraitnis (-ne)</span><span class="sxs-lookup"><span data-stu-id="beb10-460">Widowed</span></span>              |
| <span data-ttu-id="beb10-461">Šķīries (-usies)</span><span class="sxs-lookup"><span data-stu-id="beb10-461">Divorced</span></span>               | <span data-ttu-id="beb10-462">Šķīries (-usies)</span><span class="sxs-lookup"><span data-stu-id="beb10-462">Divorced</span></span>             |
| <span data-ttu-id="beb10-463">Reģistrētas attiecības</span><span class="sxs-lookup"><span data-stu-id="beb10-463">Registered Partnership</span></span> | <span data-ttu-id="beb10-464">Dzīvesbiedrs</span><span class="sxs-lookup"><span data-stu-id="beb10-464">Domestic Partnership</span></span> |
| <span data-ttu-id="beb10-465">Neviens</span><span class="sxs-lookup"><span data-stu-id="beb10-465">None</span></span>                   | <span data-ttu-id="beb10-466">Neviens</span><span class="sxs-lookup"><span data-stu-id="beb10-466">None</span></span>                 |
| <span data-ttu-id="beb10-467">Kopdzīve</span><span class="sxs-lookup"><span data-stu-id="beb10-467">Cohabiting</span></span>             | <span data-ttu-id="beb10-468">Kopdzīve</span><span class="sxs-lookup"><span data-stu-id="beb10-468">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="beb10-469">Dzimums</span><span class="sxs-lookup"><span data-stu-id="beb10-469">Gender</span></span>

<span data-ttu-id="beb10-470">Dzimuma apzīmējumi tiek kartēti uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkoti uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="beb10-470">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="beb10-471">Tālāk esošajā tabulā ir parādīts, kā dzimuma apzīmējumi tiek kartēti uz pakalpojumu Dayforce.</span><span class="sxs-lookup"><span data-stu-id="beb10-471">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="beb10-472">Personāla vadība</span><span class="sxs-lookup"><span data-stu-id="beb10-472">Human Resources</span></span>       | <span data-ttu-id="beb10-473">Dayforce</span><span class="sxs-lookup"><span data-stu-id="beb10-473">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="beb10-474">Vīrietis</span><span class="sxs-lookup"><span data-stu-id="beb10-474">Male</span></span>         | <span data-ttu-id="beb10-475">Vīrietis</span><span class="sxs-lookup"><span data-stu-id="beb10-475">Male</span></span>            |
| <span data-ttu-id="beb10-476">Sieviete</span><span class="sxs-lookup"><span data-stu-id="beb10-476">Female</span></span>       | <span data-ttu-id="beb10-477">Sieviete</span><span class="sxs-lookup"><span data-stu-id="beb10-477">Female</span></span>          |
| <span data-ttu-id="beb10-478">Nav specifisks</span><span class="sxs-lookup"><span data-stu-id="beb10-478">Non-specific</span></span> | <span data-ttu-id="beb10-479">*Netiek atbalstīts*</span><span class="sxs-lookup"><span data-stu-id="beb10-479">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="beb10-480">Ienākumu veida kodi</span><span class="sxs-lookup"><span data-stu-id="beb10-480">Earning codes</span></span>

<span data-ttu-id="beb10-481">Ienākumu veidu kodi unikāli identificē katra veida ienākumus, ko saņem nodarbinātie.</span><span class="sxs-lookup"><span data-stu-id="beb10-481">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="beb10-482">Kodiem ir vairāki ar ienākumiem saistīti parametri, piemēram, uzskaites nosacījumi, nodokļu likumi, pārskatu veidošanas prasības un bruto summas palielināšanas iespēja.</span><span class="sxs-lookup"><span data-stu-id="beb10-482">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="beb10-483">Ja tiek izmantota neatbalstīta biežuma vērtība, aprēķinā pēc noklusējuma tiek lietota biežuma vērtība **Katra apmaksa**.</span><span class="sxs-lookup"><span data-stu-id="beb10-483">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="beb10-484">Atbalstītās biežuma vērtības</span><span class="sxs-lookup"><span data-stu-id="beb10-484">Supported frequencies</span></span>

- <span data-ttu-id="beb10-485">Visus</span><span class="sxs-lookup"><span data-stu-id="beb10-485">All</span></span>
- <span data-ttu-id="beb10-486">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="beb10-486">EVERYPAY</span></span>
- <span data-ttu-id="beb10-487">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="beb10-487">EACHPAYPERIOD</span></span>
- <span data-ttu-id="beb10-488">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="beb10-488">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="beb10-489">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="beb10-489">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="beb10-490">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="beb10-490">1OFMTH</span></span>
- <span data-ttu-id="beb10-491">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="beb10-491">LASTOFMTH</span></span>
- <span data-ttu-id="beb10-492">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="beb10-492">2OFMTH</span></span>
- <span data-ttu-id="beb10-493">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="beb10-493">3OFMTH</span></span>
- <span data-ttu-id="beb10-494">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="beb10-494">4OFMTH</span></span>
- <span data-ttu-id="beb10-495">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="beb10-495">5OFMTH</span></span>
- <span data-ttu-id="beb10-496">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="beb10-496">1N2OFMTH</span></span>
- <span data-ttu-id="beb10-497">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="beb10-497">3N4OFMTH</span></span>
- <span data-ttu-id="beb10-498">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="beb10-498">1N3OFMTH</span></span>
- <span data-ttu-id="beb10-499">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="beb10-499">1N4OFMTH</span></span>
- <span data-ttu-id="beb10-500">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="beb10-500">2N3OFMTH</span></span>
- <span data-ttu-id="beb10-501">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="beb10-501">2N4OFMTH</span></span>
- <span data-ttu-id="beb10-502">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="beb10-502">1N2N3OFMTH</span></span>
- <span data-ttu-id="beb10-503">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="beb10-503">1N2N4OFMTH</span></span>
- <span data-ttu-id="beb10-504">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="beb10-504">1N3N4OFMTH</span></span>
- <span data-ttu-id="beb10-505">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="beb10-505">2N3N4OFMTH</span></span>
- <span data-ttu-id="beb10-506">1N2N3N4OFMTH–1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="beb10-506">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="beb10-507">2N3N4N5OFMth–2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="beb10-507">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="beb10-508">1OFQTR–1OFQTR</span><span class="sxs-lookup"><span data-stu-id="beb10-508">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="beb10-509">LASTOFQTR–LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="beb10-509">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="beb10-510">LASTMTHOFQTR–LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="beb10-510">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="beb10-511">1OFYEAR–1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="beb10-511">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="beb10-512">LASTOFYEAR–LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="beb10-512">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="beb10-513">NOVNDECOFYEAR–NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="beb10-513">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="beb10-514">Adreses</span><span class="sxs-lookup"><span data-stu-id="beb10-514">Addresses</span></span>

<span data-ttu-id="beb10-515">Noteiktas valsts vai reģiona, administratīvā apgabala un apgabala (pašvaldības) kodu identifikācijai ir nepieciešami konkrēti formāti, ko var atpazīt pakalpojums Dayforce un valsts/reģiona pakalpojumu sniedzēji.</span><span class="sxs-lookup"><span data-stu-id="beb10-515">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="beb10-516">Lai gan pilsētu formāts var būt dažāds, katrai pilsētai ir jābūt saistītai ar administratīvo apgabalu.</span><span class="sxs-lookup"><span data-stu-id="beb10-516">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="beb10-517">Personāla vadība</span><span class="sxs-lookup"><span data-stu-id="beb10-517">Human Resources</span></span>          | <span data-ttu-id="beb10-518">Dayforce</span><span class="sxs-lookup"><span data-stu-id="beb10-518">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="beb10-519">Valsts/reģions</span><span class="sxs-lookup"><span data-stu-id="beb10-519">Country/Region</span></span>  | <span data-ttu-id="beb10-520">Valsts kods</span><span class="sxs-lookup"><span data-stu-id="beb10-520">Country Code</span></span>          |
| <span data-ttu-id="beb10-521">Pasta indekss</span><span class="sxs-lookup"><span data-stu-id="beb10-521">Zip/Postal Code</span></span> | <span data-ttu-id="beb10-522">Pasta indekss</span><span class="sxs-lookup"><span data-stu-id="beb10-522">Postal Code</span></span>           |
| <span data-ttu-id="beb10-523">Administratīvais apgabals</span><span class="sxs-lookup"><span data-stu-id="beb10-523">State</span></span>           | <span data-ttu-id="beb10-524">Administratīvā apgabala kods</span><span class="sxs-lookup"><span data-stu-id="beb10-524">State Code</span></span>            |
| <span data-ttu-id="beb10-525">Pilsēta</span><span class="sxs-lookup"><span data-stu-id="beb10-525">City</span></span>            | <span data-ttu-id="beb10-526">Pilsēta</span><span class="sxs-lookup"><span data-stu-id="beb10-526">City</span></span>                  |
| <span data-ttu-id="beb10-527">Apgabals</span><span class="sxs-lookup"><span data-stu-id="beb10-527">County</span></span>          | <span data-ttu-id="beb10-528">Apgabals (pašvaldība)</span><span class="sxs-lookup"><span data-stu-id="beb10-528">County (Municipality)</span></span> |
| <span data-ttu-id="beb10-529">Iela</span><span class="sxs-lookup"><span data-stu-id="beb10-529">Street</span></span>          | <span data-ttu-id="beb10-530">Adreses 1. rinda</span><span class="sxs-lookup"><span data-stu-id="beb10-530">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="beb10-531">Nodokļu reģioni</span><span class="sxs-lookup"><span data-stu-id="beb10-531">Tax regions</span></span>

<span data-ttu-id="beb10-532">Nodokļu reģionus izmanto, lai noteiktu atbilstošos nodokļus, kas jāpiemēro, ģenerējot algu aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="beb10-532">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="beb10-533">Nodokļu reģioni tiek kartēti uz pakalpojumu Dayforce kā vietas adreses.</span><span class="sxs-lookup"><span data-stu-id="beb10-533">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="beb10-534">Noklusējuma nodokļu reģionam ir jābūt saistītam ar nodarbinātā aktīvo amatu.</span><span class="sxs-lookup"><span data-stu-id="beb10-534">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="beb10-535">Nodokļu reģions (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-535">Tax region (required)</span></span>
- <span data-ttu-id="beb10-536">Valsts/reģions (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-536">Country/Region (required)</span></span>
- <span data-ttu-id="beb10-537">Administratīvais apgabals (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-537">State (required)</span></span>
- <span data-ttu-id="beb10-538">Apgabals</span><span class="sxs-lookup"><span data-stu-id="beb10-538">County</span></span> 
- <span data-ttu-id="beb10-539">Pilsēta (obligāti)</span><span class="sxs-lookup"><span data-stu-id="beb10-539">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="beb10-540">Datu konfigurēšana algu aprēķina ģenerēšanai Meksikā</span><span class="sxs-lookup"><span data-stu-id="beb10-540">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="beb10-541">Ja ģenerējat algas darbiniekiem Meksikā, ir jākonfigurē tālāk norādītie elementi.</span><span class="sxs-lookup"><span data-stu-id="beb10-541">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="beb10-542">Amatiem ir jānorāda nodaļas.</span><span class="sxs-lookup"><span data-stu-id="beb10-542">Departments are required on positions.</span></span>
- <span data-ttu-id="beb10-543">Izmaksu centri ir jāiestata kā finanšu dimensijas, un tiem ir jābūt pirmajiem elementiem noklusējuma finanšu dimensijas virknē.</span><span class="sxs-lookup"><span data-stu-id="beb10-543">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="beb10-544">Darba tipi</span><span class="sxs-lookup"><span data-stu-id="beb10-544">Job types</span></span>

<span data-ttu-id="beb10-545">Darbu veidi tiek izmantoti, lai līdzīgus darbus grupētu kategorijās.</span><span class="sxs-lookup"><span data-stu-id="beb10-545">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="beb10-546">Lai apstrādātu algas Meksikā, ir nepieciešami darbu veidi.</span><span class="sxs-lookup"><span data-stu-id="beb10-546">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="beb10-547">Daži darbu veidu piemēri ir pilna laika, nepilna laika, algots un stundu apmaksas darbs.</span><span class="sxs-lookup"><span data-stu-id="beb10-547">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="beb10-548">Darbu veidi tiek kartēti uz pakalpojumu Dayforce kā apmaksas tipi, lai norādītu, vai darbinieks saņem stundas samaksu vai algu.</span><span class="sxs-lookup"><span data-stu-id="beb10-548">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="beb10-549">Ir jānorāda tālāk norādītie darbu veidi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="beb10-549">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="beb10-550">Darba veids</span><span class="sxs-lookup"><span data-stu-id="beb10-550">Job type</span></span>   | <span data-ttu-id="beb10-551">apraksts</span><span class="sxs-lookup"><span data-stu-id="beb10-551">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="beb10-552">Ik stundu</span><span class="sxs-lookup"><span data-stu-id="beb10-552">Hourly</span></span>     | <span data-ttu-id="beb10-553">Stundu (MX)</span><span class="sxs-lookup"><span data-stu-id="beb10-553">MX Hourly</span></span>   |
| <span data-ttu-id="beb10-554">Algots</span><span class="sxs-lookup"><span data-stu-id="beb10-554">Salaried</span></span>   | <span data-ttu-id="beb10-555">Algots (MX)</span><span class="sxs-lookup"><span data-stu-id="beb10-555">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="beb10-556">Amatu veidi</span><span class="sxs-lookup"><span data-stu-id="beb10-556">Position types</span></span> 

<span data-ttu-id="beb10-557">Amatu veidus izmanto, lai norādītu, vai amats ir pilna laika, nepilna laika vai cita veida darbs.</span><span class="sxs-lookup"><span data-stu-id="beb10-557">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="beb10-558">Amatu veidi tiek kartēti uz pakalpojumu Dayforce kā apmaksas klases, lai norādītu, vai darbinieks ir pilna laika vai nepilna laika darbinieks.</span><span class="sxs-lookup"><span data-stu-id="beb10-558">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="beb10-559">Ir jānorāda tālāk norādītie amatu veidi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="beb10-559">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="beb10-560">Amata tips</span><span class="sxs-lookup"><span data-stu-id="beb10-560">Position type</span></span>   | <span data-ttu-id="beb10-561">apraksts</span><span class="sxs-lookup"><span data-stu-id="beb10-561">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="beb10-562">Pilna laika</span><span class="sxs-lookup"><span data-stu-id="beb10-562">Full-time</span></span>       | <span data-ttu-id="beb10-563">Pilna laika darbinieks</span><span class="sxs-lookup"><span data-stu-id="beb10-563">Full time employee</span></span> |
| <span data-ttu-id="beb10-564">Nepilna laika</span><span class="sxs-lookup"><span data-stu-id="beb10-564">Part-time</span></span>       | <span data-ttu-id="beb10-565">Nepilna laika darbinieks</span><span class="sxs-lookup"><span data-stu-id="beb10-565">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="beb10-566">Iemeslu kodi</span><span class="sxs-lookup"><span data-stu-id="beb10-566">Reason codes</span></span>

<span data-ttu-id="beb10-567">Iemeslu kodi sniedz informāciju par darbinieka statusu.</span><span class="sxs-lookup"><span data-stu-id="beb10-567">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="beb10-568">Iemeslu kodu tiek kartēti uz pakalpojumu Dayforce kā statusa iemesli, kas norāda darbinieka amata vai nodarbinātības statusa izmaiņu iemeslu.</span><span class="sxs-lookup"><span data-stu-id="beb10-568">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="beb10-569">Ir jānorāda tālāk norādītie iemeslu kodi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="beb10-569">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="beb10-570">Iemeslu kodi</span><span class="sxs-lookup"><span data-stu-id="beb10-570">Reason code</span></span>            | <span data-ttu-id="beb10-571">apraksts</span><span class="sxs-lookup"><span data-stu-id="beb10-571">Description</span></span>                    | <span data-ttu-id="beb10-572">Piemērojamie scenāriji</span><span class="sxs-lookup"><span data-stu-id="beb10-572">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="beb10-573">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="beb10-573">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="beb10-574">Aiziešana no amata pirms pirmās algas</span><span class="sxs-lookup"><span data-stu-id="beb10-574">Departure before first payroll</span></span> | <span data-ttu-id="beb10-575">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="beb10-575">Terminate worker</span></span>     |
| <span data-ttu-id="beb10-576">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="beb10-576">RESIGNATION</span></span>            | <span data-ttu-id="beb10-577">Atlūgums</span><span class="sxs-lookup"><span data-stu-id="beb10-577">Resignation</span></span>                    | <span data-ttu-id="beb10-578">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="beb10-578">Terminate worker</span></span>     |
| <span data-ttu-id="beb10-579">PENSION</span><span class="sxs-lookup"><span data-stu-id="beb10-579">PENSION</span></span>                | <span data-ttu-id="beb10-580">Pensija</span><span class="sxs-lookup"><span data-stu-id="beb10-580">Pension</span></span>                        | <span data-ttu-id="beb10-581">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="beb10-581">Terminate worker</span></span>     |
| <span data-ttu-id="beb10-582">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="beb10-582">TERMINATION</span></span>            | <span data-ttu-id="beb10-583">Izbeigšana</span><span class="sxs-lookup"><span data-stu-id="beb10-583">Termination</span></span>                    | <span data-ttu-id="beb10-584">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="beb10-584">Terminate worker</span></span>     |
| <span data-ttu-id="beb10-585">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="beb10-585">RETIREMENT</span></span>             | <span data-ttu-id="beb10-586">Aiziešana pensijā</span><span class="sxs-lookup"><span data-stu-id="beb10-586">Retirement</span></span>                     | <span data-ttu-id="beb10-587">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="beb10-587">Terminate worker</span></span>     |
| <span data-ttu-id="beb10-588">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="beb10-588">ABSENTEE</span></span>               | <span data-ttu-id="beb10-589">Darba kavētājs</span><span class="sxs-lookup"><span data-stu-id="beb10-589">Absentee</span></span>                       | <span data-ttu-id="beb10-590">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="beb10-590">Terminate worker</span></span>     |
| <span data-ttu-id="beb10-591">CITI</span><span class="sxs-lookup"><span data-stu-id="beb10-591">OTHER</span></span>                  | <span data-ttu-id="beb10-592">Citi iemesli</span><span class="sxs-lookup"><span data-stu-id="beb10-592">Other Reasons</span></span>                  | <span data-ttu-id="beb10-593">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="beb10-593">Terminate worker</span></span>     |
| <span data-ttu-id="beb10-594">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="beb10-594">CLOSURE</span></span>                | <span data-ttu-id="beb10-595">Uzņēmuma slēgšana</span><span class="sxs-lookup"><span data-stu-id="beb10-595">Business Closure</span></span>               | <span data-ttu-id="beb10-596">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="beb10-596">Terminate worker</span></span>     |
| <span data-ttu-id="beb10-597">DEATH</span><span class="sxs-lookup"><span data-stu-id="beb10-597">DEATH</span></span>                  | <span data-ttu-id="beb10-598">Nāve</span><span class="sxs-lookup"><span data-stu-id="beb10-598">Death</span></span>                          | <span data-ttu-id="beb10-599">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="beb10-599">Terminate worker</span></span>     |
| <span data-ttu-id="beb10-600">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="beb10-600">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="beb10-601">Atvaļinājums</span><span class="sxs-lookup"><span data-stu-id="beb10-601">Leave of Absence</span></span>               | <span data-ttu-id="beb10-602">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="beb10-602">Terminate worker</span></span>     |
| <span data-ttu-id="beb10-603">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="beb10-603">CONTRACTEND</span></span>            | <span data-ttu-id="beb10-604">Līguma beigas</span><span class="sxs-lookup"><span data-stu-id="beb10-604">End of Contract</span></span>                | <span data-ttu-id="beb10-605">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="beb10-605">Terminate worker</span></span>     |
| <span data-ttu-id="beb10-606">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="beb10-606">SALARYCHANGE</span></span>           | <span data-ttu-id="beb10-607">Algas izmaiņas</span><span class="sxs-lookup"><span data-stu-id="beb10-607">Change of Salary</span></span>               | <span data-ttu-id="beb10-608">Atlīdzība</span><span class="sxs-lookup"><span data-stu-id="beb10-608">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="beb10-609">Nodarbinātības noteikumi</span><span class="sxs-lookup"><span data-stu-id="beb10-609">Terms of employment</span></span>

<span data-ttu-id="beb10-610">Nodarbinātības noteikumus izmanto, lai izveidotu nodarbinātības noteikumu kategorijas.</span><span class="sxs-lookup"><span data-stu-id="beb10-610">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="beb10-611">Noteikumi tiek kartēti uz pakalpojumu Dayforce kā nodarbinātības rādītāju vērtības.</span><span class="sxs-lookup"><span data-stu-id="beb10-611">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="beb10-612">Ir nepieciešami tālāk norādītie nodarbinātības noteikumi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="beb10-612">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="beb10-613">Nodarbinātības noteikumi</span><span class="sxs-lookup"><span data-stu-id="beb10-613">Terms of employment</span></span>   | <span data-ttu-id="beb10-614">apraksts</span><span class="sxs-lookup"><span data-stu-id="beb10-614">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="beb10-615">Regulārs</span><span class="sxs-lookup"><span data-stu-id="beb10-615">Regular</span></span>               | <span data-ttu-id="beb10-616">Regulārs</span><span class="sxs-lookup"><span data-stu-id="beb10-616">Regular</span></span>     |
| <span data-ttu-id="beb10-617">Tieši</span><span class="sxs-lookup"><span data-stu-id="beb10-617">Direct</span></span>                | <span data-ttu-id="beb10-618">Tieši</span><span class="sxs-lookup"><span data-stu-id="beb10-618">Direct</span></span>      |
| <span data-ttu-id="beb10-619">Štažēšanās</span><span class="sxs-lookup"><span data-stu-id="beb10-619">Internship</span></span>            | <span data-ttu-id="beb10-620">Štažēšanās</span><span class="sxs-lookup"><span data-stu-id="beb10-620">Internship</span></span>  |
| <span data-ttu-id="beb10-621">Pastāvīga</span><span class="sxs-lookup"><span data-stu-id="beb10-621">Permanent</span></span>             | <span data-ttu-id="beb10-622">Pastāvīga</span><span class="sxs-lookup"><span data-stu-id="beb10-622">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="beb10-623">Ģimenes stāvoklis</span><span class="sxs-lookup"><span data-stu-id="beb10-623">Marital status</span></span>

<span data-ttu-id="beb10-624">Ģimenes statusa vērtības tiek kartētas uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkotas uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="beb10-624">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="beb10-625">Tālāk esošajā tabulā ir parādīts, kā ģimenes statusa vērtības tiek kartētas uz pakalpojumu Dayforce.</span><span class="sxs-lookup"><span data-stu-id="beb10-625">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="beb10-626">Personāla vadība</span><span class="sxs-lookup"><span data-stu-id="beb10-626">Human Resources</span></span>                 | <span data-ttu-id="beb10-627">Dayforce</span><span class="sxs-lookup"><span data-stu-id="beb10-627">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="beb10-628">Precējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="beb10-628">Married</span></span>                | <span data-ttu-id="beb10-629">Precējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="beb10-629">Married</span></span>                   |
| <span data-ttu-id="beb10-630">Atsevišķs</span><span class="sxs-lookup"><span data-stu-id="beb10-630">Single</span></span>                 | <span data-ttu-id="beb10-631">Atsevišķs</span><span class="sxs-lookup"><span data-stu-id="beb10-631">Single</span></span>                    |
| <span data-ttu-id="beb10-632">Atraitnis (-ne)</span><span class="sxs-lookup"><span data-stu-id="beb10-632">Widowed</span></span>                | <span data-ttu-id="beb10-633">Atraitnis (-ne)</span><span class="sxs-lookup"><span data-stu-id="beb10-633">Widowed</span></span>                   |
| <span data-ttu-id="beb10-634">Šķīries (-usies)</span><span class="sxs-lookup"><span data-stu-id="beb10-634">Divorced</span></span>               | <span data-ttu-id="beb10-635">Šķīries (-usies)</span><span class="sxs-lookup"><span data-stu-id="beb10-635">Divorced</span></span>                  |
| <span data-ttu-id="beb10-636">Reģistrētas attiecības</span><span class="sxs-lookup"><span data-stu-id="beb10-636">Registered Partnership</span></span> | <span data-ttu-id="beb10-637">Dzīvesbiedrs</span><span class="sxs-lookup"><span data-stu-id="beb10-637">Domestic Partnership</span></span>      |
| <span data-ttu-id="beb10-638">Neviens</span><span class="sxs-lookup"><span data-stu-id="beb10-638">None</span></span>                   | <span data-ttu-id="beb10-639">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="beb10-639">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="beb10-640">Kopdzīve</span><span class="sxs-lookup"><span data-stu-id="beb10-640">Cohabiting</span></span>             | <span data-ttu-id="beb10-641">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="beb10-641">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="beb10-642">Dzimums</span><span class="sxs-lookup"><span data-stu-id="beb10-642">Gender</span></span>

<span data-ttu-id="beb10-643">Dzimuma apzīmējumi tiek kartēti uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkoti uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="beb10-643">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="beb10-644">Tālāk esošajā tabulā ir parādīts, kā dzimuma apzīmējumi tiek kartēti uz pakalpojumu Dayforce.</span><span class="sxs-lookup"><span data-stu-id="beb10-644">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="beb10-645">Personāla vadība</span><span class="sxs-lookup"><span data-stu-id="beb10-645">Human Resources</span></span>       | <span data-ttu-id="beb10-646">Dayforce</span><span class="sxs-lookup"><span data-stu-id="beb10-646">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="beb10-647">Vīrietis</span><span class="sxs-lookup"><span data-stu-id="beb10-647">Male</span></span>         | <span data-ttu-id="beb10-648">Vīrietis</span><span class="sxs-lookup"><span data-stu-id="beb10-648">Male</span></span>                      |
| <span data-ttu-id="beb10-649">Sieviete</span><span class="sxs-lookup"><span data-stu-id="beb10-649">Female</span></span>       | <span data-ttu-id="beb10-650">Sieviete</span><span class="sxs-lookup"><span data-stu-id="beb10-650">Female</span></span>                    |
| <span data-ttu-id="beb10-651">Nav specifisks</span><span class="sxs-lookup"><span data-stu-id="beb10-651">Non-specific</span></span> | <span data-ttu-id="beb10-652">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="beb10-652">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="beb10-653">Maksājumu metode</span><span class="sxs-lookup"><span data-stu-id="beb10-653">Payment method</span></span>

<span data-ttu-id="beb10-654">Maksāšanas metodes darbiniekam un uzņēmumam ļauj aprakstīt, kā darbinieki saņems samaksu.</span><span class="sxs-lookup"><span data-stu-id="beb10-654">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="beb10-655">Maksāšanas metodes tiek kartētas uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkotas uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="beb10-655">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="beb10-656">Tālāk esošajā tabulā ir parādīts, kā maksāšanas metodes tiek kartētas uz pakalpojumu Dayforce.</span><span class="sxs-lookup"><span data-stu-id="beb10-656">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="beb10-657">Personāla vadība</span><span class="sxs-lookup"><span data-stu-id="beb10-657">Human Resources</span></span>             | <span data-ttu-id="beb10-658">Dayforce</span><span class="sxs-lookup"><span data-stu-id="beb10-658">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="beb10-659">Kase</span><span class="sxs-lookup"><span data-stu-id="beb10-659">Cash</span></span>               | <span data-ttu-id="beb10-660">Kase</span><span class="sxs-lookup"><span data-stu-id="beb10-660">Cash</span></span>                      |
| <span data-ttu-id="beb10-661">Elektronisks maksājums</span><span class="sxs-lookup"><span data-stu-id="beb10-661">Electronic Payment</span></span> | <span data-ttu-id="beb10-662">Pārsūtījums</span><span class="sxs-lookup"><span data-stu-id="beb10-662">Transfer</span></span>                  |
| <span data-ttu-id="beb10-663">Pārbaudīt</span><span class="sxs-lookup"><span data-stu-id="beb10-663">Check</span></span>              | <span data-ttu-id="beb10-664">Čeks</span><span class="sxs-lookup"><span data-stu-id="beb10-664">Cheque</span></span>                    |
| <span data-ttu-id="beb10-665">Bankas vekselis</span><span class="sxs-lookup"><span data-stu-id="beb10-665">Bank Draft</span></span>         | <span data-ttu-id="beb10-666">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="beb10-666">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="beb10-667">Citi</span><span class="sxs-lookup"><span data-stu-id="beb10-667">Other</span></span>              | <span data-ttu-id="beb10-668">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="beb10-668">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="beb10-669">Bankas konta tips</span><span class="sxs-lookup"><span data-stu-id="beb10-669">Bank account type</span></span>

<span data-ttu-id="beb10-670">Bankas kontu tipus izmanto darbiniekiem sūtāmajiem elektroniskajiem maksājumiem.</span><span class="sxs-lookup"><span data-stu-id="beb10-670">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="beb10-671">Bankas kontu tipi tiek kartēti uz pakalpojumu Dayforce kā pārsūtīšanas konta informācija.</span><span class="sxs-lookup"><span data-stu-id="beb10-671">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="beb10-672">Bankas kontu tipi integrācijas laikā tiek atbilstoši tulkoti uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="beb10-672">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="beb10-673">Personāla vadība</span><span class="sxs-lookup"><span data-stu-id="beb10-673">Human Resources</span></span>            | <span data-ttu-id="beb10-674">Dayforce</span><span class="sxs-lookup"><span data-stu-id="beb10-674">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="beb10-675">Kontroles konts</span><span class="sxs-lookup"><span data-stu-id="beb10-675">Checking Account</span></span>  | <span data-ttu-id="beb10-676">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="beb10-676">CheckingAccount</span></span>           |
| <span data-ttu-id="beb10-677">Algu konts</span><span class="sxs-lookup"><span data-stu-id="beb10-677">Payroll Account</span></span>   | <span data-ttu-id="beb10-678">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="beb10-678">PayrollAccount</span></span>            |
| <span data-ttu-id="beb10-679">Uzkrājumu konts</span><span class="sxs-lookup"><span data-stu-id="beb10-679">Savings Account</span></span>   | <span data-ttu-id="beb10-680">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="beb10-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="beb10-681">BankGirot konts</span><span class="sxs-lookup"><span data-stu-id="beb10-681">BankGirot account</span></span> | <span data-ttu-id="beb10-682">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="beb10-682">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="beb10-683">PlusGirot konts</span><span class="sxs-lookup"><span data-stu-id="beb10-683">PlusGirot account</span></span> | <span data-ttu-id="beb10-684">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="beb10-684">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="beb10-685">Ienākumu veida kodi</span><span class="sxs-lookup"><span data-stu-id="beb10-685">Earning codes</span></span>

<span data-ttu-id="beb10-686">Ienākumu veidu kodi unikāli identificē katra veida ienākumus, ko saņem nodarbinātie.</span><span class="sxs-lookup"><span data-stu-id="beb10-686">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="beb10-687">Kodiem ir vairāki ar ienākumiem saistīti parametri, piemēram, uzskaites nosacījumi, nodokļu likumi, pārskatu veidošanas prasības un bruto summas palielināšanas iespēja.</span><span class="sxs-lookup"><span data-stu-id="beb10-687">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="beb10-688">Ja tiek izmantota neatbalstīta biežuma vērtība, aprēķinā pēc noklusējuma tiek lietota biežuma vērtība **Katra apmaksa**.</span><span class="sxs-lookup"><span data-stu-id="beb10-688">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="beb10-689">Atbalstītās biežuma vērtības</span><span class="sxs-lookup"><span data-stu-id="beb10-689">Supported frequencies</span></span>

- <span data-ttu-id="beb10-690">Visus</span><span class="sxs-lookup"><span data-stu-id="beb10-690">All</span></span>
- <span data-ttu-id="beb10-691">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="beb10-691">EVERYPAY</span></span>
- <span data-ttu-id="beb10-692">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="beb10-692">EACHPAYPERIOD</span></span>
- <span data-ttu-id="beb10-693">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="beb10-693">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="beb10-694">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="beb10-694">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="beb10-695">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="beb10-695">1OFMTH</span></span>
- <span data-ttu-id="beb10-696">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="beb10-696">LASTOFMTH</span></span>
- <span data-ttu-id="beb10-697">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="beb10-697">2OFMTH</span></span>
- <span data-ttu-id="beb10-698">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="beb10-698">3OFMTH</span></span>
- <span data-ttu-id="beb10-699">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="beb10-699">4OFMTH</span></span>
- <span data-ttu-id="beb10-700">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="beb10-700">5OFMTH</span></span>
- <span data-ttu-id="beb10-701">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="beb10-701">1N2OFMTH</span></span>
- <span data-ttu-id="beb10-702">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="beb10-702">3N4OFMTH</span></span>
- <span data-ttu-id="beb10-703">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="beb10-703">1N3OFMTH</span></span>
- <span data-ttu-id="beb10-704">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="beb10-704">1N4OFMTH</span></span>
- <span data-ttu-id="beb10-705">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="beb10-705">2N3OFMTH</span></span>
- <span data-ttu-id="beb10-706">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="beb10-706">2N4OFMTH</span></span>
- <span data-ttu-id="beb10-707">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="beb10-707">1N2N3OFMTH</span></span>
- <span data-ttu-id="beb10-708">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="beb10-708">1N2N4OFMTH</span></span>
- <span data-ttu-id="beb10-709">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="beb10-709">1N3N4OFMTH</span></span>
- <span data-ttu-id="beb10-710">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="beb10-710">2N3N4OFMTH</span></span>
- <span data-ttu-id="beb10-711">1N2N3N4OFMTH–1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="beb10-711">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="beb10-712">2N3N4N5OFMth–2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="beb10-712">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="beb10-713">1OFQTR–1OFQTR</span><span class="sxs-lookup"><span data-stu-id="beb10-713">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="beb10-714">LASTOFQTR–LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="beb10-714">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="beb10-715">LASTMTHOFQTR–LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="beb10-715">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="beb10-716">1OFYEAR–1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="beb10-716">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="beb10-717">LASTOFYEAR–LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="beb10-717">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="beb10-718">NOVNDECOFYEAR–NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="beb10-718">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="beb10-719">Adreses</span><span class="sxs-lookup"><span data-stu-id="beb10-719">Addresses</span></span>

<span data-ttu-id="beb10-720">Noteiktas valsts vai reģiona, administratīvā apgabala un apgabala (pašvaldības) kodu identifikācijai ir nepieciešami konkrēti formāti, ko var atpazīt pakalpojums Dayforce un valsts/reģiona pakalpojumu sniedzēji.</span><span class="sxs-lookup"><span data-stu-id="beb10-720">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="beb10-721">Lai gan pilsētu formāts var būt dažāds, katrai pilsētai ir jābūt saistītai ar administratīvo apgabalu.</span><span class="sxs-lookup"><span data-stu-id="beb10-721">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="beb10-722">Personāla vadība</span><span class="sxs-lookup"><span data-stu-id="beb10-722">Human Resources</span></span>              | <span data-ttu-id="beb10-723">Dayforce</span><span class="sxs-lookup"><span data-stu-id="beb10-723">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="beb10-724">Valsts/reģions</span><span class="sxs-lookup"><span data-stu-id="beb10-724">Country/Region</span></span>      | <span data-ttu-id="beb10-725">Valsts kods</span><span class="sxs-lookup"><span data-stu-id="beb10-725">Country Code</span></span>          |
| <span data-ttu-id="beb10-726">Pasta indekss</span><span class="sxs-lookup"><span data-stu-id="beb10-726">Zip/Postal Code</span></span>     | <span data-ttu-id="beb10-727">Pasta indekss</span><span class="sxs-lookup"><span data-stu-id="beb10-727">Postal Code</span></span>           |
| <span data-ttu-id="beb10-728">Administratīvais apgabals</span><span class="sxs-lookup"><span data-stu-id="beb10-728">State</span></span>               | <span data-ttu-id="beb10-729">Administratīvā apgabala kods</span><span class="sxs-lookup"><span data-stu-id="beb10-729">State Code</span></span>            |
| <span data-ttu-id="beb10-730">Pilsēta</span><span class="sxs-lookup"><span data-stu-id="beb10-730">City</span></span>                | <span data-ttu-id="beb10-731">Pilsēta</span><span class="sxs-lookup"><span data-stu-id="beb10-731">City</span></span>                  |
| <span data-ttu-id="beb10-732">Apgabals</span><span class="sxs-lookup"><span data-stu-id="beb10-732">County</span></span>              | <span data-ttu-id="beb10-733">Apgabals (pašvaldība)</span><span class="sxs-lookup"><span data-stu-id="beb10-733">County (Municipality)</span></span> |
| <span data-ttu-id="beb10-734">Iela</span><span class="sxs-lookup"><span data-stu-id="beb10-734">Street</span></span>              | <span data-ttu-id="beb10-735">Adreses 1. rinda</span><span class="sxs-lookup"><span data-stu-id="beb10-735">Address Line 1</span></span>        |
| <span data-ttu-id="beb10-736">Ielas numurs</span><span class="sxs-lookup"><span data-stu-id="beb10-736">Street Number</span></span>       | <span data-ttu-id="beb10-737">Adreses 2. rinda</span><span class="sxs-lookup"><span data-stu-id="beb10-737">Address Line 2</span></span>        |
| <span data-ttu-id="beb10-738">Mājas numurs/nosaukums</span><span class="sxs-lookup"><span data-stu-id="beb10-738">Building Complement</span></span> | <span data-ttu-id="beb10-739">Adreses 5. rinda</span><span class="sxs-lookup"><span data-stu-id="beb10-739">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="beb10-740">Pases numurs</span><span class="sxs-lookup"><span data-stu-id="beb10-740">Passport number</span></span>

<span data-ttu-id="beb10-741">Darbinieki var sniegt pases informāciju.</span><span class="sxs-lookup"><span data-stu-id="beb10-741">Employees can declare passport information.</span></span> <span data-ttu-id="beb10-742">Šīs informācijas identifikācijas tips ir **Pase**, un tā tiek integrēta pakalpojumā Dayforce kā daļa no darbinieka Meksikai specifiskās informācijas.</span><span class="sxs-lookup"><span data-stu-id="beb10-742">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="beb10-743">Identifikācijas tips = Pase</span><span class="sxs-lookup"><span data-stu-id="beb10-743">Identification Type = "Passport"</span></span>
- <span data-ttu-id="beb10-744">Izdošanas datums</span><span class="sxs-lookup"><span data-stu-id="beb10-744">Issued Date</span></span>
- <span data-ttu-id="beb10-745">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="beb10-745">Expiration Date</span></span>

<span data-ttu-id="beb10-746">Darbinieki var sniegt vairākus identifikācijas numurus, kuru identifikācijas tips ir **Pase**.</span><span class="sxs-lookup"><span data-stu-id="beb10-746">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="beb10-747">Taču pakalpojumā Dayforce tiek integrēts tikai pašreizējais aktīvais pases ieraksts.</span><span class="sxs-lookup"><span data-stu-id="beb10-747">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="beb10-748">Ja visiem pases ierakstiem ir beidzies derīgiem, pakalpojumā Dayforce tiek integrēta pēdējā izdotā pase.</span><span class="sxs-lookup"><span data-stu-id="beb10-748">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]