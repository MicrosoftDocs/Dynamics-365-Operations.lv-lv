---
title: Papildināšanas metodes un daudzuma modificēšana
description: Šajā tēmā ir sniegta informācija par papildināšanas metodēm un Plānošanas optimizāciju. Tajā skaidrots arī, kā preces vairāku pasūtījumu daudzums ietekmē rezultātu.
author: crytt
ms.date: 6/1/2021
ms.topic: article
ms.search.form: ReqGroup, ReqItemTable, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d5e0e671e624de2646a47647ef08d3567599b884
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261700"
---
# <a name="replenishment-methods-and-quantity-modification"></a><span data-ttu-id="1df20-104">Papildināšanas metodes un daudzuma modificēšana</span><span class="sxs-lookup"><span data-stu-id="1df20-104">Replenishment methods and quantity modification</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1df20-105">Šajā tēmā ir sniegta informācija par papildināšanas metodēm un Plānošanas optimizāciju.</span><span class="sxs-lookup"><span data-stu-id="1df20-105">This topic provides information about replenishment methods in Planning Optimization.</span></span> <span data-ttu-id="1df20-106">Tajā skaidrots arī, kā preces vairāku pasūtījumu daudzums ietekmē rezultātu.</span><span class="sxs-lookup"><span data-stu-id="1df20-106">It also explains how the multiple order quantity for a product affects the result.</span></span>

<span data-ttu-id="1df20-107">Papildināšanas metodes pazīstamas arī kā pārklājuma metodes un laidiena izmēru metodes.</span><span class="sxs-lookup"><span data-stu-id="1df20-107">Replenishment methods are also known as coverage methods and lot-sizing methods.</span></span>

## <a name="coverage-codes"></a><span data-ttu-id="1df20-108">Vajadzības kodi</span><span class="sxs-lookup"><span data-stu-id="1df20-108">Coverage codes</span></span>

<span data-ttu-id="1df20-109">Plānošanas optimizāciju var konfigurēt tā, lai izmantotu dažādas papildināšanas metodes.</span><span class="sxs-lookup"><span data-stu-id="1df20-109">Planning Optimization can be configured to use different replenishment methods.</span></span> <span data-ttu-id="1df20-110">Papildināšanas metodes ir metodes, ko sistēma izmanto, lai aprēķinātu preces prasības.</span><span class="sxs-lookup"><span data-stu-id="1df20-110">The replenishment methods are the techniques that the system uses to calculate requirements for a product.</span></span> <span data-ttu-id="1df20-111">Papildināšanas metodes tiek definētas pēc vajadzības kodiem, kurus var iestatīt vajadzību grupai vai precei.</span><span class="sxs-lookup"><span data-stu-id="1df20-111">Replenishment methods are defined by coverage codes that you can set up on either the coverage group or the product.</span></span>

<span data-ttu-id="1df20-112">Šie vajadzību kodi var tikt izmantoti Plānošanas optimizācijā:</span><span class="sxs-lookup"><span data-stu-id="1df20-112">The following coverage codes can be used in Planning Optimization:</span></span>

