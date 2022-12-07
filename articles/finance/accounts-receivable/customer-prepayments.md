---
title: Debitora priekšapmaksas
description: Šajā rakstā ir izskaidrots, kā iestatīt un apstrādāt debitoru priekšapmaksu (ko sauc arī par debitoru depozītiem).
author: twheeloc
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, LedgerJournalTransCustPaym, CustParameters
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f085d45895530aaf0a16439f62dfc13b27da84b6
ms.sourcegitcommit: fb9b6969218f2b82f0a4c72bfad75387fe00395c
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/22/2022
ms.locfileid: "9799438"
---
# <a name="customer-prepayments"></a>Debitora priekšapmaksas

[!include [banner](../includes/banner.md)]

Debitoru priekšapmaksas tiek izmantotas, kad saņemat maksājumu no debitora, bet nav rēķina, ar kuru maksājumu var nosegt. Šie maksājumu veidi tiek saukti arī par debitoru depozītiem.

Debitoru priekšapmaksu iestatīšanas un darba process sastāv no šādiem pamata soļiem.

1. Izveidojiet debitoru grāmatošanas metodi priekšapmaksām.
2. Iestatiet parametru **Grāmatošanas profils priekšapmaksas žurnāla dokumenta summā**.
3. Izveidojiet debitoru maksājumu žurnālu un atzīmējiet izvēles **rūtiņu Priekšapmaksas** žurnāla dokuments katrā rindā.
4. Grāmatojiet debitoru maksājumu žurnālu.
5. Pēc rēķina ģenerēšanas nosedziet priekšapmaksu ar to, izmantojot lapu **Nosegt atvērtos darījumus**.

## <a name="create-a-customer-posting-profile-for-prepayments"></a>Izveidojiet debitoru grāmatošanas metodi priekšapmaksām

Parasti, kad pieņemat priekšapmaksas vai depozītus no saviem debitoriem pirms preču vai pakalpojumu piegādes, vai pirms rēķins eksistē jūsu sistēmā, jūs vēlaties reģistrēt skaidru naudu kā saistības nevis kā līdzekļus jūsu kontu plānā. Tomēr šo summu ierakstīšanas prasības jūsu virsgrāmatā var atšķirties atkarībā no valsts vai reģiona. Tāpēc noteikti konsultējieties ar saviem grāmatvežiem par visiem spēkā esošajiem vietējiem likumiem.

Parasti grāmatošanas metodes izveides process, ko var izmantot priekšapmaksām, ir tāds pats process kā citu grāmatošanas metožu veidošanai. Galvenā starpība ir galvenais konts, kas atlasīts laukā **Summu konts**. Plašāku informāciju skatiet šeit: [Debitoru grāmatošanas profili](customer-posting-profiles.md).

## <a name="define-parameters-for-customer-prepayments"></a>Definēt debitoru priekšapmaksu parametrus

Pastāv divi galvenie debitoru parādu parametri, kas jāņem vērā, konfigurējot sistēmu debitoru priekšapmaksām. Veiciet tālāk norādītās darbības, lai konfigurētu parametrus.

1. Dodieties uz sadaļu **Debitoru parādi \> Iestatīšana \> Debitoru parādu parametri**.
2. Nav obligāti: cilnē **Virsgrāmata un PVN**, kopsavilkuma cilnē **Maksājums** iestatiet **Priekšapmaksas žurnāla dokumenta summas PVN** opciju uz **Jā**.
3. Laukā **Grāmatošanas metode ar priekšapmaksas žurnāla dokumentu** atlasiet debitora grāmatošanas metodi, ko izmantot, grāmatojot debitoru priekšapmaksas.
4. Aizvērt lapu.

## <a name="create-customer-prepayment-vouchers"></a>Izveidot debitoru priekšapmaksas dokumentus

Veidojot debitoru maksājumu žurnālu, katrai priekšapmaksai jums jāiestata **Priekšapmaksas žurnāla dokumenta** opcija uz **Jā** lapā **Debitoru maksājumu žurnāls**. Izpildiet tālāk aprakstītās darbības, lai izveidotu debitoru priekšapmaksu.

1. Dodieties uz **Debitori \> Maksājumi \> Debitora maksājumu žurnāls**.
2. Atlasiet **Jauns**, lai izveidotu žurnālu.
3. Laukā **Nosaukums** atlasiet izmantojamo žurnāla nosaukumu.

    > [!IMPORTANT]
    > Ja iepriekšējās procedūras ietvaros iestatāt **Priekšapmaksas žurnāla dokumenta summas PVN** opciju uz **Jā**, ir jāatlasa žurnāla nosaukums, kurā ir atlasīts parametrs **Summa iekļauj PVN**. 

4. pēc izvēles: Laukā **Apraksts** ievadiet detalizētu aprakstu.
5. Atlasiet **Rindas**.
6. Ja tukša rinda nepastāv, atlasiet **Jauns**, lai izveidotu rindu.
7. Laukā **Datums** ievadiet datumu, kad ir jāgrāmato priekšapmaksa.
8. Laukā **Uzņēmums** atlasiet klientu priekšapmaksai.
9. Pēc izvēles: laukā **Apraksts** ievadiet detalizētu darījuma aprakstu.
10. Laukā **Kredīts** ievadiet priekšapmaksas summu.
11. Laukā **Korespondējošā konts** atlasiet kontu, uz kuru veikt priekšapmaksu. Piemēram, atlasiet banku vai galveno kontu, kurā grāmatot maksājumu.
12. Laukā **Maksāšanas veids** atlasiet debitora maksāšanas veidu.
13. Cilnē **Maksājums** iestatiet **Priekšapmaksas žurnāla dokumenta** opciju uz **Jā**.
14. Atkārtojiet no 7. līdz 13. solim katrai papildu priekšapmaksai, kas ir jāiegrāmato.
15. Atlasiet **Grāmatot**, lai pabeigtu žurnāla gatavošanu.

## <a name="settle-prepayments-with-invoices"></a>Priekšapmaksas nosedziet ar rēķiniem

Varat izmantot **Debitoru maksājumu** darbvietu, lai viegli atrastu un apmaksātu maksājumus, kas nav pilnībā nosegti.

1. **Sākuma** informācijas panelī atlasiet elementu **Debitoru maksājumi**.
2. Sadaļas **Debitora darījumi** cilnē **Nenosegtie maksājumi** meklējiet un atlasiet sedzamo maksājumu.
3. Atlasiet **Segt darījumus**.
4. Atzīmējiet **rēķina** izvēles rūtiņu un maksājumu, kas tiks segts.
5. Atlasiet **Grāmatot**.

Papildinformāciju par to, kā nosegt atvērtos darījumus, skatiet sadaļā [Norēķinu pārskats](/dynamics365/finance/cash-bank-management/settlement-overview).
