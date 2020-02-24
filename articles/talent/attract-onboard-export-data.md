---
title: Datu eksportēšana no programmām Attract un Onboard
description: Datu eksportēšana no Dynamics 365 Talent — Attract un Onboard.
author: andreabichsel
manager: AnnBe
ms.date: 01/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Talent October 2019 update
ms.openlocfilehash: eb97a16c15476c2f34ec581a32a677fa6fee8739
ms.sourcegitcommit: acdd93637385246f9c5c652cccdf2cbfb263cc33
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/23/2020
ms.locfileid: "2975938"
---
# <a name="export-data-from-attract-and-onboard"></a><span data-ttu-id="4253f-103">Datu eksportēšana no programmām Attract un Onboard</span><span class="sxs-lookup"><span data-stu-id="4253f-103">Export data from Attract and Onboard</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4253f-104">Kā paziņots [Programmu Dynamics 365 Talent: Attract un Dynamics 365 Talent: Onboard darbība tiek pārtraukta](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps), mēs pārtraucam Dynamics 365 Talent: Attract un Dynamics 365 Talent: Onboard darbību 2022. gada 1 februārī.</span><span class="sxs-lookup"><span data-stu-id="4253f-104">As announced in [Retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard Apps](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps), we're retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard on February 1, 2022.</span></span> <span data-ttu-id="4253f-105">Lai palīdzētu jums migrēt uz citu, abas programmas tagad nodrošina datu eksporta iespējas.</span><span class="sxs-lookup"><span data-stu-id="4253f-105">To help with your migration to another product, both apps now provide data export capabilities.</span></span>

## <a name="export-data-from-attract"></a><span data-ttu-id="4253f-106">Eksportēt datus no Attract</span><span class="sxs-lookup"><span data-stu-id="4253f-106">Export data from Attract</span></span>

<span data-ttu-id="4253f-107">Jūs varat eksportēt savus datus, neierobežojot piekļuvi savai videi.</span><span class="sxs-lookup"><span data-stu-id="4253f-107">You can export your data without restricting access to your environment.</span></span> <span data-ttu-id="4253f-108">Iespējams, jūs vēlēsieties to darīt testēšanas nolūkā vai, lai saprastu mūsu datu struktūru.</span><span class="sxs-lookup"><span data-stu-id="4253f-108">You might want to do this for testing purposes or to understand our data structure.</span></span> <span data-ttu-id="4253f-109">Kad esat gatavs migrēt, ierobežojiet piekļuvi jūsu Attract videi, izmantojot norādījumus pēc šīs procedūras.</span><span class="sxs-lookup"><span data-stu-id="4253f-109">When you're ready to migrate, restrict access to your Attract environment using the instructions after this procedure.</span></span> <span data-ttu-id="4253f-110">Noteikti eksportējiet datus vēlreiz.</span><span class="sxs-lookup"><span data-stu-id="4253f-110">Be sure to export your data again.</span></span> 

