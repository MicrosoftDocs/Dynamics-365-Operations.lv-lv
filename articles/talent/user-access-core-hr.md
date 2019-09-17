---
title: Lietot. piekļūst Core HR, bet ne progr. Onboard/Attract
description: Šajā tēmā paskaidrots, kā atrisināt problēmu, kad lietotājs var piekļūt Microsoft Dynamics 365 for Talent Core HR, bet nevar piekļūt programmai Attract vai Onboard.
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
ms.openlocfilehash: 6fc27a4c137fef2f8d204d90366c316389da08e6
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741725"
---
# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a><span data-ttu-id="f8d83-103">Lietotājs var piekļūt Core HR, bet nevar piekļūt programmai Onboard vai Attract</span><span class="sxs-lookup"><span data-stu-id="f8d83-103">User can access Core HR but not the Onboard or Attract app</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f8d83-104">**Informācija par vidi**</span><span class="sxs-lookup"><span data-stu-id="f8d83-104">**Environment details**</span></span>

- <span data-ttu-id="f8d83-105">Microsoft Dynamics Lifecycle Services (LCS) izvietošanu veica lietotājs A.</span><span class="sxs-lookup"><span data-stu-id="f8d83-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="f8d83-106">Lietotājs A pievienoja lietotāju B kā Microsoft Dynamics 365 for Talent Core HR lietotāju.</span><span class="sxs-lookup"><span data-stu-id="f8d83-106">User A added user B as a user to Microsoft Dynamics 365 for Talent Core HR.</span></span>

<span data-ttu-id="f8d83-107">**Problēma**</span><span class="sxs-lookup"><span data-stu-id="f8d83-107">**Issue**</span></span>

<span data-ttu-id="f8d83-108">Lietot. B var piekļūt Core HR, bet nevar piekļūt Talent: Attract vai Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="f8d83-108">User B can access Core HR, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="f8d83-109">Kad lietotājs mēģina doties uz **Programmu izmantošana**, tā vietā tiek atvērta izmēģinājuma vide.</span><span class="sxs-lookup"><span data-stu-id="f8d83-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="f8d83-110">**Risinājums**</span><span class="sxs-lookup"><span data-stu-id="f8d83-110">**Solution**</span></span>

<span data-ttu-id="f8d83-111">Lietotājam B ir jāpiešķir tiesības skatīt Microsoft PowerApps vidi, kuru lietotājs A izveidoja nodrošināšanas procesa laikā.</span><span class="sxs-lookup"><span data-stu-id="f8d83-111">User B must be assigned the rights to view the Microsoft PowerApps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="f8d83-112">Papildinform. skatiet sadaļas [Talent nodrošinājums](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) iedaļā “Piekļuves piešķiršana videi”.</span><span class="sxs-lookup"><span data-stu-id="f8d83-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="f8d83-113">**Ilgterm. risināj.**</span><span class="sxs-lookup"><span data-stu-id="f8d83-113">**Long-term solution**</span></span>

<span data-ttu-id="f8d83-114">Microsoft apsver iespēju automāt. piešķirt atbilstošās tiesības programmām Onboard un Attract, pievienojot lietotāju Core HR.</span><span class="sxs-lookup"><span data-stu-id="f8d83-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Core HR.</span></span>
