---
title: Izcelsmes valsts/reģions
description: Daudzas organizācijas izsniedz sertifikātus saviem kreditoriem, lai nodrošinātu preču atbilstību noteiktiem sertifikācijas standartiem. Šie sertifikāti bieži ir atkarīgi no izcelsmes valsts/reģiona. Šajā tēmā ir sniegta informācija par izcelsmes valsts/reģiona līdzekli, kas ļauj saistīt preci ar tās izcelsmes valsti/reģionu un sekot tās preču sertifikācijai.
author: dasani-madipalli
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: fd234c57bf9893e9b8bcfa5ada7439a642f7a288
ms.sourcegitcommit: 70d0b4e6bdacc15ec75935550ae55fc02cb79624
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/15/2020
ms.locfileid: "3596254"
---
# <a name="country-of-origin"></a><span data-ttu-id="e4772-105">Izcelsmes valsts/reģions</span><span class="sxs-lookup"><span data-stu-id="e4772-105">Country of origin</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e4772-106">Daudzas organizācijas izsniedz sertifikātus saviem kreditoriem, lai nodrošinātu preču atbilstību noteiktiem sertifikācijas standartiem.</span><span class="sxs-lookup"><span data-stu-id="e4772-106">Many organizations issue certificates to their vendors to ensure that products meet specific certification standards.</span></span> <span data-ttu-id="e4772-107">Šie sertifikāti bieži ir atkarīgi no izcelsmes valsts/reģiona.</span><span class="sxs-lookup"><span data-stu-id="e4772-107">These certificates often depend on the country of origin.</span></span> <span data-ttu-id="e4772-108">Izcelsmes valsts/reģiona līdzeklis ļauj saistīt preci ar tās izcelsmes valsti/reģionu un sekot tās preču sertifikācijai.</span><span class="sxs-lookup"><span data-stu-id="e4772-108">The country of origin feature lets you link a product to its country of origin and keep track of its product certifications.</span></span>

## <a name="configure-source-and-destination-countries"></a><span data-ttu-id="e4772-109">Izcelsmes un galamērķa valstu/reģionu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="e4772-109">Configure source and destination countries</span></span>

<span data-ttu-id="e4772-110">Pirms izdot preces sertifikātu, prece ir jāsaista ar tās galamērķa valsti un tās izcelsmes valsti/reģionu.</span><span class="sxs-lookup"><span data-stu-id="e4772-110">Before you issue a certificate for a product, you must link the product to its destination country and its country of origin.</span></span>

1. <span data-ttu-id="e4772-111">Dodieties uz **Preču informācijas pārvaldība \> Iestatīšana \> Preču atbilstība \> Izcelsmes valsts/reģions \> Izcelsmes valsts/reģiona noteikumi**.</span><span class="sxs-lookup"><span data-stu-id="e4772-111">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin rules**.</span></span>
2. <span data-ttu-id="e4772-112">Atlasiet rediģēšanai esošu valsts iestatījumu vai darbību rūtī atlasiet **Jauns**, lai izveidotu jaunu valsts iestatījumu.</span><span class="sxs-lookup"><span data-stu-id="e4772-112">Select an existing country setup to edit, or select **New** on the Action Pane to create a new country setup.</span></span>
3. <span data-ttu-id="e4772-113">Atlasītajai vai jaunajai valstij iestatiet šādas vērtības.</span><span class="sxs-lookup"><span data-stu-id="e4772-113">Set the following values for the selected or new country.</span></span>

    | <span data-ttu-id="e4772-114">Lauks</span><span class="sxs-lookup"><span data-stu-id="e4772-114">Field</span></span> | <span data-ttu-id="e4772-115">apraksts</span><span class="sxs-lookup"><span data-stu-id="e4772-115">Description</span></span> |
    |---|---|
    | <span data-ttu-id="e4772-116">Krājums</span><span class="sxs-lookup"><span data-stu-id="e4772-116">Item number</span></span> | <span data-ttu-id="e4772-117">Atlasiet preces krājuma kodu.</span><span class="sxs-lookup"><span data-stu-id="e4772-117">Select the item number of the product.</span></span> |
    | <span data-ttu-id="e4772-118">Galamērķa valsts</span><span class="sxs-lookup"><span data-stu-id="e4772-118">Destination country</span></span> | <span data-ttu-id="e4772-119">Atlasiet, uz kuru valsti sūtīt preci.</span><span class="sxs-lookup"><span data-stu-id="e4772-119">Select the country that you're sending the product to.</span></span> |
    | <span data-ttu-id="e4772-120">Izcelsmes valsts</span><span class="sxs-lookup"><span data-stu-id="e4772-120">Origin country</span></span> | <span data-ttu-id="e4772-121">Atlasiet, no kuras valsts prece tiek sūtīta.</span><span class="sxs-lookup"><span data-stu-id="e4772-121">Select the country that you're shipping the product from.</span></span> |