1. <span data-ttu-id="4253f-111">Dodieties uz [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span><span class="sxs-lookup"><span data-stu-id="4253f-111">Go to [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span></span>

2. <span data-ttu-id="4253f-112">Sadaļā **Datu eksports** atlasiet **Pieprasīt datu eksportu**.</span><span class="sxs-lookup"><span data-stu-id="4253f-112">Under **Data export**, select **Request a data export**.</span></span>

   ![[<span data-ttu-id="4253f-113">Pieprasīt datu eksportu no Attract</span><span class="sxs-lookup"><span data-stu-id="4253f-113">Request a data export from Attract</span></span>](./media/attract-onboard-export-data-attract-request.png)](./media/attract-onboard-export-data-attract-request.png)

3. <span data-ttu-id="4253f-114">Kad tiek ziņojuma lodziņš **Jūsu pieprasījums tiek apstrādāts**, atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="4253f-114">When the **Your request is being processed** message box appears, select **OK**.</span></span> <span data-ttu-id="4253f-115">Datu eksports var ilgt līdz 20 minūtēm atkarībā no jūsu eksporta apjoma.</span><span class="sxs-lookup"><span data-stu-id="4253f-115">The data export can take up to 20 minutes, depending on the size of your export.</span></span>

4. <span data-ttu-id="4253f-116">Kad eksports ir pabeigts, atlasiet blakus esošo pogu **Lejupielādēt**.</span><span class="sxs-lookup"><span data-stu-id="4253f-116">When your export completes, select the **Download** button next to it.</span></span> 

   >[!NOTE]
   ><span data-ttu-id="4253f-117">Visi datu eksporti ir pieejami septiņas dienas, un tajā brīdī saites **Lejupielādēt** termiņš beidzas.</span><span class="sxs-lookup"><span data-stu-id="4253f-117">All data exports are available for seven days, at which point the **Download** link expires.</span></span></br>
   
<span data-ttu-id="4253f-118">Lejupielāde satur .zip failu ar jūsu Attract datiem, ieskaitot tālāk norādītās mapes.</span><span class="sxs-lookup"><span data-stu-id="4253f-118">The download contains a .zip file with your Attract data, including the following folders:</span></span>

| <span data-ttu-id="4253f-119">Mapes nosaukums</span><span class="sxs-lookup"><span data-stu-id="4253f-119">Folder name</span></span> | <span data-ttu-id="4253f-120">Apraksts</span><span class="sxs-lookup"><span data-stu-id="4253f-120">Description</span></span> |
| --- | --- |
| <span data-ttu-id="4253f-121">Administratora iestatījumi</span><span class="sxs-lookup"><span data-stu-id="4253f-121">Admin settings</span></span> | <span data-ttu-id="4253f-122">Attract administrēšanas centra konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="4253f-122">Attract admin center configurations.</span></span> |
| <span data-ttu-id="4253f-123">Kandidāti</span><span class="sxs-lookup"><span data-stu-id="4253f-123">Candidates</span></span> | <span data-ttu-id="4253f-124">Visi kandidāti, kas tika pievienoti darbiem vai talantu kopām.</span><span class="sxs-lookup"><span data-stu-id="4253f-124">All candidates that were added to jobs or talent pools.</span></span> |
| <span data-ttu-id="4253f-125">E-pasta veidnes</span><span class="sxs-lookup"><span data-stu-id="4253f-125">Email templates</span></span> | <span data-ttu-id="4253f-126">Visas e-pasta veidnes, kas tika konfigurētas videi.</span><span class="sxs-lookup"><span data-stu-id="4253f-126">All email templates that were configured for the environment.</span></span> |
| <span data-ttu-id="4253f-127">Darba piedāvājuma pakotņu veidnes</span><span class="sxs-lookup"><span data-stu-id="4253f-127">Job offer package templates</span></span> | <span data-ttu-id="4253f-128">Visas izveidotās darba piedāvājumu pakotņu veidnes un ar tām saistītās konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="4253f-128">All job offer package templates that were created, plus their associated configurations.</span></span> |
| <span data-ttu-id="4253f-129">Darba piedāvājuma kārtulu kopas</span><span class="sxs-lookup"><span data-stu-id="4253f-129">Job offer rule sets</span></span> |  <span data-ttu-id="4253f-130">Visi kārtulu kopu faili, kas tika augšupielādēti piedāvājuma pārvaldībai.</span><span class="sxs-lookup"><span data-stu-id="4253f-130">All rule set files that were uploaded for offer management.</span></span> |
| <span data-ttu-id="4253f-131">Darba piedāvājuma veidnes</span><span class="sxs-lookup"><span data-stu-id="4253f-131">Job offer templates</span></span> | <span data-ttu-id="4253f-132">Visas darba piedāvājumu dokumentu veidnes, kas izveidotas videi.</span><span class="sxs-lookup"><span data-stu-id="4253f-132">All job offer document templates created for the environment.</span></span> |
| <span data-ttu-id="4253f-133">Darba piedāvājumi</span><span class="sxs-lookup"><span data-stu-id="4253f-133">Job openings</span></span> | <span data-ttu-id="4253f-134">Visi izveidotie darbi.</span><span class="sxs-lookup"><span data-stu-id="4253f-134">All created jobs.</span></span> <span data-ttu-id="4253f-135">Dzēstie darbi netiek eksportēti.</span><span class="sxs-lookup"><span data-stu-id="4253f-135">Deleted jobs aren't exported.</span></span> <span data-ttu-id="4253f-136">Apakšmapēs ir iekļauti kandidātu pieteikumi, ar apakšmapēm kandidātu pieteikumu pielikumiem un piedāvājuma pakotnēm, ja piemērojams.</span><span class="sxs-lookup"><span data-stu-id="4253f-136">The sub-folders contain candidate applications, with sub-folders for candidate application attachments and offer packages, where applicable.</span></span> |
| <span data-ttu-id="4253f-137">Darba piedāvājumu veidnes</span><span class="sxs-lookup"><span data-stu-id="4253f-137">Job opening templates</span></span> | <span data-ttu-id="4253f-138">Visas darba procesa veidnes, kas tika konfigurētas videi.</span><span class="sxs-lookup"><span data-stu-id="4253f-138">Job process templates that were configured in the environment.</span></span> |
| <span data-ttu-id="4253f-139">Kandidātu kopas</span><span class="sxs-lookup"><span data-stu-id="4253f-139">Talent pools</span></span> | <span data-ttu-id="4253f-140">Visas izveidotās talantu kopas, to atbalstītāju saraksti un kandidātu saraksti talantu kopām.</span><span class="sxs-lookup"><span data-stu-id="4253f-140">All created talent pools, their contributors lists, and the candidates lists for the talent pools.</span></span> |
| <span data-ttu-id="4253f-141">Nodarbinātie</span><span class="sxs-lookup"><span data-stu-id="4253f-141">Workers</span></span> | <span data-ttu-id="4253f-142">Saraksts ar visiem darbiniekiem, kuri atrodas vidē, un viņu lomas.</span><span class="sxs-lookup"><span data-stu-id="4253f-142">List of all the workers who are present in the environment, plus their roles.</span></span> |
| <span data-ttu-id="4253f-143">(saknes mape)</span><span class="sxs-lookup"><span data-stu-id="4253f-143">(root folder)</span></span> | <span data-ttu-id="4253f-144">JSON shēmas fails, kas apraksta datu struktūras laukus.</span><span class="sxs-lookup"><span data-stu-id="4253f-144">A JSON schema file that describes the data structure fields.</span></span> |

### <a name="restrict-access-to-attract"></a><span data-ttu-id="4253f-145">Ierobežot piekļuvi programmai Attract</span><span class="sxs-lookup"><span data-stu-id="4253f-145">Restrict access to Attract</span></span>

<span data-ttu-id="4253f-146">Kad esat gatavs migrēt, ierobežojiet piekļuvi lietotājiem, kas nav administratori, video Attract un eksportējiet savus datus.</span><span class="sxs-lookup"><span data-stu-id="4253f-146">When you're ready to migrate, restrict non-admins from accessing your Attract environment and export your data.</span></span>

>[!IMPORTANT]
><span data-ttu-id="4253f-147">Piekļuves ierobežošana jūsu Attract videi ir pastāvīga, un to nevar atsaukt.</span><span class="sxs-lookup"><span data-stu-id="4253f-147">Restricting access to your Attract environment is permanent and can't be undone.</span></span> <span data-ttu-id="4253f-148">Ja vēlaties, lai lietotāji, kas nav administratori, varētu turpināt piekļūt jūsu videi, izlaidiet šo darbību.</span><span class="sxs-lookup"><span data-stu-id="4253f-148">If you want non-admin users to continue accessing your environment, skip this step.</span></span>

1. <span data-ttu-id="4253f-149">Dodieties uz [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span><span class="sxs-lookup"><span data-stu-id="4253f-149">Go to [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span></span>

2. <span data-ttu-id="4253f-150">Lai ierobežotu lietotāju, kas nav administratori, piekļuvi jūsu Attract videi, sadaļā **Ierobežot piekļuvi šai programmai** atlasiet **Ierobežot piekļuvi tagad**.</span><span class="sxs-lookup"><span data-stu-id="4253f-150">To restrict non-admins from accessing your Attract environment, under **Restrict access to this app**, select **Restrict access now**.</span></span> <span data-ttu-id="4253f-151">Piekļuves ierobežošana arī atgrāmato visus aktīvos darbus, kas ir grāmatoti.</span><span class="sxs-lookup"><span data-stu-id="4253f-151">Restricting access also unposts any active jobs that have been posted.</span></span>

   ![[<span data-ttu-id="4253f-152">Ierobežot lietotāju, kas nav administratori, piekļuvi programmai Attract</span><span class="sxs-lookup"><span data-stu-id="4253f-152">Restrict non-admin access to Attract</span></span>](./media/attract-onboard-export-data-attract-restrict-access.png)](./media/attract-onboard-export-data-attract-restrict-access.png)

3. <span data-ttu-id="4253f-153">Kad redzat brīdinājumu, **Šīs izmaiņas ir paliekošas**, atlasiet **Ierobežot piekļuvi**, lai pastāvīgi ierobežotu lietotājus, kas nav administratori, no šīs vides.</span><span class="sxs-lookup"><span data-stu-id="4253f-153">When you see the warning **This is a permanent change**, select **Restrict access** to permanently restrict non-admin users from this environment.</span></span> <span data-ttu-id="4253f-154">Ja neesat gatavs pabeigt šo darbību, atlasiet **Atcelt**.</span><span class="sxs-lookup"><span data-stu-id="4253f-154">If you're not ready to complete this step, select **Cancel**.</span></span>

   ![[<span data-ttu-id="4253f-155">Brīdinājums, ka piekļuves ierobežošana ir neatgriezeniskas izmaiņas</span><span class="sxs-lookup"><span data-stu-id="4253f-155">Warning that restricting access is a permanent change</span></span>](./media/attract-onboard-export-data-attract-warning.png)](./media/attract-onboard-export-data-attract-warning.png)

   >[!NOTE]
   ><span data-ttu-id="4253f-156">Administratori var turpināt piekļūt datu eksporta un personas pārskata lapām pēc tam, kad jūs ierobežojat piekļuvi Attract videi.</span><span class="sxs-lookup"><span data-stu-id="4253f-156">Admins can continue to access the data export and person report pages after you restrict access to the Attract environment.</span></span>

## <a name="export-data-from-onboard"></a><span data-ttu-id="4253f-157">Eksportēt datus no Onboard</span><span class="sxs-lookup"><span data-stu-id="4253f-157">Export data from Onboard</span></span>

<span data-ttu-id="4253f-158">Kad esat gatavs, varat lejupielādēt veidnes, ceļvežus un kandidātu datus no Onboard.</span><span class="sxs-lookup"><span data-stu-id="4253f-158">When you're ready, you can download templates, guides, and candidate data from Onboard.</span></span>

1. <span data-ttu-id="4253f-159">Dodieties uz [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).</span><span class="sxs-lookup"><span data-stu-id="4253f-159">Go to [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).</span></span>

2. <span data-ttu-id="4253f-160">Sadaļā **Datu eksports** atlasiet **Pieprasīt datu eksportu**.</span><span class="sxs-lookup"><span data-stu-id="4253f-160">Under **Data export**, select **Request a data export**.</span></span> 

   ![[<span data-ttu-id="4253f-161">Pieprasīt datu eksportu no Onboard</span><span class="sxs-lookup"><span data-stu-id="4253f-161">Request a data export from Onboard</span></span>](./media/attract-onboard-export-data-onboard-request.png)](./media/attract-onboard-export-data-onboard-request.png)

3. <span data-ttu-id="4253f-162">Kad tiek ziņojuma lodziņš **Jūsu pieprasījums tiek apstrādāts**, atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="4253f-162">When the **Your request is being processed** message box appears, select **OK**.</span></span> <span data-ttu-id="4253f-163">Datu eksports var ilgt līdz 20 minūtēm atkarībā no jūsu eksporta apjoma.</span><span class="sxs-lookup"><span data-stu-id="4253f-163">The data export can take up to 20 minutes, depending on the size of your export.</span></span>

4. <span data-ttu-id="4253f-164">Kad eksports ir pabeigts, atlasiet blakus esošo pogu **Lejupielādēt**.</span><span class="sxs-lookup"><span data-stu-id="4253f-164">When your export completes, select the **Download** button next to it.</span></span> 

   ![[<span data-ttu-id="4253f-165">Lejupielādēt datu eksportu no Onboard</span><span class="sxs-lookup"><span data-stu-id="4253f-165">Download data export from Onboard</span></span>](./media/attract-onboard-export-data-onboard-download.png)](./media/attract-onboard-export-data-onboard-download.png)

   >[!NOTE]
   ><span data-ttu-id="4253f-166">Jūsu datu eksports ir pieejams septiņas dienas.</span><span class="sxs-lookup"><span data-stu-id="4253f-166">Your data export is available for seven days.</span></span> <span data-ttu-id="4253f-167">Pēc septiņām dienām saites **Lejupielādēt** termiņš beidzas, un jums ir jāpieprasa jauns eksports, ja nepieciešams atkārtoti lejupielādēt datus.</span><span class="sxs-lookup"><span data-stu-id="4253f-167">After seven days, the **Download** link expires, and you must request a new export if you need to download your data again.</span></span> <span data-ttu-id="4253f-168">Kad sākat jaunu datu eksportu, visām esošajām lejupielādēm derīguma termiņš beigsies pēc jaunās eksportēšanas veiksmīgas darbības.</span><span class="sxs-lookup"><span data-stu-id="4253f-168">When you start a new data export, any existing downloads will expire after the new export succeeds.</span></span>

<span data-ttu-id="4253f-169">Lejupielāde ir.zip fails, kas satur tālāk norādīto.</span><span class="sxs-lookup"><span data-stu-id="4253f-169">The download is a .zip file that contains:</span></span>

- <span data-ttu-id="4253f-170">**Veidņu** mape, kas ietver jūsu Onboard veidnes Word dokumenta formātā.</span><span class="sxs-lookup"><span data-stu-id="4253f-170">A **Templates** folder that contains your Onboard templates in Word document format.</span></span>

- <span data-ttu-id="4253f-171">**Ceļvežu** mape, kas ietver jūsu Onboard ceļvežus Word dokumenta formātā.</span><span class="sxs-lookup"><span data-stu-id="4253f-171">A **Guides** folder that contains your Onboard guides in Word document format.</span></span>

## <a name="see-also"></a><span data-ttu-id="4253f-172">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="4253f-172">See also</span></span>

[<span data-ttu-id="4253f-173">Programmu Dynamics 365 Talent: Attract un Dynamics 365 Talent: Onboard darbības pārtraukšana</span><span class="sxs-lookup"><span data-stu-id="4253f-173">Retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard Apps</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)