---
title: Duālā ieraksta pārskats
description: Šajā tēmā ir sniegts pārskats par divrakstotību, kas nodrošina gandrīz reāllaika mijiedarbību starp klientu piesaistes lietotnēm un Finance and Operations programmām.
author: RamaKrishnamoorthy
ms.date: 02/06/2020
ms.topic: overview
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: f39322a0c2ef50ef2bbeb256c80096e0687c4642
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061338"
---
# <a name="dual-write-overview"></a>Duālā ieraksta pārskats

[!include [banner](../../includes/banner.md)]





## <a name="what-is-dual-write"></a>Kas ir duālais ieraksts?

Divrakstot ir iebūvēta infrastruktūra, kas nodrošina gandrīz reāllaika mijiedarbību starp klientu iesaistes lietotnēm un Finance and Operations lietotnēm. Kad dati par debitoriem, precēm, cilvēkiem un operācijām pārsniedz programmas robežas, tiek nodrošinātas visas organizācijas struktūrvienības.

Divrakstotā rakstīšana nodrošina cieši savienotu divvirzienu integrāciju starp Finance un Operations lietotnēm un Dataverse. Visas datu izmaiņas Finance and Operations lietojumprogrammās izraisa rakstījumiem Dataverse uz, un visas datu izmaiņas cēloņos Dataverse raksta Finance and Operations lietojumprogrammās. Šī automatizētā datu plūsma nodrošina integrētu lietotāja pieredzi programmās.

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

Divrakstotājamā rakstīšana izveido kartēšanu starp koncepcijām Finance and Operations lietotnēs un koncepcijām klientu iesaistes lietotnēs. Šī integrācija atbalsta šādus scenārijus:

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

+ Duālais ieraksts nodrošina cieši saistītu, gandrīz reāllaika un divvirzienu integrāciju starp Finance and Operations programmām un Customer Engagement programmām. Šī integrācija padara Microsoft Dynamics 365 par vienas pieturas aģentūru visiem jūsu biznesa risinājumiem. Klienti, kuri lieto Dynamics 365 Finance un Dynamics 365 Supply Chain Management, bet kas neizmanto Microsoft risinājumus klientu attiecību pārvaldībai (CRM), pāriet uz Dynamics 365 tā duālā ieraksta atbalsta dēļ.
+ Dati no debitoriem, precēm, operācijām, projektiem, kā arī no lietu interneta (IoT) tiek automātiski pārsūtīti uz Dataverse ar duālo ierakstu. Šis savienojums ir noderīgs uzņēmumiem, kas ir ieinteresēti Power Platform paplašināšanā.
+ Duālā ieraksta infrastruktūrā tiek ievērots bezkoda/zemā koda princips. Ir nepieciešami minimāli tehniskie pūliņi, lai paplašinātu standarta "no tabulas līdz tabulai" kartes un iekļautu pielāgotas kartes.
+ Duālais ieraksts atbalsta gan tiešsaistes, gan bezsaistes režīmu. Microsoft ir vienīgais uzņēmums, kas piedāvā atbalstu tiešsaistes un bezsaistes režīmiem.

## <a name="what-does-dual-write-mean-for-developers-and-architects-of-customer-engagement-apps"></a><a id="developer-architect"></a>Ko duālais ieraksts nozīmē Customer Engagement programmu izstrādātājiem un arhitektiem?

Divu rakstīšu automatizē datu plūsmu starp Finance and Operations programmām un klientu iesaistes lietotnēm. Duālais ieraksts sastāv no diviem AppSource risinājumiem, kas ir instalēti risinājumā Dataverse. Risinājumi paplašina tabulu shēmu, spraudņus un darbplūsmas risinājumā Dataverse , lai tās varētu mērogot līdz ERP lielumam. Lai veiksmīgi īstenotu, klientu piesaistes lietotņu izstrādātājiem un arhitektiem ir jāsaprot šīs izmaiņas un jāsadarbojas ar kolēģiem Finance and Operations lietotnēs.

Lai izveidotu paritāti ar Finance and Operations lietojumprogrammām, divējāda rakstīšana veic dažas būtiskas izmaiņas Dataverse shēmā. Ja jūs saprotat plānu, varat izvairīties no daļas no dizaina un attīstības pārstrādāšanas nākotnē.

+ Kad duālā ieraksta AppSource pakotne ir instalēta, risinājumam Dataverse būs jauni jēdzieni, piemēram, uzņēmums un puse. Šīs koncepcijas palīdz lietojumprogrammām, kas balstītas uz Dataverse, tostarp Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service un Dynamics 365 Field Service, netraucēti mijiedarboties ar Finance and Operations programmām.

+ Aktivitātes un piezīmes ir vienotas un paplašinātas, lai atbalstītu gan C1 (sistēmas lietotājus), gan C2 (sistēmas klientus).

+ Lai novērstu datu zudumu valūtas pārsūtīšanas laikā starp Finance un Operations lietotnēm un Dataverse, varat paplašināt decimāldaļu skaitu klientu piesaistes programmu valūtas datu tipā. Līdzeklis pārtulko esošas rindas jaunajā paplašinātajā stāvoklī metadatu slānī. Šī procesa laikā valūtas vērtība tiek pārrēķināta uz decimālajiem datiem, nevis naudas datiem, un valūtas vērtība atbalsta 10 decimāldaļu vietas. Šis līdzeklis ir izvēles iespēja, un organizācijām, kurām nav nepieciešams vairāk par 4 decimāldaļas cipariem, nav jāpiesakās. Lai iegūtu papildu informāciju, skatiet [Valūtas datu veida migrācija duālajam ierakstam](currrency-decimal-places.md).

+ [Datuma efektivitāte](../../dev-tools/date-effectivity.md) tiks pievienota Dataverse. Tā atbalstīs pagātnes, tagadnes un nākotnes datus vienā tabulā.

+ Preču [vienību pārveidošanas](../../../../supply-chain/pim/tasks/manage-unit-measure.md) tiek atbalstītas precēm, piedāvājumiem, pasūtījumiem un rēķiniem.

Papildinformāciju par gaidāmajām izmaiņām skatiet sadaļā [Kas jauns vai mainīts duālā rakstā](whats-new-dual-write.md).



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
