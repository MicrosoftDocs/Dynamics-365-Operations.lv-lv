---
title: E-pasta ziņojumu veidņu izveide transakciju notikumiem
description: Šajā tēmā ir aprakstīts, kā izveidot, augšupielādēt un konfigurēt e-pasta veidnes darbību notikumiem programmā Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: annbe
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 756e2a64ef4c33c347106968eb6bc79a413c3ff7
ms.sourcegitcommit: 88babb2fffe97e93bbde543633fc492120f2a4fc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/06/2021
ms.locfileid: "5555249"
---
# <a name="create-email-templates-for-transactional-events"></a><span data-ttu-id="7ac3b-103">E-pasta ziņojumu veidņu izveide transakciju notikumiem</span><span class="sxs-lookup"><span data-stu-id="7ac3b-103">Create email templates for transactional events</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7ac3b-104">Šajā tēmā ir aprakstīts, kā izveidot, augšupielādēt un konfigurēt e-pasta veidnes darbību notikumiem programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-104">This topic describes how to create, upload, and configure email templates for transactional events in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7ac3b-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="7ac3b-105">Overview</span></span>

<span data-ttu-id="7ac3b-106">Dynamics 365 Commerce nodrošina ārpus kastes risinājumu, kas paredzēts, lai sūtītu e-pasta ziņojumus, kas brīdina debitorus par darbību notikumiem (piemēram, kad tiek veikts pasūtījums, pasūtījums ir gatavs saņemšanai vai pasūtījums ir nosūtīts).</span><span class="sxs-lookup"><span data-stu-id="7ac3b-106">Dynamics 365 Commerce provides an out-of-box solution for sending emails that alert customers about transactional events (for example, when an order is placed, an order is ready for pickup, or an order has been shipped).</span></span> <span data-ttu-id="7ac3b-107">Šajā tēmā aprakstīti soļi, kā izveidot, augšupielādēt un konfigurēt e-pasta veidnes, kas tiek izmantotas, lai nosūtītu darbības e-pasta ziņojumus.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-107">This topic describes the steps for creating, uploading, and configuring the email templates that are used to send transactional emails.</span></span>

## <a name="create-an-email-template"></a><span data-ttu-id="7ac3b-108">E-pasta veidnes izveidošana</span><span class="sxs-lookup"><span data-stu-id="7ac3b-108">Create an email template</span></span>

<span data-ttu-id="7ac3b-109">Pirms varat kartēt specifisku darbību notikumu uz e-pasta veidni, ir jāizveido veidne.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-109">Before you can map a specific transactional event to an email template, you must create the template.</span></span>

<span data-ttu-id="7ac3b-110">Lai izveidotu e-pasta veidni, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-110">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="7ac3b-111">Programmā Commerce Headquarters atveriet **Mazumtirdzniecība un tirdzniecība \> Headquarters iestatīšana \> Organizācijas e-pasta veidnes** vai **Organizācijas administrēšana \> Iestatīšana \> Organizācijas e-pasta veidnes**.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-111">In Commerce headquarters, go to **Retail and Commerce \> Headquarters setup \> Organization email templates** or **Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="7ac3b-112">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-112">Select **New**.</span></span>
1. <span data-ttu-id="7ac3b-113">Sadaļā **Vispārīgi** iestatiet šādus laukus:</span><span class="sxs-lookup"><span data-stu-id="7ac3b-113">Under **General**, set the following fields:</span></span>

    - <span data-ttu-id="7ac3b-114">**E-pasta ID** — e-pasta ID ir unikāls veidnes identifikators, un tā ir vērtība, kas tiek rādīta, atlasot veidni, ko kartēt uz notikumu.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-114">**Email ID** – The email ID is the unique identifier for a template, and it's the value that is shown when you select a template to map to an event.</span></span>
    - <span data-ttu-id="7ac3b-115">**E-pasta apraksts** — jūs varat izmantot šo neobligāto lauku, lai sniegtu veidnes aprakstu.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-115">**Email description** – You can use this optional field to provide a description of the template.</span></span> <span data-ttu-id="7ac3b-116">Ievadītā vērtība parādās tikai Commerce galvenajā mītnē.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-116">The value that you enter appears only in Commerce headquarters.</span></span>
    - <span data-ttu-id="7ac3b-117">**Sūtītāja vārds** — ievadītais vārds parādās laukā “no” vairumā e-pasta klientu.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-117">**Sender name** – The name that you enter appears in the "from" field of most email clients.</span></span>
    - <span data-ttu-id="7ac3b-118">**Sūtītāja e-pasts** — ievadiet e-pasta adresi, kas jālieto e-pasta ziņojumiem, kas tiek nosūtīti, izmantojot šo veidni.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-118">**Sender email** – Enter the email address that should be used for emails that are sent by using this template.</span></span>
    - <span data-ttu-id="7ac3b-119">**Noklusētais valodas kods** — šis lauks norāda pēc noklusējuma nosūtītā e-pasta ziņojuma lokalizēto versiju, ja kanāls, kas izsauc šo veidni, nesniedz nekādu valodu.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-119">**Default language code** – This field specifies the localized version of the email that is sent by default, if no language is provided by the channel that invokes this template.</span></span>

