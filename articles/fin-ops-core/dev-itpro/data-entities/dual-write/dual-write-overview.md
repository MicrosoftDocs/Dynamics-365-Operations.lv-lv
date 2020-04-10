---
title: Duālā ieraksta pārskats
description: Šī tēma sniedz apskatu par duālo ierakstu. Duālais ieraksts ir infrastruktūra, kas nodrošina gandrīz reāllaika mijiedarbību starp Microsoft Dynamics 365 modeļa vadītajām programmām un Finance and Operations programmām.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 64626ebdd7fbad3d47a4b4c6bbc45bf3bc0c8277
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172788"
---
# <a name="dual-write-overview"></a>Duālā ieraksta pārskats

[!include [banner](../../includes/banner.md)]



## <a name="what-is-dual-write"></a>Kas ir duālais ieraksts?

Duālais ieraksts ir standarta infrastruktūra, kas nodrošina gandrīz reāllaika mijiedarbību starp Microsoft Dynamics 365 modeļa vadītajām programmām un Finance and Operations programmām. Kad dati par debitoriem, precēm, cilvēkiem un operācijām pārsniedz programmas robežas, tiek nodrošinātas visas organizācijas struktūrvienības.

Duālais ieraksts nodrošina cieši saistītu divvirzienu integrāciju starp Finance and Operations programmām un Common Data Service. Visas Finance and Operations programmas datu izmaiņas izraisa Common Data Service ierakstus, un jebkuras datu izmaiņas, kas rodas Common Data Service rada ierakstus Finance and Operations programmām. Šī automatizētā datu plūsma nodrošina integrētu lietotāja pieredzi programmās.

![Datu relācija starp programmām](media/dual-write-overview.jpg)

Duālajam ierakstam ir divi aspekti: *infrastruktūras* aspekts un *programmas* aspekts.

### <a name="infrastructure"></a>Infrastruktūra

Duālā ieraksta infrastruktūra ir paplašināma un uzticama, un tajā ir iekļauti šādi galvenie līdzekļi:

+ Sinhrona un divvirzienu datu plūsma starp programmām
+ Sinhronizācija kopā ar atskaņošanas, pauzes un izlīdzināšanas režīmiem, lai atbalstītu sistēmu tiešsaistes un bezsaistes/asinhrono režīmu laikā.
+ Iespēja sinhronizēt sākotnējos datus starp programmām
+ Konsolidētais darbību un kļūdu žurnālu skats datu administratoriem
+ Iespēja konfigurēt pielāgotus brīdinājumus un sliekšņus un pieteikties paziņojumiem
+ Intuitīvs lietotāja interfeiss (UI) filtrēšanai un pārveidei
+ Iespēja iestatīt un skatīt elementu atkarības un attiecības
+ Paplašināmība gan standarta, gan pielāgotajām entītijām un kartēm
+ Uzticama programmas dzīves cikla pārvaldība
+ Standarta iestatījumu pieredze jauniem debitoriem

### <a name="application"></a>Pieteikums

Duālais ieraksts izveido kartēšanu starp koncepcijām Finance and Operations programmās un koncepcijās, kas iekļautas modeļa vadītajās Dynamics 365 programmās. Šī integrācija atbalsta šādus scenārijus:

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
+ Viena avota pārvaldība lietotājiem
+ Integrētie kanāli mazumtirdzniecībai un mārketingam
+ Ieskats akcijās un atlaidēs
+ Pakalpojuma pieprasījuma funkcijas
+ Racionalizētas pakalpojuma darbības

## <a name="top-reasons-to-use-dual-write"></a>Galvenie iemesli duālā ieraksta lietošanai

Duālais ieraksts nodrošina datu integrāciju Microsoft Dynamics 365 programmās. Šīs spēcīgās struktūras saista vides un ļauj dažādām biznesa programmām strādāt kopā. Lūk, galvenie iemesli, kāpēc jums jāizmanto duālais ieraksts:

+ Duālais ieraksts nodrošina cieši saistītu, gandrīz reāllaika un divvirzienu integrāciju starp Finance and Operations programmām un modeļa vadītām programmām pakalpojumā Dynamics 365. Šī integrācija padara Microsoft Dynamics 365 par vienas pieturas aģentūru visiem jūsu biznesa risinājumiem. Klienti, kuri lieto Dynamics 365 Finance un Dynamics 365 Supply Chain Management, bet kas neizmanto Microsoft risinājumus klientu attiecību pārvaldībai (CRM), pāriet uz Dynamics 365 tā duālā ieraksta atbalsta dēļ.
+ Dati no debitoriem, precēm, operācijām, projektiem, kā arī no lietu interneta (IoT) tiek automātiski pārsūtīti uz Common Data Service ar duālo ierakstu. Šis savienojums ir ļoti noderīgs uzņēmumiem, kas ir ieinteresēti Microsoft Power Platform paplašināšanā.
+ Duālā ieraksta infrastruktūrā tiek ievērots bezkoda/zemā koda princips. Ir nepieciešami minimāli tehniskie pūliņi, lai paplašinātu standarta "no tabulas līdz tabulai" kartes un iekļautu pielāgotas kartes.
+ Duālais ieraksts atbalsta gan tiešsaistes, gan bezsaistes režīmu. Microsoft ir vienīgais uzņēmums, kas piedāvā atbalstu tiešsaistes un bezsaistes režīmiem.

## <a name="what-does-dual-write-mean-for-users-and-architects-of-crm-products"></a>Ko duālais ieraksts nozīmē CRM preču lietotājiem un arhitektiem?

Duālais ieraksts automatizē datu plūsmu starp Finance and Operations programmām un Common Data Service. Turpmākajos laidienos jēdzieni modeļa darbinātās programmās pakalpojumā Dynamics 365 (piemēram, klients, kontaktpersona, piedāvājums un pasūtījums) tiks mērogoti uz vidusmēra tirgu un vidusmēra tirgus klientiem.

Pirmajā laidienā lielākā daļa automatizācijas tiek apstrādāta ar duālā ieraksta risinājumiem. Turpmākajos laidienos šie risinājumi kļūs par daļu no Common Data Service. Izprotot gaidāmās izmaiņas Common Data Service, jūs varat ietaupīt savus pūliņus ilgākā termiņā. Dažas no būtiskām izmaiņām:

+ Common Data Service būs jaunas koncepcijas, piemēram, uzņēmums un puse. Šīs koncepcijas ietekmēs visas programmas, kas ir iebūvētas Common Data Service, piemēram, Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service un Dynamics 365 Field Service.
+ Aktivitātes un piezīmes ir vienotas un paplašinātas, lai atbalstītu gan C1 (sistēmas lietotājus), gan C2 (sistēmas klientus).
+ Dažas no gaidāmajām Common Data Service izmaiņām:

    - Decimālais datu tips aizstās naudas datu tipu.
    - Datu efektivitāte atbalstīs pagātnes, tagadnes un nākotnes datus vienuviet.
    - Būs vairāk atbalsta valūtas un maiņas kursiem, un tiks pārskatīts **Maiņas kursa** programmu programmēšanas interfeiss (API).
    - Tiks atbalstīta mērvienību konvertēšana.

Lai iegūtu papildu informāciju par gaidāmajām izmaiņām, skatiet šeit: [Dati Common Data Service– 1. un 2. fāze](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/finance-operations-crossapp-capabilities/data-common-data-service-phase-1).