<span data-ttu-id="e4772-122">Šī iestatījuma nolūks ir palīdzēt ģenerēt materiālu komplekta (MK) pārskatu, kurā var iekļaut izcelsmes valsti/reģionu katrai daļai, kam ir norādītas izcelsmes un galamērķa valstis.</span><span class="sxs-lookup"><span data-stu-id="e4772-122">The purpose of this setup is to help you generate a bill of materials (BOM) report where you can include the country of origin for each part that source and destination countries are specified for.</span></span> <span data-ttu-id="e4772-123">Šis pārskats palīdzēs iegūt visaptverošu priekšstatu par to, no kurienes daļas ir un uz kurieni tās sūta.</span><span class="sxs-lookup"><span data-stu-id="e4772-123">This report will help you get a holistic picture of where your parts come from and where they are going.</span></span>

## <a name="keep-track-of-vendor-certificates"></a><span data-ttu-id="e4772-124">Kreditora sertifikātu pārraudzīšana</span><span class="sxs-lookup"><span data-stu-id="e4772-124">Keep track of vendor certificates</span></span>

<span data-ttu-id="e4772-125">Varat izmantot lapu **Izcelsmes valsts/reģiona kreditoru sertifikāti**, lai sekotu sertifikātiem, ko izsniedzat kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="e4772-125">You can use the **Country of origin vendor certificates** page to keep track of certificates that you issue to vendors.</span></span>

<span data-ttu-id="e4772-126">Jums ir jāizlemj, kurus sertifikātu dokumentus jūs izsniedzat un kā par tiem paziņosit klientiem.</span><span class="sxs-lookup"><span data-stu-id="e4772-126">You must decide which certificate documents you're issuing and how you will report them to customers.</span></span> <span data-ttu-id="e4772-127">Šis līdzeklis palīdz sekot līdzi jūsu sertifikātiem.</span><span class="sxs-lookup"><span data-stu-id="e4772-127">This feature helps you keep track of your certificates.</span></span> <span data-ttu-id="e4772-128">Tas arī ļauj izvēlēties, vai attiecīgie sertifikātu numuri ir redzami rēķinos, pavadzīmēs un/vai pasūtījumu apstiprinājumos.</span><span class="sxs-lookup"><span data-stu-id="e4772-128">It also lets you choose whether the relevant certificate numbers appear on invoices, packing slips, and/or order confirmations.</span></span>

<span data-ttu-id="e4772-129">Lai iestatītu sertifikāta informāciju, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="e4772-129">To set up your certificate information, follow these steps.</span></span>

