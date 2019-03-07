---
title: Numuru sēriju iestatīšana, izmantojot vedni
description: Numuru sērijas tiek izmantotas, lai ģenerētu lasāmus, unikālus pamatdatu ierakstu identifikatorus un darījumu ierakstus, kam tie ir nepieciešami.
author: sericks007
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceWizard
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1808ab9240ab291f9d203893a634bd390f16e2e7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "328244"
---
# <a name="set-up-number-sequences-by-using-a-wizard"></a><span data-ttu-id="0072b-103">Numuru sēriju iestatīšana, izmantojot vedni</span><span class="sxs-lookup"><span data-stu-id="0072b-103">Set up number sequences by using a wizard</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0072b-104">Numuru sērijas tiek izmantotas, lai ģenerētu lasāmus, unikālus pamatdatu ierakstu identifikatorus un darījumu ierakstus, kam tie ir nepieciešami.</span><span class="sxs-lookup"><span data-stu-id="0072b-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require them.</span></span> <span data-ttu-id="0072b-105">Pamatdati vai darījumu ieraksts, kam nepieciešams identifikators, tiek saukts par atsauci.</span><span class="sxs-lookup"><span data-stu-id="0072b-105">A master data or transaction record that requires an identifier is referred to as a reference.</span></span> <span data-ttu-id="0072b-106">Pirms atsaucei varat izveidot jaunus ierakstus, ir jāiestata numuru sērija un tā jāsaista ar atsauci.</span><span class="sxs-lookup"><span data-stu-id="0072b-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="0072b-107">Šajā procedūrā tiek skaidrots, kā iestatīt visas nepieciešamās numuru sērijas vienlaikus, izmantojot vedni.</span><span class="sxs-lookup"><span data-stu-id="0072b-107">This procedure explains how to set up all required number sequences at the same time by using a wizard.</span></span> <span data-ttu-id="0072b-108">Demonstrācijas datu uzņēmums, kas tiek izmantots, lai izveidotu šo procedūru, ir USMF.</span><span class="sxs-lookup"><span data-stu-id="0072b-108">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="0072b-109">Pārejiet uz sadaļu Organizācijas administrēšana > Numuru secība > Numuru secība.</span><span class="sxs-lookup"><span data-stu-id="0072b-109">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="0072b-110">Noklikšķiniet uz Ģenerēt.</span><span class="sxs-lookup"><span data-stu-id="0072b-110">Click Generate.</span></span>
3. <span data-ttu-id="0072b-111">Noklikšķiniet uz Tālāk.</span><span class="sxs-lookup"><span data-stu-id="0072b-111">Click Next.</span></span>
    * <span data-ttu-id="0072b-112">Šajā lapā varat mainīt identifikācijas kodu, mazāko vērtību un lielāko vērtību.</span><span class="sxs-lookup"><span data-stu-id="0072b-112">On this page, you can modify the identification code, the lowest value, and the highest value.</span></span> <span data-ttu-id="0072b-113">Turklāt varat norādīt, vai numuru secībai jābūt nepārtrauktai.</span><span class="sxs-lookup"><span data-stu-id="0072b-113">In addition, you can indicate whether the number sequence must be continuous.</span></span>   
    * <span data-ttu-id="0072b-114">Neatlasiet opciju Nepārtraukts, ja numuri šai numuru sērijai ir jārezervē.</span><span class="sxs-lookup"><span data-stu-id="0072b-114">Do not select the Continuous option if you must preallocate numbers for the number sequence.</span></span>     <span data-ttu-id="0072b-115">Lai pievienotu sfēras segmentu numuru sērijas formātam, sarakstā atlasiet vajadzīgo formātu un pēc tam noklikšķiniet uz Iekļaut formātā tvērumu.</span><span class="sxs-lookup"><span data-stu-id="0072b-115">To add a scope segment to the format of a number sequence, select the format in the list, and then click Include scope in format.</span></span>     <span data-ttu-id="0072b-116">Lai noņemtu sfēras segmentu no numuru sērijas formāta, sarakstā atlasiet vajadzīgo formātu un pēc tam noklikšķiniet uz Noņemt no formāta tvērumu.</span><span class="sxs-lookup"><span data-stu-id="0072b-116">To remove a scope segment from the format of a number sequence, select the format in the list, and then click Remove scope from format.</span></span>     <span data-ttu-id="0072b-117">Lai numuru sēriju izslēgtu no automātiskas ģenerēšanas, sarakstā atlasiet numuru sēriju un pēc tam noklikšķiniet uz Dzēst.</span><span class="sxs-lookup"><span data-stu-id="0072b-117">To exclude a number sequence from automatic generation, select the number sequence in the list, and then click Delete.</span></span>  
4. <span data-ttu-id="0072b-118">Noklikšķiniet uz Tālāk.</span><span class="sxs-lookup"><span data-stu-id="0072b-118">Click Next.</span></span>
5. <span data-ttu-id="0072b-119">Noklikšķiniet uz Pabeigt.</span><span class="sxs-lookup"><span data-stu-id="0072b-119">Click Finish.</span></span>

