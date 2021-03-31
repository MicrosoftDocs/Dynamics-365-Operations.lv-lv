---
title: Augšupielādēt failus, kas nav attēli un video
description: Šajā tēmā aprakstīts, kā augšupielādēt bināros failus, kas nav attēli un video, risinājuma Microsoft Dynamics 365 Commerce vietnes veidotājā.
author: psimolin
manager: annbe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.openlocfilehash: c065aa961cf5c2d6770ae47c63a75953e6d38e00
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222541"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="69133-103">Failu, kas nav attēli un videoklipi, augšupielāde</span><span class="sxs-lookup"><span data-stu-id="69133-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="69133-104">Šajā tēmā aprakstīts, kā augšupielādēt failus, kas nav attēli un video, risinājuma Microsoft Dynamics 365 Commerce vietnes veidotājā.</span><span class="sxs-lookup"><span data-stu-id="69133-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="69133-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="69133-105">Overview</span></span>

<span data-ttu-id="69133-106">Commerce vietnes veidotāja multivides bibliotēka atbalsta jebkādu bināro līdzekļu augšupielādi, kas nav attēli vai videoklipi.</span><span class="sxs-lookup"><span data-stu-id="69133-106">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="69133-107">Piemēram, jūs varētu vēlēties augšupielādēt Microsoft Excel, Microsoft Word, Microsoft PowerPoint vai PDF failus.</span><span class="sxs-lookup"><span data-stu-id="69133-107">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="69133-108">Tiek atbalstīti šādi dokumentu veidi:</span><span class="sxs-lookup"><span data-stu-id="69133-108">The following document types are supported:</span></span>
- <span data-ttu-id="69133-109">7Z</span><span class="sxs-lookup"><span data-stu-id="69133-109">7Z</span></span>
- <span data-ttu-id="69133-110">AVI</span><span class="sxs-lookup"><span data-stu-id="69133-110">AVI</span></span>
- <span data-ttu-id="69133-111">CS</span><span class="sxs-lookup"><span data-stu-id="69133-111">CS</span></span>
- <span data-ttu-id="69133-112">CSS</span><span class="sxs-lookup"><span data-stu-id="69133-112">CSS</span></span>
- <span data-ttu-id="69133-113">DOC</span><span class="sxs-lookup"><span data-stu-id="69133-113">DOC</span></span>
- <span data-ttu-id="69133-114">DOCX</span><span class="sxs-lookup"><span data-stu-id="69133-114">DOCX</span></span>
- <span data-ttu-id="69133-115">EPUB</span><span class="sxs-lookup"><span data-stu-id="69133-115">EPUB</span></span>
- <span data-ttu-id="69133-116">GIF</span><span class="sxs-lookup"><span data-stu-id="69133-116">GIF</span></span>
- <span data-ttu-id="69133-117">INDD</span><span class="sxs-lookup"><span data-stu-id="69133-117">INDD</span></span>
- <span data-ttu-id="69133-118">JAR</span><span class="sxs-lookup"><span data-stu-id="69133-118">JAR</span></span>
- <span data-ttu-id="69133-119">JPG</span><span class="sxs-lookup"><span data-stu-id="69133-119">JPG</span></span>
- <span data-ttu-id="69133-120">JPEG</span><span class="sxs-lookup"><span data-stu-id="69133-120">JPEG</span></span>
- <span data-ttu-id="69133-121">JS</span><span class="sxs-lookup"><span data-stu-id="69133-121">JS</span></span>
- <span data-ttu-id="69133-122">MP3</span><span class="sxs-lookup"><span data-stu-id="69133-122">MP3</span></span>
- <span data-ttu-id="69133-123">MP4</span><span class="sxs-lookup"><span data-stu-id="69133-123">MP4</span></span>
- <span data-ttu-id="69133-124">MPEG</span><span class="sxs-lookup"><span data-stu-id="69133-124">MPEG</span></span>
- <span data-ttu-id="69133-125">MPG</span><span class="sxs-lookup"><span data-stu-id="69133-125">MPG</span></span>
- <span data-ttu-id="69133-126">ODP</span><span class="sxs-lookup"><span data-stu-id="69133-126">ODP</span></span>
- <span data-ttu-id="69133-127">ODS</span><span class="sxs-lookup"><span data-stu-id="69133-127">ODS</span></span>
- <span data-ttu-id="69133-128">ODT</span><span class="sxs-lookup"><span data-stu-id="69133-128">ODT</span></span>
- <span data-ttu-id="69133-129">PDF</span><span class="sxs-lookup"><span data-stu-id="69133-129">PDF</span></span>
- <span data-ttu-id="69133-130">PNG</span><span class="sxs-lookup"><span data-stu-id="69133-130">PNG</span></span>
- <span data-ttu-id="69133-131">PPT</span><span class="sxs-lookup"><span data-stu-id="69133-131">PPT</span></span>
- <span data-ttu-id="69133-132">PPTX</span><span class="sxs-lookup"><span data-stu-id="69133-132">PPTX</span></span>
- <span data-ttu-id="69133-133">PS</span><span class="sxs-lookup"><span data-stu-id="69133-133">PS</span></span>
- <span data-ttu-id="69133-134">QXP</span><span class="sxs-lookup"><span data-stu-id="69133-134">QXP</span></span>
- <span data-ttu-id="69133-135">RAR</span><span class="sxs-lookup"><span data-stu-id="69133-135">RAR</span></span>
- <span data-ttu-id="69133-136">RTF</span><span class="sxs-lookup"><span data-stu-id="69133-136">RTF</span></span>
- <span data-ttu-id="69133-137">SVG</span><span class="sxs-lookup"><span data-stu-id="69133-137">SVG</span></span>
- <span data-ttu-id="69133-138">TAR</span><span class="sxs-lookup"><span data-stu-id="69133-138">TAR</span></span>
- <span data-ttu-id="69133-139">TGZ</span><span class="sxs-lookup"><span data-stu-id="69133-139">TGZ</span></span>
- <span data-ttu-id="69133-140">TXT</span><span class="sxs-lookup"><span data-stu-id="69133-140">TXT</span></span>
- <span data-ttu-id="69133-141">WMV</span><span class="sxs-lookup"><span data-stu-id="69133-141">WMV</span></span>
- <span data-ttu-id="69133-142">XLS</span><span class="sxs-lookup"><span data-stu-id="69133-142">XLS</span></span>
- <span data-ttu-id="69133-143">XLSX</span><span class="sxs-lookup"><span data-stu-id="69133-143">XLSX</span></span>
- <span data-ttu-id="69133-144">XML</span><span class="sxs-lookup"><span data-stu-id="69133-144">XML</span></span>
- <span data-ttu-id="69133-145">ZIP</span><span class="sxs-lookup"><span data-stu-id="69133-145">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="69133-146">Augšupielādēt failu</span><span class="sxs-lookup"><span data-stu-id="69133-146">Upload a file</span></span>

