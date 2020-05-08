---
title: Tādu kreditoru maksājumu iestatīšana un lietošana, kas jāapmaksā pēc apmaksas
description: Šajā tēmā skaidrots, kā izveidot Apmaksāt pēc apmaksas (PWP) noteikumus, lai varētu izlaist daļējus kreditoru maksājumus, pamatojoties uz debitoru maksājumiem.
author: RadhikaRS
manager: AnnBe
ms.date: 03/30/2020
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
ms.openlocfilehash: 390cec62d2790ed10892669e283f2283c6b8e686
ms.sourcegitcommit: 399f128d90b71bd836a1c8c0c8c257b7f9eeb39a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/23/2020
ms.locfileid: "3284117"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Tādu kreditoru maksājumu iestatīšana un lietošana, kas jāapmaksā pēc apmaksas

[!include [banner](../includes/banner.md)]

Kad darbam kā apakšuzņēmēju apstiprināt kādu kreditoru, iespējams, maksājumu šim kreditoram vēlaties ieturēt, līdz debitors jums ir samaksājis par projektu. Lai atbalstītu šo scenāriju, jūs varat iestatīt nosacījumus Apmaksāt pēc apmaksas (PWP), kad iestatāt pirkšanas pasūtījumu (PP) ar kreditoru.

Piemēram, kad debitors samaksā kādu summu par projekta rēķinu, varat apmaksai atbrīvot daļu no kreditoru rēķiniem vai visu rēķinu summu. Vienkārši iestatiet PWP nosacījumus, kas norāda, ka kreditoram tiks samaksāts pēc tam, kad saņemat procentuālo daudzumu no saistītā debitora maksājuma. Ja saņemat daļēju maksājumu no debitora, varat maksājumam manuāli atbrīvot daļu no saistītajiem kreditoru rēķiniem.

Šajā piemērā tiek ieskicēts process, kad tiek izmantoti PWP nosacījumi.

## <a name="example"></a>Paraugs

Jūsu organizācija piekrīt nodrošināt debitoru ar 100 datoriem, kuros ir instalēta programmatūra, par cenu 150,- ASV dolāri (USD) par vienu datoru. Pēc tam varat nolīgt kreditoru, lai sniegtu jums datorus, kuros ir instalēta programmatūra. Saskaņā ar vienošanos klientam ir jāapstiprina datora kvalitāte, pirms viņš samaksā jūsu organizācijai. Jūsu organizācijas politika ir ieturēt maksājumus kreditoriem, līdz debitors jums ir samaksājis. Tāpēc iestatiet projektu tā, lai tā PWP procentuālā vērtība ir 100 procenti.

Kreditors sūta jums 100 datorus, kuros ir instalēta programmatūra, kopā ar rēķinu par 10 000,00 USD. Tā kā PWP nosacījumi ir iestatīti jūsu projektam, jūs nemaksājat kreditoram, saņemot datorus. Tā vietā jūs sūtat datorus klientam kopā ar rēķinu par 15 000,00. Debitors pārbauda datorus un apstiprina projekta rēķina pilnu summu.

Kad saņemat pilno maksājumu no debitora, jūs kreditoram samaksājat 10 000,00 - kreditora rēķinu pilnā apmērā.

## <a name="set-up-pwp-terms-for-a-project"></a>Iestatīt PWP nosacījumus attiecībā uz projektu

Iestatot PWP nosacījumus projektam, jums ir jānorāda minimālā summa, kas klientam ir jāmaksā jums par projektu, pirms Jūs maksājat kreditoram. Sliekšņa summu aprēķina automātiski par debitora rēķiniem, ko izveidojat projektam. Lai iestatītu sliekšņa procentu PWP nosacījumiem, veiciet tālāk norādītās darbības.

1. Dodieties uz **Projektu vadība un uzskaite** \> **Projekti** \> **Visi projekti**.
2. Atrodiet un atveriet projektu, kuram vēlaties iestatīt PWP nosacījumus.
3. Kopsavilkuma cilnē **Kreditora līgumi** atlasiet **Pievienot rindu**.
3. Laukā **Konta kods** atlasiet kādu no šādām opcijām:

    - **Tabula** — PWP nosacījumi attiecas uz vienu kreditoru.
    - **Grupa** — PWP nosacījumi attiecas uz visiem kreditoriem kreditoru grupā.
    - **Visi** — PWP nosacījumi attiecas uz visiem kreditoriem.

