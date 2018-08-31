---
title: "Algu aprēķina integrācijas konfigurēšana pakalpojumos Talent un Dayforce"
description: "Šajā tēmā ir izskaidrots, kā konfigurēt integrāciju pakalpojumos Microsoft Dynamics 365 for Talent un Ceridian Dayforce, lai varētu apstrādāt maksājuma izpildi."
author: jcart1106
manager: AnnBe
ms.date: 07/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 82f039b305503c604d64610f39838fa86a8eb08a
ms.openlocfilehash: fcddf82cffb9f0ba94b83eb21809b810585ebc9e
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2018

---

# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="b493d-103">Algu aprēķina integrācijas konfigurēšana pakalpojumos Talent un Dayforce</span><span class="sxs-lookup"><span data-stu-id="b493d-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b493d-104">Integrācija pakalpojumos Microsoft Dynamics 365 for Talent un Ceridian Dayforce izmanto vairākas konfigurācijas darbības, kas ir aprakstītas šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="b493d-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="b493d-105">Pirms maksājuma izpildes apstrādes vispirms ir jākonfigurē integrācija gan pakalpojumā Talent, gan pakalpojumā Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b493d-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="b493d-106">Ja maksājumu izpildei izmantojat tādu pakalpojumu kā Dayforce, jums ir jāiespējo integrācija pakalpojumā Talent.</span><span class="sxs-lookup"><span data-stu-id="b493d-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="b493d-107">Integrācijai ir nepieciešami noteikti Talent dati.</span><span class="sxs-lookup"><span data-stu-id="b493d-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="b493d-108">Tādēļ ir jāpārliecinās, vai uz Dayforce kartētie dati pakalpojumā Talent ir konfigurēti veidā, kas atbalsta integrāciju.</span><span class="sxs-lookup"><span data-stu-id="b493d-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="b493d-109">Integrācija izmanto tālāk norādītās vispārējās datu kategorijas.</span><span class="sxs-lookup"><span data-stu-id="b493d-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="b493d-110">Personāla vadības dati</span><span class="sxs-lookup"><span data-stu-id="b493d-110">Human resources data</span></span>
- <span data-ttu-id="b493d-111">Atlīdzības dati</span><span class="sxs-lookup"><span data-stu-id="b493d-111">Compensation data</span></span>
- <span data-ttu-id="b493d-112">Algu dati, piemēram, apmaksas cikli, apmaksas periodi un ienākumu veidu kodi</span><span class="sxs-lookup"><span data-stu-id="b493d-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="b493d-113">Nodarbināto dati</span><span class="sxs-lookup"><span data-stu-id="b493d-113">Worker data</span></span>

<span data-ttu-id="b493d-114">Šajā tēmā ir aprakstītas darbības, kas jāveic, lai iespējotu integrāciju.</span><span class="sxs-lookup"><span data-stu-id="b493d-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="b493d-115">Tajā ir arī izskaidrots, kādu veidu dati un konfigurācijas informācija ir nepieciešama integrācijai.</span><span class="sxs-lookup"><span data-stu-id="b493d-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="b493d-116">Integrācijas iespējošana</span><span class="sxs-lookup"><span data-stu-id="b493d-116">Enable the integration</span></span>

<span data-ttu-id="b493d-117">Lai izveidotu savienojumu ar Dayforce, pakalpojumā Talent ir jāieslēdz integrācija un jāievada konfigurācijas informācija.</span><span class="sxs-lookup"><span data-stu-id="b493d-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="b493d-118">Ja vēlaties, lai izveidotā Virsgrāmatas transakcija tiktu importēta programmā Microsoft Dynamics 365 for Finance and Operations, jums ir arī jāiestata Microsoft Azure krātuves konts un jāievada Azure krātuves savienojuma virkne programmā Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b493d-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="b493d-119">Lai pakalpojumā Talent ieslēgtu integrāciju, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="b493d-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="b493d-120">Lapā **Sistēmas administrēšana** atlasiet opciju **Integrācijas konfigurēšana**.</span><span class="sxs-lookup"><span data-stu-id="b493d-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="b493d-121">Ievadiet drošo failu pārsūtīšanas protokola (FTP) galapunktu un drošo FTP mapes ceļu.</span><span class="sxs-lookup"><span data-stu-id="b493d-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="b493d-122">Ievadiet tā lietotāja lietotājvārdu un paroli, kurš piekļūs drošajam FTP galapunktam un mapes ceļam.</span><span class="sxs-lookup"><span data-stu-id="b493d-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="b493d-123">Pārbaudiet savienojumu, kā nepieciešams, un opciju **Iespējot algu aprēķina integrāciju** iestatiet uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="b493d-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="b493d-124">Kad integrācija ir ieslēgta, tiek izveidota datu eksportēšanas pakotne un faili, kā arī iestatīts biežums.</span><span class="sxs-lookup"><span data-stu-id="b493d-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="b493d-125">Biežumu varat mainīt atbilstoši vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="b493d-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="b493d-126">Papildinformāciju par Azure krātuves kontiem un Azure krātuves savienojuma virknēm skatiet tālāk sniegtajās Azure tēmās.</span><span class="sxs-lookup"><span data-stu-id="b493d-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="b493d-127">Par Azure krātuves kontiem</span><span class="sxs-lookup"><span data-stu-id="b493d-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="b493d-128">Azure krātuves savienojuma virkņu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="b493d-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a><span data-ttu-id="b493d-129">Datu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="b493d-129">Configure your data</span></span> 

<span data-ttu-id="b493d-130">Lai apstrādātu algas, pakalpojumā Talent ir jākonfigurē personāla vadības dati.</span><span class="sxs-lookup"><span data-stu-id="b493d-130">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="b493d-131">Jums ir jāiestata organizācijas dati, piemēram, darbi un amati, kā arī informācija par atvieglojumiem un atlīdzību.</span><span class="sxs-lookup"><span data-stu-id="b493d-131">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="b493d-132">Šie dati nodrošina informāciju par nodarbinātību, samaksu un ieturējumiem, kas nepieciešama darbinieka algas ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="b493d-132">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="b493d-133">Personāla vadības dati</span><span class="sxs-lookup"><span data-stu-id="b493d-133">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="b493d-134">Atvieglojumi</span><span class="sxs-lookup"><span data-stu-id="b493d-134">Benefits</span></span> 

<span data-ttu-id="b493d-135">Personāla vadība nodrošina rīkus, ko var izmantot, lai iestatītu un uzturētu atvieglojumus, ieturējumus un nodarbināto atlīdzības plānus, ko organizācija piedāvā vai apstrādā saviem nodarbinātajiem.</span><span class="sxs-lookup"><span data-stu-id="b493d-135">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="b493d-136">Kad veidojat atvieglojumus, ņemiet vērā tālāk norādītos datus un konfigurācijas, kas tiek izmantoti pakalpojumā Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b493d-136">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="b493d-137">Atvieglojumu plāni</span><span class="sxs-lookup"><span data-stu-id="b493d-137">Benefit plans</span></span>

