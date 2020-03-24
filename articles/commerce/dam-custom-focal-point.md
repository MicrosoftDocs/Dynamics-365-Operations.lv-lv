---
title: Attēlu fokusa punktu pielāgošana
description: Šajā tēmā ir aprakstīts, kā pielāgot attēla fokusa punktus programmas Microsoft Dynamics 365 Commerce vietnes veidotājā.
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
ms.openlocfilehash: 2c9bbd51f1fe9a19198a455eedd3ba744d54a165
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/03/2020
ms.locfileid: "3097047"
---
# <a name="customize-image-focal-points"></a><span data-ttu-id="d531f-103">Attēlu fokusa punktu pielāgošana</span><span class="sxs-lookup"><span data-stu-id="d531f-103">Customize image focal points</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d531f-104">Šajā tēmā ir aprakstīts, kā pielāgot attēla fokusa punktus programmas Microsoft Dynamics 365 Commerce vietnes veidotājā.</span><span class="sxs-lookup"><span data-stu-id="d531f-104">This topic describes how to customize image focal points in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="d531f-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="d531f-105">Overview</span></span>

<span data-ttu-id="d531f-106">Kad attēls tiek augšupielādēts Commerce vietnes veidotāja multivides bibliotēkā, sistēma mēģina noteikt attēla fokusa punktu.</span><span class="sxs-lookup"><span data-stu-id="d531f-106">When an image is uploaded to the Commerce site builder Media Library, the system attempts to determine the focal point of the image.</span></span> <span data-ttu-id="d531f-107">Piemēram, ja attēlā ir persona, sistēma pēc noklusējuma iestatīs fokusa punktu uz personas seju.</span><span class="sxs-lookup"><span data-stu-id="d531f-107">For example, if the image has a person on it, the system will set the focal point to the face of the person by default.</span></span> <span data-ttu-id="d531f-108">Vairumā gadījumu automātiski tiek iestatīts fokusa punkts visiem skatpunktiem, bet dažkārt var būt nepieciešams pielāgot fokusa punktu, lai nodrošinātu, ka noteikta attēla daļa vienmēr ir redzama.</span><span class="sxs-lookup"><span data-stu-id="d531f-108">In most cases the automatically set focal point works well for all viewports, but sometimes you may want to adjust the focal point to ensure that a specific part of the image is always visible.</span></span>

### <a name="define-a-custom-focal-point-for-an-image"></a><span data-ttu-id="d531f-109">Definēt pielāgotu attēla fokusa punktu</span><span class="sxs-lookup"><span data-stu-id="d531f-109">Define a custom focal point for an image</span></span>

<span data-ttu-id="d531f-110">Lai definētu pielāgotu attēla fokusa punktu, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="d531f-110">To define a custom focal point for an image, follow these steps.</span></span>

1. <span data-ttu-id="d531f-111">Commerce vietnes veidotāja kreisajā navigācijas rūtī atlasiet **Multivides bibliotēka**.</span><span class="sxs-lookup"><span data-stu-id="d531f-111">In the left navigation pane of Commerce site builder, select **Media Library**.</span></span>
1. <span data-ttu-id="d531f-112">Galvenajā logā atlasiet attēlu, kuru vēlaties pārveidot.</span><span class="sxs-lookup"><span data-stu-id="d531f-112">In the main window, select the image you want to modify.</span></span>
1. <span data-ttu-id="d531f-113">Lai paņemtu failu, komandjoslā atlasiet **Rediģēt**.</span><span class="sxs-lookup"><span data-stu-id="d531f-113">On the command bar, select **Edit** to check out the file.</span></span>
1. <span data-ttu-id="d531f-114">Atlasiet attēlu, kuru vēlaties ievadīt **Rediģēšanas režīmā**.</span><span class="sxs-lookup"><span data-stu-id="d531f-114">Select the image to enter **Edit Mode**.</span></span>
1. <span data-ttu-id="d531f-115">Sadaļā **Rediģēšanas režīms** atlasiet **Mainīt fokusa punktu**.</span><span class="sxs-lookup"><span data-stu-id="d531f-115">Under **Edit Mode**, select **Change Focal Point**.</span></span> <span data-ttu-id="d531f-116">Virs attēla parādās riņķveida fokusa punktu vadīkla.</span><span class="sxs-lookup"><span data-stu-id="d531f-116">A circular focal point control appears over the image.</span></span>
1. <span data-ttu-id="d531f-117">Atlasiet fokusa punktu vadīklu, lai pārvietotu to uz vēlamo fokusa punktu.</span><span class="sxs-lookup"><span data-stu-id="d531f-117">Select the focal point control to move it over the desired focal point.</span></span>
1. <span data-ttu-id="d531f-118">Kad esat pabeidzis, komandjoslā atlasiet **Saglabāt** un pēc tam atlasiet **Pabeigt rediģēšanu**.</span><span class="sxs-lookup"><span data-stu-id="d531f-118">When you're done, on the command bar select **Save**, and then select **Finish editing**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d531f-119">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="d531f-119">Additional resources</span></span>

[<span data-ttu-id="d531f-120">Digitālo līdzekļu pārvaldības pārskats</span><span class="sxs-lookup"><span data-stu-id="d531f-120">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="d531f-121">Augšupielādēt attēlus</span><span class="sxs-lookup"><span data-stu-id="d531f-121">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="d531f-122">Augšupielādēt video</span><span class="sxs-lookup"><span data-stu-id="d531f-122">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="d531f-123">Augšupielādēt failus</span><span class="sxs-lookup"><span data-stu-id="d531f-123">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="d531f-124">Apgriezt attēlus</span><span class="sxs-lookup"><span data-stu-id="d531f-124">Crop images</span></span>](dam-crop-images.md)
