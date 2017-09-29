---
title: Zvanu centra katalogi
description: "Šajā rakstā ir aprakstīta zvanu centram specifiskā funkcionalitāte, kas tiek lietota katalogiem programmatūrā Microsoft Dynamics 365 for Retail."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16231
ms.assetid: f28a827c-3a50-4d5e-83eb-e5a768db70a1
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 7be87496ceaea2d1d5f97a5cc17e50dcddbaf33d
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---

# <a name="call-center-catalogs"></a><span data-ttu-id="73363-103">Zvanu centra katalogi</span><span class="sxs-lookup"><span data-stu-id="73363-103">Call center catalogs</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="73363-104">Šajā rakstā ir aprakstīta zvanu centram specifiskā funkcionalitāte, kas tiek lietota katalogiem programmatūrā Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="73363-104">This article describes the call center–specific functionality for catalogs in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="73363-105">Zvanu centrā preču katalogus var izmantot, lai identificētu preces, kuras vēlaties piedāvāt debitoriem.</span><span class="sxs-lookup"><span data-stu-id="73363-105">In a call center, you can use product catalogs to identify the products that you want to offer to customers.</span></span> <span data-ttu-id="73363-106">Zvanu centros parasti tiek izmantoti drukātie katalogi.</span><span class="sxs-lookup"><span data-stu-id="73363-106">Call centers typically use printed catalogs.</span></span> <span data-ttu-id="73363-107">Drukāta kataloga noformēšana un ražošana tiek veikta ārpus programmatūras Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="73363-107">The design and production of a printed catalog is handled outside Dynamics 365 for Retail.</span></span> <span data-ttu-id="73363-108">Taču varat izveidot un saglabāt katalogu digitālā formātā, izmantojot tās pašas lapas, ko lietojat tiešsaistes mazumtirdzniecības katalogu iestatīšanai.</span><span class="sxs-lookup"><span data-stu-id="73363-108">However, you can create and store a digital form of a catalog by using the same pages that you use to set up online retail catalogs.</span></span> <span data-ttu-id="73363-109">Lai varētu izveidot katalogu, jāiestata preču klāsti un jāpiešķir tie zvanu centram.</span><span class="sxs-lookup"><span data-stu-id="73363-109">Before you can create a catalog, you must set up product assortments and assign the assortments to a call center.</span></span> <span data-ttu-id="73363-110">Pēc tam pievienojiet preces katalogam, atlasot preces no šiem preču klāstiem.</span><span class="sxs-lookup"><span data-stu-id="73363-110">You then add products to the catalog by selecting products from these assortments.</span></span> <span data-ttu-id="73363-111">Kad preces ir pievienotas katalogam un katalogs ir pabeigts, validējiet katalogu, lai verificētu datus.</span><span class="sxs-lookup"><span data-stu-id="73363-111">After products have been added to the catalog, and the catalog is complete, you must validate the catalog to verify the data.</span></span> <span data-ttu-id="73363-112">Pēc tam iesniedziet katalogu pārskatīšanai un apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="73363-112">You must then submit the catalog for review and approval.</span></span> <span data-ttu-id="73363-113">Kad katalogs ir apstiprināts, to var publicēt.</span><span class="sxs-lookup"><span data-stu-id="73363-113">After the catalog is approved, it can be published.</span></span> <span data-ttu-id="73363-114">Kad esat izveidojis zvanu centra katalogu, kataloga publicēšanas brīdī varat izveidot kataloga datu momentuzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="73363-114">When a call center catalog is created, you can take a snapshot of the catalog data at the time that the catalog is published.</span></span> <span data-ttu-id="73363-115">Šī momentuzņēmumu funkcionalitāte ļauj piekļūt noteiktām kataloga versijām pat tad, ja katalogā vēlāk tiek veiktas izmaiņas un tas tiek atjaunināts.</span><span class="sxs-lookup"><span data-stu-id="73363-115">This snapshot functionality lets you access a particular version of the catalog even if the catalog is later changed and updated.</span></span> <span data-ttu-id="73363-116">Zvanu centra katalogiem arī var iestatīt, lai tiktu iekļauti šādi izvēles līdzekļi:</span><span class="sxs-lookup"><span data-stu-id="73363-116">Call center catalogs can also be set up to include the following optional features:</span></span>

-   <span data-ttu-id="73363-117">**Avota kodi** – avota kodi, kas tiek izmantoti, lai izsekotu debitora reakciju uz noteiktiem kataloga pasta sūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="73363-117">**Source codes** – Source codes are used to track the customer response to specific catalog mailings.</span></span>
-   <span data-ttu-id="73363-118">**Bezmaksas preces** – preces, kas var būt iekļautas debitora pasūtījumā bez papildu maksas.</span><span class="sxs-lookup"><span data-stu-id="73363-118">**Free products** – Products can be included in a customer's order at no additional charge.</span></span> <span data-ttu-id="73363-119">Šīs preces automātiski tiek pievienotas pasūtījumam, ja pasūtījumā ir ievadīts kataloga avota kods.</span><span class="sxs-lookup"><span data-stu-id="73363-119">These products are automatically added to an order when the source code for the catalog is entered into the order.</span></span>
-   <span data-ttu-id="73363-120">**Skripti** – skripti ir teksti, kurus zvanu centra darbinieks nolasa debitoram, kad tiek izveidots pārdošanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="73363-120">**Scripts** – Scripts are texts that a call center worker reads to a customer when a sales order is being created.</span></span> <span data-ttu-id="73363-121">Skriptos var iekļaut sveicienus vai ieteikumus pirkumu veikšanai.</span><span class="sxs-lookup"><span data-stu-id="73363-121">Scripts can include greetings or purchase suggestions.</span></span>
-   <span data-ttu-id="73363-122">**Lapas izkārtojums** – lapas izkārtojums tver produktu lapas pozīciju drukātā katalogā.</span><span class="sxs-lookup"><span data-stu-id="73363-122">**Page layout** – A page layout captures the page position of products in the printed catalog.</span></span> <span data-ttu-id="73363-123">Šī informācija tiek izmantota kataloga zonas analīzes pārskatam.</span><span class="sxs-lookup"><span data-stu-id="73363-123">This information is used for the catalog area analysis report.</span></span>





