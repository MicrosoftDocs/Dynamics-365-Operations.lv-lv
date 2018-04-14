---
title: "Izdevumu pārvaldības konfigurēšana"
description: "Šajā rakstā ir aprakstīti apsvērumi un lēmumi, kas jums ir jāpieņem plānošanas procesa laikā pirms izdevumu pārvaldības konfigurēšanas programmatūras Microsoft Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: aa7c7bfaf4301904e1b7ae242efaf8b660fb076a
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---

# <a name="configure-expense-management"></a><span data-ttu-id="b5e84-103">Izdevumu pārvaldības konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="b5e84-103">Configure expense management</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="b5e84-104">Šajā tēmā ir aprakstīti apsvērumi un lēmumi, kas jums ir jāpieņem plānošanas procesa laikā pirms izdevumu pārvaldības konfigurēšanas programmatūras Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b5e84-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="b5e84-105">Modulī Izdevumu pārvaldība jūs tostarp varat glabāt informāciju par maksāšanas metodēm, komandējumu pieprasījumiem, izdevumu pārskatiem, politikām un citiem faktoriem.</span><span class="sxs-lookup"><span data-stu-id="b5e84-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="b5e84-106">Tā kā daudzi lēmumi, ko pieņemat, kad plānojat savu izdevumu pārvaldības konfigurāciju, ir atkarīgi no jūsu organizācijas hierarhijas un finanšu struktūras, jums ir nepieciešams skatīt plānošanas dokumentus šiem apgabaliem.</span><span class="sxs-lookup"><span data-stu-id="b5e84-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="b5e84-107">Starpuzņēmumu izdevumi</span><span class="sxs-lookup"><span data-stu-id="b5e84-107">Intercompany expenses</span></span>

<span data-ttu-id="b5e84-108">Kad iespējojat starpuzņēmumu izdevumus, jūs juridiskajām personām un darbiniekiem ļaujat radīt izdevumus citas juridiskās personas vārdā un iekasēt maksājumus no citas nodarbinātības juridiskās personas jūsu organizācijas ietvaros.</span><span class="sxs-lookup"><span data-stu-id="b5e84-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="b5e84-109">Piemēram, kāds darbinieks juridiskajā personā A pabeidz projektu juridiskajai personai B un projekta gaitā rodas ar komandējumu saistīti izdevumi.</span><span class="sxs-lookup"><span data-stu-id="b5e84-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="b5e84-110">Ja ir aktivizēti starpuzņēmumu izdevumi, tad darbinieks var iesniegt izdevumu pārskatu, kurā ir grāmatoti izdevumi juridiskajai personai B, un pēc tam šie izdevumi ir jāapmaksā juridiskajai personai A. Ja jūsu organizācijai nav vairākas juridiskās personas, tad starpuzņēmumu izdevumus nav nepieciešams iespējot.</span><span class="sxs-lookup"><span data-stu-id="b5e84-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="b5e84-111">**Lēmums:** Vai vēlaties iespējot starpuzņēmumu izdevumus?</span><span class="sxs-lookup"><span data-stu-id="b5e84-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="b5e84-112">Finanšu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="b5e84-112">Financial management</span></span>

<span data-ttu-id="b5e84-113">Izdevumu pārvaldība ir cieši integrēta jūsu organizācijas finanšu pārvaldībā.</span><span class="sxs-lookup"><span data-stu-id="b5e84-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="b5e84-114">Liela daļa jūsu konfigurācijas attiecībā uz moduli Izdevumu pārvaldība būs atkarīga no lēmumiem, ko esat pieņēmis par savas organizācijas finansēm.</span><span class="sxs-lookup"><span data-stu-id="b5e84-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="b5e84-115">Nākamajās sadaļās ir aprakstīti dažādie apgabali, kuriem ir nepieciešama plānošana un lēmumi, balstoties uz jūsu organizācijas finanšu lēmumiem un norādījumiem no vadības grupas.</span><span class="sxs-lookup"><span data-stu-id="b5e84-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="b5e84-116">Dienasnauda</span><span class="sxs-lookup"><span data-stu-id="b5e84-116">Per diems</span></span>

