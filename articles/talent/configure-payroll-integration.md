---
title: Algu aprēķina integrācijas konfigurēšana pakalpojumos Talent un Dayforce
description: Šajā tēmā ir paskaidrots, kā konfigurēt Microsoft Dynamics 365 for Talent un Ceridian Dayforce integrāciju, lai varētu apstrādāt maksājuma izpildi.
author: andreabichsel
manager: AnnBe
ms.date: 06/24/2019
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
ms.openlocfilehash: 59234ef44ad22383ae5daf71d4b663c6183e6c05
ms.sourcegitcommit: d599bc1fc60a010c2753ca547219ae21456b1df9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/25/2019
ms.locfileid: "1702822"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="9a00f-103">Talent un Dayforce algu aprēķina integrācijas konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="9a00f-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9a00f-104">Microsoft Dynamics 365 for Talent un Ceridian Dayforce integrācijai tiek izmantotas vairākas konfigurācijas darbības, kas ir aprakstītas šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="9a00f-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="9a00f-105">Pirms maksājuma izpildes apstrādes vispirms ir jākonfigurē integrācija gan pakalpojumā Talent, gan pakalpojumā Dayforce.</span><span class="sxs-lookup"><span data-stu-id="9a00f-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="9a00f-106">Ja maksājumu izpildei izmantojat tādu pakalpojumu kā Dayforce, jums ir jāiespējo integrācija pakalpojumā Talent.</span><span class="sxs-lookup"><span data-stu-id="9a00f-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="9a00f-107">Integrācijai ir nepieciešami noteikti Talent dati.</span><span class="sxs-lookup"><span data-stu-id="9a00f-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="9a00f-108">Tādēļ ir jāpārliecinās, vai uz Dayforce kartētie dati pakalpojumā Talent ir konfigurēti veidā, kas atbalsta integrāciju.</span><span class="sxs-lookup"><span data-stu-id="9a00f-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="9a00f-109">Integrācija izmanto tālāk norādītās vispārējās datu kategorijas.</span><span class="sxs-lookup"><span data-stu-id="9a00f-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="9a00f-110">Personāla vadības dati</span><span class="sxs-lookup"><span data-stu-id="9a00f-110">Human resources data</span></span>
- <span data-ttu-id="9a00f-111">Atlīdzības dati</span><span class="sxs-lookup"><span data-stu-id="9a00f-111">Compensation data</span></span>
- <span data-ttu-id="9a00f-112">Algu dati, piemēram, apmaksas cikli, apmaksas periodi un ienākumu veidu kodi</span><span class="sxs-lookup"><span data-stu-id="9a00f-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="9a00f-113">Nodarbināto dati</span><span class="sxs-lookup"><span data-stu-id="9a00f-113">Worker data</span></span>

<span data-ttu-id="9a00f-114">Šajā tēmā ir aprakstītas darbības, kas jāveic, lai iespējotu integrāciju.</span><span class="sxs-lookup"><span data-stu-id="9a00f-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="9a00f-115">Tajā ir arī izskaidrots, kādu veidu dati un konfigurācijas informācija ir nepieciešama integrācijai.</span><span class="sxs-lookup"><span data-stu-id="9a00f-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="9a00f-116">Integrācijas iespējošana</span><span class="sxs-lookup"><span data-stu-id="9a00f-116">Enable the integration</span></span>

<span data-ttu-id="9a00f-117">Lai izveidotu savienojumu ar Dayforce, pakalpojumā Talent ir jāieslēdz integrācija un jāievada konfigurācijas informācija.</span><span class="sxs-lookup"><span data-stu-id="9a00f-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="9a00f-118">Ja vēlaties, lai izveidotā Virsgrāmatas transakcija tiktu importēta programmā Microsoft Dynamics 365 for Finance and Operations, ir jāiestata arī Microsoft Azure krātuves konts un programmā Finance and Operations jāievada Azure krātuves savienojuma virkne.</span><span class="sxs-lookup"><span data-stu-id="9a00f-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="9a00f-119">Lai pakalpojumā Talent ieslēgtu integrāciju, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="9a00f-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="9a00f-120">Lapā **Sistēmas administrēšana** atlasiet opciju **Integrācijas konfigurēšana**.</span><span class="sxs-lookup"><span data-stu-id="9a00f-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="9a00f-121">Ievadiet drošo failu pārsūtīšanas protokola (FTP) galapunktu un drošo FTP mapes ceļu.</span><span class="sxs-lookup"><span data-stu-id="9a00f-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="9a00f-122">Ievadiet tā lietotāja lietotājvārdu un paroli, kurš piekļūs drošajam FTP galapunktam un mapes ceļam.</span><span class="sxs-lookup"><span data-stu-id="9a00f-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="9a00f-123">Pārbaudiet savienojumu, kā nepieciešams, un opciju **Iespējot algu aprēķina integrāciju** iestatiet uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="9a00f-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="9a00f-124">Kad integrācija ir ieslēgta, tiek izveidota datu eksportēšanas pakotne un faili, kā arī iestatīts biežums.</span><span class="sxs-lookup"><span data-stu-id="9a00f-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="9a00f-125">Biežumu varat mainīt atbilstoši vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="9a00f-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="9a00f-126">Papildinformāciju par Azure krātuves kontiem un Azure krātuves savienojuma virknēm skatiet tālāk sniegtajās Azure tēmās.</span><span class="sxs-lookup"><span data-stu-id="9a00f-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="9a00f-127">Par Azure krātuves kontiem</span><span class="sxs-lookup"><span data-stu-id="9a00f-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="9a00f-128">Azure krātuves savienojuma virkņu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="9a00f-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="9a00f-129">Tehniskā informācija par algu aprēķina integrācijas iespējošanu</span><span class="sxs-lookup"><span data-stu-id="9a00f-129">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="9a00f-130">Algu aprēķina integrācijas ieslēgšanai ir divi primārie iznākumi, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="9a00f-130">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="9a00f-131">Tiek izveidots datu eksportēšanas projekts ar nosaukumu “Algu aprēķina integrācijas eksportēšana”.</span><span class="sxs-lookup"><span data-stu-id="9a00f-131">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="9a00f-132">Šajā projektā ir iekļauti elementi un lauki, kas nepieciešami algu aprēķina integrācijai.</span><span class="sxs-lookup"><span data-stu-id="9a00f-132">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="9a00f-133">Lai pārbaudītu projektu, dodieties uz sadaļu **Sistēmas administrēšana**, atlasiet elementu **Datu pārvaldība** un pēc tam atveriet datu projektu no projektu saraksta.</span><span class="sxs-lookup"><span data-stu-id="9a00f-133">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="9a00f-134">Šis pakešuzdevums izpilda datu eksportēšanas projektu, šifrē iegūto datu pakotni un pārsūta datu pakotnes failu uz SFTP galapunktu, kas konfigurēts ekrānā **Integrācijas konfigurēšana**.</span><span class="sxs-lookup"><span data-stu-id="9a00f-134">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="9a00f-135">Datu pakotne, kas pārsūtīta uz SFTP galapunktu, tiek šifrēta, izmantojot pakotnes unikālo atslēgu.</span><span class="sxs-lookup"><span data-stu-id="9a00f-135">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="9a00f-136">Atslēga glabājas Azure Key Vault krātuvē, kam var piekļūt, tikai izmantojot Ceridian.</span><span class="sxs-lookup"><span data-stu-id="9a00f-136">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="9a00f-137">Nav iespējams atšifrēt un pārbaudīt datu pakotnes saturu.</span><span class="sxs-lookup"><span data-stu-id="9a00f-137">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="9a00f-138">Ja ir jāpārbauda datu pakotnes saturs, eksportējiet datu projektu “Algu aprēķina integrācijas eksportēšana” manuāli, lejupielādējiet to un pēc tam atveriet to.</span><span class="sxs-lookup"><span data-stu-id="9a00f-138">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="9a00f-139">Eksportējot manuāli, pakotne netiks šifrēta un pārsūtīta.</span><span class="sxs-lookup"><span data-stu-id="9a00f-139">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="9a00f-140">Datu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="9a00f-140">Configure your data</span></span> 

<span data-ttu-id="9a00f-141">Lai apstrādātu algas, pakalpojumā Talent ir jākonfigurē personāla vadības dati.</span><span class="sxs-lookup"><span data-stu-id="9a00f-141">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="9a00f-142">Jums ir jāiestata organizācijas dati, piemēram, darbi un amati, kā arī informācija par atvieglojumiem un atlīdzību.</span><span class="sxs-lookup"><span data-stu-id="9a00f-142">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="9a00f-143">Šie dati nodrošina informāciju par nodarbinātību, samaksu un ieturējumiem, kas nepieciešama darbinieka algas ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="9a00f-143">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="9a00f-144">Personāla vadības dati</span><span class="sxs-lookup"><span data-stu-id="9a00f-144">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="9a00f-145">Atvieglojumi</span><span class="sxs-lookup"><span data-stu-id="9a00f-145">Benefits</span></span> 

<span data-ttu-id="9a00f-146">Personāla vadība nodrošina rīkus, ko var izmantot, lai iestatītu un uzturētu atvieglojumus, ieturējumus un nodarbināto atlīdzības plānus, ko organizācija piedāvā vai apstrādā saviem nodarbinātajiem.</span><span class="sxs-lookup"><span data-stu-id="9a00f-146">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="9a00f-147">Kad veidojat atvieglojumus, ņemiet vērā tālāk norādītos datus un konfigurācijas, kas tiek izmantoti pakalpojumā Dayforce.</span><span class="sxs-lookup"><span data-stu-id="9a00f-147">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="9a00f-148">Atvieglojumu plāni</span><span class="sxs-lookup"><span data-stu-id="9a00f-148">Benefit plans</span></span>

