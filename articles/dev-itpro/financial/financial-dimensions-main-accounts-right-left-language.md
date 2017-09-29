---
title: "Finanšu dimensijas un galvenie konti valodā ar rakstību no labās puses uz kreiso"
description: "Šajā tēmā ir aprakstīti daži no ieviešanas lēmumiem, kas ir jāņem vērā, kad lietojat valodu ar rakstību no labās puses uz kreiso un ir jāiestata finanšu dimensijas un galvenie konti."
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: b8ceee7486cae9ec0ff7dfedc35909e2f01d0616
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---

# <a name="financial-dimensions-and-main-accounts-in-a-right-to-left-language"></a><span data-ttu-id="846c5-103">Finanšu dimensijas un galvenie konti valodā ar rakstību no labās puses uz kreiso</span><span class="sxs-lookup"><span data-stu-id="846c5-103">Financial dimensions and main accounts in a right-to-left language</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="846c5-104">Šajā tēmā ir aprakstīti daži no ieviešanas lēmumiem, kas ir jāņem vērā, kad lietojat valodu ar rakstību no labās puses uz kreiso un ir jāiestata finanšu dimensijas un galvenie konti.</span><span class="sxs-lookup"><span data-stu-id="846c5-104">This topic describes some of the implementation decisions that you should consider when you use a right-to-left language, and you must set up financial dimensions and main accounts.</span></span>

<span data-ttu-id="846c5-105">Finanšu dimensijas un galvenie konti ir galvenie implementēšanas plānošanas fāzes komponenti.</span><span class="sxs-lookup"><span data-stu-id="846c5-105">Financial dimensions and main accounts are key components of the planning phase for an implementation.</span></span> <span data-ttu-id="846c5-106">Kad sistēma ir izveidotas finanšu dimensijas un galvenie konti, tie tiek izmantoti lapās **Konfigurēt kontu struktūras**, **Detalizēto kārtulu struktūras** un **Finanšu dimensijas konfigurācija programmu integrēšanai**.</span><span class="sxs-lookup"><span data-stu-id="846c5-106">After financial dimensions and main accounts are created in the system, they are used on the **Configure account structures**, **Advanced rule structures**, and **Financial dimension configuration for integrating applications** pages.</span></span> <span data-ttu-id="846c5-107">Šajās lapas definētā secība sistēmā tiek izmantota datu ievadei un patēriņam.</span><span class="sxs-lookup"><span data-stu-id="846c5-107">The order that is defined on those pages is used in the system for data entry and consumption.</span></span> <span data-ttu-id="846c5-108">Noteiktās sistēmas vietās finanšu dimensijas un galvenie konti tiek rādīti atsevišķos laukos.</span><span class="sxs-lookup"><span data-stu-id="846c5-108">In some places in the system, the financial dimensions and main accounts appear in separate fields.</span></span> <span data-ttu-id="846c5-109">Taču citviet, piemēram, žurnālos, finanšu dimensijas un galvenie konti tiek rādīti kā viena virkne.</span><span class="sxs-lookup"><span data-stu-id="846c5-109">However, in other places, such as journals, the financial dimensions and main accounts appear as a single string.</span></span>

### <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a><span data-ttu-id="846c5-110">Finanšu dimensiju un galveno kontu iestatīšanas paraugprakse sistēmā ar rakstību no labās puses uz kreiso</span><span class="sxs-lookup"><span data-stu-id="846c5-110">Best practices for setting up financial dimensions and main accounts in a right-to-left system</span></span>

-   <span data-ttu-id="846c5-111">Kad atlasāt norobežotāju kontu plāniem, atlasiet kādu no dubultajām norobežotāju opcijām: dubulto pārnesumzīmi (--), dubulto šķirtni (||) vai divpunkti (..), vai dubulto pasvītrojuma zīmi (\_\_).</span><span class="sxs-lookup"><span data-stu-id="846c5-111">When you select the delimiter for charts of accounts, select one of the double delimiter options: double hyphen (--), double bar (||) or double period (..), or double underscore (\_\_).</span></span>
-   <span data-ttu-id="846c5-112">Kad veidojat finanšu dimensijas un galvenā konta vērtības, izmantojiet tikai ciparus un rakstzīmes valodai ar rakstību no labās puses uz kreiso.</span><span class="sxs-lookup"><span data-stu-id="846c5-112">When you create financial dimension and main account values, use only numbers and right-to-left language characters.</span></span>
-   <span data-ttu-id="846c5-113">Atlasīto kontu plāna norobežotāju nelietojiet finanšu dimensijas un galveno kontu vērtībās.</span><span class="sxs-lookup"><span data-stu-id="846c5-113">Avoid using the selected chart of accounts delimiter in financial dimension and main account values.</span></span>

<span data-ttu-id="846c5-114">Ievērojot šo paraugpraksi, jūs palīdzat garantēt konsekventu lietotāja definēto pasūtījumu attēlojumu visā sistēmā.</span><span class="sxs-lookup"><span data-stu-id="846c5-114">By following these best practices, you help guarantee consistent representation of the user defined-order throughout the system.</span></span>




