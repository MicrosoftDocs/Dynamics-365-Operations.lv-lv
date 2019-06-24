---
title: Nesenības, biežuma un naudas (RFM) analīzes iestatīšana
description: Šajā tēmā skaidrots, kā iestatīt nesenības, biežuma un naudas (RFM) analīzi jūsu debitoriem.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: MCRRFMDefinition
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78943
ms.assetid: 8ff9aac3-5ada-4150-85fd-18901c926d53
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: c7cb79fa82b579bee01e51cb635597cc5f711a98
ms.sourcegitcommit: e2fb0846fcc6298050a0ec82c302e5eb5254e0b5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/27/2019
ms.locfileid: "1606830"
---
# <a name="set-up-recency-frequency-and-monetary-rfm-analysis"></a>Nesenības, biežuma un naudas (RFM) analīzes iestatīšana

[!include [banner](includes/banner.md)]

Šajā tēmā skaidrots, kā iestatīt nesenības, biežuma un naudas (RFM) analīzi jūsu debitoriem.

Nesenības, biežuma un naudas (RFM) analīze ir mārketinga rīks, ko jūsu uzņēmums var izmantot, lai novērtētu datus, kas tiek ģenerēti no debitoru pirkumiem. Pēc RFM analīzes iestatīšanas debitoriem tiek piešķirts aprēķinātais RFM rezultāts, balstoties uz to pirkumiem. RFM rezultāts var būt trīsciparu vērtējums vai kopējs skaitlis, atkarībā no tā, kā jūsu organizācija ir konfigurējusi RFM analīzi. Tālāk aprakstīts, kā šis vērtējums darbojas, ja jūsu organizācija izmanto trīsciparu vērtēšanas rezultātu.

- Pirmais cipars ir debitora nesenības vērtējums — ik ilgs laiks ir pagājis, kopš debitors veica pirkumu no jūsu organizācijas.
- Otrais cipars ir debitora biežuma vērtējums — cik bieži debitors veic pirkumus no jūsu organizācijas.
- Trešais cipars ir debitora monetārais vērtējums — cik daudz debitors tērē, veicot pirkumus no jūsu organizācijas.

Piemēram, jūsu organizācija ir noteikusi vērtējumus skalā no 1 līdz 5, kur 5 ir visaugstākais vērtējums. Šajā gadījumā debitora vērtējums 535 sniedz šādu informāciju par debitoru:

- **Nesenības vērtējums 5** — debitors nesen veicis pirkumu.
- **Biežuma vērtējums 3** — debitors pērk preces no jūsu organizācijas ar vidēju biežumu.
- **Monetārais vērtējums 5** — veicot pirkumu, debitors iztērē ievērojamu naudas summu.

Ja jūsu organizācija vērtējumam izmanto apkopotos skaitļus, individuāli vērtējumi tiek summēti. Tajā pašā piemērā debitora vērtējums ir 13 (5 + 3 + 5).

## <a name="set-up-rfm-analysis-for-the-customers-in-your-organization"></a>Iestatīt RFM analīzi debitoriem jūsu organizācijā

1. Dodieties uz **Zvanu centrs** \> **Periodisks** \> **RFM analīze**.
2. Lapā **RFM analīže** atlasiet **Jauns**. Laukā **RFM definīcija** ievadiet RFM definīcijas nosaukumu. Piemēram, varat nosaukt definīciju par RFM-A.
3. Ievadiet sākuma datumu un beigu datumu šai RFM definīcijai.
4. Kopsavilkuma cilnē **Vispārīgi** izpildiet tālāk aprakstītos norādījumus.

    - Ja katrai RFM rezultāta sadaļai ir jāietver vienāds debitoru skaits, atzīmējiet izvēles rūtiņu **Vienmērīga sadale**.
    - Atzīmējiet izvēles rūtiņu **Saskaitīt rezultātus**, lai sasummētu visus trīs rezultātus. Šādi debitoram tiktu piešķirts RFM rezultāts, piemēram, 13, nevis 535.
    - Atzīmējiet izvēles rūtiņu **Saglabāt vēsturi**, lai pieprasītu sistēmai saglabāt debitoru statistiskos datus un šos datus varētu izmantot RFM rezultāta aprēķināšanai.

