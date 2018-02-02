--- 
title: "Amata pārskatu attiecību modificēšana"
description: "Šajā procedūrā ir aprakstīts, kā mainīt darbinieka pakļautības attiecības."
author: ShielaSogge
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a9d0d9a3f278a09e89311ee75b6f95fb4f3b04cb
ms.openlocfilehash: 6e8028689d20dd1310dfb89766db3eea3218fc90
ms.contentlocale: lv-lv
ms.lasthandoff: 02/02/2018

---
# <a name="modify-reporting-relationships-for-a-position"></a><span data-ttu-id="09bf3-103">Amata pārskatu attiecību modificēšana</span><span class="sxs-lookup"><span data-stu-id="09bf3-103">Modify reporting relationships for a position</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="09bf3-104">Šajā procedūrā ir aprakstīts, kā mainīt darbinieka pakļautības attiecības.</span><span class="sxs-lookup"><span data-stu-id="09bf3-104">This procedure shows how to change the reporting relationship for an employee.</span></span> <span data-ttu-id="09bf3-105">Pakļautības attiecības var izmantot dokumentu virzībai darbplūsmā.</span><span class="sxs-lookup"><span data-stu-id="09bf3-105">The reporting relationship can be used for routing documents through workflow.</span></span> <span data-ttu-id="09bf3-106">Procedūrā arī paskaidrots, kā darbinieku piešķirt papildu hierarhijām.</span><span class="sxs-lookup"><span data-stu-id="09bf3-106">The procedure also shows how to assign the employee to additional hierarchies.</span></span> <span data-ttu-id="09bf3-107">Piemēram, darbinieks var projekta grupas loceklis ar neoficiālām pakļautības attiecībām ar projekta vadītāju.</span><span class="sxs-lookup"><span data-stu-id="09bf3-107">For example, an employee might be a part of a project team with an informal reporting relationship to a project supervisor.</span></span> <span data-ttu-id="09bf3-108">Amatam var definēt papildu pakļautības attiecības, lai izpildītu atšķirīgus projekta vai matricas scenārijus.</span><span class="sxs-lookup"><span data-stu-id="09bf3-108">Additional reporting relationships can be defined on the position to accommodate various project or matrix scenarios.</span></span> <span data-ttu-id="09bf3-109">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="09bf3-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="09bf3-110">Pārejiet uz sadaļu Personāla vadība > Amati > Amati.</span><span class="sxs-lookup"><span data-stu-id="09bf3-110">Go to Human resources > Positions > Positions.</span></span>
2. <span data-ttu-id="09bf3-111">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="09bf3-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="09bf3-112">Piemēram, filtrējiet pēc lauka Amats, izmantojot vērtību 000091.</span><span class="sxs-lookup"><span data-stu-id="09bf3-112">For example, filter on the Position field with a value of '000091'.</span></span>
3. <span data-ttu-id="09bf3-113">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="09bf3-113">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="09bf3-114">Izvērsiet sadaļu Pakļautās personas amats.</span><span class="sxs-lookup"><span data-stu-id="09bf3-114">Expand the Reports to position section.</span></span>
5. <span data-ttu-id="09bf3-115">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="09bf3-115">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="09bf3-116">Laukā Pakļautība ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="09bf3-116">In the Reports to field, enter or select a value.</span></span>
7. <span data-ttu-id="09bf3-117">Noklikšķiniet uz Izveidot.</span><span class="sxs-lookup"><span data-stu-id="09bf3-117">Click Create.</span></span>
8. <span data-ttu-id="09bf3-118">Izvērsiet sadaļu Attiecības.</span><span class="sxs-lookup"><span data-stu-id="09bf3-118">Expand the Relationships section.</span></span>
9. <span data-ttu-id="09bf3-119">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="09bf3-119">Click Add.</span></span>
10. <span data-ttu-id="09bf3-120">Atzīmējiet izvēles rūtiņu, kura atrodas pa kreisi no režģa.</span><span class="sxs-lookup"><span data-stu-id="09bf3-120">Select the check box on the left of the grid.</span></span>
11. <span data-ttu-id="09bf3-121">Laukā Hierarhijas nosaukums ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="09bf3-121">In the Hierarchy name field, enter or select a value.</span></span>
    * <span data-ttu-id="09bf3-122">Piemērs: Projekts</span><span class="sxs-lookup"><span data-stu-id="09bf3-122">Example: Project</span></span>  
12. <span data-ttu-id="09bf3-123">Laukā Pakļautās personas amats ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="09bf3-123">In the Reports to position field, enter or select a value.</span></span>  <span data-ttu-id="09bf3-124">Piemērs: 000437</span><span class="sxs-lookup"><span data-stu-id="09bf3-124">Example:  000437</span></span>
13. <span data-ttu-id="09bf3-125">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="09bf3-125">Click Save.</span></span>


