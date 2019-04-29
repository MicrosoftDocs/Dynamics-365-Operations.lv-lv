---
title: Algu aprēķina integrācijas konfigurēšana pakalpojumos Talent un Dayforce
description: Šajā tēmā ir paskaidrots, kā konfigurēt Microsoft Dynamics 365 for Talent un Ceridian Dayforce integrāciju, lai varētu apstrādāt maksājuma izpildi.
author: andreabichsel
manager: AnnBe
ms.date: 03/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9a88bf61dbb12520b555ceb7363b1c646d95386e
ms.sourcegitcommit: 204e4554e409c39fbbf7b273ad138ce2809931a8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/26/2019
ms.locfileid: "898448"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="6f1e4-103">Talent un Dayforce algu aprēķina integrācijas konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="6f1e4-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6f1e4-104">Microsoft Dynamics 365 for Talent un Ceridian Dayforce integrācijai tiek izmantotas vairākas konfigurācijas darbības, kas ir aprakstītas šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="6f1e4-105">Pirms maksājuma izpildes apstrādes vispirms ir jākonfigurē integrācija gan pakalpojumā Talent, gan pakalpojumā Dayforce.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="6f1e4-106">Ja maksājumu izpildei izmantojat tādu pakalpojumu kā Dayforce, jums ir jāiespējo integrācija pakalpojumā Talent.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="6f1e4-107">Integrācijai ir nepieciešami noteikti Talent dati.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="6f1e4-108">Tādēļ ir jāpārliecinās, vai uz Dayforce kartētie dati pakalpojumā Talent ir konfigurēti veidā, kas atbalsta integrāciju.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="6f1e4-109">Integrācija izmanto tālāk norādītās vispārējās datu kategorijas.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="6f1e4-110">Personāla vadības dati</span><span class="sxs-lookup"><span data-stu-id="6f1e4-110">Human resources data</span></span>
- <span data-ttu-id="6f1e4-111">Atlīdzības dati</span><span class="sxs-lookup"><span data-stu-id="6f1e4-111">Compensation data</span></span>
- <span data-ttu-id="6f1e4-112">Algu dati, piemēram, apmaksas cikli, apmaksas periodi un ienākumu veidu kodi</span><span class="sxs-lookup"><span data-stu-id="6f1e4-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="6f1e4-113">Nodarbināto dati</span><span class="sxs-lookup"><span data-stu-id="6f1e4-113">Worker data</span></span>

<span data-ttu-id="6f1e4-114">Šajā tēmā ir aprakstītas darbības, kas jāveic, lai iespējotu integrāciju.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="6f1e4-115">Tajā ir arī izskaidrots, kādu veidu dati un konfigurācijas informācija ir nepieciešama integrācijai.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="6f1e4-116">Integrācijas iespējošana</span><span class="sxs-lookup"><span data-stu-id="6f1e4-116">Enable the integration</span></span>

<span data-ttu-id="6f1e4-117">Lai izveidotu savienojumu ar Dayforce, pakalpojumā Talent ir jāieslēdz integrācija un jāievada konfigurācijas informācija.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="6f1e4-118">Ja vēlaties, lai izveidotā Virsgrāmatas transakcija tiktu importēta programmā Microsoft Dynamics 365 for Finance and Operations, ir jāiestata arī Microsoft Azure krātuves konts un programmā Finance and Operations jāievada Azure krātuves savienojuma virkne.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="6f1e4-119">Lai pakalpojumā Talent ieslēgtu integrāciju, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="6f1e4-120">Lapā **Sistēmas administrēšana** atlasiet opciju **Integrācijas konfigurēšana**.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="6f1e4-121">Ievadiet drošo failu pārsūtīšanas protokola (FTP) galapunktu un drošo FTP mapes ceļu.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="6f1e4-122">Ievadiet tā lietotāja lietotājvārdu un paroli, kurš piekļūs drošajam FTP galapunktam un mapes ceļam.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="6f1e4-123">Pārbaudiet savienojumu, kā nepieciešams, un opciju **Iespējot algu aprēķina integrāciju** iestatiet uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="6f1e4-124">Kad integrācija ir ieslēgta, tiek izveidota datu eksportēšanas pakotne un faili, kā arī iestatīts biežums.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="6f1e4-125">Biežumu varat mainīt atbilstoši vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="6f1e4-126">Papildinformāciju par Azure krātuves kontiem un Azure krātuves savienojuma virknēm skatiet tālāk sniegtajās Azure tēmās.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="6f1e4-127">Par Azure krātuves kontiem</span><span class="sxs-lookup"><span data-stu-id="6f1e4-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="6f1e4-128">Azure krātuves savienojuma virkņu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="6f1e4-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a><span data-ttu-id="6f1e4-129">Datu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="6f1e4-129">Configure your data</span></span> 

<span data-ttu-id="6f1e4-130">Lai apstrādātu algas, pakalpojumā Talent ir jākonfigurē personāla vadības dati.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-130">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="6f1e4-131">Jums ir jāiestata organizācijas dati, piemēram, darbi un amati, kā arī informācija par atvieglojumiem un atlīdzību.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-131">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="6f1e4-132">Šie dati nodrošina informāciju par nodarbinātību, samaksu un ieturējumiem, kas nepieciešama darbinieka algas ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-132">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="6f1e4-133">Personāla vadības dati</span><span class="sxs-lookup"><span data-stu-id="6f1e4-133">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="6f1e4-134">Atvieglojumi</span><span class="sxs-lookup"><span data-stu-id="6f1e4-134">Benefits</span></span> 

<span data-ttu-id="6f1e4-135">Personāla vadība nodrošina rīkus, ko var izmantot, lai iestatītu un uzturētu atvieglojumus, ieturējumus un nodarbināto atlīdzības plānus, ko organizācija piedāvā vai apstrādā saviem nodarbinātajiem.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-135">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="6f1e4-136">Kad veidojat atvieglojumus, ņemiet vērā tālāk norādītos datus un konfigurācijas, kas tiek izmantoti pakalpojumā Dayforce.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-136">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="6f1e4-137">Atvieglojumu plāni</span><span class="sxs-lookup"><span data-stu-id="6f1e4-137">Benefit plans</span></span>

