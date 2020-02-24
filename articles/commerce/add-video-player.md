---
title: Video atskaņotāja modulis
description: Šajā tēmā tiek stāstīts par video atskaņotāja moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e94658eed12b12d6666e63d2c06b86646c81a120
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025660"
---
# <a name="video-player-module"></a><span data-ttu-id="14d24-103">Video atskaņotāja modulis</span><span class="sxs-lookup"><span data-stu-id="14d24-103">Video player module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="14d24-104">Šajā tēmā tiek stāstīts par video atskaņotāja moduļiem un aprakstīts, kā tos pievienot vietnes lapām programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="14d24-104">This topic covers video player modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="14d24-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="14d24-105">Overview</span></span>

<span data-ttu-id="14d24-106">Video atskaņotāja modulis tiek izmantots, lai atbalstītu video atskaņošanu.</span><span class="sxs-lookup"><span data-stu-id="14d24-106">The video player module is used to support video playback.</span></span> <span data-ttu-id="14d24-107">To var pievienot jebkurai lapai, ar nosacījumu, ka video saturs tiek augšupielādēts un pieejams satura pārvaldības sistēmā (CMS).</span><span class="sxs-lookup"><span data-stu-id="14d24-107">It can be added to any page, provided that video content is uploaded to and available in the content management system (CMS).</span></span> <span data-ttu-id="14d24-108">Video atskaņotāja modulis atbalsta .mp4 multivides veidu.</span><span class="sxs-lookup"><span data-stu-id="14d24-108">The video player module supports the .mp4 media type.</span></span>

## <a name="video-player-module"></a><span data-ttu-id="14d24-109">Video atskaņotāja modulis</span><span class="sxs-lookup"><span data-stu-id="14d24-109">Video player module</span></span>

<span data-ttu-id="14d24-110">Video atskaņotāja moduli var izmantot, lai parādītu videoklipus E-komercijas vietnē.</span><span class="sxs-lookup"><span data-stu-id="14d24-110">The video player module can be used to showcase videos on an e-Commerce site.</span></span> <span data-ttu-id="14d24-111">Tas atbalsta visas atskaņošanas iespējas, piemēram, atskaņošanu, pauzi, pilna izmēra režīmu, audio aprakstus un slēptos titrus.</span><span class="sxs-lookup"><span data-stu-id="14d24-111">It supports all playback capabilities, such as play, pause, full-size mode, audio descriptions, and closed captions.</span></span> <span data-ttu-id="14d24-112">Video atskaņotāja modulis atbalsta arī slēpto titru pielāgošanu, lai tie atbilstu Microsoft pieejamības standartiem.</span><span class="sxs-lookup"><span data-stu-id="14d24-112">The video player module also supports customization of closed captions to meet Microsoft accessibility standards.</span></span> <span data-ttu-id="14d24-113">Piemēram, varat pielāgot fonta izmēru un fona krāsu.</span><span class="sxs-lookup"><span data-stu-id="14d24-113">For example, you can customize the font size and background color.</span></span>

<span data-ttu-id="14d24-114">Video atskaņotāja modulis atbalsta arī sekundāros audio celiņus.</span><span class="sxs-lookup"><span data-stu-id="14d24-114">The video player module also supports secondary audio tracks.</span></span> <span data-ttu-id="14d24-115">Augšupielādējot videoklipu satura pārvaldības sistēmā, var augšupielādēt arī sekundāro audio celiņu.</span><span class="sxs-lookup"><span data-stu-id="14d24-115">When a video is uploaded to the CMS, a secondary audio track can also be uploaded.</span></span> <span data-ttu-id="14d24-116">Pēc tam video atskaņotāja modulis var atskaņot sekundāro audio celiņu, ja lietotājs to atlasījis.</span><span class="sxs-lookup"><span data-stu-id="14d24-116">The video player module can then play the secondary audio track if a user selects it.</span></span>

### <a name="examples-of-video-player-modules-in-e-commerce"></a><span data-ttu-id="14d24-117">Video atskaņotāja moduļu piemēri E-komercijā</span><span class="sxs-lookup"><span data-stu-id="14d24-117">Examples of video player modules in e-Commerce</span></span>

