---
title: Mobilās ierīces izvēlnes vienumu iestatīšana, lai nodrošinātu izdošanas rindas pārskatu
description: Šajā tēmā ir paskaidrots, kā definēt visu darba rindu sarakstu, kas tiks parādīts noliktavas darbiniekiem, kuri apstrādā noliktavas darbu mobilajā ierīcē. Šī iespēja var būt noderīga noliktavas darbiniekiem, kuriem bieži ir nepieciešams pārskats par izdošanas rindām darba pasūtījumā, lai varētu optimizēt izdošanas secību.
author: MarkusFogelberg
manager: tfehr
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 3a2c8a69a2c64214a38a654042ea2f62575e7f52
ms.sourcegitcommit: a52a789044ca66c6771224a6cf0be8749bc99e5a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/23/2020
ms.locfileid: "3837316"
---
# <a name="set-up-a-mobile-device-menu-item-to-provide-a-pick-line-overview"></a><span data-ttu-id="c324a-104">Mobilās ierīces izvēlnes vienumu iestatīšana, lai nodrošinātu izdošanas rindas pārskatu</span><span class="sxs-lookup"><span data-stu-id="c324a-104">Set up a mobile device menu item to provide a pick line overview</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="c324a-105">Šajā tēmā ir paskaidrots, kā konfigurēt opcijas, kas saistītas ar izdošanas rindas pārskatu mobilās ierīces izvēlnes vienumiem, kas tiek izmantoti, lai apstrādātu izdošanas darbu.</span><span class="sxs-lookup"><span data-stu-id="c324a-105">This topic explains how to configure options that are related to the pick line overview for mobile device menu items that are used to process picking work.</span></span> <span data-ttu-id="c324a-106">Izdošanas rindas pārskats ļauj noliktavas darbiniekiem skatīt un atlasīt no saraksta visas darba rindas, kas saistītas ar viņu pašreizējo uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="c324a-106">The pick line overview lets warehouse workers view and select from a list of all the work lines that are related to their current task.</span></span> <span data-ttu-id="c324a-107">Šī iespēja palīdz darbiniekiem optimizēt izdošanas secību.</span><span class="sxs-lookup"><span data-stu-id="c324a-107">This capability can help workers optimize their picking sequence.</span></span> <span data-ttu-id="c324a-108">Līdzeklis nodrošina opcijas, kas aizvieto standarta **Izlaist** pogu, ļaujot darbiniekiem pārlūkot rindas pa vienai, fiksētā secībā.</span><span class="sxs-lookup"><span data-stu-id="c324a-108">The feature provides options that replace the standard **Skip** button that lets workers cycle through the lines one at a time, in a fixed order.</span></span> <span data-ttu-id="c324a-109">(Tomēr pogas izmantošanas opcija joprojām ir pieejama.)</span><span class="sxs-lookup"><span data-stu-id="c324a-109">(However, the option to use that button is still available.)</span></span>

<span data-ttu-id="c324a-110">Administratori var konfigurēt katru izvēlnes vienumu atsevišķi, lai kontrolētu, kā, kad un kur noliktavas programma parāda izdošanas rindas pārskatu.</span><span class="sxs-lookup"><span data-stu-id="c324a-110">Admins can configure each menu item individually to control how, when, and where the warehouse app presents the pick line overview.</span></span>

## <a name="turn-on-the-work-pick-line-overview-feature"></a><span data-ttu-id="c324a-111">Darba izdošanas rindas pārskata līdzekļa ieslēgšana</span><span class="sxs-lookup"><span data-stu-id="c324a-111">Turn on the Work pick line overview feature</span></span>

<span data-ttu-id="c324a-112">Lai varētu izmantot šo līdzekli, tas vispirms ir jāiespējo jūsu sistēmā.</span><span class="sxs-lookup"><span data-stu-id="c324a-112">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="c324a-113">Administratori var izmantot [funkciju pārvaldības](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) iestatījumus, lai pārbaudītu līdzekļa statusu un to ieslēgtu, ja nepieciešams.</span><span class="sxs-lookup"><span data-stu-id="c324a-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="c324a-114">Darbvietā **Līdzekļu pārvaldība** šis līdzeklis ir uzskaitīts šādi:</span><span class="sxs-lookup"><span data-stu-id="c324a-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="c324a-115">**Modulis:** _Noliktavas vadība_</span><span class="sxs-lookup"><span data-stu-id="c324a-115">**Module:** _Warehouse management_</span></span>
- <span data-ttu-id="c324a-116">**Līdzekļa nosaukums:** _Darba izdošanas rindas pārskats_</span><span class="sxs-lookup"><span data-stu-id="c324a-116">**Feature name:** _Work pick line overview_</span></span>

