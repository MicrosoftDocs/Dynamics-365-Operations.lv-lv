---
title: Augšupielādēt attēlus
description: Šajā tēmā ir aprakstīts, kā augšupielādēt attēlus programmas Microsoft Dynamics 365 Commerce vietnes veidotājā.
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
ms.openlocfilehash: f562d3376fde6a24e6a1e1a3f7f4192cf290ae90
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594288"
---
# <a name="upload-images"></a><span data-ttu-id="e6df7-103">Augšupielādēt attēlus</span><span class="sxs-lookup"><span data-stu-id="e6df7-103">Upload images</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e6df7-104">Šajā tēmā ir aprakstīts, kā augšupielādēt attēlus programmas Microsoft Dynamics 365 Commerce vietnes veidotājā.</span><span class="sxs-lookup"><span data-stu-id="e6df7-104">This topic describes how to upload images in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="e6df7-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="e6df7-105">Overview</span></span>

<span data-ttu-id="e6df7-106">Commerce vietnes veidotāja multivides bibliotēka ļauj augšupielādēt attēlus vai nu atsevišķi, vai lielapjomā, izmantojot mapes.</span><span class="sxs-lookup"><span data-stu-id="e6df7-106">The Commerce site builder Media Library allows you to upload images, either singly or in bulk using folders.</span></span> <span data-ttu-id="e6df7-107">Vienmēr augšupielādējiet attēla versiju ar augstāko izšķirtspēju un kvalitāti, jo attēla izmēra maiņas komponents automātiski optimizēs attēlu atšķirīgām skatvietām un to pārtraukumpunktiem.</span><span class="sxs-lookup"><span data-stu-id="e6df7-107">You should always upload the version of the image with highest resolution and quality, because the image resizer component will automatically optimize the image for different viewports and their breakpoints.</span></span>

### <a name="image-information-specified-during-upload"></a><span data-ttu-id="e6df7-108">Augšupielādes laikā norādītā attēla informācija</span><span class="sxs-lookup"><span data-stu-id="e6df7-108">Image information specified during upload</span></span>

<span data-ttu-id="e6df7-109">Augšupielādējot attēlu, var norādīt šādu informāciju.</span><span class="sxs-lookup"><span data-stu-id="e6df7-109">When uploading an image, the following information can be specified.</span></span>

- <span data-ttu-id="e6df7-110">**Virsraksts, alternatīvais teksts, apraksts, atslēgvārdi**: attēla vai attēlu metadati.</span><span class="sxs-lookup"><span data-stu-id="e6df7-110">**Title, Alt Text, Description, Keywords**: Metadata of the image or images.</span></span> <span data-ttu-id="e6df7-111">Nosaukums un alternatīvais teksts ir obligāta vērtības.</span><span class="sxs-lookup"><span data-stu-id="e6df7-111">Title and alt text are required values.</span></span>
- <span data-ttu-id="e6df7-112">**Atlasīt kategoriju**:</span><span class="sxs-lookup"><span data-stu-id="e6df7-112">**Select category**:</span></span>
    - <span data-ttu-id="e6df7-113">**Nav**: izmanto e-komercijas stāstu attēlam vai attēliem.</span><span class="sxs-lookup"><span data-stu-id="e6df7-113">**None**: Used for an e-Commerce storytelling image or images.</span></span>
    - <span data-ttu-id="e6df7-114">**Prece, kategorija, klients, darbinieks, katalogs**: izmanto Dynamics 365 Commerce daudzkanālu attēlu vai attēlus.</span><span class="sxs-lookup"><span data-stu-id="e6df7-114">**Product, Category, Customer, Employee, Catalog**: Used for Dynamics 365 Commerce omni-channel image or images.</span></span>
- <span data-ttu-id="e6df7-115">**Publicēt līdzekļus pēc augšupielādes**: kad šī izvēles rūtiņa ir atzīmēta, attēls vai attēli tiek publicēti uzreiz pēc augšupielādes.</span><span class="sxs-lookup"><span data-stu-id="e6df7-115">**Publish assets after upload**: When this check box is selected, the image or images are published immediately after upload.</span></span>

