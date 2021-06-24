---
title: Nodokļu aprēķins (priekšskatījums)
description: Šajā tēmā ir izskaidrots nodokļu aprēķina iespēju vispārējais tvērums un iezīmes.
author: wangchen
ms.date: 06/03/2021
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
ms.openlocfilehash: 9daa6e001200d03a2639974fb6de618d77ddf09d
ms.sourcegitcommit: cb282e8d2306ab71adf80a84346a6863d2d019e8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2021
ms.locfileid: "6184105"
---
# <a name="tax-calculation-preview"></a><span data-ttu-id="fe7e3-103">Nodokļu aprēķins (priekšskatījums)</span><span class="sxs-lookup"><span data-stu-id="fe7e3-103">Tax Calculation (Preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="fe7e3-104">Nodokļu aprēķins ir hipermērogojams daudznomnieku pakalpojums, kas ļauj Global Tax Engine automatizēt un vienkāršot nodokļu noteikšanas un aprēķināšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="fe7e3-104">Tax Calculation is a hyper-scalable multitenant service that enables the global tax engine to automate and simplify the tax determination and calculation process.</span></span> <span data-ttu-id="fe7e3-105">Nodokļu programma ir pilnībā konfigurējama.</span><span class="sxs-lookup"><span data-stu-id="fe7e3-105">The tax engine is fully configurable.</span></span> <span data-ttu-id="fe7e3-106">Elementi, kurus var konfigurēt, ietver, bet ne tikai, apliekamo datu modeli, nodokļu kodu, nodokļu piemērošanas matricu un nodokļu aprēķina formulu.</span><span class="sxs-lookup"><span data-stu-id="fe7e3-106">The elements that can be configured include, but aren't limited to, the taxable data model, tax code, tax applicability matrix, and tax calculation formula.</span></span> <span data-ttu-id="fe7e3-107">Nodokļu programma darbojas pamata pakalpojumu platformā un piedāvā modernu tehnoloģiju un Microsoft Azure eksponenciālu mērogošanu.</span><span class="sxs-lookup"><span data-stu-id="fe7e3-107">The tax engine runs on the Microsoft Azure core services platform, and offers modern technology and exponential scalability.</span></span>

<span data-ttu-id="fe7e3-108">Nodokļu aprēķins ir integrēts ar Dynamics 365 Finance un Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="fe7e3-108">Tax Calculation integrates with Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="fe7e3-109">Visbeidzot tas integrēs arī ar Dynamics 365 Project Operations, Dynamics 365 Commerce un citām pirmās puses un trešās puses programmām.</span><span class="sxs-lookup"><span data-stu-id="fe7e3-109">Eventually, it will also integrate with Dynamics 365 Project Operations, Dynamics 365 Commerce, and other first-party and third-party applications.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fe7e3-110">Kad iespējojat nodokļu aprēķināšanas pakalpojumu, atsevišķas operācijas ar saistītajiem datiem var tikt veiktas datu centrā, kurš neuztur jūsu pakalpojuma datus.</span><span class="sxs-lookup"><span data-stu-id="fe7e3-110">When you enable the Tax Calculation service, some operations on related data might be performed in a data center other than the data center that maintains your service data.</span></span> <span data-ttu-id="fe7e3-111">Pirms iespējojat nodokļu aprēķināšanas pakalpojumu, parskatiet [Noteikumus un nosacījumus](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).</span><span class="sxs-lookup"><span data-stu-id="fe7e3-111">Review the [Terms and Conditions](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md) before you enable the Tax Calculation service.</span></span> <span data-ttu-id="fe7e3-112">Mums ir svarīga jūsu konfidencialitāte.</span><span class="sxs-lookup"><span data-stu-id="fe7e3-112">Your privacy is important to us.</span></span> <span data-ttu-id="fe7e3-113">Lai uzzinātu vairāk, izlasiet mūsu [Paziņojumu par konfidencialitāti](https://go.microsoft.com/fwlink/?LinkId=521839).</span><span class="sxs-lookup"><span data-stu-id="fe7e3-113">To learn more, read our [Privacy Statement](https://go.microsoft.com/fwlink/?LinkId=521839).</span></span>

<span data-ttu-id="fe7e3-114">Nodokļu aprēķins ir uz mikroservisu balstīta nodokļu programma, kas piedāvā eksponenciālu mērogošanu.</span><span class="sxs-lookup"><span data-stu-id="fe7e3-114">Tax Calculation is a microservice-based tax engine that offers exponential scalability.</span></span> <span data-ttu-id="fe7e3-115">Tas var palīdzēt veikt šādus uzdevumus:</span><span class="sxs-lookup"><span data-stu-id="fe7e3-115">It can help you perform the following tasks:</span></span>

