---
title: Statisku failu augšupielāde un apkalpošana
description: Šajā tēmā ir aprakstīts, kā augšupielādēt statisku failu programmas Microsoft Dynamics 365 Commerce vietnes veidotājā un kā izveidot pielāgotu vietrādi URL un faila nosaukumu, ko var izmantot, lai pieprasītu šo failu.
author: StuHarg
manager: annbe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: aba9dde2ed9d5fa09e92fcdd784a53f208930eda
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211023"
---
# <a name="upload-and-serve-static-files"></a><span data-ttu-id="1d364-103">Statisku failu augšupielāde un apkalpošana</span><span class="sxs-lookup"><span data-stu-id="1d364-103">Upload and serve static files</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1d364-104">Šajā tēmā ir aprakstīts, kā augšupielādēt statisku failu programmas Microsoft Dynamics 365 Commerce vietnes veidotājā un kā izveidot pielāgotu vietrādi URL un faila nosaukumu, ko var izmantot, lai pieprasītu šo failu.</span><span class="sxs-lookup"><span data-stu-id="1d364-104">This topic describes how to upload a static file into Microsoft Dynamics 365 Commerce site builder, and how to create a custom URL and file name that can be used to request that file.</span></span>

<span data-ttu-id="1d364-105">Daži trešās puses savienotāji pieprasa, lai fails tiktu viesots un apkalpots no e-komercijas vietnes.</span><span class="sxs-lookup"><span data-stu-id="1d364-105">Some third-party connectors require that a file be hosted and served from the e-commerce site.</span></span> <span data-ttu-id="1d364-106">Šie savienotāji sagaida, ka fails tiks atgriezts pēc pieprasījumiem uz konkrētu atzvanīšanas vietrāža URL ceļu un faila nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="1d364-106">These connectors expect that the file will be returned by requests to a specific callback URL path and file name.</span></span> <span data-ttu-id="1d364-107">Tāpēc šajā tēmā ir paskaidrots, kā augšupielādēt un apkalpot statisku failu, kam ir lietotāja definējams vietrādis URL un faila nosaukums Dynamics 365 Commerce e-komercijas vietnē.</span><span class="sxs-lookup"><span data-stu-id="1d364-107">Therefore, this topic explains how to upload and serve a static file that has a user-definable URL and file name on a Dynamics 365 Commerce e-commerce site.</span></span>

## <a name="create-a-site-url-that-returns-a-static-file"></a><span data-ttu-id="1d364-108">Izveidot vietnes vietrādi URL, kas atgriež statisku failu</span><span class="sxs-lookup"><span data-stu-id="1d364-108">Create a site URL that returns a static file</span></span>

<span data-ttu-id="1d364-109">Lai izveidotu vietnes vietrādi URL, kas atgriež statisku failu Commerce vietnes veidotājā, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="1d364-109">To create a site URL that returns a static file in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="1d364-110">Dodieties uz savas vietnes multivides bibliotēku un augšupielādējiet failu, kas jāapkalpo, izmantojot pieprasījumus uz vietrādi URL, kuru definēsit.</span><span class="sxs-lookup"><span data-stu-id="1d364-110">Go to your site's Media library, and upload the file that should be served by requests to the URL that you will define.</span></span> <span data-ttu-id="1d364-111">Ja fails jau ir augšupielādēts, varat izlaist šo darbību.</span><span class="sxs-lookup"><span data-stu-id="1d364-111">If you've already uploaded the file, you can skip this step.</span></span>
1. <span data-ttu-id="1d364-112">Dodieties uz savas vietnes **URL**.</span><span class="sxs-lookup"><span data-stu-id="1d364-112">Go to **URLs** for your site.</span></span>
1. <span data-ttu-id="1d364-113">Atlasiet **Jauns \> Jauns URL**.</span><span class="sxs-lookup"><span data-stu-id="1d364-113">Select **New \> New URL**.</span></span>
1. <span data-ttu-id="1d364-114">Dialoglodziņā **Jauns URL** atlasiet **Multivides bibliotēkas līdzeklis**.</span><span class="sxs-lookup"><span data-stu-id="1d364-114">In the **New URL** dialog box, select **Media library asset**.</span></span>
1. <span data-ttu-id="1d364-115">Laukā **URL ceļš** ievadiet vietrāža URL ceļu.</span><span class="sxs-lookup"><span data-stu-id="1d364-115">In the **URL path** field, enter the URL path.</span></span> <span data-ttu-id="1d364-116">Ceļā iekļaujiet faila nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="1d364-116">Include the file name in the path.</span></span>
1. <span data-ttu-id="1d364-117">Atlasiet **Nākamais**.</span><span class="sxs-lookup"><span data-stu-id="1d364-117">Select **Next**.</span></span> <span data-ttu-id="1d364-118">Tiek atvērta multivides bibliotēka, un tajā ir parādīti visi **dokumenta** veida augšupielādētie multivides līdzekļi.</span><span class="sxs-lookup"><span data-stu-id="1d364-118">The Media library is opened and shows all media assets of the **document** type that have been uploaded.</span></span>
1. <span data-ttu-id="1d364-119">Atlasiet failu, kas ir jānodod pieprasījumiem uz vietrādi URL, kuru definējāt 5. darbībā.</span><span class="sxs-lookup"><span data-stu-id="1d364-119">Select the file that should be served for requests to the URL that you defined in step 5.</span></span>
1. <span data-ttu-id="1d364-120">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="1d364-120">Select **Save**.</span></span>

