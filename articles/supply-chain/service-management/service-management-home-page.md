---
title: "Pakalpojumu pārvaldība"
description: "Izmantojiet sadaļu Pakalpojumu pārvaldība, lai izveidotu pakalpojumu līgumus un pakalpojumu abonementus, apstrādātu pakalpojumu pasūtījumus un klientu pieprasījumus, un lai pārvaldītu un analizētu pakalpojumu piegādes klientiem."
author: YuyuScheller
manager: AnnBe
ms.date: 05/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 02cdf4615e2071f2b7de2e86b6f9e6637c6e5d8d
ms.openlocfilehash: 236ab21b2d1c5a4e82270e5381d163e97437cb7f
ms.contentlocale: lv-lv
ms.lasthandoff: 05/09/2018

---


# <a name="service-management"></a><span data-ttu-id="eb4a7-103">Pakalpojumu pārvaldība</span><span class="sxs-lookup"><span data-stu-id="eb4a7-103">Service management</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="eb4a7-104">Izmantojiet sadaļu **Pakalpojumu pārvaldība**, lai izveidotu pakalpojumu līgumus un pakalpojumu abonementus, apstrādātu pakalpojumu pasūtījumus un klientu pieprasījumus, un lai pārvaldītu un analizētu pakalpojumu piegādes klientiem.</span><span class="sxs-lookup"><span data-stu-id="eb4a7-104">Use **Service management** to establish service agreements and service subscriptions, handle service orders and customer inquiries, and to manage and analyze the delivery of services to customers.</span></span> <span data-ttu-id="eb4a7-105">Pakalpojumu līgumus var izmantot, lai definētu resursus, ko izmantot tipiskā pakalpojumu vizītē.</span><span class="sxs-lookup"><span data-stu-id="eb4a7-105">You can use service agreements to define the resources that are used in a typical service visit.</span></span> <span data-ttu-id="eb4a7-106">Pakalpojumu līgumus var arī izmantot, lai skatītu, kā šie resursi tiek iekļauti klienta rēķinos.</span><span class="sxs-lookup"><span data-stu-id="eb4a7-106">You can also use service agreements to view how those resources are invoiced to the customer.</span></span> <span data-ttu-id="eb4a7-107">Pakalpojuma līgumā var arī ietvert pakalpojumu līmeņa vienošanos, kas nosaka standarta atbildes laikus un piedāvā rīkus faktiskā laika ierakstīšanai.</span><span class="sxs-lookup"><span data-stu-id="eb4a7-107">A service agreement can also include a service level agreement that specifies standard response times, and offers tools to record the actual time.</span></span>

<span data-ttu-id="eb4a7-108">Varat izveidot pakalpojumu pasūtījumus, lai pārvaldītu informāciju par plānotajām un neplānotajām servisa speciālista vizītēm klienta atrašanās vietā.</span><span class="sxs-lookup"><span data-stu-id="eb4a7-108">You can create service orders to manage information about scheduled and unscheduled visits by a service technician to a customer site.</span></span> <span data-ttu-id="eb4a7-109">Pakalpojumu pasūtījumi ietver šādu informāciju, piemēram:</span><span class="sxs-lookup"><span data-stu-id="eb4a7-109">Service orders include information such as:</span></span>

1.  <span data-ttu-id="eb4a7-110">Servisa speciālista veicamo darba stundu skaitu</span><span class="sxs-lookup"><span data-stu-id="eb4a7-110">The hours of work that the service technician will perform</span></span>

2.  <span data-ttu-id="eb4a7-111">Pakalpojumu vai labošanas veidu</span><span class="sxs-lookup"><span data-stu-id="eb4a7-111">The type of service or repair</span></span>

3.  <span data-ttu-id="eb4a7-112">Labojamo objektu, ieskaitot detaļas par problēmām un diagnozi</span><span class="sxs-lookup"><span data-stu-id="eb4a7-112">The item to repair, including details about the symptoms and diagnosis</span></span>

4.  <span data-ttu-id="eb4a7-113">Visus izdevumus un maksas, kas saistītas ar pakalpojumu vai labošanu</span><span class="sxs-lookup"><span data-stu-id="eb4a7-113">Any expenses and fees related to the service or repair</span></span>

<span data-ttu-id="eb4a7-114">Klienti var iesniegt pakalpojumu pieprasījumu internetā, izmantojot Uzņēmuma portālu.</span><span class="sxs-lookup"><span data-stu-id="eb4a7-114">Customers can submit service requests through the Internet by using the Enterprise Portal.</span></span> <span data-ttu-id="eb4a7-115">Šos pieprasījumus varat saņemt, apstrādāt un nosūtīt.</span><span class="sxs-lookup"><span data-stu-id="eb4a7-115">You can receive, process, and dispatch these requests.</span></span> <span data-ttu-id="eb4a7-116">Pēc pakalpojumu pasūtījuma izveidošanas varat izmantot pakalpojumu stadijas, lai pārraudzītu un precizētu nosacījumus, kas kontrolē iespējotās darbības katrā stadijā.</span><span class="sxs-lookup"><span data-stu-id="eb4a7-116">After you have created a service order, you can use service stages to monitor progress and specify rules that control what actions are enabled in each stage.</span></span> <span data-ttu-id="eb4a7-117">Kad pakalpojuma pasūtījums ir pabeigts, jūs varat parakstīt pasūtījumu, lai apstiprinātu, ka tas ir pabeigts, un pēc tam to iegrāmatojiet, lai uzsāktu rēķina procesu.</span><span class="sxs-lookup"><span data-stu-id="eb4a7-117">When a service order is complete, you can sign off on the order to confirm that it is complete, and then post the order to start the invoice process.</span></span>

