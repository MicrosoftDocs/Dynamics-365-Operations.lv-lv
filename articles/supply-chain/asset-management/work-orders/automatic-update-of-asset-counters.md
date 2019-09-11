---
title: Līdzekļu skaitītāju automātiska atjaunināšana
description: Šajā tēmā aprakstīta automātiska līdzekļu skaitītāju atjaunināšana programmā Asset Management.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 97e6912cd37d6f82d8bf022141f04645a3364ee1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875784"
---
# <a name="automatic-update-of-asset-counters"></a>Līdzekļu skaitītāju automātiska atjaunināšana

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Iepriekšējā nodaļā aprakstīta manuāla līdzekļu skaitītāju atjaunināšana. Līdzekļu skaitītāju iestatīšana ir aprakstīta [Skaitītāji](../setup-for-objects/counters.md).

Skaitītāju vērtības var arī automātiski atjaunināt no produktu reģistrācijas, balstoties uz ražošanas stundām vai ražoto daudzumu. Tas tiek darīts sadaļā **Atjaunināt līdzekļu skaitītājus**. Var atjaunināt vienu vai vairākus līdzekļus, ievietojot vienu parametru **Datums no**. Šis parametrs norāda ražošanas reģistrāciju sākuma datumu (stundas vai saražoto daudzumu), tas ir, sākuma datumu, no kura jāatjaunina skaitītāja vērtības.

Visi līdzekļi, kas saistīti ar resursu *un* kam ir līdzekļu skaitītāji, kas iestatīti atjaunošanai, balstoties uz saražoto daudzumu vai ražošanas stundām, tiks iekļauti automātiskā atjauninājumā, un tiks izveidotas jaunas skaitītāja vērtības.

Attiecībā uz skaitītājiem, kas balstīti uz ražošanas daudzumu, skaitā ir iekļauts reģistrēto labas kvalitātes preču un bojāto preču daudzums. Ja saražotā daudzuma reģistrācijai lietotā vienība atšķiras no skaitītajā izmantotās vienības, daudzums tiek pārveidots, lai atbilstu skaitītāja vienībai.

Kā minēts iepriekš, automātisko skaitītāju vērtības var arī atjaunināt no produktu reģistrācijas. Tādēļ līdzeklim, kam vēlaties automātiski atjaunināt skaitītājus, jābūt saistītam ar resursu (mašīnu). Šie paskaidrojumi sniedz pārskatu par ražošanas pasūtījumu iestatīšanu un apstrādi (modulī **Ražošanas kontrole**), kas tiek izmantots kā pamats skaitītāju automātiskai atjaunināšanai modulī **Līdzekļu pārvaldība**.

Kad saražotie daudzumi vai ražošanas stundas reģistrētas resursam, varat atjaunināt saistītos līdzekļu skaitītājus.

1. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Periodiski** > **Līdzekļi** > **Līdzekļu skaitītāju atjaunināšana**.

2. Laukā **No datums** atlasiet automātiskā atjauninājuma sākuma datumu.

>[!NOTE]
>Datums šajā laukā ir "notiek darbs" datums no **Maršruta darījumi** (**Ražošanas kontrole** > **Pieprasījumi un atskaites** > **Ražošana** > **Maršruta darījumi** > **Fiziskais datums** laukā).

3. Ja vēlaties atlasīt konkrētus līdzekļus, līdzekļu veidus vai resursus automātiskam atjauninājumam, kopsavilkuma cilnē **Iekļaujamie ieraksti** noklikšķiniet uz **Filtrēt** un atlasiet attiecīgi.

4. Ja nepieciešams, jūs varat ātrajā cilnē **Palaist fonā** uzstādīt automātisku atjauninājumu kā pakešuzdevumu.

![1. attēls](media/12-work-orders.png)

5. Noklikšķiniet uz **Labi**. Kad notikusi automātiska līdzekļu skaitītāja atjaunināšana, varat redzēt ar līdzekli saistītās skaitītāja reģistrācijas sadaļā **Līdzekļu skaitītāji** (**Līdzekļu pārvaldība** > **Vispārīgi** > **Līdzekļi** > **Visi līdzekļi** > Atlasīt līdzekli > **Skaitītāji** poga).

Sarakstā **Līdzekļu skaitītāju kopsummas** ir pārskats par jaunākajām reģistrācijām visiem skaitītāju veidiem visiem līdzekļiem. Noklikšķiniet uz **Līdzekļu pārvaldība** > **Pieprasījumi** > **Līdzekļi** > **Līdzekļu apkopotā vērtība**. Skats ir ļoti līdzīgs **Līdzekļu skaitītājam**, bet jūs nevarat pievienot vai rediģēt reģistrācijas **Līdzekļu apkopotajā vērtībā**. Tas ir tikai pārskatam.

![2. attēls](media/13-work-orders.png)


- Joprojām ir iespējams veidot manuālas skaitītāja vērtības reģistrācijas skaitītāju veidiem, kas tiek automātiski atjaunināti. Skatiet sadaļu „Manuāla līdzekļu skaitītāju atjaunināšana”, kur ir vairāk informācijas.
- Varat iestatīt skaitītājus, kas saistīti ar citu skaitītāju, kas nozīmē, ka, kad tiek atjaunināts skaitītājs, vienlaicīgi tiek automātiski atjaunināti saistītie skaitītāji. Skatiet tēmu [Skaitītāji](../setup-for-objects/counters.md) attiecībā uz saistīto skaitītāju iestatīšanu.
