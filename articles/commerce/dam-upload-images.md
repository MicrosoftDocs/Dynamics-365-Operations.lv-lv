---
title: Attēlu augšupielāde
description: Šajā tēmā aprakstīts, kā augšupielādēt attēlus Microsoft Dynamics 365 Commerce vietnes veidotājā.
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
ms.openlocfilehash: 2a0a2fdb275cbeb65c06c01128e90ba660f98c9b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799233"
---
# <a name="upload-images"></a><span data-ttu-id="f3fa2-103">Attēlu augšupielāde</span><span class="sxs-lookup"><span data-stu-id="f3fa2-103">Upload images</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f3fa2-104">Šajā tēmā aprakstīts, kā augšupielādēt attēlus Microsoft Dynamics 365 Commerce vietnes veidotājā.</span><span class="sxs-lookup"><span data-stu-id="f3fa2-104">This topic describes how to upload images in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="f3fa2-105">Commerce vietnes veidotāja multivides bibliotēka ļauj augšupielādēt attēlus vai nu atsevišķi, vai lielapjomā, izmantojot mapes.</span><span class="sxs-lookup"><span data-stu-id="f3fa2-105">The Commerce site builder Media Library allows you to upload images, either singly or in bulk using folders.</span></span> <span data-ttu-id="f3fa2-106">Vienmēr augšupielādējiet attēla versiju ar augstāko izšķirtspēju un kvalitāti, jo attēla izmēra maiņas komponents automātiski optimizēs attēlu atšķirīgām skatvietām un to pārtraukumpunktiem.</span><span class="sxs-lookup"><span data-stu-id="f3fa2-106">You should always upload the version of the image with highest resolution and quality, because the image resizer component will automatically optimize the image for different viewports and their breakpoints.</span></span>

### <a name="image-information-specified-during-upload"></a><span data-ttu-id="f3fa2-107">Augšupielādes laikā norādītā attēla informācija</span><span class="sxs-lookup"><span data-stu-id="f3fa2-107">Image information specified during upload</span></span>

<span data-ttu-id="f3fa2-108">Augšupielādējot attēlu, var norādīt šādu informāciju.</span><span class="sxs-lookup"><span data-stu-id="f3fa2-108">When uploading an image, the following information can be specified.</span></span>

- <span data-ttu-id="f3fa2-109">**Virsraksts, alternatīvais teksts, apraksts, atslēgvārdi**: attēla vai attēlu metadati.</span><span class="sxs-lookup"><span data-stu-id="f3fa2-109">**Title, Alt Text, Description, Keywords**: Metadata of the image or images.</span></span> <span data-ttu-id="f3fa2-110">Nosaukums un alternatīvais teksts ir obligāta vērtības.</span><span class="sxs-lookup"><span data-stu-id="f3fa2-110">Title and alt text are required values.</span></span>
- <span data-ttu-id="f3fa2-111">**Atlasīt kategoriju**:</span><span class="sxs-lookup"><span data-stu-id="f3fa2-111">**Select category**:</span></span>
    - <span data-ttu-id="f3fa2-112">**Nav**: izmanto e-komercijas stāstu attēlam vai attēliem.</span><span class="sxs-lookup"><span data-stu-id="f3fa2-112">**None**: Used for an e-Commerce storytelling image or images.</span></span>
    - <span data-ttu-id="f3fa2-113">**Prece, kategorija, klients, darbinieks, katalogs**: izmanto Dynamics 365 Commerce daudzkanālu attēlu vai attēlus.</span><span class="sxs-lookup"><span data-stu-id="f3fa2-113">**Product, Category, Customer, Employee, Catalog**: Used for Dynamics 365 Commerce omni-channel image or images.</span></span>
- <span data-ttu-id="f3fa2-114">**Publicēt līdzekļus pēc augšupielādes**: kad šī izvēles rūtiņa ir atzīmēta, attēls vai attēli tiek publicēti uzreiz pēc augšupielādes.</span><span class="sxs-lookup"><span data-stu-id="f3fa2-114">**Publish assets after upload**: When this check box is selected, the image or images are published immediately after upload.</span></span>

> [!NOTE]
> <span data-ttu-id="f3fa2-115">Attēlu līdzekļi ar piešķirtu kategoriju tiek arī automātiski atzīmēti ar kategoriju kā atslēgvārdu, lai palīdzētu meklēt konkrētas kategorijas līdzekļus.</span><span class="sxs-lookup"><span data-stu-id="f3fa2-115">Image assets with a category assigned are also automatically tagged with the category as a keyword to aid searching for assets of a specific category.</span></span>

