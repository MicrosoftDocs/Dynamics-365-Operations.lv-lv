---
title: Eksperimenta iestatīšana
description: Šajā tēmā ir aprakstīts, kā iestatīt eksperimentu trešās puses pakalpojumos.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 9976ca461f7e988c32b81565fa2d084709e5ad6e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792514"
---
# <a name="set-up-an-experiment"></a><span data-ttu-id="eee25-103">Eksperimenta iestatīšana</span><span class="sxs-lookup"><span data-stu-id="eee25-103">Set up an experiment</span></span>

<span data-ttu-id="eee25-104">Kad esat [definējis hipotēzi un noteicis, kādus panākumu rādītājus vēlaties izmantot](experimentation-identify.md), jums ir jāiestata eksperiments trešās puses pakalpojumā.</span><span class="sxs-lookup"><span data-stu-id="eee25-104">After you [define a hypothesis and determine what success metrics you want to use](experimentation-identify.md), you'll need to set up your experiment in the third-party service.</span></span> <span data-ttu-id="eee25-105">Tālāk esošajā diagrammā ir parādītas visas darbības, kas jāveic, lai iestatītu un izpildītu eksperimentu e-komercijas tīmekļa vietnē pakalpojumā Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="eee25-105">The following diagram shows all of the steps involved in setting up and running an experiment on an e-Commerce website in Dynamics 365 Commerce.</span></span> <span data-ttu-id="eee25-106">Papildu darbības ir apskatītas atsevišķās tēmās.</span><span class="sxs-lookup"><span data-stu-id="eee25-106">Additional steps are covered in separate topics.</span></span>

