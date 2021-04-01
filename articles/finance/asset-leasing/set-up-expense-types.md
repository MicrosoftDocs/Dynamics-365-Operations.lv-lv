---
title: Izdevumu veidu iestatīšana
description: Šajā tēmā ir paskaidrots, kā līdzekļu pārvaldībā iestatīt izdevumu veidus.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1538826f140393eec59be9ff4df5242d5ced9d8f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249753"
---
# <a name="set-up-expense-types"></a><span data-ttu-id="374d0-103">Izdevumu veidu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="374d0-103">Set up expense types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="374d0-104">Šajā tēmā ir paskaidrots, kā līdzekļu pārvaldībā iestatīt izdevumu veidus.</span><span class="sxs-lookup"><span data-stu-id="374d0-104">This topic explains how to set up expense types in Asset leasing.</span></span> <span data-ttu-id="374d0-105">Izmaksas, kas nav atainotas maksājumu grafikā, ir zināmas kā *Izdevumu izmaksas*.</span><span class="sxs-lookup"><span data-stu-id="374d0-105">Costs that aren't represented by the payment schedule are known as *expense costs*.</span></span> <span data-ttu-id="374d0-106">Šo izmaksu piemēri ietver īpašuma nodokļus, kopējās platības uzturēšanas izmaksas un apdrošināšanas izdevumus.</span><span class="sxs-lookup"><span data-stu-id="374d0-106">Examples of these costs include property taxes, common area maintenance costs, and insurance expenses.</span></span>

## <a name="add-an-administrative-expense-type"></a><span data-ttu-id="374d0-107">Administratīvo izmaksu tipa pievienošana</span><span class="sxs-lookup"><span data-stu-id="374d0-107">Add an administrative expense type</span></span>

1. <span data-ttu-id="374d0-108">Dodieties uz **Līdzekļu noma \> Iestatījumi \> Izdevumu tipi**.</span><span class="sxs-lookup"><span data-stu-id="374d0-108">Go to **Asset leasing \> Setup \> Expense types**.</span></span>
2. <span data-ttu-id="374d0-109">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="374d0-109">Select **New**.</span></span>
3. <span data-ttu-id="374d0-110">Atbilstošajos laukos ievadiet jauno izdevumu tipu un aprakstu.</span><span class="sxs-lookup"><span data-stu-id="374d0-110">In the appropriate fields, enter the new expense type and a description.</span></span>

## <a name="assign-accounts-to-administrative-costs"></a><span data-ttu-id="374d0-111">Piešķirt kontus administratīvajām izmaksām</span><span class="sxs-lookup"><span data-stu-id="374d0-111">Assign accounts to administrative costs</span></span>

<span data-ttu-id="374d0-112">Pēc tam saistiet kontus ar izdevumu tipiem.</span><span class="sxs-lookup"><span data-stu-id="374d0-112">Next, you should associate accounts with the expense types.</span></span> <span data-ttu-id="374d0-113">Šie konti tiks debetēti, kad tiks grāmatoti izdevumu grafika ieraksti.</span><span class="sxs-lookup"><span data-stu-id="374d0-113">These accounts will be debited when expense schedule entries are posted.</span></span> <span data-ttu-id="374d0-114">Korespondējošais konts ir norādīts **izpildes izmaksu maksājuma grafika** rindās katrai nomai.</span><span class="sxs-lookup"><span data-stu-id="374d0-114">The offset account is specified on the **Executory costs payment schedule** lines on each lease.</span></span>

1. <span data-ttu-id="374d0-115">Dodieties uz **Līdzekļu noma \> Iestatījumi \> Līdzekļu nomas parametri**.</span><span class="sxs-lookup"><span data-stu-id="374d0-115">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="374d0-116">Cilnes **Konti**, kas atrodas kopsavilkuma cilnē **Izpildes izmaksas**, laukā **Izdevumu tips** atlasiet izdevumu tipu.</span><span class="sxs-lookup"><span data-stu-id="374d0-116">On the **Accounts** tab, on the **Executory costs** FastTab, in the **Expense type** field, select the expense type.</span></span>
3. <span data-ttu-id="374d0-117">Atlasiet **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="374d0-117">Select **Add**.</span></span>
4. <span data-ttu-id="374d0-118">Laukā **Grāmatas tips** atlasiet grāmatas tipu, ko saistīt ar administratīvajām izmaksām.</span><span class="sxs-lookup"><span data-stu-id="374d0-118">In the **Book type** field, select the book type to link to the administrative costs.</span></span>

    > [!NOTE]
    > <span data-ttu-id="374d0-119">Vairākus grāmatu tipus var saistīt ar vienu izdevumu kontu.</span><span class="sxs-lookup"><span data-stu-id="374d0-119">Multiple book types can be linked to the same expense account.</span></span>

5. <span data-ttu-id="374d0-120">Laukā **Konta kods** norādiet, kurām nomām jālieto grāmata.</span><span class="sxs-lookup"><span data-stu-id="374d0-120">In the **Account code** field, specify which leases the book should be applied to:</span></span>

    - <span data-ttu-id="374d0-121">**Visi** — lietot grāmatu visām nomām.</span><span class="sxs-lookup"><span data-stu-id="374d0-121">**All** – Apply the book to all leases.</span></span>
    - <span data-ttu-id="374d0-122">**Grupa** — lietot grāmatu konkrētai nomu grupai.</span><span class="sxs-lookup"><span data-stu-id="374d0-122">**Group** – Apply the book to a specific group of leases.</span></span>
    - <span data-ttu-id="374d0-123">**Tabula** — lietot grāmatu noteiktām nomām.</span><span class="sxs-lookup"><span data-stu-id="374d0-123">**Table** – Apply the book to specific leases.</span></span>

6. <span data-ttu-id="374d0-124">Ja laukā **Konta kods** atlasījāt **Tabula** vai **Grupa**, laukā **Konta/grupas numurs** atlasiet konta numuru vai grupas numuru.</span><span class="sxs-lookup"><span data-stu-id="374d0-124">If you selected **Group** or **Table** in the **Account code** field, select an account number or group number in the **Account/Group number** field.</span></span>
7. <span data-ttu-id="374d0-125">Atbilstošajos laukos atlasiet finanšu nomas galveno kontu un operatīvas nomas galveno kontu.</span><span class="sxs-lookup"><span data-stu-id="374d0-125">In the appropriate fields, select the finance lease main account and the operating lease main account.</span></span>

<span data-ttu-id="374d0-126">Kad šīs darbības ir pabeigtas, varat pievienot izdevumus, izmantojot **izpildes izmaksu maksājuma grafika** rindas atlasītās nomas lapā **Līguma informācija**.</span><span class="sxs-lookup"><span data-stu-id="374d0-126">When you've completed these steps, you can add expenses through the **Executory costs payment schedule** lines on the **Lease details** page of a selected lease.</span></span> <span data-ttu-id="374d0-127">Varat arī pievienot izdevumus, izveidojot jaunu nomu.</span><span class="sxs-lookup"><span data-stu-id="374d0-127">Alternatively, you can add expenses when you create a new lease.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]