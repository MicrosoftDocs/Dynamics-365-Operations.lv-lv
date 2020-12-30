---
title: Numuru sēriju iestatīšana, izmantojot vedni
description: Šajā tēmā tiek skaidrots, kā iestatīt visas nepieciešamās numuru sērijas vienlaikus, izmantojot vedni.
author: sericks007
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceWizard
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ca8174444d5a84f7efb402d6efc787e693801e82
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694743"
---
# <a name="set-up-number-sequences-using-a-wizard"></a><span data-ttu-id="60dc1-103">Numuru sēriju iestatīšana, izmantojot vedni</span><span class="sxs-lookup"><span data-stu-id="60dc1-103">Set up number sequences using a wizard</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="60dc1-104">Numuru sērijas tiek izmantotas, lai ģenerētu lasāmus, unikālus pamatdatu ierakstu identifikatorus un darījumu ierakstus, kam tie ir nepieciešami.</span><span class="sxs-lookup"><span data-stu-id="60dc1-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require them.</span></span> <span data-ttu-id="60dc1-105">Pamatdati vai darījumu ieraksts, kam nepieciešams identifikators, tiek saukts par atsauci.</span><span class="sxs-lookup"><span data-stu-id="60dc1-105">A master data or transaction record that requires an identifier is referred to as a reference.</span></span> <span data-ttu-id="60dc1-106">Pirms atsaucei varat izveidot jaunus ierakstus, ir jāiestata numuru sērija un tā jāsaista ar atsauci.</span><span class="sxs-lookup"><span data-stu-id="60dc1-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="60dc1-107">Šajā tēmā tiek skaidrots, kā iestatīt visas nepieciešamās numuru sērijas vienlaikus, izmantojot vedni.</span><span class="sxs-lookup"><span data-stu-id="60dc1-107">This topic explains how to set up all required number sequences at the same time by using a wizard.</span></span> <span data-ttu-id="60dc1-108">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="60dc1-108">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="60dc1-109">Pārejiet uz **Navigācija > Moduļi > Organizācijas administrēšana > Numuru sērijas > Numuru sērijas**.</span><span class="sxs-lookup"><span data-stu-id="60dc1-109">Go to **Navigation > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="60dc1-110">Atlasiet **Ģenerēt**.</span><span class="sxs-lookup"><span data-stu-id="60dc1-110">Select **Generate**.</span></span>
3. <span data-ttu-id="60dc1-111">Atlasiet **Nākamais**.</span><span class="sxs-lookup"><span data-stu-id="60dc1-111">Select **Next**.</span></span>

   - <span data-ttu-id="60dc1-112">Šajā lapā varat mainīt identifikācijas kodu, mazāko vērtību un lielāko vērtību.</span><span class="sxs-lookup"><span data-stu-id="60dc1-112">On this page, you can modify the identification code, the lowest value, and the highest value.</span></span> <span data-ttu-id="60dc1-113">Turklāt varat norādīt, vai numuru secībai jābūt nepārtrauktai.</span><span class="sxs-lookup"><span data-stu-id="60dc1-113">In addition, you can indicate whether the number sequence must be continuous.</span></span>   
   - <span data-ttu-id="60dc1-114">Neatlasiet opciju **Nepārtraukts**, ja numuri šai numuru sērijai ir jārezervē.</span><span class="sxs-lookup"><span data-stu-id="60dc1-114">Do not select the **Continuous** option if you must preallocate numbers for the number sequence.</span></span> <span data-ttu-id="60dc1-115">Lai pievienotu sfēras segmentu numuru sērijas formātam, sarakstā atlasiet vajadzīgo formātu un pēc tam atlasiet **Iekļaut formātā tvērumu**.</span><span class="sxs-lookup"><span data-stu-id="60dc1-115">To add a scope segment to the format of a number sequence, select the format in the list, and then select **Include scope in format**.</span></span> <span data-ttu-id="60dc1-116">Lai noņemtu sfēras segmentu no numuru sērijas formāta, sarakstā atlasiet vajadzīgo formātu un pēc tam atlasiet **Noņemt no formāta tvērumu**.</span><span class="sxs-lookup"><span data-stu-id="60dc1-116">To remove a scope segment from the format of a number sequence, select the format in the list, and then select **Remove scope from format**.</span></span> <span data-ttu-id="60dc1-117">Lai numuru sēriju izslēgtu no automātiskas ģenerēšanas, sarakstā atlasiet numuru sēriju un pēc tam atlasiet **Dzēst**.</span><span class="sxs-lookup"><span data-stu-id="60dc1-117">To exclude a number sequence from automatic generation, select the number sequence in the list, and then select **Delete**.</span></span>  

4. <span data-ttu-id="60dc1-118">Atlasiet **Nākamais**.</span><span class="sxs-lookup"><span data-stu-id="60dc1-118">Select **Next**.</span></span>
5. <span data-ttu-id="60dc1-119">Atl. **Pabeigt**.</span><span class="sxs-lookup"><span data-stu-id="60dc1-119">Select **Finish**.</span></span>

