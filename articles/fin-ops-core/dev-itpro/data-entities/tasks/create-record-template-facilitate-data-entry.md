---
title: Ieraksta veidnes izveide, lai atvieglotu datu ievadi
description: Šajā tēmā parādīts, kā izveidot ieraksta veidni, lai lauka vērtības, ko bieži izmanto, nav atsevišķi jāievada katram jaunam ierakstam.
author: margoc
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, SysRecordInfo, SysRecordTemplatePromptOnCreate
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec21415158ad611d0ad55778e76aa128f53561bd
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143388"
---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="e57be-103">Ieraksta veidnes izveide, lai atvieglotu datu ievadi</span><span class="sxs-lookup"><span data-stu-id="e57be-103">Create a record template to facilitate data entry</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e57be-104">Šajā tēmā parādīts, kā izveidot ieraksta veidni, lai lauka vērtības, ko bieži izmanto, nav atsevišķi jāievada katram jaunam ierakstam.</span><span class="sxs-lookup"><span data-stu-id="e57be-104">This topic demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="e57be-105">Šajā procedūrā jūs izveidosiet jaunu ierakstu par jauniem klēpjdatoriem, kas ir jāpievieno jūsu pamatlīdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="e57be-105">In this procedure, you'll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="e57be-106">Šajā procedūrā tiek izmantoti parauga uzņēmuma USMF dati.</span><span class="sxs-lookup"><span data-stu-id="e57be-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="e57be-107">Navigācijas rūtī ejiet uz **Moduļi > Pamatlīdzekļi > Pamatlīdzekļi > Pamatlīdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="e57be-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="e57be-108">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="e57be-108">Select **New**.</span></span>
3. <span data-ttu-id="e57be-109">Ievadiet vai atlasiet vērtību laukā **Pamatlīdzekļa grupa**.</span><span class="sxs-lookup"><span data-stu-id="e57be-109">In the **Fixed asset group** field, enter or select a value.</span></span>
4. <span data-ttu-id="e57be-110">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e57be-110">In the **Name** field, type a value.</span></span> <span data-ttu-id="e57be-111">Piemēram, ievadiet **Uzņēmuma interesenta klēpjdators**.</span><span class="sxs-lookup"><span data-stu-id="e57be-111">For example, enter **Corporate lead laptop**.</span></span>  
5. <span data-ttu-id="e57be-112">Laukā **Meklēt vārdu** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="e57be-112">In the **Search name** field, type a value.</span></span> <span data-ttu-id="e57be-113">Piemēram, ievadiet **klēpjdators**.</span><span class="sxs-lookup"><span data-stu-id="e57be-113">For example, enter **laptop**.</span></span>  
6. <span data-ttu-id="e57be-114">Izvērsiet sadaļu **Tehniskā informācija**.</span><span class="sxs-lookup"><span data-stu-id="e57be-114">Expand the **Technical information** section.</span></span>
7. <span data-ttu-id="e57be-115">Ierakstiet vērtības laukos **Izgatavotājs**, **Modelis**, **Modeļa gads**.</span><span class="sxs-lookup"><span data-stu-id="e57be-115">In the **Make**, **Model**, and **Model year** fields, type values.</span></span>
8. <span data-ttu-id="e57be-116">Darbību rūtī atlasiet **Opcijas**.</span><span class="sxs-lookup"><span data-stu-id="e57be-116">On the Action Pane, select **Options**.</span></span>
9. <span data-ttu-id="e57be-117">Atlasiet **Ieraksta informācija**.</span><span class="sxs-lookup"><span data-stu-id="e57be-117">Select **Record info**.</span></span>
10. <span data-ttu-id="e57be-118">Atlasiet **Lietotāja veidne**.</span><span class="sxs-lookup"><span data-stu-id="e57be-118">Select **User template**.</span></span>
11. <span data-ttu-id="e57be-119">Laukā **Nosaukums** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e57be-119">In the **Name** field, type a value.</span></span>
12. <span data-ttu-id="e57be-120">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="e57be-120">In the **Description** field, type a value.</span></span>
13. <span data-ttu-id="e57be-121">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="e57be-121">Select **OK**.</span></span>
14. <span data-ttu-id="e57be-122">Atlasiet **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="e57be-122">Select **Close**.</span></span>