- <span data-ttu-id="9a00f-149">Plāns (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-149">Plan (required)</span></span>
- <span data-ttu-id="9a00f-150">Tips (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-150">Type (required)</span></span>
- <span data-ttu-id="9a00f-151">Algas ietekme (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-151">Payroll impact (required)</span></span>
- <span data-ttu-id="9a00f-152">Atgūt nokavētos maksājumus</span><span class="sxs-lookup"><span data-stu-id="9a00f-152">Recover arrears</span></span>
- <span data-ttu-id="9a00f-153">Ieturējuma metode</span><span class="sxs-lookup"><span data-stu-id="9a00f-153">Deduction method</span></span>
- <span data-ttu-id="9a00f-154">Ieturējuma prioritāte</span><span class="sxs-lookup"><span data-stu-id="9a00f-154">Deduction priority</span></span>
- <span data-ttu-id="9a00f-155">Ierobežojuma periods</span><span class="sxs-lookup"><span data-stu-id="9a00f-155">Limit period</span></span>
- <span data-ttu-id="9a00f-156">Ierobežojuma summa</span><span class="sxs-lookup"><span data-stu-id="9a00f-156">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="9a00f-157">Atvieglojumi</span><span class="sxs-lookup"><span data-stu-id="9a00f-157">Benefits</span></span>

- <span data-ttu-id="9a00f-158">Plāns (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-158">Plan (required)</span></span>
- <span data-ttu-id="9a00f-159">Tips (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-159">Type (required)</span></span>
- <span data-ttu-id="9a00f-160">Opcija (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-160">Option (required)</span></span>
- <span data-ttu-id="9a00f-161">Atvieglojumu ID (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-161">Benefit ID (required)</span></span>
- <span data-ttu-id="9a00f-162">Biežums</span><span class="sxs-lookup"><span data-stu-id="9a00f-162">Frequency</span></span>
- <span data-ttu-id="9a00f-163">Pamats</span><span class="sxs-lookup"><span data-stu-id="9a00f-163">Basis</span></span>
- <span data-ttu-id="9a00f-164">Summa vai likme</span><span class="sxs-lookup"><span data-stu-id="9a00f-164">Amount or rate</span></span>
- <span data-ttu-id="9a00f-165">Ienākumu veida kods</span><span class="sxs-lookup"><span data-stu-id="9a00f-165">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="9a00f-166">Atbalstītās biežuma vērtības</span><span class="sxs-lookup"><span data-stu-id="9a00f-166">Supported frequencies</span></span> 

- <span data-ttu-id="9a00f-167">Katru nedēļu</span><span class="sxs-lookup"><span data-stu-id="9a00f-167">Weekly</span></span>
- <span data-ttu-id="9a00f-168">Katru otro nedēļu</span><span class="sxs-lookup"><span data-stu-id="9a00f-168">Bi-weekly</span></span>
- <span data-ttu-id="9a00f-169">Pusmēneša</span><span class="sxs-lookup"><span data-stu-id="9a00f-169">Semi-monthly</span></span>
- <span data-ttu-id="9a00f-170">Mēnesis</span><span class="sxs-lookup"><span data-stu-id="9a00f-170">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="9a00f-171">Atbalstītās pamata vērtības</span><span class="sxs-lookup"><span data-stu-id="9a00f-171">Supported bases</span></span> 

- <span data-ttu-id="9a00f-172">Fiksēta summa</span><span class="sxs-lookup"><span data-stu-id="9a00f-172">Fixed amount</span></span>
- <span data-ttu-id="9a00f-173">Ienākumu procentuālais daudzums</span><span class="sxs-lookup"><span data-stu-id="9a00f-173">Percent of earnings</span></span>
- <span data-ttu-id="9a00f-174">Produktīvās stundas</span><span class="sxs-lookup"><span data-stu-id="9a00f-174">Productive hours</span></span>

<span data-ttu-id="9a00f-175">Dayforce izveido tālāk norādītos ieturējumus, pamatojoties uz atvieglojumu plānā definēto algas ietekmi.</span><span class="sxs-lookup"><span data-stu-id="9a00f-175">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="9a00f-176">Atlase pakalpojumā Talent</span><span class="sxs-lookup"><span data-stu-id="9a00f-176">Selection in Talent</span></span>        | <span data-ttu-id="9a00f-177">Rezultāts pakalpojumā Dayforce</span><span class="sxs-lookup"><span data-stu-id="9a00f-177">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="9a00f-178">Neviens</span><span class="sxs-lookup"><span data-stu-id="9a00f-178">None</span></span>                       | <span data-ttu-id="9a00f-179">Nav izveidots neviens ieturējums.</span><span class="sxs-lookup"><span data-stu-id="9a00f-179">No deduction is created.</span></span>                      |
| <span data-ttu-id="9a00f-180">Tikai ieturējums</span><span class="sxs-lookup"><span data-stu-id="9a00f-180">Deduction only</span></span>             | <span data-ttu-id="9a00f-181">Ir izveidots darbinieka ieturējums.</span><span class="sxs-lookup"><span data-stu-id="9a00f-181">An employee deduction is created.</span></span>             |
| <span data-ttu-id="9a00f-182">Tikai segums</span><span class="sxs-lookup"><span data-stu-id="9a00f-182">Contribution only</span></span>          | <span data-ttu-id="9a00f-183">Ir izveidots darba devēja ieturējums.</span><span class="sxs-lookup"><span data-stu-id="9a00f-183">An employer deduction is created.</span></span>             |
| <span data-ttu-id="9a00f-184">Ieturējums un segums</span><span class="sxs-lookup"><span data-stu-id="9a00f-184">Deduction and contribution</span></span> | <span data-ttu-id="9a00f-185">Ir izveidots darbinieka un darba devēja ieturējums.</span><span class="sxs-lookup"><span data-stu-id="9a00f-185">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="9a00f-186">Papildinformāciju par atvieglojumu programmas definēšanu un pārvaldību skatiet tālāk sniegtajās tēmās.</span><span class="sxs-lookup"><span data-stu-id="9a00f-186">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="9a00f-187">Darbinieku atvieglojumu programmas nodrošināšana</span><span class="sxs-lookup"><span data-stu-id="9a00f-187">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="9a00f-188">Jauna atvieglojuma izveide</span><span class="sxs-lookup"><span data-stu-id="9a00f-188">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="9a00f-189">Atvieglojumu piemērotības kārtulu un ierobežojumu definēšana</span><span class="sxs-lookup"><span data-stu-id="9a00f-189">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="9a00f-190">Atvieglojumu reģistrēšana un noņemšana nodarbinātajiem</span><span class="sxs-lookup"><span data-stu-id="9a00f-190">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="9a00f-191">Atlīdzība</span><span class="sxs-lookup"><span data-stu-id="9a00f-191">Compensation</span></span> 

<span data-ttu-id="9a00f-192">Atlīdzību pārvaldība tiek izmantota, lai kontrolētu pamatalgas un prēmiju izsniegšanu.</span><span class="sxs-lookup"><span data-stu-id="9a00f-192">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="9a00f-193">Darbinieka fiksētā pamatalga un nopelnu palielinājumi tiek kontrolēti, izmantojot fiksētas atlīdzības plānus.</span><span class="sxs-lookup"><span data-stu-id="9a00f-193">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="9a00f-194">Veicināšanas maksājumu izsniegšana, piemēram, prēmiju maksājumi, apbalvojumi par sasniegumiem, uzņēmuma akciju iegādes iespējas un dotācijas, kā arī vienreizējas piemaksas, tiek kontrolētas ar mainīgās atlīdzības plāniem.</span><span class="sxs-lookup"><span data-stu-id="9a00f-194">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="9a00f-195">Dayforce izmanto atlīdzības informāciju, lai aprēķinātu darbinieka stundas vai gada likmi.</span><span class="sxs-lookup"><span data-stu-id="9a00f-195">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="9a00f-196">Ir jānorāda fiksētās atlīdzības plāni un apmaksas likmes konvertēšanas gadījumi.</span><span class="sxs-lookup"><span data-stu-id="9a00f-196">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="9a00f-197">Darbiniekiem ir jābūt saistītiem ar fiksētās atlīdzības plānu.</span><span class="sxs-lookup"><span data-stu-id="9a00f-197">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="9a00f-198">Papildinformāciju par atlīdzības plāniem skatiet tālāk sniegtajās tēmās.</span><span class="sxs-lookup"><span data-stu-id="9a00f-198">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="9a00f-199">Fiksētās atlīdzības plānu izveidošana</span><span class="sxs-lookup"><span data-stu-id="9a00f-199">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="9a00f-200">Mainīgās atlīdzības plānu izveidošana</span><span class="sxs-lookup"><span data-stu-id="9a00f-200">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="9a00f-201">Algas/atlīdzības organizācijas un plānu izstrāde</span><span class="sxs-lookup"><span data-stu-id="9a00f-201">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="9a00f-202">Procesa kompensācija</span><span class="sxs-lookup"><span data-stu-id="9a00f-202">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="9a00f-203">Atlīdzības procesa definēšana un rezultātu aprēķināšana</span><span class="sxs-lookup"><span data-stu-id="9a00f-203">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="9a00f-204">Darbinieka reģistrēšana fiksētās atlīdzības plānā</span><span class="sxs-lookup"><span data-stu-id="9a00f-204">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="9a00f-205">Darbinieka reģistrēšana mainīgās atlīdzības plānā</span><span class="sxs-lookup"><span data-stu-id="9a00f-205">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="9a00f-206">Darbi</span><span class="sxs-lookup"><span data-stu-id="9a00f-206">Jobs</span></span> 

<span data-ttu-id="9a00f-207">Darbs ir uzdevumu un atbildības jomu kopums, kas ir jāizpilda personai, kura veic darbu.</span><span class="sxs-lookup"><span data-stu-id="9a00f-207">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="9a00f-208">Lai iegūtu papildu informāciju, skatiet šādas tēmas:</span><span class="sxs-lookup"><span data-stu-id="9a00f-208">For more information, see the following topics:</span></span>

- [<span data-ttu-id="9a00f-209">Darba komponentu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="9a00f-209">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="9a00f-210">Jaunu darbu definēšana</span><span class="sxs-lookup"><span data-stu-id="9a00f-210">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="9a00f-211">Amati</span><span class="sxs-lookup"><span data-stu-id="9a00f-211">Positions</span></span>

<span data-ttu-id="9a00f-212">Pozīcija ir atsevišķa darba instance.</span><span class="sxs-lookup"><span data-stu-id="9a00f-212">A position is an individual instance of a job.</span></span> <span data-ttu-id="9a00f-213">Piemēram, amats Pārdošanas daļas vadītājs (austrumu reģions) ir tikai viens no amatiem, kas ir saistīti ar darbu Pārdošanas daļas vadītājs.</span><span class="sxs-lookup"><span data-stu-id="9a00f-213">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="9a00f-214">Amats pastāv nodaļā.</span><span class="sxs-lookup"><span data-stu-id="9a00f-214">A position exists in a department.</span></span> <span data-ttu-id="9a00f-215">Ar katru amatu var būt saistīts tikai viens nodarbinātais.</span><span class="sxs-lookup"><span data-stu-id="9a00f-215">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="9a00f-216">Iestatot jaunus amatus, ņemiet vērā tālāk norādītos datus un konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="9a00f-216">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="9a00f-217">Amats (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-217">Position (required)</span></span>
- <span data-ttu-id="9a00f-218">Apraksts (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-218">Description (required)</span></span>
- <span data-ttu-id="9a00f-219">Darbs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-219">Job (required)</span></span>
- <span data-ttu-id="9a00f-220">Nodaļa (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-220">Department (required)</span></span>
- <span data-ttu-id="9a00f-221">Amata veids (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-221">Position type (required)</span></span>
- <span data-ttu-id="9a00f-222">Pilnas slodzes ekvivalents</span><span class="sxs-lookup"><span data-stu-id="9a00f-222">Full-time equivalent</span></span>
- <span data-ttu-id="9a00f-223">Ikgadējās parastās stundas (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-223">Annual regular hours (required)</span></span>
- <span data-ttu-id="9a00f-224">Apmaksātāja juridiskā persona (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-224">Paid by legal entity (required)</span></span>
- <span data-ttu-id="9a00f-225">Apmaksas cikls (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-225">Pay cycle (required)</span></span>
- <span data-ttu-id="9a00f-226">Noklusējuma finanšu dimensija — izmaksu centrs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-226">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="9a00f-227">Nodarbinātā piešķire — nodarbinātais, piešķires sākums, piešķires beigas, iemesla kods</span><span class="sxs-lookup"><span data-stu-id="9a00f-227">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="9a00f-228">Ja vienā nodaļā ar to pašu darbu ir saistīti vairāki amati, tie pakalpojumā Dayforce tiek apvienoti vienā amatā.</span><span class="sxs-lookup"><span data-stu-id="9a00f-228">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="9a00f-229">Lai iegūtu papildu informāciju, skatiet šādas tēmas:</span><span class="sxs-lookup"><span data-stu-id="9a00f-229">For more information, see the following topics:</span></span>

- [<span data-ttu-id="9a00f-230">Organizēt darbaspēku, izmantojot nodaļas, darbus un amatus</span><span class="sxs-lookup"><span data-stu-id="9a00f-230">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="9a00f-231">Amatu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="9a00f-231">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="9a00f-232">Nodaļas</span><span class="sxs-lookup"><span data-stu-id="9a00f-232">Departments</span></span>

<span data-ttu-id="9a00f-233">Nodaļa ir pārvaldības struktūrvienība, kas pārstāv organizācijas kategoriju vai funkcionālo apgabalu.</span><span class="sxs-lookup"><span data-stu-id="9a00f-233">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="9a00f-234">Nodaļa ir atbildīga par noteiktu organizācijas jomu, piemēram, pārdošanu, uzskaiti vai personāla vadību.</span><span class="sxs-lookup"><span data-stu-id="9a00f-234">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="9a00f-235">Nodaļas var izmantot, lai ziņotu par funkcionālām jomām.</span><span class="sxs-lookup"><span data-stu-id="9a00f-235">You can use departments to report on functional areas.</span></span> <span data-ttu-id="9a00f-236">Nodaļām var būt peļņas un zaudējumu atbildība.</span><span class="sxs-lookup"><span data-stu-id="9a00f-236">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="9a00f-237">Lai iegūtu papildu informāciju, skatiet šādas tēmas:</span><span class="sxs-lookup"><span data-stu-id="9a00f-237">For more information, see the following topics:</span></span>

- [<span data-ttu-id="9a00f-238">Nodaļas izveide un tās saistīšana ar nodaļu hierarhiju</span><span class="sxs-lookup"><span data-stu-id="9a00f-238">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="9a00f-239">Jaunu nodaļu definēšana</span><span class="sxs-lookup"><span data-stu-id="9a00f-239">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="9a00f-240">Apmaksas cikli un apmaksas periodi</span><span class="sxs-lookup"><span data-stu-id="9a00f-240">Pay cycles and pay periods</span></span>

<span data-ttu-id="9a00f-241">Apmaksas cikls nosaka, cik bieži tiek veikts algu aprēķins, kā arī konkrētās dienas, kurās nodarbinātie saņem samaksu.</span><span class="sxs-lookup"><span data-stu-id="9a00f-241">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="9a00f-242">Apmaksas cikls var būt, piemēram, ikmēneša, un darbinieki samaksu var saņemt mēneša pēdējā dienā.</span><span class="sxs-lookup"><span data-stu-id="9a00f-242">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="9a00f-243">Vai arī apmaksas cikls var būt iknedēļas, un darbinieki samaksu var saņemt otrdienā pēc apmaksas perioda beigām.</span><span class="sxs-lookup"><span data-stu-id="9a00f-243">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="9a00f-244">Apmaksas cikli tiek piešķirti amatiem, lai kontrolētu to, kad nodarbinātie šajos amatos saņems samaksu.</span><span class="sxs-lookup"><span data-stu-id="9a00f-244">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="9a00f-245">Pēc apmaksas ciklu izveides katram ciklam varat ģenerēt apmaksas periodus.</span><span class="sxs-lookup"><span data-stu-id="9a00f-245">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="9a00f-246">Katrā apmaksas periodā ir ietverts noklusējuma maksājuma datums, kura pamatā ir jūsu sniegtā informācija.</span><span class="sxs-lookup"><span data-stu-id="9a00f-246">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="9a00f-247">Taču varat modificēt apmaksas perioda noklusējuma maksājuma datumu izņēmumu iestatīšanai, piemēram, kad maksājuma datums ir brīvdienā.</span><span class="sxs-lookup"><span data-stu-id="9a00f-247">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="9a00f-248">Dayforce izmanto tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="9a00f-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="9a00f-249">Apmaksas cikls (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-249">Pay cycle (required)</span></span>
- <span data-ttu-id="9a00f-250">Apmaksas cikla biežums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-250">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="9a00f-251">Perioda sākuma datums (ir jānorāda pirmais apmaksas periods)</span><span class="sxs-lookup"><span data-stu-id="9a00f-251">Period start date (first pay period required)</span></span>
- <span data-ttu-id="9a00f-252">Noklusējuma maksājuma datums (ir jānorāda pirmais apmaksas periods)</span><span class="sxs-lookup"><span data-stu-id="9a00f-252">Default payment date (first pay period required)</span></span>

<span data-ttu-id="9a00f-253">Šī informācija pakalpojumā Dayforce ir integrēta kā apmaksas grupas, un katram apmaksas ciklam to atdala valsts vai reģions.</span><span class="sxs-lookup"><span data-stu-id="9a00f-253">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="9a00f-254">Pirms integrācijas ir jābūt ģenerētam vismaz vienam apmaksas periodam.</span><span class="sxs-lookup"><span data-stu-id="9a00f-254">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="9a00f-255">Dayforce ģenerē apmaksas grupu kalendārus un maksājumu datumus atbilstoši pakalpojumā Talent iestatītajam pirmā apmaksas perioda sākuma datumam un noklusējuma maksājuma datumam.</span><span class="sxs-lookup"><span data-stu-id="9a00f-255">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="9a00f-256">Ienākumu veida kodi</span><span class="sxs-lookup"><span data-stu-id="9a00f-256">Earning codes</span></span>

<span data-ttu-id="9a00f-257">Ienākumu veidu kodi unikāli identificē katra veida ienākumus, ko saņem nodarbinātie.</span><span class="sxs-lookup"><span data-stu-id="9a00f-257">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="9a00f-258">Kodiem ir dažādi ar ienākumiem saistīti parametri, piemēram, uzskaites nosacījumi, nodokļu likumi, pārskatu veidošanas prasības un bruto summas palielināšanas iespēja.</span><span class="sxs-lookup"><span data-stu-id="9a00f-258">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="9a00f-259">Dayforce izmanto tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="9a00f-259">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="9a00f-260">Ienākumu veida kods (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-260">Earning Code (required)</span></span>
- <span data-ttu-id="9a00f-261">apraksts</span><span class="sxs-lookup"><span data-stu-id="9a00f-261">Description</span></span>
- <span data-ttu-id="9a00f-262">Mērvienība</span><span class="sxs-lookup"><span data-stu-id="9a00f-262">Unit of measure</span></span>
- <span data-ttu-id="9a00f-263">Produktīvs</span><span class="sxs-lookup"><span data-stu-id="9a00f-263">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="9a00f-264">Nodarbināto dati</span><span class="sxs-lookup"><span data-stu-id="9a00f-264">Worker data</span></span>

<span data-ttu-id="9a00f-265">Dažādo veidu nodarbināto ieraksti ir svarīga informācija personāla vadības un algu sistēmās.</span><span class="sxs-lookup"><span data-stu-id="9a00f-265">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="9a00f-266">Ievadīto informāciju var izmantot, lai sekotu nodarbinātajiem un personiskajai informācijai.</span><span class="sxs-lookup"><span data-stu-id="9a00f-266">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="9a00f-267">Par darbiniekiem var saglabāt tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="9a00f-267">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="9a00f-268">**Pamata** — saglabājiet pamata informāciju par darbinieku, piemēram, kontaktinformāciju, demogrāfisko informāciju, identifikācijas informāciju, ģimenes informāciju, karadienesta statusu, ekspatriantu informāciju, kā arī personiskās un ārkārtas kontaktpersonas.</span><span class="sxs-lookup"><span data-stu-id="9a00f-268">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="9a00f-269">**Nodarbinātība** — saglabājiet informāciju par darbinieka nodarbinātību, piemēram, informāciju par piederību uzņēmumam vai organizācijai, amata piešķiri, sākuma un beigu datumiem, piemērotību darbam, nodarbinātības noteikumiem, pensiju, atvaļinājumu un pārcelšanu.</span><span class="sxs-lookup"><span data-stu-id="9a00f-269">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="9a00f-270">**Atvaļinājumi un kavējumi** — saglabājiet informāciju par nodarbinātā kavējumiem, piemēram, informāciju par darba kalendāriem, kavējumu darbībām un kavējumu iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="9a00f-270">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="9a00f-271">**Atlīdzība un alga** — saglabājiet informāciju par nodarbinātā atlīdzības plāniem un algas informāciju, piemēram, plāna reģistrāciju, piemaksām, sniegumu, komisiju, nodokļu informāciju, pensionēšanos un ieturējumiem no algas.</span><span class="sxs-lookup"><span data-stu-id="9a00f-271">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="9a00f-272">Ievadot informāciju par nodarbināto, ņemiet vērā tālāk norādītos datus un konfigurācijas, kas tiek izmantoti pakalpojumā Dayforce.</span><span class="sxs-lookup"><span data-stu-id="9a00f-272">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="9a00f-273">Vispārīgā informācija</span><span class="sxs-lookup"><span data-stu-id="9a00f-273">General information</span></span>

- <span data-ttu-id="9a00f-274">Personāla numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-274">Personnel number (required)</span></span>
- <span data-ttu-id="9a00f-275">Vārds (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-275">First name (required)</span></span>
- <span data-ttu-id="9a00f-276">Uzvārds (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-276">Last name (required)</span></span>
- <span data-ttu-id="9a00f-277">Otrais vārds</span><span class="sxs-lookup"><span data-stu-id="9a00f-277">Middle name</span></span>
- <span data-ttu-id="9a00f-278">Darba stāža datums</span><span class="sxs-lookup"><span data-stu-id="9a00f-278">Seniority date</span></span>
- <span data-ttu-id="9a00f-279">Zināms kā</span><span class="sxs-lookup"><span data-stu-id="9a00f-279">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="9a00f-280">Personiskā informācija</span><span class="sxs-lookup"><span data-stu-id="9a00f-280">Personal information</span></span>

- <span data-ttu-id="9a00f-281">Ģimenes stāvoklis (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-281">Marital status (required)</span></span>
- <span data-ttu-id="9a00f-282">Dzimšanas datums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-282">Birth date (required)</span></span>
- <span data-ttu-id="9a00f-283">Dzimums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-283">Gender (required)</span></span>
- <span data-ttu-id="9a00f-284">Persona ar īpašām vajadzībām</span><span class="sxs-lookup"><span data-stu-id="9a00f-284">Person with disabilities</span></span>
- <span data-ttu-id="9a00f-285">Nacionalitātes valsts/reģions (tikai Meksikai)</span><span class="sxs-lookup"><span data-stu-id="9a00f-285">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="9a00f-286">Adreses informācija</span><span class="sxs-lookup"><span data-stu-id="9a00f-286">Address information</span></span>

- <span data-ttu-id="9a00f-287">Primārā (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-287">Primary (required)</span></span>
- <span data-ttu-id="9a00f-288">Valsts/reģions (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-288">Country/region (required)</span></span>
- <span data-ttu-id="9a00f-289">Pasta indekss (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-289">Postal code (required)</span></span>
- <span data-ttu-id="9a00f-290">Ielas numurs (obligāti) (tikai Meksikai)</span><span class="sxs-lookup"><span data-stu-id="9a00f-290">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="9a00f-291">Mājas numurs/nosaukums (tikai Meksikai)</span><span class="sxs-lookup"><span data-stu-id="9a00f-291">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="9a00f-292">Pilsēta (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-292">City (required)</span></span>
- <span data-ttu-id="9a00f-293">Administratīvais apgabals (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-293">State (required)</span></span>
- <span data-ttu-id="9a00f-294">Apgabals (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-294">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="9a00f-295">Kontaktinformācija</span><span class="sxs-lookup"><span data-stu-id="9a00f-295">Contact information</span></span> 

- <span data-ttu-id="9a00f-296">Primārā (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-296">Primary (required)</span></span>
- <span data-ttu-id="9a00f-297">Kontaktpersonas tālrunis (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-297">Contact number (required)</span></span>
- <span data-ttu-id="9a00f-298">Paplašinājums</span><span class="sxs-lookup"><span data-stu-id="9a00f-298">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="9a00f-299">Algas informācija un ienākumu veidu kodi</span><span class="sxs-lookup"><span data-stu-id="9a00f-299">Payroll information and earning codes</span></span>

<span data-ttu-id="9a00f-300">Darbiniekiem var būt piešķirti konkrēti ienākumu veidi konkrētajā maksājumu biežumā, kā arī var būt norādīta vēlamā maksāšanas metode.</span><span class="sxs-lookup"><span data-stu-id="9a00f-300">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="9a00f-301">Lai palīdzētu nodrošināt, ka šīs preferences un iestatījumi tiek izmantoti, pakalpojumā Dayforce ir tālāk norādītie lauki.</span><span class="sxs-lookup"><span data-stu-id="9a00f-301">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="9a00f-302">Ienākumu veida kodi</span><span class="sxs-lookup"><span data-stu-id="9a00f-302">Earning codes</span></span>

- <span data-ttu-id="9a00f-303">Amats (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-303">Position (required)</span></span>
- <span data-ttu-id="9a00f-304">Ienākumu veida kods (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-304">Earning Code (required)</span></span>
- <span data-ttu-id="9a00f-305">Biežums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-305">Frequency (required)</span></span>
- <span data-ttu-id="9a00f-306">Summa (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-306">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="9a00f-307">Algas informācija</span><span class="sxs-lookup"><span data-stu-id="9a00f-307">Payroll information</span></span>

- <span data-ttu-id="9a00f-308">Maksāšanas metode</span><span class="sxs-lookup"><span data-stu-id="9a00f-308">Payment Method</span></span>
- <span data-ttu-id="9a00f-309">Ekonomiskais reģions (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-309">Economic Region (required)</span></span>
- <span data-ttu-id="9a00f-310">Darbinieka atvieglojumu ID</span><span class="sxs-lookup"><span data-stu-id="9a00f-310">Employee Benefits ID</span></span>
- <span data-ttu-id="9a00f-311">Nacionālais ID numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-311">National ID Number (required)</span></span>
- <span data-ttu-id="9a00f-312">Karadienesta numurs</span><span class="sxs-lookup"><span data-stu-id="9a00f-312">Military Service Number</span></span>
- <span data-ttu-id="9a00f-313">Maiņas ID (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-313">Shift ID (required)</span></span>
- <span data-ttu-id="9a00f-314">Nodokļu numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-314">Tax Number (required)</span></span>
- <span data-ttu-id="9a00f-315">Arodbiedrības ID (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-315">Union ID (required)</span></span>
- <span data-ttu-id="9a00f-316">Darba dienas ID (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-316">Work Day ID (required)</span></span>
- <span data-ttu-id="9a00f-317">Darba atļaujas numurs</span><span class="sxs-lookup"><span data-stu-id="9a00f-317">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="9a00f-318">Meksika atbalsta šādas maksāšanas metodes: **Skaidra nauda**, **Čeks** (uzņēmuma fiziskais čeks) un **Elektroniskais maksājums**.</span><span class="sxs-lookup"><span data-stu-id="9a00f-318">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="9a00f-319">Ja nav norādīta neviena maksāšanas metode, pēc noklusējuma tiek izmantota opcija **Čeks**.</span><span class="sxs-lookup"><span data-stu-id="9a00f-319">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="9a00f-320">Nodarbinātības papildinformācija</span><span class="sxs-lookup"><span data-stu-id="9a00f-320">Employment details</span></span>

<span data-ttu-id="9a00f-321">Nodarbinātības datu vēsture pakalpojumā Dayforce tiek izmantota kā galvenā informācija, no kuras tiek iegūts darbinieka darbā pieņemšanas, darba attiecību izbeigšanas un atkārtotas pieņemšanas darbā statuss.</span><span class="sxs-lookup"><span data-stu-id="9a00f-321">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="9a00f-322">Dayforce vienlaikus atbalsta tikai vienu aktīvu nodarbinātības ierakstu.</span><span class="sxs-lookup"><span data-stu-id="9a00f-322">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="9a00f-323">Nodarbinātības sākuma datums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-323">Employment start date (required)</span></span>
- <span data-ttu-id="9a00f-324">Nodarbinātības beigu datums</span><span class="sxs-lookup"><span data-stu-id="9a00f-324">Employment end date</span></span>
- <span data-ttu-id="9a00f-325">Pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="9a00f-325">Start date</span></span>
- <span data-ttu-id="9a00f-326">Koriģētais pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="9a00f-326">Adjusted start date</span></span>
- <span data-ttu-id="9a00f-327">Darba attiecību pārtraukšanas datums (jānorāda, kad tiek pārtrauktas darba attiecības)</span><span class="sxs-lookup"><span data-stu-id="9a00f-327">Termination date (required upon termination)</span></span>
- <span data-ttu-id="9a00f-328">Darba attiecību pārtraukšanas iemesls (jānorāda, kad tiek pārtrauktas darba attiecības)</span><span class="sxs-lookup"><span data-stu-id="9a00f-328">Termination reason (required upon termination)</span></span>

<span data-ttu-id="9a00f-329">Darbinieka galvenie datumi tiek iegūti, izmantojot tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="9a00f-329">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="9a00f-330">Talent</span><span class="sxs-lookup"><span data-stu-id="9a00f-330">Talent</span></span>                | <span data-ttu-id="9a00f-331">Dayforce</span><span class="sxs-lookup"><span data-stu-id="9a00f-331">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a00f-332">Pēdējais nomas datums</span><span class="sxs-lookup"><span data-stu-id="9a00f-332">Most recent hire date</span></span> | <span data-ttu-id="9a00f-333">Pašreizējā nepārtrauktās nodarbinātības vēstures ieraksta nodarbinātības sākums</span><span class="sxs-lookup"><span data-stu-id="9a00f-333">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="9a00f-334">Izbeigšanas datums</span><span class="sxs-lookup"><span data-stu-id="9a00f-334">Termination date</span></span>      | <span data-ttu-id="9a00f-335">Pašreizējā nepārtrauktās nodarbinātības vēstures ieraksta darba attiecību pārtraukšanas datums</span><span class="sxs-lookup"><span data-stu-id="9a00f-335">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="9a00f-336">Pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="9a00f-336">Start date</span></span>            | <span data-ttu-id="9a00f-337">Pašreizējā neaktīvā nodarbinātības vēstures ieraksta koriģētais sākuma datums, sākuma datums vai nodarbinātības sākums</span><span class="sxs-lookup"><span data-stu-id="9a00f-337">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="9a00f-338">Sākotnējais darbā pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="9a00f-338">Original hire date</span></span>    | <span data-ttu-id="9a00f-339">Agrākā nodarbinātības vēstures ieraksta nodarbinātības sākums</span><span class="sxs-lookup"><span data-stu-id="9a00f-339">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="9a00f-340">Atlīdzība</span><span class="sxs-lookup"><span data-stu-id="9a00f-340">Compensation</span></span>

<span data-ttu-id="9a00f-341">Fiksētās atlīdzības plānam ir jābūt saistītam ar katra darbinieka primāro amatu visā nodarbinātības periodā.</span><span class="sxs-lookup"><span data-stu-id="9a00f-341">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="9a00f-342">Šis periods sākas ar datumu, kurā darbinieks tika pieņemts darbā (vai nodarbinātības sākuma datumu), un turpinās līdz darba attiecību pārtraukšanai.</span><span class="sxs-lookup"><span data-stu-id="9a00f-342">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="9a00f-343">Spēkā stāšanās datums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-343">Effective Date (required)</span></span>
- <span data-ttu-id="9a00f-344">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="9a00f-344">Expiration date</span></span>
- <span data-ttu-id="9a00f-345">Apmaksas likme (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-345">Pay Rate (required)</span></span>
- <span data-ttu-id="9a00f-346">Apmaksas likmes konvertēšanas gadījumi (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-346">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="9a00f-347">Gada ekvivalents (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-347">Annual equivalent (required)</span></span>
- <span data-ttu-id="9a00f-348">Stundas ekvivalents (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-348">Hourly equivalent (required)</span></span>

<span data-ttu-id="9a00f-349">Ja darbiniekam ar stundas likmi ir vairāki amati, pakalpojumā Dayforce kā darbinieka līmeņa pamatlikme/alga tiek importēta primārā amata fiksētā atlīdzība.</span><span class="sxs-lookup"><span data-stu-id="9a00f-349">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="9a00f-350">To amatu, kas nav primārie, stundas likme tiek saglabāta pakalpojumā Dayforce attiecīgajā amatā.</span><span class="sxs-lookup"><span data-stu-id="9a00f-350">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="9a00f-351">Ja darbiniekam, kurš saņem algu, ir vairāki amati, kā darbinieka līmeņa pamatlikme/alga tiek iegūta un izmantota visu aktīvo amatu kopējā stundas likme un gada alga.</span><span class="sxs-lookup"><span data-stu-id="9a00f-351">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="9a00f-352">Identifikācijas numuri</span><span class="sxs-lookup"><span data-stu-id="9a00f-352">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="9a00f-353">Sociālās apdrošināšanas numurs</span><span class="sxs-lookup"><span data-stu-id="9a00f-353">Social Security identifier</span></span> 

<span data-ttu-id="9a00f-354">Katram darbiniekam ir jābūt vienam primārajam numuram.</span><span class="sxs-lookup"><span data-stu-id="9a00f-354">Every employee must have one primary identifier.</span></span> <span data-ttu-id="9a00f-355">Šī numura identifikācijas tipam ir jābūt **SAN**.</span><span class="sxs-lookup"><span data-stu-id="9a00f-355">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="9a00f-356">Pakalpojumā Dayforce tas tiek automātiski iegūts kā darbinieka sociālās apdrošināšanas numurs, kas ir jānorāda, kad darbinieks tiek pieņemts darbā.</span><span class="sxs-lookup"><span data-stu-id="9a00f-356">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="9a00f-357">Primārais (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-357">Primary (required)</span></span>
- <span data-ttu-id="9a00f-358">Identifikācijas tips = SAN</span><span class="sxs-lookup"><span data-stu-id="9a00f-358">Identification Type = "SSN"</span></span>
- <span data-ttu-id="9a00f-359">Izdošanas datums</span><span class="sxs-lookup"><span data-stu-id="9a00f-359">Issued Date</span></span>
- <span data-ttu-id="9a00f-360">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="9a00f-360">Expiration Date</span></span>

<span data-ttu-id="9a00f-361">Darbinieki var sniegt vairākus identifikācijas numurus, kuru identifikācijas tips ir **SAN**.</span><span class="sxs-lookup"><span data-stu-id="9a00f-361">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="9a00f-362">Taču pakalpojumā Dayforce tiek integrēts tikai ieraksts, kas ir atzīmēts kā **Primārais**, neatkarīgi no tā, vai šis numurs ir aktīvs vai tam ir beidzies derīgums.</span><span class="sxs-lookup"><span data-stu-id="9a00f-362">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="9a00f-363">Banku konti un izdevumi</span><span class="sxs-lookup"><span data-stu-id="9a00f-363">Bank accounts and disbursements</span></span>

<span data-ttu-id="9a00f-364">Jebkuram darbiniekam, kurš samaksu izvēlējies saņemt bankas konta pārskaitījuma veidā, ir jāievada derīga bankas konta informācija.</span><span class="sxs-lookup"><span data-stu-id="9a00f-364">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="9a00f-365">Talent</span><span class="sxs-lookup"><span data-stu-id="9a00f-365">Talent</span></span>                         | <span data-ttu-id="9a00f-366">Dayforce</span><span class="sxs-lookup"><span data-stu-id="9a00f-366">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a00f-367">Bankas konta numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-367">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="9a00f-368">SWIFT kods (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-368">SWIFT code (required)</span></span>          | <span data-ttu-id="9a00f-369">Lauku **Bankas ID** izmanto, apstrādājot algas Meksikā.</span><span class="sxs-lookup"><span data-stu-id="9a00f-369">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="9a00f-370">Filiāles numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-370">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="9a00f-371">Bankas konta tips (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-371">Bank account type (required)</span></span>   | <span data-ttu-id="9a00f-372">Lauku **Konta tips** izmanto, apstrādājot algas Meksikā.</span><span class="sxs-lookup"><span data-stu-id="9a00f-372">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="9a00f-373">Atbalstītās vērtības ir, piemēram, **Norēķini** un **Algas**.</span><span class="sxs-lookup"><span data-stu-id="9a00f-373">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="9a00f-374">Darbiniekiem, kuri samaksu izvēlas saņemt bankas konta pārskaitījumu veidā, ir jāsniedz saite uz juridiskās personas, kuras primārā adrese ir Meksikā, atlikumu kontu, kas ir saistīts ar derīgu Meksikas bankas kontu.</span><span class="sxs-lookup"><span data-stu-id="9a00f-374">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="9a00f-375">Visi pārējie konti, kas nav atlikumu konti, tiek ignorēti.</span><span class="sxs-lookup"><span data-stu-id="9a00f-375">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="9a00f-376">Adreses informācija</span><span class="sxs-lookup"><span data-stu-id="9a00f-376">Address information</span></span>

<span data-ttu-id="9a00f-377">Katram darbiniekam ir jābūt vienai primārajai vietai.</span><span class="sxs-lookup"><span data-stu-id="9a00f-377">Every employee must have one primary location.</span></span> <span data-ttu-id="9a00f-378">Pakalpojumā Dayforce šī vieta tiek izmantota, lai nodokļu piemērošanas nolūkos noteiktu darbinieka primāro dzīvesvietu.</span><span class="sxs-lookup"><span data-stu-id="9a00f-378">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="9a00f-379">Primārā (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-379">Primary (required)</span></span>
- <span data-ttu-id="9a00f-380">Valsts/reģions (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-380">Country/region (required)</span></span>
- <span data-ttu-id="9a00f-381">Pasta indekss (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-381">Zip/postal code (required)</span></span>
- <span data-ttu-id="9a00f-382">Iela (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-382">Street (required)</span></span>
- <span data-ttu-id="9a00f-383">Ielas numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-383">Street Number (required)</span></span>
- <span data-ttu-id="9a00f-384">Mājas numurs/nosaukums</span><span class="sxs-lookup"><span data-stu-id="9a00f-384">Building Complement</span></span>
- <span data-ttu-id="9a00f-385">Pilsēta (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-385">City (required)</span></span>
- <span data-ttu-id="9a00f-386">Administratīvais apgabals (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-386">State (required)</span></span>
- <span data-ttu-id="9a00f-387">Apgabals (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-387">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="9a00f-388">Datu konfigurēšana algu ģenerēšanai Amerikas Savienotajās Valstīs un Kanādā</span><span class="sxs-lookup"><span data-stu-id="9a00f-388">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="9a00f-389">Ja ģenerējat algas darbiniekiem Amerikas Savienotajās Valstīs un Kanādā, ir jākonfigurē tālāk norādītie elementi.</span><span class="sxs-lookup"><span data-stu-id="9a00f-389">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="9a00f-390">Amatiem ir jānorāda nodaļas.</span><span class="sxs-lookup"><span data-stu-id="9a00f-390">Departments are required on positions.</span></span>
- <span data-ttu-id="9a00f-391">Izmaksu centri ir jāiestata kā finanšu dimensijas, un tiem ir jābūt pirmajiem elementiem noklusējuma finanšu dimensijas virknē.</span><span class="sxs-lookup"><span data-stu-id="9a00f-391">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="9a00f-392">Varat konfigurēt Talent, lai amatiem būtu jānorāda nodaļa.</span><span class="sxs-lookup"><span data-stu-id="9a00f-392">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="9a00f-393">Lai to izdarītu, pārejiet uz **Personāla vadības kopīgotie amati > Amati > Pieprasīt amatiem nodaļas**.</span><span class="sxs-lookup"><span data-stu-id="9a00f-393">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="9a00f-394">Ieteicams piemērot šo iestatījumu integrācijai.</span><span class="sxs-lookup"><span data-stu-id="9a00f-394">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="9a00f-395">Darba tipi</span><span class="sxs-lookup"><span data-stu-id="9a00f-395">Job types</span></span>

<span data-ttu-id="9a00f-396">Darbu veidi tiek izmantoti, lai līdzīgus darbus grupētu kategorijās.</span><span class="sxs-lookup"><span data-stu-id="9a00f-396">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="9a00f-397">Darbu veidi ir nepieciešami, lai apstrādātu algas Amerikas Savienotajās Valstīs un Kanādā.</span><span class="sxs-lookup"><span data-stu-id="9a00f-397">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="9a00f-398">Daži darbu veidu piemēri ir pilna laika, nepilna laika, algots un stundu apmaksas darbs.</span><span class="sxs-lookup"><span data-stu-id="9a00f-398">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="9a00f-399">Darbu veidi tiek kartēti uz pakalpojumu Dayforce kā apmaksas tipi, lai norādītu, vai darbinieks saņem stundas samaksu vai algu.</span><span class="sxs-lookup"><span data-stu-id="9a00f-399">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="9a00f-400">Ir jānorāda tālāk norādītie darbu veidi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="9a00f-400">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="9a00f-401">Darba veids</span><span class="sxs-lookup"><span data-stu-id="9a00f-401">Job type</span></span>   | <span data-ttu-id="9a00f-402">apraksts</span><span class="sxs-lookup"><span data-stu-id="9a00f-402">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="9a00f-403">Ik stundu</span><span class="sxs-lookup"><span data-stu-id="9a00f-403">Hourly</span></span>     | <span data-ttu-id="9a00f-404">Ik stundu</span><span class="sxs-lookup"><span data-stu-id="9a00f-404">Hourly</span></span>      |
| <span data-ttu-id="9a00f-405">Algots</span><span class="sxs-lookup"><span data-stu-id="9a00f-405">Salaried</span></span>   | <span data-ttu-id="9a00f-406">Algots</span><span class="sxs-lookup"><span data-stu-id="9a00f-406">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="9a00f-407">Amatu veidi</span><span class="sxs-lookup"><span data-stu-id="9a00f-407">Position types</span></span> 

<span data-ttu-id="9a00f-408">Amatu veidus izmanto, lai norādītu, vai amats ir pilna laika, nepilna laika vai cita veida darbs.</span><span class="sxs-lookup"><span data-stu-id="9a00f-408">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="9a00f-409">Amatu veidi tiek kartēti uz pakalpojumu Dayforce kā apmaksas klases, lai norādītu, vai darbinieks ir pilna laika vai nepilna laika darbinieks.</span><span class="sxs-lookup"><span data-stu-id="9a00f-409">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="9a00f-410">Ir jānorāda tālāk norādītie amatu veidi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="9a00f-410">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="9a00f-411">Amata tips</span><span class="sxs-lookup"><span data-stu-id="9a00f-411">Position type</span></span>   | <span data-ttu-id="9a00f-412">apraksts</span><span class="sxs-lookup"><span data-stu-id="9a00f-412">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="9a00f-413">Pilna laika</span><span class="sxs-lookup"><span data-stu-id="9a00f-413">Full-time</span></span>       | <span data-ttu-id="9a00f-414">Pilna laika darbinieks</span><span class="sxs-lookup"><span data-stu-id="9a00f-414">Full time employee</span></span> |
| <span data-ttu-id="9a00f-415">Nepilna laika</span><span class="sxs-lookup"><span data-stu-id="9a00f-415">Part-time</span></span>       | <span data-ttu-id="9a00f-416">Nepilna laika darbinieks</span><span class="sxs-lookup"><span data-stu-id="9a00f-416">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="9a00f-417">Iemeslu kodi</span><span class="sxs-lookup"><span data-stu-id="9a00f-417">Reason codes</span></span>

<span data-ttu-id="9a00f-418">Iemeslu kodi sniedz informāciju par darbinieka statusu.</span><span class="sxs-lookup"><span data-stu-id="9a00f-418">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="9a00f-419">Iemeslu kodu tiek kartēti uz pakalpojumu Dayforce kā statusa iemesli, kas norāda darbinieka amata vai nodarbinātības statusa izmaiņu iemeslu.</span><span class="sxs-lookup"><span data-stu-id="9a00f-419">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="9a00f-420">Ir jānorāda tālāk norādītie iemeslu kodi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="9a00f-420">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="9a00f-421">Iemeslu kodi</span><span class="sxs-lookup"><span data-stu-id="9a00f-421">Reason code</span></span>    | <span data-ttu-id="9a00f-422">apraksts</span><span class="sxs-lookup"><span data-stu-id="9a00f-422">Description</span></span>      | <span data-ttu-id="9a00f-423">Piemērojamie scenāriji</span><span class="sxs-lookup"><span data-stu-id="9a00f-423">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="9a00f-424">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="9a00f-424">RESIGNATION</span></span>    | <span data-ttu-id="9a00f-425">Atlūgums</span><span class="sxs-lookup"><span data-stu-id="9a00f-425">Resignation</span></span>      | <span data-ttu-id="9a00f-426">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="9a00f-426">Terminate worker</span></span>     |
| <span data-ttu-id="9a00f-427">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="9a00f-427">TERMINATION</span></span>    | <span data-ttu-id="9a00f-428">Izbeigšana</span><span class="sxs-lookup"><span data-stu-id="9a00f-428">Termination</span></span>      | <span data-ttu-id="9a00f-429">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="9a00f-429">Terminate worker</span></span>     |
| <span data-ttu-id="9a00f-430">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="9a00f-430">RETIREMENT</span></span>     | <span data-ttu-id="9a00f-431">Aiziešana pensijā</span><span class="sxs-lookup"><span data-stu-id="9a00f-431">Retirement</span></span>       | <span data-ttu-id="9a00f-432">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="9a00f-432">Terminate worker</span></span>     |
| <span data-ttu-id="9a00f-433">CITI</span><span class="sxs-lookup"><span data-stu-id="9a00f-433">OTHER</span></span>          | <span data-ttu-id="9a00f-434">Citi iemesli</span><span class="sxs-lookup"><span data-stu-id="9a00f-434">Other Reasons</span></span>    | <span data-ttu-id="9a00f-435">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="9a00f-435">Terminate worker</span></span>     |
| <span data-ttu-id="9a00f-436">DEATH</span><span class="sxs-lookup"><span data-stu-id="9a00f-436">DEATH</span></span>          | <span data-ttu-id="9a00f-437">Nāve</span><span class="sxs-lookup"><span data-stu-id="9a00f-437">Death</span></span>            | <span data-ttu-id="9a00f-438">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="9a00f-438">Terminate worker</span></span>     |
| <span data-ttu-id="9a00f-439">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="9a00f-439">LEAVEOFABSENCE</span></span> | <span data-ttu-id="9a00f-440">Atvaļinājums</span><span class="sxs-lookup"><span data-stu-id="9a00f-440">Leave of Absence</span></span> | <span data-ttu-id="9a00f-441">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="9a00f-441">Terminate worker</span></span>     |
| <span data-ttu-id="9a00f-442">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="9a00f-442">CONTRACTEND</span></span>    | <span data-ttu-id="9a00f-443">Līguma beigas</span><span class="sxs-lookup"><span data-stu-id="9a00f-443">End of Contract</span></span>  | <span data-ttu-id="9a00f-444">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="9a00f-444">Terminate worker</span></span>     |
| <span data-ttu-id="9a00f-445">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="9a00f-445">SALARYCHANGE</span></span>   | <span data-ttu-id="9a00f-446">Algas izmaiņas</span><span class="sxs-lookup"><span data-stu-id="9a00f-446">Change of Salary</span></span> | <span data-ttu-id="9a00f-447">Atlīdzība</span><span class="sxs-lookup"><span data-stu-id="9a00f-447">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="9a00f-448">Ģimenes stāvoklis</span><span class="sxs-lookup"><span data-stu-id="9a00f-448">Marital status</span></span>

<span data-ttu-id="9a00f-449">Ģimenes statusa vērtības tiek kartētas uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkotas uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="9a00f-449">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="9a00f-450">Tālāk esošajā tabulā ir parādīts, kā ģimenes statusa vērtības tiek kartētas uz pakalpojumu Dayforce.</span><span class="sxs-lookup"><span data-stu-id="9a00f-450">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="9a00f-451">Talent</span><span class="sxs-lookup"><span data-stu-id="9a00f-451">Talent</span></span>                 | <span data-ttu-id="9a00f-452">Dayforce</span><span class="sxs-lookup"><span data-stu-id="9a00f-452">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="9a00f-453">Precējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="9a00f-453">Married</span></span>                | <span data-ttu-id="9a00f-454">Precējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="9a00f-454">Married</span></span>              |
| <span data-ttu-id="9a00f-455">Neprecējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="9a00f-455">Single</span></span>                 | <span data-ttu-id="9a00f-456">Neprecējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="9a00f-456">Single</span></span>               |
| <span data-ttu-id="9a00f-457">Atraitnis</span><span class="sxs-lookup"><span data-stu-id="9a00f-457">Widowed</span></span>                | <span data-ttu-id="9a00f-458">Atraitnis</span><span class="sxs-lookup"><span data-stu-id="9a00f-458">Widowed</span></span>              |
| <span data-ttu-id="9a00f-459">Šķīries (-usies)</span><span class="sxs-lookup"><span data-stu-id="9a00f-459">Divorced</span></span>               | <span data-ttu-id="9a00f-460">Šķīries (-usies)</span><span class="sxs-lookup"><span data-stu-id="9a00f-460">Divorced</span></span>             |
| <span data-ttu-id="9a00f-461">Reģistrētas attiecības</span><span class="sxs-lookup"><span data-stu-id="9a00f-461">Registered Partnership</span></span> | <span data-ttu-id="9a00f-462">Dzīvesbiedrs</span><span class="sxs-lookup"><span data-stu-id="9a00f-462">Domestic Partnership</span></span> |
| <span data-ttu-id="9a00f-463">Neviens</span><span class="sxs-lookup"><span data-stu-id="9a00f-463">None</span></span>                   | <span data-ttu-id="9a00f-464">Neviens</span><span class="sxs-lookup"><span data-stu-id="9a00f-464">None</span></span>                 |
| <span data-ttu-id="9a00f-465">Kopdzīve</span><span class="sxs-lookup"><span data-stu-id="9a00f-465">Cohabiting</span></span>             | <span data-ttu-id="9a00f-466">Kopdzīve</span><span class="sxs-lookup"><span data-stu-id="9a00f-466">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="9a00f-467">Dzimums</span><span class="sxs-lookup"><span data-stu-id="9a00f-467">Gender</span></span>

<span data-ttu-id="9a00f-468">Dzimuma apzīmējumi tiek kartēti uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkoti uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="9a00f-468">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="9a00f-469">Tālāk esošajā tabulā ir parādīts, kā dzimuma apzīmējumi tiek kartēti uz pakalpojumu Dayforce.</span><span class="sxs-lookup"><span data-stu-id="9a00f-469">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="9a00f-470">Talent</span><span class="sxs-lookup"><span data-stu-id="9a00f-470">Talent</span></span>       | <span data-ttu-id="9a00f-471">Dayforce</span><span class="sxs-lookup"><span data-stu-id="9a00f-471">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="9a00f-472">Vīrietis</span><span class="sxs-lookup"><span data-stu-id="9a00f-472">Male</span></span>         | <span data-ttu-id="9a00f-473">Vīrietis</span><span class="sxs-lookup"><span data-stu-id="9a00f-473">Male</span></span>            |
| <span data-ttu-id="9a00f-474">Sieviete</span><span class="sxs-lookup"><span data-stu-id="9a00f-474">Female</span></span>       | <span data-ttu-id="9a00f-475">Sieviete</span><span class="sxs-lookup"><span data-stu-id="9a00f-475">Female</span></span>          |
| <span data-ttu-id="9a00f-476">Nav specifisks</span><span class="sxs-lookup"><span data-stu-id="9a00f-476">Non-specific</span></span> | <span data-ttu-id="9a00f-477">*Netiek atbalstīts*</span><span class="sxs-lookup"><span data-stu-id="9a00f-477">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="9a00f-478">Ienākumu veida kodi</span><span class="sxs-lookup"><span data-stu-id="9a00f-478">Earning codes</span></span>

<span data-ttu-id="9a00f-479">Ienākumu veidu kodi unikāli identificē katra veida ienākumus, ko saņem nodarbinātie.</span><span class="sxs-lookup"><span data-stu-id="9a00f-479">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="9a00f-480">Kodiem ir vairāki ar ienākumiem saistīti parametri, piemēram, uzskaites nosacījumi, nodokļu likumi, pārskatu veidošanas prasības un bruto summas palielināšanas iespēja.</span><span class="sxs-lookup"><span data-stu-id="9a00f-480">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="9a00f-481">Ja tiek izmantota neatbalstīta biežuma vērtība, aprēķinā pēc noklusējuma tiek lietota biežuma vērtība **Katra apmaksa**.</span><span class="sxs-lookup"><span data-stu-id="9a00f-481">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="9a00f-482">Atbalstītās biežuma vērtības</span><span class="sxs-lookup"><span data-stu-id="9a00f-482">Supported frequencies</span></span>

- <span data-ttu-id="9a00f-483">Visus</span><span class="sxs-lookup"><span data-stu-id="9a00f-483">All</span></span>
- <span data-ttu-id="9a00f-484">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="9a00f-484">EVERYPAY</span></span>
- <span data-ttu-id="9a00f-485">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="9a00f-485">EACHPAYPERIOD</span></span>
- <span data-ttu-id="9a00f-486">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="9a00f-486">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="9a00f-487">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="9a00f-487">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="9a00f-488">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="9a00f-488">1OFMTH</span></span>
- <span data-ttu-id="9a00f-489">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="9a00f-489">LASTOFMTH</span></span>
- <span data-ttu-id="9a00f-490">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="9a00f-490">2OFMTH</span></span>
- <span data-ttu-id="9a00f-491">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="9a00f-491">3OFMTH</span></span>
- <span data-ttu-id="9a00f-492">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9a00f-492">4OFMTH</span></span>
- <span data-ttu-id="9a00f-493">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="9a00f-493">5OFMTH</span></span>
- <span data-ttu-id="9a00f-494">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="9a00f-494">1N2OFMTH</span></span>
- <span data-ttu-id="9a00f-495">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9a00f-495">3N4OFMTH</span></span>
- <span data-ttu-id="9a00f-496">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="9a00f-496">1N3OFMTH</span></span>
- <span data-ttu-id="9a00f-497">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9a00f-497">1N4OFMTH</span></span>
- <span data-ttu-id="9a00f-498">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="9a00f-498">2N3OFMTH</span></span>
- <span data-ttu-id="9a00f-499">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9a00f-499">2N4OFMTH</span></span>
- <span data-ttu-id="9a00f-500">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="9a00f-500">1N2N3OFMTH</span></span>
- <span data-ttu-id="9a00f-501">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9a00f-501">1N2N4OFMTH</span></span>
- <span data-ttu-id="9a00f-502">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9a00f-502">1N3N4OFMTH</span></span>
- <span data-ttu-id="9a00f-503">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9a00f-503">2N3N4OFMTH</span></span>
- <span data-ttu-id="9a00f-504">1N2N3N4OFMTH–1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9a00f-504">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="9a00f-505">2N3N4N5OFMth–2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="9a00f-505">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="9a00f-506">1OFQTR–1OFQTR</span><span class="sxs-lookup"><span data-stu-id="9a00f-506">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="9a00f-507">LASTOFQTR–LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="9a00f-507">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="9a00f-508">LASTMTHOFQTR–LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="9a00f-508">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="9a00f-509">1OFYEAR–1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="9a00f-509">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="9a00f-510">LASTOFYEAR–LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="9a00f-510">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="9a00f-511">NOVNDECOFYEAR–NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="9a00f-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="9a00f-512">Adreses</span><span class="sxs-lookup"><span data-stu-id="9a00f-512">Addresses</span></span>

<span data-ttu-id="9a00f-513">Noteiktas valsts vai reģiona, administratīvā apgabala un apgabala (pašvaldības) kodu identifikācijai ir nepieciešami konkrēti formāti, ko var atpazīt pakalpojums Dayforce un valsts/reģiona pakalpojumu sniedzēji.</span><span class="sxs-lookup"><span data-stu-id="9a00f-513">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="9a00f-514">Lai gan pilsētu formāts var būt dažāds, katrai pilsētai ir jābūt saistītai ar administratīvo apgabalu.</span><span class="sxs-lookup"><span data-stu-id="9a00f-514">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="9a00f-515">Talent</span><span class="sxs-lookup"><span data-stu-id="9a00f-515">Talent</span></span>          | <span data-ttu-id="9a00f-516">Dayforce</span><span class="sxs-lookup"><span data-stu-id="9a00f-516">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="9a00f-517">Valsts/reģions</span><span class="sxs-lookup"><span data-stu-id="9a00f-517">Country/Region</span></span>  | <span data-ttu-id="9a00f-518">Valsts kods</span><span class="sxs-lookup"><span data-stu-id="9a00f-518">Country Code</span></span>          |
| <span data-ttu-id="9a00f-519">Pasta indekss</span><span class="sxs-lookup"><span data-stu-id="9a00f-519">Zip/Postal Code</span></span> | <span data-ttu-id="9a00f-520">Pasta indekss</span><span class="sxs-lookup"><span data-stu-id="9a00f-520">Postal Code</span></span>           |
| <span data-ttu-id="9a00f-521">Administratīvais apgabals</span><span class="sxs-lookup"><span data-stu-id="9a00f-521">State</span></span>           | <span data-ttu-id="9a00f-522">Administratīvā apgabala kods</span><span class="sxs-lookup"><span data-stu-id="9a00f-522">State Code</span></span>            |
| <span data-ttu-id="9a00f-523">Pilsēta</span><span class="sxs-lookup"><span data-stu-id="9a00f-523">City</span></span>            | <span data-ttu-id="9a00f-524">Pilsēta</span><span class="sxs-lookup"><span data-stu-id="9a00f-524">City</span></span>                  |
| <span data-ttu-id="9a00f-525">Apgabals</span><span class="sxs-lookup"><span data-stu-id="9a00f-525">County</span></span>          | <span data-ttu-id="9a00f-526">Apgabals (pašvaldība)</span><span class="sxs-lookup"><span data-stu-id="9a00f-526">County (Municipality)</span></span> |
| <span data-ttu-id="9a00f-527">Iela</span><span class="sxs-lookup"><span data-stu-id="9a00f-527">Street</span></span>          | <span data-ttu-id="9a00f-528">Adreses 1. rinda</span><span class="sxs-lookup"><span data-stu-id="9a00f-528">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="9a00f-529">Nodokļu reģioni</span><span class="sxs-lookup"><span data-stu-id="9a00f-529">Tax regions</span></span>

<span data-ttu-id="9a00f-530">Nodokļu reģionus izmanto, lai noteiktu atbilstošos nodokļus, kas jāpiemēro, ģenerējot algu aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="9a00f-530">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="9a00f-531">Nodokļu reģioni tiek kartēti uz pakalpojumu Dayforce kā vietas adreses.</span><span class="sxs-lookup"><span data-stu-id="9a00f-531">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="9a00f-532">Noklusējuma nodokļu reģionam ir jābūt saistītam ar nodarbinātā aktīvo amatu.</span><span class="sxs-lookup"><span data-stu-id="9a00f-532">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="9a00f-533">Nodokļu reģions (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-533">Tax region (required)</span></span>
- <span data-ttu-id="9a00f-534">Valsts/reģions (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-534">Country/Region (required)</span></span>
- <span data-ttu-id="9a00f-535">Administratīvais apgabals (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-535">State (required)</span></span>
- <span data-ttu-id="9a00f-536">Apgabals</span><span class="sxs-lookup"><span data-stu-id="9a00f-536">County</span></span> 
- <span data-ttu-id="9a00f-537">Pilsēta (obligāti)</span><span class="sxs-lookup"><span data-stu-id="9a00f-537">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="9a00f-538">Datu konfigurēšana algu aprēķina ģenerēšanai Meksikā</span><span class="sxs-lookup"><span data-stu-id="9a00f-538">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="9a00f-539">Ja ģenerējat algas darbiniekiem Meksikā, ir jākonfigurē tālāk norādītie elementi.</span><span class="sxs-lookup"><span data-stu-id="9a00f-539">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="9a00f-540">Amatiem ir jānorāda nodaļas.</span><span class="sxs-lookup"><span data-stu-id="9a00f-540">Departments are required on positions.</span></span>
- <span data-ttu-id="9a00f-541">Izmaksu centri ir jāiestata kā finanšu dimensijas, un tiem ir jābūt pirmajiem elementiem noklusējuma finanšu dimensijas virknē.</span><span class="sxs-lookup"><span data-stu-id="9a00f-541">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="9a00f-542">Darba tipi</span><span class="sxs-lookup"><span data-stu-id="9a00f-542">Job types</span></span>

<span data-ttu-id="9a00f-543">Darbu veidi tiek izmantoti, lai līdzīgus darbus grupētu kategorijās.</span><span class="sxs-lookup"><span data-stu-id="9a00f-543">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="9a00f-544">Lai apstrādātu algas Meksikā, ir nepieciešami darbu veidi.</span><span class="sxs-lookup"><span data-stu-id="9a00f-544">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="9a00f-545">Daži darbu veidu piemēri ir pilna laika, nepilna laika, algots un stundu apmaksas darbs.</span><span class="sxs-lookup"><span data-stu-id="9a00f-545">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="9a00f-546">Darbu veidi tiek kartēti uz pakalpojumu Dayforce kā apmaksas tipi, lai norādītu, vai darbinieks saņem stundas samaksu vai algu.</span><span class="sxs-lookup"><span data-stu-id="9a00f-546">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="9a00f-547">Ir jānorāda tālāk norādītie darbu veidi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="9a00f-547">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="9a00f-548">Darba veids</span><span class="sxs-lookup"><span data-stu-id="9a00f-548">Job type</span></span>   | <span data-ttu-id="9a00f-549">apraksts</span><span class="sxs-lookup"><span data-stu-id="9a00f-549">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="9a00f-550">Ik stundu</span><span class="sxs-lookup"><span data-stu-id="9a00f-550">Hourly</span></span>     | <span data-ttu-id="9a00f-551">Stundu (MX)</span><span class="sxs-lookup"><span data-stu-id="9a00f-551">MX Hourly</span></span>   |
| <span data-ttu-id="9a00f-552">Algots</span><span class="sxs-lookup"><span data-stu-id="9a00f-552">Salaried</span></span>   | <span data-ttu-id="9a00f-553">Algots (MX)</span><span class="sxs-lookup"><span data-stu-id="9a00f-553">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="9a00f-554">Amatu veidi</span><span class="sxs-lookup"><span data-stu-id="9a00f-554">Position types</span></span> 

<span data-ttu-id="9a00f-555">Amatu veidus izmanto, lai norādītu, vai amats ir pilna laika, nepilna laika vai cita veida darbs.</span><span class="sxs-lookup"><span data-stu-id="9a00f-555">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="9a00f-556">Amatu veidi tiek kartēti uz pakalpojumu Dayforce kā apmaksas klases, lai norādītu, vai darbinieks ir pilna laika vai nepilna laika darbinieks.</span><span class="sxs-lookup"><span data-stu-id="9a00f-556">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="9a00f-557">Ir jānorāda tālāk norādītie amatu veidi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="9a00f-557">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="9a00f-558">Amata tips</span><span class="sxs-lookup"><span data-stu-id="9a00f-558">Position type</span></span>   | <span data-ttu-id="9a00f-559">apraksts</span><span class="sxs-lookup"><span data-stu-id="9a00f-559">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="9a00f-560">Pilna laika</span><span class="sxs-lookup"><span data-stu-id="9a00f-560">Full-time</span></span>       | <span data-ttu-id="9a00f-561">Pilna laika darbinieks</span><span class="sxs-lookup"><span data-stu-id="9a00f-561">Full time employee</span></span> |
| <span data-ttu-id="9a00f-562">Nepilna laika</span><span class="sxs-lookup"><span data-stu-id="9a00f-562">Part-time</span></span>       | <span data-ttu-id="9a00f-563">Nepilna laika darbinieks</span><span class="sxs-lookup"><span data-stu-id="9a00f-563">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="9a00f-564">Iemeslu kodi</span><span class="sxs-lookup"><span data-stu-id="9a00f-564">Reason codes</span></span>

<span data-ttu-id="9a00f-565">Iemeslu kodi sniedz informāciju par darbinieka statusu.</span><span class="sxs-lookup"><span data-stu-id="9a00f-565">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="9a00f-566">Iemeslu kodu tiek kartēti uz pakalpojumu Dayforce kā statusa iemesli, kas norāda darbinieka amata vai nodarbinātības statusa izmaiņu iemeslu.</span><span class="sxs-lookup"><span data-stu-id="9a00f-566">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="9a00f-567">Ir jānorāda tālāk norādītie iemeslu kodi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="9a00f-567">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="9a00f-568">Iemeslu kodi</span><span class="sxs-lookup"><span data-stu-id="9a00f-568">Reason code</span></span>            | <span data-ttu-id="9a00f-569">apraksts</span><span class="sxs-lookup"><span data-stu-id="9a00f-569">Description</span></span>                    | <span data-ttu-id="9a00f-570">Piemērojamie scenāriji</span><span class="sxs-lookup"><span data-stu-id="9a00f-570">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="9a00f-571">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="9a00f-571">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="9a00f-572">Aiziešana no amata pirms pirmās algas</span><span class="sxs-lookup"><span data-stu-id="9a00f-572">Departure before first payroll</span></span> | <span data-ttu-id="9a00f-573">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="9a00f-573">Terminate worker</span></span>     |
| <span data-ttu-id="9a00f-574">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="9a00f-574">RESIGNATION</span></span>            | <span data-ttu-id="9a00f-575">Atlūgums</span><span class="sxs-lookup"><span data-stu-id="9a00f-575">Resignation</span></span>                    | <span data-ttu-id="9a00f-576">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="9a00f-576">Terminate worker</span></span>     |
| <span data-ttu-id="9a00f-577">PENSION</span><span class="sxs-lookup"><span data-stu-id="9a00f-577">PENSION</span></span>                | <span data-ttu-id="9a00f-578">Pensija</span><span class="sxs-lookup"><span data-stu-id="9a00f-578">Pension</span></span>                        | <span data-ttu-id="9a00f-579">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="9a00f-579">Terminate worker</span></span>     |
| <span data-ttu-id="9a00f-580">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="9a00f-580">TERMINATION</span></span>            | <span data-ttu-id="9a00f-581">Izbeigšana</span><span class="sxs-lookup"><span data-stu-id="9a00f-581">Termination</span></span>                    | <span data-ttu-id="9a00f-582">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="9a00f-582">Terminate worker</span></span>     |
| <span data-ttu-id="9a00f-583">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="9a00f-583">RETIREMENT</span></span>             | <span data-ttu-id="9a00f-584">Aiziešana pensijā</span><span class="sxs-lookup"><span data-stu-id="9a00f-584">Retirement</span></span>                     | <span data-ttu-id="9a00f-585">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="9a00f-585">Terminate worker</span></span>     |
| <span data-ttu-id="9a00f-586">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="9a00f-586">ABSENTEE</span></span>               | <span data-ttu-id="9a00f-587">Darba kavētājs</span><span class="sxs-lookup"><span data-stu-id="9a00f-587">Absentee</span></span>                       | <span data-ttu-id="9a00f-588">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="9a00f-588">Terminate worker</span></span>     |
| <span data-ttu-id="9a00f-589">CITI</span><span class="sxs-lookup"><span data-stu-id="9a00f-589">OTHER</span></span>                  | <span data-ttu-id="9a00f-590">Citi iemesli</span><span class="sxs-lookup"><span data-stu-id="9a00f-590">Other Reasons</span></span>                  | <span data-ttu-id="9a00f-591">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="9a00f-591">Terminate worker</span></span>     |
| <span data-ttu-id="9a00f-592">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="9a00f-592">CLOSURE</span></span>                | <span data-ttu-id="9a00f-593">Uzņēmuma slēgšana</span><span class="sxs-lookup"><span data-stu-id="9a00f-593">Business Closure</span></span>               | <span data-ttu-id="9a00f-594">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="9a00f-594">Terminate worker</span></span>     |
| <span data-ttu-id="9a00f-595">DEATH</span><span class="sxs-lookup"><span data-stu-id="9a00f-595">DEATH</span></span>                  | <span data-ttu-id="9a00f-596">Nāve</span><span class="sxs-lookup"><span data-stu-id="9a00f-596">Death</span></span>                          | <span data-ttu-id="9a00f-597">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="9a00f-597">Terminate worker</span></span>     |
| <span data-ttu-id="9a00f-598">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="9a00f-598">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="9a00f-599">Atvaļinājums</span><span class="sxs-lookup"><span data-stu-id="9a00f-599">Leave of Absence</span></span>               | <span data-ttu-id="9a00f-600">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="9a00f-600">Terminate worker</span></span>     |
| <span data-ttu-id="9a00f-601">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="9a00f-601">CONTRACTEND</span></span>            | <span data-ttu-id="9a00f-602">Līguma beigas</span><span class="sxs-lookup"><span data-stu-id="9a00f-602">End of Contract</span></span>                | <span data-ttu-id="9a00f-603">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="9a00f-603">Terminate worker</span></span>     |
| <span data-ttu-id="9a00f-604">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="9a00f-604">SALARYCHANGE</span></span>           | <span data-ttu-id="9a00f-605">Algas izmaiņas</span><span class="sxs-lookup"><span data-stu-id="9a00f-605">Change of Salary</span></span>               | <span data-ttu-id="9a00f-606">Atlīdzība</span><span class="sxs-lookup"><span data-stu-id="9a00f-606">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="9a00f-607">Nodarbinātības noteikumi</span><span class="sxs-lookup"><span data-stu-id="9a00f-607">Terms of employment</span></span>

<span data-ttu-id="9a00f-608">Nodarbinātības noteikumus izmanto, lai izveidotu nodarbinātības noteikumu kategorijas.</span><span class="sxs-lookup"><span data-stu-id="9a00f-608">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="9a00f-609">Noteikumi tiek kartēti uz pakalpojumu Dayforce kā nodarbinātības rādītāju vērtības.</span><span class="sxs-lookup"><span data-stu-id="9a00f-609">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="9a00f-610">Ir nepieciešami tālāk norādītie nodarbinātības noteikumi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="9a00f-610">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="9a00f-611">Nodarbinātības noteikumi</span><span class="sxs-lookup"><span data-stu-id="9a00f-611">Terms of employment</span></span>   | <span data-ttu-id="9a00f-612">apraksts</span><span class="sxs-lookup"><span data-stu-id="9a00f-612">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="9a00f-613">Regulārs</span><span class="sxs-lookup"><span data-stu-id="9a00f-613">Regular</span></span>               | <span data-ttu-id="9a00f-614">Regulārs</span><span class="sxs-lookup"><span data-stu-id="9a00f-614">Regular</span></span>     |
| <span data-ttu-id="9a00f-615">Tieši</span><span class="sxs-lookup"><span data-stu-id="9a00f-615">Direct</span></span>                | <span data-ttu-id="9a00f-616">Tieši</span><span class="sxs-lookup"><span data-stu-id="9a00f-616">Direct</span></span>      |
| <span data-ttu-id="9a00f-617">Štažēšanās</span><span class="sxs-lookup"><span data-stu-id="9a00f-617">Internship</span></span>            | <span data-ttu-id="9a00f-618">Štažēšanās</span><span class="sxs-lookup"><span data-stu-id="9a00f-618">Internship</span></span>  |
| <span data-ttu-id="9a00f-619">Pastāvīga</span><span class="sxs-lookup"><span data-stu-id="9a00f-619">Permanent</span></span>             | <span data-ttu-id="9a00f-620">Pastāvīga</span><span class="sxs-lookup"><span data-stu-id="9a00f-620">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="9a00f-621">Ģimenes stāvoklis</span><span class="sxs-lookup"><span data-stu-id="9a00f-621">Marital status</span></span>

<span data-ttu-id="9a00f-622">Ģimenes statusa vērtības tiek kartētas uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkotas uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="9a00f-622">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="9a00f-623">Tālāk esošajā tabulā ir parādīts, kā ģimenes statusa vērtības tiek kartētas uz pakalpojumu Dayforce.</span><span class="sxs-lookup"><span data-stu-id="9a00f-623">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="9a00f-624">Talent</span><span class="sxs-lookup"><span data-stu-id="9a00f-624">Talent</span></span>                 | <span data-ttu-id="9a00f-625">Dayforce</span><span class="sxs-lookup"><span data-stu-id="9a00f-625">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="9a00f-626">Precējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="9a00f-626">Married</span></span>                | <span data-ttu-id="9a00f-627">Precējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="9a00f-627">Married</span></span>                   |
| <span data-ttu-id="9a00f-628">Neprecējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="9a00f-628">Single</span></span>                 | <span data-ttu-id="9a00f-629">Neprecējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="9a00f-629">Single</span></span>                    |
| <span data-ttu-id="9a00f-630">Atraitnis</span><span class="sxs-lookup"><span data-stu-id="9a00f-630">Widowed</span></span>                | <span data-ttu-id="9a00f-631">Atraitnis</span><span class="sxs-lookup"><span data-stu-id="9a00f-631">Widowed</span></span>                   |
| <span data-ttu-id="9a00f-632">Šķīries (-usies)</span><span class="sxs-lookup"><span data-stu-id="9a00f-632">Divorced</span></span>               | <span data-ttu-id="9a00f-633">Šķīries (-usies)</span><span class="sxs-lookup"><span data-stu-id="9a00f-633">Divorced</span></span>                  |
| <span data-ttu-id="9a00f-634">Reģistrētas attiecības</span><span class="sxs-lookup"><span data-stu-id="9a00f-634">Registered Partnership</span></span> | <span data-ttu-id="9a00f-635">Dzīvesbiedrs</span><span class="sxs-lookup"><span data-stu-id="9a00f-635">Domestic Partnership</span></span>      |
| <span data-ttu-id="9a00f-636">Neviens</span><span class="sxs-lookup"><span data-stu-id="9a00f-636">None</span></span>                   | <span data-ttu-id="9a00f-637">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="9a00f-637">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="9a00f-638">Kopdzīve</span><span class="sxs-lookup"><span data-stu-id="9a00f-638">Cohabiting</span></span>             | <span data-ttu-id="9a00f-639">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="9a00f-639">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="9a00f-640">Dzimums</span><span class="sxs-lookup"><span data-stu-id="9a00f-640">Gender</span></span>

<span data-ttu-id="9a00f-641">Dzimuma apzīmējumi tiek kartēti uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkoti uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="9a00f-641">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="9a00f-642">Tālāk esošajā tabulā ir parādīts, kā dzimuma apzīmējumi tiek kartēti uz pakalpojumu Dayforce.</span><span class="sxs-lookup"><span data-stu-id="9a00f-642">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="9a00f-643">Talent</span><span class="sxs-lookup"><span data-stu-id="9a00f-643">Talent</span></span>       | <span data-ttu-id="9a00f-644">Dayforce</span><span class="sxs-lookup"><span data-stu-id="9a00f-644">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="9a00f-645">Vīrietis</span><span class="sxs-lookup"><span data-stu-id="9a00f-645">Male</span></span>         | <span data-ttu-id="9a00f-646">Vīrietis</span><span class="sxs-lookup"><span data-stu-id="9a00f-646">Male</span></span>                      |
| <span data-ttu-id="9a00f-647">Sieviete</span><span class="sxs-lookup"><span data-stu-id="9a00f-647">Female</span></span>       | <span data-ttu-id="9a00f-648">Sieviete</span><span class="sxs-lookup"><span data-stu-id="9a00f-648">Female</span></span>                    |
| <span data-ttu-id="9a00f-649">Nav specifisks</span><span class="sxs-lookup"><span data-stu-id="9a00f-649">Non-specific</span></span> | <span data-ttu-id="9a00f-650">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="9a00f-650">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="9a00f-651">Maksājumu metode</span><span class="sxs-lookup"><span data-stu-id="9a00f-651">Payment method</span></span>

<span data-ttu-id="9a00f-652">Maksāšanas metodes darbiniekam un uzņēmumam ļauj aprakstīt, kā darbinieki saņems samaksu.</span><span class="sxs-lookup"><span data-stu-id="9a00f-652">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="9a00f-653">Maksāšanas metodes tiek kartētas uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkotas uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="9a00f-653">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="9a00f-654">Tālāk esošajā tabulā ir parādīts, kā maksāšanas metodes tiek kartētas uz pakalpojumu Dayforce.</span><span class="sxs-lookup"><span data-stu-id="9a00f-654">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="9a00f-655">Talent</span><span class="sxs-lookup"><span data-stu-id="9a00f-655">Talent</span></span>             | <span data-ttu-id="9a00f-656">Dayforce</span><span class="sxs-lookup"><span data-stu-id="9a00f-656">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="9a00f-657">Kase</span><span class="sxs-lookup"><span data-stu-id="9a00f-657">Cash</span></span>               | <span data-ttu-id="9a00f-658">Kase</span><span class="sxs-lookup"><span data-stu-id="9a00f-658">Cash</span></span>                      |
| <span data-ttu-id="9a00f-659">Elektronisks maksājums</span><span class="sxs-lookup"><span data-stu-id="9a00f-659">Electronic Payment</span></span> | <span data-ttu-id="9a00f-660">Pārsūtījums</span><span class="sxs-lookup"><span data-stu-id="9a00f-660">Transfer</span></span>                  |
| <span data-ttu-id="9a00f-661">Atzīmēt</span><span class="sxs-lookup"><span data-stu-id="9a00f-661">Check</span></span>              | <span data-ttu-id="9a00f-662">Čeks</span><span class="sxs-lookup"><span data-stu-id="9a00f-662">Cheque</span></span>                    |
| <span data-ttu-id="9a00f-663">Bankas vekselis</span><span class="sxs-lookup"><span data-stu-id="9a00f-663">Bank Draft</span></span>         | <span data-ttu-id="9a00f-664">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="9a00f-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="9a00f-665">Citi</span><span class="sxs-lookup"><span data-stu-id="9a00f-665">Other</span></span>              | <span data-ttu-id="9a00f-666">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="9a00f-666">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="9a00f-667">Bankas konta tips</span><span class="sxs-lookup"><span data-stu-id="9a00f-667">Bank account type</span></span>

<span data-ttu-id="9a00f-668">Bankas kontu tipus izmanto darbiniekiem sūtāmajiem elektroniskajiem maksājumiem.</span><span class="sxs-lookup"><span data-stu-id="9a00f-668">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="9a00f-669">Bankas kontu tipi tiek kartēti uz pakalpojumu Dayforce kā pārsūtīšanas konta informācija.</span><span class="sxs-lookup"><span data-stu-id="9a00f-669">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="9a00f-670">Bankas kontu tipi integrācijas laikā tiek atbilstoši tulkoti uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="9a00f-670">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="9a00f-671">Talent</span><span class="sxs-lookup"><span data-stu-id="9a00f-671">Talent</span></span>            | <span data-ttu-id="9a00f-672">Dayforce</span><span class="sxs-lookup"><span data-stu-id="9a00f-672">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="9a00f-673">Kontroles konts</span><span class="sxs-lookup"><span data-stu-id="9a00f-673">Checking Account</span></span>  | <span data-ttu-id="9a00f-674">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="9a00f-674">CheckingAccount</span></span>           |
| <span data-ttu-id="9a00f-675">Algu konts</span><span class="sxs-lookup"><span data-stu-id="9a00f-675">Payroll Account</span></span>   | <span data-ttu-id="9a00f-676">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="9a00f-676">PayrollAccount</span></span>            |
| <span data-ttu-id="9a00f-677">Uzkrājumu konts</span><span class="sxs-lookup"><span data-stu-id="9a00f-677">Savings Account</span></span>   | <span data-ttu-id="9a00f-678">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="9a00f-678">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="9a00f-679">BankGirot konts</span><span class="sxs-lookup"><span data-stu-id="9a00f-679">BankGirot account</span></span> | <span data-ttu-id="9a00f-680">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="9a00f-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="9a00f-681">PlusGirot konts</span><span class="sxs-lookup"><span data-stu-id="9a00f-681">PlusGirot account</span></span> | <span data-ttu-id="9a00f-682">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="9a00f-682">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="9a00f-683">Ienākumu veida kodi</span><span class="sxs-lookup"><span data-stu-id="9a00f-683">Earning codes</span></span>

<span data-ttu-id="9a00f-684">Ienākumu veidu kodi unikāli identificē katra veida ienākumus, ko saņem nodarbinātie.</span><span class="sxs-lookup"><span data-stu-id="9a00f-684">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="9a00f-685">Kodiem ir vairāki ar ienākumiem saistīti parametri, piemēram, uzskaites nosacījumi, nodokļu likumi, pārskatu veidošanas prasības un bruto summas palielināšanas iespēja.</span><span class="sxs-lookup"><span data-stu-id="9a00f-685">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="9a00f-686">Ja tiek izmantota neatbalstīta biežuma vērtība, aprēķinā pēc noklusējuma tiek lietota biežuma vērtība **Katra apmaksa**.</span><span class="sxs-lookup"><span data-stu-id="9a00f-686">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="9a00f-687">Atbalstītās biežuma vērtības</span><span class="sxs-lookup"><span data-stu-id="9a00f-687">Supported frequencies</span></span>

- <span data-ttu-id="9a00f-688">Visus</span><span class="sxs-lookup"><span data-stu-id="9a00f-688">All</span></span>
- <span data-ttu-id="9a00f-689">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="9a00f-689">EVERYPAY</span></span>
- <span data-ttu-id="9a00f-690">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="9a00f-690">EACHPAYPERIOD</span></span>
- <span data-ttu-id="9a00f-691">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="9a00f-691">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="9a00f-692">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="9a00f-692">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="9a00f-693">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="9a00f-693">1OFMTH</span></span>
- <span data-ttu-id="9a00f-694">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="9a00f-694">LASTOFMTH</span></span>
- <span data-ttu-id="9a00f-695">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="9a00f-695">2OFMTH</span></span>
- <span data-ttu-id="9a00f-696">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="9a00f-696">3OFMTH</span></span>
- <span data-ttu-id="9a00f-697">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9a00f-697">4OFMTH</span></span>
- <span data-ttu-id="9a00f-698">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="9a00f-698">5OFMTH</span></span>
- <span data-ttu-id="9a00f-699">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="9a00f-699">1N2OFMTH</span></span>
- <span data-ttu-id="9a00f-700">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9a00f-700">3N4OFMTH</span></span>
- <span data-ttu-id="9a00f-701">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="9a00f-701">1N3OFMTH</span></span>
- <span data-ttu-id="9a00f-702">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9a00f-702">1N4OFMTH</span></span>
- <span data-ttu-id="9a00f-703">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="9a00f-703">2N3OFMTH</span></span>
- <span data-ttu-id="9a00f-704">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9a00f-704">2N4OFMTH</span></span>
- <span data-ttu-id="9a00f-705">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="9a00f-705">1N2N3OFMTH</span></span>
- <span data-ttu-id="9a00f-706">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9a00f-706">1N2N4OFMTH</span></span>
- <span data-ttu-id="9a00f-707">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9a00f-707">1N3N4OFMTH</span></span>
- <span data-ttu-id="9a00f-708">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9a00f-708">2N3N4OFMTH</span></span>
- <span data-ttu-id="9a00f-709">1N2N3N4OFMTH–1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="9a00f-709">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="9a00f-710">2N3N4N5OFMth–2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="9a00f-710">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="9a00f-711">1OFQTR–1OFQTR</span><span class="sxs-lookup"><span data-stu-id="9a00f-711">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="9a00f-712">LASTOFQTR–LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="9a00f-712">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="9a00f-713">LASTMTHOFQTR–LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="9a00f-713">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="9a00f-714">1OFYEAR–1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="9a00f-714">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="9a00f-715">LASTOFYEAR–LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="9a00f-715">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="9a00f-716">NOVNDECOFYEAR–NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="9a00f-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="9a00f-717">Adreses</span><span class="sxs-lookup"><span data-stu-id="9a00f-717">Addresses</span></span>

<span data-ttu-id="9a00f-718">Noteiktas valsts vai reģiona, administratīvā apgabala un apgabala (pašvaldības) kodu identifikācijai ir nepieciešami konkrēti formāti, ko var atpazīt pakalpojums Dayforce un valsts/reģiona pakalpojumu sniedzēji.</span><span class="sxs-lookup"><span data-stu-id="9a00f-718">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="9a00f-719">Lai gan pilsētu formāts var būt dažāds, katrai pilsētai ir jābūt saistītai ar administratīvo apgabalu.</span><span class="sxs-lookup"><span data-stu-id="9a00f-719">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="9a00f-720">Talent</span><span class="sxs-lookup"><span data-stu-id="9a00f-720">Talent</span></span>              | <span data-ttu-id="9a00f-721">Dayforce</span><span class="sxs-lookup"><span data-stu-id="9a00f-721">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="9a00f-722">Valsts/reģions</span><span class="sxs-lookup"><span data-stu-id="9a00f-722">Country/Region</span></span>      | <span data-ttu-id="9a00f-723">Valsts kods</span><span class="sxs-lookup"><span data-stu-id="9a00f-723">Country Code</span></span>          |
| <span data-ttu-id="9a00f-724">Pasta indekss</span><span class="sxs-lookup"><span data-stu-id="9a00f-724">Zip/Postal Code</span></span>     | <span data-ttu-id="9a00f-725">Pasta indekss</span><span class="sxs-lookup"><span data-stu-id="9a00f-725">Postal Code</span></span>           |
| <span data-ttu-id="9a00f-726">Administratīvais apgabals</span><span class="sxs-lookup"><span data-stu-id="9a00f-726">State</span></span>               | <span data-ttu-id="9a00f-727">Administratīvā apgabala kods</span><span class="sxs-lookup"><span data-stu-id="9a00f-727">State Code</span></span>            |
| <span data-ttu-id="9a00f-728">Pilsēta</span><span class="sxs-lookup"><span data-stu-id="9a00f-728">City</span></span>                | <span data-ttu-id="9a00f-729">Pilsēta</span><span class="sxs-lookup"><span data-stu-id="9a00f-729">City</span></span>                  |
| <span data-ttu-id="9a00f-730">Apgabals</span><span class="sxs-lookup"><span data-stu-id="9a00f-730">County</span></span>              | <span data-ttu-id="9a00f-731">Apgabals (pašvaldība)</span><span class="sxs-lookup"><span data-stu-id="9a00f-731">County (Municipality)</span></span> |
| <span data-ttu-id="9a00f-732">Iela</span><span class="sxs-lookup"><span data-stu-id="9a00f-732">Street</span></span>              | <span data-ttu-id="9a00f-733">Adreses 1. rinda</span><span class="sxs-lookup"><span data-stu-id="9a00f-733">Address Line 1</span></span>        |
| <span data-ttu-id="9a00f-734">Ielas numurs</span><span class="sxs-lookup"><span data-stu-id="9a00f-734">Street Number</span></span>       | <span data-ttu-id="9a00f-735">Adreses 2. rinda</span><span class="sxs-lookup"><span data-stu-id="9a00f-735">Address Line 2</span></span>        |
| <span data-ttu-id="9a00f-736">Mājas numurs/nosaukums</span><span class="sxs-lookup"><span data-stu-id="9a00f-736">Building Complement</span></span> | <span data-ttu-id="9a00f-737">Adreses 5. rinda</span><span class="sxs-lookup"><span data-stu-id="9a00f-737">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="9a00f-738">Pases numurs</span><span class="sxs-lookup"><span data-stu-id="9a00f-738">Passport number</span></span>

<span data-ttu-id="9a00f-739">Darbinieki var sniegt pases informāciju.</span><span class="sxs-lookup"><span data-stu-id="9a00f-739">Employees can declare passport information.</span></span> <span data-ttu-id="9a00f-740">Šīs informācijas identifikācijas tips ir **Pase**, un tā tiek integrēta pakalpojumā Dayforce kā daļa no darbinieka Meksikai specifiskās informācijas.</span><span class="sxs-lookup"><span data-stu-id="9a00f-740">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="9a00f-741">Identifikācijas tips = Pase</span><span class="sxs-lookup"><span data-stu-id="9a00f-741">Identification Type = "Passport"</span></span>
- <span data-ttu-id="9a00f-742">Izdošanas datums</span><span class="sxs-lookup"><span data-stu-id="9a00f-742">Issued Date</span></span>
- <span data-ttu-id="9a00f-743">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="9a00f-743">Expiration Date</span></span>

<span data-ttu-id="9a00f-744">Darbinieki var sniegt vairākus identifikācijas numurus, kuru identifikācijas tips ir **Pase**.</span><span class="sxs-lookup"><span data-stu-id="9a00f-744">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="9a00f-745">Taču pakalpojumā Dayforce tiek integrēts tikai pašreizējais aktīvais pases ieraksts.</span><span class="sxs-lookup"><span data-stu-id="9a00f-745">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="9a00f-746">Ja visiem pases ierakstiem ir beidzies derīgiem, pakalpojumā Dayforce tiek integrēta pēdējā izdotā pase.</span><span class="sxs-lookup"><span data-stu-id="9a00f-746">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
