---
title: Duālā ieraksta pārskats
description: Šajā rakstā ir sniegts apskats par dubulto rakstiet, kas nodrošina tuvu reāllaika mijiedarbībai starp debitoru iesaisību programmām un finanšu un operāciju programmām.
author: RamaKrishnamoorthy
ms.date: 02/06/2020
ms.topic: overview
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 599cfdab8232cab28c59c5098094c4afd351df77
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/02/2022
ms.locfileid: "9112400"
---
# <a name="dual-write-overview"></a>Duālā ieraksta pārskats

[!include [banner](../../includes/banner.md)]





## <a name="what-is-dual-write"></a>Kas ir duālais ieraksts?

Duālā rakstīšana ir infrastruktūra, kas atrodas ārpus kastes, kas nodrošina tuvu reāllaika mijiedarbību starp debitoru iesaisību programmām un finanšu un operāciju programmām. Kad dati par debitoriem, precēm, cilvēkiem un operācijām pārsniedz programmas robežas, tiek nodrošinātas visas organizācijas struktūrvienības.

Dubultā rakstīšana nodrošina cieši saistītas, divvirzienu integrāciju starp finanšu un operāciju programmām un Dataverse. Jebkuras datu izmaiņas finanšu un operāciju programmās izraisa rakstīšanas Dataverse, Dataverse un jebkuras datu izmaiņas izraisa rakstīšanas iemeslus finanšu un operāciju programmās. Šī automatizētā datu plūsma nodrošina integrētu lietotāja pieredzi programmās.

![Datu relācija starp programmām.](media/dual-write-overview.jpg)

Duālajam ierakstam ir divi aspekti: *infrastruktūras* aspekts un *programmas* aspekts.

### <a name="infrastructure"></a>Infrastruktūra

Duālā ieraksta infrastruktūra ir paplašināma un uzticama, un tajā ir iekļauti šādi galvenie līdzekļi:

+ Sinhrona un divvirzienu datu plūsma starp programmām
+ Sinhronizācija kopā ar atskaņošanas, pauzes un izlīdzināšanas režīmiem, lai atbalstītu sistēmu tiešsaistes un bezsaistes/asinhrono režīmu laikā.
+ Iespēja sinhronizēt sākotnējos datus starp programmām
+ Kombinētais darbību un kļūdu žurnālu skats datu administratoriem
+ Iespēja konfigurēt pielāgotus brīdinājumus un sliekšņus un pieteikties paziņojumiem
+ Intuitīvs lietotāja interfeiss (UI) filtrēšanai un pārveidei
+ Iespēja iestatīt un skatīt tabulu atkarības un attiecības
+ Paplašināmība gan standarta, gan pielāgotajām tabulām un kartēm
+ Uzticama programmas dzīves cikla pārvaldība
+ Standarta iestatījumu pieredze jauniem debitoriem

### <a name="application"></a>Pieteikums

Duālā rakstīšana izveido kartējumu starp koncepcijām finanšu un operāciju programmās un koncepcijām debitoru lietojumprogrammu darbībās. Šī integrācija atbalsta šādus scenārijus:

+ Integrētie debitoru pamatdati
+ Piekļuve klientu lojalitātes programmas kartēm un atlīdzības punktiem
+ Vienota preču šablonu pieredze
+ Organizācijas hierarhijas apzināšanās
+ Integrētie kreditoru pamatdati
+ Piekļuve finanšu un nodokļu atsauces datiem
+ Cenas programmas pieredze pēc pieprasījuma
+ Integrēta "no potenciālā klienta uz naudu" tipa pieredze
+ Iespēja apkalpot gan iekšējos līdzekļus, gan debitora līdzekļus, izmantojot uz vietas esošos aģentus
+ Integrēta piegādes-apmaksas pieredze
+ Klienta datu un dokumentu integrētās aktivitātes un piezīmes
+ Iespēja meklēt rīcībā esošo krājumu pieejamību un detalizētu informāciju
+ "Projekta-naudas" pieredze
+ Iespēja apstrādāt vairākas adreses un lomas, izmantojot puses koncepciju


## <a name="top-reasons-to-use-dual-write"></a>Galvenie iemesli duālā ieraksta lietošanai

Duālais ieraksts nodrošina datu integrāciju Microsoft Dynamics 365 programmās. Šīs spēcīgās struktūras saista vides un ļauj dažādām biznesa programmām strādāt kopā. Lūk, galvenie iemesli, kāpēc jums jāizmanto duālais ieraksts:

