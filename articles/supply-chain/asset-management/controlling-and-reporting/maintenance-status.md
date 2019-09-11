---
title: Uzturēšanas statuss
description: Šajā tēmā ir paskaidrots, kā aprēķināt uzturēšanas stāvokli programmā Asset Management.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 516607c056125a16e075c33f3c2ad069efb396d9
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918353"
---
# <a name="maintenance-status"></a><span data-ttu-id="4a2ad-103">Uzturēšanas statuss</span><span class="sxs-lookup"><span data-stu-id="4a2ad-103">Maintenance status</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="4a2ad-104">Programmā Asset Management jūs varat veikt aprēķinus, lai iegūtu pārskatu par jauniem, aktīviem un pabeigtiem uzturēšanas pieprasījumiem, darba pasūtījumiem un dīkstāves uzturēšanas dēļ darbībām konkrētā periodā.</span><span class="sxs-lookup"><span data-stu-id="4a2ad-104">In Asset Management, you can make a calculation to see an overview of new, active, and completed maintenance requests, work orders, and maintenance downtime activities for a specific period.</span></span> <span data-ttu-id="4a2ad-105">Jūs varat arī redzēt pabeigto nosacījuma izvērtējumu skaitu šim pašam periodam.</span><span class="sxs-lookup"><span data-stu-id="4a2ad-105">You can also see the number of completed condition assessments for the same period.</span></span> <span data-ttu-id="4a2ad-106">Izmantojiet šo aprēķinu, lai iegūtu pārskatu par darba slodzi attiecībā uz ienākošiem un pabeigtiem uzturēšanas pieprasījumiem un darba pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="4a2ad-106">Use this calculation to get an overview of workload regarding incoming and completed maintenance requests and work orders.</span></span>

## <a name="make-a-maintenance-status-calculation"></a><span data-ttu-id="4a2ad-107">Veiciet uzturēšanas stāvokļa aprēķinus</span><span class="sxs-lookup"><span data-stu-id="4a2ad-107">Make a maintenance status calculation</span></span>

1. <span data-ttu-id="4a2ad-108">Noklikšķiniet uz **Līdzekļu pārvaldība** > **Pieprasījumi** > **Uzturēšanas stāvoklis**.</span><span class="sxs-lookup"><span data-stu-id="4a2ad-108">Click **Asset management** > **Inquiries** > **Maintenance status**.</span></span>

2. <span data-ttu-id="4a2ad-109">Dialoglodziņā **Aprēķināt stāvokli** atlasiet periodu, kuram vēlaties veikt aprēķinu, laukos **Datums no** un **Datums līdz**.</span><span class="sxs-lookup"><span data-stu-id="4a2ad-109">In the **Calculate status** dialog, select the period for which you want to make the calculation in the **From date** and **To date** fields.</span></span>

3. <span data-ttu-id="4a2ad-110">Jūs varat izmantot lauku **Līmenis**, lai noteiktu, cik detalizētas vēlaties uzturēšanas rindas attiecībā uz funkcionālo novietojumu.</span><span class="sxs-lookup"><span data-stu-id="4a2ad-110">You can use the **Level** field to indicate how detailed you want the maintenance lines to be regarding functional locations.</span></span> <span data-ttu-id="4a2ad-111">Piemēram, ja laukā ievadāt ciparu "1" un jums ir vairāklīmeņu funkcionālā novietojuma struktūra, visas uzturēšanas grafika rindas funkcionālajam novietojumam tiks uzrādītas augstākajā līmenī, tāpēc stāvoklis rindā var tikt pievienotas no funkcionāliem novietojumiem, kas atrodas zemākā līmenī.</span><span class="sxs-lookup"><span data-stu-id="4a2ad-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance lines for a functional location will be shown on the top level, and therefore the status on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="4a2ad-112">Ja laukā **Līmenis** ievadāt ciparu "0", jūs redzēsit detalizētu rezultātu, kas uzrādīs visas uzturēšanas rindas visos funkcionālā novietojuma līmeņos, ar kuriem tie ir saistīti.</span><span class="sxs-lookup"><span data-stu-id="4a2ad-112">If you insert the number "0" in the **Level** field, you see a detailed result showing all maintenance lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="4a2ad-113">Noklikšķiniet uz **Labi**, lai sāktu aprēķināšanu.</span><span class="sxs-lookup"><span data-stu-id="4a2ad-113">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="4a2ad-114">Darbības rūšu grupās **Grupēt pēc...** klikšķiniet uz attiecīgās pogas, lai uzrādītu nepieciešamo aprēķina informācijas detalizācijas līmeni.</span><span class="sxs-lookup"><span data-stu-id="4a2ad-114">In the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="4a2ad-115">Atlasītās darbības rūts pogas ir izceltas.</span><span class="sxs-lookup"><span data-stu-id="4a2ad-115">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="4a2ad-116">Noklikšķiniet uz pogas, lai to aktivizētu vai deaktivizētu.</span><span class="sxs-lookup"><span data-stu-id="4a2ad-116">Click on a button to activate or deactivate it.</span></span>

