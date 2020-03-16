---
title: Preču ieteikumi POS
description: Šajā tēmā ir aprakstīts, kā lietot preču ieteikumus pārdošanas punkta (POS) ierīcē.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: bfb13904b774558907b29e74158b1e0a193e17cd
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057445"
---
# <a name="product-recommendations-on-pos"></a>Preču ieteikumi punktā POS

[!include [banner](includes/banner.md)]

To pašos pamatos, preču ieteikumi ir transformējoša biznesa programma, kas aptver visas komercijas vietas, lai izveidotu bagātīgu, saistošu un pielāgotu preču atklāšanas pieredzi. Lai šo funkciju ieviestu POS, izpildiet norādījumus [kā pievienot ieteikumus jūsu POS ierīcēm.](add-recommendations-control-pos-screen.md) 

Lai iegūtu vairāk informācijas par preču ieteikumu līdzekļiem, lasiet [preču ieteikumu pārskats.](../commerce/product-recommendations.md) 

## <a name="scenarios"></a>Scenāriji

Preču ieteikumi ir iespējoti tālāk norādītajos POS scenārijos. Tie ir pieejami programmā Cloud POS vai Modern POS (MPOS).

1. Lapā **Detalizēta informācija par preci**.

    - Ja veikala darbinieks apmeklē lapu **Detalizēta informācija par preci**, skatot iepriekšējās transakcijas dažādos kanālos, ieteikumu serviss piedāvā papildu preces, kas var tikt nopirktas kopā.

    [![Ieteikumi lapā Informācija par preci](./media/proddetails.png)](./media/proddetails.png)

2. Lapā **Transakcija**.

    - Ieteikumu programma iesaka preces, kuras bieži pērk kopā, pamatojoties uz visu grozam pievienoto preču sarakstu.

    > [!NOTE]
    > Lai lapā **Transakcija** tiktu rādīti ieteikumi, mazumtirgotājam ir jāatjaunina ekrāna izkārtojums programmā Dynamics 365 Commerce. Lapā **Transakcijas** ir jāaktivizē vadīkla **Ieteikumi** lapā.

    [![Ieteikumi lapā Transakcija](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

## <a name="configure-commerce-to-enable-pos-recommendations"></a>Commerce konfigurēšana, lai iespējotu POS ieteikumus

Lai iestatītu preču ieteikumus, rīkojieties šādi:

1. Pārliecinieties, ka jūsu serviss ir atjaunināts uz **10.0.6 būvējumu.**
2. Sekojiet instrukcijām, kā [iespējot produktu ieteikumus](../commerce/enable-product-recommendations.md) jūsu biznesam.
3. Pēc izvēles. Lai transakciju ekrānā tiktu rādīti ieteikumi, pārejiet uz sadaļu **Ekrāna izkārtojums**, izvēlieties savu ekrāna izkārtojumu, palaidiet līdzekli **Ekrāna izkārtojuma dizainers** un pēc tam aktivizējiet vadīklu **ieteikumi**, kur nepieciešams.
4. Pārejiet uz sadaļu **Commerce parametri**, atlasiet vienumu **Algoritmiskā mācīšanās** un sadaļā **Iespējot POS ieteikumus** atlasiet vienumu **Jā**.
5. Lai POS tiktu rādīti ieteikumi, palaidiet globālās konfigurācijas darbu Nr. **1110**. Lai atainotu POS ekrāna izkārtojuma dizainerī veiktās izmaiņas, palaidiet kanāla konfigurācijas darbu Nr. **1070**.

## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a>Problēmu novēršana, ja preču ieteikumi jau ir iespējoti

- Pārejiet uz **Commerce parametri** \> **Ieteikumu saraksti** \> **Atspējot preču ieteikumus** un palaidiet darbu **Globālais konfigurācijas darbs \[9999\]**. 
- Ja darbību ekrānam pievienojāt vadīklu **Ieteikumus pārvaldība**, izmantojot **Ekrāna izkārtojuma dizainers**, lūdzu, noņemiet arī to.
- Ja jums ir papildu jautājumi, skatiet [Bieži uzdotos jautājumus par preču ieteikumiem](../commerce/faq-recommendations.md), lai iegūtu vairāk informācijas.

## <a name="additional-resources"></a>Papildu resursi

[Ieteikumu vadīklas pievienošana POS ierīču transakciju ekrānam](add-recommendations-control-pos-screen.md)

[Preču ieteikumu apskats](../commerce/product-recommendations.md)

[Preču ieteikumu iespējošana](../commerce/enable-product-recommendations.md) 
