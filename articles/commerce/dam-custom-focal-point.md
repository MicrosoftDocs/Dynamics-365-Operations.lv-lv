---
title: Attēlu fokusa punktu pielāgošana
description: Šajā tēmā ir aprakstīts, kā pielāgot attēla fokusa punktus programmas Microsoft Dynamics 365 Commerce vietnes veidotājā.
author: psimolin
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: b20fbc20f18243c712595795a0b16ae417e755e6
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594336"
---
# <a name="customize-image-focal-points"></a><span data-ttu-id="2ff8e-103">Attēlu fokusa punktu pielāgošana</span><span class="sxs-lookup"><span data-stu-id="2ff8e-103">Customize image focal points</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2ff8e-104">Šajā tēmā ir aprakstīts, kā pielāgot attēla fokusa punktus programmas Microsoft Dynamics 365 Commerce vietnes veidotājā.</span><span class="sxs-lookup"><span data-stu-id="2ff8e-104">This topic describes how to customize image focal points in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="2ff8e-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="2ff8e-105">Overview</span></span>

<span data-ttu-id="2ff8e-106">Kad attēls tiek augšupielādēts Commerce vietnes veidotāja multivides bibliotēkā, sistēma mēģina noteikt attēla fokusa punktu.</span><span class="sxs-lookup"><span data-stu-id="2ff8e-106">When an image is uploaded to the Commerce site builder Media Library, the system attempts to determine the focal point of the image.</span></span> <span data-ttu-id="2ff8e-107">Piemēram, ja attēlā ir persona, sistēma pēc noklusējuma iestatīs fokusa punktu uz personas seju.</span><span class="sxs-lookup"><span data-stu-id="2ff8e-107">For example, if the image has a person on it, the system will set the focal point to the face of the person by default.</span></span> <span data-ttu-id="2ff8e-108">Vairumā gadījumu automātiski tiek iestatīts fokusa punkts visiem skatpunktiem, bet dažkārt var būt nepieciešams pielāgot fokusa punktu, lai nodrošinātu, ka noteikta attēla daļa vienmēr ir redzama.</span><span class="sxs-lookup"><span data-stu-id="2ff8e-108">In most cases the automatically set focal point works well for all viewports, but sometimes you may want to adjust the focal point to ensure that a specific part of the image is always visible.</span></span>

### <a name="define-a-custom-focal-point-for-an-image"></a><span data-ttu-id="2ff8e-109">Definēt pielāgotu attēla fokusa punktu</span><span class="sxs-lookup"><span data-stu-id="2ff8e-109">Define a custom focal point for an image</span></span>

<span data-ttu-id="2ff8e-110">Lai definētu pielāgotu attēla fokusa punktu, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="2ff8e-110">To define a custom focal point for an image, follow these steps.</span></span>

1. <span data-ttu-id="2ff8e-111">Commerce vietnes veidotāja kreisajā navigācijas rūtī atlasiet **Multivides bibliotēka**.</span><span class="sxs-lookup"><span data-stu-id="2ff8e-111">In the left navigation pane of Commerce site builder, select **Media Library**.</span></span>
1. <span data-ttu-id="2ff8e-112">Galvenajā logā atlasiet attēlu, kuru vēlaties pārveidot.</span><span class="sxs-lookup"><span data-stu-id="2ff8e-112">In the main window, select the image you want to modify.</span></span>
1. <span data-ttu-id="2ff8e-113">Komandjoslā atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="2ff8e-113">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="2ff8e-114">Atlasiet attēlu, kuru vēlaties ievadīt **Rediģēšanas režīmā**.</span><span class="sxs-lookup"><span data-stu-id="2ff8e-114">Select the image to enter **Edit Mode**.</span></span>
1. <span data-ttu-id="2ff8e-115">Sadaļā **Rediģēšanas režīms** atlasiet **Mainīt fokusa punktu**.</span><span class="sxs-lookup"><span data-stu-id="2ff8e-115">Under **Edit Mode**, select **Change Focal Point**.</span></span> <span data-ttu-id="2ff8e-116">Virs attēla parādās riņķveida fokusa punktu vadīkla.</span><span class="sxs-lookup"><span data-stu-id="2ff8e-116">A circular focal point control appears over the image.</span></span>
1. <span data-ttu-id="2ff8e-117">Atlasiet fokusa punktu vadīklu, lai pārvietotu to uz vēlamo fokusa punktu.</span><span class="sxs-lookup"><span data-stu-id="2ff8e-117">Select the focal point control to move it over the desired focal point.</span></span>
1. <span data-ttu-id="2ff8e-118">Kad esat pabeidzis, komandjoslā atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="2ff8e-118">When you're done, on the command bar select **Save**, and then select **Finish editing**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2ff8e-119">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="2ff8e-119">Additional resources</span></span>

[<span data-ttu-id="2ff8e-120">Pārskats par digitālo līdzekļu pārvaldību</span><span class="sxs-lookup"><span data-stu-id="2ff8e-120">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="2ff8e-121">Attēlu augšupielāde</span><span class="sxs-lookup"><span data-stu-id="2ff8e-121">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="2ff8e-122">Videoklipu augšupielāde</span><span class="sxs-lookup"><span data-stu-id="2ff8e-122">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="2ff8e-123">Augšupielādēt failus</span><span class="sxs-lookup"><span data-stu-id="2ff8e-123">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="2ff8e-124">Attēlu apgriešana</span><span class="sxs-lookup"><span data-stu-id="2ff8e-124">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="2ff8e-125">Augšupielādēt un apkalpot statiskos failus</span><span class="sxs-lookup"><span data-stu-id="2ff8e-125">Upload and serve static files</span></span>](upload-serve-static-files.md)
