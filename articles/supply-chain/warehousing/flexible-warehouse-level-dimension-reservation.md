---
title: Elastīga noliktavas līmeņa dimensiju rezervāēšanas politika
description: Šajā tēmā ir aprakstīta krājumu rezervēšanas politika, kas ļauj uzņēmumiem, kuri pārdod pēc partijas izsekotās preces un nodrošina savu loģistiku kā WMS darbības, rezervēt konkrētas partijas debitoru veiktiem pārdošanas pasūtījumiem pat tad, ja rezervāciju hierarhiju, kas ir kas saistīta ar precēm, nevar izmantot īpašu partiju rezervācijai.
author: omulvad
manager: tfehr
ms.date: 02/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2020-01-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 6c462a87494c434a6047542d448a85b3bce9f769
ms.sourcegitcommit: ffd845d4230646499b6f074cb43e69ab95787671
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2020
ms.locfileid: "3346472"
---
# <a name="flexible-warehouse-level-dimension-reservation-policy"></a><span data-ttu-id="215cf-103">Elastīga noliktavas līmeņa dimensiju rezervāēšanas politika</span><span class="sxs-lookup"><span data-stu-id="215cf-103">Flexible warehouse-level dimension reservation policy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="215cf-104">Ja "Partijas lejpusēja\[novietojuma\]" tipa krājumu rezervēšanas hierarhija ir saistīta ar precēm, tad uzņēmumi, kuri pārdod pēc partijas izsekotās preces un nodrošina savu loģistiku kā operācijas, kas ir iespējotas Microsoft Dynamics 365 noliktavas vadības sistēmai (WMS), nevar rezervēt konkrētas šo preču partijas debitoru veiktiem pārdošanas pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="215cf-104">When an inventory reservation hierarchy of the "Batch-below\[location\]" type is associated with products, businesses that sell batch-tracked products and run their logistics as operations that are enabled for the Microsoft Dynamics 365 Warehouse Management System (WMS) can't reserve specific batches of those products for customer sales orders.</span></span> <span data-ttu-id="215cf-105">Šajā tēmā aprakstīta krājumu rezervēšanas politika, kas ļauj šiem uzņēmumiem rezervēt noteiktas partijas pat tad, ja preces ir saistītas ar rezervāciju hierarhiju "Partijas lejpusējs\[—\]novietojums".</span><span class="sxs-lookup"><span data-stu-id="215cf-105">This topic describes the inventory reservation policy that lets these businesses reserve specific batches, even when the products are associated with a "Batch-below\[location\]" reservation hierarchy.</span></span>

## <a name="inventory-reservation-hierarchy"></a><span data-ttu-id="215cf-106">Krājumu rezervāciju hierarhija</span><span class="sxs-lookup"><span data-stu-id="215cf-106">Inventory reservation hierarchy</span></span>

<span data-ttu-id="215cf-107">Šajā sadaļā ir apkopota esošā krājumu rezervāciju hierarhija.</span><span class="sxs-lookup"><span data-stu-id="215cf-107">This section summarizes the existing inventory reservation hierarchy.</span></span> <span data-ttu-id="215cf-108">Galvenā uzmanība ir pievērsta veidam, kādā tiek apkalpoti pēc partijas izsekotie un pēc sērijas izsekotie krājumi.</span><span class="sxs-lookup"><span data-stu-id="215cf-108">It focuses on the way that batch-tracked and serial-tracked items are handled.</span></span>

<span data-ttu-id="215cf-109">Krājumu rezervēšanas hierarhija nosaka, ka attiecībā uz noliktavas dimensijām pieprasījuma pasūtījumā ir iekļautas vietas, noliktavas un krājumu statusa obligātās dimensijas, bet noliktavas loģika ir atbildīga par atrašanās vietas piešķiršanu pieprasītajiem daudzumiem un vietas rezervēšanu.</span><span class="sxs-lookup"><span data-stu-id="215cf-109">The inventory reservation hierarchy dictates that, as far as storage dimensions are concerned, the demand order carries the mandatory dimensions of site, warehouse, and inventory status, whereas the warehouse logic is responsible for assigning a location to the requested quantities and reserving the location.</span></span> <span data-ttu-id="215cf-110">Citiem vārdiem sakot, mijiedarbojoties pieprasījuma pasūtījuma un noliktavas operācijām, pieprasījuma pasūtījumā vajadzētu norādīt, kur pasūtījums ir jānosūta (proti, uz kādu vietu un noliktavu).</span><span class="sxs-lookup"><span data-stu-id="215cf-110">In other words, in the interactions between the demand order and the warehouse operations, the demand order is expected to indicate where the order must be shipped from (that is, what site and warehouse).</span></span> <span data-ttu-id="215cf-111">Pēc tam noliktava paļaujas uz savu loģiku, lai atrastu nepieciešamo daudzumu noliktavas telpās.</span><span class="sxs-lookup"><span data-stu-id="215cf-111">The warehouse then relies on its logic to find the required quantity in the warehouse premises.</span></span>

<span data-ttu-id="215cf-112">Tomēr, lai atspoguļotu biznesa darbības modeli, izsekošanas dimensijām (partijas un sērijas numuri) tiek piemērota lielāka elastība.</span><span class="sxs-lookup"><span data-stu-id="215cf-112">However, to reflect the operational model of the business, tracking dimensions (batch and serial numbers) are subject to more flexibility.</span></span> <span data-ttu-id="215cf-113">Krājumu rezervēšanas hierarhija var ietvert scenārijus, kuros ir spēkā tālāk norādītie nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="215cf-113">An inventory reservation hierarchy can accommodate scenarios where the following conditions apply:</span></span>

- <span data-ttu-id="215cf-114">Uzņēmums paļaujas uz savām noliktavu operācijām, lai pēc tam, kad daudzumi ir atrasti noliktavas uzglabāšanas telpā, pārvaldītu tādu daudzumu izdošanu, kuriem ir partijas vai sērijas numuri.</span><span class="sxs-lookup"><span data-stu-id="215cf-114">The business relies on its warehouse operations to manage picking of quantities that have batch or serial numbers after the quantities have been found in the warehousing storage space.</span></span> <span data-ttu-id="215cf-115">Šis modelis bieži tiek saukts par *Partijas lejpusējs\[novietojums\]*.</span><span class="sxs-lookup"><span data-stu-id="215cf-115">This model is often referred to as *Batch-below\[location\]*.</span></span> <span data-ttu-id="215cf-116">Parasti tas tiek izmantots, ja debitoriem, kuri pārdošanas uzņēmumā iesniedz pieprasījumu, nav svarīga preces partijas vai sērijas numura identifikācija.</span><span class="sxs-lookup"><span data-stu-id="215cf-116">It's typically used when a product's batch or serial number identification isn't important to the customers who place the demand with the selling company.</span></span>
- <span data-ttu-id="215cf-117">Ja partijas vai sērijas numuri ir daļa no debitora pasūtījuma specifikācijas, un tie tiek ierakstīti pieprasījuma pasūtījumā, noliktavas operācijas, kas atrod daudzumus noliktavā, ierobežo konkrēti pieprasītie numuri, un tām nav atļauts tās mainīt.</span><span class="sxs-lookup"><span data-stu-id="215cf-117">If batch or serial numbers are part of a customer's order specification, and they are recorded on the demand order, the warehouse operations that find the quantities in the warehouse are constrained by the specific requested numbers and aren't allowed to change them.</span></span> <span data-ttu-id="215cf-118">Šis modelis tiek saukts par *Partijas augšpusēju\[novietojumu\]*.</span><span class="sxs-lookup"><span data-stu-id="215cf-118">This model is referred to as *Batch-above\[location\]*.</span></span>

<span data-ttu-id="215cf-119">Šādos scenārijos grūtības rada tas, ka katrai izlaistajai precei var piešķirt tikai vienu krājumu rezervācijas hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="215cf-119">In these scenarios, the challenge is that only one inventory reservation hierarchy can be assigned to each released product.</span></span> <span data-ttu-id="215cf-120">Tāpēc, lai WMS apkalpotu izsekotos krājumus, pēc hierarhijas piešķires nosaka, kad partijas vai sērijas numurs jārezervē (vai nu, kad tiek veikts pieprasījums, vai arī noliktavas izdošanas darbā); šo laiku nevar mainīt pēkšņi.</span><span class="sxs-lookup"><span data-stu-id="215cf-120">Therefore, for the WMS to handle tracked items, after the hierarchy assignment determines when the batch or serial number should be reserved (either when the demand order is taken or during the warehouse picking work), this timing can't be changed on an ad-hoc basis.</span></span>

## <a name="flexible-reservation-for-batch-tracked-items"></a><span data-ttu-id="215cf-121">Elastīga partijas izsekoto krājumu rezervācija</span><span class="sxs-lookup"><span data-stu-id="215cf-121">Flexible reservation for batch-tracked items</span></span>

### <a name="business-scenario"></a><span data-ttu-id="215cf-122">Biznesa scenārijs</span><span class="sxs-lookup"><span data-stu-id="215cf-122">Business scenario</span></span>

<span data-ttu-id="215cf-123">Šajā scenārijā uzņēmums izmanto krājumu stratēģiju, kur gatavās preces tiek izsekotas pēc partiju numuriem.</span><span class="sxs-lookup"><span data-stu-id="215cf-123">In this scenario, a company uses an inventory strategy where finished goods are tracked by batch numbers.</span></span> <span data-ttu-id="215cf-124">Šis uzņēmums izmanto arī WMS noslodzi.</span><span class="sxs-lookup"><span data-stu-id="215cf-124">This company also uses the WMS workload.</span></span> <span data-ttu-id="215cf-125">Tā kā šai darba noslodzei ir labi aprīkota loģika, lai plānotu un izpildītu to krājumu izdošanu no noliktavas un nosūtīšanu, kuriem iespējotas partijas, lielākā daļa gatavo krājumu ir saistīti ar "Partijas lejpusēja\[novietojuma\]" krājumu rezervācijas hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="215cf-125">Because this workload has well-equipped logic for planning and running warehouse picking and shipping operations for batch-enabled items, most of the finished items are associated with a "Batch-below\[location\]" inventory reservation hierarchy.</span></span> <span data-ttu-id="215cf-126">Šāda veida darbību iestatījumam ir priekšrocība, ka lēmumi (kuri ir efektīvi rezervācijas lēmumi) par to, kuras partijas izdot un kur tās ievietot noliktavā, tiek atlikti līdz noliktavas izdošanas darbību sākumam.</span><span class="sxs-lookup"><span data-stu-id="215cf-126">The advantage of this type of operational setup is that decisions (which are effectively reservation decisions) about which batches to pick and where to put them in the warehouse are postponed until the warehouse picking operations start.</span></span> <span data-ttu-id="215cf-127">Tās netiek izpildītas, kad tiek veikts debitora pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="215cf-127">They aren't made when the customer's order is placed.</span></span>

<span data-ttu-id="215cf-128">Kaut arī "Partijas lejpusēja\[novietojuma\]" rezervāciju hierarhija kalpo uzņēmuma biznesa mērķiem, daudziem no uzņēmuma stabilajiem debitoriem ir nepieciešama tā pati partija, ko tie iegādājās iepriekš, kad vēlreiz pasūtīja preces.</span><span class="sxs-lookup"><span data-stu-id="215cf-128">Although the "Batch-below\[location\]" reservation hierarchy serves the company's business goals well, many of the company's established customers require the same batch that they previously purchased when they reorder products.</span></span> <span data-ttu-id="215cf-129">Tāpēc uzņēmums meklē elastīgu pieeju partijas rezervācijas noteikumu piemērošanai, un tādējādi atkarībā no debitora pieprasījuma tam pašam krājumam izpaužas tālāk aprakstītā rīcība.</span><span class="sxs-lookup"><span data-stu-id="215cf-129">Therefore, the company is looking for flexibility in the way that the batch reservation rules are handled, so that, depending on the customers' demand for the same item, the following behaviors occur:</span></span>

- <span data-ttu-id="215cf-130">Partijas numuru var ierakstīt un rezervēt laikā, kad pasūtījumu veic pārdošanas apstrādātājs, un to nevar mainīt noliktavas darbību laikā un/vai, ņemot vērā citas prasības.</span><span class="sxs-lookup"><span data-stu-id="215cf-130">A batch number can be recorded and reserved when the order is taken by the sales processor, and it can't be changed during warehouse operations and/or taken by other demands.</span></span> <span data-ttu-id="215cf-131">Šī rīcība palīdz garantēt, ka pasūtītais partijas numurs tiek nosūtīts debitoram.</span><span class="sxs-lookup"><span data-stu-id="215cf-131">This behavior helps guarantee that the batch number that was ordered is shipped to the customer.</span></span>
- <span data-ttu-id="215cf-132">Ja debitoram partijas numurs nav svarīgs, noliktavas darbības var norādīt partijas numuru izdošanas darba laikā, pēc pārdošanas pasūtījuma reģistrācijas un rezervēšanas veikšanas.</span><span class="sxs-lookup"><span data-stu-id="215cf-132">If the batch number isn't important to the customer, the warehouse operations can determine a batch number during picking work, after sales order registration and reservation have been done.</span></span>

### <a name="allowing-reservation-of-a-specific-batch-on-the-sales-order"></a><span data-ttu-id="215cf-133">Konkrētas partijas rezervācijas atļauśana pārdošanas pasūtījumā</span><span class="sxs-lookup"><span data-stu-id="215cf-133">Allowing reservation of a specific batch on the sales order</span></span>

<span data-ttu-id="215cf-134">Lai piemērotu vēlamo elastību partijas rezervācijas rīcībā krājumiem, kas ir saistīti ar "Partijas lejpusēja\[novietojuma\]" krājumu rezervēšanas hierarhiju, krājuma vadītājiem jāatzīmē izvēles rūtiņa **Atļaut rezervāciju pēc pieprasījuma pasūtījuma** līmenim **Partijas numurs** lapā **Krājumu rezervācijas hierarhija**.</span><span class="sxs-lookup"><span data-stu-id="215cf-134">To accommodate the desired flexibility in the batch reservation behavior for items that are associated with a "Batch-below\[location\]" inventory reservation hierarchy, inventory managers must select the **Allow reservation on demand order** check box for the **Batch number** level on the **Inventory reservation hierarchies** page.</span></span>

![Krājumu rezervācijas hierarhijas elastīguma nodrošināšana](media/Flexible-inventory-reservation-hierarchy.png)

<span data-ttu-id="215cf-136">Ja hierarhijā ir atlasīts līmenis **Partijas numurs**, tad automātiski tiks atlasītas visas dimensijas virs šī līmeņa un uz augšu līdz līmenim **Atrašanās vieta**.</span><span class="sxs-lookup"><span data-stu-id="215cf-136">When the **Batch number** level in the hierarchy is selected, all dimensions above that level and up through the **Location** level will be automatically selected.</span></span> <span data-ttu-id="215cf-137">(Pēc noklusējuma visas dimensijas virs līmeņa **Atrašanās vieta** tiek atlasītas iepriekš.) Šāda rīcība ataino loģiku, ka pasūtījuma rindā rezervējot konkrētu partijas numuru, automātiski tiek rezervetas arī visas dimensijas diapazonā starp partijas numuru un novietojumu.</span><span class="sxs-lookup"><span data-stu-id="215cf-137">(By default, all dimensions above the **Location** level are preselected.) This behavior reflects the logic where all dimensions in the range between the batch number and location are also automatically reserved after you reserve a specific batch number on the order line.</span></span>

