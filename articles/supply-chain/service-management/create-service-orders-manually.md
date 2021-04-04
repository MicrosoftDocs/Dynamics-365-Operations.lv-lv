---
title: Pakalpojumu pasūtījumu manuālā izveide
description: Pakalpojumu pasūtījumus varat izveidot manuāli, izmantojot pakalpojumu līgumu vai veidlapu **Pakalpojumu pasūtījumi**.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 72b600bc59119a6304fa043240a34051435f8691
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470957"
---
# <a name="create-service-orders-manually"></a><span data-ttu-id="a683d-103">Pakalpojumu pasūtījumu manuālā izveide</span><span class="sxs-lookup"><span data-stu-id="a683d-103">Create service orders manually</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="a683d-104">Pakalpojumu pasūtījumus varat izveidot manuāli, izmantojot pakalpojumu līgumu vai veidlapu **Pakalpojumu pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="a683d-104">You can create service orders manually by using a service agreement or by using the **Service orders** form.</span></span> <span data-ttu-id="a683d-105">Pakalpojumu pasūtījumu varat veidot arī no projekta.</span><span class="sxs-lookup"><span data-stu-id="a683d-105">You can also create a service order from a project.</span></span>

> [!TIP]
> <P><span data-ttu-id="a683d-106">Varat izmantot automatizētos pakalpojumu pasūtījumu izveides procesus.</span><span class="sxs-lookup"><span data-stu-id="a683d-106">You can use automated processes to create service orders.</span></span> 

## <a name="create-a-service-order-manually-from-a-service-agreement"></a><span data-ttu-id="a683d-107">Pakalpojumu pasūtījuma manuāla izveide no pakalpojumu līguma</span><span class="sxs-lookup"><span data-stu-id="a683d-107">Create a service order manually from a service agreement</span></span>

1.  <span data-ttu-id="a683d-108">Atlasiet **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojumu līgumi** \> **Pakalpojumu līgumi**.</span><span class="sxs-lookup"><span data-stu-id="a683d-108">Select **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>

2.  <span data-ttu-id="a683d-109">Izvēlieties pakalpojumu līgumu un izveidojiet jaunu pakalpojumu līgumu.</span><span class="sxs-lookup"><span data-stu-id="a683d-109">Select a service agreement or create a new service agreement.</span></span>

3.  <span data-ttu-id="a683d-110">Atlasiet cilni **Piegāde** un grupā **Izveidot** atlasiet **Plānotie pakalpojumu pasūtījumi**, lai atvērtu veidlapu **Pakalpojumu pasūtījumu izveide**.</span><span class="sxs-lookup"><span data-stu-id="a683d-110">Select the **Deliver** tab and in the **Create** group select **Planned service orders** to open the **Create service orders** form.</span></span>

## <a name="create-a-service-order-manually-in-the-service-orders-form"></a><span data-ttu-id="a683d-111">Pakalpojumu pasūtījuma manuāla izveide pakalpojumu pasūtījumu formā</span><span class="sxs-lookup"><span data-stu-id="a683d-111">Create a service order manually in the Service orders form</span></span>

1.  <span data-ttu-id="a683d-112">Atlasiet **Pakalpojumu pārvaldība** \> **Vispārīgi** \> **Pakalpojuma pasūtījumi** \> **Pakalpojuma pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="a683d-112">Select **Service management** \> **Common** \> **Service orders** \> **Service orders**.</span></span>

2.  <span data-ttu-id="a683d-113">Atlasiet **Jauns**, lai izveidotu jaunu pakalpojuma pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="a683d-113">Select **New** to create a new service order.</span></span>

3.  <span data-ttu-id="a683d-114">Pakalpojumu pasūtījumam izveidojiet pakalpojumu pasūtījuma rindas.</span><span class="sxs-lookup"><span data-stu-id="a683d-114">Create service order lines for the service order.</span></span>

> [!NOTE]
> <P><span data-ttu-id="a683d-115">Ja veidlapā <STRONG>Pakalpojumu pārvaldības parametri</STRONG> ir atzīmēta izvēles rūtiņa <STRONG>Atļaut bez pakalpojumu līguma</STRONG>, transakcijas no pakalpojumu pasūtījuma rindām varat grāmatot, nepiesaistot pakalpojumu pasūtījumu pakalpojumu līgumam.</span><span class="sxs-lookup"><span data-stu-id="a683d-115">If the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form is selected, you can post the transactions from the service order lines without attaching the service order to a service agreement.</span></span> <span data-ttu-id="a683d-116">Ja izvēles rūtiņai tiek izņemta atzīme, pirms pakalpojumu pasūtījuma rindu grāmatošanas jums projektam jāpiesaista manuāli izveidots pakalpojumu pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="a683d-116">If the check box is cleared, you must attach the manually created service order to a project before posting the service order lines.</span></span></P>

