---
title: Pozīciju budžeta izveides problēmu novēršana
description: Šajā raksta ir sniegtas atbildes uz jautājumiem, kas var rasties budžeta veidošanas pozīciju konfigurēšanas gaitā. Tēma atsaucas uz biežāk uzdotajiem jautājumiem par to, kā izveidot budžeta izmaksu elementus, atlīdzību grupas un atlīdzību režģus.
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmBudgetPurposeType, HcmPositionForecast
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 88253
ms.assetid: c44df01b-8700-4022-b4c6-c4b1cb84d31d
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0800a4a7c92a1a5f4d4f66bb37032eacccc4cb4e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "367114"
---
# <a name="position-budgeting-troubleshooting"></a><span data-ttu-id="cb21f-104">Pozīciju budžeta izveides problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="cb21f-104">Position budgeting troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb21f-105">Šajā raksta ir sniegtas atbildes uz jautājumiem, kas var rasties budžeta veidošanas pozīciju konfigurēšanas gaitā.</span><span class="sxs-lookup"><span data-stu-id="cb21f-105">This article provides answers to questions that you might have when you configure position budgeting.</span></span> <span data-ttu-id="cb21f-106">Tēma atsaucas uz biežāk uzdotajiem jautājumiem par to, kā izveidot budžeta izmaksu elementus, atlīdzību grupas un atlīdzību režģus.</span><span class="sxs-lookup"><span data-stu-id="cb21f-106">It addresses frequently asked questions about how to create budget cost elements, compensation groups, and compensation grids.</span></span> 

<a name="why-cant-i-find-the-forecast-position-page-in-human-resources"></a><span data-ttu-id="cb21f-107">Kāpēc nevar atrast prognozes pozīciju lapā Personāla vadība?</span><span class="sxs-lookup"><span data-stu-id="cb21f-107">Why can’t I find the forecast position page in Human resources?</span></span>
---------------------------------------------------------------

<span data-ttu-id="cb21f-108">Prognožu pozīcijas ir pārvietotas uz lapu Budžeta veidošana.</span><span class="sxs-lookup"><span data-stu-id="cb21f-108">Forecast positions have been moved to Budgeting.</span></span>

## <a name="why-cant-i-delete-a-budget-cost-element"></a><span data-ttu-id="cb21f-109">Kāpēc es nevaru izdzēst budžeta izmaksu elementu?</span><span class="sxs-lookup"><span data-stu-id="cb21f-109">Why can’t I delete a budget cost element?</span></span>
<span data-ttu-id="cb21f-110">Jūs nevarat dzēst budžeta izmaksu elementu, kas ir piešķirts prognožu pozīcijai.</span><span class="sxs-lookup"><span data-stu-id="cb21f-110">You can’t delete a budget cost element that is assigned to a forecast position.</span></span> <span data-ttu-id="cb21f-111">Lai varētu izdzēst budžeta izmaksu elementu, tas vispirms ir jānoņem visās prognožu pozīcijās.</span><span class="sxs-lookup"><span data-stu-id="cb21f-111">Before you can delete a budget cost element, you must remove it from all forecast positions.</span></span> <span data-ttu-id="cb21f-112">**Padoms.** Lai varētu atrast visas pozīcijas, kurām ir piešķirts budžeta izmaksu elements, atlasiet izmaksu elementu lapā **Budžeta izmaksu elementi** un pēc tam noklikšķiniet uz **Atjaunināt pozīcijas**.</span><span class="sxs-lookup"><span data-stu-id="cb21f-112">**Tip:** To find all the positions that a budget cost element is assigned to, select the cost element on the **Budget cost elements** page, and then click **Update positions**.</span></span> <span data-ttu-id="cb21f-113">Pozīcijas, kuras izmantoto izmaksu elementu, ir uzskaitītas augšējā režģī.</span><span class="sxs-lookup"><span data-stu-id="cb21f-113">The positions that use the cost element are listed in the upper grid.</span></span>

