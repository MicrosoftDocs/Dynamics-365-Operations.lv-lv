---
title: Nodokļu aprēķins (priekšskatījums)
description: Šajā tēmā ir izskaidrots nodokļu aprēķina iespēju vispārējais tvērums un iezīmes.
author: wangchen
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: b26472e195d9bdbba340a118c106de1a4dc79b34
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021936"
---
# <a name="tax-calculation-preview"></a><span data-ttu-id="fb65a-103">Nodokļu aprēķins (priekšskatījums)</span><span class="sxs-lookup"><span data-stu-id="fb65a-103">Tax Calculation (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="fb65a-104">Nodokļu aprēķins ir hipermērogojams daudznomnieku pakalpojums, kas ļauj Global Tax Engine automatizēt un vienkāršot nodokļu noteikšanas un aprēķināšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="fb65a-104">Tax Calculation is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="fb65a-105">Nodokļu programma ir pilnībā konfigurējama.</span><span class="sxs-lookup"><span data-stu-id="fb65a-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="fb65a-106">Elementi, kurus var konfigurēt, ietver, bet ne tikai, apliekamo datu modeli, nodokļu kodu, nodokļu piemērošanas matricu un nodokļu aprēķina formulu.</span><span class="sxs-lookup"><span data-stu-id="fb65a-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="fb65a-107">Nodokļu programma darbojas pamata pakalpojumu platformā un piedāvā modernu tehnoloģiju un Microsoft Azure eksponenciālu mērogošanu.</span><span class="sxs-lookup"><span data-stu-id="fb65a-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="fb65a-108">Nodokļu aprēķins ir integrēts ar Dynamics 365 Finance un Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="fb65a-108">Tax Calculation integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="fb65a-109">Visbeidzot tas integrēs arī ar Dynamics 365 Project Operations, Dynamics 365 Commerce un citām pirmās puses un trešās puses programmām.</span><span class="sxs-lookup"><span data-stu-id="fb65a-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

<span data-ttu-id="fb65a-110">Nodokļu aprēķins ir uz mikroservisu balstīta nodokļu programma, kas piedāvā eksponenciālu mērogošanu.</span><span class="sxs-lookup"><span data-stu-id="fb65a-110">Tax Calculation is a microservice-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="fb65a-111">Tas var palīdzēt veikt šādus uzdevumus:</span><span class="sxs-lookup"><span data-stu-id="fb65a-111">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="fb65a-112">Konfigurējiet nodokļu aprēķinu, izmantojot Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="fb65a-112">Configure Tax Calculation through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="fb65a-113">RCS ir uzlabota elektronisko pārskatu (Electronic reporting - ER) veidotāja versija un ir pieejama kā savrups pakalpojums.</span><span class="sxs-lookup"><span data-stu-id="fb65a-113">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="fb65a-114">Konfigurējiet nodokļu matricu, lai automātiski noteiktu nodokļu kodus un likmes.</span><span class="sxs-lookup"><span data-stu-id="fb65a-114">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="fb65a-115">Konfigurējiet nodokļu matricu, lai automātiski noteiktu nodokļu reģistrācijas numuru.</span><span class="sxs-lookup"><span data-stu-id="fb65a-115">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="fb65a-116">Konfigurējiet nodokļu aprēķina veidotāju, lai definētu formulas un nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="fb65a-116">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="fb65a-117">Kopīgojiet nodokļu noteikšanas un aprēķināšanas risinājumu visām juridiskajām personām.</span><span class="sxs-lookup"><span data-stu-id="fb65a-117">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="fb65a-118">Lai izmantotu nodokļu aprēķināšanas pakalpojumu, instalējiet nodokļu aprēķina pakalpojuma pievienojumprogrammu savam projektam pakalpojumā Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="fb65a-118">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="fb65a-119">Pēc tam pabeidziet iestatīšanu RCS un iespējojiet nodokļu aprēķināšanas pakalpojumu Finance un Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="fb65a-119">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="fb65a-120">Papildinformāciju skatiet sadaļā [Sākt darbu ar nodokļu pakalpojumu](./global-get-started-with-tax-calculation-service.md).</span><span class="sxs-lookup"><span data-stu-id="fb65a-120">For more information, see [Get started with tax service](./global-get-started-with-tax-calculation-service.md).</span></span>

## <a name="availability"></a><span data-ttu-id="fb65a-121">Pieejamība</span><span class="sxs-lookup"><span data-stu-id="fb65a-121">Availability</span></span>

