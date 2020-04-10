---
title: Izveidot organizācijas hierarhiju
description: Lai izveidotu organizācijas hierarhiju, veiciet šādas darbības.
author: sericks007
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMHierarchyManager, OMHierarchyPurposeAssociation, OMHierarchySelection, HierarchyDesigner
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dde06f758be57fb646696c861218565476abcadc
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140563"
---
# <a name="create-an-organization-hierarchy"></a><span data-ttu-id="3aad6-103">Izveidot organizācijas hierarhiju</span><span class="sxs-lookup"><span data-stu-id="3aad6-103">Create an organization hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3aad6-104">Lai izveidotu organizācijas hierarhiju, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="3aad6-104">Use the following procedure to create an organizational hierarchy.</span></span> <span data-ttu-id="3aad6-105">Varat izmantot organizācijas hierarhijas, lai apskatītu jūsu uzņēmējtransakciju no dažādām perspektīvām un veidotu pārskatus.</span><span class="sxs-lookup"><span data-stu-id="3aad6-105">You can use organizational hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="3aad6-106">Piemēram, varat iestatīt vienu hierarhiju nodokļu, juridiskajai vai ar likumu noteikto pārskatu veidošanai.</span><span class="sxs-lookup"><span data-stu-id="3aad6-106">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="3aad6-107">Pēc tam varat iestatīt citu hierarhiju, lai veidotu pārskatu par finanšu informāciju, kas saskaņā ar likumu nav obligāta, bet tiek izmantota iekšējos pārskatos.</span><span class="sxs-lookup"><span data-stu-id="3aad6-107">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span> 

<span data-ttu-id="3aad6-108">Pirms organizācijas hierarhijas izveides jāizveido organizācijas.</span><span class="sxs-lookup"><span data-stu-id="3aad6-108">Before you create an organizational hierarchy, you must create organizations.</span></span> <span data-ttu-id="3aad6-109">Papildinformāciju skatiet uzdevumos "Izveidot juridisko personu" vai "Izveidot pārvaldības struktūrvienību".</span><span class="sxs-lookup"><span data-stu-id="3aad6-109">For more information, see the "Create a legal entity" or "Create an operating unit" tasks.</span></span> <span data-ttu-id="3aad6-110">Varat arī izveidot nodaļas un darba grupas.</span><span class="sxs-lookup"><span data-stu-id="3aad6-110">You can also create departments and teams.</span></span> 

<span data-ttu-id="3aad6-111">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="3aad6-111">The demo data company used to create this procedure is USMF.</span></span>

## <a name="create-a-hierarchy"></a><span data-ttu-id="3aad6-112">Izveidot hierarhiju</span><span class="sxs-lookup"><span data-stu-id="3aad6-112">Create a hierarchy</span></span>
1. <span data-ttu-id="3aad6-113">Ejiet uz **Navigācijas rūts > Moduļi > Organizācijas administrēšana > Organizācijas > Organizācijas hierarhijas**.</span><span class="sxs-lookup"><span data-stu-id="3aad6-113">Go to **Navigation pane > Modules > Organization administration > Organizations > Organization hierarchies**.</span></span>
2. <span data-ttu-id="3aad6-114">**Darbību rūtī** noklikšķiniet uz **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="3aad6-114">On the **Action pane**, click **New**.</span></span>
3. <span data-ttu-id="3aad6-115">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="3aad6-115">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="3aad6-116">Sadaļā **Nolūks** klikšķiniet uz **Piešķirt nolūku**.</span><span class="sxs-lookup"><span data-stu-id="3aad6-116">In the **Purpose** section, click **Assign purpose**.</span></span>
5. <span data-ttu-id="3aad6-117">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="3aad6-117">In the list, find and select the desired record.</span></span> <span data-ttu-id="3aad6-118">Atlasiet nolūku, kas tiks piešķirts jūsu organizācijas hierarhijai.</span><span class="sxs-lookup"><span data-stu-id="3aad6-118">Select a purpose to assign to your organization hierarchy.</span></span>  
6. <span data-ttu-id="3aad6-119">Sadaļā **Piešķirtās hierarhijas** klikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="3aad6-119">In the **Assigned hierarchies** sectiom, click **Add**.</span></span>
7. <span data-ttu-id="3aad6-120">Sarakstā atzīmējiet atlasīto rindu.</span><span class="sxs-lookup"><span data-stu-id="3aad6-120">In the list, mark the selected row.</span></span> <span data-ttu-id="3aad6-121">Atrodiet tikko izveidoto hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="3aad6-121">Find the hierarchy you just created.</span></span>  
8. <span data-ttu-id="3aad6-122">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="3aad6-122">Click **OK**.</span></span>

## <a name="add-organizations-to-the-hierarchy"></a><span data-ttu-id="3aad6-123">Pievienot organizācijas hierarhijai</span><span class="sxs-lookup"><span data-stu-id="3aad6-123">Add organizations to the hierarchy</span></span>
1. <span data-ttu-id="3aad6-124">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="3aad6-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="3aad6-125">Atlasiet hierarhiju.</span><span class="sxs-lookup"><span data-stu-id="3aad6-125">Select your hierarchy.</span></span>  
2. <span data-ttu-id="3aad6-126">Sadaļā **Piešķirtās hierarhijas** klikšķiniet uz **Skatīt hierarhiju**.</span><span class="sxs-lookup"><span data-stu-id="3aad6-126">In the **Assigned hierarchies** section, click **View hierarchy**.</span></span>
    - <span data-ttu-id="3aad6-127">Nepieciešamības gadījumā pievienojiet papildu organizācijas.</span><span class="sxs-lookup"><span data-stu-id="3aad6-127">Add organizations, as necessary.</span></span>  
    - <span data-ttu-id="3aad6-128">Lai pievienotu organizāciju, klikšķiniet uz **Rediģēt**, tad uz **Ievietot**.</span><span class="sxs-lookup"><span data-stu-id="3aad6-128">To add an organization, click **Edit** and then **Insert** to add the organization.</span></span> <span data-ttu-id="3aad6-129">Kad esat veicis vajadzīgās izmaiņas, varat **Saglabāt** melnrakstu un/vai **Publicēt** izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="3aad6-129">When you are done making changes you can **Save** a draft and/or **Publish** the changes.</span></span>  

