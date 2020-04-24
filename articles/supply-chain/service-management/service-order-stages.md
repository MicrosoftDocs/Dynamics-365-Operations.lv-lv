---
title: Pakalpojuma pasūtījuma stadijas
description: Definējot pakalpojuma pasūtījuma stadijas un piešķirot tās darbiniekiem, varat kontrolēt pakalpojuma pasūtījuma plūsmu caur uzdevumiem, ko pakalpojumu organizācijā veic dažādi cilvēki.
author: ShylaThompson
manager: tfehr
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable, SMAStageTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b6ab601891faac34db6bc5397b387c126fa1289f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215060"
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

  


