---
title: Mobilie rēķinu apstiprinājumi
description: Šajā tēmā ir aprakstīta praktiska pieeja mobilo scenāriju izstrādei, kā lietojuma gadījumu apskatot kreditoru rēķinu apstiprināšanu mobilajās ierīcēs.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 262034
ms.assetid: 9db38b3f-26b3-436e-8449-7ff243568a18
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 88ba96b1d9d2f722528a4a920eabe4ab64304a7a
ms.sourcegitcommit: 4f668b23f5bfc6d6502858850d2ed59d7a79cfbb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/14/2020
ms.locfileid: "3059432"
---
# <a name="mobile-invoice-approvals"></a><span data-ttu-id="5ec30-103">Mobilie rēķinu apstiprinājumi</span><span class="sxs-lookup"><span data-stu-id="5ec30-103">Mobile invoice approvals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5ec30-104">Mobilās iespējas sniedz biznesa lietotājam iespēju izstrādāt mobilos risinājumus.</span><span class="sxs-lookup"><span data-stu-id="5ec30-104">Mobile capabilities let a business user design mobile experiences.</span></span> <span data-ttu-id="5ec30-105">Sarežģītu scenāriju gadījumā izstrādātāji var arī paplašināt iespējas atbilstoši savām vēlmēm.</span><span class="sxs-lookup"><span data-stu-id="5ec30-105">For advanced scenarios, the platform also lets developers extend the capabilities as they desire.</span></span> <span data-ttu-id="5ec30-106">Visefektīvākais veids, kā apgūt dažas no jaunajām mobilajām ierīcēm paredzētajām koncepcijām, ir jaunu scenāriju procesa izpilde.</span><span class="sxs-lookup"><span data-stu-id="5ec30-106">The most effective way to learn some of the new concepts on mobile is to go through the process of designing a few scenarios.</span></span> <span data-ttu-id="5ec30-107">Šajā tēmā ir aprakstīta praktiska pieeja mobilo scenāriju izstrādei, kā lietojuma gadījumu apskatot kreditoru rēķinu apstiprināšanu mobilajās ierīcēs.</span><span class="sxs-lookup"><span data-stu-id="5ec30-107">This topic is intended to provide a practical approach to designing mobile scenarios by taking vendor invoice approvals for mobile as a use case.</span></span> <span data-ttu-id="5ec30-108">Šajā tēmā sniegtā informācija palīdzēs jums izstrādāt arī citus scenāriju variantus, un to var lietot arī citiem scenārijiem, kas nav saistīti ar kreditoru rēķiniem.</span><span class="sxs-lookup"><span data-stu-id="5ec30-108">This topic should help you design other variations of the scenarios and can also be applied to other scenarios that aren’t related to vendor invoices.</span></span>

<a name="prerequisites"></a><span data-ttu-id="5ec30-109">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="5ec30-109">Prerequisites</span></span>
-------------

| <span data-ttu-id="5ec30-110">Priekšnoteikumi</span><span class="sxs-lookup"><span data-stu-id="5ec30-110">Prerequisite</span></span>                                                                                            | <span data-ttu-id="5ec30-111">apraksts</span><span class="sxs-lookup"><span data-stu-id="5ec30-111">Description</span></span>                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ec30-112">Iepriekš izlasiet mobilo risinājumu rokasgrāmatu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-112">Mobile handbook pre-read</span></span>                                                                                |[<span data-ttu-id="5ec30-113">Mobilā platforma</span><span class="sxs-lookup"><span data-stu-id="5ec30-113">Mobile platform</span></span>](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)                                                                                                  |
| <span data-ttu-id="5ec30-114">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="5ec30-114">Dynamics 365 Finance</span></span>                                                                              | <span data-ttu-id="5ec30-115">Vide, kurā ir instalēta versija 1611 un 3. platformas atjauninājums (2016. gada novembris)</span><span class="sxs-lookup"><span data-stu-id="5ec30-115">An environment that has version 1611 and Platform update 3 (November 2016)</span></span>                   |
| <span data-ttu-id="5ec30-116">Instalējiet labojumfailu KB 3204341.</span><span class="sxs-lookup"><span data-stu-id="5ec30-116">Install hotfix KB 3204341.</span></span>                                                                              | <span data-ttu-id="5ec30-117">Uzdevumu reģistrētājs var kļūdaini reģistrēt divas nolaižamo dialoglodziņu aizvēršanas komandas; tas ir ietverts 3. platformas atjauninājumā (2016. gada novembrī izlaistais atjauninājums)</span><span class="sxs-lookup"><span data-stu-id="5ec30-117">Task recorder can erroneously record two Close commands for dropdown dialogs; this is included in Platform update 3 (November 2016 update).</span></span> |
| <span data-ttu-id="5ec30-118">Instalējiet labojumfailu KB 3207800.</span><span class="sxs-lookup"><span data-stu-id="5ec30-118">Install hotfix KB 3207800.</span></span>                                                                              | <span data-ttu-id="5ec30-119">Šis labojumfails sniedz iespēju skatīt pielikumus mobilajā klientā; tas ir ietverts 3. platformas atjauninājumā (2016. gada novembrī izlaistais atjauninājums)</span><span class="sxs-lookup"><span data-stu-id="5ec30-119">This hotfix enables attachments to be viewed on the mobile client; this is included in Platform update 3 (November 2016 update).</span></span>           |
| <span data-ttu-id="5ec30-120">Instalējiet labojumfailu KB 3208224.</span><span class="sxs-lookup"><span data-stu-id="5ec30-120">Install hotfix KB 3208224.</span></span>                                                                              | <span data-ttu-id="5ec30-121">Kreditoru rēķinu apstiprināšanas mobilās lietojumprogrammas kods, kas ir ietverts versijā 7.0.1 (2016. gada maijs).</span><span class="sxs-lookup"><span data-stu-id="5ec30-121">Application code for the mobile vendor invoice approval application; this is included in version 7.0.1 (May 2016).</span></span>                          |
| <span data-ttu-id="5ec30-122">Android vai iOS vai Windows ierīce, kurā ir instalēta mobilā programma.</span><span class="sxs-lookup"><span data-stu-id="5ec30-122">An Android or iOS or a Windows device that has the mobile app installed.</span></span> | <span data-ttu-id="5ec30-123">Meklējiet programmu atbilstošajā programmu veikalā.</span><span class="sxs-lookup"><span data-stu-id="5ec30-123">Search for the app in the appropriate app store.</span></span>                                                                                                                     |

## <a name="introduction"></a><span data-ttu-id="5ec30-124">Ievads</span><span class="sxs-lookup"><span data-stu-id="5ec30-124">Introduction</span></span>
<span data-ttu-id="5ec30-125">Lai varētu apstiprināt kreditoru rēķinus mobilajā ierīcē, ir nepieciešami trīs labojumfaili, kas ir norādīti sadaļā Priekšnosacījumi.</span><span class="sxs-lookup"><span data-stu-id="5ec30-125">Mobile approvals for vendor invoices require the three hotfixes that are mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="5ec30-126">Šie labojumfaili nenodrošina rēķinu apstiprināšanas darbvietu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-126">These hotfixes don’t provide a workspace for the invoice approvals.</span></span> <span data-ttu-id="5ec30-127">Lai uzzinātu, kas ir darbvieta attiecībā uz mobilajām ierīcēm, izlasiet mobilo ierīču risinājumu rokasgrāmatu, kas ir pieminēta sadaļā “Priekšnosacījumi”.</span><span class="sxs-lookup"><span data-stu-id="5ec30-127">To learn what a workspace is in the context of mobile, read the mobile handbook that is mentioned in the “Prerequisites” section.</span></span> <span data-ttu-id="5ec30-128">Rēķinu apstiprināšanas darbplūsma ir jāizstrādā.</span><span class="sxs-lookup"><span data-stu-id="5ec30-128">The invoice approvals workspace must be designed.</span></span> 

<span data-ttu-id="5ec30-129">Katra organizācija atšķirīgā veidā vada un definē savu kreditoru rēķinu biznesa procesu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-129">Every organization orchestrates and defines its business process for vendor invoices differently.</span></span> <span data-ttu-id="5ec30-130">Pirms kreditoru rēķinu apstiprināšanas mobilā risinājuma izstrādes ir jāņem vērā tālāk norādītie biznesa procesa aspekti.</span><span class="sxs-lookup"><span data-stu-id="5ec30-130">Before you design a mobile experience for vendor invoice approvals, you should consider the following aspects of the business process.</span></span> <span data-ttu-id="5ec30-131">Mērķis ir pēc iespējas vairāk izmantot šos datu punktus, lai optimizētu lietotāja iespējas ierīcē.</span><span class="sxs-lookup"><span data-stu-id="5ec30-131">The idea is to use these data points as much as possible to optimize the user experience on the device.</span></span>

-   <span data-ttu-id="5ec30-132">Kurus rēķina galvenes laukus un kādā secībā lietotājs vēlēsies redzēt mobilajā risinājumā?</span><span class="sxs-lookup"><span data-stu-id="5ec30-132">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="5ec30-133">Kurus rēķina rindu laikus un kādā secībā lietotājs vēlēsies redzēt mobilajā risinājumā?</span><span class="sxs-lookup"><span data-stu-id="5ec30-133">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span>
-   <span data-ttu-id="5ec30-134">Cik rēķina rindu ir rēķinā?</span><span class="sxs-lookup"><span data-stu-id="5ec30-134">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="5ec30-135">Lietojiet 80/20 nosacījumu un optimizējiet atbilstoši 80 procentiem.</span><span class="sxs-lookup"><span data-stu-id="5ec30-135">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span>
-   <span data-ttu-id="5ec30-136">Vai lietotāji vēlas pārskatīšanas laikā mobilajā ierīcē redzēt uzskaites sadales (rēķina kodu).</span><span class="sxs-lookup"><span data-stu-id="5ec30-136">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span> <span data-ttu-id="5ec30-137">Ja atbilde uz šo jautājumu ir apstiprinoša, ņemiet vērā tālāk norādītos jautājumus.</span><span class="sxs-lookup"><span data-stu-id="5ec30-137">If the answer to this question is yes, consider the following questions:</span></span>
    -   <span data-ttu-id="5ec30-138">Cik uzskaites sadales elementu (pilna cena, PVN, izmaksas, dalījumi utt.) ir vienā rēķina rindā?</span><span class="sxs-lookup"><span data-stu-id="5ec30-138">How many accounting distributions (extended price, sales tax, charges, splits, and so on) are there for an invoice line?</span></span> <span data-ttu-id="5ec30-139">Atkal lietojiet 80/20 nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-139">Again, apply the 80-20 rule.</span></span>
    -   <span data-ttu-id="5ec30-140">Vai rēķina galvenē arī ir uzskaites sadales?</span><span class="sxs-lookup"><span data-stu-id="5ec30-140">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="5ec30-141">Jā tā ir, vai šīm uzskaites sadalēm ir jābūt pieejamām ierīcē?</span><span class="sxs-lookup"><span data-stu-id="5ec30-141">If so, should these accounting distributions be available on the device?</span></span>

    > [!NOTE]
    > <span data-ttu-id="5ec30-142">Šajā tēmā nav paskaidrots, kā rediģēt uzskaites sadales, jo šī funkcionalitāte pašlaik netiek atbalstīta mobilajiem scenārijiem.</span><span class="sxs-lookup"><span data-stu-id="5ec30-142">This topic doesn’t explain how to edit accounting distributions, because this functionality isn’t currently supported for mobile scenarios.</span></span>

