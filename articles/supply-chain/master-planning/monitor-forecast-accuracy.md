---
title: "Prognozes precizitātes pārraudzība"
description: "Šajā rakstā ir aprakstīti programmatūrā Microsoft Dynamics 365 for Finance and Operations aprēķināto prognožu precizitātes tipi, un ir paskaidrots, kā varat skatīt precizitātes vērtības."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c2f9482a9906ad6c607d275769ac06b29b22c25d
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="monitor-forecast-accuracy"></a><span data-ttu-id="1e795-103">Prognozes precizitātes pārraudzība</span><span class="sxs-lookup"><span data-stu-id="1e795-103">Monitor forecast accuracy</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1e795-104">Šajā rakstā ir aprakstīti programmatūrā Microsoft Dynamics 365 for Finance and Operations aprēķināto prognožu precizitātes tipi, un ir paskaidrots, kā varat skatīt precizitātes vērtības.</span><span class="sxs-lookup"><span data-stu-id="1e795-104">This article describes the types of forecast accuracy that Microsoft Dynamics 365 for Finance and Operations calculates, and explains how you can view the accuracy values.</span></span>

<span data-ttu-id="1e795-105">Programmatūrā Finance and Operations tiek aprēķināti tālāk norādītie prognozes precizitātes tipi.</span><span class="sxs-lookup"><span data-stu-id="1e795-105">Finance and Operations calculates the following types of forecast accuracy:</span></span>

-   <span data-ttu-id="1e795-106">Vēsturiskās prognozes precizitāte, salīdzinot vēsturisko prognozi, ko izmanto vispārējā plānošanā kopā ar vēsturiskā pieprasījuma datiem.</span><span class="sxs-lookup"><span data-stu-id="1e795-106">Historical forecast accuracy, by comparing the historical forecast that Master Planning uses with the historical demand.</span></span> <span data-ttu-id="1e795-107">Lai skatītu vēsturiskās prognozes precizitātes vērtības (gan absolūtās, gan procentuālās vērtības), noklikšķiniet uz **Rādīt precizitāti** lapā **Detalizēti pieprasījuma apjoma prognozes dati**.</span><span class="sxs-lookup"><span data-stu-id="1e795-107">To view the values (both absolute values and percentage values) for historical forecast accuracy, click **Show accuracy** on the **Demand forecast details** page.</span></span>
-   <span data-ttu-id="1e795-108">Prognožu ģenerēšanai izmantotā prognozēšanas modeļa aprēķināta precizitāte.</span><span class="sxs-lookup"><span data-stu-id="1e795-108">The estimated accuracy of the forecasting model that is used to generate the predictions.</span></span> <span data-ttu-id="1e795-109">Procentuālo precizitāti var skatīt sadaļā **Detalizēti modeļa dati - MAPE** lapā **Detalizēti pieprasījuma apjoma prognozes dati**.</span><span class="sxs-lookup"><span data-stu-id="1e795-109">You can view the accuracy percentage under **Model details - MAPE** on the **Demand forecast details** page.</span></span> 

<span data-ttu-id="1e795-110">**Piezīme.** Ja izmantojat Finance and Operations Microsoft Azure algoritmiskās mācīšanās pakalpojumu Pieprasījuma prognozēšana, iekšējā modeļa precizitāte tiek aprēķināta, pamatojoties uz testa datu kopu.</span><span class="sxs-lookup"><span data-stu-id="1e795-110">**Note:** If you use the Finance and Operations Demand forecasting Microsoft Azure Machine Learning service, the calculation of internal model accuracy is based on the test data set.</span></span> <span data-ttu-id="1e795-111">ai norādītu testa datu kopas izmēru, iestatiet parametru **TEST\_SET\_SIZE\_PERCENT** lapā **Pieprasījuma prognozēšanas parametri**.</span><span class="sxs-lookup"><span data-stu-id="1e795-111">To specify the size of the test data set, set the **TEST\_SET\_SIZE\_PERCENT** parameter on the **Demand forecasting parameters** page.</span></span> <span data-ttu-id="1e795-112">Piemēram, ja tiek iestatīta vērtība **20**, pēdējie vēsturisko datu 20 % tiks izmantoti, lai aprēķinātu iekšējā modeļa precizitāti.</span><span class="sxs-lookup"><span data-stu-id="1e795-112">For example, if you set the value to **20**, the last 20 percent of the historical data will be used to calculate the internal model accuracy.</span></span>


<a name="see-also"></a><span data-ttu-id="1e795-113">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="1e795-113">See also</span></span>
--------

[<span data-ttu-id="1e795-114">Koriģētās prognozes autorizēšana</span><span class="sxs-lookup"><span data-stu-id="1e795-114">Authorizing the adjusted forecast</span></span>](authorize-adjusted-forecast.md)

[<span data-ttu-id="1e795-115">Novirzes punktu noņemšana no vēsturiskiem transakciju datiem, aprēķinot pieprasījuma apjoma prognozi</span><span class="sxs-lookup"><span data-stu-id="1e795-115">Remove outliers from historical transaction data when calculating a demand forecast</span></span>](remove-historical-outliers-calculating-demand-forecast.md)




