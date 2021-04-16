---
title: Sagādes un avotu parametri Kopīgajās izmaksās
description: Šajā tēmā ir aprakstīts, kā iestatīt atbilstošos Sagādes un plānošanas parametrus, kad izmantojat Kopīgo izmaksu moduli.
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: df91fcb97794be32924707fcecf2b5fb34844596
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833933"
---
# <a name="procurement-and-sourcing-parameters-for-landed-cost"></a><span data-ttu-id="dec2e-103">Sagādes un avotu parametri Kopīgajās izmaksās</span><span class="sxs-lookup"><span data-stu-id="dec2e-103">Procurement and sourcing parameters for Landed cost</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dec2e-104">**Sagādes un avotu parametru** lapai ir daži iestatījumi, kas ir īpaši svarīgi, kad izmantojat **Kopīgo izmaksu** moduli. </span><span class="sxs-lookup"><span data-stu-id="dec2e-104">The **Procurement and sourcing parameters** page has a few settings that are especially relevant when you use the **Landed cost** module.</span></span> <span data-ttu-id="dec2e-105">Izmantojiet dialoglodziņu **Atjaunināt pasūtījuma rindas**, kas ir atvērts no lapas **Sagādes un avotu parametri**, lai norādītu, vai pirkšanas pasūtījuma rindas automātiski jāatjaunina, kad pirkšanas pasūtījuma galvenē tiek veiktas izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="dec2e-105">Use the **Update order lines** dialog box that is opened from the **Procurement and sourcing parameters** page to specify whether purchase order lines should automatically be updated when changes are made on the purchase order header.</span></span>

<span data-ttu-id="dec2e-106">Lai pabeigtu šos iestatījumu, rīkojieties, kā norādīts tālāk.</span><span class="sxs-lookup"><span data-stu-id="dec2e-106">To complete this setup, follow these steps.</span></span>

1. <span data-ttu-id="dec2e-107">Dodieties uz **Sagāde un avoti \> Iestatīšana \> Sagādes un avotu parametri**.</span><span class="sxs-lookup"><span data-stu-id="dec2e-107">Go to **Procurement and sourcing \> Setup \> Procurement and sourcing parameters**.</span></span>
1. <span data-ttu-id="dec2e-108">Cilnē **Vispārīgi** atlasiet saiti **Atjaunināt pasūtījuma rindas**.</span><span class="sxs-lookup"><span data-stu-id="dec2e-108">On the **General** tab, select the **Update order lines** link.</span></span>
1. <span data-ttu-id="dec2e-109">Dialoglodziņā **Atjaunināt pasūtījuma rindas** ir uzskaitīti lauki pasūtījuma galvenē, kas var lietot arī automātiskos atjauninājumus saistītajos laukos pasūtījuma rindās.</span><span class="sxs-lookup"><span data-stu-id="dec2e-109">The **Update order lines** dialog box lists the fields on the order header that can also apply automatic updates to related fields on the order lines.</span></span> <span data-ttu-id="dec2e-110">Katram saraksta laukam iestatiet vienu no šīm vērtībām:</span><span class="sxs-lookup"><span data-stu-id="dec2e-110">Set each field in the list to one of the following values:</span></span>

    - <span data-ttu-id="dec2e-111">**Vienmēr** – Pasūtījuma rindām vajadzētu automātiski atjaunināties, atjauninot pasūtījuma galveni.</span><span class="sxs-lookup"><span data-stu-id="dec2e-111">**Always** – The order lines should automatically be updated when the order header is updated.</span></span>
    - <span data-ttu-id="dec2e-112">**Nekad** – Pasūtījuma rindām nekad nevajadzētu automātiski atjaunināties, atjauninot pasūtījuma galveni.</span><span class="sxs-lookup"><span data-stu-id="dec2e-112">**Never** – The order lines should never be updated when the order header is updated.</span></span>
    - <span data-ttu-id="dec2e-113">**Uzvedne** – lietotājam tiks piedāvāts atlasīt, vai pasūtījuma rindas ir jāatjaunina.</span><span class="sxs-lookup"><span data-stu-id="dec2e-113">**Prompt** – The user will be prompted to select whether the order lines should be updated.</span></span>
