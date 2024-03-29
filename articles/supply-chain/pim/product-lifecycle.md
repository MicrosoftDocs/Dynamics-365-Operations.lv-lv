---
title: Preču dzīves cikla stāvokļa pārskats
description: Preces dzīves cikla stāvoklis dokumentē izlaistās preces vai preces varianta dzīves cikla stāvokli.
author: t-benebo
ms.date: 01/06/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductLifecycleState, EcoResReleasedProductLifecycleStateChanges
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: 5d1ea1517c75393b1c8d7c95c8aa2405042b4532
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850646"
---
# <a name="product-lifecycle-state-overview"></a>Preču dzīves cikla stāvokļa pārskats

[!include [banner](../includes/banner.md)]

Preces dzīves cikla stāvoklis dokumentē izlaistās preces vai preces varianta dzīves cikla stāvokli. Preces dzīves cikla stāvokļus definē lietotājs — parasti tas ir produktu menedžeris vai preces pamatdatu pārvaldnieks. Īpašus biznesa procesus, piemēram, vispārējo plānošanu, var ietekmēt noteikts dzīves cikla stāvoklis.

Izlaista prece vai preces variants var būt saistīts ar preces dzīves cikla stāvokli, kurš dokumentē, kādā dzīves cikla stāvoklī konkrētā prece vai variants atrodas pašlaik. Varat definēt neierobežotu skaitu preces dzīves cikla stāvokļu, piešķirot stāvokļa nosaukumu un aprakstu. Jaunajām izlaistajām precēm varat atlasīt vienu dzīves cikla stāvokli kā noklusējuma stāvokli. Izlaistie preces varianti izveidošanas laikā savu preces dzīves cikla stāvokli pārmanto no to izlaistās preces šablona. Mainot dzīves cikla stāvokli kādam izlaistas preces šablonam, varat izvēlēties atjaunināt visus esošos variantus, kuriem ir tāds pats sākotnējais stāvoklis.  

## <a name="create-a-new-product-lifecycle-state"></a>Jauna preču dzīves cikla stāvokļa izveide

- Lai izveidotu jaunu preces dzīves cikla stāvokli, skatiet [Jauna preces dzīves cikla stāvokļa izveidošana](tasks/new-product-lifecycle-state.md).

- Lai izveidotu noklusējuma preces dzīves cikla stāvokli, skatiet [Noklusējuma preces dzīves cikla stāvokļa izveidošana](tasks/default-product-lifecycle-state.md).

## <a name="associate-product-lifecycle-states-to-released-products"></a>Preces dzīves cikla stāvokļu saistīšana ar izlaistajām precēm  

Pastāv vairāki veidi, kā preces dzīves cikla stāvokļus saistīt ar izlaistajām precēm vai preces variantiem.

- Izveidojot jaunu izlaisto preci, automātiski tiek piešķirts noklusējuma **Preces dzīves cikla stāvoklis**.
- Izlaižot preci kādai juridiskajai personai, automātiski tiek piešķirts noklusējuma **Preces dzīves cikla stāvoklis**.
- Preces variantu izlaižot kādai juridiskajai personai, ar izlaistās preces šablonu saistītais **Preces dzīves cikla stāvoklis** šajā juridiskajā personā tiek automātiski piešķirts jaunajam variantam.

Preces dzīves cikla stāvokli varat atjaunināt manuāli, izmantojot tālāk norādītos vienumus.

- Saraksta lapa **Izlaistās preces** vai **Detalizēts skats**.
- Saraksta lapa **Izlaistie preces varianti** vai **Detalizēts skats**.
- Atrodiet novecojušās preces vai preces variantus, pamatojoties uz pieprasījumu, un piesaistiet dzīves cikla stāvokli.  

Plašāka informācija:

- Lai preces dzīves cikla stāvokli piesaistītu izlaistas preces šablonam, skatiet [Preces dzīves cikla stāvokļa saistīšana ar izlaistas preces šablonu](tasks/product-lifecycle-state-released-product-master.md).

- Lai preces dzīves cikla stāvokli piesaistītu izlaistai precei, skatiet [Preces dzīves cikla stāvokļa saistīšana ar izlaistu preci](tasks/product-lifecycle-state-released-product.md).

## <a name="impact-on-master-planning"></a>Ietekme uz vispārējo plānošanu

Preces dzīves cikla stāvoklim ir tikai viens kontroles karodziņš: **Ir aktīvs plānošanai**. Pēc noklusējuma tas ir iestatīts uz **Jā** visiem izveidotajiem preces dzīves cikla stāvokļiem, bet to var mainīt uz **Nē**. Ja tas ir iestatīts uz **Nē**, saistītās izlaistās preces vai izlaistie preču varianti ir:

- Izslēgts no vispārējās plānošanas.
- Izslēgts no MK līmeņa aprēķina.

Lai iegūtu detalizētu informāciju par to, kā lietot preces dzīves cikla stāvokli, lai preces izslēgtu no vispārējās plānošanas un MK līmeņa aprēķina, skatiet [Preces dzīves cikla stāvokļa izveidošana, lai izslēgtu preces no vispārējās plānošanas](tasks/exclude-products-master-planning.md)

