---
title: "Tiešsaistes veikala pārskats"
description: "Šajā rakstā ir sniegta informācija par mazumtirdzniecības tiešsaistes veikaliem un par to iestatīšanu programmā Microsoft Dynamics 365 for Operations."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16161
ms.assetid: 646d560c-f856-4701-b4ca-44e357ef09b8
ms.search.region: Global
ms.search.industry: Retail
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 40fbf8b4fdfed32dd67013b6b21cc2c8ee3d31e6
ms.lasthandoff: 03/31/2017


---

# <a name="online-store-overview"></a>Tiešsaistes veikala pārskats

Šajā rakstā ir sniegta informācija par mazumtirdzniecības tiešsaistes veikaliem un par to iestatīšanu programmā Microsoft Dynamics 365 for Operations.

Mazumtirdzniecība un komercija programmā Dynamics 365 for Operations atbalsta vairākus mazumtirdzniecības kanālus. Šie mazumtirdzniecības kanāli ietver tiešsaistes veikalus, zvanu centrus un mazumtirdzniecības veikalus (zināmi arī kā fiziskie veikali). Tiešsaistes veikali mazumtirgotājam sniedz tiešsaistes iespējas, lai klienti varētu iegādāties preces ne tikai mazumtirgotāja tiešsaistes veikalā, bet arī tā mazumtirdzniecības veikalos. Ja klienti iegādājas preces no tiešsaistes veikala, tās var saņemt ar sūtījumu vai saņemt vietējā mazumtirdzniecības veikalā. Dynamics 365 for Operations klientā ir iespējams izveidot tiešsaistes veikalu. Šis tiešsaistes veikals tad tiek publicēts trešās puses tiešsaistes veikalā, kas integrēts, izmantojot Dynamics 365 for Operations. Trešās puses tiešsaistes veikalu izmanto kā tiešsaistes veikala Storefront (UI), kas ļauj izvēlēties klientu pārvaldības sistēmu (CMS) un lietotāja interfeisa iespējas. Programmā Dynamics 365 for Operations pieejamas vairākas šāda veida integrācijas. Rekvizīti, ko definējat šim tiešsaistes veikalam, nosaka tiešsaistes veikala darbību. Varat, piemēram, programmā Dynamics 365 for Operations definēt navigācijas kategoriju hierarhiju un piešķirt to tiešsaistes veikalam. Kad tiešsaistes veikalu publicējat trešās puses tiešsaistes veikalā, šī navigācijas kategoriju hierarhija tiek parādīta veikala tiešsaistes versijā. Pircēji tad šo navigācijas kategoriju hierarhiju izmanto, lai pārlūkotu tiešsaistes veikalu un meklētu preces. Lai izveidotu tiešsaistes veikalu, ir jāiestata komponenti, kas ļauj veikt veikalam apstrādājamos darījumus. Jums, piemēram, jāpievieno preču klāsts, jālieto atribūti, jāiestata apmaksas metodes un piegādes metodes. Varat arī definēt konkrētā tiešsaistes veikala cenas, veicināšanas pasākumus, atlaides, tirdzniecības līgumus un piegādes nosacījumus. Pēc tiešsaistes veikala publicēšanas trešās puses tiešsaistes veikalā varat izveidot tiešsaistes veikala mazumtirdzniecības preču katalogus. Katalogā iekļautās preces kļūst par preču sarakstiem tiešsaistes veikalā. Kad pircējs iegādājas preces no tiešsaistes veikala, pieejamie krājumi tiek atjaunināti un sinhronizēti klientā. Turklāt pirkumiem tiek ģenerēti pārdošanas pasūtījumi, un tie tiek nosūtīti uz klientu, lai izpildītu un apstrādātu pasūtījumu.

## <a name="set-up-an-online-store"></a>Iestatīt tiešsaistes veikalu
Lai iestatītu tiešsaistes veikalu, jāizpilda šādi uzdevumi.