- <span data-ttu-id="1df20-113">**Periods** – papildināšanas metode, kas apvieno visu perioda pieprasījumu vienā pasūtījumā šai precei.</span><span class="sxs-lookup"><span data-stu-id="1df20-113">**Period** – The replenishment method combines all the demand for a period into one order for the product.</span></span> <span data-ttu-id="1df20-114">Pasūtījums tiks plānots pirmajai perioda dienai, un tā daudzums atbilstīs neto prasībām noteiktajā periodā.</span><span class="sxs-lookup"><span data-stu-id="1df20-114">The order will be planned for the first day of the period, and its quantity will fulfill the net requirements during the established period.</span></span> <span data-ttu-id="1df20-115">Periods sākas ar preces pirmo pieprasījumu un sedz noteikto laika periodu.</span><span class="sxs-lookup"><span data-stu-id="1df20-115">The period starts with the first demand of the product and covers the defined length of time.</span></span> <span data-ttu-id="1df20-116">Nākamais periods sāksies ar nākamās preces prasībām.</span><span class="sxs-lookup"><span data-stu-id="1df20-116">The next period will start with the next requirements of the product.</span></span> <span data-ttu-id="1df20-117">Vajadzības kods *Periods* bieži tiek izmantots neprognozējamu krājumu izvelkšanai, sezonas ietekmējamām precēm vai augstas izmaksas precēm.</span><span class="sxs-lookup"><span data-stu-id="1df20-117">The *Period* coverage code is often used for non-predictable inventory draw, season-influenced products, or high-cost products.</span></span> <span data-ttu-id="1df20-118">Tālāk redzamajā attēlā parādīts piemērs.</span><span class="sxs-lookup"><span data-stu-id="1df20-118">The following illustration shows an example.</span></span>

    <span data-ttu-id="1df20-119">![Perioda vajadzības koda izmantošanas piemērs](./media/coverage-code-period.png "Perioda vajadzības koda izmantošanas piemērs")</span><span class="sxs-lookup"><span data-stu-id="1df20-119">![Example of Period coverage code use](./media/coverage-code-period.png "Example of Period coverage code use")</span></span>

- <span data-ttu-id="1df20-120">**Prasība** – papildināšanas metode, saskaņā ar kuru sistēma izveido plānoto pirkšanas, pārsūtīšanas vai ražošanas pasūtījumu preces prasību.</span><span class="sxs-lookup"><span data-stu-id="1df20-120">**Requirement** – In the replenishment method, the system creates a planned purchase, transfer, or production order per requirement for the product.</span></span> <span data-ttu-id="1df20-121">Šī metode tiek izmantota dārgam precēm, kam ir intermitējošs pieprasījums.</span><span class="sxs-lookup"><span data-stu-id="1df20-121">This method is used for expensive products that have intermittent demand.</span></span> <span data-ttu-id="1df20-122">Vajadzības kods *Prasība* bieži tiek izmantots konfigurējamām precēm vai pasūtījumā veidotiem scenārijiem.</span><span class="sxs-lookup"><span data-stu-id="1df20-122">The *Requirement* coverage code is often used for configurable products or make-to-order scenarios.</span></span> <span data-ttu-id="1df20-123">Tālāk redzamajā attēlā parādīts piemērs.</span><span class="sxs-lookup"><span data-stu-id="1df20-123">The following illustration shows an example.</span></span>

    <span data-ttu-id="1df20-124">![Prasības vajadzības koda izmantošanas piemērs](./media/coverage-code-requirement.png "Prasības vajadzības koda izmantošanas piemērs")</span><span class="sxs-lookup"><span data-stu-id="1df20-124">![Example of Requirement coverage code use](./media/coverage-code-requirement.png "Example of Requirement coverage code use")</span></span>

