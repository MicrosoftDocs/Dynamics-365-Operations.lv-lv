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
ms.openlocfilehash: c26dfed9909b0dbd05fc18c206e5adc947feaef5
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742920"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="c0f96-103">Talent un Dayforce algu aprēķina integrācijas konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="c0f96-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c0f96-104">Microsoft Dynamics 365 for Talent un Ceridian Dayforce integrācijai tiek izmantotas vairākas konfigurācijas darbības, kas ir aprakstītas šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="c0f96-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="c0f96-105">Pirms maksājuma izpildes apstrādes vispirms ir jākonfigurē integrācija gan pakalpojumā Talent, gan pakalpojumā Dayforce.</span><span class="sxs-lookup"><span data-stu-id="c0f96-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="c0f96-106">Ja maksājumu izpildei izmantojat tādu pakalpojumu kā Dayforce, jums ir jāiespējo integrācija pakalpojumā Talent.</span><span class="sxs-lookup"><span data-stu-id="c0f96-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="c0f96-107">Integrācijai ir nepieciešami noteikti Talent dati.</span><span class="sxs-lookup"><span data-stu-id="c0f96-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="c0f96-108">Tādēļ ir jāpārliecinās, vai uz Dayforce kartētie dati pakalpojumā Talent ir konfigurēti veidā, kas atbalsta integrāciju.</span><span class="sxs-lookup"><span data-stu-id="c0f96-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="c0f96-109">Integrācija izmanto tālāk norādītās vispārējās datu kategorijas.</span><span class="sxs-lookup"><span data-stu-id="c0f96-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="c0f96-110">Personāla vadības dati</span><span class="sxs-lookup"><span data-stu-id="c0f96-110">Human resources data</span></span>
- <span data-ttu-id="c0f96-111">Atlīdzības dati</span><span class="sxs-lookup"><span data-stu-id="c0f96-111">Compensation data</span></span>
- <span data-ttu-id="c0f96-112">Algu dati, piemēram, apmaksas cikli, apmaksas periodi un ienākumu veidu kodi</span><span class="sxs-lookup"><span data-stu-id="c0f96-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="c0f96-113">Nodarbināto dati</span><span class="sxs-lookup"><span data-stu-id="c0f96-113">Worker data</span></span>

<span data-ttu-id="c0f96-114">Šajā tēmā ir aprakstītas darbības, kas jāveic, lai iespējotu integrāciju.</span><span class="sxs-lookup"><span data-stu-id="c0f96-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="c0f96-115">Tajā ir arī izskaidrots, kādu veidu dati un konfigurācijas informācija ir nepieciešama integrācijai.</span><span class="sxs-lookup"><span data-stu-id="c0f96-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="c0f96-116">Integrācijas iespējošana</span><span class="sxs-lookup"><span data-stu-id="c0f96-116">Enable the integration</span></span>

<span data-ttu-id="c0f96-117">Lai izveidotu savienojumu ar Dayforce, pakalpojumā Talent ir jāieslēdz integrācija un jāievada konfigurācijas informācija.</span><span class="sxs-lookup"><span data-stu-id="c0f96-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="c0f96-118">Ja vēlaties, lai izveidotā Virsgrāmatas transakcija tiktu importēta programmā Microsoft Dynamics 365 for Finance and Operations, ir jāiestata arī Microsoft Azure krātuves konts un programmā Finance and Operations jāievada Azure krātuves savienojuma virkne.</span><span class="sxs-lookup"><span data-stu-id="c0f96-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="c0f96-119">Lai pakalpojumā Talent ieslēgtu integrāciju, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="c0f96-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="c0f96-120">Lapā **Sistēmas administrēšana** atlasiet opciju **Integrācijas konfigurēšana**.</span><span class="sxs-lookup"><span data-stu-id="c0f96-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="c0f96-121">Ievadiet drošo failu pārsūtīšanas protokola (FTP) galapunktu un drošo FTP mapes ceļu.</span><span class="sxs-lookup"><span data-stu-id="c0f96-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="c0f96-122">Ievadiet tā lietotāja lietotājvārdu un paroli, kurš piekļūs drošajam FTP galapunktam un mapes ceļam.</span><span class="sxs-lookup"><span data-stu-id="c0f96-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="c0f96-123">Pārbaudiet savienojumu, kā nepieciešams, un opciju **Iespējot algu aprēķina integrāciju** iestatiet uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="c0f96-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="c0f96-124">Kad integrācija ir ieslēgta, tiek izveidota datu eksportēšanas pakotne un faili, kā arī iestatīts biežums.</span><span class="sxs-lookup"><span data-stu-id="c0f96-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="c0f96-125">Biežumu varat mainīt atbilstoši vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="c0f96-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="c0f96-126">Papildinformāciju par Azure krātuves kontiem un Azure krātuves savienojuma virknēm skatiet tālāk sniegtajās Azure tēmās.</span><span class="sxs-lookup"><span data-stu-id="c0f96-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="c0f96-127">Par Azure krātuves kontiem</span><span class="sxs-lookup"><span data-stu-id="c0f96-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="c0f96-128">Azure krātuves savienojuma virkņu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="c0f96-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="c0f96-129">Tehniskā informācija par algu aprēķina integrācijas iespējošanu</span><span class="sxs-lookup"><span data-stu-id="c0f96-129">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="c0f96-130">Algu aprēķina integrācijas ieslēgšanai ir divi primārie iznākumi, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="c0f96-130">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="c0f96-131">Tiek izveidots datu eksportēšanas projekts ar nosaukumu “Algu aprēķina integrācijas eksportēšana”.</span><span class="sxs-lookup"><span data-stu-id="c0f96-131">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="c0f96-132">Šajā projektā ir iekļauti elementi un lauki, kas nepieciešami algu aprēķina integrācijai.</span><span class="sxs-lookup"><span data-stu-id="c0f96-132">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="c0f96-133">Lai pārbaudītu projektu, dodieties uz sadaļu **Sistēmas administrēšana**, atlasiet elementu **Datu pārvaldība** un pēc tam atveriet datu projektu no projektu saraksta.</span><span class="sxs-lookup"><span data-stu-id="c0f96-133">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="c0f96-134">Šis pakešuzdevums izpilda datu eksportēšanas projektu, šifrē iegūto datu pakotni un pārsūta datu pakotnes failu uz SFTP galapunktu, kas konfigurēts ekrānā **Integrācijas konfigurēšana**.</span><span class="sxs-lookup"><span data-stu-id="c0f96-134">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="c0f96-135">Datu pakotne, kas pārsūtīta uz SFTP galapunktu, tiek šifrēta, izmantojot pakotnes unikālo atslēgu.</span><span class="sxs-lookup"><span data-stu-id="c0f96-135">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="c0f96-136">Atslēga glabājas Azure Key Vault krātuvē, kam var piekļūt, tikai izmantojot Ceridian.</span><span class="sxs-lookup"><span data-stu-id="c0f96-136">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="c0f96-137">Nav iespējams atšifrēt un pārbaudīt datu pakotnes saturu.</span><span class="sxs-lookup"><span data-stu-id="c0f96-137">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="c0f96-138">Ja ir jāpārbauda datu pakotnes saturs, eksportējiet datu projektu “Algu aprēķina integrācijas eksportēšana” manuāli, lejupielādējiet to un pēc tam atveriet to.</span><span class="sxs-lookup"><span data-stu-id="c0f96-138">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="c0f96-139">Eksportējot manuāli, pakotne netiks šifrēta un pārsūtīta.</span><span class="sxs-lookup"><span data-stu-id="c0f96-139">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="c0f96-140">Datu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="c0f96-140">Configure your data</span></span> 

<span data-ttu-id="c0f96-141">Lai apstrādātu algas, pakalpojumā Talent ir jākonfigurē personāla vadības dati.</span><span class="sxs-lookup"><span data-stu-id="c0f96-141">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="c0f96-142">Jums ir jāiestata organizācijas dati, piemēram, darbi un amati, kā arī informācija par atvieglojumiem un atlīdzību.</span><span class="sxs-lookup"><span data-stu-id="c0f96-142">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="c0f96-143">Šie dati nodrošina informāciju par nodarbinātību, samaksu un ieturējumiem, kas nepieciešama darbinieka algas ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="c0f96-143">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="c0f96-144">Personāla vadības dati</span><span class="sxs-lookup"><span data-stu-id="c0f96-144">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="c0f96-145">Atvieglojumi</span><span class="sxs-lookup"><span data-stu-id="c0f96-145">Benefits</span></span> 

<span data-ttu-id="c0f96-146">Personāla vadība nodrošina rīkus, ko var izmantot, lai iestatītu un uzturētu atvieglojumus, ieturējumus un nodarbināto atlīdzības plānus, ko organizācija piedāvā vai apstrādā saviem nodarbinātajiem.</span><span class="sxs-lookup"><span data-stu-id="c0f96-146">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="c0f96-147">Kad veidojat atvieglojumus, ņemiet vērā tālāk norādītos datus un konfigurācijas, kas tiek izmantoti pakalpojumā Dayforce.</span><span class="sxs-lookup"><span data-stu-id="c0f96-147">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="c0f96-148">Atvieglojumu plāni</span><span class="sxs-lookup"><span data-stu-id="c0f96-148">Benefit plans</span></span>

