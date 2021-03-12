---
title: Klienta preču saņemšanas laika nišu izveidošana un atjaunināšana
description: Šajā tēmā ir aprakstīts, kā izveidot, konfigurēt un atjaunināt klientu preču saņemšanas laika nišas programmā Commerce Headquarters.
author: anupamar-ms
manager: AnnBe
ms.date: 01/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2020-09-20
ms.dyn365.ops.version: Retail 10.0.15 update
ms.openlocfilehash: 125696e8f32c2452a572a2316f512779f399f5c4
ms.sourcegitcommit: 8b4cb7b6ad4aab37566bcc91e426bd56db771416
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/06/2021
ms.locfileid: "4828215"
---
# <a name="create-and-update-time-slots-for-customer-pickup"></a><span data-ttu-id="43cd2-103">Klienta preču saņemšanas laika nišu izveidošana un atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="43cd2-103">Create and update time slots for customer pickup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="43cd2-104">Šajā tēmā ir aprakstīts, kā izveidot, konfigurēt un atjaunināt klientu preču saņemšanas laika nišas programmā Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="43cd2-104">This topic describes how to create, configure, and update customer pickup time slots in Commerce headquarters.</span></span>

<span data-ttu-id="43cd2-105">Laika nišas funkcija sniedz mazumtirgotājiem veidu, kā definēt laika nišu krājumiem, kam ir ieslēgts klientu saņemšanas piegādes veids.</span><span class="sxs-lookup"><span data-stu-id="43cd2-105">The time slot feature gives retailers a way to define a time slot for items that the customer pickup delivery mode is turned on for.</span></span> <span data-ttu-id="43cd2-106">Laika nišas ļauj mazumtirgotājiem noteikt dienas un laikus, kad pasūtījumi var tikt saņemti veikalā.</span><span class="sxs-lookup"><span data-stu-id="43cd2-106">Time slots let retailers define the days and times when orders can be picked up from a store.</span></span> <span data-ttu-id="43cd2-107">Mazumtirgotāji var arī definēt pasūtījumu skaitu, ko var saņemt noteiktā periodā.</span><span class="sxs-lookup"><span data-stu-id="43cd2-107">Retailers can also define the number of orders that can be picked up during a given period.</span></span> <span data-ttu-id="43cd2-108">Šādā veidā tirgotāji var ierobežot pasūtījumu skaitu, ko var saņemt noteiktā dienā un noteiktā laikā.</span><span class="sxs-lookup"><span data-stu-id="43cd2-108">In this way, retailers can limit the number of orders that can be picked up on a given day and at a given time.</span></span> <span data-ttu-id="43cd2-109">Rezultāts ir labākas kvalitātes pieredze saviem klientiem.</span><span class="sxs-lookup"><span data-stu-id="43cd2-109">The result is a better-quality experience for their customers.</span></span>

> [!NOTE]
> <span data-ttu-id="43cd2-110">Laika nišas līdzeklis ir pieejams Microsoft Dynamics 365 Commerce versijā 10.0.15 un jaunākās versijās.</span><span class="sxs-lookup"><span data-stu-id="43cd2-110">The time slot feature is available in Microsoft Dynamics 365 Commerce version 10.0.15 and later.</span></span>

<span data-ttu-id="43cd2-111">Sekojošajā attēlā parādīts laika nišas atlases piemērs e-tirdzniecības norēķināšanās laikā.</span><span class="sxs-lookup"><span data-stu-id="43cd2-111">The following illustration shows an example of time slot selection during e-commerce checkout.</span></span>

