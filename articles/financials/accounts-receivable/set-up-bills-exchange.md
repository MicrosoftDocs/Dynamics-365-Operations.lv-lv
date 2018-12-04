---
title: "Iestatīt vekseļus"
description: "Šajā tēmā aprakstītas vekseļu iestatīšanas darbības."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 09/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustBillOfExchangeJour
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 269964
ms.assetid: f2077165-da90-4359-ab12-e05717728dc7
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: c9d6866bb994cb9fb411bdd6a9ccae0e67d2d6f3
ms.openlocfilehash: cda597b1d99e99ac5c5c396bcfcec9c0712f0eb1
ms.contentlocale: lv-lv
ms.lasthandoff: 09/17/2018

---

# <a name="set-up-bills-of-exchange"></a>Iestatīt vekseļus

[!include [banner](../includes/banner.md)]

Šajā tēmā aprakstītas vekseļu iestatīšanas darbības.

Vekselis ir rakstisks vai elektronisks pasūtījums no debitora, kurā norādīts, ka citai pusei, parasti bankai, ir uzņēmumam jāmaksā norādītā summa. Ja izmantojat vekseli kā maksājumu pārdošanas pasūtījuma rēķinam vai brīva teksta rēķinam, jūs kreditējat debitora kontu. Šo kredītu nodrošina vekselis, līdz debitors samaksā vekseli bankā. Parasti apmaksāsit rēķinu ar vekseli apmaksas datumā. Kad saņemat paziņojumu no savas bankas, ka vekselis ir izpirkts, varat aizvērt vekseli. Varat izrakstīt vekseli savā bankā jebkurā no šiem laikiem:

-   Apmaksas datumā. Šī pieeja ir pazīstama kā pārvedums apmaksai.
-   Pirms apmaksas datuma, parasti termiņatlaides datumā, kas norādīts maksājuma nosacījumos, kas iestatīti debitoram. Grāmatojot darījumu, atlaižu summa tiek grāmatota izmaksu kontā. Atlikusī summa ir saistības pret jums līdz brīdim, kad banka saņem samaksu no klienta. Šī pieeja ir pazīstama kā pārvedums termiņatlaidei.

## <a name="set-up-posting-profiles-for-bills-of-exchange"></a>Grāmatošanas profilu iestatīšana vekseļiem

Izmantojiet lapu **Debitoru grāmatošanas metodes**, lai iestatītu grāmatošanas metodes, kuras var izmantot ar vekseļiem, noraidītajiem vekseļiem, apmaksas pārskaitījumiem un atlaižu pārskaitījumiem. Laukā **Summu konts** atlasiet summu kontu, kurā grāmatot vekseļa summas. Šis konts tiek ieskaitīts debetā vai kredītā atkarībā no vekseļa darījuma tipa:
-   Vekseļiem šis konts tiek ierakstīts debetā, kad vekselis tiek grāmatots un tiek kreditēts, kad tiek grāmatots pārskaitījums termiņatlaidei vai pārskaitījums apmaksai.
-   Noraidītajiem vekseļiem šis konts tiek ierakstīts debetā, kad tiek grāmatots noraidījuma vekselis.
-   Apmaksai paredzētajiem pārskaitījumiem šis konts tiek ierakstīts debetā, kad tiek grāmatots pārskaitījums apmaksai.
-   Termiņatlaidei paredzētajiem pārskaitījumiem šis konts tiek ierakstīts debetā, kad tiek grāmatots pārskaitījums termiņatlaidei.

Laukā **Apmaksāt konta rēķinus** atlasiet kases kontu, kurā grāmatot vekseļa summas. Šis konts tiek ierakstīts debetā, kad ir apmaksāts vekselis. Laukā **PVN priekšapmaksām** atlasiet summu kontu, kurā grāmatot PVN summas, kad maksājumiem tiek izmantoti vekseļi. Laukā **Atlaižu konta saistības** atlasiet kontu, kurā grāmatot atlaides summu atlaides pārskaitījumiem. Šis konts tiek kreditēts, kad tiek grāmatots pārskaitījums termiņatlaidei.

## <a name="set-up-accounts-receivable-parameters-for-bills-of-exchange"></a>Vekseļu debitoru moduļa parametru iestatīšana

Lapā **Debitoru parametri** vekseļu noklusējuma grāmatošanas metodes tiek ievadītas cilnē **Virsgrāmata un PVN**. Numuru sērijas tiek definētas cilnē **Numuru sērijas**.