> [!NOTE]
> <span data-ttu-id="215cf-138">Izvēles rūtiņa **Atļaut rezervāciju pēc pieprasījuma pasūtījuma** attiecas tikai tiem uz rezervāciju hierarhijas līmeņiem, kas atrodas zemāk par noliktavas atrašanās vietu dimensiju.</span><span class="sxs-lookup"><span data-stu-id="215cf-138">The **Allow reservation on demand order** check box applies only to reservation hierarchy levels that are below the warehouse location dimension.</span></span>
>
> <span data-ttu-id="215cf-139">**Partijas numurs** ir vienīgais hierarhijas līmenis, kas ir atvērts elastīgai rezervācijas politikai.</span><span class="sxs-lookup"><span data-stu-id="215cf-139">**Batch number** is the only level in the hierarchy that is open for the flexible reservation policy.</span></span> <span data-ttu-id="215cf-140">Citiem vārdiem sakot, izvēles rūtiņu **Atļaut rezervāciju pieprasījuma pasūtījumā** nevar atzīmēt līmeņiem **Atrašanās vieta**, **Noliktavas vienība** vai **Sērijas numurs**.</span><span class="sxs-lookup"><span data-stu-id="215cf-140">In other words, you can't select the **Allow reservation on demand order** check box for the **Location**, **License plate**, or **Serial number** level.</span></span>
>
> <span data-ttu-id="215cf-141">Ja rezervāciju hierarhijā ir ietverta sērijas numura dimensija (kurai vienmēr jābūt zemākai par līmeni **Partijas numurs**) un ja partijas numuram ir ieslēgta partijai specifiska rezervācija, sistēma turpinās nodrošināt sērijas numura rezervāciju un izdošanu, pamatojoties uz noteikumiem, kas attiecas uz rezervācijas politiku "Sērija nesvarīgāka par\[Atrašanās vietu\]".</span><span class="sxs-lookup"><span data-stu-id="215cf-141">If your reservation hierarchy includes the serial number dimension (which must always be below the **Batch number** level), and if you've turned on batch-specific reservation for the batch number, the system will continue to handle serial number reservation and picking operations, based on the rules that apply to the "Serial-below\[location\]" reservation policy.</span></span>

<span data-ttu-id="215cf-142">Jūs jebkurā brīdī savā izvietojumā varat atļaut veikt partijai specifisko rezervāciju jau esošai rezervāciju hierarhijai "Partijas lejpusējs\[novietojums\]".</span><span class="sxs-lookup"><span data-stu-id="215cf-142">At any point, you can allow batch-specific reservation for an existing "Batch-below\[location\]" reservation hierarchy in your deployment.</span></span> <span data-ttu-id="215cf-143">Šīs izmaiņas neietekmē rezervācijas un atvērto noliktavas darbu, kas tika izveidots pirms izmaiņu rašanās.</span><span class="sxs-lookup"><span data-stu-id="215cf-143">This change won't affect any reservations and open warehouse work that were created before the change occurred.</span></span> <span data-ttu-id="215cf-144">Tomēr izvēles rūtiņu **Atļaut rezervāciju pēc pieprasījuma pasūtījuma** nevar dzēst, ja vienam vai vairākiem krājumiem, kas ir saistīti ar šo rezervāciju hierarhiju, eksistē izsniegšanas veidu **Rezervēts pasūtījumos**, **Rezervēts fiziski** vai **Pasūtīts** krājumu darbības.</span><span class="sxs-lookup"><span data-stu-id="215cf-144">However, the **Allow reservation on demand order** check box can't be cleared if inventory transactions of the **Reserved ordered**, **Reserved physical**, or **Ordered** issue type exist for one or more items that are associated with that reservation hierarchy.</span></span>

> [!NOTE]
> <span data-ttu-id="215cf-145">Ja krājuma esošā rezervāciju hierarhija pasūtījumā neatļauj partijas specifikāciju, to var piešķirt rezervāciju hierarhijai, kas pieļauj partijas specifikāciju, ar nosacījumu, ka abās hierarhijās ir vienāda hierarhijas līmeņa struktūra.</span><span class="sxs-lookup"><span data-stu-id="215cf-145">If an item's existing reservation hierarchy doesn't allow batch specification on the order, you can reassign it to a reservation hierarchy that does allow batch specification, provided that the hierarchy level structure is the same in both hierarchies.</span></span> <span data-ttu-id="215cf-146">Lai veiktu atkārtotu piešķiršanu, izmantojiet funkciju **Mainīt krājumu rezervāciju hierarhijas**.</span><span class="sxs-lookup"><span data-stu-id="215cf-146">Use the **Change reservation hierarchy for items** function to do the reassignment.</span></span> <span data-ttu-id="215cf-147">Šīs izmaiņas var būt būtiskas, ja vēlaties novērst elastīgu partijas rezervāciju partijas izsekoto krājumu apakškopai, bet atļaut to pārējam preču portfelim.</span><span class="sxs-lookup"><span data-stu-id="215cf-147">This change might be relevant when you want to prevent flexible batch reservation for a subset of batch-tracked items but allow it for the rest of the product portfolio.</span></span>

<span data-ttu-id="215cf-148">Neatkarīgi no tā, vai ir atlasīta izvēles rūtiņa **Atļaut rezervāciju pēc pieprasījuma pasūtījuma**, ja nevēlaties krājumam pasūtījuma rindā rezervēt konkrētu partijas numuru, joprojām būs spēkā noklusējuma noliktavas darbību loģika, kas ir derīga rezervācijas hierarhijai "Partijas lejpusējs\[novietojums\]".</span><span class="sxs-lookup"><span data-stu-id="215cf-148">Regardless of whether you've selected the **Allow reservation on demand order** check box, if you don't want to reserve a specific batch number for the item on an order line, default warehouse operations logic that is valid for a "Batch-below\[location\]" reservation hierarchy will still apply.</span></span>

### <a name="reserve-a-specific-batch-number-for-a-customer-order"></a><span data-ttu-id="215cf-149">Konkrētra partijas numura rezervācija debitora pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="215cf-149">Reserve a specific batch number for a customer order</span></span>

<span data-ttu-id="215cf-150">Pēc tam, kad partijas izsekotā krājuma krājumu rezervāciju hierarhija "Partijas lejpusējs\[novietojums\]" ir iestatīta, lai rezervāciju pārdošanas pasūtījumos atļautu konkrētus partiju numurus, pārdošanas pasūtījumu apstrādātaji var atkarībā no debitora pieprasījuma pieņemt debitora pasūtījumus tam pašam krājumam vienā no tālāk norādītajiem veidiem.</span><span class="sxs-lookup"><span data-stu-id="215cf-150">After a batch-tracked item's "Batch-below\[location\]" inventory reservation hierarchy is set up to allow reservation of specific batch numbers on sales orders, sales order processors can take customer orders for the same item in one of the following ways, depending on the customer's request:</span></span>

- <span data-ttu-id="215cf-151">**Pasūtījuma informācijas ievade, nenorādot partijas numuru** – šī pieeja jāizmanto, ja debitoram nav svarīga preces partijas specifikācija.</span><span class="sxs-lookup"><span data-stu-id="215cf-151">**Enter order details without specifying a batch number** – This approach should be used when the product's batch specification isn't important to the customer.</span></span> <span data-ttu-id="215cf-152">Visi esošie procesi, kas sistēmā ir saistīti ar šī tipa pasūtījuma apstrādi, paliek nemainīgi.</span><span class="sxs-lookup"><span data-stu-id="215cf-152">All existing processes that are associated with handling an order of this type in the system remain unchanged.</span></span> <span data-ttu-id="215cf-153">No lietotāju puses nav nepieciešami papildu apsvērumi.</span><span class="sxs-lookup"><span data-stu-id="215cf-153">No additional considerations are required on the part of users.</span></span>
- <span data-ttu-id="215cf-154">**Pasūtījuma informācijas ievade un konkrēta partijas numura rezervācija** – šī pieeja jālieto, kad debitors pieprasa konkrētu partiju.</span><span class="sxs-lookup"><span data-stu-id="215cf-154">**Enter order details and reserve a specific batch number** – This approach should be used when the customer requests a specific batch.</span></span> <span data-ttu-id="215cf-155">Parasti debitori pieprasīs konkrētu partiju, ja tie atkārtoti pasūta iepriekš iegādātu preci.</span><span class="sxs-lookup"><span data-stu-id="215cf-155">Typically, customers will request a specific batch when they are reordering a product that they previously purchased.</span></span> <span data-ttu-id="215cf-156">Šo partijai specifiskās rezervācijas tipu dēvē par *ar pasūtījumu saistītu rezervāciju*.</span><span class="sxs-lookup"><span data-stu-id="215cf-156">This type of batch-specific reservation is referred to as *order-committed reservation*.</span></span>

<span data-ttu-id="215cf-157">Tālāk norādītais noteikumu kopums ir spēkā, ja tiek apstrādāti lieli preču daudzumi, un partijas numurs ir saistīts ar konkrētu pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="215cf-157">The following set of rules is valid when quantities are processed, and a batch number is committed to a specific order:</span></span>

- <span data-ttu-id="215cf-158">Lai atļautu konkrēta partijas numura rezervāciju krājumam saskaņā ar rezervācijas politiku "Partijas lejpusējs\[novietojums\]", sistēmai jārezervē visas dimensijas līdz atrašanās vietai.</span><span class="sxs-lookup"><span data-stu-id="215cf-158">To allow reservation of a specific batch number for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="215cf-159">Šis diapazons parasti ietver noliktavas vienības dimensiju.</span><span class="sxs-lookup"><span data-stu-id="215cf-159">This range typically includes the license plate dimension.</span></span>
- <span data-ttu-id="215cf-160">Atrašanās vietas direktīvas netiek pielietotas, ja izdošanas darbs ir izveidots pārdošanas rindai, kas izmanto ar pasūtījumu saistītu partijas rezervāciju.</span><span class="sxs-lookup"><span data-stu-id="215cf-160">Location directives aren't used when picking work is created for a sales line that uses order-committed batch reservation.</span></span>
- <span data-ttu-id="215cf-161">Veicot noliktavā ar pasūtījumu saistītu partiju darba apstrādi, ne lietotājam, ne sistēmai nav atļauts mainīt partijas numuru.</span><span class="sxs-lookup"><span data-stu-id="215cf-161">During warehouse processing of work for order-committed batches, neither the user nor the system is allowed to change the batch number.</span></span> <span data-ttu-id="215cf-162">(Šī apstrāde ietver izņēmumu apstrādi.)</span><span class="sxs-lookup"><span data-stu-id="215cf-162">(This processing includes exception handling.)</span></span>

<span data-ttu-id="215cf-163">Tālāk piemērā ir parādītas visi plūsmas posmi.</span><span class="sxs-lookup"><span data-stu-id="215cf-163">The following example shows the end-to-end flow.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="215cf-164">Piemēra situācija</span><span class="sxs-lookup"><span data-stu-id="215cf-164">Example scenario</span></span>

<span data-ttu-id="215cf-165">Šajā piemērā jābūt instalētiem demonstrāciju datiem, un jums ir jāizmanto **USMF** demonstrācijas datu uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="215cf-165">For this example, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="set-up-an-inventory-reservation-hierarchy-to-allow-batch-specific-reservation"></a><span data-ttu-id="215cf-166">Krājumu rezervēšanas hierarhijas iestatīšana, lai atļautu partijai specifisku rezervāciju</span><span class="sxs-lookup"><span data-stu-id="215cf-166">Set up an inventory reservation hierarchy to allow batch-specific reservation</span></span>

1. <span data-ttu-id="215cf-167">Dodieties uz **Noliktavas pārvaldība** \> **Iestatījumi** \> **Krājums \> Rezervēšanas hierarhija**.</span><span class="sxs-lookup"><span data-stu-id="215cf-167">Go to **Warehouse management** \> **Setup** \> **Inventory \> Reservation hierarchy**.</span></span>
2. <span data-ttu-id="215cf-168">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="215cf-168">Select **New**.</span></span>
3. <span data-ttu-id="215cf-169">Laukā **Nosaukums** ievadiet nosaukumu (piemēram, **BatchFlex**).</span><span class="sxs-lookup"><span data-stu-id="215cf-169">In the **Name** field, enter a name (for example, **BatchFlex**).</span></span>
4. <span data-ttu-id="215cf-170">Laukā **Apraksts** ievadiet aprakstu (piemēram, **Elastīgs partijas numura novietojums**).</span><span class="sxs-lookup"><span data-stu-id="215cf-170">In the **Description** field, enter a description (for example, **Batch below flexible**).</span></span>
5. <span data-ttu-id="215cf-171">Laukā **Atlasīts** atlasiet **Sērijas numurs** un **Īpašnieks**, un pēc tam atlasiet kreiso bulttaustiņu, lai tos pārvietotu uz lauku **Pieejams**.</span><span class="sxs-lookup"><span data-stu-id="215cf-171">In the **Selected** field, select **Serial number** and **Owner**, and then select the left arrow button to move them to the **Available** field.</span></span>
6. <span data-ttu-id="215cf-172">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="215cf-172">Select **OK**.</span></span>
7. <span data-ttu-id="215cf-173">Dimensijas līmeņa rindā **Partijas numurs** atzīmējiet izvēles rūtiņu **Atļaut rezervāciju pēc pieprasījuma pasūtījuma**.</span><span class="sxs-lookup"><span data-stu-id="215cf-173">In the row for the **Batch number** dimension level, select the **Allow reservation on demand order** check box.</span></span> <span data-ttu-id="215cf-174">Automātiski tiek atlasīti līmeņi **Noliktavas vienība** un **Atrašanās vieta**, un to izvēles rūtiņas nevar dzēst.</span><span class="sxs-lookup"><span data-stu-id="215cf-174">The **License plate** and **Location** levels are automatically selected, and you can't clear the check boxes for them.</span></span>
8. <span data-ttu-id="215cf-175">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="215cf-175">Select **Save**.</span></span>

### <a name="create-a-new-released-product"></a><span data-ttu-id="215cf-176">Jaunas izlaistās preces izveide</span><span class="sxs-lookup"><span data-stu-id="215cf-176">Create a new released product</span></span>

1. <span data-ttu-id="215cf-177">Iestatiet preces trīs pamatdatu parametrus, izmantojot tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="215cf-177">Set the product's three master data parameters by using these values:</span></span>

    - <span data-ttu-id="215cf-178">Laukā **Noliktavas dimensiju grupa** atlasiet **Izstrādājumi**.</span><span class="sxs-lookup"><span data-stu-id="215cf-178">In the **Storage dimension group** field, select **Ware**.</span></span>
    - <span data-ttu-id="215cf-179">Laukā **Izsekošanas dimensijas grupa** atlasiet **Batch-Phy**.</span><span class="sxs-lookup"><span data-stu-id="215cf-179">In the **Tracking dimension group** field, select **Batch-Phy**.</span></span>
    - <span data-ttu-id="215cf-180">Laukā **Rezervācijas hierarhija** atlasiet **BatchFlex**.</span><span class="sxs-lookup"><span data-stu-id="215cf-180">In the **Reservation hierarchy** field, select **BatchFlex**.</span></span>