> [!NOTE]
> <span data-ttu-id="e6df7-116">Attēlu līdzekļi ar piešķirtu kategoriju tiek arī automātiski atzīmēti ar kategoriju kā atslēgvārdu, lai palīdzētu meklēt konkrētas kategorijas līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="e6df7-116">Image assets with a category assigned are also automatically tagged with the category as a keyword to aid searching for assets of a specific category.</span></span>

### <a name="naming-conventions-for-omni-channel-images"></a><span data-ttu-id="e6df7-117">Nosaukšanas nosacījumi daudzkanālu attēliem</span><span class="sxs-lookup"><span data-stu-id="e6df7-117">Naming conventions for omni-channel images</span></span> 

<span data-ttu-id="e6df7-118">Ja multivides bibliotēka ir konfigurēta kā daudzkanālu attēlu aizmugursistēma, varat izmantot attēlu kategorijas, lai norādītu, kurai kategorijai augšupielādētais attēls pieder.</span><span class="sxs-lookup"><span data-stu-id="e6df7-118">If you have configured the Media Library as the omni-channel image backend, you can use image categories to indicate which category the uploaded image belongs to.</span></span> <span data-ttu-id="e6df7-119">Ir arī nosaukšanas nosacījumi, kas jāievēro, lai nodrošinātu, ka attēli tiek pareizi izgūti citos kanālos, piemēram, pārdošanas punktā (POS).</span><span class="sxs-lookup"><span data-stu-id="e6df7-119">There is also a naming convention that should be followed to ensure that images are retrieved correctly by other channels, such as point of sale (POS).</span></span>

<span data-ttu-id="e6df7-120">Noklusējuma nosaukšanas nosacījumi atšķiras atkarībā no kategorijas:</span><span class="sxs-lookup"><span data-stu-id="e6df7-120">The default naming convention varies based on the category:</span></span>
- <span data-ttu-id="e6df7-121">Kataloga attēliem ir jābūt ar nosaukumu "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"</span><span class="sxs-lookup"><span data-stu-id="e6df7-121">Catalog images should be named "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"</span></span>
- <span data-ttu-id="e6df7-122">Kategorijas attēliem ir jābūt ar nosaukumu "**/Categories/\{CategoryName\}.png**"</span><span class="sxs-lookup"><span data-stu-id="e6df7-122">Category images should be named "**/Categories/\{CategoryName\}.png**"</span></span>
- <span data-ttu-id="e6df7-123">Klientu attēliem ir jābūt ar nosaukumu "**/Customers/\{CustomerNumber\}.jpg**"</span><span class="sxs-lookup"><span data-stu-id="e6df7-123">Customer images should be named "**/Customers/\{CustomerNumber\}.jpg**"</span></span>
- <span data-ttu-id="e6df7-124">Darbinieku attēliem ir jābūt ar nosaukumu "**/Workers/\{WorkerNumber\}.jpg**"</span><span class="sxs-lookup"><span data-stu-id="e6df7-124">Employee images should be named "**/Workers/\{WorkerNumber\}.jpg**"</span></span>
- <span data-ttu-id="e6df7-125">Preču attēliem ir jābūt ar nosaukumu "**/Products/\{ProductNumber\}_000_001.png**"</span><span class="sxs-lookup"><span data-stu-id="e6df7-125">Product images should be named "**/Products/\{ProductNumber\}_000_001.png**"</span></span>
    - <span data-ttu-id="e6df7-126">001 ir attēla secība, un tā var būt 001, 002, 003, 004 vai 005</span><span class="sxs-lookup"><span data-stu-id="e6df7-126">001 is the sequence of the image and it can be 001, 002, 003, 004 or 005</span></span>
- <span data-ttu-id="e6df7-127">Preču variantu attēliem ir jābūt ar nosaukumu "**/Products/\{ProductNumber\}\_\{Size\}\_\{Color\}\_\{Style\}\_000_001.png**"</span><span class="sxs-lookup"><span data-stu-id="e6df7-127">Product variant images should be named "**/Products/\{ProductNumber\}\_\{Size\}\_\{Color\}\_\{Style\}\_000_001.png**"</span></span>

## <a name="upload-an-image"></a><span data-ttu-id="e6df7-128">Augšupielādēt attēlu</span><span class="sxs-lookup"><span data-stu-id="e6df7-128">Upload an image</span></span>

<span data-ttu-id="e6df7-129">Lai augšupielādētu attēlu vietnes veidotājā, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="e6df7-129">To upload an image in site builder, follow these steps.</span></span>