<span data-ttu-id="b5e84-117">Ir nepieciešams definēt darbinieku dienasnaudas, ko nodrošina jūsu organizācija.</span><span class="sxs-lookup"><span data-stu-id="b5e84-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="b5e84-118">Tā kā dienasnaudas parasti tiek izmantotas, lai segtu tādus izdevumus kā maltītes, izmitināšana un citi gadījuma izdevumi, varat izveidot kārtulas attiecībā uz dienasnaudas piemaksām, jūsu organizācija piedāvā.</span><span class="sxs-lookup"><span data-stu-id="b5e84-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="b5e84-119">Dienasnaudas likmes var būt balstītas uz gada laiku, komandējuma vietu vai uz abiem.</span><span class="sxs-lookup"><span data-stu-id="b5e84-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="b5e84-120">Kad definējat dienasnaudas kārtulu, varat norādīt, ka tiek ieturēts procentuāls daudzums no dienas naudas, ja darbinieks saņem brīvpusdienas vai bezmaksas pakalpojumus.</span><span class="sxs-lookup"><span data-stu-id="b5e84-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="b5e84-121">Varat arī definēt dienasnaudas likmju pakāpes, lai iestatītu minimālo un maksimālo stundu skaitu, kādam dienasnaudas likmes var lietot attiecībā uz darbinieka komandējumu.</span><span class="sxs-lookup"><span data-stu-id="b5e84-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="b5e84-122">**Lēmumi:**</span><span class="sxs-lookup"><span data-stu-id="b5e84-122">**Decisions:**</span></span>

- <span data-ttu-id="b5e84-123">Noklusējuma dienasnaudas kārtulas pirmajai un pēdējai dienai:</span><span class="sxs-lookup"><span data-stu-id="b5e84-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="b5e84-124">Kāds ir minimālais stundu skaits, ko darbinieks var pieprasīt vienai dienai un joprojām saņemt dienasnaudu?</span><span class="sxs-lookup"><span data-stu-id="b5e84-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="b5e84-125">Vai tiek samazināta summa, kas tiek piedāvāta par ēdināšanu pirmajā dienā un pēdējā dienā?</span><span class="sxs-lookup"><span data-stu-id="b5e84-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="b5e84-126">Ja pastāv samazinājums — kāds ir samazinājuma procentuālais daudzums?</span><span class="sxs-lookup"><span data-stu-id="b5e84-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="b5e84-127">Vai tiek samazināta summa, kas tiek piedāvāta par viesnīcas izdevumiem pirmajā dienā un pēdējā dienā?</span><span class="sxs-lookup"><span data-stu-id="b5e84-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="b5e84-128">Ja pastāv samazinājums — kāds ir samazinājuma procentuālais daudzums?</span><span class="sxs-lookup"><span data-stu-id="b5e84-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="b5e84-129">Vai tiek samazināta summa, kas tiek piedāvāta par citiem izdevumiem, kas ir radušies pirmajā dienā un pēdējā dienā?</span><span class="sxs-lookup"><span data-stu-id="b5e84-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="b5e84-130">Ja pastāv samazinājums — kāds ir samazinājuma procentuālais daudzums?</span><span class="sxs-lookup"><span data-stu-id="b5e84-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="b5e84-131">Noklusējuma dienasnaudas kārtulas:</span><span class="sxs-lookup"><span data-stu-id="b5e84-131">Default per diem rules:</span></span>

    - <span data-ttu-id="b5e84-132">Vai notiek procentuāla dienasnaudas piemaksas samazināšana par katru maltīti, ja, piemēram, maltītes ir bez maksas?</span><span class="sxs-lookup"><span data-stu-id="b5e84-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="b5e84-133">Ja pastāv samazinājums — kāds ir samazinājuma procentuālais daudzums katrai maltītei?</span><span class="sxs-lookup"><span data-stu-id="b5e84-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="b5e84-134">Vai ēdināšanas samazinājums tiek rēķinātas par dienu, pa braucienu vai par maltīšu skaitu dienā?</span><span class="sxs-lookup"><span data-stu-id="b5e84-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="b5e84-135">Vai dienasnaudas summas ir jānoapaļo parastajā veidā vai uz augšu?</span><span class="sxs-lookup"><span data-stu-id="b5e84-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="b5e84-136">Vai dienasnaudas tiek rēķinātas 24 stundu periodam vai kalendārajai dienai?</span><span class="sxs-lookup"><span data-stu-id="b5e84-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="b5e84-137">No atrašanās vietas atkarīgās dienasnaudas kārtulas:</span><span class="sxs-lookup"><span data-stu-id="b5e84-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="b5e84-138">Vai dienasnaudas likmes atšķiras atkarībā no atrašanās vietas?</span><span class="sxs-lookup"><span data-stu-id="b5e84-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="b5e84-139">Kādas atrašanās vietas ir ietvertas?</span><span class="sxs-lookup"><span data-stu-id="b5e84-139">What locations are included?</span></span>
    - <span data-ttu-id="b5e84-140">Ja dienasnaudas likmes atšķiras atkarībā no atrašanās vietas, tad kāds procentuālais daudzums katrai atrašanās vietai tiek nodrošināts par tālāk norādītajiem izdevumu tipiem.</span><span class="sxs-lookup"><span data-stu-id="b5e84-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="b5e84-141">Maltītes</span><span class="sxs-lookup"><span data-stu-id="b5e84-141">Meals</span></span>
        - <span data-ttu-id="b5e84-142">Viesnīca</span><span class="sxs-lookup"><span data-stu-id="b5e84-142">Hotel</span></span>
        - <span data-ttu-id="b5e84-143">Citi izdevumi</span><span class="sxs-lookup"><span data-stu-id="b5e84-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="b5e84-144">Izdevumu pārvaldības žurnāli un konti</span><span class="sxs-lookup"><span data-stu-id="b5e84-144">Expense management journals and accounts</span></span>

