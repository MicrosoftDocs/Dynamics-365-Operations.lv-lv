---
title: "Pārskats par personalizētiem preču ieteikumiem"
description: "Izmantojot programmatūru Dynamics 365 for Operations, pārdošanas punkta (POS) ierīcē var tikt rādīti preču ieteikumi. Ieteikumi ir krājumi, kas debitoru varētu interesēt, pamatojoties uz debitora pirkumu vēsturi, krājumiem debitora vēlmju sarakstā, kā arī krājumiem, ko citi debitori ir nopirkuši tiešsaistes un fiziskajos veikalos. Ja mazumtirgotājam ir plašs katalogs, ieteikumi palīdz debitoram atklāt preces. Preču ieteikumi nodrošina, ka debitoram tiek piedāvātas viņa interesēm un iepirkumu vēsturei atbilstošas preces, un tādējādi var palīdzēt mazumtirgotājiem veikt papildu pārdošanu un šķērspārdošanu un uzlabot klientu lojalitātes saglabāšanas rādītājus. Programmatūrā Microsoft Dynamics 365 for Operations preču ieteikumi tiek nodrošināti, izmantojot Cognitive Services un Microsoft Azure algoritmisko mācīšanos."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: edacd4cc9f9db59617bc579cb106e8e1017b8957
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="personalized-product-recommendations-overview"></a>Pārskats par personalizētiem preču ieteikumiem

[!include[banner](includes/banner.md)]


Izmantojot programmatūru Dynamics 365 for Operations, pārdošanas punkta (POS) ierīcē var tikt rādīti preču ieteikumi. Ieteikumi ir krājumi, kas debitoru varētu interesēt, pamatojoties uz debitora pirkumu vēsturi, krājumiem debitora vēlmju sarakstā, kā arī krājumiem, ko citi debitori ir nopirkuši tiešsaistes un fiziskajos veikalos. Ja mazumtirgotājam ir plašs katalogs, ieteikumi palīdz debitoram atklāt preces. Preču ieteikumi nodrošina, ka debitoram tiek piedāvātas viņa interesēm un iepirkumu vēsturei atbilstošas preces, un tādējādi var palīdzēt mazumtirgotājiem veikt papildu pārdošanu un šķērspārdošanu un uzlabot klientu lojalitātes saglabāšanas rādītājus. Programmatūrā Microsoft Dynamics 365 for Operations preču ieteikumi tiek nodrošināti, izmantojot Cognitive Services un Microsoft Azure algoritmisko mācīšanos.

<a name="scenarios"></a>Scenāriji
---------

Preču ieteikumi ir iespējoti tālāk norādītajos POS scenārijos. Tie ir pieejami programmā Cloud POS vai Modern POS (MPOS).

1.  Lapā **Detalizēta informācija par preci**.

-   Ja veikala darbinieks apmeklē lapu **Detalizēta informācija par precei**, skatot iepriekšējās transakcijas dažādos kanālos, ieteikumu programma piedāvā papildu preces, kas var tikt nopirktas kopā.
-   Ja veikala darbinieks pievieno transakcijai debitoru un pēc tam apmeklē lapu **Detalizēta informācija par preci**, ieteikumu programma nodrošina personalizētus ieteikumus, izmantojot debitora transakciju vēsturi.

[![proddetails](./media/proddetails.png)](./media/proddetails.png)

2.  Lapā **Transakcija**.

-   Ieteikumu programma iesaka preces, pamatojoties uz visu grozam pievienoto preču sarakstu.
-   Ja veikala darbinieks pievieno transakcijai debitoru, ieteikumu programma nodrošina personalizētus ieteikumus, izmantojot debitora transakciju vēsturi un grozam pievienoto preču sarakstu.

**Piezīme.**  Lai lapā **Transakcijas** tiktu rādīti ieteikumi, mazumtirgotājam ir jāatjaunina ekrāna izkārtojums programmatūrā Dynamics 365 for Operations. Lapā **Transakcijas** ir jāaktivizē vadīkla **Ieteikumi**. [![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

3.  Lapā **Detalizēta informācija par debitoru**.
    -   Ieteikumu programma iesaka preces, pamatojoties uz lietotāja ID un precēm debitora velmju sarakstā.

[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)

## <a name="configure-dynamics-365-for-operations-to-enable-pos-recommendations"></a>Dynamics 365 for Operations konfigurēšana, lai iespējotu POS ieteikumus
Lai iestatītu preču ieteikumus, ir jāveic tālāk norādītās darbības.

1.  Pārliecinieties, ka laukā **Juridiskā persona** ir atlasīta vajadzīgā juridiskā persona.
2.  Pārejiet uz sadaļu **Elementu krātuve**, atlasiet vienumu **Pārdošana mazumtirdzniecībā** un pēc tam noklikšķiniet uz **Atsvaidzināt**.** **Šai funkcijai tiek izmantoti demonstrācijas dati (vai jūsu dati) no jūsu operāciju datu bāzes, un šie dati tiek pārvietoti uz elementu krātuvi.
3.  Pēc izvēles. Lai ekrānā Transakcijas tiktu rādīti ieteikumi, pārejiet uz sadaļu **Ekrāna izkārtojums, **izvēlieties savu ekrāna izkārtojumu, palaidiet programmu **Ekrāna izkārtojuma dizainers**** **un pēc tam aktivizējiet **ietiekumu vadīklu**, ja tas ir vajadzīgs.
4.  Pārejiet uz sadaļu **Mazumtirdzniecības rekvizīti**, atlasiet vienumu**Algoritmiskā mācīšanās** un sadaļā **Iespējot POS ieteikumus** atlasiet vienumu **Jā**.
5.  Lai POS tiktu rādīti ieteikumi, palaidiet globālās konfigurācijas darbu Nr. **1110**. Lai atainotu POS ekrāna izkārtojuma dizainerī veiktās izmaiņas, palaidiet kanāla konfigurācijas darbu Nr. **1070**.

## <a name="how-does-it-work"></a>[]()Kā tas notiek?
Kad atsvaidzināt elementu **Elementu krātuve**, tiek veiktas tālāk norādītās darbības.

-   No programmatūras Dynamics 365 for Operations operāciju datu bāzes tiek izgūti dati, kuru formāts atbilst Cognitive Services nepieciešamajam formātam, un šie dati tiek nosūtīti uz elementu krātuvi.
-   Šie dati tiek izmantoti pakalpojumā Azure Data Factory (ADF), lai ADF aktivitāšu ietvaros attīrītu datus, izmantojot Hive skriptus. Attīrītie dati tiek uzglabāti BLOB krātuvē.
-   Dati no BLOB krātuves tiek izmantoti Cognitive Services API, lai apmācītu ieteikumu modeli.

Ja aktivizējat opciju **Iespējot ieteikumus** un palaižat konfigurācijas darbus, tiek veiktas tālāk norādītās darbības.

-   No API tiek izgūti modeļa akreditācijas dati un ID, un tie tiek saglabāti Dynamics 365 for Operations operāciju datu bāzē (AOS failā web.config), kā arī mazumtirdzniecības serverī.
-   Modeļa akreditācijas dati un ID tiek padarīti pieejami CRT, lai varētu izpildīt tiešsaistes preču ieteikumu izsaukumus no programmām Cloud POS un MPOS.


<a name="see-also"></a>Skatiet arī
--------

[Ieteikumu vadīklas pievienošana POS ierīces lapā Transakcijas](add-recommendations-control-pos-screen.md)