-   <span data-ttu-id="5ec30-143">Vai lietotāji vēlēsies ierīcē redzēt rēķina pielikumus?</span><span class="sxs-lookup"><span data-stu-id="5ec30-143">Will users want to see attachments for the invoice on the device?</span></span>

<span data-ttu-id="5ec30-144">Rēķinu apstiprināšanas mobilā risinājuma izstrāde atšķiras atkarībā no atbildēm uz šiem jautājumiem.</span><span class="sxs-lookup"><span data-stu-id="5ec30-144">The design of the mobile experience for invoice approvals will differ, depending on the answers to these questions.</span></span> <span data-ttu-id="5ec30-145">Mērķis ir optimizēt lietotāja iespējas darbam ar biznesa procesu mobilajā ierīcē organizācijas ietvaros.</span><span class="sxs-lookup"><span data-stu-id="5ec30-145">The objective is to optimize the user experience for the business process on mobile in an organization.</span></span> <span data-ttu-id="5ec30-146">Šīs tēmas turpinājumā ir aprakstīti scenārija varianti, kas ir izstrādāti, pamatojoties uz dažādām atbildēm uz iepriekš norādītajiem jautājumiem.</span><span class="sxs-lookup"><span data-stu-id="5ec30-146">In the rest of this topic, we will look at two scenario variations that are based on different answers to the preceding questions.</span></span> 

<span data-ttu-id="5ec30-147">Vienmēr, kad strādājat ar mobilo programmu veidotāju, noteikti publicējiet izmaiņas, lai nepieļautu atjauninājumu zaudēšanu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-147">As a general guidance, when working with the mobile designer, make sure to 'publish' the changes to prevent losing the updates.</span></span>

## <a name="designing-a-simple-invoice-approval-scenario-for-contoso"></a><span data-ttu-id="5ec30-148">Vienkārša rēķinu apstiprināšanas scenārija izstrāde uzņēmumam Contoso</span><span class="sxs-lookup"><span data-stu-id="5ec30-148">Designing a simple invoice approval scenario for Contoso</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5ec30-149">Scenārija atribūts</span><span class="sxs-lookup"><span data-stu-id="5ec30-149">Scenario attribute</span></span></th>
<th><span data-ttu-id="5ec30-150">Atbilde</span><span class="sxs-lookup"><span data-stu-id="5ec30-150">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5ec30-151">Kurus rēķina galvenes laukus un kādā secībā lietotājs vēlēsies redzēt mobilajā risinājumā?</span><span class="sxs-lookup"><span data-stu-id="5ec30-151">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="5ec30-152">Kreditora nosaukums</span><span class="sxs-lookup"><span data-stu-id="5ec30-152">Vendor name</span></span></li>
<li><span data-ttu-id="5ec30-153">Rēķina kopsumma</span><span class="sxs-lookup"><span data-stu-id="5ec30-153">Invoice total</span></span></li>
<li><span data-ttu-id="5ec30-154">Rēķina konts</span><span class="sxs-lookup"><span data-stu-id="5ec30-154">Invoice account</span></span></li>
<li><span data-ttu-id="5ec30-155">Rēķina numurs</span><span class="sxs-lookup"><span data-stu-id="5ec30-155">Invoice number</span></span></li>
<li><span data-ttu-id="5ec30-156">Rēķina datums</span><span class="sxs-lookup"><span data-stu-id="5ec30-156">Invoice date</span></span></li>
<li><span data-ttu-id="5ec30-157">Rēķina apraksts</span><span class="sxs-lookup"><span data-stu-id="5ec30-157">Invoice description</span></span></li>
<li><span data-ttu-id="5ec30-158">Izpildes termiņš</span><span class="sxs-lookup"><span data-stu-id="5ec30-158">Due date</span></span></li>
<li><span data-ttu-id="5ec30-159">Rēķina valūta</span><span class="sxs-lookup"><span data-stu-id="5ec30-159">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ec30-160">Kurus rēķina rindu laikus un kādā secībā lietotājs vēlēsies redzēt mobilajā risinājumā?</span><span class="sxs-lookup"><span data-stu-id="5ec30-160">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="5ec30-161">Sagādes kategorija</span><span class="sxs-lookup"><span data-stu-id="5ec30-161">Procurement category</span></span></li>
<li><span data-ttu-id="5ec30-162">Daudzums</span><span class="sxs-lookup"><span data-stu-id="5ec30-162">Quantity</span></span></li>
<li><span data-ttu-id="5ec30-163">Vienības cena</span><span class="sxs-lookup"><span data-stu-id="5ec30-163">Unit price</span></span></li>
<li><span data-ttu-id="5ec30-164">Rindas neto summa</span><span class="sxs-lookup"><span data-stu-id="5ec30-164">Line net amount</span></span></li>
<li><span data-ttu-id="5ec30-165">1099. summa</span><span class="sxs-lookup"><span data-stu-id="5ec30-165">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ec30-166">Cik rēķina rindu ir rēķinā?</span><span class="sxs-lookup"><span data-stu-id="5ec30-166">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="5ec30-167">Lietojiet 80/20 nosacījumu un optimizējiet atbilstoši 80 procentiem.</span><span class="sxs-lookup"><span data-stu-id="5ec30-167">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="5ec30-168">1.</span><span class="sxs-lookup"><span data-stu-id="5ec30-168">1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ec30-169">Vai lietotāji vēlas pārskatīšanas laikā mobilajā ierīcē redzēt uzskaites sadales (rēķina kodu).</span><span class="sxs-lookup"><span data-stu-id="5ec30-169">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="5ec30-170">Jā</span><span class="sxs-lookup"><span data-stu-id="5ec30-170">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ec30-171">Cik uzskaites sadales elementu (pilna cena, PVN, izmaksas utt.) ir vienā rēķina rindā?</span><span class="sxs-lookup"><span data-stu-id="5ec30-171">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="5ec30-172">Atkal lietojiet 80/20 nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-172">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="5ec30-173">Pilna cena: 2, PVN: 0, izmaksas: 0</span><span class="sxs-lookup"><span data-stu-id="5ec30-173">Extended price: 2 Sales tax: 0 Charges: 0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ec30-174">Vai rēķina galvenē arī ir uzskaites sadales?</span><span class="sxs-lookup"><span data-stu-id="5ec30-174">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="5ec30-175">Jā tā ir, vai šīm uzskaites sadalēm ir jābūt pieejamām ierīcē?</span><span class="sxs-lookup"><span data-stu-id="5ec30-175">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="5ec30-176">Netiek lietots</span><span class="sxs-lookup"><span data-stu-id="5ec30-176">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ec30-177">Vai lietotāji vēlēsies ierīcē redzēt rēķina pielikumus?</span><span class="sxs-lookup"><span data-stu-id="5ec30-177">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="5ec30-178">Jā</span><span class="sxs-lookup"><span data-stu-id="5ec30-178">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="create-the-workspace"></a><span data-ttu-id="5ec30-179">Darbvietas izveide</span><span class="sxs-lookup"><span data-stu-id="5ec30-179">Create the workspace</span></span>

1.  <span data-ttu-id="5ec30-180">Pārlūkprogrammā un pierakstieties programmā.</span><span class="sxs-lookup"><span data-stu-id="5ec30-180">In a browser, and sign in to the application.</span></span>
2.  <span data-ttu-id="5ec30-181">Pēc pierakstīšanās pievienojiet vietrādim URL tekstu **&mode=mobile**, kā tas ir parādīts šajā piemērā, un atsvaidziniet lapu: https://&lt;jūsuurl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span><span class="sxs-lookup"><span data-stu-id="5ec30-181">After you’ve signed in, append **&mode=mobile** to the URL as shown in the following example, and refresh the page: https://&lt;yoururl&gt;/?cmp=usmf&mi=DefaultDashboard **&mode=mobile**</span></span>
3.  <span data-ttu-id="5ec30-182">Noklikšķiniet uz pogas **Iestatījumi** (zobrats) lapas augšējā labajā stūrī un pēc tam noklikšķiniet uz **Mobilā programma**.</span><span class="sxs-lookup"><span data-stu-id="5ec30-182">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**.</span></span> <span data-ttu-id="5ec30-183">Tiek parādīts mobilo programmu veidotājs, tāpat kā tiek parādīts uzdevuma reģistrētājs.</span><span class="sxs-lookup"><span data-stu-id="5ec30-183">The mobile app designer must show up just as Task recorder shows up.</span></span>
4.  <span data-ttu-id="5ec30-184">Noklikšķiniet uz **Pievienot**, lai izveidotu jaunu darbvietu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-184">Click **Add** to create a new workspace.</span></span> <span data-ttu-id="5ec30-185">Šī piemēra ietvaros piešķiriet darbvietai nosaukumu **Mani apstiprinājumi**.</span><span class="sxs-lookup"><span data-stu-id="5ec30-185">For this example, name the workspace **My approvals**.</span></span>
5.  <span data-ttu-id="5ec30-186">Ievadiet aprakstu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-186">Enter a description.</span></span>
6.  <span data-ttu-id="5ec30-187">Atlasiet darbvietas krāsu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-187">Select a workspace color.</span></span> <span data-ttu-id="5ec30-188">Darbvietas krāsa tiek izmantota šīs darbvietas mobilā risinājuma vispārējā stila izveidei.</span><span class="sxs-lookup"><span data-stu-id="5ec30-188">The workspace color will be used for the overall style of the mobile experience for this workspace.</span></span>
7.  <span data-ttu-id="5ec30-189">Atlasiet darbvietas ikonu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-189">Select an icon for the workspace.</span></span>
8.  <span data-ttu-id="5ec30-190">Noklikšķiniet uz **Gatavs**</span><span class="sxs-lookup"><span data-stu-id="5ec30-190">Click **Done**</span></span>
9.  <span data-ttu-id="5ec30-191">Noklikšķiniet uz **Publicēt darbvietu**, lai saglabātu izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="5ec30-191">Click **Publish workspace** to save the changes</span></span>