<span data-ttu-id="b5e84-145">Izdevumu pārvaldībai ir nepieciešams, lai jūs izmantotu vairākus žurnālus un kontus.</span><span class="sxs-lookup"><span data-stu-id="b5e84-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="b5e84-146">Jums ir jāizlemj, piemēram, vai to pašu kontu izmantot naudas avansiem un kredītkaršu domstarpībām.</span><span class="sxs-lookup"><span data-stu-id="b5e84-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="b5e84-147">**Lēmumi:**</span><span class="sxs-lookup"><span data-stu-id="b5e84-147">**Decisions:**</span></span>

- <span data-ttu-id="b5e84-148">Kurā virsgrāmatas žurnālā tiek grāmatotas apstiprināto izdevumu atskaites?</span><span class="sxs-lookup"><span data-stu-id="b5e84-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="b5e84-149">Kurš konts tiek izmantots naudas avansiem?</span><span class="sxs-lookup"><span data-stu-id="b5e84-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="b5e84-150">Vai naudas avansi ir jāgrāmato nekavējoties?</span><span class="sxs-lookup"><span data-stu-id="b5e84-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="b5e84-151">Maksājuma metodes</span><span class="sxs-lookup"><span data-stu-id="b5e84-151">Payment methods</span></span>

<span data-ttu-id="b5e84-152">Kad darbiniekiem ļaujat radīt izdevumus jūsu uzņēmuma vārdā, jums ir nepieciešams definēt maksājumu metodes, ko darbiniekiem ir atļauts lietot.</span><span class="sxs-lookup"><span data-stu-id="b5e84-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="b5e84-153">Piemēram, darbiniekiem varat ļaut izmantot skaidru naudu vai korporatīvo kredītkarti.</span><span class="sxs-lookup"><span data-stu-id="b5e84-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="b5e84-154">Tāpat darbiniekiem varat ļaut arī izmantot personiskās kredītkartes un pēc tam šiem darbiniekiem kompensēt izdevumus.</span><span class="sxs-lookup"><span data-stu-id="b5e84-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="b5e84-155">Attiecībā uz katru maksājumu metodi, kuru atļaujat, jums ir jāpieņem tālāk norādītie lēmumi.</span><span class="sxs-lookup"><span data-stu-id="b5e84-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="b5e84-156">**Lēmumi:**</span><span class="sxs-lookup"><span data-stu-id="b5e84-156">**Decisions:**</span></span>