<span data-ttu-id="1d364-121">Šajā brīdī vietrādis URL, kuru izveidojāt, ir melnraksta statusā.</span><span class="sxs-lookup"><span data-stu-id="1d364-121">At this point, the URL that you created is in a draft state.</span></span> <span data-ttu-id="1d364-122">Fails, uz kuru URL norāda, netiks atgriezts, līdz publicēsit vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="1d364-122">The file that the URL points to won't be returned until you publish the URL.</span></span> <span data-ttu-id="1d364-123">Pirms publicējat vietrādi URL, varat validēt, ka tiek atgriezti pareizie dati.</span><span class="sxs-lookup"><span data-stu-id="1d364-123">Before you publish the URL, you can validate that it returns the correct data.</span></span>

## <a name="validate-and-publish-a-url"></a><span data-ttu-id="1d364-124">Vietrāža URL validācija un publicēšana</span><span class="sxs-lookup"><span data-stu-id="1d364-124">Validate and publish a URL</span></span>

<span data-ttu-id="1d364-125">Lai validētu vietrādi URL pirms tā publicēšanas, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="1d364-125">To validate an URL before you publish it, follow these steps.</span></span>

1. <span data-ttu-id="1d364-126">Dodieties uz savas vietnes **URL** un atlasiet vietrādi URL, ko priekšskatīt.</span><span class="sxs-lookup"><span data-stu-id="1d364-126">Go to **URLs** for your site, and select the URL to preview.</span></span>
2. <span data-ttu-id="1d364-127">Rekvizītu rūtī labajā pusē zem pogas **Rediģēt** atlasiet pareizo vietrāža URL saiti.</span><span class="sxs-lookup"><span data-stu-id="1d364-127">In the properties pane on the right, below the **Edit** button, select the correct URL link.</span></span> <span data-ttu-id="1d364-128">Tiek atvērts jauns pārlūkprogrammas logs, un jums ir jāsaņem kļūda 404.</span><span class="sxs-lookup"><span data-stu-id="1d364-128">A new browser window is opened, and you should receive a 404 error.</span></span>
3. <span data-ttu-id="1d364-129">Pievienojiet vaicājuma virkni **?preview=inprogress** vietrādim URL (piemēram, `https://yoursite.com/callback.html?preview=inprogress`) un pārlādējiet lapu.</span><span class="sxs-lookup"><span data-stu-id="1d364-129">Append the **?preview=inprogress** query string to the URL (for example, `https://yoursite.com/callback.html?preview=inprogress`), and reload the page.</span></span> <span data-ttu-id="1d364-130">Failam, ko augšupielādējāt multivides bibliotēkā, jābūt atgrieztam atbildē.</span><span class="sxs-lookup"><span data-stu-id="1d364-130">The file that you uploaded to the Media library should be returned in the response.</span></span>

<span data-ttu-id="1d364-131">Kad esat validējis vietrādi URL, varat to publicēt.</span><span class="sxs-lookup"><span data-stu-id="1d364-131">After you've validated the URL, you can publish it.</span></span>