- <span data-ttu-id="1df20-125">**Min./maks.**</span><span class="sxs-lookup"><span data-stu-id="1df20-125">**Min./Max.**</span></span> <span data-ttu-id="1df20-126">– Papildināšanas metode ir balstīta uz krājumu līmeni.</span><span class="sxs-lookup"><span data-stu-id="1df20-126">– The replenishment method is based on the inventory level.</span></span> <span data-ttu-id="1df20-127">Tā definē krājumu papildināšanu līdz noteiktam līmenim, kad paredzamais rīcībā esošo krājumu līmenis ir zem noteikta sliekšņa.</span><span class="sxs-lookup"><span data-stu-id="1df20-127">It defines the replenishment of inventory up to a specific level when the predicted on-hand level is below a specific threshold.</span></span> <span data-ttu-id="1df20-128">Papildināšanas daudzums būs vienāds ar starpību starp maksimālo līmeni un prognozēto rīcībā esošo līmeni.</span><span class="sxs-lookup"><span data-stu-id="1df20-128">The replenishment quantity will be the difference between the maximum level and the predicted on-hand level.</span></span> <span data-ttu-id="1df20-129">Vienība *Min./maks.*</span><span class="sxs-lookup"><span data-stu-id="1df20-129">The *Min./Max.*</span></span> <span data-ttu-id="1df20-130">vajadzības kods bieži tiek izmantots paredzamu krājumu izvelkšanai, labākām precēm vai lētākām precēm.</span><span class="sxs-lookup"><span data-stu-id="1df20-130">coverage code is often used for predictable inventory draw, high runners, or less expensive products.</span></span> <span data-ttu-id="1df20-131">Tālāk redzamajā attēlā parādīts piemērs.</span><span class="sxs-lookup"><span data-stu-id="1df20-131">The following illustration shows an example.</span></span>

    <span data-ttu-id="1df20-132">![Min./Maks. vajadzības koda izmantošanas piemērs](./media/coverage-code-min-max.png "Min./Maks. vajadzības koda izmantošanas piemērs")</span><span class="sxs-lookup"><span data-stu-id="1df20-132">![Example of Min./Max. coverage code use](./media/coverage-code-min-max.png "Example of Min./Max. coverage code use")</span></span>

- <span data-ttu-id="1df20-133">**Manuāla** – papildināšanas metode, kad sistēma neiesaka precei pirkšanas, pārsūtīšanas vai ražošanas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="1df20-133">**Manual** – In the replenishment method, the system doesn't suggest purchase, transfer, or production orders for the product.</span></span> <span data-ttu-id="1df20-134">Tā vietā produkta plānotājs ir atbildīgs par nepieciešamo pasūtījumu izveidi preces papildināšanai.</span><span class="sxs-lookup"><span data-stu-id="1df20-134">Instead, the planner for the product is responsible for creating the required orders for the replenishment of the product.</span></span> <span data-ttu-id="1df20-135">Vajadzības kods *Manuāls* bieži tiek izmantots precēm, kurām nav vajadzīgi sistēmas ģenerētie plānotie pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="1df20-135">The *Manual* coverage code is often used for products that system-generated planned orders aren't wanted for.</span></span>

## <a name="impact-of-the-order-quantity-from-default-order-settings"></a><span data-ttu-id="1df20-136">Pasūtījuma daudzuma ietekme no noklusējuma pasūtījuma iestatījumiem</span><span class="sxs-lookup"><span data-stu-id="1df20-136">Impact of the order quantity from default order settings</span></span>

<span data-ttu-id="1df20-137">Izlaistai precei lapā **Noklusējuma pasūtījuma iestatījumi** varat norādīt katru no šiem daudzuma iestatījumiem kopsavilkuma cilnēs **Pirkšanas pasūtījums**, **Krājumi** un **Pārdošanas pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="1df20-137">On the **Default order setting** page for a released product, you can specify each of following quantity settings on the **Purchase order**, **Inventory**, and **Sales order** FastTabs.</span></span> <span data-ttu-id="1df20-138">(Kopsavilkuma cilne **Krājumi** tiek izmantota gan pārsūtīšanas, gan ražošanas pasūtījumiem.)</span><span class="sxs-lookup"><span data-stu-id="1df20-138">(The **Inventory** FastTab is used for both transfer orders and production orders.)</span></span>

- <span data-ttu-id="1df20-139">**Daudzkārtīgi** – plānotie pasūtījumi būs daudzkārtīgi no šī daudzuma.</span><span class="sxs-lookup"><span data-stu-id="1df20-139">**Multiple** – Planned orders will be a multiple of this quantity.</span></span>

    <span data-ttu-id="1df20-140">Piemēram, ja lauks **Daudzkārtīgi** ir iestatīts uz *5*, pasūtījums var būt ar daudzumu 5, 10, 15, 20 un tā tālāk.</span><span class="sxs-lookup"><span data-stu-id="1df20-140">For example, if the **Multiple** field is set to *5*, an order can be for a quantity of 5, 10, 15, 20, and so on.</span></span>

