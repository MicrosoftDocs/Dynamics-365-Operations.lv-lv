---
title: Papildobjekta piešķires iestatīšana
description: Šajā procedūrā parādīts, kā iestatīt papildobjekta piešķiri.
author: ShylaThompson
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSAccessorialAssignment
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 06139e87596965a481fc7fb2e2f653594be0ac1e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838470"
---
# <a name="set-up-accessorial-assignments"></a><span data-ttu-id="60e91-103">Papildobjekta piešķires iestatīšana</span><span class="sxs-lookup"><span data-stu-id="60e91-103">Set up accessorial assignments</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="60e91-104">Šajā procedūrā parādīts, kā iestatīt papildobjekta piešķiri.</span><span class="sxs-lookup"><span data-stu-id="60e91-104">This procedure shows how to set up an accessorial assignment.</span></span> <span data-ttu-id="60e91-105">To parasti veic transportēšanas koordinators.</span><span class="sxs-lookup"><span data-stu-id="60e91-105">This is typically done by a transportation coordinator.</span></span> <span data-ttu-id="60e91-106">Pirms šī ceļveža izmantošanas nepieciešams izpildīt ceļvedi Pārkraušanas punkta papildobjekta maksas un pārkraušanas šablonu iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="60e91-106">Before you use this guide you need to run the "Set up hub accessorial charges and accessorial masters" guide.</span></span>


## <a name="set-up-accessorial-assignment"></a><span data-ttu-id="60e91-107">Papildobjekta piešķiru iestatīšana</span><span class="sxs-lookup"><span data-stu-id="60e91-107">Set up Accessorial assignment</span></span>
1. <span data-ttu-id="60e91-108">Dodieties uz Transportēšanas pārvaldība > Iestatīšana > Vērtējums > Papildobjekta piešķires.</span><span class="sxs-lookup"><span data-stu-id="60e91-108">Go to Transportation management > Setup > Rating > Accessorial assignments.</span></span>
2. <span data-ttu-id="60e91-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="60e91-109">Click New.</span></span>
3. <span data-ttu-id="60e91-110">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="60e91-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="60e91-111">Pārslēdziet sadaļas Detalizēti paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="60e91-111">Toggle the expansion of the Details section.</span></span>
5. <span data-ttu-id="60e91-112">Laukā Pārkraušanas punkts noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="60e91-112">In the Hub field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="60e91-113">Sarakstā atlasiet pārkraušanas punktu, kuram izveidojāt pārkraušanas šablonu ceļvedī Pārkraušanas punkta papildobjekta maksas un pārkraušanas šablonu iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="60e91-113">In the list, select the Hub that you created an accessorial master for when you ran the "Set up hub accessorial charges and accessorial masters" guide.</span></span> 
7. <span data-ttu-id="60e91-114">Laukā Pārkraušanas punkta papildobjekta ID noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="60e91-114">In the Hub accessorial ID field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="60e91-115">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="60e91-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="60e91-116">Pārslēdziet sadaļas Kritēriji paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="60e91-116">Toggle the expansion of the Criteria section.</span></span>
    * <span data-ttu-id="60e91-117">Sadaļā Kritēriji varat izvēlēties precīzus kritērijus, kad vajadzētu piemērot maksas, pamatojoties uz dažādām šeit piedāvātām vērtībām.</span><span class="sxs-lookup"><span data-stu-id="60e91-117">In the Criteria section you can choose the exact criteria for when the charge should apply, based on the different values offered here.</span></span>  
10. <span data-ttu-id="60e91-118">Iestatiet opcijas Vienmēr lietot vērtību uz Jā.</span><span class="sxs-lookup"><span data-stu-id="60e91-118">Set the Always apply option to Yes.</span></span>
11. <span data-ttu-id="60e91-119">Atlasiet opciju laukā Papildobjekta piešķires līmenis.</span><span class="sxs-lookup"><span data-stu-id="60e91-119">In the Accessorial assignment level field, select an option.</span></span>
12. <span data-ttu-id="60e91-120">Pārslēdziet sadaļas Aprēķins paplašinājumu.</span><span class="sxs-lookup"><span data-stu-id="60e91-120">Toggle the expansion of the Calculation section.</span></span>
13. <span data-ttu-id="60e91-121">Laukā Papildobjekta maksas tips atlasiet "Pamatlikme".</span><span class="sxs-lookup"><span data-stu-id="60e91-121">In the Accessorial fee type field, select 'Flat'.</span></span>
    * <span data-ttu-id="60e91-122">Papildobjekta maksas veids nosaka, kā aprēķināt faktisko maksu.</span><span class="sxs-lookup"><span data-stu-id="60e91-122">The Accessorial fee type determines how to calculate the actual charge.</span></span> <span data-ttu-id="60e91-123">Šajā piemērā tiek izmantota noteikta maksa.</span><span class="sxs-lookup"><span data-stu-id="60e91-123">In this example it's a flat charge.</span></span>  
14. <span data-ttu-id="60e91-124">Ievadiet skaitli laukā Papildobjekta maksa.</span><span class="sxs-lookup"><span data-stu-id="60e91-124">In the Accessorial fee field, enter a number.</span></span>
15. <span data-ttu-id="60e91-125">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="60e91-125">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]