---
title: Ieteicamā tehniskā speciālista iestatīšana
description: Jebkuru darbinieku var atlasīt kā ieteicamo tehnisko speciālistu pakalpojumu līgumam vai pakalpojuma pasūtījumam.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable, SMADispatchBoard
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 850d91372fb1a918840ebc316a4479f4a70bdc24
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983137"
---
# <a name="set-up-a-preferred-technician"></a><span data-ttu-id="48ac9-103">Ieteicamā tehniskā speciālista iestatīšana</span><span class="sxs-lookup"><span data-stu-id="48ac9-103">Set up a preferred technician</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="48ac9-104">Jebkuru darbinieku var atlasīt kā ieteicamo tehnisko speciālistu pakalpojumu līgumam vai pakalpojuma pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="48ac9-104">You can select any worker as a preferred technician for a service agreement or service order.</span></span> <span data-ttu-id="48ac9-105">Taču ir ieteicams darbinieku pievienot atbilstošajai nosūtīšanas grupai, lai šis darbinieks būtu ietverts sarakstā **Dispečera pults**.</span><span class="sxs-lookup"><span data-stu-id="48ac9-105">However, it is a good idea to add the worker to the appropriate dispatch team so that the worker is included on the **Dispatch board**.</span></span>

## <a name="assign-employee-to-a-dispatch-team"></a><span data-ttu-id="48ac9-106">Darbinieka piešķiršana nosūtīšanas grupai</span><span class="sxs-lookup"><span data-stu-id="48ac9-106">Assign employee to a dispatch team</span></span>

1.  <span data-ttu-id="48ac9-107">Noklikšķiniet uz **Personāla vadība** \> **Vispārīgi** \> **Nodarbinātie** \> **Nodarbinātie**.</span><span class="sxs-lookup"><span data-stu-id="48ac9-107">Click **Human resources** \> **Common** \> **Workers** \> **Workers**.</span></span> <span data-ttu-id="48ac9-108">Veiciet dubultklikšķi uz darbinieka, lai atvērtu detalizētās informācijas lapu par darbinieku.</span><span class="sxs-lookup"><span data-stu-id="48ac9-108">Double-click a worker to open the worker details page.</span></span> <span data-ttu-id="48ac9-109">Sadaļā **Darbību rūts** noklikšķiniet uz **Iestatīšana** \>**Nosūtīšanas grupa**, lai atvērtu formu **Nosūtīšanas nodarbinātie**.</span><span class="sxs-lookup"><span data-stu-id="48ac9-109">On the **Action Pane**, click **Setup** \>**Dispatch team** to open the **Dispatch workers** form.</span></span>

2.  <span data-ttu-id="48ac9-110">Laukā **Nosūtīšanas grupa** atlasiet darba grupu, kurai piešķirt šo darbinieku.</span><span class="sxs-lookup"><span data-stu-id="48ac9-110">In the **Dispatch team** field, select the team to assign the worker to.</span></span>

## <a name="assign-a-preferred-technician-to-a-service-agreement"></a><span data-ttu-id="48ac9-111">Ieteicamā tehniskā speciālista piešķiršana pakalpojumu līgumam</span><span class="sxs-lookup"><span data-stu-id="48ac9-111">Assign a preferred technician to a service agreement</span></span>

1.  <span data-ttu-id="48ac9-112">Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojumu līgumi** \> **Pakalpojumu līgumi**.</span><span class="sxs-lookup"><span data-stu-id="48ac9-112">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span> <span data-ttu-id="48ac9-113">Veiciet dubultklikšķi uz pakalpojuma līguma, lai atvērtu detalizētās informācijas formu.</span><span class="sxs-lookup"><span data-stu-id="48ac9-113">Double-click a service agreement to open the details form.</span></span>

2.  <span data-ttu-id="48ac9-114">Cilnē **Vispārīgi** atlasiet lauku **Ieteicamais tehniskais speciālists** un pēc tam atlasiet atbilstošās nosūtīšanas grupas dalībnieku kā ieteicamo tehnisko speciālistu šim pakalpojumu līgumam.</span><span class="sxs-lookup"><span data-stu-id="48ac9-114">On the **General** tab, select the **Preferred technician** field, and then select a member of the appropriate dispatch team as the preferred technician for the service agreement.</span></span>

## <a name="assign-a-preferred-technician-to-a-service-order"></a><span data-ttu-id="48ac9-115">Ieteicamā speciālista piešķiršana pakalpojumu pasūtījumam</span><span class="sxs-lookup"><span data-stu-id="48ac9-115">Assign a preferred technician to a service order</span></span>

1.  <span data-ttu-id="48ac9-116">Noklikšķiniet uz **Pakalpojumu pārvaldība** \> **Periodiskās darbības** \> **Dispečera pults**.</span><span class="sxs-lookup"><span data-stu-id="48ac9-116">Click **Service management** \> **Periodic** \> **Dispatch board**.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="48ac9-117">Formā <STRONG>Dispečera pults</STRONG> norādiet apskatāmo nosūtīšanas aktivitāšu datumu diapazonu.</span><span class="sxs-lookup"><span data-stu-id="48ac9-117">In the <STRONG>Dispatch board</STRONG> form, specify a date range for dispatch activities to view.</span></span> <span data-ttu-id="48ac9-118">Norādiet arī, vai rādīt pabeigtās aktivitātes un vai ierobežot nosūtīšanas aktivitāšu sarakstu grupām, pie kurām jūs piederat vai kuras jums ir pilnvaras pārraudzīt.</span><span class="sxs-lookup"><span data-stu-id="48ac9-118">Also, specify whether to display closed activities and whether to limit the dispatch activity list to teams that you belong to or are authorized to monitor.</span></span> <span data-ttu-id="48ac9-119">Noklikšķiniet uz <STRONG>Labi</STRONG>, lai atvērtu sadaļu <STRONG>Dispečera pults</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="48ac9-119">Click <STRONG>OK</STRONG> to open the <STRONG>Dispatch board</STRONG>.</span></span></P>



2.  <span data-ttu-id="48ac9-120">Atlasiet modificējamās pakalpojuma aktivitātes rindu.</span><span class="sxs-lookup"><span data-stu-id="48ac9-120">Select the line of the service activity to modify.</span></span>

3.  <span data-ttu-id="48ac9-121">Cilnē **Saistīts** izmantojiet sarakstu **Nodarbinātais**, lai atbilstošās nosūtīšanas grupas dalībnieku piešķirtu kā ieteicamo tehnisko speciālistu šim pakalpojumu izsaukumam.</span><span class="sxs-lookup"><span data-stu-id="48ac9-121">On the **Related** tab, use the **Worker** list to assign a member of the appropriate dispatch team as the preferred technician for the service call.</span></span>

## <a name="see-also"></a><span data-ttu-id="48ac9-122">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="48ac9-122">See also</span></span>

[<span data-ttu-id="48ac9-123">Izstrādes un veidošanas pakalpojumu līgumu pārskats</span><span class="sxs-lookup"><span data-stu-id="48ac9-123">Develop and establish service agreements overview</span></span>](service-agreements.md)

[<span data-ttu-id="48ac9-124">Pakalpojumu pasūtījumu manuāla izveide</span><span class="sxs-lookup"><span data-stu-id="48ac9-124">Create service orders manually</span></span>](create-service-orders-manually.md)

<span data-ttu-id="48ac9-125">[Pakalpojumu līgumi (forma)](https://technet.microsoft.com/library/aa617823\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="48ac9-125">[Service agreements (form)](https://technet.microsoft.com/library/aa617823\(v=ax.60\))</span></span>
  


