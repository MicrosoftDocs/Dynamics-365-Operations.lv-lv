---
title: Preču ieteikumu apskats
description: Šajā tēmā ir sniegta vispārīga informācija par preču ieteikumiem. Preču ieteikumi ļauj klientiem viegli un ātri atrast preces, ko viņi vēlas, un pat tādas preces, kuras viņi sākotnēji neplānoja nopirkt.
author: Moonma
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: eb369e6d1356ba13a2310d523b671ac57b9642bf
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770051"
---
# <a name="product-recommendations-overview"></a><span data-ttu-id="bb37a-104">Preču ieteikumu apskats</span><span class="sxs-lookup"><span data-stu-id="bb37a-104">Product recommendations overview</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="bb37a-105">Microsoft Dynamics 365 Commerce var izmantot, lai parādītu preces ieteikumus e-tirdzniecības vietnē un pārdošanas punkta (POS) ierīcē.</span><span class="sxs-lookup"><span data-stu-id="bb37a-105">Microsoft Dynamics 365 Commerce can be used to show product recommendations on the e-Commerce website and point of sale (POS) device.</span></span> <span data-ttu-id="bb37a-106">Preces ieteikumi ir preces, kas varētu interesēt klientu.</span><span class="sxs-lookup"><span data-stu-id="bb37a-106">Product recommendations are items that a customer might be interested in.</span></span> <span data-ttu-id="bb37a-107">Ieteikumi ir balstīti uz citu klientu pirkšanas tendencēm citiem klientiem tiešsaistes un parastajos veikalos.</span><span class="sxs-lookup"><span data-stu-id="bb37a-107">The recommendations are based on the purchase trends of other customers in online and brick-and-mortar stores.</span></span>

<span data-ttu-id="bb37a-108">Preces ieteikumi ļauj klientiem viegli un ātri atrast preces, ko viņi vēlas, gūstot noderīgu pieredzi.</span><span class="sxs-lookup"><span data-stu-id="bb37a-108">Product recommendations let customers easily and quickly find products that they want while they have an experience that serves them well.</span></span> <span data-ttu-id="bb37a-109">Papildus preču pārdošana un citu preču pārdošana var pat tikt izmantota, lai palīdzētu klientiem atrast papildu preces, ko viņi sākotnēji nebija iecerējuši pirkt.</span><span class="sxs-lookup"><span data-stu-id="bb37a-109">Cross-selling and upselling can even be used to help customers find additional products than they didn't originally intend to buy.</span></span> <span data-ttu-id="bb37a-110">Kad ieteikumi tiek izmantoti, lai palīdzētu atklāt preces, tie var izveidot vairāk pārvēršanas iespēju, palīdzēt palielināt pārdošanas ieņēmumus un pat palīdzēt uzlabot klientu apmierinātību un lojalitāti.</span><span class="sxs-lookup"><span data-stu-id="bb37a-110">When recommendations are used to help with product discovery, they can create more conversion opportunities, help increase sales revenue, and even help enhance customer satisfaction and retention.</span></span>

<span data-ttu-id="bb37a-111">Commerce preces ieteikumi darbojas, plašā mērogā izmantojot Microsoft Recommendations mašīnmācības tehnoloģijas.</span><span class="sxs-lookup"><span data-stu-id="bb37a-111">In Commerce, product recommendations are powered by Microsoft Recommendations machine learning technologies on a large scale.</span></span>


## <a name="scenarios"></a><span data-ttu-id="bb37a-112">Scenāriji</span><span class="sxs-lookup"><span data-stu-id="bb37a-112">Scenarios</span></span>

<span data-ttu-id="bb37a-113">Preču ieteikumi ir pieejami tālāk minētajiem POS scenārijiem.</span><span class="sxs-lookup"><span data-stu-id="bb37a-113">Product recommendations are available for the following scenarios:</span></span>

