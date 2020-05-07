---
title: Projekta piešķīrumi
description: Šajā tēmā ir paskaidrots, kā izveidot vai pārveidot piešķīrumu.
author: RadhikaRS
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: f4f7d347dab9f02fc474656e2f4cfba8e374480d
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282838"
---
# <a name="project-grants"></a>Projekta piešķīrumi

[!include [banner](../includes/banner.md)]

Piešķīrums ir naudas dāvinājums noteiktam mērķim vai projektam. Parasti pastāv ierobežojumi tam, kā piešķīrumus var tērēt. Projekta vadības un uzskaites sadaļā varat ievadīt un izsekot piešķīrumus un noteikt to attiecības ar projektiem un projektu līgumiem. Piemēram, varat veikt šādus uzdevumus:

- Saistiet piešķīrumus ar projektiem un finansējuma avotiem, izmantojot saites uz **Projektu** un **Projekta līguma informācijas** lapām.
- Ievadiet un izsekojiet izmaiņas piešķīrumiem, kad tie pāriet no viena statusa uz citu.
- Ievadiet un izsekojiet izmaksas, pieprasītās summas un piešķirtās summas.
- Izveidojiet galvenos piešķīrumus un piesaistiet tiem pakārtotos piešķīrumus.

Piešķīrumu varat izveidot, ievadot visu informāciju jaunā ierakstā, vai varat kopēt un modificēt datus no esoša piešķīruma un tad tos atjaunināt.

## <a name="create-a-new-grant"></a>Izveidot jaunu dotāciju

1. Dodieties uz **Projekta vadība un uzskaite** \> **Piešķīrumi** \> **Piešķīrumi**.
2. Atlasiet **Jauns** \> **Piešķīrums**.
3. Piešķīruma informācijas lapā, kopsavilkuma cilnē **Vispārīgi**, laukā **Piešķīruma ID** ievadiet piešķīruma burtciparu identifikatoru.
4. Laukā **Piešķīruma nosaukums** piešķīrumam ievadiet nosaukumu.
5. Laukā **Apraksts** pievienojiet informāciju par jauno piešķīrumu.

    Vairums citu lauku lapā ir neobligāti, un varat ievadīt tik daudz vai tik maz informācijas, cik vien vēlaties.

    Sekojošajā sarakstā ir aprakstīta informācija, kas ir norādīta katrā piešķīruma informācijas lapas kopsavilkuma cilnē:

    - **Vispārīgi** – Ievadiet informāciju par piešķīruma nosaukumu, statusu, aprakstu, mērķi un summu.
    - **Kontakta informācija** – Ievadiet detalizētu informāciju par personāla locekļiem un nodaļu, kas pārvalda šo piešķīrumu, un piešķīruma debitoru vai organizāciju, kas ir piešķīruma avots. Varat arī norādīt, vai jūsu organizācijai ir tranzīta juridiskā persona, kas saņem piešķīrumu un pēc tam to nodod citam saņēmējam. Atlasiet **Pievienot**, lai pievienotu kontaktinformāciju, piemēram, tālruņa numurus un e-pasta adreses organizācijai, kas nodrošina šo piešķīrumu.
    - **Datumi un termiņi** – ievadiet datumus, kas ir saistīti ar piešķīrumu un piešķīruma lietojumu. Kā piemērus var minēt programmas apmaksas datumu, iesniegšanas datumu un datumu, kad piešķīrums ir apstiprināts vai noraidīts.
    - **Saistītie projekti un projekta līgumi** — jūs varat ievadīt informāciju šajā kopsavilkuma cilnē tikai tad, ja lauka **Piešķīruma statuss** statuss kopsavilkuma cilnē **Vispārīgi** ir iestatīts uz **Aktīvs** vai **Piešķirts**. Atlasiet vienu no šīm opcijām, lai pabeigtu saistīto uzdevumu:

        - **Pievienot finansējuma avotu** – pievienot piešķīrumam jaunu finansējuma avotu. Jūs varat ievadīt visas detaļas tagad vai izmantot noklusēto informāciju un tad atjaunināt vēlāk.
        - **Pievienot projekta līgumu** — pievienojiet vai atjauniniet projekta līguma informāciju.
        - **Pievienot projektu** – pievienot vai atjaunināt projekta detaļas.

    - **Iestatījumi** — ievadiet informāciju par salīdzināšanas līdzekļiem, ja šī informācija ir obligāta. Daudzas organizācijas, kas sniedz piešķīrumus, pieprasa, lai saņēmēji iztērētu noteiktu daudzumu savas naudas vai resursu atbilstoši piešķīrumā sniegtajam daudzumam. Laukā **Vietējais projekts vai izsekošanas ID** varat ievadīt identifikatoru, kas atšķiras no projekta identifikatora.

        > [!NOTE]
        > Ja daļa no piešķīruma tiks piešķirta citai organizācijai, iestatiet opciju **Apakšpiešķīrējs** uz **Jā**. Amerikas Savienotajās valstīs sniegtajiem piešķīrumiem var norādīt, vai piešķīrums tiks sniegts saskaņā ar valsts vai federālo pilnvarojumu.

    - **Izņemšanas detaļas** – pievienojiet vai atjauniniet informāciju par to, cik bieži piešķirtos līdzekļus var izņemt, par tiem izrakstīt rēķinu vai iztērēt.

## <a name="create-a-new-grant-from-a-copy"></a>Izveidot jaunu piešķīrumu no kopijas

1. Dodieties uz **Projekta vadība un uzskaite** \> **Piešķīrumi** \> **Piešķīrumi**.
2. Atlasiet **Jauns**\> **Kopēt no piešķīruma**.
3. Ievadiet burtciparu identifikatoru un nosaukumu jaunajam piešķīrumam un pēc tam atlasiet **Labi**.
4. Piešķīruma informācijas lapā pārskatiet kopētā piešķīruma informāciju un veiciet visas nepieciešamās izmaiņas. Lielākā daļa lauku lapā nav obligāta.

## <a name="view-or-modify-grant-details"></a>Skatīt vai mainīt piešķīruma informāciju

1. Dodieties uz **Projekta vadība un uzskaite** \> **Piešķīrumi** \> **Piešķīrumi**.
2. Atlasiet piešķīrumu, ko paredzēts mainīt.
3. Darbību rūts cilnē **Piešķīrums**, grupā **Uzturēt** atlasiet **Rediģēt**.
4. Pārskatiet piešķīruma detaļas un veiciet nepieciešamās izmaiņas.