- <span data-ttu-id="b5e84-157">Kādas maksāšanas metodes ir atļautas?</span><span class="sxs-lookup"><span data-stu-id="b5e84-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="b5e84-158">Kam pieder maksāšanas metodes izdevumi?</span><span class="sxs-lookup"><span data-stu-id="b5e84-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="b5e84-159">Vai pastāv korespondējošā konta tips?</span><span class="sxs-lookup"><span data-stu-id="b5e84-159">Is there an offset account type?</span></span> <span data-ttu-id="b5e84-160">Ja pastāv korespondējošā konta tips — kāds tas ir?</span><span class="sxs-lookup"><span data-stu-id="b5e84-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="b5e84-161">Ja pastāv korespondējošais konts — kas ir šis konts?</span><span class="sxs-lookup"><span data-stu-id="b5e84-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="b5e84-162">Ja maksāšanas metode ir kredītkarte, vai maksāšanas metode ir jāizmanto tikai ar importētajām transakcijām?</span><span class="sxs-lookup"><span data-stu-id="b5e84-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="b5e84-163">Izdevumu kategorijas un koplietojamās kategorijas</span><span class="sxs-lookup"><span data-stu-id="b5e84-163">Expense categories and shared categories</span></span>

<span data-ttu-id="b5e84-164">Kad darbinieki izveido izdevumu atskaiti, katram viņu reģistrētajam izdevumam ir jābūt saistītam ar kādu izdevumu kategoriju.</span><span class="sxs-lookup"><span data-stu-id="b5e84-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="b5e84-165">Izdevumu kategorijas tiek atvasinātas no koplietojamajām kategorijām, kuras var koplietot dažādās juridiskajās personās jūsu organizācijā.</span><span class="sxs-lookup"><span data-stu-id="b5e84-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="b5e84-166">Atkarībā no veida, kā jūsu organizācija ir definēta, šīs kategorijas ir iespējams kopīgot arī modulī Projektu vadība un uzskaite.</span><span class="sxs-lookup"><span data-stu-id="b5e84-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="b5e84-167">Pamatojoties uz jūsu organizācijas definīciju un norādījumiem no ieviešanas grupas, nosakiet, vai kategorijas, kuras tiek izmantotas modulī Izdevumu pārvaldība, ir jāizmanto tikai modulī Izdevumu pārvaldība, vai arī tās ir nepieciešams koplietot starp moduli Projektu vadība un uzskaite un moduli Izdevumu pārvaldība.</span><span class="sxs-lookup"><span data-stu-id="b5e84-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="b5e84-168">Ņemiet vērā, ka šīs kategorijas var koplietot starp moduļiem Projekts un Izdevumi vai Projekts un Ražošana, bet ne starp Izdevumi un Ražošana.</span><span class="sxs-lookup"><span data-stu-id="b5e84-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="b5e84-169">Par katru izdevumu kategoriju jums ir jāpieņem tālāk norādītie lēmumi.</span><span class="sxs-lookup"><span data-stu-id="b5e84-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="b5e84-170">**Lēmumi:**</span><span class="sxs-lookup"><span data-stu-id="b5e84-170">**Decisions:**</span></span>

