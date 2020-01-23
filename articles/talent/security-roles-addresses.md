---
title: Piekļ. priv. adresēm atbilstoši droš. lomai
description: Šajā tēmā paskaidrots, kā atrisināt problēmu, ja debitors nevar piekļūt privātām adresēm.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 58f3322ad64f7de07e17d193ff665bd6536a4070
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897101"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="cdca0-103">Piekļ. priv. adresēm atbilstoši droš. lomai</span><span class="sxs-lookup"><span data-stu-id="cdca0-103">Access to private addresses by security role</span></span>

<span data-ttu-id="cdca0-104">**Izsniegt**</span><span class="sxs-lookup"><span data-stu-id="cdca0-104">**Issue**</span></span>

<span data-ttu-id="cdca0-105">Pēc tam, kad debitors dublē drošības lomu un pierakstās ar šo jauno lomu, tas nevar skatīt adreses, kas tika atzīmētas kā privātas.</span><span class="sxs-lookup"><span data-stu-id="cdca0-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="cdca0-106">**Izšķirtspēja**</span><span class="sxs-lookup"><span data-stu-id="cdca0-106">**Resolution**</span></span>

<span data-ttu-id="cdca0-107">Lai atrisinātu probl., debitoram ir jāveic šādas darbības attiecībā uz dublēto droš. lomu.</span><span class="sxs-lookup"><span data-stu-id="cdca0-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="cdca0-108">Dod. uz **Organizācijas admin. \> Globālā adrešu grām. \> Globālās adrešu grām. parametri**.</span><span class="sxs-lookup"><span data-stu-id="cdca0-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="cdca0-109">Cilnē **Privāto vietu drošība** pārvietojiet jaunu drošības lomu no saraksta **Pieejamās lomas** uz sarakstu **Atlasītās lomas**.</span><span class="sxs-lookup"><span data-stu-id="cdca0-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="cdca0-110">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="cdca0-110">Select **Save**.</span></span>

![Lapa Glob. adrešu grām. parametri](media/GAD-parameters.png)
