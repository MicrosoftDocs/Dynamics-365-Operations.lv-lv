---
title: Uzturēšanas statuss
description: Šajā tēmā ir paskaidrots, kā aprēķināt uzturēšanas stāvokli programmā Asset Management.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetStatusCalculate, EntAssetStatus
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f3d6f86c5052c845c9c8aad1e4437f4196f78b50
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808620"
---
# <a name="maintenance-status"></a><span data-ttu-id="5303d-103">Uzturēšanas statuss</span><span class="sxs-lookup"><span data-stu-id="5303d-103">Maintenance status</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="5303d-104">Līdzekļu pārvaldībā jūs varat veikt pārskatu aprēķinus konkrētā periodā jauniem, aktīviem un pabeigtiem uzturēšanas pieprasījumiem, darba pasūtījumiem un dīkstāves uzturēšanas dēļ darbībām.</span><span class="sxs-lookup"><span data-stu-id="5303d-104">In Asset Management, you can make an overview calculation for a specific period for new, active, and completed maintenance requests, work orders, and maintenance downtime activities.</span></span> <span data-ttu-id="5303d-105">Jūs varat arī redzēt pabeigto nosacījuma izvērtējumu skaitu šim pašam periodam.</span><span class="sxs-lookup"><span data-stu-id="5303d-105">You can also see the number of completed condition assessments for the same period.</span></span> <span data-ttu-id="5303d-106">Izmantojiet šo aprēķinu, lai iegūtu pārskatu par ienākošo un pabeigto uzturēšanas pieprasījumu un darba pasūtījumu darba slodzi.</span><span class="sxs-lookup"><span data-stu-id="5303d-106">Use this calculation to get an overview of workload for incoming and completed maintenance requests and work orders.</span></span>

## <a name="make-a-maintenance-status-calculation"></a><span data-ttu-id="5303d-107">Veiciet uzturēšanas stāvokļa aprēķinus</span><span class="sxs-lookup"><span data-stu-id="5303d-107">Make a maintenance status calculation</span></span>

1. <span data-ttu-id="5303d-108">Noklikšķiniet uz **Līdzekļu pārvaldība** > **Pieprasījumi** > **Uzturēšanas stāvoklis**.</span><span class="sxs-lookup"><span data-stu-id="5303d-108">Click **Asset management** > **Inquiries** > **Maintenance status**.</span></span>

2. <span data-ttu-id="5303d-109">Dialoglodziņā **Aprēķināt stāvokli** atlasiet laika diapazonu, kuram vēlaties veikt aprēķinu, laukos **Datums no** un **Datums līdz**.</span><span class="sxs-lookup"><span data-stu-id="5303d-109">In the **Calculate status** dialog, select the time range that you want to make the calculation in the **From date** and **To date** fields.</span></span>

3. <span data-ttu-id="5303d-110">Jūs varat izmantot lauku **Līmenis**, lai noteiktu, cik detalizētas vēlaties uzturēšanas rindas attiecībā uz funkcionālo novietojumu.</span><span class="sxs-lookup"><span data-stu-id="5303d-110">You can use the **Level** field to indicate how detailed you want the maintenance lines to be regarding functional locations.</span></span> 

  <span data-ttu-id="5303d-111">Piemēram, ja laukā ievadāt ciparu "1" un jums ir vairāklīmeņu funkcionālā novietojuma struktūra, visas uzturēšanas grafika rindas funkcionālajam novietojumam tiks uzrādītas augstākajā līmenī, tāpēc stāvoklis rindā var tikt pievienotas no funkcionāliem novietojumiem, kas atrodas zemākā līmenī.</span><span class="sxs-lookup"><span data-stu-id="5303d-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance lines for a functional location will be shown on the top level, and therefore the status on a line may be added up from functional locations located at a lower level.</span></span> 
  
  <span data-ttu-id="5303d-112">Ja laukā **Līmenis** ievadāt ciparu "0", jūs redzēsit detalizētu rezultātu, kas uzrādīs visas uzturēšanas rindas visos funkcionālā novietojuma līmeņos, ar kuriem tie ir saistīti.</span><span class="sxs-lookup"><span data-stu-id="5303d-112">If you insert the number "0" in the **Level** field, you see a detailed result showing all maintenance lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="5303d-113">Noklikšķiniet uz **Labi**, lai sāktu aprēķināšanu.</span><span class="sxs-lookup"><span data-stu-id="5303d-113">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="5303d-114">Noklikšķiniet uz pogas **Grupēt pēc**, lai uzrādītu nepieciešamo aprēķina informācijas detalizācijas līmeni.</span><span class="sxs-lookup"><span data-stu-id="5303d-114">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="5303d-115">Atlasītās **Grupēt pēc** pogas ir izceltas.</span><span class="sxs-lookup"><span data-stu-id="5303d-115">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="5303d-116">Noklikšķiniet uz pogas, lai to aktivizētu vai deaktivizētu.</span><span class="sxs-lookup"><span data-stu-id="5303d-116">Click on a button to activate or deactivate it.</span></span>

