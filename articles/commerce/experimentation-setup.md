---
title: Eksperimenta iestatīšana
description: Šajā tēmā ir aprakstīts, kā iestatīt eksperimentu trešās puses pakalpojumos.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 0f7db0ce009f6ee7603952891aacfdc16fcde016
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930244"
---
# <a name="set-up-an-experiment"></a><span data-ttu-id="1643d-103">Eksperimenta iestatīšana</span><span class="sxs-lookup"><span data-stu-id="1643d-103">Set up an experiment</span></span>

<span data-ttu-id="1643d-104">Kad esat [definējis hipotēzi un noteicis, kādus panākumu rādītājus vēlaties izmantot](experimentation-identify.md), jums ir jāiestata eksperiments trešās puses pakalpojumā.</span><span class="sxs-lookup"><span data-stu-id="1643d-104">After you [define a hypothesis and determine what success metrics you want to use](experimentation-identify.md), you'll need to set up your experiment in the third-party service.</span></span> <span data-ttu-id="1643d-105">Tālāk esošajā diagrammā ir parādītas visas darbības, kas jāveic, lai iestatītu un izpildītu eksperimentu e-komercijas tīmekļa vietnē pakalpojumā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1643d-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="1643d-106">Papildu darbības ir apskatītas atsevišķās tēmās.</span><span class="sxs-lookup"><span data-stu-id="1643d-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="1643d-107">[ ![Eksperimenta lietotāja maršruts – iestatīšana](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="1643d-107">[ ![Experimentation user journey - Setup](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)</span></span>


## <a name="set-up-your-experiment-in-the-third-party-service"></a><span data-ttu-id="1643d-108">Eksperimenta iestatīšana trešās puses pakalpojumā</span><span class="sxs-lookup"><span data-stu-id="1643d-108">Set up your experiment in the third-party service</span></span>
<span data-ttu-id="1643d-109">Jums ir jāizvēlas trešās puses pakalpojums, lai varētu izpildīt un pārraudzīt jūsu eksperimentu un iestatīt eksperimenta savienotāju.</span><span class="sxs-lookup"><span data-stu-id="1643d-109">By now you should have chosen your third-party service to run and monitor your experiment, and set up the experimentation connector.</span></span> <span data-ttu-id="1643d-110">Šie priekšnosacījumi ir uzskaitīti [Eksperimentēšana pakalpojumā Dynamics 365 Commerce](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1643d-110">These prerequisites are listed in  [Experimentation in Dynamics 365 Commerce](experimentation-overview.md).</span></span>

<span data-ttu-id="1643d-111">Izpildiet nepieciešamās darbības, lai izveidotu eksperimentu trešās puses pakalpojumā.</span><span class="sxs-lookup"><span data-stu-id="1643d-111">Follow the steps required to create your experiment in the third-party service.</span></span> <span data-ttu-id="1643d-112">Ja savienotājs ir konfigurēts pareizi, pilns trešās puses pakalpojumā iestatīto eksperimentu saraksts tiks parādīts vietnes veidotājā apmēram 5 minūšu laikā.</span><span class="sxs-lookup"><span data-stu-id="1643d-112">If the connector is configured properly, the complete list of experiments you set up in the third-party service will surface in site builder within about 5 minutes.</span></span>

## <a name="set-up-your-success-metrics"></a><span data-ttu-id="1643d-113">Panākumu rādītāju iestatīšana</span><span class="sxs-lookup"><span data-stu-id="1643d-113">Set up your success metrics</span></span>
<span data-ttu-id="1643d-114">Katram eksperimentam ir nepieciešami rādītāji, lai noteiktu variantu ietekmi un pārbaudītu hipotēzi.</span><span class="sxs-lookup"><span data-stu-id="1643d-114">Every experiment needs metrics to measure the impact of the variations and to validate the hypothesis.</span></span> <span data-ttu-id="1643d-115">Veiciet tālāk norādītās darbības, lai iespējotu rādītāju aprēķināšanu trešās puses pakalpojumā, izmantojot tiešsaistes telemetrijas notikumus no Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1643d-115">Follow the steps below to enable the computation of metrics in the third-party service using live telemetry events from Dynamics 365 Commerce.</span></span>

1. <span data-ttu-id="1643d-116">Vietnes veidotājā atlasiet **Lapas** cilni kreisajā navigācijas rūtī un pēc tam atlasiet lapu, kuras rādītājus vēlaties apkopot.</span><span class="sxs-lookup"><span data-stu-id="1643d-116">In site builder, select the **Pages** tab in the left navigation pane and then select the page that you want to collect metrics on.</span></span> 
1. <span data-ttu-id="1643d-117">Dodieties uz sadaļu **Izsekojamie notikumu ID**, kas atrodas lapas labās puses rekvizītu rūtī vai modulī, kuru vēlaties izsekot.</span><span class="sxs-lookup"><span data-stu-id="1643d-117">Go to the **Event IDs to track** section in the right property pane of the page or module you want to track.</span></span>
1. <span data-ttu-id="1643d-118">Atlasiet **Skatīt**.</span><span class="sxs-lookup"><span data-stu-id="1643d-118">Select **View**.</span></span> <span data-ttu-id="1643d-119">Tiek parādīts visu notikumu ID saraksts.</span><span class="sxs-lookup"><span data-stu-id="1643d-119">A list of all event IDs is displayed.</span></span> <span data-ttu-id="1643d-120">Kopējiet notikumu, kuram vēlaties sekot, un ielīmējiet notikuma atslēgu norādītajā vietā trešās puses pakalpojumā.</span><span class="sxs-lookup"><span data-stu-id="1643d-120">Copy the event you want to track, and paste the event key into the designated location in the third-party service.</span></span> <span data-ttu-id="1643d-121">Ja ir nepieciešams vairāk nekā viens notikums, kopējiet atslēgas pa vienai.</span><span class="sxs-lookup"><span data-stu-id="1643d-121">If you need more than one event, copy the keys one at a time.</span></span> 
    - <span data-ttu-id="1643d-122">Lai uzzinātu, kā skatīt visus pieejamos notikumus un atribūtus, ieskaitot lapu skatījumus un ieņēmumu izsekošanu, skatiet sadaļu [Commerce komponentu notikumi diagnostikai un problēmu novēršanai](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="1643d-122">To learn how to view all of the available events and attributes, including page views and revenue tracking, see [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span></span>
1. <span data-ttu-id="1643d-123">Citas darbības, lai izsekotu rādītājus, veiciet pēc nepieciešamības trešās puses pakalpojumā.</span><span class="sxs-lookup"><span data-stu-id="1643d-123">Take any other steps for tracking metrics as required in the third-party service.</span></span>

## <a name="previous-step"></a><span data-ttu-id="1643d-124">Iepriekšējā darbība</span><span class="sxs-lookup"><span data-stu-id="1643d-124">Previous step</span></span>
[<span data-ttu-id="1643d-125">Hipotēzes identificēšana un eksperimenta rādītāju noteikšana</span><span class="sxs-lookup"><span data-stu-id="1643d-125">Identify a hypothesis and determine metrics for an experiment</span></span>](experimentation-identify.md) 


## <a name="next-step"></a><span data-ttu-id="1643d-126">Nākamā darbība</span><span class="sxs-lookup"><span data-stu-id="1643d-126">Next step</span></span>
[<span data-ttu-id="1643d-127">Eksperimenta pievienošana un rediģēšana</span><span class="sxs-lookup"><span data-stu-id="1643d-127">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)
