---
title: Pēc vides kopēšanas trūkst preču un kategoriju
description: Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt, ja trūkst preču un kategoriju pēc tam, kad vietne ir kopēta starp vidēm vai vienā un tajā pašā vidē.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 35f2cbd98a91149395f40bf821c1d5d7e58eaf77
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585437"
---
# <a name="products-and-categories-missing-after-environment-copy"></a><span data-ttu-id="b605d-103">Pēc vides kopēšanas trūkst preču un kategoriju</span><span class="sxs-lookup"><span data-stu-id="b605d-103">Products and categories missing after environment copy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b605d-104">Šajā tēmā ir sniegtas problēmu novēršanas norādes, kas var palīdzēt, ja trūkst preču un kategoriju pēc tam, kad vietne ir kopēta starp vidēm vai vienā un tajā pašā vidē.</span><span class="sxs-lookup"><span data-stu-id="b605d-104">This topic provides troubleshooting guidance that can help when products and categories are missing after a site is copied between environments or within the same environment.</span></span>

## <a name="description"></a><span data-ttu-id="b605d-105">Apraksts</span><span class="sxs-lookup"><span data-stu-id="b605d-105">Description</span></span>

<span data-ttu-id="b605d-106">Kad vietne ir pārkopēta no vienas vides uz citu vai vienā un tajā pašā vidē, vietnē trūkst produktu un kategoriju.</span><span class="sxs-lookup"><span data-stu-id="b605d-106">After a site is copied from one environment to another, or within the same environment, the products and categories are missing from the site.</span></span> <span data-ttu-id="b605d-107">Preces un kategorijas nebūs pieejamas no e-komercijas vitrīnām un no cilnes **Preces** Commerce vietņu veidotājā.</span><span class="sxs-lookup"><span data-stu-id="b605d-107">The products and categories will be missing from the e-commerce storefront and from the **Products** tab in Commerce site builder.</span></span>

## <a name="resolution"></a><span data-ttu-id="b605d-108">Novēršana</span><span class="sxs-lookup"><span data-stu-id="b605d-108">Resolution</span></span>

### <a name="map-the-channel-operating-unit-number-to-a-newly-copied-site-in-commerce-site-builder"></a><span data-ttu-id="b605d-109">Kanāla pārvaldības struktūrvienības numura kartēšana uz nesen kopēto vietni Commerce vietnes veidotājā</span><span class="sxs-lookup"><span data-stu-id="b605d-109">Map the channel operating unit number to a newly copied site in Commerce site builder</span></span>

<span data-ttu-id="b605d-110">Lai kartētu kanāla pārvaldības struktūrvienības numuru (OUN) uz nesen kopēto vietni Commerce vietnes veidotājā, izpildiet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="b605d-110">To map the channel operating unit number (OUN) to a newly copied site in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="b605d-111">Atlasiet tikko kopēto vietu.</span><span class="sxs-lookup"><span data-stu-id="b605d-111">Select the newly copied site.</span></span>
1. <span data-ttu-id="b605d-112">Sadaļā **Vietnes iestatījumi** atlasiet **Kanāli**.</span><span class="sxs-lookup"><span data-stu-id="b605d-112">Under **Site settings**, select **Channels**.</span></span>
1. <span data-ttu-id="b605d-113">Blakus kanāla nosaukumam atlasiet daudzpunkti (**...**) un pēc tam atlasiet **Mainīt tiešsaistes veikala kanālu**.</span><span class="sxs-lookup"><span data-stu-id="b605d-113">Next to the channel name, select the ellipsis (**...**), and then select **Change online store channel**.</span></span>
1. <span data-ttu-id="b605d-114">Dialoglodziņā **Mainīt tiešsaistes veikala kanālu** atlasiet kanālu, kuru kartēt uz tikko kopēto vietni, un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="b605d-114">In the **Change online store channel** dialog box, select the channel to map to the newly copied site, and then select **OK**.</span></span>
1. <span data-ttu-id="b605d-115">Atlasiet **Saglabāt un publicēt**.</span><span class="sxs-lookup"><span data-stu-id="b605d-115">Select **Save and publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b605d-116">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="b605d-116">Additional resources</span></span>

[<span data-ttu-id="b605d-117">Vietnes Dynamics 365 Commerce saistīšana ar tiešsaistes kanālu</span><span class="sxs-lookup"><span data-stu-id="b605d-117">Associate a Dynamics 365 Commerce site with an online channel</span></span>](../associate-site-online-store.md)