- <span data-ttu-id="1df20-141">**Min. pasūtījuma daudzums** – plānotie pasūtījumi nebūs mazāki par norādīto vērtību.</span><span class="sxs-lookup"><span data-stu-id="1df20-141">**Min. order quantity** – Planned orders won't be less than the specified value.</span></span>

    <span data-ttu-id="1df20-142">Piemēram, ja lauks **Min. pasūtījuma daudzums** ir iestatīts uz *10*, tiks izveidots plānotais pasūtījums daudzumam 10, pat ja pieprasījuma izpildei nepieciešami tikai četri.</span><span class="sxs-lookup"><span data-stu-id="1df20-142">For example, if the **Min. order quantity** field is set to *10*, a planned order for a quantity of 10 will be created, even if only four are required to fulfill the demand.</span></span>

- <span data-ttu-id="1df20-143">**Maks. pasūtījuma daudzums** – plānotie pasūtījumi nebūs lielāki par norādīto vērtību.</span><span class="sxs-lookup"><span data-stu-id="1df20-143">**Max. order quantity** – Planned orders won't exceed the specified value.</span></span> <span data-ttu-id="1df20-144">Ja pieprasījums ir lielāks nekā vērtība **Maks. pasūtījuma daudzums**, tiks izveidoti vairāki plānotie pasūtījumi, lai to nosegtu.</span><span class="sxs-lookup"><span data-stu-id="1df20-144">If the demand is more than the **Max. order quantity** value, multiple planned orders will be created to cover it.</span></span>

    <span data-ttu-id="1df20-145">Piemēram, ja lauks **Maks. pasūtījuma daudzums** ir iestatīts uz *100* un pieprasījums ir 450, tiks izveidoti četri plānotie pasūtījumi daudzumam 100 un viens plānotais pasūtījums daudzumam 50.</span><span class="sxs-lookup"><span data-stu-id="1df20-145">For example, if the **Max. order quantity** field is set to *100*, and the demand is 450, four planned orders for a quantity of 100 and one planned order for a quantity of 50 will be created.</span></span>

## <a name="examples-of-replenishment-that-use-the-minmax-coverage-code"></a><span data-ttu-id="1df20-146">Papildināšanas piemēri, kas izmanto Min./Maks.</span><span class="sxs-lookup"><span data-stu-id="1df20-146">Examples of replenishment that use the Min./Max.</span></span> <span data-ttu-id="1df20-147">vajadzības kods</span><span class="sxs-lookup"><span data-stu-id="1df20-147">coverage code</span></span>

<span data-ttu-id="1df20-148">Ja precei laukā **Daudzkārtīgi** nav norādīta vērtība lapā **Noklusējuma pasūtījuma iestatījumi** un ja izmantojat *Min./Max.*</span><span class="sxs-lookup"><span data-stu-id="1df20-148">If you don't specify a value in the **Multiple** field for a product on the **Default order setting** page, and if you're using the *Min./Max.*</span></span> <span data-ttu-id="1df20-149">papildināšanas metodi, Plānošanas optimizācija papildinās krājumus līdz noteiktam līmenim, kad paredzamais rīcībā esošo krājumu līmenis ir zem noteikta sliekšņa.</span><span class="sxs-lookup"><span data-stu-id="1df20-149">replenishment method, Planning Optimization will replenish the inventory up to a specific level when the predicted on-hand level is below a specific threshold.</span></span>

<span data-ttu-id="1df20-150">Ja precei definējat vairākus daudzumus, *Min./Maks.*</span><span class="sxs-lookup"><span data-stu-id="1df20-150">If you define a multiple quantity for a product, the *Min./Max.*</span></span> <span data-ttu-id="1df20-151">papildināšanas metode maina tās darbību un ņem vērā vērtību **Daudzkārtīgi**.</span><span class="sxs-lookup"><span data-stu-id="1df20-151">replenishment method changes its behavior and considers the **Multiple** value.</span></span>