- <span data-ttu-id="bb37a-114">**Jebkurā veikala lapā, kas paredzēta pārlūkošanai vai kā mērķlapa e-tirdzniecībā:** ja klienti vai veikala partneri apmeklē veikala lapu, ieteikumu programma var ieteikt preces sarakstos **Jauns**, **Vispirktākais** un **Populārs**.</span><span class="sxs-lookup"><span data-stu-id="bb37a-114">**On any store page for browsing or landing page in e-Commerce:** If customers or store associates visit a store page, the recommendation engine can suggest products in the **New**, **Best Selling**, and **Trending** lists.</span></span>
- <span data-ttu-id="bb37a-115">**Preces detalizētas informācijas lapā:** ja klienti vai veikala partneri apmeklē lapu **Preces detalizēta informācija**, ieteikumu programma iesaka papildu preces, kas arī iespējams tiks iegādātas.</span><span class="sxs-lookup"><span data-stu-id="bb37a-115">**On the Product details page:** If customers or store associates visit a **Product details** page, the recommendation engine suggests additional items that are also likely to be purchased.</span></span> <span data-ttu-id="bb37a-116">Šīs preces parādās sarakstā **Pircējiem patīk arī**.</span><span class="sxs-lookup"><span data-stu-id="bb37a-116">These items appear in the **People also like** list.</span></span>
- <span data-ttu-id="bb37a-117">**Transakciju lapā vai izrakstīšanas lapā:** ieteikumu programma piedāvā preces, balstoties uz visu grozā esošo preču sarakstu.</span><span class="sxs-lookup"><span data-stu-id="bb37a-117">**On the Transaction page or the checkout page:** The recommendation engine suggests items, based on the whole list of items in the basket.</span></span> <span data-ttu-id="bb37a-118">Šie krājumi parādās sarakstā **Bieži iegādāts kopā**.</span><span class="sxs-lookup"><span data-stu-id="bb37a-118">These items appear in the **Frequently bought together** list.</span></span>

## <a name="recommendation-service"></a><span data-ttu-id="bb37a-119">Recommendation pakalpojums</span><span class="sxs-lookup"><span data-stu-id="bb37a-119">Recommendation service</span></span>

<span data-ttu-id="bb37a-120">Preces ieteikumi izmanto Recommendations mašīnmācības tehnoloģijas tālāk minētajā veidā.</span><span class="sxs-lookup"><span data-stu-id="bb37a-120">Product recommendations use the Recommendations machine learning technologies in the following way:</span></span>

- <span data-ttu-id="bb37a-121">No Commerce operacionālās datu bāzes tiek izgūti Recommendation pakalpojumam nepieciešamā formāta dati, un šie dati tiek nosūtīti Entity krātuvei.</span><span class="sxs-lookup"><span data-stu-id="bb37a-121">Data in the format that the Recommendation service requires is extracted from the Commerce operational database and sent to the Entity store.</span></span>
- <span data-ttu-id="bb37a-122">Recommendation pakalpojums izmanto datus, lai apmācīt ieteikumu modeļus sarakstiem **Pircējiem patīk arī**, **Bieži iegādāts kopā**, **Jauns**, **Vispirktākais** un **Populārs**.</span><span class="sxs-lookup"><span data-stu-id="bb37a-122">The Recommendation service uses the data to train recommendation models for the **People also like**, **Frequently bought together**, **New**, **Best selling**, and **Trending** lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bb37a-123">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="bb37a-123">Additional resources</span></span>

[<span data-ttu-id="bb37a-124">Preču ieteikumu iespējošana</span><span class="sxs-lookup"><span data-stu-id="bb37a-124">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="bb37a-125">Pārraudzītu preču ieteikumu sarakstu izveide</span><span class="sxs-lookup"><span data-stu-id="bb37a-125">Create curated product recommendation lists</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="bb37a-126">Uz AI-ML balstītu preču ieteikumu rezultātu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="bb37a-126">Manage AI-ML-based product recommendation results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="bb37a-127">Preču ieteikumu sarakstu pievienošana lapām</span><span class="sxs-lookup"><span data-stu-id="bb37a-127">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)
