---
title: Līdzekļa nomas maksājumu grafiku apstiprināšana partijā
description: Šajā tēmā paskaidrots, kā apstiprināt vairākus maksājumu grafikus partijā.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9a3bd7293fed4b8df5d7bd76edacbcae253aa1f5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5816080"
---
# <a name="confirm-asset-leasing-payment-schedules-in-a-batch"></a><span data-ttu-id="a7640-103">Līdzekļa nomas maksājumu grafiku apstiprināšana partijā</span><span class="sxs-lookup"><span data-stu-id="a7640-103">Confirm Asset leasing payment schedules in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a7640-104">Šajā tēmā paskaidrots, kā apstiprināt vairākus maksājumu grafikus partijā.</span><span class="sxs-lookup"><span data-stu-id="a7640-104">This topic explains how to confirm multiple payment schedules in a batch.</span></span> <span data-ttu-id="a7640-105">Maksājumu grafiki tiek apstiprināti vai katrai nomai, vai izmantojot partijas apstiprināšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="a7640-105">Payment schedules are confirmed either on a lease-to-lease basis or through the confirmation batch process.</span></span> <span data-ttu-id="a7640-106">Žurnāla ierakstu var grāmatot tikai nomai ar apstiprinātu maksājumu grafiku.</span><span class="sxs-lookup"><span data-stu-id="a7640-106">A journal entry can be posted only against a lease that has a confirmed payment schedule.</span></span> <span data-ttu-id="a7640-107">Maksājumu grafika apstiprināšana kalpo kā nomas finanšu informācijas galīgais apstiprinājums.</span><span class="sxs-lookup"><span data-stu-id="a7640-107">Confirmation of the payment schedule serves as a final approval of the financial information for the lease.</span></span> <span data-ttu-id="a7640-108">Visas turpmākās izmaiņas nomas finanšu informācijā, piemēram, maksājumos un nomas termiņā, veido nomas korekciju, un ir jāapstrādā tādā veidā.</span><span class="sxs-lookup"><span data-stu-id="a7640-108">All future changes to the financial information for the lease, such as payments and the lease term, constitute a lease adjustment and should be processed in that way.</span></span>

<span data-ttu-id="a7640-109">Lai apstiprinātu vairākus maksājumu grafikus, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="a7640-109">To confirm multiple payment schedules, follow these steps.</span></span>

1. <span data-ttu-id="a7640-110">Doties uz **Līdzekļa noma \> Periodiskums \> Apstiprināšana partijā**.</span><span class="sxs-lookup"><span data-stu-id="a7640-110">Go to **Asset leasing \> Periodic \> Confirmation batch**.</span></span>
2. <span data-ttu-id="a7640-111">Lapā **Apstiprināšana partijā** atlasiet **Apstiprināšana partijā**.</span><span class="sxs-lookup"><span data-stu-id="a7640-111">On the **Confirmation batch** page, select **Confirmation batch**.</span></span>
3. <span data-ttu-id="a7640-112">Parādītajā dialoglodziņā filtrējiet grāmatas, ko vēlaties apstiprināt.</span><span class="sxs-lookup"><span data-stu-id="a7640-112">In the dialog box that appears, filter for the books that you want to confirm.</span></span>

    - <span data-ttu-id="a7640-113">Lai apstiprinātu visas konkrētās nomas grupas grāmatas, atlasiet grupu laukā **Nomas grupa**.</span><span class="sxs-lookup"><span data-stu-id="a7640-113">To confirm all the books in a specific lease group, select the group in the **Lease group** field.</span></span>
    - <span data-ttu-id="a7640-114">Lai apstiprinātu noteiktas grāmatas, atlasiet grāmatas laukā **Grāmatas ID**.</span><span class="sxs-lookup"><span data-stu-id="a7640-114">To confirm specific books, select the books in the **Book ID** field.</span></span>
    - <span data-ttu-id="a7640-115">Lai apstiprinātu visas grāmatas, ieslēdziet parametru **Visām grāmatām**.</span><span class="sxs-lookup"><span data-stu-id="a7640-115">To confirm all books, turn on the **For all books** parameter.</span></span>

<span data-ttu-id="a7640-116">Informācija par nesen apstiprinātajām grāmatām tiek parādīta lapā **Apstiprinātās grāmatas**.</span><span class="sxs-lookup"><span data-stu-id="a7640-116">Information for the newly confirmed books is shown on the **Confirmed books** page.</span></span> <span data-ttu-id="a7640-117">Kad maksājumu grafiki ir apstiprināti, nomai var grāmatot sākotnējos atzīšanas žurnāla ierakstus.</span><span class="sxs-lookup"><span data-stu-id="a7640-117">After the payment schedules are confirmed, the initial recognition journal entries can be posted against the leases.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]