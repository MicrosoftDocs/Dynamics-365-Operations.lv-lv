---
title: Pakalpojuma pasūtījuma stadijas
description: Definējot pakalpojuma pasūtījuma stadijas un piešķirot tās darbiniekiem, varat kontrolēt pakalpojuma pasūtījuma plūsmu caur uzdevumiem, ko pakalpojumu organizācijā veic dažādi cilvēki.
author: ShylaThompson
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAStageTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6ef52171efd422fdbd8593af4c2a5fd968dac1209ddff6cb695e22534a94678b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6711619"
---
# <a name="service-order-stages"></a>Pakalpojuma pasūtījuma stadijas   

[!include [banner](../includes/banner.md)]


Varat iestatīt stadijas pakalpojuma pasūtījumam, lai definētu veicamos uzdevumus, to veikšanas secību un darbiniekus, kuri ir atbildīgi par to izpildīšanu. Definējot pakalpojuma pasūtījuma stadijas un piešķirot tās darbiniekiem, jūs kontrolējat pakalpojuma pasūtījuma plūsmu caur uzdevumiem, ko pakalpojumu organizācijā veic dažādi cilvēki. Stadiju secībā ir jābūt ietvertai sākotnējai stadijai.

Varat arī noteikt darbības, kuras ir atļautas katrā stadijā. Piemēram, ja noņemat atzīmi izvēles rūtiņai **Publicēt** visām stadijām, izņemot pēdējo, jūs novēršat iespēju, ka kāds no pakalpojuma pasūtījumiem tiks grāmatots pirms tam, kad šim pakalpojuma pasūtījumam ir izpildīta visa stadiju secība.

## <a name="branching-in-service-order-stages"></a>Zarošana pakalpojuma pasūtījuma stadijās

Iestatot pakalpojuma posmu, var izveidot vairākas opcijas vai zarus, lai tos atlasītu nākamajā pakalpojuma posmā. Visus zarus, ko izveidojat, var atlasīt, kad ir pabeigts sākotnējais posms. Piemēram, kā sākotnējo posmu varat iestatīt **Plānošanu**. Izveidojiet divus posmus ar nosaukumu **Procesā** un **Atcelt** un pēc tam atlasiet tiem **Plānošanu** kā pamatposmu. Piešķiriet **Plānošanas** posmu pārdošanas pasūtījumam. Ja plānošanas stadija pārdošanas pasūtījumam ir pabeigta, varat atlasīt posmu **Procesā**, ja pārdošanas pasūtījums ir gatavs darbam, vai atlasīt posmu **Atcelt**, ja pārdošanas pasūtījums ir atcelts.

## <a name="see-also"></a>Skatiet arī

[Pakalpojuma pasūtījuma stadiju iestatīšana](set-up-service-order-stages.md)

[Pakalpojuma pasūtījuma stadijas maiņa](change-service-order-stage.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]