<span data-ttu-id="fb65a-122">Nodokļu aprēķins ir pieejams tikai smilškastes vidē un izvēlētajiem debitoriem, izmantojot publisku priekšskatījuma programmu.</span><span class="sxs-lookup"><span data-stu-id="fb65a-122">Tax Calculation is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="fb65a-123">Visbeidzot, tas kļūs plaši pieejams visiem debitoriem un ražošanas vidēs.</span><span class="sxs-lookup"><span data-stu-id="fb65a-123">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="fb65a-124">Arī turpmāk tiks piegādāti jauni līdzekļi, tāpēc noteikti iepazīstieties ar visjaunāko dokumentāciju, lai uzzinātu par atbalstīto funkciju segumu un darbības jomu.</span><span class="sxs-lookup"><span data-stu-id="fb65a-124">New features will continue to be delivered, so be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="fb65a-125">Nodokļu aprēķins ir izvietots tālāk redzamajās Azure ģeogrāfiskās lapās.</span><span class="sxs-lookup"><span data-stu-id="fb65a-125">Tax Calculation is deployed in the following Azure geographies.</span></span> <span data-ttu-id="fb65a-126">Tas tiks izvietots arī vairākās Azure ģeogrāfiskās vietās atbilstoši debitoru vajadzībām:</span><span class="sxs-lookup"><span data-stu-id="fb65a-126">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="fb65a-127">ASV</span><span class="sxs-lookup"><span data-stu-id="fb65a-127">United States</span></span>
- <span data-ttu-id="fb65a-128">Eiropa</span><span class="sxs-lookup"><span data-stu-id="fb65a-128">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="fb65a-129">Nodokļu aprēķins neatbalsta Dynamics 365 lokālas izvietošanas.</span><span class="sxs-lookup"><span data-stu-id="fb65a-129">Tax Calculation doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="fb65a-130">Tas neatbalsta arī agrākas versijas, piemēram, Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="fb65a-130">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="fb65a-131">Līdzekļu iezīmēšana</span><span class="sxs-lookup"><span data-stu-id="fb65a-131">Feature highlights</span></span>

- <span data-ttu-id="fb65a-132">Konfigurējama nodokļu matrica, lai automātiski noteiktu un aprēķinātu nodokli</span><span class="sxs-lookup"><span data-stu-id="fb65a-132">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="fb65a-133">Atbalstīt vairākus nodokļa reģistrācijas numurus</span><span class="sxs-lookup"><span data-stu-id="fb65a-133">Support for multiple tax registration numbers</span></span>
- <span data-ttu-id="fb65a-134">Pārsūtīšanas pasūtījuma atbalsts nodokļu noteikšanai un aprēķinam</span><span class="sxs-lookup"><span data-stu-id="fb65a-134">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="fb65a-135">Pārsūtīšanas pasūtījuma atbalsts vairāku nodokļa reģistrācijas numuru noteikšanai</span><span class="sxs-lookup"><span data-stu-id="fb65a-135">Transfer order support for determination of multiple tax registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="fb65a-136">Atbalstītie darījumi</span><span class="sxs-lookup"><span data-stu-id="fb65a-136">Supported transactions</span></span>

<span data-ttu-id="fb65a-137">Nodokļu aprēķinu var iespējot juridiska persona un darījums.</span><span class="sxs-lookup"><span data-stu-id="fb65a-137">Tax Calculation can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="fb65a-138">Tālāk ir norādīti atbalstītie darījumi.</span><span class="sxs-lookup"><span data-stu-id="fb65a-138">The following transactions are supported:</span></span>

- <span data-ttu-id="fb65a-139">Pārdošanas process</span><span class="sxs-lookup"><span data-stu-id="fb65a-139">Sales process</span></span>

    - <span data-ttu-id="fb65a-140">Pārdošanas piedāvājums</span><span class="sxs-lookup"><span data-stu-id="fb65a-140">Sales quotation</span></span>
    - <span data-ttu-id="fb65a-141">Pārdošanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="fb65a-141">Sales order</span></span>
    - <span data-ttu-id="fb65a-142">Apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="fb65a-142">Confirmation</span></span>
    - <span data-ttu-id="fb65a-143">Izdošanas saraksts</span><span class="sxs-lookup"><span data-stu-id="fb65a-143">Picking list</span></span>
    - <span data-ttu-id="fb65a-144">Pavadzīme</span><span class="sxs-lookup"><span data-stu-id="fb65a-144">Packing slip</span></span>
    - <span data-ttu-id="fb65a-145">Pārdošanas rēķins</span><span class="sxs-lookup"><span data-stu-id="fb65a-145">Sales invoice</span></span>
    - <span data-ttu-id="fb65a-146">Kredīta piezīme</span><span class="sxs-lookup"><span data-stu-id="fb65a-146">Credit note</span></span>
    - <span data-ttu-id="fb65a-147">Atgriešanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="fb65a-147">Return order</span></span>
    - <span data-ttu-id="fb65a-148">Virsraksta papildmaksa</span><span class="sxs-lookup"><span data-stu-id="fb65a-148">Header miscellaneous charge</span></span>
    - <span data-ttu-id="fb65a-149">Rindas papildmaksas pieprasījums</span><span class="sxs-lookup"><span data-stu-id="fb65a-149">Line miscellaneous charge</span></span>

