---
title: Iestatījumu stornēšana žurnālos un rindās
description: Šajā tēmā ir aplūkots, kāpēc stornēts ieraksts, kas ievadīts virsgrāmatas žurnālā, var nebūt iekļauts iegrāmatotajā transakcijā.
author: kweekley
ms.date: 04/29/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-5-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 74020f6fc9b0fa8e05a1e2a09fd13dcd60490dc0
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028574"
---
# <a name="reverse-settings-on-journals-and-lines"></a><span data-ttu-id="6933a-103">Iestatījumu stornēšana žurnālos un rindās</span><span class="sxs-lookup"><span data-stu-id="6933a-103">Reverse settings on journals and lines</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6933a-104">Šajā tēmā ir aplūkots, kāpēc stornēts ieraksts, kas ievadīts virsgrāmatas žurnālā, var nebūt iekļauts iegrāmatotajā transakcijā.</span><span class="sxs-lookup"><span data-stu-id="6933a-104">This topic addresses why a reversing entry that was entered on a general journal might not be included on the posted transaction.</span></span>  

## <a name="symptom"></a><span data-ttu-id="6933a-105">Simptoms</span><span class="sxs-lookup"><span data-stu-id="6933a-105">Symptom</span></span>

<span data-ttu-id="6933a-106">Virsgrāmatas žurnālā ir iekļauts stornēšanas ieraksts un stornēšanas datums žurnālā.</span><span class="sxs-lookup"><span data-stu-id="6933a-106">A general journal includes a reversing entry and reversing date on the journal.</span></span> <span data-ttu-id="6933a-107">Grāmatojot žurnālu, neviens dokuments netiek stornēts.</span><span class="sxs-lookup"><span data-stu-id="6933a-107">When you post the journal, none of the vouchers are reversed.</span></span> <span data-ttu-id="6933a-108">Kādēļ tā notiek?</span><span class="sxs-lookup"><span data-stu-id="6933a-108">Why does this happen?</span></span>

## <a name="resolution"></a><span data-ttu-id="6933a-109">Novēršana</span><span class="sxs-lookup"><span data-stu-id="6933a-109">Resolution</span></span>

<span data-ttu-id="6933a-110">Grāmatojot žurnālu, stornēšanas process ņem vērā tikai iestatījumus **Stornēšanas ieraksts** un **Stornēšanas datums** dokumenta sadaļā **Rindas**.</span><span class="sxs-lookup"><span data-stu-id="6933a-110">When the journal is posted, the reversing process looks only at the **Revering entry** and **Reversing date** settings on the **Lines** section of the voucher.</span></span> <span data-ttu-id="6933a-111">Šī pieeja ļauj žurnālam iekļaut dažus dokumentus, kas ir atzīmēti stornēšanai, un citus dokumentus, kas nav atzīmēti.</span><span class="sxs-lookup"><span data-stu-id="6933a-111">This approach allows a journal to include some vouchers that are marked for reversing, and others that are not.</span></span>

<span data-ttu-id="6933a-112">Žurnāla vērtības tiek izmantotas tikai kā noklusējuma vērtības, pievienojot *jaunas* rindas.</span><span class="sxs-lookup"><span data-stu-id="6933a-112">The values from the journal are only used as defaults when adding *new* lines.</span></span> <span data-ttu-id="6933a-113">Vērtību maiņa žurnālā neietekmē esošās rindas.</span><span class="sxs-lookup"><span data-stu-id="6933a-113">Changing the values on the journal doesn’t affect existing lines.</span></span> <span data-ttu-id="6933a-114">Šajā piemērā vispirms tika ievadītas dokumenta rindas.</span><span class="sxs-lookup"><span data-stu-id="6933a-114">In this example, the voucher lines were entered first.</span></span> <span data-ttu-id="6933a-115">Ievadot rindas informāciju pirms žurnāla noformēšanas par stornējamu žurnālu, apzīmējums kā stornēšanas ieraksts un datums netiks attiecināts uz esošajām rindām.</span><span class="sxs-lookup"><span data-stu-id="6933a-115">When you enter the line detail before designating the journal as reversing, the designation as a reversing entry and date won't be applied to any existing lines.</span></span>

<span data-ttu-id="6933a-116">Mainot stornēšanas ierakstu vai stornēšanas datumu esošā rindā, attiecīgās izmaiņas tiek izplatītas arī citās tā paša dokumenta rindās.</span><span class="sxs-lookup"><span data-stu-id="6933a-116">Changing the reversing entry or reversing date on an existing line propagates that change to other lines in the same voucher.</span></span> <span data-ttu-id="6933a-117">Lai optimizētu veiktspēju, pēc izmaiņu izplatīšanas citās rindās režģis netiek atsvaidzināts.</span><span class="sxs-lookup"><span data-stu-id="6933a-117">To optimize performance, the grid is not refreshed after propagating changes to other Lines.</span></span> <span data-ttu-id="6933a-118">Atjauninātās vērtības var parādīt, atsvaidzinot režģi.</span><span class="sxs-lookup"><span data-stu-id="6933a-118">You can display the updated values by refreshing the grid.</span></span>


