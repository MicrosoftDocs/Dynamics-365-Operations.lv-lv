---
title: Integrācijas konfigurēšana ar Dayforce
description: Integrācija starp Microsoft Dynamics 365 Human Resources un Ceridian Dayforce balstās uz vairākām konfigurācijas darbībām, kas ir aprakstītas šajā rakstā. Pirms maksājuma izpildes apstrādes vispirms ir jākonfigurē integrācija gan Human Resources, gan Dayforce.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 044a2d2f632b2c98ce94b6d61c2582a861640b68
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113400"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="5efc2-104">Integrācijas konfigurēšana ar Dayforce</span><span class="sxs-lookup"><span data-stu-id="5efc2-104">Configure integration with Dayforce</span></span>

<span data-ttu-id="5efc2-105">Integrācija starp Microsoft Dynamics 365 Human Resources un Ceridian Dayforce balstās uz vairākām konfigurācijas darbībām, kas ir aprakstītas šajā rakstā.</span><span class="sxs-lookup"><span data-stu-id="5efc2-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="5efc2-106">Pirms maksājuma izpildes apstrādes vispirms ir jākonfigurē integrācija gan Human Resources, gan Dayforce.</span><span class="sxs-lookup"><span data-stu-id="5efc2-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="5efc2-107">Ja maksājumu izpildei izmantojat tādu pakalpojumu kā Dayforce, jāiespējo integrācija Human Resources.</span><span class="sxs-lookup"><span data-stu-id="5efc2-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="5efc2-108">Integrācijai ir nepieciešami noteikti Human Resources dati.</span><span class="sxs-lookup"><span data-stu-id="5efc2-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="5efc2-109">Tādēļ ir jāpārliecinās, vai uz Dayforce kartētie dati Human Resources ir konfigurēti veidā, kas atbalsta integrāciju.</span><span class="sxs-lookup"><span data-stu-id="5efc2-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="5efc2-110">Integrācija izmanto tālāk norādītās vispārējās datu kategorijas.</span><span class="sxs-lookup"><span data-stu-id="5efc2-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="5efc2-111">Personāla vadības dati</span><span class="sxs-lookup"><span data-stu-id="5efc2-111">Human resources data</span></span>
- <span data-ttu-id="5efc2-112">Atlīdzības dati</span><span class="sxs-lookup"><span data-stu-id="5efc2-112">Compensation data</span></span>
- <span data-ttu-id="5efc2-113">Algu dati, piemēram, apmaksas cikli, apmaksas periodi un ienākumu veidu kodi</span><span class="sxs-lookup"><span data-stu-id="5efc2-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="5efc2-114">Nodarbināto dati</span><span class="sxs-lookup"><span data-stu-id="5efc2-114">Worker data</span></span>

<span data-ttu-id="5efc2-115">Šajā rakstā ir aprakstītas darbības, kas jāveic, lai iespējotu integrāciju.</span><span class="sxs-lookup"><span data-stu-id="5efc2-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="5efc2-116">Tajā ir arī izskaidrots, kādu veidu dati un konfigurācijas informācija ir nepieciešama integrācijai.</span><span class="sxs-lookup"><span data-stu-id="5efc2-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="5efc2-117">Integrācijas iespējošana</span><span class="sxs-lookup"><span data-stu-id="5efc2-117">Enable the integration</span></span>

