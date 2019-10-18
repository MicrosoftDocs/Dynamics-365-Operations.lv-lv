---
title: Lietotājs var piekļūt Core HR, bet nevar piekļūt Onboard vai Attract
description: Šajā tēmā paskaidrots, kā atrisināt problēmu, kad lietotājs var piekļūt Microsoft Dynamics 365 Talent — Core HR, bet nevar piekļūt programmai Attract vai Onboard.
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
ms.openlocfilehash: 80b1f8aeabfd033f393463f4be5a61447377f2d9
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/23/2019
ms.locfileid: "2009310"
---
# <a name="user-can-access-core-hr-but-not-onboard-or-attract"></a>Lietotājs var piekļūt Core HR, bet nevar piekļūt Onboard vai Attract

[!include [banner](includes/banner.md)]

**Informācija par vidi**

- Microsoft Dynamics Lifecycle Services (LCS) izvietošanu veica lietotājs A.
- Lietotājs A pievienoja lietotāju B kā Microsoft Dynamics 365 Talent: Core HR.

**Izejas plūsma**

Lietot. B var piekļūt Core HR, bet nevar piekļūt Talent: Attract vai Talent: Onboard. Kad lietotājs mēģina doties uz **Programmu izmantošana**, tā vietā tiek atvērta izmēģinājuma vide.

**Risinājums**

Lietotājam B ir jāpiešķir tiesības skatīt Microsoft PowerApps vidi, kuru lietotājs A izveidoja nodrošināšanas procesa laikā.

Papildinform. skatiet sadaļas [Talent nodrošinājums](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) iedaļā “Piekļuves piešķiršana videi”.

**Ilgterm. risināj.**

Microsoft apsver iespēju automāt. piešķirt atbilstošās tiesības programmām Onboard un Attract, pievienojot lietotāju Core HR.
