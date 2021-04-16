---
title: Augšupielādēt failus, kas nav attēli un video
description: Šajā tēmā aprakstīts, kā augšupielādēt bināros failus, kas nav attēli un video, risinājuma Microsoft Dynamics 365 Commerce vietnes veidotājā.
author: psimolin
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 380bcccd1053cbcc276e964ce97f16d1d39ea75a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799257"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="ac8f9-103">Failu, kas nav attēli un videoklipi, augšupielāde</span><span class="sxs-lookup"><span data-stu-id="ac8f9-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ac8f9-104">Šajā tēmā aprakstīts, kā augšupielādēt failus, kas nav attēli un video, risinājuma Microsoft Dynamics 365 Commerce vietnes veidotājā.</span><span class="sxs-lookup"><span data-stu-id="ac8f9-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="ac8f9-105">Commerce vietnes veidotāja multivides bibliotēka atbalsta jebkādu bināro līdzekļu augšupielādi, kas nav attēli vai videoklipi.</span><span class="sxs-lookup"><span data-stu-id="ac8f9-105">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="ac8f9-106">Piemēram, jūs varētu vēlēties augšupielādēt Microsoft Excel, Microsoft Word, Microsoft PowerPoint vai PDF failus.</span><span class="sxs-lookup"><span data-stu-id="ac8f9-106">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="ac8f9-107">Tiek atbalstīti šādi dokumentu veidi:</span><span class="sxs-lookup"><span data-stu-id="ac8f9-107">The following document types are supported:</span></span>
- <span data-ttu-id="ac8f9-108">7Z</span><span class="sxs-lookup"><span data-stu-id="ac8f9-108">7Z</span></span>
- <span data-ttu-id="ac8f9-109">AVI</span><span class="sxs-lookup"><span data-stu-id="ac8f9-109">AVI</span></span>
- <span data-ttu-id="ac8f9-110">CS</span><span class="sxs-lookup"><span data-stu-id="ac8f9-110">CS</span></span>
- <span data-ttu-id="ac8f9-111">CSS</span><span class="sxs-lookup"><span data-stu-id="ac8f9-111">CSS</span></span>
- <span data-ttu-id="ac8f9-112">DOC</span><span class="sxs-lookup"><span data-stu-id="ac8f9-112">DOC</span></span>
- <span data-ttu-id="ac8f9-113">DOCX</span><span class="sxs-lookup"><span data-stu-id="ac8f9-113">DOCX</span></span>
- <span data-ttu-id="ac8f9-114">EPUB</span><span class="sxs-lookup"><span data-stu-id="ac8f9-114">EPUB</span></span>
- <span data-ttu-id="ac8f9-115">GIF</span><span class="sxs-lookup"><span data-stu-id="ac8f9-115">GIF</span></span>
- <span data-ttu-id="ac8f9-116">INDD</span><span class="sxs-lookup"><span data-stu-id="ac8f9-116">INDD</span></span>
- <span data-ttu-id="ac8f9-117">JAR</span><span class="sxs-lookup"><span data-stu-id="ac8f9-117">JAR</span></span>
- <span data-ttu-id="ac8f9-118">JPG</span><span class="sxs-lookup"><span data-stu-id="ac8f9-118">JPG</span></span>
- <span data-ttu-id="ac8f9-119">JPEG</span><span class="sxs-lookup"><span data-stu-id="ac8f9-119">JPEG</span></span>
- <span data-ttu-id="ac8f9-120">JS</span><span class="sxs-lookup"><span data-stu-id="ac8f9-120">JS</span></span>
- <span data-ttu-id="ac8f9-121">MP3</span><span class="sxs-lookup"><span data-stu-id="ac8f9-121">MP3</span></span>
- <span data-ttu-id="ac8f9-122">MP4</span><span class="sxs-lookup"><span data-stu-id="ac8f9-122">MP4</span></span>
- <span data-ttu-id="ac8f9-123">MPEG</span><span class="sxs-lookup"><span data-stu-id="ac8f9-123">MPEG</span></span>
- <span data-ttu-id="ac8f9-124">MPG</span><span class="sxs-lookup"><span data-stu-id="ac8f9-124">MPG</span></span>
- <span data-ttu-id="ac8f9-125">ODP</span><span class="sxs-lookup"><span data-stu-id="ac8f9-125">ODP</span></span>
- <span data-ttu-id="ac8f9-126">ODS</span><span class="sxs-lookup"><span data-stu-id="ac8f9-126">ODS</span></span>
- <span data-ttu-id="ac8f9-127">ODT</span><span class="sxs-lookup"><span data-stu-id="ac8f9-127">ODT</span></span>
- <span data-ttu-id="ac8f9-128">PDF</span><span class="sxs-lookup"><span data-stu-id="ac8f9-128">PDF</span></span>
- <span data-ttu-id="ac8f9-129">PNG</span><span class="sxs-lookup"><span data-stu-id="ac8f9-129">PNG</span></span>
- <span data-ttu-id="ac8f9-130">PPT</span><span class="sxs-lookup"><span data-stu-id="ac8f9-130">PPT</span></span>
- <span data-ttu-id="ac8f9-131">PPTX</span><span class="sxs-lookup"><span data-stu-id="ac8f9-131">PPTX</span></span>
- <span data-ttu-id="ac8f9-132">PS</span><span class="sxs-lookup"><span data-stu-id="ac8f9-132">PS</span></span>
- <span data-ttu-id="ac8f9-133">QXP</span><span class="sxs-lookup"><span data-stu-id="ac8f9-133">QXP</span></span>
- <span data-ttu-id="ac8f9-134">RAR</span><span class="sxs-lookup"><span data-stu-id="ac8f9-134">RAR</span></span>
- <span data-ttu-id="ac8f9-135">RTF</span><span class="sxs-lookup"><span data-stu-id="ac8f9-135">RTF</span></span>
- <span data-ttu-id="ac8f9-136">SVG</span><span class="sxs-lookup"><span data-stu-id="ac8f9-136">SVG</span></span>
- <span data-ttu-id="ac8f9-137">TAR</span><span class="sxs-lookup"><span data-stu-id="ac8f9-137">TAR</span></span>
- <span data-ttu-id="ac8f9-138">TGZ</span><span class="sxs-lookup"><span data-stu-id="ac8f9-138">TGZ</span></span>
- <span data-ttu-id="ac8f9-139">TXT</span><span class="sxs-lookup"><span data-stu-id="ac8f9-139">TXT</span></span>
- <span data-ttu-id="ac8f9-140">WMV</span><span class="sxs-lookup"><span data-stu-id="ac8f9-140">WMV</span></span>
- <span data-ttu-id="ac8f9-141">XLS</span><span class="sxs-lookup"><span data-stu-id="ac8f9-141">XLS</span></span>
- <span data-ttu-id="ac8f9-142">XLSX</span><span class="sxs-lookup"><span data-stu-id="ac8f9-142">XLSX</span></span>
- <span data-ttu-id="ac8f9-143">XML</span><span class="sxs-lookup"><span data-stu-id="ac8f9-143">XML</span></span>
- <span data-ttu-id="ac8f9-144">ZIP</span><span class="sxs-lookup"><span data-stu-id="ac8f9-144">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="ac8f9-145">Augšupielādēt failu</span><span class="sxs-lookup"><span data-stu-id="ac8f9-145">Upload a file</span></span>

