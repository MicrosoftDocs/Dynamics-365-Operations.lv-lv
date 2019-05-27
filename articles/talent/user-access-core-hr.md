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
ms.openlocfilehash: ece6a81c54ef1421284fc79ab82ed3e31a972255
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518570"
---
# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a><span data-ttu-id="33ba5-103">Lietotājs var piekļūt Core HR, bet nevar piekļūt programmai Onboard vai Attract</span><span class="sxs-lookup"><span data-stu-id="33ba5-103">User can access Core HR but not the Onboard or Attract app</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="33ba5-104">**Informācija par vidi**</span><span class="sxs-lookup"><span data-stu-id="33ba5-104">**Environment details**</span></span>

- <span data-ttu-id="33ba5-105">Microsoft Dynamics Lifecycle Services (LCS) izvietošanu veica lietotājs A.</span><span class="sxs-lookup"><span data-stu-id="33ba5-105">The Microsoft Dynamics Lifecycle Services (LCS) deployment was done by user A.</span></span>
- <span data-ttu-id="33ba5-106">Lietotājs A pievienoja lietotāju B kā Microsoft Dynamics 365 for Talent Core HR lietotāju.</span><span class="sxs-lookup"><span data-stu-id="33ba5-106">User A added user B as a user to Microsoft Dynamics 365 for Talent Core HR.</span></span>

<span data-ttu-id="33ba5-107">**Problēma**</span><span class="sxs-lookup"><span data-stu-id="33ba5-107">**Issue**</span></span>

<span data-ttu-id="33ba5-108">Lietot. B var piekļūt Core HR, bet nevar piekļūt Talent: Attract vai Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="33ba5-108">User B can access Core HR, but can't access the Talent: Attract or Talent: Onboard app.</span></span> <span data-ttu-id="33ba5-109">Kad lietotājs mēģina doties uz **Programmu izmantošana**, tā vietā tiek atvērta izmēģinājuma vide.</span><span class="sxs-lookup"><span data-stu-id="33ba5-109">When the user tries to go to **Experience apps**, he or she is taken to a trial environment instead.</span></span>

<span data-ttu-id="33ba5-110">**Risinājums**</span><span class="sxs-lookup"><span data-stu-id="33ba5-110">**Solution**</span></span>

<span data-ttu-id="33ba5-111">Lietotājam B ir jāpiešķir tiesības skatīt Microsoft PowerApps vidi, kuru lietotājs A izveidoja nodrošināšanas procesa laikā.</span><span class="sxs-lookup"><span data-stu-id="33ba5-111">User B must be assigned the rights to view the Microsoft PowerApps environment that user A created during the provisioning process.</span></span>

<span data-ttu-id="33ba5-112">Papildinform. skatiet sadaļas [Talent nodrošinājums](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent) iedaļā “Piekļuves piešķiršana videi”.</span><span class="sxs-lookup"><span data-stu-id="33ba5-112">For information, see the "Granting access to the environment" section in [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="33ba5-113">**Ilgterm. risināj.**</span><span class="sxs-lookup"><span data-stu-id="33ba5-113">**Long-term solution**</span></span>

<span data-ttu-id="33ba5-114">Microsoft apsver iespēju automāt. piešķirt atbilstošās tiesības programmām Onboard un Attract, pievienojot lietotāju Core HR.</span><span class="sxs-lookup"><span data-stu-id="33ba5-114">Microsoft is considering automatically assigning the appropriate rights to Onboard and Attract when a user is added to Core HR.</span></span>