## <a name="set-up-journal-names-for-bills-of-exchange"></a>Vekseļu žurnālu nosaukumu iestatīšana


Lapā **Žurnālu nosaukumi** izveidojiet vismaz piecus žurnāla nosaukumus, ko izmantot vekseļiem. Tālāk ir norādīti žurnālu veidi.
-   **Debitora izrakstīts vekselis** — izveidojiet žurnāla nosaukumu vekseļu izrakstīšanas žurnālam.
-   **Debitora vekseļa noraidīšana** — izveidojiet žurnāla nosaukumu vekseļu noraidīšanas žurnālam.
-   **Atkārtoti izrakstīts debitora vekselis** — izveidojiet žurnāla nosaukumu atkārtotas vekseļu izrakstīšanas žurnālam.
-   **Debitora bankas pārskaitījums** — izveidojiet žurnāla nosaukumu pārskaitījumu žurnālam.
-   **Debitoru vekseļu apmaksa** — izveidojiet žurnāla nosaukumu vekseļu apmaksas žurnālam.

Žurnāla dokumentu lapā katram vekseļa žurnālam ievadiet informāciju par vekseli cilnē **Vekselis**. Kad vekseļa žurnāla rindas ir iegrāmatotas, varat tās apskatīt lapā **Vekseļu žurnāla pieprasījums**, kā arī lapā **Vekseļu statistika**.

## <a name="set-up-methods-of-payment-for-bills-of-exchange"></a>Vekseļu apmaksas veida iestatīšana

Lapā **Maksāšanas metodes** iestatiet vekseļiem vismaz vienu maksāšanas metodi. Ja sadarbojaties vairāk nekā ar vienu banku, iestatiet maksājuma veidu, kas atbilst pārveduma formātam, kuru katra banka pieprasa attiecībā uz vekseļiem.

## <a name="set-up-payment-fees-for-bills-of-exchange"></a>Vekseļa maksājumu papildmaksu iestatīšana

Maksājuma papildmaksa ir maksa, kas saistīta ar maksājumu iekasēšanas procesu no debitoriem. Ar katru maksājuma papildmaksu var būt saistītas vairākas maksājuma papildmaksas iestatījumu rindas. Varat izmantot iestatījumu rindas, lai kontrolētu to, kā noklusējuma maksājumu papildmaksu summas tiek aprēķinātas. Piemēram, varat izveidot iestatījumu rindas maksājumu veidiem, maksājumu specifikācijām, valūtām un laika periodiem. Varat arī izveidot iestatījumu rindas procentuālajam daudzumam vai summai, kas balstās uz dienu intervāliem. Piemēram, varat iestatīt procentu likmi, kas balstās uz laiku, par kādu maksājums ir nokavēts. Ja banka iekasē atšķirīgas papildmaksas par dažādiem pārskaitījumu veidiem, piemēram **Iekasēšana** vai **Atlaide**, iestatiet atsevišķu maksājuma papildmaksas rindu katram pārskaitījuma veidam.

## <a name="set-up-remittance-fees-for-bank-remittance-files"></a>Iestatiet pārskaitījuma papildmaksas bankas pārskaitījuma failiem

Lapā **Bankas konti** varat iestatīt pārskaitījuma papildmaksas, ko banka iekasē par katru izveidoto pārveduma failu. Pārskaitījumu papildmaksas tiek grāmatotas, kad pārvedums ir akceptēts un ir zināmas realizēto papildmaksu summas. Papildmaksas par pārskaitījumu atšķiras no maksājumu papildmaksām, kas iekasētas no debitoriem un ir pievienotas žurnāla rindām.

## <a name="set-up-document-layouts-for-bills-of-exchange"></a>Vekseļu dokumentu izkārtojumu iestatīšana

Lapā **Bankas konti** noklikšķiniet uz **Iestatīt** un norādiet dokumenta izkārtojumu, kas nepieciešams katram bankas kontam, kuram veidosit drukātus vekseļu dokumentus.

## <a name="set-up-customers-for-bills-of-exchange"></a>Vekseļu debitoru iestatīšana

Lapā **Debitori** katram debitoram, kas piekritis maksāt, izmantojot vekseli, varat iestatīt vekseļu maksājuma noklusējuma metodi cilnē **Maksājuma noklusējuma informācija**.






