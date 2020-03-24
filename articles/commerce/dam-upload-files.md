---
title: Augšupielādēt failus, kas nav attēli un video
description: Šajā tēmā ir aprakstīts, kā Microsoft Dynamics 365 Commerce vietnes veidotājā var augšupielādēt bināros failus, kas nav attēli un videoklipi.
author: psimolin
manager: annbe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: fc0490e3532dcbb9c1e91101009b2d4605315416
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/03/2020
ms.locfileid: "3097048"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="44cec-103">Augšupielādēt failus, kas nav attēli un video</span><span class="sxs-lookup"><span data-stu-id="44cec-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="44cec-104">Šajā tēmā ir aprakstīts, kā Microsoft Dynamics 365 Commerce vietnes veidotājā var augšupielādēt failus, kas nav attēli un videoklipi.</span><span class="sxs-lookup"><span data-stu-id="44cec-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="44cec-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="44cec-105">Overview</span></span>

<span data-ttu-id="44cec-106">Commerce vietnes veidotāja multivides bibliotēka atbalsta jebkādu bināro līdzekļu augšupielādi, kas nav attēli vai videoklipi.</span><span class="sxs-lookup"><span data-stu-id="44cec-106">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="44cec-107">Piemēram, jūs varētu vēlēties augšupielādēt Microsoft Excel, Microsoft Word, Microsoft PowerPoint vai PDF failus.</span><span class="sxs-lookup"><span data-stu-id="44cec-107">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="44cec-108">Tiek atbalstīti šādi dokumentu veidi:</span><span class="sxs-lookup"><span data-stu-id="44cec-108">The following document types are supported:</span></span>
- <span data-ttu-id="44cec-109">7Z</span><span class="sxs-lookup"><span data-stu-id="44cec-109">7Z</span></span>
- <span data-ttu-id="44cec-110">AVI</span><span class="sxs-lookup"><span data-stu-id="44cec-110">AVI</span></span>
- <span data-ttu-id="44cec-111">CS</span><span class="sxs-lookup"><span data-stu-id="44cec-111">CS</span></span>
- <span data-ttu-id="44cec-112">CSS</span><span class="sxs-lookup"><span data-stu-id="44cec-112">CSS</span></span>
- <span data-ttu-id="44cec-113">DOC</span><span class="sxs-lookup"><span data-stu-id="44cec-113">DOC</span></span>
- <span data-ttu-id="44cec-114">DOCX</span><span class="sxs-lookup"><span data-stu-id="44cec-114">DOCX</span></span>
- <span data-ttu-id="44cec-115">EPUB</span><span class="sxs-lookup"><span data-stu-id="44cec-115">EPUB</span></span>
- <span data-ttu-id="44cec-116">GIF</span><span class="sxs-lookup"><span data-stu-id="44cec-116">GIF</span></span>
- <span data-ttu-id="44cec-117">INDD</span><span class="sxs-lookup"><span data-stu-id="44cec-117">INDD</span></span>
- <span data-ttu-id="44cec-118">JAR</span><span class="sxs-lookup"><span data-stu-id="44cec-118">JAR</span></span>
- <span data-ttu-id="44cec-119">JPG</span><span class="sxs-lookup"><span data-stu-id="44cec-119">JPG</span></span>
- <span data-ttu-id="44cec-120">JPEG</span><span class="sxs-lookup"><span data-stu-id="44cec-120">JPEG</span></span>
- <span data-ttu-id="44cec-121">JS</span><span class="sxs-lookup"><span data-stu-id="44cec-121">JS</span></span>
- <span data-ttu-id="44cec-122">MP3</span><span class="sxs-lookup"><span data-stu-id="44cec-122">MP3</span></span>
- <span data-ttu-id="44cec-123">MP4</span><span class="sxs-lookup"><span data-stu-id="44cec-123">MP4</span></span>
- <span data-ttu-id="44cec-124">MPEG</span><span class="sxs-lookup"><span data-stu-id="44cec-124">MPEG</span></span>
- <span data-ttu-id="44cec-125">MPG</span><span class="sxs-lookup"><span data-stu-id="44cec-125">MPG</span></span>
- <span data-ttu-id="44cec-126">ODP</span><span class="sxs-lookup"><span data-stu-id="44cec-126">ODP</span></span>
- <span data-ttu-id="44cec-127">ODS</span><span class="sxs-lookup"><span data-stu-id="44cec-127">ODS</span></span>
- <span data-ttu-id="44cec-128">ODT</span><span class="sxs-lookup"><span data-stu-id="44cec-128">ODT</span></span>
- <span data-ttu-id="44cec-129">PDF</span><span class="sxs-lookup"><span data-stu-id="44cec-129">PDF</span></span>
- <span data-ttu-id="44cec-130">PNG</span><span class="sxs-lookup"><span data-stu-id="44cec-130">PNG</span></span>
- <span data-ttu-id="44cec-131">PPT</span><span class="sxs-lookup"><span data-stu-id="44cec-131">PPT</span></span>
- <span data-ttu-id="44cec-132">PPTX</span><span class="sxs-lookup"><span data-stu-id="44cec-132">PPTX</span></span>
- <span data-ttu-id="44cec-133">PS</span><span class="sxs-lookup"><span data-stu-id="44cec-133">PS</span></span>
- <span data-ttu-id="44cec-134">QXP</span><span class="sxs-lookup"><span data-stu-id="44cec-134">QXP</span></span>
- <span data-ttu-id="44cec-135">RAR</span><span class="sxs-lookup"><span data-stu-id="44cec-135">RAR</span></span>
- <span data-ttu-id="44cec-136">RTF</span><span class="sxs-lookup"><span data-stu-id="44cec-136">RTF</span></span>
- <span data-ttu-id="44cec-137">SVG</span><span class="sxs-lookup"><span data-stu-id="44cec-137">SVG</span></span>
- <span data-ttu-id="44cec-138">TAR</span><span class="sxs-lookup"><span data-stu-id="44cec-138">TAR</span></span>
- <span data-ttu-id="44cec-139">TGZ</span><span class="sxs-lookup"><span data-stu-id="44cec-139">TGZ</span></span>
- <span data-ttu-id="44cec-140">TXT</span><span class="sxs-lookup"><span data-stu-id="44cec-140">TXT</span></span>
- <span data-ttu-id="44cec-141">WMV</span><span class="sxs-lookup"><span data-stu-id="44cec-141">WMV</span></span>
- <span data-ttu-id="44cec-142">XLS</span><span class="sxs-lookup"><span data-stu-id="44cec-142">XLS</span></span>
- <span data-ttu-id="44cec-143">XLSX</span><span class="sxs-lookup"><span data-stu-id="44cec-143">XLSX</span></span>
- <span data-ttu-id="44cec-144">XML</span><span class="sxs-lookup"><span data-stu-id="44cec-144">XML</span></span>
- <span data-ttu-id="44cec-145">ZIP</span><span class="sxs-lookup"><span data-stu-id="44cec-145">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="44cec-146">Augšupielādēt failu</span><span class="sxs-lookup"><span data-stu-id="44cec-146">Upload a file</span></span>

