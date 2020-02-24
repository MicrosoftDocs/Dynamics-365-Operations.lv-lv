---
title: Bieži uzdotie jautājumi par preču ieteikumiem
description: Šajā tēmā sniegta informācija par procesiem un rīkiem, ko varat izmantot, lai meklētu traucējumus problēmās, kas saistītas ar preču ieteikumiem vai to rezultātiem.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Core, Operations
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7951f92ef68a7a782f2874d7b73d7e45eba0afba
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003031"
---
# <a name="product-recommendations-faq"></a>Bieži uzdotie jautājumi par preču ieteikumiem


[!include [banner](includes/banner.md)]

Šajā tēmā sniegta informācija par procesiem un rīkiem, ko varat izmantot, lai meklētu traucējumus problēmās, kas saistītas ar [preču ieteikumiem](product-recommendations.md) vai to rezultātiem.

## <a name="best-practices"></a>Labākās prakses
Ir ļoti svarīgi izmantot preces šablonu un variantu koncepciju. Saprātīga variantu grupēšana pamata preces šablonā palīdz saraksta algoritmam un pakalpojumam izveidot labākus modeļus. Turklāt pakalpojumu var izmantot tikai vienam preces gadījumam, nevis ievietojot sarakstā visus cieši saistītos variantus. Kad visi cieši saistītie varianti tiek ievietoti sarakstā, var rasties kļūdaini vai dubulti rezultāti.

## <a name="why-are-products-missing-from-my-recommendation-lists"></a>Kāpēc manos ieteikumu sarakstos trūkst preces?

Parasti, ja preču ieteikumu sarakstā trūkst preces, iespējama preces konfigurācijas problēma. Piemēram, iespējams, ka ir nepareizs preces sākuma vai beigu datums, ir nepareizi konfigurēta dimensija vai arī prece nav pareizā kanāla klāstā utt.

Ja preces trūkst ieteikumu sarakstā, kas balstīts uz mākslīgo intelektu – mašīnmācību (AI-ML), iespējams, prece neatbilst ieteikumu saraksta kritērijiem, vai arī tai var nebūt pietiekami daudz pirkšanas transakciju, lai ieteikumu saraksts to parādītu.

Ieteicams pārbaudīt tālāk minētās darbības.
1. **Pārliecinieties, vai HQ ir iespējoti preces ieteikumi.** Lai iegūtu vairāk informācijas par to, kā iespējot šo pakalpojumu, skatiet [Preču ieteikumu iespējošana](enable-product-recommendations.md).
1. **Pārliecinieties, vai ir iestatīti galvenie preces rekvizīti.** Piemēram, preču klāsts ir jāiestata uz **Iekļauts**.
1. **No jauna sašķirotām precēm var paiet līdz pat 3 stundām pirms prece sāks parādīties jaunajā sarakstā.**
1. **Ja prece joprojām neparādās kategorijās "Populārs", "Vispirktākais", "Pircējiem patīk arī" vai "Bieži iegādāts kopā", tad šai precei, iespējams, nav pietiekami daudz transakciju.** Šādā gadījumā varat vai nu gaidīt, kamēr tiks veikts vairāk transakciju, atjaunināt noklusējuma ieteikumu saraksta parametrus vai izmantot manuālu iejaukšanos, lai modificētu ieteikuma preču saraksta rezultātus. Lai iegūtu vairāk informācijas par ieteikumu parametriem, skatiet [Uz AI-ML balstītu ieteikumu rezultātu pārvaldīšana](modify-product-recommendation-results.md).
1. **Pārliecinieties, vai prece atbilst saraksta ieteikumu kritērijiem.** Lai iegūtu vairāk informācijas par preces ieteikumu parametriem, skatiet [Uz AI-ML balstītu ieteikumu rezultātu pārvaldīšana](modify-product-recommendation-results.md).

## <a name="how-can-i-prevent-poor-recommendation-results-from-being-returned"></a>Kā iespējams novērst sliktu ieteikumu rezultātu atgriešanu?