1. <span data-ttu-id="7ac3b-120">Sadaļā **E-pasta** ziņojuma saturs atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-120">Under **Email message content**, select **New**.</span></span>
1. <span data-ttu-id="7ac3b-121">Laukā **Valoda** ievadiet e-pasta veidnes valodu.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-121">In the **Language** field, enter the language for the email template.</span></span> <span data-ttu-id="7ac3b-122">Vēlāk varat pievienot vairākas valodas un lokalizētas veidnes.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-122">You can add more languages and localized templates later.</span></span>
1. <span data-ttu-id="7ac3b-123">Laukā **Tēma** ievadiet e-pasta tēmu, kam jāparādās e-pasta tēmas laukā.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-123">In the **Subject** field, enter the email subject that should appear in the subject field of the email.</span></span>
1. <span data-ttu-id="7ac3b-124">Atlasiet **Rediģēt**, lai augšupielādētu savu e-pasta veidni.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-124">Select **Edit** to upload your email template.</span></span>

## <a name="create-an-email-message-body-by-using-html"></a><span data-ttu-id="7ac3b-125">E-pasta ziņojuma pamatteksta izveidošana, izmantojot HTML</span><span class="sxs-lookup"><span data-stu-id="7ac3b-125">Create an email message body by using HTML</span></span>

<span data-ttu-id="7ac3b-126">E-pasta ziņojuma pamatteksts ir sastādīts HTML formātā.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-126">The message body of your email is composed in HTML.</span></span> <span data-ttu-id="7ac3b-127">Jūs varat izmantot jebkuru izkārtojumu, stilu un zīmolu, ko HTML un iekļautās kaskadētās stila lapas (CSS) atļauj.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-127">You can use any layout, styling, and branding that HTML and inline Cascading Style Sheets (CSS) allow for.</span></span> <span data-ttu-id="7ac3b-128">Varat arī izmantot attēlus, ja tos uzturēsiet publiski pieejamā Web galapunktā.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-128">You can also use images, if you host them on a publicly available web endpoint.</span></span> <span data-ttu-id="7ac3b-129">Lai pievienotu attēlu, ievadiet attēla vietrādi URL, kas ir norādīts **src** atribūtā HTML **&lt;img&gt;** etiķetei.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-129">To add an image, enter the image's URL in the **src** attribute of the HTML **&lt;img&gt;** tag.</span></span>

> [!NOTE]
> <span data-ttu-id="7ac3b-130">E-pasta klienti nosaka izkārtojuma un stila ierobežojumus, kas varētu prasīt labojumus HTML un CSS, ko izmantojat ziņojuma pamattekstam.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-130">Email clients impose layout and style limitations that might require adjustments to the HTML and CSS that you use for the message body.</span></span> <span data-ttu-id="7ac3b-131">Mēs iesakām jums iepazīties ar labāko praksi, lai izveidotu HTML, ko atbalstīs populārākie e-pasta klienti.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-131">We recommend that you familiarize yourself with the best practices for creating HTML that will be supported by the most popular email clients.</span></span>

## <a name="add-placeholders-to-the-email-message-body"></a><span data-ttu-id="7ac3b-132">Pievienot vietturus e-pasta ziņojuma pamattekstam</span><span class="sxs-lookup"><span data-stu-id="7ac3b-132">Add placeholders to the email message body</span></span>

<span data-ttu-id="7ac3b-133">E-pasta ziņojumā var iekļaut vietturus, kas ir aizstāti ar debitoram specifiskām un darbībām specifiskām vērtībām laikā, kad tiek ģenerēts e-pasts.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-133">Your email can contain placeholders that are replaced with customer-specific and transaction-specific values when the email is generated.</span></span> <span data-ttu-id="7ac3b-134">Vietturus vienmēr ietver procentu zīmes (%), un tie tiek ievietoti tieši HTML dokumentā.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-134">Placeholders are always surrounded by percent signs (%) and are inserted directly into the HTML document.</span></span>

<span data-ttu-id="7ac3b-135">Tālāk ir minēts piemērs.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-135">Here is an example.</span></span>

```html
<p>
    Hello %customername%,<br />
    Order number %salesid%, can be picked up from the <b>%pickupstorename%</b> store.
</p>
```

### <a name="order-placeholders-sales-order-level"></a><span data-ttu-id="7ac3b-136">Pasūtījuma vietturi (pārdošanas pasūtījuma līmenis)</span><span class="sxs-lookup"><span data-stu-id="7ac3b-136">Order placeholders (sales order level)</span></span>