1. <span data-ttu-id="1d364-132">Dodieties uz savas vietnes **URL** un atlasiet vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="1d364-132">Go to **URLs** for your site, and select the URL.</span></span>
2. <span data-ttu-id="1d364-133">Komandjoslā atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="1d364-133">Select **Publish** on the command bar.</span></span>

## <a name="update-the-file-that-a-url-points-to"></a><span data-ttu-id="1d364-134">Faila, uz kuru norāda vietrādis URL, atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="1d364-134">Update the file that a URL points to</span></span>

<span data-ttu-id="1d364-135">Kad URL ir publicēts, to var atjaunināt, lai tas norādītu uz citu failu.</span><span class="sxs-lookup"><span data-stu-id="1d364-135">After a URL is published, you can update it so that it points to a different file.</span></span> <span data-ttu-id="1d364-136">Varat arī atjaunināt vietrādi URL, lai tas norādītu uz citu resursa veidu, kā aprakstīts nākamajā sadaļā.</span><span class="sxs-lookup"><span data-stu-id="1d364-136">Alternatively, you can update the URL so that it points to a different the type of resource, as described in the next section.</span></span> <span data-ttu-id="1d364-137">Piemēram, varat norādīt vietrādi URL uz iekšējo lapu vai novirzīt.</span><span class="sxs-lookup"><span data-stu-id="1d364-137">For example, you can point the URL to an internal page or a redirect.</span></span>

<span data-ttu-id="1d364-138">Lai atjauninātu failu, uz kuru norāda vietrādis URL, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="1d364-138">To update the file that a URL points to, follow these steps.</span></span>

1. <span data-ttu-id="1d364-139">Dodieties uz savas vietnes **URL** un atlasiet vietrādi URL, ko atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="1d364-139">Go to **URLs** for your site, and select the URL to update.</span></span>
1. <span data-ttu-id="1d364-140">Rekvizītu rūts labajā pusē atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="1d364-140">In the properties pane on the right, select **Edit**.</span></span>
1. <span data-ttu-id="1d364-141">Sadaļā **Vietrāža URL piešķire** atlasiet lodziņu **2. darbība** un pēc tam atlasiet jaunu dokumentu no multivides bibliotēkas.</span><span class="sxs-lookup"><span data-stu-id="1d364-141">Under **URL assignment**, select the **Step 2** box, and then select a new document from the Media library.</span></span>
1. <span data-ttu-id="1d364-142">Atlasiet **Lietot**.</span><span class="sxs-lookup"><span data-stu-id="1d364-142">Select **Apply**.</span></span>

## <a name="update-the-asset-type-that-a-url-points-to"></a><span data-ttu-id="1d364-143">Līdzekļa veida, uz kuru norāda vietrādis URL, atjaunināšana</span><span class="sxs-lookup"><span data-stu-id="1d364-143">Update the asset type that a URL points to</span></span>

<span data-ttu-id="1d364-144">Varat arī atjaunināt vietrādi URL, lai tas norādītu uz citu līdzekļa veidu (resursu), piemēram, iekšējo lapu vai novirzīšanu.</span><span class="sxs-lookup"><span data-stu-id="1d364-144">You can also update a URL so that it points to a different type of asset (resource), such as an internal page or a redirect.</span></span>

<span data-ttu-id="1d364-145">Lai atjauninātu līdzekļa veidu, uz kuru norāda vietrādis URL, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="1d364-145">To update the asset type that a URL points to, follow these steps.</span></span>

1. <span data-ttu-id="1d364-146">Dodieties uz savas vietnes **URL** un atlasiet vietrādi URL, ko atjaunināt.</span><span class="sxs-lookup"><span data-stu-id="1d364-146">Go to **URLs** for your site, and select the URL to update.</span></span>
1. <span data-ttu-id="1d364-147">Rekvizītu rūts labajā pusē atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="1d364-147">In the properties pane on the right, select **Edit**.</span></span>
1. <span data-ttu-id="1d364-148">Sadaļā **Vietrāža URL piešķire** zem **1. darbība** atlasiet citu līdzekļa veidu.</span><span class="sxs-lookup"><span data-stu-id="1d364-148">Under **URL assignment**, under **Step 1**, select a different asset type.</span></span>
1. <span data-ttu-id="1d364-149">Atlasiet lodziņu **2. darbība** un pēc tam atlasiet jauno līdzekli.</span><span class="sxs-lookup"><span data-stu-id="1d364-149">Select the **Step 2** box, and then select the new asset.</span></span>
1. <span data-ttu-id="1d364-150">Atlasiet **Lietot**.</span><span class="sxs-lookup"><span data-stu-id="1d364-150">Select **Apply**.</span></span>

