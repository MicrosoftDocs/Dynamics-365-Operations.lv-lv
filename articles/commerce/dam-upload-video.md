---
title: Augšupielādēt videoklipus
description: Šajā tēmā aprakstīts, kā augšupielādēt videoklipus Microsoft Dynamics 365 Commerce vietnes veidotājā.
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
ms.openlocfilehash: 5ec20f8caee2f5a62230be05923dfd52600c1e35
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799209"
---
# <a name="upload-videos"></a><span data-ttu-id="c45a9-103">Augšupielādēt videoklipus</span><span class="sxs-lookup"><span data-stu-id="c45a9-103">Upload videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c45a9-104">Šajā tēmā aprakstīts, kā augšupielādēt videoklipus Microsoft Dynamics 365 Commerce vietnes veidotājā.</span><span class="sxs-lookup"><span data-stu-id="c45a9-104">This topic describes how to upload videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="c45a9-105">Commerce vietnes veidotāja multivides bibliotēka ļauj augšupielādēt videoklipus.</span><span class="sxs-lookup"><span data-stu-id="c45a9-105">The Commerce site builder Media Library allows you to upload videos.</span></span> <span data-ttu-id="c45a9-106">Vienmēr augšupielādējiet videoklipa versiju ar augstāko bitu pārraides ātrumu un izšķirtspēju, jo videoklips tiks automātiski pārveidots, lai tas būtu piemērots dažādām skatvietām un to pārtraukumpunktiem.</span><span class="sxs-lookup"><span data-stu-id="c45a9-106">You should always upload the version of a video with the highest bitrate and resolution, because the video will be automatically converted to be suitable for different viewports and their breakpoints.</span></span>

### <a name="video-information-specified-during-upload"></a><span data-ttu-id="c45a9-107">Augšupielādes laikā norādītā videoklipa informācija</span><span class="sxs-lookup"><span data-stu-id="c45a9-107">Video information specified during upload</span></span>

<span data-ttu-id="c45a9-108">Augšupielādējot videoklipu, var norādīt šādu informāciju.</span><span class="sxs-lookup"><span data-stu-id="c45a9-108">When uploading a video, the following information can be specified.</span></span>

- <span data-ttu-id="c45a9-109">**Nosaukums, apraksts, atslēgvārdi**: videoklipa metadati.</span><span class="sxs-lookup"><span data-stu-id="c45a9-109">**Title, Description, Keywords**: Metadata of the video.</span></span>
- <span data-ttu-id="c45a9-110">**Automātiski ģenerēt slēgtos titrus**: norāda, vai videoklipam automātiski jāģenerē slēgtos titrus.</span><span class="sxs-lookup"><span data-stu-id="c45a9-110">**Automatically generate closed captions**: Specifies whether closed captions should be automatically generated for the video.</span></span>
- <span data-ttu-id="c45a9-111">**Slēgtie titri**: Norāda izmantojamos slēgtos titrus.</span><span class="sxs-lookup"><span data-stu-id="c45a9-111">**Closed Caption**: Specifies the closed captions to be used.</span></span>
- <span data-ttu-id="c45a9-112">**Parastais audio**: Norāda izmantojamo parasto audio ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c45a9-112">**Regular Audio**: Specifies the regular audio track to be used.</span></span>
- <span data-ttu-id="c45a9-113">**Sīktēls**: Norāda videoklipa sīktēlu.</span><span class="sxs-lookup"><span data-stu-id="c45a9-113">**Thumbnail**: Specifies the thumbnail for the video.</span></span> <span data-ttu-id="c45a9-114">Numuru sērija tiks izveidota automātiski, ja tā netiek konkretizēta.</span><span class="sxs-lookup"><span data-stu-id="c45a9-114">If not specified, it will be generated automatically.</span></span>
- <span data-ttu-id="c45a9-115">**Aprakstošais audio**: Norāda izmantojamo aprakstošo audio ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c45a9-115">**Descriptive Audio**: Specifies the descriptive audio track to be used.</span></span>