<span data-ttu-id="69133-147">Lai Commerce vietnes veidotāju augšupielādētu failu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="69133-147">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="69133-148">Kreisās puses navigācijas rūtī atlasiet **Mediju bibliotēka**.</span><span class="sxs-lookup"><span data-stu-id="69133-148">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="69133-149">Komandu joslā atlasiet **Augšupielādēt \> Augšupielādēt mediju vienumus**.</span><span class="sxs-lookup"><span data-stu-id="69133-149">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="69133-150">Failu pārlūkā atlasiet vienu vai vairākus failus un pēc tam atlasiet **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="69133-150">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="69133-151">Dialoglodziņā **Augšupielādēt multivides vienumu** pēc nepieciešamības ievadiet nosaukumu, aprakstu un atslēgvārdu metadatus.</span><span class="sxs-lookup"><span data-stu-id="69133-151">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="69133-152">Lai publicētu failus tūlīt pēc augšupielādes, atzīmējiet izvēles rūtiņu **Publicēt multivides vienumus pēc augšupielādes**.</span><span class="sxs-lookup"><span data-stu-id="69133-152">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="69133-153">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="69133-153">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="69133-154">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="69133-154">Additional resources</span></span>

[<span data-ttu-id="69133-155">Digitālo līdzekļu pārvaldības pārskats</span><span class="sxs-lookup"><span data-stu-id="69133-155">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="69133-156">Attēlu augšupielāde</span><span class="sxs-lookup"><span data-stu-id="69133-156">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="69133-157">Videoklipu augšupielāde</span><span class="sxs-lookup"><span data-stu-id="69133-157">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="69133-158">Attēlu apgriešana</span><span class="sxs-lookup"><span data-stu-id="69133-158">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="69133-159">Attēlu fokusa punktu pielāgošana</span><span class="sxs-lookup"><span data-stu-id="69133-159">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="69133-160">Augšupielādēt un apkalpot statiskos failus</span><span class="sxs-lookup"><span data-stu-id="69133-160">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]