## <a name="change-the-url-path"></a><span data-ttu-id="1d364-151">Vietrāža URL ceļa mainīšana</span><span class="sxs-lookup"><span data-stu-id="1d364-151">Change the URL path</span></span>

<span data-ttu-id="1d364-152">Kad URL ir izveidots, tā ceļu nevar mainīt.</span><span class="sxs-lookup"><span data-stu-id="1d364-152">After a URL is created, its path can't be changed.</span></span> <span data-ttu-id="1d364-153">Ja jāmaina vietrāža URL ceļš, kas kalpo failam vai kādam citam resursa veidam, ir jāizveido jauns vietrādis URL, jākartē tas uz esošo failu vai citu resursu un pēc tam jānoņem un jādzēš vecais vietrādis URL.</span><span class="sxs-lookup"><span data-stu-id="1d364-153">If you must change the URL path that serves a file or any other type of resource, you have to create a new URL, map it to the existing file or other resource, and then unpublish and delete the old URL.</span></span>

<span data-ttu-id="1d364-154">Lai mainītu vietrāža URL ceļu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="1d364-154">To change the URL path, follow these steps.</span></span>

1. <span data-ttu-id="1d364-155">Lai izveidotu jaunu vietrādi URL un kartētu to uz esošo failu vai citu resursu, izpildiet norādes sadaļā [Izveidot vietnes vietrādi URL, kas atgriež statisku failu](#create-a-site-url-that-returns-a-static-file) iepriekš šajā tēmā.</span><span class="sxs-lookup"><span data-stu-id="1d364-155">To create a new URL and map it to the existing file or another resource, follow the instructions in the [Create a site URL that returns a static file](#create-a-site-url-that-returns-a-static-file) section earlier in this topic.</span></span>
1. <span data-ttu-id="1d364-156">Atlasiet jauno vietrādi URL un komandjoslā atlasiet **Publicēt**.</span><span class="sxs-lookup"><span data-stu-id="1d364-156">Select the new URL, and select **Publish** on the command bar.</span></span> <span data-ttu-id="1d364-157">Jaunais vietrādis URL ir publicēts.</span><span class="sxs-lookup"><span data-stu-id="1d364-157">The new URL is published.</span></span>
1. <span data-ttu-id="1d364-158">Lai noņemtu veco vietrādi URL, atlasiet to un pēc tam komandjoslā atlasiet **Atsaukt publicēšanu**.</span><span class="sxs-lookup"><span data-stu-id="1d364-158">To unpublish the old URL, select it, and then select **Unpublish** on the command bar.</span></span> <span data-ttu-id="1d364-159">Ja vēlaties, tagad varat dzēst veco vietrādi URL.</span><span class="sxs-lookup"><span data-stu-id="1d364-159">You can now delete the old URL if you want.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1d364-160">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="1d364-160">Additional resources</span></span>

[<span data-ttu-id="1d364-161">Pārskats par digitālo līdzekļu pārvaldību</span><span class="sxs-lookup"><span data-stu-id="1d364-161">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="1d364-162">Attēlu augšupielāde</span><span class="sxs-lookup"><span data-stu-id="1d364-162">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="1d364-163">Augšupielādēt videoklipus</span><span class="sxs-lookup"><span data-stu-id="1d364-163">Upload videos</span></span>](dam-upload-video.md)

[<span data-ttu-id="1d364-164">Failu, kas nav attēli un videoklipi, augšupielāde</span><span class="sxs-lookup"><span data-stu-id="1d364-164">Upload files other than images and videos</span></span>](dam-upload-files.md)

[<span data-ttu-id="1d364-165">Attēlu apgriešana</span><span class="sxs-lookup"><span data-stu-id="1d364-165">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="1d364-166">Attēlu fokusa punktu pielāgošana</span><span class="sxs-lookup"><span data-stu-id="1d364-166">Customize image focal points</span></span>](dam-custom-focal-point.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]