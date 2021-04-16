---
title: Izcelsmes valsts/reģions
description: Daudzas organizācijas izsniedz sertifikātus saviem kreditoriem, lai nodrošinātu preču atbilstību noteiktiem sertifikācijas standartiem. Šie sertifikāti bieži ir atkarīgi no izcelsmes valsts/reģiona. Šajā tēmā ir sniegta informācija par izcelsmes valsts/reģiona līdzekli, kas ļauj saistīt preci ar tās izcelsmes valsti/reģionu un sekot tās preču sertifikācijai.
author: dasani-madipalli
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: COOVendorCerts
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: b07747752dd09f39c3a7a9a647cc3d10cc4b5cc7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829550"
---
# <a name="country-of-origin"></a><span data-ttu-id="6272b-105">Izcelsmes valsts/reģions</span><span class="sxs-lookup"><span data-stu-id="6272b-105">Country of origin</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6272b-106">Daudzas organizācijas izsniedz sertifikātus saviem kreditoriem, lai nodrošinātu preču atbilstību noteiktiem sertifikācijas standartiem.</span><span class="sxs-lookup"><span data-stu-id="6272b-106">Many organizations issue certificates to their vendors to ensure that products meet specific certification standards.</span></span> <span data-ttu-id="6272b-107">Šie sertifikāti bieži ir atkarīgi no izcelsmes valsts/reģiona.</span><span class="sxs-lookup"><span data-stu-id="6272b-107">These certificates often depend on the country of origin.</span></span> <span data-ttu-id="6272b-108">Izcelsmes valsts/reģiona līdzeklis ļauj saistīt preci ar tās izcelsmes valsti/reģionu un sekot tās preču sertifikācijai.</span><span class="sxs-lookup"><span data-stu-id="6272b-108">The country of origin feature lets you link a product to its country of origin and keep track of its product certifications.</span></span>

## <a name="turn-on-the-country-of-origin-feature"></a><span data-ttu-id="6272b-109">Ieslēgt izcelsmes valsts līdzekli</span><span class="sxs-lookup"><span data-stu-id="6272b-109">Turn on the country of origin feature</span></span>

<span data-ttu-id="6272b-110">Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="6272b-110">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="6272b-111">Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu.</span><span class="sxs-lookup"><span data-stu-id="6272b-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="6272b-112">Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:</span><span class="sxs-lookup"><span data-stu-id="6272b-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="6272b-113">**Modulis:** *Preču informācijas pārvaldība*</span><span class="sxs-lookup"><span data-stu-id="6272b-113">**Module:** *Product information management*</span></span>
- <span data-ttu-id="6272b-114">**Līdzekļa nosaukums:** *Izcelsmes valsts pārvaldības līdzeklis*</span><span class="sxs-lookup"><span data-stu-id="6272b-114">**Feature name:** *Country of origin management feature*</span></span>

## <a name="configure-source-and-destination-countries"></a><span data-ttu-id="6272b-115">Izcelsmes un galamērķa valstu/reģionu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="6272b-115">Configure source and destination countries</span></span>

<span data-ttu-id="6272b-116">Pirms izdot preces sertifikātu, prece ir jāsaista ar tās galamērķa valsti un tās izcelsmes valsti/reģionu.</span><span class="sxs-lookup"><span data-stu-id="6272b-116">Before you issue a certificate for a product, you must link the product to its destination country and its country of origin.</span></span>