### <a name="vendor-invoices-assigned-to-me"></a><span data-ttu-id="5ec30-192">Kreditora rēķini, kas piešķirti man</span><span class="sxs-lookup"><span data-stu-id="5ec30-192">Vendor invoices assigned to me</span></span>

<span data-ttu-id="5ec30-193">Pirmā mobilā lapa, kas ir jāizstrādā, ir lietotājam pārskatīšanai piešķirto rēķinu saraksts.</span><span class="sxs-lookup"><span data-stu-id="5ec30-193">The first mobile page that you should design is the list of invoices that are assigned to the user for review.</span></span> <span data-ttu-id="5ec30-194">Lai izstrādātu šo mobilo lapu, izmantojiet lapu **VendMobileInvoiceAssignedToMeListPage**.</span><span class="sxs-lookup"><span data-stu-id="5ec30-194">To design this mobile page, use the **VendMobileInvoiceAssignedToMeListPage** page.</span></span> <span data-ttu-id="5ec30-195">Pirms šīs procedūras pabeigšanas pārliecinieties, ka jums pārskatīšanai ir piešķirts vismaz viens kreditora rēķins un ka rēķina rindā ir divi sadales elementi.</span><span class="sxs-lookup"><span data-stu-id="5ec30-195">Before you complete this procedure, make sure that at least one vendor invoice is assigned to you for review, and that the invoice line has two distributions.</span></span> <span data-ttu-id="5ec30-196">Šie iestatījumi atbilst šī scenārija prasībām.</span><span class="sxs-lookup"><span data-stu-id="5ec30-196">This setup meets the requirements for this scenario.</span></span>