<span data-ttu-id="7ac3b-137">Šie vietturi izgūst un rāda datus, kas ir definēti pārdošanas pasūtījuma līmenī (pretēji pārdošanas rindas līmenim).</span><span class="sxs-lookup"><span data-stu-id="7ac3b-137">The following placeholders retrieve and show data that is defined at the sales order level (as opposed to the sales line level).</span></span>

| <span data-ttu-id="7ac3b-138">Viettura nosaukums</span><span class="sxs-lookup"><span data-stu-id="7ac3b-138">Placeholder name</span></span>     | <span data-ttu-id="7ac3b-139">Viettura vērtība</span><span class="sxs-lookup"><span data-stu-id="7ac3b-139">Placeholder value</span></span>                                            |
| -------------------- | ------------------------------------------------------------ |
| <span data-ttu-id="7ac3b-140">customername</span><span class="sxs-lookup"><span data-stu-id="7ac3b-140">customername</span></span>         | <span data-ttu-id="7ac3b-141">Klienta vārds, kurš veica pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-141">The name of the customer who placed the order.</span></span>               |
| <span data-ttu-id="7ac3b-142">salesid</span><span class="sxs-lookup"><span data-stu-id="7ac3b-142">salesid</span></span>              | <span data-ttu-id="7ac3b-143">Pasūtījuma pārdošanas ID.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-143">The sales ID of the order.</span></span>                                   |
| <span data-ttu-id="7ac3b-144">deliveryaddress</span><span class="sxs-lookup"><span data-stu-id="7ac3b-144">deliveryaddress</span></span>      | <span data-ttu-id="7ac3b-145">Piegādes adrese nosūtītajiem pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-145">The delivery address for shipped orders.</span></span>                     |
| <span data-ttu-id="7ac3b-146">customeraddress</span><span class="sxs-lookup"><span data-stu-id="7ac3b-146">customeraddress</span></span>      | <span data-ttu-id="7ac3b-147">Klienta adrese.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-147">The address of the customer.</span></span>                                 |
| <span data-ttu-id="7ac3b-148">customeremailaddress</span><span class="sxs-lookup"><span data-stu-id="7ac3b-148">customeremailaddress</span></span> | <span data-ttu-id="7ac3b-149">E-pasta adrese, kuru klients ievadīja norēķināšanās laikā.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-149">The email address that the customer entered at checkout.</span></span>     |
| <span data-ttu-id="7ac3b-150">deliverydate</span><span class="sxs-lookup"><span data-stu-id="7ac3b-150">deliverydate</span></span>         | <span data-ttu-id="7ac3b-151">Piegādes datums.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-151">The delivery date.</span></span>                                           |
| <span data-ttu-id="7ac3b-152">shipdate</span><span class="sxs-lookup"><span data-stu-id="7ac3b-152">shipdate</span></span>             | <span data-ttu-id="7ac3b-153">Nosūtīšanas datums.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-153">The ship date.</span></span>                                               |
| <span data-ttu-id="7ac3b-154">modeofdelivery</span><span class="sxs-lookup"><span data-stu-id="7ac3b-154">modeofdelivery</span></span>       | <span data-ttu-id="7ac3b-155">Pasūtījuma piegādes veids.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-155">The delivery mode of the order.</span></span>                              |
| <span data-ttu-id="7ac3b-156">maksas</span><span class="sxs-lookup"><span data-stu-id="7ac3b-156">charges</span></span>              | <span data-ttu-id="7ac3b-157">Pasūtījuma kopējās izmaksas.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-157">The total charges for the order.</span></span>                             |
| <span data-ttu-id="7ac3b-158">nodokļi</span><span class="sxs-lookup"><span data-stu-id="7ac3b-158">tax</span></span>                  | <span data-ttu-id="7ac3b-159">Pasūtījuma kopējie nodokļi.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-159">The total tax for the order.</span></span>                                 |
| <span data-ttu-id="7ac3b-160">kopā</span><span class="sxs-lookup"><span data-stu-id="7ac3b-160">total</span></span>                | <span data-ttu-id="7ac3b-161">Pasūtījuma kopējā summa.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-161">The total amount for the order.</span></span>                              |
| <span data-ttu-id="7ac3b-162">ordernetamount</span><span class="sxs-lookup"><span data-stu-id="7ac3b-162">ordernetamount</span></span>       | <span data-ttu-id="7ac3b-163">Pasūtījuma kopējā summa, no kuras atņem nodokļu kopsummu.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-163">The total amount for the order, minus the total tax.</span></span>         |
| <span data-ttu-id="7ac3b-164">atlaide</span><span class="sxs-lookup"><span data-stu-id="7ac3b-164">discount</span></span>             | <span data-ttu-id="7ac3b-165">Pasūtījuma kopējā atlaide.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-165">The total discount for the order.</span></span>                            |
| <span data-ttu-id="7ac3b-166">storename</span><span class="sxs-lookup"><span data-stu-id="7ac3b-166">storename</span></span>            | <span data-ttu-id="7ac3b-167">Veikala nosaukums, kur tika veikts pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-167">The name of the store where the order was placed.</span></span>            |
| <span data-ttu-id="7ac3b-168">storeaddress</span><span class="sxs-lookup"><span data-stu-id="7ac3b-168">storeaddress</span></span>         | <span data-ttu-id="7ac3b-169">Veikala adrese, kur tika veikts pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-169">The address of the store that placed the order.</span></span>              |
| <span data-ttu-id="7ac3b-170">storeopenfrom</span><span class="sxs-lookup"><span data-stu-id="7ac3b-170">storeopenfrom</span></span>        | <span data-ttu-id="7ac3b-171">Veikala, kuš veica pasūtījumu, atvēršanās laiks.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-171">The opening time of the store that placed the order.</span></span>         |
| <span data-ttu-id="7ac3b-172">storeopento</span><span class="sxs-lookup"><span data-stu-id="7ac3b-172">storeopento</span></span>          | <span data-ttu-id="7ac3b-173">Veikala, kuš veica pasūtījumu, aizvēršanās laiks.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-173">The closing time of the store that placed the order.</span></span>         |
| <span data-ttu-id="7ac3b-174">pickupstorename</span><span class="sxs-lookup"><span data-stu-id="7ac3b-174">pickupstorename</span></span>      | <span data-ttu-id="7ac3b-175">Veikala nosaukums, kurā pasūtījums tiks paņemts.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-175">The name of the store where the order will be picked up.</span></span>     |
| <span data-ttu-id="7ac3b-176">pickupstoreaddress</span><span class="sxs-lookup"><span data-stu-id="7ac3b-176">pickupstoreaddress</span></span>   | <span data-ttu-id="7ac3b-177">Veikala adrese, kurā pasūtījums tiks paņemts.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-177">The address of the store where the order will be picked up.</span></span>  |
| <span data-ttu-id="7ac3b-178">pickupopenstorefrom</span><span class="sxs-lookup"><span data-stu-id="7ac3b-178">pickupopenstorefrom</span></span>  | <span data-ttu-id="7ac3b-179">Veikala atvēršanās laiks, kurā pasūtījums tiks paņemts.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-179">The opening time of the store where the order will be picked up.</span></span> |
| <span data-ttu-id="7ac3b-180">pickupopenstoreto</span><span class="sxs-lookup"><span data-stu-id="7ac3b-180">pickupopenstoreto</span></span>    | <span data-ttu-id="7ac3b-181">Veikala aizvēršanās laiks, kurā pasūtījums tiks paņemts.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-181">The closing time of the store where the order will be picked up.</span></span> |