<span data-ttu-id="eee25-107">[ ![Eksperimenta lietotāja maršruts – iestatīšana](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)</span><span class="sxs-lookup"><span data-stu-id="eee25-107">[ ![Experimentation user journey - Setup](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)</span></span>


## <a name="set-up-your-experiment-in-the-third-party-service"></a><span data-ttu-id="eee25-108">Eksperimenta iestatīšana trešās puses pakalpojumā</span><span class="sxs-lookup"><span data-stu-id="eee25-108">Set up your experiment in the third-party service</span></span>
<span data-ttu-id="eee25-109">Jums ir jāizvēlas trešās puses pakalpojums, lai varētu izpildīt un pārraudzīt jūsu eksperimentu un iestatīt eksperimenta savienotāju.</span><span class="sxs-lookup"><span data-stu-id="eee25-109">By now you should have chosen your third-party service to run and monitor your experiment, and set up the experimentation connector.</span></span> <span data-ttu-id="eee25-110">Šie priekšnosacījumi ir uzskaitīti  [Eksperimentēšana pakalpojumā Dynamics 365 Commerce](experimentation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="eee25-110">These prerequisites are listed in  [Experimentation in Dynamics 365 Commerce](experimentation-overview.md).</span></span>

<span data-ttu-id="eee25-111">Izpildiet nepieciešamās darbības, lai izveidotu eksperimentu trešās puses pakalpojumā.</span><span class="sxs-lookup"><span data-stu-id="eee25-111">Follow the steps required to create your experiment in the third-party service.</span></span> <span data-ttu-id="eee25-112">Ja savienotājs ir konfigurēts pareizi, pilns trešās puses pakalpojumā iestatīto eksperimentu saraksts tiks parādīts Commerce vietņu veidotājā apmēram 5 minūšu laikā.</span><span class="sxs-lookup"><span data-stu-id="eee25-112">If the connector is configured properly, the complete list of experiments you set up in the third-party service will appear in Commerce site builder within about 5 minutes.</span></span>

## <a name="set-up-your-success-metrics"></a><span data-ttu-id="eee25-113">Panākumu rādītāju iestatīšana</span><span class="sxs-lookup"><span data-stu-id="eee25-113">Set up your success metrics</span></span>
<span data-ttu-id="eee25-114">Katram eksperimentam ir nepieciešami rādītāji, lai noteiktu variantu ietekmi un pārbaudītu hipotēzi.</span><span class="sxs-lookup"><span data-stu-id="eee25-114">Every experiment needs metrics to measure the impact of the variations and to validate the hypothesis.</span></span> <span data-ttu-id="eee25-115">Veiciet tālāk norādītās darbības, lai iespējotu rādītāju aprēķināšanu trešās puses pakalpojumā, izmantojot tiešsaistes telemetrijas notikumus no Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="eee25-115">Follow the steps below to enable the computation of metrics in the third-party service using live telemetry events from Dynamics 365 Commerce.</span></span>

<span data-ttu-id="eee25-116">Lai iestatītu jūsu panākumu rādītājus, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="eee25-116">To set up your success metrics, follow these steps.</span></span>

1. <span data-ttu-id="eee25-117">Commerce vietņu veidotājā atlasiet **Lapas** kreisajā navigācijas rūtī un pēc tam atlasiet lapu, kuras rādītājus vēlaties apkopot.</span><span class="sxs-lookup"><span data-stu-id="eee25-117">In Commerce site builder, select **Pages** in the left navigation pane, and then select the page that you want to collect metrics for.</span></span> 
1. <span data-ttu-id="eee25-118">Dodieties uz sadaļu **Izsekojamie notikumu ID**, kas atrodas lapas labās puses rekvizītu rūtī vai modulī, kuru vēlaties izsekot.</span><span class="sxs-lookup"><span data-stu-id="eee25-118">Go to the **Event IDs to track** section in the right property pane of the page or module you want to track.</span></span>
1. <span data-ttu-id="eee25-119">Atlasiet **Skatīt**.</span><span class="sxs-lookup"><span data-stu-id="eee25-119">Select **View**.</span></span> <span data-ttu-id="eee25-120">Tiek parādīts visu notikumu ID saraksts.</span><span class="sxs-lookup"><span data-stu-id="eee25-120">A list of all event IDs is displayed.</span></span> <span data-ttu-id="eee25-121">Kopējiet notikumu, kuram vēlaties sekot, un ielīmējiet notikuma atslēgu norādītajā vietā trešās puses pakalpojumā.</span><span class="sxs-lookup"><span data-stu-id="eee25-121">Copy the event you want to track, and paste the event key into the designated location in the third-party service.</span></span> <span data-ttu-id="eee25-122">Ja ir nepieciešams vairāk nekā viens notikums, kopējiet atslēgas pa vienai.</span><span class="sxs-lookup"><span data-stu-id="eee25-122">If you need more than one event, copy the keys one at a time.</span></span> 
    - <span data-ttu-id="eee25-123">Lai uzzinātu, kā skatīt visus pieejamos notikumus un atribūtus, ieskaitot lapu skatījumus un ieņēmumu izsekošanu, skatiet sadaļu [Commerce komponentu notikumi diagnostikai un problēmu novēršanai](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="eee25-123">To learn how to view all of the available events and attributes, including page views and revenue tracking, see [Commerce component events for diagnostics and troubleshooting](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).</span></span>
1. <span data-ttu-id="eee25-124">Citas darbības, lai izsekotu rādītājus, veiciet pēc nepieciešamības trešās puses pakalpojumā.</span><span class="sxs-lookup"><span data-stu-id="eee25-124">Take any other steps for tracking metrics as required in the third-party service.</span></span>

## <a name="previous-step"></a><span data-ttu-id="eee25-125">Iepriekšējā darbība</span><span class="sxs-lookup"><span data-stu-id="eee25-125">Previous step</span></span>
[<span data-ttu-id="eee25-126">Hipotēzes identificēšana un eksperimenta rādītāju noteikšana</span><span class="sxs-lookup"><span data-stu-id="eee25-126">Identify a hypothesis and determine metrics for an experiment</span></span>](experimentation-identify.md) 


## <a name="next-step"></a><span data-ttu-id="eee25-127">Nākamā darbība</span><span class="sxs-lookup"><span data-stu-id="eee25-127">Next step</span></span>
[<span data-ttu-id="eee25-128">Eksperimenta pievienošana un rediģēšana</span><span class="sxs-lookup"><span data-stu-id="eee25-128">Connect and edit an experiment</span></span>](experimentation-connect-edit.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]