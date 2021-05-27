---
title: Veikala krājumu pārvaldība
description: Šajā tēmā ir aprakstīti dokumentu veidi, ko varat izmantot krājumu pārvaldībai.
author: rubencdelgado
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 64106cb1aeea01f1f227247d32b8b1dfdea98362
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020199"
---
# <a name="commerce-inventory-management"></a>Commerce krājumu pārvaldība

[!include [banner](includes/banner.md)]

Kad strādājat ar krājumu programmā Microsoft Dynamics 365 Commerce un izmantojat kādu no Commerce programmām, kas ir savienotas ar Commerce Scale Unit (CSU), ir svarīgi zināt, ka pasūtījuma apstrādes loģika CSU nodrošina ierobežotu atbalstu dažām krājumu dimensijām un dažiem krājumu veidiem. Commerce programmas neatbalsta pilnu krājumu konfigurācijas iespēju klāstu, kas ir pieejams, izmantojot krājuma konfigurācijas opcijas objektā Dynamics 365 Supply Chain Management.

Commerce programmas, kas darbojas CSU, neatbalsta šādas produktu dimensijas un krājumu konfigurācijas:

- Konfigurācijas preces dimensija un materiālu komplekta (MK) krājumi (izņemot mazumtirdzniecības komplekta preces, kas izmanto dažus MK struktūras komponentus)
- Pieļaujamā svara krājumus
- Versijas preces dimensija — kontrolētie krājumi

Commerce programmas, kas darbojas CSU, neatbalsta šādas izsekošanas dimensijas:
- Īpašnieka dimensija

- Pārdošanas punkta (POS) programma var sniegt ierobežotu atbalstu šādām dimensijām. POS var automātiski izmantot dažas no dimensijām krājumu transakcijās, pamatojoties uz noliktavas vai veikala iestatījumu konfigurāciju. Taču POS nenodrošina pilnīgu atbalstu dimensijām tādā veidā, kādā tās tiek atbalstītas, ja pārdošanas transakcija ir manuāli ievadīta Commerce Headquarters. 

- **Noliktavas atrašanās vieta** — izmantojot jaunas [Ienākošo operāciju](./pos-inbound-inventory-operation.md) un [izejošo operāciju](./pos-outbound-inventory-operation.md) POS operācijas, lietotāji var atlasīt noliktavas krājumu novietojumu, lai varētu saņemt krājumus vai nosūtīt izejošos pārsūtīšanas pasūtījuma krājumus. Ja tiek izmantota novecojuša **Izdošanas un saņemšanas** operācija, ir pieejams ierobežots novietojuma pārvaldības atbalsts, lai varētu saņemt un nosūtīt izejošās pārsūtīšanas. Šis atbalsts ir pieejams tikai tad, ja krājumam un veikala noliktavai ir ieslēgta opcija **Izmantot noliktavas vadības procesus**. Krājumu atrašanās vietu pašlaik nevar izmantot kopā ar **Krājumu uzskaites** vai **Krājumu pārlūkošanas** operāciju.

- **Numura zīme** – piemērojamas tikai tad, ja krājuma un veikala noliktavai ir ieslēgta opcija **Izmantot noliktavas vadības procesus**. Sistēmā POS, ja krājumi tiek saņemti veikala noliktavā, izmantojot **Ienākošo operāciju** vai **Izdošanas un saņemšanas** operāciju ar ieslēgtu noliktavas pārvaldības procesu, un ja novietojums, kas tika izvēlēts krājumu saņemšanai, ir saistīts ar atrašanās vietas profilu, kam nepieciešama numura zīmes kontrole, POS lietojumprogramma sistemātiski piemēro numura zīmi saņemšanas rindai. POS lietotāji nevar mainīt vai pārvaldīt šo numura zīmju datus. Ja ir nepieciešama pilna numura zīmju pārvaldīšana, veikalam ieteicams izmantot [noliktavas programmu](../supply-chain/warehousing/install-configure-warehousing-app.md) vai uzskaites daļas klientu, lai pārvaldītu šo krājumu saņemšanu.

- **Sērijas numurs** – lietojumprogramma POS nodrošina ierobežotu atbalstu atsevišķu sērijas numuru reģistrēšanai pārdošanas rindā pasūtījumiem, kas izveidoti POS un ietver serializētus krājumus. Šis sērijas numurs nav pārbaudīts pret reģistrētajiem sērijas numuriem, kas jau ir krājumos. Ja pārdošanas pasūtījums tiek izveidots zvanu centra kanālā vai izpildīts izmantojot uzņēmuma resursu plānošanu (ERP), un vairāki sērijas numuri ir reģistrēti vienā pārdošanas rindā ERP izpildes procesa laikā, tos sērijas numurus nevarēs lietot vai pārbaudīt, ja atgriešana pasūtījumam tiek apstrādāta lietojumprogrammā POS. Kad krājumi ir saņemti, izmantojot **Ienākošo operāciju**, lietotāji var [reģistrēt vai apstiprināt saņemtos sērijas numuru](./pos-serialized-items.md).

- **Partijas ID** - POS programma nodrošina ierobežotu atbalstu zrakstu grāmatošanas laikā, ja tiek pārdota partijas kontrolēta prece, taču POS lietotāji nevar definēt partijas ID, kas tika pārdots vai izdots, izmantojot POS programmu.