- <span data-ttu-id="14d24-118">Pasniegšanas video preču detalizētas informācijas lapās vai mārketinga lapās</span><span class="sxs-lookup"><span data-stu-id="14d24-118">Instructional videos on product details pages or marketing pages</span></span>
- <span data-ttu-id="14d24-119">Reklāmas videoklipi vai videoklipi par politikām jebkurā mārketinga lapā</span><span class="sxs-lookup"><span data-stu-id="14d24-119">Promotional videos or videos about policies on any marketing page</span></span>
- <span data-ttu-id="14d24-120">Mārketinga videoklipi, kas izceļ preces funkcijas preces informācijas lapās vai mārketinga lapās</span><span class="sxs-lookup"><span data-stu-id="14d24-120">Marketing videos that highlight product features on product details pages or marketing pages</span></span>

### <a name="video-player-module-properties"></a><span data-ttu-id="14d24-121">Video atskaņotāja moduļa rekvizīti</span><span class="sxs-lookup"><span data-stu-id="14d24-121">Video player module properties</span></span>

| <span data-ttu-id="14d24-122">Rekvizīta nosaukums</span><span class="sxs-lookup"><span data-stu-id="14d24-122">Property name</span></span>         | <span data-ttu-id="14d24-123">Vērtība</span><span class="sxs-lookup"><span data-stu-id="14d24-123">Value</span></span>                               | <span data-ttu-id="14d24-124">Apraksts</span><span class="sxs-lookup"><span data-stu-id="14d24-124">Description</span></span> |
|-----------------------|-------------------------------------|-------------|
| <span data-ttu-id="14d24-125">Automātiskā atskaņošana</span><span class="sxs-lookup"><span data-stu-id="14d24-125">Auto play</span></span>             | <span data-ttu-id="14d24-126">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="14d24-126">**True** or **False**</span></span>               | <span data-ttu-id="14d24-127">Ja vērtība ir iestatīta uz **Patiess**, videoklips tiek automātiski atskaņots.</span><span class="sxs-lookup"><span data-stu-id="14d24-127">When the value is set to **True**, the video is automatically played.</span></span> |
| <span data-ttu-id="14d24-128">Izslēgt skaņu</span><span class="sxs-lookup"><span data-stu-id="14d24-128">Mute</span></span>                  | <span data-ttu-id="14d24-129">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="14d24-129">**True** or **False**</span></span>               | <span data-ttu-id="14d24-130">Ja vērtība ir iestatīta uz **Patiess**, tiek izslēgta skaņa.</span><span class="sxs-lookup"><span data-stu-id="14d24-130">When the value is set to **True**, the audio is muted.</span></span> <span data-ttu-id="14d24-131">Šajā atskaņotājā noklusējuma vērtība ir **Nepatiess**.</span><span class="sxs-lookup"><span data-stu-id="14d24-131">For this player, the default value is **False**.</span></span> <span data-ttu-id="14d24-132">Google Chrome pārlūkā automātiskās atskaņošanas videoklipiem pēc noklusējuma tiek izslēgta skaņa, kura tiek atskaņota tikai tad, ja lietotājs manuāli atskaņo videoklipu.</span><span class="sxs-lookup"><span data-stu-id="14d24-132">In the Chrome browser, autoplay videos are muted by default, and the audio is played only if the user manually plays the video.</span></span> |
| <span data-ttu-id="14d24-133">Cilpa</span><span class="sxs-lookup"><span data-stu-id="14d24-133">Loop</span></span>                  | <span data-ttu-id="14d24-134">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="14d24-134">**True** or **False**</span></span>               | <span data-ttu-id="14d24-135">Ja vērtība ir iestatīta uz **Patiess**, videoklipa atskaņošana tiek atkārtota.</span><span class="sxs-lookup"><span data-stu-id="14d24-135">When the value is set to **True**, the video is repeated in a loop.</span></span> |
| <span data-ttu-id="14d24-136">Plašsaziņas līdzekļi</span><span class="sxs-lookup"><span data-stu-id="14d24-136">Media</span></span>                 | <span data-ttu-id="14d24-137">Video faila ceļš un nosaukums</span><span class="sxs-lookup"><span data-stu-id="14d24-137">Video file path and name</span></span> | <span data-ttu-id="14d24-138">Video fails, ko atskaņo video atskaņotājā.</span><span class="sxs-lookup"><span data-stu-id="14d24-138">The video file that is played in the video player.</span></span> |
| <span data-ttu-id="14d24-139">Atskaņot pilnekrāna režīmā</span><span class="sxs-lookup"><span data-stu-id="14d24-139">Play fullscreen</span></span>       | <span data-ttu-id="14d24-140">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="14d24-140">**True** or **False**</span></span>               | <span data-ttu-id="14d24-141">Ja vērtība ir iestatīta uz **Patiess**, videoklips tiek automātiski atskaņots pilnekrāna režīmā.</span><span class="sxs-lookup"><span data-stu-id="14d24-141">When the value is set to **True**, the video is played in full-screen mode.</span></span> |
| <span data-ttu-id="14d24-142">Atskaņošanas vai pauzes trigeris</span><span class="sxs-lookup"><span data-stu-id="14d24-142">Play pause trigger</span></span>    | <span data-ttu-id="14d24-143">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="14d24-143">**True** or **False**</span></span>               | <span data-ttu-id="14d24-144">Ja vērtība ir iestatīta kā **Patiess**, videoklipā ir redzama poga atskaņot/apturēt.</span><span class="sxs-lookup"><span data-stu-id="14d24-144">When the value is set to **True**, a play/pause button is shown on the video.</span></span> |
| <span data-ttu-id="14d24-145">Video atskaņotāja vadīklas</span><span class="sxs-lookup"><span data-stu-id="14d24-145">Video player controls</span></span> | <span data-ttu-id="14d24-146">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="14d24-146">**True** or **False**</span></span>               | <span data-ttu-id="14d24-147">Ja vērtība ir iestatīta uz **Patiess**, tiek rādītas visas video atskaņotāja vadīklas.</span><span class="sxs-lookup"><span data-stu-id="14d24-147">When the value is set to **True**, all video player controls are shown.</span></span> <span data-ttu-id="14d24-148">Šīs vadīklas ietver atskaņošanas un pauzes pogas, progresa indikatoru un slēpts titru opcijas.</span><span class="sxs-lookup"><span data-stu-id="14d24-148">These controls include play and pause buttons, a progress indicator, and closed caption options.</span></span> |
| <span data-ttu-id="14d24-149">Paslēpt grāmatotāja attēlu</span><span class="sxs-lookup"><span data-stu-id="14d24-149">Hide poster image</span></span>     | <span data-ttu-id="14d24-150">**Patiess** vai **Nepatiess**</span><span class="sxs-lookup"><span data-stu-id="14d24-150">**True** or **False**</span></span>               | <span data-ttu-id="14d24-151">Videoklipam var būt plakāta kadrs.</span><span class="sxs-lookup"><span data-stu-id="14d24-151">A video can have a poster frame.</span></span> <span data-ttu-id="14d24-152">Ja šī rekvizīta vērtība ir iestatīta uz **Patiess**, plakāta kadrs ir paslēpts.</span><span class="sxs-lookup"><span data-stu-id="14d24-152">When the value of this property is set to **True**, the poster frame is hidden.</span></span> |
| <span data-ttu-id="14d24-153">Maskas līmenis</span><span class="sxs-lookup"><span data-stu-id="14d24-153">Mask level</span></span>            | <span data-ttu-id="14d24-154">Skaitlis no **0** līdz **100**</span><span class="sxs-lookup"><span data-stu-id="14d24-154">A number from **0** through **100**</span></span> | <span data-ttu-id="14d24-155">Maska, kas tiek lietota videoklipa stilizēšanai.</span><span class="sxs-lookup"><span data-stu-id="14d24-155">The mask that is applied to the video for styling.</span></span> |