+ Duālais ieraksts nodrošina cieši saistītu, gandrīz reāllaika un divvirzienu integrāciju starp Finance and Operations programmām un Customer Engagement programmām. Šī integrācija padara Microsoft Dynamics 365 par vienas pieturas aģentūru visiem jūsu biznesa risinājumiem. Debitori, kas izmanto Dynamics 365 finanses Dynamics 365 Supply Chain Management un, taču kas klientu attiecību pārvaldībai (CRM) izmanto risinājumus, kas nav Microsoft risinājumi, virzās uz programmu Dynamics 365 tās duālās rakstīšanas atbalstam.
+ Dati no debitoriem, precēm, operācijām, projektiem, kā arī no lietu interneta (IoT) tiek automātiski pārsūtīti uz Dataverse ar duālo ierakstu. Šis savienojums ir noderīgs uzņēmumiem, kas ir ieinteresēti Power Platform paplašināšanā.
+ Duālā ieraksta infrastruktūrā tiek ievērots bezkoda/zemā koda princips. Ir nepieciešami minimāli tehniskie pūliņi, lai paplašinātu standarta "no tabulas līdz tabulai" kartes un iekļautu pielāgotas kartes.
+ Duālais ieraksts atbalsta gan tiešsaistes, gan bezsaistes režīmu. Microsoft ir vienīgais uzņēmums, kas piedāvā atbalstu tiešsaistes un bezsaistes režīmiem.

## <a name="what-does-dual-write-mean-for-developers-and-architects-of-customer-engagement-apps"></a><a id="developer-architect"></a>Ko duālais ieraksts nozīmē Customer Engagement programmu izstrādātājiem un arhitektiem?

Duālās rakstīšanas automatizē datu plūsmu starp finanšu un operāciju programmām un debitoru piesaistes programmām. Duālais ieraksts sastāv no diviem AppSource risinājumiem, kas ir instalēti risinājumā Dataverse. Risinājumi paplašina tabulu shēmu, spraudņus un darbplūsmas risinājumā Dataverse , lai tās varētu mērogot līdz ERP lielumam. Lai ieviestu veiksmīgi, debitoru lietojumprogrammu izstrādātājiem un arhitektiem ir jāsaprot šīs izmaiņas un jāsadarbojas ar to citiem finanšu un operāciju programmām.

Lai izveidotu pārību ar finanšu un operāciju programmām, duālā rakstīšana veic dažas izšķirošas izmaiņas Dataverse shēmā. Ja jūs saprotat plānu, varat izvairīties no daļas no dizaina un attīstības pārstrādāšanas nākotnē.

+ Kad duālā ieraksta AppSource pakotne ir instalēta, risinājumam Dataverse būs jauni jēdzieni, piemēram, uzņēmums un puse. Šīs koncepcijas palīdz uz tām programmām, kas veidotas Dataverse, iekļaujot Dynamics 365 Pārdošanu, Dynamics 365 Marketing, Dynamics 365 Customer Service un Dynamics 365 Field Service efektīvi sadarboties ar finanšu un operāciju programmām.

+ Aktivitātes un piezīmes ir vienotas un paplašinātas, lai atbalstītu gan C1 (sistēmas lietotājus), gan C2 (sistēmas klientus).

+ Lai novērstu datu zudumus Dataverse valūtas pārsūtīšanas laikā starp finanšu un operāciju programmām un, iespējams paplašināt decimāldaļu skaitu debitoru lietojumprogrammu valūtas datu tipa. Līdzeklis pārtulko esošas rindas jaunajā paplašinātajā stāvoklī metadatu slānī. Šī procesa laikā valūtas vērtība tiek pārrēķināta uz decimālajiem datiem, nevis naudas datiem, un valūtas vērtība atbalsta 10 decimāldaļu vietas. Šis līdzeklis ir izvēles iespēja, un organizācijām, kurām nav nepieciešams vairāk par 4 decimāldaļas cipariem, nav jāpiesakās. Lai iegūtu papildu informāciju, skatiet [Valūtas datu veida migrācija duālajam ierakstam](currrency-decimal-places.md).

+ [Datuma efektivitāte](../../dev-tools/date-effectivity.md) tiks pievienota Dataverse. Tā atbalstīs pagātnes, tagadnes un nākotnes datus vienā tabulā.

+ Preču [vienību pārveidošanas](../../../../supply-chain/pim/tasks/manage-unit-measure.md) tiek atbalstītas precēm, piedāvājumiem, pasūtījumiem un rēķiniem.

Papildinformāciju par gaidāmajām izmaiņām skatiet sadaļā [Kas jauns vai mainīts duālā rakstā](whats-new-dual-write.md).



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