1. <span data-ttu-id="e4772-130">Dodieties uz **Preču informācijas pārvaldība \> Iestatīšana \> Preču atbilstība \> Izcelsmes valsts/reģions \> Izcelsmes valsts/reģiona kreditora sertifikāti**.</span><span class="sxs-lookup"><span data-stu-id="e4772-130">Go to **Product information management \> Setup \> Product compliance \> Country of origin \> Country of origin vendor certificates**.</span></span>
2. <span data-ttu-id="e4772-131">Atlasiet rediģēšanai esošu sertifikāta iestatījumu vai darbību rūtī atlasiet **Jauns**, lai izveidotu jaunu sertifikāta iestatījumu.</span><span class="sxs-lookup"><span data-stu-id="e4772-131">Select an existing certificate setup to edit, or select **New** on the Action Pane to create a new certificate setup.</span></span>
3. <span data-ttu-id="e4772-132">Atlasītajam vai jaunajam sertifikātam iestatiet šādus iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="e4772-132">Set the following settings for the selected or new certificate.</span></span>

    | <span data-ttu-id="e4772-133">Lauks</span><span class="sxs-lookup"><span data-stu-id="e4772-133">Field</span></span> | <span data-ttu-id="e4772-134">apraksts</span><span class="sxs-lookup"><span data-stu-id="e4772-134">Description</span></span> |
    |---|---|
    | <span data-ttu-id="e4772-135">Kreditora konts</span><span class="sxs-lookup"><span data-stu-id="e4772-135">Vendor account</span></span> | <span data-ttu-id="e4772-136">Atlasiet kreditoru, kuram sertifikāts izsniegts.</span><span class="sxs-lookup"><span data-stu-id="e4772-136">Select the vendor that you issued the certificate to.</span></span> |
    | <span data-ttu-id="e4772-137">Krājums</span><span class="sxs-lookup"><span data-stu-id="e4772-137">Item number</span></span> | <span data-ttu-id="e4772-138">Atlasiet krājumu, kuram sertifikāts izsniegts.</span><span class="sxs-lookup"><span data-stu-id="e4772-138">Select the item that you issued the certificate for.</span></span> |
    | <span data-ttu-id="e4772-139">Valsts/reģions</span><span class="sxs-lookup"><span data-stu-id="e4772-139">Country/region</span></span> | <span data-ttu-id="e4772-140">Galamērķa valsts vai reģions, kurā jāizmanto šis sertifikāts.</span><span class="sxs-lookup"><span data-stu-id="e4772-140">The destination country or region where you must use this certificate.</span></span> |
    | <span data-ttu-id="e4772-141">Sertifikāta numurs</span><span class="sxs-lookup"><span data-stu-id="e4772-141">Certificate number</span></span> | <span data-ttu-id="e4772-142">Ievadiet izsniegtā sertifikāta identifikācijas numuru.</span><span class="sxs-lookup"><span data-stu-id="e4772-142">Enter the identification number of the certificate that you issued.</span></span> |
    | <span data-ttu-id="e4772-143">Spēkā esošs</span><span class="sxs-lookup"><span data-stu-id="e4772-143">Effective</span></span> | <span data-ttu-id="e4772-144">Atlasiet pirmo datumu, kad pašreizējais sertifikāts ir derīgs.</span><span class="sxs-lookup"><span data-stu-id="e4772-144">Select the first date when the current certificate is valid.</span></span>|
    | <span data-ttu-id="e4772-145">Termiņa beigas</span><span class="sxs-lookup"><span data-stu-id="e4772-145">Expiration</span></span> | <span data-ttu-id="e4772-146">Atlasiet pēdējo datumu, kad pašreizējais sertifikāts ir derīgs.</span><span class="sxs-lookup"><span data-stu-id="e4772-146">Select the last date when the current certificate is valid.</span></span> |
    | <span data-ttu-id="e4772-147">Drukāt rēķinā</span><span class="sxs-lookup"><span data-stu-id="e4772-147">Print on invoice</span></span> | <span data-ttu-id="e4772-148">Atzīmējiet šo izvēles rūtiņu, lai drukātu sertifikāta numuru rēķinos, kas norādītajā datumu diapazonā ir adresēti norādītajai valstij.</span><span class="sxs-lookup"><span data-stu-id="e4772-148">Select this check box to print the certificate number on invoices that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="e4772-149">Drukāt pavadzīmē</span><span class="sxs-lookup"><span data-stu-id="e4772-149">Print on packing slip</span></span> | <span data-ttu-id="e4772-150">Atzīmējiet šo izvēles rūtiņu, lai drukātu sertifikāta numuru pavadzīmēs, kas norādītajā datumu diapazonā ir adresētas norādītajai valstij.</span><span class="sxs-lookup"><span data-stu-id="e4772-150">Select this check box to print the certificate number on packing slips that are addressed to the specified country during the specified date range.</span></span> |
    | <span data-ttu-id="e4772-151">Drukāt pārdošanas pasūtījumā</span><span class="sxs-lookup"><span data-stu-id="e4772-151">Print on sales order</span></span> | <span data-ttu-id="e4772-152">Atzīmējiet šo izvēles rūtiņu, lai drukātu sertifikāta numuru pārdošanas pasūtījumos, kas norādītajā datumu diapazonā ir adresēti norādītajai valstij.</span><span class="sxs-lookup"><span data-stu-id="e4772-152">Select this check box to print the certificate number on sales orders that are addressed to the specified country during the specified date range.</span></span> |

