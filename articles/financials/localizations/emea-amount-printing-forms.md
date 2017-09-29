---
title: "Atjaunināt veidu, kā summas tiek rādītas pārskatos un dokumentos"
description: "Šajā tēmā ir sniegta informācija par to, kā atjaunināt veidu, kādā pārskatos un citos dokumentos summas tiek rādītas Igaunijai, Latvijai, Lietuvai, Polijai, Čehijai, Ungārijai un Krievijai."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 264254
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 226eecd49fb5c4daeb701fbb019f402519999610
ms.contentlocale: lv-lv
ms.lasthandoff: 06/29/2017


---

# <a name="update-how-amounts-are-displayed-on-reports-and-documents"></a><span data-ttu-id="7fa92-103">Atjaunināt veidu, kā summas tiek rādītas pārskatos un dokumentos</span><span class="sxs-lookup"><span data-stu-id="7fa92-103">Update how amounts are displayed on reports and documents</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="7fa92-104">Šajā tēmā ir sniegta informācija par to, kā atjaunināt veidu, kādā pārskatos un citos dokumentos summas tiek rādītas Igaunijai, Latvijai, Lietuvai, Polijai, Čehijai, Ungārijai un Krievijai.</span><span class="sxs-lookup"><span data-stu-id="7fa92-104">This topic provides information about how to update how amounts are displayed on reports and other documents for Estonia, Latvia, Lithuania, Poland, Czech Republic, Hungary, and Russia.</span></span>

<span data-ttu-id="7fa92-105">Juridiskajām personām Igaunijā, Latvijā, Lietuvā, Polijā, Čehijā, Ungārijā un Krievijā valūtas vienībām un apakšvienībām varat iestatīt pilnos nosaukumus un īsos nosaukumus.</span><span class="sxs-lookup"><span data-stu-id="7fa92-105">For legal entities in Estonia, Latvia, Lithuania, Poland, Czech Republic, Hungary, and Russia, you can set up full names and short names for currency units and subunits.</span></span> <span data-ttu-id="7fa92-106">Šos nosaukumus var izmantot, lai pārveidotu summu rādīšanu dokumentos un pārskatos.</span><span class="sxs-lookup"><span data-stu-id="7fa92-106">These names can be used to transform how amounts are represented on documents and reports.</span></span> <span data-ttu-id="7fa92-107">Piemēram: summu **LTL 100,20** var rādīt kā **100 liti 20 centi**.</span><span class="sxs-lookup"><span data-stu-id="7fa92-107">For example: The amount **LTL 100.20** can be displayed as **100 Litas 20 Centas**.</span></span>

## <a name="set-up-full-and-short-names-for-currency-units-and-subunits"></a><span data-ttu-id="7fa92-108">Iestatīt pilnos un īsos nosaukumus valūtas vienībām un apakšvienībām</span><span class="sxs-lookup"><span data-stu-id="7fa92-108">Set up full and short names for currency units and subunits</span></span>
<span data-ttu-id="7fa92-109">Lai kādai valodai iestatītu valūtas vienību un apakšvienību pilnos un īsos nosaukumus, izpildiet tālāk sniegtos norādījumus.</span><span class="sxs-lookup"><span data-stu-id="7fa92-109">To set up full and short names for currency units and subunits for a language, complete the following steps:</span></span>