<span data-ttu-id="1df20-152">Citiem vārdiem sakot, Plānošanas optimizācija joprojām papildinās krājumus līdz definētajam maksimālajam līmenim, ja prognozētais rīcībā esošo krājumu līmenis ir mazāks par noteikto minimālo līmeni.</span><span class="sxs-lookup"><span data-stu-id="1df20-152">In other words, Planning Optimization will still replenish the inventory up to the defined maximum level when the predicted on-hand level is less than the defined minimum level.</span></span> <span data-ttu-id="1df20-153">Tomēr papildināšanas daudzumam jābūt daudzkārtīgai vērtībai **Daudzkārtīgi**.</span><span class="sxs-lookup"><span data-stu-id="1df20-153">However, the replenishment quantity must be a multiple of the **Multiple** value.</span></span>

<span data-ttu-id="1df20-154">Ja papildināšanas daudzums (starpība starp maksimālo līmeni un prognozēto rīcībā esošo līmeni) nedalās ar definēto daudzkārtēju daudzumu, Plānošanas optimizācija izmanto pirmo iespējamo vērtību, kas kopā ar prognozēto rīcībā esošo līmeni būs zem maksimālā līmeņa.</span><span class="sxs-lookup"><span data-stu-id="1df20-154">If the replenishment quantity (the difference between the maximum level and the predicted on-hand level) isn't a multiple of the defined multiple quantity, Planning Optimization uses the first possible value that, together with predicted on-hand level, will be below the maximum level.</span></span> <span data-ttu-id="1df20-155">Ja summa ir mazāka par minimālo līmeni, Plānošanas optimizācija izmanto pirmo vērtību, kas kopā ar prognozējamu rīcībā esošo, būs virs maksimālā līmeņa.</span><span class="sxs-lookup"><span data-stu-id="1df20-155">If the sum is less than the minimum level, Planning Optimization uses the first value that, together with predicted on-hand, will be above the maximum level.</span></span>

<span data-ttu-id="1df20-156">Sekojošās apakšsadaļas sniedz dažus piemērus, kas parāda, kā daudzkārtēju pasūtījumu daudzums precei ietekmē rezultātu *Min./Max.*</span><span class="sxs-lookup"><span data-stu-id="1df20-156">The following subsections provide some examples that show how the multiple order quantity for a product affects the result of the *Min./Max.*</span></span> <span data-ttu-id="1df20-157">papildināšanas metode.</span><span class="sxs-lookup"><span data-stu-id="1df20-157">replenishment method.</span></span>

### <a name="example-1"></a><span data-ttu-id="1df20-158">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="1df20-158">Example 1</span></span>

<span data-ttu-id="1df20-159">Precei ir šāda konfigurācija:</span><span class="sxs-lookup"><span data-stu-id="1df20-159">A product has the following configuration:</span></span>

- <span data-ttu-id="1df20-160">**Vajadzību kods:** *Min./Max.*</span><span class="sxs-lookup"><span data-stu-id="1df20-160">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="1df20-161">**Minimums:** *15*</span><span class="sxs-lookup"><span data-stu-id="1df20-161">**Minimum:** *15*</span></span>
- <span data-ttu-id="1df20-162">**Maksimums:** *22*</span><span class="sxs-lookup"><span data-stu-id="1df20-162">**Maximum:** *22*</span></span>
- <span data-ttu-id="1df20-163">**Daudzkārtīgi:** *0*</span><span class="sxs-lookup"><span data-stu-id="1df20-163">**Multiple:** *0*</span></span>

<span data-ttu-id="1df20-164">Precei ir 10 rīcībā esošo krājumu vienības, un nav cita pieprasījuma vai piedāvājuma.</span><span class="sxs-lookup"><span data-stu-id="1df20-164">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="1df20-165">Kad tiek palaista vispārējā plānošana, tiek izveidots plānotais pasūtījums 12 gabaliem, lai papildinātu krājumus līdz maksimālām daudzumam.</span><span class="sxs-lookup"><span data-stu-id="1df20-165">When master planning runs, a planned order for 12 pieces is created to replenish inventory to the maximum quantity.</span></span>

