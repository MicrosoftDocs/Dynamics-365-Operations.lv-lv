---
title: Veikala krājumu pārvaldība
description: Šajā tēmā ir aprakstīti dokumentu veidi, ko varat izmantot krājumu pārvaldībai.
author: rubencdelgado
manager: AnnBe
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a3e6450c358d12dc62c2ffa20e7ff529be86bbe5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414064"
---
# <a name="store-inventory-management"></a>Veikala krājumu pārvaldība

[!include [banner](includes/banner.md)]

Strādājot ar krājumiem programmā Microsoft Dynamics 365 Commerce un izmantojot pārdošanas punktu (POS) lietojumprogrammu, ir svarīgi zināt, ka POS sniedz ierobežotu atbalstu dažām krājumu dimensijām un dažiem krājuma vienību tipiem. POS lietojumprogramma neatbalsta pilnu krājumu konfigurācijas iespēju klāstu, kas ir pieejams, izmantojot krājuma konfigurācijas opcijas objektā Dynamics 365 Supply Chain Management.

POS risinājums pašlaik neatbalsta šādas produktu dimensijas un krājumu konfigurācijas:

- Konfigurācijas preces dimensija un materiālu komplekta (MK) krājumi (izņemot mazumtirdzniecības komplekta preces, kas izmanto dažus MK struktūras komponentus)
- Pieļaujamā svara krājumus
- Versijas preces dimensija — kontrolētie krājumi

POS lietojumprogramma pašlaik neatbalsta šādas izsekošanas dimensijas POS:

- Partijas izsekošanas dimensija
- Īpašnieka dimensija

POS nodrošina ierobežotu atbalstu šādām dimensijām. Citiem vārdiem sakot, POS varētu automātiski izmantot dažas no šīm dimensijām krājumu transakcijās, pamatojoties uz noliktavas vai veikala iestatījumu konfigurāciju. POS nenodrošina pilnīgu atbalstu dimensijām tādā veidā, kādā tās tiek atbalstītas, ja pārdošanas transakcija ir manuāli ievadīta Commerce Headquarters. 