### <a name="order-line-placeholders-sales-line-level"></a><span data-ttu-id="7ac3b-182">Pasūtījuma rindas vietturi (pārdošanas rindas līmenis)</span><span class="sxs-lookup"><span data-stu-id="7ac3b-182">Order line placeholders (sales line level)</span></span>

<span data-ttu-id="7ac3b-183">Šie vietturi izgūst un parāda datus par atsevišķām precēm (rindām) pārdošanas pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-183">The following placeholders retrieve and show data for individual products (lines) in the sales order.</span></span>

| <span data-ttu-id="7ac3b-184">Viettura nosaukums</span><span class="sxs-lookup"><span data-stu-id="7ac3b-184">Placeholder name</span></span>               | <span data-ttu-id="7ac3b-185">Viettura vērtība</span><span class="sxs-lookup"><span data-stu-id="7ac3b-185">Placeholder value</span></span> |
|--------------------------------|-------------------|
| <span data-ttu-id="7ac3b-186">productid</span><span class="sxs-lookup"><span data-stu-id="7ac3b-186">productid</span></span>                      | <span data-ttu-id="7ac3b-187">Preces ID rindai.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-187">The product ID for the line.</span></span> |
| <span data-ttu-id="7ac3b-188">lineproductname</span><span class="sxs-lookup"><span data-stu-id="7ac3b-188">lineproductname</span></span>                | <span data-ttu-id="7ac3b-189">Preces nosaukums.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-189">The name of the product.</span></span> |
| <span data-ttu-id="7ac3b-190">lineproductdescription</span><span class="sxs-lookup"><span data-stu-id="7ac3b-190">lineproductdescription</span></span>         | <span data-ttu-id="7ac3b-191">Preces apraksts.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-191">The description of the product.</span></span> |
| <span data-ttu-id="7ac3b-192">linequantity</span><span class="sxs-lookup"><span data-stu-id="7ac3b-192">linequantity</span></span>                   | <span data-ttu-id="7ac3b-193">Vienību skaits, kas pasūtīts rindai, plus mērvienība (piemēram, **katrs** vai **pāris**).</span><span class="sxs-lookup"><span data-stu-id="7ac3b-193">The number of units that were ordered for the line, plus the unit of measure (for example, **ea**, or **pair**).</span></span> |
| <span data-ttu-id="7ac3b-194">lineunit</span><span class="sxs-lookup"><span data-stu-id="7ac3b-194">lineunit</span></span>                       | <span data-ttu-id="7ac3b-195">Mērvienība rindai.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-195">The unit of measure for the line.</span></span> |
| <span data-ttu-id="7ac3b-196">linequantity_withoutunit</span><span class="sxs-lookup"><span data-stu-id="7ac3b-196">linequantity_withoutunit</span></span>       | <span data-ttu-id="7ac3b-197">Vienību skaits, kas pasūtīts rindai bez mērvienības.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-197">The number of units that were ordered for the line, without the unit of measure.</span></span> |
| <span data-ttu-id="7ac3b-198">linequantitypicked</span><span class="sxs-lookup"><span data-stu-id="7ac3b-198">linequantitypicked</span></span>             | <span data-ttu-id="7ac3b-199">Izvēlēto vienību skaits, kad tiek izmantots **PickOrder** notikums.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-199">When the **PickOrder** event is used, the number of units that were picked.</span></span> <span data-ttu-id="7ac3b-200">Pretējā gadījumā **0** (nulle).</span><span class="sxs-lookup"><span data-stu-id="7ac3b-200">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="7ac3b-201">linequantitypicked_withoutunit</span><span class="sxs-lookup"><span data-stu-id="7ac3b-201">linequantitypicked_withoutunit</span></span> | <span data-ttu-id="7ac3b-202">Izdotais vienību skaits bez mērvienības, kad tiek izmantots **PickOrder** notikums.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-202">When the **PickOrder** event is used, the number of units that were picked, without the unit of measure.</span></span> <span data-ttu-id="7ac3b-203">Pretējā gadījumā **0** (nulle).</span><span class="sxs-lookup"><span data-stu-id="7ac3b-203">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="7ac3b-204">linequantitypacked</span><span class="sxs-lookup"><span data-stu-id="7ac3b-204">linequantitypacked</span></span>             | <span data-ttu-id="7ac3b-205">Vienību skaits, kas tika iepakots, kad tiek izmantoti **PackOrder** un **Pasūtījums gatavs saņemšanai** notikumi.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-205">When the **PackOrder** and **Order ready for pickup** events are used, the number of units that were packed.</span></span> <span data-ttu-id="7ac3b-206">Pretējā gadījumā **0** (nulle).</span><span class="sxs-lookup"><span data-stu-id="7ac3b-206">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="7ac3b-207">linequantitypacked_withoutuom</span><span class="sxs-lookup"><span data-stu-id="7ac3b-207">linequantitypacked_withoutuom</span></span>  | <span data-ttu-id="7ac3b-208">Vienību skaits, kas tika iepakots bez mērvienības, kad tiek izmantoti **PackOrder** un **Pasūtījums gatavs saņemšanai** notikumi.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-208">When the **PackOrder** and **Order ready for pickup** events are used, the number of units that were packed, without the unit of measure.</span></span> <span data-ttu-id="7ac3b-209">Pretējā gadījumā **0** (nulle).</span><span class="sxs-lookup"><span data-stu-id="7ac3b-209">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="7ac3b-210">linequantityshipped</span><span class="sxs-lookup"><span data-stu-id="7ac3b-210">linequantityshipped</span></span>            | <span data-ttu-id="7ac3b-211">Vienmēr **0**, izņemot gadījumus, kad tiek izmantoti konkrēti notikumi, kā aprakstīts nākamajā rindā.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-211">Always **0**, except when specific events are used, as described in the next row.</span></span> |
| <span data-ttu-id="7ac3b-212">linequantityshipped_withoutuom</span><span class="sxs-lookup"><span data-stu-id="7ac3b-212">linequantityshipped_withoutuom</span></span> | <span data-ttu-id="7ac3b-213">Izdotais vienību skaits bez mērvienības, kad tiek izmantots **ShipOrder** notikums.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-213">When the **ShipOrder** event is used, the number of units that were picked, without the unit of measure.</span></span> <span data-ttu-id="7ac3b-214">Pretējā gadījumā **0** (nulle).</span><span class="sxs-lookup"><span data-stu-id="7ac3b-214">Otherwise, **0** (zero).</span></span> |
| <span data-ttu-id="7ac3b-215">lineprice</span><span class="sxs-lookup"><span data-stu-id="7ac3b-215">lineprice</span></span>                      | <span data-ttu-id="7ac3b-216">Vienas vienības cena.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-216">The price of a single unit.</span></span> |
| <span data-ttu-id="7ac3b-217">linenetamount</span><span class="sxs-lookup"><span data-stu-id="7ac3b-217">linenetamount</span></span>                  | <span data-ttu-id="7ac3b-218">Tiek pielietota rindas cena pēc vienību skaita un atlaides.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-218">The price of the line after the number of units and discount are applied.</span></span> |
| <span data-ttu-id="7ac3b-219">linediscount</span><span class="sxs-lookup"><span data-stu-id="7ac3b-219">linediscount</span></span>                   | <span data-ttu-id="7ac3b-220">Atlaide atsevišķai vienībai.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-220">The discount for an individual unit.</span></span> |
| <span data-ttu-id="7ac3b-221">lineshipdate</span><span class="sxs-lookup"><span data-stu-id="7ac3b-221">lineshipdate</span></span>                   | <span data-ttu-id="7ac3b-222">Rindas nosūtīšanas datums.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-222">The ship date for the line.</span></span> |
| <span data-ttu-id="7ac3b-223">linedeliverydate</span><span class="sxs-lookup"><span data-stu-id="7ac3b-223">linedeliverydate</span></span>               | <span data-ttu-id="7ac3b-224">Rindas piegādes datums.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-224">The delivery date for the line.</span></span> |
| <span data-ttu-id="7ac3b-225">linedeliverymode</span><span class="sxs-lookup"><span data-stu-id="7ac3b-225">linedeliverymode</span></span>               | <span data-ttu-id="7ac3b-226">Rindas piegādes veids.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-226">The delivery mode for the line.</span></span> |
| <span data-ttu-id="7ac3b-227">linedeliveryaddress</span><span class="sxs-lookup"><span data-stu-id="7ac3b-227">linedeliveryaddress</span></span>            | <span data-ttu-id="7ac3b-228">Rindas piegādes adrese.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-228">The delivery address for the line.</span></span> |
| <span data-ttu-id="7ac3b-229">giftcardnumber</span><span class="sxs-lookup"><span data-stu-id="7ac3b-229">giftcardnumber</span></span>                 | <span data-ttu-id="7ac3b-230">Dāvanu kartes numurs dāvanu kartes veida precēm.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-230">The gift card number, for products of the gift card type.</span></span> |
| <span data-ttu-id="7ac3b-231">giftcardbalance</span><span class="sxs-lookup"><span data-stu-id="7ac3b-231">giftcardbalance</span></span>                | <span data-ttu-id="7ac3b-232">Dāvanu kartes bilance dāvanu kartes veida precēm.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-232">The gift card balance, for products of the gift card type.</span></span> |
| <span data-ttu-id="7ac3b-233">giftcardmessage</span><span class="sxs-lookup"><span data-stu-id="7ac3b-233">giftcardmessage</span></span>                | <span data-ttu-id="7ac3b-234">Dāvanu kartes ziņojums dāvanu kartes veida precēm.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-234">The gift card message, for products of the gift card type.</span></span> |
| <span data-ttu-id="7ac3b-235">giftcardpin</span><span class="sxs-lookup"><span data-stu-id="7ac3b-235">giftcardpin</span></span>                    | <span data-ttu-id="7ac3b-236">Dāvanu kartes personīgais identifikācijas numurs (PIN) dāvanu kartes veida precēm.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-236">The personal identification number (PIN) of the gift card, for products of the gift card type.</span></span> <span data-ttu-id="7ac3b-237">(Šis vietturis ir raksturīgs ārējām dāvanu kartēm.)</span><span class="sxs-lookup"><span data-stu-id="7ac3b-237">(This placeholder is specific to external gift cards.)</span></span> |
| <span data-ttu-id="7ac3b-238">giftcardexpiration</span><span class="sxs-lookup"><span data-stu-id="7ac3b-238">giftcardexpiration</span></span>             | <span data-ttu-id="7ac3b-239">Dāvanu kartes beigu datums dāvanu kartes veida precēm.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-239">The expiration date of the gift card, for products of the gift card type.</span></span> <span data-ttu-id="7ac3b-240">(Šis vietturis ir raksturīgs ārējām dāvanu kartēm.)</span><span class="sxs-lookup"><span data-stu-id="7ac3b-240">(This placeholder is specific to external gift cards.)</span></span> |
| <span data-ttu-id="7ac3b-241">giftcardrecipientname</span><span class="sxs-lookup"><span data-stu-id="7ac3b-241">giftcardrecipientname</span></span>          | <span data-ttu-id="7ac3b-242">Dāvanu kartes saņēmēja vārds dāvanu kartes veida precēm.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-242">The name of the gift card recipient, for products of the gift card type.</span></span> |
| <span data-ttu-id="7ac3b-243">giftcardbuyername</span><span class="sxs-lookup"><span data-stu-id="7ac3b-243">giftcardbuyername</span></span>              | <span data-ttu-id="7ac3b-244">Dāvanu kartes pircēja vārds dāvanu kartes veida precēm.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-244">The name of the gift card buyer, for products of the gift card type.</span></span> |