Lai iegūtu rezultātus, ieteikumu sarakstiem ir nepieciešama liela apjoma transakcijas. Tāpēc ir svarīgi, ka lietotāji sniedz visus vēsturiskos transakciju datus.

Turklāt preces, kurām nav nevienas transakcijas vai tikai dažas transakcijas, parasti nav **Pircējiem patīk arī** vai **Bieži iegādāts kopā** rezultātos, un neparādās **Populārs** vai **Vispirktākais** ieteikumu sarakstos. Šī situācija bieži var rasties ļoti jaunām precēm vai arī vecām precēm, kurām ir neliels pirkumu skaits. Populāras jaunas preces viegli pārvarēs šo problēmu.

Ieteicams veikt tālāk minētās darbības.
1. **Pārliecinieties, vai prece atbilst šī saraksta ieteikumu kritērijiem.** Lai iegūtu vairāk informācijas par preces ieteikumu parametriem, skatiet uz AI-ML balstītu ieteikumu rezultātu modificēšana.
1. **Ja prece ir jauna, apsveriet iespēju modificēt ieteikumu sarakstu, līdz precei būs vairāk transakciju.** Lai iegūtu vairāk informācijas par to, kā modificēt ieteikumu saraksta rezultātus, skatiet [Uz AI-ML balstītu ieteikumu rezultātu pārvaldīšana](modify-product-recommendation-results.md).


- **Pārliecinieties, vai prece atbilst šī saraksta ieteikumu kritērijiem.** Lai iegūtu vairāk informācijas par preces ieteikumu parametriem, skatiet [Uz AI-ML balstītu ieteikumu rezultātu pārvaldīšana](modify-product-recommendation-results.md).
- **Ja prece ir jauna, apsveriet iespēju modificēt ieteikumu sarakstu, līdz precei būs vairāk transakciju**. Lai iegūtu vairāk informācijas par to, kā modificēt ieteikumu saraksta rezultātus, skatiet [Uz AI-ML balstītu ieteikumu rezultātu pārvaldīšana](modify-product-recommendation-results.md).

## <a name="can-i-remove-a-product-but-still-see-it-in-the-store"></a>Vai preci var noņemt, bet joprojām to redzēt veikalā?

Varat pielāgot algoritmiski ģenerētus sarakstus, ja biznesam pēc tā rodas nepieciešamība. Tomēr, ja prece ir noņemta no ieteikumu saraksta, prece paliks redzama veikalā. Lai iegūtu vairāk informācijas par to, kā modificēt preču ieteikumu rezultātus, skatiet [Uz AI-ML balstītu ieteikumu rezultātu pārvaldīšana](modify-product-recommendation-results.md).

Ja ir jāaiztur prece, lai to nevarētu redzēt veikalā, vērtība **Preču sortiments** jāmaina uz **Izslēgt**.

## <a name="how-do-i-add-a-list-to-an-e-commerce-page"></a>Kā pievienot sarakstu e-tirdzniecības lapai?

Lai iegūtu informāciju par to, kā pievienot preču ieteikumu lapas savai e-tirdzniecības tīmekļa lapai, skatiet [Preču ieteikumu sarakstu pievienošana lapām](add-reco-list-to-page.md).

## <a name="how-do-i-enable-recommendations-on-pos"></a>Kā iespējot ieteikumus POS?

Pēc preču ieteikumu iespējošanas kontroles POS ekrānam ir jāpievieno ieteikumu panelis. Skatiet [šī līdzekļa dokumentāciju](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen), lai iegūtu vairāk informācijas par to, kā pievienot ieteikumu paneli savas POS ierīces izkārtojumam.

## <a name="additional-resources"></a>Papildu resursi

[Preču ieteikumu apskats](product-recommendations.md)

[Preču ieteikumu iespējošana](enable-product-recommendations.md)

[Uz AI-ML balstītu preču ieteikumu rezultātu pārvaldība](modify-product-recommendation-results.md)