2. <span data-ttu-id="215cf-181">Izveidojiet divus partiju numurus, piemēram, **B11** un **B22**.</span><span class="sxs-lookup"><span data-stu-id="215cf-181">Create two batch numbers, such as **B11** and **B22**.</span></span>
3. <span data-ttu-id="215cf-182">Pievienojiet krājumu daudzumus rīcībā esošajiem krājumiem, izmantojot tālāk norādītās vērtības.</span><span class="sxs-lookup"><span data-stu-id="215cf-182">Add item quantities to on-hand stock by using the following values.</span></span>

    | <span data-ttu-id="215cf-183">Noliktava</span><span class="sxs-lookup"><span data-stu-id="215cf-183">Warehouse</span></span> | <span data-ttu-id="215cf-184">Paketes numurs</span><span class="sxs-lookup"><span data-stu-id="215cf-184">Batch number</span></span> | <span data-ttu-id="215cf-185">Vieta</span><span class="sxs-lookup"><span data-stu-id="215cf-185">Location</span></span> | <span data-ttu-id="215cf-186">Numura zīme</span><span class="sxs-lookup"><span data-stu-id="215cf-186">License plate</span></span> | <span data-ttu-id="215cf-187">Daudzums</span><span class="sxs-lookup"><span data-stu-id="215cf-187">Quantity</span></span> |
    |-----------|--------------|----------|---------------|----------|
    | <span data-ttu-id="215cf-188">24</span><span class="sxs-lookup"><span data-stu-id="215cf-188">24</span></span>        | <span data-ttu-id="215cf-189">B11</span><span class="sxs-lookup"><span data-stu-id="215cf-189">B11</span></span>          | <span data-ttu-id="215cf-190">BULK-001</span><span class="sxs-lookup"><span data-stu-id="215cf-190">BULK-001</span></span> | <span data-ttu-id="215cf-191">Nav</span><span class="sxs-lookup"><span data-stu-id="215cf-191">None</span></span>          | <span data-ttu-id="215cf-192">10.</span><span class="sxs-lookup"><span data-stu-id="215cf-192">10</span></span>       |
    | <span data-ttu-id="215cf-193">24</span><span class="sxs-lookup"><span data-stu-id="215cf-193">24</span></span>        | <span data-ttu-id="215cf-194">B11</span><span class="sxs-lookup"><span data-stu-id="215cf-194">B11</span></span>          | <span data-ttu-id="215cf-195">FL-001</span><span class="sxs-lookup"><span data-stu-id="215cf-195">FL-001</span></span>   | <span data-ttu-id="215cf-196">LP11</span><span class="sxs-lookup"><span data-stu-id="215cf-196">LP11</span></span>          | <span data-ttu-id="215cf-197">10.</span><span class="sxs-lookup"><span data-stu-id="215cf-197">10</span></span>       |
    | <span data-ttu-id="215cf-198">24</span><span class="sxs-lookup"><span data-stu-id="215cf-198">24</span></span>        | <span data-ttu-id="215cf-199">B22</span><span class="sxs-lookup"><span data-stu-id="215cf-199">B22</span></span>          | <span data-ttu-id="215cf-200">FL-002</span><span class="sxs-lookup"><span data-stu-id="215cf-200">FL-002</span></span>   | <span data-ttu-id="215cf-201">LP22</span><span class="sxs-lookup"><span data-stu-id="215cf-201">LP22</span></span>          | <span data-ttu-id="215cf-202">10.</span><span class="sxs-lookup"><span data-stu-id="215cf-202">10</span></span>       |

### <a name="enter-sales-order-details"></a><span data-ttu-id="215cf-203">Pārdošanas pasūtījumu informācijas ievade</span><span class="sxs-lookup"><span data-stu-id="215cf-203">Enter sales order details</span></span>

1. <span data-ttu-id="215cf-204">Dodieties uz **Pārdošana un mārketings** \> **Pārdošanas pasūtījumi** \> **Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="215cf-204">Go to **Sales and marketing** \> **Sales orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="215cf-205">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="215cf-205">Select **New**.</span></span>
3. <span data-ttu-id="215cf-206">Pārdošanas pasūtījumu virsrakstā, laukā **Debitora konts**, ievadiet **US-003**.</span><span class="sxs-lookup"><span data-stu-id="215cf-206">On the sales order header, in the **Customer account** field, enter **US-003**.</span></span>
4. <span data-ttu-id="215cf-207">Pievienojiet rindu jaunajam krājumam un kā daudzumu ievadiet **10**.</span><span class="sxs-lookup"><span data-stu-id="215cf-207">Add a line for the new item, and enter **10** as the quantity.</span></span> <span data-ttu-id="215cf-208">Pārliecinieties, ka laukam **Noliktava** ir atlasīts iestatījums **24**.</span><span class="sxs-lookup"><span data-stu-id="215cf-208">Make sure that the **Warehouse** field is set to **24**.</span></span>
5. <span data-ttu-id="215cf-209">Kopsavilkuma cilnē **Pārdošanas pasūtījuma rindas** atlasiet **Krājums** un pēc tam grupā **Uzturēt** atlasiet **Partijas rezervācija**.</span><span class="sxs-lookup"><span data-stu-id="215cf-209">On the **Sales order lines** FastTab, select **Inventory**, and then, in the **Maintain** group, select **Batch reservation**.</span></span> <span data-ttu-id="215cf-210">Lapā **Partijas rezervācija** tiek parādīts to partiju saraksts, kas ir pieejamas pasūtījuma rindas rezervācijai.</span><span class="sxs-lookup"><span data-stu-id="215cf-210">The **Batch reservation** page shows a list of batches that are available for reservation for the order line.</span></span> <span data-ttu-id="215cf-211">Šajā piemērā tas rāda daudzumu **20** partijas numuram **B11** un daudzumu **10** partijas numuram **B22**.</span><span class="sxs-lookup"><span data-stu-id="215cf-211">For this example, it shows a quantity of **20** for batch number **B11** and a quantity of **10** for batch number **B22**.</span></span> <span data-ttu-id="215cf-212">Ņemiet vērā, ka lapai **Partijas rezervācija** nevar piekļūt no rindas, ja krājums šajā rindā ir saistīts ar rezervāciju hierarhiju "Partijas lejpusējs\[novietojums\]", ja vien tā nav iestatīta, lai atļautu partijai specifisku rezervāciju.</span><span class="sxs-lookup"><span data-stu-id="215cf-212">Note that the **Batch reservation** page cannot be accessed from a line if the item on that line is associated with "Batch-below\[location\]" reservation hierarchy unless it is set up to allow batch-specific reservation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="215cf-213">Lai pārdošanas pasūtījumam rezervētu konkrētu partiju, jāizmanto lapa **Partijas rezervācija**.</span><span class="sxs-lookup"><span data-stu-id="215cf-213">To reserve a specific batch for a sales order, you must use the **Batch reservation** page.</span></span>
    >
    > <span data-ttu-id="215cf-214">Ja ievadāt partijas numuru tieši pārdošanas pasūtījumu rindā, sistēma izturēsies tā, it kā jūs ievadījāt konkrētu partijas vērtību krājumam, uz kuru attiecas rezervācijas pincips "Partijas lejpusējs\[novietojums\]".</span><span class="sxs-lookup"><span data-stu-id="215cf-214">If you enter the batch number directly on the sales order line, the system will behave as though you entered a specific batch value for an item that is subject to the "Batch-below\[location\]" reservation policy.</span></span> <span data-ttu-id="215cf-215">Kad saglabāsit rindu, tiks parādīts brīdinājuma ziņojums.</span><span class="sxs-lookup"><span data-stu-id="215cf-215">When you save the line, you will receive a warning message.</span></span> <span data-ttu-id="215cf-216">Ja apstiprināt, ka partijas numurs ir jānorāda tieši pasūtījuma rindā, rindu neapstrādās parastā noliktavas pārvaldības loģika.</span><span class="sxs-lookup"><span data-stu-id="215cf-216">If you confirm that the batch number should be specified directly on the order line, the line won't be handled by the regular warehouse management logic.</span></span>
    >
    > <span data-ttu-id="215cf-217">Rezervējot daudzumu no lapas **Rerezervācija**, neviena konkrēta pakete netiks rezervēta, un noliktavas darbību izpilde rindai sekos noteikumiem, kas tiek piemēroti saskaņā ar rezervēšanas politiku "Partijas lejpusējs\[novietojums\]".</span><span class="sxs-lookup"><span data-stu-id="215cf-217">If you reserve the quantity from the **Reservation** page, no specific batch will be reserved, and the execution of warehouse operations for the line will follow the rules that are applicable under the "Batch-below\[location\]" reservation policy.</span></span>

    <span data-ttu-id="215cf-218">Parasti šī lapa darbojas un ir tiek izmantota tādā pašā veidā, kā tā darbojas, un to izmanto krājumiem, kuriem ir ar tipu "Partijas augšpusējs\[novietojums\]" saistīta rezervāciju hierarhija.</span><span class="sxs-lookup"><span data-stu-id="215cf-218">In general, this page works and is interacted with in the same way that it works and is interacted with for items that have an associated reservation hierarchy of the "Batch-above\[location\]" type.</span></span> <span data-ttu-id="215cf-219">Tomēr tiek piemēroti tālāk norādītie izņēmumi.</span><span class="sxs-lookup"><span data-stu-id="215cf-219">However, the following exceptions apply:</span></span>

    - <span data-ttu-id="215cf-220">Kopsavilkuma cilne **Avota rindai piesaistīti partijas numuri** tiek parādīti partijas numuri, kas ir rezervēti pasūtījuma rindai.</span><span class="sxs-lookup"><span data-stu-id="215cf-220">The **Batch numbers committed to source line** FastTab shows the batch numbers that are reserved for the order line.</span></span> <span data-ttu-id="215cf-221">Partijas vērtības režģī tiks rādītas visā pasūtījuma rindas izpildes ciklā, ieskaitot noliktavas apstrādes stadijas.</span><span class="sxs-lookup"><span data-stu-id="215cf-221">The batch values in the grid will be shown throughout the fulfilment cycle of the order line, including the warehouse processing stages.</span></span> <span data-ttu-id="215cf-222">Turpretī kopsavilkuma cilnē **Pārskats** regulāra pasūtījuma rindas rezervācija (tas ir, rezervēšana, kas tiek veikta dimensijām virs **Novietojuma** līmeņa) tiek rādīta režģī līdz vietai, kad tiek izveidots noliktavas darbs.</span><span class="sxs-lookup"><span data-stu-id="215cf-222">By contrast, on the **Overview** FastTab, regular order line reservation (that is, reservation that is done for the dimensions above the **Location** level) is shown in the grid up to the point when warehouse work is created.</span></span> <span data-ttu-id="215cf-223">Pēc tam rindas rezervāciju pārņem darba elements, un rindas rezervācija lapā vairs netiek rādīta.</span><span class="sxs-lookup"><span data-stu-id="215cf-223">The work entity then takes over the line reservation, and the line reservation no longer appears on the page.</span></span> <span data-ttu-id="215cf-224">Kopsavilkuma cilne **Avota rindai piesaistīti partijas numuri** palīdz garantēt, ka pārdošanas pasūtījumu apsatrādātājs var apskatīt partiju numurus, kas tika piesaistīti klienta pasūtījumam jebkurā dzīves cikla laikā līdz rēķinu izrakstīšanai.</span><span class="sxs-lookup"><span data-stu-id="215cf-224">The **Batch numbers committed to source line** FastTab helps guarantee that the sales order processor can view the batch numbers that were committed to the customer's order at any point during its lifecycle, up through invoicing.</span></span>
    - <span data-ttu-id="215cf-225">Papildus konkrētas partijas rezervēšanai lietotājs var manuāli atlasīt partijas konkrēto atrašanās vietu un numura zīmi, nevis ļaut sistēmai tās automātiski atlasīt.</span><span class="sxs-lookup"><span data-stu-id="215cf-225">In addition to reserving a specific batch, a user can manually select the batch's specific location and license plate instead of letting the system automatically select them.</span></span> <span data-ttu-id="215cf-226">Šī iespēja ir saistīta ar pasūtījumu saistītas partijas rezervācijas mehānisma izkārtojumu.</span><span class="sxs-lookup"><span data-stu-id="215cf-226">This capability is related to the design of the order-committed batch reservation mechanism.</span></span> <span data-ttu-id="215cf-227">Kā minēts iepriekš, kad partijas numurs tiek rezervēts krājumam saskaņā ar rezervācijas politiku "Partijas lejpusējs\[novietojums\]", sistēmai jārezervē visas dimensijas līdz atrašanās vietai.</span><span class="sxs-lookup"><span data-stu-id="215cf-227">As was mentioned earlier, when a batch number is reserved for an item under the "Batch-below\[location\]" reservation policy, the system must reserve all dimensions up through location.</span></span> <span data-ttu-id="215cf-228">Tāpēc noliktavas darbs veiks tās pašas noliktavas dimensijas, ko rezervēja lietotāji, kuri strādāja ar pasūtījumiem, un tas varētu ne vienmēr atainot tādu krājuma glabāšanas novietojumu, kas izdošanas darbībām ir ērts vai pat iespējams.</span><span class="sxs-lookup"><span data-stu-id="215cf-228">Therefore, warehouse work will carry the same storage dimensions that were reserved by the users who worked with the orders, and it might not always represent the item storage placement that is convenient, or even possible, for picking operations.</span></span> <span data-ttu-id="215cf-229">Ja pasūtījumu apstrādātāji ir informēti par noliktavas ierobežojumiem, tie, rezervējot partiju, varētu vēlēties manuāli atlasīt konkrētus novietojumus un noliktavas vienības.</span><span class="sxs-lookup"><span data-stu-id="215cf-229">If order processors are aware of the warehouse constraints, they might want to manually select the specific locations and license plates when they reserve a batch.</span></span> <span data-ttu-id="215cf-230">Šādā gadījumā lietotājam ir jāizmanto lapas galvenes funkcionalitāte **Parādīt dimensijas** un jāpievieno novietojuma un noliktavas vienība kopsavilkuma cilnes **Pārskats** režģī.</span><span class="sxs-lookup"><span data-stu-id="215cf-230">In this case, the user must use the **Display dimensions** functionality on the page header, and must add the location and license plate in the grid on the **Overview** FastTab.</span></span>

