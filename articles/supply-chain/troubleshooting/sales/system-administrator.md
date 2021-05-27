---
title: Sistēmas administratori nevar dzēst pasūtījumu aizturēšanu, jo tie nav autorizēti
description: Sistēmas administratori nevar dzēst pasūtījumu aizturēšanu, jo tie nav autorizēti.
author: SmithaNataraj
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: acabd6409d9b2860535335bc648bcc34304e0cb0
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026728"
---
# <a name="system-administrators-cant-clear-order-holds-because-they-arent-authorized"></a><span data-ttu-id="87752-103">Sistēmas administratori nevar dzēst pasūtījumu aizturēšanu, jo tie nav autorizēti</span><span class="sxs-lookup"><span data-stu-id="87752-103">System administrators can't clear order holds because they aren't authorized</span></span>

<span data-ttu-id="87752-104">KB numurs: 4614642</span><span class="sxs-lookup"><span data-stu-id="87752-104">KB number: 4614642</span></span>

## <a name="symptoms"></a><span data-ttu-id="87752-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="87752-105">Symptoms</span></span>

<span data-ttu-id="87752-106">Sistēmas administratori nevar dzēst pārdošanas pasūtījumu aizturēšanas gadījumus, ja tiem nav noteikta loma, kas piešķirta pasūtījuma aizturēšanas kodā.</span><span class="sxs-lookup"><span data-stu-id="87752-106">System administrators can't clear sales order holds unless they have the specific role that is assigned in the order hold code.</span></span>

## <a name="resolution"></a><span data-ttu-id="87752-107">Novēršana</span><span class="sxs-lookup"><span data-stu-id="87752-107">Resolution</span></span>

<span data-ttu-id="87752-108">Piekļuvi dažām operācijām, piemēram, pārdošanas pasūtījumu aizturēšanas dzēšanai, nosaka biznesa politikas iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="87752-108">Access to some operations, such as clearing sales order holds, is driven by the setup of a business policy.</span></span> <span data-ttu-id="87752-109">Sistēmas administratoriem parasti nav atļauts veikt šī tipa operācijas.</span><span class="sxs-lookup"><span data-stu-id="87752-109">System administrators aren't typically allowed to perform operations of this type.</span></span> 

<span data-ttu-id="87752-110">Piekļuve noteikta uzdevuma veikšanai bieži tiek pārvaldīta ar uzņēmējdarbības politiku, un tikai noteiktas personas organizācijā tiek akceptētas veikt šo uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="87752-110">More often, access to perform a specific task is governed by business policies, and only specific persons in an organization are approved to perform that task.</span></span> <span data-ttu-id="87752-111">Piemēri iekļauj apstiprinājumus, kas ir darbplūsmas apstiprinājumu rezultāts, un konkrētus uzdevumus, kas ir darbplūsmas konfigurācijas rezultāts.</span><span class="sxs-lookup"><span data-stu-id="87752-111">Examples include approvals that are the result of workflow approvals and specific tasks that are the result of a workflow configuration.</span></span>

<span data-ttu-id="87752-112">Lai gan neviena darbplūsma nav saistīta ar pasūtījumu aizturēšanu, princips ir līdzīgs.</span><span class="sxs-lookup"><span data-stu-id="87752-112">Although no workflow is associated with order holds, the principle is similar.</span></span> <span data-ttu-id="87752-113">Atbilstoša loma norāda noteiktu personu grupu organizācijā, kurai ir tiesības dzēst pasūtījumu aizturēšanu.</span><span class="sxs-lookup"><span data-stu-id="87752-113">A relevant role designates the specific group of people in an organization who have the right to clear order holds.</span></span> <span data-ttu-id="87752-114">Šīs tiesības nav jāpiešķir visiem administratoriem, jo šī pieeja pārkāpj noteikto uzņēmējdarbības politiku.</span><span class="sxs-lookup"><span data-stu-id="87752-114">This right should not necessarily be granted to all administrators, because that approach violates the defined business policy.</span></span>