## <a name="how-can-i-remove-a-cost-element-from-multiple-forecast-positions-without-opening-each-one"></a><span data-ttu-id="cb21f-114">Kā var noņemt izmaksu elementu vairākās budžeta pozīcijās, neatverot tās katru atsevišķi?</span><span class="sxs-lookup"><span data-stu-id="cb21f-114">How can I remove a cost element from multiple forecast positions without opening each one?</span></span>
<span data-ttu-id="cb21f-115">Izmaksu elementu nevar noņemt.</span><span class="sxs-lookup"><span data-stu-id="cb21f-115">You can’t remove a cost element.</span></span> <span data-ttu-id="cb21f-116">Tomēr, ja tiek mainīts sākuma un beigu datums tā, tie būtu ārpus budžeta plānošanas cikla, izmaksu elements vairs netiek piešķirts prognožu pozīcijām budžeta plānošanas ciklā.</span><span class="sxs-lookup"><span data-stu-id="cb21f-116">However, if you change the start and end dates so that they are outside the budget planning cycle dates, the cost element will no longer be assigned to the forecast positions in that budget planning cycle.</span></span> <span data-ttu-id="cb21f-117">Lai varētu veikt šādas izmaiņas, atveriet budžeta izmaksu elementu un pēc tam kopsavilkuma cilnē **Izmaksu aprēķināšana** noklikšķiniet uz **Mainīt datumus** un mainiet spēkā stāšanās vai beigu datumu.</span><span class="sxs-lookup"><span data-stu-id="cb21f-117">To make this change, open the budget cost element, and then, on the **Cost calculation** FastTab, click **Change dates**, and change the effective date or expiration date.</span></span> <span data-ttu-id="cb21f-118">Pēc tam noklikšķiniet uz **Labi**, lai automātiski atjaunina visas prognozes pozīcijas, kurām ir piešķirts izmaksu elements.</span><span class="sxs-lookup"><span data-stu-id="cb21f-118">Then click **OK** to automatically update all forecast positions that the cost element is assigned to.</span></span> <span data-ttu-id="cb21f-119">**Padoms.** Ja tiek izmantota šī metode, ņemiet vērā, ka tādējādi budžeta izmaksu elements tiek noņemts **visās** prognožu pozīcijās, kuru sākuma un beigu datums vairs nav atbilstošajā diapazonā.</span><span class="sxs-lookup"><span data-stu-id="cb21f-119">**Tip:** If you use this method, be aware that it removes the budget cost element from **all** forecast positions where the start and end dates are no longer within the appropriate range.</span></span> <span data-ttu-id="cb21f-120">Ja to nevēlaties, katra prognozes pozīcija, kurai vēlaties noņemt budžeta izmaksu elementu, ir jāatver atsevišķi un jāveic izmaiņas manuāli.</span><span class="sxs-lookup"><span data-stu-id="cb21f-120">If this effect isn't what you intend, you must open each forecast position that you want to remove the budget cost element from and manually make the change.</span></span>

## <a name="why-cant-i-enter-an-annual-amount-on-the-cost-calculation-fasttab-for-the-budget-cost-element"></a><span data-ttu-id="cb21f-121">Kāpēc nevar ievadīt budžeta izmaksu elementa gada summu kopsavilkuma cilnē Izmaksu aprēķināšana?</span><span class="sxs-lookup"><span data-stu-id="cb21f-121">Why can’t I enter an annual amount on the Cost calculation FastTab for the budget cost element?</span></span>
<span data-ttu-id="cb21f-122">Gada summu nevar ievadīt, ja kopsavilkuma cilnē **Aprēķina bāze** ir budžeta izmaksu elementi, jo, lai varētu aprēķināt vērtību, sistēmā ir nepieciešama procentuālā vērtība.</span><span class="sxs-lookup"><span data-stu-id="cb21f-122">You can’t enter an annual amount if there are budget cost elements on the **Calculation basis** FastTab, because the system requires a percentage in order to calculate the value.</span></span> <span data-ttu-id="cb21f-123">Lai mainītu vērtību, noņemiet visus budžeta izmaksu elementus kopsavilkuma cilnē **Aprēķina bāze**.</span><span class="sxs-lookup"><span data-stu-id="cb21f-123">To change the value, remove all budget cost elements from the **Calculation basis** FastTab.</span></span>

## <a name="why-cant-i-change-the-budget-cost-type-from-earning-to-another-budget-cost-type"></a><span data-ttu-id="cb21f-124">Kāpēc nevar izmainīt budžeta izmaksu veidu Ienākums uz citu budžeta izmaksu veidu?</span><span class="sxs-lookup"><span data-stu-id="cb21f-124">Why can’t I change the budget cost type from earning to another budget cost type?</span></span>
<span data-ttu-id="cb21f-125">Daži budžeta izmaksu elementi izmanto izmaksu elementu Ienākums kā aprēķinu bāzi.</span><span class="sxs-lookup"><span data-stu-id="cb21f-125">Some budget cost elements use the earning cost element as a calculation basis.</span></span> <span data-ttu-id="cb21f-126">Lai mainītu vērtību laukā **Budžeta izmaksu veids**, noņemiet ieņēmumu izmaksu elementu kopsavilkuma cilnē **Aprēķina bāze** visiem budžeta izmaksu elementiem.</span><span class="sxs-lookup"><span data-stu-id="cb21f-126">To change the **Budget cost type** field, remove the earning cost element from the **Calculation basis** FastTab of all budget cost elements.</span></span>