1. <span data-ttu-id="6272b-117">Dodieties uz **Preču informācijas pārvaldība \> Iestatīšana \> Preču atbilstība \> Izcelsmes valsts/reģions \> Izcelsmes valsts/reģiona noteikumi**.</span><span class="sxs-lookup"><span data-stu-id="6272b-117">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin rules**.</span></span>
2. <span data-ttu-id="6272b-118">Atlasiet rediģēšanai esošu valsts iestatījumu vai darbību rūtī atlasiet **Jauns**, lai izveidotu jaunu valsts iestatījumu.</span><span class="sxs-lookup"><span data-stu-id="6272b-118">Select an existing country setup to edit, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="6272b-119">Atlasītajai vai jaunajai valstij iestatiet šādas vērtības.</span><span class="sxs-lookup"><span data-stu-id="6272b-119">Set the following values for the selected or new country.</span></span>

    | <span data-ttu-id="6272b-120">Lauks</span><span class="sxs-lookup"><span data-stu-id="6272b-120">Field</span></span> | <span data-ttu-id="6272b-121">apraksts</span><span class="sxs-lookup"><span data-stu-id="6272b-121">Description</span></span> |
    |---|---|
    | <span data-ttu-id="6272b-122">Krājums</span><span class="sxs-lookup"><span data-stu-id="6272b-122">Item number</span></span> | <span data-ttu-id="6272b-123">Atlasiet preces krājuma kodu.</span><span class="sxs-lookup"><span data-stu-id="6272b-123">Select the item number of the product.</span></span> |
    | <span data-ttu-id="6272b-124">Galamērķa valsts</span><span class="sxs-lookup"><span data-stu-id="6272b-124">Destination country</span></span> | <span data-ttu-id="6272b-125">Atlasiet, uz kuru valsti sūtīt preci.</span><span class="sxs-lookup"><span data-stu-id="6272b-125">Select the country that you're sending the product to.</span></span> |
    | <span data-ttu-id="6272b-126">Izcelsmes valsts</span><span class="sxs-lookup"><span data-stu-id="6272b-126">Origin country</span></span> | <span data-ttu-id="6272b-127">Atlasiet, no kuras valsts prece tiek sūtīta.</span><span class="sxs-lookup"><span data-stu-id="6272b-127">Select the country that you're shipping the product from.</span></span> |

<span data-ttu-id="6272b-128">Šī iestatījuma nolūks ir palīdzēt ģenerēt materiālu komplekta (MK) pārskatu, kurā var iekļaut izcelsmes valsti katrai daļai, kam ir norādītas izcelsmes un galamērķa valstis.</span><span class="sxs-lookup"><span data-stu-id="6272b-128">The purpose of this setup is to help you generate a bill of materials (BOM) report where you can include the country of origin for each part that source and destination countries are specified for.</span></span> <span data-ttu-id="6272b-129">Šis pārskats palīdzēs iegūt visaptverošu priekšstatu par to, no kurienes daļas ir un uz kurieni tās sūta.</span><span class="sxs-lookup"><span data-stu-id="6272b-129">This report will help you get a holistic picture of where your parts come from and where they are going.</span></span>

## <a name="keep-track-of-vendor-certificates"></a><span data-ttu-id="6272b-130">Kreditora sertifikātu pārraudzīšana</span><span class="sxs-lookup"><span data-stu-id="6272b-130">Keep track of vendor certificates</span></span>

<span data-ttu-id="6272b-131">Varat izmantot lapu **Izcelsmes valsts/reģiona kreditoru sertifikāti**, lai sekotu sertifikātiem, ko izsniedzat kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="6272b-131">You can use the **Country of origin vendor certificates** page to keep track of certificates that you issue to vendors.</span></span>

<span data-ttu-id="6272b-132">Jums ir jāizlemj, kurus sertifikātu dokumentus jūs izsniedzat un kā par tiem paziņosit klientiem.</span><span class="sxs-lookup"><span data-stu-id="6272b-132">You must decide which certificate documents you're issuing and how you will report them to customers.</span></span> <span data-ttu-id="6272b-133">Šis līdzeklis palīdz sekot līdzi jūsu sertifikātiem.</span><span class="sxs-lookup"><span data-stu-id="6272b-133">This feature helps you keep track of your certificates.</span></span> <span data-ttu-id="6272b-134">Tas arī ļauj izvēlēties, vai attiecīgie sertifikātu numuri ir redzami rēķinos, pavadzīmēs un/vai pasūtījumu apstiprinājumos.</span><span class="sxs-lookup"><span data-stu-id="6272b-134">It also lets you choose whether the relevant certificate numbers appear on invoices, packing slips, and/or order confirmations.</span></span>