1. <span data-ttu-id="e6df7-130">Kreisās puses navigācijas rūtī atlasiet **Mediju bibliotēka**.</span><span class="sxs-lookup"><span data-stu-id="e6df7-130">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="e6df7-131">Komandu joslā atlasiet **Augšupielādēt \> Augšupielādēt mediju vienumus**.</span><span class="sxs-lookup"><span data-stu-id="e6df7-131">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="e6df7-132">Failu pārlūka logā navigējiet uz un atlasiet vienu vai vairākus augšupielādējamos attēlu failus un pēc tam atlasiet **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="e6df7-132">In the File Explorer window, navigate to and select one or more image files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="e6df7-133">Dialoglodziņā **Augšupielādēt multivides vienumu** ievadiet nepieciešamo nosaukumu un alternatīvo tekstu.</span><span class="sxs-lookup"><span data-stu-id="e6df7-133">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="e6df7-134">Ievadiet neobligāto aprakstu un atslēgvārdus un, ja nepieciešams, atlasiet kategoriju.</span><span class="sxs-lookup"><span data-stu-id="e6df7-134">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="e6df7-135">Ja vēlaties publicēt attēlus tūlīt pēc augšupielādes, atzīmējiet izvēles rūtiņu **Publicēt multivides vienumus pēc augšupielādes**.</span><span class="sxs-lookup"><span data-stu-id="e6df7-135">If you want to publish the image(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="e6df7-136">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e6df7-136">Select **OK**.</span></span>

## <a name="upload-a-folder-of-images"></a><span data-ttu-id="e6df7-137">Augšupielādēt attēlu mapi</span><span class="sxs-lookup"><span data-stu-id="e6df7-137">Upload a folder of images</span></span>

<span data-ttu-id="e6df7-138">Lai augšupielādēt vairākus attēlus kopā vietnes veidotājā, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="e6df7-138">To bulk upload a folder of images in site builder, follow these steps.</span></span>

1. <span data-ttu-id="e6df7-139">Kreisās puses navigācijas rūtī atlasiet **Mediju bibliotēka**.</span><span class="sxs-lookup"><span data-stu-id="e6df7-139">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="e6df7-140">Komandu joslā atlasiet **Augšupielādēt \> Augšupielādēt mapi**.</span><span class="sxs-lookup"><span data-stu-id="e6df7-140">On the command bar, select **Upload \> Upload Folder**.</span></span>
1. <span data-ttu-id="e6df7-141">Failu pārlūka logā navigējiet uz un atlasiet augšupielādējamo mapi un pēc tam atlasiet **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="e6df7-141">In the File Explorer window, navigate to and select a folder to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="e6df7-142">Dialoglodziņā **Augšupielādēt multivides vienumus** ievadiet neobligātos atslēgvārdus un, ja nepieciešams, atlasiet kategoriju.</span><span class="sxs-lookup"><span data-stu-id="e6df7-142">In the **Upload Media Items** dialog box, enter optional keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="e6df7-143">Ja vēlaties publicēt mapē esošos attēlus tūlīt pēc augšupielādes, atzīmējiet izvēles rūtiņu **Publicēt multivides vienumus pēc augšupielādes**.</span><span class="sxs-lookup"><span data-stu-id="e6df7-143">If you want to publish the images in the folder immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="e6df7-144">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e6df7-144">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e6df7-145">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="e6df7-145">Additional resources</span></span>

[<span data-ttu-id="e6df7-146">Digitālo līdzekļu pārvaldības pārskats</span><span class="sxs-lookup"><span data-stu-id="e6df7-146">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="e6df7-147">Videoklipu augšupielāde</span><span class="sxs-lookup"><span data-stu-id="e6df7-147">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="e6df7-148">Augšupielādēt failus</span><span class="sxs-lookup"><span data-stu-id="e6df7-148">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="e6df7-149">Attēlu apgriešana</span><span class="sxs-lookup"><span data-stu-id="e6df7-149">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="e6df7-150">Attēlu fokusa punktu pielāgošana</span><span class="sxs-lookup"><span data-stu-id="e6df7-150">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="e6df7-151">Augšupielādēt un apkalpot statiskos failus</span><span class="sxs-lookup"><span data-stu-id="e6df7-151">Upload and serve static files</span></span>](upload-serve-static-files.md)
