---
title: Lietotājs var piekļūt Human Resources, bet nevar piekļūt pakalpojumam Onboard vai Attract
description: Šajā tēmā paskaidrots, kā atrisināt problēmu, kad lietotājs var piekļūt Microsoft Dynamics 365 Talent — Human Resources, bet nevar piekļūt programmai Attract vai Onboard.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6c384d9a7100982eabd201d910e1bea14355dc1f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461859"
---
# <a name="user-can-access-human-resources-but-not-onboard-or-attract"></a><span data-ttu-id="94fcc-103">Lietotājs var piekļūt Human Resources, bet nevar piekļūt pakalpojumam Onboard vai Attract</span><span class="sxs-lookup"><span data-stu-id="94fcc-103">User can access Human Resources but not Onboard or Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="94fcc-104">**Informācija par vidi**</span><span class="sxs-lookup"><span data-stu-id="94fcc-104">**Environment details**</span></span>

- <span data-ttu-id="94fcc-105">Microsoft Dynamics Lifecycle Services (LCS) izvietošanu veica lietotājs A.</span><span class="sxs-lookup"><span data-stu-id="94fcc-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="94fcc-106">Lietotājs A pievienoja lietotāju B kā Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="94fcc-106">User A added user B as a user to Microsoft Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="94fcc-107">**Izejas plūsma**</span><span class="sxs-lookup"><span data-stu-id="94fcc-107">**Issue**</span></span>

<span data-ttu-id="94fcc-108">Lietot. B var piekļūt Human Resources, bet nevar piekļūt Talent: Attract vai Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="94fcc-108">User B can access Human Resources, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="94fcc-109">Kad lietotājs mēģina doties uz **Programmu izmantošana**, tā vietā tiek atvērta izmēģinājuma vide.</span><span class="sxs-lookup"><span data-stu-id="94fcc-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="94fcc-110">**Risinājums**</span><span class="sxs-lookup"><span data-stu-id="94fcc-110">**Solution**</span></span>

<span data-ttu-id="94fcc-111">Lietotājam B ir jāpiešķir tiesības skatīt Microsoft Power Apps vidi, kuru lietotājs A izveidoja nodrošināšanas procesa laikā.</span><span class="sxs-lookup"><span data-stu-id="94fcc-111">User B must be assigned the rights to view the Microsoft Power Apps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="94fcc-112">Papildinform. skatiet sadaļas [Talent nodrošinājums](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) iedaļā “Piekļuves piešķiršana videi”.</span><span class="sxs-lookup"><span data-stu-id="94fcc-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="94fcc-113">**Ilgterm. risināj.**</span><span class="sxs-lookup"><span data-stu-id="94fcc-113">**Long-term solution**</span></span>

<span data-ttu-id="94fcc-114">Microsoft apsver iespēju automāt. piešķirt atbilstošās tiesības programmām Onboard un Attract, pievienojot lietotāju Human Resources.</span><span class="sxs-lookup"><span data-stu-id="94fcc-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Human Resources.</span></span>