<span data-ttu-id="5efc2-118">Lai pieslēgtos Dayforce, Human Resources ir jāieslēdz integrācija un jāievada konfigurācijas informācija.</span><span class="sxs-lookup"><span data-stu-id="5efc2-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="5efc2-119">Ja vēlaties, lai izveidotā Virsgrāmatas transakcija tiktu importēta programmā Microsoft Dynamics 365 Finance, ir jāiestata arī Microsoft Azure krātuves konts un programmā Finance jāievada Azure krātuves savienojuma virkne.</span><span class="sxs-lookup"><span data-stu-id="5efc2-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="5efc2-120">Lai Human Resources ieslēgtu integrāciju, veiciet tālāk minētās darbības.</span><span class="sxs-lookup"><span data-stu-id="5efc2-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="5efc2-121">Lapā **Sistēmas administrēšana** atlasiet opciju **Integrācijas konfigurēšana**.</span><span class="sxs-lookup"><span data-stu-id="5efc2-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="5efc2-122">Ievadiet drošo failu pārsūtīšanas protokola (FTP) galapunktu un drošo FTP mapes ceļu.</span><span class="sxs-lookup"><span data-stu-id="5efc2-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="5efc2-123">Ievadiet tā lietotāja lietotājvārdu un paroli, kurš piekļūs drošajam FTP galapunktam un mapes ceļam.</span><span class="sxs-lookup"><span data-stu-id="5efc2-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="5efc2-124">Pārbaudiet savienojumu, kā nepieciešams, un opciju **Iespējot algu aprēķina integrāciju** iestatiet uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="5efc2-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="5efc2-125">Kad integrācija ir ieslēgta, tiek izveidota datu eksportēšanas pakotne un faili, kā arī iestatīts biežums.</span><span class="sxs-lookup"><span data-stu-id="5efc2-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="5efc2-126">Biežumu varat mainīt atbilstoši vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="5efc2-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="5efc2-127">Papildinformāciju par Azure krātuves kontiem un Azure krātuves savienojuma virknēm skatiet tālāk minētajos Azure rakstos.</span><span class="sxs-lookup"><span data-stu-id="5efc2-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="5efc2-128">Par Azure krātuves kontiem</span><span class="sxs-lookup"><span data-stu-id="5efc2-128">About Azure storage accounts</span></span>](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="5efc2-129">Azure krātuves savienojuma virkņu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="5efc2-129">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="5efc2-130">Tehniskā informācija par algu aprēķina integrācijas iespējošanu</span><span class="sxs-lookup"><span data-stu-id="5efc2-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="5efc2-131">Algu aprēķina integrācijas ieslēgšanai ir divi primārie iznākumi, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="5efc2-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="5efc2-132">Tiek izveidots datu eksportēšanas projekts ar nosaukumu “Algu aprēķina integrācijas eksportēšana”.</span><span class="sxs-lookup"><span data-stu-id="5efc2-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="5efc2-133">Šajā projektā ir iekļauti elementi un lauki, kas nepieciešami algu aprēķina integrācijai.</span><span class="sxs-lookup"><span data-stu-id="5efc2-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="5efc2-134">Lai pārbaudītu projektu, dodieties uz sadaļu **Sistēmas administrēšana**, atlasiet elementu **Datu pārvaldība** un pēc tam atveriet datu projektu no projektu saraksta.</span><span class="sxs-lookup"><span data-stu-id="5efc2-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="5efc2-135">Šis pakešuzdevums izpilda datu eksportēšanas projektu, šifrē iegūto datu pakotni un pārsūta datu pakotnes failu uz SFTP galapunktu, kas konfigurēts ekrānā **Integrācijas konfigurēšana**.</span><span class="sxs-lookup"><span data-stu-id="5efc2-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="5efc2-136">Datu pakotne, kas pārsūtīta uz SFTP galapunktu, tiek šifrēta, izmantojot pakotnes unikālo atslēgu.</span><span class="sxs-lookup"><span data-stu-id="5efc2-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="5efc2-137">Atslēga glabājas Azure Key Vault krātuvē, kam var piekļūt, tikai izmantojot Ceridian.</span><span class="sxs-lookup"><span data-stu-id="5efc2-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="5efc2-138">Nav iespējams atšifrēt un pārbaudīt datu pakotnes saturu.</span><span class="sxs-lookup"><span data-stu-id="5efc2-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="5efc2-139">Ja ir jāpārbauda datu pakotnes saturs, eksportējiet datu projektu “Algu aprēķina integrācijas eksportēšana” manuāli, lejupielādējiet to un pēc tam atveriet to.</span><span class="sxs-lookup"><span data-stu-id="5efc2-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="5efc2-140">Eksportējot manuāli, pakotne netiks šifrēta un pārsūtīta.</span><span class="sxs-lookup"><span data-stu-id="5efc2-140">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="5efc2-141">Datu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="5efc2-141">Configure your data</span></span> 

<span data-ttu-id="5efc2-142">Lai apstrādātu algas, Human Resources ir jākonfigurē personāla vadības dati.</span><span class="sxs-lookup"><span data-stu-id="5efc2-142">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="5efc2-143">Jums ir jāiestata organizācijas dati, piemēram, darbi un amati, kā arī informācija par atvieglojumiem un atlīdzību.</span><span class="sxs-lookup"><span data-stu-id="5efc2-143">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="5efc2-144">Šie dati nodrošina informāciju par nodarbinātību, samaksu un ieturējumiem, kas nepieciešama darbinieka algas ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="5efc2-144">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="5efc2-145">Personāla vadības dati</span><span class="sxs-lookup"><span data-stu-id="5efc2-145">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="5efc2-146">Atvieglojumi</span><span class="sxs-lookup"><span data-stu-id="5efc2-146">Benefits</span></span> 

<span data-ttu-id="5efc2-147">Personāla vadība nodrošina rīkus, ko var izmantot, lai iestatītu un uzturētu atvieglojumus, ieturējumus un nodarbināto atlīdzības plānus, ko organizācija piedāvā vai apstrādā saviem nodarbinātajiem.</span><span class="sxs-lookup"><span data-stu-id="5efc2-147">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="5efc2-148">Kad veidojat atvieglojumus, ņemiet vērā tālāk norādītos datus un konfigurācijas, kas tiek izmantoti pakalpojumā Dayforce.</span><span class="sxs-lookup"><span data-stu-id="5efc2-148">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="5efc2-149">Atvieglojumu plāni</span><span class="sxs-lookup"><span data-stu-id="5efc2-149">Benefit plans</span></span>

- <span data-ttu-id="5efc2-150">Plāns (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-150">Plan (required)</span></span>
- <span data-ttu-id="5efc2-151">Tips (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-151">Type (required)</span></span>
- <span data-ttu-id="5efc2-152">Algas ietekme (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-152">Payroll impact (required)</span></span>
- <span data-ttu-id="5efc2-153">Atgūt nokavētos maksājumus</span><span class="sxs-lookup"><span data-stu-id="5efc2-153">Recover arrears</span></span>
- <span data-ttu-id="5efc2-154">Ieturējuma metode</span><span class="sxs-lookup"><span data-stu-id="5efc2-154">Deduction method</span></span>
- <span data-ttu-id="5efc2-155">Ieturējuma prioritāte</span><span class="sxs-lookup"><span data-stu-id="5efc2-155">Deduction priority</span></span>
- <span data-ttu-id="5efc2-156">Ierobežojuma periods</span><span class="sxs-lookup"><span data-stu-id="5efc2-156">Limit period</span></span>
- <span data-ttu-id="5efc2-157">Ierobežojuma summa</span><span class="sxs-lookup"><span data-stu-id="5efc2-157">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="5efc2-158">Atvieglojumi</span><span class="sxs-lookup"><span data-stu-id="5efc2-158">Benefits</span></span>

- <span data-ttu-id="5efc2-159">Plāns (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-159">Plan (required)</span></span>
- <span data-ttu-id="5efc2-160">Tips (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-160">Type (required)</span></span>
- <span data-ttu-id="5efc2-161">Opcija (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-161">Option (required)</span></span>
- <span data-ttu-id="5efc2-162">Atvieglojumu ID (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-162">Benefit ID (required)</span></span>
- <span data-ttu-id="5efc2-163">Biežums</span><span class="sxs-lookup"><span data-stu-id="5efc2-163">Frequency</span></span>
- <span data-ttu-id="5efc2-164">Pamats</span><span class="sxs-lookup"><span data-stu-id="5efc2-164">Basis</span></span>
- <span data-ttu-id="5efc2-165">Summa vai likme</span><span class="sxs-lookup"><span data-stu-id="5efc2-165">Amount or rate</span></span>
- <span data-ttu-id="5efc2-166">Ienākumu veida kods</span><span class="sxs-lookup"><span data-stu-id="5efc2-166">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="5efc2-167">Atbalstītās biežuma vērtības</span><span class="sxs-lookup"><span data-stu-id="5efc2-167">Supported frequencies</span></span> 

- <span data-ttu-id="5efc2-168">Katru nedēļu</span><span class="sxs-lookup"><span data-stu-id="5efc2-168">Weekly</span></span>
- <span data-ttu-id="5efc2-169">Katru otro nedēļu</span><span class="sxs-lookup"><span data-stu-id="5efc2-169">Bi-weekly</span></span>
- <span data-ttu-id="5efc2-170">Pusmēneša</span><span class="sxs-lookup"><span data-stu-id="5efc2-170">Semi-monthly</span></span>
- <span data-ttu-id="5efc2-171">Mēnesis</span><span class="sxs-lookup"><span data-stu-id="5efc2-171">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="5efc2-172">Atbalstītās pamata vērtības</span><span class="sxs-lookup"><span data-stu-id="5efc2-172">Supported bases</span></span> 

- <span data-ttu-id="5efc2-173">Fiksēta summa</span><span class="sxs-lookup"><span data-stu-id="5efc2-173">Fixed amount</span></span>
- <span data-ttu-id="5efc2-174">Ienākumu procentuālais daudzums</span><span class="sxs-lookup"><span data-stu-id="5efc2-174">Percent of earnings</span></span>
- <span data-ttu-id="5efc2-175">Produktīvās stundas</span><span class="sxs-lookup"><span data-stu-id="5efc2-175">Productive hours</span></span>

<span data-ttu-id="5efc2-176">Dayforce izveido tālāk norādītos ieturējumus, pamatojoties uz atvieglojumu plānā definēto algas ietekmi.</span><span class="sxs-lookup"><span data-stu-id="5efc2-176">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="5efc2-177">Atlasīšana Human Resources</span><span class="sxs-lookup"><span data-stu-id="5efc2-177">Selection in Human Resources</span></span>        | <span data-ttu-id="5efc2-178">Rezultāts pakalpojumā Dayforce</span><span class="sxs-lookup"><span data-stu-id="5efc2-178">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="5efc2-179">Nav</span><span class="sxs-lookup"><span data-stu-id="5efc2-179">None</span></span>                       | <span data-ttu-id="5efc2-180">Nav izveidots neviens ieturējums.</span><span class="sxs-lookup"><span data-stu-id="5efc2-180">No deduction is created.</span></span>                      |
| <span data-ttu-id="5efc2-181">Tikai ieturējums</span><span class="sxs-lookup"><span data-stu-id="5efc2-181">Deduction only</span></span>             | <span data-ttu-id="5efc2-182">Ir izveidots darbinieka ieturējums.</span><span class="sxs-lookup"><span data-stu-id="5efc2-182">An employee deduction is created.</span></span>             |
| <span data-ttu-id="5efc2-183">Tikai segums</span><span class="sxs-lookup"><span data-stu-id="5efc2-183">Contribution only</span></span>          | <span data-ttu-id="5efc2-184">Ir izveidots darba devēja ieturējums.</span><span class="sxs-lookup"><span data-stu-id="5efc2-184">An employer deduction is created.</span></span>             |
| <span data-ttu-id="5efc2-185">Ieturējums un segums</span><span class="sxs-lookup"><span data-stu-id="5efc2-185">Deduction and contribution</span></span> | <span data-ttu-id="5efc2-186">Ir izveidots darbinieka un darba devēja ieturējums.</span><span class="sxs-lookup"><span data-stu-id="5efc2-186">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="5efc2-187">Papildinformāciju par atvieglojumu programmas definēšanu un pārvaldību skatiet tālāk minētajos rakstos.</span><span class="sxs-lookup"><span data-stu-id="5efc2-187">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="5efc2-188">Darbinieku atvieglojumu programmas nodrošināšana</span><span class="sxs-lookup"><span data-stu-id="5efc2-188">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="5efc2-189">Izveidot jaunu atvieglojumu</span><span class="sxs-lookup"><span data-stu-id="5efc2-189">Create a new benefit</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="5efc2-190">Atvieglojumu piemērotības kārtulu un ierobežojumu definēšana</span><span class="sxs-lookup"><span data-stu-id="5efc2-190">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="5efc2-191">Atvieglojumu reģistrēšana un noņemšana nodarbinātajiem</span><span class="sxs-lookup"><span data-stu-id="5efc2-191">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="5efc2-192">Atlīdzība</span><span class="sxs-lookup"><span data-stu-id="5efc2-192">Compensation</span></span> 

<span data-ttu-id="5efc2-193">Atlīdzību pārvaldība tiek izmantota, lai kontrolētu pamatalgas un prēmiju izsniegšanu.</span><span class="sxs-lookup"><span data-stu-id="5efc2-193">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="5efc2-194">Darbinieka fiksētā pamatalga un nopelnu palielinājumi tiek kontrolēti, izmantojot fiksētas atlīdzības plānus.</span><span class="sxs-lookup"><span data-stu-id="5efc2-194">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="5efc2-195">Veicināšanas maksājumu izsniegšana, piemēram, prēmiju maksājumi, apbalvojumi par sasniegumiem, uzņēmuma akciju iegādes iespējas un dotācijas, kā arī vienreizējas piemaksas, tiek kontrolētas ar mainīgās atlīdzības plāniem.</span><span class="sxs-lookup"><span data-stu-id="5efc2-195">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="5efc2-196">Dayforce izmanto atlīdzības informāciju, lai aprēķinātu darbinieka stundas vai gada likmi.</span><span class="sxs-lookup"><span data-stu-id="5efc2-196">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="5efc2-197">Ir jānorāda fiksētās atlīdzības plāni un apmaksas likmes konvertēšanas gadījumi.</span><span class="sxs-lookup"><span data-stu-id="5efc2-197">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="5efc2-198">Darbiniekiem ir jābūt saistītiem ar fiksētās atlīdzības plānu.</span><span class="sxs-lookup"><span data-stu-id="5efc2-198">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="5efc2-199">Papildinformāciju par atlīdzības plāniem skatiet tālāk minētajos rakstos.</span><span class="sxs-lookup"><span data-stu-id="5efc2-199">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="5efc2-200">Fiksētās atlīdzības plānu izveidošana</span><span class="sxs-lookup"><span data-stu-id="5efc2-200">Create fixed compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="5efc2-201">Mainīgās atlīdzības plānu izveidošana</span><span class="sxs-lookup"><span data-stu-id="5efc2-201">Create variable compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="5efc2-202">Algas/atlīdzības organizācijas un plānu izstrāde</span><span class="sxs-lookup"><span data-stu-id="5efc2-202">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="5efc2-203">Procesa kompensācija</span><span class="sxs-lookup"><span data-stu-id="5efc2-203">Process compensation</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="5efc2-204">Atlīdzības procesa definēšana un rezultātu aprēķināšana</span><span class="sxs-lookup"><span data-stu-id="5efc2-204">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="5efc2-205">Darbinieka reģistrēšana fiksētās atlīdzības plānā</span><span class="sxs-lookup"><span data-stu-id="5efc2-205">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="5efc2-206">Darbinieka reģistrēšana mainīgās atlīdzības plānā</span><span class="sxs-lookup"><span data-stu-id="5efc2-206">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="5efc2-207">Darbi</span><span class="sxs-lookup"><span data-stu-id="5efc2-207">Jobs</span></span> 

<span data-ttu-id="5efc2-208">Darbs ir uzdevumu un atbildības jomu kopums, kas ir jāizpilda personai, kura veic darbu.</span><span class="sxs-lookup"><span data-stu-id="5efc2-208">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="5efc2-209">Papildinformāciju skatiet tālāk minētajos rakstos.</span><span class="sxs-lookup"><span data-stu-id="5efc2-209">For more information, see the following articles:</span></span>

- [<span data-ttu-id="5efc2-210">Darba komponentu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="5efc2-210">Setting up the components of a job</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="5efc2-211">Jaunu darbu definēšana</span><span class="sxs-lookup"><span data-stu-id="5efc2-211">Define new jobs</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="5efc2-212">Amati</span><span class="sxs-lookup"><span data-stu-id="5efc2-212">Positions</span></span>

<span data-ttu-id="5efc2-213">Pozīcija ir atsevišķa darba instance.</span><span class="sxs-lookup"><span data-stu-id="5efc2-213">A position is an individual instance of a job.</span></span> <span data-ttu-id="5efc2-214">Piemēram, amats Pārdošanas daļas vadītājs (austrumu reģions) ir tikai viens no amatiem, kas ir saistīti ar darbu Pārdošanas daļas vadītājs.</span><span class="sxs-lookup"><span data-stu-id="5efc2-214">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="5efc2-215">Amats pastāv nodaļā.</span><span class="sxs-lookup"><span data-stu-id="5efc2-215">A position exists in a department.</span></span> <span data-ttu-id="5efc2-216">Ar katru amatu var būt saistīts tikai viens nodarbinātais.</span><span class="sxs-lookup"><span data-stu-id="5efc2-216">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="5efc2-217">Iestatot jaunus amatus, ņemiet vērā tālāk norādītos datus un konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="5efc2-217">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="5efc2-218">Amats (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-218">Position (required)</span></span>
- <span data-ttu-id="5efc2-219">Apraksts (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-219">Description (required)</span></span>
- <span data-ttu-id="5efc2-220">Darbs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-220">Job (required)</span></span>
- <span data-ttu-id="5efc2-221">Nodaļa (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-221">Department (required)</span></span>
- <span data-ttu-id="5efc2-222">Amata veids (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-222">Position type (required)</span></span>
- <span data-ttu-id="5efc2-223">Pilnas slodzes ekvivalents</span><span class="sxs-lookup"><span data-stu-id="5efc2-223">Full-time equivalent</span></span>
- <span data-ttu-id="5efc2-224">Ikgadējās parastās stundas (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-224">Annual regular hours (required)</span></span>
- <span data-ttu-id="5efc2-225">Apmaksātāja juridiskā persona (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-225">Paid by legal entity (required)</span></span>
- <span data-ttu-id="5efc2-226">Apmaksas cikls (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-226">Pay cycle (required)</span></span>
- <span data-ttu-id="5efc2-227">Noklusējuma finanšu dimensija — izmaksu centrs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-227">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="5efc2-228">Nodarbinātā piešķire — nodarbinātais, piešķires sākums, piešķires beigas, iemesla kods</span><span class="sxs-lookup"><span data-stu-id="5efc2-228">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="5efc2-229">Ja vienā nodaļā ar to pašu darbu ir saistīti vairāki amati, tie pakalpojumā Dayforce tiek apvienoti vienā amatā.</span><span class="sxs-lookup"><span data-stu-id="5efc2-229">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="5efc2-230">Papildinformāciju skatiet tālāk minētajos rakstos.</span><span class="sxs-lookup"><span data-stu-id="5efc2-230">For more information, see the following articles:</span></span>

- [<span data-ttu-id="5efc2-231">Darbaspēka organizēšana, izmantojot nodaļas, darbus un amatus</span><span class="sxs-lookup"><span data-stu-id="5efc2-231">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="5efc2-232">Amatu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="5efc2-232">Set up positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="5efc2-233">Nodaļas</span><span class="sxs-lookup"><span data-stu-id="5efc2-233">Departments</span></span>

<span data-ttu-id="5efc2-234">Nodaļa ir pārvaldības struktūrvienība, kas pārstāv organizācijas kategoriju vai funkcionālo apgabalu.</span><span class="sxs-lookup"><span data-stu-id="5efc2-234">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="5efc2-235">Nodaļa ir atbildīga par noteiktu organizācijas jomu, piemēram, pārdošanu, uzskaiti vai personāla vadību.</span><span class="sxs-lookup"><span data-stu-id="5efc2-235">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="5efc2-236">Nodaļas var izmantot, lai ziņotu par funkcionālām jomām.</span><span class="sxs-lookup"><span data-stu-id="5efc2-236">You can use departments to report on functional areas.</span></span> <span data-ttu-id="5efc2-237">Nodaļām var būt peļņas un zaudējumu atbildība.</span><span class="sxs-lookup"><span data-stu-id="5efc2-237">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="5efc2-238">Papildinformāciju skatiet tālāk minētajos rakstos.</span><span class="sxs-lookup"><span data-stu-id="5efc2-238">For more information, see the following articles:</span></span>

- [<span data-ttu-id="5efc2-239">Nodaļas izveide un tās saistīšana ar nodaļu hierarhiju</span><span class="sxs-lookup"><span data-stu-id="5efc2-239">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="5efc2-240">Jaunu nodaļu definēšana</span><span class="sxs-lookup"><span data-stu-id="5efc2-240">Define new departments</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="5efc2-241">Apmaksas cikli un apmaksas periodi</span><span class="sxs-lookup"><span data-stu-id="5efc2-241">Pay cycles and pay periods</span></span>

<span data-ttu-id="5efc2-242">Apmaksas cikls nosaka, cik bieži tiek veikts algu aprēķins, kā arī konkrētās dienas, kurās nodarbinātie saņem samaksu.</span><span class="sxs-lookup"><span data-stu-id="5efc2-242">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="5efc2-243">Apmaksas cikls var būt, piemēram, ikmēneša, un darbinieki samaksu var saņemt mēneša pēdējā dienā.</span><span class="sxs-lookup"><span data-stu-id="5efc2-243">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="5efc2-244">Vai arī apmaksas cikls var būt iknedēļas, un darbinieki samaksu var saņemt otrdienā pēc apmaksas perioda beigām.</span><span class="sxs-lookup"><span data-stu-id="5efc2-244">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="5efc2-245">Apmaksas cikli tiek piešķirti amatiem, lai kontrolētu to, kad nodarbinātie šajos amatos saņems samaksu.</span><span class="sxs-lookup"><span data-stu-id="5efc2-245">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="5efc2-246">Pēc apmaksas ciklu izveides katram ciklam varat ģenerēt apmaksas periodus.</span><span class="sxs-lookup"><span data-stu-id="5efc2-246">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="5efc2-247">Katrā apmaksas periodā ir ietverts noklusējuma maksājuma datums, kura pamatā ir jūsu sniegtā informācija.</span><span class="sxs-lookup"><span data-stu-id="5efc2-247">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="5efc2-248">Taču varat modificēt apmaksas perioda noklusējuma maksājuma datumu izņēmumu iestatīšanai, piemēram, kad maksājuma datums ir brīvdienā.</span><span class="sxs-lookup"><span data-stu-id="5efc2-248">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="5efc2-249">Dayforce izmanto tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="5efc2-249">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="5efc2-250">Apmaksas cikls (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-250">Pay cycle (required)</span></span>
- <span data-ttu-id="5efc2-251">Apmaksas cikla biežums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-251">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="5efc2-252">Perioda sākuma datums (ir jānorāda pirmais apmaksas periods)</span><span class="sxs-lookup"><span data-stu-id="5efc2-252">Period start date (first pay period required)</span></span>
- <span data-ttu-id="5efc2-253">Noklusējuma maksājuma datums (ir jānorāda pirmais apmaksas periods)</span><span class="sxs-lookup"><span data-stu-id="5efc2-253">Default payment date (first pay period required)</span></span>

<span data-ttu-id="5efc2-254">Šī informācija pakalpojumā Dayforce ir integrēta kā apmaksas grupas, un katram apmaksas ciklam to atdala valsts vai reģions.</span><span class="sxs-lookup"><span data-stu-id="5efc2-254">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="5efc2-255">Pirms integrācijas ir jābūt ģenerētam vismaz vienam apmaksas periodam.</span><span class="sxs-lookup"><span data-stu-id="5efc2-255">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="5efc2-256">Dayforce ģenerē apmaksas grupu kalendārus un maksājumu datumus atbilstoši Human Resources iestatītajam pirmā apmaksas perioda sākuma datumam un noklusējuma maksājuma datumam.</span><span class="sxs-lookup"><span data-stu-id="5efc2-256">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="5efc2-257">Ienākumu veida kodi</span><span class="sxs-lookup"><span data-stu-id="5efc2-257">Earning codes</span></span>

<span data-ttu-id="5efc2-258">Ienākumu veidu kodi unikāli identificē katra veida ienākumus, ko saņem nodarbinātie.</span><span class="sxs-lookup"><span data-stu-id="5efc2-258">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="5efc2-259">Kodiem ir dažādi ar ienākumiem saistīti parametri, piemēram, uzskaites nosacījumi, nodokļu likumi, pārskatu veidošanas prasības un bruto summas palielināšanas iespēja.</span><span class="sxs-lookup"><span data-stu-id="5efc2-259">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="5efc2-260">Dayforce izmanto tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="5efc2-260">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="5efc2-261">Ienākumu veida kods (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-261">Earning Code (required)</span></span>
- <span data-ttu-id="5efc2-262">apraksts</span><span class="sxs-lookup"><span data-stu-id="5efc2-262">Description</span></span>
- <span data-ttu-id="5efc2-263">Mērvienība</span><span class="sxs-lookup"><span data-stu-id="5efc2-263">Unit of measure</span></span>
- <span data-ttu-id="5efc2-264">Produktīvs</span><span class="sxs-lookup"><span data-stu-id="5efc2-264">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="5efc2-265">Nodarbināto dati</span><span class="sxs-lookup"><span data-stu-id="5efc2-265">Worker data</span></span>

<span data-ttu-id="5efc2-266">Dažādo veidu nodarbināto ieraksti ir svarīga informācija personāla vadības un algu sistēmās.</span><span class="sxs-lookup"><span data-stu-id="5efc2-266">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="5efc2-267">Ievadīto informāciju var izmantot, lai sekotu nodarbinātajiem un personiskajai informācijai.</span><span class="sxs-lookup"><span data-stu-id="5efc2-267">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="5efc2-268">Par darbiniekiem var saglabāt tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="5efc2-268">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="5efc2-269">**Pamata** — saglabājiet pamata informāciju par darbinieku, piemēram, kontaktinformāciju, demogrāfisko informāciju, identifikācijas informāciju, ģimenes informāciju, karadienesta statusu, ekspatriantu informāciju, kā arī personiskās un ārkārtas kontaktpersonas.</span><span class="sxs-lookup"><span data-stu-id="5efc2-269">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="5efc2-270">**Nodarbinātība** — saglabājiet informāciju par darbinieka nodarbinātību, piemēram, informāciju par piederību uzņēmumam vai organizācijai, amata piešķiri, sākuma un beigu datumiem, piemērotību darbam, nodarbinātības noteikumiem, pensiju, atvaļinājumu un pārcelšanu.</span><span class="sxs-lookup"><span data-stu-id="5efc2-270">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="5efc2-271">**Atvaļinājumi un kavējumi** — saglabājiet informāciju par nodarbinātā kavējumiem, piemēram, informāciju par darba kalendāriem, kavējumu darbībām un kavējumu iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="5efc2-271">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="5efc2-272">**Atlīdzība un alga** — saglabājiet informāciju par nodarbinātā atlīdzības plāniem un algas informāciju, piemēram, plāna reģistrāciju, piemaksām, sniegumu, komisiju, nodokļu informāciju, pensionēšanos un ieturējumiem no algas.</span><span class="sxs-lookup"><span data-stu-id="5efc2-272">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="5efc2-273">Ievadot informāciju par nodarbināto, ņemiet vērā tālāk norādītos datus un konfigurācijas, kas tiek izmantoti pakalpojumā Dayforce.</span><span class="sxs-lookup"><span data-stu-id="5efc2-273">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="5efc2-274">Vispārīgā informācija</span><span class="sxs-lookup"><span data-stu-id="5efc2-274">General information</span></span>

- <span data-ttu-id="5efc2-275">Personāla numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-275">Personnel number (required)</span></span>
- <span data-ttu-id="5efc2-276">Vārds (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-276">First name (required)</span></span>
- <span data-ttu-id="5efc2-277">Uzvārds (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-277">Last name (required)</span></span>
- <span data-ttu-id="5efc2-278">Otrais vārds</span><span class="sxs-lookup"><span data-stu-id="5efc2-278">Middle name</span></span>
- <span data-ttu-id="5efc2-279">Darba stāža datums</span><span class="sxs-lookup"><span data-stu-id="5efc2-279">Seniority date</span></span>
- <span data-ttu-id="5efc2-280">Zināms kā</span><span class="sxs-lookup"><span data-stu-id="5efc2-280">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="5efc2-281">Personiskā informācija</span><span class="sxs-lookup"><span data-stu-id="5efc2-281">Personal information</span></span>

- <span data-ttu-id="5efc2-282">Ģimenes stāvoklis (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-282">Marital status (required)</span></span>
- <span data-ttu-id="5efc2-283">Dzimšanas datums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-283">Birth date (required)</span></span>
- <span data-ttu-id="5efc2-284">Dzimums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-284">Gender (required)</span></span>
- <span data-ttu-id="5efc2-285">Persona ar īpašām vajadzībām</span><span class="sxs-lookup"><span data-stu-id="5efc2-285">Person with disabilities</span></span>
- <span data-ttu-id="5efc2-286">Nacionalitātes valsts/reģions (tikai Meksikai)</span><span class="sxs-lookup"><span data-stu-id="5efc2-286">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="5efc2-287">Adreses informācija</span><span class="sxs-lookup"><span data-stu-id="5efc2-287">Address information</span></span>

- <span data-ttu-id="5efc2-288">Primārā (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-288">Primary (required)</span></span>
- <span data-ttu-id="5efc2-289">Valsts/reģions (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-289">Country/region (required)</span></span>
- <span data-ttu-id="5efc2-290">Pasta indekss (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-290">Postal code (required)</span></span>
- <span data-ttu-id="5efc2-291">Ielas numurs (obligāti) (tikai Meksikai)</span><span class="sxs-lookup"><span data-stu-id="5efc2-291">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="5efc2-292">Mājas numurs/nosaukums (tikai Meksikai)</span><span class="sxs-lookup"><span data-stu-id="5efc2-292">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="5efc2-293">Pilsēta (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-293">City (required)</span></span>
- <span data-ttu-id="5efc2-294">Administratīvais apgabals (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-294">State (required)</span></span>
- <span data-ttu-id="5efc2-295">Apgabals (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-295">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="5efc2-296">Kontaktinformācija</span><span class="sxs-lookup"><span data-stu-id="5efc2-296">Contact information</span></span> 

- <span data-ttu-id="5efc2-297">Primārā (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-297">Primary (required)</span></span>
- <span data-ttu-id="5efc2-298">Kontaktpersonas tālrunis (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-298">Contact number (required)</span></span>
- <span data-ttu-id="5efc2-299">Paplašinājums</span><span class="sxs-lookup"><span data-stu-id="5efc2-299">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="5efc2-300">Algas informācija un ienākumu veidu kodi</span><span class="sxs-lookup"><span data-stu-id="5efc2-300">Payroll information and earning codes</span></span>

<span data-ttu-id="5efc2-301">Darbiniekiem var būt piešķirti konkrēti ienākumu veidi konkrētajā maksājumu biežumā, kā arī var būt norādīta vēlamā maksāšanas metode.</span><span class="sxs-lookup"><span data-stu-id="5efc2-301">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="5efc2-302">Lai palīdzētu nodrošināt, ka šīs preferences un iestatījumi tiek izmantoti, pakalpojumā Dayforce ir tālāk norādītie lauki.</span><span class="sxs-lookup"><span data-stu-id="5efc2-302">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="5efc2-303">Ienākumu veida kodi</span><span class="sxs-lookup"><span data-stu-id="5efc2-303">Earning codes</span></span>

- <span data-ttu-id="5efc2-304">Amats (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-304">Position (required)</span></span>
- <span data-ttu-id="5efc2-305">Ienākumu veida kods (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-305">Earning Code (required)</span></span>
- <span data-ttu-id="5efc2-306">Biežums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-306">Frequency (required)</span></span>
- <span data-ttu-id="5efc2-307">Summa (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-307">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="5efc2-308">Algas informācija</span><span class="sxs-lookup"><span data-stu-id="5efc2-308">Payroll information</span></span>

- <span data-ttu-id="5efc2-309">Maksāšanas metode</span><span class="sxs-lookup"><span data-stu-id="5efc2-309">Payment Method</span></span>
- <span data-ttu-id="5efc2-310">Ekonomiskais reģions (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-310">Economic Region (required)</span></span>
- <span data-ttu-id="5efc2-311">Darbinieka atvieglojumu ID</span><span class="sxs-lookup"><span data-stu-id="5efc2-311">Employee Benefits ID</span></span>
- <span data-ttu-id="5efc2-312">Nacionālais ID numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-312">National ID Number (required)</span></span>
- <span data-ttu-id="5efc2-313">Karadienesta numurs</span><span class="sxs-lookup"><span data-stu-id="5efc2-313">Military Service Number</span></span>
- <span data-ttu-id="5efc2-314">Maiņas ID (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-314">Shift ID (required)</span></span>
- <span data-ttu-id="5efc2-315">Nodokļu numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-315">Tax Number (required)</span></span>
- <span data-ttu-id="5efc2-316">Arodbiedrības ID (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-316">Union ID (required)</span></span>
- <span data-ttu-id="5efc2-317">Darba dienas ID (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-317">Work Day ID (required)</span></span>
- <span data-ttu-id="5efc2-318">Darba atļaujas numurs</span><span class="sxs-lookup"><span data-stu-id="5efc2-318">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="5efc2-319">Meksika atbalsta šādas maksāšanas metodes: **Skaidra nauda**, **Čeks** (uzņēmuma fiziskais čeks) un **Elektroniskais maksājums**.</span><span class="sxs-lookup"><span data-stu-id="5efc2-319">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="5efc2-320">Ja nav norādīta neviena maksāšanas metode, pēc noklusējuma tiek izmantota opcija **Čeks**.</span><span class="sxs-lookup"><span data-stu-id="5efc2-320">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="5efc2-321">Nodarbinātības papildinformācija</span><span class="sxs-lookup"><span data-stu-id="5efc2-321">Employment details</span></span>

<span data-ttu-id="5efc2-322">Nodarbinātības datu vēsture pakalpojumā Dayforce tiek izmantota kā galvenā informācija, no kuras tiek iegūts darbinieka darbā pieņemšanas, darba attiecību izbeigšanas un atkārtotas pieņemšanas darbā statuss.</span><span class="sxs-lookup"><span data-stu-id="5efc2-322">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="5efc2-323">Dayforce vienlaikus atbalsta tikai vienu aktīvu nodarbinātības ierakstu.</span><span class="sxs-lookup"><span data-stu-id="5efc2-323">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="5efc2-324">Nodarbinātības sākuma datums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-324">Employment start date (required)</span></span>
- <span data-ttu-id="5efc2-325">Nodarbinātības beigu datums</span><span class="sxs-lookup"><span data-stu-id="5efc2-325">Employment end date</span></span>
- <span data-ttu-id="5efc2-326">Pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="5efc2-326">Start date</span></span>
- <span data-ttu-id="5efc2-327">Koriģētais pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="5efc2-327">Adjusted start date</span></span>
- <span data-ttu-id="5efc2-328">Darba attiecību pārtraukšanas datums (jānorāda, kad tiek pārtrauktas darba attiecības)</span><span class="sxs-lookup"><span data-stu-id="5efc2-328">Termination date (required upon termination)</span></span>
- <span data-ttu-id="5efc2-329">Darba attiecību pārtraukšanas iemesls (jānorāda, kad tiek pārtrauktas darba attiecības)</span><span class="sxs-lookup"><span data-stu-id="5efc2-329">Termination reason (required upon termination)</span></span>

<span data-ttu-id="5efc2-330">Darbinieka galvenie datumi tiek iegūti, izmantojot tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="5efc2-330">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="5efc2-331">Personāla vadība</span><span class="sxs-lookup"><span data-stu-id="5efc2-331">Human Resources</span></span>                | <span data-ttu-id="5efc2-332">Dayforce</span><span class="sxs-lookup"><span data-stu-id="5efc2-332">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5efc2-333">Pēdējais nomas datums</span><span class="sxs-lookup"><span data-stu-id="5efc2-333">Most recent hire date</span></span> | <span data-ttu-id="5efc2-334">Pašreizējā nepārtrauktās nodarbinātības vēstures ieraksta nodarbinātības sākums</span><span class="sxs-lookup"><span data-stu-id="5efc2-334">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="5efc2-335">Izbeigšanas datums</span><span class="sxs-lookup"><span data-stu-id="5efc2-335">Termination date</span></span>      | <span data-ttu-id="5efc2-336">Pašreizējā nepārtrauktās nodarbinātības vēstures ieraksta darba attiecību pārtraukšanas datums</span><span class="sxs-lookup"><span data-stu-id="5efc2-336">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="5efc2-337">Pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="5efc2-337">Start date</span></span>            | <span data-ttu-id="5efc2-338">Pašreizējā neaktīvā nodarbinātības vēstures ieraksta koriģētais sākuma datums, sākuma datums vai nodarbinātības sākums</span><span class="sxs-lookup"><span data-stu-id="5efc2-338">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="5efc2-339">Sākotnējais darbā pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="5efc2-339">Original hire date</span></span>    | <span data-ttu-id="5efc2-340">Agrākā nodarbinātības vēstures ieraksta nodarbinātības sākums</span><span class="sxs-lookup"><span data-stu-id="5efc2-340">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="5efc2-341">Atlīdzība</span><span class="sxs-lookup"><span data-stu-id="5efc2-341">Compensation</span></span>

<span data-ttu-id="5efc2-342">Fiksētās atlīdzības plānam ir jābūt saistītam ar katra darbinieka primāro amatu visā nodarbinātības periodā.</span><span class="sxs-lookup"><span data-stu-id="5efc2-342">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="5efc2-343">Šis periods sākas ar datumu, kurā darbinieks tika pieņemts darbā (vai nodarbinātības sākuma datumu), un turpinās līdz darba attiecību pārtraukšanai.</span><span class="sxs-lookup"><span data-stu-id="5efc2-343">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="5efc2-344">Spēkā stāšanās datums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-344">Effective Date (required)</span></span>
- <span data-ttu-id="5efc2-345">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="5efc2-345">Expiration date</span></span>
- <span data-ttu-id="5efc2-346">Apmaksas likme (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-346">Pay Rate (required)</span></span>
- <span data-ttu-id="5efc2-347">Apmaksas likmes konvertēšanas gadījumi (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-347">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="5efc2-348">Gada ekvivalents (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-348">Annual equivalent (required)</span></span>
- <span data-ttu-id="5efc2-349">Stundas ekvivalents (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-349">Hourly equivalent (required)</span></span>

<span data-ttu-id="5efc2-350">Ja darbiniekam ar stundas likmi ir vairāki amati, pakalpojumā Dayforce kā darbinieka līmeņa pamatlikme/alga tiek importēta primārā amata fiksētā atlīdzība.</span><span class="sxs-lookup"><span data-stu-id="5efc2-350">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="5efc2-351">To amatu, kas nav primārie, stundas likme tiek saglabāta pakalpojumā Dayforce attiecīgajā amatā.</span><span class="sxs-lookup"><span data-stu-id="5efc2-351">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="5efc2-352">Ja darbiniekam, kurš saņem algu, ir vairāki amati, kā darbinieka līmeņa pamatlikme/alga tiek iegūta un izmantota visu aktīvo amatu kopējā stundas likme un gada alga.</span><span class="sxs-lookup"><span data-stu-id="5efc2-352">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="5efc2-353">Identifikācijas numuri</span><span class="sxs-lookup"><span data-stu-id="5efc2-353">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="5efc2-354">Sociālās apdrošināšanas numurs</span><span class="sxs-lookup"><span data-stu-id="5efc2-354">Social Security identifier</span></span> 

<span data-ttu-id="5efc2-355">Katram darbiniekam ir jābūt vienam primārajam numuram.</span><span class="sxs-lookup"><span data-stu-id="5efc2-355">Every employee must have one primary identifier.</span></span> <span data-ttu-id="5efc2-356">Šī numura identifikācijas tipam ir jābūt **SAN**.</span><span class="sxs-lookup"><span data-stu-id="5efc2-356">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="5efc2-357">Pakalpojumā Dayforce tas tiek automātiski iegūts kā darbinieka sociālās apdrošināšanas numurs, kas ir jānorāda, kad darbinieks tiek pieņemts darbā.</span><span class="sxs-lookup"><span data-stu-id="5efc2-357">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="5efc2-358">Primārais (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-358">Primary (required)</span></span>
- <span data-ttu-id="5efc2-359">Identifikācijas tips = SAN</span><span class="sxs-lookup"><span data-stu-id="5efc2-359">Identification Type = "SSN"</span></span>
- <span data-ttu-id="5efc2-360">Izdošanas datums</span><span class="sxs-lookup"><span data-stu-id="5efc2-360">Issued Date</span></span>
- <span data-ttu-id="5efc2-361">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="5efc2-361">Expiration Date</span></span>

<span data-ttu-id="5efc2-362">Darbinieki var sniegt vairākus identifikācijas numurus, kuru identifikācijas tips ir **SAN**.</span><span class="sxs-lookup"><span data-stu-id="5efc2-362">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="5efc2-363">Taču pakalpojumā Dayforce tiek integrēts tikai ieraksts, kas ir atzīmēts kā **Primārais**, neatkarīgi no tā, vai šis numurs ir aktīvs vai tam ir beidzies derīgums.</span><span class="sxs-lookup"><span data-stu-id="5efc2-363">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="5efc2-364">Banku konti un izdevumi</span><span class="sxs-lookup"><span data-stu-id="5efc2-364">Bank accounts and disbursements</span></span>

<span data-ttu-id="5efc2-365">Jebkuram darbiniekam, kurš samaksu izvēlējies saņemt bankas konta pārskaitījuma veidā, ir jāievada derīga bankas konta informācija.</span><span class="sxs-lookup"><span data-stu-id="5efc2-365">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="5efc2-366">Personāla vadība</span><span class="sxs-lookup"><span data-stu-id="5efc2-366">Human Resources</span></span>                         | <span data-ttu-id="5efc2-367">Dayforce</span><span class="sxs-lookup"><span data-stu-id="5efc2-367">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5efc2-368">Bankas konta numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-368">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="5efc2-369">SWIFT kods (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-369">SWIFT code (required)</span></span>          | <span data-ttu-id="5efc2-370">Lauku **Bankas ID** izmanto, apstrādājot algas Meksikā.</span><span class="sxs-lookup"><span data-stu-id="5efc2-370">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="5efc2-371">Filiāles numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-371">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="5efc2-372">Bankas konta tips (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-372">Bank account type (required)</span></span>   | <span data-ttu-id="5efc2-373">Lauku **Konta tips** izmanto, apstrādājot algas Meksikā.</span><span class="sxs-lookup"><span data-stu-id="5efc2-373">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="5efc2-374">Atbalstītās vērtības ir, piemēram, **Norēķini** un **Algas**.</span><span class="sxs-lookup"><span data-stu-id="5efc2-374">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="5efc2-375">Darbiniekiem, kuri samaksu izvēlas saņemt bankas konta pārskaitījumu veidā, ir jāsniedz saite uz juridiskās personas, kuras primārā adrese ir Meksikā, atlikumu kontu, kas ir saistīts ar derīgu Meksikas bankas kontu.</span><span class="sxs-lookup"><span data-stu-id="5efc2-375">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="5efc2-376">Visi pārējie konti, kas nav atlikumu konti, tiek ignorēti.</span><span class="sxs-lookup"><span data-stu-id="5efc2-376">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="5efc2-377">Adreses informācija</span><span class="sxs-lookup"><span data-stu-id="5efc2-377">Address information</span></span>

<span data-ttu-id="5efc2-378">Katram darbiniekam ir jābūt vienai primārajai vietai.</span><span class="sxs-lookup"><span data-stu-id="5efc2-378">Every employee must have one primary location.</span></span> <span data-ttu-id="5efc2-379">Pakalpojumā Dayforce šī vieta tiek izmantota, lai nodokļu piemērošanas nolūkos noteiktu darbinieka primāro dzīvesvietu.</span><span class="sxs-lookup"><span data-stu-id="5efc2-379">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="5efc2-380">Primārā (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-380">Primary (required)</span></span>
- <span data-ttu-id="5efc2-381">Valsts/reģions (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-381">Country/region (required)</span></span>
- <span data-ttu-id="5efc2-382">Pasta indekss (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-382">Zip/postal code (required)</span></span>
- <span data-ttu-id="5efc2-383">Iela (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-383">Street (required)</span></span>
- <span data-ttu-id="5efc2-384">Ielas numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-384">Street Number (required)</span></span>
- <span data-ttu-id="5efc2-385">Mājas numurs/nosaukums</span><span class="sxs-lookup"><span data-stu-id="5efc2-385">Building Complement</span></span>
- <span data-ttu-id="5efc2-386">Pilsēta (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-386">City (required)</span></span>
- <span data-ttu-id="5efc2-387">Administratīvais apgabals (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-387">State (required)</span></span>
- <span data-ttu-id="5efc2-388">Apgabals (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-388">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="5efc2-389">Datu konfigurēšana algu ģenerēšanai Amerikas Savienotajās Valstīs un Kanādā</span><span class="sxs-lookup"><span data-stu-id="5efc2-389">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="5efc2-390">Ja ģenerējat algas darbiniekiem Amerikas Savienotajās Valstīs un Kanādā, ir jākonfigurē tālāk norādītie elementi.</span><span class="sxs-lookup"><span data-stu-id="5efc2-390">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="5efc2-391">Amatiem ir jānorāda nodaļas.</span><span class="sxs-lookup"><span data-stu-id="5efc2-391">Departments are required on positions.</span></span>
- <span data-ttu-id="5efc2-392">Izmaksu centri ir jāiestata kā finanšu dimensijas, un tiem ir jābūt pirmajiem elementiem noklusējuma finanšu dimensijas virknē.</span><span class="sxs-lookup"><span data-stu-id="5efc2-392">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="5efc2-393">Varat konfigurēt Human Resources, lai amatiem būtu jānorāda nodaļa.</span><span class="sxs-lookup"><span data-stu-id="5efc2-393">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="5efc2-394">Lai to izdarītu, pārejiet uz **Personāla vadības kopīgotie amati > Amati > Pieprasīt amatiem nodaļas**.</span><span class="sxs-lookup"><span data-stu-id="5efc2-394">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="5efc2-395">Ieteicams piemērot šo iestatījumu integrācijai.</span><span class="sxs-lookup"><span data-stu-id="5efc2-395">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="5efc2-396">Darba tipi</span><span class="sxs-lookup"><span data-stu-id="5efc2-396">Job types</span></span>

<span data-ttu-id="5efc2-397">Darbu veidi tiek izmantoti, lai līdzīgus darbus grupētu kategorijās.</span><span class="sxs-lookup"><span data-stu-id="5efc2-397">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="5efc2-398">Darbu veidi ir nepieciešami, lai apstrādātu algas Amerikas Savienotajās Valstīs un Kanādā.</span><span class="sxs-lookup"><span data-stu-id="5efc2-398">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="5efc2-399">Daži darbu veidu piemēri ir pilna laika, nepilna laika, algots un stundu apmaksas darbs.</span><span class="sxs-lookup"><span data-stu-id="5efc2-399">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="5efc2-400">Darbu veidi tiek kartēti uz pakalpojumu Dayforce kā apmaksas tipi, lai norādītu, vai darbinieks saņem stundas samaksu vai algu.</span><span class="sxs-lookup"><span data-stu-id="5efc2-400">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="5efc2-401">Ir jānorāda tālāk norādītie darbu veidi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="5efc2-401">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="5efc2-402">Darba veids</span><span class="sxs-lookup"><span data-stu-id="5efc2-402">Job type</span></span>   | <span data-ttu-id="5efc2-403">apraksts</span><span class="sxs-lookup"><span data-stu-id="5efc2-403">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="5efc2-404">Ik stundu</span><span class="sxs-lookup"><span data-stu-id="5efc2-404">Hourly</span></span>     | <span data-ttu-id="5efc2-405">Ik stundu</span><span class="sxs-lookup"><span data-stu-id="5efc2-405">Hourly</span></span>      |
| <span data-ttu-id="5efc2-406">Algots</span><span class="sxs-lookup"><span data-stu-id="5efc2-406">Salaried</span></span>   | <span data-ttu-id="5efc2-407">Algots</span><span class="sxs-lookup"><span data-stu-id="5efc2-407">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="5efc2-408">Amatu veidi</span><span class="sxs-lookup"><span data-stu-id="5efc2-408">Position types</span></span> 

<span data-ttu-id="5efc2-409">Amatu veidus izmanto, lai norādītu, vai amats ir pilna laika, nepilna laika vai cita veida darbs.</span><span class="sxs-lookup"><span data-stu-id="5efc2-409">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="5efc2-410">Amatu veidi tiek kartēti uz pakalpojumu Dayforce kā apmaksas klases, lai norādītu, vai darbinieks ir pilna laika vai nepilna laika darbinieks.</span><span class="sxs-lookup"><span data-stu-id="5efc2-410">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="5efc2-411">Ir jānorāda tālāk norādītie amatu veidi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="5efc2-411">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="5efc2-412">Amata tips</span><span class="sxs-lookup"><span data-stu-id="5efc2-412">Position type</span></span>   | <span data-ttu-id="5efc2-413">apraksts</span><span class="sxs-lookup"><span data-stu-id="5efc2-413">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="5efc2-414">Pilna laika</span><span class="sxs-lookup"><span data-stu-id="5efc2-414">Full-time</span></span>       | <span data-ttu-id="5efc2-415">Pilna laika darbinieks</span><span class="sxs-lookup"><span data-stu-id="5efc2-415">Full time employee</span></span> |
| <span data-ttu-id="5efc2-416">Nepilna laika</span><span class="sxs-lookup"><span data-stu-id="5efc2-416">Part-time</span></span>       | <span data-ttu-id="5efc2-417">Nepilna laika darbinieks</span><span class="sxs-lookup"><span data-stu-id="5efc2-417">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="5efc2-418">Iemeslu kodi</span><span class="sxs-lookup"><span data-stu-id="5efc2-418">Reason codes</span></span>

<span data-ttu-id="5efc2-419">Iemeslu kodi sniedz informāciju par darbinieka statusu.</span><span class="sxs-lookup"><span data-stu-id="5efc2-419">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="5efc2-420">Iemeslu kodu tiek kartēti uz pakalpojumu Dayforce kā statusa iemesli, kas norāda darbinieka amata vai nodarbinātības statusa izmaiņu iemeslu.</span><span class="sxs-lookup"><span data-stu-id="5efc2-420">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="5efc2-421">Ir jānorāda tālāk norādītie iemeslu kodi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="5efc2-421">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="5efc2-422">Iemeslu kodi</span><span class="sxs-lookup"><span data-stu-id="5efc2-422">Reason code</span></span>    | <span data-ttu-id="5efc2-423">apraksts</span><span class="sxs-lookup"><span data-stu-id="5efc2-423">Description</span></span>      | <span data-ttu-id="5efc2-424">Piemērojamie scenāriji</span><span class="sxs-lookup"><span data-stu-id="5efc2-424">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="5efc2-425">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="5efc2-425">RESIGNATION</span></span>    | <span data-ttu-id="5efc2-426">Atlūgums</span><span class="sxs-lookup"><span data-stu-id="5efc2-426">Resignation</span></span>      | <span data-ttu-id="5efc2-427">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="5efc2-427">Terminate worker</span></span>     |
| <span data-ttu-id="5efc2-428">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="5efc2-428">TERMINATION</span></span>    | <span data-ttu-id="5efc2-429">Izbeigšana</span><span class="sxs-lookup"><span data-stu-id="5efc2-429">Termination</span></span>      | <span data-ttu-id="5efc2-430">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="5efc2-430">Terminate worker</span></span>     |
| <span data-ttu-id="5efc2-431">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="5efc2-431">RETIREMENT</span></span>     | <span data-ttu-id="5efc2-432">Aiziešana pensijā</span><span class="sxs-lookup"><span data-stu-id="5efc2-432">Retirement</span></span>       | <span data-ttu-id="5efc2-433">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="5efc2-433">Terminate worker</span></span>     |
| <span data-ttu-id="5efc2-434">CITI</span><span class="sxs-lookup"><span data-stu-id="5efc2-434">OTHER</span></span>          | <span data-ttu-id="5efc2-435">Citi iemesli</span><span class="sxs-lookup"><span data-stu-id="5efc2-435">Other Reasons</span></span>    | <span data-ttu-id="5efc2-436">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="5efc2-436">Terminate worker</span></span>     |
| <span data-ttu-id="5efc2-437">DEATH</span><span class="sxs-lookup"><span data-stu-id="5efc2-437">DEATH</span></span>          | <span data-ttu-id="5efc2-438">Nāve</span><span class="sxs-lookup"><span data-stu-id="5efc2-438">Death</span></span>            | <span data-ttu-id="5efc2-439">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="5efc2-439">Terminate worker</span></span>     |
| <span data-ttu-id="5efc2-440">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="5efc2-440">LEAVEOFABSENCE</span></span> | <span data-ttu-id="5efc2-441">Atvaļinājums</span><span class="sxs-lookup"><span data-stu-id="5efc2-441">Leave of Absence</span></span> | <span data-ttu-id="5efc2-442">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="5efc2-442">Terminate worker</span></span>     |
| <span data-ttu-id="5efc2-443">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="5efc2-443">CONTRACTEND</span></span>    | <span data-ttu-id="5efc2-444">Līguma beigas</span><span class="sxs-lookup"><span data-stu-id="5efc2-444">End of Contract</span></span>  | <span data-ttu-id="5efc2-445">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="5efc2-445">Terminate worker</span></span>     |
| <span data-ttu-id="5efc2-446">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="5efc2-446">SALARYCHANGE</span></span>   | <span data-ttu-id="5efc2-447">Algas izmaiņas</span><span class="sxs-lookup"><span data-stu-id="5efc2-447">Change of Salary</span></span> | <span data-ttu-id="5efc2-448">Atlīdzība</span><span class="sxs-lookup"><span data-stu-id="5efc2-448">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="5efc2-449">Ģimenes stāvoklis</span><span class="sxs-lookup"><span data-stu-id="5efc2-449">Marital status</span></span>

<span data-ttu-id="5efc2-450">Ģimenes statusa vērtības tiek kartētas uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkotas uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="5efc2-450">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="5efc2-451">Tālāk esošajā tabulā ir parādīts, kā ģimenes statusa vērtības tiek kartētas uz pakalpojumu Dayforce.</span><span class="sxs-lookup"><span data-stu-id="5efc2-451">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="5efc2-452">Personāla vadība</span><span class="sxs-lookup"><span data-stu-id="5efc2-452">Human Resources</span></span>                 | <span data-ttu-id="5efc2-453">Dayforce</span><span class="sxs-lookup"><span data-stu-id="5efc2-453">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="5efc2-454">Precējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="5efc2-454">Married</span></span>                | <span data-ttu-id="5efc2-455">Precējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="5efc2-455">Married</span></span>              |
| <span data-ttu-id="5efc2-456">Atsevišķs</span><span class="sxs-lookup"><span data-stu-id="5efc2-456">Single</span></span>                 | <span data-ttu-id="5efc2-457">Atsevišķs</span><span class="sxs-lookup"><span data-stu-id="5efc2-457">Single</span></span>               |
| <span data-ttu-id="5efc2-458">Atraitnis (-ne)</span><span class="sxs-lookup"><span data-stu-id="5efc2-458">Widowed</span></span>                | <span data-ttu-id="5efc2-459">Atraitnis (-ne)</span><span class="sxs-lookup"><span data-stu-id="5efc2-459">Widowed</span></span>              |
| <span data-ttu-id="5efc2-460">Šķīries (-usies)</span><span class="sxs-lookup"><span data-stu-id="5efc2-460">Divorced</span></span>               | <span data-ttu-id="5efc2-461">Šķīries (-usies)</span><span class="sxs-lookup"><span data-stu-id="5efc2-461">Divorced</span></span>             |
| <span data-ttu-id="5efc2-462">Reģistrētas attiecības</span><span class="sxs-lookup"><span data-stu-id="5efc2-462">Registered Partnership</span></span> | <span data-ttu-id="5efc2-463">Dzīvesbiedrs</span><span class="sxs-lookup"><span data-stu-id="5efc2-463">Domestic Partnership</span></span> |
| <span data-ttu-id="5efc2-464">Neviens</span><span class="sxs-lookup"><span data-stu-id="5efc2-464">None</span></span>                   | <span data-ttu-id="5efc2-465">Neviens</span><span class="sxs-lookup"><span data-stu-id="5efc2-465">None</span></span>                 |
| <span data-ttu-id="5efc2-466">Kopdzīve</span><span class="sxs-lookup"><span data-stu-id="5efc2-466">Cohabiting</span></span>             | <span data-ttu-id="5efc2-467">Kopdzīve</span><span class="sxs-lookup"><span data-stu-id="5efc2-467">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="5efc2-468">Dzimums</span><span class="sxs-lookup"><span data-stu-id="5efc2-468">Gender</span></span>

<span data-ttu-id="5efc2-469">Dzimuma apzīmējumi tiek kartēti uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkoti uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="5efc2-469">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="5efc2-470">Tālāk esošajā tabulā ir parādīts, kā dzimuma apzīmējumi tiek kartēti uz pakalpojumu Dayforce.</span><span class="sxs-lookup"><span data-stu-id="5efc2-470">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="5efc2-471">Personāla vadība</span><span class="sxs-lookup"><span data-stu-id="5efc2-471">Human Resources</span></span>       | <span data-ttu-id="5efc2-472">Dayforce</span><span class="sxs-lookup"><span data-stu-id="5efc2-472">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="5efc2-473">Vīrietis</span><span class="sxs-lookup"><span data-stu-id="5efc2-473">Male</span></span>         | <span data-ttu-id="5efc2-474">Vīrietis</span><span class="sxs-lookup"><span data-stu-id="5efc2-474">Male</span></span>            |
| <span data-ttu-id="5efc2-475">Sieviete</span><span class="sxs-lookup"><span data-stu-id="5efc2-475">Female</span></span>       | <span data-ttu-id="5efc2-476">Sieviete</span><span class="sxs-lookup"><span data-stu-id="5efc2-476">Female</span></span>          |
| <span data-ttu-id="5efc2-477">Nav specifisks</span><span class="sxs-lookup"><span data-stu-id="5efc2-477">Non-specific</span></span> | <span data-ttu-id="5efc2-478">*Netiek atbalstīts*</span><span class="sxs-lookup"><span data-stu-id="5efc2-478">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="5efc2-479">Ienākumu veida kodi</span><span class="sxs-lookup"><span data-stu-id="5efc2-479">Earning codes</span></span>

<span data-ttu-id="5efc2-480">Ienākumu veidu kodi unikāli identificē katra veida ienākumus, ko saņem nodarbinātie.</span><span class="sxs-lookup"><span data-stu-id="5efc2-480">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="5efc2-481">Kodiem ir vairāki ar ienākumiem saistīti parametri, piemēram, uzskaites nosacījumi, nodokļu likumi, pārskatu veidošanas prasības un bruto summas palielināšanas iespēja.</span><span class="sxs-lookup"><span data-stu-id="5efc2-481">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="5efc2-482">Ja tiek izmantota neatbalstīta biežuma vērtība, aprēķinā pēc noklusējuma tiek lietota biežuma vērtība **Katra apmaksa**.</span><span class="sxs-lookup"><span data-stu-id="5efc2-482">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="5efc2-483">Atbalstītās biežuma vērtības</span><span class="sxs-lookup"><span data-stu-id="5efc2-483">Supported frequencies</span></span>

- <span data-ttu-id="5efc2-484">Visus</span><span class="sxs-lookup"><span data-stu-id="5efc2-484">All</span></span>
- <span data-ttu-id="5efc2-485">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="5efc2-485">EVERYPAY</span></span>
- <span data-ttu-id="5efc2-486">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="5efc2-486">EACHPAYPERIOD</span></span>
- <span data-ttu-id="5efc2-487">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="5efc2-487">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="5efc2-488">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="5efc2-488">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="5efc2-489">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="5efc2-489">1OFMTH</span></span>
- <span data-ttu-id="5efc2-490">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="5efc2-490">LASTOFMTH</span></span>
- <span data-ttu-id="5efc2-491">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="5efc2-491">2OFMTH</span></span>
- <span data-ttu-id="5efc2-492">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="5efc2-492">3OFMTH</span></span>
- <span data-ttu-id="5efc2-493">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="5efc2-493">4OFMTH</span></span>
- <span data-ttu-id="5efc2-494">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="5efc2-494">5OFMTH</span></span>
- <span data-ttu-id="5efc2-495">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="5efc2-495">1N2OFMTH</span></span>
- <span data-ttu-id="5efc2-496">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="5efc2-496">3N4OFMTH</span></span>
- <span data-ttu-id="5efc2-497">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="5efc2-497">1N3OFMTH</span></span>
- <span data-ttu-id="5efc2-498">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="5efc2-498">1N4OFMTH</span></span>
- <span data-ttu-id="5efc2-499">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="5efc2-499">2N3OFMTH</span></span>
- <span data-ttu-id="5efc2-500">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="5efc2-500">2N4OFMTH</span></span>
- <span data-ttu-id="5efc2-501">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="5efc2-501">1N2N3OFMTH</span></span>
- <span data-ttu-id="5efc2-502">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="5efc2-502">1N2N4OFMTH</span></span>
- <span data-ttu-id="5efc2-503">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="5efc2-503">1N3N4OFMTH</span></span>
- <span data-ttu-id="5efc2-504">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="5efc2-504">2N3N4OFMTH</span></span>
- <span data-ttu-id="5efc2-505">1N2N3N4OFMTH–1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="5efc2-505">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="5efc2-506">2N3N4N5OFMth–2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="5efc2-506">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="5efc2-507">1OFQTR–1OFQTR</span><span class="sxs-lookup"><span data-stu-id="5efc2-507">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="5efc2-508">LASTOFQTR–LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="5efc2-508">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="5efc2-509">LASTMTHOFQTR–LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="5efc2-509">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="5efc2-510">1OFYEAR–1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="5efc2-510">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="5efc2-511">LASTOFYEAR–LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="5efc2-511">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="5efc2-512">NOVNDECOFYEAR–NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="5efc2-512">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="5efc2-513">Adreses</span><span class="sxs-lookup"><span data-stu-id="5efc2-513">Addresses</span></span>

<span data-ttu-id="5efc2-514">Noteiktas valsts vai reģiona, administratīvā apgabala un apgabala (pašvaldības) kodu identifikācijai ir nepieciešami konkrēti formāti, ko var atpazīt pakalpojums Dayforce un valsts/reģiona pakalpojumu sniedzēji.</span><span class="sxs-lookup"><span data-stu-id="5efc2-514">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="5efc2-515">Lai gan pilsētu formāts var būt dažāds, katrai pilsētai ir jābūt saistītai ar administratīvo apgabalu.</span><span class="sxs-lookup"><span data-stu-id="5efc2-515">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="5efc2-516">Personāla vadība</span><span class="sxs-lookup"><span data-stu-id="5efc2-516">Human Resources</span></span>          | <span data-ttu-id="5efc2-517">Dayforce</span><span class="sxs-lookup"><span data-stu-id="5efc2-517">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="5efc2-518">Valsts/reģions</span><span class="sxs-lookup"><span data-stu-id="5efc2-518">Country/Region</span></span>  | <span data-ttu-id="5efc2-519">Valsts kods</span><span class="sxs-lookup"><span data-stu-id="5efc2-519">Country Code</span></span>          |
| <span data-ttu-id="5efc2-520">Pasta indekss</span><span class="sxs-lookup"><span data-stu-id="5efc2-520">Zip/Postal Code</span></span> | <span data-ttu-id="5efc2-521">Pasta indekss</span><span class="sxs-lookup"><span data-stu-id="5efc2-521">Postal Code</span></span>           |
| <span data-ttu-id="5efc2-522">Administratīvais apgabals</span><span class="sxs-lookup"><span data-stu-id="5efc2-522">State</span></span>           | <span data-ttu-id="5efc2-523">Administratīvā apgabala kods</span><span class="sxs-lookup"><span data-stu-id="5efc2-523">State Code</span></span>            |
| <span data-ttu-id="5efc2-524">Pilsēta</span><span class="sxs-lookup"><span data-stu-id="5efc2-524">City</span></span>            | <span data-ttu-id="5efc2-525">Pilsēta</span><span class="sxs-lookup"><span data-stu-id="5efc2-525">City</span></span>                  |
| <span data-ttu-id="5efc2-526">Apgabals</span><span class="sxs-lookup"><span data-stu-id="5efc2-526">County</span></span>          | <span data-ttu-id="5efc2-527">Apgabals (pašvaldība)</span><span class="sxs-lookup"><span data-stu-id="5efc2-527">County (Municipality)</span></span> |
| <span data-ttu-id="5efc2-528">Iela</span><span class="sxs-lookup"><span data-stu-id="5efc2-528">Street</span></span>          | <span data-ttu-id="5efc2-529">Adreses 1. rinda</span><span class="sxs-lookup"><span data-stu-id="5efc2-529">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="5efc2-530">Nodokļu reģioni</span><span class="sxs-lookup"><span data-stu-id="5efc2-530">Tax regions</span></span>

<span data-ttu-id="5efc2-531">Nodokļu reģionus izmanto, lai noteiktu atbilstošos nodokļus, kas jāpiemēro, ģenerējot algu aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="5efc2-531">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="5efc2-532">Nodokļu reģioni tiek kartēti uz pakalpojumu Dayforce kā vietas adreses.</span><span class="sxs-lookup"><span data-stu-id="5efc2-532">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="5efc2-533">Noklusējuma nodokļu reģionam ir jābūt saistītam ar nodarbinātā aktīvo amatu.</span><span class="sxs-lookup"><span data-stu-id="5efc2-533">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="5efc2-534">Nodokļu reģions (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-534">Tax region (required)</span></span>
- <span data-ttu-id="5efc2-535">Valsts/reģions (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-535">Country/Region (required)</span></span>
- <span data-ttu-id="5efc2-536">Administratīvais apgabals (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-536">State (required)</span></span>
- <span data-ttu-id="5efc2-537">Apgabals</span><span class="sxs-lookup"><span data-stu-id="5efc2-537">County</span></span> 
- <span data-ttu-id="5efc2-538">Pilsēta (obligāti)</span><span class="sxs-lookup"><span data-stu-id="5efc2-538">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="5efc2-539">Datu konfigurēšana algu aprēķina ģenerēšanai Meksikā</span><span class="sxs-lookup"><span data-stu-id="5efc2-539">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="5efc2-540">Ja ģenerējat algas darbiniekiem Meksikā, ir jākonfigurē tālāk norādītie elementi.</span><span class="sxs-lookup"><span data-stu-id="5efc2-540">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="5efc2-541">Amatiem ir jānorāda nodaļas.</span><span class="sxs-lookup"><span data-stu-id="5efc2-541">Departments are required on positions.</span></span>
- <span data-ttu-id="5efc2-542">Izmaksu centri ir jāiestata kā finanšu dimensijas, un tiem ir jābūt pirmajiem elementiem noklusējuma finanšu dimensijas virknē.</span><span class="sxs-lookup"><span data-stu-id="5efc2-542">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="5efc2-543">Darba tipi</span><span class="sxs-lookup"><span data-stu-id="5efc2-543">Job types</span></span>

<span data-ttu-id="5efc2-544">Darbu veidi tiek izmantoti, lai līdzīgus darbus grupētu kategorijās.</span><span class="sxs-lookup"><span data-stu-id="5efc2-544">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="5efc2-545">Lai apstrādātu algas Meksikā, ir nepieciešami darbu veidi.</span><span class="sxs-lookup"><span data-stu-id="5efc2-545">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="5efc2-546">Daži darbu veidu piemēri ir pilna laika, nepilna laika, algots un stundu apmaksas darbs.</span><span class="sxs-lookup"><span data-stu-id="5efc2-546">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="5efc2-547">Darbu veidi tiek kartēti uz pakalpojumu Dayforce kā apmaksas tipi, lai norādītu, vai darbinieks saņem stundas samaksu vai algu.</span><span class="sxs-lookup"><span data-stu-id="5efc2-547">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="5efc2-548">Ir jānorāda tālāk norādītie darbu veidi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="5efc2-548">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="5efc2-549">Darba veids</span><span class="sxs-lookup"><span data-stu-id="5efc2-549">Job type</span></span>   | <span data-ttu-id="5efc2-550">apraksts</span><span class="sxs-lookup"><span data-stu-id="5efc2-550">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="5efc2-551">Ik stundu</span><span class="sxs-lookup"><span data-stu-id="5efc2-551">Hourly</span></span>     | <span data-ttu-id="5efc2-552">Stundu (MX)</span><span class="sxs-lookup"><span data-stu-id="5efc2-552">MX Hourly</span></span>   |
| <span data-ttu-id="5efc2-553">Algots</span><span class="sxs-lookup"><span data-stu-id="5efc2-553">Salaried</span></span>   | <span data-ttu-id="5efc2-554">Algots (MX)</span><span class="sxs-lookup"><span data-stu-id="5efc2-554">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="5efc2-555">Amatu veidi</span><span class="sxs-lookup"><span data-stu-id="5efc2-555">Position types</span></span> 

<span data-ttu-id="5efc2-556">Amatu veidus izmanto, lai norādītu, vai amats ir pilna laika, nepilna laika vai cita veida darbs.</span><span class="sxs-lookup"><span data-stu-id="5efc2-556">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="5efc2-557">Amatu veidi tiek kartēti uz pakalpojumu Dayforce kā apmaksas klases, lai norādītu, vai darbinieks ir pilna laika vai nepilna laika darbinieks.</span><span class="sxs-lookup"><span data-stu-id="5efc2-557">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="5efc2-558">Ir jānorāda tālāk norādītie amatu veidi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="5efc2-558">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="5efc2-559">Amata tips</span><span class="sxs-lookup"><span data-stu-id="5efc2-559">Position type</span></span>   | <span data-ttu-id="5efc2-560">apraksts</span><span class="sxs-lookup"><span data-stu-id="5efc2-560">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="5efc2-561">Pilna laika</span><span class="sxs-lookup"><span data-stu-id="5efc2-561">Full-time</span></span>       | <span data-ttu-id="5efc2-562">Pilna laika darbinieks</span><span class="sxs-lookup"><span data-stu-id="5efc2-562">Full time employee</span></span> |
| <span data-ttu-id="5efc2-563">Nepilna laika</span><span class="sxs-lookup"><span data-stu-id="5efc2-563">Part-time</span></span>       | <span data-ttu-id="5efc2-564">Nepilna laika darbinieks</span><span class="sxs-lookup"><span data-stu-id="5efc2-564">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="5efc2-565">Iemeslu kodi</span><span class="sxs-lookup"><span data-stu-id="5efc2-565">Reason codes</span></span>

<span data-ttu-id="5efc2-566">Iemeslu kodi sniedz informāciju par darbinieka statusu.</span><span class="sxs-lookup"><span data-stu-id="5efc2-566">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="5efc2-567">Iemeslu kodu tiek kartēti uz pakalpojumu Dayforce kā statusa iemesli, kas norāda darbinieka amata vai nodarbinātības statusa izmaiņu iemeslu.</span><span class="sxs-lookup"><span data-stu-id="5efc2-567">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="5efc2-568">Ir jānorāda tālāk norādītie iemeslu kodi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="5efc2-568">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="5efc2-569">Iemeslu kodi</span><span class="sxs-lookup"><span data-stu-id="5efc2-569">Reason code</span></span>            | <span data-ttu-id="5efc2-570">apraksts</span><span class="sxs-lookup"><span data-stu-id="5efc2-570">Description</span></span>                    | <span data-ttu-id="5efc2-571">Piemērojamie scenāriji</span><span class="sxs-lookup"><span data-stu-id="5efc2-571">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="5efc2-572">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="5efc2-572">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="5efc2-573">Aiziešana no amata pirms pirmās algas</span><span class="sxs-lookup"><span data-stu-id="5efc2-573">Departure before first payroll</span></span> | <span data-ttu-id="5efc2-574">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="5efc2-574">Terminate worker</span></span>     |
| <span data-ttu-id="5efc2-575">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="5efc2-575">RESIGNATION</span></span>            | <span data-ttu-id="5efc2-576">Atlūgums</span><span class="sxs-lookup"><span data-stu-id="5efc2-576">Resignation</span></span>                    | <span data-ttu-id="5efc2-577">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="5efc2-577">Terminate worker</span></span>     |
| <span data-ttu-id="5efc2-578">PENSION</span><span class="sxs-lookup"><span data-stu-id="5efc2-578">PENSION</span></span>                | <span data-ttu-id="5efc2-579">Pensija</span><span class="sxs-lookup"><span data-stu-id="5efc2-579">Pension</span></span>                        | <span data-ttu-id="5efc2-580">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="5efc2-580">Terminate worker</span></span>     |
| <span data-ttu-id="5efc2-581">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="5efc2-581">TERMINATION</span></span>            | <span data-ttu-id="5efc2-582">Izbeigšana</span><span class="sxs-lookup"><span data-stu-id="5efc2-582">Termination</span></span>                    | <span data-ttu-id="5efc2-583">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="5efc2-583">Terminate worker</span></span>     |
| <span data-ttu-id="5efc2-584">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="5efc2-584">RETIREMENT</span></span>             | <span data-ttu-id="5efc2-585">Aiziešana pensijā</span><span class="sxs-lookup"><span data-stu-id="5efc2-585">Retirement</span></span>                     | <span data-ttu-id="5efc2-586">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="5efc2-586">Terminate worker</span></span>     |
| <span data-ttu-id="5efc2-587">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="5efc2-587">ABSENTEE</span></span>               | <span data-ttu-id="5efc2-588">Darba kavētājs</span><span class="sxs-lookup"><span data-stu-id="5efc2-588">Absentee</span></span>                       | <span data-ttu-id="5efc2-589">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="5efc2-589">Terminate worker</span></span>     |
| <span data-ttu-id="5efc2-590">CITI</span><span class="sxs-lookup"><span data-stu-id="5efc2-590">OTHER</span></span>                  | <span data-ttu-id="5efc2-591">Citi iemesli</span><span class="sxs-lookup"><span data-stu-id="5efc2-591">Other Reasons</span></span>                  | <span data-ttu-id="5efc2-592">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="5efc2-592">Terminate worker</span></span>     |
| <span data-ttu-id="5efc2-593">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="5efc2-593">CLOSURE</span></span>                | <span data-ttu-id="5efc2-594">Uzņēmuma slēgšana</span><span class="sxs-lookup"><span data-stu-id="5efc2-594">Business Closure</span></span>               | <span data-ttu-id="5efc2-595">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="5efc2-595">Terminate worker</span></span>     |
| <span data-ttu-id="5efc2-596">DEATH</span><span class="sxs-lookup"><span data-stu-id="5efc2-596">DEATH</span></span>                  | <span data-ttu-id="5efc2-597">Nāve</span><span class="sxs-lookup"><span data-stu-id="5efc2-597">Death</span></span>                          | <span data-ttu-id="5efc2-598">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="5efc2-598">Terminate worker</span></span>     |
| <span data-ttu-id="5efc2-599">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="5efc2-599">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="5efc2-600">Atvaļinājums</span><span class="sxs-lookup"><span data-stu-id="5efc2-600">Leave of Absence</span></span>               | <span data-ttu-id="5efc2-601">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="5efc2-601">Terminate worker</span></span>     |
| <span data-ttu-id="5efc2-602">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="5efc2-602">CONTRACTEND</span></span>            | <span data-ttu-id="5efc2-603">Līguma beigas</span><span class="sxs-lookup"><span data-stu-id="5efc2-603">End of Contract</span></span>                | <span data-ttu-id="5efc2-604">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="5efc2-604">Terminate worker</span></span>     |
| <span data-ttu-id="5efc2-605">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="5efc2-605">SALARYCHANGE</span></span>           | <span data-ttu-id="5efc2-606">Algas izmaiņas</span><span class="sxs-lookup"><span data-stu-id="5efc2-606">Change of Salary</span></span>               | <span data-ttu-id="5efc2-607">Atlīdzība</span><span class="sxs-lookup"><span data-stu-id="5efc2-607">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="5efc2-608">Nodarbinātības noteikumi</span><span class="sxs-lookup"><span data-stu-id="5efc2-608">Terms of employment</span></span>

<span data-ttu-id="5efc2-609">Nodarbinātības noteikumus izmanto, lai izveidotu nodarbinātības noteikumu kategorijas.</span><span class="sxs-lookup"><span data-stu-id="5efc2-609">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="5efc2-610">Noteikumi tiek kartēti uz pakalpojumu Dayforce kā nodarbinātības rādītāju vērtības.</span><span class="sxs-lookup"><span data-stu-id="5efc2-610">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="5efc2-611">Ir nepieciešami tālāk norādītie nodarbinātības noteikumi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="5efc2-611">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="5efc2-612">Nodarbinātības noteikumi</span><span class="sxs-lookup"><span data-stu-id="5efc2-612">Terms of employment</span></span>   | <span data-ttu-id="5efc2-613">apraksts</span><span class="sxs-lookup"><span data-stu-id="5efc2-613">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="5efc2-614">Regulārs</span><span class="sxs-lookup"><span data-stu-id="5efc2-614">Regular</span></span>               | <span data-ttu-id="5efc2-615">Regulārs</span><span class="sxs-lookup"><span data-stu-id="5efc2-615">Regular</span></span>     |
| <span data-ttu-id="5efc2-616">Tieši</span><span class="sxs-lookup"><span data-stu-id="5efc2-616">Direct</span></span>                | <span data-ttu-id="5efc2-617">Tieši</span><span class="sxs-lookup"><span data-stu-id="5efc2-617">Direct</span></span>      |
| <span data-ttu-id="5efc2-618">Štažēšanās</span><span class="sxs-lookup"><span data-stu-id="5efc2-618">Internship</span></span>            | <span data-ttu-id="5efc2-619">Štažēšanās</span><span class="sxs-lookup"><span data-stu-id="5efc2-619">Internship</span></span>  |
| <span data-ttu-id="5efc2-620">Pastāvīga</span><span class="sxs-lookup"><span data-stu-id="5efc2-620">Permanent</span></span>             | <span data-ttu-id="5efc2-621">Pastāvīga</span><span class="sxs-lookup"><span data-stu-id="5efc2-621">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="5efc2-622">Ģimenes stāvoklis</span><span class="sxs-lookup"><span data-stu-id="5efc2-622">Marital status</span></span>

<span data-ttu-id="5efc2-623">Ģimenes statusa vērtības tiek kartētas uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkotas uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="5efc2-623">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="5efc2-624">Tālāk esošajā tabulā ir parādīts, kā ģimenes statusa vērtības tiek kartētas uz pakalpojumu Dayforce.</span><span class="sxs-lookup"><span data-stu-id="5efc2-624">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="5efc2-625">Personāla vadība</span><span class="sxs-lookup"><span data-stu-id="5efc2-625">Human Resources</span></span>                 | <span data-ttu-id="5efc2-626">Dayforce</span><span class="sxs-lookup"><span data-stu-id="5efc2-626">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="5efc2-627">Precējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="5efc2-627">Married</span></span>                | <span data-ttu-id="5efc2-628">Precējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="5efc2-628">Married</span></span>                   |
| <span data-ttu-id="5efc2-629">Atsevišķs</span><span class="sxs-lookup"><span data-stu-id="5efc2-629">Single</span></span>                 | <span data-ttu-id="5efc2-630">Atsevišķs</span><span class="sxs-lookup"><span data-stu-id="5efc2-630">Single</span></span>                    |
| <span data-ttu-id="5efc2-631">Atraitnis (-ne)</span><span class="sxs-lookup"><span data-stu-id="5efc2-631">Widowed</span></span>                | <span data-ttu-id="5efc2-632">Atraitnis (-ne)</span><span class="sxs-lookup"><span data-stu-id="5efc2-632">Widowed</span></span>                   |
| <span data-ttu-id="5efc2-633">Šķīries (-usies)</span><span class="sxs-lookup"><span data-stu-id="5efc2-633">Divorced</span></span>               | <span data-ttu-id="5efc2-634">Šķīries (-usies)</span><span class="sxs-lookup"><span data-stu-id="5efc2-634">Divorced</span></span>                  |
| <span data-ttu-id="5efc2-635">Reģistrētas attiecības</span><span class="sxs-lookup"><span data-stu-id="5efc2-635">Registered Partnership</span></span> | <span data-ttu-id="5efc2-636">Dzīvesbiedrs</span><span class="sxs-lookup"><span data-stu-id="5efc2-636">Domestic Partnership</span></span>      |
| <span data-ttu-id="5efc2-637">Neviens</span><span class="sxs-lookup"><span data-stu-id="5efc2-637">None</span></span>                   | <span data-ttu-id="5efc2-638">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="5efc2-638">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="5efc2-639">Kopdzīve</span><span class="sxs-lookup"><span data-stu-id="5efc2-639">Cohabiting</span></span>             | <span data-ttu-id="5efc2-640">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="5efc2-640">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="5efc2-641">Dzimums</span><span class="sxs-lookup"><span data-stu-id="5efc2-641">Gender</span></span>

<span data-ttu-id="5efc2-642">Dzimuma apzīmējumi tiek kartēti uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkoti uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="5efc2-642">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="5efc2-643">Tālāk esošajā tabulā ir parādīts, kā dzimuma apzīmējumi tiek kartēti uz pakalpojumu Dayforce.</span><span class="sxs-lookup"><span data-stu-id="5efc2-643">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="5efc2-644">Personāla vadība</span><span class="sxs-lookup"><span data-stu-id="5efc2-644">Human Resources</span></span>       | <span data-ttu-id="5efc2-645">Dayforce</span><span class="sxs-lookup"><span data-stu-id="5efc2-645">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="5efc2-646">Vīrietis</span><span class="sxs-lookup"><span data-stu-id="5efc2-646">Male</span></span>         | <span data-ttu-id="5efc2-647">Vīrietis</span><span class="sxs-lookup"><span data-stu-id="5efc2-647">Male</span></span>                      |
| <span data-ttu-id="5efc2-648">Sieviete</span><span class="sxs-lookup"><span data-stu-id="5efc2-648">Female</span></span>       | <span data-ttu-id="5efc2-649">Sieviete</span><span class="sxs-lookup"><span data-stu-id="5efc2-649">Female</span></span>                    |
| <span data-ttu-id="5efc2-650">Nav specifisks</span><span class="sxs-lookup"><span data-stu-id="5efc2-650">Non-specific</span></span> | <span data-ttu-id="5efc2-651">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="5efc2-651">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="5efc2-652">Maksājumu metode</span><span class="sxs-lookup"><span data-stu-id="5efc2-652">Payment method</span></span>

<span data-ttu-id="5efc2-653">Maksāšanas metodes darbiniekam un uzņēmumam ļauj aprakstīt, kā darbinieki saņems samaksu.</span><span class="sxs-lookup"><span data-stu-id="5efc2-653">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="5efc2-654">Maksāšanas metodes tiek kartētas uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkotas uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="5efc2-654">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="5efc2-655">Tālāk esošajā tabulā ir parādīts, kā maksāšanas metodes tiek kartētas uz pakalpojumu Dayforce.</span><span class="sxs-lookup"><span data-stu-id="5efc2-655">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="5efc2-656">Personāla vadība</span><span class="sxs-lookup"><span data-stu-id="5efc2-656">Human Resources</span></span>             | <span data-ttu-id="5efc2-657">Dayforce</span><span class="sxs-lookup"><span data-stu-id="5efc2-657">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="5efc2-658">Kase</span><span class="sxs-lookup"><span data-stu-id="5efc2-658">Cash</span></span>               | <span data-ttu-id="5efc2-659">Kase</span><span class="sxs-lookup"><span data-stu-id="5efc2-659">Cash</span></span>                      |
| <span data-ttu-id="5efc2-660">Elektronisks maksājums</span><span class="sxs-lookup"><span data-stu-id="5efc2-660">Electronic Payment</span></span> | <span data-ttu-id="5efc2-661">Pārsūtījums</span><span class="sxs-lookup"><span data-stu-id="5efc2-661">Transfer</span></span>                  |
| <span data-ttu-id="5efc2-662">Pārbaudīt</span><span class="sxs-lookup"><span data-stu-id="5efc2-662">Check</span></span>              | <span data-ttu-id="5efc2-663">Čeks</span><span class="sxs-lookup"><span data-stu-id="5efc2-663">Cheque</span></span>                    |
| <span data-ttu-id="5efc2-664">Bankas vekselis</span><span class="sxs-lookup"><span data-stu-id="5efc2-664">Bank Draft</span></span>         | <span data-ttu-id="5efc2-665">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="5efc2-665">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="5efc2-666">Citi</span><span class="sxs-lookup"><span data-stu-id="5efc2-666">Other</span></span>              | <span data-ttu-id="5efc2-667">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="5efc2-667">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="5efc2-668">Bankas konta tips</span><span class="sxs-lookup"><span data-stu-id="5efc2-668">Bank account type</span></span>

<span data-ttu-id="5efc2-669">Bankas kontu tipus izmanto darbiniekiem sūtāmajiem elektroniskajiem maksājumiem.</span><span class="sxs-lookup"><span data-stu-id="5efc2-669">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="5efc2-670">Bankas kontu tipi tiek kartēti uz pakalpojumu Dayforce kā pārsūtīšanas konta informācija.</span><span class="sxs-lookup"><span data-stu-id="5efc2-670">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="5efc2-671">Bankas kontu tipi integrācijas laikā tiek atbilstoši tulkoti uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="5efc2-671">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="5efc2-672">Personāla vadība</span><span class="sxs-lookup"><span data-stu-id="5efc2-672">Human Resources</span></span>            | <span data-ttu-id="5efc2-673">Dayforce</span><span class="sxs-lookup"><span data-stu-id="5efc2-673">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="5efc2-674">Kontroles konts</span><span class="sxs-lookup"><span data-stu-id="5efc2-674">Checking Account</span></span>  | <span data-ttu-id="5efc2-675">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="5efc2-675">CheckingAccount</span></span>           |
| <span data-ttu-id="5efc2-676">Algu konts</span><span class="sxs-lookup"><span data-stu-id="5efc2-676">Payroll Account</span></span>   | <span data-ttu-id="5efc2-677">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="5efc2-677">PayrollAccount</span></span>            |
| <span data-ttu-id="5efc2-678">Uzkrājumu konts</span><span class="sxs-lookup"><span data-stu-id="5efc2-678">Savings Account</span></span>   | <span data-ttu-id="5efc2-679">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="5efc2-679">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="5efc2-680">BankGirot konts</span><span class="sxs-lookup"><span data-stu-id="5efc2-680">BankGirot account</span></span> | <span data-ttu-id="5efc2-681">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="5efc2-681">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="5efc2-682">PlusGirot konts</span><span class="sxs-lookup"><span data-stu-id="5efc2-682">PlusGirot account</span></span> | <span data-ttu-id="5efc2-683">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="5efc2-683">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="5efc2-684">Ienākumu veida kodi</span><span class="sxs-lookup"><span data-stu-id="5efc2-684">Earning codes</span></span>

<span data-ttu-id="5efc2-685">Ienākumu veidu kodi unikāli identificē katra veida ienākumus, ko saņem nodarbinātie.</span><span class="sxs-lookup"><span data-stu-id="5efc2-685">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="5efc2-686">Kodiem ir vairāki ar ienākumiem saistīti parametri, piemēram, uzskaites nosacījumi, nodokļu likumi, pārskatu veidošanas prasības un bruto summas palielināšanas iespēja.</span><span class="sxs-lookup"><span data-stu-id="5efc2-686">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="5efc2-687">Ja tiek izmantota neatbalstīta biežuma vērtība, aprēķinā pēc noklusējuma tiek lietota biežuma vērtība **Katra apmaksa**.</span><span class="sxs-lookup"><span data-stu-id="5efc2-687">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="5efc2-688">Atbalstītās biežuma vērtības</span><span class="sxs-lookup"><span data-stu-id="5efc2-688">Supported frequencies</span></span>

- <span data-ttu-id="5efc2-689">Visus</span><span class="sxs-lookup"><span data-stu-id="5efc2-689">All</span></span>
- <span data-ttu-id="5efc2-690">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="5efc2-690">EVERYPAY</span></span>
- <span data-ttu-id="5efc2-691">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="5efc2-691">EACHPAYPERIOD</span></span>
- <span data-ttu-id="5efc2-692">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="5efc2-692">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="5efc2-693">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="5efc2-693">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="5efc2-694">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="5efc2-694">1OFMTH</span></span>
- <span data-ttu-id="5efc2-695">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="5efc2-695">LASTOFMTH</span></span>
- <span data-ttu-id="5efc2-696">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="5efc2-696">2OFMTH</span></span>
- <span data-ttu-id="5efc2-697">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="5efc2-697">3OFMTH</span></span>
- <span data-ttu-id="5efc2-698">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="5efc2-698">4OFMTH</span></span>
- <span data-ttu-id="5efc2-699">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="5efc2-699">5OFMTH</span></span>
- <span data-ttu-id="5efc2-700">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="5efc2-700">1N2OFMTH</span></span>
- <span data-ttu-id="5efc2-701">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="5efc2-701">3N4OFMTH</span></span>
- <span data-ttu-id="5efc2-702">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="5efc2-702">1N3OFMTH</span></span>
- <span data-ttu-id="5efc2-703">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="5efc2-703">1N4OFMTH</span></span>
- <span data-ttu-id="5efc2-704">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="5efc2-704">2N3OFMTH</span></span>
- <span data-ttu-id="5efc2-705">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="5efc2-705">2N4OFMTH</span></span>
- <span data-ttu-id="5efc2-706">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="5efc2-706">1N2N3OFMTH</span></span>
- <span data-ttu-id="5efc2-707">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="5efc2-707">1N2N4OFMTH</span></span>
- <span data-ttu-id="5efc2-708">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="5efc2-708">1N3N4OFMTH</span></span>
- <span data-ttu-id="5efc2-709">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="5efc2-709">2N3N4OFMTH</span></span>
- <span data-ttu-id="5efc2-710">1N2N3N4OFMTH–1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="5efc2-710">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="5efc2-711">2N3N4N5OFMth–2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="5efc2-711">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="5efc2-712">1OFQTR–1OFQTR</span><span class="sxs-lookup"><span data-stu-id="5efc2-712">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="5efc2-713">LASTOFQTR–LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="5efc2-713">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="5efc2-714">LASTMTHOFQTR–LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="5efc2-714">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="5efc2-715">1OFYEAR–1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="5efc2-715">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="5efc2-716">LASTOFYEAR–LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="5efc2-716">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="5efc2-717">NOVNDECOFYEAR–NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="5efc2-717">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="5efc2-718">Adreses</span><span class="sxs-lookup"><span data-stu-id="5efc2-718">Addresses</span></span>

<span data-ttu-id="5efc2-719">Noteiktas valsts vai reģiona, administratīvā apgabala un apgabala (pašvaldības) kodu identifikācijai ir nepieciešami konkrēti formāti, ko var atpazīt pakalpojums Dayforce un valsts/reģiona pakalpojumu sniedzēji.</span><span class="sxs-lookup"><span data-stu-id="5efc2-719">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="5efc2-720">Lai gan pilsētu formāts var būt dažāds, katrai pilsētai ir jābūt saistītai ar administratīvo apgabalu.</span><span class="sxs-lookup"><span data-stu-id="5efc2-720">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="5efc2-721">Personāla vadība</span><span class="sxs-lookup"><span data-stu-id="5efc2-721">Human Resources</span></span>              | <span data-ttu-id="5efc2-722">Dayforce</span><span class="sxs-lookup"><span data-stu-id="5efc2-722">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="5efc2-723">Valsts/reģions</span><span class="sxs-lookup"><span data-stu-id="5efc2-723">Country/Region</span></span>      | <span data-ttu-id="5efc2-724">Valsts kods</span><span class="sxs-lookup"><span data-stu-id="5efc2-724">Country Code</span></span>          |
| <span data-ttu-id="5efc2-725">Pasta indekss</span><span class="sxs-lookup"><span data-stu-id="5efc2-725">Zip/Postal Code</span></span>     | <span data-ttu-id="5efc2-726">Pasta indekss</span><span class="sxs-lookup"><span data-stu-id="5efc2-726">Postal Code</span></span>           |
| <span data-ttu-id="5efc2-727">Administratīvais apgabals</span><span class="sxs-lookup"><span data-stu-id="5efc2-727">State</span></span>               | <span data-ttu-id="5efc2-728">Administratīvā apgabala kods</span><span class="sxs-lookup"><span data-stu-id="5efc2-728">State Code</span></span>            |
| <span data-ttu-id="5efc2-729">Pilsēta</span><span class="sxs-lookup"><span data-stu-id="5efc2-729">City</span></span>                | <span data-ttu-id="5efc2-730">Pilsēta</span><span class="sxs-lookup"><span data-stu-id="5efc2-730">City</span></span>                  |
| <span data-ttu-id="5efc2-731">Apgabals</span><span class="sxs-lookup"><span data-stu-id="5efc2-731">County</span></span>              | <span data-ttu-id="5efc2-732">Apgabals (pašvaldība)</span><span class="sxs-lookup"><span data-stu-id="5efc2-732">County (Municipality)</span></span> |
| <span data-ttu-id="5efc2-733">Iela</span><span class="sxs-lookup"><span data-stu-id="5efc2-733">Street</span></span>              | <span data-ttu-id="5efc2-734">Adreses 1. rinda</span><span class="sxs-lookup"><span data-stu-id="5efc2-734">Address Line 1</span></span>        |
| <span data-ttu-id="5efc2-735">Ielas numurs</span><span class="sxs-lookup"><span data-stu-id="5efc2-735">Street Number</span></span>       | <span data-ttu-id="5efc2-736">Adreses 2. rinda</span><span class="sxs-lookup"><span data-stu-id="5efc2-736">Address Line 2</span></span>        |
| <span data-ttu-id="5efc2-737">Mājas numurs/nosaukums</span><span class="sxs-lookup"><span data-stu-id="5efc2-737">Building Complement</span></span> | <span data-ttu-id="5efc2-738">Adreses 5. rinda</span><span class="sxs-lookup"><span data-stu-id="5efc2-738">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="5efc2-739">Pases numurs</span><span class="sxs-lookup"><span data-stu-id="5efc2-739">Passport number</span></span>

<span data-ttu-id="5efc2-740">Darbinieki var sniegt pases informāciju.</span><span class="sxs-lookup"><span data-stu-id="5efc2-740">Employees can declare passport information.</span></span> <span data-ttu-id="5efc2-741">Šīs informācijas identifikācijas tips ir **Pase**, un tā tiek integrēta pakalpojumā Dayforce kā daļa no darbinieka Meksikai specifiskās informācijas.</span><span class="sxs-lookup"><span data-stu-id="5efc2-741">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="5efc2-742">Identifikācijas tips = Pase</span><span class="sxs-lookup"><span data-stu-id="5efc2-742">Identification Type = "Passport"</span></span>
- <span data-ttu-id="5efc2-743">Izdošanas datums</span><span class="sxs-lookup"><span data-stu-id="5efc2-743">Issued Date</span></span>
- <span data-ttu-id="5efc2-744">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="5efc2-744">Expiration Date</span></span>

<span data-ttu-id="5efc2-745">Darbinieki var sniegt vairākus identifikācijas numurus, kuru identifikācijas tips ir **Pase**.</span><span class="sxs-lookup"><span data-stu-id="5efc2-745">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="5efc2-746">Taču pakalpojumā Dayforce tiek integrēts tikai pašreizējais aktīvais pases ieraksts.</span><span class="sxs-lookup"><span data-stu-id="5efc2-746">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="5efc2-747">Ja visiem pases ierakstiem ir beidzies derīgiem, pakalpojumā Dayforce tiek integrēta pēdējā izdotā pase.</span><span class="sxs-lookup"><span data-stu-id="5efc2-747">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>