## <a name="add-a-video-player-module-to-a-page"></a><span data-ttu-id="14d24-156">Video atskaņotāja moduļa pievienošana lapā</span><span class="sxs-lookup"><span data-stu-id="14d24-156">Add a video player module to a page</span></span>

> [!NOTE] 
> <span data-ttu-id="14d24-157">Pirms video atskaņotāja moduļa izveides vispirms ir jāaugšupielādē video multivides bibliotēkā.</span><span class="sxs-lookup"><span data-stu-id="14d24-157">Before you create a video player module, you must first upload a video to the Media Library.</span></span>

<span data-ttu-id="14d24-158">Lai pievienotu video atskaņotāja moduli jaunā lapā un iestatītu nepieciešamos rekvizītus, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="14d24-158">To add a video player module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="14d24-159">Izveidojiet lapas veidni ar nosaukumu **video atskaņotāja veidne**.</span><span class="sxs-lookup"><span data-stu-id="14d24-159">Create a page template that is named **video player template**.</span></span>
1. <span data-ttu-id="14d24-160">Noklusējuma lapas **Galvenajā** slotā pievienojiet konteinera moduli.</span><span class="sxs-lookup"><span data-stu-id="14d24-160">In the **Main** slot of the default page, add a container module.</span></span>
1. <span data-ttu-id="14d24-161">Konteinera modulī pievienojiet video atskaņotāju un ambienta video atskaņotāja moduļus.</span><span class="sxs-lookup"><span data-stu-id="14d24-161">In the container module, add video player and ambient video player modules.</span></span>
1. <span data-ttu-id="14d24-162">Pabeidziet rediģēt veidni un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="14d24-162">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="14d24-163">Izmantojiet jūsu izveidoto video atskaņotāja veidni, lai izveidotu lapu ar nosaukumu **video atskaņotāja lapa**.</span><span class="sxs-lookup"><span data-stu-id="14d24-163">Use the video player template that you created to create a page that is named **video player page**.</span></span>
1. <span data-ttu-id="14d24-164">Jaunās lapas **Galvenajā** slotā pievienojiet ambienta video atskaņotāja moduli.</span><span class="sxs-lookup"><span data-stu-id="14d24-164">In the **Main** slot of the new page, add a video player module.</span></span>
1. <span data-ttu-id="14d24-165">Video atskaņotāja moduļa rekvizītu rūtī atlasiet **Pievienot videoklipu**.</span><span class="sxs-lookup"><span data-stu-id="14d24-165">In the property pane for the video player module, select **Add a video**.</span></span>
1. <span data-ttu-id="14d24-166">Dialoglodziņā **Multivides atlasītājs** atlasiet videoklipu un pēc tam atlasiet **Augšupielādēt jaunu multivides vienumu**.</span><span class="sxs-lookup"><span data-stu-id="14d24-166">In the **Media Picker** dialog box, select a video, and then select **Upload new media item**.</span></span>
1. <span data-ttu-id="14d24-167">Saglabājiet un priekšskatiet lapu.</span><span class="sxs-lookup"><span data-stu-id="14d24-167">Save and preview the page.</span></span> <span data-ttu-id="14d24-168">Lapā jābūt redzamam video modulim.</span><span class="sxs-lookup"><span data-stu-id="14d24-168">You should see the video module on the page.</span></span> <span data-ttu-id="14d24-169">Varat mainīt papildu iestatījumus, lai pielāgotu moduļa darbību.</span><span class="sxs-lookup"><span data-stu-id="14d24-169">You can change additional settings to customize the behavior of the module.</span></span>
1. <span data-ttu-id="14d24-170">Pabeidziet rediģēt lapu un publicējiet to.</span><span class="sxs-lookup"><span data-stu-id="14d24-170">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="14d24-171">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="14d24-171">Additional resources</span></span>

[<span data-ttu-id="14d24-172">Sākuma komplekta pārskats</span><span class="sxs-lookup"><span data-stu-id="14d24-172">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="14d24-173">Veicināšanas reklāmkarogu modulis</span><span class="sxs-lookup"><span data-stu-id="14d24-173">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="14d24-174">Karuseļa modulis</span><span class="sxs-lookup"><span data-stu-id="14d24-174">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="14d24-175">Teksta bloka modulis</span><span class="sxs-lookup"><span data-stu-id="14d24-175">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="14d24-176">Satura bloka modulis</span><span class="sxs-lookup"><span data-stu-id="14d24-176">Content block module</span></span>](add-hero-module.md)
