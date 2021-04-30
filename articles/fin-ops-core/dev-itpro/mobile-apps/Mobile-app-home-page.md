---
title: Mobilās programmas mājas lapa
description: Šajā tēmā ir aprakstīta Finance and Operations (Dynamics 365) mobilā programma un ir sniegtas saites uz resursiem, kas var palīdzēt to ieviest organizācijā.
author: ChrisGarty
ms.date: 01/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: cgarty
ms.dyn365.ops.version: Platform update 4
ms.search.validFrom: 2017-02-28
ms.openlocfilehash: 9707a1f8a90a615dbc8f34f4bb1f05d34d8fe7f3
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908236"
---
# <a name="mobile-app-home-page"></a><span data-ttu-id="60d81-103">Mobilās programmas mājas lapa</span><span class="sxs-lookup"><span data-stu-id="60d81-103">Mobile app home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="60d81-104">Šajā tēmā ir aprakstīta **Finance and Operations (Dynamics 365)** mobilā programma un ir sniegtas saites uz resursiem, kas var palīdzēt to ieviest organizācijā.</span><span class="sxs-lookup"><span data-stu-id="60d81-104">This topic describes the **Finance and Operations (Dynamics 365)** mobile app and provides links to resources that can help you implement it in your organization.</span></span>

<a name="overview"></a><span data-ttu-id="60d81-105">Kopsavilkums</span><span class="sxs-lookup"><span data-stu-id="60d81-105">Overview</span></span>
--------

<span data-ttu-id="60d81-106">Šī mobilā programma jūsu organizācijai sniedz iespējas savus uzņēmējdarbības procesus padarīt pieejamus mobilajās ierīcēs.</span><span class="sxs-lookup"><span data-stu-id="60d81-106">The mobile app enables your organization to make its business processes available on mobile devices.</span></span> <span data-ttu-id="60d81-107">Kad IT administrators jūsu organizācijai ir iespējojis mobilās darbvietas, lietotāji var pierakstīties programmā un nekavējoties sākt biznesa procesu izpildi no savām mobilajām ierīcēm.</span><span class="sxs-lookup"><span data-stu-id="60d81-107">After your IT admin enables the mobile workspaces for your organization, users can sign in to the app and immediately begin to run business processes from their mobile devices.</span></span> <span data-ttu-id="60d81-108">Šī mobilā programma ietver tālāk norādītos līdzekļus, kas var palīdzēt uzlabot produktivitāti.</span><span class="sxs-lookup"><span data-stu-id="60d81-108">The mobile app includes the following features that can help increase productivity:</span></span>

- <span data-ttu-id="60d81-109">Lietotāji var skatīt biznesa datus, tos rediģēt un rīkoties ar šiem datiem, pat ja šo lietotāju tīkla savienojamība darbojas ar pārtraukumiem vai ja viņu mobilās ierīces ir pilnīgi bezsaistē.</span><span class="sxs-lookup"><span data-stu-id="60d81-109">Users can view, edit, and act on business data, even if they have intermittent network connectivity or their mobile devices are completely offline.</span></span> <span data-ttu-id="60d81-110">Kad ierīce no jauna izveido savienojumu ar tīklu, bezsaistes datu operācijas tiek automātiski sinhronizētas.</span><span class="sxs-lookup"><span data-stu-id="60d81-110">When a device reestablishes a network connection, offline data operations are automatically synchronized.</span></span>
- <span data-ttu-id="60d81-111">IT administratori vai izstrādātāji var veidot un publicēt mobilās darbvietas, kas ir īpaši izstrādātas viņu organizācijai.</span><span class="sxs-lookup"><span data-stu-id="60d81-111">IT admins or developers can build and publish mobile workspaces that have been tailored to their organization.</span></span> <span data-ttu-id="60d81-112">Šī programmu izmanto jūsu jau esošos koda līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="60d81-112">The app uses your existing code assets.</span></span> <span data-ttu-id="60d81-113">Tāpēc jums nav nepieciešamības atkārtoti ieviest savas validēšanas procedūras, biznesa loģiku vai drošības konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="60d81-113">Therefore, you don't have to re-implement your validation procedures, business logic, or security configuration.</span></span>
- <span data-ttu-id="60d81-114">IT administratori vai izstrādātāji mobilās darbvietas var ērti projektēt, izmantojot norādīšanas un klikšķināšanas darbvietas veidotāju, kas ir iekļauts tīmekļa klientā.</span><span class="sxs-lookup"><span data-stu-id="60d81-114">IT admins or developers can easily design mobile workspaces by using the point-and-click workspace designer that is included with the web client.</span></span>
- <span data-ttu-id="60d81-115">IT administratori vai izstrādātāji pēc izvēles varat optimizēt darbvietas bezsaistes iespējas, izmantojot biznesa loģikas paplašināšanas struktūru.</span><span class="sxs-lookup"><span data-stu-id="60d81-115">IT admins or developers can optionally optimize the offline capabilities of workspaces by using the Business logic extensibility framework.</span></span> <span data-ttu-id="60d81-116">Tā kā datu apstrāde turpinās arī laikā, kamēr ierīce ir bezsaistē, jūsu mobilie scenāriji joprojām ir bagātīgi un plūstoši, pat ja ierīcēm nav pastāvīga savienojuma ar tīklu.</span><span class="sxs-lookup"><span data-stu-id="60d81-116">Because data continues to be processed while a device is offline, your mobile scenarios remain rich and fluid, even if devices don't have constant network connectivity.</span></span>

