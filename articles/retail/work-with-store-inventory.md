---
title: Veikala krājumu pārvaldība
description: Šajā tēmā ir aprakstīti dokumentu veidi, ko varat izmantot krājumu pārvaldībai.
author: rubencdelgado
manager: AnnBe
ms.date: 01/18/2019
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
ms.openlocfilehash: 02f8afbe3bb6f94c66a8b5aa02531c219adc3963
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "339238"
---
# <a name="store-inventory-management"></a>Veikala krājumu pārvaldība

[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīti dokumentu veidi, ko varat izmantot krājumu pārvaldībai.

Lai pārvaldītu savas organizācija krājumus, varat izmantot tālāk uzskaitītos dokumentu tipus.

Strādājot ar krājumiem programmā Dynamics 365 for Retail un izmantojot POS programmu, ir jāņem vērā, ka POS nodrošina ierobežotu atbalstu krājumu dimensijām un noteiktiem krājumu vienību tipiem.  

POS risinājums neatbalsta šādas krājumu konfigurācijas:
- MK krājumus (izņemot komplekta preces, kurās izmantoti daži MK struktūras komponenti)
- Pieļaujamā svara krājumus
- Partijās kontrolētus krājumus

POS programma pašlaik neatbalsta šādas izsekošanas dimensijas POS:
- Partijas izsekošanas dimensija
- Īpašnieka dimensija

POS risinājums nodrošina ierobežotu atbalstu šādām dimensijām. Ierobežots atbalsts norāda, ka POS var automātiski izmantot noklusējuma vērtības dažām no šīm dimensijām krājumu darbībās, pamatojoties uz noliktavas/veikala iestatījumu konfigurāciju. POS nenodrošinās pilnīgu atbalstu dimensijām tādā veidā, kādā tās tiek atbalstītas, ja pārdošanas transakcija ir manuāli ievadīta ERP. 

- Vieta
- Numura zīme (piemērojams tikai tad, ja krājumu un veikala noliktavā ir iespējots vienums **Izmantot noliktavas vadības procesus**)
- Sērijas numurs
- Krājumu statuss

> [!NOTE]
> Visām organizācijām ir jāpārbauda krājumu konfigurācijas, izmantojot POS izstrādes vai testēšanas vidē, pirms to izvietošanas ražošanā. Pārbaudiet krājumus, īstenojot parastus pārdošanas darījumus, kas veikti skaidrā naudā un bez piegādes, apstrādājot un izveidojot debitoru pasūtījumus (ja piemērojams) ar POS starpniecību ar jūsu krājumiem. Testēšanas ietvaros pilnībā jāizpilda izrakstu grāmatošanas procesi jūsu testēšanas vidē un jāpārbauda, vai nerodas problēmas.
> Krājumu konfigurēšana tādā veidā, ko neatbalsta POS programma, bez pienācīgas testēšanas var izraisīt kļūmes izrakstu grāmatošanas procesā ražošanas laikā, un problēmu novēršana būs apgrūtināta. Var izvērtēt iespējamos partneru vai debitoru pielāgojumus programmā, lai nodrošinātu šo grāmatošanas procesu veiksmīgu pabeigšanu. Ja pielāgošana nav nepieciešama, organizācijai ir jānodrošina, ka jūsu preču konfigurēšana ir veikta tādā veidā, ko atbalsta standarta POS programma/pasūtījumu izveidošana/izrakstu grāmatošanas process.

## <a name="purchase-orders"></a>Pirkšanas pasūtījumi

Pirkšanas pasūtījumi tiek izveidoti galvenajā birojā. Ja pirkšanas pasūtījuma virsrakstā ir iekļauta mazumtirdzniecības noliktava, pasūtījumu var saņemt veikalā, izmantojot programmu Modern POS (MPOS) vai Cloud POS programmatūrā Microsoft Dynamics 365 for Retail. Pēc veikalā saņemto daudzumu ievadīšanas tos var lokāli saglabāt papildu modifikāciju veikšanai. Alternatīvi daudzumus var fiksēt un nosūtīt uz galveno biroju. Galvenajā birojā veikalā saņemtie daudzumi tiek rādīti programmatūrā Dynamics 365 for Retail, pirkšanas pasūtījuma laukā **Saņemt tūlīt**.

## <a name="transfer-orders"></a>Pārsūtīšanas pasūtījumi

Pārsūtīšanas pasūtījums var norādīt, ka konkrēts veikals ir novietojums, no kura krājumus var sūtīt. Šādā gadījumā pārsūtīšanas pakalpojums veikalos tiek rādīts kā izdošanas pieprasījums programmā MPOS vai Cloud POS. Pēc pieprasīto daudzumu izdošanas tie tiek fiksēti un nosūtīti uz centrālo biroju. Galvenajā birojā veikalā izdotie daudzumi tiek rādīti programmatūrā Dynamics 365 for Retail, pārsūtīšanas pasūtījuma laukā **Nosūtīt tūlīt**. Pārsūtīšanas pasūtījums var norādīt, ka konkrēts veikals ir novietojums, uz kuru krājumus var sūtīt. Šādā gadījumā pārsūtīšanas pakalpojums veikalos tiek rādīts kā saņemšanas pieprasījums programmā MPOS vai Cloud POS. Pēc veikalā saņemto daudzumu ievadīšanas tos var lokāli saglabāt papildu modifikāciju veikšanai. Alternatīvi daudzumus var fiksēt un nosūtīt uz galveno biroju. Galvenajā birojā veikalā saņemtie daudzumi tiek rādīti programmatūrā Dynamics 365 for Retail, pārsūtīšanas pasūtījuma laukā **Saņemt tūlīt**.

## <a name="stock-counts"></a>Krājumu uzskaite

Krājumu uzskaites var būt plānotas vai neplānotas. Plānotas krājumu uzskaites tiek uzsāktas galvenajā birojā, kurš norāda uzskaitāmos krājumus. Galvenajā birojā tiek izveidots uzskaites dokuments, ko var saņemt veikalā, kurā faktisko rīcībā esošo krājumu daudzumi ir ievadīto programmā MPOS vai Cloud POS. Veikalā tiek sākta neplānota krājumu uzskaite, programmā MPOS vai Cloud POS tiek atjaunināti faktisko rīcībā esošo krājumu daudzumi. Atšķirībā no ieplānotās krājumu uzskaites neplānotajai krājumu uzskaitei netiek lietots iepriekš definēts krājumu saraksts. Kad abu tipu krājumu uzskaite ir pabeigta, tā tiek fiksēta un nosūtīta uz galveno biroju. Galvenajā birojā uzskaite tiek pārbaudīta un iegrāmatota.

## <a name="inventory-lookup"></a>Krājumu pārlūkošana

Pašreizējo rīcībā esošo preču daudzumu vairākiem veikaliem un noliktavām var skatīt lapā Krājumu uzmeklēšana. Papildus pašreizējam rīcībā esošajam daudzumam katram atsevišķajam veikalam var skatīt arī turpmākos solīšanai pieejamos (ATP) daudzumus. Lai to izdarītu, atlasiet veikalu, kuram vēlaties skatīt ATP, un pēc tam noklikšķiniet uz **Rādīt veikala pieejamību**.