## <a name="why-cant-i-change-the-date-on-budget-cost-element-lines-for-a-budget-cost-element"></a><span data-ttu-id="cb21f-127">Kāpēc es nevaru mainīt datumu budžeta izmaksu elementu rindās budžeta izmaksu elementam?</span><span class="sxs-lookup"><span data-stu-id="cb21f-127">Why can’t I change the date on budget cost element lines for a budget cost element?</span></span>
<span data-ttu-id="cb21f-128">Ja budžeta izmaksu elements ir izmantots prognozes pozīcijā, budžeta izmaksu elementa rindā nevar mainīt datumu.</span><span class="sxs-lookup"><span data-stu-id="cb21f-128">You can’t change the date on the budget cost element line when a budget cost element is used by a forecast position.</span></span> <span data-ttu-id="cb21f-129">Šis ierobežojums nodrošina, ka prognožu pozīcijas vienmēr atbilst budžeta izmaksu elementa vadlīnijām.</span><span class="sxs-lookup"><span data-stu-id="cb21f-129">This limitation helps guarantee that the forecast positions are always within the guidelines of the budget cost element.</span></span> <span data-ttu-id="cb21f-130">Lai mainītu datumu, kopsavilkuma cilnē **Izmaksu aprēķināšana** noklikšķiniet uz **Mainīt datumu** un ievadiet jaunu datumu.</span><span class="sxs-lookup"><span data-stu-id="cb21f-130">To change the date, on the **Cost calculation** FastTab, click **Change dates**, and enter the new dates.</span></span> <span data-ttu-id="cb21f-131">Pēc tam noklikšķiniet uz **Labi**, lai atjaunina pozīcijas, kurām ir piešķirts izmaksu elements.</span><span class="sxs-lookup"><span data-stu-id="cb21f-131">Then click **OK** to update the positions that the cost element is assigned to.</span></span>

## <a name="why-cant-i-change-the-costs-for-a-budget-cost-element-on-the-compensation-group-page"></a><span data-ttu-id="cb21f-132">Kāpēc nevar mainīt budžeta izmaksu elementa izmaksas lapā Atlīdzības grupa?</span><span class="sxs-lookup"><span data-stu-id="cb21f-132">Why can’t I change the costs for a budget cost element on the Compensation group page?</span></span>
<span data-ttu-id="cb21f-133">Budžeta izmaksu elementus var izveidot un mainīt tikai lapā **Budžeta izmaksu elementi**.</span><span class="sxs-lookup"><span data-stu-id="cb21f-133">You can create and change budget cost elements only on the **Budget cost elements** page.</span></span>

## <a name="why-do-i-receive-an-error-message-when-i-change-the-dates-for-a-cost-element-on-a-forecast-position"></a><span data-ttu-id="cb21f-134">Kāpēc, mainot izmaksu elementa datumu prognozes pozīcijā, tiek parādīts kļūdas ziņojums?</span><span class="sxs-lookup"><span data-stu-id="cb21f-134">Why do I receive an error message when I change the dates for a cost element on a forecast position?</span></span>
<span data-ttu-id="cb21f-135">Prognozes pozīcijas izmaksu elementa rindas datumiem jābūt tālāk norādītajās robežās.</span><span class="sxs-lookup"><span data-stu-id="cb21f-135">The dates on the forecast position cost element line must be within the following ranges:</span></span>

-   <span data-ttu-id="cb21f-136">Pozīcijas aktivizēšanas un norakstīšanas datums.</span><span class="sxs-lookup"><span data-stu-id="cb21f-136">The activation and retirement dates of the position.</span></span>
-   <span data-ttu-id="cb21f-137">Budžeta izmaksu elementa aktivizēšanas un beigu datums.</span><span class="sxs-lookup"><span data-stu-id="cb21f-137">The activation and expiration dates of the budget cost element.</span></span>
-   <span data-ttu-id="cb21f-138">Budžeta cikla sākuma un beigu datums, kas ir saistīts ar prognozes pozīcijas budžeta plānošanas procesu.</span><span class="sxs-lookup"><span data-stu-id="cb21f-138">The start and end dates of the budget cycle that is associated with the budget planning process of the forecast position.</span></span>