- <span data-ttu-id="b5e84-171">Kas ir izdevumu kategorija?</span><span class="sxs-lookup"><span data-stu-id="b5e84-171">What is the expense category?</span></span> <span data-ttu-id="b5e84-172">Piemēri ir kategorijas lidojumiem, viesnīcām vai attālumam.</span><span class="sxs-lookup"><span data-stu-id="b5e84-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="b5e84-173">Vai izdevumu kategoriju var izmantot arī modulī Projektu vadība un uzskaite?</span><span class="sxs-lookup"><span data-stu-id="b5e84-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="b5e84-174">Kas ir izdevumu tips?</span><span class="sxs-lookup"><span data-stu-id="b5e84-174">What is the expense type?</span></span>
- <span data-ttu-id="b5e84-175">Kas ir noklusējuma maksāšanas metode izdevumu kategorijai?</span><span class="sxs-lookup"><span data-stu-id="b5e84-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="b5e84-176">Vai izdevumi šajā izdevumu kategorijā ir jāuzskaita?</span><span class="sxs-lookup"><span data-stu-id="b5e84-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="b5e84-177">Kas ir galvenais noklusējuma konts izdevumu kategorijai?</span><span class="sxs-lookup"><span data-stu-id="b5e84-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="b5e84-178">Kas ir noklusējuma krājumu pārdošanas nodokļu grupa izdevumu kategorijai?</span><span class="sxs-lookup"><span data-stu-id="b5e84-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="b5e84-179">Vai izdevumu kategorijai ir atļautas papildu maksāšanas metodes?</span><span class="sxs-lookup"><span data-stu-id="b5e84-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="b5e84-180">Ja ir atļautas papildu maksāšanas metodes — kādas tās ir?</span><span class="sxs-lookup"><span data-stu-id="b5e84-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="b5e84-181">Vai šajā izdevumu kategorijā pastāv apakškategorijas?</span><span class="sxs-lookup"><span data-stu-id="b5e84-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="b5e84-182">Ja pastāv apakškategorijas, jums ir jāpieņem arī tālāk norādītie lēmumi.</span><span class="sxs-lookup"><span data-stu-id="b5e84-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="b5e84-183">Vai kādas apakškategorijas ir izslēgtas no nodokļu atgūšanas?</span><span class="sxs-lookup"><span data-stu-id="b5e84-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="b5e84-184">Kas ir apakškategoriju krājuma pārdošanas nodokļu grupa?</span><span class="sxs-lookup"><span data-stu-id="b5e84-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="b5e84-185">Ja izdevumu kategorija tiek izmantota arī modulī Projektu vadība un uzskaite, atbildiet uz atlikušajiem jautājumiem.</span><span class="sxs-lookup"><span data-stu-id="b5e84-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="b5e84-186">Pretējā gadījumā pārejiet uz nākamo sadaļu.</span><span class="sxs-lookup"><span data-stu-id="b5e84-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="b5e84-187">Kuri izmaksu konti tiks izmantoti tālāk norādītajiem izdevumiem?</span><span class="sxs-lookup"><span data-stu-id="b5e84-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="b5e84-188">Izmaksas</span><span class="sxs-lookup"><span data-stu-id="b5e84-188">Cost</span></span>
    - <span data-ttu-id="b5e84-189">Algu sadalījums</span><span class="sxs-lookup"><span data-stu-id="b5e84-189">Payroll allocation</span></span>
    - <span data-ttu-id="b5e84-190">NP - Izmaksu vērtība</span><span class="sxs-lookup"><span data-stu-id="b5e84-190">WIP-cost value</span></span>
    - <span data-ttu-id="b5e84-191">Izmaksas-krājumi</span><span class="sxs-lookup"><span data-stu-id="b5e84-191">Cost-item</span></span>
    - <span data-ttu-id="b5e84-192">NP - Izmaksu vērtība - Krājumi</span><span class="sxs-lookup"><span data-stu-id="b5e84-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="b5e84-193">Uzkrātie zaudējumi</span><span class="sxs-lookup"><span data-stu-id="b5e84-193">Accrued loss</span></span>
    - <span data-ttu-id="b5e84-194">NP-uzkrātie zaudējumi</span><span class="sxs-lookup"><span data-stu-id="b5e84-194">WIP-accrued loss</span></span>

- <span data-ttu-id="b5e84-195">Kuri ieņēmumu konti tiks izmantoti tālāk norādītajiem mērķiem?</span><span class="sxs-lookup"><span data-stu-id="b5e84-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="b5e84-196">Rēķinos iekļautie ieņēmumi</span><span class="sxs-lookup"><span data-stu-id="b5e84-196">Invoiced revenue</span></span>
    - <span data-ttu-id="b5e84-197">Uzkrātie ieņēmumi-pārdošanas vērtība</span><span class="sxs-lookup"><span data-stu-id="b5e84-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="b5e84-198">NP-pārdošanas vērtība</span><span class="sxs-lookup"><span data-stu-id="b5e84-198">WIP-sales value</span></span>
    - <span data-ttu-id="b5e84-199">Uzkrātie ieņēmumi-ražošana</span><span class="sxs-lookup"><span data-stu-id="b5e84-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="b5e84-200">NP-ražošana</span><span class="sxs-lookup"><span data-stu-id="b5e84-200">WIP-production</span></span>
    - <span data-ttu-id="b5e84-201">Uzkrātie ieņēmumi-peļņa</span><span class="sxs-lookup"><span data-stu-id="b5e84-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="b5e84-202">NP-peļņa</span><span class="sxs-lookup"><span data-stu-id="b5e84-202">WIP-profit</span></span>
    - <span data-ttu-id="b5e84-203">Uzkrātie ieņēmumi-abonements</span><span class="sxs-lookup"><span data-stu-id="b5e84-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="b5e84-204">NP-abonements</span><span class="sxs-lookup"><span data-stu-id="b5e84-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="b5e84-205">Nodokļi</span><span class="sxs-lookup"><span data-stu-id="b5e84-205">Taxes</span></span>

