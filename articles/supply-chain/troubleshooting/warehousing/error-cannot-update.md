---
title: Kļūda rodas, ja izdošanas saraksta reģistrācijas laikā ir atlasīta atrašanās vieta
description: Kļūda rodas, ja izdošanas saraksta reģistrācijas laikā ir atlasīta atrašanās vieta.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b7fc579821f9a80d94aea949fcc0301b9d8f6935
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026695"
---
# <a name="an-error-occurs-when-the-location-is-selected-during-picking-list-registration"></a><span data-ttu-id="9b147-103">Kļūda rodas, ja izdošanas saraksta reģistrācijas laikā ir atlasīta atrašanās vieta</span><span class="sxs-lookup"><span data-stu-id="9b147-103">An error occurs when the location is selected during picking list registration</span></span>

<span data-ttu-id="9b147-104">KB numurs: 4613106</span><span class="sxs-lookup"><span data-stu-id="9b147-104">KB number: 4613106</span></span>

## <a name="symptoms"></a><span data-ttu-id="9b147-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="9b147-105">Symptoms</span></span>

<span data-ttu-id="9b147-106">Šī problēma rodas, kad sistēma ir konfigurēta tā, lai automātiski rezervētu pārdošanas pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="9b147-106">This issue occurs when your system is configured to automatically reserve sales orders.</span></span> <span data-ttu-id="9b147-107">Ja mēģināsiet atlasīt izdošanas saraksta reģistrācijas rindas atrašanās vietu, jūs saņemat šādu kļūdas ziņojumu, kad izmantojat noliktavas vadības (WMS) rezervācijas procesus:</span><span class="sxs-lookup"><span data-stu-id="9b147-107">If you try to select the location for a picking list registration line, you receive the following error message when you use warehouse management (WMS) reservation processes:</span></span>

> <span data-ttu-id="9b147-108">Nevar atjaunināt daudzumu, izmantojot jaunas dimensijas</span><span class="sxs-lookup"><span data-stu-id="9b147-108">Can't update quantity with new dimensions</span></span>

<span data-ttu-id="9b147-109">Šī problēma var rasties, jo norādītajā vietā nepietiek rīcībā esošo krājumu.</span><span class="sxs-lookup"><span data-stu-id="9b147-109">This issue can occur because you don't have enough on-hand inventory at a specified location.</span></span>

## <a name="resolution"></a><span data-ttu-id="9b147-110">Novēršana</span><span class="sxs-lookup"><span data-stu-id="9b147-110">Resolution</span></span>

<span data-ttu-id="9b147-111">Sistēma darbojas kā paredzēts.</span><span class="sxs-lookup"><span data-stu-id="9b147-111">The system is behaving as designed.</span></span>

<span data-ttu-id="9b147-112">Scenārijos, kuros tiek izmantots noliktavas līmeņa rezervācijas process, ja rīcībā esošie krājumi netiks rezervēti visos krājumu dimensiju līmeņos un norādītajā vietā nav pietiekami daudz rīcībā esošo krājumu, ieteicams izdošanas rindā izmantot manuālo rezervēšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="9b147-112">In scenarios where you use the warehouse-level reservation process, if the on-hand inventory won't be reserved on all inventory dimension levels, and you don't have enough on-hand inventory at a specified location, we recommend that you use the manual reservation process from the picking line.</span></span> <span data-ttu-id="9b147-113">Pēc tam varat izmantot funkciju *Rezervēt laidienu*, lai sadalītu zemākās rezervācijas, piemēram, atrašanās vietu, visiem pieejamajiem rīcībā esošajiem daudzumiem.</span><span class="sxs-lookup"><span data-stu-id="9b147-113">You can then use the *Reserve lot* function to distribute the lower reservations, such as location, for all the available on-hand quantities.</span></span>