### <a name="naming-conventions-for-omni-channel-images"></a><span data-ttu-id="f3fa2-116">Nosaukšanas nosacījumi daudzkanālu attēliem</span><span class="sxs-lookup"><span data-stu-id="f3fa2-116">Naming conventions for omni-channel images</span></span> 

<span data-ttu-id="f3fa2-117">Ja multivides bibliotēka ir konfigurēta kā daudzkanālu attēlu aizmugursistēma, varat izmantot attēlu kategorijas, lai norādītu, kurai kategorijai augšupielādētais attēls pieder.</span><span class="sxs-lookup"><span data-stu-id="f3fa2-117">If you have configured the Media Library as the omni-channel image backend, you can use image categories to indicate which category the uploaded image belongs to.</span></span> <span data-ttu-id="f3fa2-118">Ir arī nosaukšanas nosacījumi, kas jāievēro, lai nodrošinātu, ka attēli tiek pareizi izgūti citos kanālos, piemēram, pārdošanas punktā (POS).</span><span class="sxs-lookup"><span data-stu-id="f3fa2-118">There is also a naming convention that should be followed to ensure that images are retrieved correctly by other channels, such as point of sale (POS).</span></span>

<span data-ttu-id="f3fa2-119">Noklusējuma nosaukšanas nosacījumi atšķiras atkarībā no kategorijas:</span><span class="sxs-lookup"><span data-stu-id="f3fa2-119">The default naming convention varies based on the category:</span></span>
- <span data-ttu-id="f3fa2-120">Kataloga attēliem ir jābūt ar nosaukumu "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"</span><span class="sxs-lookup"><span data-stu-id="f3fa2-120">Catalog images should be named "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"</span></span>
- <span data-ttu-id="f3fa2-121">Kategorijas attēliem ir jābūt ar nosaukumu "**/Categories/\{CategoryName\}.png**"</span><span class="sxs-lookup"><span data-stu-id="f3fa2-121">Category images should be named "**/Categories/\{CategoryName\}.png**"</span></span>
- <span data-ttu-id="f3fa2-122">Klientu attēliem ir jābūt ar nosaukumu "**/Customers/\{CustomerNumber\}.jpg**"</span><span class="sxs-lookup"><span data-stu-id="f3fa2-122">Customer images should be named "**/Customers/\{CustomerNumber\}.jpg**"</span></span>
- <span data-ttu-id="f3fa2-123">Darbinieku attēliem ir jābūt ar nosaukumu "**/Workers/\{WorkerNumber\}.jpg**"</span><span class="sxs-lookup"><span data-stu-id="f3fa2-123">Employee images should be named "**/Workers/\{WorkerNumber\}.jpg**"</span></span>
- <span data-ttu-id="f3fa2-124">Preču attēliem ir jābūt ar nosaukumu "**/Products/\{ProductNumber\}_000_001.png**"</span><span class="sxs-lookup"><span data-stu-id="f3fa2-124">Product images should be named "**/Products/\{ProductNumber\}_000_001.png**"</span></span>
    - <span data-ttu-id="f3fa2-125">001 ir attēla secība, un tā var būt 001, 002, 003, 004 vai 005</span><span class="sxs-lookup"><span data-stu-id="f3fa2-125">001 is the sequence of the image and it can be 001, 002, 003, 004 or 005</span></span>
- <span data-ttu-id="f3fa2-126">Preču variantu attēliem ir jābūt ar nosaukumu "**/Products/\{ProductNumber\} \^ \{Style\} \^ \{Size\} \^ \{Color\} \^\_000_001.png**"</span><span class="sxs-lookup"><span data-stu-id="f3fa2-126">Product variant images should be named "**/Products/\{ProductNumber\} \^ \{Style\} \^ \{Size\} \^ \{Color\} \^\_000_001.png**"</span></span>
    - <span data-ttu-id="f3fa2-127">Piemēram: 93039 \^\^2 \^ melna \^_000_001.png</span><span class="sxs-lookup"><span data-stu-id="f3fa2-127">For example: 93039 \^ \^ 2 \^ Black \^_000_001.png</span></span>

## <a name="upload-an-image"></a><span data-ttu-id="f3fa2-128">Augšupielādēt attēlu</span><span class="sxs-lookup"><span data-stu-id="f3fa2-128">Upload an image</span></span>