<span data-ttu-id="6272b-135">Lai iestatītu sertifikāta informāciju, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="6272b-135">To set up your certificate information, follow these steps.</span></span>

1. <span data-ttu-id="6272b-136">Dodieties uz **Preču informācijas pārvaldība \> Iestatīšana \> Preču atbilstība \> Izcelsmes valsts/reģions \> Izcelsmes valsts/reģiona kreditora sertifikāti**.</span><span class="sxs-lookup"><span data-stu-id="6272b-136">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin vendor certificates**.</span></span>
2. <span data-ttu-id="6272b-137">Atlasiet rediģēšanai esošu sertifikāta iestatījumu vai darbību rūtī atlasiet **Jauns**, lai izveidotu jaunu sertifikāta iestatījumu.</span><span class="sxs-lookup"><span data-stu-id="6272b-137">Select an existing certificate setup to edit, or select **New** on the Action Pane to create a new certificate setup.</span></span>
3. <span data-ttu-id="6272b-138">Atlasītajam vai jaunajam sertifikātam iestatiet šādus iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="6272b-138">Set the following settings for the selected or new certificate.</span></span>

    | <span data-ttu-id="6272b-139">Lauks</span><span class="sxs-lookup"><span data-stu-id="6272b-139">Field</span></span> | <span data-ttu-id="6272b-140">apraksts</span><span class="sxs-lookup"><span data-stu-id="6272b-140">Description</span></span> |
    |---|---|
    | <span data-ttu-id="6272b-141">Kreditora konts</span><span class="sxs-lookup"><span data-stu-id="6272b-141">Vendor account</span></span> | <span data-ttu-id="6272b-142">Atlasiet kreditoru, kuram sertifikāts izsniegts.</span><span class="sxs-lookup"><span data-stu-id="6272b-142">Select the vendor that you issued the certificate to.</span></span> |
    | <span data-ttu-id="6272b-143">Krājums</span><span class="sxs-lookup"><span data-stu-id="6272b-143">Item number</span></span> | <span data-ttu-id="6272b-144">Atlasiet krājumu, kuram sertifikāts izsniegts.</span><span class="sxs-lookup"><span data-stu-id="6272b-144">Select the item that you issued the certificate for.</span></span> |
    | <span data-ttu-id="6272b-145">Valsts/reģions</span><span class="sxs-lookup"><span data-stu-id="6272b-145">Country/region</span></span> | <span data-ttu-id="6272b-146">Galamērķa valsts vai reģions, kurā jāizmanto šis sertifikāts.</span><span class="sxs-lookup"><span data-stu-id="6272b-146">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="6272b-147">Sertifikāta numurs</span><span class="sxs-lookup"><span data-stu-id="6272b-147">Certificate number</span></span> | <span data-ttu-id="6272b-148">Ievadiet izsniegtā sertifikāta identifikācijas numuru.</span><span class="sxs-lookup"><span data-stu-id="6272b-148">Enter the identification number of the certificate that you issued.</span></span> |
    | <span data-ttu-id="6272b-149">Spēkā esošs</span><span class="sxs-lookup"><span data-stu-id="6272b-149">Effective</span></span> | <span data-ttu-id="6272b-150">Atlasiet pirmo datumu, kad pašreizējais sertifikāts ir derīgs.</span><span class="sxs-lookup"><span data-stu-id="6272b-150">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="6272b-151">Termiņa beigas</span><span class="sxs-lookup"><span data-stu-id="6272b-151">Expiration</span></span> | <span data-ttu-id="6272b-152">Atlasiet pēdējo datumu, kad pašreizējais sertifikāts ir derīgs.</span><span class="sxs-lookup"><span data-stu-id="6272b-152">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="6272b-153">Drukāt rēķinā</span><span class="sxs-lookup"><span data-stu-id="6272b-153">Print on invoice</span></span> | <span data-ttu-id="6272b-154">Atzīmējiet šo izvēles rūtiņu, lai drukātu sertifikāta numuru rēķinos, kas norādītajā datumu diapazonā ir adresēti norādītajai valstij.</span><span class="sxs-lookup"><span data-stu-id="6272b-154">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="6272b-155">Drukāt pavadzīmē</span><span class="sxs-lookup"><span data-stu-id="6272b-155">Print on packing slip</span></span> | <span data-ttu-id="6272b-156">Atzīmējiet šo izvēles rūtiņu, lai drukātu sertifikāta numuru pavadzīmēs, kas norādītajā datumu diapazonā ir adresētas norādītajai valstij.</span><span class="sxs-lookup"><span data-stu-id="6272b-156">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="6272b-157">Drukāt pārdošanas pasūtījumā</span><span class="sxs-lookup"><span data-stu-id="6272b-157">Print on sales order</span></span> | <span data-ttu-id="6272b-158">Atzīmējiet šo izvēles rūtiņu, lai drukātu sertifikāta numuru pārdošanas pasūtījumos, kas norādītajā datumu diapazonā ir adresēti norādītajai valstij.</span><span class="sxs-lookup"><span data-stu-id="6272b-158">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |

