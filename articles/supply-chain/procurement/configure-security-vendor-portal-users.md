---
title: "Kreditoru portāla lietotāja drošība"
description: "Šajā rakstā ir paskaidrots, kā veikt drošības iestatīšanu ārējiem kreditoriem, kuri lieto kreditoru portālu. Šī informācija attiecas tikai uz 2016. februāra un 2016. gada maija Dynamics AX versijām."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserManagement
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 30231
ms.assetid: 3574db17-81c7-4c5a-999b-0098aa0b9cda
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 30836b1851d124abcbc515db3cea696c3c04a203
ms.contentlocale: lv-lv
ms.lasthandoff: 04/13/2018

---

# <a name="vendor-portal-user-security"></a><span data-ttu-id="ae44b-104">Kreditoru portāla lietotāja drošība</span><span class="sxs-lookup"><span data-stu-id="ae44b-104">Vendor portal user security</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="ae44b-105">Šajā rakstā ir paskaidrots, kā veikt drošības iestatīšanu ārējiem kreditoriem, kuri lieto kreditoru portālu.</span><span class="sxs-lookup"><span data-stu-id="ae44b-105">This article explains how to set up security for external vendors who use the Vendor portal.</span></span> <span data-ttu-id="ae44b-106">Šī informācija attiecas tikai uz 2016. februāra un 2016. gada maija Dynamics AX versijām.</span><span class="sxs-lookup"><span data-stu-id="ae44b-106">This information applies only to the February 2016 &amp; May 2016 versions of Dynamics AX.</span></span>

<span data-ttu-id="ae44b-107">Dynamics 365 for Operations versijā 1611 kreditoru portāla funkcionalitāte ir aizstāta ar paplašināto kreditoru sadarbības funkcionalitāti.</span><span class="sxs-lookup"><span data-stu-id="ae44b-107">The Vendor portal functionality has been replaced by extended vendor collaboration functionality in Dynamics 365 for Operations version 1611.</span></span> <span data-ttu-id="ae44b-108">Papildinformāciju par drošības iestatīšanu kreditoru sadarbībai skatiet rakstā [Iestatīt un uzturēt kreditoru sadarbību](set-up-maintain-vendor-collaboration.md).</span><span class="sxs-lookup"><span data-stu-id="ae44b-108">For more information about setting up security for vendor collaboration, see [Set up and maintain vendor collaboration](set-up-maintain-vendor-collaboration.md).</span></span> <span data-ttu-id="ae44b-109">Kreditoru portālā ārējiem kreditoriem ir pieejama ierobežota informācija par pirkšanas pasūtījumiem (PP).</span><span class="sxs-lookup"><span data-stu-id="ae44b-109">The Vendor portal exposes a limited set of information about purchase orders (POs) to external vendors.</span></span> <span data-ttu-id="ae44b-110">Ir svarīgi pareizi iestatīt lietotāja atļaujas kreditoru portālam programmā Microsoft Dynamics AX, lai kreditoriem netiktu netīšam nodrošināta piekļuve papildu informācijai jūsu Dynamics AX instalācijā.</span><span class="sxs-lookup"><span data-stu-id="ae44b-110">It's important that you correctly set up user permissions for the Vendor portal in Microsoft Dynamics AX, so that vendors don't have unintended access to additional information in your Dynamics AX installation.</span></span> <span data-ttu-id="ae44b-111">**Svarīgi:** atšķirībā no citiem lietotājiem, ārējiem kreditoriem nedrīkst būt loma **SystemUser**.</span><span class="sxs-lookup"><span data-stu-id="ae44b-111">**Important:** Unlike other users, external vendors should not have the **SystemUser** role.</span></span> <span data-ttu-id="ae44b-112">Loma **SystemUser** piešķir piekļuvi privilēģiju kopai, kas nav piemērota ārējiem lietotājiem.</span><span class="sxs-lookup"><span data-stu-id="ae44b-112">The **SystemUser** role grants access to a set of privileges that aren't suitable for external users.</span></span>

## <a name="setting-up-a-vendor-portal-user"></a><span data-ttu-id="ae44b-113">Kreditoru portāla lietotāja iestatīšana</span><span class="sxs-lookup"><span data-stu-id="ae44b-113">Setting up a Vendor portal user</span></span>
<span data-ttu-id="ae44b-114">Pirms kādam kreditoru portāla lietotājam izveidot lietotāja kontu, jāiestata kreditors, lai atļautu kreditoru portāla sadarbību.</span><span class="sxs-lookup"><span data-stu-id="ae44b-114">Before you create a user account for someone who will use the Vendor portal, you must set up the vendor to allow for Vendor portal collaboration.</span></span> <span data-ttu-id="ae44b-115">Izmantojiet lauku **Pirkšanas pasūtījuma sadarbība** cilnē **Vispārējā** lapā **Kreditori**.</span><span class="sxs-lookup"><span data-stu-id="ae44b-115">Use the **Purchase order collaboration** field on the **General** tab on the **Vendors** page.</span></span> <span data-ttu-id="ae44b-116">Ārējiem kreditoriem, kuri lieto kreditoru portālu, jābūt šādiem iestatījumiem:</span><span class="sxs-lookup"><span data-stu-id="ae44b-116">External vendors that use the Vendor portal must have the following setup:</span></span>