### <a name="format-of-order-line-placeholders-in-the-email-message-body"></a><span data-ttu-id="7ac3b-245">Pasūtījuma rindu vietturu formāts e-pasta ziņojuma pamattekstā</span><span class="sxs-lookup"><span data-stu-id="7ac3b-245">Format of order line placeholders in the email message body</span></span>

<span data-ttu-id="7ac3b-246">Kad jūs izveidojat HTML atsevišķu pasūtījuma rindu e-pasta ziņojuma pamattekstā, aplieciet atkārtojošos HTML un vietturu bloku rindas ar šādiem vietturiem, kas tiek ievietoti HTML komentāra tagos.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-246">When you create the HTML for the individual order lines in the email message body, surround the repeating block of HTML and placeholders for the lines with the following placeholders that are put inside HTML comment tags.</span></span>

```html
<!--%tablebegin.salesline%-->

(Insert the repeating block of HTML and placeholders for individual lines here.)

<!--%tableend.salesline%-->
```

<span data-ttu-id="7ac3b-247">Tālāk ir minēts piemērs.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-247">Here is an example.</span></span>

```HTML
<table>
    <tr>
        <td>Product name</td>
        <td>Quantity</td>
        <td>Price</td>
    </tr>
    <!--%tablebegin.salesline%-->
    <tr>
        <td>%lineproductname%</td>
        <td>%linequantity_withoutunit%</td>
        <td>%lineprice%</td>
    </tr>
    <!--%tableend.salesline%-->
</table>
```