6. <span data-ttu-id="215cf-231">Lapā **Partijas rezervēšana** atlasiet partijas rindu **B11** un pēc tam atlasiet **Rezervēt rindu**.</span><span class="sxs-lookup"><span data-stu-id="215cf-231">On the **Batch reservation** page, select the line for batch **B11**, and then select **Reserve line**.</span></span> <span data-ttu-id="215cf-232">Automātiskās rezervēšanas laikā novietojuma un numura zīmju piešķiršanai nav norādīta loģika.</span><span class="sxs-lookup"><span data-stu-id="215cf-232">There is no designated logic for assigning locations and license plates during automatic reservation.</span></span> <span data-ttu-id="215cf-233">Daudzumu laukā **Rezervācija** var ievadīt manuāli.</span><span class="sxs-lookup"><span data-stu-id="215cf-233">You can manually enter the quantity in the **Reservation** field.</span></span> <span data-ttu-id="215cf-234">Ievērojiet, ka kopsavilkuma cilnē **Avota rindai piesaistīti partijas numuri** partija **B11** tiek norādīta kā **Piešķirts**.</span><span class="sxs-lookup"><span data-stu-id="215cf-234">Notice that, on the **Batch numbers committed to source line** FastTab, batch **B11** is shown as **Committed**.</span></span>

    ![Konkrēta partijas numura piešķiršana pārdošanas pasūtījuma rindai lapā Partijas rezervēšana](media/Batch-reservation-form-with-order-committed-reservation.png)

    > [!NOTE]
    > <span data-ttu-id="215cf-236">Pārdošanas pasūtījuma rindā norādītā daudzuma rezervāciju var veikt vairākām partijām.</span><span class="sxs-lookup"><span data-stu-id="215cf-236">Reservation of the quantity on a sales order line can be done across multiple batches.</span></span> <span data-ttu-id="215cf-237">Tāpat tās pašas partijas rezervāciju var veikt vairākām vietām un noliktavas vienībām (ja novietojumiem ir iespējotas noliktavas vienības).</span><span class="sxs-lookup"><span data-stu-id="215cf-237">Likewise, reservation of the same batch can be done against multiple locations and license plates (if license plates are enabled for the locations).</span></span>
    >
    > <span data-ttu-id="215cf-238">Konkrētas partijas rezervēšana pārdošanas pasūtījuma rindā esošajam daudzumam arī var būt daļēja.</span><span class="sxs-lookup"><span data-stu-id="215cf-238">Reservation of a specific batch for the quantity on a sales order line can also be partial.</span></span> <span data-ttu-id="215cf-239">Piemēram, 100 vienību kopējo daudzumu var rezervēt tā, ka 20 vienībām ir piešķirta konkrēta partija, turpretī 80 vienības tiek vietas un noliktavas līmeņos rezervētas jebkurai pieejamai partijai.</span><span class="sxs-lookup"><span data-stu-id="215cf-239">For example, the total quantity of 100 units can be reserved so that a specific batch is committed to 20 units, whereas 80 units are reserved at the site and warehouse levels for any available batch.</span></span> <span data-ttu-id="215cf-240">Šādā gadījumā WMS veiks izdošanas operācijas, izmantojot divas atsevišķas darba rindas.</span><span class="sxs-lookup"><span data-stu-id="215cf-240">In this case, the WMS will handle picking operations by using two separate work lines.</span></span>

7. <span data-ttu-id="215cf-241">DOdieties uz **Preču informācijas pārvaldība** \> **Preces** \> **Nodotās preces**.</span><span class="sxs-lookup"><span data-stu-id="215cf-241">Go to **Product information management** \> **Products** \> **Released products**.</span></span> <span data-ttu-id="215cf-242">Atlasiet savu vienību un pēc tam atlasiet **Pārvaldīt krājumu** \> **Skatīt** \> **Darbības**.</span><span class="sxs-lookup"><span data-stu-id="215cf-242">Select your item, and then select **Manage inventory** \> **View** \> **Transactions**.</span></span>

    ![Ar pasūtījumu saistīta rezervācija kā krājumu darbības tips](media/Inventory-transactions-for-order-committed-reservation.png)

8. <span data-ttu-id="215cf-244">Pārskatiet vienuma krājumu transakcijas, kas saistītas ar pārdošanas pasūtījuma rindas rezervāciju.</span><span class="sxs-lookup"><span data-stu-id="215cf-244">Review the item's inventory transactions that are related to the sales order line reservation.</span></span>

    - <span data-ttu-id="215cf-245">Transakcijas, kurā lauks **Atsauces** ir iestatīts uz **Pārdošanas pasūtījums** un lauks **Izsniegšana** iestatīts uz **Rezervēts fiziski** parāda pasūtījuma rindas rezervāciju krājumu dimensijām virs līmeņa **Novietojums**.</span><span class="sxs-lookup"><span data-stu-id="215cf-245">A transaction where the **Reference** field is set to **Sales order** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the inventory dimensions above the **Location** level.</span></span> <span data-ttu-id="215cf-246">Saskaņā ar vienuma krājumu rezervēšanas hierarhiju šīs dimensijas ir novietojums, noliktava un krājuma statuss.</span><span class="sxs-lookup"><span data-stu-id="215cf-246">According to the item's inventory reservation hierarchy, those dimensions are site, warehouse, and inventory status.</span></span>
    - <span data-ttu-id="215cf-247">Transakcija, kurā lauks **Atsauce** ir iestatīts uz **Ar pasūtījumu saistīta rezervācija** un lauks **Izsniegšana** ir iestatīts uz **Rezervēts fiziski**, parāda pasūtījuma rindas rezervāciju konkrētam krājumam un visām krājuma dimensijām virs tā.</span><span class="sxs-lookup"><span data-stu-id="215cf-247">A transaction where the **Reference** field is set to **Order-committed reservation** and the **Issue** field is set to **Reserved physical** represents the order line reservation for the specific batch and all inventory dimensions above it.</span></span> <span data-ttu-id="215cf-248">Saskaņā ar vienuma krājumu rezervēšanas hierarhiju šīs dimensijas ir partijas numurs un novietojums.</span><span class="sxs-lookup"><span data-stu-id="215cf-248">According to the item's inventory reservation hierarchy, those dimensions are batch number and location.</span></span> <span data-ttu-id="215cf-249">Šajā piemērā atrašanās vieta ir **Lielapjoma-001**.</span><span class="sxs-lookup"><span data-stu-id="215cf-249">In this example, the location is **Bulk-001**.</span></span>

9. <span data-ttu-id="215cf-250">Pārdošanas pasūtījuma virsrakstā atlasiet **Noliktava** \> **Darbības** \> **Pārvietot uz noliktavu**.</span><span class="sxs-lookup"><span data-stu-id="215cf-250">On the sales order header, select **Warehouse** \> **Actions** \> **Release to warehouse**.</span></span> <span data-ttu-id="215cf-251">Tagad pasūtījuma rinda ir viļņota, un tiek izveidota krava un darbs.</span><span class="sxs-lookup"><span data-stu-id="215cf-251">The order line is now waved, and a load and work are created.</span></span>

### <a name="review-and-process-warehouse-work-that-has-order-committed-batch-numbers"></a><span data-ttu-id="215cf-252">Tāda noliktavas darba pārskatīšana un apstrāde, kam ir ar pasūtījumu saistītu partiju numuri</span><span class="sxs-lookup"><span data-stu-id="215cf-252">Review and process warehouse work that has order-committed batch numbers</span></span>