- <span data-ttu-id="fe7e3-116">Konfigurējiet nodokļu aprēķinu, izmantojot Regulatory Configuration Service (RCS).</span><span class="sxs-lookup"><span data-stu-id="fe7e3-116">Configure Tax Calculation through Regulatory Configuration Service (RCS).</span></span> <span data-ttu-id="fe7e3-117">RCS ir uzlabota elektronisko pārskatu (Electronic reporting - ER) veidotāja versija un ir pieejama kā savrups pakalpojums.</span><span class="sxs-lookup"><span data-stu-id="fe7e3-117">RCS is an enhanced version of the Electronic reporting (ER) designer and is available as a standalone service.</span></span>
- <span data-ttu-id="fe7e3-118">Konfigurējiet nodokļu matricu, lai automātiski noteiktu nodokļu kodus un likmes.</span><span class="sxs-lookup"><span data-stu-id="fe7e3-118">Configure the tax matrix to automatically determine tax codes and rates.</span></span>
- <span data-ttu-id="fe7e3-119">Konfigurējiet nodokļu matricu, lai automātiski noteiktu nodokļu reģistrācijas numuru.</span><span class="sxs-lookup"><span data-stu-id="fe7e3-119">Configure the tax matrix to automatically determine the tax registration number.</span></span>
- <span data-ttu-id="fe7e3-120">Konfigurējiet nodokļu aprēķina veidotāju, lai definētu formulas un nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="fe7e3-120">Configure the tax calculation designer to define formulas and conditions.</span></span>
- <span data-ttu-id="fe7e3-121">Kopīgojiet nodokļu noteikšanas un aprēķināšanas risinājumu visām juridiskajām personām.</span><span class="sxs-lookup"><span data-stu-id="fe7e3-121">Share the tax determination and calculation solution across legal entities.</span></span>

<span data-ttu-id="fe7e3-122">Lai izmantotu nodokļu aprēķināšanas pakalpojumu, instalējiet nodokļu aprēķina pakalpojuma pievienojumprogrammu savam projektam pakalpojumā Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="fe7e3-122">To use the tax calculation service, install the tax calculation service add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="fe7e3-123">Pēc tam pabeidziet iestatīšanu RCS un iespējojiet nodokļu aprēķināšanas pakalpojumu Finance un Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="fe7e3-123">Then complete the setup in RCS, and enable the tax calculation service in Finance and Supply Chain Management.</span></span> <span data-ttu-id="fe7e3-124">Papildinformāciju skatiet sadaļā [Sākt darbu ar nodokļu pakalpojumu](./global-get-started-with-tax-calculation-service.md).</span><span class="sxs-lookup"><span data-stu-id="fe7e3-124">For more information, see [Get started with tax service](./global-get-started-with-tax-calculation-service.md).</span></span>

## <a name="availability"></a><span data-ttu-id="fe7e3-125">Pieejamība</span><span class="sxs-lookup"><span data-stu-id="fe7e3-125">Availability</span></span>

<span data-ttu-id="fe7e3-126">Nodokļu aprēķins ir pieejams tikai smilškastes vidē un izvēlētajiem debitoriem, izmantojot publisku priekšskatījuma programmu.</span><span class="sxs-lookup"><span data-stu-id="fe7e3-126">Tax Calculation is available only in sandbox environments and to selected customers, through a public preview program.</span></span> <span data-ttu-id="fe7e3-127">Visbeidzot, tas kļūs plaši pieejams visiem debitoriem un ražošanas vidēs.</span><span class="sxs-lookup"><span data-stu-id="fe7e3-127">Eventually, it will become generally available to all customers and in production environments.</span></span>

<span data-ttu-id="fe7e3-128">Arī turpmāk tiks piegādāti jauni līdzekļi, tāpēc noteikti iepazīstieties ar visjaunāko dokumentāciju, lai uzzinātu par atbalstīto funkciju segumu un darbības jomu.</span><span class="sxs-lookup"><span data-stu-id="fe7e3-128">New features will continue to be delivered, so be sure to check the most up-to-date documentation often to learn about the coverage and scope of supported features.</span></span>

<span data-ttu-id="fe7e3-129">Nodokļu aprēķins ir izvietots tālāk redzamajās Azure ģeogrāfiskās lapās.</span><span class="sxs-lookup"><span data-stu-id="fe7e3-129">Tax Calculation is deployed in the following Azure geographies.</span></span> <span data-ttu-id="fe7e3-130">Tas tiks izvietots arī vairākās Azure ģeogrāfiskās vietās atbilstoši debitoru vajadzībām:</span><span class="sxs-lookup"><span data-stu-id="fe7e3-130">It will also be deployed to more Azure geographies, based on customer needs:</span></span>

