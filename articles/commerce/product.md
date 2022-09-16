---
title: Preču ieteikumu pievienošana programmā POS
description: Šajā rakstā ir aprakstīta produktu ieteikumus izmantošana pārdošanas punkta (POS) ierīcē.
author: bebeale
ms.date: 09/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 170e2bf18aefc79a796620818c7100ff8e6e689a
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460061"
---
# <a name="add-product-recommendations-on-pos"></a>Pievienot preču ieteikumi punktā POS

[!include [banner](includes/banner.md)]

To pašos pamatos, preču ieteikumi ir transformējoša biznesa programma, kas aptver visas komercijas vietas, lai izveidotu bagātīgu, saistošu un pielāgotu preču atklāšanas pieredzi. Lai šo funkciju ieviestu POS, izpildiet norādījumus [kā pievienot ieteikumus jūsu POS ierīcēm.](add-recommendations-control-pos-screen.md) 

Lai iegūtu vairāk informācijas par preču ieteikumu līdzekļiem, lasiet [preču ieteikumu pārskats.](../commerce/product-recommendations.md) 

## <a name="scenarios"></a>Scenāriji

Preču ieteikumi ir iespējoti tālāk norādītajos POS scenārijos. Tie ir pieejami programmā Cloud POS vai Modern POS (MPOS).

1. Lapā **Detalizēta informācija par preci**.

    - Ja ar veikalu **tiek** apmeklēta lapa Detalizēta informācija par preci, kad tas meklē iepriekšējās darbības dažādos kanālos, rekomendāciju pakalpojums iesaka papildu krājumus, kas, iespējams, tiks iegādāti kopā. Papildus personalizētiem rekomendācijām lietotājiem ar agrāku pirkšanas vēsturi, atkarībā no pakalpojuma pievienojumdatiem var rādīt līdzīgus veikala izskatus un **līdzīgus** **veikala** aprakstu ieteikumus.

    [![Ieteikumi lapā Informācija par preci.](./media/proddetails.png)](./media/proddetails.png)

2. Lapā **Transakcija**.

    - Ieteikumu programma iesaka preces, kuras bieži pērk kopā, pamatojoties uz visu grozam pievienoto preču sarakstu.

    > [!NOTE]
    > Lai lapā **Transakcija** tiktu rādīti ieteikumi, mazumtirgotājam ir jāatjaunina ekrāna izkārtojums programmā Dynamics 365 Commerce. Lapā **Transakcijas** ir jāaktivizē vadīkla **Ieteikumi** lapā.

    [![Ieteikumi lapā Transakcija.](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

## <a name="configure-commerce-to-enable-pos-recommendations"></a>Commerce konfigurēšana, lai iespējotu POS ieteikumus 

Lai iestatītu produktu ieteikumus, apstipriniet, ka esat pabeiguši nodrošinājuma procesu Commerce produktu rekomendācijām, izpildot Darbības, kas sadaļā [Iespējot preces ieteikumus](../commerce/enable-product-recommendations.md). Pēc noklusējuma ieteikumi tiek parādīti **gan** **lapā** Detalizēta informācija par preci, gan lapā Detalizēta informācija par debitoru, pēc tam, kad esiet pabeidzis (-usi) nodrošinājuma soļus, un dati ir veiksmīgi apstrādāti. 

## <a name="add-recommendations-to-the-transaction-screen"></a>Ieteikumu pievienošana darījumu ekrānam

1. Lai darbības ekrānam pievienotu ieteikumus, sekojiet soļiem [Sadaļā Pievienot ieteikumus darbības ekrānam](add-recommendations-control-pos-screen.md).
1. Lai atspoguļotu POS ekrāna izkārtojuma veidotājā veiktās izmaiņas, izpildiet kanāla konfigurācijas darbu **1070 programmā** Commerce Headquarters.

> [!NOTE] 
> Ja vēlaties iespējot POS ieteikumus, izmantojot Komatu atdalāmo vērtību (CSV) failu, pirms izkārtojuma pārvaldnieka konfigurēšanas Lifecycle Services (LCS) līdzekļu bibliotēkā ir jāizvieto CSV Microsoft Dynamics fails. Ja izmantojat CSV failu RecoMock, nav jāiespējo rekomendācijas. CSV fails ir pieejams tikai demonstrācijas nolūkiem. Debitoriem vai risinājumu arhitektiem ir ieteicams migrēt rekomendāciju sarakstu izskatu demonstrācijas nolūkiem bez nepieciešamības iegādāties noliktavas papildu vienību (NV).

## <a name="additional-resources"></a>Papildu resursi

[Preču ieteikumu apskats](product-recommendations.md)

[Iespējojiet Azure Data Lake Storage pakalpojuma Dynamics 365 Commerce vidē](enable-adls-environment.md)

[Iespējot preču ieteikumus](enable-product-recommendations.md)

[Personalizētu ieteikumu iespējošana](personalized-recommendations.md)

[Atteikšanās no personalizētiem ieteikumiem](personalization-gdpr.md)

[Iespējot "veikala līdzīgie izskati" rekomendācijas](shop-similar-looks.md)

[Ieteikumu pievienošana transakciju ekrānam](add-recommendations-control-pos-screen.md)

[AI-ML ieteikumu rezultātu pielāgošana](modify-product-recommendation-results.md)

[Manuāli izveidot pārraudzītus ieteikumus](create-editorial-recommendation-lists.md)

[Izveidot ieteikumus ar demonstrācijas datiem](product-recommendations-demo-data.md)

[Bieži uzdotie jautājumi par preču ieteikumiem](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