-   <span data-ttu-id="ae44b-117">Microsoft Azure Active Directory (AAD) lietotāja konts ir jāreģistrē kreditoram Dynamics AX lapā **Lietotāji**.</span><span class="sxs-lookup"><span data-stu-id="ae44b-117">A Microsoft Azure Active Directory (AAD) user account must be registered for the vendor on the **Users** page in Dynamics AX.</span></span>
-   <span data-ttu-id="ae44b-118">Kreditoram ir jābūt drošības lomai **Kreditors (ārējs)**, nevis lomai **SystemUser**.</span><span class="sxs-lookup"><span data-stu-id="ae44b-118">The vendor must have the **Vendor (external)** security role, not the **SystemUser** role.</span></span> <span data-ttu-id="ae44b-119">**Piezīme:** loma **SystemUser** tiek automātiski piešķirta, kad izveidojat jaunu lietotāja kontu programmā Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="ae44b-119">**Note:** The **SystemUser** role is automatically granted when you create a new user account in Dynamics AX.</span></span> <span data-ttu-id="ae44b-120">Tāpēc šī loma ir jānoņem un jāapstiprina saņemtais brīdinājuma ziņojums.</span><span class="sxs-lookup"><span data-stu-id="ae44b-120">Therefore, you must remove that role and acknowledge the warning message that you receive.</span></span>
-   <span data-ttu-id="ae44b-121">Kreditora lietotājam nevajadzētu piešķirt atļauju pievienot papildu laukus no PP tabulām PP skatā.</span><span class="sxs-lookup"><span data-stu-id="ae44b-121">The vendor user should not be granted permission to add additional fields from the PO tables to their view of the PO.</span></span> <span data-ttu-id="ae44b-122">Cilnē **Personalizēšana**, cilnē **Lietotāji** iestatiet lietotājam opciju **Atļaut skaidri izteiktu personalizēšanu** uz **Nē**.</span><span class="sxs-lookup"><span data-stu-id="ae44b-122">On the **Personalization** tab, on the **Users** tab, set the **Explicit personalization allowed** option for the user to **No**.</span></span>
-   <span data-ttu-id="ae44b-123">Lietotāja kontam ir jābūt saistītam ar reģistrētu kontaktpersonu.</span><span class="sxs-lookup"><span data-stu-id="ae44b-123">The user account must be associated with a registered contact person.</span></span> <span data-ttu-id="ae44b-124">Lapā **Lietotāji** izvēlieties kontaktpersonu laukā **Nosaukums**.</span><span class="sxs-lookup"><span data-stu-id="ae44b-124">On the **Users** page, select a contact person in the **Name** field.</span></span> <span data-ttu-id="ae44b-125">Personai, kuru atlasījāt, jābūt lomai **Kontaktpersona** attiecīgajam kreditoram.</span><span class="sxs-lookup"><span data-stu-id="ae44b-125">The person that you select should have the **Contact** role for the relevant vendor.</span></span>

<span data-ttu-id="ae44b-126">Ja viena un tā pati persona pieprasa piekļuvi vairākiem kreditoru kontiem kreditoru portālā (iespējams, dažādām juridiskajām personām), katram šīs personas lietotāja kontam ir jābūt saistītām ar to pašu reģistrēto kontaktpersonu.</span><span class="sxs-lookup"><span data-stu-id="ae44b-126">If the same person requires access to the Vendor portal for multiple vendor accounts (for different legal entities, perhaps), each of that person's user accounts must be associated with the same registered contact person.</span></span> <span data-ttu-id="ae44b-127">Loma **Kreditors (ārējs)** ietver pamata iespējas, kas ir nepieciešamas, lai varētu izmantot funkcionalitāti, kas ir pieejamas kreditoru portālā.</span><span class="sxs-lookup"><span data-stu-id="ae44b-127">The **Vendor (external)** role includes all the basic capabilities that are required in order to use the functionality that is available in the Vendor portal.</span></span> <span data-ttu-id="ae44b-128">Šis iestatījums palīdz garantēt, ka lietotāja interfeiss, ko ārējais lietotājs redz, ir vērsts tikai uz paredzēto scenāriju.</span><span class="sxs-lookup"><span data-stu-id="ae44b-128">This setup helps guarantee that the user interface that the external user sees is focused on the intended scenario only.</span></span>

<a name="see-also"></a><span data-ttu-id="ae44b-129">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="ae44b-129">See also</span></span>
--------

[<span data-ttu-id="ae44b-130">Kreditoru sadarbība</span><span class="sxs-lookup"><span data-stu-id="ae44b-130">Vendor collaboration</span></span>](collaborate-vendors-vendor-portal.md)




