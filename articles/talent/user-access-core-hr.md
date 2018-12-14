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

# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a>Lietot. piekļūst Core HR, bet ne progr. Onboard/Attract

[!include [banner](includes/banner.md)]

**Informācija par vidi**

- Microsoft Dynamics Lifecycle Services (LCS) izvietošanu veica lietotājs A.
- Lietot. A pievienoja lietot. B kā Microsoft Dynamics 365 for Talent Core HR lietot.

**Izsniegt**

Lietot. B var piekļūt Core HR, bet nevar piekļūt Talent: Attract vai Talent: Onboard. Kad lietotājs mēģina doties uz **Programmu izmantošana**, tā vietā tiek atvērta izmēģinājuma vide.

**Risinājums**

Lietotājam B ir jāpiešķir tiesības skatīt Microsoft PowerApps vidi, kuru lietotājs A izveidoja nodrošināšanas procesa laikā.

Papildinform. skatiet sadaļas [Talent nodrošinājums](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent) iedaļā “Piekļuves piešķiršana videi”.

**Ilgterm. risināj.**

Microsoft apsver iespēju automāt. piešķirt atbilstošās tiesības programmām Onboard un Attract, pievienojot lietotāju Core HR.