## <a name="elements-of-the-mobile-app"></a><span data-ttu-id="60d81-117">Mobilās programmas elementi</span><span class="sxs-lookup"><span data-stu-id="60d81-117">Elements of the mobile app</span></span>
<span data-ttu-id="60d81-118">Navigāciju mobilajā programmā veido četri galvenie jēdzieni: informācijas panelis, darbvietas, lapas un darbības.</span><span class="sxs-lookup"><span data-stu-id="60d81-118">Navigation in the mobile app consists of four basic concepts: the dashboard, workspaces, pages, and actions.</span></span> 

<span data-ttu-id="60d81-119">[![Navigācijas jēdzieni mobilajā programmā](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span><span class="sxs-lookup"><span data-stu-id="60d81-119">[![Navigation concepts in the mobile app](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span></span>

1. <span data-ttu-id="60d81-120">Kad programmu startējat, jūs dodieties uz **informācijas paneli**.</span><span class="sxs-lookup"><span data-stu-id="60d81-120">When you start the app, you go to the **dashboard**.</span></span>
2. <span data-ttu-id="60d81-121">Informācijas panelī varat redzēt sarakstu ar **darbvietām**, kuras ir publicētas.</span><span class="sxs-lookup"><span data-stu-id="60d81-121">On the dashboard, you can see a list of **workspaces** that have been published.</span></span>
3. <span data-ttu-id="60d81-122">Katrā darbvietā ir redzams saraksts ar **lapām**, kas ir pieejamas attiecīgajai darbvietai.</span><span class="sxs-lookup"><span data-stu-id="60d81-122">In each workspace, you can see a list of **pages** that are available for that workspace.</span></span>
4. <span data-ttu-id="60d81-123">Pēc lapas atvēršanas varat veikt vairākas darbības.</span><span class="sxs-lookup"><span data-stu-id="60d81-123">After you're on a page, you can perform several actions.</span></span> <span data-ttu-id="60d81-124">Daži piemēri:</span><span class="sxs-lookup"><span data-stu-id="60d81-124">Here are some examples:</span></span>

    - <span data-ttu-id="60d81-125">Skatīt detalizētus datus.</span><span class="sxs-lookup"><span data-stu-id="60d81-125">View detailed data.</span></span>
    - <span data-ttu-id="60d81-126">Pāriet uz citām lapām ar saistītiem datiem, piemēram, ar detalizētu informāciju par elementu vai rindām.</span><span class="sxs-lookup"><span data-stu-id="60d81-126">Navigate to other pages for related data, such as entity details or lines.</span></span>
    - <span data-ttu-id="60d81-127">Skatīt sarakstu ar **darbībām**, kas ir pieejamas šai lapai.</span><span class="sxs-lookup"><span data-stu-id="60d81-127">See a list of **actions** that are available for that page.</span></span> <span data-ttu-id="60d81-128">Darbības jums ļauj izveidot vai rediģēt esošus datus.</span><span class="sxs-lookup"><span data-stu-id="60d81-128">Actions let you create or edit existing data.</span></span>

## <a name="implementation-process"></a><span data-ttu-id="60d81-129">Ieviešanas process</span><span class="sxs-lookup"><span data-stu-id="60d81-129">Implementation process</span></span>
<span data-ttu-id="60d81-130">Nākamajā attēlā ir parādīts ieviešanas process gan mobilajām darbvietām, ko nodrošina Microsoft, gan pielāgotajām mobilajām darbvietām.</span><span class="sxs-lookup"><span data-stu-id="60d81-130">The following illustration shows the process for implementing both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> 

<span data-ttu-id="60d81-131">[![Mobilo programmu ieviešanas process](./media/Mobile-implementation-process-5.png)](./media/Mobile-implementation-process-5.png)</span><span class="sxs-lookup"><span data-stu-id="60d81-131">[![Mobile apps implementation process](./media/Mobile-implementation-process-5.png)](./media/Mobile-implementation-process-5.png)</span></span>

<span data-ttu-id="60d81-132">Nākamajā tabulā ir ietvertas saites uz resursiem, kas jums var palīdzēt ieviest gan mobilās darbvietas, ko nodrošina Microsoft, gan pielāgotās mobilās darbvietas.</span><span class="sxs-lookup"><span data-stu-id="60d81-132">The following table includes links to resources that can help you implement both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> <span data-ttu-id="60d81-133">Numuri pirmajā kolonnā atbilst iepriekšējā attēlā uzskaitītajiem soļiem.</span><span class="sxs-lookup"><span data-stu-id="60d81-133">The numbers in the first column correspond to the numbered steps in the previous illustration.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="60d81-134">Solis</span><span class="sxs-lookup"><span data-stu-id="60d81-134">Step</span></span></th>
<th><span data-ttu-id="60d81-135">Loma</span><span class="sxs-lookup"><span data-stu-id="60d81-135">Role</span></span></th>
<th><span data-ttu-id="60d81-136">Darbība</span><span class="sxs-lookup"><span data-stu-id="60d81-136">Action</span></span></th>
<th><span data-ttu-id="60d81-137">Resurss, kas jums palīdz izpildīt šo darbību</span><span class="sxs-lookup"><span data-stu-id="60d81-137">Resources to help you complete the action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="60d81-138">1.</span><span class="sxs-lookup"><span data-stu-id="60d81-138">1</span></span></td>
<td><span data-ttu-id="60d81-139">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="60d81-139">System administrator</span></span></td>
<td><span data-ttu-id="60d81-140">Īstenojiet Finance and Operations programmu savā organizācijā.</span><span class="sxs-lookup"><span data-stu-id="60d81-140">Implement the Finance and Operations app in your organization.</span></span></td>
<td><ul><li><span data-ttu-id="60d81-141">Ja vēl neesa&#39;t izvietojis Microsoft Dynamics 365 versiju, skatiet rakstu <a href="../deployment/deploy-demo-environment.md">Demonstrācijas vides izvietošana</a>.</span><span class="sxs-lookup"><span data-stu-id="60d81-141">If you haven&#39;t yet deployed a version of Microsoft Dynamics 365, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span></li><li><span data-ttu-id="60d81-142">Lai apskatītu sarakstu ar mobilajām darbvietām, ko var izmantot, skatiet rakstu <a href="mobile-workspaces-released.md">Nesen izlaistās mobilās darbvietas</a>.</span><span class="sxs-lookup"><span data-stu-id="60d81-142">To see a list of mobile workspaces that can be used, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span></li></ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="60d81-143">2</span><span class="sxs-lookup"><span data-stu-id="60d81-143">2</span></span></td>
<td><span data-ttu-id="60d81-144">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="60d81-144">System administrator</span></span></td>
<td><span data-ttu-id="60d81-145"><strong>Ja l&#39;ietojat Microsoft Dynamics 365 for Operations versiju 1611:</strong> lejupielādējiet un instalējiet KB, kas iespējo Microsoft nodrošinātās mobilās darbvietas.</span><span class="sxs-lookup"><span data-stu-id="60d81-145"><strong>If you&#39;re using Microsoft Dynamics 365 for Operations version 1611:</strong> Download and install KBs that enable the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="60d81-146">Papildinformāciju skatiet tālāk norādītajās tēmās.</span><span class="sxs-lookup"><span data-stu-id="60d81-146">See the following topics for more information:</span></span>
<ul>

<li><span data-ttu-id="60d81-147"><a href="../../../finance/cost-accounting/cost-controlling-mobile-workspace.md">Izmaksu kontrolēšanas mobilās darbvietas</a></span><span class="sxs-lookup"><span data-stu-id="60d81-147"><a href="../../../finance/cost-accounting/cost-controlling-mobile-workspace.md">Cost controlling mobile workspaces</a></span></span></li>
<li><span data-ttu-id="60d81-148"><a href="../../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Rīcībā esošo krājumu mobilā darbvieta</a></span><span class="sxs-lookup"><span data-stu-id="60d81-148"><a href="../../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Inventory on-hand mobile workspace</a></span></span></li>
<li><span data-ttu-id="60d81-149"><a href="../../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Pārdošanas pasūtījumu mobilās darbvietas</a></span><span class="sxs-lookup"><span data-stu-id="60d81-149"><a href="../../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Sales orders mobile workspaces</a></span></span></li>
<li><span data-ttu-id="60d81-150"><a href="../../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Kreditoru sadarbības mobilā darbvieta</a></span><span class="sxs-lookup"><span data-stu-id="60d81-150"><a href="../../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Vendor collaboration mobile workspace</a></span></span></li>
<li><span data-ttu-id="60d81-151"><a href="/dynamics365/project-operations/prod-pma/project-time-entry-mobile-workspace">Projekta laika ieraksta mobilajām ierīcēm paredzēta darbvieta</a></span><span class="sxs-lookup"><span data-stu-id="60d81-151"><a href="/dynamics365/project-operations/prod-pma/project-time-entry-mobile-workspace">Project time entry mobile workspace</a></span></span></li>
<li><span data-ttu-id="60d81-152"><a href="/dynamics365/project-operations/prod-exp/expense-management-mobile-workspace">Izmaksu pārvaldības mobilā darbvieta</a></span><span class="sxs-lookup"><span data-stu-id="60d81-152"><a href="/dynamics365/project-operations/prod-exp/expense-management-mobile-workspace">Expense management mobile workspace</a></span></span></li>

</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="60d81-153">3.</span><span class="sxs-lookup"><span data-stu-id="60d81-153">3</span></span></td>
<td><span data-ttu-id="60d81-154">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="60d81-154">System administrator</span></span></td>
<td><span data-ttu-id="60d81-155">Publicējiet Microsoft nodrošinātās mobilās darbvietas.</span><span class="sxs-lookup"><span data-stu-id="60d81-155">Publish the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="60d81-156"><a href="publish-mobile-workspace.md">Mobilās darbvietas publicēšana</a>
</span><span class="sxs-lookup"><span data-stu-id="60d81-156"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a>
</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="60d81-157">4.</span><span class="sxs-lookup"><span data-stu-id="60d81-157">4</span></span></td>
<td><span data-ttu-id="60d81-158">Izstrādātājs vai neatkarīgs programmatūras izstrādātājs (independent software vendor — ISV)</span><span class="sxs-lookup"><span data-stu-id="60d81-158">Developer or independent software vendor (ISV)</span></span></td>
<td><span data-ttu-id="60d81-159">Izmantojiet mobilo platformu, lai izveidotu pielāgotas mobilās darbvietas.</span><span class="sxs-lookup"><span data-stu-id="60d81-159">Use the mobile platform to create custom mobile workspaces.</span></span></td>
<td><span data-ttu-id="60d81-160"><a href="platform/mobile-platform-home-page.md">Mobilā platforma</a></span><span class="sxs-lookup"><span data-stu-id="60d81-160"><a href="platform/mobile-platform-home-page.md">Mobile platform</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="60d81-161">5.</span><span class="sxs-lookup"><span data-stu-id="60d81-161">5</span></span></td>
<td><span data-ttu-id="60d81-162">NPI</span><span class="sxs-lookup"><span data-stu-id="60d81-162">ISV</span></span></td>
<td><span data-ttu-id="60d81-163">Izveidojiet izvietojamu pakotni, kurā ir ietvertas pielāgotas mobilās darbvietas, un augšupielādējiet šo pakotni portālā Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="60d81-163">Create a deployable package that contains custom mobile workspaces, and upload the package to Microsoft Dynamics Lifecycle Services (LCS).</span></span></td>
<td><span data-ttu-id="60d81-164"><a href="../deployment/create-apply-deployable-package.md">Izvietojamas pakotnes izveide</a></span><span class="sxs-lookup"><span data-stu-id="60d81-164"><a href="../deployment/create-apply-deployable-package.md">Create a deployable package</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="60d81-165">6.</span><span class="sxs-lookup"><span data-stu-id="60d81-165">6</span></span></td>
<td><span data-ttu-id="60d81-166">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="60d81-166">System administrator</span></span></td>
<td><span data-ttu-id="60d81-167">Lietojiet izvietojamo pakotni, kas ietver neatkarīgu programmatūras izstrādātāju (independent software vendor — ISV) nodrošinātās pielāgotās darbvietas.</span><span class="sxs-lookup"><span data-stu-id="60d81-167">Apply the deployable package that contains the custom workspaces that are provided by the independent software vendor (ISV).</span></span></td>
<td><span data-ttu-id="60d81-168"><a href="../deployment/apply-deployable-package-system.md">Lietot izvietojamu pakotni</a></span><span class="sxs-lookup"><span data-stu-id="60d81-168"><a href="../deployment/apply-deployable-package-system.md">Apply a deployable package</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="60d81-169">7.</span><span class="sxs-lookup"><span data-stu-id="60d81-169">7</span></span></td>
<td><span data-ttu-id="60d81-170">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="60d81-170">System administrator</span></span></td>
<td><span data-ttu-id="60d81-171">Publicējiet pielāgotās mobilās darbvietas, ko nodrošina ISV.</span><span class="sxs-lookup"><span data-stu-id="60d81-171">Publish the custom mobile workspaces that are provided by the ISV.</span></span></td>
<td><span data-ttu-id="60d81-172"><a href="publish-mobile-workspace.md">Mobilās darbvietas publicēšana</a></span><span class="sxs-lookup"><span data-stu-id="60d81-172"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="60d81-173">8</span><span class="sxs-lookup"><span data-stu-id="60d81-173">8</span></span></td>
<td><span data-ttu-id="60d81-174">Lietotājs</span><span class="sxs-lookup"><span data-stu-id="60d81-174">User</span></span></td>
<td><span data-ttu-id="60d81-175">Lejupielādējiet un instalējiet mobilo programmu.</span><span class="sxs-lookup"><span data-stu-id="60d81-175">Download and install the mobile app.</span></span></td>
<td><span data-ttu-id="60d81-176">
<a href="https://go.microsoft.com/fwlink/?linkid=850662">Finance and Operations programma programmatūrai Android</a></span><span class="sxs-lookup"><span data-stu-id="60d81-176">
<a href="https://go.microsoft.com/fwlink/?linkid=850662">Finance and Operations app for Android</a></span></span><BR/><span data-ttu-id="60d81-177">
<a href="https://go.microsoft.com/fwlink/?linkid=850663">Finance and Operations programma programmatūrai iOS</a></span><span class="sxs-lookup"><span data-stu-id="60d81-177">
<a href="https://go.microsoft.com/fwlink/?linkid=850663">Finance and Operations app for iOS</a></span></span><BR/>
<span data-ttu-id="60d81-178">(Windows Phone ierīces netiek atbalstītas)</span><span class="sxs-lookup"><span data-stu-id="60d81-178">(Windows Phone unsupported)</span></span>
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="60d81-179">9</span><span class="sxs-lookup"><span data-stu-id="60d81-179">9</span></span></td>
<td><span data-ttu-id="60d81-180">Lietotājs</span><span class="sxs-lookup"><span data-stu-id="60d81-180">User</span></span></td>
<td><span data-ttu-id="60d81-181">Pierakstieties mobilajā programmā un lietojiet to.</span><span class="sxs-lookup"><span data-stu-id="60d81-181">Sign in, and use the mobile app.</span></span> <span data-ttu-id="60d81-182">Programma ietver mobilās darbvietas, kuras ir publicējis sistēmas administrators.</span><span class="sxs-lookup"><span data-stu-id="60d81-182">The app includes the mobile workspaces that have been published by the system administrator.</span></span></td>
<td><span data-ttu-id="60d81-183">Lai apskatītu sarakstu ar mobilajām darbvietām, ko nodrošina korporācija Microsoft, skatiet rakstu <a href="mobile-workspaces-released.md">Nesen izlaistās mobilās darbvietas</a>.</span><span class="sxs-lookup"><span data-stu-id="60d81-183">To see a list of mobile workspaces that are provided by Microsoft, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span>
</td>
</tr>
</tbody>
</table>

## <a name="troubleshooting"></a><span data-ttu-id="60d81-184">Problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="60d81-184">Troubleshooting</span></span>
[<span data-ttu-id="60d81-185">Mobilās platformas resursi</span><span class="sxs-lookup"><span data-stu-id="60d81-185">Mobile platform resources</span></span>](platform/mobile-platform-home-page.md#troubleshooting-the-app)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]