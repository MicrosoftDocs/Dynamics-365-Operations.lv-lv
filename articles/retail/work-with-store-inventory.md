---
title: Veikala krājumu pārvaldība
description: Šajā tēmā ir aprakstīti dokumentu veidi, ko varat izmantot krājumu pārvaldībai.
author: rubencdelgado
manager: AnnBe
ms.date: 04/23/2019
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
ms.openlocfilehash: efc729c83b81bd8afb806c403d52fd85b36efc9d
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2019
ms.locfileid: "1523765"
---
# <a name="store-inventory-management"></a>Veikala krājumu pārvaldība

[!include [banner](includes/banner.md)]

Strādājot ar krājumiem programmā Dynamics 365 for Retail un izmantojot POS programmu, ir jāņem vērā, ka POS nodrošina ierobežotu atbalstu krājumu dimensijām un noteiktiem krājumu vienību tipiem.  

POS risinājums neatbalsta šādas krājumu konfigurācijas:
- MK krājumus (izņemot komplekta preces, kurās izmantoti daži MK struktūras komponenti)
- Pieļaujamā svara krājumus
- Partijās kontrolētus krājumus

POS programma pašlaik neatbalsta šādas izsekošanas dimensijas POS:
- Partijas izsekošanas dimensija
- Īpašnieka dimensija

POS risinājums nodrošina ierobežotu atbalstu šādām dimensijām. Ierobežots atbalsts norāda, ka POS var automātiski izmantot noklusējuma vērtības dažām no šīm dimensijām krājumu darbībās, pamatojoties uz noliktavas/veikala iestatījumu konfigurāciju. POS nenodrošinās pilnīgu atbalstu dimensijām tādā veidā, kādā tās tiek atbalstītas, ja pārdošanas transakcija ir manuāli ievadīta ERP. 

- **Noliktavas novietojums** — lietotājiem nebūs iespēju pārvaldīt saņemšanas noliktavas atrašanās vietu krājumiem, kas saņemti veikala noliktavā, kad veikals nav konfigurēts noliktavas pārvaldības procesa izmantošanai.  Šiem krājumiem tiks izmantota noklusējuma saņemšanas vieta, kas noteikta veikala noliktavā.  Ja veikalam ir iespējots noliktavas pārvaldības process, tiek aktivizēts ierobežots atbalsts, kas parāda lietotājam uzvedni, aicinot izvēlēties saņemšanas vietu attiecībā uz visu saņemto.  Veikalā pārdotie krājumi vienmēr tiks pārdoti no noklusējuma mazumtirdzniecības vietas, kā noteikts veikala noliktavas iestatījumos.   Krājumu atgriešanas pārvaldības atrašanās vietu var kontrolēt, izmantojot noklusējuma atgriešanas vietas definīciju veikala noliktavā vai pamatojoties uz atgriešanas pamatojuma kodiem, kas noteikti atgriešanas vietas politikā.
- **Numura zīme** — piemērojams tikai tad, ja krājumu un veikala noliktavā ir iespējots vienums **Izmantot noliktavas vadības procesus**.  Programmā POS, ja krājumi ir saņemti veikala noliktavā, kur ir iespējots noliktavas pārvaldības process, un vieta, kas izvēlēta, lai saņemtu krājumu, ir saistīta ar atrašanās vietas profilu, kam nepieciešama numura zīmes kontrole, POS lietojumprogramma sistemātiski lietos numura zīmi saņemšanas rindai.  Lietotājiem programmā POS nebūs iespēju mainīt vai pārvaldīt šos numura zīmes datus.   Ja ir nepieciešama pilna numura zīmju pārvaldīšana, veikalam ieteicams izmantot WMS mobilo lietojumprogrammu vai iekšējās uzskaites ERP klientu, lai pārvaldītu šo krājumu saņemšanu.
- **Sērijas numurs** — lietojumprogrammā POS ir ierobežots atbalsts atsevišķam sērijas numuram, kas ir jāreģistrē transakcijas pārdošanas rindā pasūtījumiem, kas izveidoti lietojumprogrammā POS ar serializētiem krājumiem.  Šis sērijas numurs nav pārbaudīts attiecībā pret reģistrētajiem sērijas numuriem, kas jau ir krājumos.  Ja pārdošanas pasūtījums tiek izveidots zvanu centra kanālā vai izpildīts ar ERP starpniecību un vairāki sērijas numuri ir reģistrēti vienā pārdošanas rindā ERP izpildes procesa laikā, šos sērijas numurus nevarēs lietot vai pārbaudīt, ja atgriešana šiem pasūtījumiem tiek apstrādāta lietojumprogrammā POS.
- **Krājumu statuss** — krājumiem, kas izmanto noliktavas pārvaldības procesu un kam nepieciešams krājumu statuss, šis statusa lauks nevar tikt iestatīts vai modificēts, izmantojot POS lietojumprogrammu.  Kad krājumi tiek saņemti krājumos, tiks izmantots noklusējuma krājumu statuss, kas noteikts veikala noliktavas konfigurācijā.  