## <a name="create-a-template-for-emailed-receipts"></a><span data-ttu-id="7ac3b-248">Izveidot e-pasta saņēmēju veidni</span><span class="sxs-lookup"><span data-stu-id="7ac3b-248">Create a template for emailed receipts</span></span>

<span data-ttu-id="7ac3b-249">Saņemšanu var nosūtīt debitoriem, kuri veic pirkumus pārdošanas punktā (POS).</span><span class="sxs-lookup"><span data-stu-id="7ac3b-249">Receipts can be emailed to customers who make purchases at a retail point of sale (POS).</span></span> <span data-ttu-id="7ac3b-250">Kopumā darbības e-pasta saņemšanas veidnes izveidei ir tādas paša, lai izveidotu veidnes citiem darbību notikumiem.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-250">In general, the steps for creating the emailed receipt template are the same as the steps for creating templates for other transactional events.</span></span> <span data-ttu-id="7ac3b-251">Tomēr ir nepieciešamas šādas izmaiņas:</span><span class="sxs-lookup"><span data-stu-id="7ac3b-251">However, the following changes are required:</span></span>

- <span data-ttu-id="7ac3b-252">Kvīts teksts tiek iesprausts e-pasta ziņojumā, izmantojot **%message%** vietturi.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-252">The text of the receipt is inserted into the email by using the **%message%** placeholder.</span></span> <span data-ttu-id="7ac3b-253">Lai nodrošinātu, ka kvīts struktūra ir pareizi izveidota, ietveriet **%message%** vietturi ar HTML **&lt;pre&gt;** and **&lt;/pre&gt;** tagiem.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-253">To ensure that the receipt body is correctly rendered, surround the **%message%** placeholder with HTML **&lt;pre&gt;** and **&lt;/pre&gt;** tags.</span></span>
- <span data-ttu-id="7ac3b-254">Vietturi **%receiptid%** var izmantot, lai parādītu QR kodu vai svītrkodu, kas pārstāv kvīts ID.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-254">The **%receiptid%** placeholder can be used to show a QR code or bar code that represents the receipt ID.</span></span> <span data-ttu-id="7ac3b-255">(QR kodi un svītrkodi tiek dinamiski izveidoti un apkalpoti ar trešās puses pakalpojumu.) Papildinformāciju par to, kā e-pasta kvītī parādīt QR kodu vai svītrkodu, skatiet sadaļā [QR koda vai svītrkoda pievienošana darījumu un kvīts e-pasta ziņojumiem](add-qr-code-barcode-email.md).</span><span class="sxs-lookup"><span data-stu-id="7ac3b-255">(QR codes and bar codes are dynamically generated and served by a third-party service.) For more information about how to show a QR code or bar code in an emailed receipt, see [Add a QR code or bar code to transactional and receipt emails](add-qr-code-barcode-email.md).</span></span>

