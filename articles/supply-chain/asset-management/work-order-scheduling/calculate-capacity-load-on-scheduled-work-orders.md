---
title: Noslodzes aprēķināšana plānotajiem darba pasūtījumiem
description: Šajā tēmā ir paskaidrots, kā aprēķināt noslodzi plānotajiem darba pasūtījumiem programmā Asset Management.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b817909ac0950b773cba775be2502b5796c6d8d6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432916"
---
# <a name="calculate-capacity-load-on-scheduled-work-orders"></a><span data-ttu-id="c724b-103">Noslodzes aprēķināšana plānotajiem darba pasūtījumiem</span><span class="sxs-lookup"><span data-stu-id="c724b-103">Calculate capacity load on scheduled work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c724b-104">Varat aprēķināt noslodzi plānotajiem darbu pasūtījumiem, lai iegūtu pārskatu par resursu darba noslodzi konkrētam periodam.</span><span class="sxs-lookup"><span data-stu-id="c724b-104">You can calculate capacity load on scheduled work orders to get an overview of the work load on resources for a specific period.</span></span> <span data-ttu-id="c724b-105">Aprēķinus var veikt šādiem resursiem: uzturēšanas speciālisti, strādnieku grupas un līdzekļi.</span><span class="sxs-lookup"><span data-stu-id="c724b-105">Calculations can be made for the following resources: Maintenance workers, worker groups, tools, and assets.</span></span>

1. <span data-ttu-id="c724b-106">Klikšķiniet uz **Līdzekļu pārvaldība** > **Pieprasījumi** > **Pieprasījumi** > **Noslodze**.</span><span class="sxs-lookup"><span data-stu-id="c724b-106">Click **Asset management** > **Inquiries** > **Schedule** > **Capacity load**.</span></span>

2. <span data-ttu-id="c724b-107">Dialoglodziņā **Aprēķināt noslodzi** laukā > **Parādīt** atlasiet, kādu noslodzes veidu vēlaties aprēķināt: **Noslodze**, **Rezervēts** vai **Atlikums**.</span><span class="sxs-lookup"><span data-stu-id="c724b-107">In the **Calculate capacity load** dialog > **Show** field, select which load type you want to calculate: **Capacity**, **Reserved**, or **Remainder**.</span></span>

3. <span data-ttu-id="c724b-108">Pārslēgšanas pogā **Izlaist nulli** atlasiet **Jā**, ja nevēlaties, lai rāda rezultātus, kas satur nulli.</span><span class="sxs-lookup"><span data-stu-id="c724b-108">Select **Yes** on the **Skip zero** toggle button if you do not want to show results containing zero.</span></span>

4. <span data-ttu-id="c724b-109">Atlasiet resursa veidus, kam vēlaties aprēķināt noslodzi, atlasot **Jā** attiecīgajās pārslēgšanas pogās: **Darbinieks**, **Uzturēšanas darbinieku grupa**, **Rīks** un **Līdzeklis**.</span><span class="sxs-lookup"><span data-stu-id="c724b-109">Select the resource types for which you want to calculate capacity load by selecting **Yes** on the relevant toggle buttons: **Worker**, **Maintenance worker group**, **Tool**, and **Asset**.</span></span>

5. <span data-ttu-id="c724b-110">Laukā **No datums** atlasiet aprēķina sākuma datumu.</span><span class="sxs-lookup"><span data-stu-id="c724b-110">Select the start date for the calculation in the **From date** field.</span></span>

6. <span data-ttu-id="c724b-111">Laukā **Intervāla veids** atlasiet aprēķina intervālu: **Diena**, **Nedēļa**, **Mēnesis** vai **Ceturksnis**.</span><span class="sxs-lookup"><span data-stu-id="c724b-111">In the **Interval type** field, select the interval for the calculation: **Day**, **Week**, **Month**, or **Quarter**.</span></span>

7. <span data-ttu-id="c724b-112">Laukā **Perioda biežums** ievadiet intervālu skaitu, ko vēlaties aprēķināt.</span><span class="sxs-lookup"><span data-stu-id="c724b-112">In the **Period frequency** field, insert the number of intervals you want to calculate.</span></span> <span data-ttu-id="c724b-113">Piemēram, ja izvēlaties kā intervāla veidu **Diena** un laukā ievadāt skaitli "5", tiks veikts aprēķins par piecām dienām no sākuma datuma.</span><span class="sxs-lookup"><span data-stu-id="c724b-113">For example, if you have selected **Day** as the interval type, and you enter the number "5" in this field, a calculation of five days from the start date will be made.</span></span>

8. <span data-ttu-id="c724b-114">Noklikšķiniet uz **Labi**, lai sāktu aprēķināšanu.</span><span class="sxs-lookup"><span data-stu-id="c724b-114">Click **OK** to start the calculation.</span></span>

<span data-ttu-id="c724b-115">Šajā attēlā parādīts aprēķina rezultāts par trim nedēļām noslodzes veidam **Rezervēts**.</span><span class="sxs-lookup"><span data-stu-id="c724b-115">The figure below shows the result of a calculation covering three weeks for the load type **Reserved**.</span></span>

![1. attēls](media/08-work-order-scheduling.png)

[!NOTE]
<span data-ttu-id="c724b-117">Ja savam aprēķinam izvēlaties noslodzes veidus **Noslodze** vai **Atlikums**, tiks parādīts tas pats rezultāts, ja atlasītajā periodā resursiem nav veiktas rezervācijas.</span><span class="sxs-lookup"><span data-stu-id="c724b-117">If you select the load types **Capacity** or **Remainder** for your calculation, the same result will be displayed if no reservations have been made for the resources in the selected period.</span></span>

<span data-ttu-id="c724b-118">Informāciju par noslodzes aprēķināšanu uzturēšanas grafika rindām un neieplānotu darba pasūtījumiem skatiet sadaļā [Noslodzes aprēķināšana](../capacity-planning/calculate-capacity-load.md).</span><span class="sxs-lookup"><span data-stu-id="c724b-118">For information about how to calculate capacity load on maintenance schedule lines and not scheduled work orders, refer to [Calculate capacity load](../capacity-planning/calculate-capacity-load.md).</span></span>