> [!NOTE]
> Visām organizācijām ir jāpārbauda krājumu konfigurācijas, izmantojot POS izstrādes vai testēšanas vidē, pirms to izvietošanas ražošanā. Pārbaudiet krājumus, īstenojot parastus pārdošanas darījumus, kas veikti skaidrā naudā un bez piegādes, apstrādājot un izveidojot debitoru pasūtījumus (ja piemērojams) ar POS starpniecību ar jūsu krājumiem. Testēšanas ietvaros pilnībā jāizpilda izrakstu grāmatošanas procesi jūsu testēšanas vidē un jāpārbauda, vai nerodas problēmas.
> Krājumu konfigurēšana tādā veidā, ko neatbalsta POS programma, bez pienācīgas testēšanas var izraisīt kļūmes izrakstu grāmatošanas procesā ražošanas laikā, un problēmu novēršana būs apgrūtināta. Var izvērtēt iespējamos partneru vai debitoru pielāgojumus programmā, lai nodrošinātu šo grāmatošanas procesu veiksmīgu pabeigšanu. Ja pielāgošana nav nepieciešama, organizācijai ir jānodrošina, ka jūsu preču konfigurēšana ir veikta tādā veidā, ko atbalsta standarta POS programma/pasūtījumu izveidošana/izrakstu grāmatošanas process.

## <a name="purchase-orders"></a>Pirkšanas pasūtījumi

Pirkšanas pasūtījumi tiek izveidoti galvenajā birojā. Ja pirkšanas pasūtījuma virsrakstā ir iekļauta mazumtirdzniecības noliktava, pasūtījumu var saņemt veikalā, izmantojot programmu Modern POS (MPOS) vai Cloud POS pakalpojumā Microsoft Dynamics 365 for Retail ar operācijas **Izdošana/saņemšana** starpniecību. Kad noliktavā saņemtie daudzumi tiek ievadīti lietojumprogrammas POS laukā **Saņemt tūlīt** attiecīgajam pirkšanas pasūtījuma dokumentam, tie var tikt saglabāti lokāli vai iesniegti. Saglabājot šos datus lokāli, noliktavā esošie krājumi netiek ietekmēti. Saglabāšana ir jāveic tikai tad, ja lietotājs nav gatavs grāmatot kvīti datu bāzē HQ un vēlas tikai īslaicīgi saglabāt iepriekš ievadītos darbības **Saņemt tūlīt** datus.  Šādā veidā ar saņemšanu tagad saistītie dati tiek saglabāti lokāli lietotāja kanāla datu bāzē. Pēc tam, kad dokuments tiek apstrādāts, izmantojot opciju **Iesniegt**, dati **Saņemt tūļīt** tiek nosūtīti uz datu bāzi HQ, un tiek grāmatota pirkšanas pasūtījuma saņemšana. 

## <a name="transfer-orders"></a>Pārsūtīšanas pasūtījumi

