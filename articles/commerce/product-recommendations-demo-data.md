---
title: Preču ieteikumu iegūšana, izmantojot demonstrācijas datus
description: Šis dokuments sniedz vadlīnijas par to, kā gūt labumu no daudzkanālu preču ieteikumiem 1. līmeņa atsevišķa lodziņa vidēs, izmantojot iepriekš aizpildītus, pielāgojamus demonstrācijas datus.
author: bebeale
manager: AnnBe
ms.date: 10/01/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 1456feb0665b6ec79a36a3704f17da80ffd759a0
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042784"
---
# <a name="get-product-recommendations-using-demo-data"></a>Preču ieteikumu iegūšana, izmantojot demonstrācijas datus
Šis dokuments sniedz vadlīnijas par to, kā gūt labumu no daudzkanālu preču ieteikumiem 1. līmeņa atsevišķa lodziņa vidēs, izmantojot iepriekš aizpildītus, pielāgojamus demonstrācijas datus.

Daudzkanālu preces ieteikumi sniedz redakcionāli pārraudzītu vai programmiski ģenerētu preču sarakstu kopu. Šos sarakstus var izmantot vairākos scenārijos atkarībā no biznesa vajadzībām. Lai iegūtu vairāk informācijas par preču ieteikumu sarakstiem, skatiet [Preču ieteikumu pārskats](product-recommendations.md).

2. līmeņa un augstākās Dynamics 365 vidēs preces ieteikumi tiek automātiski aprēķinātas, pamatojoties uz klienta datiem. Preču ieteikumu demonstrācijas datu izmantošana neatspējo nevienu produkta rekomendāciju risinājumu, kas jau ir nodrošināts vidē, un visas ar tā izmantošanu saistītās izmaksas.

1. līmeņa vidēs preces ieteikumi ir balstīti tikai uz nemainīgajiem demonstrācijas datiem, kas saglabāti .scv failā.

## <a name="enabling-product-recommendations-demo-data-in-an-environment"></a>Produkta rekomendāciju demonstrāciju datu aktivizēšana vidē
Lai iespējotu preču ieteikumu demonstrācijas datus, ir jāizvieto Dynamics 365 Commerce priekšskatījuma demonstrācijas paplašinājums attiecīgajai videi. Tas automātiski iespējo preces ieteikumu demonstrācijas datus.

## <a name="default-demo-data"></a>Noklusējuma demonstrācijas dati
Katrai Onebox veida videi komplektā ir ietverts iepriekš ielādēts preces ieteikumu demonstrācijas datu kopums, kas tiek glabāts ar komatu atdalītā ‘reco_demo_data.csv’ failā, kas atrodas Commerce Scale Unit.

Dati ir strukturēti tālāk redzamajās kolonnās.

| Kolonnas nosaukums         | Obligāts          | Apraksts                                                                                                                                 | Iespējamās vērtības                                                              |
|---------------------|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| IeteikumuSaraksts            | :heavy_check_mark: | Īpašais preču ieteikumu saraksta veids, kas ir jāģenerē demonstrācijas datu punktam.                                                    | <ul><li>IeteikumiVislabākPārdotais</li><li>IeteikumiJauns</li><li>IeteikumiTendences</li><li>IeteikumiGrozs</li><li>IeteikumiCilvēkiArīPērk</li></ul> |
| PārvaldībasStruktūrvienībuNumurs | :heavy_check_mark: | Konkrētais pārvaldības struktūrvienības numurs, kurā ir paredzēts uzrasties preču ieteikumiem.                                        |                                                                              |
| Kategorija            |                    |    Kategorija, kurai jāatgriež konkrētais saraksts. Ja kategorija nav norādīta, saraksts ir paredzēts tikai augšējai navigācijas hierarhijai.    |                                                                              |
| AtlasesPrecesId          |                    |    Sarakstiem, kam ir nepieciešams sākums (RecoPeopleAlsoBuy un RecoCart), preces, kurām šiem sarakstiem jāparāda papildu preces.            |                                                                              |
| PrecesId             | :heavy_check_mark: | Viena vai vairākas preces, kas jāatgriež kā rezultāts, kas atdalīts ar ";".                                                                  |                                                                              |

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

[Vides plānošana](../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)
