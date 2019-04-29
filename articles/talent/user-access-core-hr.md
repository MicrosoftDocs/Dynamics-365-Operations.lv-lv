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
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/19/2019
ms.locfileid: "855660"
---
# <a name="user-can-access-core-hr-but-not-the-onboard-or-attract-app"></a>Lietotājs var piekļūt Core HR, bet nevar piekļūt programmai Onboard vai Attract

[!include [banner](includes/banner.md)]

**Informācija par vidi**

- Microsoft Dynamics Lifecycle Services (LCS) izvietošanu veica lietotājs A.
- Lietotājs A pievienoja lietotāju B kā Microsoft Dynamics 365 for Talent Core HR lietotāju.

**Problēma**

Lietot. B var piekļūt Core HR, bet nevar piekļūt Talent: Attract vai Talent: Onboard. Kad lietotājs mēģina doties uz **Programmu izmantošana**, tā vietā tiek atvērta izmēģinājuma vide.

**Risinājums**

Lietotājam B ir jāpiešķir tiesības skatīt Microsoft PowerApps vidi, kuru lietotājs A izveidoja nodrošināšanas procesa laikā.

Papildinform. skatiet sadaļas [Talent nodrošinājums](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent) iedaļā “Piekļuves piešķiršana videi”.

**Ilgterm. risināj.**

Microsoft apsver iespēju automāt. piešķirt atbilstošās tiesības programmām Onboard un Attract, pievienojot lietotāju Core HR.
