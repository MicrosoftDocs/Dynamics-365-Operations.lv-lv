---
title: Globālā ieturētā nodokļa iestatīšana
description: Šajā tēmā ir uzskaitītas darbības globālā ieturētā nodokļa iestatīšanai pārdošanai un pirkšanai.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 00c472e90f4926c52ffe9b19661e68cbfa6bd493
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204837"
---
# <a name="set-up-global-withholding-tax"></a><span data-ttu-id="628d4-103">Globālā ieturētā nodokļa iestatīšana</span><span class="sxs-lookup"><span data-stu-id="628d4-103">Set up global withholding tax</span></span>

<span data-ttu-id="628d4-104">Šajā tēmā ir uzskaitītas darbības globālā ieturētā nodokļa iestatīšanai pārdošanai un pirkšanai.</span><span class="sxs-lookup"><span data-stu-id="628d4-104">This topic lists the steps for setting up global withholding tax for sales and purchases.</span></span> 

1. <span data-ttu-id="628d4-105">Iestatiet ieturēto nodokļu iestādes lapā **Ieturēto nodokļu iestādes**.</span><span class="sxs-lookup"><span data-stu-id="628d4-105">Set up withholding tax authorities on the **Withholding tax authorities** page.</span></span>

2. <span data-ttu-id="628d4-106">Iestatiet ieturētā nodokļa apmaksas periodus lapā **Ieturētā nodokļa apmaksas periodi**.</span><span class="sxs-lookup"><span data-stu-id="628d4-106">Set up withholding settlement periods on the **Withholding tax settlement periods** page.</span></span>

3. <span data-ttu-id="628d4-107">Iestatiet ieturētās Virsgrāmatas grāmatošanas grupu lapā **Ieturētais nodoklis > Virsgrāmatas grāmatošanas grupa**.</span><span class="sxs-lookup"><span data-stu-id="628d4-107">Set up withholding ledger posting group on the **Withholding tax > ledger posting group** page.</span></span>

   > [!Note] 
   >
   > <span data-ttu-id="628d4-108">**Ieturētā nodokļa** konts tiks piešķirts ar galveno kontu ar Ieturētā nodokļa **Grāmatošanas veidu**.</span><span class="sxs-lookup"><span data-stu-id="628d4-108">**Withholding tax** account will be assigned with a main account with **Posting type** of Withholding tax.</span></span> <span data-ttu-id="628d4-109">**Ieturētā nodokļa nobīdes** konts tiks arī piešķirts ar galveno kontu ar **Grāmatošanas veidu** "Ieturētā nodokļa nobīde".</span><span class="sxs-lookup"><span data-stu-id="628d4-109">**Withholding tax offset** account will also be assigned with a main account with **Posting type** "Withholding tax offset".</span></span> <span data-ttu-id="628d4-110">Dodieties uz **Virsgrāmata > Kontu plāns > Konti > Galvenie konti**, iestatiet **Grāmatošanas veidu** galveno kontu apakšformā **Grāmatošanas apstiprināšana**.</span><span class="sxs-lookup"><span data-stu-id="628d4-110">Go to **General ledger > Chart of accounts > Accounts > Main accounts**, set up the **Posting type** in the **Posting validation** sub-form for the main accounts.</span></span>

4. <span data-ttu-id="628d4-111">Iestatiet ieturēto nodokļu kodus lapā **Ieturēto nodokļu kodi**.</span><span class="sxs-lookup"><span data-stu-id="628d4-111">Set up withholding tax codes on the **Withholding tax codes** page.</span></span>

5. <span data-ttu-id="628d4-112">Iestatiet ieturēto nodokļu grupas lapā **Ieturēto nodokļu grupas**.</span><span class="sxs-lookup"><span data-stu-id="628d4-112">Set up withholding tax groups on the **Withholding tax groups** page.</span></span>

6. <span data-ttu-id="628d4-113">Iestatiet ieturētā nodokļa ieņēmumu veidus lapā **Ieturētā nodokļa ieņēmumu** **veidi**.</span><span class="sxs-lookup"><span data-stu-id="628d4-113">Set up withholding tax revenue types on the **Withholding tax revenue** **types** page.</span></span>

7. <span data-ttu-id="628d4-114">Iestatiet ieturēto nodokļu grupas lapā **Pakalpojumu krājuma ieturēto nodokļu grupas** krājumam vai pakalpojumam.</span><span class="sxs-lookup"><span data-stu-id="628d4-114">Set up withholding tax groups on the **Item withholding tax groups** page for an item or service.</span></span>

8. <span data-ttu-id="628d4-115">Iestatiet **Minimālo rēķina summu** lapā **Virsgrāmatas parametri > Ieturētais nodoklis**.</span><span class="sxs-lookup"><span data-stu-id="628d4-115">Set up **Minimum invoice amount** on the **General ledger parameters > Withholding tax** page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]