- <span data-ttu-id="b493d-138">Plāns (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-138">Plan (required)</span></span>
- <span data-ttu-id="b493d-139">Tips (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-139">Type (required)</span></span>
- <span data-ttu-id="b493d-140">Algas ietekme (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-140">Payroll impact (required)</span></span>
- <span data-ttu-id="b493d-141">Atgūt nokavētos maksājumus</span><span class="sxs-lookup"><span data-stu-id="b493d-141">Recover arrears</span></span>
- <span data-ttu-id="b493d-142">Ieturējuma metode</span><span class="sxs-lookup"><span data-stu-id="b493d-142">Deduction method</span></span>
- <span data-ttu-id="b493d-143">Ieturējuma prioritāte</span><span class="sxs-lookup"><span data-stu-id="b493d-143">Deduction priority</span></span>
- <span data-ttu-id="b493d-144">Ierobežojuma periods</span><span class="sxs-lookup"><span data-stu-id="b493d-144">Limit period</span></span>
- <span data-ttu-id="b493d-145">Ierobežojuma summa</span><span class="sxs-lookup"><span data-stu-id="b493d-145">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="b493d-146">Atvieglojumi</span><span class="sxs-lookup"><span data-stu-id="b493d-146">Benefits</span></span>

- <span data-ttu-id="b493d-147">Plāns (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-147">Plan (required)</span></span>
- <span data-ttu-id="b493d-148">Tips (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-148">Type (required)</span></span>
- <span data-ttu-id="b493d-149">Opcija (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-149">Option (required)</span></span>
- <span data-ttu-id="b493d-150">Atvieglojumu ID (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-150">Benefit ID (required)</span></span>
- <span data-ttu-id="b493d-151">Biežums</span><span class="sxs-lookup"><span data-stu-id="b493d-151">Frequency</span></span>
- <span data-ttu-id="b493d-152">Pamats</span><span class="sxs-lookup"><span data-stu-id="b493d-152">Basis</span></span>
- <span data-ttu-id="b493d-153">Summa vai likme</span><span class="sxs-lookup"><span data-stu-id="b493d-153">Amount or rate</span></span>
- <span data-ttu-id="b493d-154">Ienākumu veida kods</span><span class="sxs-lookup"><span data-stu-id="b493d-154">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="b493d-155">Atbalstītās biežuma vērtības</span><span class="sxs-lookup"><span data-stu-id="b493d-155">Supported frequencies</span></span> 

- <span data-ttu-id="b493d-156">Katru nedēļu</span><span class="sxs-lookup"><span data-stu-id="b493d-156">Weekly</span></span>
- <span data-ttu-id="b493d-157">Katru otro nedēļu</span><span class="sxs-lookup"><span data-stu-id="b493d-157">Bi-weekly</span></span>
- <span data-ttu-id="b493d-158">Pusmēneša</span><span class="sxs-lookup"><span data-stu-id="b493d-158">Semi-monthly</span></span>
- <span data-ttu-id="b493d-159">Mēnesis</span><span class="sxs-lookup"><span data-stu-id="b493d-159">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="b493d-160">Atbalstītās pamata vērtības</span><span class="sxs-lookup"><span data-stu-id="b493d-160">Supported bases</span></span> 

- <span data-ttu-id="b493d-161">Fiksēta summa</span><span class="sxs-lookup"><span data-stu-id="b493d-161">Fixed amount</span></span>
- <span data-ttu-id="b493d-162">Ienākumu procentuālais daudzums</span><span class="sxs-lookup"><span data-stu-id="b493d-162">Percent of earnings</span></span>
- <span data-ttu-id="b493d-163">Produktīvās stundas</span><span class="sxs-lookup"><span data-stu-id="b493d-163">Productive hours</span></span>

<span data-ttu-id="b493d-164">Dayforce izveido tālāk norādītos ieturējumus, pamatojoties uz atvieglojumu plānā definēto algas ietekmi.</span><span class="sxs-lookup"><span data-stu-id="b493d-164">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="b493d-165">Atlase pakalpojumā Talent</span><span class="sxs-lookup"><span data-stu-id="b493d-165">Selection in Talent</span></span>        | <span data-ttu-id="b493d-166">Rezultāts pakalpojumā Dayforce</span><span class="sxs-lookup"><span data-stu-id="b493d-166">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="b493d-167">Neviens</span><span class="sxs-lookup"><span data-stu-id="b493d-167">None</span></span>                       | <span data-ttu-id="b493d-168">Nav izveidots neviens ieturējums.</span><span class="sxs-lookup"><span data-stu-id="b493d-168">No deduction is created.</span></span>                      |
| <span data-ttu-id="b493d-169">Tikai ieturējums</span><span class="sxs-lookup"><span data-stu-id="b493d-169">Deduction only</span></span>             | <span data-ttu-id="b493d-170">Ir izveidots darbinieka ieturējums.</span><span class="sxs-lookup"><span data-stu-id="b493d-170">An employee deduction is created.</span></span>             |
| <span data-ttu-id="b493d-171">Tikai segums</span><span class="sxs-lookup"><span data-stu-id="b493d-171">Contribution only</span></span>          | <span data-ttu-id="b493d-172">Ir izveidots darba devēja ieturējums.</span><span class="sxs-lookup"><span data-stu-id="b493d-172">An employer deduction is created.</span></span>             |
| <span data-ttu-id="b493d-173">Ieturējums un segums</span><span class="sxs-lookup"><span data-stu-id="b493d-173">Deduction and contribution</span></span> | <span data-ttu-id="b493d-174">Ir izveidots darbinieka un darba devēja ieturējums.</span><span class="sxs-lookup"><span data-stu-id="b493d-174">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="b493d-175">Papildinformāciju par atvieglojumu programmas definēšanu un pārvaldību skatiet tālāk sniegtajās tēmās.</span><span class="sxs-lookup"><span data-stu-id="b493d-175">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="b493d-176">Darbinieku atvieglojumu programmas nodrošināšana</span><span class="sxs-lookup"><span data-stu-id="b493d-176">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="b493d-177">Jauna atvieglojuma izveide</span><span class="sxs-lookup"><span data-stu-id="b493d-177">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="b493d-178">Atvieglojumu piemērotības kārtulu un ierobežojumu definēšana</span><span class="sxs-lookup"><span data-stu-id="b493d-178">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="b493d-179">Atvieglojumu reģistrēšana un noņemšana nodarbinātajiem</span><span class="sxs-lookup"><span data-stu-id="b493d-179">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="b493d-180">Atlīdzība</span><span class="sxs-lookup"><span data-stu-id="b493d-180">Compensation</span></span> 

<span data-ttu-id="b493d-181">Atlīdzību pārvaldība tiek izmantota, lai kontrolētu pamatalgas un prēmiju izsniegšanu.</span><span class="sxs-lookup"><span data-stu-id="b493d-181">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="b493d-182">Darbinieka fiksētā pamatalga un nopelnu palielinājumi tiek kontrolēti, izmantojot fiksētas atlīdzības plānus.</span><span class="sxs-lookup"><span data-stu-id="b493d-182">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="b493d-183">Veicināšanas maksājumu izsniegšana, piemēram, prēmiju maksājumi, apbalvojumi par sasniegumiem, uzņēmuma akciju iegādes iespējas un dotācijas, kā arī vienreizējas piemaksas, tiek kontrolētas ar mainīgās atlīdzības plāniem.</span><span class="sxs-lookup"><span data-stu-id="b493d-183">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="b493d-184">Dayforce izmanto atlīdzības informāciju, lai aprēķinātu darbinieka stundas vai gada likmi.</span><span class="sxs-lookup"><span data-stu-id="b493d-184">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="b493d-185">Ir jānorāda fiksētās atlīdzības plāni un apmaksas likmes konvertēšanas gadījumi.</span><span class="sxs-lookup"><span data-stu-id="b493d-185">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="b493d-186">Darbiniekiem ir jābūt saistītiem ar fiksētās atlīdzības plānu.</span><span class="sxs-lookup"><span data-stu-id="b493d-186">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="b493d-187">Papildinformāciju par atlīdzības plāniem skatiet tālāk sniegtajās tēmās.</span><span class="sxs-lookup"><span data-stu-id="b493d-187">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="b493d-188">Fiksētās atlīdzības plānu izveidošana</span><span class="sxs-lookup"><span data-stu-id="b493d-188">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="b493d-189">Mainīgās atlīdzības plānu izveidošana</span><span class="sxs-lookup"><span data-stu-id="b493d-189">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="b493d-190">Algas/atlīdzības organizācijas un plānu izstrāde</span><span class="sxs-lookup"><span data-stu-id="b493d-190">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="b493d-191">Procesa kompensācija</span><span class="sxs-lookup"><span data-stu-id="b493d-191">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="b493d-192">Atlīdzības procesa definēšana un rezultātu aprēķināšana</span><span class="sxs-lookup"><span data-stu-id="b493d-192">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="b493d-193">Darbinieka reģistrēšana fiksētās atlīdzības plānā</span><span class="sxs-lookup"><span data-stu-id="b493d-193">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="b493d-194">Darbinieka reģistrēšana mainīgās atlīdzības plānā</span><span class="sxs-lookup"><span data-stu-id="b493d-194">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="b493d-195">Darbi</span><span class="sxs-lookup"><span data-stu-id="b493d-195">Jobs</span></span> 

<span data-ttu-id="b493d-196">Darbs ir uzdevumu un atbildības jomu kopums, kas ir jāizpilda personai, kura veic darbu.</span><span class="sxs-lookup"><span data-stu-id="b493d-196">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="b493d-197">Lai iegūtu papildu informāciju, skatiet šādas tēmas:</span><span class="sxs-lookup"><span data-stu-id="b493d-197">For more information, see the following topics:</span></span>

- [<span data-ttu-id="b493d-198">Darba komponentu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="b493d-198">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="b493d-199">Jaunu darbu definēšana</span><span class="sxs-lookup"><span data-stu-id="b493d-199">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="b493d-200">Amati</span><span class="sxs-lookup"><span data-stu-id="b493d-200">Positions</span></span>

<span data-ttu-id="b493d-201">Pozīcija ir atsevišķa darba instance.</span><span class="sxs-lookup"><span data-stu-id="b493d-201">A position is an individual instance of a job.</span></span> <span data-ttu-id="b493d-202">Piemēram, amats Pārdošanas daļas vadītājs (austrumu reģions) ir tikai viens no amatiem, kas ir saistīti ar darbu Pārdošanas daļas vadītājs.</span><span class="sxs-lookup"><span data-stu-id="b493d-202">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="b493d-203">Amats pastāv nodaļā.</span><span class="sxs-lookup"><span data-stu-id="b493d-203">A position exists in a department.</span></span> <span data-ttu-id="b493d-204">Ar katru amatu var būt saistīts tikai viens nodarbinātais.</span><span class="sxs-lookup"><span data-stu-id="b493d-204">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="b493d-205">Iestatot jaunus amatus, ņemiet vērā tālāk norādītos datus un konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="b493d-205">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="b493d-206">Amats (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-206">Position (required)</span></span>
- <span data-ttu-id="b493d-207">Apraksts (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-207">Description (required)</span></span>
- <span data-ttu-id="b493d-208">Darbs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-208">Job (required)</span></span>
- <span data-ttu-id="b493d-209">Nodaļa (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-209">Department (required)</span></span>
- <span data-ttu-id="b493d-210">Amata veids (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-210">Position type (required)</span></span>
- <span data-ttu-id="b493d-211">Pilnas slodzes ekvivalents</span><span class="sxs-lookup"><span data-stu-id="b493d-211">Full-time equivalent</span></span>
- <span data-ttu-id="b493d-212">Ikgadējās parastās stundas (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-212">Annual regular hours (required)</span></span>
- <span data-ttu-id="b493d-213">Apmaksātāja juridiskā persona (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-213">Paid by legal entity (required)</span></span>
- <span data-ttu-id="b493d-214">Apmaksas cikls (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-214">Pay cycle (required)</span></span>
- <span data-ttu-id="b493d-215">Noklusējuma finanšu dimensija — izmaksu centrs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-215">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="b493d-216">Nodarbinātā piešķire — nodarbinātais, piešķires sākums, piešķires beigas, iemesla kods</span><span class="sxs-lookup"><span data-stu-id="b493d-216">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="b493d-217">Ja vienā nodaļā ar to pašu darbu ir saistīti vairāki amati, tie pakalpojumā Dayforce tiek apvienoti vienā amatā.</span><span class="sxs-lookup"><span data-stu-id="b493d-217">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="b493d-218">Lai iegūtu papildu informāciju, skatiet šādas tēmas:</span><span class="sxs-lookup"><span data-stu-id="b493d-218">For more information, see the following topics:</span></span>

- [<span data-ttu-id="b493d-219">Organizēt darbaspēku, izmantojot nodaļas, darbus un amatus</span><span class="sxs-lookup"><span data-stu-id="b493d-219">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="b493d-220">Amatu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="b493d-220">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="b493d-221">Nodaļas</span><span class="sxs-lookup"><span data-stu-id="b493d-221">Departments</span></span>

<span data-ttu-id="b493d-222">Nodaļa ir pārvaldības struktūrvienība, kas pārstāv organizācijas kategoriju vai funkcionālo apgabalu.</span><span class="sxs-lookup"><span data-stu-id="b493d-222">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="b493d-223">Nodaļa ir atbildīga par noteiktu organizācijas jomu, piemēram, pārdošanu, uzskaiti vai personāla vadību.</span><span class="sxs-lookup"><span data-stu-id="b493d-223">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="b493d-224">Nodaļas var izmantot, lai ziņotu par funkcionālām jomām.</span><span class="sxs-lookup"><span data-stu-id="b493d-224">You can use departments to report on functional areas.</span></span> <span data-ttu-id="b493d-225">Nodaļām var būt peļņas un zaudējumu atbildība.</span><span class="sxs-lookup"><span data-stu-id="b493d-225">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="b493d-226">Lai iegūtu papildu informāciju, skatiet šādas tēmas:</span><span class="sxs-lookup"><span data-stu-id="b493d-226">For more information, see the following topics:</span></span>

- [<span data-ttu-id="b493d-227">Nodaļas izveide un tās saistīšana ar nodaļu hierarhiju</span><span class="sxs-lookup"><span data-stu-id="b493d-227">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="b493d-228">Jaunu nodaļu definēšana</span><span class="sxs-lookup"><span data-stu-id="b493d-228">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="b493d-229">Apmaksas cikli un apmaksas periodi</span><span class="sxs-lookup"><span data-stu-id="b493d-229">Pay cycles and pay periods</span></span>

<span data-ttu-id="b493d-230">Apmaksas cikls nosaka, cik bieži tiek veikts algu aprēķins, kā arī konkrētās dienas, kurās nodarbinātie saņem samaksu.</span><span class="sxs-lookup"><span data-stu-id="b493d-230">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="b493d-231">Apmaksas cikls var būt, piemēram, ikmēneša, un darbinieki samaksu var saņemt mēneša pēdējā dienā.</span><span class="sxs-lookup"><span data-stu-id="b493d-231">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="b493d-232">Vai arī apmaksas cikls var būt iknedēļas, un darbinieki samaksu var saņemt otrdienā pēc apmaksas perioda beigām.</span><span class="sxs-lookup"><span data-stu-id="b493d-232">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="b493d-233">Apmaksas cikli tiek piešķirti amatiem, lai kontrolētu to, kad nodarbinātie šajos amatos saņems samaksu.</span><span class="sxs-lookup"><span data-stu-id="b493d-233">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="b493d-234">Pēc apmaksas ciklu izveides katram ciklam varat ģenerēt apmaksas periodus.</span><span class="sxs-lookup"><span data-stu-id="b493d-234">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="b493d-235">Katrā apmaksas periodā ir ietverts noklusējuma maksājuma datums, kura pamatā ir jūsu sniegtā informācija.</span><span class="sxs-lookup"><span data-stu-id="b493d-235">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="b493d-236">Taču varat modificēt apmaksas perioda noklusējuma maksājuma datumu izņēmumu iestatīšanai, piemēram, kad maksājuma datums ir brīvdienā.</span><span class="sxs-lookup"><span data-stu-id="b493d-236">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="b493d-237">Dayforce izmanto tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="b493d-237">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="b493d-238">Apmaksas cikls (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-238">Pay cycle (required)</span></span>
- <span data-ttu-id="b493d-239">Apmaksas cikla biežums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-239">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="b493d-240">Perioda sākuma datums (ir jānorāda pirmais apmaksas periods)</span><span class="sxs-lookup"><span data-stu-id="b493d-240">Period start date (first pay period required)</span></span>
- <span data-ttu-id="b493d-241">Noklusējuma maksājuma datums (ir jānorāda pirmais apmaksas periods)</span><span class="sxs-lookup"><span data-stu-id="b493d-241">Default payment date (first pay period required)</span></span>

<span data-ttu-id="b493d-242">Šī informācija pakalpojumā Dayforce ir integrēta kā apmaksas grupas, un katram apmaksas ciklam to atdala valsts vai reģions.</span><span class="sxs-lookup"><span data-stu-id="b493d-242">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="b493d-243">Pirms integrācijas ir jābūt ģenerētam vismaz vienam apmaksas periodam.</span><span class="sxs-lookup"><span data-stu-id="b493d-243">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="b493d-244">Dayforce ģenerē apmaksas grupu kalendārus un maksājumu datumus atbilstoši pakalpojumā Talent iestatītajam pirmā apmaksas perioda sākuma datumam un noklusējuma maksājuma datumam.</span><span class="sxs-lookup"><span data-stu-id="b493d-244">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="b493d-245">Ienākumu veida kodi</span><span class="sxs-lookup"><span data-stu-id="b493d-245">Earning codes</span></span>

<span data-ttu-id="b493d-246">Ienākumu veidu kodi unikāli identificē katra veida ienākumus, ko saņem nodarbinātie.</span><span class="sxs-lookup"><span data-stu-id="b493d-246">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="b493d-247">Kodiem ir dažādi ar ienākumiem saistīti parametri, piemēram, uzskaites nosacījumi, nodokļu likumi, pārskatu veidošanas prasības un bruto summas palielināšanas iespēja.</span><span class="sxs-lookup"><span data-stu-id="b493d-247">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="b493d-248">Dayforce izmanto tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="b493d-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="b493d-249">Ienākumu veida kods (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-249">Earning Code (required)</span></span>
- <span data-ttu-id="b493d-250">apraksts</span><span class="sxs-lookup"><span data-stu-id="b493d-250">Description</span></span>
- <span data-ttu-id="b493d-251">Mērvienība</span><span class="sxs-lookup"><span data-stu-id="b493d-251">Unit of measure</span></span>
- <span data-ttu-id="b493d-252">Produktīvs</span><span class="sxs-lookup"><span data-stu-id="b493d-252">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="b493d-253">Nodarbināto dati</span><span class="sxs-lookup"><span data-stu-id="b493d-253">Worker data</span></span>

<span data-ttu-id="b493d-254">Dažādo veidu nodarbināto ieraksti ir svarīga informācija personāla vadības un algu sistēmās.</span><span class="sxs-lookup"><span data-stu-id="b493d-254">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="b493d-255">Ievadīto informāciju var izmantot, lai sekotu nodarbinātajiem un personiskajai informācijai.</span><span class="sxs-lookup"><span data-stu-id="b493d-255">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="b493d-256">Par darbiniekiem var saglabāt tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="b493d-256">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="b493d-257">**Pamata** — saglabājiet pamata informāciju par darbinieku, piemēram, kontaktinformāciju, demogrāfisko informāciju, identifikācijas informāciju, ģimenes informāciju, karadienesta statusu, ekspatriantu informāciju, kā arī personiskās un ārkārtas kontaktpersonas.</span><span class="sxs-lookup"><span data-stu-id="b493d-257">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="b493d-258">**Nodarbinātība** — saglabājiet informāciju par darbinieka nodarbinātību, piemēram, informāciju par piederību uzņēmumam vai organizācijai, amata piešķiri, sākuma un beigu datumiem, piemērotību darbam, nodarbinātības noteikumiem, pensiju, atvaļinājumu un pārcelšanu.</span><span class="sxs-lookup"><span data-stu-id="b493d-258">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="b493d-259">**Atvaļinājumi un kavējumi** — saglabājiet informāciju par nodarbinātā kavējumiem, piemēram, informāciju par darba kalendāriem, kavējumu darbībām un kavējumu iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="b493d-259">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="b493d-260">**Atlīdzība un alga** — saglabājiet informāciju par nodarbinātā atlīdzības plāniem un algas informāciju, piemēram, plāna reģistrāciju, piemaksām, sniegumu, komisiju, nodokļu informāciju, pensionēšanos un ieturējumiem no algas.</span><span class="sxs-lookup"><span data-stu-id="b493d-260">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="b493d-261">Ievadot informāciju par nodarbināto, ņemiet vērā tālāk norādītos datus un konfigurācijas, kas tiek izmantoti pakalpojumā Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b493d-261">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="b493d-262">Vispārīgā informācija</span><span class="sxs-lookup"><span data-stu-id="b493d-262">General information</span></span>

- <span data-ttu-id="b493d-263">Personāla numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-263">Personnel number (required)</span></span>
- <span data-ttu-id="b493d-264">Vārds (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-264">First name (required)</span></span>
- <span data-ttu-id="b493d-265">Uzvārds (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-265">Last name (required)</span></span>
- <span data-ttu-id="b493d-266">Otrais vārds</span><span class="sxs-lookup"><span data-stu-id="b493d-266">Middle name</span></span>
- <span data-ttu-id="b493d-267">Darba stāža datums</span><span class="sxs-lookup"><span data-stu-id="b493d-267">Seniority date</span></span>
- <span data-ttu-id="b493d-268">Zināms kā</span><span class="sxs-lookup"><span data-stu-id="b493d-268">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="b493d-269">Personiskā informācija</span><span class="sxs-lookup"><span data-stu-id="b493d-269">Personal information</span></span>

- <span data-ttu-id="b493d-270">Ģimenes stāvoklis (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-270">Marital status (required)</span></span>
- <span data-ttu-id="b493d-271">Dzimšanas datums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-271">Birth date (required)</span></span>
- <span data-ttu-id="b493d-272">Dzimums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-272">Gender (required)</span></span>
- <span data-ttu-id="b493d-273">Persona ar īpašām vajadzībām</span><span class="sxs-lookup"><span data-stu-id="b493d-273">Person with disabilities</span></span>
- <span data-ttu-id="b493d-274">Nacionalitātes valsts/reģions (tikai Meksikai)</span><span class="sxs-lookup"><span data-stu-id="b493d-274">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="b493d-275">Adreses informācija</span><span class="sxs-lookup"><span data-stu-id="b493d-275">Address information</span></span>

- <span data-ttu-id="b493d-276">Primārā (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-276">Primary (required)</span></span>
- <span data-ttu-id="b493d-277">Valsts/reģions (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-277">Country/region (required)</span></span>
- <span data-ttu-id="b493d-278">Pasta indekss (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-278">Postal code (required)</span></span>
- <span data-ttu-id="b493d-279">Ielas numurs (obligāti) (tikai Meksikai)</span><span class="sxs-lookup"><span data-stu-id="b493d-279">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="b493d-280">Mājas numurs/nosaukums (tikai Meksikai)</span><span class="sxs-lookup"><span data-stu-id="b493d-280">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="b493d-281">Pilsēta (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-281">City (required)</span></span>
- <span data-ttu-id="b493d-282">Administratīvais apgabals (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-282">State (required)</span></span>
- <span data-ttu-id="b493d-283">Apgabals (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-283">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="b493d-284">Kontaktinformācija</span><span class="sxs-lookup"><span data-stu-id="b493d-284">Contact information</span></span> 

- <span data-ttu-id="b493d-285">Primārā (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-285">Primary (required)</span></span>
- <span data-ttu-id="b493d-286">Kontaktpersonas tālrunis (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-286">Contact number (required)</span></span>
- <span data-ttu-id="b493d-287">Paplašinājums</span><span class="sxs-lookup"><span data-stu-id="b493d-287">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="b493d-288">Algas informācija un ienākumu veidu kodi</span><span class="sxs-lookup"><span data-stu-id="b493d-288">Payroll information and earning codes</span></span>

<span data-ttu-id="b493d-289">Darbiniekiem var būt piešķirti konkrēti ienākumu veidi konkrētajā maksājumu biežumā, kā arī var būt norādīta vēlamā maksāšanas metode.</span><span class="sxs-lookup"><span data-stu-id="b493d-289">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="b493d-290">Lai palīdzētu nodrošināt, ka šīs preferences un iestatījumi tiek izmantoti, pakalpojumā Dayforce ir tālāk norādītie lauki.</span><span class="sxs-lookup"><span data-stu-id="b493d-290">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="b493d-291">Ienākumu veida kodi</span><span class="sxs-lookup"><span data-stu-id="b493d-291">Earning codes</span></span>

- <span data-ttu-id="b493d-292">Amats (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-292">Position (required)</span></span>
- <span data-ttu-id="b493d-293">Ienākumu veida kods (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-293">Earning Code (required)</span></span>
- <span data-ttu-id="b493d-294">Biežums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-294">Frequency (required)</span></span>
- <span data-ttu-id="b493d-295">Summa (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-295">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="b493d-296">Algas informācija</span><span class="sxs-lookup"><span data-stu-id="b493d-296">Payroll information</span></span>

- <span data-ttu-id="b493d-297">Maksāšanas metode</span><span class="sxs-lookup"><span data-stu-id="b493d-297">Payment Method</span></span>
- <span data-ttu-id="b493d-298">Ekonomiskais reģions (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-298">Economic Region (required)</span></span>
- <span data-ttu-id="b493d-299">Darbinieka atvieglojumu ID</span><span class="sxs-lookup"><span data-stu-id="b493d-299">Employee Benefits ID</span></span>
- <span data-ttu-id="b493d-300">Nacionālais ID numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-300">National ID Number (required)</span></span>
- <span data-ttu-id="b493d-301">Karadienesta numurs</span><span class="sxs-lookup"><span data-stu-id="b493d-301">Military Service Number</span></span>
- <span data-ttu-id="b493d-302">Maiņas ID (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-302">Shift ID (required)</span></span>
- <span data-ttu-id="b493d-303">Nodokļu numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-303">Tax Number (required)</span></span>
- <span data-ttu-id="b493d-304">Arodbiedrības ID (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-304">Union ID (required)</span></span>
- <span data-ttu-id="b493d-305">Darba dienas ID (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-305">Work Day ID (required)</span></span>
- <span data-ttu-id="b493d-306">Darba atļaujas numurs</span><span class="sxs-lookup"><span data-stu-id="b493d-306">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="b493d-307">Meksika atbalsta šādas maksāšanas metodes: **Skaidra nauda**, **Čeks** (uzņēmuma fiziskais čeks) un **Elektroniskais maksājums**.</span><span class="sxs-lookup"><span data-stu-id="b493d-307">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="b493d-308">Ja nav norādīta neviena maksāšanas metode, pēc noklusējuma tiek izmantota opcija **Čeks**.</span><span class="sxs-lookup"><span data-stu-id="b493d-308">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="b493d-309">Nodarbinātības papildinformācija</span><span class="sxs-lookup"><span data-stu-id="b493d-309">Employment details</span></span>

<span data-ttu-id="b493d-310">Nodarbinātības datu vēsture pakalpojumā Dayforce tiek izmantota kā galvenā informācija, no kuras tiek iegūts darbinieka darbā pieņemšanas, darba attiecību izbeigšanas un atkārtotas pieņemšanas darbā statuss.</span><span class="sxs-lookup"><span data-stu-id="b493d-310">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="b493d-311">Dayforce vienlaikus atbalsta tikai vienu aktīvu nodarbinātības ierakstu.</span><span class="sxs-lookup"><span data-stu-id="b493d-311">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="b493d-312">Nodarbinātības sākuma datums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-312">Employment start date (required)</span></span>
- <span data-ttu-id="b493d-313">Nodarbinātības beigu datums</span><span class="sxs-lookup"><span data-stu-id="b493d-313">Employment end date</span></span>
- <span data-ttu-id="b493d-314">Pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="b493d-314">Start date</span></span>
- <span data-ttu-id="b493d-315">Koriģētais pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="b493d-315">Adjusted start date</span></span>
- <span data-ttu-id="b493d-316">Darba attiecību pārtraukšanas datums (jānorāda, kad tiek pārtrauktas darba attiecības)</span><span class="sxs-lookup"><span data-stu-id="b493d-316">Termination date (required upon termination)</span></span>
- <span data-ttu-id="b493d-317">Darba attiecību pārtraukšanas iemesls (jānorāda, kad tiek pārtrauktas darba attiecības)</span><span class="sxs-lookup"><span data-stu-id="b493d-317">Termination reason (required upon termination)</span></span>

<span data-ttu-id="b493d-318">Darbinieka galvenie datumi tiek iegūti, izmantojot tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="b493d-318">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="b493d-319">Talent</span><span class="sxs-lookup"><span data-stu-id="b493d-319">Talent</span></span>                | <span data-ttu-id="b493d-320">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b493d-320">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b493d-321">Pēdējais nomas datums</span><span class="sxs-lookup"><span data-stu-id="b493d-321">Most recent hire date</span></span> | <span data-ttu-id="b493d-322">Pašreizējā nepārtrauktās nodarbinātības vēstures ieraksta nodarbinātības sākums</span><span class="sxs-lookup"><span data-stu-id="b493d-322">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="b493d-323">Izbeigšanas datums</span><span class="sxs-lookup"><span data-stu-id="b493d-323">Termination date</span></span>      | <span data-ttu-id="b493d-324">Pašreizējā nepārtrauktās nodarbinātības vēstures ieraksta darba attiecību pārtraukšanas datums</span><span class="sxs-lookup"><span data-stu-id="b493d-324">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="b493d-325">Pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="b493d-325">Start date</span></span>            | <span data-ttu-id="b493d-326">Pašreizējā neaktīvā nodarbinātības vēstures ieraksta koriģētais sākuma datums, sākuma datums vai nodarbinātības sākums</span><span class="sxs-lookup"><span data-stu-id="b493d-326">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="b493d-327">Sākotnējais darbā pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="b493d-327">Original hire date</span></span>    | <span data-ttu-id="b493d-328">Agrākā nodarbinātības vēstures ieraksta nodarbinātības sākums</span><span class="sxs-lookup"><span data-stu-id="b493d-328">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="b493d-329">Atlīdzība</span><span class="sxs-lookup"><span data-stu-id="b493d-329">Compensation</span></span>

<span data-ttu-id="b493d-330">Fiksētās atlīdzības plānam ir jābūt saistītam ar katra darbinieka primāro amatu visā nodarbinātības periodā.</span><span class="sxs-lookup"><span data-stu-id="b493d-330">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="b493d-331">Šis periods sākas ar datumu, kurā darbinieks tika pieņemts darbā (vai nodarbinātības sākuma datumu), un turpinās līdz darba attiecību pārtraukšanai.</span><span class="sxs-lookup"><span data-stu-id="b493d-331">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="b493d-332">Spēkā stāšanās datums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-332">Effective Date (required)</span></span>
- <span data-ttu-id="b493d-333">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="b493d-333">Expiration date</span></span>
- <span data-ttu-id="b493d-334">Apmaksas likme (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-334">Pay Rate (required)</span></span>
- <span data-ttu-id="b493d-335">Apmaksas likmes konvertēšanas gadījumi (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-335">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="b493d-336">Gada ekvivalents (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-336">Annual equivalent (required)</span></span>
- <span data-ttu-id="b493d-337">Stundas ekvivalents (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-337">Hourly equivalent (required)</span></span>

<span data-ttu-id="b493d-338">Ja darbiniekam ar stundas likmi ir vairāki amati, pakalpojumā Dayforce kā darbinieka līmeņa pamatlikme/alga tiek importēta primārā amata fiksētā atlīdzība.</span><span class="sxs-lookup"><span data-stu-id="b493d-338">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="b493d-339">To amatu, kas nav primārie, stundas likme tiek saglabāta pakalpojumā Dayforce attiecīgajā amatā.</span><span class="sxs-lookup"><span data-stu-id="b493d-339">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="b493d-340">Ja darbiniekam, kurš saņem algu, ir vairāki amati, kā darbinieka līmeņa pamatlikme/alga tiek iegūta un izmantota visu aktīvo amatu kopējā stundas likme un gada alga.</span><span class="sxs-lookup"><span data-stu-id="b493d-340">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="b493d-341">Identifikācijas numuri</span><span class="sxs-lookup"><span data-stu-id="b493d-341">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="b493d-342">Sociālās apdrošināšanas numurs</span><span class="sxs-lookup"><span data-stu-id="b493d-342">Social Security identifier</span></span> 

<span data-ttu-id="b493d-343">Katram darbiniekam ir jābūt vienam primārajam numuram.</span><span class="sxs-lookup"><span data-stu-id="b493d-343">Every employee must have one primary identifier.</span></span> <span data-ttu-id="b493d-344">Šī numura identifikācijas tipam ir jābūt **SAN**.</span><span class="sxs-lookup"><span data-stu-id="b493d-344">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="b493d-345">Pakalpojumā Dayforce tas tiek automātiski iegūts kā darbinieka sociālās apdrošināšanas numurs, kas ir jānorāda, kad darbinieks tiek pieņemts darbā.</span><span class="sxs-lookup"><span data-stu-id="b493d-345">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="b493d-346">Primārais (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-346">Primary (required)</span></span>
- <span data-ttu-id="b493d-347">Identifikācijas tips = SAN</span><span class="sxs-lookup"><span data-stu-id="b493d-347">Identification Type = "SSN"</span></span>
- <span data-ttu-id="b493d-348">Izdošanas datums</span><span class="sxs-lookup"><span data-stu-id="b493d-348">Issued Date</span></span>
- <span data-ttu-id="b493d-349">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="b493d-349">Expiration Date</span></span>

<span data-ttu-id="b493d-350">Darbinieki var sniegt vairākus identifikācijas numurus, kuru identifikācijas tips ir **SAN**.</span><span class="sxs-lookup"><span data-stu-id="b493d-350">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="b493d-351">Taču pakalpojumā Dayforce tiek integrēts tikai ieraksts, kas ir atzīmēts kā **Primārais**, neatkarīgi no tā, vai šis numurs ir aktīvs vai tam ir beidzies derīgums.</span><span class="sxs-lookup"><span data-stu-id="b493d-351">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="b493d-352">Banku konti un izdevumi</span><span class="sxs-lookup"><span data-stu-id="b493d-352">Bank accounts and disbursements</span></span>

<span data-ttu-id="b493d-353">Jebkuram darbiniekam, kurš samaksu izvēlējies saņemt bankas konta pārskaitījuma veidā, ir jāievada derīga bankas konta informācija.</span><span class="sxs-lookup"><span data-stu-id="b493d-353">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="b493d-354">Talent</span><span class="sxs-lookup"><span data-stu-id="b493d-354">Talent</span></span>                         | <span data-ttu-id="b493d-355">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b493d-355">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b493d-356">Bankas konta numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-356">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="b493d-357">SWIFT kods (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-357">SWIFT code (required)</span></span>          | <span data-ttu-id="b493d-358">Lauku **Bankas ID** izmanto, apstrādājot algas Meksikā.</span><span class="sxs-lookup"><span data-stu-id="b493d-358">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="b493d-359">Filiāles numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-359">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="b493d-360">Bankas konta tips (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-360">Bank account type (required)</span></span>   | <span data-ttu-id="b493d-361">Lauku **Konta tips** izmanto, apstrādājot algas Meksikā.</span><span class="sxs-lookup"><span data-stu-id="b493d-361">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="b493d-362">Atbalstītās vērtības ir, piemēram, **Norēķini** un **Algas**.</span><span class="sxs-lookup"><span data-stu-id="b493d-362">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="b493d-363">Darbiniekiem, kuri samaksu izvēlas saņemt bankas konta pārskaitījumu veidā, ir jāsniedz saite uz juridiskās personas, kuras primārā adrese ir Meksikā, atlikumu kontu, kas ir saistīts ar derīgu Meksikas bankas kontu.</span><span class="sxs-lookup"><span data-stu-id="b493d-363">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="b493d-364">Visi pārējie konti, kas nav atlikumu konti, tiek ignorēti.</span><span class="sxs-lookup"><span data-stu-id="b493d-364">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="b493d-365">Adreses informācija</span><span class="sxs-lookup"><span data-stu-id="b493d-365">Address information</span></span>

<span data-ttu-id="b493d-366">Katram darbiniekam ir jābūt vienai primārajai vietai.</span><span class="sxs-lookup"><span data-stu-id="b493d-366">Every employee must have one primary location.</span></span> <span data-ttu-id="b493d-367">Pakalpojumā Dayforce šī vieta tiek izmantota, lai nodokļu piemērošanas nolūkos noteiktu darbinieka primāro dzīvesvietu.</span><span class="sxs-lookup"><span data-stu-id="b493d-367">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="b493d-368">Primārā (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-368">Primary (required)</span></span>
- <span data-ttu-id="b493d-369">Valsts/reģions (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-369">Country/region (required)</span></span>
- <span data-ttu-id="b493d-370">Pasta indekss (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-370">Zip/postal code (required)</span></span>
- <span data-ttu-id="b493d-371">Iela (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-371">Street (required)</span></span>
- <span data-ttu-id="b493d-372">Ielas numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-372">Street Number (required)</span></span>
- <span data-ttu-id="b493d-373">Mājas numurs/nosaukums</span><span class="sxs-lookup"><span data-stu-id="b493d-373">Building Complement</span></span>
- <span data-ttu-id="b493d-374">Pilsēta (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-374">City (required)</span></span>
- <span data-ttu-id="b493d-375">Administratīvais apgabals (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-375">State (required)</span></span>
- <span data-ttu-id="b493d-376">Apgabals (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-376">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="b493d-377">Datu konfigurēšana algu ģenerēšanai Amerikas Savienotajās Valstīs un Kanādā</span><span class="sxs-lookup"><span data-stu-id="b493d-377">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="b493d-378">Ja ģenerējat algas darbiniekiem Amerikas Savienotajās Valstīs un Kanādā, ir jākonfigurē tālāk norādītie elementi.</span><span class="sxs-lookup"><span data-stu-id="b493d-378">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="b493d-379">Amatiem ir jānorāda nodaļas.</span><span class="sxs-lookup"><span data-stu-id="b493d-379">Departments are required on positions.</span></span>
- <span data-ttu-id="b493d-380">Izmaksu centri ir jāiestata kā finanšu dimensijas, un tiem ir jābūt pirmajiem elementiem noklusējuma finanšu dimensijas virknē.</span><span class="sxs-lookup"><span data-stu-id="b493d-380">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="b493d-381">Darba tipi</span><span class="sxs-lookup"><span data-stu-id="b493d-381">Job types</span></span>

<span data-ttu-id="b493d-382">Darbu veidi tiek izmantoti, lai līdzīgus darbus grupētu kategorijās.</span><span class="sxs-lookup"><span data-stu-id="b493d-382">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="b493d-383">Darbu veidi ir nepieciešami, lai apstrādātu algas Amerikas Savienotajās Valstīs un Kanādā.</span><span class="sxs-lookup"><span data-stu-id="b493d-383">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="b493d-384">Daži darbu veidu piemēri ir pilna laika, nepilna laika, algots un stundu apmaksas darbs.</span><span class="sxs-lookup"><span data-stu-id="b493d-384">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="b493d-385">Darbu veidi tiek kartēti uz pakalpojumu Dayforce kā apmaksas tipi, lai norādītu, vai darbinieks saņem stundas samaksu vai algu.</span><span class="sxs-lookup"><span data-stu-id="b493d-385">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="b493d-386">Ir jānorāda tālāk norādītie darbu veidi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="b493d-386">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="b493d-387">Darba veids</span><span class="sxs-lookup"><span data-stu-id="b493d-387">Job type</span></span>   | <span data-ttu-id="b493d-388">apraksts</span><span class="sxs-lookup"><span data-stu-id="b493d-388">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="b493d-389">Ik stundu</span><span class="sxs-lookup"><span data-stu-id="b493d-389">Hourly</span></span>     | <span data-ttu-id="b493d-390">Ik stundu</span><span class="sxs-lookup"><span data-stu-id="b493d-390">Hourly</span></span>      |
| <span data-ttu-id="b493d-391">Algots</span><span class="sxs-lookup"><span data-stu-id="b493d-391">Salaried</span></span>   | <span data-ttu-id="b493d-392">Algots</span><span class="sxs-lookup"><span data-stu-id="b493d-392">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="b493d-393">Amatu veidi</span><span class="sxs-lookup"><span data-stu-id="b493d-393">Position types</span></span> 

<span data-ttu-id="b493d-394">Amatu veidus izmanto, lai norādītu, vai amats ir pilna laika, nepilna laika vai cita veida darbs.</span><span class="sxs-lookup"><span data-stu-id="b493d-394">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="b493d-395">Amatu veidi tiek kartēti uz pakalpojumu Dayforce kā apmaksas klases, lai norādītu, vai darbinieks ir pilna laika vai nepilna laika darbinieks.</span><span class="sxs-lookup"><span data-stu-id="b493d-395">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="b493d-396">Ir jānorāda tālāk norādītie amatu veidi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="b493d-396">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="b493d-397">Amata tips</span><span class="sxs-lookup"><span data-stu-id="b493d-397">Position type</span></span>   | <span data-ttu-id="b493d-398">apraksts</span><span class="sxs-lookup"><span data-stu-id="b493d-398">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="b493d-399">Pilna laika</span><span class="sxs-lookup"><span data-stu-id="b493d-399">Full-time</span></span>       | <span data-ttu-id="b493d-400">Pilna laika darbinieks</span><span class="sxs-lookup"><span data-stu-id="b493d-400">Full time employee</span></span> |
| <span data-ttu-id="b493d-401">Nepilna laika</span><span class="sxs-lookup"><span data-stu-id="b493d-401">Part-time</span></span>       | <span data-ttu-id="b493d-402">Nepilna laika darbinieks</span><span class="sxs-lookup"><span data-stu-id="b493d-402">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="b493d-403">Iemeslu kodi</span><span class="sxs-lookup"><span data-stu-id="b493d-403">Reason codes</span></span>

<span data-ttu-id="b493d-404">Iemeslu kodi sniedz informāciju par darbinieka statusu.</span><span class="sxs-lookup"><span data-stu-id="b493d-404">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="b493d-405">Iemeslu kodu tiek kartēti uz pakalpojumu Dayforce kā statusa iemesli, kas norāda darbinieka amata vai nodarbinātības statusa izmaiņu iemeslu.</span><span class="sxs-lookup"><span data-stu-id="b493d-405">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="b493d-406">Ir jānorāda tālāk norādītie iemeslu kodi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="b493d-406">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="b493d-407">Iemeslu kodi</span><span class="sxs-lookup"><span data-stu-id="b493d-407">Reason code</span></span>    | <span data-ttu-id="b493d-408">apraksts</span><span class="sxs-lookup"><span data-stu-id="b493d-408">Description</span></span>      | <span data-ttu-id="b493d-409">Piemērojamie scenāriji</span><span class="sxs-lookup"><span data-stu-id="b493d-409">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="b493d-410">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="b493d-410">RESIGNATION</span></span>    | <span data-ttu-id="b493d-411">Atlūgums</span><span class="sxs-lookup"><span data-stu-id="b493d-411">Resignation</span></span>      | <span data-ttu-id="b493d-412">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="b493d-412">Terminate worker</span></span>     |
| <span data-ttu-id="b493d-413">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="b493d-413">TERMINATION</span></span>    | <span data-ttu-id="b493d-414">Izbeigšana</span><span class="sxs-lookup"><span data-stu-id="b493d-414">Termination</span></span>      | <span data-ttu-id="b493d-415">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="b493d-415">Terminate worker</span></span>     |
| <span data-ttu-id="b493d-416">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="b493d-416">RETIREMENT</span></span>     | <span data-ttu-id="b493d-417">Aiziešana pensijā</span><span class="sxs-lookup"><span data-stu-id="b493d-417">Retirement</span></span>       | <span data-ttu-id="b493d-418">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="b493d-418">Terminate worker</span></span>     |
| <span data-ttu-id="b493d-419">CITI</span><span class="sxs-lookup"><span data-stu-id="b493d-419">OTHER</span></span>          | <span data-ttu-id="b493d-420">Citi iemesli</span><span class="sxs-lookup"><span data-stu-id="b493d-420">Other Reasons</span></span>    | <span data-ttu-id="b493d-421">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="b493d-421">Terminate worker</span></span>     |
| <span data-ttu-id="b493d-422">DEATH</span><span class="sxs-lookup"><span data-stu-id="b493d-422">DEATH</span></span>          | <span data-ttu-id="b493d-423">Nāve</span><span class="sxs-lookup"><span data-stu-id="b493d-423">Death</span></span>            | <span data-ttu-id="b493d-424">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="b493d-424">Terminate worker</span></span>     |
| <span data-ttu-id="b493d-425">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="b493d-425">LEAVEOFABSENCE</span></span> | <span data-ttu-id="b493d-426">Atvaļinājums</span><span class="sxs-lookup"><span data-stu-id="b493d-426">Leave of Absence</span></span> | <span data-ttu-id="b493d-427">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="b493d-427">Terminate worker</span></span>     |
| <span data-ttu-id="b493d-428">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="b493d-428">CONTRACTEND</span></span>    | <span data-ttu-id="b493d-429">Līguma beigas</span><span class="sxs-lookup"><span data-stu-id="b493d-429">End of Contract</span></span>  | <span data-ttu-id="b493d-430">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="b493d-430">Terminate worker</span></span>     |
| <span data-ttu-id="b493d-431">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="b493d-431">SALARYCHANGE</span></span>   | <span data-ttu-id="b493d-432">Algas izmaiņas</span><span class="sxs-lookup"><span data-stu-id="b493d-432">Change of Salary</span></span> | <span data-ttu-id="b493d-433">Atlīdzība</span><span class="sxs-lookup"><span data-stu-id="b493d-433">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="b493d-434">Ģimenes stāvoklis</span><span class="sxs-lookup"><span data-stu-id="b493d-434">Marital status</span></span>

<span data-ttu-id="b493d-435">Ģimenes statusa vērtības tiek kartētas uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkotas uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="b493d-435">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="b493d-436">Tālāk esošajā tabulā ir parādīts, kā ģimenes statusa vērtības tiek kartētas uz pakalpojumu Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b493d-436">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="b493d-437">Talent</span><span class="sxs-lookup"><span data-stu-id="b493d-437">Talent</span></span>                 | <span data-ttu-id="b493d-438">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b493d-438">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="b493d-439">Precējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="b493d-439">Married</span></span>                | <span data-ttu-id="b493d-440">Precējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="b493d-440">Married</span></span>              |
| <span data-ttu-id="b493d-441">Neprecējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="b493d-441">Single</span></span>                 | <span data-ttu-id="b493d-442">Neprecējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="b493d-442">Single</span></span>               |
| <span data-ttu-id="b493d-443">Atraitnis</span><span class="sxs-lookup"><span data-stu-id="b493d-443">Widowed</span></span>                | <span data-ttu-id="b493d-444">Atraitnis</span><span class="sxs-lookup"><span data-stu-id="b493d-444">Widowed</span></span>              |
| <span data-ttu-id="b493d-445">Šķīries (-usies)</span><span class="sxs-lookup"><span data-stu-id="b493d-445">Divorced</span></span>               | <span data-ttu-id="b493d-446">Šķīries (-usies)</span><span class="sxs-lookup"><span data-stu-id="b493d-446">Divorced</span></span>             |
| <span data-ttu-id="b493d-447">Reģistrētas attiecības</span><span class="sxs-lookup"><span data-stu-id="b493d-447">Registered Partnership</span></span> | <span data-ttu-id="b493d-448">Dzīvesbiedrs</span><span class="sxs-lookup"><span data-stu-id="b493d-448">Domestic Partnership</span></span> |
| <span data-ttu-id="b493d-449">Neviens</span><span class="sxs-lookup"><span data-stu-id="b493d-449">None</span></span>                   | <span data-ttu-id="b493d-450">Neviens</span><span class="sxs-lookup"><span data-stu-id="b493d-450">None</span></span>                 |
| <span data-ttu-id="b493d-451">Kopdzīve</span><span class="sxs-lookup"><span data-stu-id="b493d-451">Cohabiting</span></span>             | <span data-ttu-id="b493d-452">Kopdzīve</span><span class="sxs-lookup"><span data-stu-id="b493d-452">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="b493d-453">Dzimums</span><span class="sxs-lookup"><span data-stu-id="b493d-453">Gender</span></span>

<span data-ttu-id="b493d-454">Dzimuma apzīmējumi tiek kartēti uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkoti uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="b493d-454">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="b493d-455">Tālāk esošajā tabulā ir parādīts, kā dzimuma apzīmējumi tiek kartēti uz pakalpojumu Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b493d-455">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="b493d-456">Talent</span><span class="sxs-lookup"><span data-stu-id="b493d-456">Talent</span></span>       | <span data-ttu-id="b493d-457">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b493d-457">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="b493d-458">Vīrietis</span><span class="sxs-lookup"><span data-stu-id="b493d-458">Male</span></span>         | <span data-ttu-id="b493d-459">Vīrietis</span><span class="sxs-lookup"><span data-stu-id="b493d-459">Male</span></span>            |
| <span data-ttu-id="b493d-460">Sieviete</span><span class="sxs-lookup"><span data-stu-id="b493d-460">Female</span></span>       | <span data-ttu-id="b493d-461">Sieviete</span><span class="sxs-lookup"><span data-stu-id="b493d-461">Female</span></span>          |
| <span data-ttu-id="b493d-462">Nav specifisks</span><span class="sxs-lookup"><span data-stu-id="b493d-462">Non-specific</span></span> | <span data-ttu-id="b493d-463">*Netiek atbalstīts*</span><span class="sxs-lookup"><span data-stu-id="b493d-463">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="b493d-464">Ienākumu veida kodi</span><span class="sxs-lookup"><span data-stu-id="b493d-464">Earning codes</span></span>

<span data-ttu-id="b493d-465">Ienākumu veidu kodi unikāli identificē katra veida ienākumus, ko saņem nodarbinātie.</span><span class="sxs-lookup"><span data-stu-id="b493d-465">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="b493d-466">Kodiem ir vairāki ar ienākumiem saistīti parametri, piemēram, uzskaites nosacījumi, nodokļu likumi, pārskatu veidošanas prasības un bruto summas palielināšanas iespēja.</span><span class="sxs-lookup"><span data-stu-id="b493d-466">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="b493d-467">Ja tiek izmantota neatbalstīta biežuma vērtība, aprēķinā pēc noklusējuma tiek lietota biežuma vērtība **Katra apmaksa**.</span><span class="sxs-lookup"><span data-stu-id="b493d-467">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="b493d-468">Atbalstītās biežuma vērtības</span><span class="sxs-lookup"><span data-stu-id="b493d-468">Supported frequencies</span></span>

- <span data-ttu-id="b493d-469">Visus</span><span class="sxs-lookup"><span data-stu-id="b493d-469">All</span></span>
- <span data-ttu-id="b493d-470">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="b493d-470">EVERYPAY</span></span>
- <span data-ttu-id="b493d-471">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="b493d-471">EACHPAYPERIOD</span></span>
- <span data-ttu-id="b493d-472">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="b493d-472">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="b493d-473">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="b493d-473">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="b493d-474">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="b493d-474">1OFMTH</span></span>
- <span data-ttu-id="b493d-475">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="b493d-475">LASTOFMTH</span></span>
- <span data-ttu-id="b493d-476">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="b493d-476">2OFMTH</span></span>
- <span data-ttu-id="b493d-477">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b493d-477">3OFMTH</span></span>
- <span data-ttu-id="b493d-478">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b493d-478">4OFMTH</span></span>
- <span data-ttu-id="b493d-479">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="b493d-479">5OFMTH</span></span>
- <span data-ttu-id="b493d-480">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="b493d-480">1N2OFMTH</span></span>
- <span data-ttu-id="b493d-481">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b493d-481">3N4OFMTH</span></span>
- <span data-ttu-id="b493d-482">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b493d-482">1N3OFMTH</span></span>
- <span data-ttu-id="b493d-483">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b493d-483">1N4OFMTH</span></span>
- <span data-ttu-id="b493d-484">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b493d-484">2N3OFMTH</span></span>
- <span data-ttu-id="b493d-485">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b493d-485">2N4OFMTH</span></span>
- <span data-ttu-id="b493d-486">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b493d-486">1N2N3OFMTH</span></span>
- <span data-ttu-id="b493d-487">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b493d-487">1N2N4OFMTH</span></span>
- <span data-ttu-id="b493d-488">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b493d-488">1N3N4OFMTH</span></span>
- <span data-ttu-id="b493d-489">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b493d-489">2N3N4OFMTH</span></span>
- <span data-ttu-id="b493d-490">1N2N3N4OFMTH–1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b493d-490">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="b493d-491">2N3N4N5OFMth–2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="b493d-491">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="b493d-492">1OFQTR–1OFQTR</span><span class="sxs-lookup"><span data-stu-id="b493d-492">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="b493d-493">LASTOFQTR–LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="b493d-493">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="b493d-494">LASTMTHOFQTR–LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="b493d-494">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="b493d-495">1OFYEAR–1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="b493d-495">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="b493d-496">LASTOFYEAR–LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="b493d-496">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="b493d-497">NOVNDECOFYEAR–NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="b493d-497">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="b493d-498">Adreses</span><span class="sxs-lookup"><span data-stu-id="b493d-498">Addresses</span></span>

<span data-ttu-id="b493d-499">Noteiktas valsts vai reģiona, administratīvā apgabala un apgabala (pašvaldības) kodu identifikācijai ir nepieciešami konkrēti formāti, ko var atpazīt pakalpojums Dayforce un valsts/reģiona pakalpojumu sniedzēji.</span><span class="sxs-lookup"><span data-stu-id="b493d-499">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="b493d-500">Lai gan pilsētu formāts var būt dažāds, katrai pilsētai ir jābūt saistītai ar administratīvo apgabalu.</span><span class="sxs-lookup"><span data-stu-id="b493d-500">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="b493d-501">Talent</span><span class="sxs-lookup"><span data-stu-id="b493d-501">Talent</span></span>          | <span data-ttu-id="b493d-502">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b493d-502">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="b493d-503">Valsts/reģions</span><span class="sxs-lookup"><span data-stu-id="b493d-503">Country/Region</span></span>  | <span data-ttu-id="b493d-504">Valsts kods</span><span class="sxs-lookup"><span data-stu-id="b493d-504">Country Code</span></span>          |
| <span data-ttu-id="b493d-505">Pasta indekss</span><span class="sxs-lookup"><span data-stu-id="b493d-505">Zip/Postal Code</span></span> | <span data-ttu-id="b493d-506">Pasta indekss</span><span class="sxs-lookup"><span data-stu-id="b493d-506">Postal Code</span></span>           |
| <span data-ttu-id="b493d-507">Administratīvais apgabals</span><span class="sxs-lookup"><span data-stu-id="b493d-507">State</span></span>           | <span data-ttu-id="b493d-508">Administratīvā apgabala kods</span><span class="sxs-lookup"><span data-stu-id="b493d-508">State Code</span></span>            |
| <span data-ttu-id="b493d-509">Pilsēta</span><span class="sxs-lookup"><span data-stu-id="b493d-509">City</span></span>            | <span data-ttu-id="b493d-510">Pilsēta</span><span class="sxs-lookup"><span data-stu-id="b493d-510">City</span></span>                  |
| <span data-ttu-id="b493d-511">Apgabals</span><span class="sxs-lookup"><span data-stu-id="b493d-511">County</span></span>          | <span data-ttu-id="b493d-512">Apgabals (pašvaldība)</span><span class="sxs-lookup"><span data-stu-id="b493d-512">County (Municipality)</span></span> |
| <span data-ttu-id="b493d-513">Iela</span><span class="sxs-lookup"><span data-stu-id="b493d-513">Street</span></span>          | <span data-ttu-id="b493d-514">Adreses 1. rinda</span><span class="sxs-lookup"><span data-stu-id="b493d-514">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="b493d-515">Nodokļu reģioni</span><span class="sxs-lookup"><span data-stu-id="b493d-515">Tax regions</span></span>

<span data-ttu-id="b493d-516">Nodokļu reģionus izmanto, lai noteiktu atbilstošos nodokļus, kas jāpiemēro, ģenerējot algu aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="b493d-516">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="b493d-517">Nodokļu reģioni tiek kartēti uz pakalpojumu Dayforce kā vietas adreses.</span><span class="sxs-lookup"><span data-stu-id="b493d-517">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="b493d-518">Noklusējuma nodokļu reģionam ir jābūt saistītam ar nodarbinātā aktīvo amatu.</span><span class="sxs-lookup"><span data-stu-id="b493d-518">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="b493d-519">Nodokļu reģions (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-519">Tax region (required)</span></span>
- <span data-ttu-id="b493d-520">Valsts/reģions (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-520">Country/Region (required)</span></span>
- <span data-ttu-id="b493d-521">Administratīvais apgabals (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-521">State (required)</span></span>
- <span data-ttu-id="b493d-522">Apgabals</span><span class="sxs-lookup"><span data-stu-id="b493d-522">County</span></span> 
- <span data-ttu-id="b493d-523">Pilsēta (obligāti)</span><span class="sxs-lookup"><span data-stu-id="b493d-523">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="b493d-524">Datu konfigurēšana algu aprēķina ģenerēšanai Meksikā</span><span class="sxs-lookup"><span data-stu-id="b493d-524">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="b493d-525">Ja ģenerējat algas darbiniekiem Meksikā, ir jākonfigurē tālāk norādītie elementi.</span><span class="sxs-lookup"><span data-stu-id="b493d-525">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="b493d-526">Amatiem ir jānorāda nodaļas.</span><span class="sxs-lookup"><span data-stu-id="b493d-526">Departments are required on positions.</span></span>
- <span data-ttu-id="b493d-527">Izmaksu centri ir jāiestata kā finanšu dimensijas, un tiem ir jābūt pirmajiem elementiem noklusējuma finanšu dimensijas virknē.</span><span class="sxs-lookup"><span data-stu-id="b493d-527">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="b493d-528">Darba tipi</span><span class="sxs-lookup"><span data-stu-id="b493d-528">Job types</span></span>

<span data-ttu-id="b493d-529">Darbu veidi tiek izmantoti, lai līdzīgus darbus grupētu kategorijās.</span><span class="sxs-lookup"><span data-stu-id="b493d-529">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="b493d-530">Lai apstrādātu algas Meksikā, ir nepieciešami darbu veidi.</span><span class="sxs-lookup"><span data-stu-id="b493d-530">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="b493d-531">Daži darbu veidu piemēri ir pilna laika, nepilna laika, algots un stundu apmaksas darbs.</span><span class="sxs-lookup"><span data-stu-id="b493d-531">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="b493d-532">Darbu veidi tiek kartēti uz pakalpojumu Dayforce kā apmaksas tipi, lai norādītu, vai darbinieks saņem stundas samaksu vai algu.</span><span class="sxs-lookup"><span data-stu-id="b493d-532">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="b493d-533">Ir jānorāda tālāk norādītie darbu veidi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="b493d-533">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="b493d-534">Darba veids</span><span class="sxs-lookup"><span data-stu-id="b493d-534">Job type</span></span>   | <span data-ttu-id="b493d-535">apraksts</span><span class="sxs-lookup"><span data-stu-id="b493d-535">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="b493d-536">Ik stundu</span><span class="sxs-lookup"><span data-stu-id="b493d-536">Hourly</span></span>     | <span data-ttu-id="b493d-537">Stundu (MX)</span><span class="sxs-lookup"><span data-stu-id="b493d-537">MX Hourly</span></span>   |
| <span data-ttu-id="b493d-538">Algots</span><span class="sxs-lookup"><span data-stu-id="b493d-538">Salaried</span></span>   | <span data-ttu-id="b493d-539">Algots (MX)</span><span class="sxs-lookup"><span data-stu-id="b493d-539">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="b493d-540">Amatu veidi</span><span class="sxs-lookup"><span data-stu-id="b493d-540">Position types</span></span> 

<span data-ttu-id="b493d-541">Amatu veidus izmanto, lai norādītu, vai amats ir pilna laika, nepilna laika vai cita veida darbs.</span><span class="sxs-lookup"><span data-stu-id="b493d-541">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="b493d-542">Amatu veidi tiek kartēti uz pakalpojumu Dayforce kā apmaksas klases, lai norādītu, vai darbinieks ir pilna laika vai nepilna laika darbinieks.</span><span class="sxs-lookup"><span data-stu-id="b493d-542">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="b493d-543">Ir jānorāda tālāk norādītie amatu veidi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="b493d-543">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="b493d-544">Amata tips</span><span class="sxs-lookup"><span data-stu-id="b493d-544">Position type</span></span>   | <span data-ttu-id="b493d-545">apraksts</span><span class="sxs-lookup"><span data-stu-id="b493d-545">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="b493d-546">Pilna laika</span><span class="sxs-lookup"><span data-stu-id="b493d-546">Full-time</span></span>       | <span data-ttu-id="b493d-547">Pilna laika darbinieks</span><span class="sxs-lookup"><span data-stu-id="b493d-547">Full time employee</span></span> |
| <span data-ttu-id="b493d-548">Nepilna laika</span><span class="sxs-lookup"><span data-stu-id="b493d-548">Part-time</span></span>       | <span data-ttu-id="b493d-549">Nepilna laika darbinieks</span><span class="sxs-lookup"><span data-stu-id="b493d-549">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="b493d-550">Iemeslu kodi</span><span class="sxs-lookup"><span data-stu-id="b493d-550">Reason codes</span></span>

<span data-ttu-id="b493d-551">Iemeslu kodi sniedz informāciju par darbinieka statusu.</span><span class="sxs-lookup"><span data-stu-id="b493d-551">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="b493d-552">Iemeslu kodu tiek kartēti uz pakalpojumu Dayforce kā statusa iemesli, kas norāda darbinieka amata vai nodarbinātības statusa izmaiņu iemeslu.</span><span class="sxs-lookup"><span data-stu-id="b493d-552">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="b493d-553">Ir jānorāda tālāk norādītie iemeslu kodi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="b493d-553">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="b493d-554">Iemeslu kodi</span><span class="sxs-lookup"><span data-stu-id="b493d-554">Reason code</span></span>            | <span data-ttu-id="b493d-555">apraksts</span><span class="sxs-lookup"><span data-stu-id="b493d-555">Description</span></span>                    | <span data-ttu-id="b493d-556">Piemērojamie scenāriji</span><span class="sxs-lookup"><span data-stu-id="b493d-556">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="b493d-557">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="b493d-557">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="b493d-558">Aiziešana no amata pirms pirmās algas</span><span class="sxs-lookup"><span data-stu-id="b493d-558">Departure before first payroll</span></span> | <span data-ttu-id="b493d-559">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="b493d-559">Terminate worker</span></span>     |
| <span data-ttu-id="b493d-560">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="b493d-560">RESIGNATION</span></span>            | <span data-ttu-id="b493d-561">Atlūgums</span><span class="sxs-lookup"><span data-stu-id="b493d-561">Resignation</span></span>                    | <span data-ttu-id="b493d-562">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="b493d-562">Terminate worker</span></span>     |
| <span data-ttu-id="b493d-563">PENSION</span><span class="sxs-lookup"><span data-stu-id="b493d-563">PENSION</span></span>                | <span data-ttu-id="b493d-564">Pensija</span><span class="sxs-lookup"><span data-stu-id="b493d-564">Pension</span></span>                        | <span data-ttu-id="b493d-565">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="b493d-565">Terminate worker</span></span>     |
| <span data-ttu-id="b493d-566">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="b493d-566">TERMINATION</span></span>            | <span data-ttu-id="b493d-567">Izbeigšana</span><span class="sxs-lookup"><span data-stu-id="b493d-567">Termination</span></span>                    | <span data-ttu-id="b493d-568">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="b493d-568">Terminate worker</span></span>     |
| <span data-ttu-id="b493d-569">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="b493d-569">RETIREMENT</span></span>             | <span data-ttu-id="b493d-570">Aiziešana pensijā</span><span class="sxs-lookup"><span data-stu-id="b493d-570">Retirement</span></span>                     | <span data-ttu-id="b493d-571">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="b493d-571">Terminate worker</span></span>     |
| <span data-ttu-id="b493d-572">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="b493d-572">ABSENTEE</span></span>               | <span data-ttu-id="b493d-573">Darba kavētājs</span><span class="sxs-lookup"><span data-stu-id="b493d-573">Absentee</span></span>                       | <span data-ttu-id="b493d-574">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="b493d-574">Terminate worker</span></span>     |
| <span data-ttu-id="b493d-575">CITI</span><span class="sxs-lookup"><span data-stu-id="b493d-575">OTHER</span></span>                  | <span data-ttu-id="b493d-576">Citi iemesli</span><span class="sxs-lookup"><span data-stu-id="b493d-576">Other Reasons</span></span>                  | <span data-ttu-id="b493d-577">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="b493d-577">Terminate worker</span></span>     |
| <span data-ttu-id="b493d-578">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="b493d-578">CLOSURE</span></span>                | <span data-ttu-id="b493d-579">Uzņēmuma slēgšana</span><span class="sxs-lookup"><span data-stu-id="b493d-579">Business Closure</span></span>               | <span data-ttu-id="b493d-580">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="b493d-580">Terminate worker</span></span>     |
| <span data-ttu-id="b493d-581">DEATH</span><span class="sxs-lookup"><span data-stu-id="b493d-581">DEATH</span></span>                  | <span data-ttu-id="b493d-582">Nāve</span><span class="sxs-lookup"><span data-stu-id="b493d-582">Death</span></span>                          | <span data-ttu-id="b493d-583">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="b493d-583">Terminate worker</span></span>     |
| <span data-ttu-id="b493d-584">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="b493d-584">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="b493d-585">Atvaļinājums</span><span class="sxs-lookup"><span data-stu-id="b493d-585">Leave of Absence</span></span>               | <span data-ttu-id="b493d-586">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="b493d-586">Terminate worker</span></span>     |
| <span data-ttu-id="b493d-587">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="b493d-587">CONTRACTEND</span></span>            | <span data-ttu-id="b493d-588">Līguma beigas</span><span class="sxs-lookup"><span data-stu-id="b493d-588">End of Contract</span></span>                | <span data-ttu-id="b493d-589">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="b493d-589">Terminate worker</span></span>     |
| <span data-ttu-id="b493d-590">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="b493d-590">SALARYCHANGE</span></span>           | <span data-ttu-id="b493d-591">Algas izmaiņas</span><span class="sxs-lookup"><span data-stu-id="b493d-591">Change of Salary</span></span>               | <span data-ttu-id="b493d-592">Atlīdzība</span><span class="sxs-lookup"><span data-stu-id="b493d-592">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="b493d-593">Nodarbinātības noteikumi</span><span class="sxs-lookup"><span data-stu-id="b493d-593">Terms of employment</span></span>

<span data-ttu-id="b493d-594">Nodarbinātības noteikumus izmanto, lai izveidotu nodarbinātības noteikumu kategorijas.</span><span class="sxs-lookup"><span data-stu-id="b493d-594">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="b493d-595">Noteikumi tiek kartēti uz pakalpojumu Dayforce kā nodarbinātības rādītāju vērtības.</span><span class="sxs-lookup"><span data-stu-id="b493d-595">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="b493d-596">Ir nepieciešami tālāk norādītie nodarbinātības noteikumi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="b493d-596">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="b493d-597">Nodarbinātības noteikumi</span><span class="sxs-lookup"><span data-stu-id="b493d-597">Terms of employment</span></span>   | <span data-ttu-id="b493d-598">apraksts</span><span class="sxs-lookup"><span data-stu-id="b493d-598">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="b493d-599">Regulārs</span><span class="sxs-lookup"><span data-stu-id="b493d-599">Regular</span></span>               | <span data-ttu-id="b493d-600">Regulārs</span><span class="sxs-lookup"><span data-stu-id="b493d-600">Regular</span></span>     |
| <span data-ttu-id="b493d-601">Tieši</span><span class="sxs-lookup"><span data-stu-id="b493d-601">Direct</span></span>                | <span data-ttu-id="b493d-602">Tieši</span><span class="sxs-lookup"><span data-stu-id="b493d-602">Direct</span></span>      |
| <span data-ttu-id="b493d-603">Štažēšanās</span><span class="sxs-lookup"><span data-stu-id="b493d-603">Internship</span></span>            | <span data-ttu-id="b493d-604">Štažēšanās</span><span class="sxs-lookup"><span data-stu-id="b493d-604">Internship</span></span>  |
| <span data-ttu-id="b493d-605">Pastāvīga</span><span class="sxs-lookup"><span data-stu-id="b493d-605">Permanent</span></span>             | <span data-ttu-id="b493d-606">Pastāvīga</span><span class="sxs-lookup"><span data-stu-id="b493d-606">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="b493d-607">Ģimenes stāvoklis</span><span class="sxs-lookup"><span data-stu-id="b493d-607">Marital status</span></span>

<span data-ttu-id="b493d-608">Ģimenes statusa vērtības tiek kartētas uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkotas uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="b493d-608">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="b493d-609">Tālāk esošajā tabulā ir parādīts, kā ģimenes statusa vērtības tiek kartētas uz pakalpojumu Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b493d-609">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="b493d-610">Talent</span><span class="sxs-lookup"><span data-stu-id="b493d-610">Talent</span></span>                 | <span data-ttu-id="b493d-611">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b493d-611">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="b493d-612">Precējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="b493d-612">Married</span></span>                | <span data-ttu-id="b493d-613">Precējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="b493d-613">Married</span></span>                   |
| <span data-ttu-id="b493d-614">Neprecējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="b493d-614">Single</span></span>                 | <span data-ttu-id="b493d-615">Neprecējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="b493d-615">Single</span></span>                    |
| <span data-ttu-id="b493d-616">Atraitnis</span><span class="sxs-lookup"><span data-stu-id="b493d-616">Widowed</span></span>                | <span data-ttu-id="b493d-617">Atraitnis</span><span class="sxs-lookup"><span data-stu-id="b493d-617">Widowed</span></span>                   |
| <span data-ttu-id="b493d-618">Šķīries (-usies)</span><span class="sxs-lookup"><span data-stu-id="b493d-618">Divorced</span></span>               | <span data-ttu-id="b493d-619">Šķīries (-usies)</span><span class="sxs-lookup"><span data-stu-id="b493d-619">Divorced</span></span>                  |
| <span data-ttu-id="b493d-620">Reģistrētas attiecības</span><span class="sxs-lookup"><span data-stu-id="b493d-620">Registered Partnership</span></span> | <span data-ttu-id="b493d-621">Dzīvesbiedrs</span><span class="sxs-lookup"><span data-stu-id="b493d-621">Domestic Partnership</span></span>      |
| <span data-ttu-id="b493d-622">Neviens</span><span class="sxs-lookup"><span data-stu-id="b493d-622">None</span></span>                   | <span data-ttu-id="b493d-623">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="b493d-623">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="b493d-624">Kopdzīve</span><span class="sxs-lookup"><span data-stu-id="b493d-624">Cohabiting</span></span>             | <span data-ttu-id="b493d-625">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="b493d-625">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="b493d-626">Dzimums</span><span class="sxs-lookup"><span data-stu-id="b493d-626">Gender</span></span>

<span data-ttu-id="b493d-627">Dzimuma apzīmējumi tiek kartēti uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkoti uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="b493d-627">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="b493d-628">Tālāk esošajā tabulā ir parādīts, kā dzimuma apzīmējumi tiek kartēti uz pakalpojumu Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b493d-628">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="b493d-629">Talent</span><span class="sxs-lookup"><span data-stu-id="b493d-629">Talent</span></span>       | <span data-ttu-id="b493d-630">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b493d-630">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="b493d-631">Vīrietis</span><span class="sxs-lookup"><span data-stu-id="b493d-631">Male</span></span>         | <span data-ttu-id="b493d-632">Vīrietis</span><span class="sxs-lookup"><span data-stu-id="b493d-632">Male</span></span>                      |
| <span data-ttu-id="b493d-633">Sieviete</span><span class="sxs-lookup"><span data-stu-id="b493d-633">Female</span></span>       | <span data-ttu-id="b493d-634">Sieviete</span><span class="sxs-lookup"><span data-stu-id="b493d-634">Female</span></span>                    |
| <span data-ttu-id="b493d-635">Nav specifisks</span><span class="sxs-lookup"><span data-stu-id="b493d-635">Non-specific</span></span> | <span data-ttu-id="b493d-636">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="b493d-636">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="b493d-637">Maksājumu metode</span><span class="sxs-lookup"><span data-stu-id="b493d-637">Payment method</span></span>

<span data-ttu-id="b493d-638">Maksāšanas metodes darbiniekam un uzņēmumam ļauj aprakstīt, kā darbinieki saņems samaksu.</span><span class="sxs-lookup"><span data-stu-id="b493d-638">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="b493d-639">Maksāšanas metodes tiek kartētas uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkotas uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="b493d-639">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="b493d-640">Tālāk esošajā tabulā ir parādīts, kā maksāšanas metodes tiek kartētas uz pakalpojumu Dayforce.</span><span class="sxs-lookup"><span data-stu-id="b493d-640">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="b493d-641">Talent</span><span class="sxs-lookup"><span data-stu-id="b493d-641">Talent</span></span>             | <span data-ttu-id="b493d-642">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b493d-642">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="b493d-643">Kase</span><span class="sxs-lookup"><span data-stu-id="b493d-643">Cash</span></span>               | <span data-ttu-id="b493d-644">Kase</span><span class="sxs-lookup"><span data-stu-id="b493d-644">Cash</span></span>                      |
| <span data-ttu-id="b493d-645">Elektronisks maksājums</span><span class="sxs-lookup"><span data-stu-id="b493d-645">Electronic Payment</span></span> | <span data-ttu-id="b493d-646">Pārsūtījums</span><span class="sxs-lookup"><span data-stu-id="b493d-646">Transfer</span></span>                  |
| <span data-ttu-id="b493d-647">Atzīmēt</span><span class="sxs-lookup"><span data-stu-id="b493d-647">Check</span></span>              | <span data-ttu-id="b493d-648">Čeks</span><span class="sxs-lookup"><span data-stu-id="b493d-648">Cheque</span></span>                    |
| <span data-ttu-id="b493d-649">Bankas vekselis</span><span class="sxs-lookup"><span data-stu-id="b493d-649">Bank Draft</span></span>         | <span data-ttu-id="b493d-650">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="b493d-650">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="b493d-651">Citi</span><span class="sxs-lookup"><span data-stu-id="b493d-651">Other</span></span>              | <span data-ttu-id="b493d-652">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="b493d-652">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="b493d-653">Bankas konta tips</span><span class="sxs-lookup"><span data-stu-id="b493d-653">Bank account type</span></span>

<span data-ttu-id="b493d-654">Bankas kontu tipus izmanto darbiniekiem sūtāmajiem elektroniskajiem maksājumiem.</span><span class="sxs-lookup"><span data-stu-id="b493d-654">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="b493d-655">Bankas kontu tipi tiek kartēti uz pakalpojumu Dayforce kā pārsūtīšanas konta informācija.</span><span class="sxs-lookup"><span data-stu-id="b493d-655">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="b493d-656">Bankas kontu tipi integrācijas laikā tiek atbilstoši tulkoti uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="b493d-656">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="b493d-657">Talent</span><span class="sxs-lookup"><span data-stu-id="b493d-657">Talent</span></span>            | <span data-ttu-id="b493d-658">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b493d-658">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="b493d-659">Kontroles konts</span><span class="sxs-lookup"><span data-stu-id="b493d-659">Checking Account</span></span>  | <span data-ttu-id="b493d-660">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="b493d-660">CheckingAccount</span></span>           |
| <span data-ttu-id="b493d-661">Algu konts</span><span class="sxs-lookup"><span data-stu-id="b493d-661">Payroll Account</span></span>   | <span data-ttu-id="b493d-662">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="b493d-662">PayrollAccount</span></span>            |
| <span data-ttu-id="b493d-663">Uzkrājumu konts</span><span class="sxs-lookup"><span data-stu-id="b493d-663">Savings Account</span></span>   | <span data-ttu-id="b493d-664">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="b493d-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="b493d-665">BankGirot konts</span><span class="sxs-lookup"><span data-stu-id="b493d-665">BankGirot account</span></span> | <span data-ttu-id="b493d-666">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="b493d-666">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="b493d-667">PlusGirot konts</span><span class="sxs-lookup"><span data-stu-id="b493d-667">PlusGirot account</span></span> | <span data-ttu-id="b493d-668">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="b493d-668">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="b493d-669">Ienākumu veida kodi</span><span class="sxs-lookup"><span data-stu-id="b493d-669">Earning codes</span></span>

<span data-ttu-id="b493d-670">Ienākumu veidu kodi unikāli identificē katra veida ienākumus, ko saņem nodarbinātie.</span><span class="sxs-lookup"><span data-stu-id="b493d-670">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="b493d-671">Kodiem ir vairāki ar ienākumiem saistīti parametri, piemēram, uzskaites nosacījumi, nodokļu likumi, pārskatu veidošanas prasības un bruto summas palielināšanas iespēja.</span><span class="sxs-lookup"><span data-stu-id="b493d-671">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="b493d-672">Ja tiek izmantota neatbalstīta biežuma vērtība, aprēķinā pēc noklusējuma tiek lietota biežuma vērtība **Katra apmaksa**.</span><span class="sxs-lookup"><span data-stu-id="b493d-672">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="b493d-673">Atbalstītās biežuma vērtības</span><span class="sxs-lookup"><span data-stu-id="b493d-673">Supported frequencies</span></span>

- <span data-ttu-id="b493d-674">Visus</span><span class="sxs-lookup"><span data-stu-id="b493d-674">All</span></span>
- <span data-ttu-id="b493d-675">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="b493d-675">EVERYPAY</span></span>
- <span data-ttu-id="b493d-676">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="b493d-676">EACHPAYPERIOD</span></span>
- <span data-ttu-id="b493d-677">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="b493d-677">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="b493d-678">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="b493d-678">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="b493d-679">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="b493d-679">1OFMTH</span></span>
- <span data-ttu-id="b493d-680">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="b493d-680">LASTOFMTH</span></span>
- <span data-ttu-id="b493d-681">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="b493d-681">2OFMTH</span></span>
- <span data-ttu-id="b493d-682">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b493d-682">3OFMTH</span></span>
- <span data-ttu-id="b493d-683">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b493d-683">4OFMTH</span></span>
- <span data-ttu-id="b493d-684">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="b493d-684">5OFMTH</span></span>
- <span data-ttu-id="b493d-685">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="b493d-685">1N2OFMTH</span></span>
- <span data-ttu-id="b493d-686">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b493d-686">3N4OFMTH</span></span>
- <span data-ttu-id="b493d-687">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b493d-687">1N3OFMTH</span></span>
- <span data-ttu-id="b493d-688">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b493d-688">1N4OFMTH</span></span>
- <span data-ttu-id="b493d-689">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b493d-689">2N3OFMTH</span></span>
- <span data-ttu-id="b493d-690">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b493d-690">2N4OFMTH</span></span>
- <span data-ttu-id="b493d-691">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="b493d-691">1N2N3OFMTH</span></span>
- <span data-ttu-id="b493d-692">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b493d-692">1N2N4OFMTH</span></span>
- <span data-ttu-id="b493d-693">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b493d-693">1N3N4OFMTH</span></span>
- <span data-ttu-id="b493d-694">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b493d-694">2N3N4OFMTH</span></span>
- <span data-ttu-id="b493d-695">1N2N3N4OFMTH–1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="b493d-695">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="b493d-696">2N3N4N5OFMth–2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="b493d-696">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="b493d-697">1OFQTR–1OFQTR</span><span class="sxs-lookup"><span data-stu-id="b493d-697">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="b493d-698">LASTOFQTR–LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="b493d-698">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="b493d-699">LASTMTHOFQTR–LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="b493d-699">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="b493d-700">1OFYEAR–1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="b493d-700">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="b493d-701">LASTOFYEAR–LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="b493d-701">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="b493d-702">NOVNDECOFYEAR–NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="b493d-702">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="b493d-703">Adreses</span><span class="sxs-lookup"><span data-stu-id="b493d-703">Addresses</span></span>

<span data-ttu-id="b493d-704">Noteiktas valsts vai reģiona, administratīvā apgabala un apgabala (pašvaldības) kodu identifikācijai ir nepieciešami konkrēti formāti, ko var atpazīt pakalpojums Dayforce un valsts/reģiona pakalpojumu sniedzēji.</span><span class="sxs-lookup"><span data-stu-id="b493d-704">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="b493d-705">Lai gan pilsētu formāts var būt dažāds, katrai pilsētai ir jābūt saistītai ar administratīvo apgabalu.</span><span class="sxs-lookup"><span data-stu-id="b493d-705">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="b493d-706">Talent</span><span class="sxs-lookup"><span data-stu-id="b493d-706">Talent</span></span>              | <span data-ttu-id="b493d-707">Dayforce</span><span class="sxs-lookup"><span data-stu-id="b493d-707">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="b493d-708">Valsts/reģions</span><span class="sxs-lookup"><span data-stu-id="b493d-708">Country/Region</span></span>      | <span data-ttu-id="b493d-709">Valsts kods</span><span class="sxs-lookup"><span data-stu-id="b493d-709">Country Code</span></span>          |
| <span data-ttu-id="b493d-710">Pasta indekss</span><span class="sxs-lookup"><span data-stu-id="b493d-710">Zip/Postal Code</span></span>     | <span data-ttu-id="b493d-711">Pasta indekss</span><span class="sxs-lookup"><span data-stu-id="b493d-711">Postal Code</span></span>           |
| <span data-ttu-id="b493d-712">Administratīvais apgabals</span><span class="sxs-lookup"><span data-stu-id="b493d-712">State</span></span>               | <span data-ttu-id="b493d-713">Administratīvā apgabala kods</span><span class="sxs-lookup"><span data-stu-id="b493d-713">State Code</span></span>            |
| <span data-ttu-id="b493d-714">Pilsēta</span><span class="sxs-lookup"><span data-stu-id="b493d-714">City</span></span>                | <span data-ttu-id="b493d-715">Pilsēta</span><span class="sxs-lookup"><span data-stu-id="b493d-715">City</span></span>                  |
| <span data-ttu-id="b493d-716">Apgabals</span><span class="sxs-lookup"><span data-stu-id="b493d-716">County</span></span>              | <span data-ttu-id="b493d-717">Apgabals (pašvaldība)</span><span class="sxs-lookup"><span data-stu-id="b493d-717">County (Municipality)</span></span> |
| <span data-ttu-id="b493d-718">Iela</span><span class="sxs-lookup"><span data-stu-id="b493d-718">Street</span></span>              | <span data-ttu-id="b493d-719">Adreses 1. rinda</span><span class="sxs-lookup"><span data-stu-id="b493d-719">Address Line 1</span></span>        |
| <span data-ttu-id="b493d-720">Ielas numurs</span><span class="sxs-lookup"><span data-stu-id="b493d-720">Street Number</span></span>       | <span data-ttu-id="b493d-721">Adreses 2. rinda</span><span class="sxs-lookup"><span data-stu-id="b493d-721">Address Line 2</span></span>        |
| <span data-ttu-id="b493d-722">Mājas numurs/nosaukums</span><span class="sxs-lookup"><span data-stu-id="b493d-722">Building Complement</span></span> | <span data-ttu-id="b493d-723">Adreses 5. rinda</span><span class="sxs-lookup"><span data-stu-id="b493d-723">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="b493d-724">Pases numurs</span><span class="sxs-lookup"><span data-stu-id="b493d-724">Passport number</span></span>

<span data-ttu-id="b493d-725">Darbinieki var sniegt pases informāciju.</span><span class="sxs-lookup"><span data-stu-id="b493d-725">Employees can declare passport information.</span></span> <span data-ttu-id="b493d-726">Šīs informācijas identifikācijas tips ir **Pase**, un tā tiek integrēta pakalpojumā Dayforce kā daļa no darbinieka Meksikai specifiskās informācijas.</span><span class="sxs-lookup"><span data-stu-id="b493d-726">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="b493d-727">Identifikācijas tips = Pase</span><span class="sxs-lookup"><span data-stu-id="b493d-727">Identification Type = "Passport"</span></span>
- <span data-ttu-id="b493d-728">Izdošanas datums</span><span class="sxs-lookup"><span data-stu-id="b493d-728">Issued Date</span></span>
- <span data-ttu-id="b493d-729">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="b493d-729">Expiration Date</span></span>

<span data-ttu-id="b493d-730">Darbinieki var sniegt vairākus identifikācijas numurus, kuru identifikācijas tips ir **Pase**.</span><span class="sxs-lookup"><span data-stu-id="b493d-730">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="b493d-731">Taču pakalpojumā Dayforce tiek integrēts tikai pašreizējais aktīvais pases ieraksts.</span><span class="sxs-lookup"><span data-stu-id="b493d-731">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="b493d-732">Ja visiem pases ierakstiem ir beidzies derīgiem, pakalpojumā Dayforce tiek integrēta pēdējā izdotā pase.</span><span class="sxs-lookup"><span data-stu-id="b493d-732">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
