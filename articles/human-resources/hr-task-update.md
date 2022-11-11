---
title: Uzdevumu iestatīšana uzdevumu pārvaldībā
description: Šajā rakstā skaidrots, kā iestatīt uzdevumus Uzdevumu pārvaldībā Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2022-06-09
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6a38cc2e36c24ddbfe0d8b2886301c108599ab25
ms.sourcegitcommit: 55e440e30490b2d36d86b22aa1263d5da97633aa
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/04/2022
ms.locfileid: "9745422"
---
# <a name="set-up-tasks-in-task-management"></a>Uzdevumu iestatīšana uzdevumu pārvaldībā

[!INCLUDE [PEAP](../includes/peap-1.md)]

Microsoft Dynamics 365 Human Resources versijās pirms versijas 10.0.30 lietotāji, kas vēlējās rediģēt uzdevumu, bija individuāli rediģēt šo uzdevumu katrā kontrolsarakstā, kas to ietver. Tomēr cilvēkresursu versijā 10.0.30 lietotāji var atlasīt, kā tiek apstrādāti labotie uzdevumi. Ja rediģējamais uzdevums ir kontrolsarakstā, **·** **·** **tad cilnes Uzdevumu pārvaldība lapā Cilvēkresursu koplietojamie parametri ir jāatlasa opcija Iespējot uzdevumu pārvaldības jaunināšanu**, lai iespējotu kontrolsaraksta izmantošanu rediģēto uzdevumu.

[![Iespējojiet uzdevumu pārvaldības jaunināšanas opciju lapā Cilvēkresursu kopīgie parametri.](./media/task-update.png)](./media/task-update.png)

Ja uzdevumiem ir jārediģē visi saistītie kontrolsaraksta uzdevumi, jau pastāv saistībai starp uzdevumu bibliotēkā esošo uzdevumu un kontrolsaraksta uzdevumu. Opcija tika pievienota, lai izveidotu attiecības starp bibliotēkas uzdevumu un kontrolsaraksta uzdevumu.

Varat izveidot uzdevumus atsevišķi un pēc tam atkārtoti izmantot tos vairākos kontrolsarakstos. Lai izveidotu uzdevumu, cilnē **Uzdevumi** **cilnē** Iestatījumi atlasiet Jauns.**·**

## <a name="set-up-tasks"></a>Uzdevumu iestatīšana

Lai piešķirtu izveidoto uzdevumu vairākiem kontrolsarakstam, atlasiet uzdevumu un pēc tam izvēlnē atlasiet **Lietot kontrolsarakstam**.

Alternatīvi uzdevumus var pievienot tieši kontrolsarakstā. Lai kontrolsarakstam pievienotu uzdevumu, **iestatījumu lapas Onboarding** **iestatījums** cilnē Kontrolsaraksts izveidojiet jaunu kontrolsarakstu, lai pievienotu uzdevumu esošajam kontrolsarakstam vai pievienotu to esošajam kontrolsarakstam.

Lai rediģētu bibliotēkas uzdevumu, uzdevumu **bibliotēkas** izvēlnē atlasiet Rediģēt. Ja uzdevums ir saistīts ar kontrolsarakstu, šie kontrolsaraksti tiks parādīti uzdevumu **lapas Rediģēt**. Ja vēlaties, lai uzdevumi jebkurā kontrolsarakstā tiktu atjaunināti ar labojumiem, atlasiet šos kontrolsarakstus **sadaļā Lietot kontrolsaraksta**.

Lai dzēstu uzdevumus no uzdevumu bibliotēkas, atlasiet **Dzēst**. Ja uzdevums ir saistīts ar kontrolsarakstu, šī darbība nedzēš uzdevumu no kontrolsaraksta. Lai uzdevumu izņemtu no kontrolsaraksta, ir nepieciešama atsevišķa darbība.

### <a name="set-up-checklists"></a>Iestatīt kontrolsarakstus

Kontrolsaraksts ir uzdevumu grupa. Varat izveidot tik daudz kontrolsarakstu, cik nepieciešams, un jūs variet piešķirt tos pašus uzdevumus vairākiem kontrolsarakstam. Veidojot kontrolsarakstu, norādiet īpašnieku un kalendāru.

Lai kontrolsarakstā izveidotu jaunu uzdevumu, uzdevumu **izvēlnes** joslā atlasiet Jauns. Veidojot jaunu uzdevumu, varat uzdevumu bibliotēkai pievienot šo uzdevumu pēc izvēles, lai to varētu koplietot vairākos kontrolsarakstos. Lai uzdevumu bibliotēkai pievienotu uzdevumu, opcijai Lietot **uzdevumu bibliotēkai ir jāiestata** opcija **Jā**. Ja izvēlaties pievienot uzdevumu uzdevumu bibliotēkai, varat pievienot uzdevumu citiem kontrolsarakstam vienlaicīgi, atlasot šos kontrolsarakstus **sadaļā Lietot kontrolsarakstam**. Ja izvēlaties ne pievienot uzdevumu uzdevumu bibliotēkai, uzdevums būs vienīgi kontrolsarakstā, kur to izveidojat.

Lai kontrolsarakstā rediģētu uzdevumu, uzdevumu **izvēlnē** atlasiet Rediģēt. Ja uzdevums ir saistīts ar kontrolsarakstu, šie kontrolsaraksti tiks parādīti uzdevumu **lapas Rediģēt**. Ja vēlaties, lai uzdevumi jebkurā citā kontrolsarakstā tiktu atjaunināti ar labojumiem, atlasiet šos kontrolsarakstus sadaļā Lietot **kontrolsaraksta**.

Lai noņemtu uzdevumus no kontrolsaraksta, atlasiet **Noņemt**. Ar šo darbību uzdevumi tiks noņemti no kontrolsaraksta. Tomēr uzdevumi netiks dzēsti uzdevumu bibliotēkā. Lai dzēstu uzdevumus no uzdevumu bibliotēkas, atveriet uzdevumu **bibliotēkas** lapu un atlasiet **Dzēst**.
