---
title: Nevar noņemt noliktavas pieprasījuma apjoma prognozes dimensiju no prognozes rindām
description: Nevar noņemt noliktavas pieprasījuma apjoma prognozes dimensiju no prognozes rindām.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 6b643c4fe51ae6ce73b34ab81d4e458dcd5032df
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026714"
---
# <a name="you-cant-remove-the-warehouse-demand-forecast-dimension-from-forecast-lines"></a><span data-ttu-id="abcbc-103">Nevar noņemt noliktavas pieprasījuma apjoma prognozes dimensiju no prognozes rindām</span><span class="sxs-lookup"><span data-stu-id="abcbc-103">You can't remove the Warehouse demand forecast dimension from forecast lines</span></span>

<span data-ttu-id="abcbc-104">KB numurs: 4614408</span><span class="sxs-lookup"><span data-stu-id="abcbc-104">KB number: 4614408</span></span>

## <a name="symptoms"></a><span data-ttu-id="abcbc-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="abcbc-105">Symptoms</span></span>

<span data-ttu-id="abcbc-106">Šī problēma rodas, ja **Noliktavas** dimensija nav piešķirta cilnes **Prognozes dimensijas** laukā **Pieprasījuma apjoma prognozes parametri**.</span><span class="sxs-lookup"><span data-stu-id="abcbc-106">This issue occurs when the **Warehouse** dimension isn't assigned on the **Forecast dimensions** tab of the **Demand forecasting parameter** page.</span></span> <span data-ttu-id="abcbc-107">Tomēr kolonna **Noliktava** tiek parādīta lapā **Pieprasījuma apjoma prognoze** (**Vispārējā plānošana \> Prognozēšana \> Manuālās prognozes elements \> Pieprasījuma apjoma prognozes rindas**).</span><span class="sxs-lookup"><span data-stu-id="abcbc-107">Nevertheless, the **Warehouse** column is shown on the **Demand forecast** page (**Master planning \> Forecasting \> Manual forecast entity \> Demand forecast lines**).</span></span>

## <a name="resolution"></a><span data-ttu-id="abcbc-108">Novēršana</span><span class="sxs-lookup"><span data-stu-id="abcbc-108">Resolution</span></span>

<span data-ttu-id="abcbc-109">Cilnes **Prognozes dimensijas** iestatījumi lapā **Pieprasījuma apjoma prognozes parametri** neietekmē lapu **Pieprasījuma apjoma prognoze**.</span><span class="sxs-lookup"><span data-stu-id="abcbc-109">The settings on the **Forecast dimensions** tab of the **Demand forecasting parameter** page don't affect the **Demand forecast** page.</span></span> <span data-ttu-id="abcbc-110">Tie kontrolē bāzlīnijas prognozi, kas tiek ģenerēta un parādīta pielāgotajā pieprasījuma apjoma prognozē.</span><span class="sxs-lookup"><span data-stu-id="abcbc-110">They control the baseline forecast that is generated and shown in the adjusted demand forecast.</span></span> <span data-ttu-id="abcbc-111">Tomēr tie nekontrolē dimensijas, kas ir nepieciešamas "reālajai" pieprasījuma apjoma prognozei.</span><span class="sxs-lookup"><span data-stu-id="abcbc-111">However, they don't control the dimensions that are required for the "real" demand forecast.</span></span> <span data-ttu-id="abcbc-112">Autorizējot ierakstus, kas tiek rādīti lapā **Pielāgotā pieprasījuma apjoma prognoze**, tos var pārveidot par "reāliem" prognozes modeļa ierakstiem.</span><span class="sxs-lookup"><span data-stu-id="abcbc-112">By authorizing the records that are shown on the **Adjusted demand forecast** page, you can convert them to "real" forecast entries for a forecast model.</span></span> <span data-ttu-id="abcbc-113">Šo modeli pēc tam var izmantot vispārējai plānošanai.</span><span class="sxs-lookup"><span data-stu-id="abcbc-113">That model can then be used for master planning.</span></span>

<span data-ttu-id="abcbc-114">Lapā **Pieprasījuma apjoma prognoze** "reālās" prognozes dimensijas, kas parādītas pieprasījuma apjoma prognožu rindās, ir daļa no krājumu dimensijām.</span><span class="sxs-lookup"><span data-stu-id="abcbc-114">On the **Demand forecast** page, the dimensions for the "real" forecast that are shown on the demand forecast lines are part of the inventory dimensions.</span></span> <span data-ttu-id="abcbc-115">(Šī darbība ir līdzīga pārdošanas pasūtījumu rindu uzvedībai.) Ja jūsu sistēmā nav iestatīts lietot **Noliktavu** kā obligātu krājumu dimensiju, lapu var pielāgot, lai paslēptu kolonnu.</span><span class="sxs-lookup"><span data-stu-id="abcbc-115">(This behavior resembles the behavior for sales order lines.) If your system isn't set up to use **Warehouse** as a mandatory inventory dimension, you can customize the page to hide the column.</span></span>