## <a name="upload-the-email-html"></a><span data-ttu-id="7ac3b-256">Augšupielādēt e-pasta HTML</span><span class="sxs-lookup"><span data-stu-id="7ac3b-256">Upload the email HTML</span></span>

<span data-ttu-id="7ac3b-257">Pēc tam, kad esat izveidojis un pārbaudījis HTML jūsu ziņojuma pamattekstam, tas ir jāaugšupielādē Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-257">After you've created and tested the HTML for your message body, it must be uploaded to Commerce headquarters.</span></span> <span data-ttu-id="7ac3b-258">Pašlaik e-pasta HTML nevar eksportēt.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-258">Currently, email HTML can't be exported.</span></span> <span data-ttu-id="7ac3b-259">Tāpēc jums ir jāsaglabā galvenā kopija jūsu HTML ārpus Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-259">Therefore, you must maintain the master copy of your HTML outside Commerce headquarters.</span></span>

<span data-ttu-id="7ac3b-260">Lai augšupielādētu jaunu vai rediģētu e-pasta veidnes HTML, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-260">To upload a new or edited email template HTML, follow these steps.</span></span>

1. <span data-ttu-id="7ac3b-261">Commerce galvenajā mītnē dodieties uz **Mazumtirdzniecība un tirdzniecība \> Galvenās mītnes iestatījumi \> Organizācijas e-pasta veidnes**.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-261">In Commerce headquarters, go to **Retail and Commerce \> Headquarters setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="7ac3b-262">Atlasiet tās valodas rindu, kurai vēlaties pievienot vai aizstāt HTML.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-262">Select the row for the language that you want to add or replace HTML for.</span></span> <span data-ttu-id="7ac3b-263">Varat arī atlasīt **Jauns**, lai izveidotu rindu jaunai valodai.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-263">Alternatively, select **New** to create a row for a new language.</span></span>
1. <span data-ttu-id="7ac3b-264">Atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-264">Select **Edit**.</span></span>
1. <span data-ttu-id="7ac3b-265">Parādītajā dialoglodziņā atlasiet **Pārlūkot**.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-265">In the dialog box that appears, select **Browse**.</span></span> <span data-ttu-id="7ac3b-266">Pārlūkojiet HTML dokumentu, kuru vēlaties augšupielādēt, atlasiet to un pēc tam atlasiet **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-266">Browse to the HTML document that you want to upload, select it, and then select **Open**.</span></span>
1. <span data-ttu-id="7ac3b-267">Atlasiet **Augšupielādēt**.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-267">Select **Upload**.</span></span>
1. <span data-ttu-id="7ac3b-268">Kad e-pasta HTML tiek parādīts priekšskatījuma logā, izvēlieties **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-268">After your email HTML appears in the preview window, select **OK**.</span></span>
1. <span data-ttu-id="7ac3b-269">Pārliecinieties ka ir atlasīta **Ir ķermenis** izvēles rūtiņa rindai.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-269">Make sure that the **Has body** check box is selected for the row.</span></span>