<span data-ttu-id="f3fa2-129">Lai augšupielādētu attēlu vietnes veidotājā, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="f3fa2-129">To upload an image in site builder, follow these steps.</span></span>

1. <span data-ttu-id="f3fa2-130">Kreisās puses navigācijas rūtī atlasiet **Mediju bibliotēka**.</span><span class="sxs-lookup"><span data-stu-id="f3fa2-130">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="f3fa2-131">Komandu joslā atlasiet **Augšupielādēt \> Augšupielādēt mediju vienumus**.</span><span class="sxs-lookup"><span data-stu-id="f3fa2-131">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="f3fa2-132">Failu pārlūka logā navigējiet uz un atlasiet vienu vai vairākus augšupielādējamos attēlu failus un pēc tam atlasiet **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="f3fa2-132">In the File Explorer window, navigate to and select one or more image files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="f3fa2-133">Dialoglodziņā **Augšupielādēt multivides vienumu** ievadiet nepieciešamo nosaukumu un alternatīvo tekstu.</span><span class="sxs-lookup"><span data-stu-id="f3fa2-133">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="f3fa2-134">Ievadiet neobligāto aprakstu un atslēgvārdus un, ja nepieciešams, atlasiet kategoriju.</span><span class="sxs-lookup"><span data-stu-id="f3fa2-134">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="f3fa2-135">Ja vēlaties publicēt attēlus tūlīt pēc augšupielādes, atzīmējiet izvēles rūtiņu **Publicēt multivides vienumus pēc augšupielādes**.</span><span class="sxs-lookup"><span data-stu-id="f3fa2-135">If you want to publish the image(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="f3fa2-136">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="f3fa2-136">Select **OK**.</span></span>

## <a name="upload-a-folder-of-images"></a><span data-ttu-id="f3fa2-137">Augšupielādēt attēlu mapi</span><span class="sxs-lookup"><span data-stu-id="f3fa2-137">Upload a folder of images</span></span>

<span data-ttu-id="f3fa2-138">Lai augšupielādēt vairākus attēlus kopā vietnes veidotājā, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="f3fa2-138">To bulk upload a folder of images in site builder, follow these steps.</span></span>

1. <span data-ttu-id="f3fa2-139">Kreisās puses navigācijas rūtī atlasiet **Mediju bibliotēka**.</span><span class="sxs-lookup"><span data-stu-id="f3fa2-139">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="f3fa2-140">Komandu joslā atlasiet **Augšupielādēt \> Augšupielādēt mapi**.</span><span class="sxs-lookup"><span data-stu-id="f3fa2-140">On the command bar, select **Upload \> Upload Folder**.</span></span>
1. <span data-ttu-id="f3fa2-141">Failu pārlūka logā navigējiet uz un atlasiet augšupielādējamo mapi un pēc tam atlasiet **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="f3fa2-141">In the File Explorer window, navigate to and select a folder to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="f3fa2-142">Dialoglodziņā **Augšupielādēt multivides vienumus** ievadiet neobligātos atslēgvārdus un, ja nepieciešams, atlasiet kategoriju.</span><span class="sxs-lookup"><span data-stu-id="f3fa2-142">In the **Upload Media Items** dialog box, enter optional keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="f3fa2-143">Ja vēlaties publicēt mapē esošos attēlus tūlīt pēc augšupielādes, atzīmējiet izvēles rūtiņu **Publicēt multivides vienumus pēc augšupielādes**.</span><span class="sxs-lookup"><span data-stu-id="f3fa2-143">If you want to publish the images in the folder immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="f3fa2-144">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="f3fa2-144">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f3fa2-145">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="f3fa2-145">Additional resources</span></span>

[<span data-ttu-id="f3fa2-146">Digitālo līdzekļu pārvaldības pārskats</span><span class="sxs-lookup"><span data-stu-id="f3fa2-146">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="f3fa2-147">Videoklipu augšupielāde</span><span class="sxs-lookup"><span data-stu-id="f3fa2-147">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="f3fa2-148">Augšupielādēt failus</span><span class="sxs-lookup"><span data-stu-id="f3fa2-148">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="f3fa2-149">Attēlu apgriešana</span><span class="sxs-lookup"><span data-stu-id="f3fa2-149">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="f3fa2-150">Attēlu fokusa punktu pielāgošana</span><span class="sxs-lookup"><span data-stu-id="f3fa2-150">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="f3fa2-151">Augšupielādēt un apkalpot statiskos failus</span><span class="sxs-lookup"><span data-stu-id="f3fa2-151">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
