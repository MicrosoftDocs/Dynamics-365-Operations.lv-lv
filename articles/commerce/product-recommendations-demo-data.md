---
title: Izveidot ieteikumus ar demo datiem
description: Šajā rakstā ir sniegtas norādes par to, kā pielāgot kanāla produktu ieteikumus 1. pakāpes vienas kastes vidēs, izmantojot iepriekš aizpildītus, pielāgojamus demonstrācijas datus.
author: bebeale
ms.date: 09/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7e3df414b3c16c28b6f5ca04f765d91c1312ada4
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/09/2022
ms.locfileid: "9459973"
---
# <a name="create-recommendations-with-demo-data"></a>Izveidot ieteikumus ar demo datiem

[!include [banner](includes/banner.md)]

Šajā rakstā ir sniegtas norādes par to, kā pielāgot kanāla produktu ieteikumus 1. pakāpes vienas kastes vidēs, izmantojot iepriekš aizpildītus, pielāgojamus demonstrācijas datus.

Daudzkanālu preces ieteikumi sniedz redakcionāli pārraudzītu vai programmiski ģenerētu preču sarakstu kopu. Šos sarakstus var izmantot vairākos scenārijos atkarībā no biznesa vajadzībām. Lai iegūtu vairāk informācijas par preču ieteikumu sarakstiem, skatiet [Preču ieteikumu pārskats](product-recommendations.md).

2. līmeņa un augstākās Dynamics 365 vidēs preces ieteikumi tiek automātiski aprēķinātas, pamatojoties uz klienta datiem. Preču ieteikumu demonstrācijas datu izmantošana neatspējo nevienu produkta rekomendāciju risinājumu, kas jau ir nodrošināts vidē, un visas ar tā izmantošanu saistītās izmaksas.

1. līmeņa vidēs preces ieteikumi ir balstīti tikai uz nemainīgajiem demonstrācijas datiem, kas saglabāti .scv failā.

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a>Produkta rekomendāciju demonstrāciju datu aktivizēšana vidē
Lai iespējotu preču ieteikumu demonstrācijas datus, ir jāizvieto Dynamics 365 Commerce priekšskatījuma demonstrācijas paplašinājums attiecīgajai videi. Tas automātiski iespējo preces ieteikumu demonstrācijas datus.

## <a name="default-demo-data"></a>Noklusējuma demonstrācijas dati
Katrai Onebox veida videi komplektā ir ietverts iepriekš ielādēts preces ieteikumu demonstrācijas datu kopums, kas tiek glabāts ar komatu atdalītā ‘reco_demo_data.csv’ failā, kas atrodas Commerce Scale Unit.

Dati ir strukturēti tālāk redzamajās kolonnās.

| Kolonnas nosaukums         | Obligāts          | apraksts                                                                                                                                 | Iespējamās vērtības                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| RecoList            | :heavy_check_mark: | Īpašais preču ieteikumu saraksta veids, kas ir jāģenerē demonstrācijas datu punktam.                                                    | <ul><li>RecoBestSelling</li><li>RecoNew</li><li>RecoTrending</li><li>RecoCart</li><li>RecoPeopleAlsoBuy</li><li>RecoPicks</li><li>RecoSpendilarVisual</li><li>RecoSpendilarTextual</li></ul> |
| OperatingUnitNumber | :heavy_check_mark: | Konkrētais pārvaldības struktūrvienības numurs, kurā ir paredzēts uzrasties preču ieteikumiem.                                        |                                                                              |
| Kategorija            |                    |    Kategorija, kurai jāatgriež konkrētais saraksts. Ja kategorija nav norādīta, saraksts ir paredzēts tikai augšējai navigācijas hierarhijai.    |                                                                              |
| SeedItemId          |                    |    Sarakstiem, kam ir nepieciešams sākums (RecoPeopleAlsoBuy un RecoCart), preces, kurām šiem sarakstiem jāparāda papildu preces.            |                                                                              |
| CustomerId          |                    |    Sarakstiem, kam nepieciešams debitora identifikators (RecoPicks).  Noklusētā vērtība "0" attiecas uz visiem debitoriem.          |                                                                              |
| ItemIds             | :heavy_check_mark: | Viena vai vairākas preces, kas jāatgriež kā rezultāts, kas atdalīts ar ';'.                                                                  |                                                                              |

## <a name="customize-demo-data"></a>Pielāgot demonstrācijas datus
Varat rediģēt noklusējuma demonstrācijas datus ar jebkuru preču un kategoriju informāciju, kas ir konfigurēta HQ. Kad atjaunināt .csv, preču ieteikumi, kas tiek sniegti klientiem, nekavējoties atspoguļos izmaiņas.

Paplašinājums ietver datu faila ar nosaukumu 'RecoMockDataset.csv', kas ļauj jums kontrolēt datu kopu, kas tiek izmantota, lai darbinātu neīstos ieteikumu rezultātus. Faila nosaukumu var kontrolēt, izmantojot paplašinājumu konfigurāciju, izmantojot **ext.Recommendations.DemoFilePath** iestatījumu. Minētais iespējo to, ka jums var būt pieejamas vairākas datu kopas, kuras var ērti pārslēgt, izmantojot konfigurāciju.


```xml
<settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
</settings>
```

## <a name="additional-resources"></a>Papildu resursi

[Preču ieteikumu apskats](product-recommendations.md)

[Iespējojiet Azure Data Lake Storage pakalpojuma Dynamics 365 Commerce vidē](enable-adls-environment.md)

[Iespējot preču ieteikumus](enable-product-recommendations.md)

[Personalizētu ieteikumu iespējošana](personalized-recommendations.md)

[Atteikšanās no personalizētiem ieteikumiem](personalization-gdpr.md)

[Iespējot "veikala līdzīgie izskati" rekomendācijas](shop-similar-looks.md)

[Preču ieteikumu pievienošana punktā POS](product.md)

[Ieteikumu pievienošana transakciju ekrānam](add-recommendations-control-pos-screen.md)

[AI-ML ieteikumu rezultātu pielāgošana](modify-product-recommendation-results.md)

[Manuāli izveidot pārraudzītus ieteikumus](create-editorial-recommendation-lists.md)

[Bieži uzdotie jautājumi par preču ieteikumiem](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