1.  <span data-ttu-id="7fa92-110">Atveriet lapu **Valūtas**.</span><span class="sxs-lookup"><span data-stu-id="7fa92-110">Open the **Currencies** page.</span></span>
2.  <span data-ttu-id="7fa92-111">Izvēlieties valūtu.</span><span class="sxs-lookup"><span data-stu-id="7fa92-111">Select a currency.</span></span>
3.  <span data-ttu-id="7fa92-112">Darbību rūtī noklikšķiniet uz **Locījumi**.</span><span class="sxs-lookup"><span data-stu-id="7fa92-112">On the Action Pane, click **Declension**.</span></span>
4.  <span data-ttu-id="7fa92-113">Lai kādai valodai pievienotu pilno nosaukumu un īso nosaukumu, noklikšķiniet uz **Jauns** un aizpildiet tālāk uzskaitītos laukus.</span><span class="sxs-lookup"><span data-stu-id="7fa92-113">To add full name and short name for a language, click **New** and complete the following fields.</span></span>
    |                                                           |                                                                                                                                                                                                                    |
    |-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="7fa92-114">**Lauks**</span><span class="sxs-lookup"><span data-stu-id="7fa92-114">**Field**</span></span>                                                 | <span data-ttu-id="7fa92-115">**Apraksts**</span><span class="sxs-lookup"><span data-stu-id="7fa92-115">**Description**</span></span>                                                                                                                                                                                                    |
    | <span data-ttu-id="7fa92-116">**Valoda**</span><span class="sxs-lookup"><span data-stu-id="7fa92-116">**Language**</span></span>                                              | <span data-ttu-id="7fa92-117">Atlasiet pašreizējā teksta valodu.</span><span class="sxs-lookup"><span data-stu-id="7fa92-117">Select the language for the current text.</span></span>                                                                                                                                                                          |
    | <span data-ttu-id="7fa92-118">**Vienskaitļa nominatīvs (vienības nosaukumu lauku grupa)**</span><span class="sxs-lookup"><span data-stu-id="7fa92-118">**Singular nominative (Name of units field group)**</span></span>       | <span data-ttu-id="7fa92-119">Ievadiet valūtas nosaukumu vienskaitļa formā.</span><span class="sxs-lookup"><span data-stu-id="7fa92-119">Enter the singular form of the currency.</span></span> <span data-ttu-id="7fa92-120">Piemēram, vienskaitļa forma no litiem ir “lits”.</span><span class="sxs-lookup"><span data-stu-id="7fa92-120">For example, the singular form of Litas is Litas.</span></span>                                                                                                                         |
    | <span data-ttu-id="7fa92-121">**Daudzskaitļa nominatīvs (vienības nosaukumu lauku grupa)**</span><span class="sxs-lookup"><span data-stu-id="7fa92-121">**Plural nominative (Name of units field group)**</span></span>         | <span data-ttu-id="7fa92-122">Ievadiet valūtas nosaukumu daudzskaitļa formā.</span><span class="sxs-lookup"><span data-stu-id="7fa92-122">Enter the plural form of the currency.</span></span> <span data-ttu-id="7fa92-123">Ievadiet, piemēram, “liti”.</span><span class="sxs-lookup"><span data-stu-id="7fa92-123">For example, enter Litai.</span></span> <span data-ttu-id="7fa92-124">**Piezīme**. Lauki **Vienskaitļa ģenitīvs** un **Daudzskaitļa ģenitīvs** ir pieejami atkarībā no valodas, kas atlasīta laukā **Valoda**.</span><span class="sxs-lookup"><span data-stu-id="7fa92-124">**Note**: The **Singular genitive** and **Plural genitive** fields are available based on the language that you select in the **Language** field.</span></span> |
    | <span data-ttu-id="7fa92-125">**Vienskaitļa nominatīva lauks (daļu nosaukumu lauku grupa)**</span><span class="sxs-lookup"><span data-stu-id="7fa92-125">**Singular nominative field (Name of parts field group)**</span></span> | <span data-ttu-id="7fa92-126">Ievadiet valūtas apakšvienības nosaukumu vienskaitļa formā.</span><span class="sxs-lookup"><span data-stu-id="7fa92-126">Enter the singular form of the subunit of the currency.</span></span>                                                                                                                                                            |
    | <span data-ttu-id="7fa92-127">**Daudzskaitļa nominatīvs (daļu nosaukumu lauku grupa)**</span><span class="sxs-lookup"><span data-stu-id="7fa92-127">**Plural nominative (Name of parts field group)**</span></span>         | <span data-ttu-id="7fa92-128">Ievadiet valūtas apakšvienības nosaukumu daudzskaitļa formā.</span><span class="sxs-lookup"><span data-stu-id="7fa92-128">Enter the plural form of the subunit of the currency.</span></span>                                                                                                                                                              |
    | <span data-ttu-id="7fa92-129">**Vienību saīsinātais nosaukums (īso nosaukumu lauku grupa)**</span><span class="sxs-lookup"><span data-stu-id="7fa92-129">**Shortcut name of units (Short name field group)**</span></span>       | <span data-ttu-id="7fa92-130">Ievadiet ISO kodu, lai identificētu attiecīgo valūtu.</span><span class="sxs-lookup"><span data-stu-id="7fa92-130">Enter the ISO code to identify the currency.</span></span> <span data-ttu-id="7fa92-131">Piemēram, ievadiet LTL, lai identificētu litus.</span><span class="sxs-lookup"><span data-stu-id="7fa92-131">For example, enter LTL to identify Litas.</span></span>                                                                                                                             |
    | <span data-ttu-id="7fa92-132">**Daļu saīsinātais nosaukums (īso nosaukumu lauku grupa)**</span><span class="sxs-lookup"><span data-stu-id="7fa92-132">**Shortcut name for parts (Short name field group)**</span></span>      | <span data-ttu-id="7fa92-133">Ievadiet valūtas apakšvienības apzīmējumu.</span><span class="sxs-lookup"><span data-stu-id="7fa92-133">Enter the denomination of the currency subunit.</span></span> <span data-ttu-id="7fa92-134">Ievadiet, piemēram, “centi”.</span><span class="sxs-lookup"><span data-stu-id="7fa92-134">For example, enter Centas.</span></span>                                                                                                                                         |
    | <span data-ttu-id="7fa92-135">**Saiklis “un” starp vienībām un daļām**</span><span class="sxs-lookup"><span data-stu-id="7fa92-135">**Conjunction 'and' between units and parts**</span></span>             | <span data-ttu-id="7fa92-136">Atzīmējiet šo opciju, lai starp valūtas vienībām un vienības daļām drukātu saikli “un”.</span><span class="sxs-lookup"><span data-stu-id="7fa92-136">Select to print the conjunction “and” between the currency units and unit parts.</span></span> <span data-ttu-id="7fa92-137">Piemēram, rēķinos vai pārskatos summa LTL 100,20 tiks rādīta kā “100 liti un 20 centi”.</span><span class="sxs-lookup"><span data-stu-id="7fa92-137">For example, on invoices or reports, the amount for LTL 100.20 will be displayed as 100 Litas and 20 Centas.</span></span>                      |

5.  <span data-ttu-id="7fa92-138">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="7fa92-138">Click **Save**.</span></span>





