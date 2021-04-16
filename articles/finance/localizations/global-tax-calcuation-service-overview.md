---
title: Nodokļu aprēķināšanas pakalpojums (Priekšskatījums)
description: Šajā tēmā ir izskaidrots nodokļu aprēķināšanas pakalpojuma vispārējais tvērums un iezīmes.
author: wangchen
ms.date: 03/02/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 518d3fda7b97e55d23beea6a1ba0e50b44a7aa0e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818228"
---
# <a name="tax-calculation-service-preview"></a><span data-ttu-id="478c9-103">Nodokļu aprēķināšanas pakalpojums (Priekšskatījums)</span><span class="sxs-lookup"><span data-stu-id="478c9-103">Tax calculation service (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="478c9-104">Nodokļu aprēķināšanas pakalpojums ir hipermērogojams daudznomnieku pakalpojums, kas ļauj Global Tax Engine automatizēt un vienkāršot nodokļu noteikšanas un aprēķināšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="478c9-104">The tax calculation service is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="478c9-105">Nodokļu programma ir pilnībā konfigurējama.</span><span class="sxs-lookup"><span data-stu-id="478c9-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="478c9-106">Elementi, kurus var konfigurēt, ietver, bet ne tikai, apliekamo datu modeli, nodokļu kodu, nodokļu piemērošanas matricu un nodokļu aprēķina formulu.</span><span class="sxs-lookup"><span data-stu-id="478c9-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="478c9-107">Nodokļu programma darbojas pamata pakalpojumu platformā un piedāvā modernu tehnoloģiju un Microsoft Azure eksponenciālu mērogošanu.</span><span class="sxs-lookup"><span data-stu-id="478c9-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="478c9-108">Nodokļu aprēķināšanas pakalpojums ir integrēts ar Dynamics 365 Finance un Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="478c9-108">The tax calculation service integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="478c9-109">Visbeidzot tas integrēs arī ar Dynamics 365 Project Operations, Dynamics 365 Commerce un citām pirmās puses un trešās puses programmām.</span><span class="sxs-lookup"><span data-stu-id="478c9-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