<span data-ttu-id="ac8f9-146">Lai Commerce vietnes veidotāju augšupielādētu failu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="ac8f9-146">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="ac8f9-147">Kreisās puses navigācijas rūtī atlasiet **Mediju bibliotēka**.</span><span class="sxs-lookup"><span data-stu-id="ac8f9-147">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="ac8f9-148">Komandu joslā atlasiet **Augšupielādēt \> Augšupielādēt mediju vienumus**.</span><span class="sxs-lookup"><span data-stu-id="ac8f9-148">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="ac8f9-149">Failu pārlūkā atlasiet vienu vai vairākus failus un pēc tam atlasiet **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="ac8f9-149">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="ac8f9-150">Dialoglodziņā **Augšupielādēt multivides vienumu** pēc nepieciešamības ievadiet nosaukumu, aprakstu un atslēgvārdu metadatus.</span><span class="sxs-lookup"><span data-stu-id="ac8f9-150">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="ac8f9-151">Lai publicētu failus tūlīt pēc augšupielādes, atzīmējiet izvēles rūtiņu **Publicēt multivides vienumus pēc augšupielādes**.</span><span class="sxs-lookup"><span data-stu-id="ac8f9-151">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="ac8f9-152">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="ac8f9-152">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ac8f9-153">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="ac8f9-153">Additional resources</span></span>

[<span data-ttu-id="ac8f9-154">Digitālo līdzekļu pārvaldības pārskats</span><span class="sxs-lookup"><span data-stu-id="ac8f9-154">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="ac8f9-155">Attēlu augšupielāde</span><span class="sxs-lookup"><span data-stu-id="ac8f9-155">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="ac8f9-156">Videoklipu augšupielāde</span><span class="sxs-lookup"><span data-stu-id="ac8f9-156">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="ac8f9-157">Attēlu apgriešana</span><span class="sxs-lookup"><span data-stu-id="ac8f9-157">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="ac8f9-158">Attēlu fokusa punktu pielāgošana</span><span class="sxs-lookup"><span data-stu-id="ac8f9-158">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="ac8f9-159">Augšupielādēt un apkalpot statiskos failus</span><span class="sxs-lookup"><span data-stu-id="ac8f9-159">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
