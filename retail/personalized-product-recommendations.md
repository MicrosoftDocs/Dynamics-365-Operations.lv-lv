---
title: "Personalizētu produktu ieteikumus pārskats"
description: "Dynamics 365 operācijām, var tikt rādītas produktu ieteikumus solīja sale (POS) ierīci. Ieteikumi ir priekšmeti, kurus klients varētu interesēt pamatojoties uz savu pirkumu vēsturi, viņu vēlmju saraksta vienumos un elementus, kas citiem klientiem iegādāties tiešsaistē un ķieģeļu un javas veikalos. Tirgotājiem ar lielu katalogus, ieteikumi palīdz klientam ar produktu atklāšana. Pēc demonstrētu produktu mērķauditorija ir klienta intereses un pirkšanas paradumus, produktu ieteikumus var palīdzēt mazumtirgotājiem un līdz pārdot papildproduktus un uzlabo klientu saglabāšana. Programmā Dynamics 365 operācijām, product ieteikumi ir aprīkoti ar izziņas services un Microsoft Azure mašīna mācībām."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: af1f4ba1ed5efe0e35d08d37d09e7ada4a4c1b7a
ms.lasthandoff: 03/31/2017


---

# <a name="personalized-product-recommendations-overview"></a>Personalizētu produktu ieteikumus pārskats

Dynamics 365 operācijām, var tikt rādītas produktu ieteikumus solīja sale (POS) ierīci. Ieteikumi ir priekšmeti, kurus klients varētu interesēt pamatojoties uz savu pirkumu vēsturi, viņu vēlmju saraksta vienumos un elementus, kas citiem klientiem iegādāties tiešsaistē un ķieģeļu un javas veikalos. Tirgotājiem ar lielu katalogus, ieteikumi palīdz klientam ar produktu atklāšana. Pēc demonstrētu produktu mērķauditorija ir klienta intereses un pirkšanas paradumus, produktu ieteikumus var palīdzēt mazumtirgotājiem un līdz pārdot papildproduktus un uzlabo klientu saglabāšana. Programmā Dynamics 365 operācijām, product ieteikumi ir aprīkoti ar izziņas services un Microsoft Azure mašīna mācībām.

<a name="scenarios"></a>Scenāriji
---------

Product ieteikumi ir iespējotas POS šādos scenārijos. Tie ir pieejami mākoni ražotāju organizācijas vai mūsdienu POS (MPOS).

1.  Par **Product details** lapas:

-   Ja veikalā saistīt vizītes **Product details** lapu, kad skatās uz iepriekšējiem darījumiem pa dažādiem kanāliem, ieteikums motoru ierosina papildu krājumus, kas, visticamāk, iegādāties kopā.
-   Ja veikalā saistīt pievieno klienta darbība un pēc tam apmeklē **Product details** lapa, ieteikums dzinējs nodrošina personificētas ieteikumus, izmantojot klienta darbību vēsturi.

[![proddetails](./media/proddetails.png)](./media/proddetails.png)

1.  Par **darījumu** lapas:

-   Ieteikums motoru liecina vienumus, pamatojoties uz visu preču grozu sarakstu.
-   Ja veikalā saistīt pievieno klienta darbība, ieteikums dzinējs nodrošina personiskiem ieteikumiem, izmantojot klienta darbību vēsturi un vienumu saraksta grozā.

**Piezīme** attēlošanai ieteikumus **darījumu** lapu, mazumtirgotājs jāatjaunina ekrāna izkārtojumu Dynamics 365 operācijām. **Ieteikumi** kontrole ir samazinājies uz **darījumu** lapā. [![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

1.  Par **informāciju par klientiem** lapas:
    -   Ieteikums motoru liecina vienumus, pamatojoties uz lietotāja ID un klienta vēlmju saraksta vienumiem.

[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)

## <a name="configure-dynamics-365-for-operations-to-enable-pos-recommendations"></a>Konfigurēt Dynamics 365 operācijām, lai ļautu ražotāju organizāciju ieteikumi
Lai iestatītu produktu ieteikumus, kas jums jādara šādi.

1.  Pārliecinieties, ka esat atlasījis pareizo **juridisku personu**.
2.  Naviģējiet uz **entītiju veikala**, izvēlieties **mazumtirdzniecība**, un pēc tam noklikšķiniet uz **atsvaidzināt**. * * * * tas izmantot demo datu (vai jūsu datus) no darbības bāzes un pārvietot to uz entītiju veikalā.
3.  Nav obligāti: Lai darbība ekrānā parādītu ieteikumus, iet uz * ekrāna izkārtojumu, **izvēlēties ekrāna izkārtojumu, uzsākt **ekrāna izkārtojuma dizainers**,** * * un tad nometiet * * ieteikumiem kontroles * * tur, kur tas ir vajadzīgs.
4.  Iet uz **mazumtirdzniecības parametrus**, izvēlieties **Machine learning**, izvēlieties * * Jā * * zem **iespējot POS ieteikumus**.
5.  Redzēt ieteikumus par POS, vadīt globālos konfigurācijas darbu **1110**. Lai atspoguļotu izmaiņas, kas veiktas POS ekrāna izkārtojuma dizainers, palaist kanāla konfigurācija darbam **1070**.

## <a name="how-does-it-work"></a>[]()Kā tas darbojas?
Atsvaidzinot **entītiju veikala** vienība, notiek šādas darbības.

-   Datu formātā, kuru pieprasa izziņas dienestu ekstrahē no Dynamics 365 darbības operatīvo datu bāzes un nosūtīts uz entītiju veikalā.
-   Dati tiek izmantoti Azure dati fabrika (ADF), lai attīrītu datus, izmantojot stropu skriptus, kā daļu no ADF aktivitātēm. Iztīra dati tiek glabāti krātuves lāse.
-   Datus no krātuves lāse izmanto izziņas dienestu, API apmācīt ieteikumu modeli.

Kad ieslēdzat **iespējot ieteikumus** un palaist konfigurācijas darbus, veikt šādas darbības.

-   Modeļa akreditācijas ID ir palielinājies no API un uzglabā Dynamics 365 darbības operatīvo datu bāzes, Web. config uz AOS, kā arī mazumtirdzniecības serveru.
-   Modeļa akreditācijas datus un ID padarīti pieejami CRT, tāpēc, ka aicinājumi produktu ieteikumus no mākoņa POS un MPOS tiešsaistes režīmā var cienījams.


<a name="see-also"></a>Skatiet arī
--------

[Rekomendācijas vadīklas pievienošana POS ierīces darbības lapā](add-recommendations-control-pos-screen.md)