6. <span data-ttu-id="4a2ad-117">Neaizmirstiet noklikšķināt uz pogas **Atjaunināt**, lai atjauninātu aprēķinus katru reizi, kad veicat izmaiņas, aktivizējot vai deaktivizējot pogas **Grupēt pēc...** vai veicot aprēķinu jaunam periodam.</span><span class="sxs-lookup"><span data-stu-id="4a2ad-117">Remember to click the **Update** button to update the calculation each time you make changes by activating or deactivating **Group by...** buttons, or by making a calculation for a new period.</span></span>

7. <span data-ttu-id="4a2ad-118">Noklikšķiniet uz **Stāvoklis**, ja vēlaties izveidot jaunu uzturēšanas statusa aprēķinu.</span><span class="sxs-lookup"><span data-stu-id="4a2ad-118">Click **Status** if you want to create a new maintenance status calculation.</span></span>

>[!NOTE]
><span data-ttu-id="4a2ad-119">Rezultāti, kas parādās laukā **Uzturēšanas stāvoklis** ietver vienīgi uzturēšanas pieprasījumus un darba pasūtījumus, kuriem ir reāls sākuma datums un laiks.</span><span class="sxs-lookup"><span data-stu-id="4a2ad-119">The results shown in **Maintenance status** only include maintenance requests and work orders that have an actual start date and time.</span></span> <span data-ttu-id="4a2ad-120">Beigu datuma un laika lauki var būt tukši.</span><span class="sxs-lookup"><span data-stu-id="4a2ad-120">End date and time may be blank.</span></span>

<span data-ttu-id="4a2ad-121">*1. piemērs:*</span><span class="sxs-lookup"><span data-stu-id="4a2ad-121">*Example 1:*</span></span>

<span data-ttu-id="4a2ad-122">Zemāk esošajā attēlā ir aktivizētas pogas **Gads** un **Mēnesis**.</span><span class="sxs-lookup"><span data-stu-id="4a2ad-122">In the figure below, the **Year** and **Month** buttons have been activated.</span></span> <span data-ttu-id="4a2ad-123">Šeit ir vispārīgs ikmēneša pārskats par darba slodzi un caurlaidspēju attiecībā uz uzturēšanas pieprasījumiem un darba pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="4a2ad-123">Here, you get a general overview on a monthly basis of workload and throughput related to maintenance requests and work orders.</span></span> 

![1. attēls](media/13-controlling-and-reporting.png)

<span data-ttu-id="4a2ad-125">*2. piemērs:*</span><span class="sxs-lookup"><span data-stu-id="4a2ad-125">*Example 2:*</span></span>

<span data-ttu-id="4a2ad-126">Zemāk esošajā attēlā ir pievienota informācija par funkcionālo novietojumu.</span><span class="sxs-lookup"><span data-stu-id="4a2ad-126">In the figure below, information about functional locations has been added.</span></span> <span data-ttu-id="4a2ad-127">Tagad ir iespējams salīdzināt darba slodzi un caurlaidspēju visos funkcionālajos novietojumos, kas var reprezentēt ģeogrāfisko novietojumu, ražotnes vai darba zonas.</span><span class="sxs-lookup"><span data-stu-id="4a2ad-127">Now, it is possible to compare workload and throughput across functional locations, which may represent geographical locations, factories, or work areas.</span></span> 

![2. attēls](media/14-controlling-and-reporting.png)

