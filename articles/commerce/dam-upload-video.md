---
title: Augšupielādēt videoklipus
description: Šajā tēmā ir aprakstīts, kā augšupielādēt videoklipus programmas Microsoft Dynamics 365 Commerce vietnes veidotājā.
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
ms.openlocfilehash: 98cb4f9049509dd700cf38a5d176447f86e9c824
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/03/2020
ms.locfileid: "3097051"
---
# <a name="upload-videos"></a><span data-ttu-id="405d4-103">Augšupielādēt videoklipus</span><span class="sxs-lookup"><span data-stu-id="405d4-103">Upload videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="405d4-104">Šajā tēmā ir aprakstīts, kā augšupielādēt videoklipus programmas Microsoft Dynamics 365 Commerce vietnes veidotājā.</span><span class="sxs-lookup"><span data-stu-id="405d4-104">This topic describes how to upload videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="405d4-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="405d4-105">Overview</span></span>

<span data-ttu-id="405d4-106">Commerce vietnes veidotāja multivides bibliotēka ļauj augšupielādēt videoklipus.</span><span class="sxs-lookup"><span data-stu-id="405d4-106">The Commerce site builder Media Library allows you to upload videos.</span></span> <span data-ttu-id="405d4-107">Vienmēr augšupielādējiet videoklipa versiju ar augstāko bitu pārraides ātrumu un izšķirtspēju, jo videoklips tiks automātiski pārveidots, lai tas būtu piemērots dažādām skatvietām un to pārtraukumpunktiem.</span><span class="sxs-lookup"><span data-stu-id="405d4-107">You should always upload the version of a video with the highest bitrate and resolution, because the video will be automatically converted to be suitable for different viewports and their breakpoints.</span></span>

### <a name="video-information-specified-during-upload"></a><span data-ttu-id="405d4-108">Augšupielādes laikā norādītā videoklipa informācija</span><span class="sxs-lookup"><span data-stu-id="405d4-108">Video information specified during upload</span></span>

<span data-ttu-id="405d4-109">Augšupielādējot videoklipu, var norādīt šādu informāciju.</span><span class="sxs-lookup"><span data-stu-id="405d4-109">When uploading a video, the following information can be specified.</span></span>

- <span data-ttu-id="405d4-110">**Nosaukums, apraksts, atslēgvārdi**: videoklipa metadati.</span><span class="sxs-lookup"><span data-stu-id="405d4-110">**Title, Description, Keywords**: Metadata of the video.</span></span>
- <span data-ttu-id="405d4-111">**Automātiski ģenerēt slēgtos titrus**: norāda, vai videoklipam automātiski jāģenerē slēgtos titrus.</span><span class="sxs-lookup"><span data-stu-id="405d4-111">**Automatically generate closed captions**: Specifies whether closed captions should be automatically generated for the video.</span></span>
- <span data-ttu-id="405d4-112">**Slēgtie titri**: Norāda izmantojamos slēgtos titrus.</span><span class="sxs-lookup"><span data-stu-id="405d4-112">**Closed Caption**: Specifies the closed captions to be used.</span></span>
- <span data-ttu-id="405d4-113">**Parastais audio**: Norāda izmantojamo parasto audio ierakstu.</span><span class="sxs-lookup"><span data-stu-id="405d4-113">**Regular Audio**: Specifies the regular audio track to be used.</span></span>
- <span data-ttu-id="405d4-114">**Sīktēls**: Norāda videoklipa sīktēlu.</span><span class="sxs-lookup"><span data-stu-id="405d4-114">**Thumbnail**: Specifies the thumbnail for the video.</span></span> <span data-ttu-id="405d4-115">Numuru sērija tiks izveidota automātiski, ja tā netiek konkretizēta.</span><span class="sxs-lookup"><span data-stu-id="405d4-115">If not specified, it will be generated automatically.</span></span>
- <span data-ttu-id="405d4-116">**Aprakstošais audio**: Norāda izmantojamo aprakstošo audio ierakstu.</span><span class="sxs-lookup"><span data-stu-id="405d4-116">**Descriptive Audio**: Specifies the descriptive audio track to be used.</span></span>

