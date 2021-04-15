---
title: Ierakstu veidņu pārskats
description: Šajā rakstā tiek iepazīstināts ar ierakstu veidņu koncepciju un paskaidrots, kā tās var izmantot, lai veidotu ierakstus, kuri koplieto informāciju.
author: pvillads
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 16101
ms.assetid: 61ada2d8-84c3-44bc-b4c5-516b1aeac3d1
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d802d8bb86313dba512f52ec977b4dd18aa25c61
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747541"
---
# <a name="record-templates-overview"></a><span data-ttu-id="89d39-103">Ierakstu veidņu pārskats</span><span class="sxs-lookup"><span data-stu-id="89d39-103">Record templates overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="89d39-104">Šajā rakstā tiek iepazīstināts ar ierakstu veidņu koncepciju un paskaidrots, kā tās var izmantot, lai veidotu ierakstus, kuri koplieto informāciju.</span><span class="sxs-lookup"><span data-stu-id="89d39-104">This article introduces the concept of record templates and explains how they can be used to create records that share information.</span></span>

<span data-ttu-id="89d39-105">Ierakstu veidnes var palīdzēt jums izveidot ierakstus ātrāk, taču ierakstu veidnes varat izveidot tikai dažiem ierakstu veidiem.</span><span class="sxs-lookup"><span data-stu-id="89d39-105">Record templates can help you to create records more quickly, however you can only create record templates for some record types.</span></span>

<span data-ttu-id="89d39-106">Piemēram, iedomājieties, ka jūs ievadāt nomas informāciju par automašīnu nomas darījumu, kas atrodas San Francisko.</span><span class="sxs-lookup"><span data-stu-id="89d39-106">For example, imagine you are entering rental information for a car rental business that is located in San Francisco.</span></span> <span data-ttu-id="89d39-107">Tā kā lielākā daļa klientu visdrīzāk ir no San Francisko apvidus, būtu jauki, ja jūs varētu automātiski aizpildīt nomas veidlapas lauku **Administratīvais apgabals**, **Valsts**, un **Pilsēta** vērtības.</span><span class="sxs-lookup"><span data-stu-id="89d39-107">Since most of the customers are likely to be from the San Francisco area, it would be nice if you could automatically fill in the values for the **State**, **Country**, and **City** fields on the rental form.</span></span>

> [!NOTE]
> <span data-ttu-id="89d39-108">Veidnes varat lietot tikai tādos apgabalos, kam varat piekļūt.</span><span class="sxs-lookup"><span data-stu-id="89d39-108">You can apply templates only in areas that you have access to.</span></span> <span data-ttu-id="89d39-109">Tomēr ir redzami visi veidņu nosaukumi, kad izveidojat jaunu ierakstu, un tie ir redzami arī citiem lietotājiem, ja jūs izveidojat veidnes, kas būs pieejamas visiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="89d39-109">However all template titles are visible to you when you create a new record, and to other users as well, if you are creating templates that will be available for all users.</span></span> <span data-ttu-id="89d39-110">Paturiet to prātā, kad piešķirsiet veidnēm nosaukumus.</span><span class="sxs-lookup"><span data-stu-id="89d39-110">Be sure to consider this when naming templates.</span></span> <span data-ttu-id="89d39-111">Piemēram, centieties neizmantot nosaukumus, kuri satur tādus vārdus kā “komisija”, ja ne visiem lietotājiem būtu jāzina, ka dažiem uzņēmuma darbiniekiem algas ir balstītas uz komisiju.</span><span class="sxs-lookup"><span data-stu-id="89d39-111">For example, avoid using names that include words, such as "commission," if is confidential that some employees in the company have commission-based salaries.</span></span>

<span data-ttu-id="89d39-112">Kad specifiskai formai pastāv viena vai vairākas veidnes, kam jums ir piekļuve, un jūs mēģināt izveidot jaunu ierakstu šajā formā, tiek parādīta lapa **Atlasiet veidni, kas paredzēta...**.</span><span class="sxs-lookup"><span data-stu-id="89d39-112">When one or more templates that you have access to exist for a specific form and you attempt to create a new record in the form, the **Select a template for** page is displayed.</span></span> <span data-ttu-id="89d39-113">Kad atlasāt veidni no saraksta, tiek izveidots jauns ieraksts, kas satur uz atlasīto veidni balstītu noklusējuma informāciju.</span><span class="sxs-lookup"><span data-stu-id="89d39-113">When you select a template from the list, the new record is created and contains default information that is based on the template that you selected.</span></span> <span data-ttu-id="89d39-114">Ja nevēlaties izmantot veidnes jaunu ierakstu izveidei, atzīmējiet izvēles rūtiņu **Nejautāt atkārtoti** lapā **Atlasiet veidni, kas paredzēta**.</span><span class="sxs-lookup"><span data-stu-id="89d39-114">If you do not want to use templates when you create new records, select the **Do not ask again** check box in the **Select a template for** page.</span></span> <span data-ttu-id="89d39-115">Lai atkal tiktu parādīts veidnes atlases dialoglodziņš, ar peles labo pogu noklikšķiniet uz jebkura ieraksta, noklikšķiniet uz **Informācija par ierakstu** un pēc tam noklikšķiniet uz **Parādīt veidnes atlasi**.</span><span class="sxs-lookup"><span data-stu-id="89d39-115">To display the template selection dialog box again, right-click any record, click **Record info**, and then click **Show template selection**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]