---
title: Ieraksta veidnes izveide, lai atvieglotu datu ievadi
description: Šajā procedūrā ir parādīts, kā izveidot ierakstu veidnes, lai katram jaunam ierakstam nevajadzētu atkārtoti ievadīt bieži izmantotās lauku vērtības.
author: margoc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, SysRecordInfo, SysRecordTemplatePromptOnCreate
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 36d14c386322adab0cc0ba9b7b47c874aefbe519
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544256"
---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="c937a-103">Ieraksta veidnes izveide, lai atvieglotu datu ievadi</span><span class="sxs-lookup"><span data-stu-id="c937a-103">Create a record template to facilitate data entry</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c937a-104">Šajā procedūrā ir parādīts, kā izveidot ierakstu veidnes, lai katram jaunam ierakstam nevajadzētu atkārtoti ievadīt bieži izmantotās lauku vērtības.</span><span class="sxs-lookup"><span data-stu-id="c937a-104">This procedure demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="c937a-105">Šajā procedūrā jūs izveidosiet jaunu ierakstu par jauniem klēpjdatoriem, kas ir jāpievieno jūsu pamatlīdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="c937a-105">In this procedure, you’ll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="c937a-106">Šajā procedūrā tiek izmantoti parauga uzņēmuma USMF dati.</span><span class="sxs-lookup"><span data-stu-id="c937a-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="c937a-107">Pārejiet uz sadaļu Pamatlīdzekļi > Pamatlīdzekļi > Pamatlīdzekļi.</span><span class="sxs-lookup"><span data-stu-id="c937a-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="c937a-108">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="c937a-108">Click New.</span></span>
3. <span data-ttu-id="c937a-109">Ievadiet vai atlasiet vērtību laukā Pamatlīdzekļu grupa.</span><span class="sxs-lookup"><span data-stu-id="c937a-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="c937a-110">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="c937a-110">In the Name field, type a value.</span></span>
    * <span data-ttu-id="c937a-111">Ievadiet, piemēram, “Korporatīva potenciālā klienta klēpjdators”.</span><span class="sxs-lookup"><span data-stu-id="c937a-111">For example, enter 'Corporate lead laptop'.</span></span>  
5. <span data-ttu-id="c937a-112">Laukā Meklēšanas nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="c937a-112">In the Search name field, type a value.</span></span>
    * <span data-ttu-id="c937a-113">Ievadiet, piemēram, “klēpjdators”.</span><span class="sxs-lookup"><span data-stu-id="c937a-113">For example, enter 'laptop.'</span></span>  
6. <span data-ttu-id="c937a-114">Izvērsiet sadaļu Tehniskā informācija.</span><span class="sxs-lookup"><span data-stu-id="c937a-114">Expand the Technical information section.</span></span>
7. <span data-ttu-id="c937a-115">Laukā Ražojums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="c937a-115">In the Make field, type a value.</span></span>
8. <span data-ttu-id="c937a-116">Laukā Modelis ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="c937a-116">In the Model field, type a value.</span></span>
9. <span data-ttu-id="c937a-117">Laukā Modeļa gads ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="c937a-117">In the Model year field, type a value.</span></span>
10. <span data-ttu-id="c937a-118">Darbību rūtī noklikšķiniet uz Opcijas.</span><span class="sxs-lookup"><span data-stu-id="c937a-118">On the Action Pane, click Options.</span></span>
11. <span data-ttu-id="c937a-119">Noklikšķiniet uz Informācija par ierakstu.</span><span class="sxs-lookup"><span data-stu-id="c937a-119">Click Record info.</span></span>
12. <span data-ttu-id="c937a-120">Noklikšķiniet uz Lietotāja veidne.</span><span class="sxs-lookup"><span data-stu-id="c937a-120">Click User template.</span></span>
13. <span data-ttu-id="c937a-121">Laukā Nosaukums ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="c937a-121">In the Name field, type a value.</span></span>
    * <span data-ttu-id="c937a-122">Ievadiet, piemēram, “Korporatīva klēpjdators”.</span><span class="sxs-lookup"><span data-stu-id="c937a-122">For example, enter 'Corporate laptop.'</span></span>  
14. <span data-ttu-id="c937a-123">Apraksta laukā ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="c937a-123">In the Description field, type a value.</span></span>
    * <span data-ttu-id="c937a-124">Ievadiet, piemēram, “Korporatīva klēpjdators”.</span><span class="sxs-lookup"><span data-stu-id="c937a-124">For example, enter 'Corporate laptop'.</span></span>  
15. <span data-ttu-id="c937a-125">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="c937a-125">Click OK.</span></span>
16. <span data-ttu-id="c937a-126">Noklikšķiniet uz Aizvērt.</span><span class="sxs-lookup"><span data-stu-id="c937a-126">Click Close.</span></span>