## <a name="create-a-service-order-from-a-project"></a><span data-ttu-id="a683d-117">Pakalpojumu pasūtījuma izveide no projekta</span><span class="sxs-lookup"><span data-stu-id="a683d-117">Create a service order from a project</span></span>

1.  <span data-ttu-id="a683d-118">Dodieties uz **Projektu pārvaldība un uzskaite** \> **Vispārīgi** \> **Projekti** \> **Visi projekti**.</span><span class="sxs-lookup"><span data-stu-id="a683d-118">Go to **Project management and accounting** \> **Common** \> **Projects** \> **All projects**.</span></span>

2.  <span data-ttu-id="a683d-119">Veidlapas **Projekti** **Darbību rūtī** cilnē **Pārvaldīt** noklikšķiniet uz \> **Pakalpojums** \> **Pakalpojumu pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="a683d-119">In the **Projects** form, on the **Action Pane**, select the **Manage** tab \> select **Service** \> **Service orders**.</span></span>

3.  <span data-ttu-id="a683d-120">Izpildiet iepriekš norādītās darbības, lai manuāli izveidotu pakalpojumu pasūtījumu veidlapā **Pakalpojumu pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="a683d-120">Follow the previous procedure to create a service order manually in the **Service orders** form.</span></span> <span data-ttu-id="a683d-121">Laukā **Projekta ID** tiek parādīta projekta atsauce.</span><span class="sxs-lookup"><span data-stu-id="a683d-121">The **Project ID** field displays the project reference.</span></span>

> [!NOTE]
> <P><span data-ttu-id="a683d-122">Ja veidlapā <STRONG>Pakalpojumu pārvaldības parametri</STRONG> ir atzīmēta izvēles rūtiņa <STRONG>Atļaut bez pakalpojumu līguma</STRONG>, transakcijas no pakalpojumu pasūtījuma rindām varat grāmatot, nepiesaistot pakalpojumu pasūtījumu pakalpojumu līgumam.</span><span class="sxs-lookup"><span data-stu-id="a683d-122">If the <STRONG>Allow without service agreement</STRONG> check box in the <STRONG>Service management parameters</STRONG> form is selected, you can post the transactions from the service order lines without attaching the service order to a service agreement.</span></span> <span data-ttu-id="a683d-123">Ja izvēles rūtiņai tiek izņemta atzīme, pirms pakalpojumu pasūtījuma rindu grāmatošanas jums projektam jāpiesaista manuāli izveidots pakalpojumu pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="a683d-123">If the check box is cleared, you must attach the manually created service order to a project before posting the service order lines.</span></span></P>

## <a name="create-a-service-order-from-the-sales-order-form"></a><span data-ttu-id="a683d-124">Pakalpojumu pasūtījuma izveide no veidlapas Pārdošanas pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="a683d-124">Create a service order from the Sales order form</span></span>

<span data-ttu-id="a683d-125">Varat izveidot pakalpojumu pasūtījumu no veidlapas **Pārdošanas pasūtījumi**, izmantojot vedni **Izveidot jaunu pakalpojumu pasūtījumu, izmantojot pārdošanas pasūtījumu**.</span><span class="sxs-lookup"><span data-stu-id="a683d-125">You can create a service order from the **Sales orders** form by using the **Create a new service order based on the sales order** wizard.</span></span>

1.  <span data-ttu-id="a683d-126">Noklikšķiniet uz **Pārdošana un mārketings** \> **Vispārīgi** \> **Pārdošanas pasūtījumi** \> **Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="a683d-126">Go to **Sales and marketing** \> **Common** \> **Sales orders** \> **All sales orders**.</span></span>

2.  <span data-ttu-id="a683d-127">Atveriet attiecīgo pārdošanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="a683d-127">Open the relevant sales order.</span></span>

