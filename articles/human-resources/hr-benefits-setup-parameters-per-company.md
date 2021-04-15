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
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 87d4f1e7580b333fd17d3b779aafa47c5baed424
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805662"
---
# <a name="configure-benefits-management-parameters-per-company"></a><span data-ttu-id="e849e-103">Konfigurēt atvieglojumu pārvaldības parametrus katram uzņēmumam</span><span class="sxs-lookup"><span data-stu-id="e849e-103">Configure Benefits management parameters per company</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e849e-104">Katrai organizācijai, kas piedāvā atvieglojumus, ir jākonfigurē atvieglojumu apstiprinājuma e-pastu iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="e849e-104">For each organization that offers benefits, you must configure settings for benefits confirmation emails.</span></span>

## <a name="configure-confirmation-email-settings"></a><span data-ttu-id="e849e-105">E-pasta apstiprinājuma iestatījumu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="e849e-105">Configure confirmation email settings</span></span>

1. <span data-ttu-id="e849e-106">Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Personāla vadības parametri**.</span><span class="sxs-lookup"><span data-stu-id="e849e-106">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="e849e-107">Cilnē **Atvieglojumu pārvaldība** norādiet vērtības šiem laukiem:</span><span class="sxs-lookup"><span data-stu-id="e849e-107">In the **Benefits management** tab, specify values for the following fields:</span></span> 

   | <span data-ttu-id="e849e-108">Lauks</span><span class="sxs-lookup"><span data-stu-id="e849e-108">Field</span></span> | <span data-ttu-id="e849e-109">Apraksts</span><span class="sxs-lookup"><span data-stu-id="e849e-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="e849e-110">**Nosūtīt apstiprinājuma e-pasta ziņojumu**</span><span class="sxs-lookup"><span data-stu-id="e849e-110">**Send confirmation email**</span></span> | <span data-ttu-id="e849e-111">Kad šī funkcija ir ieslēgta, darbiniekiem tiks nosūtīta apstiprinājuma e-pasta adrese, kad viņi iepazīsies ar atvieglojumu reģistrācijas pieredzi Darbinieku pašapkalpošanās sadaļā.</span><span class="sxs-lookup"><span data-stu-id="e849e-111">When this feature is on, a confirmation email will be sent to employees when they check out from the benefits enrollment experience in Employee self-service.</span></span> |
   | <span data-ttu-id="e849e-112">**Apstiprinājuma e-pasta veidne**</span><span class="sxs-lookup"><span data-stu-id="e849e-112">**Confirmation email template**</span></span> | <span data-ttu-id="e849e-113">Atlasiet organizācijas e-pasta veidni, ko izmantot, sūtot reģistrācijas apstiprinājumu.</span><span class="sxs-lookup"><span data-stu-id="e849e-113">Select the organization email template to use when sending the enrollment confirmation.</span></span> <span data-ttu-id="e849e-114">Ja neatlasāt veidni, tiks nosūtīta šāda vispārīga e-pasta vēstule:</span><span class="sxs-lookup"><span data-stu-id="e849e-114">If you don't select a template, the following generic email will be sent:</span></span><br><br><span data-ttu-id="e849e-115">%EmployeeFirstName%,</span><span class="sxs-lookup"><span data-stu-id="e849e-115">%EmployeeFirstName%,</span></span><br><br><span data-ttu-id="e849e-116">Apsveicam!</span><span class="sxs-lookup"><span data-stu-id="e849e-116">Congratulations!</span></span> <span data-ttu-id="e849e-117">Ir sekmīgi pabeigta atvieglojumu reģistrācija.</span><span class="sxs-lookup"><span data-stu-id="e849e-117">You’ve successfully completed benefits enrollment.</span></span><br><br><span data-ttu-id="e849e-118">Paldies,</span><span class="sxs-lookup"><span data-stu-id="e849e-118">Thank you,</span></span><br><span data-ttu-id="e849e-119"><Kompānija/Org nosaukums> Atvieglojumi.</span><span class="sxs-lookup"><span data-stu-id="e849e-119"><Company/Org name> Benefits.</span></span> |
   | <span data-ttu-id="e849e-120">**Noklusējuma e-pasta sūtītāja adrese**</span><span class="sxs-lookup"><span data-stu-id="e849e-120">**Default email sender address**</span></span> | <span data-ttu-id="e849e-121">E-pasta adrese, ko izmantot, sūtot apstiprinājuma e-pastu.</span><span class="sxs-lookup"><span data-stu-id="e849e-121">The email address to use when sending the confirmation email.</span></span> |

3. <span data-ttu-id="e849e-122">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="e849e-122">Select **Save**.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]