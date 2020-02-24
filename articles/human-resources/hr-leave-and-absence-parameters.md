---
title: Atvaļinājumu un prombūtnes parametru konfigurēšana
description: Definējiet cilvēkresursu parametrus atvaļinājumam un prombūtnei pakalpojumā Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2acb8502ebcab122a0a1ff21e9f5e23931026327
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009789"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="b0d3e-103">Atvaļinājumu un prombūtnes parametru konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="b0d3e-103">Configure leave and absence parameters</span></span>

<span data-ttu-id="b0d3e-104">Pirms atvaļinājumu un prombūtnes plānu iestatīšanas pakalpojumā Dynamics 365 Human Resources, ir ieteicams pārbaudīt visu saistīto personāla vadības parametru iestatījumus, tostarp:</span><span class="sxs-lookup"><span data-stu-id="b0d3e-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="b0d3e-105">Atvaļinājumu pieprasījumu numuru sēriju</span><span class="sxs-lookup"><span data-stu-id="b0d3e-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="b0d3e-106">Likuma par ģimenes un medicīniskajiem atvaļinājumiem (FMLA) iestatījumus</span><span class="sxs-lookup"><span data-stu-id="b0d3e-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="b0d3e-107">Darbinieku patstāvīgi izmantojamo pakalpojumu iestatījumus atvaļinājumu un prombūtnes pieprasījumiem</span><span class="sxs-lookup"><span data-stu-id="b0d3e-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="b0d3e-108">Atvaļinājumu un prombūtnes parametri</span><span class="sxs-lookup"><span data-stu-id="b0d3e-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="b0d3e-109">Skatīt un mainīt personāla vadības parametrus</span><span class="sxs-lookup"><span data-stu-id="b0d3e-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="b0d3e-110">Lapā **Atvaļinājums un prombūtne** atlasiet cilni **Saites**.</span><span class="sxs-lookup"><span data-stu-id="b0d3e-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="b0d3e-111">Sadaļā **Iestatījumi** atlasiet **Personāla vadības parametri**.</span><span class="sxs-lookup"><span data-stu-id="b0d3e-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="b0d3e-112">Cilnē **Numuru sērijas** pārbaudiet **Numuru secības kodu** **Atvaļinājuma pieprasījuma ID** un pēc nepieciešamības veiciet izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="b0d3e-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="b0d3e-113">Šis iestatījums nosaka secību, kas tiek izmantota, lai automātiski piešķirtu ID atvaļinājumu pieprasījumiem.</span><span class="sxs-lookup"><span data-stu-id="b0d3e-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="b0d3e-114">Cilnē **FMLA** pārbaudiet FMLA iestatījumus un pēc nepieciešamības mainiet.</span><span class="sxs-lookup"><span data-stu-id="b0d3e-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="b0d3e-115">Cilnē **Darbinieku patstāvīgi izmantojamie pakalpojumi** norādiet, vai vadītāji var ievadīt atvaļinājumu un kavējumu pieprasījumus savu darbinieku vārdā.</span><span class="sxs-lookup"><span data-stu-id="b0d3e-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

6. <span data-ttu-id="b0d3e-116">Cilnē **Atvaļinājums un prombūtne** pārbaudiet FMLA iestatījumus un pēc nepieciešamības veiciet izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="b0d3e-116">On the **Leave and absence** tab, verify the settings and change as necessary.</span></span>

7. <span data-ttu-id="b0d3e-117">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="b0d3e-117">Select **Save**.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="b0d3e-118">Konfigurējiet kalendāra parametrus</span><span class="sxs-lookup"><span data-stu-id="b0d3e-118">Configure calendar parameters</span></span>

<span data-ttu-id="b0d3e-119">Ja esat iespējojis atvaļinājumu un prombūtnes kalendāra priekšskatījuma funkciju, ir jākonfigurē papildu parametri.</span><span class="sxs-lookup"><span data-stu-id="b0d3e-119">If you have enabled the Leave and absence calendar preview feature, you need to configure additional parameters.</span></span> 

[!include [banner](includes/preview-feature-leave-absence.md)]

> [!NOTE]
> <span data-ttu-id="b0d3e-120">Priekšskatījuma laidienam 2020. gada 3. februārī tiek iespējoti tikai **Gaidoši atvaļinājumu pieprasījumi**.</span><span class="sxs-lookup"><span data-stu-id="b0d3e-120">For the preview release on February 3, 2020, only **Pending leave requests** are enabled.</span></span>

1. <span data-ttu-id="b0d3e-121">Lapā **Atvaļinājums un prombūtne** atlasiet cilni **Saites**.</span><span class="sxs-lookup"><span data-stu-id="b0d3e-121">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="b0d3e-122">Sadaļā **Iestatījumi** atlasiet **Personāla vadības parametri**.</span><span class="sxs-lookup"><span data-stu-id="b0d3e-122">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="b0d3e-123">Cilnē **Kalendārs** pēc nepieciešamības mainiet kalendāra iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="b0d3e-123">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="b0d3e-124">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="b0d3e-124">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="b0d3e-125">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="b0d3e-125">See also</span></span>

- [<span data-ttu-id="b0d3e-126">Atvaļinājumu un kavējumu apskats</span><span class="sxs-lookup"><span data-stu-id="b0d3e-126">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