## <a name="include-the-country-of-origin-on-bom-reports"></a><span data-ttu-id="e4772-153">Izcelsmes valsts/reģiona iekļaušana MK pārskatos</span><span class="sxs-lookup"><span data-stu-id="e4772-153">Include the country of origin on BOM reports</span></span>

<span data-ttu-id="e4772-154">Ģenerējot MK pārskatu, varat iekļaut izcelsmes valsti/reģionu katrai daļai, kam norādījāt izcelsmes un galamērķa valstis, lapā **Izcelsmes valsts/reģiona noteikumi**.</span><span class="sxs-lookup"><span data-stu-id="e4772-154">When you generate a BOM report, you can include the country of origin for each part that you specified source and destination countries for on the **Country of origin rules** page.</span></span>

1. <span data-ttu-id="e4772-155">Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="e4772-155">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="e4772-156">Atlasiet vai izveidojiet preci, lai atvērtu tās lapu **Izlaisto preču detalizēta informācija**.</span><span class="sxs-lookup"><span data-stu-id="e4772-156">Select or create a product to open its **Released product details** page.</span></span>
1. <span data-ttu-id="e4772-157">Darbību rūts cilnē **Inženieris**, grupā **MK** atlasiet **Noformētājs**.</span><span class="sxs-lookup"><span data-stu-id="e4772-157">On the Action Pane, on the **Engineer** tab, in the **BOM** group, select **Designer**.</span></span>
1. <span data-ttu-id="e4772-158">Parādītās lapas darbību rūtī atlasiet **MK \> Drukāt**.</span><span class="sxs-lookup"><span data-stu-id="e4772-158">On the page that appears, on the Action Pane, select **BOM \> Print**.</span></span>
1. <span data-ttu-id="e4772-159">Dialoglodziņā **Materiālu komplektu rindas** iestatiet lauku **Galamērķa valsts** uz galamērķa valsti, kuru vēlaties skatīt savā pārskatā.</span><span class="sxs-lookup"><span data-stu-id="e4772-159">In **Bill of materials lines** dialog box, set the **Destination country** field to the destination country that you want to view on your report.</span></span>
1. <span data-ttu-id="e4772-160">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e4772-160">Select **OK**.</span></span>

<span data-ttu-id="e4772-161">Tiek ģenerēts un parādīts pārskats, kas parāda informāciju par katras daļas izcelsmes valsti/reģion.</span><span class="sxs-lookup"><span data-stu-id="e4772-161">A report that shows information about the country of origin of each part is generated and shown.</span></span> <span data-ttu-id="e4772-162">Tālāk ir sniegts pārskata piemērs.</span><span class="sxs-lookup"><span data-stu-id="e4772-162">Here is an example of the report.</span></span>

<span data-ttu-id="e4772-163">![Izcelsmes valsts/reģiona pārskats](media/country-of-origin-report.png "Izcelsmes valsts/reģiona pārskats")</span><span class="sxs-lookup"><span data-stu-id="e4772-163">![Country of origin report](media/country-of-origin-report.png "Country of origin report")</span></span>