3.  <span data-ttu-id="a683d-128">Cilnē **Pārdošanas pasūtījums** noklikšķiniet uz vienuma **Pakalpojuma pasūtījums**, lai palaistu vedni **Izveidot jaunu pakalpojumu pasūtījumu, izmantojot pārdošanas pasūtījumu**.</span><span class="sxs-lookup"><span data-stu-id="a683d-128">On the **Sales order** tab, select **Service order** to start the **Create a new service order based on the sales order** wizard.</span></span>

4.  <span data-ttu-id="a683d-129">Noklikšķiniet uz **Tālāk \>** un pēc tam lapā **Atlasīt pakalpojumu pasūtījuma līgumu** veiciet šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="a683d-129">Select **Next \>**, and then complete the following steps on the **Select agreement for service order** page:</span></span>
    
      - <span data-ttu-id="a683d-130">Izmantojiet lauku **Pakalpojuma līgums**, lai atlasītu pakalpojuma līgumu ar kuru ir jāsaista jaunais pakalpojuma pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="a683d-130">Use the **Service agreement** field to select the service agreement with which the new service order should be associated.</span></span>
    
      - <span data-ttu-id="a683d-131">Pēc izvēles: izmantojiet lauku **Projekta ID**, lai saistītu šo pakalpojuma pasūtījumu ar konkrētu projektu.</span><span class="sxs-lookup"><span data-stu-id="a683d-131">Optional: Use the **Project ID** field to associate this service order with a particular project.</span></span>

5.  <span data-ttu-id="a683d-132">Noklikšķiniet uz **Tālāk \>** un pēc tam lapā **Pakalpojuma pasūtījuma izveide** veiciet šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="a683d-132">Select **Next \>**, and then complete the following steps on the **Create service order** page:</span></span>
    
      - <span data-ttu-id="a683d-133">Laukā **Ieteicamais pakalpojuma laiks** ievadiet pakalpojuma izsaukuma sākuma datumu un laiku.</span><span class="sxs-lookup"><span data-stu-id="a683d-133">Enter a date and time for the service call to begin in the **Preferred service time** field.</span></span>
    
      - <span data-ttu-id="a683d-134">Pēc izvēles: modificējiet tekstu laukā **Apraksts**.</span><span class="sxs-lookup"><span data-stu-id="a683d-134">Optional: Modify the text in the **Description** field.</span></span> <span data-ttu-id="a683d-135">Pēc noklusējuma šajā laukā ir iepriekšējā lapā atlasītā pakalpojuma līguma apraksts.</span><span class="sxs-lookup"><span data-stu-id="a683d-135">By default, this field contains the description of the service agreement that you selected on the previous page.</span></span>
    
      - <span data-ttu-id="a683d-136">Laukā **Atbildīgā persona** atlasiet par līgumu atbildīgā darbinieka ID un, ja ziniet, kurš tas ir, — klienta iecienītākā tehniķa ID, kurš būs atbildīgs par pakalpojuma izsaukumu.</span><span class="sxs-lookup"><span data-stu-id="a683d-136">In the **Responsible** field, select the ID of the employee who is responsible for the agreement, and if you know what it is, enter the ID of the customer's preferred technician for the service call.</span></span>
    
      - <span data-ttu-id="a683d-137">Laukā **Kontaktpersonas ID** atlasiet klienta uzņēmuma kontaktpersonu, ar kuru ir jāsazinās saistībā ar šo pakalpojuma pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="a683d-137">In the **Contact ID** field, select the person in the customer's company who should be contacted regarding this service order.</span></span>

6.  <span data-ttu-id="a683d-138">Atlasiet **Tālāk \>** un pēc tam atlasiet **Pabeigt**.</span><span class="sxs-lookup"><span data-stu-id="a683d-138">Select **Next \>**, and then select **Finish**.</span></span>


## <a name="see-also"></a><span data-ttu-id="a683d-139">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="a683d-139">See also</span></span>

[<span data-ttu-id="a683d-140">Pakalpojumu pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="a683d-140">Service orders</span></span>](service-orders.md)

[<span data-ttu-id="a683d-141">Automātiska pakalpojumu pasūtījumu izveide</span><span class="sxs-lookup"><span data-stu-id="a683d-141">Create service orders automatically</span></span>](create-service-orders-automatically.md)

<span data-ttu-id="a683d-142">[Pakalpojumu pasūtījumu izveidošana (klases forma)](https://technet.microsoft.com/library/aa553901\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="a683d-142">[Create service orders (class form)](https://technet.microsoft.com/library/aa553901\(v=ax.60\))</span></span> 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]