- **Noliktavas atrašanās vieta** — izmantojot jaunas [Ienākošo operāciju](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) un [izejošo operāciju](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation) POS operācijas, lietotāji var atlasīt noliktavas krājumu novietojumu, lai varētu saņemt krājumus vai nosūtīt izejošos pārsūtīšanas pasūtījuma krājumus. Ja tiek izmantota novecojuša **Izdošanas un saņemšanas** operācija, ir pieejams ierobežots novietojuma pārvaldības atbalsts, lai varētu saņemt un nosūtīt izejošās pārsūtīšanas. Šis atbalsts ir pieejams tikai tad, ja krājumam un veikala noliktavai ir ieslēgta opcija **Izmantot noliktavas vadības procesus**. Krājumu atrašanās vietu pašlaik nevar izmantot kopā ar **Krājumu uzskaites** vai **Krājumu pārlūkošanas** operāciju.
- **Numura zīme** – piemērojamas tikai tad, ja krājuma un veikala noliktavai ir ieslēgta opcija **Izmantot noliktavas vadības procesus**. Sistēmā POS, ja krājumi tiek saņemti veikala noliktavā, izmantojot **Ienākošo operāciju** vai **Izdošanas un saņemšanas** operāciju ar ieslēgtu noliktavas pārvaldības procesu, un ja novietojums, kas tika izvēlēts krājumu saņemšanai, ir saistīts ar atrašanās vietas profilu, kam nepieciešama numura zīmes kontrole, POS lietojumprogramma sistemātiski piemēro numura zīmi saņemšanas rindai. POS lietotāji nevar mainīt vai pārvaldīt šo numura zīmju datus. Ja ir nepieciešama pilna numura zīmju pārvaldīšana, veikalam ieteicams izmantot [noliktavas programmu](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/install-configure-warehousing-app) vai uzskaites daļas klientu, lai pārvaldītu šo krājumu saņemšanu.
- **Sērijas numurs** – lietojumprogramma POS nodrošina ierobežotu atbalstu atsevišķu sērijas numuru reģistrēšanai pārdošanas rindā pasūtījumiem, kas izveidoti POS un ietver serializētus krājumus. Šis sērijas numurs nav pārbaudīts pret reģistrētajiem sērijas numuriem, kas jau ir krājumos. Ja pārdošanas pasūtījums tiek izveidots zvanu centra kanālā vai izpildīts izmantojot uzņēmuma resursu plānošanu (ERP), un vairāki sērijas numuri ir reģistrēti vienā pārdošanas rindā ERP izpildes procesa laikā, tos sērijas numurus nevarēs lietot vai pārbaudīt, ja atgriešana pasūtījumam tiek apstrādāta lietojumprogrammā POS. Kad krājumi ir saņemti, izmantojot **Ienākošo operāciju**, lietotāji var [reģistrēt vai apstiprināt saņemtos sērijas numuru](https://docs.microsoft.com/dynamics365/commerce/pos-serialized-items).
- **Krājumu statuss** – krājumiem, kas izmanto noliktavas pārvaldības procesu un kam nepieciešams krājumu statuss, šis statusa lauks nevar tikt iestatīts vai modificēts, izmantojot POS lietojumprogrammu. Kad krājuma vienības tiek saņemtas, tiek izmantots noklusējuma krājumu statuss, kas noteikts veikala noliktavas konfigurācijā.

> [!NOTE]
> Visām organizācijām ir jāpārbauda krājumu konfigurācijas, izmantojot POS izstrādes vai testēšanas vidē, pirms tās izvieto šīs krājumu konfigurācijas ražošanas vidēs. Pārbaudiet krājumus, izmantojot tos, lai veiktu regulārus skaidras naudas un bez piegādes darījumus, apstrādājot un izveidojot debitoru pasūtījumus (ja piemērojams) ar POS starpniecību. Jums ir jāpārbauda arī POS izpildes un krājumu procesi (piemēram, krājumu saņemšanas un pasūtījuma izpildes operācijas) pirms jaunu krājumu konfigurāciju izvietošanas, lai pārliecinātos, ka POS lietojumprogramma var tās atbalstīt. Pārbaudēs ir jāiekļauj pilns izrakstu grāmatošanas process jūsu testēšanas vidē, un vai nav problēmu, kas rodas, kad pasūtījumi šiem krājumiem tiek izveidoti un grāmatoti Commerce Headquarters.
>
> Ja vienumi ir konfigurēti tā, ka POS lietojumprogramma netiek atbalstīta un netiek veikta atbilstoša testēšana, pasūtījuma izveides laikā var rasties datu kļūmes, kuras nav viegli novēršamas vai kuras nav ietvertas standarta produktu atbalstā.

## <a name="purchase-orders"></a>Pirkšanas pasūtījumi

Pirkšanas pasūtījumi tiek izveidoti Commerce Headquarters. Ja pirkšanas pasūtījuma virsrakstā vai pirkšanas pasūtījuma rindā ir iekļauta veikala noliktava, tad rindas var saņemt veikalā, izmantojot programmu [Ienākošās operācijas](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) POS operācijās. 

## <a name="transfer-orders"></a>Pārsūtīšanas pasūtījumi

Pārsūtīšanas pasūtījumus var izveidot Commerce Headquarters vai izmantojot [ienākošo operāciju](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) vai [izejošo operāciju](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation) POS operācijās. Izmantojiet POS **ienākošo operāciju**, lai izveidotu pārsūtīšanas pasūtījuma pieprasījumu, krājumu nosūtīšanai uz veikalu no citas noliktavas vai veikala vietas. Izmantojiet POS **izejošās operācijas**, lai izveidotu pārsūtīšanas pasūtījuma pieprasījumu, krājumu nosūtīšanai no veikala uz citu noliktavu vai veikala vietu. Kad veikala pārsūtīšanas pasūtījums ir izveidots, šis veikals var pārvaldīt krājumu saņemšanu pārsūtīšanas pasūtījumam, izmantojot POS **ienākošo operāciju**. Ja veikals nosūta krājumus uz citu vietu, POS **izejošās operācija** tiek izmantota, lai pārvaldītu šī veikala izejošo sūtījumu procesu.

## <a name="stock-counts"></a>Krājumu uzskaite

Krājumu uzskaites var būt plānotas vai neplānotas. Plānotais krājumu skaits tiek izveidots caur Commerce Headquarters, izveidojot Inventarizācijas žurnāla dokumentu, kas ir saistīts ar veikala noliktavu. Šis žurnāls norāda krājumus, kas ir jāuzskaita. Veikals pēc tam var piekļūt šiem iepriekš definētajiem inventarizācijas žurnāliem un rīkoties ar tiem, izmantojot **krājumu inventarizācijas** operāciju sistēmā POS. Veikala lietotāji sāk neplānotu krājumu uzskaiti, kad tas ir nepieciešams, izmantojot **krājumu uzskaites** operācijas POS. Atšķirībā no ieplānotās krājumu uzskaites, neplānotajai krājumu uzskaitei netiek lietots iepriekš definēts krājumu saraksts. Kad abu tipu krājumu uzskaite POS ir pabeigta, tā tiek fiksēta un nosūtīta uz galveno biroju. Pēc tam galvenajā birojā uzskaite ir jāapstiprina un jāgrāmato Commerce Headquarters kā atsevišķa darbība.

## <a name="inventory-lookup"></a>Krājumu pārlūkošana

Pašreizējo rīcībā esošo preču daudzumu vairākiem veikaliem un noliktavām var skatīt lapā **Krājumu pārlūkošana**. Papildus pašreizējam rīcībā esošajam daudzumam katram atsevišķajam veikalam var skatīt arī turpmākos solīšanai pieejamos (ATP) daudzumus. Atlasiet veikalu, kam vēlaties skatīt ATP krājumus, un pēc tam atlasiet **Rādīt veikalu pieejamību**. Papildinformāciju par pieejamām konfigurācijas opcijām, skatiet sadaļā [Krājumu pieejamības aprēķināšana mazumtirdzniecības kanāliem](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).