Pārsūtīšanas pasūtījumā var norādīt, ka konkrētais veikals ir vieta, no kuras krājumi var tikt nosūtīti, vai vieta, kurā tiks saņemti krājumi. Ja POS lietotājs ir pārsūtīšanas pasūtījuma nosūtīšanas noliktava, tas varēs ievadīt **Nosūtīt tūlīt** daudzumus no lietojumprogrammas POS.  Nosūtīšanas veikala ievadītos datus var saglabāt lokāli vai iesniegt.  Saglabājot lokāli, pārsūtīšanas pasūtījuma dokumentā datu bāzē HQ netiek veikts neviens atjauninājums. Saglabāšana ir jāveic tikai tad, ja lietotājs nav gatavs grāmatot sūtījumu datu bāzē HQ un vēlas tikai īslaicīgi saglabāt iepriekš ievadītos darbības **Nosūtīt tūlīt** datus. Kad veikals ir gatavs sūtījuma apstiprināšanai, ir jāatlasa opcija **Iesniegt**. Tādējādi pārsūtīšanas pasūtījuma sūtījums tiek iegrāmatots datu bāzē HQ, lai saņemšanas noliktava tagad varētu saņemt vienumus attiecībā uz to. 

Ja POS lietotājs ir pārsūtīšanas pasūtījuma saņemšanas noliktava, tas varēs ievadīt **Saņemt tūlīt** daudzumus no lietojumprogrammas POS.  Saņemšanas veikala ievadītos datus var saglabāt lokāli vai iesniegt. Saglabāšana ir jāveic tikai tad, ja lietotājs nav gatavs grāmatot kvīti datu bāzē HQ un vēlas tikai īslaicīgi saglabāt iepriekš ievadītos darbības **Saņemt tūlīt** datus. Šādā veidā ar saņemšanu tagad saistītie dati tiek saglabāti lokāli lietotāja kanāla datu bāzē. Pēc tam, kad dokuments tiek apstrādāts, izmantojot opciju **Iesniegt**, dati **Saņemt tūļīt** tiek nosūtīti uz datu bāzi HQ, un tiek grāmatota pārsūtīšanas pasūtījuma saņemšana. Ir svarīgi atzīmēt, ka saņemšanas veikalam ir ierobežojums un tas var iesniegt tikai saņemšanas daudzumus, kas ir vienādi ar vai mazāki par nosūtītajiem daudzumiem. Mēģinājums saņemt daudzumus pārsūtīšanas pasūtījumā, kas iepriekš nav nosūtīti, izraisīs kļūdas, un saņemšana netiks apstiprināta datu bāzē HQ.

## <a name="stock-counts"></a>Krājumu uzskaite

Krājumu uzskaites var būt plānotas vai neplānotas. Plānotas krājumu uzskaites tiek uzsāktas galvenajā birojā, kurš norāda uzskaitāmos krājumus. Galvenajā birojā tiek izveidots uzskaites dokuments, ko var saņemt veikalā, kurā faktisko rīcībā esošo krājumu daudzumi ir ievadīto programmā MPOS vai Cloud POS. Veikalā tiek sākta neplānota krājumu uzskaite, programmā MPOS vai Cloud POS tiek atjaunināti faktisko rīcībā esošo krājumu daudzumi. Atšķirībā no ieplānotās krājumu uzskaites neplānotajai krājumu uzskaitei netiek lietots iepriekš definēts krājumu saraksts. Kad abu tipu krājumu uzskaite ir pabeigta, tā tiek fiksēta un nosūtīta uz galveno biroju. Galvenajā birojā uzskaite tiek pārbaudīta un iegrāmatota kā atsevišķa darbība.

## <a name="inventory-lookup"></a>Krājumu pārlūkošana

Pašreizējo rīcībā esošo preču daudzumu vairākiem veikaliem un noliktavām var skatīt lapā **Krājumu meklēšana**. Papildus pašreizējam rīcībā esošajam daudzumam katram atsevišķajam veikalam var skatīt arī turpmākos solīšanai pieejamos (ATP) daudzumus. Lai to izdarītu, atlasiet veikalu, kuram vēlaties skatīt ATP, un pēc tam noklikšķiniet uz **Rādīt veikala pieejamību**.