- <span data-ttu-id="6f1e4-138">Plāns (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-138">Plan (required)</span></span>
- <span data-ttu-id="6f1e4-139">Tips (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-139">Type (required)</span></span>
- <span data-ttu-id="6f1e4-140">Algas ietekme (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-140">Payroll impact (required)</span></span>
- <span data-ttu-id="6f1e4-141">Atgūt nokavētos maksājumus</span><span class="sxs-lookup"><span data-stu-id="6f1e4-141">Recover arrears</span></span>
- <span data-ttu-id="6f1e4-142">Ieturējuma metode</span><span class="sxs-lookup"><span data-stu-id="6f1e4-142">Deduction method</span></span>
- <span data-ttu-id="6f1e4-143">Ieturējuma prioritāte</span><span class="sxs-lookup"><span data-stu-id="6f1e4-143">Deduction priority</span></span>
- <span data-ttu-id="6f1e4-144">Ierobežojuma periods</span><span class="sxs-lookup"><span data-stu-id="6f1e4-144">Limit period</span></span>
- <span data-ttu-id="6f1e4-145">Ierobežojuma summa</span><span class="sxs-lookup"><span data-stu-id="6f1e4-145">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="6f1e4-146">Atvieglojumi</span><span class="sxs-lookup"><span data-stu-id="6f1e4-146">Benefits</span></span>

- <span data-ttu-id="6f1e4-147">Plāns (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-147">Plan (required)</span></span>
- <span data-ttu-id="6f1e4-148">Tips (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-148">Type (required)</span></span>
- <span data-ttu-id="6f1e4-149">Opcija (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-149">Option (required)</span></span>
- <span data-ttu-id="6f1e4-150">Atvieglojumu ID (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-150">Benefit ID (required)</span></span>
- <span data-ttu-id="6f1e4-151">Biežums</span><span class="sxs-lookup"><span data-stu-id="6f1e4-151">Frequency</span></span>
- <span data-ttu-id="6f1e4-152">Pamats</span><span class="sxs-lookup"><span data-stu-id="6f1e4-152">Basis</span></span>
- <span data-ttu-id="6f1e4-153">Summa vai likme</span><span class="sxs-lookup"><span data-stu-id="6f1e4-153">Amount or rate</span></span>
- <span data-ttu-id="6f1e4-154">Ienākumu veida kods</span><span class="sxs-lookup"><span data-stu-id="6f1e4-154">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="6f1e4-155">Atbalstītās biežuma vērtības</span><span class="sxs-lookup"><span data-stu-id="6f1e4-155">Supported frequencies</span></span> 

- <span data-ttu-id="6f1e4-156">Katru nedēļu</span><span class="sxs-lookup"><span data-stu-id="6f1e4-156">Weekly</span></span>
- <span data-ttu-id="6f1e4-157">Katru otro nedēļu</span><span class="sxs-lookup"><span data-stu-id="6f1e4-157">Bi-weekly</span></span>
- <span data-ttu-id="6f1e4-158">Pusmēneša</span><span class="sxs-lookup"><span data-stu-id="6f1e4-158">Semi-monthly</span></span>
- <span data-ttu-id="6f1e4-159">Mēnesis</span><span class="sxs-lookup"><span data-stu-id="6f1e4-159">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="6f1e4-160">Atbalstītās pamata vērtības</span><span class="sxs-lookup"><span data-stu-id="6f1e4-160">Supported bases</span></span> 

- <span data-ttu-id="6f1e4-161">Fiksēta summa</span><span class="sxs-lookup"><span data-stu-id="6f1e4-161">Fixed amount</span></span>
- <span data-ttu-id="6f1e4-162">Ienākumu procentuālais daudzums</span><span class="sxs-lookup"><span data-stu-id="6f1e4-162">Percent of earnings</span></span>
- <span data-ttu-id="6f1e4-163">Produktīvās stundas</span><span class="sxs-lookup"><span data-stu-id="6f1e4-163">Productive hours</span></span>

<span data-ttu-id="6f1e4-164">Dayforce izveido tālāk norādītos ieturējumus, pamatojoties uz atvieglojumu plānā definēto algas ietekmi.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-164">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="6f1e4-165">Atlase pakalpojumā Talent</span><span class="sxs-lookup"><span data-stu-id="6f1e4-165">Selection in Talent</span></span>        | <span data-ttu-id="6f1e4-166">Rezultāts pakalpojumā Dayforce</span><span class="sxs-lookup"><span data-stu-id="6f1e4-166">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="6f1e4-167">Neviens</span><span class="sxs-lookup"><span data-stu-id="6f1e4-167">None</span></span>                       | <span data-ttu-id="6f1e4-168">Nav izveidots neviens ieturējums.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-168">No deduction is created.</span></span>                      |
| <span data-ttu-id="6f1e4-169">Tikai ieturējums</span><span class="sxs-lookup"><span data-stu-id="6f1e4-169">Deduction only</span></span>             | <span data-ttu-id="6f1e4-170">Ir izveidots darbinieka ieturējums.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-170">An employee deduction is created.</span></span>             |
| <span data-ttu-id="6f1e4-171">Tikai segums</span><span class="sxs-lookup"><span data-stu-id="6f1e4-171">Contribution only</span></span>          | <span data-ttu-id="6f1e4-172">Ir izveidots darba devēja ieturējums.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-172">An employer deduction is created.</span></span>             |
| <span data-ttu-id="6f1e4-173">Ieturējums un segums</span><span class="sxs-lookup"><span data-stu-id="6f1e4-173">Deduction and contribution</span></span> | <span data-ttu-id="6f1e4-174">Ir izveidots darbinieka un darba devēja ieturējums.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-174">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="6f1e4-175">Papildinformāciju par atvieglojumu programmas definēšanu un pārvaldību skatiet tālāk sniegtajās tēmās.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-175">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="6f1e4-176">Darbinieku atvieglojumu programmas nodrošināšana</span><span class="sxs-lookup"><span data-stu-id="6f1e4-176">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="6f1e4-177">Jauna atvieglojuma izveide</span><span class="sxs-lookup"><span data-stu-id="6f1e4-177">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="6f1e4-178">Atvieglojumu piemērotības kārtulu un ierobežojumu definēšana</span><span class="sxs-lookup"><span data-stu-id="6f1e4-178">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="6f1e4-179">Atvieglojumu reģistrēšana un noņemšana nodarbinātajiem</span><span class="sxs-lookup"><span data-stu-id="6f1e4-179">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="6f1e4-180">Atlīdzība</span><span class="sxs-lookup"><span data-stu-id="6f1e4-180">Compensation</span></span> 

<span data-ttu-id="6f1e4-181">Atlīdzību pārvaldība tiek izmantota, lai kontrolētu pamatalgas un prēmiju izsniegšanu.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-181">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="6f1e4-182">Darbinieka fiksētā pamatalga un nopelnu palielinājumi tiek kontrolēti, izmantojot fiksētas atlīdzības plānus.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-182">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="6f1e4-183">Veicināšanas maksājumu izsniegšana, piemēram, prēmiju maksājumi, apbalvojumi par sasniegumiem, uzņēmuma akciju iegādes iespējas un dotācijas, kā arī vienreizējas piemaksas, tiek kontrolētas ar mainīgās atlīdzības plāniem.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-183">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="6f1e4-184">Dayforce izmanto atlīdzības informāciju, lai aprēķinātu darbinieka stundas vai gada likmi.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-184">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="6f1e4-185">Ir jānorāda fiksētās atlīdzības plāni un apmaksas likmes konvertēšanas gadījumi.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-185">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="6f1e4-186">Darbiniekiem ir jābūt saistītiem ar fiksētās atlīdzības plānu.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-186">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="6f1e4-187">Papildinformāciju par atlīdzības plāniem skatiet tālāk sniegtajās tēmās.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-187">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="6f1e4-188">Fiksētās atlīdzības plānu izveidošana</span><span class="sxs-lookup"><span data-stu-id="6f1e4-188">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="6f1e4-189">Mainīgās atlīdzības plānu izveidošana</span><span class="sxs-lookup"><span data-stu-id="6f1e4-189">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="6f1e4-190">Algas/atlīdzības organizācijas un plānu izstrāde</span><span class="sxs-lookup"><span data-stu-id="6f1e4-190">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="6f1e4-191">Procesa kompensācija</span><span class="sxs-lookup"><span data-stu-id="6f1e4-191">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="6f1e4-192">Atlīdzības procesa definēšana un rezultātu aprēķināšana</span><span class="sxs-lookup"><span data-stu-id="6f1e4-192">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="6f1e4-193">Darbinieka reģistrēšana fiksētās atlīdzības plānā</span><span class="sxs-lookup"><span data-stu-id="6f1e4-193">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="6f1e4-194">Darbinieka reģistrēšana mainīgās atlīdzības plānā</span><span class="sxs-lookup"><span data-stu-id="6f1e4-194">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="6f1e4-195">Darbi</span><span class="sxs-lookup"><span data-stu-id="6f1e4-195">Jobs</span></span> 

<span data-ttu-id="6f1e4-196">Darbs ir uzdevumu un atbildības jomu kopums, kas ir jāizpilda personai, kura veic darbu.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-196">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="6f1e4-197">Lai iegūtu papildu informāciju, skatiet šādas tēmas:</span><span class="sxs-lookup"><span data-stu-id="6f1e4-197">For more information, see the following topics:</span></span>

- [<span data-ttu-id="6f1e4-198">Darba komponentu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="6f1e4-198">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="6f1e4-199">Jaunu darbu definēšana</span><span class="sxs-lookup"><span data-stu-id="6f1e4-199">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="6f1e4-200">Amati</span><span class="sxs-lookup"><span data-stu-id="6f1e4-200">Positions</span></span>

<span data-ttu-id="6f1e4-201">Pozīcija ir atsevišķa darba instance.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-201">A position is an individual instance of a job.</span></span> <span data-ttu-id="6f1e4-202">Piemēram, amats Pārdošanas daļas vadītājs (austrumu reģions) ir tikai viens no amatiem, kas ir saistīti ar darbu Pārdošanas daļas vadītājs.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-202">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="6f1e4-203">Amats pastāv nodaļā.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-203">A position exists in a department.</span></span> <span data-ttu-id="6f1e4-204">Ar katru amatu var būt saistīts tikai viens nodarbinātais.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-204">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="6f1e4-205">Iestatot jaunus amatus, ņemiet vērā tālāk norādītos datus un konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-205">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="6f1e4-206">Amats (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-206">Position (required)</span></span>
- <span data-ttu-id="6f1e4-207">Apraksts (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-207">Description (required)</span></span>
- <span data-ttu-id="6f1e4-208">Darbs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-208">Job (required)</span></span>
- <span data-ttu-id="6f1e4-209">Nodaļa (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-209">Department (required)</span></span>
- <span data-ttu-id="6f1e4-210">Amata veids (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-210">Position type (required)</span></span>
- <span data-ttu-id="6f1e4-211">Pilnas slodzes ekvivalents</span><span class="sxs-lookup"><span data-stu-id="6f1e4-211">Full-time equivalent</span></span>
- <span data-ttu-id="6f1e4-212">Ikgadējās parastās stundas (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-212">Annual regular hours (required)</span></span>
- <span data-ttu-id="6f1e4-213">Apmaksātāja juridiskā persona (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-213">Paid by legal entity (required)</span></span>
- <span data-ttu-id="6f1e4-214">Apmaksas cikls (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-214">Pay cycle (required)</span></span>
- <span data-ttu-id="6f1e4-215">Noklusējuma finanšu dimensija — izmaksu centrs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-215">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="6f1e4-216">Nodarbinātā piešķire — nodarbinātais, piešķires sākums, piešķires beigas, iemesla kods</span><span class="sxs-lookup"><span data-stu-id="6f1e4-216">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="6f1e4-217">Ja vienā nodaļā ar to pašu darbu ir saistīti vairāki amati, tie pakalpojumā Dayforce tiek apvienoti vienā amatā.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-217">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="6f1e4-218">Lai iegūtu papildu informāciju, skatiet šādas tēmas:</span><span class="sxs-lookup"><span data-stu-id="6f1e4-218">For more information, see the following topics:</span></span>

- [<span data-ttu-id="6f1e4-219">Organizēt darbaspēku, izmantojot nodaļas, darbus un amatus</span><span class="sxs-lookup"><span data-stu-id="6f1e4-219">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="6f1e4-220">Amatu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="6f1e4-220">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="6f1e4-221">Nodaļas</span><span class="sxs-lookup"><span data-stu-id="6f1e4-221">Departments</span></span>

<span data-ttu-id="6f1e4-222">Nodaļa ir pārvaldības struktūrvienība, kas pārstāv organizācijas kategoriju vai funkcionālo apgabalu.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-222">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="6f1e4-223">Nodaļa ir atbildīga par noteiktu organizācijas jomu, piemēram, pārdošanu, uzskaiti vai personāla vadību.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-223">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="6f1e4-224">Nodaļas var izmantot, lai ziņotu par funkcionālām jomām.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-224">You can use departments to report on functional areas.</span></span> <span data-ttu-id="6f1e4-225">Nodaļām var būt peļņas un zaudējumu atbildība.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-225">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="6f1e4-226">Lai iegūtu papildu informāciju, skatiet šādas tēmas:</span><span class="sxs-lookup"><span data-stu-id="6f1e4-226">For more information, see the following topics:</span></span>

- [<span data-ttu-id="6f1e4-227">Nodaļas izveide un tās saistīšana ar nodaļu hierarhiju</span><span class="sxs-lookup"><span data-stu-id="6f1e4-227">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="6f1e4-228">Jaunu nodaļu definēšana</span><span class="sxs-lookup"><span data-stu-id="6f1e4-228">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="6f1e4-229">Apmaksas cikli un apmaksas periodi</span><span class="sxs-lookup"><span data-stu-id="6f1e4-229">Pay cycles and pay periods</span></span>

<span data-ttu-id="6f1e4-230">Apmaksas cikls nosaka, cik bieži tiek veikts algu aprēķins, kā arī konkrētās dienas, kurās nodarbinātie saņem samaksu.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-230">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="6f1e4-231">Apmaksas cikls var būt, piemēram, ikmēneša, un darbinieki samaksu var saņemt mēneša pēdējā dienā.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-231">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="6f1e4-232">Vai arī apmaksas cikls var būt iknedēļas, un darbinieki samaksu var saņemt otrdienā pēc apmaksas perioda beigām.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-232">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="6f1e4-233">Apmaksas cikli tiek piešķirti amatiem, lai kontrolētu to, kad nodarbinātie šajos amatos saņems samaksu.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-233">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="6f1e4-234">Pēc apmaksas ciklu izveides katram ciklam varat ģenerēt apmaksas periodus.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-234">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="6f1e4-235">Katrā apmaksas periodā ir ietverts noklusējuma maksājuma datums, kura pamatā ir jūsu sniegtā informācija.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-235">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="6f1e4-236">Taču varat modificēt apmaksas perioda noklusējuma maksājuma datumu izņēmumu iestatīšanai, piemēram, kad maksājuma datums ir brīvdienā.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-236">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="6f1e4-237">Dayforce izmanto tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-237">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="6f1e4-238">Apmaksas cikls (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-238">Pay cycle (required)</span></span>
- <span data-ttu-id="6f1e4-239">Apmaksas cikla biežums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-239">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="6f1e4-240">Perioda sākuma datums (ir jānorāda pirmais apmaksas periods)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-240">Period start date (first pay period required)</span></span>
- <span data-ttu-id="6f1e4-241">Noklusējuma maksājuma datums (ir jānorāda pirmais apmaksas periods)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-241">Default payment date (first pay period required)</span></span>

<span data-ttu-id="6f1e4-242">Šī informācija pakalpojumā Dayforce ir integrēta kā apmaksas grupas, un katram apmaksas ciklam to atdala valsts vai reģions.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-242">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="6f1e4-243">Pirms integrācijas ir jābūt ģenerētam vismaz vienam apmaksas periodam.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-243">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="6f1e4-244">Dayforce ģenerē apmaksas grupu kalendārus un maksājumu datumus atbilstoši pakalpojumā Talent iestatītajam pirmā apmaksas perioda sākuma datumam un noklusējuma maksājuma datumam.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-244">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="6f1e4-245">Ienākumu veida kodi</span><span class="sxs-lookup"><span data-stu-id="6f1e4-245">Earning codes</span></span>

<span data-ttu-id="6f1e4-246">Ienākumu veidu kodi unikāli identificē katra veida ienākumus, ko saņem nodarbinātie.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-246">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="6f1e4-247">Kodiem ir dažādi ar ienākumiem saistīti parametri, piemēram, uzskaites nosacījumi, nodokļu likumi, pārskatu veidošanas prasības un bruto summas palielināšanas iespēja.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-247">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="6f1e4-248">Dayforce izmanto tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="6f1e4-249">Ienākumu veida kods (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-249">Earning Code (required)</span></span>
- <span data-ttu-id="6f1e4-250">apraksts</span><span class="sxs-lookup"><span data-stu-id="6f1e4-250">Description</span></span>
- <span data-ttu-id="6f1e4-251">Mērvienība</span><span class="sxs-lookup"><span data-stu-id="6f1e4-251">Unit of measure</span></span>
- <span data-ttu-id="6f1e4-252">Produktīvs</span><span class="sxs-lookup"><span data-stu-id="6f1e4-252">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="6f1e4-253">Nodarbināto dati</span><span class="sxs-lookup"><span data-stu-id="6f1e4-253">Worker data</span></span>

<span data-ttu-id="6f1e4-254">Dažādo veidu nodarbināto ieraksti ir svarīga informācija personāla vadības un algu sistēmās.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-254">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="6f1e4-255">Ievadīto informāciju var izmantot, lai sekotu nodarbinātajiem un personiskajai informācijai.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-255">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="6f1e4-256">Par darbiniekiem var saglabāt tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-256">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="6f1e4-257">**Pamata** — saglabājiet pamata informāciju par darbinieku, piemēram, kontaktinformāciju, demogrāfisko informāciju, identifikācijas informāciju, ģimenes informāciju, karadienesta statusu, ekspatriantu informāciju, kā arī personiskās un ārkārtas kontaktpersonas.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-257">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="6f1e4-258">**Nodarbinātība** — saglabājiet informāciju par darbinieka nodarbinātību, piemēram, informāciju par piederību uzņēmumam vai organizācijai, amata piešķiri, sākuma un beigu datumiem, piemērotību darbam, nodarbinātības noteikumiem, pensiju, atvaļinājumu un pārcelšanu.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-258">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="6f1e4-259">**Atvaļinājumi un kavējumi** — saglabājiet informāciju par nodarbinātā kavējumiem, piemēram, informāciju par darba kalendāriem, kavējumu darbībām un kavējumu iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-259">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="6f1e4-260">**Atlīdzība un alga** — saglabājiet informāciju par nodarbinātā atlīdzības plāniem un algas informāciju, piemēram, plāna reģistrāciju, piemaksām, sniegumu, komisiju, nodokļu informāciju, pensionēšanos un ieturējumiem no algas.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-260">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="6f1e4-261">Ievadot informāciju par nodarbināto, ņemiet vērā tālāk norādītos datus un konfigurācijas, kas tiek izmantoti pakalpojumā Dayforce.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-261">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="6f1e4-262">Vispārīgā informācija</span><span class="sxs-lookup"><span data-stu-id="6f1e4-262">General information</span></span>

- <span data-ttu-id="6f1e4-263">Personāla numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-263">Personnel number (required)</span></span>
- <span data-ttu-id="6f1e4-264">Vārds (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-264">First name (required)</span></span>
- <span data-ttu-id="6f1e4-265">Uzvārds (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-265">Last name (required)</span></span>
- <span data-ttu-id="6f1e4-266">Otrais vārds</span><span class="sxs-lookup"><span data-stu-id="6f1e4-266">Middle name</span></span>
- <span data-ttu-id="6f1e4-267">Darba stāža datums</span><span class="sxs-lookup"><span data-stu-id="6f1e4-267">Seniority date</span></span>
- <span data-ttu-id="6f1e4-268">Zināms kā</span><span class="sxs-lookup"><span data-stu-id="6f1e4-268">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="6f1e4-269">Personiskā informācija</span><span class="sxs-lookup"><span data-stu-id="6f1e4-269">Personal information</span></span>

- <span data-ttu-id="6f1e4-270">Ģimenes stāvoklis (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-270">Marital status (required)</span></span>
- <span data-ttu-id="6f1e4-271">Dzimšanas datums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-271">Birth date (required)</span></span>
- <span data-ttu-id="6f1e4-272">Dzimums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-272">Gender (required)</span></span>
- <span data-ttu-id="6f1e4-273">Persona ar īpašām vajadzībām</span><span class="sxs-lookup"><span data-stu-id="6f1e4-273">Person with disabilities</span></span>
- <span data-ttu-id="6f1e4-274">Nacionalitātes valsts/reģions (tikai Meksikai)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-274">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="6f1e4-275">Adreses informācija</span><span class="sxs-lookup"><span data-stu-id="6f1e4-275">Address information</span></span>

- <span data-ttu-id="6f1e4-276">Primārā (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-276">Primary (required)</span></span>
- <span data-ttu-id="6f1e4-277">Valsts/reģions (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-277">Country/region (required)</span></span>
- <span data-ttu-id="6f1e4-278">Pasta indekss (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-278">Postal code (required)</span></span>
- <span data-ttu-id="6f1e4-279">Ielas numurs (obligāti) (tikai Meksikai)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-279">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="6f1e4-280">Mājas numurs/nosaukums (tikai Meksikai)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-280">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="6f1e4-281">Pilsēta (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-281">City (required)</span></span>
- <span data-ttu-id="6f1e4-282">Administratīvais apgabals (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-282">State (required)</span></span>
- <span data-ttu-id="6f1e4-283">Apgabals (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-283">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="6f1e4-284">Kontaktinformācija</span><span class="sxs-lookup"><span data-stu-id="6f1e4-284">Contact information</span></span> 

- <span data-ttu-id="6f1e4-285">Primārā (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-285">Primary (required)</span></span>
- <span data-ttu-id="6f1e4-286">Kontaktpersonas tālrunis (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-286">Contact number (required)</span></span>
- <span data-ttu-id="6f1e4-287">Paplašinājums</span><span class="sxs-lookup"><span data-stu-id="6f1e4-287">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="6f1e4-288">Algas informācija un ienākumu veidu kodi</span><span class="sxs-lookup"><span data-stu-id="6f1e4-288">Payroll information and earning codes</span></span>

<span data-ttu-id="6f1e4-289">Darbiniekiem var būt piešķirti konkrēti ienākumu veidi konkrētajā maksājumu biežumā, kā arī var būt norādīta vēlamā maksāšanas metode.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-289">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="6f1e4-290">Lai palīdzētu nodrošināt, ka šīs preferences un iestatījumi tiek izmantoti, pakalpojumā Dayforce ir tālāk norādītie lauki.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-290">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="6f1e4-291">Ienākumu veida kodi</span><span class="sxs-lookup"><span data-stu-id="6f1e4-291">Earning codes</span></span>

- <span data-ttu-id="6f1e4-292">Amats (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-292">Position (required)</span></span>
- <span data-ttu-id="6f1e4-293">Ienākumu veida kods (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-293">Earning Code (required)</span></span>
- <span data-ttu-id="6f1e4-294">Biežums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-294">Frequency (required)</span></span>
- <span data-ttu-id="6f1e4-295">Summa (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-295">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="6f1e4-296">Algas informācija</span><span class="sxs-lookup"><span data-stu-id="6f1e4-296">Payroll information</span></span>

- <span data-ttu-id="6f1e4-297">Maksāšanas metode</span><span class="sxs-lookup"><span data-stu-id="6f1e4-297">Payment Method</span></span>
- <span data-ttu-id="6f1e4-298">Ekonomiskais reģions (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-298">Economic Region (required)</span></span>
- <span data-ttu-id="6f1e4-299">Darbinieka atvieglojumu ID</span><span class="sxs-lookup"><span data-stu-id="6f1e4-299">Employee Benefits ID</span></span>
- <span data-ttu-id="6f1e4-300">Nacionālais ID numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-300">National ID Number (required)</span></span>
- <span data-ttu-id="6f1e4-301">Karadienesta numurs</span><span class="sxs-lookup"><span data-stu-id="6f1e4-301">Military Service Number</span></span>
- <span data-ttu-id="6f1e4-302">Maiņas ID (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-302">Shift ID (required)</span></span>
- <span data-ttu-id="6f1e4-303">Nodokļu numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-303">Tax Number (required)</span></span>
- <span data-ttu-id="6f1e4-304">Arodbiedrības ID (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-304">Union ID (required)</span></span>
- <span data-ttu-id="6f1e4-305">Darba dienas ID (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-305">Work Day ID (required)</span></span>
- <span data-ttu-id="6f1e4-306">Darba atļaujas numurs</span><span class="sxs-lookup"><span data-stu-id="6f1e4-306">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="6f1e4-307">Meksika atbalsta šādas maksāšanas metodes: **Skaidra nauda**, **Čeks** (uzņēmuma fiziskais čeks) un **Elektroniskais maksājums**.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-307">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="6f1e4-308">Ja nav norādīta neviena maksāšanas metode, pēc noklusējuma tiek izmantota opcija **Čeks**.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-308">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="6f1e4-309">Nodarbinātības papildinformācija</span><span class="sxs-lookup"><span data-stu-id="6f1e4-309">Employment details</span></span>

<span data-ttu-id="6f1e4-310">Nodarbinātības datu vēsture pakalpojumā Dayforce tiek izmantota kā galvenā informācija, no kuras tiek iegūts darbinieka darbā pieņemšanas, darba attiecību izbeigšanas un atkārtotas pieņemšanas darbā statuss.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-310">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="6f1e4-311">Dayforce vienlaikus atbalsta tikai vienu aktīvu nodarbinātības ierakstu.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-311">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="6f1e4-312">Nodarbinātības sākuma datums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-312">Employment start date (required)</span></span>
- <span data-ttu-id="6f1e4-313">Nodarbinātības beigu datums</span><span class="sxs-lookup"><span data-stu-id="6f1e4-313">Employment end date</span></span>
- <span data-ttu-id="6f1e4-314">Pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="6f1e4-314">Start date</span></span>
- <span data-ttu-id="6f1e4-315">Koriģētais pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="6f1e4-315">Adjusted start date</span></span>
- <span data-ttu-id="6f1e4-316">Darba attiecību pārtraukšanas datums (jānorāda, kad tiek pārtrauktas darba attiecības)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-316">Termination date (required upon termination)</span></span>
- <span data-ttu-id="6f1e4-317">Darba attiecību pārtraukšanas iemesls (jānorāda, kad tiek pārtrauktas darba attiecības)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-317">Termination reason (required upon termination)</span></span>

<span data-ttu-id="6f1e4-318">Darbinieka galvenie datumi tiek iegūti, izmantojot tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-318">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="6f1e4-319">Talent</span><span class="sxs-lookup"><span data-stu-id="6f1e4-319">Talent</span></span>                | <span data-ttu-id="6f1e4-320">Dayforce</span><span class="sxs-lookup"><span data-stu-id="6f1e4-320">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f1e4-321">Pēdējais nomas datums</span><span class="sxs-lookup"><span data-stu-id="6f1e4-321">Most recent hire date</span></span> | <span data-ttu-id="6f1e4-322">Pašreizējā nepārtrauktās nodarbinātības vēstures ieraksta nodarbinātības sākums</span><span class="sxs-lookup"><span data-stu-id="6f1e4-322">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="6f1e4-323">Izbeigšanas datums</span><span class="sxs-lookup"><span data-stu-id="6f1e4-323">Termination date</span></span>      | <span data-ttu-id="6f1e4-324">Pašreizējā nepārtrauktās nodarbinātības vēstures ieraksta darba attiecību pārtraukšanas datums</span><span class="sxs-lookup"><span data-stu-id="6f1e4-324">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="6f1e4-325">Pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="6f1e4-325">Start date</span></span>            | <span data-ttu-id="6f1e4-326">Pašreizējā neaktīvā nodarbinātības vēstures ieraksta koriģētais sākuma datums, sākuma datums vai nodarbinātības sākums</span><span class="sxs-lookup"><span data-stu-id="6f1e4-326">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="6f1e4-327">Sākotnējais darbā pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="6f1e4-327">Original hire date</span></span>    | <span data-ttu-id="6f1e4-328">Agrākā nodarbinātības vēstures ieraksta nodarbinātības sākums</span><span class="sxs-lookup"><span data-stu-id="6f1e4-328">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="6f1e4-329">Atlīdzība</span><span class="sxs-lookup"><span data-stu-id="6f1e4-329">Compensation</span></span>

<span data-ttu-id="6f1e4-330">Fiksētās atlīdzības plānam ir jābūt saistītam ar katra darbinieka primāro amatu visā nodarbinātības periodā.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-330">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="6f1e4-331">Šis periods sākas ar datumu, kurā darbinieks tika pieņemts darbā (vai nodarbinātības sākuma datumu), un turpinās līdz darba attiecību pārtraukšanai.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-331">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="6f1e4-332">Spēkā stāšanās datums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-332">Effective Date (required)</span></span>
- <span data-ttu-id="6f1e4-333">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="6f1e4-333">Expiration date</span></span>
- <span data-ttu-id="6f1e4-334">Apmaksas likme (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-334">Pay Rate (required)</span></span>
- <span data-ttu-id="6f1e4-335">Apmaksas likmes konvertēšanas gadījumi (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-335">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="6f1e4-336">Gada ekvivalents (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-336">Annual equivalent (required)</span></span>
- <span data-ttu-id="6f1e4-337">Stundas ekvivalents (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-337">Hourly equivalent (required)</span></span>

<span data-ttu-id="6f1e4-338">Ja darbiniekam ar stundas likmi ir vairāki amati, pakalpojumā Dayforce kā darbinieka līmeņa pamatlikme/alga tiek importēta primārā amata fiksētā atlīdzība.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-338">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="6f1e4-339">To amatu, kas nav primārie, stundas likme tiek saglabāta pakalpojumā Dayforce attiecīgajā amatā.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-339">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="6f1e4-340">Ja darbiniekam, kurš saņem algu, ir vairāki amati, kā darbinieka līmeņa pamatlikme/alga tiek iegūta un izmantota visu aktīvo amatu kopējā stundas likme un gada alga.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-340">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="6f1e4-341">Identifikācijas numuri</span><span class="sxs-lookup"><span data-stu-id="6f1e4-341">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="6f1e4-342">Sociālās apdrošināšanas numurs</span><span class="sxs-lookup"><span data-stu-id="6f1e4-342">Social Security identifier</span></span> 

<span data-ttu-id="6f1e4-343">Katram darbiniekam ir jābūt vienam primārajam numuram.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-343">Every employee must have one primary identifier.</span></span> <span data-ttu-id="6f1e4-344">Šī numura identifikācijas tipam ir jābūt **SAN**.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-344">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="6f1e4-345">Pakalpojumā Dayforce tas tiek automātiski iegūts kā darbinieka sociālās apdrošināšanas numurs, kas ir jānorāda, kad darbinieks tiek pieņemts darbā.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-345">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="6f1e4-346">Primārais (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-346">Primary (required)</span></span>
- <span data-ttu-id="6f1e4-347">Identifikācijas tips = SAN</span><span class="sxs-lookup"><span data-stu-id="6f1e4-347">Identification Type = "SSN"</span></span>
- <span data-ttu-id="6f1e4-348">Izdošanas datums</span><span class="sxs-lookup"><span data-stu-id="6f1e4-348">Issued Date</span></span>
- <span data-ttu-id="6f1e4-349">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="6f1e4-349">Expiration Date</span></span>

<span data-ttu-id="6f1e4-350">Darbinieki var sniegt vairākus identifikācijas numurus, kuru identifikācijas tips ir **SAN**.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-350">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="6f1e4-351">Taču pakalpojumā Dayforce tiek integrēts tikai ieraksts, kas ir atzīmēts kā **Primārais**, neatkarīgi no tā, vai šis numurs ir aktīvs vai tam ir beidzies derīgums.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-351">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="6f1e4-352">Banku konti un izdevumi</span><span class="sxs-lookup"><span data-stu-id="6f1e4-352">Bank accounts and disbursements</span></span>

<span data-ttu-id="6f1e4-353">Jebkuram darbiniekam, kurš samaksu izvēlējies saņemt bankas konta pārskaitījuma veidā, ir jāievada derīga bankas konta informācija.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-353">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="6f1e4-354">Talent</span><span class="sxs-lookup"><span data-stu-id="6f1e4-354">Talent</span></span>                         | <span data-ttu-id="6f1e4-355">Dayforce</span><span class="sxs-lookup"><span data-stu-id="6f1e4-355">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f1e4-356">Bankas konta numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-356">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="6f1e4-357">SWIFT kods (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-357">SWIFT code (required)</span></span>          | <span data-ttu-id="6f1e4-358">Lauku **Bankas ID** izmanto, apstrādājot algas Meksikā.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-358">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="6f1e4-359">Filiāles numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-359">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="6f1e4-360">Bankas konta tips (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-360">Bank account type (required)</span></span>   | <span data-ttu-id="6f1e4-361">Lauku **Konta tips** izmanto, apstrādājot algas Meksikā.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-361">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="6f1e4-362">Atbalstītās vērtības ir, piemēram, **Norēķini** un **Algas**.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-362">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="6f1e4-363">Darbiniekiem, kuri samaksu izvēlas saņemt bankas konta pārskaitījumu veidā, ir jāsniedz saite uz juridiskās personas, kuras primārā adrese ir Meksikā, atlikumu kontu, kas ir saistīts ar derīgu Meksikas bankas kontu.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-363">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="6f1e4-364">Visi pārējie konti, kas nav atlikumu konti, tiek ignorēti.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-364">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="6f1e4-365">Adreses informācija</span><span class="sxs-lookup"><span data-stu-id="6f1e4-365">Address information</span></span>

<span data-ttu-id="6f1e4-366">Katram darbiniekam ir jābūt vienai primārajai vietai.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-366">Every employee must have one primary location.</span></span> <span data-ttu-id="6f1e4-367">Pakalpojumā Dayforce šī vieta tiek izmantota, lai nodokļu piemērošanas nolūkos noteiktu darbinieka primāro dzīvesvietu.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-367">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="6f1e4-368">Primārā (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-368">Primary (required)</span></span>
- <span data-ttu-id="6f1e4-369">Valsts/reģions (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-369">Country/region (required)</span></span>
- <span data-ttu-id="6f1e4-370">Pasta indekss (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-370">Zip/postal code (required)</span></span>
- <span data-ttu-id="6f1e4-371">Iela (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-371">Street (required)</span></span>
- <span data-ttu-id="6f1e4-372">Ielas numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-372">Street Number (required)</span></span>
- <span data-ttu-id="6f1e4-373">Mājas numurs/nosaukums</span><span class="sxs-lookup"><span data-stu-id="6f1e4-373">Building Complement</span></span>
- <span data-ttu-id="6f1e4-374">Pilsēta (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-374">City (required)</span></span>
- <span data-ttu-id="6f1e4-375">Administratīvais apgabals (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-375">State (required)</span></span>
- <span data-ttu-id="6f1e4-376">Apgabals (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-376">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="6f1e4-377">Datu konfigurēšana algu ģenerēšanai Amerikas Savienotajās Valstīs un Kanādā</span><span class="sxs-lookup"><span data-stu-id="6f1e4-377">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="6f1e4-378">Ja ģenerējat algas darbiniekiem Amerikas Savienotajās Valstīs un Kanādā, ir jākonfigurē tālāk norādītie elementi.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-378">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="6f1e4-379">Amatiem ir jānorāda nodaļas.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-379">Departments are required on positions.</span></span>
- <span data-ttu-id="6f1e4-380">Izmaksu centri ir jāiestata kā finanšu dimensijas, un tiem ir jābūt pirmajiem elementiem noklusējuma finanšu dimensijas virknē.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-380">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="6f1e4-381">Varat konfigurēt Talent, lai amatiem būtu jānorāda nodaļa.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-381">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="6f1e4-382">Lai to izdarītu, pārejiet uz **Personāla vadības kopīgotie amati > Amati > Pieprasīt amatiem nodaļas**.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-382">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="6f1e4-383">Ieteicams piemērot šo iestatījumu integrācijai.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-383">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="6f1e4-384">Darba tipi</span><span class="sxs-lookup"><span data-stu-id="6f1e4-384">Job types</span></span>

<span data-ttu-id="6f1e4-385">Darbu veidi tiek izmantoti, lai līdzīgus darbus grupētu kategorijās.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-385">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="6f1e4-386">Darbu veidi ir nepieciešami, lai apstrādātu algas Amerikas Savienotajās Valstīs un Kanādā.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-386">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="6f1e4-387">Daži darbu veidu piemēri ir pilna laika, nepilna laika, algots un stundu apmaksas darbs.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-387">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="6f1e4-388">Darbu veidi tiek kartēti uz pakalpojumu Dayforce kā apmaksas tipi, lai norādītu, vai darbinieks saņem stundas samaksu vai algu.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-388">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="6f1e4-389">Ir jānorāda tālāk norādītie darbu veidi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-389">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="6f1e4-390">Darba veids</span><span class="sxs-lookup"><span data-stu-id="6f1e4-390">Job type</span></span>   | <span data-ttu-id="6f1e4-391">apraksts</span><span class="sxs-lookup"><span data-stu-id="6f1e4-391">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="6f1e4-392">Ik stundu</span><span class="sxs-lookup"><span data-stu-id="6f1e4-392">Hourly</span></span>     | <span data-ttu-id="6f1e4-393">Ik stundu</span><span class="sxs-lookup"><span data-stu-id="6f1e4-393">Hourly</span></span>      |
| <span data-ttu-id="6f1e4-394">Algots</span><span class="sxs-lookup"><span data-stu-id="6f1e4-394">Salaried</span></span>   | <span data-ttu-id="6f1e4-395">Algots</span><span class="sxs-lookup"><span data-stu-id="6f1e4-395">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="6f1e4-396">Amatu veidi</span><span class="sxs-lookup"><span data-stu-id="6f1e4-396">Position types</span></span> 

<span data-ttu-id="6f1e4-397">Amatu veidus izmanto, lai norādītu, vai amats ir pilna laika, nepilna laika vai cita veida darbs.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-397">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="6f1e4-398">Amatu veidi tiek kartēti uz pakalpojumu Dayforce kā apmaksas klases, lai norādītu, vai darbinieks ir pilna laika vai nepilna laika darbinieks.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-398">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="6f1e4-399">Ir jānorāda tālāk norādītie amatu veidi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-399">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="6f1e4-400">Amata tips</span><span class="sxs-lookup"><span data-stu-id="6f1e4-400">Position type</span></span>   | <span data-ttu-id="6f1e4-401">apraksts</span><span class="sxs-lookup"><span data-stu-id="6f1e4-401">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="6f1e4-402">Pilna laika</span><span class="sxs-lookup"><span data-stu-id="6f1e4-402">Full-time</span></span>       | <span data-ttu-id="6f1e4-403">Pilna laika darbinieks</span><span class="sxs-lookup"><span data-stu-id="6f1e4-403">Full time employee</span></span> |
| <span data-ttu-id="6f1e4-404">Nepilna laika</span><span class="sxs-lookup"><span data-stu-id="6f1e4-404">Part-time</span></span>       | <span data-ttu-id="6f1e4-405">Nepilna laika darbinieks</span><span class="sxs-lookup"><span data-stu-id="6f1e4-405">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="6f1e4-406">Iemeslu kodi</span><span class="sxs-lookup"><span data-stu-id="6f1e4-406">Reason codes</span></span>

<span data-ttu-id="6f1e4-407">Iemeslu kodi sniedz informāciju par darbinieka statusu.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-407">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="6f1e4-408">Iemeslu kodu tiek kartēti uz pakalpojumu Dayforce kā statusa iemesli, kas norāda darbinieka amata vai nodarbinātības statusa izmaiņu iemeslu.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-408">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="6f1e4-409">Ir jānorāda tālāk norādītie iemeslu kodi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-409">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="6f1e4-410">Iemeslu kodi</span><span class="sxs-lookup"><span data-stu-id="6f1e4-410">Reason code</span></span>    | <span data-ttu-id="6f1e4-411">apraksts</span><span class="sxs-lookup"><span data-stu-id="6f1e4-411">Description</span></span>      | <span data-ttu-id="6f1e4-412">Piemērojamie scenāriji</span><span class="sxs-lookup"><span data-stu-id="6f1e4-412">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="6f1e4-413">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="6f1e4-413">RESIGNATION</span></span>    | <span data-ttu-id="6f1e4-414">Atlūgums</span><span class="sxs-lookup"><span data-stu-id="6f1e4-414">Resignation</span></span>      | <span data-ttu-id="6f1e4-415">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="6f1e4-415">Terminate worker</span></span>     |
| <span data-ttu-id="6f1e4-416">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="6f1e4-416">TERMINATION</span></span>    | <span data-ttu-id="6f1e4-417">Izbeigšana</span><span class="sxs-lookup"><span data-stu-id="6f1e4-417">Termination</span></span>      | <span data-ttu-id="6f1e4-418">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="6f1e4-418">Terminate worker</span></span>     |
| <span data-ttu-id="6f1e4-419">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="6f1e4-419">RETIREMENT</span></span>     | <span data-ttu-id="6f1e4-420">Aiziešana pensijā</span><span class="sxs-lookup"><span data-stu-id="6f1e4-420">Retirement</span></span>       | <span data-ttu-id="6f1e4-421">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="6f1e4-421">Terminate worker</span></span>     |
| <span data-ttu-id="6f1e4-422">CITI</span><span class="sxs-lookup"><span data-stu-id="6f1e4-422">OTHER</span></span>          | <span data-ttu-id="6f1e4-423">Citi iemesli</span><span class="sxs-lookup"><span data-stu-id="6f1e4-423">Other Reasons</span></span>    | <span data-ttu-id="6f1e4-424">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="6f1e4-424">Terminate worker</span></span>     |
| <span data-ttu-id="6f1e4-425">DEATH</span><span class="sxs-lookup"><span data-stu-id="6f1e4-425">DEATH</span></span>          | <span data-ttu-id="6f1e4-426">Nāve</span><span class="sxs-lookup"><span data-stu-id="6f1e4-426">Death</span></span>            | <span data-ttu-id="6f1e4-427">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="6f1e4-427">Terminate worker</span></span>     |
| <span data-ttu-id="6f1e4-428">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="6f1e4-428">LEAVEOFABSENCE</span></span> | <span data-ttu-id="6f1e4-429">Atvaļinājums</span><span class="sxs-lookup"><span data-stu-id="6f1e4-429">Leave of Absence</span></span> | <span data-ttu-id="6f1e4-430">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="6f1e4-430">Terminate worker</span></span>     |
| <span data-ttu-id="6f1e4-431">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="6f1e4-431">CONTRACTEND</span></span>    | <span data-ttu-id="6f1e4-432">Līguma beigas</span><span class="sxs-lookup"><span data-stu-id="6f1e4-432">End of Contract</span></span>  | <span data-ttu-id="6f1e4-433">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="6f1e4-433">Terminate worker</span></span>     |
| <span data-ttu-id="6f1e4-434">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="6f1e4-434">SALARYCHANGE</span></span>   | <span data-ttu-id="6f1e4-435">Algas izmaiņas</span><span class="sxs-lookup"><span data-stu-id="6f1e4-435">Change of Salary</span></span> | <span data-ttu-id="6f1e4-436">Atlīdzība</span><span class="sxs-lookup"><span data-stu-id="6f1e4-436">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="6f1e4-437">Ģimenes stāvoklis</span><span class="sxs-lookup"><span data-stu-id="6f1e4-437">Marital status</span></span>

<span data-ttu-id="6f1e4-438">Ģimenes statusa vērtības tiek kartētas uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkotas uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-438">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="6f1e4-439">Tālāk esošajā tabulā ir parādīts, kā ģimenes statusa vērtības tiek kartētas uz pakalpojumu Dayforce.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-439">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="6f1e4-440">Talent</span><span class="sxs-lookup"><span data-stu-id="6f1e4-440">Talent</span></span>                 | <span data-ttu-id="6f1e4-441">Dayforce</span><span class="sxs-lookup"><span data-stu-id="6f1e4-441">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="6f1e4-442">Precējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-442">Married</span></span>                | <span data-ttu-id="6f1e4-443">Precējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-443">Married</span></span>              |
| <span data-ttu-id="6f1e4-444">Neprecējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-444">Single</span></span>                 | <span data-ttu-id="6f1e4-445">Neprecējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-445">Single</span></span>               |
| <span data-ttu-id="6f1e4-446">Atraitnis</span><span class="sxs-lookup"><span data-stu-id="6f1e4-446">Widowed</span></span>                | <span data-ttu-id="6f1e4-447">Atraitnis</span><span class="sxs-lookup"><span data-stu-id="6f1e4-447">Widowed</span></span>              |
| <span data-ttu-id="6f1e4-448">Šķīries (-usies)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-448">Divorced</span></span>               | <span data-ttu-id="6f1e4-449">Šķīries (-usies)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-449">Divorced</span></span>             |
| <span data-ttu-id="6f1e4-450">Reģistrētas attiecības</span><span class="sxs-lookup"><span data-stu-id="6f1e4-450">Registered Partnership</span></span> | <span data-ttu-id="6f1e4-451">Dzīvesbiedrs</span><span class="sxs-lookup"><span data-stu-id="6f1e4-451">Domestic Partnership</span></span> |
| <span data-ttu-id="6f1e4-452">Neviens</span><span class="sxs-lookup"><span data-stu-id="6f1e4-452">None</span></span>                   | <span data-ttu-id="6f1e4-453">Neviens</span><span class="sxs-lookup"><span data-stu-id="6f1e4-453">None</span></span>                 |
| <span data-ttu-id="6f1e4-454">Kopdzīve</span><span class="sxs-lookup"><span data-stu-id="6f1e4-454">Cohabiting</span></span>             | <span data-ttu-id="6f1e4-455">Kopdzīve</span><span class="sxs-lookup"><span data-stu-id="6f1e4-455">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="6f1e4-456">Dzimums</span><span class="sxs-lookup"><span data-stu-id="6f1e4-456">Gender</span></span>

<span data-ttu-id="6f1e4-457">Dzimuma apzīmējumi tiek kartēti uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkoti uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-457">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="6f1e4-458">Tālāk esošajā tabulā ir parādīts, kā dzimuma apzīmējumi tiek kartēti uz pakalpojumu Dayforce.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-458">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="6f1e4-459">Talent</span><span class="sxs-lookup"><span data-stu-id="6f1e4-459">Talent</span></span>       | <span data-ttu-id="6f1e4-460">Dayforce</span><span class="sxs-lookup"><span data-stu-id="6f1e4-460">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="6f1e4-461">Vīrietis</span><span class="sxs-lookup"><span data-stu-id="6f1e4-461">Male</span></span>         | <span data-ttu-id="6f1e4-462">Vīrietis</span><span class="sxs-lookup"><span data-stu-id="6f1e4-462">Male</span></span>            |
| <span data-ttu-id="6f1e4-463">Sieviete</span><span class="sxs-lookup"><span data-stu-id="6f1e4-463">Female</span></span>       | <span data-ttu-id="6f1e4-464">Sieviete</span><span class="sxs-lookup"><span data-stu-id="6f1e4-464">Female</span></span>          |
| <span data-ttu-id="6f1e4-465">Nav specifisks</span><span class="sxs-lookup"><span data-stu-id="6f1e4-465">Non-specific</span></span> | <span data-ttu-id="6f1e4-466">*Netiek atbalstīts*</span><span class="sxs-lookup"><span data-stu-id="6f1e4-466">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="6f1e4-467">Ienākumu veida kodi</span><span class="sxs-lookup"><span data-stu-id="6f1e4-467">Earning codes</span></span>

<span data-ttu-id="6f1e4-468">Ienākumu veidu kodi unikāli identificē katra veida ienākumus, ko saņem nodarbinātie.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-468">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="6f1e4-469">Kodiem ir vairāki ar ienākumiem saistīti parametri, piemēram, uzskaites nosacījumi, nodokļu likumi, pārskatu veidošanas prasības un bruto summas palielināšanas iespēja.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-469">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="6f1e4-470">Ja tiek izmantota neatbalstīta biežuma vērtība, aprēķinā pēc noklusējuma tiek lietota biežuma vērtība **Katra apmaksa**.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-470">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="6f1e4-471">Atbalstītās biežuma vērtības</span><span class="sxs-lookup"><span data-stu-id="6f1e4-471">Supported frequencies</span></span>

- <span data-ttu-id="6f1e4-472">Visus</span><span class="sxs-lookup"><span data-stu-id="6f1e4-472">All</span></span>
- <span data-ttu-id="6f1e4-473">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="6f1e4-473">EVERYPAY</span></span>
- <span data-ttu-id="6f1e4-474">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="6f1e4-474">EACHPAYPERIOD</span></span>
- <span data-ttu-id="6f1e4-475">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="6f1e4-475">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="6f1e4-476">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="6f1e4-476">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="6f1e4-477">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="6f1e4-477">1OFMTH</span></span>
- <span data-ttu-id="6f1e4-478">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="6f1e4-478">LASTOFMTH</span></span>
- <span data-ttu-id="6f1e4-479">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="6f1e4-479">2OFMTH</span></span>
- <span data-ttu-id="6f1e4-480">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="6f1e4-480">3OFMTH</span></span>
- <span data-ttu-id="6f1e4-481">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6f1e4-481">4OFMTH</span></span>
- <span data-ttu-id="6f1e4-482">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="6f1e4-482">5OFMTH</span></span>
- <span data-ttu-id="6f1e4-483">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="6f1e4-483">1N2OFMTH</span></span>
- <span data-ttu-id="6f1e4-484">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6f1e4-484">3N4OFMTH</span></span>
- <span data-ttu-id="6f1e4-485">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="6f1e4-485">1N3OFMTH</span></span>
- <span data-ttu-id="6f1e4-486">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6f1e4-486">1N4OFMTH</span></span>
- <span data-ttu-id="6f1e4-487">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="6f1e4-487">2N3OFMTH</span></span>
- <span data-ttu-id="6f1e4-488">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6f1e4-488">2N4OFMTH</span></span>
- <span data-ttu-id="6f1e4-489">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="6f1e4-489">1N2N3OFMTH</span></span>
- <span data-ttu-id="6f1e4-490">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6f1e4-490">1N2N4OFMTH</span></span>
- <span data-ttu-id="6f1e4-491">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6f1e4-491">1N3N4OFMTH</span></span>
- <span data-ttu-id="6f1e4-492">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6f1e4-492">2N3N4OFMTH</span></span>
- <span data-ttu-id="6f1e4-493">1N2N3N4OFMTH–1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6f1e4-493">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="6f1e4-494">2N3N4N5OFMth–2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="6f1e4-494">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="6f1e4-495">1OFQTR–1OFQTR</span><span class="sxs-lookup"><span data-stu-id="6f1e4-495">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="6f1e4-496">LASTOFQTR–LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="6f1e4-496">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="6f1e4-497">LASTMTHOFQTR–LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="6f1e4-497">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="6f1e4-498">1OFYEAR–1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="6f1e4-498">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="6f1e4-499">LASTOFYEAR–LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="6f1e4-499">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="6f1e4-500">NOVNDECOFYEAR–NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="6f1e4-500">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="6f1e4-501">Adreses</span><span class="sxs-lookup"><span data-stu-id="6f1e4-501">Addresses</span></span>

<span data-ttu-id="6f1e4-502">Noteiktas valsts vai reģiona, administratīvā apgabala un apgabala (pašvaldības) kodu identifikācijai ir nepieciešami konkrēti formāti, ko var atpazīt pakalpojums Dayforce un valsts/reģiona pakalpojumu sniedzēji.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-502">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="6f1e4-503">Lai gan pilsētu formāts var būt dažāds, katrai pilsētai ir jābūt saistītai ar administratīvo apgabalu.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-503">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="6f1e4-504">Talent</span><span class="sxs-lookup"><span data-stu-id="6f1e4-504">Talent</span></span>          | <span data-ttu-id="6f1e4-505">Dayforce</span><span class="sxs-lookup"><span data-stu-id="6f1e4-505">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="6f1e4-506">Valsts/reģions</span><span class="sxs-lookup"><span data-stu-id="6f1e4-506">Country/Region</span></span>  | <span data-ttu-id="6f1e4-507">Valsts kods</span><span class="sxs-lookup"><span data-stu-id="6f1e4-507">Country Code</span></span>          |
| <span data-ttu-id="6f1e4-508">Pasta indekss</span><span class="sxs-lookup"><span data-stu-id="6f1e4-508">Zip/Postal Code</span></span> | <span data-ttu-id="6f1e4-509">Pasta indekss</span><span class="sxs-lookup"><span data-stu-id="6f1e4-509">Postal Code</span></span>           |
| <span data-ttu-id="6f1e4-510">Administratīvais apgabals</span><span class="sxs-lookup"><span data-stu-id="6f1e4-510">State</span></span>           | <span data-ttu-id="6f1e4-511">Administratīvā apgabala kods</span><span class="sxs-lookup"><span data-stu-id="6f1e4-511">State Code</span></span>            |
| <span data-ttu-id="6f1e4-512">Pilsēta</span><span class="sxs-lookup"><span data-stu-id="6f1e4-512">City</span></span>            | <span data-ttu-id="6f1e4-513">Pilsēta</span><span class="sxs-lookup"><span data-stu-id="6f1e4-513">City</span></span>                  |
| <span data-ttu-id="6f1e4-514">Apgabals</span><span class="sxs-lookup"><span data-stu-id="6f1e4-514">County</span></span>          | <span data-ttu-id="6f1e4-515">Apgabals (pašvaldība)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-515">County (Municipality)</span></span> |
| <span data-ttu-id="6f1e4-516">Iela</span><span class="sxs-lookup"><span data-stu-id="6f1e4-516">Street</span></span>          | <span data-ttu-id="6f1e4-517">Adreses 1. rinda</span><span class="sxs-lookup"><span data-stu-id="6f1e4-517">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="6f1e4-518">Nodokļu reģioni</span><span class="sxs-lookup"><span data-stu-id="6f1e4-518">Tax regions</span></span>

<span data-ttu-id="6f1e4-519">Nodokļu reģionus izmanto, lai noteiktu atbilstošos nodokļus, kas jāpiemēro, ģenerējot algu aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-519">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="6f1e4-520">Nodokļu reģioni tiek kartēti uz pakalpojumu Dayforce kā vietas adreses.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-520">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="6f1e4-521">Noklusējuma nodokļu reģionam ir jābūt saistītam ar nodarbinātā aktīvo amatu.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-521">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="6f1e4-522">Nodokļu reģions (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-522">Tax region (required)</span></span>
- <span data-ttu-id="6f1e4-523">Valsts/reģions (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-523">Country/Region (required)</span></span>
- <span data-ttu-id="6f1e4-524">Administratīvais apgabals (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-524">State (required)</span></span>
- <span data-ttu-id="6f1e4-525">Apgabals</span><span class="sxs-lookup"><span data-stu-id="6f1e4-525">County</span></span> 
- <span data-ttu-id="6f1e4-526">Pilsēta (obligāti)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-526">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="6f1e4-527">Datu konfigurēšana algu aprēķina ģenerēšanai Meksikā</span><span class="sxs-lookup"><span data-stu-id="6f1e4-527">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="6f1e4-528">Ja ģenerējat algas darbiniekiem Meksikā, ir jākonfigurē tālāk norādītie elementi.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-528">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="6f1e4-529">Amatiem ir jānorāda nodaļas.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-529">Departments are required on positions.</span></span>
- <span data-ttu-id="6f1e4-530">Izmaksu centri ir jāiestata kā finanšu dimensijas, un tiem ir jābūt pirmajiem elementiem noklusējuma finanšu dimensijas virknē.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-530">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="6f1e4-531">Darba tipi</span><span class="sxs-lookup"><span data-stu-id="6f1e4-531">Job types</span></span>

<span data-ttu-id="6f1e4-532">Darbu veidi tiek izmantoti, lai līdzīgus darbus grupētu kategorijās.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-532">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="6f1e4-533">Lai apstrādātu algas Meksikā, ir nepieciešami darbu veidi.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-533">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="6f1e4-534">Daži darbu veidu piemēri ir pilna laika, nepilna laika, algots un stundu apmaksas darbs.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-534">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="6f1e4-535">Darbu veidi tiek kartēti uz pakalpojumu Dayforce kā apmaksas tipi, lai norādītu, vai darbinieks saņem stundas samaksu vai algu.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-535">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="6f1e4-536">Ir jānorāda tālāk norādītie darbu veidi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-536">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="6f1e4-537">Darba veids</span><span class="sxs-lookup"><span data-stu-id="6f1e4-537">Job type</span></span>   | <span data-ttu-id="6f1e4-538">apraksts</span><span class="sxs-lookup"><span data-stu-id="6f1e4-538">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="6f1e4-539">Ik stundu</span><span class="sxs-lookup"><span data-stu-id="6f1e4-539">Hourly</span></span>     | <span data-ttu-id="6f1e4-540">Stundu (MX)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-540">MX Hourly</span></span>   |
| <span data-ttu-id="6f1e4-541">Algots</span><span class="sxs-lookup"><span data-stu-id="6f1e4-541">Salaried</span></span>   | <span data-ttu-id="6f1e4-542">Algots (MX)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-542">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="6f1e4-543">Amatu veidi</span><span class="sxs-lookup"><span data-stu-id="6f1e4-543">Position types</span></span> 

<span data-ttu-id="6f1e4-544">Amatu veidus izmanto, lai norādītu, vai amats ir pilna laika, nepilna laika vai cita veida darbs.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-544">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="6f1e4-545">Amatu veidi tiek kartēti uz pakalpojumu Dayforce kā apmaksas klases, lai norādītu, vai darbinieks ir pilna laika vai nepilna laika darbinieks.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-545">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="6f1e4-546">Ir jānorāda tālāk norādītie amatu veidi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-546">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="6f1e4-547">Amata tips</span><span class="sxs-lookup"><span data-stu-id="6f1e4-547">Position type</span></span>   | <span data-ttu-id="6f1e4-548">apraksts</span><span class="sxs-lookup"><span data-stu-id="6f1e4-548">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="6f1e4-549">Pilna laika</span><span class="sxs-lookup"><span data-stu-id="6f1e4-549">Full-time</span></span>       | <span data-ttu-id="6f1e4-550">Pilna laika darbinieks</span><span class="sxs-lookup"><span data-stu-id="6f1e4-550">Full time employee</span></span> |
| <span data-ttu-id="6f1e4-551">Nepilna laika</span><span class="sxs-lookup"><span data-stu-id="6f1e4-551">Part-time</span></span>       | <span data-ttu-id="6f1e4-552">Nepilna laika darbinieks</span><span class="sxs-lookup"><span data-stu-id="6f1e4-552">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="6f1e4-553">Iemeslu kodi</span><span class="sxs-lookup"><span data-stu-id="6f1e4-553">Reason codes</span></span>

<span data-ttu-id="6f1e4-554">Iemeslu kodi sniedz informāciju par darbinieka statusu.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-554">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="6f1e4-555">Iemeslu kodu tiek kartēti uz pakalpojumu Dayforce kā statusa iemesli, kas norāda darbinieka amata vai nodarbinātības statusa izmaiņu iemeslu.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-555">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="6f1e4-556">Ir jānorāda tālāk norādītie iemeslu kodi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-556">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="6f1e4-557">Iemeslu kodi</span><span class="sxs-lookup"><span data-stu-id="6f1e4-557">Reason code</span></span>            | <span data-ttu-id="6f1e4-558">apraksts</span><span class="sxs-lookup"><span data-stu-id="6f1e4-558">Description</span></span>                    | <span data-ttu-id="6f1e4-559">Piemērojamie scenāriji</span><span class="sxs-lookup"><span data-stu-id="6f1e4-559">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="6f1e4-560">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="6f1e4-560">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="6f1e4-561">Aiziešana no amata pirms pirmās algas</span><span class="sxs-lookup"><span data-stu-id="6f1e4-561">Departure before first payroll</span></span> | <span data-ttu-id="6f1e4-562">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="6f1e4-562">Terminate worker</span></span>     |
| <span data-ttu-id="6f1e4-563">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="6f1e4-563">RESIGNATION</span></span>            | <span data-ttu-id="6f1e4-564">Atlūgums</span><span class="sxs-lookup"><span data-stu-id="6f1e4-564">Resignation</span></span>                    | <span data-ttu-id="6f1e4-565">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="6f1e4-565">Terminate worker</span></span>     |
| <span data-ttu-id="6f1e4-566">PENSION</span><span class="sxs-lookup"><span data-stu-id="6f1e4-566">PENSION</span></span>                | <span data-ttu-id="6f1e4-567">Pensija</span><span class="sxs-lookup"><span data-stu-id="6f1e4-567">Pension</span></span>                        | <span data-ttu-id="6f1e4-568">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="6f1e4-568">Terminate worker</span></span>     |
| <span data-ttu-id="6f1e4-569">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="6f1e4-569">TERMINATION</span></span>            | <span data-ttu-id="6f1e4-570">Izbeigšana</span><span class="sxs-lookup"><span data-stu-id="6f1e4-570">Termination</span></span>                    | <span data-ttu-id="6f1e4-571">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="6f1e4-571">Terminate worker</span></span>     |
| <span data-ttu-id="6f1e4-572">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="6f1e4-572">RETIREMENT</span></span>             | <span data-ttu-id="6f1e4-573">Aiziešana pensijā</span><span class="sxs-lookup"><span data-stu-id="6f1e4-573">Retirement</span></span>                     | <span data-ttu-id="6f1e4-574">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="6f1e4-574">Terminate worker</span></span>     |
| <span data-ttu-id="6f1e4-575">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="6f1e4-575">ABSENTEE</span></span>               | <span data-ttu-id="6f1e4-576">Darba kavētājs</span><span class="sxs-lookup"><span data-stu-id="6f1e4-576">Absentee</span></span>                       | <span data-ttu-id="6f1e4-577">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="6f1e4-577">Terminate worker</span></span>     |
| <span data-ttu-id="6f1e4-578">CITI</span><span class="sxs-lookup"><span data-stu-id="6f1e4-578">OTHER</span></span>                  | <span data-ttu-id="6f1e4-579">Citi iemesli</span><span class="sxs-lookup"><span data-stu-id="6f1e4-579">Other Reasons</span></span>                  | <span data-ttu-id="6f1e4-580">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="6f1e4-580">Terminate worker</span></span>     |
| <span data-ttu-id="6f1e4-581">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="6f1e4-581">CLOSURE</span></span>                | <span data-ttu-id="6f1e4-582">Uzņēmuma slēgšana</span><span class="sxs-lookup"><span data-stu-id="6f1e4-582">Business Closure</span></span>               | <span data-ttu-id="6f1e4-583">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="6f1e4-583">Terminate worker</span></span>     |
| <span data-ttu-id="6f1e4-584">DEATH</span><span class="sxs-lookup"><span data-stu-id="6f1e4-584">DEATH</span></span>                  | <span data-ttu-id="6f1e4-585">Nāve</span><span class="sxs-lookup"><span data-stu-id="6f1e4-585">Death</span></span>                          | <span data-ttu-id="6f1e4-586">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="6f1e4-586">Terminate worker</span></span>     |
| <span data-ttu-id="6f1e4-587">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="6f1e4-587">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="6f1e4-588">Atvaļinājums</span><span class="sxs-lookup"><span data-stu-id="6f1e4-588">Leave of Absence</span></span>               | <span data-ttu-id="6f1e4-589">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="6f1e4-589">Terminate worker</span></span>     |
| <span data-ttu-id="6f1e4-590">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="6f1e4-590">CONTRACTEND</span></span>            | <span data-ttu-id="6f1e4-591">Līguma beigas</span><span class="sxs-lookup"><span data-stu-id="6f1e4-591">End of Contract</span></span>                | <span data-ttu-id="6f1e4-592">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="6f1e4-592">Terminate worker</span></span>     |
| <span data-ttu-id="6f1e4-593">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="6f1e4-593">SALARYCHANGE</span></span>           | <span data-ttu-id="6f1e4-594">Algas izmaiņas</span><span class="sxs-lookup"><span data-stu-id="6f1e4-594">Change of Salary</span></span>               | <span data-ttu-id="6f1e4-595">Atlīdzība</span><span class="sxs-lookup"><span data-stu-id="6f1e4-595">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="6f1e4-596">Nodarbinātības noteikumi</span><span class="sxs-lookup"><span data-stu-id="6f1e4-596">Terms of employment</span></span>

<span data-ttu-id="6f1e4-597">Nodarbinātības noteikumus izmanto, lai izveidotu nodarbinātības noteikumu kategorijas.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-597">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="6f1e4-598">Noteikumi tiek kartēti uz pakalpojumu Dayforce kā nodarbinātības rādītāju vērtības.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-598">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="6f1e4-599">Ir nepieciešami tālāk norādītie nodarbinātības noteikumi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-599">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="6f1e4-600">Nodarbinātības noteikumi</span><span class="sxs-lookup"><span data-stu-id="6f1e4-600">Terms of employment</span></span>   | <span data-ttu-id="6f1e4-601">apraksts</span><span class="sxs-lookup"><span data-stu-id="6f1e4-601">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="6f1e4-602">Regulārs</span><span class="sxs-lookup"><span data-stu-id="6f1e4-602">Regular</span></span>               | <span data-ttu-id="6f1e4-603">Regulārs</span><span class="sxs-lookup"><span data-stu-id="6f1e4-603">Regular</span></span>     |
| <span data-ttu-id="6f1e4-604">Tieši</span><span class="sxs-lookup"><span data-stu-id="6f1e4-604">Direct</span></span>                | <span data-ttu-id="6f1e4-605">Tieši</span><span class="sxs-lookup"><span data-stu-id="6f1e4-605">Direct</span></span>      |
| <span data-ttu-id="6f1e4-606">Štažēšanās</span><span class="sxs-lookup"><span data-stu-id="6f1e4-606">Internship</span></span>            | <span data-ttu-id="6f1e4-607">Štažēšanās</span><span class="sxs-lookup"><span data-stu-id="6f1e4-607">Internship</span></span>  |
| <span data-ttu-id="6f1e4-608">Pastāvīga</span><span class="sxs-lookup"><span data-stu-id="6f1e4-608">Permanent</span></span>             | <span data-ttu-id="6f1e4-609">Pastāvīga</span><span class="sxs-lookup"><span data-stu-id="6f1e4-609">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="6f1e4-610">Ģimenes stāvoklis</span><span class="sxs-lookup"><span data-stu-id="6f1e4-610">Marital status</span></span>

<span data-ttu-id="6f1e4-611">Ģimenes statusa vērtības tiek kartētas uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkotas uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-611">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="6f1e4-612">Tālāk esošajā tabulā ir parādīts, kā ģimenes statusa vērtības tiek kartētas uz pakalpojumu Dayforce.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-612">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="6f1e4-613">Talent</span><span class="sxs-lookup"><span data-stu-id="6f1e4-613">Talent</span></span>                 | <span data-ttu-id="6f1e4-614">Dayforce</span><span class="sxs-lookup"><span data-stu-id="6f1e4-614">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="6f1e4-615">Precējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-615">Married</span></span>                | <span data-ttu-id="6f1e4-616">Precējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-616">Married</span></span>                   |
| <span data-ttu-id="6f1e4-617">Neprecējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-617">Single</span></span>                 | <span data-ttu-id="6f1e4-618">Neprecējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-618">Single</span></span>                    |
| <span data-ttu-id="6f1e4-619">Atraitnis</span><span class="sxs-lookup"><span data-stu-id="6f1e4-619">Widowed</span></span>                | <span data-ttu-id="6f1e4-620">Atraitnis</span><span class="sxs-lookup"><span data-stu-id="6f1e4-620">Widowed</span></span>                   |
| <span data-ttu-id="6f1e4-621">Šķīries (-usies)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-621">Divorced</span></span>               | <span data-ttu-id="6f1e4-622">Šķīries (-usies)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-622">Divorced</span></span>                  |
| <span data-ttu-id="6f1e4-623">Reģistrētas attiecības</span><span class="sxs-lookup"><span data-stu-id="6f1e4-623">Registered Partnership</span></span> | <span data-ttu-id="6f1e4-624">Dzīvesbiedrs</span><span class="sxs-lookup"><span data-stu-id="6f1e4-624">Domestic Partnership</span></span>      |
| <span data-ttu-id="6f1e4-625">Neviens</span><span class="sxs-lookup"><span data-stu-id="6f1e4-625">None</span></span>                   | <span data-ttu-id="6f1e4-626">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="6f1e4-626">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="6f1e4-627">Kopdzīve</span><span class="sxs-lookup"><span data-stu-id="6f1e4-627">Cohabiting</span></span>             | <span data-ttu-id="6f1e4-628">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="6f1e4-628">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="6f1e4-629">Dzimums</span><span class="sxs-lookup"><span data-stu-id="6f1e4-629">Gender</span></span>

<span data-ttu-id="6f1e4-630">Dzimuma apzīmējumi tiek kartēti uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkoti uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-630">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="6f1e4-631">Tālāk esošajā tabulā ir parādīts, kā dzimuma apzīmējumi tiek kartēti uz pakalpojumu Dayforce.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-631">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="6f1e4-632">Talent</span><span class="sxs-lookup"><span data-stu-id="6f1e4-632">Talent</span></span>       | <span data-ttu-id="6f1e4-633">Dayforce</span><span class="sxs-lookup"><span data-stu-id="6f1e4-633">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="6f1e4-634">Vīrietis</span><span class="sxs-lookup"><span data-stu-id="6f1e4-634">Male</span></span>         | <span data-ttu-id="6f1e4-635">Vīrietis</span><span class="sxs-lookup"><span data-stu-id="6f1e4-635">Male</span></span>                      |
| <span data-ttu-id="6f1e4-636">Sieviete</span><span class="sxs-lookup"><span data-stu-id="6f1e4-636">Female</span></span>       | <span data-ttu-id="6f1e4-637">Sieviete</span><span class="sxs-lookup"><span data-stu-id="6f1e4-637">Female</span></span>                    |
| <span data-ttu-id="6f1e4-638">Nav specifisks</span><span class="sxs-lookup"><span data-stu-id="6f1e4-638">Non-specific</span></span> | <span data-ttu-id="6f1e4-639">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="6f1e4-639">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="6f1e4-640">Maksājumu metode</span><span class="sxs-lookup"><span data-stu-id="6f1e4-640">Payment method</span></span>

<span data-ttu-id="6f1e4-641">Maksāšanas metodes darbiniekam un uzņēmumam ļauj aprakstīt, kā darbinieki saņems samaksu.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-641">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="6f1e4-642">Maksāšanas metodes tiek kartētas uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkotas uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-642">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="6f1e4-643">Tālāk esošajā tabulā ir parādīts, kā maksāšanas metodes tiek kartētas uz pakalpojumu Dayforce.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-643">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="6f1e4-644">Talent</span><span class="sxs-lookup"><span data-stu-id="6f1e4-644">Talent</span></span>             | <span data-ttu-id="6f1e4-645">Dayforce</span><span class="sxs-lookup"><span data-stu-id="6f1e4-645">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="6f1e4-646">Kase</span><span class="sxs-lookup"><span data-stu-id="6f1e4-646">Cash</span></span>               | <span data-ttu-id="6f1e4-647">Kase</span><span class="sxs-lookup"><span data-stu-id="6f1e4-647">Cash</span></span>                      |
| <span data-ttu-id="6f1e4-648">Elektronisks maksājums</span><span class="sxs-lookup"><span data-stu-id="6f1e4-648">Electronic Payment</span></span> | <span data-ttu-id="6f1e4-649">Pārsūtījums</span><span class="sxs-lookup"><span data-stu-id="6f1e4-649">Transfer</span></span>                  |
| <span data-ttu-id="6f1e4-650">Atzīmēt</span><span class="sxs-lookup"><span data-stu-id="6f1e4-650">Check</span></span>              | <span data-ttu-id="6f1e4-651">Čeks</span><span class="sxs-lookup"><span data-stu-id="6f1e4-651">Cheque</span></span>                    |
| <span data-ttu-id="6f1e4-652">Bankas vekselis</span><span class="sxs-lookup"><span data-stu-id="6f1e4-652">Bank Draft</span></span>         | <span data-ttu-id="6f1e4-653">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="6f1e4-653">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="6f1e4-654">Citi</span><span class="sxs-lookup"><span data-stu-id="6f1e4-654">Other</span></span>              | <span data-ttu-id="6f1e4-655">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="6f1e4-655">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="6f1e4-656">Bankas konta tips</span><span class="sxs-lookup"><span data-stu-id="6f1e4-656">Bank account type</span></span>

<span data-ttu-id="6f1e4-657">Bankas kontu tipus izmanto darbiniekiem sūtāmajiem elektroniskajiem maksājumiem.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-657">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="6f1e4-658">Bankas kontu tipi tiek kartēti uz pakalpojumu Dayforce kā pārsūtīšanas konta informācija.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-658">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="6f1e4-659">Bankas kontu tipi integrācijas laikā tiek atbilstoši tulkoti uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-659">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="6f1e4-660">Talent</span><span class="sxs-lookup"><span data-stu-id="6f1e4-660">Talent</span></span>            | <span data-ttu-id="6f1e4-661">Dayforce</span><span class="sxs-lookup"><span data-stu-id="6f1e4-661">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="6f1e4-662">Kontroles konts</span><span class="sxs-lookup"><span data-stu-id="6f1e4-662">Checking Account</span></span>  | <span data-ttu-id="6f1e4-663">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="6f1e4-663">CheckingAccount</span></span>           |
| <span data-ttu-id="6f1e4-664">Algu konts</span><span class="sxs-lookup"><span data-stu-id="6f1e4-664">Payroll Account</span></span>   | <span data-ttu-id="6f1e4-665">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="6f1e4-665">PayrollAccount</span></span>            |
| <span data-ttu-id="6f1e4-666">Uzkrājumu konts</span><span class="sxs-lookup"><span data-stu-id="6f1e4-666">Savings Account</span></span>   | <span data-ttu-id="6f1e4-667">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="6f1e4-667">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="6f1e4-668">BankGirot konts</span><span class="sxs-lookup"><span data-stu-id="6f1e4-668">BankGirot account</span></span> | <span data-ttu-id="6f1e4-669">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="6f1e4-669">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="6f1e4-670">PlusGirot konts</span><span class="sxs-lookup"><span data-stu-id="6f1e4-670">PlusGirot account</span></span> | <span data-ttu-id="6f1e4-671">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="6f1e4-671">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="6f1e4-672">Ienākumu veida kodi</span><span class="sxs-lookup"><span data-stu-id="6f1e4-672">Earning codes</span></span>

<span data-ttu-id="6f1e4-673">Ienākumu veidu kodi unikāli identificē katra veida ienākumus, ko saņem nodarbinātie.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-673">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="6f1e4-674">Kodiem ir vairāki ar ienākumiem saistīti parametri, piemēram, uzskaites nosacījumi, nodokļu likumi, pārskatu veidošanas prasības un bruto summas palielināšanas iespēja.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-674">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="6f1e4-675">Ja tiek izmantota neatbalstīta biežuma vērtība, aprēķinā pēc noklusējuma tiek lietota biežuma vērtība **Katra apmaksa**.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-675">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="6f1e4-676">Atbalstītās biežuma vērtības</span><span class="sxs-lookup"><span data-stu-id="6f1e4-676">Supported frequencies</span></span>

- <span data-ttu-id="6f1e4-677">Visus</span><span class="sxs-lookup"><span data-stu-id="6f1e4-677">All</span></span>
- <span data-ttu-id="6f1e4-678">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="6f1e4-678">EVERYPAY</span></span>
- <span data-ttu-id="6f1e4-679">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="6f1e4-679">EACHPAYPERIOD</span></span>
- <span data-ttu-id="6f1e4-680">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="6f1e4-680">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="6f1e4-681">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="6f1e4-681">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="6f1e4-682">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="6f1e4-682">1OFMTH</span></span>
- <span data-ttu-id="6f1e4-683">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="6f1e4-683">LASTOFMTH</span></span>
- <span data-ttu-id="6f1e4-684">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="6f1e4-684">2OFMTH</span></span>
- <span data-ttu-id="6f1e4-685">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="6f1e4-685">3OFMTH</span></span>
- <span data-ttu-id="6f1e4-686">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6f1e4-686">4OFMTH</span></span>
- <span data-ttu-id="6f1e4-687">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="6f1e4-687">5OFMTH</span></span>
- <span data-ttu-id="6f1e4-688">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="6f1e4-688">1N2OFMTH</span></span>
- <span data-ttu-id="6f1e4-689">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6f1e4-689">3N4OFMTH</span></span>
- <span data-ttu-id="6f1e4-690">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="6f1e4-690">1N3OFMTH</span></span>
- <span data-ttu-id="6f1e4-691">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6f1e4-691">1N4OFMTH</span></span>
- <span data-ttu-id="6f1e4-692">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="6f1e4-692">2N3OFMTH</span></span>
- <span data-ttu-id="6f1e4-693">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6f1e4-693">2N4OFMTH</span></span>
- <span data-ttu-id="6f1e4-694">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="6f1e4-694">1N2N3OFMTH</span></span>
- <span data-ttu-id="6f1e4-695">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6f1e4-695">1N2N4OFMTH</span></span>
- <span data-ttu-id="6f1e4-696">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6f1e4-696">1N3N4OFMTH</span></span>
- <span data-ttu-id="6f1e4-697">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6f1e4-697">2N3N4OFMTH</span></span>
- <span data-ttu-id="6f1e4-698">1N2N3N4OFMTH–1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="6f1e4-698">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="6f1e4-699">2N3N4N5OFMth–2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="6f1e4-699">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="6f1e4-700">1OFQTR–1OFQTR</span><span class="sxs-lookup"><span data-stu-id="6f1e4-700">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="6f1e4-701">LASTOFQTR–LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="6f1e4-701">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="6f1e4-702">LASTMTHOFQTR–LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="6f1e4-702">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="6f1e4-703">1OFYEAR–1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="6f1e4-703">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="6f1e4-704">LASTOFYEAR–LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="6f1e4-704">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="6f1e4-705">NOVNDECOFYEAR–NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="6f1e4-705">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="6f1e4-706">Adreses</span><span class="sxs-lookup"><span data-stu-id="6f1e4-706">Addresses</span></span>

<span data-ttu-id="6f1e4-707">Noteiktas valsts vai reģiona, administratīvā apgabala un apgabala (pašvaldības) kodu identifikācijai ir nepieciešami konkrēti formāti, ko var atpazīt pakalpojums Dayforce un valsts/reģiona pakalpojumu sniedzēji.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-707">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="6f1e4-708">Lai gan pilsētu formāts var būt dažāds, katrai pilsētai ir jābūt saistītai ar administratīvo apgabalu.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-708">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="6f1e4-709">Talent</span><span class="sxs-lookup"><span data-stu-id="6f1e4-709">Talent</span></span>              | <span data-ttu-id="6f1e4-710">Dayforce</span><span class="sxs-lookup"><span data-stu-id="6f1e4-710">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="6f1e4-711">Valsts/reģions</span><span class="sxs-lookup"><span data-stu-id="6f1e4-711">Country/Region</span></span>      | <span data-ttu-id="6f1e4-712">Valsts kods</span><span class="sxs-lookup"><span data-stu-id="6f1e4-712">Country Code</span></span>          |
| <span data-ttu-id="6f1e4-713">Pasta indekss</span><span class="sxs-lookup"><span data-stu-id="6f1e4-713">Zip/Postal Code</span></span>     | <span data-ttu-id="6f1e4-714">Pasta indekss</span><span class="sxs-lookup"><span data-stu-id="6f1e4-714">Postal Code</span></span>           |
| <span data-ttu-id="6f1e4-715">Administratīvais apgabals</span><span class="sxs-lookup"><span data-stu-id="6f1e4-715">State</span></span>               | <span data-ttu-id="6f1e4-716">Administratīvā apgabala kods</span><span class="sxs-lookup"><span data-stu-id="6f1e4-716">State Code</span></span>            |
| <span data-ttu-id="6f1e4-717">Pilsēta</span><span class="sxs-lookup"><span data-stu-id="6f1e4-717">City</span></span>                | <span data-ttu-id="6f1e4-718">Pilsēta</span><span class="sxs-lookup"><span data-stu-id="6f1e4-718">City</span></span>                  |
| <span data-ttu-id="6f1e4-719">Apgabals</span><span class="sxs-lookup"><span data-stu-id="6f1e4-719">County</span></span>              | <span data-ttu-id="6f1e4-720">Apgabals (pašvaldība)</span><span class="sxs-lookup"><span data-stu-id="6f1e4-720">County (Municipality)</span></span> |
| <span data-ttu-id="6f1e4-721">Iela</span><span class="sxs-lookup"><span data-stu-id="6f1e4-721">Street</span></span>              | <span data-ttu-id="6f1e4-722">Adreses 1. rinda</span><span class="sxs-lookup"><span data-stu-id="6f1e4-722">Address Line 1</span></span>        |
| <span data-ttu-id="6f1e4-723">Ielas numurs</span><span class="sxs-lookup"><span data-stu-id="6f1e4-723">Street Number</span></span>       | <span data-ttu-id="6f1e4-724">Adreses 2. rinda</span><span class="sxs-lookup"><span data-stu-id="6f1e4-724">Address Line 2</span></span>        |
| <span data-ttu-id="6f1e4-725">Mājas numurs/nosaukums</span><span class="sxs-lookup"><span data-stu-id="6f1e4-725">Building Complement</span></span> | <span data-ttu-id="6f1e4-726">Adreses 5. rinda</span><span class="sxs-lookup"><span data-stu-id="6f1e4-726">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="6f1e4-727">Pases numurs</span><span class="sxs-lookup"><span data-stu-id="6f1e4-727">Passport number</span></span>

<span data-ttu-id="6f1e4-728">Darbinieki var sniegt pases informāciju.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-728">Employees can declare passport information.</span></span> <span data-ttu-id="6f1e4-729">Šīs informācijas identifikācijas tips ir **Pase**, un tā tiek integrēta pakalpojumā Dayforce kā daļa no darbinieka Meksikai specifiskās informācijas.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-729">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="6f1e4-730">Identifikācijas tips = Pase</span><span class="sxs-lookup"><span data-stu-id="6f1e4-730">Identification Type = "Passport"</span></span>
- <span data-ttu-id="6f1e4-731">Izdošanas datums</span><span class="sxs-lookup"><span data-stu-id="6f1e4-731">Issued Date</span></span>
- <span data-ttu-id="6f1e4-732">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="6f1e4-732">Expiration Date</span></span>

<span data-ttu-id="6f1e4-733">Darbinieki var sniegt vairākus identifikācijas numurus, kuru identifikācijas tips ir **Pase**.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-733">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="6f1e4-734">Taču pakalpojumā Dayforce tiek integrēts tikai pašreizējais aktīvais pases ieraksts.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-734">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="6f1e4-735">Ja visiem pases ierakstiem ir beidzies derīgiem, pakalpojumā Dayforce tiek integrēta pēdējā izdotā pase.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-735">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