5. Kopsavilkuma cilnē **Nesenība** izpildiet tālāk aprakstītos norādījumus.

    - Laukā **Nodaļas** ievadiet nodaļu vai grupu skaitu, kas tiks izmantots debitoru nesenības rezultāta aprēķināšanai. Piemēram, ja jums ir 100 debitori, sadalījums 5 nodaļās, ka katram rezultātam ir 20 debitori. Tiem 20 debitoriem, kuri pirkumus veica pēdējie, nesenības rezultāts ir 5. Nākamajiem 20 debitoriem nesenības rezultāts ir 4 un tā tālāk. Ja jums ir 50 debitori, 10 debitoriem nesenības rezultāts ir 5, un 10 debitoriem nesenības rezultāts ir 4 un tā tālāk.
    - Laukā **Prioritāte** atlasiet, cik lielu svaru vēlaties piešķirt nesenības parametram salīdzinājumā ar pārējiem parametriem, aprēķinot debitora RFM rezultātu. Piemēram, varat piešķirt lielāku nozīmi nesenības rezultātam nekā naudas rezultātam.
    - Laukā **Reizinātājs** ievadiet vērtību, ar kuru reizināt nesenības rezultātu. Ja neievadāt vērtību, rezultāts netiks reizināts.
    - Lauka **Periods** atlasiet laika periodu, pēc kura tiek aprēķināts nesenības rezultāts. Piemēram, pa nedēļām vai mēnešiem.

6. Kopsavilkuma cilnē **Biežums** izpildiet tālāk aprakstītos norādījumus.

    - Laukā **Nodaļas** ievadiet nodaļu vai grupu skaitu, kas tiks izmantots debitoru biežuma rezultāta aprēķināšanai.
    - Laukā **Prioritāte** atlasiet, cik lielu svaru vēlaties piešķirt biežuma parametram salīdzinājuma ar pārējiem parametriem, aprēķinot debitora RFM rezultātu.
    - Laukā **Reizinātājs** ievadiet vērtību, ar kuru reizināt biežuma rezultātu. Ja neievadāt vērtību, rezultāts netiks reizināts.

7. Kopsavilkuma cilnē **Monetārs** izpildiet tālāk aprakstītos norādījumus.

    - Laukā **Nodaļas** ievadiet nodaļu vai grupu skaitu, kas tiks izmantots debitoru monetārā rezultāta aprēķināšanai.
    - Laukā **Prioritāte** atlasiet, cik lielu svaru vēlaties piešķirt monetārajam parametram salīdzinājuma ar pārējiem parametriem, aprēķinot debitora RFM rezultātu.
    - Laukā **Reizinātājs** ievadiet vērtību, ar kuru reizināt monetāro rezultātu. Ja neievadāt vērtību, rezultāts netiks reizināts.
    - Laukā **Bruto/neto** izvēlieties, vai, aprēķinot debitora monetāro rezultātu, ir jāizmanto rēķinā norādītā bruto vai neto summa.
    - Ja debitora atgriešanas summas ir jāatņem no debitora rēķina kopējā aprēķina, atzīmējiet izvēles rūtiņu **Atņemt atgriešanas vērtību**.

## <a name="view-a-customers-rfm-score"></a>Debitora RFM rādītāja skatīšana

Lai skatītu klienta RFM rādītāju, izmantojiet tālāk aprakstīto procedūru.

1. Dodieties uz **Zvanu centrs** \> **Žurnāli** \> **Klientu apkalpošana**.
2. Lapas **Klientu apkalpošana** rūtī **Klientu apkalpošana**, meklēšanas laukos atlasiet meklējamā atslēgvārda veidu un ievadiet meklējamo tekstu.
3. Atlasiet **Meklēt**.
4. Lapā **Debitora meklēšana** atlasiet nepieciešamo debitora ierakstu un pēc tam noklikšķiniet uz **Atlasīt debitoru**.

RFM rezultāts tiek rādīts lapas **Klientu apkalpošana** labajā pusē, grupā **Pasūtījumu vēsture**.

## <a name="view-or-clear-the-history-of-an-rfm-analysis-record"></a>RFM analīzes ierakstu skatīšana vai vēstures notīrīšana

Lai skatītu RFM analīzes ierakstus vai notīrītu vēsturi, izmantojiet tālāk aprakstīto procedūru.

1. Dodieties uz **Zvanu centrs** \> **Periodisks** \> **RFM analīze**.
2. Lapā **RFM analīze** atlasiet ierakstu, kuru vēlaties apskatīt.
3. Lai skatītu ierakstu vēsturi, atlasiet kopsavilkuma cilni **Vēsture**.
4. Lai notīrītu ieraksta vēsturi, atlasiet **Notīrīt vēsturi**.