## <a name="include-the-country-of-origin-on-bom-reports"></a><span data-ttu-id="6272b-159">Izcelsmes valsts/reģiona iekļaušana MK pārskatos</span><span class="sxs-lookup"><span data-stu-id="6272b-159">Include the country of origin on BOM reports</span></span>

<span data-ttu-id="6272b-160">Ģenerējot MK pārskatu, varat iekļaut izcelsmes valsti katrai daļai, kam norādījāt izcelsmes un galamērķa valstis, lapā **Izcelsmes valsts noteikumi**.</span><span class="sxs-lookup"><span data-stu-id="6272b-160">When you generate a BOM report, you can include the country of origin for each part that you specified source and destination countries for on the **Country of origin rules** page.</span></span>

1. <span data-ttu-id="6272b-161">Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="6272b-161">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="6272b-162">Atlasiet vai izveidojiet preci, lai atvērtu tās lapu **Izlaisto preču detalizēta informācija**.</span><span class="sxs-lookup"><span data-stu-id="6272b-162">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="6272b-163">Darbību rūts cilnē **Inženieris**, grupā **MK** atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="6272b-163">On the Action Pane, on the **Engineer** tab, in the **BOM** group, select **Designer**.</span></span>
1. <span data-ttu-id="6272b-164">Parādītās lapas darbību rūtī atlasiet **MK \> Drukāt**.</span><span class="sxs-lookup"><span data-stu-id="6272b-164">On the page that appears, on the Action Pane, select **BOM \> Print**.</span></span>
1. <span data-ttu-id="6272b-165">Dialoglodziņā **Materiālu komplektu rindas** iestatiet lauku **Galamērķa valsts** uz galamērķa valsti, kuru vēlaties skatīt savā pārskatā.</span><span class="sxs-lookup"><span data-stu-id="6272b-165">In **Bill of materials lines** dialog box, set the **Destination country** field to the destination country that you want to view on your report.</span></span>
1. <span data-ttu-id="6272b-166">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="6272b-166">Select **OK**.</span></span>

<span data-ttu-id="6272b-167">Tiek ģenerēts un parādīts pārskats, kas parāda informāciju par katras daļas izcelsmes valsti/reģion.</span><span class="sxs-lookup"><span data-stu-id="6272b-167">A report that shows information about the country of origin of each part is generated and shown.</span></span> <span data-ttu-id="6272b-168">Tālāk ir sniegts pārskata piemērs.</span><span class="sxs-lookup"><span data-stu-id="6272b-168">Here is an example of the report.</span></span>

<span data-ttu-id="6272b-169">![Izcelsmes valsts/reģiona pārskats](media/country-of-origin-report.png "Izcelsmes valsts/reģiona pārskats")</span><span class="sxs-lookup"><span data-stu-id="6272b-169">![Country of origin report](media/country-of-origin-report.png "Country of origin report")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]