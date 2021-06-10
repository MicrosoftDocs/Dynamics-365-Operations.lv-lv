---
title: Konfigurēt atvieglojumu pārvaldības parametrus katram uzņēmumam
description: Konfigurējiet parametrus atvieglojumu pārvaldībai katrai kompānijai risinājumā Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d2c564f0dfd1cbe44566269c97218450fedf2173
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6057626"
---
# <a name="configure-benefits-management-parameters-per-company"></a><span data-ttu-id="57001-103">Konfigurēt atvieglojumu pārvaldības parametrus katram uzņēmumam</span><span class="sxs-lookup"><span data-stu-id="57001-103">Configure Benefits management parameters per company</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="57001-104">Katrai organizācijai, kas piedāvā atvieglojumus, ir jākonfigurē atvieglojumu apstiprinājuma e-pastu iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="57001-104">For each organization that offers benefits, you must configure settings for benefits confirmation emails.</span></span>

## <a name="configure-confirmation-email-settings"></a><span data-ttu-id="57001-105">E-pasta apstiprinājuma iestatījumu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="57001-105">Configure confirmation email settings</span></span>

1. <span data-ttu-id="57001-106">Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Personāla vadības parametri**.</span><span class="sxs-lookup"><span data-stu-id="57001-106">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="57001-107">Cilnē **Atvieglojumu pārvaldība** norādiet vērtības šiem laukiem:</span><span class="sxs-lookup"><span data-stu-id="57001-107">In the **Benefits management** tab, specify values for the following fields:</span></span> 

   | <span data-ttu-id="57001-108">Lauks</span><span class="sxs-lookup"><span data-stu-id="57001-108">Field</span></span> | <span data-ttu-id="57001-109">Apraksts</span><span class="sxs-lookup"><span data-stu-id="57001-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="57001-110">**Nosūtīt apstiprinājuma e-pasta ziņojumu**</span><span class="sxs-lookup"><span data-stu-id="57001-110">**Send confirmation email**</span></span> | <span data-ttu-id="57001-111">Kad šī funkcija ir ieslēgta, darbiniekiem tiks nosūtīta apstiprinājuma e-pasta adrese, kad viņi iepazīsies ar atvieglojumu reģistrācijas pieredzi Darbinieku pašapkalpošanās sadaļā.</span><span class="sxs-lookup"><span data-stu-id="57001-111">When this feature is on, a confirmation email will be sent to employees when they check out from the benefits enrollment experience in Employee self-service.</span></span> |
   | <span data-ttu-id="57001-112">**Apstiprinājuma e-pasta veidne**</span><span class="sxs-lookup"><span data-stu-id="57001-112">**Confirmation email template**</span></span> | <span data-ttu-id="57001-113">Atlasiet organizācijas e-pasta veidni, ko izmantot, sūtot reģistrācijas apstiprinājumu.</span><span class="sxs-lookup"><span data-stu-id="57001-113">Select the organization email template to use when sending the enrollment confirmation.</span></span> <span data-ttu-id="57001-114">Ja neatlasāt veidni, tiks nosūtīta šāda vispārīga e-pasta vēstule:</span><span class="sxs-lookup"><span data-stu-id="57001-114">If you don't select a template, the following generic email will be sent:</span></span><br><br><span data-ttu-id="57001-115">%EmployeeFirstName%,</span><span class="sxs-lookup"><span data-stu-id="57001-115">%EmployeeFirstName%,</span></span><br><br><span data-ttu-id="57001-116">Apsveicam!</span><span class="sxs-lookup"><span data-stu-id="57001-116">Congratulations!</span></span> <span data-ttu-id="57001-117">Ir sekmīgi pabeigta atvieglojumu reģistrācija.</span><span class="sxs-lookup"><span data-stu-id="57001-117">You’ve successfully completed benefits enrollment.</span></span><br><br><span data-ttu-id="57001-118">Paldies,</span><span class="sxs-lookup"><span data-stu-id="57001-118">Thank you,</span></span><br><span data-ttu-id="57001-119"><Kompānija/Org nosaukums> Atvieglojumi.</span><span class="sxs-lookup"><span data-stu-id="57001-119"><Company/Org name> Benefits.</span></span> |
   | <span data-ttu-id="57001-120">**Noklusējuma e-pasta sūtītāja adrese**</span><span class="sxs-lookup"><span data-stu-id="57001-120">**Default email sender address**</span></span> | <span data-ttu-id="57001-121">E-pasta adrese, ko izmantot, sūtot apstiprinājuma e-pastu.</span><span class="sxs-lookup"><span data-stu-id="57001-121">The email address to use when sending the confirmation email.</span></span> |

3. <span data-ttu-id="57001-122">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="57001-122">Select **Save**.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]