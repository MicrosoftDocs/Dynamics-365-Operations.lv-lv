---
title: Jaunumi un izmaiņas programmā Dynamics 365 Talent (2019. gada 29. oktobris)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-10-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e2d79ee9e182df4a4efe65beb685567b1e7446ce
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897446"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-29-2019"></a><span data-ttu-id="55ea0-103">Jaunumi un izmaiņas programmā Dynamics 365 Talent (2019. gada 29. oktobris)</span><span class="sxs-lookup"><span data-stu-id="55ea0-103">What's new or changed in Dynamics 365 Talent (October 29, 2019)</span></span>

<span data-ttu-id="55ea0-104">Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="55ea0-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="55ea0-105">Izmaiņas programmā Attract</span><span class="sxs-lookup"><span data-stu-id="55ea0-105">Changes in Attract</span></span>

<span data-ttu-id="55ea0-106">Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="55ea0-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="55ea0-107">Izmaiņas programmā Onboard</span><span class="sxs-lookup"><span data-stu-id="55ea0-107">Changes in Onboard</span></span>

<span data-ttu-id="55ea0-108">Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="55ea0-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="55ea0-109">Izmaiņas programmā Core HR</span><span class="sxs-lookup"><span data-stu-id="55ea0-109">Changes in Core HR</span></span>

<span data-ttu-id="55ea0-110">Šajā sadaļā aprakstītās izmaiņas attiecas uz būvējumu Nr. 8.1.2586.</span><span class="sxs-lookup"><span data-stu-id="55ea0-110">Changes described in this section apply to build number 8.1.2586.</span></span> <span data-ttu-id="55ea0-111">Dažos virsrakstos redzamie numuri iekavās attiecas uz atbalsta numuriem portālā Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="55ea0-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="delete-parties-with-no-roles-should-be-on-by-default-371233"></a><span data-ttu-id="55ea0-112">Dzēst puses bez lomām ir jāiestata pēc noklusējuma (371233)</span><span class="sxs-lookup"><span data-stu-id="55ea0-112">Delete parties with no roles should be on by default (371233)</span></span>

<span data-ttu-id="55ea0-113">Kad jūs nodrošināt jaunu vidi programmā Talent, funkcija **Dzēst puses, ja nav lomu** ir ieslēgta pēc noklusējuma.</span><span class="sxs-lookup"><span data-stu-id="55ea0-113">When you provision a new environment in Talent, **Delete parties if no roles exist** is turned on by default.</span></span> <span data-ttu-id="55ea0-114">Dzēšot darbinieku, ar darbinieku saistītā puse netiek noņemta, ja vien šis iestatījums nav iestatīts.</span><span class="sxs-lookup"><span data-stu-id="55ea0-114">When you delete a worker, the party associated with the worker is not removed unless this setting is on.</span></span> <span data-ttu-id="55ea0-115">Šīs izmaiņas ierobežo ierakstu dublikātus globālajā adrešu grāmatā, kad nepieciešams importēt, mainīt vai atkārtoti importēt darbiniekus.</span><span class="sxs-lookup"><span data-stu-id="55ea0-115">This change limits duplicate records in the global address book when you need to import, change, or reimport workers.</span></span>

### <a name="draft-and-cancelled-leave-requests-should-be-allowed-to-be-deleted-in-common-data-service-376999"></a><span data-ttu-id="55ea0-116">Melnraksta un atcelto atvaļinājumu pieprasījumi ir jāatļauj dzēst programmā Common Data Service (376999)</span><span class="sxs-lookup"><span data-stu-id="55ea0-116">Draft and cancelled leave requests should be allowed to be deleted in Common Data Service (376999)</span></span>

<span data-ttu-id="55ea0-117">Ar šīm izmaiņām tagad varat dzēst atvaļinājumu pieprasījumus ar statusu **Melnraksts** vai **Atcelts** Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="55ea0-117">With this change, you can now delete leave requests with a status of **Draft** or **Cancelled** in Common Data Service.</span></span>

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a><span data-ttu-id="55ea0-118">Papildu saraksta vērtības pielāgotos laukos netiek parādītas Common Data Service pēc noklikšķināšanas uz Pielietot Pielāgoto lauku formā (379599).</span><span class="sxs-lookup"><span data-stu-id="55ea0-118">Additional list values in custom fields aren't reflected in Common Data Service after clicking Apply on the Custom fields form (379599)</span></span>

<span data-ttu-id="55ea0-119">Kad pievienojat jaunas saraksta vērtības esošam pielāgotam laukam, kas jau ir sinhronizēts ar Common Data Service, tās tagad ir pieejamas Common Data Service pēc izmaiņu piemērošanas formā **Pielāgoti lauki**.</span><span class="sxs-lookup"><span data-stu-id="55ea0-119">When you add new list values to an existing custom field that has already synchronized with Common Data Service, they're now available in Common Data Serivce after you apply your changes in the **Custom fields** form.</span></span>

