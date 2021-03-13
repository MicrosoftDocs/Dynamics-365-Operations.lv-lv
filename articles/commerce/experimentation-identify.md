---
title: Hipotēzes identificēšana un eksperimenta rādītāju noteikšana
description: Šajā tēmā ir aprakstīts, kā identificēt hipotēzi un panākumu rādītājus eksperimentam, ko izpildāt e-komercijas tīmekļa vietnē pakalpojumā Dynamics 365 Commerce.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 5594b81d09eade263487244a14c0305d589ff94e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010003"
---
# <a name="identify-a-hypothesis-and-determine-success-metrics-for-an-experiment"></a><span data-ttu-id="5ca52-103">Hipotēzes identificēšana un eksperimenta panākumu rādītāju noteikšana</span><span class="sxs-lookup"><span data-stu-id="5ca52-103">Identify a hypothesis and determine success metrics for an experiment</span></span>
<span data-ttu-id="5ca52-104">Pirmā eksperimenta dzīves cikla fāze ietver eksperimenta hipotēzes identificēšanu un rādītāju noteikšanu, kam sekosit, lai novērtētu panākumus.</span><span class="sxs-lookup"><span data-stu-id="5ca52-104">The first phase in the experimentation lifecycle includes identifying the hypothesis for the experiment and determining the metrics you'll track to evaluate success.</span></span> <span data-ttu-id="5ca52-105">Tālāk esošajā diagrammā ir parādītas visas darbības, kas jāveic, lai [iestatītu un izpildītu eksperimentu](experimentation-overview.md) e-komercijas tīmekļa vietnē pakalpojumā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5ca52-105">The following diagram shows all of the steps involved in [setting up and running an experiment](experimentation-overview.md) on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="5ca52-106">Papildu darbības ir apskatītas atsevišķās tēmās.</span><span class="sxs-lookup"><span data-stu-id="5ca52-106">Additional steps are covered in separate topics.</span></span> 

<span data-ttu-id="5ca52-107">[ ![Eksperimenta lietotāja maršruts – identificēšana](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="5ca52-107">[ ![Experimentation user journey - Identify](./media/experimentation_identify.svg) ](./media/experimentation_identify.svg#lightbox)</span></span>

<span data-ttu-id="5ca52-108">Hipotēze ir apgalvojums, kurā prognozēts eksperimenta rezultāts.</span><span class="sxs-lookup"><span data-stu-id="5ca52-108">A hypothesis is a statement where you predict the outcome of the experiment.</span></span> <span data-ttu-id="5ca52-109">Hipotēzes definēšanā ir iesaistīti daudzi faktori, piemēram, lietotāju uzvedības un apkopoto tīmekļa vietņu datu izpēte.</span><span class="sxs-lookup"><span data-stu-id="5ca52-109">Many factors go into defining a hypothesis, for example, research about user behavior and website data you've collected.</span></span> <span data-ttu-id="5ca52-110">Ar hipotēzi jūs definēsit pieņēmumu vai teoriju, kuru vēlaties apstiprināt ar savu eksperimentu.</span><span class="sxs-lookup"><span data-stu-id="5ca52-110">With the hypothesis, you'll define the assumption or theory you want to validate with your experiment.</span></span> <span data-ttu-id="5ca52-111">Eksperimenta hipotēzes piemērs varētu būt “*Vasaras mēnešos attēls ar baltas krāsas t-kreklu manā mājas lapā radīs lielāku vidējo klikšķu skaitu nekā tumši zils džemperis, jo vasarā cilvēki vēlas valkāt kaut ko plānu un gaišās krāsās.*”</span><span class="sxs-lookup"><span data-stu-id="5ca52-111">An example of a hypothesis for your experiment may be "*a picture of a white t-shirt on my home page will drive a higher clickthrough rate than a navy sweater during summer months because people want to wear something lightweight and light colored in the summer.*"</span></span> <span data-ttu-id="5ca52-112">Šādā gadījumā jūs izveidosit variantus, kas ietver baltu t-kreklu un tumši zilu džemperi, un abus publicēsit vienlaicīgi.</span><span class="sxs-lookup"><span data-stu-id="5ca52-112">In that case, you'll create variations that include a white t-shirt and a navy sweater, and publish both at the same time.</span></span>

<span data-ttu-id="5ca52-113">Lai apstiprinātu hipotēzi, eksperimenta sekmībai vai nesekmībai jābūt tieši saistītai ar lietotāja darbībām, piemēram, vai tīmekļa vietnes lietotājs noklikšķina uz saites vai pogas.</span><span class="sxs-lookup"><span data-stu-id="5ca52-113">To validate a hypothesis, the success or failure of an experiment should be directly tied to user actions; for example, if the website user clicks on a link or button.</span></span> <span data-ttu-id="5ca52-114">Šīm darbībām jāatbilst notikumiem, par kuriem tiks ziņots trešās puses pakalpojumam, kas seko eksperimentam.</span><span class="sxs-lookup"><span data-stu-id="5ca52-114">These actions must correspond with events that will be reported to the third-party service tracking the experiment.</span></span> <span data-ttu-id="5ca52-115">Laika gaitā to lietotāju procentuālais īpatsvars, kuri veic šo darbību, tiks aprēķināts kā rādītāji, ko varat izmantot, lai veidotu pārskatus un veiktu analīzes.</span><span class="sxs-lookup"><span data-stu-id="5ca52-115">Over time, the percentage of users that take the action will be tallied as a metric you can use to generate reports and conduct analyses.</span></span> <span data-ttu-id="5ca52-116">Lai pārskatītu visus pieejamos notikumus un atribūtus, skatiet tēmu [Commerce komponentu notikumi diagnostikai un problēmu novēršanai](dev-itpro/retail-component-events-diagnostics-troubleshooting.md), .</span><span class="sxs-lookup"><span data-stu-id="5ca52-116">To review all of the available events and attributes, see [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span></span>

## <a name="previous-step"></a><span data-ttu-id="5ca52-117">Iepriekšējā darbība</span><span class="sxs-lookup"><span data-stu-id="5ca52-117">Previous step</span></span>
[<span data-ttu-id="5ca52-118">Eksperimentēšana pakalpojumā Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="5ca52-118">Experimentation in Dynamics 365 Commerce</span></span>](experimentation-overview.md)


## <a name="next-step"></a><span data-ttu-id="5ca52-119">Nākamā darbība</span><span class="sxs-lookup"><span data-stu-id="5ca52-119">Next step</span></span>
[<span data-ttu-id="5ca52-120">Eksperimenta iestatīšana</span><span class="sxs-lookup"><span data-stu-id="5ca52-120">Set up an experiment</span></span>](experimentation-setup.md)