- <span data-ttu-id="fe7e3-131">ASV</span><span class="sxs-lookup"><span data-stu-id="fe7e3-131">United States</span></span>
- <span data-ttu-id="fe7e3-132">Eiropa</span><span class="sxs-lookup"><span data-stu-id="fe7e3-132">Europe</span></span>

> [!NOTE]
> <span data-ttu-id="fe7e3-133">Nodokļu aprēķins neatbalsta Dynamics 365 lokālas izvietošanas.</span><span class="sxs-lookup"><span data-stu-id="fe7e3-133">Tax Calculation doesn't support on-premises deployments of Dynamics 365.</span></span> <span data-ttu-id="fe7e3-134">Tas neatbalsta arī agrākas versijas, piemēram, Dynamics AX 2012.</span><span class="sxs-lookup"><span data-stu-id="fe7e3-134">It also doesn't support earlier versions, such as Dynamics AX 2012.</span></span>

## <a name="feature-highlights"></a><span data-ttu-id="fe7e3-135">Līdzekļu iezīmēšana</span><span class="sxs-lookup"><span data-stu-id="fe7e3-135">Feature highlights</span></span>

- <span data-ttu-id="fe7e3-136">Konfigurējama nodokļu matrica, lai automātiski noteiktu un aprēķinātu nodokli</span><span class="sxs-lookup"><span data-stu-id="fe7e3-136">A configurable tax matrix to automatically determine and calculate tax</span></span>
- <span data-ttu-id="fe7e3-137">Atbalstīt vairākus nodokļa reģistrācijas numurus</span><span class="sxs-lookup"><span data-stu-id="fe7e3-137">Support for multiple tax registration numbers</span></span>
- <span data-ttu-id="fe7e3-138">Pārsūtīšanas pasūtījuma atbalsts nodokļu noteikšanai un aprēķinam</span><span class="sxs-lookup"><span data-stu-id="fe7e3-138">Transfer order support for tax determination and calculation</span></span>
- <span data-ttu-id="fe7e3-139">Pārsūtīšanas pasūtījuma atbalsts vairāku nodokļa reģistrācijas numuru noteikšanai</span><span class="sxs-lookup"><span data-stu-id="fe7e3-139">Transfer order support for determination of multiple tax registration numbers</span></span>

## <a name="supported-transactions"></a><span data-ttu-id="fe7e3-140">Atbalstītie darījumi</span><span class="sxs-lookup"><span data-stu-id="fe7e3-140">Supported transactions</span></span>

<span data-ttu-id="fe7e3-141">Nodokļu aprēķinu var iespējot juridiska persona un darījums.</span><span class="sxs-lookup"><span data-stu-id="fe7e3-141">Tax Calculation can be enabled by legal entity and transaction.</span></span> <span data-ttu-id="fe7e3-142">Tālāk ir norādīti atbalstītie darījumi.</span><span class="sxs-lookup"><span data-stu-id="fe7e3-142">The following transactions are supported:</span></span>

- <span data-ttu-id="fe7e3-143">Pārdošanas process</span><span class="sxs-lookup"><span data-stu-id="fe7e3-143">Sales process</span></span>

    - <span data-ttu-id="fe7e3-144">Pārdošanas piedāvājums</span><span class="sxs-lookup"><span data-stu-id="fe7e3-144">Sales quotation</span></span>
    - <span data-ttu-id="fe7e3-145">Pārdošanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="fe7e3-145">Sales order</span></span>
    - <span data-ttu-id="fe7e3-146">Apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="fe7e3-146">Confirmation</span></span>
    - <span data-ttu-id="fe7e3-147">Izdošanas saraksts</span><span class="sxs-lookup"><span data-stu-id="fe7e3-147">Picking list</span></span>
    - <span data-ttu-id="fe7e3-148">Pavadzīme</span><span class="sxs-lookup"><span data-stu-id="fe7e3-148">Packing slip</span></span>
    - <span data-ttu-id="fe7e3-149">Pārdošanas rēķins</span><span class="sxs-lookup"><span data-stu-id="fe7e3-149">Sales invoice</span></span>
    - <span data-ttu-id="fe7e3-150">Kredīta piezīme</span><span class="sxs-lookup"><span data-stu-id="fe7e3-150">Credit note</span></span>
    - <span data-ttu-id="fe7e3-151">Atgriešanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="fe7e3-151">Return order</span></span>
    - <span data-ttu-id="fe7e3-152">Virsraksta papildmaksa</span><span class="sxs-lookup"><span data-stu-id="fe7e3-152">Header miscellaneous charge</span></span>
    - <span data-ttu-id="fe7e3-153">Rindas papildmaksas pieprasījums</span><span class="sxs-lookup"><span data-stu-id="fe7e3-153">Line miscellaneous charge</span></span>

