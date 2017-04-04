---
title: "Iestatīt vekseļus"
description: "Šajā tēmā aprakstīti soļi iestatīšana vekseļiem."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269964
ms.assetid: f2077165-da90-4359-ab12-e05717728dc7
ms.search.region: global
ms.author: abruer
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: ce2142d946085d8bfc577accf1bb31a89ea29156
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-bills-of-exchange"></a>Iestatīt vekseļus

Šajā tēmā aprakstīti soļi iestatīšana vekseļiem.

Vekselis ir rakstiski vai elektroniski pasūtījuma no klienta, kas norāda, ka cita puse, parasti banka, būtu uzņēmumam maksā norādīto summu. Ja izmantojat vekseli kā maksājumu pārdošanas pasūtījuma rēķinam vai brīva teksta rēķinam, jūs kreditējat debitora kontu. Šo kredītu nodrošina vekselis, līdz debitors samaksā vekseli bankā. Parasti būs iestatīt rēķinu ar vekseļa apmaksas datumā. Kad saņemat paziņojumu no savas bankas, ka vekselis ir izpirkts, varat aizvērt vekseli. Jūs varat izdarīt vekseļa caur jūsu bankas vienā no šādām reizēm:

-   Apmaksas datumā. Šī pieeja ir pazīstama kā kompetences iegūšanai.
-   Pirms noteiktā termiņa, parasti atlaides datumā, kas norādīts maksāšanas termiņi, kas iestatīti klientam. Grāmatojot darījumu, atlaižu summa tiek grāmatota izmaksu kontā. Atlikusī summa ir saistības pret jums līdz brīdim, kad banka saņem samaksu no klienta. Šī pieeja ir pazīstama kā kompetences atlaidei.

## <a name="set-up-posting-profiles-for-bills-of-exchange"></a>Grāmatošanas profilu iestatīšana vekseļiem
Izmantojiet **debitora grāmatošanas profiliem** lapu, lai iestatītu grāmatošanas metodes, ko var lietot ar vekseļiem, vekseļu protesta, pārvedumiem savākšanai un atlaides pārskaitījumiem. Šajā **kopsavilkuma konts** lauku, atlasiet kopsavilkuma konts, kurā jāgrāmato vekseļu summas. Šī konta debetā vai kredītā, atkarībā no tā, kāda veida vekseļa darbība:
-   Vekseļiem, šis konts tiek debetēts, ja Vekselis ir ievietojis, un kreditē, grāmatojot pārskaitījuma atlaidei vai pārskaitījumu savākšanai.
-   Noraidītajiem vekseļiem šis konts tiek ierakstīts debetā, kad tiek grāmatots noraidījuma vekselis.
-   Apmaksai paredzētajiem pārskaitījumiem šis konts tiek ierakstīts debetā, kad tiek grāmatots pārskaitījums apmaksai.
-   Termiņatlaidei paredzētajiem pārskaitījumiem šis konts tiek ierakstīts debetā, kad tiek grāmatots pārskaitījums termiņatlaidei.

Šajā **nosegtu kontu** lauku, izvēlieties kases kontu, lai grāmatotu vekseļu summas. Šis konts tiek ierakstīts debetā, kad ir apmaksāts vekselis. Šajā **PVN priekšapmaksas** lauku, atlasiet kopsavilkuma konts, kurā jāgrāmato PVN summas, kad vekseļi tiek izmantoti priekšapmaksu. Šajā **pasīvi uz atlaižu rēķina** lauku, atlasiet kontu, lai grāmatotu atlaižu summu pārskaitījumiem atlaidi. Šis konts tiek kreditēts, kad tiek grāmatots pārskaitījums termiņatlaidei.

## <a name="set-up-accounts-receivable-parameters-for-bills-of-exchange"></a>Iestatiet kontu saņemamajiem parametriem vekseļiem
Par **Accounts receivable parameters** lappušu noklusējuma grāmatošanas metodes, lai vekseļi tiek ievadītas **Virsgrāmata un PVN** tab. Numuru sērijas, ir definētas **numuru sērijas** tab.
Vekseļu žurnālu nosaukumu iestatīšana
------------------------------------------