1.  <span data-ttu-id="5ec30-197">Vietrādī URL izvēlnes vienuma nosaukumu aizstājiet ar **VendMobileInvoiceAssignedToMeListPage**, lai atvērtu moduļa **Parādi kreditoriem** lapas **Gaidošie kreditoru rēķini, kas piešķirti man** mobilo versiju.</span><span class="sxs-lookup"><span data-stu-id="5ec30-197">In the URL, replace the name of the menu item with **VendMobileInvoiceAssignedToMeListPage** to open the mobile version of the **Pending vendor invoices assigned to me** list page in the **Accounts payable** module.</span></span> <span data-ttu-id="5ec30-198">Atkarībā no tā, cik rēķinu jums ir piešķirts sistēmā, šajā lapā tiek rādīti šie rēķini.</span><span class="sxs-lookup"><span data-stu-id="5ec30-198">Depending on the number of invoices that you have in your system assigned to you, this page will show those invoices.</span></span> <span data-ttu-id="5ec30-199">Lai atrastu konkrētu rēķinu, varat izmantot kreisajā pusē esošo filtru.</span><span class="sxs-lookup"><span data-stu-id="5ec30-199">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="5ec30-200">Taču šī piemēra ietvaros nav nepieciešams konkrēts rēķins.</span><span class="sxs-lookup"><span data-stu-id="5ec30-200">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="5ec30-201">Ir nepieciešams jebkurš jums piešķirts rēķins, ko var izmantot mobilās lapas izstrādei.</span><span class="sxs-lookup"><span data-stu-id="5ec30-201">We just require some invoice assigned to you which is going to allow you to design the mobile page.</span></span> <span data-ttu-id="5ec30-202">Jaunās pieejamās lapas ir īpaši izstrādātas kreditoru rēķinu mobilo scenāriju izstrādei.</span><span class="sxs-lookup"><span data-stu-id="5ec30-202">The new pages that are available have been designed specifically for developing mobile scenarios for vendor invoice.</span></span> <span data-ttu-id="5ec30-203">Tāpēc ir jāizmanto šīs lapas.</span><span class="sxs-lookup"><span data-stu-id="5ec30-203">Therefore, you must use these pages.</span></span> <span data-ttu-id="5ec30-204">Vietrādim URL ir jālīdzinās šim vietrādim URL, un pēc tā ievades ir jātiek atvērtai attēlā redzamajai lapai: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile</span><span class="sxs-lookup"><span data-stu-id="5ec30-204">The URL should resemble the following URL, and after you enter it, the page that is shown in the illustration must appear: https://&lt;yourURL&gt;/?cmp=usmf&mi=**VendMobileInvoiceAssignedToMeListPage**&mode=mobile</span></span> 

    <span data-ttu-id="5ec30-205">[![Gaidošie kreditoru rēķini, kas piešķirti man lapa](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span><span class="sxs-lookup"><span data-stu-id="5ec30-205">[![Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals01-1024x281.png)](./media/mobile-invoice-approvals01.png)</span></span>
    
2.  <span data-ttu-id="5ec30-206">Noklikšķiniet uz pogas **Iestatījumi** (zobrats) lapas augšējā labajā stūrī un pēc tam noklikšķiniet uz **Mobilā programma**.</span><span class="sxs-lookup"><span data-stu-id="5ec30-206">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>
3.  <span data-ttu-id="5ec30-207">Atlasiet savu darbvietu un noklikšķiniet uz **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="5ec30-207">Select your workspace and click **Edit**</span></span>
4.  <span data-ttu-id="5ec30-208">Noklikšķiniet uz **Pievienot lapu**, lai izveidotu pirmo mobilo lapu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-208">Click **Add page** to create the first mobile page.</span></span>
5.  <span data-ttu-id="5ec30-209">Ievadiet nosaukumu, piemēram, **Mani kreditoru rēķini**, un aprakstu, piemēram, **Man pārskatīšanai piešķirtie kreditoru rēķini**.</span><span class="sxs-lookup"><span data-stu-id="5ec30-209">Enter a name, such as **My vendor invoices**, and a description, such as **Vendor invoices assigned to me for review**.</span></span>
6.  <span data-ttu-id="5ec30-210">Noklikšķiniet uz **Gatavs**.</span><span class="sxs-lookup"><span data-stu-id="5ec30-210">Click **Done**.</span></span>
7.  <span data-ttu-id="5ec30-211">Mobilo programmu veidotāja cilnē **Lauki** noklikšķiniet uz **Atlasīt laukus**.</span><span class="sxs-lookup"><span data-stu-id="5ec30-211">In the mobile designer, on the **Fields** tab, click **Select fields**.</span></span> <span data-ttu-id="5ec30-212">Saraksta lapā redzamajām kolonnām ir jālīdzinās tālāk esošajam attēlam.</span><span class="sxs-lookup"><span data-stu-id="5ec30-212">The columns on the list page must resemble the following illustration.</span></span> 

    <span data-ttu-id="5ec30-213">[![Kolonnas lapā Gaidošie kreditoru rēķini, kas piešķirti man](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span><span class="sxs-lookup"><span data-stu-id="5ec30-213">[![Columns on the Pending vendor invoices assigned to me page](./media/mobile-invoice-approvals02-1024x117.png)](./media/mobile-invoice-approvals02.png)</span></span>
    
8.  <span data-ttu-id="5ec30-214">Pievienojiet tās kolonnas no saraksta lapas, kuras ir jārāda lietotājiem mobilajā lapā.</span><span class="sxs-lookup"><span data-stu-id="5ec30-214">Add the required columns from the list page that must be shown to the users in the mobile page.</span></span> <span data-ttu-id="5ec30-215">Pievienošanas secība atbilst secībai, kādā laiki tiek rādīti lietotājam.</span><span class="sxs-lookup"><span data-stu-id="5ec30-215">The order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="5ec30-216">Vienīgais veids, kā mainīt laiku secību, ir atkārtoti atlasīt visus laukus.</span><span class="sxs-lookup"><span data-stu-id="5ec30-216">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> <span data-ttu-id="5ec30-217">Pamatojoties uz šī scenārija prasībām, ir nepieciešami astoņi tālāk norādītie lauki.</span><span class="sxs-lookup"><span data-stu-id="5ec30-217">Based on the requirements for this scenario, the following eight fields are required.</span></span> <span data-ttu-id="5ec30-218">Taču dažiem lietotājiem var šķist, ka astoņi lauki ir pārāk daudz informācijas, ko skatīt mobilajā ierīcē.</span><span class="sxs-lookup"><span data-stu-id="5ec30-218">However, some users might consider eight fields too much information to have on a mobile device.</span></span> <span data-ttu-id="5ec30-219">Tāpēc mobilās lapas saraksta skatā tiks rādīti tika svarīgākie lauki.</span><span class="sxs-lookup"><span data-stu-id="5ec30-219">Therefore, we will show only the most important fields in the mobile list view.</span></span> <span data-ttu-id="5ec30-220">Pārējie laiki tiks rādīti detalizētās informācijas skatā, kas tiks izstrādāts vēlāk.</span><span class="sxs-lookup"><span data-stu-id="5ec30-220">The remaining fields will appear in the details view that we will design later.</span></span> <span data-ttu-id="5ec30-221">Pagaidām tiks pievienoti tālāk norādītie lauki.</span><span class="sxs-lookup"><span data-stu-id="5ec30-221">For now, we will add the following fields.</span></span> <span data-ttu-id="5ec30-222">Noklikšķiniet uz pluszīmes (**+**) šajās kolonnās, lai pievienoto mobilajai lapai.</span><span class="sxs-lookup"><span data-stu-id="5ec30-222">Click the plus sign (**+**) in these columns to add to the mobile page.</span></span>
    - <span data-ttu-id="5ec30-223">Kreditora nosaukums</span><span class="sxs-lookup"><span data-stu-id="5ec30-223">Vendor name</span></span>
    - <span data-ttu-id="5ec30-224">Rēķina kopsumma</span><span class="sxs-lookup"><span data-stu-id="5ec30-224">Invoice total</span></span>
    - <span data-ttu-id="5ec30-225">Rēķina konts</span><span class="sxs-lookup"><span data-stu-id="5ec30-225">Invoice account</span></span>
    - <span data-ttu-id="5ec30-226">Rēķina numurs</span><span class="sxs-lookup"><span data-stu-id="5ec30-226">Invoice number</span></span>
    - <span data-ttu-id="5ec30-227">Rēķina datums</span><span class="sxs-lookup"><span data-stu-id="5ec30-227">Invoice date</span></span>

    <span data-ttu-id="5ec30-228">Pēc laiku pievienošanas mobilajai lapai ir jālīdzinās tālāk esošajam attēlam.</span><span class="sxs-lookup"><span data-stu-id="5ec30-228">After the fields are added, the mobile page must resemble the following illustration.</span></span> 
    
    <span data-ttu-id="5ec30-229">[![Lapa pēc lauku pievienošanas](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span><span class="sxs-lookup"><span data-stu-id="5ec30-229">[![Page after fields are added](./media/mobile-invoice-approvals03.png)](./media/mobile-invoice-approvals03.png)</span></span>

9.  <span data-ttu-id="5ec30-230">Tagad ir jāpievieno arī tālāk norādītās kolonnas, lai vēlāk varētu iespējot darbplūsmas darbības.</span><span class="sxs-lookup"><span data-stu-id="5ec30-230">You must also add the following columns now, so that we can enable workflow actions later.</span></span>
    - <span data-ttu-id="5ec30-231">Rādīt pabeigšanas uzdevumu</span><span class="sxs-lookup"><span data-stu-id="5ec30-231">Show complete task</span></span>
    - <span data-ttu-id="5ec30-232">Rādīt deleģēšanas uzdevumu</span><span class="sxs-lookup"><span data-stu-id="5ec30-232">Show delegate task</span></span>
    - <span data-ttu-id="5ec30-233">Rādīt atsaukšanas uzdevumu</span><span class="sxs-lookup"><span data-stu-id="5ec30-233">Show recall task</span></span>
    - <span data-ttu-id="5ec30-234">Rādīt noraidīšanas uzdevumu</span><span class="sxs-lookup"><span data-stu-id="5ec30-234">Show reject task</span></span>
    - <span data-ttu-id="5ec30-235">Rādīt pabeigšanas pieprasījuma uzdevumu</span><span class="sxs-lookup"><span data-stu-id="5ec30-235">Show request completion task</span></span>
    - <span data-ttu-id="5ec30-236">Rādīt atkārtotas iesniegšanas uzdevumu</span><span class="sxs-lookup"><span data-stu-id="5ec30-236">Show resubmit task</span></span>

10. <span data-ttu-id="5ec30-237">Noklikšķiniet uz **Gatavs**, lai izslēgtu rediģēšanas režīmu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-237">Click **Done** to exit edit mode.</span></span>
11. <span data-ttu-id="5ec30-238">Noklikšķiniet uz **Atpakaļ** un pēc tam uz **Gatavs**, lai aizvērtu darbvietu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-238">Click **Back** and then **Done** to exit the workspace</span></span>
12. <span data-ttu-id="5ec30-239">Noklikšķiniet uz **Publicēt darbvietu**, lai saglabātu darbu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-239">Click **Publish workspace** to save your work.</span></span>
13. <span data-ttu-id="5ec30-240">Parādu kreditoriem parametru veidlapas sadaļā **Rēķins** iespējojiet opiju **Rādīt rēķina kopsummu gaidošo kreditoru rēķinu sarakstā**.</span><span class="sxs-lookup"><span data-stu-id="5ec30-240">Enable **Display invoice total on pending vendor invoices list** in accounts payable parameters form under **Invoice**.</span></span> <span data-ttu-id="5ec30-241">Ņemiet vērā, ka rēķinu kopsummas tiek aprēķinātas un rādītas gaidošo kreditoru rēķinu saraksta lapā tikai tad, ja ir iespējots šis parametrs.</span><span class="sxs-lookup"><span data-stu-id="5ec30-241">Note that, only by enabling this parameter, invoice totals will be calculated to be displayed on the pending vendor invoices list page.</span></span> <span data-ttu-id="5ec30-242">Tā ir jauna iespēja, kas ir ietverta priekšnoteikuma labojumfailā KB 3208224.</span><span class="sxs-lookup"><span data-stu-id="5ec30-242">This is a new capability as part of the pre-requisite hot fix 3208224.</span></span>

### <a name="vendor-invoice-details"></a><span data-ttu-id="5ec30-243">Kreditora rēķina detalizēta informācija</span><span class="sxs-lookup"><span data-stu-id="5ec30-243">Vendor invoice details</span></span>

<span data-ttu-id="5ec30-244">Lai izstrādātu rēķina detalizētas informācijas lapu mobilajām ierīcēm, izmantojiet lapu **VendMobileInvoiceHeaderDetails**.</span><span class="sxs-lookup"><span data-stu-id="5ec30-244">To design the invoice details page for mobile, use the **VendMobileInvoiceHeaderDetails** page.</span></span> <span data-ttu-id="5ec30-245">Ņemiet vērā, ka atkarībā no rēķinu skaita jūsu sistēmā šajā lapā tiek rādīti vecākie rēķini (rēķini, kas tika izveidoti pirmie).</span><span class="sxs-lookup"><span data-stu-id="5ec30-245">Note that, depending on the number of invoices that you have in your system, this page shows the oldest invoice (the invoice that was created first).</span></span> <span data-ttu-id="5ec30-246">Lai atrastu konkrētu rēķinu, varat izmantot kreisajā pusē esošo filtru.</span><span class="sxs-lookup"><span data-stu-id="5ec30-246">To find a specific invoice, you can use the filter on the left.</span></span> <span data-ttu-id="5ec30-247">Taču šī piemēra ietvaros nav nepieciešams konkrēts rēķins.</span><span class="sxs-lookup"><span data-stu-id="5ec30-247">However, we don’t require a specific invoice for this example.</span></span> <span data-ttu-id="5ec30-248">Ir nepieciešami dažu rēķinu dati, lai varētu izstrādāt mobilo lapu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-248">We just require some invoice data so that we can design the mobile page.</span></span> 

<span data-ttu-id="5ec30-249">[![Lapa Darbplūsma](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span><span class="sxs-lookup"><span data-stu-id="5ec30-249">[![Workflow page](./media/mobile-invoice-approvals04-1024x425.png)](./media/mobile-invoice-approvals04.png)</span></span>

1. <span data-ttu-id="5ec30-250">Vietrādī URL izvēlnes vienuma nosaukumu aizstājiet ar **VendMobileInvoiceHeaderDetails**, lai atvērtu formu</span><span class="sxs-lookup"><span data-stu-id="5ec30-250">In the URL, replace the name of the menu item with **VendMobileInvoiceHeaderDetails** to open the form</span></span>

2. <span data-ttu-id="5ec30-251">Atveriet mobilo programmu veidotāju, izmantojot pogu **Iestatījumi** (zobrats).</span><span class="sxs-lookup"><span data-stu-id="5ec30-251">Open the mobile designer from the **Settings** (gear) button.</span></span>

3. <span data-ttu-id="5ec30-252">Noklikšķiniet uz pogas **Rediģēt**, lai darbvietā ieslēgtu rediģēšanas režīmu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-252">Click the **Edit** button to start edit mode in the workspace.</span></span>

4. <span data-ttu-id="5ec30-253">Atlasiet lapu **Mani kreditoru rēķini**, ko iepriekš izveidojāt, un pēc tam noklikšķiniet uz **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="5ec30-253">Select the **My vendor invoices** page that you created earlier, and then click **Edit**.</span></span>

5. <span data-ttu-id="5ec30-254">Cilnē **Lauki** noklikšķiniet uz kolonnas galvenes **Režģis**.</span><span class="sxs-lookup"><span data-stu-id="5ec30-254">On the **Fields** tab, click the **Grid** column heading.</span></span>

6. <span data-ttu-id="5ec30-255">Noklikšķiniet uz **Rekvizīti &gt; Pievienot lapu**.</span><span class="sxs-lookup"><span data-stu-id="5ec30-255">Click **Properties &gt; Add page**.</span></span> <span data-ttu-id="5ec30-256">**Piezīme.** Kad noklikšķināt uz galvenes **Režģis** un pievienojat lapu, tiek automātiski izveidotas attiecības ar detalizētas informācijas lapu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-256">**Note:** When you click the **Grid** heading and add a page, the relationship with the details page is established automatically.</span></span>

7. <span data-ttu-id="5ec30-257">Ievadiet lapas nosaukumu, piemēram, **Rēķina detalizēta informācija**, un aprakstu, piemēram, **Skatīt rēķina galvenes un rindu detalizētu informāciju**.</span><span class="sxs-lookup"><span data-stu-id="5ec30-257">Enter a page title, such as **Invoice details**, and a description, such as **View invoice header and line details**.</span></span>

8. <span data-ttu-id="5ec30-258">Noklikšķiniet uz **Atlasīt laukus**.</span><span class="sxs-lookup"><span data-stu-id="5ec30-258">Click **Select fields**.</span></span> <span data-ttu-id="5ec30-259">Ņemiet vērā, ka pievienošanas secība atbilst secībai, kādā laiki tiek rādīti lietotājam.</span><span class="sxs-lookup"><span data-stu-id="5ec30-259">Note that, the order in which you add is the order in which the fields will be displayed to the end user.</span></span> <span data-ttu-id="5ec30-260">Vienīgais veids, kā mainīt laiku secību, ir atkārtoti atlasīt visus laukus.</span><span class="sxs-lookup"><span data-stu-id="5ec30-260">The only way to change the ordering of the fields will be by re-selecting all the fields.</span></span> 

9. <span data-ttu-id="5ec30-261">Pievienojiet tālāk norādītos laukus no galvenes, pamatojoties uz šī scenārija prasībām.</span><span class="sxs-lookup"><span data-stu-id="5ec30-261">Add the following fields from the header, based on the requirements for this scenario:</span></span>
   - <span data-ttu-id="5ec30-262">Kreditora nosaukums</span><span class="sxs-lookup"><span data-stu-id="5ec30-262">Vendor name</span></span>
   - <span data-ttu-id="5ec30-263">Rēķina kopsumma</span><span class="sxs-lookup"><span data-stu-id="5ec30-263">Invoice total</span></span>
   - <span data-ttu-id="5ec30-264">Rēķina konts</span><span class="sxs-lookup"><span data-stu-id="5ec30-264">Invoice account</span></span>
   - <span data-ttu-id="5ec30-265">Rēķina numurs</span><span class="sxs-lookup"><span data-stu-id="5ec30-265">Invoice number</span></span>
   - <span data-ttu-id="5ec30-266">Rēķina datums</span><span class="sxs-lookup"><span data-stu-id="5ec30-266">Invoice date</span></span>
   - <span data-ttu-id="5ec30-267">Rēķina apraksts</span><span class="sxs-lookup"><span data-stu-id="5ec30-267">Invoice description</span></span>
   - <span data-ttu-id="5ec30-268">Izpildes termiņš</span><span class="sxs-lookup"><span data-stu-id="5ec30-268">Due date</span></span>
   - <span data-ttu-id="5ec30-269">Rēķina valūta</span><span class="sxs-lookup"><span data-stu-id="5ec30-269">Invoice currency</span></span>

10. <span data-ttu-id="5ec30-270">Pievienojiet tālāk norādītos laukus no lapas rindu režģa.</span><span class="sxs-lookup"><span data-stu-id="5ec30-270">Add the following fields from the lines grid on the page:</span></span>
    - <span data-ttu-id="5ec30-271">Sagādes kategorija</span><span class="sxs-lookup"><span data-stu-id="5ec30-271">Procurement category</span></span>
    - <span data-ttu-id="5ec30-272">Daudzums</span><span class="sxs-lookup"><span data-stu-id="5ec30-272">Quantity</span></span>
    - <span data-ttu-id="5ec30-273">Vienības cena</span><span class="sxs-lookup"><span data-stu-id="5ec30-273">Unit price</span></span>
    - <span data-ttu-id="5ec30-274">Rindas neto summa</span><span class="sxs-lookup"><span data-stu-id="5ec30-274">Line net amount</span></span>
    - <span data-ttu-id="5ec30-275">1099. summa</span><span class="sxs-lookup"><span data-stu-id="5ec30-275">1099 amount</span></span>

11. <span data-ttu-id="5ec30-276">Kad ir pievienoti visi divu iepriekšējo darbību aprakstā norādītie lauki, noklikšķiniet uz **Gatavs**.</span><span class="sxs-lookup"><span data-stu-id="5ec30-276">After all the fields from the previous two steps have been added, click **Done**.</span></span> <span data-ttu-id="5ec30-277">Lapai ir jālīdzinās tālāk esošajam attēlam.</span><span class="sxs-lookup"><span data-stu-id="5ec30-277">The page must resemble the following illustration.</span></span>
    
    <span data-ttu-id="5ec30-278">[![Lapa pēc lauku pievienošanas](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span><span class="sxs-lookup"><span data-stu-id="5ec30-278">[![Page after fields are added](./media/mobile-invoice-approvals05.png)](./media/mobile-invoice-approvals05.png)</span></span>

12. <span data-ttu-id="5ec30-279">Noklikšķiniet uz **Gatavs**, lai izslēgtu rediģēšanas režīmu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-279">Click **Done** to exit edit mode.</span></span>

13. <span data-ttu-id="5ec30-280">Noklikšķiniet uz **Atpakaļ** un pēc tam uz **Gatavs**, lai aizvērtu darbvietu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-280">Click **Back** and then **Done** to exit the workspace</span></span>

14. <span data-ttu-id="5ec30-281">Noklikšķiniet uz **Publicēt darbvietu**, lai saglabātu darbu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-281">Click **Publish workspace** to save your work</span></span>

### <a name="workflow-actions"></a><span data-ttu-id="5ec30-282">Darbplūsmas darbības</span><span class="sxs-lookup"><span data-stu-id="5ec30-282">Workflow actions</span></span>

<span data-ttu-id="5ec30-283">Lai pievienotu darbplūsmas darbības, izmantojiet lapu **VendMobileInvoiceHeaderDetails**.</span><span class="sxs-lookup"><span data-stu-id="5ec30-283">To add workflow actions, use the **VendMobileInvoiceHeaderDetails** page.</span></span> <span data-ttu-id="5ec30-284">Lai atvērtu šo lapu, aizstājiet izvēlnes elementa nosaukumu URL tekstā, kā to darījāt iepriekš.</span><span class="sxs-lookup"><span data-stu-id="5ec30-284">To open this page, replace the name of the menu item in the URL, as you did earlier.</span></span> <span data-ttu-id="5ec30-285">Pēc tam tveriet mobilo programmu veidotāju, izmantojot pogu **Iestatījumi** (zobrats).</span><span class="sxs-lookup"><span data-stu-id="5ec30-285">Then open the mobile designer from the **Settings** (gear) button.</span></span> <span data-ttu-id="5ec30-286">Izpildiet tālāk norādītās darbības, lai pievienotu darbplūsmas darbības detalizētas informācijas lapā.</span><span class="sxs-lookup"><span data-stu-id="5ec30-286">Follow these steps to add workflow actions on the details page.</span></span> <span data-ttu-id="5ec30-287">Lai jums kļūtu pieejamas darbplūsmas darbības, kurām vēlaties veidot noformējumu, jums ir jābūt piešķirtiem rēķiniem, kuri atrodas atbilstošajā stāvoklī.</span><span class="sxs-lookup"><span data-stu-id="5ec30-287">You must have invoices assigned to you that are in the appropriate state to make the workflow actions available to you that you are going to design for.</span></span>

#### <a name="record-workflow-actions"></a><span data-ttu-id="5ec30-288">Ieraksta darbplūsmas darbības</span><span class="sxs-lookup"><span data-stu-id="5ec30-288">Record workflow actions</span></span>
1.  <span data-ttu-id="5ec30-289">Noklikšķiniet uz pogas **Rediģēt**, lai darbvietā ieslēgtu rediģēšanas režīmu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-289">Click the **Edit** button to start edit mode in the workspace.</span></span>
2.  <span data-ttu-id="5ec30-290">Atlasiet lapu **Rēķina detalizēta informācija**, ko iepriekš izveidojāt, un pēc tam noklikšķiniet uz **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="5ec30-290">Select the **Invoice details** page that you created earlier, and then click **Edit**.</span></span>
3.  <span data-ttu-id="5ec30-291">Cilnē **Darbības** noklikšķiniet uz **Pievienot darbību**.</span><span class="sxs-lookup"><span data-stu-id="5ec30-291">On the **Actions** tab, click **Add action**.</span></span>
4.  <span data-ttu-id="5ec30-292">Ievadiet darbības nosaukumu, piemēram, **Apstiprināt**, un aprakstu, piemēram, **Apstiprināt rēķinu**.</span><span class="sxs-lookup"><span data-stu-id="5ec30-292">Enter an action title, such as **Approve**, and a description, such as **Approve invoice**.</span></span> <span data-ttu-id="5ec30-293">Ņemiet vērā, ka šeit ievadītais darbības nosaukums kļūst par darbības nosaukumu, kas tiek rādīts lietotājam mobilajā programmā.</span><span class="sxs-lookup"><span data-stu-id="5ec30-293">Note that the action title that you enter here becomes the name of the action that is shown to the user in the mobile app.</span></span>
5.  <span data-ttu-id="5ec30-294">Noklikšķiniet uz **Gatavs**.</span><span class="sxs-lookup"><span data-stu-id="5ec30-294">Click **Done**.</span></span>
6.  <span data-ttu-id="5ec30-295">Noklikšķiniet uz **Atlasīt laukus**.</span><span class="sxs-lookup"><span data-stu-id="5ec30-295">Click **Select fields**.</span></span>
7.  <span data-ttu-id="5ec30-296">Pārskatiet darbplūsmas procesu lapā **VendMobileInvoiceHeaderDetails** un veiciet darbību, ko vēlaties ierakstīt.</span><span class="sxs-lookup"><span data-stu-id="5ec30-296">Go through the workflow process on the **VendMobileInvoiceHeaderDetails** page, and complete the action that you wanted to record.</span></span> <span data-ttu-id="5ec30-297">Šī procesa laikā noteikti ievadiet darbplūsmas komentārus, lai mobilajā risinājumā tiktu ietverts arī komentāru lauks.</span><span class="sxs-lookup"><span data-stu-id="5ec30-297">Make sure that you enter workflow comments during this process, so that a comments field is also included in the mobile experience.</span></span>
8.  <span data-ttu-id="5ec30-298">Pēc darbplūsmas darbības veikšanas noklikšķiniet uz **Gatavs**, lai pabeigtu darbību Atlasīt laukus.</span><span class="sxs-lookup"><span data-stu-id="5ec30-298">After the workflow action is run, click **Done** to complete the Select fields task.</span></span>
9.  <span data-ttu-id="5ec30-299">Noklikšķiniet uz **Gatavs**, lai izslēgtu rediģēšanas režīmu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-299">Click **Done** to exit edit mode.</span></span>
10. <span data-ttu-id="5ec30-300">Noklikšķiniet uz **Atpakaļ** un pēc tam uz **Gatavs**, lai aizvērtu darbvietu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-300">Click **Back** and then **Done** to exit the workspace</span></span>
11. <span data-ttu-id="5ec30-301">Noklikšķiniet uz **Publicēt darbvietu**, lai saglabātu darbu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-301">Click **Publish workspace** to save your work</span></span>
12. <span data-ttu-id="5ec30-302">Atkārtojiet iepriekšējās darbības, lai ierakstītu visas nepieciešamās darbplūsmas darbības.</span><span class="sxs-lookup"><span data-stu-id="5ec30-302">Repeat the previous steps to record all the required workflow actions.</span></span> 

#### <a name="create-a-js-file"></a><span data-ttu-id="5ec30-303">Izveidot .js failu</span><span class="sxs-lookup"><span data-stu-id="5ec30-303">Create a .js file</span></span>
1. <span data-ttu-id="5ec30-304">Atveriet programmu Piezīmjbloks vai Microsoft Visual Studio un ielīmējiet tālāk norādīto kodu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-304">Open Notepad or Microsoft Visual Studio, and paste the following code.</span></span> <span data-ttu-id="5ec30-305">Saglabājiet failu .js formātā.</span><span class="sxs-lookup"><span data-stu-id="5ec30-305">Save the file as a .js file.</span></span> <span data-ttu-id="5ec30-306">Šis kods tālāk aprakstītos uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="5ec30-306">This code does the following:</span></span>
    - <span data-ttu-id="5ec30-307">Tas paslēpj ar darbplūsmu saistītās papildu kolonnas, kas iepriekš tika pievienotas mobilajā saraksta lapā.</span><span class="sxs-lookup"><span data-stu-id="5ec30-307">It hides the extra workflow-related columns that we added earlier on the mobile list page.</span></span> <span data-ttu-id="5ec30-308">Šīs kolonnas tika pievienotas, lai programmā būtu pieejama šī informācija kontekstā un varētu veikt nākamo darbību.</span><span class="sxs-lookup"><span data-stu-id="5ec30-308">We added these columns so that the app has that information in context and can do the next step.</span></span>
    - <span data-ttu-id="5ec30-309">Pamatojoties uz aktīvajiem darbplūsmas soļiem, tiek lietota loģika, lai rādītu tikai šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="5ec30-309">Based on the workflow step that is active, it applies logic to show only those actions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5ec30-310">Lapu un citu vadīklu nosaukumiem kodā ir jābūt tādiem pašiem kā nosaukumiem darbvietā.</span><span class="sxs-lookup"><span data-stu-id="5ec30-310">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    ```javascript
    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                       var showRejectControl = Boolean(rejectControl == 1);
                      var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                     metadataService.configureAction('Resubmit', { visible: showResubmitControl });
                   }
                 },
           };
        }
    ```

2.  <span data-ttu-id="5ec30-311">Augšupielādējiet koda failu darbvietā, atlasot cilni **Loģika**.</span><span class="sxs-lookup"><span data-stu-id="5ec30-311">Upload the code file to the workspace by selecting the **Logic** tab</span></span>
3.  <span data-ttu-id="5ec30-312">Noklikšķiniet uz **Gatavs**, lai izslēgtu rediģēšanas režīmu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-312">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="5ec30-313">Noklikšķiniet uz **Atpakaļ** un pēc tam uz **Gatavs**, lai aizvērtu darbvietu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-313">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="5ec30-314">Noklikšķiniet uz **Publicēt darbvietu**, lai saglabātu darbu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-314">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-attachments"></a><span data-ttu-id="5ec30-315">Kreditoru rēķinu pielikumi</span><span class="sxs-lookup"><span data-stu-id="5ec30-315">Vendor invoice attachments</span></span>

1. <span data-ttu-id="5ec30-316">Noklikšķiniet uz pogas **Iestatījumi** (zobrats) lapas augšējā labajā stūrī un pēc tam noklikšķiniet uz **Mobilā programma**.</span><span class="sxs-lookup"><span data-stu-id="5ec30-316">Click the **Settings** (gear) button in the upper right of the page, and then click **Mobile app**</span></span>

2. <span data-ttu-id="5ec30-317">Noklikšķiniet uz pogas **Rediģēt**, lai darbvietā ieslēgtu rediģēšanas režīmu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-317">Click the **Edit** button to start edit mode in the workspace.</span></span>

3. <span data-ttu-id="5ec30-318">Atlasiet lapu <strong>Rēķina detalizēta informācija\*\*, ko iepriekš izveidojāt, un pēc tam noklikšķiniet uz \*\*Rediģēt</strong>.</span><span class="sxs-lookup"><span data-stu-id="5ec30-318">Select the <strong>Invoice details \*\*page that you created earlier, and then click \*\*Edit</strong>.</span></span>

4. <span data-ttu-id="5ec30-319">Iestatiet opcijas **Dokumentu vadība** vērtību **Ja**, kā tas ir redzams tālāk.</span><span class="sxs-lookup"><span data-stu-id="5ec30-319">Set the **Document management** option to **Yes** as shown below.</span></span> <span data-ttu-id="5ec30-320">**Piezīme.** Ja nav nepieciešams rādīt pielikumus mobilajā ierīcē, varat atstāt šīs opcijas vērtību **Nē**, kas ir noklusējuma iestatījums.</span><span class="sxs-lookup"><span data-stu-id="5ec30-320">**Note:** If there are no requirements to show attachments on the mobile device, you can leave this option set to **No**, which is the default setting.</span></span>
   
   ![Dokumentu vadība](./media/docmanagement-216x300.png)

5. <span data-ttu-id="5ec30-322">Noklikšķiniet uz **Gatavs**, lai izslēgtu rediģēšanas režīmu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-322">Click **Done** to exit edit mode.</span></span>

6. <span data-ttu-id="5ec30-323">Noklikšķiniet uz **Atpakaļ** un pēc tam uz **Gatavs**, lai aizvērtu darbvietu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-323">Click **Back** and then **Done** to exit the workspace</span></span>

7. <span data-ttu-id="5ec30-324">Noklikšķiniet uz **Publicēt darbvietu**, lai saglabātu darbu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-324">Click **Publish workspace** to save your work</span></span>

### <a name="vendor-invoice-line-distributions"></a><span data-ttu-id="5ec30-325">Kreditora rēķina rindas sadales</span><span class="sxs-lookup"><span data-stu-id="5ec30-325">Vendor invoice line distributions</span></span>

<span data-ttu-id="5ec30-326">Saskaņā ar šī scenārija prasībām tiks lietotas tikai rindas līmeņa sadales un rēķinā vienmēr būs tikai viena rinda.</span><span class="sxs-lookup"><span data-stu-id="5ec30-326">The requirements for this scenario confirm that there will be only line-level distributions, and that an invoice will always have only one line.</span></span> <span data-ttu-id="5ec30-327">Tā kā šis ir vienkāršs scenārijs, arī lietotāja iespējām mobilajā ierīcē ir jābūt pietiekami vienkāršām, sniedzot lietotājam iespēju skatīt sadales, nepiekļūstot vairākiem zemākiem līmeņiem.</span><span class="sxs-lookup"><span data-stu-id="5ec30-327">Because this scenario is simple, the user experience on the mobile device must also be simple enough that the user doesn’t have to drill down several levels to view the distributions.</span></span> <span data-ttu-id="5ec30-328">Kreditoru rēķinos ir ietverta opcija visas sadales parādīšanai no rēķina virsraksta.</span><span class="sxs-lookup"><span data-stu-id="5ec30-328">Vendor invoices include the option of showing all distributions from the invoice header.</span></span> <span data-ttu-id="5ec30-329">Šis risinājums ir jāizmanto mobilajā scenārijā.</span><span class="sxs-lookup"><span data-stu-id="5ec30-329">This experience is what we need for the mobile scenario.</span></span> <span data-ttu-id="5ec30-330">Tāpēc šīs mobilā scenārija daļās izstrādei ir jāizmanto lapa **VendMobileInvoiceAllDistributionTree**.</span><span class="sxs-lookup"><span data-stu-id="5ec30-330">Therefore, we will use the **VendMobileInvoiceAllDistributionTree** page to design this part of the mobile scenario.</span></span> 

> [!NOTE] 
> <span data-ttu-id="5ec30-331">Tas, ka ir zināmas prasības, palīdz scenārija izstrādes laikā izvēlēties konkrētu izmantojamo lapu un to, kā optimizēt mobilo risinājumu atbilstoši lietotāja vajadzībām.</span><span class="sxs-lookup"><span data-stu-id="5ec30-331">Knowing the requirements helps us decide which specific page to use and how exactly to optimize the mobile experience for the user when we design the scenario.</span></span> <span data-ttu-id="5ec30-332">Otrā scenārija ietvaros sadales rādīšanai tiks izmantotas citas lapas, jo šī scenārija prasības atšķiras.</span><span class="sxs-lookup"><span data-stu-id="5ec30-332">In the second scenario, we will use a different page to show the distributions, because the requirements for that scenario differ.</span></span>

1.  <span data-ttu-id="5ec30-333">Aizstājiet izvēlnes elementa nosaukumu URL tekstā, kā to darījāt iepriekš.</span><span class="sxs-lookup"><span data-stu-id="5ec30-333">In the URL, replace the name of the menu item, as you did before.</span></span> <span data-ttu-id="5ec30-334">Parādītajai lapai ir jālīdzinās tālāk esošajam attēlam.</span><span class="sxs-lookup"><span data-stu-id="5ec30-334">The page that appears should resemble the following illustration.</span></span>

    <span data-ttu-id="5ec30-335">[![Lapa Visas sadales](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span><span class="sxs-lookup"><span data-stu-id="5ec30-335">[![All distributions page](./media/mobile-invoice-approvals06.png)](./media/mobile-invoice-approvals06.png)</span></span>

2.  <span data-ttu-id="5ec30-336">Atveriet mobilo programmu veidotāju, izmantojot pogu **Iestatījumi** (zobrats).</span><span class="sxs-lookup"><span data-stu-id="5ec30-336">Open the mobile designer from the **Settings** (gear) button.</span></span>

3.  <span data-ttu-id="5ec30-337">Noklikšķiniet uz pogas **Rediģēt**, lai darbvietā ieslēgtu rediģēšanas režīmu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-337">Click the **Edit** button to start edit mode in the workspace.</span></span> <span data-ttu-id="5ec30-338">**Piezīme.** Ir automātiski izveidotas divas jaunas lapas.</span><span class="sxs-lookup"><span data-stu-id="5ec30-338">**Note:** You will see that two new pages were created automatically.</span></span> <span data-ttu-id="5ec30-339">Sistēmā šīs lapas tiek izveidotas, jo, veicot iepriekšējā sadaļā aprakstītās darbības, jūs ieslēdzāt dokumentu vadību.</span><span class="sxs-lookup"><span data-stu-id="5ec30-339">The system creates these pages, because you turned on document management in the previous section.</span></span> <span data-ttu-id="5ec30-340">Varat ignorēt šīs divas lapas.</span><span class="sxs-lookup"><span data-stu-id="5ec30-340">You can ignore these new pages.</span></span>

4.  <span data-ttu-id="5ec30-341">Noklikšķiniet uz **Pievienot lapu**.</span><span class="sxs-lookup"><span data-stu-id="5ec30-341">Click **Add page**.</span></span>

5.  <span data-ttu-id="5ec30-342">Ievadiet lapas nosaukumu, piemēram, **Skatīt uzskaiti**, un aprakstu, piemēram, **Skatīt rēķina uzskaiti**.</span><span class="sxs-lookup"><span data-stu-id="5ec30-342">Enter a page title, such as **View accounting**, and a description, such as **View accounting for the invoice**.</span></span>

6.  <span data-ttu-id="5ec30-343">Noklikšķiniet uz **Gatavs**.</span><span class="sxs-lookup"><span data-stu-id="5ec30-343">Click **Done**.</span></span>

7.  <span data-ttu-id="5ec30-344">Cilnē **Lauki** noklikšķiniet uz **Atlasīt laukus**, sadales elementu lapā atlasiet tālāk norādītos laukus un pēc tam noklikšķiniet uz **Gatavs**:</span><span class="sxs-lookup"><span data-stu-id="5ec30-344">On the **Fields** tab, click **Select fields**, select the following fields from the distributions page, and then click **Done**:</span></span>
    1.  <span data-ttu-id="5ec30-345">Summa</span><span class="sxs-lookup"><span data-stu-id="5ec30-345">Amount</span></span>
    2.  <span data-ttu-id="5ec30-346">Valūta</span><span class="sxs-lookup"><span data-stu-id="5ec30-346">Currency</span></span>
    3.  <span data-ttu-id="5ec30-347">Virsgrāmatas konts</span><span class="sxs-lookup"><span data-stu-id="5ec30-347">Ledger account</span></span>

    > [!NOTE] 
    > <span data-ttu-id="5ec30-348">Sadales režģī netika atlasīta kolonna **Apraksts**, jo saskaņā ar šī scenārija prasībām pilna cena ir vienīgā summa, kam ir sadale.</span><span class="sxs-lookup"><span data-stu-id="5ec30-348">We didn’t select the **Description** column from the distributions grid, because the requirements for this scenario confirmed that the extended price is the only amount that there will be distributions for.</span></span> <span data-ttu-id="5ec30-349">Tāpēc lietotājam nebūs vajadzīgs cits lauks, lai norādīto summas veidu, uz ko attiecas sadale.</span><span class="sxs-lookup"><span data-stu-id="5ec30-349">Therefore, the user won’t require another field to determine the amount type that the distribution is for.</span></span> <span data-ttu-id="5ec30-350">Taču nākamā scenārija ietvaros šī informācija **tiks** izmantota, jo saskaņā ar tā scenārija prasībām sadales ir arī citiem summas veidiem (piemēram, PVN).</span><span class="sxs-lookup"><span data-stu-id="5ec30-350">However, in the next scenario, we **will** use this information, because the requirements for that scenario specify that other amount types have distributions (for example, sales tax).</span></span>

8.  <span data-ttu-id="5ec30-351">Noklikšķiniet uz **Gatavs**, lai izslēgtu rediģēšanas režīmu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-351">Click **Done** to exit edit mode.</span></span>

9.  <span data-ttu-id="5ec30-352">Noklikšķiniet uz **Atpakaļ** un pēc tam uz **Gatavs**, lai aizvērtu darbvietu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-352">Click **Back** and then **Done** to exit the workspace</span></span>

10. <span data-ttu-id="5ec30-353">Noklikšķiniet uz **Publicēt darbvietu**, lai saglabātu darbu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-353">Click **Publish workspace** to save your work</span></span>

#### <a name="adding-navigation-to-view-accounting-page"></a><span data-ttu-id="5ec30-354">Navigācijas pievienošana lapai "Skatīt uzskaiti"</span><span class="sxs-lookup"><span data-stu-id="5ec30-354">Adding navigation to "View accounting" page</span></span>

<span data-ttu-id="5ec30-355">Mobilā lapa **Skatīt uzskaiti** pašlaik nav saistīta ne ar vienu līdz šim izveidoto mobilo lapu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-355">The **View accounting** mobile page isn’t currently linked to any of the mobile pages that we have designed so far.</span></span> <span data-ttu-id="5ec30-356">Tā kā lietotājam ir jāvar mobilajā ierīcē pāriet no lapas **Rēķina detalizēta informācija** uz lapu **Skatīt uzskaiti**, ir jānodrošina navigācija no lapas **Rēķina detalizēta informācija** uz lapu **Skatīt uzskaiti**.</span><span class="sxs-lookup"><span data-stu-id="5ec30-356">Because the user should be able to navigate to the **View accounting** page from the **Invoice details** page on the mobile device, we must provide navigation from the **Invoice details** page to the **View accounting** page.</span></span> <span data-ttu-id="5ec30-357">Šī navigācija tiek nodrošināta, izmantojot papildu loģiku valodā JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5ec30-357">We establish this navigation by using additional logic via JavaScript.</span></span>

1.  <span data-ttu-id="5ec30-358">Atveriet iepriekš izveidoto .js formāta failu un pievienojiet tālāk esošā koda iezīmētās rindas.</span><span class="sxs-lookup"><span data-stu-id="5ec30-358">Open the .js file that you created earlier, and add the lines that are highlighted in the following code.</span></span> <span data-ttu-id="5ec30-359">Šis kods nodrošina divas darbības.</span><span class="sxs-lookup"><span data-stu-id="5ec30-359">This code does two things:</span></span>
    1.  <span data-ttu-id="5ec30-360">Tas palīdz nodrošināt, ka lietotāji nevar tieši navigēt no darbvietas uz lapu **Skatīt uzskaiti**.</span><span class="sxs-lookup"><span data-stu-id="5ec30-360">It helps guarantee that users can’t navigate directly from the workspace to the **View accounting** page.</span></span>
    2.  <span data-ttu-id="5ec30-361">Tas nodrošina navigācijas vadīklu navigācijai no lapas **Rēķina detalizēta informācija** uz lapu **Skatīt uzskaiti**.</span><span class="sxs-lookup"><span data-stu-id="5ec30-361">It establishes a navigation control from the **Invoice details** page to the **View accounting** page.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="5ec30-362">Lapu un citu vadīklu nosaukumiem kodā ir jābūt tādiem pašiem kā nosaukumiem darbvietā.</span><span class="sxs-lookup"><span data-stu-id="5ec30-362">The name of the pages and other controls in the code must be the same as the names in the workspace.</span></span>

    ```javascript
    function main(metadataService, dataService, cacheService, $q) {
           return {
               appInit: function (appMetadata) {
                   // Hide controls that need to be present, but not visible
                   metadataService.configureControl('My-vendor-invoices', 'ShowAccept', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowApprove', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowReject', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowDelegate', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowRequestChange', { hidden: true });
                 metadataService.configureControl('My-vendor-invoices', 'ShowRecall', { hidden: true });
                   metadataService.configureControl('My-vendor-invoices', 'ShowComplete', { hidden: true });
               metadataService.configureControl('My-vendor-invoices', 'ShowResubmit', { hidden: true });
                   // Hide pages not applicable for root navigation
                   metadataService.hideNavigation('View-accounting');
                   //Link to view accounting
                   metadataService.addLink('Invoice-details', 'View-accounting', 'View-accounting-nav-control', 'View accounting', true);
               },
               pageInit: function (pageMetadata, params) {
        if (pageMetadata.Name == 'Invoice-details') {
                       // Show/hide workflow actions based on workflow step
                       metadataService.configureAction('Accept', { visible: true });
                       metadataService.configureAction('Approve', { visible: true });
                       metadataService.configureAction('Reject', { visible: true });
                       metadataService.configureAction('Delegate', { visible: true });
                       metadataService.configureAction('Request-change', { visible: true });
                       metadataService.configureAction('Recall', { visible: true });
                       metadataService.configureAction('Complete', { visible: true });
                       metadataService.configureAction('Resubmit', { visible: true });

                       var entityContextParts = params.pageContext.split(':');
                       var data = dataService.getEntityData(entityContextParts[0], entityContextParts[1]);

                       var acceptControl = data.getPropertyValue('VendInvoiceInfoTable/showAccept');
                       var approveControl = data.getPropertyValue('VendInvoiceInfoTable/showApprove');
                       var rejectControl = data.getPropertyValue('VendInvoiceInfoTable/showReject');
                       var delegateControl = data.getPropertyValue('VendInvoiceInfoTable/showDelegate');
                       var requestChangeControl = data.getPropertyValue('VendInvoiceInfoTable/showRequestChange');
                       var recallControl = data.getPropertyValue('VendInvoiceInfoTable/showRecall');
                       var completeControl = data.getPropertyValue('VendInvoiceInfoTable/showComplete');
                       var resubmitControl = data.getPropertyValue('VendInvoiceInfoTable/showResubmit');

                       var showAcceptControl = Boolean(acceptControl == 1);
                       var showApproveControl = Boolean(approveControl == 1);
                     var showRejectControl = Boolean(rejectControl == 1);
                       var showDelegateControl = Boolean(delegateControl == 1);
                       var showRequestChangeControl = Boolean(requestChangeControl == 1);
                       var showRecallControl = Boolean(recallControl == 1);
                       var showCompleteControl = Boolean(completeControl == 1);
                       var showResubmitControl = Boolean(resubmitControl == 1);

                       metadataService.configureAction('Accept', { visible: showAcceptControl });
                       metadataService.configureAction('Approve', { visible: showApproveControl });
                       metadataService.configureAction('Reject', { visible: showRejectControl });
                       metadataService.configureAction('Delegate', { visible: showDelegateControl });
                       metadataService.configureAction('Request-change', { visible: showRequestChangeControl });
                       metadataService.configureAction('Recall', { visible: showRecallControl });
                       metadataService.configureAction('Complete', { visible: showCompleteControl });
                       metadataService.configureAction('Resubmit', { visible: showResubmitControl });
        }
                 },
           };
        }
    ```
    
2.  <span data-ttu-id="5ec30-363">Augšupielādējiet koda failu darbvietā, atlasot cilni **Loģika**, lai pārrakstītu iepriekšējo kodu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-363">Upload the code file to the workspace by selecting the **Logic** tab to overwrite the previous code</span></span>
3.  <span data-ttu-id="5ec30-364">Noklikšķiniet uz **Gatavs**, lai izslēgtu rediģēšanas režīmu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-364">Click **Done** to exit edit mode.</span></span>
4.  <span data-ttu-id="5ec30-365">Noklikšķiniet uz **Atpakaļ** un pēc tam uz **Gatavs**, lai aizvērtu darbvietu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-365">Click **Back** and then **Done** to exit the workspace</span></span>
5.  <span data-ttu-id="5ec30-366">Noklikšķiniet uz **Publicēt darbvietu**, lai saglabātu darbu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-366">Click **Publish workspace** to save your work</span></span>

### <a name="validation"></a><span data-ttu-id="5ec30-367">Validēšana</span><span class="sxs-lookup"><span data-stu-id="5ec30-367">Validation</span></span>

<span data-ttu-id="5ec30-368">Mobilajā ierīcē atveriet programmu un izveidojiet savienojumu ar savu instanci.</span><span class="sxs-lookup"><span data-stu-id="5ec30-368">From your mobile device, open the app, and connect to your instance.</span></span> <span data-ttu-id="5ec30-369">Pārliecinieties, ka pierakstāties uzņēmumā, kurā jums pārskatīšanai ir piešķirti kreditoru rēķini.</span><span class="sxs-lookup"><span data-stu-id="5ec30-369">Make sure that you sign in to the company where vendor invoices are assigned to you for review.</span></span> <span data-ttu-id="5ec30-370">Jums ir jāvar veikt tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="5ec30-370">You should be able to perform the following actions:</span></span>

-   <span data-ttu-id="5ec30-371">Skatīt darbvietu **Mani apstiprinājumi**.</span><span class="sxs-lookup"><span data-stu-id="5ec30-371">See the **My approvals** workspace.</span></span>
-   <span data-ttu-id="5ec30-372">Detalizēti skatīt darbvietu **Mani apstiprinājumi** un skatīt lapu **Mani kreditoru rēķini**.</span><span class="sxs-lookup"><span data-stu-id="5ec30-372">Drill into the **My approvals** workspace and see the **My vendor invoices** page.</span></span>
-   <span data-ttu-id="5ec30-373">Detalizēti skatīt lapu **Mani kreditoru rēķini** un skatīt jums piešķirto rēķinu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-373">Drill into the **My vendor invoices** page and see the list of invoices that are assigned to you.</span></span>
-   <span data-ttu-id="5ec30-374">Detalizēti skatīt vienu no rēķiniem un skatīt rēķina galvenes un rindu detalizētu informāciju.</span><span class="sxs-lookup"><span data-stu-id="5ec30-374">Drill into one of the invoices, and see the invoice header details and line details.</span></span>
-   <span data-ttu-id="5ec30-375">Detalizētas informācijas lapā redzēt pielikumu saiti un to izmantoto, lai navigētu uz pielikumu sarakstu un skatītu pielikumus.</span><span class="sxs-lookup"><span data-stu-id="5ec30-375">On the details page, see a link to attachments, and use this link to navigate to the attachments list and view the attachments.</span></span>
-   <span data-ttu-id="5ec30-376">Detalizētas informācijas lapā redzēt saiti uz lapu **Skatīt uzskaiti** un izmantot šo saiti, lai navigētu uz sadales lapu un skatītu sadales.</span><span class="sxs-lookup"><span data-stu-id="5ec30-376">On the details page, see a link to the **View accounting** page, and use this link to navigate to the distributions page and view the distributions.</span></span>
-   <span data-ttu-id="5ec30-377">Detalizētas informācija lapas apakšdaļā noklikšķināt uz izvēlnes **Darbības** un veikt darbplūsmas darbības, kas attiecas uz konkrēto darbplūsmas soli.</span><span class="sxs-lookup"><span data-stu-id="5ec30-377">On the details page, click the **Actions** menu at the bottom, and perform workflow actions that are applicable to the workflow step.</span></span>

## <a name="designing-a-complex-invoice-approval-scenario-for-fabrikam"></a><span data-ttu-id="5ec30-378">Sarežģīta rēķina apstiprināšanas scenārija izstāde uzņēmumam Fabrikam</span><span class="sxs-lookup"><span data-stu-id="5ec30-378">Designing a complex invoice approval scenario for Fabrikam</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5ec30-379">Scenārija atribūts</span><span class="sxs-lookup"><span data-stu-id="5ec30-379">Scenario attribute</span></span></th>
<th><span data-ttu-id="5ec30-380">Atbilde</span><span class="sxs-lookup"><span data-stu-id="5ec30-380">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5ec30-381">Kurus rēķina galvenes laukus un kādā secībā lietotājs vēlēsies redzēt mobilajā risinājumā?</span><span class="sxs-lookup"><span data-stu-id="5ec30-381">What fields from the invoice header will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="5ec30-382">Kreditora nosaukums</span><span class="sxs-lookup"><span data-stu-id="5ec30-382">Vendor name</span></span></li>
<li><span data-ttu-id="5ec30-383">Rēķina summa</span><span class="sxs-lookup"><span data-stu-id="5ec30-383">Invoice amount</span></span></li>
<li><span data-ttu-id="5ec30-384">Rēķina konts</span><span class="sxs-lookup"><span data-stu-id="5ec30-384">Invoice account</span></span></li>
<li><span data-ttu-id="5ec30-385">Rēķina numurs</span><span class="sxs-lookup"><span data-stu-id="5ec30-385">Invoice number</span></span></li>
<li><span data-ttu-id="5ec30-386">Rēķina datums</span><span class="sxs-lookup"><span data-stu-id="5ec30-386">Invoice date</span></span></li>
<li><span data-ttu-id="5ec30-387">Rēķina apraksts</span><span class="sxs-lookup"><span data-stu-id="5ec30-387">Invoice description</span></span></li>
<li><span data-ttu-id="5ec30-388">Izpildes termiņš</span><span class="sxs-lookup"><span data-stu-id="5ec30-388">Due date</span></span></li>
<li><span data-ttu-id="5ec30-389">Rēķina valūta</span><span class="sxs-lookup"><span data-stu-id="5ec30-389">Invoice currency</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ec30-390">Kurus rēķina rindu laikus un kādā secībā lietotājs vēlēsies redzēt mobilajā risinājumā?</span><span class="sxs-lookup"><span data-stu-id="5ec30-390">What fields from the invoice lines will the user want to see in the mobile experience, and in what order?</span></span></td>
<td><ol>
<li><span data-ttu-id="5ec30-391">Sagādes kategorija</span><span class="sxs-lookup"><span data-stu-id="5ec30-391">Procurement category</span></span></li>
<li><span data-ttu-id="5ec30-392">Daudzums</span><span class="sxs-lookup"><span data-stu-id="5ec30-392">Quantity</span></span></li>
<li><span data-ttu-id="5ec30-393">Vienības cena</span><span class="sxs-lookup"><span data-stu-id="5ec30-393">Unit price</span></span></li>
<li><span data-ttu-id="5ec30-394">Rindas neto summa</span><span class="sxs-lookup"><span data-stu-id="5ec30-394">Line net amount</span></span></li>
<li><span data-ttu-id="5ec30-395">1099. summa</span><span class="sxs-lookup"><span data-stu-id="5ec30-395">1099 amount</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ec30-396">Cik rēķina rindu ir rēķinā?</span><span class="sxs-lookup"><span data-stu-id="5ec30-396">How many invoice lines are there in an invoice?</span></span> <span data-ttu-id="5ec30-397">Lietojiet 80/20 nosacījumu un optimizējiet atbilstoši 80 procentiem.</span><span class="sxs-lookup"><span data-stu-id="5ec30-397">Apply the 80-20 rule here, and optimize for the 80 percent.</span></span></td>
<td><span data-ttu-id="5ec30-398">5.</span><span class="sxs-lookup"><span data-stu-id="5ec30-398">5</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ec30-399">Vai lietotāji vēlas pārskatīšanas laikā mobilajā ierīcē redzēt uzskaites sadales (rēķina kodu).</span><span class="sxs-lookup"><span data-stu-id="5ec30-399">Will users want to see accounting distributions (invoice coding) on the mobile device during reviews?</span></span></td>
<td><span data-ttu-id="5ec30-400">Jā</span><span class="sxs-lookup"><span data-stu-id="5ec30-400">Yes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ec30-401">Cik uzskaites sadales elementu (pilna cena, PVN, izmaksas utt.) ir vienā rēķina rindā?</span><span class="sxs-lookup"><span data-stu-id="5ec30-401">How many accounting distributions (extended price, sales tax, charges, and so on) are there for an invoice line?</span></span> <span data-ttu-id="5ec30-402">Atkal lietojiet 80/20 nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="5ec30-402">Again, apply the 80-20 rule.</span></span></td>
<td><span data-ttu-id="5ec30-403">Pilna cena: 2, PVN: 2, izmaksas: 2</span><span class="sxs-lookup"><span data-stu-id="5ec30-403">Extended price: 2 Sales tax: 2 Charges: 2</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ec30-404">Vai rēķina galvenē arī ir uzskaites sadales?</span><span class="sxs-lookup"><span data-stu-id="5ec30-404">Do the invoices also have accounting distributions on the invoice header?</span></span> <span data-ttu-id="5ec30-405">Jā tā ir, vai šīm uzskaites sadalēm ir jābūt pieejamām ierīcē?</span><span class="sxs-lookup"><span data-stu-id="5ec30-405">If so, should these accounting distributions be available on the device?</span></span></td>
<td><span data-ttu-id="5ec30-406">Netiek lietots</span><span class="sxs-lookup"><span data-stu-id="5ec30-406">Not used</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ec30-407">Vai lietotāji vēlēsies ierīcē redzēt rēķina pielikumus?</span><span class="sxs-lookup"><span data-stu-id="5ec30-407">Will users want to see attachments for the invoice on the device?</span></span></td>
<td><span data-ttu-id="5ec30-408">Jā</span><span class="sxs-lookup"><span data-stu-id="5ec30-408">Yes</span></span></td>
</tr>
</tbody>
</table>

### <a name="next-steps"></a><span data-ttu-id="5ec30-409">Turpmākās darbības</span><span class="sxs-lookup"><span data-stu-id="5ec30-409">Next steps</span></span>

<span data-ttu-id="5ec30-410">Pamatojoties uz 2. scenārija prasībām, var izstrādāt tālāk norādītos 1. scenārija variantus.</span><span class="sxs-lookup"><span data-stu-id="5ec30-410">The following variations can be done for scenario 1, based on the requirements for scenario 2.</span></span> <span data-ttu-id="5ec30-411">Šo sadaļu varat izmantot, lai uzlabotu savas mobilās programmas funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="5ec30-411">You can use this section to improve your mobile app experience.</span></span>

1.  <span data-ttu-id="5ec30-412">Tā kā 2. scenārija ietvaros ir paredzēts apstrādāt vairāk rēķina rindu, tālāk norādītās izstrādes izmaiņas palīdzēs optimizēt lietotāja iespējas mobilajā ierīcē.</span><span class="sxs-lookup"><span data-stu-id="5ec30-412">Because more invoice lines are expected in scenario 2, the following changes to the design will help optimize the user experience on the mobile device:</span></span>
    1.  <span data-ttu-id="5ec30-413">Tā vieta, lai skatītu rēķina rindas detalizētas informācijas lapā (kā 1. scenārijā), lietotāji var izvelēties skatīt rindas atsevišķā mobilajā lapā.</span><span class="sxs-lookup"><span data-stu-id="5ec30-413">Instead of viewing invoice lines on the details page (as in scenario 1), users can choose to view lines on a separate mobile page.</span></span>
    2.  <span data-ttu-id="5ec30-414">Tā kā šī scenārija ietvaros ir paredzēts apstrādāt vairākas rēķina rindas, ja mobilās sadales lapas izstrādei tiek izmantota lapa **VendMobileInvoiceAllDistributionTree** (kā 1. scenārijā), lietotājam var būt grūti saistīt rindas ar sadalēm.</span><span class="sxs-lookup"><span data-stu-id="5ec30-414">Because more than one invoice line is expected in this scenario, if the **VendMobileInvoiceAllDistributionTree** page is used to design the distributions page for mobile (as in scenario 1), it might be confusing for the user to correlate lines to distributions.</span></span> <span data-ttu-id="5ec30-415">Tāpēc sadales lapas izstrādei izmantojiet lapu **VendMobileInvoiceLineDistributionTree**.</span><span class="sxs-lookup"><span data-stu-id="5ec30-415">Therefore, use the **VendMobileInvoiceLineDistributionTree** page to design the distributions page.</span></span>
    3.  <span data-ttu-id="5ec30-416">Ideālā gadījumā šī scenārija ietvaros sadales ir jārāda rēķina rindas kontekstā.</span><span class="sxs-lookup"><span data-stu-id="5ec30-416">Ideally, the distributions should be shown in the context of an invoice line in this scenario.</span></span> <span data-ttu-id="5ec30-417">Tāpēc nodrošiniet, lai lietotājs varētu detalizēti skatīt rindas informāciju, tādējādi piekļūstot sadales lapai.</span><span class="sxs-lookup"><span data-stu-id="5ec30-417">Therefore, make sure that the user can drill into a line to see the distributions page.</span></span> <span data-ttu-id="5ec30-418">Izmantojiet lapas saites iespēju, lai nodrošinātu detalizēto apskati, tāpat kā to darījāt galvenes lapai un detalizētās informācijas lapai 1. scenārija ietvaros.</span><span class="sxs-lookup"><span data-stu-id="5ec30-418">Use the page link capability to establish the drill-through, just as you did for the header and details pages in scenario 1.</span></span>

2.  <span data-ttu-id="5ec30-419">Tā kā 2. scenārija ietvaros ir paredzēts apstrādāt vairākus summas veidus (PVN, izmaksas utt.), ir noderīgi rādīt summas veida sadali.</span><span class="sxs-lookup"><span data-stu-id="5ec30-419">Because more than one amount type is expected on the distributions in scenario 2 (sales tax, charges, and so on), it will be useful to show the description of the amount type.</span></span> <span data-ttu-id="5ec30-420">(Šī informācija tika atmesta 1. scenārija ietvaros.)</span><span class="sxs-lookup"><span data-stu-id="5ec30-420">(We omitted this information in scenario 1.)</span></span>