## <a name="configure-menu-items-to-show-a-list-of-all-work-lines"></a><span data-ttu-id="c324a-117">Izvēlnes vienumu konfigurēšana, lai parādītu sarakstu ar visām darba rindām</span><span class="sxs-lookup"><span data-stu-id="c324a-117">Configure menu items to show a list of all work lines</span></span>

<span data-ttu-id="c324a-118">Lai iestatītu mobilās ierīces izvēlnes vienumu, kas nodrošinātu izdošanas rindas pārskatu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="c324a-118">To set up a mobile device menu item to provide a pick line overview, follow these steps.</span></span>

1. <span data-ttu-id="c324a-119">Dodieties uz **Noliktavas pārvaldība \> Iestatījumi \> Mobilā ierīce \> Mobilās ierīces izvēlnes vienumi**.</span><span class="sxs-lookup"><span data-stu-id="c324a-119">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="c324a-120">Atlasiet vai izveidojiet izvēlnes vienumu, kas ir saistīts ar izdošanas darbu, un iestatiet šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="c324a-120">Select or create a menu item that is related to picking work, and set the following values:</span></span>

    - <span data-ttu-id="c324a-121">**Režīms:** *Darbs*</span><span class="sxs-lookup"><span data-stu-id="c324a-121">**Mode:** *Work*</span></span>
    - <span data-ttu-id="c324a-122">**Izmantot esošo darbu:** *Jā*</span><span class="sxs-lookup"><span data-stu-id="c324a-122">**Use existing work:** *Yes*</span></span>
    - <span data-ttu-id="c324a-123">**Noteicējs:** *Lietotāja noteikts* vai *Sistēmas noteikts*</span><span class="sxs-lookup"><span data-stu-id="c324a-123">**Directed by:** *User directed* or *System directed*</span></span>

    <span data-ttu-id="c324a-124">Papildinformāciju par izvēlnes vienumu izveidi un izmantojumu dažādos iestatījumos, kas ir pieejami **mobilās ierīces izvēlnes vienumu** lapā, skatiet sadaļā [mobilo ierīču iestatīšana darbam noliktavā](configure-mobile-devices-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="c324a-124">For more information about how to create menu items and use the various settings that are available on the **Mobile device menu items** page, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>

1. <span data-ttu-id="c324a-125">Kopsavilkuma cilnē **Vispārīgi** konfigurējiet līdzekli, iestatot lauku **Rādīt darba rindu sarakstu** uz vienu no šīm vērtībām:</span><span class="sxs-lookup"><span data-stu-id="c324a-125">On the **General** FastTab, configure the feature by setting the **Show work line list** field to one of the following values:</span></span>

    - <span data-ttu-id="c324a-126">**Rādīt tikai pēc pieprasījuma** – darbinieki var izvēlēties skatīt izdošanas rindu sarakstu, noliktavas programmā atlasot pogu **Pāriet uz**.</span><span class="sxs-lookup"><span data-stu-id="c324a-126">**Show only upon request** – Workers can choose to view the pick line list by selecting the **Skip to** button in the warehouse app.</span></span>
    - <span data-ttu-id="c324a-127">**Rādīt katras izdošanas sākumā** – darbinieki redz sarakstu katru reizi, kad tiek sākta vai pabeigta izdošanas rinda.</span><span class="sxs-lookup"><span data-stu-id="c324a-127">**Show at the start of every pick** – Workers see the list every time that they start or finish a pick line.</span></span> <span data-ttu-id="c324a-128">Viņi var skatīt sarakstu arī atkārtoti, noliktavas programmā atlasot pogu **Pāriet uz**.</span><span class="sxs-lookup"><span data-stu-id="c324a-128">They can also view the list again by selecting the **Skip to** button in the warehouse app.</span></span>
    - <span data-ttu-id="c324a-129">**Rādīt tikai pirmās izdošanas sākumā** – darbinieki redz sarakstu katru reizi, kad tiek sākts jauns izdošanas darbs, bet ne pēc katras rindas.</span><span class="sxs-lookup"><span data-stu-id="c324a-129">**Show at the start of the first pick only** – Workers see the list every time that they start new picking work, but not after each line.</span></span> <span data-ttu-id="c324a-130">Viņi var skatīt sarakstu arī atkārtoti, noliktavas programmā atlasot pogu **Pāriet uz**.</span><span class="sxs-lookup"><span data-stu-id="c324a-130">They can also view the list again by selecting the **Skip to** button in the warehouse app.</span></span>
    - <span data-ttu-id="c324a-131">**Nekad nerādīt** – noliktavas programmā tiek parādīta standarta poga **Izlaist** un tiek izslēgts darba rindu saraksta rādījums.</span><span class="sxs-lookup"><span data-stu-id="c324a-131">**Never show** – The standard **Skip** button appears in the warehouse app, and display of the work line list is turned off.</span></span> <span data-ttu-id="c324a-132">Poga **Izlaist** ļauj darbiniekiem pārlūkot rindas pa vienai, fiksētā secībā.</span><span class="sxs-lookup"><span data-stu-id="c324a-132">The **Skip** button lets workers cycle through the lines one at a time, in a fixed order.</span></span> <span data-ttu-id="c324a-133">Viņi var arī pārlūkot sarakstu tik daudz reižu, cik nepieciešams, līdz visas rindas ir apstrādātas.</span><span class="sxs-lookup"><span data-stu-id="c324a-133">They can also cycle through the list as many times as they require, until all lines have been processed.</span></span>

1. <span data-ttu-id="c324a-134">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="c324a-134">On the Action Pane, select **Save**.</span></span>

    <span data-ttu-id="c324a-135">Ja lauku **Rādīt darba rindu sarakstu** iestatāt uz jebkādu vērtību, izņemot *Nekad nerādīt*, tad darbību rūts poga **Lauku saraksts** kļūst pieejama.</span><span class="sxs-lookup"><span data-stu-id="c324a-135">If you set the **Show work line list** field to any value except *Never show*, the **Field list** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="c324a-136">Darbību rūtī atlasiet **Lauku saraksts**.</span><span class="sxs-lookup"><span data-stu-id="c324a-136">On the Action Pane, select **Field list**.</span></span>
1. <span data-ttu-id="c324a-137">Lapā **Lauku saraksts** konfigurējiet informāciju, ko noliktavas programma rāda katrai rindai sarakstā.</span><span class="sxs-lookup"><span data-stu-id="c324a-137">On the **Field list** page, configure the information that the warehouse app shows for each line in the list.</span></span>

    - <span data-ttu-id="c324a-138">Lauks **Primārā kontrole** vienmēr ir iestatīts uz *LineNum*.</span><span class="sxs-lookup"><span data-stu-id="c324a-138">The **Primary control** field is always set to *LineNum*.</span></span> <span data-ttu-id="c324a-139">Tāpēc katra saraksta rinda sākas ar rindas numuru.</span><span class="sxs-lookup"><span data-stu-id="c324a-139">Therefore, each row in the list begins with a line number.</span></span>
    - <span data-ttu-id="c324a-140">Izmantojiet atlikušos **Parādāmais lauks** laukus, lai pievienotu līdz septiņiem papildu parādāmajiem laukiem, pēc nepieciešamības.</span><span class="sxs-lookup"><span data-stu-id="c324a-140">Use the remaining **Display field** fields to add up to seven additional display fields, as you require.</span></span> <span data-ttu-id="c324a-141">Katrā **Parādāmais lauks** laukā atlasiet darba rindas lauka nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="c324a-141">In each **Display field** field, select the name of a work line field.</span></span> <span data-ttu-id="c324a-142">Katrai rindai tiks parādīta šī lauka vērtība.</span><span class="sxs-lookup"><span data-stu-id="c324a-142">Each line will then show a value for that field.</span></span> <span data-ttu-id="c324a-143">Vērtības tiks rādītas šeit atlasītajā pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="c324a-143">The values will be shown in the order that you select here.</span></span> <span data-ttu-id="c324a-144">Dažus no **Parādāmais lauks** laukiem var atstāt tukšus, ja nav nepieciešamas visas septiņas vērtības.</span><span class="sxs-lookup"><span data-stu-id="c324a-144">You can leave some of the **Display field** fields blank if you don't require all seven values.</span></span>

1. <span data-ttu-id="c324a-145">Darbību rūtī atlasiet **Saglabāt** un pēc tam aizveriet lapu **Lauku saraksts**.</span><span class="sxs-lookup"><span data-stu-id="c324a-145">On the Action Pane, select **Save**, and then close the **Field list** page.</span></span>