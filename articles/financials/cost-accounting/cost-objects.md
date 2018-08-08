---
title: Izmaksu objekta dimensijas
description: "Analizējot izmaksas, jūs izmantojat izmaksu elementa dimensijas, lai noteiktu, kur plūst izmaksas. Izmaksu objekta dimensijas tiek izmantotas, lai noteiktu, kur var piešķirt izmaksas. Šajā tēmā ir sniegta informācija par izmaksas objekta dimensijām."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimensionMember
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 223174
ms.assetid: 2a1cdd35-30cb-41e7-9506-67fd04a537c5
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 60a6575387a6ebe3b349a61368a7561d78dc69f3
ms.contentlocale: lv-lv
ms.lasthandoff: 08/07/2018

---

# <a name="cost-object-dimensions"></a><span data-ttu-id="d7019-105">Izmaksu objekta dimensijas</span><span class="sxs-lookup"><span data-stu-id="d7019-105">Cost object dimensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d7019-106">Analizējot izmaksas, jūs izmantojat izmaksu elementa dimensijas, lai noteiktu, kur plūst izmaksas.</span><span class="sxs-lookup"><span data-stu-id="d7019-106">When you analyze costs, you use cost element dimensions to determine where costs flow to.</span></span> <span data-ttu-id="d7019-107">Izmaksu objekta dimensijas tiek izmantotas, lai noteiktu, kur var piešķirt izmaksas.</span><span class="sxs-lookup"><span data-stu-id="d7019-107">You use cost object dimensions to determine where you should assign costs.</span></span> <span data-ttu-id="d7019-108">Šajā tēmā ir sniegta informācija par izmaksas objekta dimensijām.</span><span class="sxs-lookup"><span data-stu-id="d7019-108">This topic provides information about cost object dimensions.</span></span>

<span data-ttu-id="d7019-109">Izmaksu objekts var būt jebkura veida objekts, kuru vēlaties novērtēt, iedalīt izmaksas vai mērīt pa tiešo.</span><span class="sxs-lookup"><span data-stu-id="d7019-109">A cost object can be any type of object that you want to estimate, allocate costs to, or measure directly.</span></span> <span data-ttu-id="d7019-110">Tipiski izmaksu objekti ietver preces, projektus, resursus, nodaļas, izmaksu centrus un ģeogrāfiskus reģionus.</span><span class="sxs-lookup"><span data-stu-id="d7019-110">Typical cost objects include products, projects, resources, departments, cost centers, and geographical regions.</span></span> <span data-ttu-id="d7019-111">Vadība izmanto izmaksu objektus, lai aprēķinātu izmaksu daudzumu, kā arī veiktu ienesīguma analīzi.</span><span class="sxs-lookup"><span data-stu-id="d7019-111">Management uses cost objects to quantify costs and also to drive profitability analysis.</span></span>

## <a name="cost-object-dimensions-and-cost-object-dimension-members"></a><span data-ttu-id="d7019-112">Izmaksu objekta dimensijas un izmaksu objekta dimensijas dalībnieki</span><span class="sxs-lookup"><span data-stu-id="d7019-112">Cost object dimensions and cost object dimension members</span></span>
<span data-ttu-id="d7019-113">Izmaksu objekti tiek saukti par *izmaksu objekta dimensijas*.</span><span class="sxs-lookup"><span data-stu-id="d7019-113">Cost objects are known as *cost object dimensions*.</span></span> <span data-ttu-id="d7019-114">Pēc tam, kad esat izlēmis, uz kuru elementu jāattiecas izmaksu objekta dimensijai, norādiet atsevišķas dimensijas vērtības, vai arī importējiet tas Izmaksu uzskaitē no citām avota sistēmām.</span><span class="sxs-lookup"><span data-stu-id="d7019-114">After you’ve decided which entity the cost object dimension should refer to, you must specify the individual dimension values or import them into Cost accounting from other source systems.</span></span> <span data-ttu-id="d7019-115">Šīs atsevišķās dimensiju vērtības tiek sauktas par *izmaksu objekta dimensijas dalībnieki*.</span><span class="sxs-lookup"><span data-stu-id="d7019-115">These individual dimension values are known as *cost object dimension members*.</span></span> <span data-ttu-id="d7019-116">Piemēram, jūs vēlaties izmantot finanšu dimensiju, kas ir nosaukta Izmaksu centrs kā izmaksu objekta dimensiju.</span><span class="sxs-lookup"><span data-stu-id="d7019-116">For example, you want to use the financial dimension that is named Cost center as the cost object dimension.</span></span> <span data-ttu-id="d7019-117">Lai apskatītu, kā izmaksas plūst uz atsevišķiem izmaksu centriem, nepieciešams importēt izmaksu objekta dimensijas dalībniekus.</span><span class="sxs-lookup"><span data-stu-id="d7019-117">To see how costs flow to the individual cost centers, you must import the cost object dimension members.</span></span> <span data-ttu-id="d7019-118">Šajā gadījumā izmaksu objekta dimensijas dalībnieki ir faktiskie izmaksu centri, piemēram, Pārdošana, Ražošana, Administrēšana un Ģeogrāfiskas vietas.</span><span class="sxs-lookup"><span data-stu-id="d7019-118">In this case, the cost object dimension members are the actual cost centers, such as Sales, Production, Administration, and Geographic locations.</span></span> <span data-ttu-id="d7019-119">Šajā ekrānuzņēmumā parādīts Izmaksu centru kā izmaksu objekta dimensijas piemērs, ar tā faktiskajiem izmaksu centriem kā izmaksu objekta dimensijas dalībniekiem.</span><span class="sxs-lookup"><span data-stu-id="d7019-119">The following screenshot shows an example of Cost Centers as the cost object dimension with its actual cost centers as cost object dimension members.</span></span> 

<span data-ttu-id="d7019-120">[![cost-object-dimensions](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="d7019-120">[![cost-object-dimensions](./media/cost-object-dimensions.png)](./media/cost-object-dimensions.png)</span></span>

## <a name="import-cost-object-dimension-members-through-data-connectors"></a><span data-ttu-id="d7019-121">Importējiet izmaksu objekta dimensijas dalībniekus, izmantojot datu savienotājus</span><span class="sxs-lookup"><span data-stu-id="d7019-121">Import cost object dimension members through data connectors</span></span>
<span data-ttu-id="d7019-122">Lai atvieglotu izmaksu objekta dimensijas dalībnieku importēšanu, izmantojiet datu savienotājus, lai izgūtu vērtības no elementiem, kurus vēlaties izmantot kā izmaksu objekta dimensijas.</span><span class="sxs-lookup"><span data-stu-id="d7019-122">To make the import of cost object dimension members easier, you use data connectors to retrieve the values from the entities that you want to use as cost object dimensions.</span></span> <span data-ttu-id="d7019-123">Jūs varat izmantot iepriekš izveidotus datu savienotājus vai pielāgotus datu savienotājus, ko esat izveidojis.</span><span class="sxs-lookup"><span data-stu-id="d7019-123">You can use either the pre-built data connectors or custom data connectors that you build.</span></span>