<span data-ttu-id="eb4a7-118">Lietojiet atskaišu rīkus, lai pārraudzītu pakalpojumu pasūtījuma summas un abonementu darbības, un izdrukājiet darbu aprakstus un darba rēķinus.</span><span class="sxs-lookup"><span data-stu-id="eb4a7-118">Use the reporting tools to monitor service order margins and subscription transactions, and print work descriptions and work receipts.</span></span>

## <a name="business-processes"></a><span data-ttu-id="eb4a7-119">Biznesa procesi</span><span class="sxs-lookup"><span data-stu-id="eb4a7-119">Business processes</span></span>

<span data-ttu-id="eb4a7-120">Nākamajā diagrammā ir parādīti augstā līmeņa biznesa procesi modulim **Pakalpojumu pārvaldība**, kā arī parādīts, kur pakalpojuma procesi iekļaujas citos moduļos programmatūrā Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="eb4a7-120">The following diagram illustrates the high level business processes for **Service management**, and shows where service processes integrate with other modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="eb4a7-121">[![Pakalpojumu pārvaldības biznesa procesu diagramma](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span><span class="sxs-lookup"><span data-stu-id="eb4a7-121">[![Service management business process diagram](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span></span>

## <a name="service-management-at-a-glance"></a><span data-ttu-id="eb4a7-122">Pakalpojumu pārvaldības apskats</span><span class="sxs-lookup"><span data-stu-id="eb4a7-122">Service management at a glance</span></span>

<table>
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="eb4a7-123">Svarīgi uzdevumi</span><span class="sxs-lookup"><span data-stu-id="eb4a7-123">Important tasks</span></span></p></th>
<th><p><span data-ttu-id="eb4a7-124">Primārās formas</span><span class="sxs-lookup"><span data-stu-id="eb4a7-124">Primary forms</span></span></p></th>
<th><p><span data-ttu-id="eb4a7-125">Populāri pārskati</span><span class="sxs-lookup"><span data-stu-id="eb4a7-125">Popular reports</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eb4a7-126">Pakalpojumu līgumu izpildīšana</span><span class="sxs-lookup"><span data-stu-id="eb4a7-126">Fulfill service agreements</span></span></a></p></td>
<td><p><span data-ttu-id="eb4a7-127"><a href="https://technet.microsoft.com/en-us/library/aa617823(v=ax.60)">Pakalpojumu līgumi (forma)</a></span><span class="sxs-lookup"><span data-stu-id="eb4a7-127"><a href="https://technet.microsoft.com/en-us/library/aa617823(v=ax.60)">Service agreements (form)</a></span></span></p></td>
<td><p><span data-ttu-id="eb4a7-128"><strong>Pakalpojumu pasūtījumu uzcenojums</strong></span><span class="sxs-lookup"><span data-stu-id="eb4a7-128"><strong>Service order margin</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eb4a7-129">Klientu pieprasījumu regulēšana</span><span class="sxs-lookup"><span data-stu-id="eb4a7-129">Handle customer inquiries</span></span></a></p></td>
<td><p><span data-ttu-id="eb4a7-130"><a href="https://technet.microsoft.com/en-us/library/aa554361(v=ax.60)">Pakalpojumu pasūtījumi (forma)</a></span><span class="sxs-lookup"><span data-stu-id="eb4a7-130"><a href="https://technet.microsoft.com/en-us/library/aa554361(v=ax.60)">Service orders (form)</a></span></span></p></td>
<td><p><span data-ttu-id="eb4a7-131"><strong>Darba apraksts</strong></span><span class="sxs-lookup"><span data-stu-id="eb4a7-131"><strong>Work description</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="eb4a7-132"><a href="https://technet.microsoft.com/en-us/library/hh242789(v=ax.60)">Nosūtīšanas dēlis (forma)</a></span><span class="sxs-lookup"><span data-stu-id="eb4a7-132"><a href="https://technet.microsoft.com/en-us/library/hh242789(v=ax.60)">Dispatch board (form)</a></span></span></p></td>
<td><p><span data-ttu-id="eb4a7-133"><strong>Darbība - Abonements</strong></span><span class="sxs-lookup"><span data-stu-id="eb4a7-133"><strong>Transaction - subscription</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="eb4a7-134"><strong>Abonēšanas maksas transakcijas</strong></span><span class="sxs-lookup"><span data-stu-id="eb4a7-134"><strong>Subscription fee transactions</strong></span></span></p></td>
</tr>
</tbody>
</table>


## <a name="integration-of-service-management"></a><span data-ttu-id="eb4a7-135">Pakalpojumu pārvaldības integrācija</span><span class="sxs-lookup"><span data-stu-id="eb4a7-135">Integration of Service management</span></span>

<span data-ttu-id="eb4a7-136">Pakalpojumu pārvaldību var integrēt tālāk norādītajos moduļos programmatūrā Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="eb4a7-136">Service management can be integrated with the following modules in Microsoft Dynamics 365 for Finance and Operations:</span></span>

  - [<span data-ttu-id="eb4a7-137">Pārdošana un mārketings</span><span class="sxs-lookup"><span data-stu-id="eb4a7-137">Sales and marketing</span></span>](../sales-marketing/overview-sales-marketing.md)

  - [<span data-ttu-id="eb4a7-138">Personāla vadība</span><span class="sxs-lookup"><span data-stu-id="eb4a7-138">Human resources</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/index)

  