<span data-ttu-id="44cec-147">Lai Commerce vietnes veidotāju augšupielādētu failu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="44cec-147">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="44cec-148">Kreisās puses navigācijas rūtī atlasiet **Mediju bibliotēka**.</span><span class="sxs-lookup"><span data-stu-id="44cec-148">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="44cec-149">Komandu joslā atlasiet **Augšupielādēt \>Augšupielādēt mediju vienumus**.</span><span class="sxs-lookup"><span data-stu-id="44cec-149">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="44cec-150">Failu pārlūkā atlasiet vienu vai vairākus failus un pēc tam atlasiet **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="44cec-150">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="44cec-151">Dialoglodziņā **Augšupielādēt multivides vienumu** pēc nepieciešamības ievadiet nosaukumu, aprakstu un atslēgvārdu metadatus.</span><span class="sxs-lookup"><span data-stu-id="44cec-151">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="44cec-152">Lai publicētu failus tūlīt pēc augšupielādes, atzīmējiet izvēles rūtiņu **Publicēt multivides vienumus pēc augšupielādes**.</span><span class="sxs-lookup"><span data-stu-id="44cec-152">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="44cec-153">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="44cec-153">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="44cec-154">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="44cec-154">Additional resources</span></span>

[<span data-ttu-id="44cec-155">Digitālo līdzekļu pārvaldības pārskats</span><span class="sxs-lookup"><span data-stu-id="44cec-155">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="44cec-156">Augšupielādēt attēlus</span><span class="sxs-lookup"><span data-stu-id="44cec-156">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="44cec-157">Augšupielādēt video</span><span class="sxs-lookup"><span data-stu-id="44cec-157">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="44cec-158">Apgriezt attēlus</span><span class="sxs-lookup"><span data-stu-id="44cec-158">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="44cec-159">Attēlu fokusa punktu pielāgošana</span><span class="sxs-lookup"><span data-stu-id="44cec-159">Customize image focal points</span></span>](dam-custom-focal-point.md)
