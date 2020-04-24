---
title: Izmantot ārējos katalogus elektroniskai atzīmēšanas sagādei
description: Šajā tēmā paskaidrots, kā izmantot ārējos katalogus pieprasījumu izveidei un iesniegšanai.
author: mkirknel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f7a784e6a66c0c2df9043468e9878de161c3be0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3207420"
---
# <a name="use-external-catalogs-for-punchout-eprocurement"></a><span data-ttu-id="3c628-103">Izmantot ārējos katalogus elektroniskai atzīmēšanas sagādei</span><span class="sxs-lookup"><span data-stu-id="3c628-103">Use external catalogs for PunchOut eProcurement</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c628-104">Izmantojot ārējos katalogus elektroniskai atzīmēšanas sagādei, jums nav jāuztur informācija par kreditoru precēm savos pamatdatos.</span><span class="sxs-lookup"><span data-stu-id="3c628-104">By using external catalogs for PunchOut e-procurement, you don't have to maintain information about your vendors' products in your own master data.</span></span> <span data-ttu-id="3c628-105">Tā vietā iepirkumu grozs kreditora vietnē tiek pārveidots pieprasījuma rindās, kurās ir pareizā preces informācija.</span><span class="sxs-lookup"><span data-stu-id="3c628-105">Instead, the shopping cart on a vendor's website is converted to requisition lines that have the correct product information.</span></span> 

<span data-ttu-id="3c628-106">Ieteicams neuzturēt aprakstus un cenas kreditoru precēm savos preces pamatdatos.</span><span class="sxs-lookup"><span data-stu-id="3c628-106">You should avoid maintaining the descriptions and prices of your vendors’ products in your own product master data.</span></span> <span data-ttu-id="3c628-107">Tā vietā izmantojiet ārējos katalogus elektroniskai atzīmēšanas sagādei.</span><span class="sxs-lookup"><span data-stu-id="3c628-107">Instead, use external catalogs for PunchOut e-procurement.</span></span> <span data-ttu-id="3c628-108">Kad darbinieki izveido pieprasījumus, viņi var pāriet uz kreditora ārējā kataloga vietni (t.i., viņi atstāj jūsu sistēmu un dodas uz kreditora vietni).</span><span class="sxs-lookup"><span data-stu-id="3c628-108">Then, when employees create requisitions, they can “punch out” to a vendor’s external catalog site (in other words, they leave your system and go to the vendor’s site).</span></span> <span data-ttu-id="3c628-109">Preces, kas tiek pievienotas iepirkumu grozam kreditora vietnē, var pārveidot pieprasījuma rindās.</span><span class="sxs-lookup"><span data-stu-id="3c628-109">The products that are added to the shopping cart on the vendor’s website can then be converted to requisition lines.</span></span> <span data-ttu-id="3c628-110">Tādējādi jūs iegūstat pareizo preces informāciju: preces ID, nosaukumu, cenu un citu informāciju.</span><span class="sxs-lookup"><span data-stu-id="3c628-110">Therefore, you get the correct product information: product ID, name, price, and so on.</span></span>

<span data-ttu-id="3c628-111">Lai izmantotu ārējos katalogus, darbiniekam ir jāizveido pieprasījums lapā **Mani pirkšanas pieprasījumi**.</span><span class="sxs-lookup"><span data-stu-id="3c628-111">To use external catalogs, an employee must create a requisition on the **My purchase requisitions** page.</span></span>

<span data-ttu-id="3c628-112">Darbinieks, kurš izveido pieprasījumu, tiek dēvēts par pieprasījuma sagatavotāju.</span><span class="sxs-lookup"><span data-stu-id="3c628-112">The employee who creates a requisition is referred to as the preparer of the requisition.</span></span> <span data-ttu-id="3c628-113">Kā sagatavotājs varat veikt tālāk aprakstītos uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="3c628-113">As a preparer, you can complete the following tasks.</span></span>

<span data-ttu-id="3c628-114">Izmantojiet rindas darbību **Ārējie katalogi**, lai atvērtu lapu, kurā ir visi norādītajam pieprasītājam, iepirkuma juridiskajai personai un saņemošajai pārvaldības struktūrvienībai pieejamie ārējie katalogi.</span><span class="sxs-lookup"><span data-stu-id="3c628-114">Use the **External catalogs** line action to open a page that includes all external catalogs that are available for the specified requester, buying legal entity, and receiving operating unit.</span></span>

