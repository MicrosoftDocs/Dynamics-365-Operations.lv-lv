---
title: "Konvertēt grāmatvedības vai pārskatu valūtas"
description: "Uzņēmumam, kam ir jānomaina uzskaites valūta vai pārskata valūta, ir divas iespējas."
author: aprilolson
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 78223
ms.assetid: 31c56f9a-9c64-40a2-90e3-1969a760614b
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ad840f4ed2cf27615e699a13fcd8be7f3c2cd5c8
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="convert-accounting-or-reporting-currencies"></a>Konvertēt grāmatvedības vai pārskatu valūtas

[!include [banner](../includes/banner.md)]

Uzņēmumam, kam ir jānomaina uzskaites valūta vai pārskata valūta, ir divas iespējas. Pirmā iespēja ir izveidot jaunu uzņēmumu un sākt visu no jauna. Otra iespēja ir veikt uzskaites un pārskata valūtas konvertēšanu. Tas ir ļoti ilglaicīgs process, kas maina katru sistēmas darbību. Pirms procesa sākšanas ir nepieciešami arī daži iestatījumi.

## <a name="preparing-the-legal-entity-for-currency-conversion"></a>Juridiskas personas sagatavošana valūtas konvertēšanai
Pirms konvertēt juridiskas personas valūtu ir jāatgriež ārvalstu valūtas pārvērtēšanas summas debitoru un kreditoru kontos un jānoslēdz iepriekšējie finanšu gadi. Ir arī jāsagatavo datu bāze konvertēšanai, un pēc tam jāveic nepieciešamās izmaiņas tās juridiskās personas kontā, kurai tiek veikta valūtas konvertēšana. Pēc valūtas konvertēšanas paveikšanas ir jāpabeidz dažas papildu procedūras. Jums jāsaskaņo noapaļošanas atšķirības konvertētajās summas, jāpārrēķina biznesa statistika, jāreģistrē virsgrāmatas darbības, jāierobežo piekļuve konvertēšanas rīkam un jāpārvērtē klientu un piegādātāju kontu ārvalstu valūtas summa.

## <a name="setting-up-accounts-for-automatic-transactions"></a>Automātisko darījumu kontu iestatīšana
Valūtu konvertēšanas laikā ieguvumi, zaudējumi vai sīknaudas starpības tiek grāmatotas kontiem, kas definēti lapā **Automātisko darījumu konti**. Pirms konvertēšanas sākšanas galvenie konti jāpiešķir šādu veidu darbībām.

-   Peļņa no uzskaites valūtas konvertēšanas
-   Zaudējumi no uzskaites valūtas konvertēšanas
-   Sīknaudas starpība uzskaites valūtā
-   Sīknaudas starpība pārskata valūtā
-   Rezultāts gada beigās

## <a name="posting-rounding-differences-and-sum-recalculations"></a>Summu noapaļošanas un pārrēķināšanas atšķirību grāmatošana
Šajā informācijā izskaidrots, kā var rasties noapaļošanas atšķirības.

-   Ja preču cenas ir konvertētas uz 0 (nulli), tiek ģenerēts pārskats, kurā parādīts preces numurs, moduļa veids, cena pirms konvertēšanas un vienība.
-   Noapaļošanas atšķirības starp PVN un Virsgrāmatu tiek grāmatotas Virsgrāmatas žurnālā.
-   Ārvalstu valūtas pārvērtēšanas summas tiek pārrēķinātas, un tiek pārrēķinātas arī debitoru un kreditoru darbību summas.
-   Debitoru un kreditoru norēķinu ieraksti tiek izveidoti noapaļošanas atšķirībām par katru debitora un kreditora darbību.
-   Debitoru un kreditoru noapaļošanas atšķirības tiek grāmatotas Virsgrāmatas žurnālā.
-   Tiek pārrēķinātas nosegto izmaksu summas un izmaksu korekcijas summas slēgtās krājumu darbībās.
-   Krājumu vadības noapaļošanas atšķirības tiek grāmatotas Virsgrāmatas žurnālā.
-   Tiek pārrēķināti rīcībā esošie krājumi.
-   Tiek pārrēķinātas kopsummas Virsgrāmatas žurnālos.
-   Tiek pārrēķinātas Virsgrāmatas slēguma lapas.
-   Tiek pārrēķinātas Virsgrāmatas bilances.
-   Virsgrāmatas noapaļošanas atšķirības tiek grāmatotas Virsgrāmatas žurnālā.
-   Tiek pārrēķinātas Virsgrāmatas sākuma darbības.
-   Tiek pārrēķināta Virsgrāmatas summu gala summa.

Ja veicat konvertāciju uz jaunu virsgrāmatas uzskaites valūtu un kopējo summu pārrēķināšanas vai noapaļošanas atšķirību grāmatošanas laikā radusies kļūda, jāaizver lapa **Virsgrāmatas uzskaites valūtas konvertēšana**. Kopējās summas tad tiek pārrēķinātas, un noapaļošanas atšķirības — grāmatotas.

## <a name="processing-the-currency-conversion"></a>Valūtas konvertēšanas veikšana
Sākot valūtas konvertēšanu, visiem lietotājiem ir jāizrakstās no sistēmas. Jums jādefinē jauna virsgrāmata vai pārskata valūta un maiņas kursi. Noklikšķinot uz **Labi**, process tiek palaists un atjaunina ikvienu sistēmas darbību. Valūtas konvertēšana ir ilgstošs process. Kad tas ir pabeigts, redzēsit, ka grāmatvedības vai pārskata valūta ir atjaunināta lapā **Virsgrāmata**.

## <a name="completing-the-currency-conversion"></a>Valūtas konvertēšanas pabeigšana
Pēc konvertēšanas vēlreiz ir jāģenerē visi saskaņošanas pārskati, lai pārliecinātos, ka visas konvertētās summas ir pareizas.

-   Ja virsgrāmatas uzskaites valūtas konvertēšana rada noapaļošanas atšķirības, šīs atšķirības netiek grāmatotas, izmantojot dokumentu, kurā ir radusies noapaļošanas atšķirība. Tā vietā atšķirības tiek grāmatota, lietojot konvertēšanas grāmatojumiem ievadīto dokumentu. Pēc konvertēšanas visos pārskatos, kuri tiek pārbaudīti pēc dokumenta un datuma, tiks iekļautas šīs noapaļošanas atšķirības. Šī darbība ir pareiza, un to var ignorēt.
-   Ja kreditora un debitora saskaņošanas pārskati parāda atšķirīgu daudzumu kopsummas rindā un pirms konvertēšanas nav daudzuma atšķirību, atšķirīgais daudzums jāiegrāmato. Konts ir debitoru un kreditoru kopsavilkuma konts. Korespondējošais konts ir konvertēšanas zaudējumu vai konvertēšanas peļņas virsgrāmatas konts.

Kad visi virsgrāmatas darbību žurnāli izdzēsti, varat ierakstiet žurnālā virsgrāmatas darbības. Noklikšķiniet uz **Virsgrāmata** &gt; **Periodiskās darbības** &gt; **Žurnāli** &gt; **Reģistrācija žurnālā**. Pēc valūtas konvertēšanas varat pārvērtēt ārvalstu valūtas summas, ja pārvērtēšana ir nepieciešama. Pārvērtējiet ārvalstu valūtas summas, atlasot opciju **Standarta** laukā **Metode**.

Plašāku informāciju skatiet šeit: [Žurnālā grāmatoto ierakstu reģistrēšana žurnālā](tasks/journalize-posted-journal-entries.md).


