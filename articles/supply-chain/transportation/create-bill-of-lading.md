---
title: Izveidot preču transporta pavadzīmi
description: Šajā tēmā ir aprakstīts, kā izveidot preču transporta pavadzīmi, izmantojot noliktavas vadības procesus.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench, WHSBillOfLadingCarrier, WHSBillOfLadingOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7b001ef8936e7e35db89163683c023211f79b24c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996474"
---
# <a name="create-a-bill-of-lading"></a><span data-ttu-id="7d7b0-103">Izveidot preču transporta pavadzīmi</span><span class="sxs-lookup"><span data-stu-id="7d7b0-103">Create a bill of lading</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d7b0-104">Šajā tēmā ir aprakstīts, kā izveidot preču transporta pavadzīmi, izmantojot noliktavas vadības procesus.</span><span class="sxs-lookup"><span data-stu-id="7d7b0-104">This topic describes how to create a bill of lading when using warehouse management processes.</span></span>  

<span data-ttu-id="7d7b0-105">Preču transporta pavadzīme ir juridisks dokuments, kas noslēgts starp uzņēmumu, kurš nosūta preces, un pārvadātāju.</span><span class="sxs-lookup"><span data-stu-id="7d7b0-105">A bill of lading is a legal document between the company that ships the items and the carrier.</span></span> <span data-ttu-id="7d7b0-106">Dokuments ir pievienots nosūtītajām precēm, un tas kalpo kā sūtījuma saņemšanas apliecinājums, kad preces tiek piegādātas galamērķī.</span><span class="sxs-lookup"><span data-stu-id="7d7b0-106">The document accompanies the shipped items, and it serves as a receipt of shipment when the items are delivered at the destination.</span></span> <span data-ttu-id="7d7b0-107">Ja lietojat noliktavas vadību, ir divi veidi, kā izveidot preču transporta pavadzīmi:</span><span class="sxs-lookup"><span data-stu-id="7d7b0-107">If you're using warehouse management, there are two ways to generate a bill of lading:</span></span>

  -   <span data-ttu-id="7d7b0-108">Izveidojiet pārskatu manuāli, izmantojot lapu **Preču transporta pavadzīme**.</span><span class="sxs-lookup"><span data-stu-id="7d7b0-108">Create the report manually, using the **Bill of lading** page.</span></span>
  -   <span data-ttu-id="7d7b0-109">Ģenerējiet pārskatu no sadaļas **Kravu plānošanas rīks**.</span><span class="sxs-lookup"><span data-stu-id="7d7b0-109">Generate the report from the **Load planning workbench**.</span></span>

<span data-ttu-id="7d7b0-110">Ja ģenerējat preču transporta pavadzīmi no sadaļas **Kravu plānošanas rīks**, kravas statusam jābūt **Nosūtīts.**</span><span class="sxs-lookup"><span data-stu-id="7d7b0-110">If you generate the bill of lading from the **Load planning workbench**, the load status must be **Shipped.**</span></span> <span data-ttu-id="7d7b0-111">Ja kravā ir vairāki sūtījumi, preču transporta pavadzīme tiek izveidota katram sūtījumam.</span><span class="sxs-lookup"><span data-stu-id="7d7b0-111">If there's more than one shipment in the load, a bill of lading is created for each shipment.</span></span> <span data-ttu-id="7d7b0-112">Pēc preču transporta pavadzīmes izveidošanas izmaiņas tai varat veikt lapā **Preču transporta pavadzīme**.</span><span class="sxs-lookup"><span data-stu-id="7d7b0-112">After a bill of lading has been created you can make changes to it on the **Bill of lading** page.</span></span>

## <a name="master-bill-of-lading"></a><span data-ttu-id="7d7b0-113">Apvienotā preču transporta pavadzīme</span><span class="sxs-lookup"><span data-stu-id="7d7b0-113">Master bill of lading</span></span>
<span data-ttu-id="7d7b0-114">Ja kravā ir vairāki sūtījumi, varat ģenerēt apvienotu preču transporta pavadzīmi.</span><span class="sxs-lookup"><span data-stu-id="7d7b0-114">If there's more than one shipment in the load, you can generate a master bill of lading.</span></span> <span data-ttu-id="7d7b0-115">Tai ir tāds pats izkārtojums un informācija kā preču transporta pavadzīmei, bet tā satur apkopotu visu sūtījumu saturu.</span><span class="sxs-lookup"><span data-stu-id="7d7b0-115">This has the same layout and information as a bill of lading, but contains the summarized content for all the shipments.</span></span> <span data-ttu-id="7d7b0-116">Ja opcijai **Izveidot apvienoto preču transporta pavadzīmi, ja kravā ir vairāki sūtījumi** ir iestatīts vienums **Jā** lapā **Transportēšanas pārvaldības parametri**, apvienotā preču transporta pavadzīme tiek ģenerēta automātiski, ja tiek izveidota preču transporta pavadzīme no sadaļas **Kravu plānošanas rīks** un ja ir vairāk nekā viens sūtījums.</span><span class="sxs-lookup"><span data-stu-id="7d7b0-116">If the **Create a master bill of lading when there's more than one shipment on a load** option is set to **Yes** on the **Transportation management parameters** page, a master bill of lading is automatically generated if you create a bill of lading from the **Load planning workbench**, and there's more than one shipment.</span></span> <span data-ttu-id="7d7b0-117">Varat arī skatīt preču transporta pavadzīmju sarakstu, noklikšķinot uz **Saistītā informācija** &gt; **Preču transporta pavadzīme**.</span><span class="sxs-lookup"><span data-stu-id="7d7b0-117">You can also get a list of the bills of lading by clicking **Related information** &gt; **Bill of lading**.</span></span> <span data-ttu-id="7d7b0-118">Ja veidojat preču transporta pavadzīmes manuāli, varat izveidot pvienotu preču transporta pavadzīmi lapā **Preču transporta pavadzīme**.</span><span class="sxs-lookup"><span data-stu-id="7d7b0-118">If you're creating bills of lading manually, you can create a master bill of lading on the **Bill of lading** page.</span></span>