<span data-ttu-id="3c628-115">Atkarībā no jūsu atļaujām mainiet pieprasītāju, iepirkuma juridisko personu un saņemošo pārvaldības struktūrvienību.</span><span class="sxs-lookup"><span data-stu-id="3c628-115">Depending on your permissions, change the requester, buying legal entity, and receiving operating unit.</span></span> <span data-ttu-id="3c628-116">Šo vērtības izmaiņas var mainīt sarakstu ar ārējiem katalogiem, kas ir pieejami pieprasītājam.</span><span class="sxs-lookup"><span data-stu-id="3c628-116">A change in those values might change the list of external catalogs that are available to a requester.</span></span> <span data-ttu-id="3c628-117">Pieejamie ārējie katalogi ir atkarīgi no pašreizējiem aktīvajiem pirkšanas ierobežojumiem iepirkuma juridiskajai personai vai saņemošajai pārvaldības struktūrvienībai.</span><span class="sxs-lookup"><span data-stu-id="3c628-117">The external catalogs that are available depend on the current active purchasing policies for the buying legal entity or the receiving operating unit.</span></span> <span data-ttu-id="3c628-118">Šie ierobežojumi var atļaut vai liegt piekļuvi noteiktām sagādes kategorijām.</span><span class="sxs-lookup"><span data-stu-id="3c628-118">These policies can allow or prevent access to specific procurement categories.</span></span> <span data-ttu-id="3c628-119">Tādējādi var tikt ietekmēts saraksts ar ārējiem katalogiem, kas tiek kartēti uz šīm sagādes kategorijām.</span><span class="sxs-lookup"><span data-stu-id="3c628-119">Therefore, the list of external catalogs that are mapped to these procurement categories can be affected.</span></span>

<span data-ttu-id="3c628-120">Papildinformāciju par ierobežojumiem skatiet sadaļā [Pirkšanas ierobežojumu pārskats](../procurement/purchase-policies.md).</span><span class="sxs-lookup"><span data-stu-id="3c628-120">For more information about policies, see [Purchasing policies overview](../procurement/purchase-policies.md).</span></span>

- <span data-ttu-id="3c628-121">Lai atrastu ārējos katalogus noteiktām sagādes kategorijām, ievadiet tekstu katalogu meklēšanas laukā.</span><span class="sxs-lookup"><span data-stu-id="3c628-121">To find external catalogs for specific procurement categories, enter text in the catalog search field.</span></span>
- <span data-ttu-id="3c628-122">Lai pievienotu preces no kreditora ārējā kataloga kreditora vietnē, noklikšķiniet uz ārējā kataloga.</span><span class="sxs-lookup"><span data-stu-id="3c628-122">To add products from a vendor’s external catalog on the vendor’s website, click the external catalog.</span></span> <span data-ttu-id="3c628-123">Pēc tam pievienojiet preces iepirkumu grozam un paņemiet tās. Iepirkumu groza rindas tiks pārsūtītas uz Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="3c628-123">Then add products to the shopping cart, and check out. The shopping cart lines will be transferred to Microsoft Dynamics 365.</span></span>

<span data-ttu-id="3c628-124">Ja sagādes kategorijām ir vairākas opcijas, atlasiet pareizo sagādes kategoriju, pirms pievienojat rindas pieprasījumam.</span><span class="sxs-lookup"><span data-stu-id="3c628-124">If there are multiple options for procurement categories, select the correct procurement category before you add the lines to the requisition.</span></span>
<span data-ttu-id="3c628-125">Pēc tam, kad rindas ir pievienotas pieprasījumam, varat pievienot vairāk rindu, neizmantojot ārējos katalogus.</span><span class="sxs-lookup"><span data-stu-id="3c628-125">After lines have been added to a requisition, you can add more lines without using external catalogs.</span></span> <span data-ttu-id="3c628-126">Vai arī varat turpināt izmantot ārējos katalogus, lai pievienotu rindas.</span><span class="sxs-lookup"><span data-stu-id="3c628-126">Alternatively, you can continue to use external catalogs to add lines.</span></span>

<span data-ttu-id="3c628-127">Kad pieprasījums ir gatavs, izmantojiet darbību **Darbplūsma** > **Iesniegt**, lai to iesniegtu apstiprināšanai.</span><span class="sxs-lookup"><span data-stu-id="3c628-127">When the requisition is ready, use the **Workflow** > **Submit** action to submit it for approval.</span></span>