### <a name="example-2"></a><span data-ttu-id="1df20-166">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="1df20-166">Example 2</span></span>

<span data-ttu-id="1df20-167">Precei ir šāda konfigurācija:</span><span class="sxs-lookup"><span data-stu-id="1df20-167">A product has the following configuration:</span></span>

- <span data-ttu-id="1df20-168">**Vajadzību kods:** *Min./Max.*</span><span class="sxs-lookup"><span data-stu-id="1df20-168">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="1df20-169">**Minimums:** *15*</span><span class="sxs-lookup"><span data-stu-id="1df20-169">**Minimum:** *15*</span></span>
- <span data-ttu-id="1df20-170">**Maksimums:** *22*</span><span class="sxs-lookup"><span data-stu-id="1df20-170">**Maximum:** *22*</span></span>
- <span data-ttu-id="1df20-171">**Daudzkārtīgi:** *5*</span><span class="sxs-lookup"><span data-stu-id="1df20-171">**Multiple:** *5*</span></span>

<span data-ttu-id="1df20-172">Precei ir 10 rīcībā esošo krājumu vienības, un nav cita pieprasījuma vai piedāvājuma.</span><span class="sxs-lookup"><span data-stu-id="1df20-172">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="1df20-173">Kad tiek palaista vispārējā plānošana, tiek izveidots plānotais pasūtījums 10 gabaliem (jo 15 papildināšanas gabali plus 10 rīcībā esošo krājumu vienības pārsniegs maksimālo daudzumu).</span><span class="sxs-lookup"><span data-stu-id="1df20-173">When master planning runs, a planned order for 10 pieces is created (because 15 pieces of replenishment plus 10 pieces of on-hand inventory will exceed the maximum quantity).</span></span>

### <a name="example-3"></a><span data-ttu-id="1df20-174">3. piemērs</span><span class="sxs-lookup"><span data-stu-id="1df20-174">Example 3</span></span>

<span data-ttu-id="1df20-175">Precei ir šāda konfigurācija:</span><span class="sxs-lookup"><span data-stu-id="1df20-175">A product has the following configuration:</span></span>

- <span data-ttu-id="1df20-176">**Vajadzību kods:** *Min./Max.*</span><span class="sxs-lookup"><span data-stu-id="1df20-176">**Coverage code:** *Min./Max.*</span></span>
- <span data-ttu-id="1df20-177">**Minimums:** *21*</span><span class="sxs-lookup"><span data-stu-id="1df20-177">**Minimum:** *21*</span></span>
- <span data-ttu-id="1df20-178">**Maksimums:** *24*</span><span class="sxs-lookup"><span data-stu-id="1df20-178">**Maximum:** *24*</span></span>
- <span data-ttu-id="1df20-179">**Daudzkārtīgi:** *5*</span><span class="sxs-lookup"><span data-stu-id="1df20-179">**Multiple:** *5*</span></span>

<span data-ttu-id="1df20-180">Precei ir 10 rīcībā esošo krājumu vienības, un nav cita pieprasījuma vai piedāvājuma.</span><span class="sxs-lookup"><span data-stu-id="1df20-180">There are 10 pieces of on-hand inventory for the product, and there is no other demand or supply.</span></span>

<span data-ttu-id="1df20-181">Kad tiek palaista vispārējā plānošana, tiek izveidots plānotais pasūtījums 15 gabaliem (jo 10 papildināšanas gabali plus 10 rīcībā esošo krājumu vienības nesasniegs minimālo daudzumu).</span><span class="sxs-lookup"><span data-stu-id="1df20-181">When master planning runs, the planned order for 15 pieces is created (because 10 pieces of replenishment plus 10 pieces of on-hand inventory will be less than the minimum quantity).</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