## <a name="upload-a-video"></a><span data-ttu-id="c45a9-116">Augšupielādēt videoklipu</span><span class="sxs-lookup"><span data-stu-id="c45a9-116">Upload a video</span></span>

<span data-ttu-id="c45a9-117">Lai augšupielādētu videoklipu vietnes veidotājā, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="c45a9-117">To upload a video in site builder, follow these steps.</span></span>

1. <span data-ttu-id="c45a9-118">Kreisās puses navigācijas rūtī atlasiet **Mediju bibliotēka**.</span><span class="sxs-lookup"><span data-stu-id="c45a9-118">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="c45a9-119">Komandu joslā atlasiet **Augšupielādēt \> Augšupielādēt mediju vienumus**.</span><span class="sxs-lookup"><span data-stu-id="c45a9-119">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="c45a9-120">Failu pārlūka logā navigējiet uz un atlasiet vienu vai vairākus augšupielādējamos videoklipu failus un pēc tam atlasiet **Atvērt**.</span><span class="sxs-lookup"><span data-stu-id="c45a9-120">In the File Explorer window, navigate to and select one or more video files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="c45a9-121">Dialoglodziņā **Augšupielādēt multivides vienumu** ievadiet nepieciešamo nosaukumu un alternatīvo tekstu.</span><span class="sxs-lookup"><span data-stu-id="c45a9-121">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="c45a9-122">Ievadiet neobligāto aprakstu un atslēgvārdus un, ja nepieciešams, atlasiet kategoriju.</span><span class="sxs-lookup"><span data-stu-id="c45a9-122">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="c45a9-123">Ja vēlaties publicēt attēlus pēc tūlītējas augšupielādes, atzīmējiet izvēles rūtiņu **Publicēt multivides vienumus pēc augšupielādes**</span><span class="sxs-lookup"><span data-stu-id="c45a9-123">If you want to publish the image(s) after immediately upload, select the **Publish media items after upload** check box</span></span>
1. <span data-ttu-id="c45a9-124">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="c45a9-124">Select **OK**.</span></span>

<span data-ttu-id="c45a9-125">Ja ielādējat vairāku tipu līdzekļus vienlaicīgi (piemēram, attēlus un videoklipus), dialoglodziņā **Augšupielādēt multivides vienumu** varēsit tikai norādīt atslēgvārdus, to, vai faili ir jāpublicē uzreiz pēc augšupielādes, un vai videoklipu failiem automātiski jāģenerē slēgtie titri.</span><span class="sxs-lookup"><span data-stu-id="c45a9-125">If you are uploading multiple types of assets simultaneously (for example, images and videos), in the **Upload Media Item** dialog box you will only be able to specify keywords, whether the files should be published immediately after upload, and whether closed captions should be automatically generated for video files.</span></span> <span data-ttu-id="c45a9-126">Visiem pamatlīdzekļiem būs vienādi atslēgvārdi.</span><span class="sxs-lookup"><span data-stu-id="c45a9-126">All the assets will share the same keywords.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c45a9-127">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="c45a9-127">Additional resources</span></span>

[<span data-ttu-id="c45a9-128">Digitālo līdzekļu pārvaldības pārskats</span><span class="sxs-lookup"><span data-stu-id="c45a9-128">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="c45a9-129">Attēlu augšupielāde</span><span class="sxs-lookup"><span data-stu-id="c45a9-129">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="c45a9-130">Augšupielādēt failus</span><span class="sxs-lookup"><span data-stu-id="c45a9-130">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="c45a9-131">Attēlu apgriešana</span><span class="sxs-lookup"><span data-stu-id="c45a9-131">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="c45a9-132">Attēlu fokusa punktu pielāgošana</span><span class="sxs-lookup"><span data-stu-id="c45a9-132">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="c45a9-133">Augšupielādēt un apkalpot statiskos failus</span><span class="sxs-lookup"><span data-stu-id="c45a9-133">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
