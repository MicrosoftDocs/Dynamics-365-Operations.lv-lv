---
title: Darba pasūtījumu izveidošana
description: Šajā tēmā ir paskaidrots, kā izveidot darba pasūtījumus programmā Asset Management.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
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
ms.openlocfilehash: f94f8bc20753e38ce1cb6eccdfbc85c2e491ffad
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206131"
---
# <a name="creating-work-orders"></a><span data-ttu-id="1790b-103">Darba pasūtījumu izveidošana</span><span class="sxs-lookup"><span data-stu-id="1790b-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="1790b-104">Kad ir izveidots profilaktisks uzturēšanas darbs, nākamais solis ir darba pasūtījumu izveide darbiem.</span><span class="sxs-lookup"><span data-stu-id="1790b-104">When you have scheduled preventive maintenance jobs, next step is to create work orders for the jobs.</span></span> <span data-ttu-id="1790b-105">Tas tiek darīts kādā uzturēšanas grafikā.</span><span class="sxs-lookup"><span data-stu-id="1790b-105">This is done in one of the maintenance schedules.</span></span> <span data-ttu-id="1790b-106">Uzturēšanas grafikā ieplānotajiem darbiem var būt dažādi atsauces veidi.</span><span class="sxs-lookup"><span data-stu-id="1790b-106">The scheduled jobs in a maintenance schedule can have different reference types:</span></span>

| <span data-ttu-id="1790b-107">Atsauces tips</span><span class="sxs-lookup"><span data-stu-id="1790b-107">Reference type</span></span> | <span data-ttu-id="1790b-108">Apraksts</span><span class="sxs-lookup"><span data-stu-id="1790b-108">Description</span></span>                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1790b-109">Uzturēšanas plāni</span><span class="sxs-lookup"><span data-stu-id="1790b-109">Maintenance plans</span></span>     | <span data-ttu-id="1790b-110">Profilaktiskie uzturēšanas darbi, balstoties uz apkopes plāna veidiem „Laiks” vai „Skaitītājs”.</span><span class="sxs-lookup"><span data-stu-id="1790b-110">Preventive maintenance jobs based on maintenance plan types "Time" or "Counter".</span></span>                       |
| <span data-ttu-id="1790b-111">Uzturēšanas cikls</span><span class="sxs-lookup"><span data-stu-id="1790b-111">Maintenance rounds</span></span>    | <span data-ttu-id="1790b-112">Profilaktiskie uzturēšanas darbi, kas satur vairākus līdzekļus, kam vajadzīga viena veida uzturēšana.</span><span class="sxs-lookup"><span data-stu-id="1790b-112">Preventive maintenance jobs containing several assets that require a similar type of maintenance.</span></span>           |
| <span data-ttu-id="1790b-113">Uzturēšanas pieprasījums</span><span class="sxs-lookup"><span data-stu-id="1790b-113">Maintenance request</span></span>   | <span data-ttu-id="1790b-114">Manuāli izveidots pieprasījums līdzekļa uzturēšanai vai remontam, ko var pārvērt par darba pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="1790b-114">Manually created request for maintenance or repair of an asset, which can be converted into a work order.</span></span> |


1. <span data-ttu-id="1790b-115">Noklikšķiniet uz **Līdzekļu pārvaldība** > **Vispārīgi** > **Viss uzturēšanas grafiks** vai **Atvērt uzturēšanas grafika rindas**, vai **Atvērt uzturēšanas grafika kopas**.</span><span class="sxs-lookup"><span data-stu-id="1790b-115">Click **Asset management** > **Common** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="1790b-116">Atlasiet ieplānotos uzturēšanas darbus, kam vēlaties izveidot darba pasūtījumu, un noklikšķiniet uz **Darba pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="1790b-116">Select the scheduled maintenance jobs for which you want to create a work order and click **Work order**.</span></span> <span data-ttu-id="1790b-117">Dialoglodziņā **Izveidot darba pasūtījumus** kopīgais paredzamais stundu skaits atlasītajām rindām tiek parādīts laukā **Uzturēšanas prognozes stundas**.</span><span class="sxs-lookup"><span data-stu-id="1790b-117">In the **Create work orders** dialog, the total number of forecast hours for the selected lines is shown in the **Maintenance forecast hours** field.</span></span>

3. <span data-ttu-id="1790b-118">Sadaļā **Parametri** atlasiet, cik darba pasūtījumu jāizveido.</span><span class="sxs-lookup"><span data-stu-id="1790b-118">In the **Parameters** section, select how many work orders should be created.</span></span> <span data-ttu-id="1790b-119">Varat izveidot vienu darba pasūtījumu uzturēšanas grafika rindai vai vairākus darba uzdevumus, balstoties uz jūsu izvēli sadaļā **Viens darba pasūtījums kategorijā**.</span><span class="sxs-lookup"><span data-stu-id="1790b-119">You can create one work order per maintenance schedule line, or a number of work orders based on your selections in the **One work order per** section.</span></span>

4. <span data-ttu-id="1790b-120">Atlasiet **Darba pasūtījuma veidu**, kas tiks izmantots visiem jūsu veidotajiem darba pasūtījumiem.</span><span class="sxs-lookup"><span data-stu-id="1790b-120">Select a **Work order type** that will be used on all the work orders you create.</span></span> <span data-ttu-id="1790b-121">Attēlā zemāk ir parādīts dialoglodziņš **Izveidot darba pasūtījumus**.</span><span class="sxs-lookup"><span data-stu-id="1790b-121">The illustration below shows an example of the **Create work orders** dialog.</span></span>

![1. attēls](media/18-preventive-maintenance.png)

5. <span data-ttu-id="1790b-123">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="1790b-123">Click **OK**.</span></span> <span data-ttu-id="1790b-124">Tiek izveidots viens vai vairāki darba pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="1790b-124">One or more work orders are created.</span></span>