<span data-ttu-id="b5e84-206">Attiecībā uz nodokļiem, kas saistīti ar izdevumiem, jums ir jānosaka, kas tiek iekļauts vai iespējots izdevumu atskaitēs.</span><span class="sxs-lookup"><span data-stu-id="b5e84-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="b5e84-207">**Lēmumi:**</span><span class="sxs-lookup"><span data-stu-id="b5e84-207">**Decisions:**</span></span>

- <span data-ttu-id="b5e84-208">Vai pārdošanas nodoklis ir iekļauts izdevumu summās?</span><span class="sxs-lookup"><span data-stu-id="b5e84-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="b5e84-209">Vai izdevumiem ir jāiespējo nodokļu atgūšana?</span><span class="sxs-lookup"><span data-stu-id="b5e84-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="b5e84-210">Ja virsgrāmatas plānošanas laikā izlēmāt lietot ASV PVN un nodokļu importa nodokļa kārtulas, tad izdevumiem nevar iespējot nodokļu atgūšanu.</span><span class="sxs-lookup"><span data-stu-id="b5e84-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="b5e84-211">(Lai lietotu ASV PVN un importa nodokļa kārtulas, opcija **Lietot PVN nodokļu kārtulas** ir jāiestata uz **Jā**.)</span><span class="sxs-lookup"><span data-stu-id="b5e84-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="b5e84-212">Politikas</span><span class="sxs-lookup"><span data-stu-id="b5e84-212">Policies</span></span>

<span data-ttu-id="b5e84-213">Izveidojot izdevumu pārskatu politikas, varat savai organizācijai palīdzēt taupīt laiku un naudu, kad darbinieki rada izdevumus šīs organizācijas vārdā.</span><span class="sxs-lookup"><span data-stu-id="b5e84-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="b5e84-214">Politikas palīdz garantēt, ka darbinieki iekļaujas budžetā, sniedz visu nepieciešamo informāciju un tērē naudu tikai tad, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="b5e84-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="b5e84-215">Attiecībā uz katru izdevumu atskaišu politiku un katru izdevumu atskaites apstiprināšanas politiku, ko izveidojat, jums ir jāpieņem tālāk norādītie lēmumi.</span><span class="sxs-lookup"><span data-stu-id="b5e84-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="b5e84-216">**Lēmumi:**</span><span class="sxs-lookup"><span data-stu-id="b5e84-216">**Decisions:**</span></span>

- <span data-ttu-id="b5e84-217">Kāds ir politikas nosaukums?</span><span class="sxs-lookup"><span data-stu-id="b5e84-217">What is the name of the policy?</span></span>
- <span data-ttu-id="b5e84-218">Kam šī izdevumu politika ir paredzēta?</span><span class="sxs-lookup"><span data-stu-id="b5e84-218">What is the expense policy for?</span></span>
- <span data-ttu-id="b5e84-219">Ja iepriekš izlēmāt iespējot starpuzņēmumu izdevumus — uz kuriem uzņēmumiem jūsu organizācijas ietvaros šī politika attiecas?</span><span class="sxs-lookup"><span data-stu-id="b5e84-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="b5e84-220">Kad šī politika stājas spēkā?</span><span class="sxs-lookup"><span data-stu-id="b5e84-220">When does the policy become effective?</span></span>
- <span data-ttu-id="b5e84-221">Kad beidzas šīs politikas darbība?</span><span class="sxs-lookup"><span data-stu-id="b5e84-221">When does the policy expire?</span></span>
- <span data-ttu-id="b5e84-222">Kāda ir politikas kārtula?</span><span class="sxs-lookup"><span data-stu-id="b5e84-222">What is the policy rule?</span></span>
- <span data-ttu-id="b5e84-223">Kāds ir politikas kārtulas iznākums?</span><span class="sxs-lookup"><span data-stu-id="b5e84-223">What is the outcome of the policy rule?</span></span>