1.  Izveidojiet tiešsaistes veikalu.
2.  Pievienojiet tiešsaistes veikalu atbilstošajām organizācijas hierarhijām.
3.  Pievienojiet preču klāstus, kas ietver tiešsaistes veikalā pieejamās preces.
4.  Piešķiriet vai izveidojiet tiešsaistes veikala cenu grupas.
5.  Iestatiet tiešsaistes veikalam pieejamos piegādes režīmus.
6.  Piešķiriet tiešsaistes veikalā pieņemtās maksājumu metodes.
7.  Ja pircējiem ļaujat pasūtīt preces tiešsaistē un pēc tam tās saņemt vietējā veikalā, piešķiriet tiešsaistes veikalam veikala vietrāžu grupas.
8.  Piešķiriet tiešsaistes veikalam atribūtus, kas paredzēti kanāliem, precēm un pārdošanas pasūtījumiem. Kanāla atribūti attiecas uz visu tiešsaistes veikalu, preču īpašība attiecas uz precēm, kas tiek piedāvātas tiešsaistes veikalā, un pārdošanas pasūtījuma atribūti attiecas uz pārdošanas pasūtījumiem, kas tiek ģenerēti no šī tiešsaistes veikala.
9.  Kartējiet atribūtus, lai definētu rekvizītus, kas nosaka, kā šie atribūti darbosies tiešsaistes veikalā. Piemēram, atribūtus var definēt kā obligātus vai meklējamus.
10. Publicējiet tiešsaistes veikalu, lai veidotu savu trešās puses tiešsaistes veikala struktūru pēc saviem ieskatiem. **Svarīgi!** Pirms tiešsaistes veikala publicēšanas tam jāiestata sadales vieta.

## <a name="retail-channel-navigation-hierarchies"></a>Mazumtirdzniecības kanāla navigācijas hierarhijas
Pirms tiešsaistes veikala izveidošanas ir jādefinē mazumtirdzniecības kanāla navigācijas hierarhija, kuru vēlaties izmantot attiecīgajā tiešsaistes veikalā. Mazumtirdzniecības kanāla navigācijas hierarhija pārstāv kategoriju hierarhiju, kas tiešsaistes veikalā tiek rādīta pēc šī veikala publicēšanas. Kad tiešsaistes veikalā publicējat mazumtirdzniecības preču katalogus, šajā katalogā ietvertās preces tiek kartētas uz attiecīgajām mazumtirdzniecības kanāla navigācijas hierarhijas kategorijām. Šo hierarhiju tad izmanto pircēji, lai pārvietotos tiešsaistes veikalā.

## <a name="organization-hierarchies"></a>Organizācijas hierarhijas
Organizācijas hierarhijas izmanto, lai piešķirtu struktūru mazumtirdzniecības kanāliem. Organizācijas hierarhijas pārstāv attiecības starp organizācijām, kas veido jūsu uzņēmumu. Iestatot tiešsaistes veikalus, varat tos pievienot organizāciju hierarhijai. Pēc tam veikali koplieto datus, kas tiek izmantoti preču klāstiem, papildināšanai un pārskatu veidošanai. Kad veidojat organizāciju hierarhiju, jūs tai piešķirat nolūku. Nolūks norāda, kā šī hierarhija tiek izmantota uzņēmumu struktūrā. Varat izveidot vienu organizāciju hierarhiju sava veikala operācijām, un varat šo hierarhiju izmantot preču klāstiem, papildināšanai un pārskatu veidošanai. Varat arī katram nolūkam izveidot atsevišķu organizācijas hierarhiju. Tāpat varat izveidot vairākas hierarhijas ar vienādu nolūku un katrai no tām piešķirt atsevišķu kanālu. Ja mazumtirdzniecības preču katalogus plānojat publicēt tiešsaistes veikalā, tiešsaistes veikali ir jāpievieno organizāciju hierarhijai vismaz attiecībā uz preču sortimentiem. Katalogā iekļautās preces tiek atlasītas no preču sortimentiem, kas ir piešķirti šim tiešsaistes veikalam. Pēc kataloga publicēšanas šis publicēšanas process salīdzina tiešsaistes veikalam piešķirtā preču klāsta spēkā stāšanās datumus un preces, kas ir iekļautas šajā katalogā, lai noteiktu, kurām precēm ir jābūt pieejamām tiešsaistes veikalā.


