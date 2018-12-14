---
title: "Lietot. piekļūst Core HR, bet ne progr. Onboard/Attract"
description: "Šajā tēmā paskaidrots, kā atrisināt probl., kad lietot. var piekļūt Microsoft Dynamics 365 for Talent Core HR, bet nevar piekļūt progr. Attract vai Onboard."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 2e5d0b1bf993aec89c7d2c6d4916732f5824310d
ms.contentlocale: lv-lv
ms.lasthandoff: 12/04/2018

---

# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a><span data-ttu-id="7c74e-103">Lietot. piekļūst Core HR, bet ne progr. Onboard/Attract</span><span class="sxs-lookup"><span data-stu-id="7c74e-103">User can access Core HR but not the Onboard or Attract app</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7c74e-104">**Informācija par vidi**</span><span class="sxs-lookup"><span data-stu-id="7c74e-104">**Environment details**</span></span>

- <span data-ttu-id="7c74e-105">Microsoft Dynamics Lifecycle Services (LCS) izvietošanu veica lietotājs A.</span><span class="sxs-lookup"><span data-stu-id="7c74e-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="7c74e-106">Lietot. A pievienoja lietot. B kā Microsoft Dynamics 365 for Talent Core HR lietot.</span><span class="sxs-lookup"><span data-stu-id="7c74e-106">User A added user B as a user to Microsoft Dynamics 365 for Talent Core HR.</span></span>

<span data-ttu-id="7c74e-107">**Izsniegt**</span><span class="sxs-lookup"><span data-stu-id="7c74e-107">**Issue**</span></span>

<span data-ttu-id="7c74e-108">Lietot. B var piekļūt Core HR, bet nevar piekļūt Talent: Attract vai Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="7c74e-108">User B can access Core HR, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="7c74e-109">Kad lietotājs mēģina doties uz **Programmu izmantošana**, tā vietā tiek atvērta izmēģinājuma vide.</span><span class="sxs-lookup"><span data-stu-id="7c74e-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="7c74e-110">**Risinājums**</span><span class="sxs-lookup"><span data-stu-id="7c74e-110">**Solution**</span></span>

<span data-ttu-id="7c74e-111">Lietotājam B ir jāpiešķir tiesības skatīt Microsoft PowerApps vidi, kuru lietotājs A izveidoja nodrošināšanas procesa laikā.</span><span class="sxs-lookup"><span data-stu-id="7c74e-111">User B must be assigned the rights to view the Microsoft PowerApps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="7c74e-112">Papildinform. skatiet sadaļas [Talent nodrošinājums](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent) iedaļā “Piekļuves piešķiršana videi”.</span><span class="sxs-lookup"><span data-stu-id="7c74e-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="7c74e-113">**Ilgterm. risināj.**</span><span class="sxs-lookup"><span data-stu-id="7c74e-113">**Long-term solution**</span></span>

<span data-ttu-id="7c74e-114">Microsoft apsver iespēju automāt. piešķirt atbilstošās tiesības programmām Onboard un Attract, pievienojot lietotāju Core HR.</span><span class="sxs-lookup"><span data-stu-id="7c74e-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Core HR.</span></span>