> [!NOTE]
> Veiktspējas apsvērumu dēļ ir ļoti ieteicams visas novecojušās izlaistās preces vai preces variantus — it īpaši, ja strādājat ar preces konfigurācijas variantiem, kas nav lietojami atkārtoti — saistīt ar preces dzīves cikla stāvokli, kas ir deaktivizēts vispārējai plānošanai.  

## <a name="default-migration-import-and-export"></a>Noklusējuma migrēšana, importēšana un eksportēšana

Preces dzīves cikla stāvokļi netiek atbalstīti datu elementos, un dzīves cikla stāvokli var iestatīt uz mainīgu stāvokli, vai nu, izmantojot izlaistas preces datu elementu vai datu elementa izlaisto variantu.

## <a name="find-obsolete-products-and-products-variants"></a>Novecojušu preču un preces variantu atrašana

Varat palaist simulācijas analīzi, lai atrastu novecojušas izlaistās preces vai preču variantus, un pēc tam atjaunināt to preces dzīves cikla statusu. Lai atrastu novecojušas preces, skatiet [Novecojušu preces variantu atrašana un preces dzīves cikla stāvokļa piešķiršana](tasks/obsolete-product-variants.md). Šajā rakstā ir parādīts, kā atrast novecojušas izlaistās preces vai preču variantus un kā saistīt preces dzīves cikla stāvokli ar novecojušajām precēm. Tajā ir arī parādīts, kā skatīt simulācijas rezultātus un novērtēt, cik preču un preces variantu tiks saistīti ar jaunu preces dzīves cikla stāvokli, izpildot atjauninājumu bez simulācijas.  

Izpildot analīzi simulācijas režīmā, preces un preču varianti, kas identificēti kā novecojuši, tiek parādīti īpašā veidlapā, kur tos var vienkārši pārskatīt. Analīze meklē transakcijas un īpašus pamatdatus, lai identificētu preces, kurām nav pieprasījuma mainīgā periodā un nav pamatdatu, kas varētu radīt pieprasījumu. Jaunās izlaistās preces mainīgā periodā var izslēgt no analīzes. Ja analīzes simulācija atgriež prognozētos rezultātus, lietotājs var palaist analīzi un iestatīt jaunu preces dzīves cikla stāvokli visām precēm, ko analīze identificējusi kā novecojušas.  

> [!NOTE]
> Ņemiet vērā, ka visas analīzes un atjauninājumi ir jāizpilda tajā pašā juridiskajā personā.  

## <a name="criteria-to-select-and-update-released-products-or-product-variants"></a>Izlaisto preču vai preču variantu atlasīšanas un atjaunināšanas kritēriji

Lai atlasītu un atjauninātu izlaistās preces un preču variantus, izmantojiet tālāk norādītos kritērijus.

- Preces vai preces varianta preces dzīves cikla stāvoklim ir jāatšķiras no jaunā vēlamā stāvokļa.
- Prece vai preces variants tika izveidots pirms dažām dienām, ņemot vērā atlases dialoglodziņā ievadīto dienu skaitu.
- Šai precei vai preces variantam nav atvērtu ražošanas pasūtījumu (= statuss < beidzies).
- Šai precei vai preces variantam nav atvērtu krājumu transakciju (= statuss izejas plūsma no ReservPhysical uz QuotationIssue vai status ieejas plūsma no Registrered uz QuotationReceipt).
- Šai precei vai preces variantam nav krājumu transakciju noteiktā iepriekšējo dienu skaita periodā.
- Šai precei vai preces variantam nav nākotnes pieprasījuma vai piedāvājuma apjoma prognozes.  
- Šai precei vai preces variantam krājumu vajadzībā nav iestatīts minimālais krājumu līmenis.
- Šai precei vai preces variantam nav aktīvu fiksēta daudzuma Kanban nosacījumu.  
- Šai precei vai preces variantam nav pakalpojuma pasūtījuma rindas.
- Šai precei vai preces variantam nav aktīvu vai nākotnes pārdošanas vai pirkšanas līguma rindu.
- Šī prece vai preces variants netiek lietots tādā MK, kurš ir piesaistīts plānošanai aktīvas preces vai varianta apstiprinātai MK versijai, kurai nav beidzies derīgums.

## <a name="related-articles"></a>Saistītie raksti

- [Jauna preču dzīves cikla stāvokļa izveide](tasks/new-product-lifecycle-state.md)
- [Noklusējuma preču dzīves cikla stāvokļa izveide](tasks/default-product-lifecycle-state.md)
- [Preces dzīves cikla stāvokļa piešķiršana izlaistam preces šablonam](tasks/product-lifecycle-state-released-product-master.md)
- [Preces dzīves cikla stāvokļa piešķiršana izlaistai precei](tasks/product-lifecycle-state-released-product.md)
- [Novecojušu preču variantu atrašana un preces dzīves cikla stāvokļa piešķiršana](tasks/obsolete-product-variants.md)
- [Preces dzīves cikla stāvokļa izveidošana, lai izslēgtu preces no vispārējās plānošanas](tasks/exclude-products-master-planning.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]