### <a name="apply-onboarding-checklists-across-legal-entities-when-more-than-one-employment-exists-371270"></a><span data-ttu-id="55ea0-120">Piemērot pārbaudes kontrolsarakstus visās juridiskajās personās, ja pastāv vairāk nekā viens darbs (371270)</span><span class="sxs-lookup"><span data-stu-id="55ea0-120">Apply onboarding checklists across legal entities when more than one employment exists (371270)</span></span>

<span data-ttu-id="55ea0-121">Šīs nedēļas laidienā varat pielietot kontrolsarakstus darbiniekiem ar vairāk nekā vienu darbu **Darbinieku forma > Kontrolsaraksti**.</span><span class="sxs-lookup"><span data-stu-id="55ea0-121">In this week's release, you can apply checklists to employees with more than one employment in **Worker form > Checklists**.</span></span>

### <a name="benefits-open-enrollment-preview-feature-has-been-removed"></a><span data-ttu-id="55ea0-122">Priekšrocības atvērtās reģistrācijas priekšskatījuma funkcija ir noņemta</span><span class="sxs-lookup"><span data-stu-id="55ea0-122">Benefits open enrollment preview feature has been removed</span></span>

<span data-ttu-id="55ea0-123">Saistībā ar mūsu paziņojumu [Stratēģiskās investīcijas Core HR Drive Operational Excellence](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) blogā, korporācija Microsoft noņem atvieglojumus, kas atvērti reģistrācijai no publiskās priekšskatīšanas.</span><span class="sxs-lookup"><span data-stu-id="55ea0-123">In conjunction with our announcement in the [Strategic investments in core HR drive operational excellence](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) blog post, Microsoft has removed the benefits open enrollment feature from public preview.</span></span> <span data-ttu-id="55ea0-124">Nākotnē tiks izlaista jauna funkcionalitāte.</span><span class="sxs-lookup"><span data-stu-id="55ea0-124">New functionality will be released in the future.</span></span> <span data-ttu-id="55ea0-125">Ražošanas priekšrocību atvērta reģistrēšanās funkcija netiek atbalstīta.</span><span class="sxs-lookup"><span data-stu-id="55ea0-125">Production use of the benefits open enrollment feature isn't be supported.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="55ea0-126">Drīzumā</span><span class="sxs-lookup"><span data-stu-id="55ea0-126">Coming soon</span></span>

### <a name="print-performance-reviews"></a><span data-ttu-id="55ea0-127">Veiktspējas pārskatu drukāšana</span><span class="sxs-lookup"><span data-stu-id="55ea0-127">Print performance reviews</span></span>

<span data-ttu-id="55ea0-128">Aplūkojiet [Drukāšanas veiktspējas pārskati](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) Dynamics 365: 2019. gada izlaiduma 2. laidiena plāns.</span><span class="sxs-lookup"><span data-stu-id="55ea0-128">See [Print performance reviews](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in the Dynamics 365: 2019 release wave 2 plan.</span></span>

### <a name="feature-management-workspace"></a><span data-ttu-id="55ea0-129">Līdzekļu pārvaldības darbvieta</span><span class="sxs-lookup"><span data-stu-id="55ea0-129">Feature management workspace</span></span>

<span data-ttu-id="55ea0-130">Katrā laidienā tiek pievienoti un atjaunināti līdzekļi.</span><span class="sxs-lookup"><span data-stu-id="55ea0-130">Features are added and updated in every release.</span></span> <span data-ttu-id="55ea0-131">Līdzekļu pārvaldības pieredze nodrošina darbvietu, kur varat skatīt katrā laidienā piegādāto līdzekļu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="55ea0-131">The feature management experience provides a workspace where you can view a list of features that have been delivered in each release.</span></span> <span data-ttu-id="55ea0-132">Pēc noklusējuma jaunie līdzekļi ir izslēgti.</span><span class="sxs-lookup"><span data-stu-id="55ea0-132">By default, new features are turned off.</span></span> <span data-ttu-id="55ea0-133">Varat izmantot darbvietu, lai tos ieslēgtu un skatītu ar tiem saistīto dokumentāciju.</span><span class="sxs-lookup"><span data-stu-id="55ea0-133">You can use the workspace to turn them on and view the documentation for them.</span></span>

<span data-ttu-id="55ea0-134">Lai iegūtu plašāku informāciju par izmaiņām, kas tiek veiktas ar funkciju pārvaldību, skatīt [Funkciju pārvaldības pārskatu](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="55ea0-134">To learn more about the changes coming with feature management, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>
