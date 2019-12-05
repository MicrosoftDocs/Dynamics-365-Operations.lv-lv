---
title: Prognozes precizitātes pārraudzība
description: Šajā tēmā ir aprakstīti programmā Dynamics 365 Supply Chain Management aprēķinātās prognozes precizitātes veidi un ir paskaidrots, kā varat skatīt precizitātes vērtības.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4cf65826279f0741ce5abc89d8f15bfec98c83ef
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813688"
---
# <a name="monitor-forecast-accuracy"></a><span data-ttu-id="56bd1-103">Prognozes precizitātes pārraudzība</span><span class="sxs-lookup"><span data-stu-id="56bd1-103">Monitor forecast accuracy</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="56bd1-104">Šajā tēmā ir aprakstīti programmā Microsoft Dynamics 365 Supply Chain Management aprēķinātās prognozes precizitātes veidi un ir paskaidrots, kā varat skatīt precizitātes vērtības.</span><span class="sxs-lookup"><span data-stu-id="56bd1-104">This topic describes the types of forecast accuracy that Microsoft Dynamics 365 Supply Chain Management calculates, and explains how you can view the accuracy values.</span></span>

<span data-ttu-id="56bd1-105">Supply Chain Management tiek aprēķināti tālāk norādītie prognozes precizitātes tipi.</span><span class="sxs-lookup"><span data-stu-id="56bd1-105">Supply Chain Management calculates the following types of forecast accuracy:</span></span>

-   <span data-ttu-id="56bd1-106">Vēsturiskās prognozes precizitāte, salīdzinot vēsturisko prognozi, ko izmanto vispārējā plānošanā kopā ar vēsturiskā pieprasījuma datiem.</span><span class="sxs-lookup"><span data-stu-id="56bd1-106">Historical forecast accuracy, by comparing the historical forecast that Master Planning uses with the historical demand.</span></span> <span data-ttu-id="56bd1-107">Lai skatītu vēsturiskās prognozes precizitātes vērtības (gan absolūtās, gan procentuālās vērtības), noklikšķiniet uz **Rādīt precizitāti** lapā **Detalizēti pieprasījuma apjoma prognozes dati**.</span><span class="sxs-lookup"><span data-stu-id="56bd1-107">To view the values (both absolute values and percentage values) for historical forecast accuracy, click **Show accuracy** on the **Demand forecast details** page.</span></span>
-   <span data-ttu-id="56bd1-108">Prognožu ģenerēšanai izmantotā prognozēšanas modeļa aprēķināta precizitāte.</span><span class="sxs-lookup"><span data-stu-id="56bd1-108">The estimated accuracy of the forecasting model that is used to generate the predictions.</span></span> <span data-ttu-id="56bd1-109">Procentuālo precizitāti var skatīt sadaļā **Detalizēti modeļa dati - MAPE** lapā **Detalizēti pieprasījuma apjoma prognozes dati**.</span><span class="sxs-lookup"><span data-stu-id="56bd1-109">You can view the accuracy percentage under **Model details - MAPE** on the **Demand forecast details** page.</span></span> 

> [!NOTE]
> <span data-ttu-id="56bd1-110">Ja izmantojat Microsoft Azure algoritmiskās mācīšanās pakalpojumu pieprasījuma prognozēšana, iekšējā modeļa precizitāte tiek aprēķināta, pamatojoties uz testa datu kopu.</span><span class="sxs-lookup"><span data-stu-id="56bd1-110">If you use the Demand forecasting Microsoft Azure Machine Learning service, the calculation of internal model accuracy is based on the test data set.</span></span> <span data-ttu-id="56bd1-111">ai norādītu testa datu kopas izmēru, iestatiet parametru **TEST\_SET\_SIZE\_PERCENT** lapā **Pieprasījuma prognozēšanas parametri**.</span><span class="sxs-lookup"><span data-stu-id="56bd1-111">To specify the size of the test data set, set the **TEST\_SET\_SIZE\_PERCENT** parameter on the **Demand forecasting parameters** page.</span></span> <span data-ttu-id="56bd1-112">Piemēram, ja tiek iestatīta vērtība **20**, pēdējie vēsturisko datu 20 % tiks izmantoti, lai aprēķinātu iekšējā modeļa precizitāti.</span><span class="sxs-lookup"><span data-stu-id="56bd1-112">For example, if you set the value to **20**, the last 20 percent of the historical data will be used to calculate the internal model accuracy.</span></span>


<a name="additional-resources"></a><span data-ttu-id="56bd1-113">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="56bd1-113">Additional resources</span></span>
--------

[<span data-ttu-id="56bd1-114">Autorizēt koriģēto pieprasījuma apjoma prognozi</span><span class="sxs-lookup"><span data-stu-id="56bd1-114">Authorize an adjusted forecast</span></span>](authorize-adjusted-forecast.md)

[<span data-ttu-id="56bd1-115">Novirzes punktu noņemšana no vēsturiskiem transakciju datiem, aprēķinot pieprasījuma apjoma prognozi</span><span class="sxs-lookup"><span data-stu-id="56bd1-115">Remove outliers from historical transaction data when calculating a demand forecast</span></span>](remove-historical-outliers-calculating-demand-forecast.md)