- **Krājumu statuss** – krājumiem, kas izmanto noliktavas pārvaldības procesu un kam nepieciešams krājumu statuss, šis statusa lauks nevar tikt iestatīts vai modificēts, izmantojot POS lietojumprogrammu. Kad krājuma vienības tiek saņemtas, tiek izmantots noklusējuma krājumu statuss, kas noteikts veikala noliktavas konfigurācijā.

> [!NOTE]
> Visām organizācijām ir jāpārbauda krājumu konfigurācijas, izmantojot Commerce programmas izstrādes vai testēšanas vidē, pirms tās izvieto šīs krājumu konfigurācijas ražošanas vidēs. Pārbaudiet savas preces, izmantojot tās, lai POS veiktu regulāras skaidras naudas un pārvedumu transakcijas un izveidotu debitoru pasūtījumus (ja piemērojams), izmantojot POS, zvanu centru vai e-komerciju, lai pārbaudītu, var tos var pilnībā atbalstīt. Jums ir jāpārbauda arī POS izpildes un krājumu procesi (piemēram, krājumu saņemšanas un pasūtījuma izpildes operācijas) pirms jaunu krājumu konfigurāciju izvietošanas, lai pārliecinātos, ka POS lietojumprogramma var tās atbalstīt. Pārbaudēs ir jāiekļauj pilns izrakstu/pasūtījumu grāmatošanas process jūsu testēšanas vidē, un vai nav grāmatošanas problēmu, kas rodas, kad pasūtījumi šiem krājumiem tiek izveidoti un grāmatoti Commerce Headquarters.
>
> Ja krājumi ir konfigurēti veidā, ko neatbalsta Commerce programmas, un nav veikta atbilstoša testēšana, var rasties datu kļūmes, kas nav viegli izlabojamas vai, iespējams, tās nevarēs izlabot vispār.

## <a name="purchase-orders"></a>Pirkšanas pasūtījumi

Pirkšanas pasūtījumi tiek izveidoti Commerce Headquarters. Ja pirkšanas pasūtījuma virsrakstā vai pirkšanas pasūtījuma rindā ir iekļauta veikala noliktava, tad rindas var saņemt veikalā, izmantojot programmu [Ienākošās operācijas](./pos-inbound-inventory-operation.md) POS operācijās. 

## <a name="transfer-orders"></a>Pārsūtīšanas pasūtījumi

Pārsūtīšanas pasūtījumus var izveidot Commerce Headquarters vai izmantojot [ienākošo operāciju](./pos-inbound-inventory-operation.md) vai [izejošo operāciju](./pos-outbound-inventory-operation.md) POS operācijās. Izmantojiet POS **ienākošo operāciju**, lai izveidotu pārsūtīšanas pasūtījuma pieprasījumu, krājumu nosūtīšanai uz veikalu no citas noliktavas vai veikala vietas. Izmantojiet POS **izejošās operācijas**, lai izveidotu pārsūtīšanas pasūtījuma pieprasījumu, krājumu nosūtīšanai no veikala uz citu noliktavu vai veikala vietu. Kad veikala pārsūtīšanas pasūtījums ir izveidots, šis veikals var pārvaldīt krājumu saņemšanu pārsūtīšanas pasūtījumam, izmantojot POS **ienākošo operāciju**. Ja veikals nosūta krājumus uz citu vietu, POS **izejošās operācija** tiek izmantota, lai pārvaldītu šī veikala izejošo sūtījumu procesu.

## <a name="stock-counts"></a>Krājumu uzskaite

Krājumu uzskaites var būt plānotas vai neplānotas. Plānotais krājumu skaits tiek izveidots caur Commerce Headquarters, izveidojot Inventarizācijas žurnāla dokumentu, kas ir saistīts ar veikala noliktavu. Šis žurnāls norāda krājumus, kas ir jāuzskaita. Veikals pēc tam var piekļūt šiem iepriekš definētajiem inventarizācijas žurnāliem un rīkoties ar tiem, izmantojot **krājumu inventarizācijas** operāciju sistēmā POS. Veikala lietotāji sāk neplānotu krājumu uzskaiti, kad tas ir nepieciešams, izmantojot **krājumu uzskaites** operācijas POS. Atšķirībā no ieplānotās krājumu uzskaites, neplānotajai krājumu uzskaitei netiek lietots iepriekš definēts krājumu saraksts. Kad abu tipu krājumu uzskaite POS ir pabeigta, tā tiek fiksēta un nosūtīta uz galveno biroju. Pēc tam galvenajā birojā uzskaite ir jāapstiprina un jāgrāmato Commerce Headquarters kā atsevišķa darbība.

## <a name="inventory-lookup"></a>Krājumu pārlūkošana

Pašreizējo rīcībā esošo preču daudzumu vairākiem veikaliem un noliktavām var skatīt lapā **Krājumu pārlūkošana**. Papildus pašreizējam rīcībā esošajam daudzumam katram atsevišķajam veikalam var skatīt arī turpmākos solīšanai pieejamos (ATP) daudzumus. Atlasiet veikalu, kam vēlaties skatīt ATP krājumus, un pēc tam atlasiet **Rādīt veikalu pieejamību**. Papildinformāciju par pieejamām konfigurācijas opcijām, skatiet sadaļā [Krājumu pieejamības aprēķināšana mazumtirdzniecības kanāliem](./calculated-inventory-retail-channels.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]