- <span data-ttu-id="fe7e3-154">Pirkšanas process</span><span class="sxs-lookup"><span data-stu-id="fe7e3-154">Purchase process</span></span>

    - <span data-ttu-id="fe7e3-155">Pirkuma pasūtījums</span><span class="sxs-lookup"><span data-stu-id="fe7e3-155">Purchase order</span></span>
    - <span data-ttu-id="fe7e3-156">Apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="fe7e3-156">Confirmation</span></span>
    - <span data-ttu-id="fe7e3-157">Saņemšanas saraksts</span><span class="sxs-lookup"><span data-stu-id="fe7e3-157">Receipts list</span></span>
    - <span data-ttu-id="fe7e3-158">Produktu ieejas plūsma</span><span class="sxs-lookup"><span data-stu-id="fe7e3-158">Product receipt</span></span>
    - <span data-ttu-id="fe7e3-159">Pirkšanas rēķins</span><span class="sxs-lookup"><span data-stu-id="fe7e3-159">Purchase invoice</span></span>
    - <span data-ttu-id="fe7e3-160">Virsraksta papildmaksas pieprasījums</span><span class="sxs-lookup"><span data-stu-id="fe7e3-160">Header miscellaneous charge</span></span>
    - <span data-ttu-id="fe7e3-161">Rindas papildmaksas pieprasījums</span><span class="sxs-lookup"><span data-stu-id="fe7e3-161">Line miscellaneous charge</span></span>
    - <span data-ttu-id="fe7e3-162">Kredīta piezīme</span><span class="sxs-lookup"><span data-stu-id="fe7e3-162">Credit note</span></span>
    - <span data-ttu-id="fe7e3-163">Atgriešanas pasūtījums</span><span class="sxs-lookup"><span data-stu-id="fe7e3-163">Return order</span></span>
    - <span data-ttu-id="fe7e3-164">Pirkšanas pieprasījums</span><span class="sxs-lookup"><span data-stu-id="fe7e3-164">Purchase requisition</span></span>
    - <span data-ttu-id="fe7e3-165">Pirkšanas pieprasījuma rindas papildmaksas pieprasījums</span><span class="sxs-lookup"><span data-stu-id="fe7e3-165">Purchase requisition line miscellaneous charge</span></span>
    - <span data-ttu-id="fe7e3-166">Piedāvājuma pieprasījums</span><span class="sxs-lookup"><span data-stu-id="fe7e3-166">Request for quotation</span></span>
    - <span data-ttu-id="fe7e3-167">Piedāvājuma pieprasījuma virsraksta papildmaksas pieprasījums</span><span class="sxs-lookup"><span data-stu-id="fe7e3-167">Request for quotation header miscellaneous charge</span></span>
    - <span data-ttu-id="fe7e3-168">Piedāvājuma pieprasījuma rindas papildmaksas pieprasījums</span><span class="sxs-lookup"><span data-stu-id="fe7e3-168">Request for quotation line miscellaneous charge</span></span>

- <span data-ttu-id="fe7e3-169">Krājumu process</span><span class="sxs-lookup"><span data-stu-id="fe7e3-169">Inventory process</span></span>

    - <span data-ttu-id="fe7e3-170">Pārvietošanas pasūtījums – nosūtīšana</span><span class="sxs-lookup"><span data-stu-id="fe7e3-170">Transfer order – ship</span></span>
    - <span data-ttu-id="fe7e3-171">Pārsūtīšanas pasūtījums – saņemšana</span><span class="sxs-lookup"><span data-stu-id="fe7e3-171">Transfer order – receive</span></span>

## <a name="related-resources"></a><span data-ttu-id="fe7e3-172">Saistītie resursi</span><span class="sxs-lookup"><span data-stu-id="fe7e3-172">Related resources</span></span>

[<span data-ttu-id="fe7e3-173">Darba sākšana ar nodokļu pakalpojumu</span><span class="sxs-lookup"><span data-stu-id="fe7e3-173">Get started with tax service</span></span>](./global-get-started-with-tax-calculation-service.md)

[<span data-ttu-id="fe7e3-174">Vairāki PVN reģistrācijas numuri</span><span class="sxs-lookup"><span data-stu-id="fe7e3-174">Multiple VAT registration number</span></span>](./emea-multiple-vat-registration-numbers.md)

[<span data-ttu-id="fe7e3-175">Nodokļu līdzekļu atbalsts pārsūtīšanas pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="fe7e3-175">Tax feature support for transfer order</span></span>](./tasks/tax-feature-support-for-transfer-order.md)

[<span data-ttu-id="fe7e3-176">Kā veidot paplašinājumu nodokļu pakalpojumā</span><span class="sxs-lookup"><span data-stu-id="fe7e3-176">How to build extension in tax service</span></span>](./tax-service-add-data-fields-tax-integration-by-extension.md)
