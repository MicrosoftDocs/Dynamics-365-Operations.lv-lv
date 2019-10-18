---
title: Iespējot Broadbean integrāciju programmā Microsoft Dynamics 365 Talent - Attract
description: Šajā tēmā ir paskaidrots, kā konfigurēt Microsoft Dynamics 365 Talent - Attract, lai grāmatotu darbus uz ārējiem darba sludinājuma dēļiem, piemēram, Broadbean.
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 808f91fb4b68ba9b5cee54d86423d23232df23a4
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008597"
---
# <a name="enable-broadbean-integration"></a><span data-ttu-id="19035-103">Iespējot Broadbean integrāciju</span><span class="sxs-lookup"><span data-stu-id="19035-103">Enable Broadbean integration</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="19035-104">Jūs vēlaties, lai jūsu atvērtās pozīcijas redz iespējami daudz kvalificētu kandidātu.</span><span class="sxs-lookup"><span data-stu-id="19035-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="19035-105">Personāla atlases vietnes, piemēram, Broadbean, palīdz jums sasniegt šo mērķi.</span><span class="sxs-lookup"><span data-stu-id="19035-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="19035-106">Microsoft Dynamics 365 Talent: Attract tagad ļauj jums publicēt vietnē Broadbean, un Microsoft pastāvīgi nodrošina jaunu piedāvājumu šajā jomā.</span><span class="sxs-lookup"><span data-stu-id="19035-106">Microsoft Dynamics 365 Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

> [!NOTE]
> - <span data-ttu-id="19035-107">Lai publicētu darbus ārējās vietnēs, ir nepieciešama [visaptveroša nolīgšanas pievienojumprogramma](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span><span class="sxs-lookup"><span data-stu-id="19035-107">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="19035-108">Lai grāmatotu darbus programmatūrā Broadbean, izmantojot Attract, jums ir nepieciešams Broadbean abonements.</span><span class="sxs-lookup"><span data-stu-id="19035-108">To post jobs to Broadbean through Attract, you must have a Broadbean subscription.</span></span>
> - <span data-ttu-id="19035-109">Šis līdzeklis pašreiz ir priekšskatījumā.</span><span class="sxs-lookup"><span data-stu-id="19035-109">This feature is currently in preview.</span></span> <span data-ttu-id="19035-110">Ja vēlaties to izmēģināt, jums [tā ir jāieslēdz pakalpojuma Attract administratora iestatījumos](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="19035-110">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

## <a name="configure-broadbean-integration"></a><span data-ttu-id="19035-111">Broadbean integrācijas konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="19035-111">Configure Broadbean integration</span></span>

1. <span data-ttu-id="19035-112">Piesakieties pakalpojumā Attract kā administrators.</span><span class="sxs-lookup"><span data-stu-id="19035-112">Sign in to Attract as an admin.</span></span>

2. <span data-ttu-id="19035-113">Atlasiet pogu **Iestatījumi** (zobrata simbols) lapas labās puses augšējā stūrī un pēc tam atlasiet **Administrēšanas centrs**.</span><span class="sxs-lookup"><span data-stu-id="19035-113">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>

3. <span data-ttu-id="19035-114">Sazinieties ar Broadbean un ievadiet informāciju laukā **Lietotājvārds**, **Klienta ID**, un **Šifrēšanas pilnvara**.</span><span class="sxs-lookup"><span data-stu-id="19035-114">Contact Broadbean, and enter your information in the **Username**, **Client ID**, and **Encryption Token** fields.</span></span>

4. <span data-ttu-id="19035-115">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="19035-115">Select **Save**.</span></span>

> [!WARNING]
> <span data-ttu-id="19035-116">Jūsu Broadbean akreditācijas dati ir jutīgi un konfidenciāli.</span><span class="sxs-lookup"><span data-stu-id="19035-116">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="19035-117">Tāpēc glabājiet un koplietojiet tos atbildīgi.</span><span class="sxs-lookup"><span data-stu-id="19035-117">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="19035-118">Ikviena persona, kurai administratora loma pakalpojumā Attract, var skatīt šos akreditācijas datus.</span><span class="sxs-lookup"><span data-stu-id="19035-118">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="19035-119">Microsoft un Attract nav iesaistīti šo vērtību izveidē un saglabāšanā.</span><span class="sxs-lookup"><span data-stu-id="19035-119">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="19035-120">Jūsu pienākums ir tos atjaunināt pakalpojumā Attract un sadarboties ar Broadbean, lai atrisinātu jebkādas problēmas, kas ir saistītas ar jūsu akreditācijas datiem.</span><span class="sxs-lookup"><span data-stu-id="19035-120">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>
