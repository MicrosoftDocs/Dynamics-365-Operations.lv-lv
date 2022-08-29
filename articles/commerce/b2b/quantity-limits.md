---
title: Preču daudzuma ierobežojumu iestatīšana B2B e-komercijas vietnēs
description: Šajā rakstā ir aprakstīts, kā iestatīt preču daudzuma ierobežojumus e-komercijas vietnēm "bizness-biznesam".
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.search.industry: retail
ms.search.form: RetailOperations
ms.openlocfilehash: 76a7ad2c3095d1402ff214dbfee26b344b492681
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275683"
---
# <a name="set-product-quantity-limits-for-b2b-e-commerce-sites"></a>Preču daudzuma ierobežojumu iestatīšana B2B e-komercijas vietnēs

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā iestatīt preču daudzuma ierobežojumus e-komercijas vietnēm "bizness-biznesam".

Lielākajai daļai preču grupēšanu nosaka mērvienība. Grupēšana ietekmē preču pārdošanas veidu. Dažām precēm var būt daudzumu papildu grupēšana. Šī grupēšana nosaka, vai preces var pārdot kā atsevišķas vai daudzkārtējas vienības, un, vai ir jāievēro minimālais vai maksimālais pasūtījuma daudzuma ierobežojums.

Daudzuma ierobežošanas līdzeklis nodrošina, ka minimālie, maksimālie, daudzkārtējie un standarta daudzumi, kas konfigurēti programmā Microsoft Dynamics 365 Commerce (noklusējuma pasūtījuma iestatījumos vai Commerce vietnes veidotāja vietnes iestatījumos), tiek lietoti klientu pasūtījumiem, kas tiek novietoti e-komercijas vietnē. Preces daudzuma ierobežojumi pārdošanas punktam (POS) un zvanu centriem pašlaik netiek atbalstīti.

Daudzi mazumtirgotāji nodrošina iespēju izmantot klientu pasūtījumus (sauktus arī par īpašajiem pasūtījumiem), lai izpildītu dažādas preču un izpildes prasības. Tālāk uzskaitīti daži tipiski scenāriji.

- Klients vēlas, lai noteiktu variantu preces tiktu pārdotas daudzkārtēji.
- Klients preces vēlas saņemt tādā veikalā vai atrašanās vietā, kas atšķiras no veikala vai atrašanās vietas, kur klients šīs preces iegādājās. Tomēr veikalu iepakošanas standarti atšķiras no tiešsaistes pārdošanas sadales iepakošanas standartiem.
- Klients vēlas iegādāties ierobežota izdevuma preci, kam ir piemērots maksimālā daudzuma ierobežojums preces iegādei.

## <a name="turn-on-the-default-order-settings-feature-in-commerce-headquarters"></a>Pasūtījuma noklusējuma iestatījumu līdzekļa ieslēgšana programmā Commerce Headquarters

Pirms varat iestatīt preču daudzuma ierobežojumus, programmā Commerce Headquarters ir jābūt ieslēgtam pasūtījuma noklusējuma iestatījumu līdzeklim.

Lai ieslēgtu pasūtījuma noklusējuma iestatījumu līdzekli, veiciet tālāk norādītās darbības.

1. Dodieties uz **Sistēmas administrēšana \> Darbvietas \> Līdzekļu pārvaldība**.
1. Atrodiet un atlasiet līdzekli **Atbalsts vietnes un pasūtījuma noklusējuma iestatījumiem klienta pasūtījumā**.
1. Labās rūts apakšdaļā atlasiet **Iespējot tūlīt**. 

## <a name="define-quantity-settings"></a>Daudzuma iestatījumu definēšana 

Daudzuma iestatījumus varat definēt lapā **Pasūtījuma noklusējuma iestatījumi**.

Lai definētu daudzuma iestatījumus, veiciet tālāk norādītās darbības. 

1. Dodieties uz Preču **Retail un Commerce \> Preces un kategorijas \> Izpildei nodotās preces pēc kategorijas**.
1. Atlasiet izlaisto preci.
1. Darbību rūts cilnē **Pārvaldīt krājumu** grupā **Pasūtījuma iestatījumi** atlasiet **Pasūtījuma noklusējuma iestatījumi**. 
1. Lapas **Pasūtījuma noklusējuma iestatījumi** kopsavilkuma cilnē **Pārdošanas pasūtījums** sadaļā **Pārdošanas daudzums** iestatiet preces pārdošanas daudzumu:

    - **Daudzkārtēji** – daudzums, kādā preces var iegādāties daudzkārtīgi.
    - **Minimālais pasūtījuma daudzums** – minimālais iegādājamo preču skaits.
    - **Maksimālais pasūtījuma daudzums** – maksimālais iegādājamo preču skaits.
    - **Standarta pasūtījuma daudzums** – noklusējuma daudzums, kas tiek ievadīts automātiski, kad produkts ir atlasīts.

## <a name="turn-on-the-b2b-order-quantity-limits-feature-in-commerce-site-builder"></a>Commerce vietnes veidotājā ieslēgšana B2B pasūtījuma daudzuma ierobežošanas līdzeklim

Lai ieslēgtu Commerce vietnes veidotāju B2B pasūtījuma daudzuma ierobežošanas līdzeklim, veiciet tālāk norādītās darbības.

1. Dodieties uz **Vietnes iestatījumi \> Paplašinājumi**
1. Zem sadaļas **Pasūtījuma daudzuma ierobežošanas iespējošana** atlasiet **Iespējot B2B klientiem** nolaižamajā izvēlnē. 

> [!NOTE] 
> Atjauninātā vietnes veidotāja iestatījumi stājas spēkā tikai pēc app.settings.json faila atjaunināšanas. Papildinformāciju skatiet [SDK un moduļu bibliotēkas atjauninājumi](../e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).

## <a name="additional-resources"></a>Papildu resursi

[B2B e-komercijas vietnes iestatīšana](set-up-b2b-site.md)

[B2B biznesa partneru pārvaldība, izmantojot debitoru hierarhijas](partners-customer-hierarchies.md)

[Biznesa partnera lietotāju pārvaldība B2B e-komercijas vietnēs](manage-b2b-users.md)

[Klienta konta maksājuma metodes konfigurēšana B2B e-komercijas vietnēs](payment-method.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
