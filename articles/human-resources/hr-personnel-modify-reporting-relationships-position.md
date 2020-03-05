---
title: Amata pārskatu attiecību modificēšana
description: Šajā procedūrā ir aprakstīts, kā mainīt darbinieka pakļautības attiecības.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmPosition, HcmPositionReportsToDialog, HcmPositionLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3285222b11905999f0eadb846ac785342c16aa38
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009836"
---
# <a name="modify-reporting-relationships-for-a-position"></a><span data-ttu-id="dd924-103">Amata pārskatu attiecību modificēšana</span><span class="sxs-lookup"><span data-stu-id="dd924-103">Modify reporting relationships for a position</span></span>



<span data-ttu-id="dd924-104">Šajā procedūrā ir aprakstīts, kā mainīt darbinieka pakļautības attiecības.</span><span class="sxs-lookup"><span data-stu-id="dd924-104">This procedure shows how to change the reporting relationship for an employee.</span></span> <span data-ttu-id="dd924-105">Pakļautības attiecības var izmantot dokumentu virzībai darbplūsmā.</span><span class="sxs-lookup"><span data-stu-id="dd924-105">The reporting relationship can be used for routing documents through workflow.</span></span> <span data-ttu-id="dd924-106">Procedūrā arī paskaidrots, kā darbinieku piešķirt papildu hierarhijām.</span><span class="sxs-lookup"><span data-stu-id="dd924-106">The procedure also shows how to assign the employee to additional hierarchies.</span></span> <span data-ttu-id="dd924-107">Piemēram, darbinieks var projekta grupas loceklis ar neoficiālām pakļautības attiecībām ar projekta vadītāju.</span><span class="sxs-lookup"><span data-stu-id="dd924-107">For example, an employee might be a part of a project team with an informal reporting relationship to a project supervisor.</span></span> <span data-ttu-id="dd924-108">Amatam var definēt papildu pakļautības attiecības, lai izpildītu atšķirīgus projekta vai matricas scenārijus.</span><span class="sxs-lookup"><span data-stu-id="dd924-108">Additional reporting relationships can be defined on the position to accommodate various project or matrix scenarios.</span></span> <span data-ttu-id="dd924-109">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="dd924-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="dd924-110">Pārejiet uz sadaļu Personāla vadība > Amati > Amati.</span><span class="sxs-lookup"><span data-stu-id="dd924-110">Go to Human resources > Positions > Positions.</span></span>
2. <span data-ttu-id="dd924-111">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="dd924-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="dd924-112">Piemēram, filtrējiet pēc lauka Amats, izmantojot vērtību 000091.</span><span class="sxs-lookup"><span data-stu-id="dd924-112">For example, filter on the Position field with a value of '000091'.</span></span>
3. <span data-ttu-id="dd924-113">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="dd924-113">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="dd924-114">Izvērsiet sadaļu Pakļautās personas amats.</span><span class="sxs-lookup"><span data-stu-id="dd924-114">Expand the Reports to position section.</span></span>
5. <span data-ttu-id="dd924-115">Noklikšķiniet uz Jauns, lai atvērtu nolaižamo dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="dd924-115">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="dd924-116">Laukā Pakļautība ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="dd924-116">In the Reports to field, enter or select a value.</span></span>
7. <span data-ttu-id="dd924-117">Noklikšķiniet uz Izveidot.</span><span class="sxs-lookup"><span data-stu-id="dd924-117">Click Create.</span></span>
8. <span data-ttu-id="dd924-118">Izvērsiet sadaļu Attiecības.</span><span class="sxs-lookup"><span data-stu-id="dd924-118">Expand the Relationships section.</span></span>
9. <span data-ttu-id="dd924-119">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="dd924-119">Click Add.</span></span>
10. <span data-ttu-id="dd924-120">Atzīmējiet izvēles rūtiņu, kura atrodas pa kreisi no režģa.</span><span class="sxs-lookup"><span data-stu-id="dd924-120">Select the check box on the left of the grid.</span></span>
11. <span data-ttu-id="dd924-121">Laukā Hierarhijas nosaukums ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="dd924-121">In the Hierarchy name field, enter or select a value.</span></span>
    * <span data-ttu-id="dd924-122">Piemērs: Projekts</span><span class="sxs-lookup"><span data-stu-id="dd924-122">Example: Project</span></span>  
12. <span data-ttu-id="dd924-123">Laukā Pakļautās personas amats ievadiet vai atlasiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="dd924-123">In the Reports to position field, enter or select a value.</span></span>  <span data-ttu-id="dd924-124">Piemērs: 000437</span><span class="sxs-lookup"><span data-stu-id="dd924-124">Example:  000437</span></span>
13. <span data-ttu-id="dd924-125">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="dd924-125">Click Save.</span></span>