1. <span data-ttu-id="215cf-253">Kopsavilkuma cilnē **Pārdošanas pasūtījumu rindas** atlasiet **Noliktava** \> **Detalizēta informācija par darbu**</span><span class="sxs-lookup"><span data-stu-id="215cf-253">On the **Sales order lines** FastTab, select **Warehouse** \> **Work details**.</span></span>

    <span data-ttu-id="215cf-254">Uz darbu, kas apstrādā izdošanas darbību partiju daudzumiem, kuri ir saistīti ar pārdošanas pasūtījuma rindu, attiecas tālāk norādītie raksturlielumi.</span><span class="sxs-lookup"><span data-stu-id="215cf-254">The work that handles the picking operation for batch quantities that are committed to the sales order line has the following characteristics:</span></span>

    - <span data-ttu-id="215cf-255">Lai izveidotu darbu, sistēma izmanto darba veidnes, bet ne novietojuma direktīvas.</span><span class="sxs-lookup"><span data-stu-id="215cf-255">To create work, the system uses work templates but not location directives.</span></span> <span data-ttu-id="215cf-256">Visi standarta iestatījumi, kas definēti darba veidnēm, piemēram, maksimālais izdošanas rindu skaits vai noteikta mērvienība, tiks lietoti, lai noteiktu, kad jāizveido jauns darbs.</span><span class="sxs-lookup"><span data-stu-id="215cf-256">All the standard settings that are defined for work templates, such as a maximum number of pick lines or a specific unit of measure, will be applied to determine when new work should be created.</span></span> <span data-ttu-id="215cf-257">Tomēr noteikumi, kas ar novietojuma direktīvām ir saistīti, lai identificētu izdošanas vietas, netiek ņemti vērā, jo ar pasūtījumu saistītajā rezervācija jau ir norādītas visas krājuma dimensijas.</span><span class="sxs-lookup"><span data-stu-id="215cf-257">However, the rules that are associated with location directives for identifying pick locations aren't considered, because the order-committed reservation already specifies all the inventory dimensions.</span></span> <span data-ttu-id="215cf-258">Šīs krājuma dimensijas ietver dimensijas noliktavas glabāšanas līmenī.</span><span class="sxs-lookup"><span data-stu-id="215cf-258">Those inventory dimensions include the dimensions at the warehouse storage level.</span></span> <span data-ttu-id="215cf-259">Tāpēc darbs pārmanto šīs dimensijas, nekonsultējoties ar novietojuma direktīvām.</span><span class="sxs-lookup"><span data-stu-id="215cf-259">Therefore, the work inherits those dimensions without having to consult location directives.</span></span>
    - <span data-ttu-id="215cf-260">Partijas numurs netiek uzrādīts izdošanas rindā (kā tas ir darba rindas gadījumā, kas izveidota krājumam, kuram ir saistītā rezervācijas hierarhija "Partijas augšpusējs\[novietojums\]".) Partijas numurs "no" un visas citas glabāšanas dimensijas tiek rādītas darba rindas darbu krājumu transakcijā, kam ir atsauce no saistītajām krājuma transakcijām.</span><span class="sxs-lookup"><span data-stu-id="215cf-260">The batch number isn't shown on the pick line (as is the case for the work line that is created for an item that has an associated "Batch-above\[location\]" reservation hierarchy.) Instead, the "from" batch number and all other storage dimensions are shown on the work line's work inventory transaction that is referenced from the associated inventory transactions.</span></span>

        ![Noliktavas krājuma transakcija, kas izveidota no ar pasūtījumu saistītas rezervācijas](media/Work-inventory-transactions-for-order-committed-reservation.png)

    - <span data-ttu-id="215cf-262">Pēc darba izveides tiek noņemta vienuma krājuma transakcija, kurā lauks **Atsauce** ir iestatīts kā **Ar pasūtījumu saistīta rezervēšana**.</span><span class="sxs-lookup"><span data-stu-id="215cf-262">After work is created, the item's inventory transaction where the **Reference** field is set to **Order-committed reservation** is removed.</span></span> <span data-ttu-id="215cf-263">Krājumu transakcija, kurā lauks **Atsauces** ir iestatīts uz **Darbs**, tagad ietver fizisko rezervāciju visām daudzuma krājumu dimensijām.</span><span class="sxs-lookup"><span data-stu-id="215cf-263">The inventory transaction where the **Reference** field is set to **Work** now holds the physical reservation on all the quantity's inventory dimensions.</span></span>

        <span data-ttu-id="215cf-264">Noliktavas darbības var turpināt darba izpildi parastajā kārtībā.</span><span class="sxs-lookup"><span data-stu-id="215cf-264">Warehouse operations can proceed to handle execution of the work in the usual manner.</span></span> <span data-ttu-id="215cf-265">Tomēr mobilās ierīces instrukcijās darbiniekam tiks norādīts izvēlēties konkrētu partijas numuru.</span><span class="sxs-lookup"><span data-stu-id="215cf-265">However, the instructions on the mobile device will instruct the worker to pick a specific batch number.</span></span> <span data-ttu-id="215cf-266">Noliktavas vidēs, kur novietojumu pārvalda noliktavas vienības, pēc tam, kad darbinieks sasniedz vietu, kurā vairākās noliktavas vienībās tiek glabāta tā pati partija, viņš var izvēlēties no jebkuras noliktavas vienības, kas vēl nav rezervēta (piemēram, cita ar pasūtījumu saitīta rezervācija vai darbs, kas radies no šī tipa rezervācijas).</span><span class="sxs-lookup"><span data-stu-id="215cf-266">In warehouse environments where locations are license plate–controlled, after a worker reaches a location that stores the same batch on multiple license plates, he or she can pick from any license plate that isn't already reserved (for example, by another order-committed reservation or work that originates from a reservation of that type.)</span></span>

        <span data-ttu-id="215cf-267">Ja izrādās, ka nav praktiski izvēlēties no vietas, kas norādīta darba rindā, noliktavas operatori var izmantot vienu no tālāk norādītajām darbībām, lai novirzītu konkrētas partijas izdošanu no ērtākas atrašanās vietas.</span><span class="sxs-lookup"><span data-stu-id="215cf-267">If it turns out to be impractical to pick from the location that is specified on the work line, the warehouse operators can use one of the following actions to redirect picking of the specific batch from a more convenient location:</span></span>

        - <span data-ttu-id="215cf-268">Standarta darbība **Ignorēt atrašanās vietu** mobilajā ierīcē (ar nosacījumu, ka ir iespējots noliktavas darbinieka iestatījums **Atļaut izdošanas novietojuma ignorēšanu**)</span><span class="sxs-lookup"><span data-stu-id="215cf-268">The standard **Override location** action on a mobile device (provided that the warehouse worker's **Allow pick location override** setting is enabled)</span></span>
        - <span data-ttu-id="215cf-269">Darbība **Mainīt atrašanāš vietu** lapā **Detalizēta informācija par darba sarakstu**.</span><span class="sxs-lookup"><span data-stu-id="215cf-269">The **Change location** action on the **Work list details** page.</span></span> 

2. <span data-ttu-id="215cf-270">Mobilajā ierīcē pabeidziet darba izdošanu un nodošanu.</span><span class="sxs-lookup"><span data-stu-id="215cf-270">On the mobile device, finish picking and putting the work.</span></span>

    <span data-ttu-id="215cf-271">Daudzums **10**, kas paredzēts partijas numuram **B11**, tagad ir izdots pārdošanas pasūtījuma rindai un ievietots atrašanās vietā **Aizmugurējās durvis**.</span><span class="sxs-lookup"><span data-stu-id="215cf-271">The quantity of **10** for batch number **B11** is now picked for the sales order line and put in the **Baydoor** location.</span></span> <span data-ttu-id="215cf-272">Šajā brīdī tas ir sagatavots iekraušanai kravas automašīnā un nosūtīšanai uz debitora adresi.</span><span class="sxs-lookup"><span data-stu-id="215cf-272">At this point, it's ready to be loaded onto the truck and dispatched to the customer's address.</span></span>

## <a name="exception-handling-of-warehouse-work-thas-has-order-committed-batch-numbers"></a><span data-ttu-id="215cf-273">Tāda noliktavas darba iIzņēmumu apstrāde, kam ir ar pasūtījumu saistītu partiju numuri</span><span class="sxs-lookup"><span data-stu-id="215cf-273">Exception handling of warehouse work thas has order-committed batch numbers</span></span>

<span data-ttu-id="215cf-274">Uz noliktavas darbu ar pasūtījumu saistītu partijas numuru izdošanai attiecas tā pati standarta noliktavas izņēmuma apstrāde un darbības kā uz parastu darbu.</span><span class="sxs-lookup"><span data-stu-id="215cf-274">Warehouse work for picking order-committed batch numbers is subject to the same standard warehouse exception handling and actions as regular work.</span></span> <span data-ttu-id="215cf-275">Parasti atvērto darbu vai darba rindu var atcelt, to var pārtraukt, jo lietotāja novietojums ir pilns, tā var būt ar saīsinātu izdošanu un tā var būt atjaunināta kustības dēļ.</span><span class="sxs-lookup"><span data-stu-id="215cf-275">In general, the open work or work line can be canceled, it can be interrupted because a user location is full, it can be short-picked, and it can be updated because of a movement.</span></span> <span data-ttu-id="215cf-276">Tāpat var tikt samazināts izdotais pabeigtā darba daudzums, vai arī darbu var atsaukt.</span><span class="sxs-lookup"><span data-stu-id="215cf-276">Likewise, the picked quantity of work that has already been completed can be reduced, or the work can be reversed.</span></span>

<span data-ttu-id="215cf-277">Visām šīm izņēmuma apstrādes darbībām tiek piemērots šāds pamatprincips: partijas numurs, kas tika rezervēts debitoram, nekad nevar tikt aizstāts ar citu partijas numuru, bet tā noliktavas dimensijas (novietojums un noliktavas vienība) var mainīt, izmantojot vai nu manuālu atjauninājumu, ko veic lietotājs, vai sistēmas automātisku atjaunināšanu.</span><span class="sxs-lookup"><span data-stu-id="215cf-277">The following key rule is applied to all these exception handling actions: the batch number that was reserved for the customer can never be replaced with a different batch number, but its storage dimensions (location and license plate) can be changed through either a manual update by the user or an automatic update by the system.</span></span> <span data-ttu-id="215cf-278">Automātiskās atjaunināšanas pamatā ir tā pati izlases veida noliktavas dimensiju piešķiršana, kas tiek piemērota, kad automātiski tika rezervēta konkrēta partija, bet netika norādītas noliktavas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="215cf-278">The automatic update is based on the same random assignment of storage dimensions that applied when a specific batch was automatically reserved but no storage dimensions were specified.</span></span>

### <a name="example-scenario"></a><span data-ttu-id="215cf-279">Piemēra situācija</span><span class="sxs-lookup"><span data-stu-id="215cf-279">Example scenario</span></span>

<span data-ttu-id="215cf-280">Šī scenārija piemērs ir situācija, kad iepriekš pabeigtais darbs tiek izdots, izmantojot funkciju **Samazināt izdoto daudzumu**.</span><span class="sxs-lookup"><span data-stu-id="215cf-280">An example of this scenario is a situation where previously completed work is being unpicked by using the **Reduce picked quantity** function.</span></span> <span data-ttu-id="215cf-281">Šajā piemēra tiek turpināta iepriekšējā piemērā minētā tēma.</span><span class="sxs-lookup"><span data-stu-id="215cf-281">This example continues the previous example in this topic.</span></span>

1. <span data-ttu-id="215cf-282">Dodieties uz **Noliktavas pārvaldība** \> **Kravas** \> **Aktīvās kravas**.</span><span class="sxs-lookup"><span data-stu-id="215cf-282">Go to **Warehouse management** \> **Loads** \> **Active loads**.</span></span>
2. <span data-ttu-id="215cf-283">Atlasiet noslodzi, kas tika izveidota saistībā ar jūsu pārdošanas pasūtījuma sūtījumu.</span><span class="sxs-lookup"><span data-stu-id="215cf-283">Select the load that was created in connection with the shipment of your sales order.</span></span>
3. <span data-ttu-id="215cf-284">No kopsavilkuma cilnes **Noslodzes pasūtījuma rindas** atlasiet **Samazināt izdoto daudzumu**.</span><span class="sxs-lookup"><span data-stu-id="215cf-284">From the **Load order lines** FastTab, select **Reduce picked quantity**.</span></span>
4. <span data-ttu-id="215cf-285">Lapas **Samazināt izdoto daudzumu** laukā **Pārvietot uz atrašānās vietu** atlasiet **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="215cf-285">On the **Reduce picked quantity** page, in the **Move to location** field, select **FL-001**.</span></span>
5. <span data-ttu-id="215cf-286">Laukā **Pārvietot uz noliktavas vienību** atlasiet **LP33**.</span><span class="sxs-lookup"><span data-stu-id="215cf-286">In the **Move to license plate** field, select **LP33**.</span></span>
6. <span data-ttu-id="215cf-287">Režģa laukā **Krājumu daudzums līdz izdošanai** ievadiet **10**.</span><span class="sxs-lookup"><span data-stu-id="215cf-287">In the grid, in the **Inventory quantity to unpick** field, enter **10**.</span></span>
7. <span data-ttu-id="215cf-288">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="215cf-288">Select **OK**.</span></span>

<span data-ttu-id="215cf-289">Tālak norādīti neizdošanas darbības rezultāti.</span><span class="sxs-lookup"><span data-stu-id="215cf-289">Here are the results of the unpicking action:</span></span>

- <span data-ttu-id="215cf-290">Iepriekš slēgtā darba statuss ir iestatīts uz **Atcelts**.</span><span class="sxs-lookup"><span data-stu-id="215cf-290">The status of the previously closed work is set to **Canceled**.</span></span>
- <span data-ttu-id="215cf-291">Jauns tipa **Krājuma kustība** darbs ir izveidots neizdotajam **10** daudzumam ar partijas numuru **B11**.</span><span class="sxs-lookup"><span data-stu-id="215cf-291">New work of the **Inventory movement** type is created for the unpicked quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="215cf-292">Šis darbs apzīmē pārvietošanos no novietojuma **Aizmugurējās durvis** uz noliktavas vienību **LP33** novietojumā **FL-001**.</span><span class="sxs-lookup"><span data-stu-id="215cf-292">This work represents the movement from the **Baydoor** location to license plate **LP33** in location **FL-001**.</span></span> <span data-ttu-id="215cf-293">Statuss jāiestata uz **Slēgts**.</span><span class="sxs-lookup"><span data-stu-id="215cf-293">The status is set to **Closed**.</span></span>
- <span data-ttu-id="215cf-294">Sistēma atkārtoti rezervē partijas numuru, kas tika sākotnēji pasūtīts, un piešķir novietojuma un noliktavas vienības ID.</span><span class="sxs-lookup"><span data-stu-id="215cf-294">The system re-reserves the batch number that was originally ordered, and assigns the location and license plate IDs.</span></span> <span data-ttu-id="215cf-295">(Šis process ir līdzvērtīgs funkcijas **Rezerves rinda** palaišanai noteikta partijas numura pasūtījuma rindai).</span><span class="sxs-lookup"><span data-stu-id="215cf-295">(This process is equivalent to running the **Reserve line** function for the order line for a given batch number).</span></span> <span data-ttu-id="215cf-296">Rezultātā partija **B11** tiek rādīta kā piesaistīta lapas **Partijas rezervēšana** kopsavilkuma cilnē **Avota rindai piesaistīti partijas numuri**, un laukā **Rezervācija** partijas numuram **B11** ir norādīts daudzums **B10**.</span><span class="sxs-lookup"><span data-stu-id="215cf-296">As a result, batch **B11** is shown as committed on the **Batch numbers committed to source line** FastTab of the **Batch reservation** page, and the **Reservation** field contains a quantity of **10** for batch number **B11**.</span></span> <span data-ttu-id="215cf-297">Turklāt lauks **Vieta** ir iestatīts kā **FL-001**, un lauks **Noliktavas vienība** ir iestatīts uz **LP11**.</span><span class="sxs-lookup"><span data-stu-id="215cf-297">Additionally, the **Location** field is set to **FL-001**, and the **License plate** field is set to **LP11**.</span></span> <span data-ttu-id="215cf-298">(Šos laukus var pievienot režģim, ja tie nav redzami.)</span><span class="sxs-lookup"><span data-stu-id="215cf-298">(You can add these fields to the grid if they aren't visible.)</span></span>

<span data-ttu-id="215cf-299">Tālāk norādītās tabulas sniedz pārskatu, kas parāda, kā sistēma apstrādā ar pasūtījumu saitītu partijas rezervāciju konkrētām noliktavas darbībām.</span><span class="sxs-lookup"><span data-stu-id="215cf-299">The following tables provide an overview that shows how the system handles order-committed batch reservation for specific warehouse actions.</span></span> <span data-ttu-id="215cf-300">Lai interpretētu tabulu saturu, pieņemiet, ka katra noliktavas darbība tiek izpildīta, ņemot vērā esošo noliktavas darbu, ko nosaka ar pasūtījumu saistītas partijas rezervācija, vai ka katras noliktavas darbības izpilde ietekmē šī tipa darbu.</span><span class="sxs-lookup"><span data-stu-id="215cf-300">To interpret the content in the tables, assume that each warehouse action is run in the context of existing warehouse work that originates from an order-committed batch reservation, or that execution of each warehouse action affects work of that type.</span></span>

> [!NOTE]
> <span data-ttu-id="215cf-301">Šajās tabulās kolonna "Partijas daudzums ir pieejams" norāda, vai partijas daudzums ir pieejams papildus daudzumam, kas vai nu jau ir rezervēts pašreizējām, ar pasūtījumu saistītās rezervācijām, vai arī to jau ir rezervējis noliktavas darbs, kas rodas no šī tipa rezervācijām.</span><span class="sxs-lookup"><span data-stu-id="215cf-301">In these tables, the "Batch quantity is available" column indicates whether a batch quantity is available in addition to the quantity that is either already reserved for the current order-committed reservations or already reserved by the warehouse work that originates from reservations of that type.</span></span>

#### <a name="override-the-pick-location-on-the-open-work"></a><span data-ttu-id="215cf-302">Izdošanas novietojuma ignorēšana atvēŗtā darbā</span><span class="sxs-lookup"><span data-stu-id="215cf-302">Override the pick location on the open work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="215cf-303">Galvenie iestatīšanas parametri</span><span class="sxs-lookup"><span data-stu-id="215cf-303">Key setup parameter</span></span></th>
<th><span data-ttu-id="215cf-304">Partijas daudzums ir pieejams</span><span class="sxs-lookup"><span data-stu-id="215cf-304">Batch quantity is available</span></span></th>
<th><span data-ttu-id="215cf-305">Galvenās lietotāja darbības</span><span class="sxs-lookup"><span data-stu-id="215cf-305">Key user steps</span></span></th>
<th><span data-ttu-id="215cf-306">Noliktavas darbs</span><span class="sxs-lookup"><span data-stu-id="215cf-306">Warehouse work</span></span></th>
<th><span data-ttu-id="215cf-307">Ar pasūtījumu saistītas partijas rezervēšana</span><span class="sxs-lookup"><span data-stu-id="215cf-307">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="215cf-308">Opcija <strong>Atļaut izdošanas novietojuma ignorēšanu</strong> ir aktivizēta darbiniekam.</span><span class="sxs-lookup"><span data-stu-id="215cf-308">The <strong>Allow pick location override</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="215cf-309">Jā</span><span class="sxs-lookup"><span data-stu-id="215cf-309">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="215cf-310">Kad sākat izdošanas darbu, noliktavas programmā atlasiet izvēlnes elementu <strong>Ignorēt atrašanās vietu</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-310">Select the <strong>Override location</strong> menu item on the warehousing app when you start picking work.</span></span></li>
<li><span data-ttu-id="215cf-311">Atlasiet <strong>Ieteikt</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-311">Select <strong>Suggest</strong>.</span></span></li>
<li><span data-ttu-id="215cf-312">Apstipriniet jauno atrašanās vietu, kas tiek piedāvāta, pamatojoties uz partijas daudzuma pieejamību.</span><span class="sxs-lookup"><span data-stu-id="215cf-312">Confirm the new location that is suggested based on batch quantity availability.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="215cf-313">Pašreizējā darbā tiek veiktas tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="215cf-313">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="215cf-314">Novietojums izdošanas rindā tiek atjaunināts uz jauno novietojumu.</span><span class="sxs-lookup"><span data-stu-id="215cf-314">The location on the pick line is updated to the new location.</span></span> <span data-ttu-id="215cf-315">(Ja novietojumu pārvalda noliktavas vienība, darba krājumu transakcijai tiek piešķirta izlases veda noliktavas vienība, un darbinieks var izdot no jebkuras noliktavas vienības, kurai ir pieejams daudzums.)</span><span class="sxs-lookup"><span data-stu-id="215cf-315">(If the location is license plate–controlled, a random license plate is assigned to the work inventory transaction, and the worker can pick from any license plate that has available quantity.)</span></span></li>
<li><span data-ttu-id="215cf-316">Ja daudzums jaunajā atrašanās vietā ir atrodams vairāk nekā vienā noliktavas vienībā, sākotnējā izdošanas rinda tiek sadalīta vairākās rindās, lai atbilstu katrai noliktavas vienībai.</span><span class="sxs-lookup"><span data-stu-id="215cf-316">If the quantity is found on more than one license plate in the new location, the original pick line is split into multiple lines to match each license plate.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="215cf-317">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="215cf-317">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="215cf-318">Nr.</span><span class="sxs-lookup"><span data-stu-id="215cf-318">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="215cf-319">Kad sākat izdošanas darbu, noliktavas programmā atlasiet izvēlnes elementu <strong>Ignorēt atrašanās vietu</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-319">Select the <strong>Override location</strong> menu item on the warehousing app when you start picking work.</span></span></li>
<li><span data-ttu-id="215cf-320">Manuāli ievadiet atrašānās vietu.</span><span class="sxs-lookup"><span data-stu-id="215cf-320">Manually enter a location.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="215cf-321">Darbība <strong>Ignorēt atrašanās vietu</strong> nav iespējama.</span><span class="sxs-lookup"><span data-stu-id="215cf-321">The <strong>Override location</strong> action isn't possible.</span></span> <span data-ttu-id="215cf-322">Tā neizdodas, un tiek izmesta kļūda.</span><span class="sxs-lookup"><span data-stu-id="215cf-322">It fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="215cf-323">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="215cf-323">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="full-button--split-a-work-line-because-of-overflow-on-the-user-location"></a><span data-ttu-id="215cf-324">Poga Pilna – darba rindas sadale, jo lietotāja atrašanās vietā radusies pārpilde</span><span class="sxs-lookup"><span data-stu-id="215cf-324">Full button – Split a work line because of overflow on the user location</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="215cf-325">Galvenie iestatīšanas parametri</span><span class="sxs-lookup"><span data-stu-id="215cf-325">Key setup parameter</span></span></th>
<th><span data-ttu-id="215cf-326">Partijas daudzums ir pieejams</span><span class="sxs-lookup"><span data-stu-id="215cf-326">Batch quantity is available</span></span></th>
<th><span data-ttu-id="215cf-327">Galvenās lietotāja darbības</span><span class="sxs-lookup"><span data-stu-id="215cf-327">Key user steps</span></span></th>
<th><span data-ttu-id="215cf-328">Noliktavas darbs</span><span class="sxs-lookup"><span data-stu-id="215cf-328">Warehouse work</span></span></th>
<th><span data-ttu-id="215cf-329">Ar pasūtījumu saistītas partijas rezervēšana</span><span class="sxs-lookup"><span data-stu-id="215cf-329">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="215cf-330">Opcija <strong>Atļaut darba sadali</strong> ir aktivizēta mobilās ierīces izvēlnes elementā.</span><span class="sxs-lookup"><span data-stu-id="215cf-330">The <strong>Allow splitting of work</strong> option is enabled on the mobile device menu item.</span></span></td>
<td><span data-ttu-id="215cf-331">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="215cf-331">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="215cf-332">Kad apstrādājat izdošanas darbu, noliktavas programmā atlasiet izvēlnes elementu <strong>Pilna</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-332">Select the <strong>Full</strong> menu item on the warehousing app when you process picking work.</span></span></li>
<li><span data-ttu-id="215cf-333">Laukā <strong>izdošanas daudzums</strong> ievadiet daļēju nepieciešamās izdošanas daudzumu, lai norādītu pilnu noslodzi.</span><span class="sxs-lookup"><span data-stu-id="215cf-333">In the <strong>Pick Qty</strong> field, enter a partial quantity of the required pick to indicate the full capacity.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="215cf-334">Pašreizējā darbā daudzums tiek atjaunināts uz atlikušo izdodamo daudzumu.</span><span class="sxs-lookup"><span data-stu-id="215cf-334">On the current work, the quantity is updated to the remaining quantity that must be picked.</span></span></li>
<li><span data-ttu-id="215cf-335">Izdotajam daudzumam tiek izveidots un slēgts jauns darbs.</span><span class="sxs-lookup"><span data-stu-id="215cf-335">New work for the picked quantity is created and closed.</span></span></li>
</ul></td>
<td><span data-ttu-id="215cf-336">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="215cf-336">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reduce-the-picked-quantity-of-completed-work-from-a-load"></a><span data-ttu-id="215cf-337">Izdotā pabeigtā darba daudzuma (no kravas) samazināšana</span><span class="sxs-lookup"><span data-stu-id="215cf-337">Reduce the picked quantity of completed work (from a load)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="215cf-338">Galvenie iestatīšanas parametri</span><span class="sxs-lookup"><span data-stu-id="215cf-338">Key setup parameter</span></span></th>
<th><span data-ttu-id="215cf-339">Partijas daudzums ir pieejams</span><span class="sxs-lookup"><span data-stu-id="215cf-339">Batch quantity is available</span></span></th>
<th><span data-ttu-id="215cf-340">Galvenās lietotāja darbības</span><span class="sxs-lookup"><span data-stu-id="215cf-340">Key user steps</span></span></th>
<th><span data-ttu-id="215cf-341">Noliktavas darbs</span><span class="sxs-lookup"><span data-stu-id="215cf-341">Warehouse work</span></span></th>
<th><span data-ttu-id="215cf-342">Ar pasūtījumu saistītas partijas rezervēšana</span><span class="sxs-lookup"><span data-stu-id="215cf-342">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="215cf-343">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="215cf-343">Not applicable</span></span></td>
<td><span data-ttu-id="215cf-344">Jā</span><span class="sxs-lookup"><span data-stu-id="215cf-344">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="215cf-345">Atveriet lapu <strong>Samazināt izdoto daudzumu</strong> no noslodzes rindas.</span><span class="sxs-lookup"><span data-stu-id="215cf-345">Open the <strong>Reduce picked quantity</strong> page from the load line.</span></span></li>
<li><span data-ttu-id="215cf-346">Ievadiet pilnu daudzumu, kuram tiks anulēta izdošana.</span><span class="sxs-lookup"><span data-stu-id="215cf-346">Enter the full quantity to unpick.</span></span></li>
<li><span data-ttu-id="215cf-347">Atlasiet "pārvietot uz" atrašanās vietu/noliktavas vienību.</span><span class="sxs-lookup"><span data-stu-id="215cf-347">Select a "move to" location/license plate.</span></span></li>
</ol>
</td>
<td>
<ul> 
<li><span data-ttu-id="215cf-348">Ar kravas rindu saistītais darbs ir atcelts.</span><span class="sxs-lookup"><span data-stu-id="215cf-348">Work that is associated with the load line is canceled.</span></span></li>
<li><span data-ttu-id="215cf-349">Jaunais krājuma pārvietošanas darbs ir izveidots un slēgts.</span><span class="sxs-lookup"><span data-stu-id="215cf-349">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="215cf-350">Daudzums ir atkārtoti rezervēts vienai partijai.</span><span class="sxs-lookup"><span data-stu-id="215cf-350">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="215cf-351">Sistēma nejaušās izlases veidā piešķir atrašanās vietu un noliktavas vienību (ja atrašanās vietu pārvalda noliktavas vienība), kurā ir pieejams daudzums.</span><span class="sxs-lookup"><span data-stu-id="215cf-351">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="215cf-352">Nē</span><span class="sxs-lookup"><span data-stu-id="215cf-352">No</span></span></td>
<td><span data-ttu-id="215cf-353">Skatīt iepriekšējo rindu.</span><span class="sxs-lookup"><span data-stu-id="215cf-353">See the previous row.</span></span></td>
<td><span data-ttu-id="215cf-354">Skatīt iepriekšējo rindu.</span><span class="sxs-lookup"><span data-stu-id="215cf-354">See the previous row.</span></span></td>
<td><span data-ttu-id="215cf-355">Daudzums ir atkārtoti rezervēts tai pašai partijai un tai pašai atrašanās vietai un noliktavas vienībai (ja atrašanās vietu pārvalda noliktavas vienība), kas tika ievadīta izdošanas anulēšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="215cf-355">The quantity is re-reserved for the same batch, and for the same location and license plate (if the location is license plate–controlled) that were entered during unpicking.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="move-an-item-within-a-warehouse"></a><span data-ttu-id="215cf-356">Krājuma pārvietošana noliktavā</span><span class="sxs-lookup"><span data-stu-id="215cf-356">Move an item within a warehouse</span></span>

> [!NOTE]
> <span data-ttu-id="215cf-357">Šī noliktavas darbība ir piemērojama tikai **Darba izveides procesa** tipa kustībai, nevis kustībai pēc veidnes.</span><span class="sxs-lookup"><span data-stu-id="215cf-357">This warehouse action is applicable only to movement of the **Work creation process** type, not to movement by template.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="215cf-358">Galvenie iestatīšanas parametri</span><span class="sxs-lookup"><span data-stu-id="215cf-358">Key setup parameter</span></span></th>
<th><span data-ttu-id="215cf-359">Partijas daudzums ir pieejams</span><span class="sxs-lookup"><span data-stu-id="215cf-359">Batch quantity is available</span></span></th>
<th><span data-ttu-id="215cf-360">Galvenās lietotāja darbības</span><span class="sxs-lookup"><span data-stu-id="215cf-360">Key user steps</span></span></th>
<th><span data-ttu-id="215cf-361">Noliktavas darbs</span><span class="sxs-lookup"><span data-stu-id="215cf-361">Warehouse work</span></span></th>
<th><span data-ttu-id="215cf-362">Ar pasūtījumu saistītas partijas rezervēšana</span><span class="sxs-lookup"><span data-stu-id="215cf-362">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="215cf-363">Darbiniekam ir aktivizēta opcija <strong>Atļaut krājumu kustību saistītajā tīklā</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-363">The <strong>Allow movement of inventory with associated work</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="215cf-364">Jā</span><span class="sxs-lookup"><span data-stu-id="215cf-364">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="215cf-365">Sākt kustību noliktavas programmā.</span><span class="sxs-lookup"><span data-stu-id="215cf-365">Start a movement on the warehousing app.</span></span></li>
<li><span data-ttu-id="215cf-366">Enter "no" un "uz" atrašanās vietas.</span><span class="sxs-lookup"><span data-stu-id="215cf-366">Enter "from" and "to" locations.</span></span></li>
</ol></td>
<td>
<ul>
<li><span data-ttu-id="215cf-367">Visā esošajā darbā, ko ietekmēja pārvietošana, izdošanas atrašanās vieta ir atjaunināta uz jaunu "uz" atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="215cf-367">On all existing work that is affected by the move, the pick location is updated to the new "to" location.</span></span></li>
<li><span data-ttu-id="215cf-368">Jaunais krājuma pārvietošanas darbs ir izveidots un slēgts.</span><span class="sxs-lookup"><span data-stu-id="215cf-368">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="215cf-369">Visas esošās rezervācijas, ko ietekmējusi daudzuma pārvietošana no dotās atrašanās vietas, ir rezervētas vienai partijai.</span><span class="sxs-lookup"><span data-stu-id="215cf-369">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch.</span></span> <span data-ttu-id="215cf-370">Sistēma nejaušās izlases veidā piešķir atrašanās vietu un noliktavas vienību (ja atrašanās vietu pārvalda noliktavas vienība), kurā ir pieejams daudzums.</span><span class="sxs-lookup"><span data-stu-id="215cf-370">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="215cf-371">Nē</span><span class="sxs-lookup"><span data-stu-id="215cf-371">No</span></span></td>
<td><span data-ttu-id="215cf-372">Skatīt iepriekšējo rindu.</span><span class="sxs-lookup"><span data-stu-id="215cf-372">See the previous row.</span></span></td>
<td><span data-ttu-id="215cf-373">Skatīt iepriekšējo rindu.</span><span class="sxs-lookup"><span data-stu-id="215cf-373">See the previous row.</span></span></td>
<td><span data-ttu-id="215cf-374">Visas esošās rezervācijas, ko ietekmējusi daudzuma pārvietošana no dotās atrašanās vietas, ir rezervētas tai pašai partijai un jaunai "uz" atrašanās vietai un noliktavas vienībai (ja atrašanās vietu pārvalda noliktavas vienība).</span><span class="sxs-lookup"><span data-stu-id="215cf-374">All existing reservations that are affected by the quantity movement from the given location are re-reserved for the same batch, and for the new "to" location and license plate (if the location is license plate–controlled).</span></span></td>
</tr>
</tbody>
</table>

#### <a name="reverse-the-picked-quantity-of-completed-work-from-a-load-or-a-wave"></a><span data-ttu-id="215cf-375">Izdotā pabeigtā darba daudzuma (no kravas vai kopuma) atsaukšana</span><span class="sxs-lookup"><span data-stu-id="215cf-375">Reverse the picked quantity of completed work (from a load or a wave)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="215cf-376">Galvenie iestatīšanas parametri</span><span class="sxs-lookup"><span data-stu-id="215cf-376">Key setup parameter</span></span></th>
<th><span data-ttu-id="215cf-377">Partijas daudzums ir pieejams</span><span class="sxs-lookup"><span data-stu-id="215cf-377">Batch quantity is available</span></span></th>
<th><span data-ttu-id="215cf-378">Galvenās lietotāja darbības</span><span class="sxs-lookup"><span data-stu-id="215cf-378">Key user steps</span></span></th>
<th><span data-ttu-id="215cf-379">Noliktavas darbs</span><span class="sxs-lookup"><span data-stu-id="215cf-379">Warehouse work</span></span></th>
<th><span data-ttu-id="215cf-380">Ar pasūtījumu saistītas partijas rezervēšana</span><span class="sxs-lookup"><span data-stu-id="215cf-380">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='6'><span data-ttu-id="215cf-381">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="215cf-381">Not applicable</span></span></td>
<td><span data-ttu-id="215cf-382">Jā</span><span class="sxs-lookup"><span data-stu-id="215cf-382">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="215cf-383">Atveriet lapu <strong>Atsaukt darbu</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-383">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="215cf-384">Pieprasījuma lapā atlasiet opciju <strong>Atstāt krājumus pašreizējā atrašanās vietā</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-384">On the request page, select the <strong>Leave items at current location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="215cf-385">Viss ar kravu saistītais darbs ir atcelts.</span><span class="sxs-lookup"><span data-stu-id="215cf-385">All work that is associated with the load is canceled.</span></span></td>
<td><span data-ttu-id="215cf-386">Daudzums ir atkārtoti rezervēts vienai partijai.</span><span class="sxs-lookup"><span data-stu-id="215cf-386">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="215cf-387">Sistēma nejaušās izlases veidā piešķir atrašanās vietu un noliktavas vienību (ja atrašanās vietu pārvalda noliktavas vienība), kurā ir pieejams daudzums.</span><span class="sxs-lookup"><span data-stu-id="215cf-387">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="215cf-388">Nē</span><span class="sxs-lookup"><span data-stu-id="215cf-388">No</span></span></td>
<td><span data-ttu-id="215cf-389">Skatīt iepriekšējo rindu.</span><span class="sxs-lookup"><span data-stu-id="215cf-389">See the previous row.</span></span></td>
<td><span data-ttu-id="215cf-390">Skatīt iepriekšējo rindu.</span><span class="sxs-lookup"><span data-stu-id="215cf-390">See the previous row.</span></span></td>
<td><span data-ttu-id="215cf-391">Daudzums tiek atkārtoti rezervēts vienai partijai, atrašanās vietai un noliktavas vienībai, kur daudzums tika atstāts atgriešanas brīdī.</span><span class="sxs-lookup"><span data-stu-id="215cf-391">The quantity is re-reserved for the same batch, and for the location and license plate where the quantity was left upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="215cf-392">Jā</span><span class="sxs-lookup"><span data-stu-id="215cf-392">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="215cf-393">Atveriet lapu <strong>Atsaukt darbu</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-393">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="215cf-394">Pieprasījuma lapā atlasiet opciju <strong>Piešķirt krājumus šai atrašanās vietai</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-394">On the request page, select the <strong>Assign items to this location</strong> option.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="215cf-395">Pašreizējais darbs ir atcelts.</span><span class="sxs-lookup"><span data-stu-id="215cf-395">The current work is canceled.</span></span></li>
<li><span data-ttu-id="215cf-396">Jaunais krājuma pārvietošanas darbs ir izveidots un slēgts.</span><span class="sxs-lookup"><span data-stu-id="215cf-396">New work for the inventory movement is created and closed.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="215cf-397">Daudzums ir atkārtoti rezervēts vienai partijai.</span><span class="sxs-lookup"><span data-stu-id="215cf-397">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="215cf-398">Sistēma nejaušās izlases veidā piešķir atrašanās vietu un noliktavas vienību (ja atrašanās vietu pārvalda noliktavas vienība), kurā ir pieejams daudzums.</span><span class="sxs-lookup"><span data-stu-id="215cf-398">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="215cf-399">Nē</span><span class="sxs-lookup"><span data-stu-id="215cf-399">No</span></span></td>
<td><span data-ttu-id="215cf-400">Skatīt iepriekšējo rindu.</span><span class="sxs-lookup"><span data-stu-id="215cf-400">See the previous row.</span></span></td>
<td><span data-ttu-id="215cf-401">Skatīt iepriekšējo rindu.</span><span class="sxs-lookup"><span data-stu-id="215cf-401">See the previous row.</span></span></td>
<td><span data-ttu-id="215cf-402">Daudzums tiek atkārtoti rezervēts vienai partijai, atrašanās vietai un noliktavas vienībai, kam daudzums tika piešķirts atcelšanas brīdī.</span><span class="sxs-lookup"><span data-stu-id="215cf-402">The quantity is re-reserved for the same batch, and for the location and license plate that the quantity was assigned to upon reversal.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="215cf-403">Jā/Nē</span><span class="sxs-lookup"><span data-stu-id="215cf-403">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="215cf-404">Atveriet lapu <strong>Atsaukt darbu</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-404">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="215cf-405">Pieprasījuma lapā atlasiet opciju <strong>Pārvietot krājumus uz šo atrašanās vietu</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-405">On the request page, select the <strong>Move items to this location</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="215cf-406">Atcelšana netiek atbalstīta.</span><span class="sxs-lookup"><span data-stu-id="215cf-406">Reversal isn't supported.</span></span></td>
<td><span data-ttu-id="215cf-407">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="215cf-407">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="215cf-408">Jā/Nē</span><span class="sxs-lookup"><span data-stu-id="215cf-408">Yes/No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="215cf-409">Atveriet lapu <strong>Atsaukt darbu</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-409">Open the <strong>Reverse work</strong> page.</span></span></li>
<li><span data-ttu-id="215cf-410">Pieprasījuma lapā atlasiet opciju <strong>Pārvietot krājumus, pamatojoties uz novietojuma direktīvām</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-410">On the request page, select the <strong>Move items based on location directives</strong> option.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="215cf-411">Atcelšana netiek atbalstīta.</span><span class="sxs-lookup"><span data-stu-id="215cf-411">Reversal isn't supported.</span></span> </td>
<td><span data-ttu-id="215cf-412">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="215cf-412">Not applicable</span></span></td>
</tr>
</tbody>
</table>

#### <a name="short-pick-a-quantity--register-the-quantity-as-physically-not-found-at-the-locationlicense-plate-while-you-perform-picking-work"></a><span data-ttu-id="215cf-413">Sīsināt izdošanas daudzumu – reģistrēt daudzumu kā fiziski neatrodamu novietojuma/noliktavas vienībā, kamēr veicat izdošanas darbu</span><span class="sxs-lookup"><span data-stu-id="215cf-413">Short-pick a quantity – Register the quantity as physically not found at the location/license plate while you perform picking work</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="215cf-414">Galvenie iestatīšanas parametri</span><span class="sxs-lookup"><span data-stu-id="215cf-414">Key setup parameter</span></span></th>
<th><span data-ttu-id="215cf-415">Partijas daudzums ir pieejams</span><span class="sxs-lookup"><span data-stu-id="215cf-415">Batch quantity is available</span></span></th>
<th><span data-ttu-id="215cf-416">Galvenās lietotāja darbības</span><span class="sxs-lookup"><span data-stu-id="215cf-416">Key user steps</span></span></th>
<th><span data-ttu-id="215cf-417">Noliktavas darbs</span><span class="sxs-lookup"><span data-stu-id="215cf-417">Warehouse work</span></span></th>
<th><span data-ttu-id="215cf-418">Ar pasūtījumu saistītas partijas rezervēšana</span><span class="sxs-lookup"><span data-stu-id="215cf-418">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="215cf-419">Ir iestatīts darba izņēmums ar <strong>Saīsinātās izdošanas</strong> tipu, kur <strong>Krājuma atkārtots sadalījums</strong> = <strong>Nav</strong>, <strong>Koriģēt krājumu</strong> = <strong>Jā</strong> un <strong>Noņemt rezervācijas</strong> = <strong>Nē</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-419">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span></td>
<td><span data-ttu-id="215cf-420">Jā</span><span class="sxs-lookup"><span data-stu-id="215cf-420">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="215cf-421">Kad palaižat izdošanas darbu, noliktavas programmā atlasiet izvēlnes elementu <strong>Saīsinātā izdošana</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-421">Select the <strong>Shortpick</strong> menu item on the warehousing app when you run picking work.</span></span></li>
<li><span data-ttu-id="215cf-422">Laukā <strong>Izdošanas daudzums</strong> ievadiet <strong>0</strong> (nulle).</span><span class="sxs-lookup"><span data-stu-id="215cf-422">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="215cf-423">Laukā <strong>Pamatojums</strong> ievadiet <strong>Nav atkārtotas sadales</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-423">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="215cf-424">Pašreizējais darbs tiek slēgts, un izdotais daudzums ir 0 (nulle).</span><span class="sxs-lookup"><span data-stu-id="215cf-424">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="215cf-425"><strong>Uzskaites</strong> tipa krājumu transakcija un <strong>Pārdošanas</strong> izsniegšanas veids tiek izveidots, lai attēlotu pielāgojumu.</span><span class="sxs-lookup"><span data-stu-id="215cf-425">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="215cf-426">Daudzums ir atkārtoti rezervēts vienai partijai.</span><span class="sxs-lookup"><span data-stu-id="215cf-426">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="215cf-427">Sistēma nejaušās izlases veidā piešķir atrašanās vietu un noliktavas vienību (ja atrašanās vietu pārvalda noliktavas vienība), kurā ir pieejams daudzums.</span><span class="sxs-lookup"><span data-stu-id="215cf-427">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="215cf-428">Nē</span><span class="sxs-lookup"><span data-stu-id="215cf-428">No</span></span></td>
<td><span data-ttu-id="215cf-429">Skatīt iepriekšējo rindu.</span><span class="sxs-lookup"><span data-stu-id="215cf-429">See the previous row.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="215cf-430">Saīsinātas izdošanas darbība neizdodas, un tiek izmesta kļūda.</span><span class="sxs-lookup"><span data-stu-id="215cf-430">The short-picking action fails, and an error is thrown.</span></span></li>
<li><span data-ttu-id="215cf-431">Pašreizējais darbs paliek atvērts.</span><span class="sxs-lookup"><span data-stu-id="215cf-431">The current work remains open.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="215cf-432">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="215cf-432">Not applicable</span></span></td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="215cf-433">Ir iestatīts darba izņēmums ar <strong>Saīsinātās izdošanas</strong> tipu, kur <strong>Krājuma atkārtots sadalījums</strong> = <strong>Nav</strong>, <strong>Koriģēt krājumu</strong> = <strong>Jā</strong> un <strong>Noņemt rezervācijas</strong> = <strong>Jā</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-433">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>None</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span></td>
<td><span data-ttu-id="215cf-434">Jā</span><span class="sxs-lookup"><span data-stu-id="215cf-434">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="215cf-435">Kad palaižat izdošanas darbu, noliktavas programmā atlasiet izvēlnes elementu <strong>Saīsinātā izdošana</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-435">Select the <strong>Shortpick</strong> menu item on the warehousing app when you run picking work.</span></span></li>
<li><span data-ttu-id="215cf-436">Laukā <strong>Izdošanas daudzums</strong> ievadiet <strong>0</strong> (nulle).</span><span class="sxs-lookup"><span data-stu-id="215cf-436">In the <strong>Pick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="215cf-437">Laukā <strong>Pamatojums</strong> ievadiet <strong>Nav atkārtotas sadales</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-437">In the <strong>Reason</strong> field, enter <strong>No reallocation</strong>.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="215cf-438">Pašreizējais darbs tiek slēgts, un izdotais daudzums ir 0 (nulle).</span><span class="sxs-lookup"><span data-stu-id="215cf-438">The current work is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="215cf-439"><strong>Uzskaites</strong> tipa krājumu transakcija un <strong>Pārdošanas</strong> izsniegšanas veids tiek izveidots, lai attēlotu pielāgojumu.</span><span class="sxs-lookup"><span data-stu-id="215cf-439">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="215cf-440">Visas esošās rezervācijas, ko ietekmējusi daudzuma koriģēšana saīsinātās izdošanas vietā, ir rezervētas vienai partijai.</span><span class="sxs-lookup"><span data-stu-id="215cf-440">All existing reservations that are affected by the quantity adjustment in the short-picked location are re-reserved for the same batch.</span></span> <span data-ttu-id="215cf-441">Sistēma nejaušās izlases veidā piešķir atrašanās vietu un noliktavas vienību (ja atrašanās vietu pārvalda noliktavas vienība), kurā ir pieejams daudzums.</span><span class="sxs-lookup"><span data-stu-id="215cf-441">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="215cf-442">Nē</span><span class="sxs-lookup"><span data-stu-id="215cf-442">No</span></span></td>
<td><span data-ttu-id="215cf-443">Skatīt iepriekšējo rindu.</span><span class="sxs-lookup"><span data-stu-id="215cf-443">See the previous row.</span></span></td>
<td><span data-ttu-id="215cf-444">Skatīt iepriekšējo rindu.</span><span class="sxs-lookup"><span data-stu-id="215cf-444">See the previous row.</span></span></td>
<td><span data-ttu-id="215cf-445">Visas esošās rezervācijas, ko ietekmējusi daudzuma koriģēšana saīsinātās izdošanas vietā, ir noņemtas.</span><span class="sxs-lookup"><span data-stu-id="215cf-445">All existing reservations that are affected by the quantity adjustment in the short-picked location are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="215cf-446">Ir iestatīts darba izņēmums ar <strong>Saīsinātās izdošanas</strong> tipu, kur <strong>Krājuma atkārtots sadalījums</strong> = <strong>Manuāls</strong>, <strong>Koriģēt krājumu</strong> = <strong>Jā</strong> un <strong>Noņemt rezervācijas</strong> = <strong>Nē/Jā</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-446">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No/Yes</strong>.</span></span> <span data-ttu-id="215cf-447">Turklāt darbiniekam tiek aktivizēta opcija <strong>Atļaut manuālu krājumu pārdalīšanu</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-447">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="215cf-448">Jā</span><span class="sxs-lookup"><span data-stu-id="215cf-448">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="215cf-449">Kad palaižat izdošanas darbu, noliktavas programmā atlasiet izvēlnes elementu <strong>Saīsinātā izdošana</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-449">Select the <strong>Shortpick</strong> menu item on the warehousing app when you run picking work.</span></span></li>
<li><span data-ttu-id="215cf-450">Laukā <strong>Saīsinātās izdošanas daudzums</strong> ievadiet <strong>0</strong> (nulle).</span><span class="sxs-lookup"><span data-stu-id="215cf-450">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="215cf-451">Laukā <strong>Pamatojums</strong> atlasiet <strong>Saīsinātā izdošana, izmantojot manuālu pārdalīšanu</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-451">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="215cf-452">Sarakstā atlasiet atrašanās vietu / noliktavas vienību.</span><span class="sxs-lookup"><span data-stu-id="215cf-452">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="215cf-453">Pašreizējā darbā tiek veiktas tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="215cf-453">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="215cf-454">Pašreizējā izdošanas līnija tiek slēgta, un izdotais daudzums ir 0 (nulle).</span><span class="sxs-lookup"><span data-stu-id="215cf-454">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="215cf-455">Novietošanas rinda ir atcelta.</span><span class="sxs-lookup"><span data-stu-id="215cf-455">The put line is canceled.</span></span></li>
<li><span data-ttu-id="215cf-456">Izveidota jauna izdošanas rinda.</span><span class="sxs-lookup"><span data-stu-id="215cf-456">A new pick line is created.</span></span> <span data-ttu-id="215cf-457">Tā izmanto atrašanās vietu / noliktavas vienību, ko izvēlējies lietotājs.</span><span class="sxs-lookup"><span data-stu-id="215cf-457">It uses the location/license plate that the user selected.</span></span></li>
<li><span data-ttu-id="215cf-458">Izveidota jauna novietošanas rinda.</span><span class="sxs-lookup"><span data-stu-id="215cf-458">A new put line is created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="215cf-459"><strong>Uzskaites</strong> tipa krājumu transakcija un <strong>Pārdošanas</strong> izsniegšanas veids tiek izveidots, lai attēlotu pielāgojumu.</span><span class="sxs-lookup"><span data-stu-id="215cf-459">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="215cf-460">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="215cf-460">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="215cf-461">Ir iestatīts darba izņēmums ar <strong>Saīsinātās izdošanas</strong> tipu, kur <strong>Krājuma atkārtots sadalījums</strong> = <strong>Manuāls</strong>, <strong>Koriģēt krājumu</strong> = <strong>Jā</strong> un <strong>Noņemt rezervācijas</strong> = <strong>Nē</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-461">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>No</strong>.</span></span> <span data-ttu-id="215cf-462">Turklāt darbiniekam tiek aktivizēta opcija <strong>Atļaut manuālu krājumu pārdalīšanu</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-462">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="215cf-463">Nr.</span><span class="sxs-lookup"><span data-stu-id="215cf-463">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="215cf-464">Kad palaižat izdošanas darbu, noliktavas programmā atlasiet izvēlnes elementu <strong>Saīsinātā izdošana</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-464">Select the <strong>Shortpick</strong> menu item on the warehousing app when you run picking work.</span></span></li>
<li><span data-ttu-id="215cf-465">Laukā <strong>Saīsinātās izdošanas daudzums</strong> ievadiet <strong>0</strong> (nulle).</span><span class="sxs-lookup"><span data-stu-id="215cf-465">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="215cf-466">Laukā <strong>Pamatojums</strong> atlasiet <strong>Saīsinātā izdošana, izmantojot manuālu pārdalīšanu</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-466">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="215cf-467">Saīsinātas izdošanas darbība neizdodas, un tiek izmesta kļūda.</span><span class="sxs-lookup"><span data-stu-id="215cf-467">The short-picking action fails, and an error is thrown.</span></span></td>
<td><span data-ttu-id="215cf-468">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="215cf-468">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="215cf-469">Ir iestatīts darba izņēmums ar <strong>Saīsinātās izdošanas</strong> tipu, kur <strong>Krājuma atkārtots sadalījums</strong> = <strong>Manuāls</strong>, <strong>Koriģēt krājumu</strong> = <strong>Jā</strong> un <strong>Noņemt rezervācijas</strong> = <strong>Jā</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-469">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Manual</strong>, <strong>Adjust inventory</strong> = <strong>Yes</strong>, and <strong>Remove reservations</strong> = <strong>Yes</strong>.</span></span> <span data-ttu-id="215cf-470">Turklāt darbiniekam tiek aktivizēta opcija <strong>Atļaut manuālu krājumu pārdalīšanu</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-470">Additionally, the <strong>Allow manual item reallocation</strong> option is enabled on the worker.</span></span></td>
<td><span data-ttu-id="215cf-471">Nr.</span><span class="sxs-lookup"><span data-stu-id="215cf-471">No</span></span></td>
<td>
<ol>
<li><span data-ttu-id="215cf-472">Kad palaižat izdošanas darbu, noliktavas programmā atlasiet izvēlnes elementu <strong>Saīsinātā izdošana</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-472">Select the <strong>Shortpick</strong> menu item on the warehousing app when you run picking work.</span></span></li>
<li><span data-ttu-id="215cf-473">Laukā <strong>Saīsinātās izdošanas daudzums</strong> ievadiet <strong>0</strong> (nulle).</span><span class="sxs-lookup"><span data-stu-id="215cf-473">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="215cf-474">Laukā <strong>Pamatojums</strong> atlasiet <strong>Saīsinātā izdošana, izmantojot manuālu pārdalīšanu</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-474">In the <strong>Reason</strong> field, select <strong>Short Picking with manual reallocation</strong>.</span></span></li>
<li><span data-ttu-id="215cf-475">Sarakstā atlasiet atrašanās vietu / noliktavas vienību.</span><span class="sxs-lookup"><span data-stu-id="215cf-475">Select the location/license plate in the list.</span></span></li>
</ol>
</td>
<td>
<ul>
<li><span data-ttu-id="215cf-476">Pašreizējā darbā tiek veiktas tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="215cf-476">On the current work, the following actions occur:</span></span>
<ul>
<li><span data-ttu-id="215cf-477">Pašreizējā izdošanas līnija tiek slēgta, un izdotais daudzums ir 0 (nulle).</span><span class="sxs-lookup"><span data-stu-id="215cf-477">The pick line is closed, and the picked quantity is 0 (zero).</span></span></li>
<li><span data-ttu-id="215cf-478">Novietošanas rinda ir atcelta.</span><span class="sxs-lookup"><span data-stu-id="215cf-478">The put line is canceled.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="215cf-479"><strong>Uzskaites</strong> tipa krājumu transakcija un <strong>Pārdošanas</strong> izsniegšanas veids tiek izveidots, lai attēlotu pielāgojumu.</span><span class="sxs-lookup"><span data-stu-id="215cf-479">An inventory transaction of the <strong>Counting</strong> type and the <strong>Sold</strong> issue type is created to represent the adjustment.</span></span></li>
</ul>
</td>
<td><span data-ttu-id="215cf-480">Visas esošās rezervācijas, ko ietekmējusi daudzuma koriģēšana saīsinātās izdošanas vietā / noliktavas vienībā, ir noņemtas.</span><span class="sxs-lookup"><span data-stu-id="215cf-480">All existing reservations that are affected by the quantity adjustment in the short-picked location/license plate are removed.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="215cf-481">Ir iestatīts darba izņēmums ar <strong>Saīsinātās izdošanas</strong> tipu, kur <strong>Krājuma atkārtots sadalījums</strong> = <strong>Automātisks</strong>, <strong>Koriģēt krājumu</strong> = <strong>Jā</strong> un <strong>Noņemt rezervācijas</strong> = <strong>Jā/Nē</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-481">A work exception of the <strong>Short pick</strong> type is set up, where <strong>Item reallocation</strong> = <strong>Automatic</strong>, <strong>Adjust inventory</strong> = <strong>Yes/No</strong>, and <strong>Remove reservations</strong> = <strong>Yes/No</strong>.</span></span></td>
<td><span data-ttu-id="215cf-482">Nav attiecināms</span><span class="sxs-lookup"><span data-stu-id="215cf-482">Not applicable</span></span></td>
<td>
<ol>
<li><span data-ttu-id="215cf-483">Kad palaižat izdošanas darbu, noliktavas programmā atlasiet izvēlnes elementu <strong>Saīsinātā izdošana</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-483">Select the <strong>Shortpick</strong> menu item on the warehousing app when you run picking work.</span></span></li>
<li><span data-ttu-id="215cf-484">Laukā <strong>Saīsinātās izdošanas daudzums</strong> ievadiet <strong>0</strong> (nulle).</span><span class="sxs-lookup"><span data-stu-id="215cf-484">In the <strong>Shortpick Quantity</strong> field, enter <strong>0</strong> (zero).</span></span></li>
<li><span data-ttu-id="215cf-485">Laukā <strong>Pamatojums</strong> atlasiet <strong>Saīsinātā izdošana, izmantojot automātisku pārdalīšanu</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-485">In the <strong>Reason</strong> field, select <strong>Short Picking with automatic reallocation</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="215cf-486">Saīsināta izdošana, kas ietver automātisku pārdalīšanu, netiek atbalstīta.</span><span class="sxs-lookup"><span data-stu-id="215cf-486">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
<td><span data-ttu-id="215cf-487">Saīsināta izdošana, kas ietver automātisku pārdalīšanu, netiek atbalstīta.</span><span class="sxs-lookup"><span data-stu-id="215cf-487">Short-picking that involves automatic reallocation isn't supported.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="change-the-inventory-status"></a><span data-ttu-id="215cf-488">Mainīt krājuma statusu</span><span class="sxs-lookup"><span data-stu-id="215cf-488">Change the inventory status</span></span>

> [!NOTE]
> <span data-ttu-id="215cf-489">Šo noliktavas darbību var veikt no vairākiem ieejas punktiem.</span><span class="sxs-lookup"><span data-stu-id="215cf-489">This warehouse action can be performed from multiple entry points.</span></span> <span data-ttu-id="215cf-490">Šeit redzamajā piemēra izmantota darbība **Krājumu statusa maiņa** lapā **Rīcībā esošie krājumi pēc atrašanās vietas**.</span><span class="sxs-lookup"><span data-stu-id="215cf-490">The example that is shown here uses **Inventory status change** action on the **On-hand by location** page.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="215cf-491">Galvenie iestatīšanas parametri</span><span class="sxs-lookup"><span data-stu-id="215cf-491">Key setup parameter</span></span></th>
<th><span data-ttu-id="215cf-492">Partijas daudzums ir pieejams</span><span class="sxs-lookup"><span data-stu-id="215cf-492">Batch quantity is available</span></span></th>
<th><span data-ttu-id="215cf-493">Galvenās lietotāja darbības</span><span class="sxs-lookup"><span data-stu-id="215cf-493">Key user steps</span></span></th>
<th><span data-ttu-id="215cf-494">Noliktavas darbs</span><span class="sxs-lookup"><span data-stu-id="215cf-494">Warehouse work</span></span></th>
<th><span data-ttu-id="215cf-495">Ar pasūtījumu saistītas partijas rezervēšana</span><span class="sxs-lookup"><span data-stu-id="215cf-495">Order-committed batch reservation</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan='2'><span data-ttu-id="215cf-496">Cilnē <strong>Noliktava</strong>, ierakstā <strong>Noliktava</strong> lauks <strong>Noņemt rezervācijas un atzīmes</strong> ir iestatīts uz <strong>Rezervācijas</strong> vai <strong>Atzīmes un rezervācijas</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-496">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>Reservations</strong> or <strong>Markings and reservations</strong>.</span></span></td>
<td><span data-ttu-id="215cf-497">Jā</span><span class="sxs-lookup"><span data-stu-id="215cf-497">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="215cf-498">Atlasiet noteiktu atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="215cf-498">Select a specific location.</span></span></li>
<li><span data-ttu-id="215cf-499">Atlasiet rindu, kurai ir noteikts krājums, atrašānās vieta un noliktavas vienība (ja atrašanās vietu pārvalda noliktavas vienība).</span><span class="sxs-lookup"><span data-stu-id="215cf-499">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="215cf-500">Atlasiet <strong>Krājumu statusa maiņa</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-500">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="215cf-501">Iestatiet lauku <strong>Krājuma statuss</strong> uz <strong>Bloķēšana</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-501">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="215cf-502">Krājumu statusa izmaiņas nav atļautas daudzumiem, kas ir rezervēti darbam.</span><span class="sxs-lookup"><span data-stu-id="215cf-502">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="215cf-503">Daudzums ir atkārtoti rezervēts vienai partijai.</span><span class="sxs-lookup"><span data-stu-id="215cf-503">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="215cf-504">Sistēma nejaušās izlases veidā piešķir atrašanās vietu un noliktavas vienību (ja atrašanās vietu pārvalda noliktavas vienība), kurā ir pieejams daudzums.</span><span class="sxs-lookup"><span data-stu-id="215cf-504">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></li>
<li><span data-ttu-id="215cf-505">Lai attēlotu izmaiņas krājumu statusa dimensijā, izveidotas divas <strong>Krājumu statusa maiņas</strong> tipa krājumu transakcijas.</span><span class="sxs-lookup"><span data-stu-id="215cf-505">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="215cf-506">Lai attēlotu bloķētā daudzuma rezervāciju, izveidota <strong>Krājuma bloķēšanas</strong> tipa krājumu transakcija un <strong>Rezervēts fiziski</strong> izsniegšanas veids.</span><span class="sxs-lookup"><span data-stu-id="215cf-506">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="215cf-507">Nē</span><span class="sxs-lookup"><span data-stu-id="215cf-507">No</span></span></td>
<td><span data-ttu-id="215cf-508">Skatīt iepriekšējo rindu.</span><span class="sxs-lookup"><span data-stu-id="215cf-508">See the previous row.</span></span></td>
<td><span data-ttu-id="215cf-509">Krājumu statusa izmaiņas nav atļautas daudzumiem, kas ir rezervēti darbam.</span><span class="sxs-lookup"><span data-stu-id="215cf-509">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="215cf-510">Rezervēšana tiek noņemta.</span><span class="sxs-lookup"><span data-stu-id="215cf-510">The reservation is removed.</span></span></li>
<li><span data-ttu-id="215cf-511">Lai attēlotu izmaiņas krājumu statusa dimensijā, izveidotas divas <strong>Krājumu statusa maiņas</strong> tipa krājumu transakcijas.</span><span class="sxs-lookup"><span data-stu-id="215cf-511">Two inventory transactions of the <strong>Inventory status change</strong> type are created to represent the change in the inventory status dimension.</span></span></li>
<li><span data-ttu-id="215cf-512">Lai attēlotu bloķētā daudzuma rezervāciju, izveidota <strong>Krājuma bloķēšanas</strong> tipa krājumu transakcija un <strong>Rezervēts fiziski</strong> izsniegšanas veids.</span><span class="sxs-lookup"><span data-stu-id="215cf-512">An inventory transaction of the <strong>Inventory blocking</strong> type and the <strong>Reserved physical</strong> issue type is created to represent the reservation of the blocked quantity.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td rowspan='2'><span data-ttu-id="215cf-513">Cilnē <strong>Noliktava</strong>, ierakstā <strong>Noliktava</strong> lauks <strong>Noņemt rezervācijas un atzīmes</strong> ir iestatīts uz <strong>Nav</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-513">On the <strong>Warehouse</strong> tab, in the <strong>Warehouse</strong> record, the <strong>Remove reservations and markings</strong> field is set to <strong>None</strong>.</span></span></td>
<td><span data-ttu-id="215cf-514">Jā</span><span class="sxs-lookup"><span data-stu-id="215cf-514">Yes</span></span></td>
<td>
<ol>
<li><span data-ttu-id="215cf-515">Atlasiet noteiktu atrašanās vietu.</span><span class="sxs-lookup"><span data-stu-id="215cf-515">Select a specific location.</span></span></li>
<li><span data-ttu-id="215cf-516">Atlasiet rindu, kurai ir noteikts krājums, atrašānās vieta un noliktavas vienība (ja atrašanās vietu pārvalda noliktavas vienība).</span><span class="sxs-lookup"><span data-stu-id="215cf-516">Select a line that has a specific item, location, and license plate (if the location is license plate–controlled).</span></span></li>
<li><span data-ttu-id="215cf-517">Atlasiet <strong>Krājumu statusa maiņa</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-517">Select <strong>Inventory status change</strong>.</span></span></li>
<li><span data-ttu-id="215cf-518">Iestatiet lauku <strong>Krājuma statuss</strong> uz <strong>Bloķēšana</strong>.</span><span class="sxs-lookup"><span data-stu-id="215cf-518">Set the <strong>Inventory status</strong> field to <strong>Blocking</strong>.</span></span></li>
</ol>
</td>
<td><span data-ttu-id="215cf-519">Krājumu statusa izmaiņas nav atļautas daudzumiem, kas ir rezervēti darbam.</span><span class="sxs-lookup"><span data-stu-id="215cf-519">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="215cf-520">Daudzums ir atkārtoti rezervēts vienai partijai.</span><span class="sxs-lookup"><span data-stu-id="215cf-520">The quantity is re-reserved for the same batch.</span></span> <span data-ttu-id="215cf-521">Sistēma nejaušās izlases veidā piešķir atrašanās vietu un noliktavas vienību (ja atrašanās vietu pārvalda noliktavas vienība), kurā ir pieejams daudzums.</span><span class="sxs-lookup"><span data-stu-id="215cf-521">The system randomly assigns a location and license plate (if the location is license plate–controlled) where the quantity is available.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="215cf-522">Nē</span><span class="sxs-lookup"><span data-stu-id="215cf-522">No</span></span></td>
<td><span data-ttu-id="215cf-523">Skatīt iepriekšējo rindu.</span><span class="sxs-lookup"><span data-stu-id="215cf-523">See the previous row.</span></span></td>
<td><span data-ttu-id="215cf-524">Krājumu statusa izmaiņas nav atļautas daudzumiem, kas ir rezervēti darbam.</span><span class="sxs-lookup"><span data-stu-id="215cf-524">Inventory status changes aren't allowed for quantities that are reserved for work.</span></span></td>
<td><span data-ttu-id="215cf-525">Krājumu statusa izmaiņas nav atļautas.</span><span class="sxs-lookup"><span data-stu-id="215cf-525">Inventory status changes aren't allowed.</span></span></td>
</tr>
</tbody>
</table>

## <a name="limitations"></a><span data-ttu-id="215cf-526">Ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="215cf-526">Limitations</span></span>

- <span data-ttu-id="215cf-527">Pielāgojama noliktavas līmeņa dimensiju rezervēšanas funkcionalitāte neatbalsta tālāk norādītos līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="215cf-527">The flexible warehouse-level dimension reservation functionality doesn't support the following features:</span></span>

    - <span data-ttu-id="215cf-528">Pieļaujamā svara pārvaldība</span><span class="sxs-lookup"><span data-stu-id="215cf-528">Catch weight management</span></span>
    - <span data-ttu-id="215cf-529">Negatīvi fiziskie krājumi</span><span class="sxs-lookup"><span data-stu-id="215cf-529">Physical negative inventory</span></span>
    - <span data-ttu-id="215cf-530">Rezervēšana pret pasūtīto piegādi</span><span class="sxs-lookup"><span data-stu-id="215cf-530">Reservation against ordered supply</span></span>
    - <span data-ttu-id="215cf-531">Pārsūtīšanas pasūtījumi un izejmateriālu izdošana</span><span class="sxs-lookup"><span data-stu-id="215cf-531">Transfer orders and raw material picking</span></span>

- <span data-ttu-id="215cf-532">Konteineru konsolidācijas kārtulai par iepakošanu pēc direktīvas vienības ir ierobežojumi.</span><span class="sxs-lookup"><span data-stu-id="215cf-532">The container consolidation rule for packing by directive unit has limitations.</span></span> <span data-ttu-id="215cf-533">Ar pasūtījumu saistītām rezervācijām mēs iesakām neizmantot konteineru veidošanas veidnes, kur ir iespējots lauks **Iepakot pēc direktīvas vienības**.</span><span class="sxs-lookup"><span data-stu-id="215cf-533">For order-committed reservations, we recommend that you not use container build templates where the **Pack by directive unit** field is enabled.</span></span> <span data-ttu-id="215cf-534">Pašreizējā versija novietojuma direktīvas netiek izmantotas, kad tiek izveidots noliktavas darbs.</span><span class="sxs-lookup"><span data-stu-id="215cf-534">In the current design, location directives aren't used when warehouse work is created.</span></span> <span data-ttu-id="215cf-535">Tāpēc konteinerizācijas kopuma darbības laikā tiek lietota tikai viszemākā vienība vienību secību grupā (krājumu uzskaites vienība).</span><span class="sxs-lookup"><span data-stu-id="215cf-535">Therefore, only the lowest unit in the unit sequence group (the inventory unit) is applied during the containerization wave step.</span></span>