4. Ja iepriekšējā solī atlasījāt **Tabula** vai **Grupa**, laukā **Kreditors/kreditora grupa** atlasiet kreditoru vai kreditoru grupu, uz kuru attiecas PWP nosacījumi. Ja iepriekšējā solī atlasījāt **Visi**, lauku **Kreditors/kreditoru grupa** nevar rediģēt.
5. Ja kreditoram projektā ir iestatīti arī kreditora aizturēšanas nosacījumi, laukā **Kreditora aizturēšanas nosacījumi** atlasiet aizturēšanas nosacījumu kārtulas ID.
6. Laukā **PWP sliekšņa procents** ievadiet sliekšņa procentuālo vērtību projektam. Procentuālā vērtība, ko ievadāt projektam, definē minimālo summu, ko debitoram jums ir jāsamaksā, pirms jūs maksājat kreditoram.

## <a name="create-a-po-that-has-pwp-terms"></a>Izveidot PP ar PWP nosacījumiem

Kad grāmatojat rēķinu no kreditora, ja kreditors ir pakļauts PWP nosacījumiem, šie nosacījumi tiek parādīti PP rindās. Lai izveidotu PP, kam ir PWP nosacījumi, veiciet tālāk norādītās darbības.

1. Dodieties uz **Sagāde un avoti** \> **Pirkšanas pasūtījumi** \> **Visi pirkšanas pasūtījumi**.
2. Darbību rūtī atlasiet **Jauns**. Pēc tam dialoglodziņā **Izveidot pirkšanas pasūtījumu** ievadiet nepieciešamo informāciju un atlasiet **Labi**.

    Varat arī atvērt esošo PP **Visu pirkšanas pasūtījumu** saraksta lapā.

4. Lapā **Pirkšanas pasūtījums**, kopsavilkuma cilnē **Pirkšanas pasūtījuma rindas** pārskatiet kreditora PP rindas informāciju. Opcija **Apmaksāt pēc apmaksas** tiek automātiski atlasīta, un vērtība **PWP sliekšņa procents** tiek automātiski kopēta no lauka **PWP sliekšņa procents** lapā **Projekti**.
6. Ja nevēlaties, lai kreditoram tiktu attiecināti PWP nosacījumi uz PO rindu, noņemiet **Apmaksāt pēc apmaksas** opciju. Šādā gadījumā **PWP sliekšņa procentuālā vērtība** lauks PP rindai tiks atiestatīts uz 0 (nulli).

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Debitora maksājuma atjaunināšana un samaksa kreditoram

Ja kreditors pabeidz darbu pie projekta un nosūta jums rēķinu, jums jāpārskata projekta statuss un debitora rēķini, lai noteiktu, vai projekts atbilst PWP nosacījumiem. Ja kreditors ir izpildījis PWP nosacījumus, varat noteikt, kuras kreditora rēķina rindas ir jāapmaksā, pamatojoties uz projekta debitora maksājumiem. Ja izlemjat samaksāt kreditoram, pat ja PWP nosacījumi netika izpildīti, varat ignorēt PWP nosacījumus lapā **Kreditora rēķins ar apmaksāt pēc apmaksas**.

1. Dodieties uz **Projektu pārvaldība un uzskaite** \> **Vaicājumi un pārskati** \> **Ieturējumu pieprasījumi** \> **Kreditora rēķins ar apmaksāt pēc apmaksas**.
2. Lapā **Kreditora rēķins ar apmaksāt pēc apmaksas** meklēšanas laukā ievadiet vērtības, lai atrastu kreditora rēķinu, ko vēlaties pārskatīt, un pēc tam atlasiet **Meklēt**.
3. Kopsavilkuma cilnē **Kreditora rēķina rindas** atlasiet rindas, kuras vēlaties mainīt.
4. Ja **Apmaksāt pēc apmaksas** nosacījumi ir izpildīti rēķina rindai, atlasiet **Palaist kreditora maksājumu**. **Apmaksāt pēc apmaksas** opcija tiek notīrīta un lauka vērtība **Gatavs maksājumam** tiek mainīta uz **Jā**.