Par **žurnālu nosaukumus** lapu, izveidot vismaz pieci žurnāli izmantot vekseļus. Piedāvājam žurnāla tipos:
-   **Klienta vekseļa izrakstīšana** – izveidojiet žurnāla nosaukumu Draw vekseļu žurnāls.
-   **Klienta protestēt vekseli** – izveidojiet žurnāla nosaukumu protesta vekseļu žurnāls.
-   **Klienta atjaunošanos vekseļa** – izveidojiet žurnāla nosaukumu atjaunošanos vekseļu žurnāls.
-   **Debitora bankas pārskaitījums** – izveidojiet pārskaitījumu žurnāla žurnāla nosaukumu.
-   **Klienta nokārtot vekseļa** – izveidojiet žurnāla nosaukumu nokārtot vekseļu žurnāls.

Žurnāla dokumenta lappuses katrā vekseļu žurnāls, ievadiet informāciju par vekseļu **vekseļa** tab. Pēc vekseļa žurnāla rindas iegrāmatošanas, jūs varat apskatīt tos **vekseļu žurnāls izmeklēšanas** lapu un **Vekseļu statistika** lapā.
Vekseļu apmaksas veida iestatīšana
-----------------------------------------------

Par **maksāšanas** lapu, izveidot vismaz vienu maksāšanas metodi vekseļus. Ja sadarbojaties ar vairāk nekā vienu bankas pārskaitījuma formātu katrai bankai ir nepieciešama vekseļiem, kas atbilst maksājumu veidu iestatīšana.
Vekseļa maksājumu papildmaksu iestatīšana
-----------------------------------------

Maksājuma papildmaksa ir maksa, kas saistīta ar maksājumu iekasēšanas procesu no debitoriem. Rindas var būt vairākas Komisijas maksu iestatījumi saistīta katra Komisijas maksu. Var vadīt kā noklusējuma maksu summas tiek aprēķinātas, izmantojot iestatīšanas līnijām. Piemēram, varat izveidot iestatījumu rindas maksājumu veidiem, maksājumu specifikācijām, valūtām un laika periodiem. Varat arī izveidot uzstādīšanas rindas procenti vai summa, kas ir balstīta uz dienu starplaiku. Piemēram, varat iestatīt procentu likme, kas balstīta uz laiku ir nokavēts maksājums. Ja Banka iekasē dažādas nodevas dažādiem pārskaitījumu tipiem, piemēram, **kolekcijas** vai **Discount**, iestatiet atsevišķu maksājumu maksa rindu katram pārskaitījuma veidam.
Iestatiet pārskaitījuma papildmaksas bankas pārskaitījuma failiem
------------------------------------------------

Par **bankas kontiem** lapu, varat iestatīt pārskaitījuma izmaksas, kas bankai maksu par katru pārskaitījumu fails, kas tiek ģenerēts. Pārskaitījumu papildmaksas tiek grāmatotas, kad pārvedums ir akceptēts un ir zināmas realizēto papildmaksu summas. Pārskaitījuma maksas atšķiras no Komisijas maksām, ko iekasē no klientiem un pievienoti žurnāla rindas.
Vekseļu dokumentu izkārtojumu iestatīšana
---------------------------------------------

Par **bankas kontiem** lapu, noklikšķiniet uz **iestatīt**, un norādiet dokumenta izkārtojumu, kas ir nepieciešams, katram bankas kontam, jums radīs drukātā vekseļu dokumentiem par.
Vekseļu debitoru iestatīšana
--------------------------------------

Par **klientiem** lapas, katram klientam, kurš ir piekritis maksāt, izmantojot vekseli, var iestatīt noklusēto maksāšanas veidu vekseļiem **maksājumu saistību nepildīšanas** tab.




