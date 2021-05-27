---
title: Sagādes un avotu parametri Kopīgajās izmaksās
description: Šajā tēmā ir aprakstīts, kā iestatīt atbilstošos Sagādes un plānošanas parametrus, kad izmantojat Kopīgo izmaksu moduli.
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: ccda3bd769a646e2390711883b8e40bec50e4d6a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020987"
---
# <a name="procurement-and-sourcing-parameters-for-landed-cost"></a><span data-ttu-id="648d2-103">Sagādes un avotu parametri Kopīgajās izmaksās</span><span class="sxs-lookup"><span data-stu-id="648d2-103">Procurement and sourcing parameters for Landed cost</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="648d2-104">**Sagādes un avotu parametru** lapai ir daži iestatījumi, kas ir īpaši svarīgi, kad izmantojat **Kopīgo izmaksu** moduli. </span><span class="sxs-lookup"><span data-stu-id="648d2-104">The **Procurement and sourcing parameters** page has a few settings that are especially relevant when you use the **Landed cost** module.</span></span> <span data-ttu-id="648d2-105">Izmantojiet dialoglodziņu **Atjaunināt pasūtījuma rindas**, kas ir atvērts no lapas **Sagādes un avotu parametri**, lai norādītu, vai pirkšanas pasūtījuma rindas automātiski jāatjaunina, kad pirkšanas pasūtījuma galvenē tiek veiktas izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="648d2-105">Use the **Update order lines** dialog box that is opened from the **Procurement and sourcing parameters** page to specify whether purchase order lines should automatically be updated when changes are made on the purchase order header.</span></span>

<span data-ttu-id="648d2-106">Lai pabeigtu šos iestatījumu, rīkojieties, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="648d2-106">To complete this setup, follow these steps.</span></span>

1. <span data-ttu-id="648d2-107">Dodieties uz **Sagāde un avoti \> Iestatīšana \> Sagādes un avotu parametri**.</span><span class="sxs-lookup"><span data-stu-id="648d2-107">Go to **Procurement and sourcing \> Setup \> Procurement and sourcing parameters**.</span></span>
1. <span data-ttu-id="648d2-108">Cilnē **Vispārīgi** atlasiet saiti **Atjaunināt pasūtījuma rindas**.</span><span class="sxs-lookup"><span data-stu-id="648d2-108">On the **General** tab, select the **Update order lines** link.</span></span>
1. <span data-ttu-id="648d2-109">Dialoglodziņā **Atjaunināt pasūtījuma rindas** ir uzskaitīti lauki pasūtījuma galvenē, kas var lietot arī automātiskos atjauninājumus saistītajos laukos pasūtījuma rindās.</span><span class="sxs-lookup"><span data-stu-id="648d2-109">The **Update order lines** dialog box lists the fields on the order header that can also apply automatic updates to related fields on the order lines.</span></span> <span data-ttu-id="648d2-110">Katram saraksta laukam iestatiet vienu no šīm vērtībām:</span><span class="sxs-lookup"><span data-stu-id="648d2-110">Set each field in the list to one of the following values:</span></span>

    - <span data-ttu-id="648d2-111">**Vienmēr** – Pasūtījuma rindām vajadzētu automātiski atjaunināties, atjauninot pasūtījuma galveni.</span><span class="sxs-lookup"><span data-stu-id="648d2-111">**Always** – The order lines should automatically be updated when the order header is updated.</span></span>
    - <span data-ttu-id="648d2-112">**Nekad** – Pasūtījuma rindām nekad nevajadzētu automātiski atjaunināties, atjauninot pasūtījuma galveni.</span><span class="sxs-lookup"><span data-stu-id="648d2-112">**Never** – The order lines should never be updated when the order header is updated.</span></span>
    - <span data-ttu-id="648d2-113">**Uzvedne** – lietotājam tiks piedāvāts atlasīt, vai pasūtījuma rindas ir jāatjaunina.</span><span class="sxs-lookup"><span data-stu-id="648d2-113">**Prompt** – The user will be prompted to select whether the order lines should be updated.</span></span>