<span data-ttu-id="7ac3b-270">Ja esat jau konfigurējis Commerce Headquarters, lai sūtītu e-pastu, jaunais vai atjauninātais e-pasts tiks nosūtīts visiem debitoriem, kuri veic darbību, un tas, savukārt, izsauc notikumu, kas ir kartēts veidnē.</span><span class="sxs-lookup"><span data-stu-id="7ac3b-270">If you've already configured Commerce headquarters to send email, your new or updated email will be sent to all customers who perform a transaction that invokes the event that is mapped to the template.</span></span>

<span data-ttu-id="7ac3b-271">Papildinformāciju par to, kā konfigurēt e-pasta vēstules Dynamics 365 Commerce, skatiet sadaļā [E-pasta konfigurēšana un sūtīšana](../fin-ops-core/fin-ops/organization-administration/configure-email.md).</span><span class="sxs-lookup"><span data-stu-id="7ac3b-271">For more information about how to configure emails in Dynamics 365 Commerce, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7ac3b-272">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="7ac3b-272">Additional resources</span></span> 

[<span data-ttu-id="7ac3b-273">E-pasta paziņojumu profila iestatīšana</span><span class="sxs-lookup"><span data-stu-id="7ac3b-273">Set up an email notification profile</span></span>](email-notification-profiles.md)

[<span data-ttu-id="7ac3b-274">E-pasta konfigurēšana un sūtīšana</span><span class="sxs-lookup"><span data-stu-id="7ac3b-274">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md)

[<span data-ttu-id="7ac3b-275">Iestatīt e-pasta saņemšanu</span><span class="sxs-lookup"><span data-stu-id="7ac3b-275">Set up email receipts</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-email-receipts)

[<span data-ttu-id="7ac3b-276">E-pasta kvīšu sūtīšana no Modern POS </span><span class="sxs-lookup"><span data-stu-id="7ac3b-276">Send email receipts from Modern POS </span></span>](email-receipts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
