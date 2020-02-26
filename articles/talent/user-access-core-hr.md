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
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2020
ms.locfileid: "3006314"
---
# <a name="user-can-access-human-resources-but-not-onboard-or-attract"></a>Lietotājs var piekļūt Human Resources, bet nevar piekļūt pakalpojumam Onboard vai Attract

[!include [banner](includes/banner.md)]

**Informācija par vidi**

- Microsoft Dynamics Lifecycle Services (LCS) izvietošanu veica lietotājs A.
- Lietotājs A pievienoja lietotāju B kā Microsoft Dynamics 365 Human Resources.

**Izejas plūsma**

Lietot. B var piekļūt Human Resources, bet nevar piekļūt Talent: Attract vai Talent: Onboard. Kad lietotājs mēģina doties uz **Programmu izmantošana**, tā vietā tiek atvērta izmēģinājuma vide.

**Risinājums**

Lietotājam B ir jāpiešķir tiesības skatīt Microsoft Power Apps vidi, kuru lietotājs A izveidoja nodrošināšanas procesa laikā.

Papildinform. skatiet sadaļas [Talent nodrošinājums](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) iedaļā “Piekļuves piešķiršana videi”.

**Ilgterm. risināj.**

Microsoft apsver iespēju automāt. piešķirt atbilstošās tiesības programmām Onboard un Attract, pievienojot lietotāju Human Resources.
