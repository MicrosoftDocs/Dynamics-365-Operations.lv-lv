---
title: Izmēģināt mēroga vienības sadalītajā hibrīdajā topoloģijā
description: Šajā rakstā ir sniegta informācija, kā izmēģināt mākoņa un malas apjoma vienības ražošanas un noliktavas pārvaldības darba noslodzei.
author: perlynne
ms.date: 05/02/2022
ms.topic: article
ms.search.form: ScaleUnitWorkloadsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-03-03
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 5645955109e7a942e617b3b90a27065c2a8fe4a3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893589"
---
# <a name="try-out-scale-units-in-a-distributed-hybrid-topology"></a>Izmēģināt mēroga vienības sadalītajā hibrīdajā topoloģijā

[!include [banner](../includes/banner.md)]

Dalītās topoloģijas izmēģinšanas process ir vienkāršs. Pirmajā posmā jums ir jāpārbauda pielāgojumi, lai nodrošinātu, ka tie darbojas sadalītā topoloģijā. Ir divas opcijas.

## <a name="option-1-evaluate-customizations-in-development-environments"></a>1. opcija: pielāgošanas vērtējiet izstrādes vidēs

Pirms sākat darbu ar kastu vidēm, ieteicams izstrādes iestatījumos izpētīt mēroga vienības, piemēram, vienlodziņa vidē (ko sauc arī par 1. pakāpes vidi), lai varētu validēt procesus, pielāgojumus un risinājumus. Šā posma laikā dati un pielāgojumi tiks pielietoti vienas kastes vidēm. Jūs varat darboties vienā vidē, kurai var būt gan uzņēmuma pārkraušanas centra, gan mēroga vienības loma. Alternatīvi var būt divas izstrādes vides, no kurām viena veic pārkraušanas centra lomu, un otrai no tām ir loma mēroga vienībā. Šis iestatījums nodrošina labāko veidu, kā identificēt un risināt problēmas. Jaunāko priekšskatījuma [būvējumu](../../fin-ops-core/fin-ops/get-started/one-version.md#how-can-i-get-early-access-to-non-released-platform-updates) var izmantot arī šīs stadijas pabeigšanai.

Lai instalētu un uzturētu [vides, jums jāizmanto mēroga vienību izvietošanas rīki vienas kastes](https://github.com/microsoft/SCMScaleUnitDevTools) izstrādes vidēm. Izmantojot šos rīkus, varat konfigurēt pārkraušanas centra un mēroga vienības vienā vai divos lodziņa vidēs. Rīki tiek nodrošināti kā binārais laidiens un GitHub avota kods. No jauna izpētiet projekta to, kurā iekļauta [pakāpeniskas lietošanas rokasgrāmata](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide), kurā aprakstīts, kā izmantot rīkus. Ja pielāgotajā aparatūru [izvietojat malu skalas vienības, izmantojot vietējos biznesa datus (LBD),](cloud-edge-edge-scale-units-lbd.md) jums jāatbilst dažādiem procesiem.

## <a name="option-2-acquire-add-ins-and-deploy-in-your-sandbox-environments"></a>2. opcija: pievienojumprogrammu ieguve un izvietošana jūsu kastēs vidēs

Lai mēģinātu izplatīto topoloģiju, ir jābūt divām kastu vidēm (2. pakāpe), no kurām vienai ir jūsu dati (uzņēmuma pārkraušanas punkts), bet otrai ir jābūt mēroga vienībai un ir "tukši dati".

Ir jāiegūst pievienojumprogrammas vismaz vienai mākoņa vai malas mēroga vienībai. Pēc tam atbilstošie projekta un vides sloti tiks piešķirti pakalpojumos [Microsoft Dynamics](https://lcs.dynamics.com/) Lifecycle Services (LCS), [lai mēroga vienību vides varētu izvietot, izmantojot mēroga vienību pārvaldnieka portālu](https://aka.ms/SCMSUM).

Sazinieties ar Microsoft atbalsta dienestu, lai pieprasītu kases vides iespējošanu.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