6. <span data-ttu-id="5303d-117">Neaizmirstiet noklikšķināt uz pogas **Atjaunināt**, lai atjauninātu aprēķinus katru reizi, kad veicat izmaiņas, aktivizējot vai deaktivizējot pogas **Grupēt pēc** vai veicot aprēķinu jaunam periodam.</span><span class="sxs-lookup"><span data-stu-id="5303d-117">Remember to click the **Update** button to update the calculation each time you make changes by activating or deactivating **Group by** buttons, or by making a calculation for a new period.</span></span>

7. <span data-ttu-id="5303d-118">Noklikšķiniet uz **Stāvoklis**, ja vēlaties izveidot jaunu uzturēšanas statusa aprēķinu.</span><span class="sxs-lookup"><span data-stu-id="5303d-118">Click **Status** if you want to create a new maintenance status calculation.</span></span>

>[!NOTE]
><span data-ttu-id="5303d-119">Rezultāti, kas parādās laukā **Uzturēšanas stāvoklis** ietver vienīgi uzturēšanas pieprasījumus un darba pasūtījumus, kuriem ir reāls sākuma datums un laiks.</span><span class="sxs-lookup"><span data-stu-id="5303d-119">The results shown in **Maintenance status** only include maintenance requests and work orders that have an actual start date and time.</span></span> <span data-ttu-id="5303d-120">Beigu datuma un laika lauki var būt tukši.</span><span class="sxs-lookup"><span data-stu-id="5303d-120">End date and time may be blank.</span></span>

## <a name="example-1"></a><span data-ttu-id="5303d-121">1. piemērs</span><span class="sxs-lookup"><span data-stu-id="5303d-121">Example 1</span></span>

<span data-ttu-id="5303d-122">Zemāk esošajā ekrānuzņēmumā ir aktivizētas pogas **Gads** un **Mēnesis**.</span><span class="sxs-lookup"><span data-stu-id="5303d-122">In the screenshot below, the **Year** and **Month** buttons have been activated.</span></span> <span data-ttu-id="5303d-123">Atlasot šīs **Grupēt pēc** opcijas, jūs saņemat vispārīgu ikmēneša pārskatu par darba slodzi un caurlaidspēju attiecībā uz uzturēšanas pieprasījumiem un darba pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="5303d-123">With these **Group by** options selected, you get a general overview on a monthly basis of workload and throughput related to maintenance requests and work orders.</span></span> 

![Mēneša darba slodzes piemērs](media/13-controlling-and-reporting.png)

## <a name="example-2"></a><span data-ttu-id="5303d-125">2. piemērs</span><span class="sxs-lookup"><span data-stu-id="5303d-125">Example 2</span></span>

<span data-ttu-id="5303d-126">Zemāk esošajā ekrānuzņēmumā ir pievienota informācija par funkcionālo novietojumu.</span><span class="sxs-lookup"><span data-stu-id="5303d-126">In the screenshot below, information about functional locations has been added.</span></span> <span data-ttu-id="5303d-127">Tagad ir iespējams salīdzināt darba slodzi un caurlaidspēju dažādos funkcionālajos novietojumos, kas var reprezentēt ģeogrāfisko novietojumu, ražotnes vai darba zonas.</span><span class="sxs-lookup"><span data-stu-id="5303d-127">Now it is possible to compare workload and throughput across functional locations, which may represent geographical locations, factories, or work areas.</span></span> 

![Mēneša darba slodzes piemērs ar funkcionālajiem novietojumiem](media/14-controlling-and-reporting.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]