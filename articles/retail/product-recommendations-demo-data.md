---
title: Omni-Channel preču ieteikumu demonstrācijas dati
description: Šī dokumenta mērķis ir sniegt vadlīnijas par to, kā līdzekļu Omni-Channel preces rekomendācijas 1. līmeņa Onebox vidē, izmantojot iepriekš aizpildītus, pielāgojamus demonstrācijas datus.
author: bebeale
manager: AnnBe
ms.date: 12/1/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 31aa5dbd2fa814fd572024a4ae36b9d9b46a2fb0
ms.sourcegitcommit: 398c0652acde12c953de007d06055456d6e0a516
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/02/2019
ms.locfileid: "2872330"
---
# <a name="omni-channel-product-recommendations-demo-data"></a>Omni-Channel preču ieteikumu demonstrācijas dati

Šī dokumenta mērķis ir sniegt vadlīnijas par to, kā līdzekļu Omni-Channel preces rekomendācijas 1. līmeņa Onebox vidē, izmantojot iepriekš aizpildītus, pielāgojamus demonstrācijas datus.

Omni-Channel preces ieteikumi sniedz redakcionāli pārraudzītu vai programmatiski ģenerētu paredzētu preču sarakstu. Šos sarakstus var izmantot vairākos scenārijos atkarībā no biznesa vajadzībām. Lai iegūtu vairāk informācijas par preču ieteikumu sarakstiem, lasiet [Preču ieteikumu pārskats.](../commerce/product-recommendations.md)

2. līmeņa un augstākas Dynamics vides preces rekomendācijas tiek automātiski aprēķinātas, pamatojoties uz klienta datiem.
Preču ieteikumu demonstrācijas datu izmantošana neatspējo nevienu produkta rekomendāciju risinājumu, kas jau ir nodrošināts vidē, un visas ar tā izmantošanu saistītās izmaksas.

1. līmeņa vides preces ieteikumi ir balstīti tikai uz nemainīgajiem demonstrācijas datiem, kas saglabāti CSV failā.

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a>Produkta rekomendāciju demonstrāciju datu aktivizēšana vidē

Klientiem ir jāizvieto **Dynamics 365 Commerce priekšskatījuma demonstrācijas paplašinājums** attiecīgajai videi, kas automātiski aktivizē preces rekomendāciju demonstrācijas datus.

## <a name="default-demo-data"></a>Noklusējuma demonstrācijas dati
Katrai Onebox tipa videi komplektā ir ietverts iepriekš ielādēts preces rekomendāciju demonstrācijas datu kopums, kas tiek glabāts **‘reco_demo_data.csv’** failā, kas atrodas tajā pašā mapē, kur šis dokuments, mazumtirdzniecības serverī.

Šie dati ir iedalīti šādās kolonnās

| Kolonnas nosaukums         | Obligāts          | Apraksts                                                                                                                                 | Iespējamās vērtības                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| IeteikumuSaraksts            | :heavy_check_mark: | Īpašais preču ieteikumu saraksta veids, kas ir jāģenerē demonstrācijas datu punktam.                                                    | <ul><li>IeteikumiVislabākPārdotais</li><li>IeteikumiJauns</li><li>IeteikumiTendences</li><li>IeteikumiGrozs</li><li>IeteikumiCilvēkiArīPērk</li></ul> |
| PārvaldībasStruktūrvienībuNumurs | :heavy_check_mark: | Konkrētais pārvaldības struktūrvienības numurs, kurā ir paredzēts, ka preču ieteikumi tiks saklāti.                                        |                                                                              |
| Kategorija            |                    |    Kategorija, kurai jāatgriež konkrētais saraksts. Ja kategorija nav norādīta, saraksts ir paredzēts tikai augšajai navigācijas hierarhijai.    |                                                                              |
| AtlasesPrecesId          |                    |    Saraksti, kuriem ir vajadzīga atlase (IeteikumiCilvēkiArīPērk un IeteikumiGrozs), prese, kurai šiem sarakstiem ir jāuzrāda papildu preces.            |                                                                              |
| PrecesId             | :heavy_check_mark: | Viena vai vairākas preces, kas jāatgriež kā rezultāts, kas ir atdalītas ar **";"**.                                                                  |                                                                              |


## <a name="customize-demo-data"></a>Pielāgot demonstrācijas datus
Klienti var rediģēt noklusējuma demonstrācijas datus ar jebkuru preču un kategorijas informāciju, kas ir konfigurēta HQ. Kad CSV ir atjaunināts, klientiem Atgrieztie preces ieteikumi nekavējoties parādīs izmaiņas.

Paplašinājums ietver datu faila nosaukumu RecoMockDataset.csv, kas ļauj klientam kontrolēt datu kopu, ko izmanto, lai darbinātu pārbaudes objekta ieteikumu rezultātus. Faila nosaukumu var kontrolēt, izmantojot paplašinājumu konfigurāciju, izmantojot **ext.Recommendations.DemoFilePath** iestatījumu. Tas ļauj klientiem ipieeju vairākiem datu kopam, kuras var ērti pārslēgt, izmantojot konfigurāciju.

```
  <settings>
    <add name="ext.Recommendations.DemoFilePath" value="RecoMockDataset.csv" />
  </settings>
```

## <a name="additional-resources"></a>Papildu resursi

[Preču ieteikumu pārskats](../commerce/product-recommendations.md)

[Vides plānošana](../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)