<span data-ttu-id="478c9-110">Nodokļu aprēķināšanas pakalpojums ir Microsoft nodokļu programma, kas piedāvā eksponenciālu mērogošanu.</span><span class="sxs-lookup"><span data-stu-id="478c9-110">The tax calculation service is a Microsoft-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="478c9-111">Tas var palīdzēt veikt šādus uzdevumus:</span><span class="sxs-lookup"><span data-stu-id="478c9-111">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="478c9-112">Konfigurējiet nodokļu aprēķina pakalpojumu, izmantojot Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="478c9-112">Configure the tax calculation service through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="478c9-113">RCS ir uzlabota elektronisko pārskatu (Electronic reporting - ER) veidotāja versija un ir pieejama kā savrups pakalpojums.</span><span class="sxs-lookup"><span data-stu-id="478c9-113">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="478c9-114">Konfigurējiet nodokļu matricu, lai automātiski noteiktu nodokļu kodus un likmes.</span><span class="sxs-lookup"><span data-stu-id="478c9-114">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="478c9-115">Konfigurējiet nodokļu matricu, lai automātiski noteiktu nodokļu reģistrācijas numuru.</span><span class="sxs-lookup"><span data-stu-id="478c9-115">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="478c9-116">Konfigurējiet nodokļu aprēķina veidotāju, lai definētu formulas un nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="478c9-116">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="478c9-117">Kopīgojiet nodokļu noteikšanas un aprēķināšanas risinājumu visām juridiskajām personām.</span><span class="sxs-lookup"><span data-stu-id="478c9-117">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="478c9-118">Lai izmantotu nodokļu aprēķināšanas pakalpojumu, instalējiet nodokļu aprēķina pakalpojuma pievienojumprogrammu savam projektam pakalpojumā Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="478c9-118">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="478c9-119">Pēc tam pabeidziet iestatīšanu RCS un iespējojiet nodokļu aprēķināšanas pakalpojumu Finance un Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="478c9-119">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="478c9-120">Papildinformāciju skatiet sadaļā [Sākt darbu ar nodokļu pakalpojumu](https://go.microsoft.com/fwlink/?linkid=2138482).</span><span class="sxs-lookup"><span data-stu-id="478c9-120">For more information, see [Get started with tax service](https://go.microsoft.com/fwlink/?linkid=2138482).</span></span>

## <a name="availability"></a><span data-ttu-id="478c9-121">Pieejamība</span><span class="sxs-lookup"><span data-stu-id="478c9-121">Availability</span></span>

<span data-ttu-id="478c9-122">Nodokļu aprēķināšanas pakalpojums ir pieejams tikai smilškastes vidē un izvēlētajiem debitoriem, izmantojot publisku priekšskatījuma programmu.</span><span class="sxs-lookup"><span data-stu-id="478c9-122">The tax calculation service is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="478c9-123">Visbeidzot, tas kļūs plaši pieejams visiem debitoriem un ražošanas vidēs.</span><span class="sxs-lookup"><span data-stu-id="478c9-123">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="478c9-124">Jaunie līdzekļi tiks piegādāti nodokļu aprēķināšanas pakalpojumā.</span><span class="sxs-lookup"><span data-stu-id="478c9-124">New features will continue to be delivered in the tax calculation service.</span></span> <span data-ttu-id="478c9-125">Tāpēc noteikti iepazīstieties ar visjaunāko dokumentāciju, lai uzzinātu par atbalstīto funkciju segumu un darbības jomu.</span><span class="sxs-lookup"><span data-stu-id="478c9-125">Therefore, be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="478c9-126">Nodokļu aprēķināšanas pakalpojums ir izvietots tālāk redzamajās Azure ģeogrāfiskās lapās.</span><span class="sxs-lookup"><span data-stu-id="478c9-126">The tax calculation service is deployed in the following Azure geographies.</span></span> <span data-ttu-id="478c9-127">Tas tiks izvietots arī vairākās Azure ģeogrāfiskās vietās atbilstoši debitoru vajadzībām:</span><span class="sxs-lookup"><span data-stu-id="478c9-127">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="478c9-128">ASV</span><span class="sxs-lookup"><span data-stu-id="478c9-128">United States</span></span>
- <span data-ttu-id="478c9-129">Eiropa</span><span class="sxs-lookup"><span data-stu-id="478c9-129">Europe</span></span>
- <span data-ttu-id="478c9-130">Francija</span><span class="sxs-lookup"><span data-stu-id="478c9-130">France</span></span>
- <span data-ttu-id="478c9-131">Apvienotā Karaliste</span><span class="sxs-lookup"><span data-stu-id="478c9-131">United Kingdom</span></span>

> [!NOTE]
> <span data-ttu-id="478c9-132">Nodokļu aprēķināšanas pakalpojums neatbalsta Dynamics 365 lokālas izvietošanas.</span><span class="sxs-lookup"><span data-stu-id="478c9-132">The tax calculation service doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="478c9-133">Tas neatbalsta arī agrākas versijas, piemēram, Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="478c9-133">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="478c9-134">Līdzekļu iezīmēšana</span><span class="sxs-lookup"><span data-stu-id="478c9-134">Feature highlights</span></span>

- <span data-ttu-id="478c9-135">Konfigurējama nodokļu matrica, lai automātiski noteiktu un aprēķinātu nodokli</span><span class="sxs-lookup"><span data-stu-id="478c9-135">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="478c9-136">Atbalstīt vairākus pievienotās vērtības nodokļa (PVN) reģistrācijas numurus</span><span class="sxs-lookup"><span data-stu-id="478c9-136">Support for multiple value-added tax (VAT) registration numbers</span></span>
- <span data-ttu-id="478c9-137">Pārsūtīšanas pasūtījuma atbalsts nodokļu noteikšanai un aprēķinam</span><span class="sxs-lookup"><span data-stu-id="478c9-137">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="478c9-138">Pārsūtīšanas pasūtījuma atbalsts vairāku PVN reģistrācijas numuru noteikšanai</span><span class="sxs-lookup"><span data-stu-id="478c9-138">Transfer order support for determination of multiple VAT registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="478c9-139">Atbalstītie darījumi</span><span class="sxs-lookup"><span data-stu-id="478c9-139">Supported transactions</span></span>

<span data-ttu-id="478c9-140">Nodokļu aprēķināšanas pakalpojumu var iespējot juridiska persona un darījums.</span><span class="sxs-lookup"><span data-stu-id="478c9-140">The tax calculation service can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="478c9-141">Tālāk ir norādīti atbalstītie darījumi.</span><span class="sxs-lookup"><span data-stu-id="478c9-141">The following transactions are supported:</span></span>

- <span data-ttu-id="478c9-142">Pārdošanas process</span><span class="sxs-lookup"><span data-stu-id="478c9-142">Sales process</span></span>

    - <span data-ttu-id="478c9-143">Pārdošanas piedāvājums</span><span class="sxs-lookup"><span data-stu-id="478c9-143">Sales quotation</span></span>
    - <span data-ttu-id="478c9-144">Pārdošanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="478c9-144">Sales order</span></span>
    - <span data-ttu-id="478c9-145">Apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="478c9-145">Confirmation</span></span>
    - <span data-ttu-id="478c9-146">Izdošanas saraksts</span><span class="sxs-lookup"><span data-stu-id="478c9-146">Picking list</span></span>
    - <span data-ttu-id="478c9-147">Pavadzīme</span><span class="sxs-lookup"><span data-stu-id="478c9-147">Packing slip</span></span>
    - <span data-ttu-id="478c9-148">Pārdošanas rēķins</span><span class="sxs-lookup"><span data-stu-id="478c9-148">Sales invoice</span></span>
    - <span data-ttu-id="478c9-149">Kredīta piezīme</span><span class="sxs-lookup"><span data-stu-id="478c9-149">Credit note</span></span>
    - <span data-ttu-id="478c9-150">Atgriešanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="478c9-150">Return order</span></span>
    - <span data-ttu-id="478c9-151">Virsraksta papildmaksa</span><span class="sxs-lookup"><span data-stu-id="478c9-151">Header miscellaneous charge</span></span>
    - <span data-ttu-id="478c9-152">Rindas papildmaksas pieprasījums</span><span class="sxs-lookup"><span data-stu-id="478c9-152">Line miscellaneous charge</span></span>

- <span data-ttu-id="478c9-153">Pirkšanas process</span><span class="sxs-lookup"><span data-stu-id="478c9-153">Purchase process</span></span>

    - <span data-ttu-id="478c9-154">Pirkuma pasūtījums</span><span class="sxs-lookup"><span data-stu-id="478c9-154">Purchase order</span></span>
    - <span data-ttu-id="478c9-155">Apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="478c9-155">Confirmation</span></span>
    - <span data-ttu-id="478c9-156">Saņemšanas saraksts</span><span class="sxs-lookup"><span data-stu-id="478c9-156">Receipts list</span></span>
    - <span data-ttu-id="478c9-157">Produktu ieejas plūsma</span><span class="sxs-lookup"><span data-stu-id="478c9-157">Product receipt</span></span>
    - <span data-ttu-id="478c9-158">Pirkšanas rēķins</span><span class="sxs-lookup"><span data-stu-id="478c9-158">Purchase invoice</span></span>
    - <span data-ttu-id="478c9-159">Virsraksta papildmaksas pieprasījums</span><span class="sxs-lookup"><span data-stu-id="478c9-159">Header miscellaneous charge</span></span>
    - <span data-ttu-id="478c9-160">Rindas papildmaksas pieprasījums</span><span class="sxs-lookup"><span data-stu-id="478c9-160">Line miscellaneous charge</span></span>
    - <span data-ttu-id="478c9-161">Kredīta piezīme</span><span class="sxs-lookup"><span data-stu-id="478c9-161">Credit note</span></span>
    - <span data-ttu-id="478c9-162">Atgriešanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="478c9-162">Return order</span></span>
    - <span data-ttu-id="478c9-163">Pirkšanas pieprasījums</span><span class="sxs-lookup"><span data-stu-id="478c9-163">Purchase requisition</span></span>
    - <span data-ttu-id="478c9-164">Pirkšanas pieprasījuma rindas papildmaksas pieprasījums</span><span class="sxs-lookup"><span data-stu-id="478c9-164">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="478c9-165">Piedāvājuma pieprasījums</span><span class="sxs-lookup"><span data-stu-id="478c9-165">Request for quotation</span></span>
    - <span data-ttu-id="478c9-166">Piedāvājuma pieprasījuma virsraksta papildmaksas pieprasījums</span><span class="sxs-lookup"><span data-stu-id="478c9-166">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="478c9-167">Piedāvājuma pieprasījuma rindas papildmaksas pieprasījums</span><span class="sxs-lookup"><span data-stu-id="478c9-167">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="478c9-168">Krājumu process</span><span class="sxs-lookup"><span data-stu-id="478c9-168">Inventory process</span></span>

    - <span data-ttu-id="478c9-169">Pārvietošanas pasūtījums – nosūtīšana</span><span class="sxs-lookup"><span data-stu-id="478c9-169">Transfer order – ship</span></span>
    - <span data-ttu-id="478c9-170">Pārsūtīšanas pasūtījums – saņemšana</span><span class="sxs-lookup"><span data-stu-id="478c9-170">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="478c9-171">Saistītie resursi</span><span class="sxs-lookup"><span data-stu-id="478c9-171">Related resources</span></span>

[<span data-ttu-id="478c9-172">Darba sākšana ar nodokļu pakalpojumu</span><span class="sxs-lookup"><span data-stu-id="478c9-172">Get started with tax service</span></span>](https://go.microsoft.com/fwlink/?linkid=2138482)

[<span data-ttu-id="478c9-173">Vairāki PVN reģistrācijas numuri</span><span class="sxs-lookup"><span data-stu-id="478c9-173">Multiple VAT registration number</span></span>](https://go.microsoft.com/fwlink/?linkid=2153387)

[<span data-ttu-id="478c9-174">Nodokļu līdzekļu atbalsts pārsūtīšanas pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="478c9-174">Tax feature support for transfer order</span></span>](https://go.microsoft.com/fwlink/?linkid=2153388)

[<span data-ttu-id="478c9-175">Kā veidot paplašinājumu nodokļu pakalpojumā</span><span class="sxs-lookup"><span data-stu-id="478c9-175">How to build extension in tax service</span></span>](https://go.microsoft.com/fwlink/?linkid=2138483)
