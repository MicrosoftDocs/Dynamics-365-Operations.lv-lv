---
title: "Piekļ. priv. adresēm atbilstoši droš. lomai"
description: "Šajā tēmā paskaidrots, kā atrisināt problēmu, ja debitors nevar piekļūt privātām adresēm."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: c1c1c3ce1233408e73d177f9e04f1137f3171a49
ms.contentlocale: lv-lv
ms.lasthandoff: 12/04/2018

---

# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="be9fd-103">Piekļ. priv. adresēm atbilstoši droš. lomai</span><span class="sxs-lookup"><span data-stu-id="be9fd-103">Access to private addresses by security role</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="be9fd-104">**Izsniegt**</span><span class="sxs-lookup"><span data-stu-id="be9fd-104">**Issue**</span></span>

<span data-ttu-id="be9fd-105">Pēc tam, kad debitors dublē drošības lomu un pierakstās ar šo jauno lomu, tas nevar skatīt adreses, kas tika atzīmētas kā privātas.</span><span class="sxs-lookup"><span data-stu-id="be9fd-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="be9fd-106">**Izšķirtspēja**</span><span class="sxs-lookup"><span data-stu-id="be9fd-106">**Resolution**</span></span>

<span data-ttu-id="be9fd-107">Lai atrisinātu probl., debitoram ir jāveic šādas darbības attiecībā uz dublēto droš. lomu.</span><span class="sxs-lookup"><span data-stu-id="be9fd-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="be9fd-108">Dod. uz **Organizācijas admin. \> Globālā adrešu grām. \> Globālās adrešu grām. parametri**.</span><span class="sxs-lookup"><span data-stu-id="be9fd-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="be9fd-109">Cilnē **Privāto vietu drošība** pārvietojiet jaunu drošības lomu no saraksta **Pieejamās lomas** uz sarakstu **Atlasītās lomas**.</span><span class="sxs-lookup"><span data-stu-id="be9fd-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="be9fd-110">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="be9fd-110">Select **Save**.</span></span>

![Lapa Glob. adrešu grām. parametri](media/GAD-parameters.png)