- <span data-ttu-id="fb65a-150">Pirkšanas process</span><span class="sxs-lookup"><span data-stu-id="fb65a-150">Purchase process</span></span>

    - <span data-ttu-id="fb65a-151">Pirkuma pasūtījums</span><span class="sxs-lookup"><span data-stu-id="fb65a-151">Purchase order</span></span>
    - <span data-ttu-id="fb65a-152">Apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="fb65a-152">Confirmation</span></span>
    - <span data-ttu-id="fb65a-153">Saņemšanas saraksts</span><span class="sxs-lookup"><span data-stu-id="fb65a-153">Receipts list</span></span>
    - <span data-ttu-id="fb65a-154">Produktu ieejas plūsma</span><span class="sxs-lookup"><span data-stu-id="fb65a-154">Product receipt</span></span>
    - <span data-ttu-id="fb65a-155">Pirkšanas rēķins</span><span class="sxs-lookup"><span data-stu-id="fb65a-155">Purchase invoice</span></span>
    - <span data-ttu-id="fb65a-156">Virsraksta papildmaksas pieprasījums</span><span class="sxs-lookup"><span data-stu-id="fb65a-156">Header miscellaneous charge</span></span>
    - <span data-ttu-id="fb65a-157">Rindas papildmaksas pieprasījums</span><span class="sxs-lookup"><span data-stu-id="fb65a-157">Line miscellaneous charge</span></span>
    - <span data-ttu-id="fb65a-158">Kredīta piezīme</span><span class="sxs-lookup"><span data-stu-id="fb65a-158">Credit note</span></span>
    - <span data-ttu-id="fb65a-159">Atgriešanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="fb65a-159">Return order</span></span>
    - <span data-ttu-id="fb65a-160">Pirkšanas pieprasījums</span><span class="sxs-lookup"><span data-stu-id="fb65a-160">Purchase requisition</span></span>
    - <span data-ttu-id="fb65a-161">Pirkšanas pieprasījuma rindas papildmaksas pieprasījums</span><span class="sxs-lookup"><span data-stu-id="fb65a-161">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="fb65a-162">Piedāvājuma pieprasījums</span><span class="sxs-lookup"><span data-stu-id="fb65a-162">Request for quotation</span></span>
    - <span data-ttu-id="fb65a-163">Piedāvājuma pieprasījuma virsraksta papildmaksas pieprasījums</span><span class="sxs-lookup"><span data-stu-id="fb65a-163">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="fb65a-164">Piedāvājuma pieprasījuma rindas papildmaksas pieprasījums</span><span class="sxs-lookup"><span data-stu-id="fb65a-164">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="fb65a-165">Krājumu process</span><span class="sxs-lookup"><span data-stu-id="fb65a-165">Inventory process</span></span>

    - <span data-ttu-id="fb65a-166">Pārvietošanas pasūtījums – nosūtīšana</span><span class="sxs-lookup"><span data-stu-id="fb65a-166">Transfer order – ship</span></span>
    - <span data-ttu-id="fb65a-167">Pārsūtīšanas pasūtījums – saņemšana</span><span class="sxs-lookup"><span data-stu-id="fb65a-167">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="fb65a-168">Saistītie resursi</span><span class="sxs-lookup"><span data-stu-id="fb65a-168">Related resources</span></span>

[<span data-ttu-id="fb65a-169">Darba sākšana ar nodokļu pakalpojumu</span><span class="sxs-lookup"><span data-stu-id="fb65a-169">Get started with tax service</span></span>](./global-get-started-with-tax-calculation-service.md)

[<span data-ttu-id="fb65a-170">Vairāki PVN reģistrācijas numuri</span><span class="sxs-lookup"><span data-stu-id="fb65a-170">Multiple VAT registration number</span></span>](./emea-multiple-vat-registration-numbers.md)

[<span data-ttu-id="fb65a-171">Nodokļu līdzekļu atbalsts pārsūtīšanas pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="fb65a-171">Tax feature support for transfer order</span></span>](./tasks/tax-feature-support-for-transfer-order.md)

[<span data-ttu-id="fb65a-172">Kā veidot paplašinājumu nodokļu pakalpojumā</span><span class="sxs-lookup"><span data-stu-id="fb65a-172">How to build extension in tax service</span></span>](./tax-service-add-data-fields-tax-integration-by-extension.md)