## <a name="upload-a-video"></a><span data-ttu-id="405d4-117">Augšupielādēt videoklipu</span><span class="sxs-lookup"><span data-stu-id="405d4-117">Upload a video</span></span>

<span data-ttu-id="405d4-118">Lai augšupielādētu videoklipu vietnes veidotājā, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="405d4-118">To upload a video in site builder, follow these steps.</span></span>

1. <span data-ttu-id="405d4-119">Kreisās puses navigācijas rūtī atlasiet **Mediju bibliotēka**.</span><span class="sxs-lookup"><span data-stu-id="405d4-119">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="405d4-120">Komandu joslā atlasiet **Augšupielādēt \>Augšupielādēt mediju vienumus**.</span><span class="sxs-lookup"><span data-stu-id="405d4-120">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="405d4-121">Failu pārlūka logā navigējiet uz un atlasiet vienu vai vairākus augšupielādējamos videoklipu failus un pēc tam atlasiet **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="405d4-121">In the File Explorer window, navigate to and select one or more video files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="405d4-122">Dialoglodziņā **Augšupielādēt multivides vienumu** ievadiet nepieciešamo nosaukumu un alternatīvo tekstu.</span><span class="sxs-lookup"><span data-stu-id="405d4-122">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="405d4-123">Ievadiet neobligāto aprakstu un atslēgvārdus un, ja nepieciešams, atlasiet kategoriju.</span><span class="sxs-lookup"><span data-stu-id="405d4-123">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="405d4-124">Ja vēlaties publicēt attēlus pēc tūlītējas augšupielādes, atzīmējiet izvēles rūtiņu **Publicēt multivides vienumus pēc augšupielādes**</span><span class="sxs-lookup"><span data-stu-id="405d4-124">If you want to publish the image(s) after immediately upload, select the **Publish media items after upload** check box</span></span>
1. <span data-ttu-id="405d4-125">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="405d4-125">Select **OK**.</span></span>

<span data-ttu-id="405d4-126">Ja ielādējat vairāku tipu līdzekļus vienlaicīgi (piemēram, attēlus un videoklipus), dialoglodziņā **Augšupielādēt multivides vienumu** varēsit tikai norādīt atslēgvārdus, to, vai faili ir jāpublicē uzreiz pēc augšupielādes, un vai videoklipu failiem automātiski jāģenerē slēgtie titri.</span><span class="sxs-lookup"><span data-stu-id="405d4-126">If you are uploading multiple types of assets simultaneously (for example, images and videos), in the **Upload Media Item** dialog box you will only be able to specify keywords, whether the files should be published immediately after upload, and whether closed captions should be automatically generated for video files.</span></span> <span data-ttu-id="405d4-127">Visiem pamatlīdzekļiem būs vienādi atslēgvārdi.</span><span class="sxs-lookup"><span data-stu-id="405d4-127">All the assets will share the same keywords.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="405d4-128">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="405d4-128">Additional resources</span></span>

[<span data-ttu-id="405d4-129">Digitālo līdzekļu pārvaldības pārskats</span><span class="sxs-lookup"><span data-stu-id="405d4-129">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="405d4-130">Augšupielādēt attēlus</span><span class="sxs-lookup"><span data-stu-id="405d4-130">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="405d4-131">Augšupielādēt failus</span><span class="sxs-lookup"><span data-stu-id="405d4-131">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="405d4-132">Apgriezt attēlus</span><span class="sxs-lookup"><span data-stu-id="405d4-132">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="405d4-133">Attēlu fokusa punktu pielāgošana</span><span class="sxs-lookup"><span data-stu-id="405d4-133">Customize image focal points</span></span>](dam-custom-focal-point.md)
