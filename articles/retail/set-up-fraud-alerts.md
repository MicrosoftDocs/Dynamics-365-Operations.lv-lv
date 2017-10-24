---
title: "Pārkāpumu brīdinājumu iestatīšana"
description: "Šajā tēmā izskaidrots, kā iestatīt kārtulas, lai brīdinātu klientu apkalpošanas pārstāvjus par potenciāli krāpniecisku informāciju, kad tiek apstrādāti pasūtījumi. Var definēt īpašus izmantošanai paredzētus kodus, lai automātiski vai manuāli aizturētu aizdomīgus pasūtījumus."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 09d80015298c3d0219b6ffb290dc456990536a62
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-fraud-alerts"></a><span data-ttu-id="ce71b-104">Pārkāpumu brīdinājumu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="ce71b-104">Set up fraud alerts</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="ce71b-105">Šajā tēmā izskaidrots, kā iestatīt kārtulas, lai brīdinātu klientu apkalpošanas pārstāvjus par potenciāli krāpniecisku informāciju, kad tiek apstrādāti pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="ce71b-105">This topic explains how to set up rules to alert customer service representatives of potentially fraudulent information when orders are processed.</span></span> <span data-ttu-id="ce71b-106">Var definēt īpašus izmantošanai paredzētus kodus, lai automātiski vai manuāli aizturētu aizdomīgus pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="ce71b-106">You can define specific codes to use to automatically or manually put suspicious orders on hold.</span></span> 

<span data-ttu-id="ce71b-107">Pirms iestatāt un izmantojat pārkāpumu pārbaudes kārtulas, ir jāiespējo pārkāpumu pārbaude un jādefinē pamata pārkāpumu pārbaudes vērtības zvanu centra parametros.</span><span class="sxs-lookup"><span data-stu-id="ce71b-107">Before you set up and use fraud checking rules, you must enable fraud checking and define the basic fraud checking values in the call center parameters.</span></span> <span data-ttu-id="ce71b-108">Ir divi pārkāpumu kārtulu tipi:</span><span class="sxs-lookup"><span data-stu-id="ce71b-108">There are two types of fraud rules:</span></span>

-   <span data-ttu-id="ce71b-109">**Statiskās kārtulas** izmanto noteiktu vērtību, piemēram, tālruņa numuru, kas ir melnajā sarakstā.</span><span class="sxs-lookup"><span data-stu-id="ce71b-109">**Static rules** use a specific value, such as a phone number that has been blacklisted.</span></span>
-   <span data-ttu-id="ce71b-110">**Dinamiskās kārtulas** var veidot no mainīgajiem un nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="ce71b-110">**Dynamic rules** can be composed from variables and conditions.</span></span>

<span data-ttu-id="ce71b-111">Pirms dinamiskās kārtulas izveidošanas ir jāizveido mainīgie un nosacījumi, kas definē, uz kurām personām kārtula attiecas un kad kārtula ir jāpiemēro.</span><span class="sxs-lookup"><span data-stu-id="ce71b-111">Before you create a dynamic rule, you must create the variables and conditions that define who the rule applies to and when the rule should be applied.</span></span> <span data-ttu-id="ce71b-112">Piemēram, jūs vēlaties izveidot kārtulu, lai pieprasītu to, ka, debitoram Nr. 1202 izdarot pārdošanas pasūtījumu vismaz 1000,00 vērtībā, pārdošanas pasūtījums ir jāaiztur, līdz iespējams pārbaudīt debitora maksājumu.</span><span class="sxs-lookup"><span data-stu-id="ce71b-112">For example, you want to create a rule to require that any sales order that customer 1202 places that is worth 1,000.00 or more be put on hold until the customer payment can be verified.</span></span> <span data-ttu-id="ce71b-113">Šajā gadījumā mainīgie ir: debitors Nr. 1202 un pasūtījuma kopējā summa 1000,00.</span><span class="sxs-lookup"><span data-stu-id="ce71b-113">In this case, the variables are customer 1202 and an order total of 1,000.00.</span></span> <span data-ttu-id="ce71b-114">Nosacījums norāda, ka ja debitors Nr. 1202 veic pasūtījumu un kopējā pasūtījuma summa ir 1,000.00 vai lielāka, pārdošanas pasūtījums ir jāaiztur līdz debitora maksājumu būs iespējams pārbaudīt.</span><span class="sxs-lookup"><span data-stu-id="ce71b-114">The condition specifies that if customer 1202 places an order, and the total amount of the order is equal to or more than 1,000.00, the sales order must be put on hold until the customer payment can be verified.</span></span>