![Laika nišas atlases piemērs e-tirdzniecības norēķināšanās laikā](../dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="time-slot-properties"></a><span data-ttu-id="43cd2-113">Laika nišas rekvizīti</span><span class="sxs-lookup"><span data-stu-id="43cd2-113">Time slot properties</span></span>

<span data-ttu-id="43cd2-114">Laika niša ir noteikts intervāls, kad klients var izvēlēties saņemt pasūtījumu no noteikta veikala vai atrašanās vietas.</span><span class="sxs-lookup"><span data-stu-id="43cd2-114">A time slot is a specific interval when a customer can choose to pick up an order from a specific store or location.</span></span> <span data-ttu-id="43cd2-115">Laika nišu pārvaldības līdzeklis ir pieejams tikai tad, ja ir konfigurēts klienta saņemšanas piegādes veids risinājumā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="43cd2-115">The time slot management feature is available only when the customer pickup delivery mode is configured in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="43cd2-116">Laika niša tiek definēta, izmantojot šādus rekvizītus:</span><span class="sxs-lookup"><span data-stu-id="43cd2-116">A time slot is defined by using the following properties:</span></span>

- <span data-ttu-id="43cd2-117">**Piegādes veids** - norādiet piegādes saņemšanas veidu, uz kuru attiecas laika niša.</span><span class="sxs-lookup"><span data-stu-id="43cd2-117">**Mode of delivery** – Specify the pickup mode of delivery that the time slot applies to.</span></span>
- <span data-ttu-id="43cd2-118">**Minimālo dienu skaits** un **Maksimālo dienu skaits** - norādiet agrākos un vēlākos datumus, ko var atlasīt preču izsniegšanai attiecībā pret datumu, kad tiek veikts pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="43cd2-118">**Minimum Days** and **Maximum Days** – Specify the earliest and latest dates that can be selected for pickup relative to the date when the order is placed.</span></span> 

    <span data-ttu-id="43cd2-119">**Minimālo dienu skaits** rekvizīts nodrošina, ka ir pietiekami daudz laika, lai mazumtirgotājs varētu apstrādāt pasūtījumu, pirms tas ir gatavs saņemšanai.</span><span class="sxs-lookup"><span data-stu-id="43cd2-119">The **Minimum Days** property ensures that there is enough time for the retailer to process the order before it's ready for pickup.</span></span> <span data-ttu-id="43cd2-120">**Maksimālo dienu skaits** rekvizīts nodrošina, ka lietotājs nevar atlasīt datumu, kas ir pārāk tālu nākotnē.</span><span class="sxs-lookup"><span data-stu-id="43cd2-120">The **Maximum Days** property ensures that the user can't select a date that is too far in the future.</span></span> <span data-ttu-id="43cd2-121">Piemēram, ja minimālā vērtība ir iestatīta uz **1** un pasūtījums tiek veikts 20. septembrī, agrākā diena, kad pasūtījums būs pieejams savākšanai, ir nākamā piemērotā diena (21. septembris).</span><span class="sxs-lookup"><span data-stu-id="43cd2-121">For example, if the minimum value is set to **1**, and an order is placed on September 20, the earliest day that the order will be available for pickup is the next eligible day (September 21).</span></span> <span data-ttu-id="43cd2-122">Līdzīgi, iestatot maksimālo vērtību, varat definēt maksimālo dienu skaitu, kad var saņemt pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="43cd2-122">In a similar way, by setting a maximum value, you can define the maximum number of days that an order can be picked up.</span></span> <span data-ttu-id="43cd2-123">Kad minimālās un maksimālās vērtības ir definētas, vietnes lietotāji var redzēt un atlasīt tikai noteiktu dienu kopu norēķināšanās laikā.</span><span class="sxs-lookup"><span data-stu-id="43cd2-123">When minimum and maximum values are defined, site users can see and select only a specific set of days during their checkout experience.</span></span>

    <span data-ttu-id="43cd2-124">Minimālo vērtību var iestatīt uz decimālu vērtību, kas ir mazāka par 1.</span><span class="sxs-lookup"><span data-stu-id="43cd2-124">You can set the minimum value to a decimal value that is less than 1.</span></span> <span data-ttu-id="43cd2-125">Piemēram, ja paņemšana ir pieejama četras stundas pēc pasūtījuma veikšanas, iestatiet minimālo vērtību uz **0,17** (= 4 ÷ 24, noapaļojot līdz divām decimāldaļām).</span><span class="sxs-lookup"><span data-stu-id="43cd2-125">For example, if pickup is available four hours after an order is placed, set the minimum value to **0.17** (= 4 ÷ 24, rounded up to two decimal places).</span></span> <span data-ttu-id="43cd2-126">Tomēr, ja iestatāt minimālo vērtību uz decimālu vērtību, kas ir lielāka par 1, tā vienmēr tiek noapaļota uz tuvāko veselo skaitli.</span><span class="sxs-lookup"><span data-stu-id="43cd2-126">However, if you set the minimum value to a decimal value that is more than 1, it's always rounded up to the nearest whole number.</span></span> <span data-ttu-id="43cd2-127">Piemēram, vērtība **1,2** tiks noapaļota uz **2**.</span><span class="sxs-lookup"><span data-stu-id="43cd2-127">For example, a value of **1.2** will be rounded up to **2**.</span></span> <span data-ttu-id="43cd2-128">Līdzīgi, ja iestatāt maksimālo vērtību uz decimālu vērtību, tā vienmēr tiek noapaļota uz tuvāko veselo skaitli.</span><span class="sxs-lookup"><span data-stu-id="43cd2-128">Similarly, if you set the maximum value to a decimal value, it's always rounded up to the nearest whole number.</span></span> 

- <span data-ttu-id="43cd2-129">**Sākuma datums** un **Beigu datums** - norādiet laika nišas sākuma un beigu datumus.</span><span class="sxs-lookup"><span data-stu-id="43cd2-129">**Start Date** and **End Date** – Specify the start and end dates of the time slot.</span></span> <span data-ttu-id="43cd2-130">Katram laika nišas ierakstam ir sākuma datums un beigu datums.</span><span class="sxs-lookup"><span data-stu-id="43cd2-130">Each time slot entry has a start date and an end date.</span></span> <span data-ttu-id="43cd2-131">Tāpēc varat brīvi pievienot dažādas laika nišas visu gadu (piemēram, saņemšanu svētku laikā).</span><span class="sxs-lookup"><span data-stu-id="43cd2-131">Therefore, you have the flexibility to add different time slots throughout the year (for example, pickups during holiday hours).</span></span> <span data-ttu-id="43cd2-132">Ja laika nišas sākuma un beigu datumi tiek mainīti pēc tam, kad pasūtījums ir ticis veikts, izmaiņas netiek piemērotas šim pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="43cd2-132">If a time slot's start and dates are changed after an order is placed, the changes won't apply to that order.</span></span> <span data-ttu-id="43cd2-133">Definējot sākuma un beigu datumus, ir jāņem vērā veikala slēgšanas datumi (piemēram, Ziemassvētku diena) un jānodrošina, ka laika nišas nav definētas šīm dienām.</span><span class="sxs-lookup"><span data-stu-id="43cd2-133">When you define start and end dates, you must consider store closure dates (for example, Christmas day) and ensure that time slots aren't defined for those days.</span></span>
- <span data-ttu-id="43cd2-134">**Aktīvās saņemšanas stundas** - norādiet periodu, kad ir atļauta saņemšana.</span><span class="sxs-lookup"><span data-stu-id="43cd2-134">**Active Hours of Pickup** – Specify the period when pickup is allowed.</span></span> <span data-ttu-id="43cd2-135">Piemēram, saņemšanas laiki varētu būt no plkst. 14.00 līdz 17.00 katru dienu.</span><span class="sxs-lookup"><span data-stu-id="43cd2-135">For example, the pickup times might be between 2 PM and 5 PM every day.</span></span> <span data-ttu-id="43cd2-136">Šis rekvizīts ļauj saņemšanas laikiem būt neatkarīgiem no veikala darba laika.</span><span class="sxs-lookup"><span data-stu-id="43cd2-136">This property enables the pickup times to be independent of store hours.</span></span> <span data-ttu-id="43cd2-137">Tāpēc mazumtirgotājs var konfigurēt saņemšanas laikus, kas atbilst tā īpašajām biznesa prasībām.</span><span class="sxs-lookup"><span data-stu-id="43cd2-137">Therefore, the retailer can configure pickup times that meet its specific business requirements.</span></span> <span data-ttu-id="43cd2-138">Definējot aktīvās preču saņemšanas stundas, ir jāapsver veikala darba laiks un jānodrošina, ka saņemšanas laiki nav definēti laikos, kad veikals ir slēgts.</span><span class="sxs-lookup"><span data-stu-id="43cd2-138">When you define the active hours of pickup, you must consider store hours and ensure that pickup times aren't defined for times when the store is closed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="43cd2-139">Veikala preču saņemšanas darba laiks ir jādefinē attiecīgā veikala darba laikā..</span><span class="sxs-lookup"><span data-stu-id="43cd2-139">The hours for store pickup must be defined in the time zone of the appropriate store.</span></span>

- <span data-ttu-id="43cd2-140">**Laika nišas intervāls**- norādiet ilgumu, ko var piešķirt katrai laika nišai.</span><span class="sxs-lookup"><span data-stu-id="43cd2-140">**Time Slot Interval** – Specify the duration that can be allotted to each time slot.</span></span> <span data-ttu-id="43cd2-141">Piemēram, katras laika nišas ilgums var būt 15 minūtes, 30 minūtes vai viena stunda.</span><span class="sxs-lookup"><span data-stu-id="43cd2-141">For example, the duration of each time slot might be in increments of 15 minutes, 30 minutes, or one hour.</span></span> <span data-ttu-id="43cd2-142">Ja laika nišas vērtība ir 0, laika niša ir pieejama visam laikam starp sākuma un beigu laiku.</span><span class="sxs-lookup"><span data-stu-id="43cd2-142">If time slot value is 0, the time slot is available for the entire duration between the start and end time.</span></span>
- <span data-ttu-id="43cd2-143">**Laika nišas pa intervāliem** - norādiet klientu vai pasūtījumu skaitu, kurus var apkalpot saņemšanai katrā laika nišā.</span><span class="sxs-lookup"><span data-stu-id="43cd2-143">**Slots Per Interval** – Specify the number of customer or orders that can be served for pickup during each time slot interval.</span></span> <span data-ttu-id="43cd2-144">Piemēram, ievadiet **1**, **2**, **3** vai jebkuru citu veselu skaitli.</span><span class="sxs-lookup"><span data-stu-id="43cd2-144">For example, enter **1**, **2**, **3**, or any other whole number.</span></span>
- <span data-ttu-id="43cd2-145">**Aktīvās dienas** - norādiet nedēļas dienas, kad saņemšanas laika nišas ir aktīvas.</span><span class="sxs-lookup"><span data-stu-id="43cd2-145">**Active Days** – Specify the days of the week when the pickup time slots are active.</span></span> <span data-ttu-id="43cd2-146">Šis rekvizīts ļauj mazumtirgotājam noteikt dienas, kad tas vēlas atbalstīt saņemšanas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="43cd2-146">This property lets the retailer define the days when it wants to support pickup orders.</span></span>
- <span data-ttu-id="43cd2-147">**Mazumtirdzniecības kanāli** - norādiet mazumtirdzniecības kanālus.</span><span class="sxs-lookup"><span data-stu-id="43cd2-147">**Retail Channels** – Specify the retail channels.</span></span> <span data-ttu-id="43cd2-148">Katru laika nišu var saistīt ar vienu vai vairākiem mazumtirdzniecības veikaliem.</span><span class="sxs-lookup"><span data-stu-id="43cd2-148">Each time slot can be associated with one or more retail stores.</span></span> <span data-ttu-id="43cd2-149">Atkarībā no katra veikala darbības laika, var izveidot vienu vai vairākus laika nišas ierakstus un saistīt tos ar kanālu.</span><span class="sxs-lookup"><span data-stu-id="43cd2-149">Depending on each store's hours of operation, one or more time slot entries can be created and associated with a channel.</span></span> 

<!-- ![HQ Timeslot overview](../dev-itpro/media/Curbside_timeslot_Settings_overview.PNG) -->

<span data-ttu-id="43cd2-150">Katram kanālam var konfigurēt tikai vienu laika nišas veidni.</span><span class="sxs-lookup"><span data-stu-id="43cd2-150">Only one time slot template can be configured per channel.</span></span> <span data-ttu-id="43cd2-151">Šie kanāli ietver fiziskus veikalus, zvanu centrus, mobilās ierīces un e-komercijas vietnes.</span><span class="sxs-lookup"><span data-stu-id="43cd2-151">These channels include brick-and-mortar stores, call centers, mobile devices, and e-Commerce sites.</span></span>

## <a name="configure-the-time-slot-feature-in-commerce-headquarters"></a><span data-ttu-id="43cd2-152">Laika nišas līdzekļa konfigurēšana Commerce Headquarters</span><span class="sxs-lookup"><span data-stu-id="43cd2-152">Configure the time slot feature in Commerce headquarters</span></span>

<span data-ttu-id="43cd2-153">Laika nišas ir jādefinē katram saņemšanas veidam Commerce Headquarters, tādējādi pārdošanas punkts (POS) un e-tirdzniecības kanāli var atsaukties uz tiem.</span><span class="sxs-lookup"><span data-stu-id="43cd2-153">Time slots must be defined for each pickup mode of delivery in Commerce headquarters, so that point of sale (POS) and e-commerce channels can reference them.</span></span>

- <span data-ttu-id="43cd2-154">Ar katru veikalu vai kanālu var saistīt tikai vienu laika nišas veidni.</span><span class="sxs-lookup"><span data-stu-id="43cd2-154">Only one time slot template can be associated with each store or channel.</span></span>
- <span data-ttu-id="43cd2-155">Katrai izveidotajai laika nišai veidnē ir jābūt unikālam piegādes veidam.</span><span class="sxs-lookup"><span data-stu-id="43cd2-155">Each time slot that is created should be unique to each delivery mode in each template.</span></span>
- <span data-ttu-id="43cd2-156">Pēc laika nišas līdzekļa konfigurēšanas laika nišu kalendārs būs pieejams atlasītajiem veikaliem vai veikalu grupām.</span><span class="sxs-lookup"><span data-stu-id="43cd2-156">After the time slot feature is configured, the time slot calendar will be available to the selected stores or store groups.</span></span> <span data-ttu-id="43cd2-157">Atsaucei tas būs redzams arī POS sistēmā.</span><span class="sxs-lookup"><span data-stu-id="43cd2-157">It will also be visible at the POS, for reference.</span></span>

<span data-ttu-id="43cd2-158">Lai konfigurētu laika nišu līdzekli Commerce Headquarters, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="43cd2-158">To configure the time slot feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="43cd2-159">Doties uz **Commerce** \> **Kanāla uzstādīšana** \> **Veikala preču saņemšanas laika niša**.</span><span class="sxs-lookup"><span data-stu-id="43cd2-159">Go to **Commerce** \> **Channel setup** \> **Store pickup time slot**.</span></span>
1. <span data-ttu-id="43cd2-160">Atlasiet **Jauns**, lai izveidotu jaunu laika nišas veidni.</span><span class="sxs-lookup"><span data-stu-id="43cd2-160">Select **New** to create a new time slot template.</span></span> <span data-ttu-id="43cd2-161">Lai izmantotu esošu veidni, atlasiet veidni kreisajā rūtī.</span><span class="sxs-lookup"><span data-stu-id="43cd2-161">To use an existing template, select the template in the left pane.</span></span>
1. <span data-ttu-id="43cd2-162">Ievadiet vērtības laukos **Laika nišas ID** un **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="43cd2-162">Enter values in the **Time Slot ID** and **Description** fields.</span></span>
1. <span data-ttu-id="43cd2-163">Kopsavilkuma cilnē **Pasūtījuma saņemšana - Laika iestatījumi** atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="43cd2-163">On the **Order Pickup - Time Settings** FastTab, select **Add**.</span></span>
1. <span data-ttu-id="43cd2-164">Dialoglodziņā **Pasūtījuma saņemšana - laika iestatījumi** definējiet datumu diapazonu, piegādes veidu, aktīvās piegādes stundas, aktīvās dienas, laika nišas intervālu, laika nišas pa intervāliem un citus iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="43cd2-164">In the **Order Pickup - Time Settings** dialog box, define the date range, mode of delivery, active hours of delivery, active days, time slot interval, slots per interval, and other settings.</span></span>

    <span data-ttu-id="43cd2-165">Ja laika nišas tuvākajā nākotnē būs statiskas, iestatiet lauku **Beigu datums** uz **Nekad**.</span><span class="sxs-lookup"><span data-stu-id="43cd2-165">If time slots will be static for the foreseeable future, set the **End Date** field to **Never**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="43cd2-166">Varat izveidot vairākas veidnes, bet tikai vienu veidni var saistīt ar vienu kanālu vai veikalu.</span><span class="sxs-lookup"><span data-stu-id="43cd2-166">You can create multiple templates, but only one template can be associated with a single channel or store.</span></span>

    ![Pasūtījuma saņemšana - laika iestatījumu dialoglodziņš](../dev-itpro/media/Curbside_timeslot_Settings_Page.PNG)

1. <span data-ttu-id="43cd2-168">Pēc pabeigšanas atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="43cd2-168">When you've finished, select **OK**.</span></span>
1. <span data-ttu-id="43cd2-169">Ja laika nišas dienā atšķirsies, izveidojiet papildu ierakstus kopsavilkuma cilnē **Pasūtījuma saņemšana - laika iestatījumi**, lai nodrošinātu, ka datumi un laiki nepārklājas.</span><span class="sxs-lookup"><span data-stu-id="43cd2-169">If the time slots in a day will vary, create additional entries on the **Order Pickup - Time Settings** FastTab to ensure that the dates and times don't overlap.</span></span>
1. <span data-ttu-id="43cd2-170">Kopsavilkuma cilnē **Mazumtirdzniecības kanāli** atlasiet **Pievienot**, lai saistītu laika nišas veidni ar veikaliem vai kanāliem, kuros tas tiks izmantots.</span><span class="sxs-lookup"><span data-stu-id="43cd2-170">On the **Retail Channels** FastTab, select **Add** to associate the time slot template with the stores or channels where it will be used.</span></span>
1. <span data-ttu-id="43cd2-171">Dialoglodziņā **Izvēlēties organizācijas mezglus**, izmantojiet bultiņu pogas, lai atlasītu (vai notīrītu izvēli) veikalus, reģionus un organizācijas, ar kurām veidne jāsaista.</span><span class="sxs-lookup"><span data-stu-id="43cd2-171">In the **Choose organization nodes** dialog box, use the arrow buttons to select (or clear the selection of) the stores, regions, and organizations that the template should be associated with.</span></span>

    <!-- ![HQ Timeslot overview](../dev-itpro/media/Curbside_timeslot_Settings_overview.PNG) -->

1. <span data-ttu-id="43cd2-172">Pēc pabeigšanas atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="43cd2-172">When you've finished, select **OK**.</span></span>
1. <span data-ttu-id="43cd2-173">Lapā **Sadales grafiks** palaidiet darbus **1070** un **1135**, lai sinhronizētu datus ar kanāliem.</span><span class="sxs-lookup"><span data-stu-id="43cd2-173">On the **Distribution schedule** page, run the **1070** and **1135** jobs to sync the data to the channels.</span></span>

## <a name="time-slot-selection-for-pos-orders"></a><span data-ttu-id="43cd2-174">Laika nišas atlase POS pasūtījumiem</span><span class="sxs-lookup"><span data-stu-id="43cd2-174">Time slot selection for POS orders</span></span>

<span data-ttu-id="43cd2-175">Kad pasūtījuma vai pasūtījuma rinda ir identificēta izsniegšanai POS sistēmā, kasieris var izvēlēties saņemšanas veikalu vai vietu un datumu un laika nišu.</span><span class="sxs-lookup"><span data-stu-id="43cd2-175">At the POS, when an order or order line is identified for pickup, the cashier can select the pickup store or location, and a date and time slot.</span></span> <span data-ttu-id="43cd2-176">Ja klientam ir paņemšanas pasūtījums citam veikalam, kasieris var izvēlēties datumus, kad paņemšana būs pieejama šajā veikalā.</span><span class="sxs-lookup"><span data-stu-id="43cd2-176">If a customer has a pickup order for a different store, the cashier can select dates when the pickup will be available in that store.</span></span> <span data-ttu-id="43cd2-177">Veikala uzmeklēšanā tiks sniegta atsauce uz datumiem un veikalu laikiem.</span><span class="sxs-lookup"><span data-stu-id="43cd2-177">The store lookup will provide a reference to the dates and store times.</span></span>

<span data-ttu-id="43cd2-178">Sekojošajā attēlā parādīts laika nišu atlases piemērs POS pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="43cd2-178">The following illustration shows an example of time slot selection for a POS order.</span></span>

![Laika nišu atlases piemērs POS pasūtījumam](../dev-itpro/media/Curbside_timeslot_POS.png)

## <a name="time-slot-selection-for-e-commerce-orders"></a><span data-ttu-id="43cd2-180">Laika nišu atlase e-tirdzniecības pasūtījumiem</span><span class="sxs-lookup"><span data-stu-id="43cd2-180">Time slot selection for e-commerce orders</span></span>

<span data-ttu-id="43cd2-181">Informāciju par to, kā veikt laika nišu atlasi e-tirdzniecības pasūtījumiem, skatiet [Saņemšanas informācijas modulis](../pickup-info-module.md).</span><span class="sxs-lookup"><span data-stu-id="43cd2-181">For information about how to make time slot selection available for e-commerce orders, see [Pickup information module](../pickup-info-module.md).</span></span>

> [!NOTE]
> <span data-ttu-id="43cd2-182">Lietotāji var skatīt vai rediģēt saņemšanas laika nišas Commerce vietnes izrakstīšanās lapā tikai tad, ja saņemšanas informācijas modulis ir pievienots šai lapai.</span><span class="sxs-lookup"><span data-stu-id="43cd2-182">Users can view or edit pickup time slots on a Commerce site's checkout page only if the pickup information module has been added to that page.</span></span> <span data-ttu-id="43cd2-183">Ja izrakstīšanās lapā nav ietverts saņemšanas informācijas modulis, pasūtījumi tiks izveidoti, neļaujot lietotājiem norādīt vai skatīt laika nišas informāciju.</span><span class="sxs-lookup"><span data-stu-id="43cd2-183">If the checkout page doesn't include the pickup information module, orders will be placed without letting users specify or view time slot information.</span></span>

<span data-ttu-id="43cd2-184">Sekojošajā attēlā redzams e-tirdzniecības pasūtījuma piemērs, kurā ir izvēlēta saņemšanas laika niša.</span><span class="sxs-lookup"><span data-stu-id="43cd2-184">The following illustration shows an example of an e-commerce order where a pickup time slot has been selected.</span></span>

![E-tirdzniecības pasūtījuma piemērs, kurā ir izvēlēta saņemšanas laika niša](../dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="time-slot-selection-for-call-center-orders"></a><span data-ttu-id="43cd2-186">Laika nišu atlase zvanu centra pasūtījumiem</span><span class="sxs-lookup"><span data-stu-id="43cd2-186">Time slot selection for call center orders</span></span>

<span data-ttu-id="43cd2-187">Zvanu centra programmā zvanu centra aģenti var atlasīt saņemšanas veikalu vai atrašanās vietu, kā arī datuma un laika nišu, kā parādīts šajā ilustrācijā.</span><span class="sxs-lookup"><span data-stu-id="43cd2-187">In the call center app, call center agents can select the pickup store or location, as well as a date and time slot as highlighted in the following illustration.</span></span>

![Zvanu centra pasūtījuma piemērs, kurā ir izvēlēta saņemšanas laika niša](../dev-itpro/media/Curbside_timeslot_callcenter.png)

## <a name="additional-resources"></a><span data-ttu-id="43cd2-189">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="43cd2-189">Additional resources</span></span>

[<span data-ttu-id="43cd2-190">Saņemšanas informācijas modulis</span><span class="sxs-lookup"><span data-stu-id="43cd2-190">Pickup information module</span></span>](../pickup-info-module.md)