- <span data-ttu-id="c0f96-149">Plāns (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-149">Plan (required)</span></span>
- <span data-ttu-id="c0f96-150">Tips (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-150">Type (required)</span></span>
- <span data-ttu-id="c0f96-151">Algas ietekme (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-151">Payroll impact (required)</span></span>
- <span data-ttu-id="c0f96-152">Atgūt nokavētos maksājumus</span><span class="sxs-lookup"><span data-stu-id="c0f96-152">Recover arrears</span></span>
- <span data-ttu-id="c0f96-153">Ieturējuma metode</span><span class="sxs-lookup"><span data-stu-id="c0f96-153">Deduction method</span></span>
- <span data-ttu-id="c0f96-154">Ieturējuma prioritāte</span><span class="sxs-lookup"><span data-stu-id="c0f96-154">Deduction priority</span></span>
- <span data-ttu-id="c0f96-155">Ierobežojuma periods</span><span class="sxs-lookup"><span data-stu-id="c0f96-155">Limit period</span></span>
- <span data-ttu-id="c0f96-156">Ierobežojuma summa</span><span class="sxs-lookup"><span data-stu-id="c0f96-156">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="c0f96-157">Atvieglojumi</span><span class="sxs-lookup"><span data-stu-id="c0f96-157">Benefits</span></span>

- <span data-ttu-id="c0f96-158">Plāns (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-158">Plan (required)</span></span>
- <span data-ttu-id="c0f96-159">Tips (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-159">Type (required)</span></span>
- <span data-ttu-id="c0f96-160">Opcija (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-160">Option (required)</span></span>
- <span data-ttu-id="c0f96-161">Atvieglojumu ID (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-161">Benefit ID (required)</span></span>
- <span data-ttu-id="c0f96-162">Biežums</span><span class="sxs-lookup"><span data-stu-id="c0f96-162">Frequency</span></span>
- <span data-ttu-id="c0f96-163">Pamats</span><span class="sxs-lookup"><span data-stu-id="c0f96-163">Basis</span></span>
- <span data-ttu-id="c0f96-164">Summa vai likme</span><span class="sxs-lookup"><span data-stu-id="c0f96-164">Amount or rate</span></span>
- <span data-ttu-id="c0f96-165">Ienākumu veida kods</span><span class="sxs-lookup"><span data-stu-id="c0f96-165">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="c0f96-166">Atbalstītās biežuma vērtības</span><span class="sxs-lookup"><span data-stu-id="c0f96-166">Supported frequencies</span></span> 

- <span data-ttu-id="c0f96-167">Katru nedēļu</span><span class="sxs-lookup"><span data-stu-id="c0f96-167">Weekly</span></span>
- <span data-ttu-id="c0f96-168">Katru otro nedēļu</span><span class="sxs-lookup"><span data-stu-id="c0f96-168">Bi-weekly</span></span>
- <span data-ttu-id="c0f96-169">Pusmēneša</span><span class="sxs-lookup"><span data-stu-id="c0f96-169">Semi-monthly</span></span>
- <span data-ttu-id="c0f96-170">Mēnesis</span><span class="sxs-lookup"><span data-stu-id="c0f96-170">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="c0f96-171">Atbalstītās pamata vērtības</span><span class="sxs-lookup"><span data-stu-id="c0f96-171">Supported bases</span></span> 

- <span data-ttu-id="c0f96-172">Fiksēta summa</span><span class="sxs-lookup"><span data-stu-id="c0f96-172">Fixed amount</span></span>
- <span data-ttu-id="c0f96-173">Ienākumu procentuālais daudzums</span><span class="sxs-lookup"><span data-stu-id="c0f96-173">Percent of earnings</span></span>
- <span data-ttu-id="c0f96-174">Produktīvās stundas</span><span class="sxs-lookup"><span data-stu-id="c0f96-174">Productive hours</span></span>

<span data-ttu-id="c0f96-175">Dayforce izveido tālāk norādītos ieturējumus, pamatojoties uz atvieglojumu plānā definēto algas ietekmi.</span><span class="sxs-lookup"><span data-stu-id="c0f96-175">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="c0f96-176">Atlase pakalpojumā Talent</span><span class="sxs-lookup"><span data-stu-id="c0f96-176">Selection in Talent</span></span>        | <span data-ttu-id="c0f96-177">Rezultāts pakalpojumā Dayforce</span><span class="sxs-lookup"><span data-stu-id="c0f96-177">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="c0f96-178">Neviens</span><span class="sxs-lookup"><span data-stu-id="c0f96-178">None</span></span>                       | <span data-ttu-id="c0f96-179">Nav izveidots neviens ieturējums.</span><span class="sxs-lookup"><span data-stu-id="c0f96-179">No deduction is created.</span></span>                      |
| <span data-ttu-id="c0f96-180">Tikai ieturējums</span><span class="sxs-lookup"><span data-stu-id="c0f96-180">Deduction only</span></span>             | <span data-ttu-id="c0f96-181">Ir izveidots darbinieka ieturējums.</span><span class="sxs-lookup"><span data-stu-id="c0f96-181">An employee deduction is created.</span></span>             |
| <span data-ttu-id="c0f96-182">Tikai segums</span><span class="sxs-lookup"><span data-stu-id="c0f96-182">Contribution only</span></span>          | <span data-ttu-id="c0f96-183">Ir izveidots darba devēja ieturējums.</span><span class="sxs-lookup"><span data-stu-id="c0f96-183">An employer deduction is created.</span></span>             |
| <span data-ttu-id="c0f96-184">Ieturējums un segums</span><span class="sxs-lookup"><span data-stu-id="c0f96-184">Deduction and contribution</span></span> | <span data-ttu-id="c0f96-185">Ir izveidots darbinieka un darba devēja ieturējums.</span><span class="sxs-lookup"><span data-stu-id="c0f96-185">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="c0f96-186">Papildinformāciju par atvieglojumu programmas definēšanu un pārvaldību skatiet tālāk sniegtajās tēmās.</span><span class="sxs-lookup"><span data-stu-id="c0f96-186">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="c0f96-187">Darbinieku atvieglojumu programmas nodrošināšana</span><span class="sxs-lookup"><span data-stu-id="c0f96-187">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="c0f96-188">Jauna atvieglojuma izveide</span><span class="sxs-lookup"><span data-stu-id="c0f96-188">Create a new benefit</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="c0f96-189">Atvieglojumu piemērotības kārtulu un ierobežojumu definēšana</span><span class="sxs-lookup"><span data-stu-id="c0f96-189">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="c0f96-190">Atvieglojumu reģistrēšana un noņemšana nodarbinātajiem</span><span class="sxs-lookup"><span data-stu-id="c0f96-190">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="c0f96-191">Atlīdzība</span><span class="sxs-lookup"><span data-stu-id="c0f96-191">Compensation</span></span> 

<span data-ttu-id="c0f96-192">Atlīdzību pārvaldība tiek izmantota, lai kontrolētu pamatalgas un prēmiju izsniegšanu.</span><span class="sxs-lookup"><span data-stu-id="c0f96-192">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="c0f96-193">Darbinieka fiksētā pamatalga un nopelnu palielinājumi tiek kontrolēti, izmantojot fiksētas atlīdzības plānus.</span><span class="sxs-lookup"><span data-stu-id="c0f96-193">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="c0f96-194">Veicināšanas maksājumu izsniegšana, piemēram, prēmiju maksājumi, apbalvojumi par sasniegumiem, uzņēmuma akciju iegādes iespējas un dotācijas, kā arī vienreizējas piemaksas, tiek kontrolētas ar mainīgās atlīdzības plāniem.</span><span class="sxs-lookup"><span data-stu-id="c0f96-194">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="c0f96-195">Dayforce izmanto atlīdzības informāciju, lai aprēķinātu darbinieka stundas vai gada likmi.</span><span class="sxs-lookup"><span data-stu-id="c0f96-195">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="c0f96-196">Ir jānorāda fiksētās atlīdzības plāni un apmaksas likmes konvertēšanas gadījumi.</span><span class="sxs-lookup"><span data-stu-id="c0f96-196">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="c0f96-197">Darbiniekiem ir jābūt saistītiem ar fiksētās atlīdzības plānu.</span><span class="sxs-lookup"><span data-stu-id="c0f96-197">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="c0f96-198">Papildinformāciju par atlīdzības plāniem skatiet tālāk sniegtajās tēmās.</span><span class="sxs-lookup"><span data-stu-id="c0f96-198">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="c0f96-199">Fiksētās atlīdzības plānu izveidošana</span><span class="sxs-lookup"><span data-stu-id="c0f96-199">Create fixed compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="c0f96-200">Mainīgās atlīdzības plānu izveidošana</span><span class="sxs-lookup"><span data-stu-id="c0f96-200">Create variable compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="c0f96-201">Algas/atlīdzības organizācijas un plānu izstrāde</span><span class="sxs-lookup"><span data-stu-id="c0f96-201">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="c0f96-202">Procesa kompensācija</span><span class="sxs-lookup"><span data-stu-id="c0f96-202">Process compensation</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="c0f96-203">Atlīdzības procesa definēšana un rezultātu aprēķināšana</span><span class="sxs-lookup"><span data-stu-id="c0f96-203">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="c0f96-204">Darbinieka reģistrēšana fiksētās atlīdzības plānā</span><span class="sxs-lookup"><span data-stu-id="c0f96-204">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="c0f96-205">Darbinieka reģistrēšana mainīgās atlīdzības plānā</span><span class="sxs-lookup"><span data-stu-id="c0f96-205">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="c0f96-206">Darbi</span><span class="sxs-lookup"><span data-stu-id="c0f96-206">Jobs</span></span> 

<span data-ttu-id="c0f96-207">Darbs ir uzdevumu un atbildības jomu kopums, kas ir jāizpilda personai, kura veic darbu.</span><span class="sxs-lookup"><span data-stu-id="c0f96-207">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="c0f96-208">Lai iegūtu papildu informāciju, skatiet šādas tēmas:</span><span class="sxs-lookup"><span data-stu-id="c0f96-208">For more information, see the following topics:</span></span>

- [<span data-ttu-id="c0f96-209">Darba komponentu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="c0f96-209">Setting up the components of a job</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="c0f96-210">Jaunu darbu definēšana</span><span class="sxs-lookup"><span data-stu-id="c0f96-210">Define new jobs</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="c0f96-211">Amati</span><span class="sxs-lookup"><span data-stu-id="c0f96-211">Positions</span></span>

<span data-ttu-id="c0f96-212">Pozīcija ir atsevišķa darba instance.</span><span class="sxs-lookup"><span data-stu-id="c0f96-212">A position is an individual instance of a job.</span></span> <span data-ttu-id="c0f96-213">Piemēram, amats Pārdošanas daļas vadītājs (austrumu reģions) ir tikai viens no amatiem, kas ir saistīti ar darbu Pārdošanas daļas vadītājs.</span><span class="sxs-lookup"><span data-stu-id="c0f96-213">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="c0f96-214">Amats pastāv nodaļā.</span><span class="sxs-lookup"><span data-stu-id="c0f96-214">A position exists in a department.</span></span> <span data-ttu-id="c0f96-215">Ar katru amatu var būt saistīts tikai viens nodarbinātais.</span><span class="sxs-lookup"><span data-stu-id="c0f96-215">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="c0f96-216">Iestatot jaunus amatus, ņemiet vērā tālāk norādītos datus un konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="c0f96-216">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="c0f96-217">Amats (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-217">Position (required)</span></span>
- <span data-ttu-id="c0f96-218">Apraksts (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-218">Description (required)</span></span>
- <span data-ttu-id="c0f96-219">Darbs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-219">Job (required)</span></span>
- <span data-ttu-id="c0f96-220">Nodaļa (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-220">Department (required)</span></span>
- <span data-ttu-id="c0f96-221">Amata veids (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-221">Position type (required)</span></span>
- <span data-ttu-id="c0f96-222">Pilnas slodzes ekvivalents</span><span class="sxs-lookup"><span data-stu-id="c0f96-222">Full-time equivalent</span></span>
- <span data-ttu-id="c0f96-223">Ikgadējās parastās stundas (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-223">Annual regular hours (required)</span></span>
- <span data-ttu-id="c0f96-224">Apmaksātāja juridiskā persona (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-224">Paid by legal entity (required)</span></span>
- <span data-ttu-id="c0f96-225">Apmaksas cikls (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-225">Pay cycle (required)</span></span>
- <span data-ttu-id="c0f96-226">Noklusējuma finanšu dimensija — izmaksu centrs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-226">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="c0f96-227">Nodarbinātā piešķire — nodarbinātais, piešķires sākums, piešķires beigas, iemesla kods</span><span class="sxs-lookup"><span data-stu-id="c0f96-227">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="c0f96-228">Ja vienā nodaļā ar to pašu darbu ir saistīti vairāki amati, tie pakalpojumā Dayforce tiek apvienoti vienā amatā.</span><span class="sxs-lookup"><span data-stu-id="c0f96-228">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="c0f96-229">Lai iegūtu papildu informāciju, skatiet šādas tēmas:</span><span class="sxs-lookup"><span data-stu-id="c0f96-229">For more information, see the following topics:</span></span>

- [<span data-ttu-id="c0f96-230">Organizēt darbaspēku, izmantojot nodaļas, darbus un amatus</span><span class="sxs-lookup"><span data-stu-id="c0f96-230">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="c0f96-231">Amatu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="c0f96-231">Set up positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="c0f96-232">Nodaļas</span><span class="sxs-lookup"><span data-stu-id="c0f96-232">Departments</span></span>

<span data-ttu-id="c0f96-233">Nodaļa ir pārvaldības struktūrvienība, kas pārstāv organizācijas kategoriju vai funkcionālo apgabalu.</span><span class="sxs-lookup"><span data-stu-id="c0f96-233">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="c0f96-234">Nodaļa ir atbildīga par noteiktu organizācijas jomu, piemēram, pārdošanu, uzskaiti vai personāla vadību.</span><span class="sxs-lookup"><span data-stu-id="c0f96-234">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="c0f96-235">Nodaļas var izmantot, lai ziņotu par funkcionālām jomām.</span><span class="sxs-lookup"><span data-stu-id="c0f96-235">You can use departments to report on functional areas.</span></span> <span data-ttu-id="c0f96-236">Nodaļām var būt peļņas un zaudējumu atbildība.</span><span class="sxs-lookup"><span data-stu-id="c0f96-236">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="c0f96-237">Lai iegūtu papildu informāciju, skatiet šādas tēmas:</span><span class="sxs-lookup"><span data-stu-id="c0f96-237">For more information, see the following topics:</span></span>

- [<span data-ttu-id="c0f96-238">Nodaļas izveide un tās saistīšana ar nodaļu hierarhiju</span><span class="sxs-lookup"><span data-stu-id="c0f96-238">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="c0f96-239">Jaunu nodaļu definēšana</span><span class="sxs-lookup"><span data-stu-id="c0f96-239">Define new departments</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="c0f96-240">Apmaksas cikli un apmaksas periodi</span><span class="sxs-lookup"><span data-stu-id="c0f96-240">Pay cycles and pay periods</span></span>

<span data-ttu-id="c0f96-241">Apmaksas cikls nosaka, cik bieži tiek veikts algu aprēķins, kā arī konkrētās dienas, kurās nodarbinātie saņem samaksu.</span><span class="sxs-lookup"><span data-stu-id="c0f96-241">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="c0f96-242">Apmaksas cikls var būt, piemēram, ikmēneša, un darbinieki samaksu var saņemt mēneša pēdējā dienā.</span><span class="sxs-lookup"><span data-stu-id="c0f96-242">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="c0f96-243">Vai arī apmaksas cikls var būt iknedēļas, un darbinieki samaksu var saņemt otrdienā pēc apmaksas perioda beigām.</span><span class="sxs-lookup"><span data-stu-id="c0f96-243">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="c0f96-244">Apmaksas cikli tiek piešķirti amatiem, lai kontrolētu to, kad nodarbinātie šajos amatos saņems samaksu.</span><span class="sxs-lookup"><span data-stu-id="c0f96-244">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="c0f96-245">Pēc apmaksas ciklu izveides katram ciklam varat ģenerēt apmaksas periodus.</span><span class="sxs-lookup"><span data-stu-id="c0f96-245">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="c0f96-246">Katrā apmaksas periodā ir ietverts noklusējuma maksājuma datums, kura pamatā ir jūsu sniegtā informācija.</span><span class="sxs-lookup"><span data-stu-id="c0f96-246">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="c0f96-247">Taču varat modificēt apmaksas perioda noklusējuma maksājuma datumu izņēmumu iestatīšanai, piemēram, kad maksājuma datums ir brīvdienā.</span><span class="sxs-lookup"><span data-stu-id="c0f96-247">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="c0f96-248">Dayforce izmanto tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="c0f96-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="c0f96-249">Apmaksas cikls (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-249">Pay cycle (required)</span></span>
- <span data-ttu-id="c0f96-250">Apmaksas cikla biežums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-250">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="c0f96-251">Perioda sākuma datums (ir jānorāda pirmais apmaksas periods)</span><span class="sxs-lookup"><span data-stu-id="c0f96-251">Period start date (first pay period required)</span></span>
- <span data-ttu-id="c0f96-252">Noklusējuma maksājuma datums (ir jānorāda pirmais apmaksas periods)</span><span class="sxs-lookup"><span data-stu-id="c0f96-252">Default payment date (first pay period required)</span></span>

<span data-ttu-id="c0f96-253">Šī informācija pakalpojumā Dayforce ir integrēta kā apmaksas grupas, un katram apmaksas ciklam to atdala valsts vai reģions.</span><span class="sxs-lookup"><span data-stu-id="c0f96-253">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="c0f96-254">Pirms integrācijas ir jābūt ģenerētam vismaz vienam apmaksas periodam.</span><span class="sxs-lookup"><span data-stu-id="c0f96-254">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="c0f96-255">Dayforce ģenerē apmaksas grupu kalendārus un maksājumu datumus atbilstoši pakalpojumā Talent iestatītajam pirmā apmaksas perioda sākuma datumam un noklusējuma maksājuma datumam.</span><span class="sxs-lookup"><span data-stu-id="c0f96-255">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="c0f96-256">Ienākumu veida kodi</span><span class="sxs-lookup"><span data-stu-id="c0f96-256">Earning codes</span></span>

<span data-ttu-id="c0f96-257">Ienākumu veidu kodi unikāli identificē katra veida ienākumus, ko saņem nodarbinātie.</span><span class="sxs-lookup"><span data-stu-id="c0f96-257">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="c0f96-258">Kodiem ir dažādi ar ienākumiem saistīti parametri, piemēram, uzskaites nosacījumi, nodokļu likumi, pārskatu veidošanas prasības un bruto summas palielināšanas iespēja.</span><span class="sxs-lookup"><span data-stu-id="c0f96-258">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="c0f96-259">Dayforce izmanto tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="c0f96-259">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="c0f96-260">Ienākumu veida kods (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-260">Earning Code (required)</span></span>
- <span data-ttu-id="c0f96-261">apraksts</span><span class="sxs-lookup"><span data-stu-id="c0f96-261">Description</span></span>
- <span data-ttu-id="c0f96-262">Mērvienība</span><span class="sxs-lookup"><span data-stu-id="c0f96-262">Unit of measure</span></span>
- <span data-ttu-id="c0f96-263">Produktīvs</span><span class="sxs-lookup"><span data-stu-id="c0f96-263">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="c0f96-264">Nodarbināto dati</span><span class="sxs-lookup"><span data-stu-id="c0f96-264">Worker data</span></span>

<span data-ttu-id="c0f96-265">Dažādo veidu nodarbināto ieraksti ir svarīga informācija personāla vadības un algu sistēmās.</span><span class="sxs-lookup"><span data-stu-id="c0f96-265">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="c0f96-266">Ievadīto informāciju var izmantot, lai sekotu nodarbinātajiem un personiskajai informācijai.</span><span class="sxs-lookup"><span data-stu-id="c0f96-266">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="c0f96-267">Par darbiniekiem var saglabāt tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="c0f96-267">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="c0f96-268">**Pamata** — saglabājiet pamata informāciju par darbinieku, piemēram, kontaktinformāciju, demogrāfisko informāciju, identifikācijas informāciju, ģimenes informāciju, karadienesta statusu, ekspatriantu informāciju, kā arī personiskās un ārkārtas kontaktpersonas.</span><span class="sxs-lookup"><span data-stu-id="c0f96-268">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="c0f96-269">**Nodarbinātība** — saglabājiet informāciju par darbinieka nodarbinātību, piemēram, informāciju par piederību uzņēmumam vai organizācijai, amata piešķiri, sākuma un beigu datumiem, piemērotību darbam, nodarbinātības noteikumiem, pensiju, atvaļinājumu un pārcelšanu.</span><span class="sxs-lookup"><span data-stu-id="c0f96-269">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="c0f96-270">**Atvaļinājumi un kavējumi** — saglabājiet informāciju par nodarbinātā kavējumiem, piemēram, informāciju par darba kalendāriem, kavējumu darbībām un kavējumu iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="c0f96-270">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="c0f96-271">**Atlīdzība un alga** — saglabājiet informāciju par nodarbinātā atlīdzības plāniem un algas informāciju, piemēram, plāna reģistrāciju, piemaksām, sniegumu, komisiju, nodokļu informāciju, pensionēšanos un ieturējumiem no algas.</span><span class="sxs-lookup"><span data-stu-id="c0f96-271">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="c0f96-272">Ievadot informāciju par nodarbināto, ņemiet vērā tālāk norādītos datus un konfigurācijas, kas tiek izmantoti pakalpojumā Dayforce.</span><span class="sxs-lookup"><span data-stu-id="c0f96-272">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="c0f96-273">Vispārīgā informācija</span><span class="sxs-lookup"><span data-stu-id="c0f96-273">General information</span></span>

- <span data-ttu-id="c0f96-274">Personāla numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-274">Personnel number (required)</span></span>
- <span data-ttu-id="c0f96-275">Vārds (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-275">First name (required)</span></span>
- <span data-ttu-id="c0f96-276">Uzvārds (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-276">Last name (required)</span></span>
- <span data-ttu-id="c0f96-277">Otrais vārds</span><span class="sxs-lookup"><span data-stu-id="c0f96-277">Middle name</span></span>
- <span data-ttu-id="c0f96-278">Darba stāža datums</span><span class="sxs-lookup"><span data-stu-id="c0f96-278">Seniority date</span></span>
- <span data-ttu-id="c0f96-279">Zināms kā</span><span class="sxs-lookup"><span data-stu-id="c0f96-279">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="c0f96-280">Personiskā informācija</span><span class="sxs-lookup"><span data-stu-id="c0f96-280">Personal information</span></span>

- <span data-ttu-id="c0f96-281">Ģimenes stāvoklis (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-281">Marital status (required)</span></span>
- <span data-ttu-id="c0f96-282">Dzimšanas datums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-282">Birth date (required)</span></span>
- <span data-ttu-id="c0f96-283">Dzimums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-283">Gender (required)</span></span>
- <span data-ttu-id="c0f96-284">Persona ar īpašām vajadzībām</span><span class="sxs-lookup"><span data-stu-id="c0f96-284">Person with disabilities</span></span>
- <span data-ttu-id="c0f96-285">Nacionalitātes valsts/reģions (tikai Meksikai)</span><span class="sxs-lookup"><span data-stu-id="c0f96-285">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="c0f96-286">Adreses informācija</span><span class="sxs-lookup"><span data-stu-id="c0f96-286">Address information</span></span>

- <span data-ttu-id="c0f96-287">Primārā (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-287">Primary (required)</span></span>
- <span data-ttu-id="c0f96-288">Valsts/reģions (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-288">Country/region (required)</span></span>
- <span data-ttu-id="c0f96-289">Pasta indekss (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-289">Postal code (required)</span></span>
- <span data-ttu-id="c0f96-290">Ielas numurs (obligāti) (tikai Meksikai)</span><span class="sxs-lookup"><span data-stu-id="c0f96-290">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="c0f96-291">Mājas numurs/nosaukums (tikai Meksikai)</span><span class="sxs-lookup"><span data-stu-id="c0f96-291">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="c0f96-292">Pilsēta (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-292">City (required)</span></span>
- <span data-ttu-id="c0f96-293">Administratīvais apgabals (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-293">State (required)</span></span>
- <span data-ttu-id="c0f96-294">Apgabals (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-294">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="c0f96-295">Kontaktinformācija</span><span class="sxs-lookup"><span data-stu-id="c0f96-295">Contact information</span></span> 

- <span data-ttu-id="c0f96-296">Primārā (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-296">Primary (required)</span></span>
- <span data-ttu-id="c0f96-297">Kontaktpersonas tālrunis (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-297">Contact number (required)</span></span>
- <span data-ttu-id="c0f96-298">Paplašinājums</span><span class="sxs-lookup"><span data-stu-id="c0f96-298">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="c0f96-299">Algas informācija un ienākumu veidu kodi</span><span class="sxs-lookup"><span data-stu-id="c0f96-299">Payroll information and earning codes</span></span>

<span data-ttu-id="c0f96-300">Darbiniekiem var būt piešķirti konkrēti ienākumu veidi konkrētajā maksājumu biežumā, kā arī var būt norādīta vēlamā maksāšanas metode.</span><span class="sxs-lookup"><span data-stu-id="c0f96-300">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="c0f96-301">Lai palīdzētu nodrošināt, ka šīs preferences un iestatījumi tiek izmantoti, pakalpojumā Dayforce ir tālāk norādītie lauki.</span><span class="sxs-lookup"><span data-stu-id="c0f96-301">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="c0f96-302">Ienākumu veida kodi</span><span class="sxs-lookup"><span data-stu-id="c0f96-302">Earning codes</span></span>

- <span data-ttu-id="c0f96-303">Amats (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-303">Position (required)</span></span>
- <span data-ttu-id="c0f96-304">Ienākumu veida kods (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-304">Earning Code (required)</span></span>
- <span data-ttu-id="c0f96-305">Biežums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-305">Frequency (required)</span></span>
- <span data-ttu-id="c0f96-306">Summa (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-306">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="c0f96-307">Algas informācija</span><span class="sxs-lookup"><span data-stu-id="c0f96-307">Payroll information</span></span>

- <span data-ttu-id="c0f96-308">Maksāšanas metode</span><span class="sxs-lookup"><span data-stu-id="c0f96-308">Payment Method</span></span>
- <span data-ttu-id="c0f96-309">Ekonomiskais reģions (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-309">Economic Region (required)</span></span>
- <span data-ttu-id="c0f96-310">Darbinieka atvieglojumu ID</span><span class="sxs-lookup"><span data-stu-id="c0f96-310">Employee Benefits ID</span></span>
- <span data-ttu-id="c0f96-311">Nacionālais ID numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-311">National ID Number (required)</span></span>
- <span data-ttu-id="c0f96-312">Karadienesta numurs</span><span class="sxs-lookup"><span data-stu-id="c0f96-312">Military Service Number</span></span>
- <span data-ttu-id="c0f96-313">Maiņas ID (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-313">Shift ID (required)</span></span>
- <span data-ttu-id="c0f96-314">Nodokļu numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-314">Tax Number (required)</span></span>
- <span data-ttu-id="c0f96-315">Arodbiedrības ID (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-315">Union ID (required)</span></span>
- <span data-ttu-id="c0f96-316">Darba dienas ID (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-316">Work Day ID (required)</span></span>
- <span data-ttu-id="c0f96-317">Darba atļaujas numurs</span><span class="sxs-lookup"><span data-stu-id="c0f96-317">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="c0f96-318">Meksika atbalsta šādas maksāšanas metodes: **Skaidra nauda**, **Čeks** (uzņēmuma fiziskais čeks) un **Elektroniskais maksājums**.</span><span class="sxs-lookup"><span data-stu-id="c0f96-318">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="c0f96-319">Ja nav norādīta neviena maksāšanas metode, pēc noklusējuma tiek izmantota opcija **Čeks**.</span><span class="sxs-lookup"><span data-stu-id="c0f96-319">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="c0f96-320">Nodarbinātības papildinformācija</span><span class="sxs-lookup"><span data-stu-id="c0f96-320">Employment details</span></span>

<span data-ttu-id="c0f96-321">Nodarbinātības datu vēsture pakalpojumā Dayforce tiek izmantota kā galvenā informācija, no kuras tiek iegūts darbinieka darbā pieņemšanas, darba attiecību izbeigšanas un atkārtotas pieņemšanas darbā statuss.</span><span class="sxs-lookup"><span data-stu-id="c0f96-321">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="c0f96-322">Dayforce vienlaikus atbalsta tikai vienu aktīvu nodarbinātības ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c0f96-322">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="c0f96-323">Nodarbinātības sākuma datums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-323">Employment start date (required)</span></span>
- <span data-ttu-id="c0f96-324">Nodarbinātības beigu datums</span><span class="sxs-lookup"><span data-stu-id="c0f96-324">Employment end date</span></span>
- <span data-ttu-id="c0f96-325">Pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="c0f96-325">Start date</span></span>
- <span data-ttu-id="c0f96-326">Koriģētais pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="c0f96-326">Adjusted start date</span></span>
- <span data-ttu-id="c0f96-327">Darba attiecību pārtraukšanas datums (jānorāda, kad tiek pārtrauktas darba attiecības)</span><span class="sxs-lookup"><span data-stu-id="c0f96-327">Termination date (required upon termination)</span></span>
- <span data-ttu-id="c0f96-328">Darba attiecību pārtraukšanas iemesls (jānorāda, kad tiek pārtrauktas darba attiecības)</span><span class="sxs-lookup"><span data-stu-id="c0f96-328">Termination reason (required upon termination)</span></span>

<span data-ttu-id="c0f96-329">Darbinieka galvenie datumi tiek iegūti, izmantojot tālāk norādīto informāciju.</span><span class="sxs-lookup"><span data-stu-id="c0f96-329">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="c0f96-330">Talent</span><span class="sxs-lookup"><span data-stu-id="c0f96-330">Talent</span></span>                | <span data-ttu-id="c0f96-331">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c0f96-331">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0f96-332">Pēdējais nomas datums</span><span class="sxs-lookup"><span data-stu-id="c0f96-332">Most recent hire date</span></span> | <span data-ttu-id="c0f96-333">Pašreizējā nepārtrauktās nodarbinātības vēstures ieraksta nodarbinātības sākums</span><span class="sxs-lookup"><span data-stu-id="c0f96-333">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="c0f96-334">Izbeigšanas datums</span><span class="sxs-lookup"><span data-stu-id="c0f96-334">Termination date</span></span>      | <span data-ttu-id="c0f96-335">Pašreizējā nepārtrauktās nodarbinātības vēstures ieraksta darba attiecību pārtraukšanas datums</span><span class="sxs-lookup"><span data-stu-id="c0f96-335">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="c0f96-336">Pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="c0f96-336">Start date</span></span>            | <span data-ttu-id="c0f96-337">Pašreizējā neaktīvā nodarbinātības vēstures ieraksta koriģētais sākuma datums, sākuma datums vai nodarbinātības sākums</span><span class="sxs-lookup"><span data-stu-id="c0f96-337">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="c0f96-338">Sākotnējais darbā pieņemšanas datums</span><span class="sxs-lookup"><span data-stu-id="c0f96-338">Original hire date</span></span>    | <span data-ttu-id="c0f96-339">Agrākā nodarbinātības vēstures ieraksta nodarbinātības sākums</span><span class="sxs-lookup"><span data-stu-id="c0f96-339">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="c0f96-340">Atlīdzība</span><span class="sxs-lookup"><span data-stu-id="c0f96-340">Compensation</span></span>

<span data-ttu-id="c0f96-341">Fiksētās atlīdzības plānam ir jābūt saistītam ar katra darbinieka primāro amatu visā nodarbinātības periodā.</span><span class="sxs-lookup"><span data-stu-id="c0f96-341">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="c0f96-342">Šis periods sākas ar datumu, kurā darbinieks tika pieņemts darbā (vai nodarbinātības sākuma datumu), un turpinās līdz darba attiecību pārtraukšanai.</span><span class="sxs-lookup"><span data-stu-id="c0f96-342">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="c0f96-343">Spēkā stāšanās datums (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-343">Effective Date (required)</span></span>
- <span data-ttu-id="c0f96-344">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="c0f96-344">Expiration date</span></span>
- <span data-ttu-id="c0f96-345">Apmaksas likme (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-345">Pay Rate (required)</span></span>
- <span data-ttu-id="c0f96-346">Apmaksas likmes konvertēšanas gadījumi (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-346">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="c0f96-347">Gada ekvivalents (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-347">Annual equivalent (required)</span></span>
- <span data-ttu-id="c0f96-348">Stundas ekvivalents (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-348">Hourly equivalent (required)</span></span>

<span data-ttu-id="c0f96-349">Ja darbiniekam ar stundas likmi ir vairāki amati, pakalpojumā Dayforce kā darbinieka līmeņa pamatlikme/alga tiek importēta primārā amata fiksētā atlīdzība.</span><span class="sxs-lookup"><span data-stu-id="c0f96-349">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="c0f96-350">To amatu, kas nav primārie, stundas likme tiek saglabāta pakalpojumā Dayforce attiecīgajā amatā.</span><span class="sxs-lookup"><span data-stu-id="c0f96-350">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="c0f96-351">Ja darbiniekam, kurš saņem algu, ir vairāki amati, kā darbinieka līmeņa pamatlikme/alga tiek iegūta un izmantota visu aktīvo amatu kopējā stundas likme un gada alga.</span><span class="sxs-lookup"><span data-stu-id="c0f96-351">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="c0f96-352">Identifikācijas numuri</span><span class="sxs-lookup"><span data-stu-id="c0f96-352">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="c0f96-353">Sociālās apdrošināšanas numurs</span><span class="sxs-lookup"><span data-stu-id="c0f96-353">Social Security identifier</span></span> 

<span data-ttu-id="c0f96-354">Katram darbiniekam ir jābūt vienam primārajam numuram.</span><span class="sxs-lookup"><span data-stu-id="c0f96-354">Every employee must have one primary identifier.</span></span> <span data-ttu-id="c0f96-355">Šī numura identifikācijas tipam ir jābūt **SAN**.</span><span class="sxs-lookup"><span data-stu-id="c0f96-355">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="c0f96-356">Pakalpojumā Dayforce tas tiek automātiski iegūts kā darbinieka sociālās apdrošināšanas numurs, kas ir jānorāda, kad darbinieks tiek pieņemts darbā.</span><span class="sxs-lookup"><span data-stu-id="c0f96-356">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="c0f96-357">Primārais (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-357">Primary (required)</span></span>
- <span data-ttu-id="c0f96-358">Identifikācijas tips = SAN</span><span class="sxs-lookup"><span data-stu-id="c0f96-358">Identification Type = "SSN"</span></span>
- <span data-ttu-id="c0f96-359">Izdošanas datums</span><span class="sxs-lookup"><span data-stu-id="c0f96-359">Issued Date</span></span>
- <span data-ttu-id="c0f96-360">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="c0f96-360">Expiration Date</span></span>

<span data-ttu-id="c0f96-361">Darbinieki var sniegt vairākus identifikācijas numurus, kuru identifikācijas tips ir **SAN**.</span><span class="sxs-lookup"><span data-stu-id="c0f96-361">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="c0f96-362">Taču pakalpojumā Dayforce tiek integrēts tikai ieraksts, kas ir atzīmēts kā **Primārais**, neatkarīgi no tā, vai šis numurs ir aktīvs vai tam ir beidzies derīgums.</span><span class="sxs-lookup"><span data-stu-id="c0f96-362">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="c0f96-363">Banku konti un izdevumi</span><span class="sxs-lookup"><span data-stu-id="c0f96-363">Bank accounts and disbursements</span></span>

<span data-ttu-id="c0f96-364">Jebkuram darbiniekam, kurš samaksu izvēlējies saņemt bankas konta pārskaitījuma veidā, ir jāievada derīga bankas konta informācija.</span><span class="sxs-lookup"><span data-stu-id="c0f96-364">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="c0f96-365">Talent</span><span class="sxs-lookup"><span data-stu-id="c0f96-365">Talent</span></span>                         | <span data-ttu-id="c0f96-366">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c0f96-366">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0f96-367">Bankas konta numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-367">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="c0f96-368">SWIFT kods (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-368">SWIFT code (required)</span></span>          | <span data-ttu-id="c0f96-369">Lauku **Bankas ID** izmanto, apstrādājot algas Meksikā.</span><span class="sxs-lookup"><span data-stu-id="c0f96-369">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="c0f96-370">Filiāles numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-370">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="c0f96-371">Bankas konta tips (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-371">Bank account type (required)</span></span>   | <span data-ttu-id="c0f96-372">Lauku **Konta tips** izmanto, apstrādājot algas Meksikā.</span><span class="sxs-lookup"><span data-stu-id="c0f96-372">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="c0f96-373">Atbalstītās vērtības ir, piemēram, **Norēķini** un **Algas**.</span><span class="sxs-lookup"><span data-stu-id="c0f96-373">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="c0f96-374">Darbiniekiem, kuri samaksu izvēlas saņemt bankas konta pārskaitījumu veidā, ir jāsniedz saite uz juridiskās personas, kuras primārā adrese ir Meksikā, atlikumu kontu, kas ir saistīts ar derīgu Meksikas bankas kontu.</span><span class="sxs-lookup"><span data-stu-id="c0f96-374">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="c0f96-375">Visi pārējie konti, kas nav atlikumu konti, tiek ignorēti.</span><span class="sxs-lookup"><span data-stu-id="c0f96-375">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="c0f96-376">Adreses informācija</span><span class="sxs-lookup"><span data-stu-id="c0f96-376">Address information</span></span>

<span data-ttu-id="c0f96-377">Katram darbiniekam ir jābūt vienai primārajai vietai.</span><span class="sxs-lookup"><span data-stu-id="c0f96-377">Every employee must have one primary location.</span></span> <span data-ttu-id="c0f96-378">Pakalpojumā Dayforce šī vieta tiek izmantota, lai nodokļu piemērošanas nolūkos noteiktu darbinieka primāro dzīvesvietu.</span><span class="sxs-lookup"><span data-stu-id="c0f96-378">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="c0f96-379">Primārā (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-379">Primary (required)</span></span>
- <span data-ttu-id="c0f96-380">Valsts/reģions (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-380">Country/region (required)</span></span>
- <span data-ttu-id="c0f96-381">Pasta indekss (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-381">Zip/postal code (required)</span></span>
- <span data-ttu-id="c0f96-382">Iela (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-382">Street (required)</span></span>
- <span data-ttu-id="c0f96-383">Ielas numurs (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-383">Street Number (required)</span></span>
- <span data-ttu-id="c0f96-384">Mājas numurs/nosaukums</span><span class="sxs-lookup"><span data-stu-id="c0f96-384">Building Complement</span></span>
- <span data-ttu-id="c0f96-385">Pilsēta (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-385">City (required)</span></span>
- <span data-ttu-id="c0f96-386">Administratīvais apgabals (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-386">State (required)</span></span>
- <span data-ttu-id="c0f96-387">Apgabals (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-387">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="c0f96-388">Datu konfigurēšana algu ģenerēšanai Amerikas Savienotajās Valstīs un Kanādā</span><span class="sxs-lookup"><span data-stu-id="c0f96-388">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="c0f96-389">Ja ģenerējat algas darbiniekiem Amerikas Savienotajās Valstīs un Kanādā, ir jākonfigurē tālāk norādītie elementi.</span><span class="sxs-lookup"><span data-stu-id="c0f96-389">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="c0f96-390">Amatiem ir jānorāda nodaļas.</span><span class="sxs-lookup"><span data-stu-id="c0f96-390">Departments are required on positions.</span></span>
- <span data-ttu-id="c0f96-391">Izmaksu centri ir jāiestata kā finanšu dimensijas, un tiem ir jābūt pirmajiem elementiem noklusējuma finanšu dimensijas virknē.</span><span class="sxs-lookup"><span data-stu-id="c0f96-391">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="c0f96-392">Varat konfigurēt Talent, lai amatiem būtu jānorāda nodaļa.</span><span class="sxs-lookup"><span data-stu-id="c0f96-392">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="c0f96-393">Lai to izdarītu, pārejiet uz **Personāla vadības kopīgotie amati > Amati > Pieprasīt amatiem nodaļas**.</span><span class="sxs-lookup"><span data-stu-id="c0f96-393">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="c0f96-394">Ieteicams piemērot šo iestatījumu integrācijai.</span><span class="sxs-lookup"><span data-stu-id="c0f96-394">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="c0f96-395">Darba tipi</span><span class="sxs-lookup"><span data-stu-id="c0f96-395">Job types</span></span>

<span data-ttu-id="c0f96-396">Darbu veidi tiek izmantoti, lai līdzīgus darbus grupētu kategorijās.</span><span class="sxs-lookup"><span data-stu-id="c0f96-396">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="c0f96-397">Darbu veidi ir nepieciešami, lai apstrādātu algas Amerikas Savienotajās Valstīs un Kanādā.</span><span class="sxs-lookup"><span data-stu-id="c0f96-397">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="c0f96-398">Daži darbu veidu piemēri ir pilna laika, nepilna laika, algots un stundu apmaksas darbs.</span><span class="sxs-lookup"><span data-stu-id="c0f96-398">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="c0f96-399">Darbu veidi tiek kartēti uz pakalpojumu Dayforce kā apmaksas tipi, lai norādītu, vai darbinieks saņem stundas samaksu vai algu.</span><span class="sxs-lookup"><span data-stu-id="c0f96-399">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="c0f96-400">Ir jānorāda tālāk norādītie darbu veidi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="c0f96-400">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="c0f96-401">Darba veids</span><span class="sxs-lookup"><span data-stu-id="c0f96-401">Job type</span></span>   | <span data-ttu-id="c0f96-402">apraksts</span><span class="sxs-lookup"><span data-stu-id="c0f96-402">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="c0f96-403">Ik stundu</span><span class="sxs-lookup"><span data-stu-id="c0f96-403">Hourly</span></span>     | <span data-ttu-id="c0f96-404">Ik stundu</span><span class="sxs-lookup"><span data-stu-id="c0f96-404">Hourly</span></span>      |
| <span data-ttu-id="c0f96-405">Algots</span><span class="sxs-lookup"><span data-stu-id="c0f96-405">Salaried</span></span>   | <span data-ttu-id="c0f96-406">Algots</span><span class="sxs-lookup"><span data-stu-id="c0f96-406">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="c0f96-407">Amatu veidi</span><span class="sxs-lookup"><span data-stu-id="c0f96-407">Position types</span></span> 

<span data-ttu-id="c0f96-408">Amatu veidus izmanto, lai norādītu, vai amats ir pilna laika, nepilna laika vai cita veida darbs.</span><span class="sxs-lookup"><span data-stu-id="c0f96-408">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="c0f96-409">Amatu veidi tiek kartēti uz pakalpojumu Dayforce kā apmaksas klases, lai norādītu, vai darbinieks ir pilna laika vai nepilna laika darbinieks.</span><span class="sxs-lookup"><span data-stu-id="c0f96-409">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="c0f96-410">Ir jānorāda tālāk norādītie amatu veidi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="c0f96-410">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="c0f96-411">Amata tips</span><span class="sxs-lookup"><span data-stu-id="c0f96-411">Position type</span></span>   | <span data-ttu-id="c0f96-412">apraksts</span><span class="sxs-lookup"><span data-stu-id="c0f96-412">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="c0f96-413">Pilna laika</span><span class="sxs-lookup"><span data-stu-id="c0f96-413">Full-time</span></span>       | <span data-ttu-id="c0f96-414">Pilna laika darbinieks</span><span class="sxs-lookup"><span data-stu-id="c0f96-414">Full time employee</span></span> |
| <span data-ttu-id="c0f96-415">Nepilna laika</span><span class="sxs-lookup"><span data-stu-id="c0f96-415">Part-time</span></span>       | <span data-ttu-id="c0f96-416">Nepilna laika darbinieks</span><span class="sxs-lookup"><span data-stu-id="c0f96-416">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="c0f96-417">Iemeslu kodi</span><span class="sxs-lookup"><span data-stu-id="c0f96-417">Reason codes</span></span>

<span data-ttu-id="c0f96-418">Iemeslu kodi sniedz informāciju par darbinieka statusu.</span><span class="sxs-lookup"><span data-stu-id="c0f96-418">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="c0f96-419">Iemeslu kodu tiek kartēti uz pakalpojumu Dayforce kā statusa iemesli, kas norāda darbinieka amata vai nodarbinātības statusa izmaiņu iemeslu.</span><span class="sxs-lookup"><span data-stu-id="c0f96-419">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="c0f96-420">Ir jānorāda tālāk norādītie iemeslu kodi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="c0f96-420">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="c0f96-421">Iemeslu kodi</span><span class="sxs-lookup"><span data-stu-id="c0f96-421">Reason code</span></span>    | <span data-ttu-id="c0f96-422">apraksts</span><span class="sxs-lookup"><span data-stu-id="c0f96-422">Description</span></span>      | <span data-ttu-id="c0f96-423">Piemērojamie scenāriji</span><span class="sxs-lookup"><span data-stu-id="c0f96-423">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="c0f96-424">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="c0f96-424">RESIGNATION</span></span>    | <span data-ttu-id="c0f96-425">Atlūgums</span><span class="sxs-lookup"><span data-stu-id="c0f96-425">Resignation</span></span>      | <span data-ttu-id="c0f96-426">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="c0f96-426">Terminate worker</span></span>     |
| <span data-ttu-id="c0f96-427">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="c0f96-427">TERMINATION</span></span>    | <span data-ttu-id="c0f96-428">Izbeigšana</span><span class="sxs-lookup"><span data-stu-id="c0f96-428">Termination</span></span>      | <span data-ttu-id="c0f96-429">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="c0f96-429">Terminate worker</span></span>     |
| <span data-ttu-id="c0f96-430">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="c0f96-430">RETIREMENT</span></span>     | <span data-ttu-id="c0f96-431">Aiziešana pensijā</span><span class="sxs-lookup"><span data-stu-id="c0f96-431">Retirement</span></span>       | <span data-ttu-id="c0f96-432">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="c0f96-432">Terminate worker</span></span>     |
| <span data-ttu-id="c0f96-433">CITI</span><span class="sxs-lookup"><span data-stu-id="c0f96-433">OTHER</span></span>          | <span data-ttu-id="c0f96-434">Citi iemesli</span><span class="sxs-lookup"><span data-stu-id="c0f96-434">Other Reasons</span></span>    | <span data-ttu-id="c0f96-435">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="c0f96-435">Terminate worker</span></span>     |
| <span data-ttu-id="c0f96-436">DEATH</span><span class="sxs-lookup"><span data-stu-id="c0f96-436">DEATH</span></span>          | <span data-ttu-id="c0f96-437">Nāve</span><span class="sxs-lookup"><span data-stu-id="c0f96-437">Death</span></span>            | <span data-ttu-id="c0f96-438">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="c0f96-438">Terminate worker</span></span>     |
| <span data-ttu-id="c0f96-439">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="c0f96-439">LEAVEOFABSENCE</span></span> | <span data-ttu-id="c0f96-440">Atvaļinājums</span><span class="sxs-lookup"><span data-stu-id="c0f96-440">Leave of Absence</span></span> | <span data-ttu-id="c0f96-441">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="c0f96-441">Terminate worker</span></span>     |
| <span data-ttu-id="c0f96-442">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="c0f96-442">CONTRACTEND</span></span>    | <span data-ttu-id="c0f96-443">Līguma beigas</span><span class="sxs-lookup"><span data-stu-id="c0f96-443">End of Contract</span></span>  | <span data-ttu-id="c0f96-444">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="c0f96-444">Terminate worker</span></span>     |
| <span data-ttu-id="c0f96-445">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="c0f96-445">SALARYCHANGE</span></span>   | <span data-ttu-id="c0f96-446">Algas izmaiņas</span><span class="sxs-lookup"><span data-stu-id="c0f96-446">Change of Salary</span></span> | <span data-ttu-id="c0f96-447">Atlīdzība</span><span class="sxs-lookup"><span data-stu-id="c0f96-447">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="c0f96-448">Ģimenes stāvoklis</span><span class="sxs-lookup"><span data-stu-id="c0f96-448">Marital status</span></span>

<span data-ttu-id="c0f96-449">Ģimenes statusa vērtības tiek kartētas uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkotas uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="c0f96-449">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="c0f96-450">Tālāk esošajā tabulā ir parādīts, kā ģimenes statusa vērtības tiek kartētas uz pakalpojumu Dayforce.</span><span class="sxs-lookup"><span data-stu-id="c0f96-450">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="c0f96-451">Talent</span><span class="sxs-lookup"><span data-stu-id="c0f96-451">Talent</span></span>                 | <span data-ttu-id="c0f96-452">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c0f96-452">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="c0f96-453">Precējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="c0f96-453">Married</span></span>                | <span data-ttu-id="c0f96-454">Precējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="c0f96-454">Married</span></span>              |
| <span data-ttu-id="c0f96-455">Neprecējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="c0f96-455">Single</span></span>                 | <span data-ttu-id="c0f96-456">Neprecējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="c0f96-456">Single</span></span>               |
| <span data-ttu-id="c0f96-457">Atraitnis</span><span class="sxs-lookup"><span data-stu-id="c0f96-457">Widowed</span></span>                | <span data-ttu-id="c0f96-458">Atraitnis</span><span class="sxs-lookup"><span data-stu-id="c0f96-458">Widowed</span></span>              |
| <span data-ttu-id="c0f96-459">Šķīries (-usies)</span><span class="sxs-lookup"><span data-stu-id="c0f96-459">Divorced</span></span>               | <span data-ttu-id="c0f96-460">Šķīries (-usies)</span><span class="sxs-lookup"><span data-stu-id="c0f96-460">Divorced</span></span>             |
| <span data-ttu-id="c0f96-461">Reģistrētas attiecības</span><span class="sxs-lookup"><span data-stu-id="c0f96-461">Registered Partnership</span></span> | <span data-ttu-id="c0f96-462">Dzīvesbiedrs</span><span class="sxs-lookup"><span data-stu-id="c0f96-462">Domestic Partnership</span></span> |
| <span data-ttu-id="c0f96-463">Neviens</span><span class="sxs-lookup"><span data-stu-id="c0f96-463">None</span></span>                   | <span data-ttu-id="c0f96-464">Neviens</span><span class="sxs-lookup"><span data-stu-id="c0f96-464">None</span></span>                 |
| <span data-ttu-id="c0f96-465">Kopdzīve</span><span class="sxs-lookup"><span data-stu-id="c0f96-465">Cohabiting</span></span>             | <span data-ttu-id="c0f96-466">Kopdzīve</span><span class="sxs-lookup"><span data-stu-id="c0f96-466">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="c0f96-467">Dzimums</span><span class="sxs-lookup"><span data-stu-id="c0f96-467">Gender</span></span>

<span data-ttu-id="c0f96-468">Dzimuma apzīmējumi tiek kartēti uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkoti uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="c0f96-468">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="c0f96-469">Tālāk esošajā tabulā ir parādīts, kā dzimuma apzīmējumi tiek kartēti uz pakalpojumu Dayforce.</span><span class="sxs-lookup"><span data-stu-id="c0f96-469">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="c0f96-470">Talent</span><span class="sxs-lookup"><span data-stu-id="c0f96-470">Talent</span></span>       | <span data-ttu-id="c0f96-471">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c0f96-471">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="c0f96-472">Vīrietis</span><span class="sxs-lookup"><span data-stu-id="c0f96-472">Male</span></span>         | <span data-ttu-id="c0f96-473">Vīrietis</span><span class="sxs-lookup"><span data-stu-id="c0f96-473">Male</span></span>            |
| <span data-ttu-id="c0f96-474">Sieviete</span><span class="sxs-lookup"><span data-stu-id="c0f96-474">Female</span></span>       | <span data-ttu-id="c0f96-475">Sieviete</span><span class="sxs-lookup"><span data-stu-id="c0f96-475">Female</span></span>          |
| <span data-ttu-id="c0f96-476">Nav specifisks</span><span class="sxs-lookup"><span data-stu-id="c0f96-476">Non-specific</span></span> | <span data-ttu-id="c0f96-477">*Netiek atbalstīts*</span><span class="sxs-lookup"><span data-stu-id="c0f96-477">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="c0f96-478">Ienākumu veida kodi</span><span class="sxs-lookup"><span data-stu-id="c0f96-478">Earning codes</span></span>

<span data-ttu-id="c0f96-479">Ienākumu veidu kodi unikāli identificē katra veida ienākumus, ko saņem nodarbinātie.</span><span class="sxs-lookup"><span data-stu-id="c0f96-479">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="c0f96-480">Kodiem ir vairāki ar ienākumiem saistīti parametri, piemēram, uzskaites nosacījumi, nodokļu likumi, pārskatu veidošanas prasības un bruto summas palielināšanas iespēja.</span><span class="sxs-lookup"><span data-stu-id="c0f96-480">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="c0f96-481">Ja tiek izmantota neatbalstīta biežuma vērtība, aprēķinā pēc noklusējuma tiek lietota biežuma vērtība **Katra apmaksa**.</span><span class="sxs-lookup"><span data-stu-id="c0f96-481">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="c0f96-482">Atbalstītās biežuma vērtības</span><span class="sxs-lookup"><span data-stu-id="c0f96-482">Supported frequencies</span></span>

- <span data-ttu-id="c0f96-483">Visus</span><span class="sxs-lookup"><span data-stu-id="c0f96-483">All</span></span>
- <span data-ttu-id="c0f96-484">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="c0f96-484">EVERYPAY</span></span>
- <span data-ttu-id="c0f96-485">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="c0f96-485">EACHPAYPERIOD</span></span>
- <span data-ttu-id="c0f96-486">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="c0f96-486">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="c0f96-487">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="c0f96-487">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="c0f96-488">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0f96-488">1OFMTH</span></span>
- <span data-ttu-id="c0f96-489">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="c0f96-489">LASTOFMTH</span></span>
- <span data-ttu-id="c0f96-490">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0f96-490">2OFMTH</span></span>
- <span data-ttu-id="c0f96-491">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0f96-491">3OFMTH</span></span>
- <span data-ttu-id="c0f96-492">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0f96-492">4OFMTH</span></span>
- <span data-ttu-id="c0f96-493">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0f96-493">5OFMTH</span></span>
- <span data-ttu-id="c0f96-494">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0f96-494">1N2OFMTH</span></span>
- <span data-ttu-id="c0f96-495">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0f96-495">3N4OFMTH</span></span>
- <span data-ttu-id="c0f96-496">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0f96-496">1N3OFMTH</span></span>
- <span data-ttu-id="c0f96-497">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0f96-497">1N4OFMTH</span></span>
- <span data-ttu-id="c0f96-498">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0f96-498">2N3OFMTH</span></span>
- <span data-ttu-id="c0f96-499">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0f96-499">2N4OFMTH</span></span>
- <span data-ttu-id="c0f96-500">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0f96-500">1N2N3OFMTH</span></span>
- <span data-ttu-id="c0f96-501">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0f96-501">1N2N4OFMTH</span></span>
- <span data-ttu-id="c0f96-502">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0f96-502">1N3N4OFMTH</span></span>
- <span data-ttu-id="c0f96-503">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0f96-503">2N3N4OFMTH</span></span>
- <span data-ttu-id="c0f96-504">1N2N3N4OFMTH–1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0f96-504">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="c0f96-505">2N3N4N5OFMth–2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="c0f96-505">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="c0f96-506">1OFQTR–1OFQTR</span><span class="sxs-lookup"><span data-stu-id="c0f96-506">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="c0f96-507">LASTOFQTR–LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="c0f96-507">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="c0f96-508">LASTMTHOFQTR–LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="c0f96-508">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="c0f96-509">1OFYEAR–1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="c0f96-509">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="c0f96-510">LASTOFYEAR–LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="c0f96-510">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="c0f96-511">NOVNDECOFYEAR–NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="c0f96-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="c0f96-512">Adreses</span><span class="sxs-lookup"><span data-stu-id="c0f96-512">Addresses</span></span>

<span data-ttu-id="c0f96-513">Noteiktas valsts vai reģiona, administratīvā apgabala un apgabala (pašvaldības) kodu identifikācijai ir nepieciešami konkrēti formāti, ko var atpazīt pakalpojums Dayforce un valsts/reģiona pakalpojumu sniedzēji.</span><span class="sxs-lookup"><span data-stu-id="c0f96-513">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="c0f96-514">Lai gan pilsētu formāts var būt dažāds, katrai pilsētai ir jābūt saistītai ar administratīvo apgabalu.</span><span class="sxs-lookup"><span data-stu-id="c0f96-514">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="c0f96-515">Talent</span><span class="sxs-lookup"><span data-stu-id="c0f96-515">Talent</span></span>          | <span data-ttu-id="c0f96-516">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c0f96-516">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="c0f96-517">Valsts/reģions</span><span class="sxs-lookup"><span data-stu-id="c0f96-517">Country/Region</span></span>  | <span data-ttu-id="c0f96-518">Valsts kods</span><span class="sxs-lookup"><span data-stu-id="c0f96-518">Country Code</span></span>          |
| <span data-ttu-id="c0f96-519">Pasta indekss</span><span class="sxs-lookup"><span data-stu-id="c0f96-519">Zip/Postal Code</span></span> | <span data-ttu-id="c0f96-520">Pasta indekss</span><span class="sxs-lookup"><span data-stu-id="c0f96-520">Postal Code</span></span>           |
| <span data-ttu-id="c0f96-521">Administratīvais apgabals</span><span class="sxs-lookup"><span data-stu-id="c0f96-521">State</span></span>           | <span data-ttu-id="c0f96-522">Administratīvā apgabala kods</span><span class="sxs-lookup"><span data-stu-id="c0f96-522">State Code</span></span>            |
| <span data-ttu-id="c0f96-523">Pilsēta</span><span class="sxs-lookup"><span data-stu-id="c0f96-523">City</span></span>            | <span data-ttu-id="c0f96-524">Pilsēta</span><span class="sxs-lookup"><span data-stu-id="c0f96-524">City</span></span>                  |
| <span data-ttu-id="c0f96-525">Apgabals</span><span class="sxs-lookup"><span data-stu-id="c0f96-525">County</span></span>          | <span data-ttu-id="c0f96-526">Apgabals (pašvaldība)</span><span class="sxs-lookup"><span data-stu-id="c0f96-526">County (Municipality)</span></span> |
| <span data-ttu-id="c0f96-527">Iela</span><span class="sxs-lookup"><span data-stu-id="c0f96-527">Street</span></span>          | <span data-ttu-id="c0f96-528">Adreses 1. rinda</span><span class="sxs-lookup"><span data-stu-id="c0f96-528">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="c0f96-529">Nodokļu reģioni</span><span class="sxs-lookup"><span data-stu-id="c0f96-529">Tax regions</span></span>

<span data-ttu-id="c0f96-530">Nodokļu reģionus izmanto, lai noteiktu atbilstošos nodokļus, kas jāpiemēro, ģenerējot algu aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="c0f96-530">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="c0f96-531">Nodokļu reģioni tiek kartēti uz pakalpojumu Dayforce kā vietas adreses.</span><span class="sxs-lookup"><span data-stu-id="c0f96-531">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="c0f96-532">Noklusējuma nodokļu reģionam ir jābūt saistītam ar nodarbinātā aktīvo amatu.</span><span class="sxs-lookup"><span data-stu-id="c0f96-532">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="c0f96-533">Nodokļu reģions (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-533">Tax region (required)</span></span>
- <span data-ttu-id="c0f96-534">Valsts/reģions (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-534">Country/Region (required)</span></span>
- <span data-ttu-id="c0f96-535">Administratīvais apgabals (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-535">State (required)</span></span>
- <span data-ttu-id="c0f96-536">Apgabals</span><span class="sxs-lookup"><span data-stu-id="c0f96-536">County</span></span> 
- <span data-ttu-id="c0f96-537">Pilsēta (obligāti)</span><span class="sxs-lookup"><span data-stu-id="c0f96-537">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="c0f96-538">Datu konfigurēšana algu aprēķina ģenerēšanai Meksikā</span><span class="sxs-lookup"><span data-stu-id="c0f96-538">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="c0f96-539">Ja ģenerējat algas darbiniekiem Meksikā, ir jākonfigurē tālāk norādītie elementi.</span><span class="sxs-lookup"><span data-stu-id="c0f96-539">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="c0f96-540">Amatiem ir jānorāda nodaļas.</span><span class="sxs-lookup"><span data-stu-id="c0f96-540">Departments are required on positions.</span></span>
- <span data-ttu-id="c0f96-541">Izmaksu centri ir jāiestata kā finanšu dimensijas, un tiem ir jābūt pirmajiem elementiem noklusējuma finanšu dimensijas virknē.</span><span class="sxs-lookup"><span data-stu-id="c0f96-541">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="c0f96-542">Darba tipi</span><span class="sxs-lookup"><span data-stu-id="c0f96-542">Job types</span></span>

<span data-ttu-id="c0f96-543">Darbu veidi tiek izmantoti, lai līdzīgus darbus grupētu kategorijās.</span><span class="sxs-lookup"><span data-stu-id="c0f96-543">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="c0f96-544">Lai apstrādātu algas Meksikā, ir nepieciešami darbu veidi.</span><span class="sxs-lookup"><span data-stu-id="c0f96-544">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="c0f96-545">Daži darbu veidu piemēri ir pilna laika, nepilna laika, algots un stundu apmaksas darbs.</span><span class="sxs-lookup"><span data-stu-id="c0f96-545">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="c0f96-546">Darbu veidi tiek kartēti uz pakalpojumu Dayforce kā apmaksas tipi, lai norādītu, vai darbinieks saņem stundas samaksu vai algu.</span><span class="sxs-lookup"><span data-stu-id="c0f96-546">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="c0f96-547">Ir jānorāda tālāk norādītie darbu veidi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="c0f96-547">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="c0f96-548">Darba veids</span><span class="sxs-lookup"><span data-stu-id="c0f96-548">Job type</span></span>   | <span data-ttu-id="c0f96-549">apraksts</span><span class="sxs-lookup"><span data-stu-id="c0f96-549">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="c0f96-550">Ik stundu</span><span class="sxs-lookup"><span data-stu-id="c0f96-550">Hourly</span></span>     | <span data-ttu-id="c0f96-551">Stundu (MX)</span><span class="sxs-lookup"><span data-stu-id="c0f96-551">MX Hourly</span></span>   |
| <span data-ttu-id="c0f96-552">Algots</span><span class="sxs-lookup"><span data-stu-id="c0f96-552">Salaried</span></span>   | <span data-ttu-id="c0f96-553">Algots (MX)</span><span class="sxs-lookup"><span data-stu-id="c0f96-553">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="c0f96-554">Amatu veidi</span><span class="sxs-lookup"><span data-stu-id="c0f96-554">Position types</span></span> 

<span data-ttu-id="c0f96-555">Amatu veidus izmanto, lai norādītu, vai amats ir pilna laika, nepilna laika vai cita veida darbs.</span><span class="sxs-lookup"><span data-stu-id="c0f96-555">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="c0f96-556">Amatu veidi tiek kartēti uz pakalpojumu Dayforce kā apmaksas klases, lai norādītu, vai darbinieks ir pilna laika vai nepilna laika darbinieks.</span><span class="sxs-lookup"><span data-stu-id="c0f96-556">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="c0f96-557">Ir jānorāda tālāk norādītie amatu veidi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="c0f96-557">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="c0f96-558">Amata tips</span><span class="sxs-lookup"><span data-stu-id="c0f96-558">Position type</span></span>   | <span data-ttu-id="c0f96-559">apraksts</span><span class="sxs-lookup"><span data-stu-id="c0f96-559">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="c0f96-560">Pilna laika</span><span class="sxs-lookup"><span data-stu-id="c0f96-560">Full-time</span></span>       | <span data-ttu-id="c0f96-561">Pilna laika darbinieks</span><span class="sxs-lookup"><span data-stu-id="c0f96-561">Full time employee</span></span> |
| <span data-ttu-id="c0f96-562">Nepilna laika</span><span class="sxs-lookup"><span data-stu-id="c0f96-562">Part-time</span></span>       | <span data-ttu-id="c0f96-563">Nepilna laika darbinieks</span><span class="sxs-lookup"><span data-stu-id="c0f96-563">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="c0f96-564">Iemeslu kodi</span><span class="sxs-lookup"><span data-stu-id="c0f96-564">Reason codes</span></span>

<span data-ttu-id="c0f96-565">Iemeslu kodi sniedz informāciju par darbinieka statusu.</span><span class="sxs-lookup"><span data-stu-id="c0f96-565">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="c0f96-566">Iemeslu kodu tiek kartēti uz pakalpojumu Dayforce kā statusa iemesli, kas norāda darbinieka amata vai nodarbinātības statusa izmaiņu iemeslu.</span><span class="sxs-lookup"><span data-stu-id="c0f96-566">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="c0f96-567">Ir jānorāda tālāk norādītie iemeslu kodi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="c0f96-567">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="c0f96-568">Iemeslu kodi</span><span class="sxs-lookup"><span data-stu-id="c0f96-568">Reason code</span></span>            | <span data-ttu-id="c0f96-569">apraksts</span><span class="sxs-lookup"><span data-stu-id="c0f96-569">Description</span></span>                    | <span data-ttu-id="c0f96-570">Piemērojamie scenāriji</span><span class="sxs-lookup"><span data-stu-id="c0f96-570">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="c0f96-571">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="c0f96-571">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="c0f96-572">Aiziešana no amata pirms pirmās algas</span><span class="sxs-lookup"><span data-stu-id="c0f96-572">Departure before first payroll</span></span> | <span data-ttu-id="c0f96-573">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="c0f96-573">Terminate worker</span></span>     |
| <span data-ttu-id="c0f96-574">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="c0f96-574">RESIGNATION</span></span>            | <span data-ttu-id="c0f96-575">Atlūgums</span><span class="sxs-lookup"><span data-stu-id="c0f96-575">Resignation</span></span>                    | <span data-ttu-id="c0f96-576">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="c0f96-576">Terminate worker</span></span>     |
| <span data-ttu-id="c0f96-577">PENSION</span><span class="sxs-lookup"><span data-stu-id="c0f96-577">PENSION</span></span>                | <span data-ttu-id="c0f96-578">Pensija</span><span class="sxs-lookup"><span data-stu-id="c0f96-578">Pension</span></span>                        | <span data-ttu-id="c0f96-579">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="c0f96-579">Terminate worker</span></span>     |
| <span data-ttu-id="c0f96-580">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="c0f96-580">TERMINATION</span></span>            | <span data-ttu-id="c0f96-581">Izbeigšana</span><span class="sxs-lookup"><span data-stu-id="c0f96-581">Termination</span></span>                    | <span data-ttu-id="c0f96-582">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="c0f96-582">Terminate worker</span></span>     |
| <span data-ttu-id="c0f96-583">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="c0f96-583">RETIREMENT</span></span>             | <span data-ttu-id="c0f96-584">Aiziešana pensijā</span><span class="sxs-lookup"><span data-stu-id="c0f96-584">Retirement</span></span>                     | <span data-ttu-id="c0f96-585">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="c0f96-585">Terminate worker</span></span>     |
| <span data-ttu-id="c0f96-586">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="c0f96-586">ABSENTEE</span></span>               | <span data-ttu-id="c0f96-587">Darba kavētājs</span><span class="sxs-lookup"><span data-stu-id="c0f96-587">Absentee</span></span>                       | <span data-ttu-id="c0f96-588">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="c0f96-588">Terminate worker</span></span>     |
| <span data-ttu-id="c0f96-589">CITI</span><span class="sxs-lookup"><span data-stu-id="c0f96-589">OTHER</span></span>                  | <span data-ttu-id="c0f96-590">Citi iemesli</span><span class="sxs-lookup"><span data-stu-id="c0f96-590">Other Reasons</span></span>                  | <span data-ttu-id="c0f96-591">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="c0f96-591">Terminate worker</span></span>     |
| <span data-ttu-id="c0f96-592">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="c0f96-592">CLOSURE</span></span>                | <span data-ttu-id="c0f96-593">Uzņēmuma slēgšana</span><span class="sxs-lookup"><span data-stu-id="c0f96-593">Business Closure</span></span>               | <span data-ttu-id="c0f96-594">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="c0f96-594">Terminate worker</span></span>     |
| <span data-ttu-id="c0f96-595">DEATH</span><span class="sxs-lookup"><span data-stu-id="c0f96-595">DEATH</span></span>                  | <span data-ttu-id="c0f96-596">Nāve</span><span class="sxs-lookup"><span data-stu-id="c0f96-596">Death</span></span>                          | <span data-ttu-id="c0f96-597">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="c0f96-597">Terminate worker</span></span>     |
| <span data-ttu-id="c0f96-598">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="c0f96-598">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="c0f96-599">Atvaļinājums</span><span class="sxs-lookup"><span data-stu-id="c0f96-599">Leave of Absence</span></span>               | <span data-ttu-id="c0f96-600">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="c0f96-600">Terminate worker</span></span>     |
| <span data-ttu-id="c0f96-601">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="c0f96-601">CONTRACTEND</span></span>            | <span data-ttu-id="c0f96-602">Līguma beigas</span><span class="sxs-lookup"><span data-stu-id="c0f96-602">End of Contract</span></span>                | <span data-ttu-id="c0f96-603">Pārtraukt darba attiecības ar nodarbināto</span><span class="sxs-lookup"><span data-stu-id="c0f96-603">Terminate worker</span></span>     |
| <span data-ttu-id="c0f96-604">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="c0f96-604">SALARYCHANGE</span></span>           | <span data-ttu-id="c0f96-605">Algas izmaiņas</span><span class="sxs-lookup"><span data-stu-id="c0f96-605">Change of Salary</span></span>               | <span data-ttu-id="c0f96-606">Atlīdzība</span><span class="sxs-lookup"><span data-stu-id="c0f96-606">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="c0f96-607">Nodarbinātības noteikumi</span><span class="sxs-lookup"><span data-stu-id="c0f96-607">Terms of employment</span></span>

<span data-ttu-id="c0f96-608">Nodarbinātības noteikumus izmanto, lai izveidotu nodarbinātības noteikumu kategorijas.</span><span class="sxs-lookup"><span data-stu-id="c0f96-608">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="c0f96-609">Noteikumi tiek kartēti uz pakalpojumu Dayforce kā nodarbinātības rādītāju vērtības.</span><span class="sxs-lookup"><span data-stu-id="c0f96-609">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="c0f96-610">Ir nepieciešami tālāk norādītie nodarbinātības noteikumi un apraksti.</span><span class="sxs-lookup"><span data-stu-id="c0f96-610">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="c0f96-611">Nodarbinātības noteikumi</span><span class="sxs-lookup"><span data-stu-id="c0f96-611">Terms of employment</span></span>   | <span data-ttu-id="c0f96-612">apraksts</span><span class="sxs-lookup"><span data-stu-id="c0f96-612">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="c0f96-613">Regulārs</span><span class="sxs-lookup"><span data-stu-id="c0f96-613">Regular</span></span>               | <span data-ttu-id="c0f96-614">Regulārs</span><span class="sxs-lookup"><span data-stu-id="c0f96-614">Regular</span></span>     |
| <span data-ttu-id="c0f96-615">Tieši</span><span class="sxs-lookup"><span data-stu-id="c0f96-615">Direct</span></span>                | <span data-ttu-id="c0f96-616">Tieši</span><span class="sxs-lookup"><span data-stu-id="c0f96-616">Direct</span></span>      |
| <span data-ttu-id="c0f96-617">Štažēšanās</span><span class="sxs-lookup"><span data-stu-id="c0f96-617">Internship</span></span>            | <span data-ttu-id="c0f96-618">Štažēšanās</span><span class="sxs-lookup"><span data-stu-id="c0f96-618">Internship</span></span>  |
| <span data-ttu-id="c0f96-619">Pastāvīga</span><span class="sxs-lookup"><span data-stu-id="c0f96-619">Permanent</span></span>             | <span data-ttu-id="c0f96-620">Pastāvīga</span><span class="sxs-lookup"><span data-stu-id="c0f96-620">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="c0f96-621">Ģimenes stāvoklis</span><span class="sxs-lookup"><span data-stu-id="c0f96-621">Marital status</span></span>

<span data-ttu-id="c0f96-622">Ģimenes statusa vērtības tiek kartētas uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkotas uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="c0f96-622">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="c0f96-623">Tālāk esošajā tabulā ir parādīts, kā ģimenes statusa vērtības tiek kartētas uz pakalpojumu Dayforce.</span><span class="sxs-lookup"><span data-stu-id="c0f96-623">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="c0f96-624">Talent</span><span class="sxs-lookup"><span data-stu-id="c0f96-624">Talent</span></span>                 | <span data-ttu-id="c0f96-625">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c0f96-625">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="c0f96-626">Precējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="c0f96-626">Married</span></span>                | <span data-ttu-id="c0f96-627">Precējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="c0f96-627">Married</span></span>                   |
| <span data-ttu-id="c0f96-628">Neprecējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="c0f96-628">Single</span></span>                 | <span data-ttu-id="c0f96-629">Neprecējies (-usies)</span><span class="sxs-lookup"><span data-stu-id="c0f96-629">Single</span></span>                    |
| <span data-ttu-id="c0f96-630">Atraitnis</span><span class="sxs-lookup"><span data-stu-id="c0f96-630">Widowed</span></span>                | <span data-ttu-id="c0f96-631">Atraitnis</span><span class="sxs-lookup"><span data-stu-id="c0f96-631">Widowed</span></span>                   |
| <span data-ttu-id="c0f96-632">Šķīries (-usies)</span><span class="sxs-lookup"><span data-stu-id="c0f96-632">Divorced</span></span>               | <span data-ttu-id="c0f96-633">Šķīries (-usies)</span><span class="sxs-lookup"><span data-stu-id="c0f96-633">Divorced</span></span>                  |
| <span data-ttu-id="c0f96-634">Reģistrētas attiecības</span><span class="sxs-lookup"><span data-stu-id="c0f96-634">Registered Partnership</span></span> | <span data-ttu-id="c0f96-635">Dzīvesbiedrs</span><span class="sxs-lookup"><span data-stu-id="c0f96-635">Domestic Partnership</span></span>      |
| <span data-ttu-id="c0f96-636">Neviens</span><span class="sxs-lookup"><span data-stu-id="c0f96-636">None</span></span>                   | <span data-ttu-id="c0f96-637">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="c0f96-637">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="c0f96-638">Kopdzīve</span><span class="sxs-lookup"><span data-stu-id="c0f96-638">Cohabiting</span></span>             | <span data-ttu-id="c0f96-639">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="c0f96-639">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="c0f96-640">Dzimums</span><span class="sxs-lookup"><span data-stu-id="c0f96-640">Gender</span></span>

<span data-ttu-id="c0f96-641">Dzimuma apzīmējumi tiek kartēti uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkoti uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="c0f96-641">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="c0f96-642">Tālāk esošajā tabulā ir parādīts, kā dzimuma apzīmējumi tiek kartēti uz pakalpojumu Dayforce.</span><span class="sxs-lookup"><span data-stu-id="c0f96-642">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="c0f96-643">Talent</span><span class="sxs-lookup"><span data-stu-id="c0f96-643">Talent</span></span>       | <span data-ttu-id="c0f96-644">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c0f96-644">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="c0f96-645">Vīrietis</span><span class="sxs-lookup"><span data-stu-id="c0f96-645">Male</span></span>         | <span data-ttu-id="c0f96-646">Vīrietis</span><span class="sxs-lookup"><span data-stu-id="c0f96-646">Male</span></span>                      |
| <span data-ttu-id="c0f96-647">Sieviete</span><span class="sxs-lookup"><span data-stu-id="c0f96-647">Female</span></span>       | <span data-ttu-id="c0f96-648">Sieviete</span><span class="sxs-lookup"><span data-stu-id="c0f96-648">Female</span></span>                    |
| <span data-ttu-id="c0f96-649">Nav specifisks</span><span class="sxs-lookup"><span data-stu-id="c0f96-649">Non-specific</span></span> | <span data-ttu-id="c0f96-650">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="c0f96-650">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="c0f96-651">Maksājumu metode</span><span class="sxs-lookup"><span data-stu-id="c0f96-651">Payment method</span></span>

<span data-ttu-id="c0f96-652">Maksāšanas metodes darbiniekam un uzņēmumam ļauj aprakstīt, kā darbinieki saņems samaksu.</span><span class="sxs-lookup"><span data-stu-id="c0f96-652">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="c0f96-653">Maksāšanas metodes tiek kartētas uz pakalpojumu Dayforce un integrācijas laikā atbilstoši tulkotas uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="c0f96-653">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="c0f96-654">Tālāk esošajā tabulā ir parādīts, kā maksāšanas metodes tiek kartētas uz pakalpojumu Dayforce.</span><span class="sxs-lookup"><span data-stu-id="c0f96-654">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="c0f96-655">Talent</span><span class="sxs-lookup"><span data-stu-id="c0f96-655">Talent</span></span>             | <span data-ttu-id="c0f96-656">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c0f96-656">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="c0f96-657">Kase</span><span class="sxs-lookup"><span data-stu-id="c0f96-657">Cash</span></span>               | <span data-ttu-id="c0f96-658">Kase</span><span class="sxs-lookup"><span data-stu-id="c0f96-658">Cash</span></span>                      |
| <span data-ttu-id="c0f96-659">Elektronisks maksājums</span><span class="sxs-lookup"><span data-stu-id="c0f96-659">Electronic Payment</span></span> | <span data-ttu-id="c0f96-660">Pārsūtījums</span><span class="sxs-lookup"><span data-stu-id="c0f96-660">Transfer</span></span>                  |
| <span data-ttu-id="c0f96-661">Atzīmēt</span><span class="sxs-lookup"><span data-stu-id="c0f96-661">Check</span></span>              | <span data-ttu-id="c0f96-662">Čeks</span><span class="sxs-lookup"><span data-stu-id="c0f96-662">Cheque</span></span>                    |
| <span data-ttu-id="c0f96-663">Bankas vekselis</span><span class="sxs-lookup"><span data-stu-id="c0f96-663">Bank Draft</span></span>         | <span data-ttu-id="c0f96-664">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="c0f96-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="c0f96-665">Citi</span><span class="sxs-lookup"><span data-stu-id="c0f96-665">Other</span></span>              | <span data-ttu-id="c0f96-666">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="c0f96-666">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="c0f96-667">Bankas konta tips</span><span class="sxs-lookup"><span data-stu-id="c0f96-667">Bank account type</span></span>

<span data-ttu-id="c0f96-668">Bankas kontu tipus izmanto darbiniekiem sūtāmajiem elektroniskajiem maksājumiem.</span><span class="sxs-lookup"><span data-stu-id="c0f96-668">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="c0f96-669">Bankas kontu tipi tiek kartēti uz pakalpojumu Dayforce kā pārsūtīšanas konta informācija.</span><span class="sxs-lookup"><span data-stu-id="c0f96-669">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="c0f96-670">Bankas kontu tipi integrācijas laikā tiek atbilstoši tulkoti uz apstiprinātajām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="c0f96-670">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="c0f96-671">Talent</span><span class="sxs-lookup"><span data-stu-id="c0f96-671">Talent</span></span>            | <span data-ttu-id="c0f96-672">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c0f96-672">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="c0f96-673">Kontroles konts</span><span class="sxs-lookup"><span data-stu-id="c0f96-673">Checking Account</span></span>  | <span data-ttu-id="c0f96-674">CheckingAccount</span><span class="sxs-lookup"><span data-stu-id="c0f96-674">CheckingAccount</span></span>           |
| <span data-ttu-id="c0f96-675">Algu konts</span><span class="sxs-lookup"><span data-stu-id="c0f96-675">Payroll Account</span></span>   | <span data-ttu-id="c0f96-676">PayrollAccount</span><span class="sxs-lookup"><span data-stu-id="c0f96-676">PayrollAccount</span></span>            |
| <span data-ttu-id="c0f96-677">Uzkrājumu konts</span><span class="sxs-lookup"><span data-stu-id="c0f96-677">Savings Account</span></span>   | <span data-ttu-id="c0f96-678">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="c0f96-678">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="c0f96-679">BankGirot konts</span><span class="sxs-lookup"><span data-stu-id="c0f96-679">BankGirot account</span></span> | <span data-ttu-id="c0f96-680">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="c0f96-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="c0f96-681">PlusGirot konts</span><span class="sxs-lookup"><span data-stu-id="c0f96-681">PlusGirot account</span></span> | <span data-ttu-id="c0f96-682">*Netiek atbalstīts Meksikā*</span><span class="sxs-lookup"><span data-stu-id="c0f96-682">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="c0f96-683">Ienākumu veida kodi</span><span class="sxs-lookup"><span data-stu-id="c0f96-683">Earning codes</span></span>

<span data-ttu-id="c0f96-684">Ienākumu veidu kodi unikāli identificē katra veida ienākumus, ko saņem nodarbinātie.</span><span class="sxs-lookup"><span data-stu-id="c0f96-684">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="c0f96-685">Kodiem ir vairāki ar ienākumiem saistīti parametri, piemēram, uzskaites nosacījumi, nodokļu likumi, pārskatu veidošanas prasības un bruto summas palielināšanas iespēja.</span><span class="sxs-lookup"><span data-stu-id="c0f96-685">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="c0f96-686">Ja tiek izmantota neatbalstīta biežuma vērtība, aprēķinā pēc noklusējuma tiek lietota biežuma vērtība **Katra apmaksa**.</span><span class="sxs-lookup"><span data-stu-id="c0f96-686">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="c0f96-687">Atbalstītās biežuma vērtības</span><span class="sxs-lookup"><span data-stu-id="c0f96-687">Supported frequencies</span></span>

- <span data-ttu-id="c0f96-688">Visus</span><span class="sxs-lookup"><span data-stu-id="c0f96-688">All</span></span>
- <span data-ttu-id="c0f96-689">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="c0f96-689">EVERYPAY</span></span>
- <span data-ttu-id="c0f96-690">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="c0f96-690">EACHPAYPERIOD</span></span>
- <span data-ttu-id="c0f96-691">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="c0f96-691">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="c0f96-692">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="c0f96-692">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="c0f96-693">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0f96-693">1OFMTH</span></span>
- <span data-ttu-id="c0f96-694">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="c0f96-694">LASTOFMTH</span></span>
- <span data-ttu-id="c0f96-695">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0f96-695">2OFMTH</span></span>
- <span data-ttu-id="c0f96-696">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0f96-696">3OFMTH</span></span>
- <span data-ttu-id="c0f96-697">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0f96-697">4OFMTH</span></span>
- <span data-ttu-id="c0f96-698">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0f96-698">5OFMTH</span></span>
- <span data-ttu-id="c0f96-699">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0f96-699">1N2OFMTH</span></span>
- <span data-ttu-id="c0f96-700">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0f96-700">3N4OFMTH</span></span>
- <span data-ttu-id="c0f96-701">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0f96-701">1N3OFMTH</span></span>
- <span data-ttu-id="c0f96-702">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0f96-702">1N4OFMTH</span></span>
- <span data-ttu-id="c0f96-703">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0f96-703">2N3OFMTH</span></span>
- <span data-ttu-id="c0f96-704">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0f96-704">2N4OFMTH</span></span>
- <span data-ttu-id="c0f96-705">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0f96-705">1N2N3OFMTH</span></span>
- <span data-ttu-id="c0f96-706">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0f96-706">1N2N4OFMTH</span></span>
- <span data-ttu-id="c0f96-707">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0f96-707">1N3N4OFMTH</span></span>
- <span data-ttu-id="c0f96-708">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0f96-708">2N3N4OFMTH</span></span>
- <span data-ttu-id="c0f96-709">1N2N3N4OFMTH–1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="c0f96-709">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="c0f96-710">2N3N4N5OFMth–2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="c0f96-710">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="c0f96-711">1OFQTR–1OFQTR</span><span class="sxs-lookup"><span data-stu-id="c0f96-711">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="c0f96-712">LASTOFQTR–LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="c0f96-712">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="c0f96-713">LASTMTHOFQTR–LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="c0f96-713">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="c0f96-714">1OFYEAR–1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="c0f96-714">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="c0f96-715">LASTOFYEAR–LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="c0f96-715">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="c0f96-716">NOVNDECOFYEAR–NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="c0f96-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="c0f96-717">Adreses</span><span class="sxs-lookup"><span data-stu-id="c0f96-717">Addresses</span></span>

<span data-ttu-id="c0f96-718">Noteiktas valsts vai reģiona, administratīvā apgabala un apgabala (pašvaldības) kodu identifikācijai ir nepieciešami konkrēti formāti, ko var atpazīt pakalpojums Dayforce un valsts/reģiona pakalpojumu sniedzēji.</span><span class="sxs-lookup"><span data-stu-id="c0f96-718">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="c0f96-719">Lai gan pilsētu formāts var būt dažāds, katrai pilsētai ir jābūt saistītai ar administratīvo apgabalu.</span><span class="sxs-lookup"><span data-stu-id="c0f96-719">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="c0f96-720">Talent</span><span class="sxs-lookup"><span data-stu-id="c0f96-720">Talent</span></span>              | <span data-ttu-id="c0f96-721">Dayforce</span><span class="sxs-lookup"><span data-stu-id="c0f96-721">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="c0f96-722">Valsts/reģions</span><span class="sxs-lookup"><span data-stu-id="c0f96-722">Country/Region</span></span>      | <span data-ttu-id="c0f96-723">Valsts kods</span><span class="sxs-lookup"><span data-stu-id="c0f96-723">Country Code</span></span>          |
| <span data-ttu-id="c0f96-724">Pasta indekss</span><span class="sxs-lookup"><span data-stu-id="c0f96-724">Zip/Postal Code</span></span>     | <span data-ttu-id="c0f96-725">Pasta indekss</span><span class="sxs-lookup"><span data-stu-id="c0f96-725">Postal Code</span></span>           |
| <span data-ttu-id="c0f96-726">Administratīvais apgabals</span><span class="sxs-lookup"><span data-stu-id="c0f96-726">State</span></span>               | <span data-ttu-id="c0f96-727">Administratīvā apgabala kods</span><span class="sxs-lookup"><span data-stu-id="c0f96-727">State Code</span></span>            |
| <span data-ttu-id="c0f96-728">Pilsēta</span><span class="sxs-lookup"><span data-stu-id="c0f96-728">City</span></span>                | <span data-ttu-id="c0f96-729">Pilsēta</span><span class="sxs-lookup"><span data-stu-id="c0f96-729">City</span></span>                  |
| <span data-ttu-id="c0f96-730">Apgabals</span><span class="sxs-lookup"><span data-stu-id="c0f96-730">County</span></span>              | <span data-ttu-id="c0f96-731">Apgabals (pašvaldība)</span><span class="sxs-lookup"><span data-stu-id="c0f96-731">County (Municipality)</span></span> |
| <span data-ttu-id="c0f96-732">Iela</span><span class="sxs-lookup"><span data-stu-id="c0f96-732">Street</span></span>              | <span data-ttu-id="c0f96-733">Adreses 1. rinda</span><span class="sxs-lookup"><span data-stu-id="c0f96-733">Address Line 1</span></span>        |
| <span data-ttu-id="c0f96-734">Ielas numurs</span><span class="sxs-lookup"><span data-stu-id="c0f96-734">Street Number</span></span>       | <span data-ttu-id="c0f96-735">Adreses 2. rinda</span><span class="sxs-lookup"><span data-stu-id="c0f96-735">Address Line 2</span></span>        |
| <span data-ttu-id="c0f96-736">Mājas numurs/nosaukums</span><span class="sxs-lookup"><span data-stu-id="c0f96-736">Building Complement</span></span> | <span data-ttu-id="c0f96-737">Adreses 5. rinda</span><span class="sxs-lookup"><span data-stu-id="c0f96-737">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="c0f96-738">Pases numurs</span><span class="sxs-lookup"><span data-stu-id="c0f96-738">Passport number</span></span>

<span data-ttu-id="c0f96-739">Darbinieki var sniegt pases informāciju.</span><span class="sxs-lookup"><span data-stu-id="c0f96-739">Employees can declare passport information.</span></span> <span data-ttu-id="c0f96-740">Šīs informācijas identifikācijas tips ir **Pase**, un tā tiek integrēta pakalpojumā Dayforce kā daļa no darbinieka Meksikai specifiskās informācijas.</span><span class="sxs-lookup"><span data-stu-id="c0f96-740">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="c0f96-741">Identifikācijas tips = Pase</span><span class="sxs-lookup"><span data-stu-id="c0f96-741">Identification Type = "Passport"</span></span>
- <span data-ttu-id="c0f96-742">Izdošanas datums</span><span class="sxs-lookup"><span data-stu-id="c0f96-742">Issued Date</span></span>
- <span data-ttu-id="c0f96-743">Beigu datums</span><span class="sxs-lookup"><span data-stu-id="c0f96-743">Expiration Date</span></span>

<span data-ttu-id="c0f96-744">Darbinieki var sniegt vairākus identifikācijas numurus, kuru identifikācijas tips ir **Pase**.</span><span class="sxs-lookup"><span data-stu-id="c0f96-744">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="c0f96-745">Taču pakalpojumā Dayforce tiek integrēts tikai pašreizējais aktīvais pases ieraksts.</span><span class="sxs-lookup"><span data-stu-id="c0f96-745">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="c0f96-746">Ja visiem pases ierakstiem ir beidzies derīgiem, pakalpojumā Dayforce tiek integrēta pēdējā izdotā pase.</span><span class="sxs-lookup"><span data-stu-id="c0f96-746">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
